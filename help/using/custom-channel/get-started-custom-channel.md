---
title: Erste Schritte mit benutzerdefinierten Kanälen
description: Erfahren Sie, wie  [!DNL Journey Optimizer]'s Channel Builder to bring any outbound messaging channel into [!DNL Journey Optimizer]  in Kampagnen, Journey und orchestrierten Kampagnen verwendet und verwendet werden können.
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 5%

---


# Erste Schritte mit benutzerdefinierten Kanälen {#get-started-custom-channel}

>[!AVAILABILITY]
>
>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

<!--Multilingual support, business rules enforcement, and [!DNL Adobe Experience Decisioning] integration are planned for a future release.-->

Mit der Funktion **Benutzerdefinierte Kanäle** von [!DNL Journey Optimizer] können Sie jeden ausgehenden Kanal in [!DNL Journey Optimizer] importieren, damit Sie ihn in Kampagnen, Journey und orchestrierten Kampagnen verwenden können - genau wie in jedem nativen Kanal. Mit dem **Channel Builder** können Administratoren neue Kanäle erstellen und konfigurieren, ohne dass das Engineering involviert ist, und Marketing-Experten können sofort damit beginnen, sie für die Kommunikation mit Kunden zu verwenden.

## Welches Problem löst es? {#why-custom-channels}

[!DNL Journey Optimizer] unterstützt nativ E-Mail, SMS, Push-Benachrichtigungen, WhatsApp, LINE und andere Kanäle. Viele Unternehmen verwenden jedoch Messaging-Plattformen, die nicht nativ integriert sind - wie z. B. WeChat, Kakao Talk, Messenger oder ein externer Anbieter - und möchten sie in [!DNL Journey Optimizer] für die Orchestrierung und Kampagnenerstellung verwenden, während sie weiterhin mit ihrem eigenen Anbieter liefern.

<!--TBC: Another use case is when organizations have a legacy messaging gateway that exposes an HTTP endpoint, and they want to use it in [!DNL Journey Optimizer] without having to build a custom integration.-->

Benutzerdefinierte Kanäle füllen diese Lücke: Sie ermöglichen es Ihnen, jeden ausgehenden HTTP-Endpunkt als vollständigen [!DNL Journey Optimizer] zu verwenden, wodurch Folgendes freigeschaltet wird:

* **Vollständige Kanalfunktionen** - Optimierung (Inhaltsexperimentierung und Zielgruppenbestimmung), vorkonfiguriertes Reporting und Überwachung, Durchsetzung von Einverständnis und Governance und Ausdrucksfragmente. <!--Multilingual and business rules are planned for a future release.-->
* **Einheitliche Orchestrierung** - Verwalten Sie alle Messaging-Kanäle an einem Ort, unabhängig vom zugrunde liegenden Versandanbieter.
* **Einrichtung ohne Code** - Administratoren konfigurieren den Kanal über die Channel Builder-Benutzeroberfläche. Es ist kein benutzerdefinierter Code oder technischer Aufwand erforderlich.

## Benutzerdefinierter Kanal im Vergleich zu benutzerdefinierten Aktionen {#custom-channel-vs-custom-action}

Wenn Sie zuvor [benutzerdefinierte Aktionen](../action/action.md) in [!DNL Journey Optimizer] Journey verwendet haben, können benutzerdefinierte Kanäle andere Anwendungsfälle behandeln.

**Verwenden Sie benutzerdefinierte Kanäle** wenn Sie Nachrichten an Endbenutzer über eine Plattform senden müssen, die von [!DNL Journey Optimizer] nicht unterstützt wird, z. B. WeChat, Kakao Talk oder ein benutzerdefiniertes Messaging-Gateway. Benutzerdefinierte Kanäle sind in -Kampagnen, -Journey und -orchestrierten Kampagnen und im Support verfügbar:

* Vollständige Personalisierung über den Personalisierungseditor, ähnlich wie bei nativen ausgehenden Kanälen
* Bild-/Formular-Payload-Editor, Vorschau und Testversand
* Inhaltsexperiment und Targeting
* Vorkonfiguriertes Reporting und Monitoring
* Mehrere API-Anmeldeinformationen und Kanalkonfigurationen
* RBAC/ABAC

Benutzerdefinierte Kanäle unterstützen POST als einzige HTTP-Methode.

**Verwenden Sie benutzerdefinierte Aktionen** wenn Sie Daten aus einem externen System - z. B. einem Callcenter, einer Protokollierungsplattform oder einer Offline-Datenbank - abrufen oder Informationen an ein externes System senden müssen, um einen Schritt innerhalb eines Journey zu machen. Benutzerdefinierte Aktionen sind nur in Journey verfügbar und unterstützen GET-, PUT- und POST-Methoden.

<!--
| | Custom Action | Custom Channel |
| --- | --- | --- |
| **Primary use case** | Retrieve data from or send information to external systems (call centers, offline systems, logging) | Send messages to end users through channels not natively supported in [!DNL Journey Optimizer] |
| **Available in** | Journeys only | Campaigns, journeys, and orchestrated campaigns |
| **Supported HTTP methods** | GET, PUT, POST | POST only |
| **Full personalization (PE)** | No | Yes, through the personalization editor, similar to native outbound channels |
| **Visual/form editor** | No | Yes |
| **Preview and proof** | No | Yes |
| **Content experimentation** | No | Yes |
| **Targeting** | No | Yes |
| **OOTB Reporting** | Yes | Yes |
| **Multiple API credentials and channel configurations** | No | Yes |
| **RBAC/ABAC** | No | Yes |
-->

>[!TIP]
>
>Als allgemeine Empfehlung sollten Sie benutzerdefinierte Kanäle für Kanal-Anwendungsfälle verwenden, in denen Sie Nachrichten an Endbenutzer senden. Für andere Connector-ähnliche Anwendungsfälle, die in Journey benötigt werden, z. B. das Abrufen von Daten oder das Auslösen externer Systeme, können Sie weiterhin benutzerdefinierte Aktionen verwenden.

## Anwendungsszenarien {#use-cases}

Benutzerdefinierte Kanäle eignen sich ideal für:

* **Nicht unterstützte Messaging-Plattformen** - Kanäle wie WeChat, Kakao Talk, Messenger, Telegram oder regionale Messaging-Services, die keinen nativen [!DNL Journey Optimizer]-Kanal haben.
* **Benutzerdefinierte Versandanbieter** Organisationen, die in einen externen Anbieter investiert haben, den sie weiterhin für den Nachrichtenversand verwenden möchten, aber [!DNL Journey Optimizer] für Orchestrierung, Personalisierung und Kampagnen-Management bevorzugen.
* **Legacy-Kanäle** - proprietäre oder veraltete Messaging-Gateways, die einen HTTP-Endpunkt bereitstellen.
* **Branchenspezifische Kanäle** - Sicheres Messaging für das Gesundheitswesen, Warnsysteme für Banken oder Benachrichtigungsdienste der Regierung.

## Funktionsweise {#how-it-works}

Die Einrichtung und Verwendung eines benutzerdefinierten Kanals folgt den wichtigsten Schritten unten:

1. **Konfigurieren** (Admin): Ein Administrator erstellt einen benutzerdefinierten Kanal im **Channel Builder**, definiert den Endpunkt, die Authentifizierung, die Drosselungsrichtlinie und die Payload-Struktur der Nachricht. Anschließend wird eine Kanalkonfiguration erstellt und mit dem benutzerdefinierten Kanal verknüpft. [Weitere Informationen](configure-custom-channel.md)
1. **Erstellen** (Marketing-Experte): Ein Marketing-Experte fügt den benutzerdefinierten Kanal einer Journey, Kampagne oder orchestrierten Kampagne hinzu, wählt eine Kanalkonfiguration aus und verfasst die Nachrichten-Payload mit dem Personalisierungseditor von [!DNL Journey Optimizer]. [Weitere Informationen](create-custom-experience.md)
1. **Senden** - Wenn ein Profil qualifiziert ist, sendet [!DNL Journey Optimizer] die personalisierte Payload an den konfigurierten Endpunkt. Das externe System verarbeitet den Aufruf und sendet die Nachricht.
1. **Überwachen** (Administrator/Marketer) - Administratoren und Marketer können die Leistung und Zuverlässigkeit des benutzerdefinierten Kanals über die Berichts- und Überwachungs-Dashboards von [!DNL Journey Optimizer] überwachen. [Weitere Informationen](monitor-custom-channel.md)

<!--
## Next steps {#next-steps}

* Review the prerequisites and permissions before setting up your first custom channel. [Learn more](custom-channel-prerequisites.md)
* Configure your first custom channel using the Channel Builder. [Learn more](custom-channel-configuration.md)
* Create a custom channel experience in a journey or campaign. [Learn more](create-custom-experience.md)
-->
