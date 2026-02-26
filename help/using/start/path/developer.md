---
title: Erste Schritte für Entwickler
description: Hier erfahren Entwickler mehr über die Arbeit mit Journey Optimizer.
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: fd10a600cb54b8c35e2d195be7379b0dd120b6a7
workflow-type: tm+mt
source-wordcount: '1918'
ht-degree: 93%

---

# Erste Schritte für Entwickler {#get-started-developers}

Als **Entwicklerin bzw. Entwickler** sind Sie für die Implementierung und Integration von [!DNL Adobe Journey Optimizer] in Ihre Anwendungen und Systeme verantwortlich. Sie können mit der Arbeit mit [!DNL Adobe Journey Optimizer] beginnen, sobald Ihnen [Systemadmin](administrator.md) und [Dateningenieurin bzw. -ingenieur](data-engineer.md) Zugriff auf Ihre Umgebung gewährt und diese vorbereitet haben.

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

1. **Authentifizierung und Sicherheit**: Alle Implementierungen erfordern eine ordnungsgemäße Authentifizierung. Erfahren Sie, wie Sie die Authentifizierung für SDKs und APIs einrichten. Erfahren Sie mehr über die [API-Authentifizierung](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

## Einrichten von App-Integrationen {#mobile-integration}

### Konfigurieren des Adobe Experience Platform Mobile SDK

Um Push-Benachrichtigungen, In-App-Nachrichten und andere Mobile-Funktionen zu aktivieren, integrieren Sie das Adobe Experience Platform Mobile SDK in Ihre Apps.

1. **Installieren und Konfigurieren des Mobile SDK**: Befolgen Sie die [Dokumentation zum Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"}, um mit der SDK-Integration loszulegen.

1. **Erstellen einer Mobile-Eigenschaft**: Richten Sie eine Mobile-Eigenschaft in [!DNL Adobe Experience Platform Data Collection] ein. Erfahren Sie, wie Sie [eine Mobile-Eigenschaft erstellen und konfigurieren](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}.

1. **Konfigurieren von Push-Benachrichtigungen**:
   * Für **iOS-Apps**: Registrieren Sie Ihre App bei APNs (Apple Push Notification Service). Erfahren Sie mehr in der [Dokumentation von Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Für **Android-Apps**: Richten Sie Firebase Cloud Messaging für Ihre Android-App ein. Erfahren Sie mehr in der [Dokumentation von Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Testen Ihrer Mobile-Integration**: Verwenden Sie den [Schnellstart-Workflow für Mobile-Onboarding](../../push/mobile-onboarding-wf.md), um Ihre Mobile-Einrichtung schnell zu konfigurieren und zu testen.

Detaillierte Schritte zum Konfigurieren von Push-Benachrichtigungen finden Sie auf [dieser Seite](../../push/push-configuration.md).

### Implementieren von Code-basierten Erlebnissen (Mobile SDK)

Für die native App-Personalisierung mithilfe von Code-basierten Erlebnissen:

* Befolgen Sie [dieses Tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} bei der Implementierung von Mobile SDK
* Überprüfen Sie die Beispielimplementierungen für [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} und [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}

## Implementieren von Web-Erlebnissen {#web-implementation}

### Einrichten des Adobe Experience Platform Web SDK

Bei Web-basierten Implementierungen ist das Web SDK Ihr primärer Integrationspunkt:

1. **Installieren des Web SDK**: Befolgen Sie das [Implementierungshandbuch des Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de){target="_blank"}, um das SDK auf Ihrer Website einzurichten.

1. **Konfigurieren von Datenströmen**: Erstellen und konfigurieren Sie einen Datenstrom in [!DNL Adobe Experience Platform Data Collection], während Journey Optimizer aktiviert ist. Erfahren Sie mehr in der [Dokumentation zu Datenströmen](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=de){target="_blank"}.

1. **Web-Push-Benachrichtigungen aktivieren** (optional): Web-Push-Benachrichtigungen sind jetzt allgemein verfügbar. Konfigurieren Sie die [pushNotifications](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"}Eigenschaft in Ihrer Web-SDK-Konfiguration und verwenden Sie den [sendPushSubscription-Befehl](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"} zum Registrieren von Push-Abonnements. [Erfahren Sie mehr über die Web-Push-Konfiguration](../../push/push-configuration-web.md).

### Implementieren von Code-basierten Erlebnissen (Web SDK)

Code-basierte Erlebnisse ermöglichen es Ihnen, jeden digitalen Kontaktpunkt zu personalisieren:

1. **Auswählen Ihrer Implementierungsmethode**: Client-seitig, Server-seitig oder hybrid. Sehen Sie sich die [Implementierungsbeispiele](../../code-based/code-based-implementation-samples.md) für jeden Ansatz an.

1. **Definieren von Oberflächen**: Identifizieren Sie die Bereiche in Ihrer Anwendung, an denen Sie personalisierte Inhalte bereitstellen möchten. Erfahren Sie mehr über die [Oberflächenkonfiguration](../../code-based/code-based-surface.md).

1. **Implementieren des Inhalts-Renderings**: Verwenden Sie das Web SDK, um Personalisierungsinhalte abzurufen und anzuwenden. Siehe [Tutorials zur Code-basierten Implementierung](../../code-based/code-based-decisioning-implementations.md).

1. **Senden von Anzeige- und Interaktionsereignissen**: Verfolgen Sie aus Analyse- und Optimierungszwecken, wann Inhalte angezeigt werden und wann Benutzende mit diesen interagieren.

Erkunden Sie [Beispielimplementierungen auf GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}, um Code-basierte Erlebnisse in Aktion zu sehen.

Erfahren Sie mehr über die [ersten Schritte mit Code-basierten Erlebnissen](../../code-based/get-started-code-based.md).

## Implementieren von Ereignis-Streaming {#event-streaming}

### Senden von Ereignissen zum Auslösen von Journeys

Als Entwicklern bzw. Entwickler implementieren Sie den Code zum Senden von Ereignissen, die Journeys auslösen. [Ihre Dateningenieurin bzw. Ihr Dateningenieur](data-engineer.md) konfiguriert die Ereignisschemata und -definitionen in Journey Optimizer.

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

Benutzerdefinierte Aktionen ermöglichen es Journeys, Ihre APIs aufzurufen. Als Entwicklerin bzw. Entwickler erstellen Sie die API-Endpunkte, die durch benutzerdefinierte Aktionen aufgerufen werden:

1. **Erstellen Ihres API-Endpunkts**: Erstellen Sie RESTful-API-Endpunkte, die Journey Optimizer während der Journey-Ausführung aufruft. Ihr Endpunkt sollte:
   * JSON-Payloads akzeptieren
   * Anfragen authentifizieren (OAuth, API-Schlüssel oder JWT)
   * Anforderungen innerhalb angemessener Timeout-Limits verarbeiten
   * Antworten im erwarteten Format zurückgeben

1. **Grundlegendes zu den Funktionen von benutzerdefinierten Aktionen**: Benutzerdefinierte Aktionen können eine Verbindung zu Drittanbietersystemen wie Epsilon, Slack, Firebase oder Ihren eigenen Diensten herstellen. Weitere Informationen über [benutzerdefinierte Aktionen](../../action/action.md).

1. **Arbeiten mit Aktionskonfigurationen**: [Ihre bzw. Ihr Admin](administrator.md) oder [Ihre Dateningenieurin bzw. Ihr Dateningenieur](data-engineer.md) konfiguriert die benutzerdefinierte Aktion in Journey Optimizer und definiert die API-Endpunkt-URL, Authentifizierungsmethode und Parameter. Sie geben ihnen Ihre API-Spezifikation. Erfahren Sie mehr über [Konfiguration benutzerdefinierter Aktionen](../../action/about-custom-action-configuration.md). Sie können eine optionale **Fehlerantwort-Payload) für** Fallback-Logik in Verzweigungen mit Zeitüberschreitung/Fehler definieren.

1. **Zurückgeben verwertbarer Daten**: Konzipieren Sie Ihre API so, dass sie Daten zurückgibt, die in nachfolgenden Journey-Schritten verwendet werden können. Erfahren Sie mehr über [Aktionsantworten](../../action/action-response.md).

1. **Überwachen der Konsistenz benutzerdefinierter Aktionen**: Verwenden Sie das Dashboard zur Überwachung benutzerdefinierter Aktionen, um erfolgreiche Aufrufe, Fehler, Durchsatz, Antwortzeiten und Warteschlangen-Wartezeiten zu verfolgen. Erfahren Sie mehr über [Berichte für benutzerdefinierte Aktionen](../../action/reporting.md).

1. **Implementieren einer Ratenbegrenzung**: Stellen Sie sicher, dass Ihre Endpunkte das erwartete Volumen verarbeiten können. Journey Optimizer begrenzt die Anzahl der Aufrufe pro Sekunde auf 5.000. Ihr System sollte jedoch resilient sein. Erfahren Sie mehr über [Begrenzung und Drosselung](../../configuration/external-systems.md).

**Beispiel eines Anwendungsfalls**: [Schreiben von Journey-Ereignissen in Experience Platform](../../building-journeys/custom-action-aep.md) unter Verwendung von benutzerdefinierten Aktionen.

## Arbeiten mit Journey Optimizer-APIs {#apis}

Journey Optimizer bietet umfassende REST-APIs für den programmgesteuerten Zugriff:

1. **Grundlegendes zu API-Funktionen**: Mit Journey Optimizer-APIs können Sie verschiedene Ressourcen programmgesteuert erstellen, lesen, aktualisieren und löschen. Erfahren Sie mehr über [Journey Optimizer-APIs](../../configuration/ajo-apis.md).

1. **Authentifizierung**: Befolgen Sie [dieses Tutorial](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}, um die API-Authentifizierung mit Adobe Developer Console einzurichten.

1. **Erkunden von API-Referenzen**: Sehen Sie sich die vollständige API-Dokumentation an und probieren Sie APIs direkt in der [Adobe Journey Optimizer-API-Referenz](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"} aus.

1. **Durch APIs ausgelöste Kampagnen**: Erstellen Sie Transaktions-Messaging mit durch APIs ausgelösten Kampagnen. Bei Szenarien mit hohem Volumen (bis zu 5.000 TPS) sollten Sie den [Modus mit hohem Durchsatz](../../campaigns/api-triggered-high-throughput.md) in Erwägung ziehen (Add-on-Lizenz erforderlich).

1. **Entscheidungs-Management-APIs**: Verwenden Sie spezielle APIs für Angebotsverwaltung und Entscheidungsfindung. Erfahren Sie mehr im [Handbuch zur Entscheidungs-Management-API](../../offers/api-reference/getting-started.md).

1. **Decisioning-Migrations-APIs**: Programmgesteuerte Migration von Entscheidungs-Management-Entitäten zu Decisioning mit flexiblen Bereichen, automatisierter Validierung und Rollback-Unterstützung. Weitere Informationen finden Sie im [Handbuch zur Decisioning-API](../../experience-decisioning/decisioning-migration-api.md).

1. **SMS-Webhooks**: Konfigurieren Sie eingehende Webhooks, um eingehende Nachrichten und Feedback-Webhooks zu erfassen, damit Versandbestätigungen und Statusaktualisierungen empfangen werden können. [Weitere Informationen](../../sms/sms-webhook.md).

## Testen und Debuggen {#testing}

1. **Debuggen der SDK-Implementierung**: Verwenden Sie Adobe Experience Platform Assurance, um SDK-Ereignisse zu untersuchen, die Datenerfassung zu validieren und Integrationsprobleme in Echtzeit zu beheben. [Erfahren Sie mehr über Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=de){target="_blank"}.

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

### Arbeiten mit kontextuellen Daten und Anreicherung

* **Iteration über Arrays**: Verwenden Sie die Handlebars-Syntax, um dynamische Listen aus Ereignissen, benutzerdefinierten Aktionsantworten und Datensatzsuchen in Nachrichten anzuzeigen. Erfahren Sie mehr über das [Iterieren über kontextuelle Daten](../../personalization/iterate-contextual-data.md).
* **Datensatzsuche**: Implementieren von Datensatzsuchen zur Anreicherung von Journey-Daten aus Adobe Experience Platform-Datensätzen. Arbeiten Sie bei der Konfiguration mit Ihrer Dateningenieurin bzw. Ihrem Dateningenieur zusammen. Erfahren Sie mehr über die [Datensatzsuche](../../building-journeys/dataset-lookup.md).

### Arbeiten mit Einverständnis und Governance

Implementieren von Data-Governance- und Einverständnisrichtlinien in Ihre Integrationen:

* **Data Governance**: Wenden Sie Datennutzungsrichtlinien auf benutzerdefinierte Aktionen an. Erfahren Sie mehr über [Data Governance](../../action/action-privacy.md).
* **Einverständnisverwaltung**: Verarbeiten Sie die Voreinstellungen für das Kundeneinverständnis in Ihren Implementierungen. Erfahren Sie mehr über [Einverständnis](../../action/consent.md).

### Optimierung und Best Practices

* **Begrenzung und Drosselung**: Machen Sie sich mit den Ratenbegrenzungen vertraut und implementieren Sie geeignete Drosselungen. Erfahren Sie mehr über [externe Systeme](../../configuration/external-systems.md).
* **Journey-Optimierung**: Befolgen Sie die Best Practices für die [Journey-Optimierung](../../building-journeys/optimize.md).
* **Fehlerbehandlung**: Implementieren Sie eine robuste Fehlerbehandlung. Sehen Sie sich [Fehler-Codes](../../building-journeys/error-codes-reference.md) und [Handbücher zur Fehlerbehebung](../../building-journeys/troubleshooting.md) an.

## Weitere Ressourcen {#additional-resources}

* **Developer Console**: Greifen Sie auf die [Adobe Developer Console](https://developer.adobe.com){target="_blank"} zu, um Integrationen zu erstellen und API-Anmeldedaten zu verwalten.
* **Beispiel-Code**: Sehen Sie sich [Beispielimplementierungen auf GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} an.
* **Video-Tutorials**: Lernen Sie durch praktische Tutorials auf [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=de){target="_blank"}.
* **Entwickler-Community**: Treten Sie mit anderen Entwickelnden in Kontakt und erhalten Sie Unterstützung in den Adobe-Community-Foren.

## Rollenübergreifendes Zusammenarbeiten {#next-steps}

Ihre Implementierungsarbeit überschneidet sich mit anderen Team-Mitgliedern:

>[!BEGINTABS]

>[!TAB Arbeiten mit Dateningenieurinnen und -ingenieuren]

Arbeiten Sie mit [Dateningenieurinnen und -ingenieuren](data-engineer.md) bei Daten und Ereigniskonfigurationen zusammen:

* Abrufen der XDM-Schemata und Ereignisstrukturen, die Sie implementieren müssen
* Verstehen, welche Ereignisse gesendet werden müssen und welches Payload-Format erforderlich ist
* Abstimmen der Anforderungen an die Datenerfassung und der Datenqualitätsstandards
* Gemeinsames Testen des Ereignisversands und der Datenaufnahme

>[!TAB Arbeiten mit Admins]

Arbeiten Sie mit [Admins](administrator.md) bei Zugriff und Konfigurationen zusammen:

* Angeben von API-Spezifikationen für benutzerdefinierte Aktionen, die sie konfigurieren
* Anfordern von erforderlichen Berechtigungen und API-Anmeldedaten
* Koordinieren der Anforderungen an die Kanalkonfiguration (z. B. Push-Zertifikate)
* Abstimmen zu Testumgebungen und Sandbox-Strategie

>[!TAB Arbeiten mit Marketing-Fachleuten]

Arbeiten Sie mit [Marketing-Fachleuten](marketer.md) bei Journey-Anforderungen und Tests zusammen:

* Verstehen, welche Benutzerinteraktionen Ereignisse auslösen sollen
* Implementieren des Trackings für Inhaltsleistung und Benutzerinteraktion
* Unterstützen von Tests von Journeys mit Ihren implementierten Funktionen
* Beheben von Problemen beim Nachrichtenversand oder bei der Personalisierung

>[!ENDTABS]

## Starten der Implementierung

Bereit, mit dem Erstellen zu beginnen? Wählen Sie Ihren ersten Implementierungsbereich aus den obigen Abschnitten:

1. **App?** Beginnen Sie mit der [Mobile SDK-Integration](#mobile-integration)
2. **Website?** Beginnen Sie mit der [Web SDK-Einrichtung](#web-implementation)
3. **API-Integration?** Wechseln Sie zu [Arbeiten mit APIs](#apis)
4. **Benutzerdefiniertes System?** Sehen Sie sich [benutzerdefinierte Aktionen](#custom-actions) an

Jeder Abschnitt enthält Links zu detaillierter technischer Dokumentation, Code-Beispielen und Tutorials, die Sie bei der Implementierung unterstützen.
