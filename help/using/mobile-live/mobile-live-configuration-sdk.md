---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren des Kanals für Live-Aktivitäten
description: Informationen zum Konfigurieren Ihrer Adobe Experience Platform Mobile SDK-Integration
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 02ca7c8e-105a-4e77-9aad-2381904255d0
source-git-commit: 6b4e3a6c32d24861f1ea8df54fc2e4fbb19d0ce7
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 100%

---

# Integration von Live-Aktivitäten mit Adobe Experience Platform Mobile SDK {#mobile-live-config-sdk}


Das Adobe Experience Platform Mobile SDK bietet integrierte Unterstützung für Live-Aktivitäten von Apple. Dadurch kann Ihre App dynamische Aktualisierungen in Echtzeit direkt auf dem Sperrbildschirm und auf der Dynamic Island anzeigen, ohne dass die App geöffnet werden muss.

1. [Importieren erforderlicher Module](#import)

   Importieren Sie die folgenden Module: **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]**.

1. [Definieren von Attributen](#attributes)

   Nehmen Sie eine Anpassung an `LiveActivityAttributes` vor und schließen Sie die Attribute `LiveActivityData` und `ContentState` ein.

1. [Registrieren von Live-Aktivitäten](#register)

   Verwenden Sie `Messaging.registerLiveActivity()` nach der SDK-Initialisierung.

1. [Erstellen einer Widget-Konfiguration](#widget)

   Implementieren Sie `ActivityConfiguration` sowohl für den Sperrbildschirm als auch für die Dynamic Island-Oberfläche.

1. [Lokales Starten einer Live-Aktivität (optional)](#local)

   Live-Aktivitäten können entweder remote über Journey Optimizer oder lokal im Anwendungs-Code initiiert werden.

1. [Hinzufügen von Debugging-Unterstützung (optional)](#debug)

   Implementieren Sie `LiveActivityAssuranceDebuggable` für Assurance.

Stellen Sie sicher, dass mindestens die folgenden Versionen installiert sind, um eine korrekte Konfiguration und Kompatibilität zu gewährleisten.

>[!BEGINSHADEBOX]

**Voraussetzungen:**

* **iOS:**
   * **iOS 16.1 oder höher**: Grundlegende Funktionen von Live-Aktivitäten
   * **iOS 17.2 oder höher**: Push-to-Start-Unterstützung
   * **iOS 18 oder höher**: Unterstützung für Übertragungskanäle
* **Xcode:** 14.0 oder höher
* **Swift:** 5.7 oder höher
* **Abhängigkeiten:** AEPCore, AEPMessaging, AEPMessagingLiveActivity, ActivityKit

>[!ENDSHADEBOX]

## Schritt 1: Importieren der erforderlichen Module {#import}

Zunächst müssen Sie die folgenden Module importieren: **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]**.

```swift
import AEPMessaging
import AEPMessagingLiveActivity
import ActivityKit
```

## Schritt 2: Definieren Ihrer Live-Aktivitätsattribute {#attributes}

Erstellen Sie eine Struktur, die dem Protokoll `LiveActivityAttributes` entspricht. Dadurch werden sowohl die statischen Daten als auch der Status der dynamischen Inhalte für Ihre Live-Aktivität definiert.

Zu den wichtigsten Komponenten gehören:

* **`liveActivityData`** (erforderlich), enthält Adobe Experience Platform-spezifische Daten.
   * Für einzelne Benutzende: Verwenden Sie `LiveActivityData(liveActivityID: "unique-id")`
   * Für Übertragung: Verwenden Sie `LiveActivityData(channelID: "channel-id")`

* Statische Attribute, benutzerdefinierte Eigenschaften, die für Ihren Anwendungsfall spezifisch sind, z. B. `restaurantName`.

* **`ContentState`** definiert dynamische Daten, die während des Lebenszyklus der Live-Aktivität aktualisiert werden können. Sie müssen `Codable` und `Hashable` entsprechen.

* Die Auflistung `LiveActivityOrigin` gibt an, ob eine Aktivität lokal in der App oder remote über eine Push-to-Start-Benachrichtigung initiiert wurde; wird in iOS 17.2 und höher unterstützt. Dieser Wert ermöglicht es dem SDK, bei der Datenerfassung zwischen lokal initiierten und remote ausgelösten Live-Aktivitäten zu unterscheiden.

**Beispiele**

```swift
@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
    // Mandatory: AEP Integration Data
    var liveActivityData: LiveActivityData
    
    // Static Attributes: Custom properties that do not change
    var restaurantName: String
    
    // Dynamic Content State: Data that can be updated
    struct ContentState: Codable, Hashable {
        var orderStatus: String
    }
}
```

```swift
@available(iOS 16.1, *)
public struct LiveActivityData: Codable {
    /// Unique identifier for broadcast Live activity channels
    public let channelID: String?
     
    /// Unique identifier for individual Live activities
    public let liveActivityID: String?
     
    /// Indicates local vs remote creation
    public let origin: LiveActivityOrigin?
     
    // Initializers
    public init(channelID: String)        // For broadcast Live activities
    public init(liveActivityID: String)   // For individual Live activities
}
```

Sie können auch mehrere Typen an Live-Aktivitäten für Ihre App registrieren:

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(AirplaneTrackingAttributes.self)
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
    Messaging.registerLiveActivity(GameScoreLiveActivityAttributes.self)
}
```

## Schritt 3: Registrieren von Live-Aktivitäten {#register}

Registrieren Sie die Typen Ihrer Live-Aktivitäten in `AppDelegate` nach der SDK-Initialisierung. Das ermöglicht Ihnen Folgendes:

* Aktiviert die automatische Push-to-Start-Token-Erfassung (iOS 17.2 und höher)
* Erfasst automatisch Aktualisierungs-Token für Live-Aktivitäten
* Ermöglicht Lebenszyklus-Management und Ereignis-Tracking

**Beispiel für eine Live-Aktivität eines Lebensmittelversands:**

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
}
```

## Schritt 4: Erstellen von Widgets für Live-Aktivitäten {#widgets}

Live-Aktivitäten werden über Widgets angezeigt. Sie müssen ein Widget-Paket und eine Widget-Konfiguration erstellen:

**Beispiel für eine Live-Aktivität eines Lebensmittelversands:**

```swift
@main
struct FoodDeliveryWidgetBundle: WidgetBundle {
    var body: some Widget {
        FoodDeliveryLiveActivityWidget()
    }
}

@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityWidget: Widget {
    var body: some WidgetConfiguration {
        ActivityConfiguration(for: FoodDeliveryLiveActivityAttributes.self) { context in
            // Lock Screen UI
            VStack {
                Text("Order from \(context.attributes.restaurantName)")
                Text("Status: \(context.state.orderStatus)") // possible status may include "Ordered", "Order accepted", "Preparing", "On the Way","Delivered"
            }
        } dynamicIsland: { context in
            // Dynamic Island UI
            DynamicIsland {
                // Expanded UI
            } compactLeading: {
                // Compact leading UI
            } compactTrailing: {
                // Compact trailing UI
            } minimal: {
                // Minimal UI
            }
        }
    }
}
```

## Schritt 5: Lokales Starten einer Live-Aktivität (optional) {#local}

Journey Optimizer kann Live-Aktivitäten zwar remote starten, Sie können sie aber auch lokal starten:

**Beispiel für eine Live-Aktivität eines Lebensmittelversands:**

```swift
let attributes = FoodDeliveryLiveActivityAttributes(
    liveActivityData: LiveActivityData(liveActivityID: "order123"),
    restaurantName: "Pizza Palace"
)

let contentState = FoodDeliveryLiveActivityAttributes.ContentState(
    orderStatus: "Ordered"
)

let activity = try Activity<FoodDeliveryLiveActivityAttributes>.request(
    attributes: attributes,
    contentState: contentState,
    pushType: .token
)
```

## Schritt 6: Hinzufügen von Debugging-Unterstützung (optional) {#debug}

Bei Bedarf können Sie Schemata von Live-Aktivitäten in Adobe Assurance debuggen:

**Beispiel für eine Live-Aktivität eines Lebensmittelversands:**

```swift
@available(iOS 16.1, *)
extension FoodDeliveryLiveActivityAttributes: LiveActivityAssuranceDebuggable {
    static func getDebugInfo() -> (attributes: FoodDeliveryLiveActivityAttributes, state: ContentState) {
        return (
            FoodDeliveryLiveActivityAttributes(
                liveActivityData: LiveActivityData(liveActivityID: "debug-order-123"),
                restaurantName: "Debug Restaurant"
            ),
            ContentState(orderStatus: "Ordered")
        )
    }
}
```
