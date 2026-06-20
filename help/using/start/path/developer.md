---
title: Erste Schritte für Entwickler
description: Hier erfahren Entwickler mehr über die Arbeit mit Journey Optimizer.
feature: Get Started
role: Developer
level: Intermediate
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
TQID: https://experienceleague.adobe.com/7fRI-CPkIeBAPjtXmDgFdyNKgB4WwEc01yKrGUXnc3U
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: d08afb72-92f6-4856-88e3-11ec34313c2fid: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b4dd41a7-ccf8-4e9d-918e-acaab534a307id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: d3cdead0-685a-4489-9250-4bb709942f66id: e9001ce2-5245-4a8e-8601-dd958009072fid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: e5e8545bef077219ff91428c9048c978184b57ec
workflow-type: tm+mt
source-wordcount: 3456
ht-degree: 54%

---

# Erste Schritte für Entwickelnde {#get-started-developers}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Implementieren Sie die SDKs, Ereignis-Streaming, benutzerdefinierten Aktionsendpunkte und APIs, die Ihre Programme mit Adobe Journey Optimizer verbinden, damit Ihre Journey mit Live-Daten arbeiten können.

>[!ENDSHADEBOX]

Als **Entwicklerin bzw. Entwickler** sind Sie für die Implementierung und Integration von [!DNL Adobe Journey Optimizer] in Ihre Anwendungen und Systeme verantwortlich. Sie können mit der Arbeit mit [!DNL Adobe Journey Optimizer] beginnen, sobald Ihnen [Systemadmin](administrator.md) und [Dateningenieurin bzw. -ingenieur](data-engineer.md) Zugriff auf Ihre Umgebung gewährt und diese vorbereitet haben.

>[!NOTE]
>
>**Implementierungsreihenfolge:** [Administrator](administrator.md) → [Datentechniker](data-engineer.md) → → Sie sind hier: **Entwickler** [Marketer](marketer.md)
>
>Stellen Sie [, dass (Datenschemata und Ereignisse](data-engineer.md) konfiguriert sind, bevor Sie Ihre Mobile- und Web-Integrationen implementieren.

## Ihre Rolle im Journey Optimizer-Ökosystem

Während andere Team-Mitglieder Journey Optimizer über die Benutzeroberfläche konfigurieren, konzentrieren Sie sich auf:

* **Implementieren von SDKs** in Mobile- und Web-Anwendungen
* **Senden von Ereignissen** von Ihren Anwendungen zum Auslösen von Journeys
* **Erstellen von API-Endpunkten**, die Journey Optimizer über benutzerdefinierte Aktionen aufrufen kann
* **Integrieren** von Journey Optimizer mit Ihren vorhandenen Systemen und Infrastrukturen
* **Testen und Debuggen** Ihrer Implementierungen

[Ihre Dateningenieurin bzw. Ihr Dateningenieur](data-engineer.md) verarbeitet Datenschemata, Ereigniskonfigurationen und Datenquellen. [Ihre bzw. Ihr Admin](administrator.md) richtet Berechtigungen und Kanalkonfigurationen ein. [Marketing-Fachleute](marketer.md) entwerfen die Journeys und Inhalte, die Ihre Implementierungen verwenden.

In diesem Handbuch werden die wesentlichen Schritte der technischen Implementierung für die ersten Schritte mit Journey Optimizer beschrieben. Gehen Sie wie folgt vor, um Ihre Implementierung einzurichten, unabhängig davon, ob Sie Apps, Web-Erlebnisse oder API-Integrationen erstellen.

## Voraussetzungen {#prerequisites}

Bevor Sie mit der Implementierung beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

| Kategorie | Anforderungen |
|----------|-------------|
| **Technische Fähigkeiten** | * Erfahrung mit JavaScript (für Web SDK) oder Swift/Kotlin (für Mobile SDK)<br>* Grundlegendes Verständnis von RESTful-APIs und JSON<br>* Erfahrung mit asynchroner Programmierung und ereignisgesteuerten Architekturen<br>* Kenntnis der Anwendungsarchitektur Ihres Unternehmens |
| **Zugriff und Tools** | * Zugriff auf [Adobe Developer Console](https://developer.adobe.com){target="_blank"} für API-Anmeldedaten<br>* Entwicklungsumgebung mit Zugriff auf die Code-Basis Ihrer Anwendung<br>* Test-Tools wie Postman für API-Tests<br>* Browser-Entwicklungs-Tools oder Mobile-Debugging-Tools |
| **Von anderen Team-Mitgliedern** | * Zugriff auf die Umgebung von [Admin](administrator.md)<br>* XDM-Schemata und Ereignisdefinitionen von [Dateningenieurin bzw. -ingenieur](data-engineer.md)<br>* Anforderungen und Anwendungsfälle von [Marketing-Fachleuten](marketer.md) |

## Grundlegendes zur technischen Grundlage {#technical-foundation}

Machen Sie sich mit den wichtigsten technischen Konzepten vertraut, bevor Sie sich mit der Implementierung befassen:

1. **Adobe Experience Platform-Integration**: Journey Optimizer basiert nativ auf Adobe Experience Platform. Wenn Sie die zugrunde liegende Architektur verstehen, können Sie effektivere Implementierungen erstellen. Erfahren Sie mehr über [die Funktionsweise von Journey Optimizer](../understanding-ajo.md).

1. **XDM-Datenmodelle**: Journey Optimizer verwendet das Experience-Datenmodell (XDM), um Ereignis- und Profildaten zu strukturieren. Als Entwicklerin bzw. Entwickler müssen Sie verstehen, wie Sie Daten senden, die den von [Ihrer Dateningenieurin bzw. Ihrem Dateningenieur](data-engineer.md) konfigurierten Schemata entsprechen. Erfahren Sie mehr über [XDM-Schemata](../../data/get-started-schemas.md).

1. **Authentifizierung und Sicherheit**: Alle Implementierungen erfordern eine ordnungsgemäße Authentifizierung. Erfahren Sie, wie Sie die Authentifizierung für SDKs und APIs einrichten. Erfahren Sie mehr über die [API-Authentifizierung](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}.

## Einrichten von App-Integrationen {#mobile-integration}

### Konfigurieren des Adobe Experience Platform Mobile SDK

Mobile SDK ist eine Sammlung von Bibliotheken, die Sie direkt in Ihre iOS- oder Android-App einbetten. Sie fungiert als Kommunikationsebene zwischen Ihrer App und Adobe Experience Platform: Sie identifiziert Benutzende, sammelt Verhaltensereignisse und stellt Anweisungen von Journey Optimizer bereit - einschließlich Push-Benachrichtigungen, In-App-Nachrichten und personalisierter Inhalte. Ohne sie hat Journey Optimizer keine Einsicht in die Aktivitäten Ihrer App-Benutzer und keine Möglichkeit, sie zu erreichen.

1. **Installieren und Konfigurieren des Mobile SDK**: Befolgen Sie die [Dokumentation zum Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/getting-started){target="_blank"}, um mit der SDK-Integration loszulegen.

1. **Erstellen einer Mobile-Eigenschaft**: Richten Sie eine Mobile-Eigenschaft in [!DNL Adobe Experience Platform Data Collection] ein. Erfahren Sie, wie Sie [eine Mobile-Eigenschaft erstellen und konfigurieren](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property){target="_blank"}.

1. **Konfigurieren von Push-Benachrichtigungen**:
   * Für **iOS-Apps**: Registrieren Sie Ihre App bei APNs (Apple Push Notification Service). Erfahren Sie mehr in der [Dokumentation von Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Für **Android-Apps**: Richten Sie Firebase Cloud Messaging für Ihre Android-App ein. Erfahren Sie mehr in der [Dokumentation von Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Testen Ihrer Mobile-Integration**: Verwenden Sie den [Schnellstart-Workflow für Mobile-Onboarding](../../push/mobile-onboarding-wf.md), um Ihre Mobile-Einrichtung schnell zu konfigurieren und zu testen.

Detaillierte Schritte zum Konfigurieren von Push-Benachrichtigungen finden Sie auf [dieser Seite](../../push/push-configuration.md).

### Implementieren von Code-basierten Erlebnissen (Mobile SDK)

Mit Code-basierten Erlebnissen können Sie personalisierte Inhalte für jede Oberfläche in Ihrer nativen Mobile App bereitstellen - von Onboarding-Bildschirmen und Produktdetailseiten bis hin zu In-App-Bannern und Feature Flags -, ohne dass eine neue App-Version erforderlich ist. Verwenden Sie die Mobile SDK, um personalisierte Inhalte zur Laufzeit abzurufen und zu rendern, sodass Ihr Team die volle Kontrolle über Platzierung und Präsentation hat:

* Befolgen Sie [dieses Tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial){target="_blank"} bei der Implementierung von Mobile SDK
* Überprüfen Sie die Beispielimplementierungen für [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} und [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}

## Implementieren von Web-Erlebnissen {#web-implementation}

### Einrichten des Adobe Experience Platform Web SDK

Web SDK (`alloy.js`) ist eine einzelne JavaScript-Bibliothek, die das Patchwork separater Adobe-Tags ersetzt, die Ihre Site andernfalls möglicherweise benötigt. Es erfasst Verhaltensdaten, streamt sie über einen von Ihnen konfigurierten Datenstrom an Adobe Experience Platform und empfängt Personalisierungsanweisungen zurück - alles in einer Netzwerk-Roundtrip. Sobald sie eingerichtet ist, kann Journey Optimizer Besucher und Trigger-Journey anhand ihrer Aktionen identifizieren und Ihren Seiten sofort maßgeschneiderte Inhalte bereitstellen.

1. **Installieren des Web SDK**: Befolgen Sie das [Implementierungshandbuch des Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de){target="_blank"}, um das SDK auf Ihrer Website einzurichten.

1. **Konfigurieren von Datenströmen**: Erstellen und konfigurieren Sie einen Datenstrom in [!DNL Adobe Experience Platform Data Collection], während Journey Optimizer aktiviert ist. Erfahren Sie mehr in der [Dokumentation zu Datenströmen](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=de){target="_blank"}.

1. **Aktivieren von Web-Push-Benachrichtigungen** (optional): Web-Push-Benachrichtigungen sind nun allgemein verfügbar. Konfigurieren Sie die [pushNotifications-Eigenschaft](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"} in Ihrer Web-SDK-Konfiguration und verwenden Sie den [sendPushSubscription-Befehl](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"} zum Registrieren von Push-Abonnements. [Erfahren Sie mehr zur Web-Push-Konfiguration](../../push/push-configuration-web.md).

### Implementieren von Code-basierten Erlebnissen (Web SDK)

Im Gegensatz zu visuellen Kanälen, bei denen Marketer das Layout vollständig steuern, bieten Code-basierte Erlebnisse Ihnen volle Verantwortung dafür, wie personalisierte Inhalte auf der Seite gerendert werden. Journey Optimizer gibt eine JSON-Payload mit den Personalisierungsdaten zurück. Ihr Code entscheidet, wo und wie sie angezeigt wird. Dieses Modell funktioniert für jede Web-Oberfläche - Hero-Banner, Empfehlungskarussells, Suchergebnis-Rankings, A/B-Testvarianten -, ohne dass ein visueller Editor oder ein Seitenveröffentlichungs-Workflow erforderlich ist.

1. **Auswählen Ihrer Implementierungsmethode**: Client-seitig, Server-seitig oder hybrid. Sehen Sie sich die [Implementierungsbeispiele](../../code-based/code-based-implementation-samples.md) für jeden Ansatz an.

1. **Definieren von Oberflächen**: Identifizieren Sie die Bereiche in Ihrer Anwendung, an denen Sie personalisierte Inhalte bereitstellen möchten. Erfahren Sie mehr über die [Oberflächenkonfiguration](../../code-based/code-based-surface.md).

1. **Implementieren des Inhalts-Renderings**: Verwenden Sie das Web SDK, um Personalisierungsinhalte abzurufen und anzuwenden. Siehe [Tutorials zur Code-basierten Implementierung](../../code-based/code-based-decisioning-implementations.md).

1. **Senden von Anzeige- und Interaktionsereignissen**: Verfolgen Sie aus Analyse- und Optimierungszwecken, wann Inhalte angezeigt werden und wann Benutzende mit diesen interagieren.

Erkunden Sie [Beispielimplementierungen auf GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}, um Code-basierte Erlebnisse in Aktion zu sehen.

Erfahren Sie mehr über die [ersten Schritte mit Code-basierten Erlebnissen](../../code-based/get-started-code-based.md).

## Implementieren von Ereignis-Streaming {#event-streaming}

### Senden von Ereignissen zum Auslösen von Journeys

Journey werden bei Ereignissen ausgeführt: Ein Benutzer meldet sich an, fügt einen Artikel zu einem Warenkorb hinzu, schließt einen Kauf ab oder bricht ein Formular ab. Ihre Aufgabe besteht darin, diese Ereignisse aus Ihrer Anwendung genau zum richtigen Zeitpunkt auszugeben. Jedes Ereignis ist eine XDM-strukturierte JSON-Payload, die an die Experience Platform Streaming-Aufnahme-API gesendet wird. Journey Optimizer nimmt es innerhalb von Millisekunden auf und leitet das Profil an eine beliebige passende Journey weiter. Das Ereignisschema und die Payload-Struktur werden von Ihrem [Dateningenieur](data-engineer.md) definiert. Stimmen Sie sich mit ihnen ab, bevor Sie mit der Codierung beginnen.

1. **Grundlegendes zur Ereignis-Payload**: Arbeiten Sie mit Ihrer Dateningenieurin bzw. Ihrem Dateningenieur zusammen, um das Ereignisschema und die erforderliche Payload-Struktur zu erhalten. Die Payload muss dem konfigurierten XDM-Schema entsprechen. Erfahren Sie mehr über [Anforderungen an Ereignisschemata](../../event/experience-event-schema.md).

1. **Implementeiren von Ereignis-Streaming**: Senden Sie Ereignisse mithilfe der [Streaming-Aufnahme-APIs](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=de){target="_blank"} an Adobe Experience Platform. Erfahren Sie mehr über die [Schritte zum Senden von Ereignissen](../../event/additional-steps-to-send-events-to-journey.md).

1. **Verarbeiten von Ereignistypen**:
   * **Unitäre Ereignisse**: Implementieren des Ereignisversands für personenspezifische Aktionen (z. B. Klick auf eine Schaltfläche, Kaufabschluss)
   * **Geschäftsereignisse**: Senden von geschäftsbezogenen Ereignissen (z. B. Bestandsaktualisierungen, Preisänderungen)

1. **Testen des Ereignisversands**: Überprüfen Sie, ob die Ereignisse ordnungsgemäß empfangen werden und die Journeys wie erwartet auslösen. Erfahren Sie mehr über die [Fehlerbehebung bei Ereignissen](../../building-journeys/troubleshooting-inbound.md).

**Beispielimplementierung** zum Senden eines Ereignisses über die API:

```javascript
POST https://{DATACOLLECTION_ENDPOINT}/collection/{DATASTREAM_ID}
Content-Type: application/json

{
  "header": {
    "datasetId": "{DATASET_ID}",
    "imsOrgId": "{ORG_ID}",
    "source": {
      "name": "Web SDK"
    }
  },
  "body": {
    "xdmMeta": {
      "schemaRef": {
        "id": "{SCHEMA_ID}"
      }
    },
    "xdmEntity": {
      "_id": "unique-event-id",
      "eventType": "purchase",
      "timestamp": "2024-01-01T12:00:00Z",
      // ... your event data
    }
  }
}
```

Erfahren Sie mehr über das [Arbeiten mit Journey-Ereignissen](../../event/about-events.md).

## Entwickeln von Endpunkten benutzerdefinierter Aktionen {#custom-actions}

Wenn eine Journey einen benutzerdefinierten Aktionsschritt erreicht, führt Journey Optimizer einen ausgehenden HTTP-Aufruf an eine von Ihnen angegebene URL durch: Ihr Backend, ein CRM, eine Treueplattform oder einen beliebigen REST-Endpunkt. Ihre Aufgabe besteht darin, diesen Endpunkt zu erstellen und bereitzustellen: Definieren Sie den Anfragevertrag (Payload-Form, Authentifizierungsmethode, Antwortformat), implementieren Sie die dahinter stehende Geschäftslogik und stellen Sie sicher, dass sie das von Journey Optimizer generierte Aufrufvolumen verarbeiten kann. Ihr [Administrator](administrator.md) registriert den Endpunkt dann in Journey Optimizer, damit Marketing-Experten ihn als Schritt in ihren Journey verwenden können.

1. **Erstellen Ihres API-Endpunkts**: Erstellen Sie RESTful-API-Endpunkte, die Journey Optimizer während der Journey-Ausführung aufruft. Ihr Endpunkt sollte:
   * JSON-Payloads akzeptieren
   * Anfragen authentifizieren (OAuth, API-Schlüssel oder JWT)
   * Anforderungen innerhalb angemessener Timeout-Limits verarbeiten
   * Antworten im erwarteten Format zurückgeben

1. **Grundlegendes zu den Funktionen von benutzerdefinierten Aktionen**: Benutzerdefinierte Aktionen können eine Verbindung zu Drittanbietersystemen wie Epsilon, Slack, Firebase oder Ihren eigenen Diensten herstellen. Weitere Informationen über [benutzerdefinierte Aktionen](../../action/action.md).

1. **Arbeiten mit Aktionskonfigurationen**: [Ihre bzw. Ihr Admin](administrator.md) oder [Ihre Dateningenieurin bzw. Ihr Dateningenieur](data-engineer.md) konfiguriert die benutzerdefinierte Aktion in Journey Optimizer und definiert die API-Endpunkt-URL, Authentifizierungsmethode und Parameter. Sie geben ihnen Ihre API-Spezifikation. Erfahren Sie mehr über die [Konfiguration benutzerdefinierter Aktionen](../../action/about-custom-action-configuration.md). Sie können eine optionale **Fehlerantwort-Payload** für eine umfassendere Fallback-Logik in Timeout-/Fehlerverzweigungen definieren.

1. **Zurückgeben verwertbarer Daten**: Konzipieren Sie Ihre API so, dass sie Daten zurückgibt, die in nachfolgenden Journey-Schritten verwendet werden können. Erfahren Sie mehr über [Aktionsantworten](../../action/action-response.md).

1. **Überwachen des Zustands benutzerdefinierter Aktionen**: Verwenden Sie das Dashboard zur Überwachung benutzerdefinierter Aktionen, um erfolgreiche Aufrufe, Fehler, Durchsatz, Antwortzeiten und Warteschlangen-Wartezeiten zu verfolgen. Erfahren Sie mehr über das [Reporting von benutzerdefinierten Aktionen](../../action/reporting.md).

1. **Implementieren einer Ratenbegrenzung**: Stellen Sie sicher, dass Ihre Endpunkte das erwartete Volumen verarbeiten können. Journey Optimizer begrenzt die Anzahl der Aufrufe pro Sekunde auf 5.000. Ihr System sollte jedoch resilient sein. Erfahren Sie mehr über [Begrenzung und Drosselung](../../configuration/external-systems.md).

**Beispiel eines Anwendungsfalls**: [Schreiben von Journey-Ereignissen in Experience Platform](../../building-journeys/custom-action-aep.md) unter Verwendung von benutzerdefinierten Aktionen.

## Arbeiten mit Journey Optimizer-APIs {#apis}

Nicht alles muss über die Journey Optimizer-Benutzeroberfläche erfolgen. Manchmal müssen Sie einen Trigger über Ihr eigenes Backend durchführen, eine E-Mail-Adresse nach einer Datenschutzanfrage unterdrücken oder Inhaltsvorlagen aus einer externen CMS synchronisieren. Die REST-APIs von Journey Optimizer bieten Ihnen programmgesteuerten Zugriff auf die Kernfunktionen der Plattform. Alle Aufrufe verwenden OAuth-Server-zu-Server-Authentifizierung - die ältere JWT-Methode ist veraltet.

1. **Grundlegendes zu API-Funktionen**: Mit Journey Optimizer-APIs können Sie verschiedene Ressourcen programmgesteuert erstellen, lesen, aktualisieren und löschen. Erfahren Sie mehr über [Journey Optimizer-APIs](../../configuration/ajo-apis.md).

1. **Authentifizierung**: Befolgen Sie [dieses Tutorial](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}, um die API-Authentifizierung mit Adobe Developer Console einzurichten.

1. **Erkunden von API-Referenzen**: Sehen Sie sich die vollständige API-Dokumentation an und probieren Sie APIs direkt in der [Adobe Journey Optimizer-API-Referenz](https://developer.adobe.com/journey-optimizer-apis){target="_blank"} aus.

1. **Durch APIs ausgelöste Kampagnen**: Erstellen Sie Transaktions-Messaging mit durch APIs ausgelösten Kampagnen. Bei Szenarien mit hohem Volumen (bis zu 5.000 TPS) sollten Sie den [Modus mit hohem Durchsatz](../../campaigns/api-triggered-high-throughput.md) in Erwägung ziehen (Add-on-Lizenz erforderlich).

1. **Entscheidungs-Management-APIs**: Verwenden Sie spezielle APIs für Angebotsverwaltung und Entscheidungsfindung. Erfahren Sie mehr im [Handbuch zur Entscheidungs-Management-API](../../offers/api-reference/getting-started.md).

1. **Entscheidungsfindungsmigrations-APIs**: Migrieren Sie Entscheidungs-Management-Entitäten programmgesteuert in die Entscheidungsfindung mit flexiblen Bereichen, automatisierter Validierung und Rollback-Unterstützung. Erfahren Sie mehr im [Handbuch zur Entscheidungsfindungsmigrations-API](../../experience-decisioning/decisioning-migration-api.md).

1. **SMS-Webhooks**: Konfigurieren Sie eingehende Webhooks, um eingehende Nachrichten und Feedback-Webhooks zu erfassen, damit Versandbestätigungen und Statusaktualisierungen empfangen werden können. [Weitere Informationen](../../mobile/mobile-webhook.md).

## Testen und Debuggen {#testing}

Bevor Ihre Implementierung live geht, müssen Sie darauf vertrauen können, dass die Ereignisse zum richtigen Zeitpunkt ausgelöst werden, der Journey wie erwartet den Trigger ausführen, sich benutzerdefinierte Aktionen unter realistischer Last verhalten und personalisierte Inhalte korrekt gerendert werden. In diesem Abschnitt werden die Tools und Techniken zum frühzeitigen Erkennen von Problemen beschrieben - von der SDK-Protokollierung auf niedriger Ebene bis hin zu End-to-End-Journey-Testläufen mit echten Profilen.

1. **SDK-Implementierung debuggen**: Verwenden Sie Adobe Experience Platform Assurance, um SDK-Ereignisse zu überprüfen, die Datenerfassung zu validieren und Integrationsprobleme zu beheben, sobald sie auftreten. [Erfahren Sie mehr über Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=de){target="_blank"}.

1. **Testen des Ereignisversands**: Überprüfen Sie, ob Ereignisse aus Ihrer Anwendung von Adobe Experience Platform empfangen werden und Journeys wie erwartet auslösen. Überwachen Sie die Ereignisaufnahme und überprüfen Sie die Payload-Struktur.

1. **Validieren von API-Integrationen**: Testen Sie die Endpunkte Ihrer benutzerdefinierten Aktion, um sicherzustellen, dass sie Journey Optimizer-Anfragen korrekt verarbeiten, innerhalb der Timeout-Limits reagieren und die erwarteten Datenformate zurückgeben.

1. **Verwenden des Testmodus mit Testprofilen**: Arbeiten Sie mit Ihren [Dateningenieurinnen und -ingenieuren](data-engineer.md) zusammen, um Zugriff auf Testprofile zu erhalten, und validieren Sie dann Ihre Implementierung mithilfe des Journey-Testmodus. Erfahren Sie mehr über das [Testen von Journeys](../../building-journeys/testing-the-journey.md).

1. **Überwachen von SDK-Protokollen**: Aktivieren Sie die Debug-Protokollierung in Ihrer SDK-Implementierung, um Probleme während der Entwicklung zu beheben:
   * **Mobile SDK**: Aktivieren der Protokollierung, um SDK-Ereignisse und API-Aufrufe anzuzeigen
   * **Web SDK**: Verwenden der Browser-Konsole, um SDK-Aktivität zu überwachen

1. **Überprüfen der Datenstromkonfiguration**: Stellen Sie sicher, dass Ihr Datenstrom ordnungsgemäß konfiguriert ist, um Daten an Journey Optimizer zu senden. Überprüfen Sie, ob Ereignisse durch den Datenstrom zu den richtigen Zielen fließen.

1. **Abfrage von Journey-Daten für die Analyse**: Verwenden Sie SQL-Abfragen im Data Lake, um Journey-Schrittereignisse zu analysieren, Probleme zu debuggen und die Leistung benutzerdefinierter Aktionen zu überwachen. Erkunden Sie [Abfragebeispiele für die Journey-Analyse](../../reports/query-examples.md), einschließlich:
   * Tracking von Profileintritten/-ausstiegen und Verwerfungsgründe
   * Leistungsmetriken für benutzerdefinierte Aktionen (Latenz, Durchsatz, Fehler)
   * Ereignisversand- und Fehlermuster
   * Journey-Instanzstatus

## Fortgeschrittene Entwicklerthemen {#advanced-topics}

Sobald Ihre Kern-SDKs, Ereignisse und APIs eingerichtet sind, helfen Ihnen diese Themen weiter: Anreicherung von Journey-Daten zur Laufzeit ohne Profilaufblähung, Handhabung von Einverständnissignalen, sodass Opt-outs sich über jede Integration ausbreiten, und Abstimmung Ihrer Implementierung auf den Durchsatz und die Zuverlässigkeit, die der Produktionsmaßstab erfordert.

### Arbeiten mit kontextuellen Daten und Anreicherung

Journey benötigen häufig mehr Daten als die, die im auslösenden Ereignis eingehen - einen Produktnamen, eine Treuestufe, eine Bestellzeilenelementliste. Anstatt all dies in alle Profile vorab zu laden, können Sie es mit der kontextuellen Anreicherung zur Laufzeit aus AEP-Datensätzen nachschlagen oder von einer benutzerdefinierten Aktionsantwort weiterleiten. Ihre Nachrichten- und Verzweigungsbedingungen können dann auf diese Daten verweisen, ohne dass sie jemals dauerhaft im Profil gespeichert werden.

* **Iteration über Arrays**: Verwenden Sie die Handlebars-Syntax, um dynamische Listen aus Ereignissen, benutzerdefinierten Aktionsantworten und Datensatzsuchen in Nachrichten anzuzeigen. Erfahren Sie mehr über das [Iterieren über kontextuelle Daten](../../personalization/iterate-contextual-data.md).
* **Datensatzsuche**: Implementieren von Datensatzsuchen zur Anreicherung von Journey-Daten aus Adobe Experience Platform-Datensätzen. Arbeiten Sie bei der Konfiguration mit Ihrer Dateningenieurin bzw. Ihrem Dateningenieur zusammen. Erfahren Sie mehr über die [Datensatzsuche](../../building-journeys/dataset-lookup.md).

### Arbeiten mit Einverständnis und Governance

Journey Optimizer erzwingt Richtlinien zur Data Governance und zum Einverständnis auf Plattformebene, aber Ihre Integration muss diese auch berücksichtigen. Wenn ein Kunde sich von Marketing-Nachrichten abmeldet oder wenn eine Datennutzungskennzeichnung die Verwendung eines Felds einschränkt, müssen diese Regeln durch Ihre benutzerdefinierten Aktionen und Datensatzsuchen verbreitet werden - nicht nur durch die Blockierung von Aktionen in der Benutzeroberfläche.

* **Data Governance**: Wenden Sie Datennutzungsrichtlinien auf benutzerdefinierte Aktionen an. Erfahren Sie mehr über [Data Governance](../../action/action-privacy.md).
* **Einverständnisverwaltung**: Verarbeiten Sie die Voreinstellungen für das Kundeneinverständnis in Ihren Implementierungen. Erfahren Sie mehr über [Einverständnis](../../action/consent.md).

### Optimierung und Best Practices

In Produktions-Journey Optimizer-Implementierungen werden regelmäßig Millionen von Ereignissen und Tausende von Journey-Ausführungen pro Sekunde verarbeitet. Mit diesen Ressourcen können Sie Ihre Integration auf diese Größenordnung abstimmen. So verstehen Sie Ratenbeschränkungen, bevor Sie sie erreichen, vermeiden gängige Journey-Design-Fallstricke, die Profile im Hintergrund löschen, und erstellen Fehlerbehandlungsmethoden, die sich elegant abschwächen, anstatt opak zu scheitern.

* **Begrenzung und Drosselung**: Machen Sie sich mit den Ratenbegrenzungen vertraut und implementieren Sie geeignete Drosselungen. Erfahren Sie mehr über [externe Systeme](../../configuration/external-systems.md).
* **Journey-Optimierung**: Befolgen Sie die Best Practices für die [Journey-Optimierung](../../building-journeys/optimize.md).
* **Fehlerbehandlung**: Implementieren Sie eine robuste Fehlerbehandlung. Sehen Sie sich [Fehler-Codes](../../building-journeys/error-codes-reference.md) und [Handbücher zur Fehlerbehebung](../../building-journeys/troubleshooting.md) an.

## Aufrufen von Journey Optimizer REST-APIs {#rest-apis}

Neben der Implementierung von SDKs und Ereignis-Streaming können Sie Journey Optimizer auch programmgesteuert von Ihren eigenen Systemen aus steuern. Die vollständige API-Referenz, OpenAPI-Spezifikationen und Code-Beispiele finden Sie im [Journey Optimizer-Entwicklerportal](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}.

>[!NOTE]
>
>Alle Integrationen müssen eine OAuth-Server-zu-Server-Authentifizierung verwenden - die JWT-Methode ist veraltet. [Einrichten der Authentifizierung](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}

### API-ausgelöste Kampagnen ausführen {#api-triggered}

Trigger von Transaktions- oder Marketing-Nachrichten aus einem externen System mithilfe der Interactive Message Execution REST-API. Vor dem Aufrufen des Endpunkts:

* Die Kampagne muss **aktiviert** bevor der Endpunkt Aufrufe akzeptiert.
* Aufrufe haben eine **Zeitüberschreitung von 60 Sekunden** interne Wiederholungsversuche verarbeiten unerwartete Zeitüberschreitungen.
* Wenn Start-/Enddatum der Kampagne konfiguriert sind, schlagen API-Aufrufe außerhalb dieser Daten fehl.
* Um Ihre Payload zu erstellen, rufen Sie die generierte Beispiel-cURL-Anfrage aus dem Abschnitt **cURL-Anfrage** Ihrer Live-Kampagne in der Journey Optimizer-Benutzeroberfläche ab. Sie enthält alle Personalisierungsvariablen für diese Kampagne.
* Standard- und [Kampagnen mit hohem Durchsatz](../../campaigns/api-triggered-high-throughput.md) verwenden verschiedene Endpunkte.

[API-Referenz](https://developer.adobe.com/journey-optimizer-apis/references/messaging){target="_blank"} ・ [Code-Beispiele](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples){target="_blank"} ・ [Arbeiten mit API-ausgelösten Kampagnen](../../campaigns/api-triggered-campaigns.md)

### Begrenzung und Drosselung für externe Endpunkte {#capping-throttling}

Wenn Journey externe Systeme über benutzerdefinierte Aktionen oder Datenquellen aufrufen, schützen die Begrenzungs- und Einschränkungs-APIs diese Systeme vor Überlastung. Durch Begrenzung werden Aufrufe abgelehnt, die das konfigurierte Limit überschreiten; durch Drosselung werden sie für bis zu 6 Stunden in die Warteschlange gestellt (nur Produktions-Sandboxes, benutzerdefinierte Aktionen).

[Referenz zur Begrenzungs](https://developer.adobe.com/journey-optimizer-apis/references/journeys-throttling){target="_blank"} ・ [Arbeiten mit der Begrenzungs-](../../configuration/capping.md) ・ [Arbeiten mit der Drosselungs-API](../../configuration/throttling.md)

### Weitere REST-APIs {#more-rest-apis}

Über Messaging und Begrenzungen hinaus stellt Journey Optimizer REST-Endpunkte für die Unterdrückungsverwaltung, Inhaltsvorlagen, den Kampagnenabruf, das Proofing und die orchestrierte Kampagnenausführung bereit. Verwenden Sie diese , wenn Sie Vorgänge automatisieren müssen, die andernfalls manuelle Schritte in der Benutzeroberfläche erfordern würden, z. B. das Unterdrücken von Massenadressen nach einem Daten-Pull oder das Synchronisieren von Vorlagen aus einer externen Inhalts-Pipeline.

| Was Sie tun müssen | API-Referenz |
| ------------------- | ------------- |
| Programmgesteuertes Ausschließen von E-Mail-Adressen oder Domains vom Versand | [Unterdrückungs-API](https://developer.adobe.com/journey-optimizer-apis/references/suppression){target="_blank"} ・ [Verwalten der Unterdrückungsliste](../../configuration/manage-suppression-list.md) |
| Abrufen von Journey-Metadaten für Auditing oder externe Synchronisierung | [Journey-API](https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve){target="_blank"} |
| Erstellen und Verwalten von Inhaltsvorlagen und Fragmenten aus einer externen Pipeline | [Content-API](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"} ・ [Vorlagen](../../content-management/content-templates.md) ・ [Fragments](../../content-management/fragments.md) |
| Abrufen und Filtern von Aktionskampagnen | [Kampagnen-API](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"} |
| Programmgesteuerte Vorschau von Kampagnen und Durchführen von Testsendungen | [Simulations-API](https://developer.adobe.com/journey-optimizer-apis/references/simulations){target="_blank"} |
| Datensätze validieren und Trigger der koordinierten Kampagnenausführung | [Datensatzvalidierung](https://developer.adobe.com/journey-optimizer-apis/references/orchestrated-campaign-dataset){target="_blank"} ・ [Trigger ](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} ・ [Datensätze aktivieren](../../orchestrated/manual-schema.md) |

## Zusätzliche Ressourcen {#additional-resources}

* **Developer Console**: Greifen Sie auf die [Adobe Developer Console](https://developer.adobe.com){target="_blank"} zu, um Integrationen zu erstellen und API-Anmeldedaten zu verwalten.
* **Beispiel-Code**: Sehen Sie sich [Beispielimplementierungen auf GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} an.
* **Video-Tutorials**: Lernen Sie durch praktische Tutorials auf [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=de){target="_blank"}.
* **Entwickler-Community**: Treten Sie mit anderen Entwickelnden in Kontakt und erhalten Sie Unterstützung in den Adobe-Community-Foren.

## Rollenübergreifendes Zusammenarbeiten {#next-steps}

Ihre Implementierungsarbeit überschneidet sich mit anderen Team-Mitgliedern:

>[!BEGINTABS]

>[!TAB Arbeiten mit Dateningenieurinnen und -ingenieuren]

Zusammenarbeit mit [Dateningenieuren](data-engineer.md) bei Daten- und Ereigniskonfigurationen. Jeder Journey, der auf das Benutzerverhalten reagiert, hängt von den von Ihnen gesendeten Ereignissen ab: Der Data Engineer definiert die Schemata, Sie implementieren den Code, der sie erzeugt.

* Rufen Sie die [XDM-Schemata](../../data/get-started-schemas.md) und Ereignisstrukturen ab, die Sie implementieren müssen
* Erfahren Sie, welche Ereignisse Sie senden müssen und welches Payload-Format erforderlich ist - siehe [Arbeiten mit Journey-Ereignissen](../../event/about-events.md)
* Überprüfen Sie, welche Felder in jeder Ereignis-Payload erforderlich bzw. optional sind und was in Journey passiert, wenn erwartete Felder fehlen oder fehlerhaft sind - siehe [Schemaanforderungen](../../event/experience-event-schema.md#schema-requirements)
* Gemeinsames Testen des Versands und der Datenaufnahme mithilfe von [Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=de){target="_blank"}

>[!TAB Arbeiten mit Admins]

Zusammenarbeit mit [Administratoren](administrator.md) bei Zugriffs- und Kanalkonfigurationen. Journey können Benutzende nur über vom Administrator eingerichtete Kanäle erreichen - koordinieren Sie diese frühzeitig, damit Ihre SDK-Arbeit und deren Konfiguration synchron bleiben.

* Angeben von API-Spezifikationen für [benutzerdefinierte Aktionen](../../action/about-custom-action-configuration.md) die in Journey Optimizer konfiguriert werden
* Erforderliche Berechtigungen und API-Anmeldedaten über [Adobe Developer Console anfordern](https://developer.adobe.com){target="_blank"}
* Koordinieren Sie die Anforderungen an die Kanalkonfiguration - Push-Zertifikate für die Endpunkte {](../../push/push-configuration.md)}iOSund Android[Web-Push](../../push/push-configuration-web.md), [SMS-Webhook](../../mobile/mobile-webhook.md)[
* Ausrichtung der Sandbox-Strategie und der Testumgebungen vor der Ausführung des [Journey-Testmodus](../../building-journeys/testing-the-journey.md)

>[!TAB Arbeiten mit Marketing-Fachleuten]

Zusammenarbeit mit [Marketern](marketer.md) beim Entwerfen und Testen von Journey. Marketer erstellen die Journey und Inhalte, die vollständig von den gesendeten Ereignissen und den Oberflächen abhängen, die Sie bereitstellen - je näher Sie einander abstimmen, desto schneller werden die Journey live geschaltet.

* Überprüfen Sie gemeinsam die Journey-Designs in [Journey Optimizer](../../building-journeys/journey.md), um zu verstehen, welche Benutzerinteraktionen Trigger-Ereignisse auslösen müssen und welche Oberflächen personalisiert werden müssen
* Implementieren des Trackings, damit Marketing-Experten [Content-Performance und Benutzerinteraktion) messen ](../../reports/report-gs-cja.md)
* Führen Sie [Journey Testmodus](../../building-journeys/testing-the-journey.md) zusammen mit Testprofilen aus, um den vollständigen Fluss End-to-End zu validieren.
* Fehlerbehebung bei Problemen mit Nachrichtenversand, Personalisierung, Rendering oder [benutzerdefinierten ](../../action/action.md))

>[!ENDTABS]

## Starten der Implementierung

Bereit, mit dem Erstellen zu beginnen? Wählen Sie Ihren ersten Implementierungsbereich aus den obigen Abschnitten:

1. **App?** Beginnen Sie mit der [Mobile-SDK-Integration](#mobile-integration)
2. **Website?** Beginnen Sie mit der [Web-SDK-Einrichtung](#web-implementation)
3. **API-Integration?** Wechseln Sie zu [Arbeiten mit APIs](#apis)
4. **Benutzerdefiniertes System?** Wechseln Sie zu [Benutzerdefinierte Aktionen](#custom-actions)

Jeder Abschnitt enthält Links zu detaillierter technischer Dokumentation, Code-Beispielen und Tutorials, die Sie bei der Implementierung unterstützen.

## Weitere Rollenleitfäden {#other-role-guides}

| Rolle | Handbuch |
|------|-------|
| Administrator | [Erste Schritte für Administratoren](administrator.md) |
| Datentechniker | [Erste Schritte für Dateningenieure](data-engineer.md) |
| Entwickler | [Erste Schritte für Entwickler](developer.md) |
| Marketer | [Erste Schritte für Marketing-Fachleute](marketer.md) |

Zurück zu [Überblick über Rollen und Zuständigkeiten](../quick-start.md) ・ Zurück zu [Erste Schritte](../../../rp_landing_pages/get-started-landing-page.md)
