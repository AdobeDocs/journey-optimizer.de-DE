---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren des Live-Aktivitätskanals
description: Erfahren Sie, wie Sie Ihre Adobe Experience Platform Mobile SDK-Integration konfigurieren
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 1%

---


# Live-Aktivitätsintegration mit Adobe Experience Platform Mobile SDK {#mobile-live-config-sdk}

>[!BEGINSHADEBOX]

* [Erste Schritte mit Live-Aktivitäten](get-started-mobile-live.md)
* [Konfiguration der Live-Aktivität](mobile-live-configuration.md)
* **[Live-Aktivitätsintegration mit Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**
* [Erstellen einer Live-Aktivität](create-mobile-live.md)
* [Häufig gestellte Fragen](mobile-live-faq.md)
* [Live-Kampagnenbericht](../reports/campaign-global-report-cja-activity.md)


>[!ENDSHADEBOX]

Adobe Experience Platform Mobile SDK bietet integrierte Unterstützung für Live-Aktivitäten von Apple. Dadurch kann Ihre App dynamische Aktualisierungen in Echtzeit direkt auf dem Sperrbildschirm und auf Dynamic Island anzeigen, ohne die App zu öffnen.

1. [Erforderliche Module importieren](#import)

   Die folgenden Module importieren: **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]**.

1. [Attribute definieren](#attributes)

   `LiveActivityAttributes` Sie die Attribute `LiveActivityData` und `ContentState` ein.

1. [Live-Aktivitäten registrieren](#register)

   Verwenden Sie `Messaging.registerLiveActivity()` nach der Initialisierung von SDK.

1. [Widget-Konfiguration erstellen](#widget)

   Implementieren Sie `ActivityConfiguration` sowohl für den Sperrbildschirm als auch für die Dynamic Island-Schnittstelle.

1. [Lokales Starten einer Live-Aktivität (optional)](#local)

   Live-Aktivitäten können entweder remote über Journey Optimizer oder lokal im Anwendungs-Code initiiert werden.

1. [Hinzufügen von Debugging-Unterstützung (optional)](#debug)

   Implementieren von `LiveActivityAssuranceDebuggable` für Assurance.

Stellen Sie sicher, dass die folgenden Mindestversionen installiert sind, um eine korrekte Konfiguration und Kompatibilität zu gewährleisten.

>[!BEGINSHADEBOX]

**Voraussetzungen:**

* **iOS:**
   * **iOS16.1 oder höher**: Grundlegende Funktionen für Live-Aktivitäten
   * **iOS 17.2+**: Push-to-Start-Unterstützung
   * **iOS 18+**: Unterstützung für Broadcast-Kanäle
* **Xcode:** 14.0 oder höher
* **Swift:** 5.7 oder höher
* **Abhängigkeiten:** AEPCore, AEPMessaging, AEPMessagingLiveActivity, ActivityKit

>[!ENDSHADEBOX]

## Schritt 1: Erforderliche Module importieren {#import}

Zunächst müssen Sie die folgenden Module importieren: **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]**.

```swift
import AEPMessaging
import AEPMessagingLiveActivity
import ActivityKit
```

## Schritt 2: Definieren Sie Ihre Live-Aktivitätsattribute {#attributes}

Erstellen Sie eine Struktur, die dem `LiveActivityAttributes` entspricht. Dadurch werden sowohl die statischen Daten als auch der dynamische Inhaltsstatus für Ihre Live-Aktivität definiert.

Zu den wichtigsten Komponenten gehören:

* **`liveActivityData`** (erforderlich), das Adobe Experience Platform-spezifische Daten enthält.
   * Für einzelne Benutzer: Verwenden Sie `LiveActivityData(liveActivityID: "unique-id")`
   * Für Übertragung: `LiveActivityData(channelID: "channel-id")` verwenden

* Statische Attribute, benutzerdefinierte Eigenschaften, die für Ihren Anwendungsfall spezifisch sind, z. B. `restaurantName`.

* **`ContentState`** definiert dynamische Daten, die während des Lebenszyklus der Live-Aktivität aktualisiert werden können. Sie muss `Codable` und `Hashable` entsprechen.

* `LiveActivityOrigin` Auflistung gibt an, ob eine Aktivität lokal in der App oder remote über eine Push-to-Start-Benachrichtigung initiiert wurde, die in iOS 17.2 und höher unterstützt wird. Dieser Wert ermöglicht es dem SDK, bei der Datenerfassung zwischen lokal initiierten und remote ausgelösten Live-Aktivitäten zu unterscheiden.

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

Sie können auch mehrere Live-Aktivitätstypen für Ihre App registrieren:

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(AirplaneTrackingAttributes.self)
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
    Messaging.registerLiveActivity(GameScoreLiveActivityAttributes.self)
}
```

## Schritt 3: Live-Aktivitäten registrieren {#register}

Registrieren Sie Ihre Live-Aktivitätstypen in Ihrem `AppDelegate` nach der Initialisierung von SDK. So können Sie:

* Aktiviert die automatische Push-to-Start-Token-Erfassung (iOS 17.2+)
* Erfasst automatisch Aktualisierungstoken für Live-Aktivitäten
* Ermöglicht Lebenszyklus-Management und Ereignis-Tracking

**Beispiel für eine Live-Aktivität eines Lebensmittelversands:**

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
}
```

## Schritt 4: Erstellen von Live-Aktivitäts-Widgets {#widgets}

Live-Aktivitäten werden über Widgets angezeigt. Sie müssen ein Widget-Bundle und eine Konfiguration erstellen:

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

## Schritt 5: Live-Aktivität lokal starten (optional) {#local}

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

## Schritt 6: Hinzufügen von Debugging-Unterstützung (optional) {#debug}

Bei Bedarf können Sie Live-Aktivitätsschemata in Adobe Assurance debuggen:

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


