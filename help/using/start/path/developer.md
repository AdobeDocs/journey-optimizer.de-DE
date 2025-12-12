---
title: Erste Schritte für Entwickler
description: Hier erfahren Entwickler mehr über die Arbeit mit Journey Optimizer.
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '1891'
ht-degree: 2%

---

# Erste Schritte für Entwickler {#get-started-developers}

Als **Entwickler** sind Sie für die Implementierung und Integration von [!DNL Adobe Journey Optimizer] in Ihre Anwendungen und Systeme verantwortlich. Sie können mit [!DNL Adobe Journey Optimizer] arbeiten, sobald Ihnen [Systemadministrator](administrator.md) und der [Datentechniker](data-engineer.md) Zugriff gewährt und Ihre Umgebung vorbereitet haben.

## Ihre Rolle im Journey Optimizer-Ökosystem

Während andere Team-Mitglieder Journey Optimizer über die Benutzeroberfläche konfigurieren, konzentrieren Sie sich auf:

* **Implementieren von SDKs** in Mobile- und Web-Anwendungen
* **Senden von Ereignissen** von Ihren Programmen an Trigger-Journey
* **Erstellen von API-**), die Journey Optimizer über benutzerdefinierte Aktionen aufrufen kann
* **Integrieren** von Journey Optimizer mit vorhandenen Systemen und Infrastrukturen
* **Testen und Debuggen** Ihrer Implementierungen

Ihr [Dateningenieur](data-engineer.md) verarbeitet Datenschemata, Ereigniskonfigurationen und Datenquellen. Ihr [Administrator](administrator.md) richtet Berechtigungen und Kanalkonfigurationen ein. [Marketer](marketer.md) entwerfen die Journey und Inhalte, die Ihre Implementierungen verwenden.

In diesem Handbuch werden die wesentlichen technischen Implementierungsschritte für die ersten Schritte mit Journey Optimizer beschrieben. Gehen Sie wie folgt vor, um Ihre Implementierung einzurichten, unabhängig davon, ob Sie Mobile Apps, Web-Erlebnisse oder API-Integrationen erstellen.

## Voraussetzungen {#prerequisites}

Bevor Sie mit der Implementierung beginnen, stellen Sie Folgendes sicher:

**Technische Fähigkeiten:**

* Erfahrung mit JavaScript (für Web SDK) oder Swift/Kotlin (für Mobile SDK)
* Grundlegendes zu RESTful-APIs und JSON
* Vertrautheit mit asynchroner Programmierung und ereignisgesteuerten Architekturen
* Kenntnisse der Anwendungsarchitektur Ihres Unternehmens

**Zugriff und Tools:**

* Zugriff auf [Adobe Developer Console](https://developer.adobe.com){target="_blank"} für API-Anmeldeinformationen
* Entwicklungsumgebung mit Zugriff auf die Code-Basis Ihres Programms
* Test-Tools wie Postman für API-Tests
* Browser-Entwickler-Tools oder mobile Debugging-Tools

**Von anderen Team-Mitgliedern:**

* Umgebungszugriff durch Ihren [Administrator](administrator.md)
* XDM-Schemata und Ereignisdefinitionen von Ihrem [Data Engineer](data-engineer.md)
* Anforderungen und Anwendungsfälle von Ihren [Marketern](marketer.md)

## Technische Grundlagen {#technical-foundation}

Machen Sie sich mit den wichtigsten technischen Konzepten vertraut, bevor Sie sich mit der Implementierung befassen:

1. **Adobe Experience Platform-Integration**: Journey Optimizer basiert nativ auf Adobe Experience Platform. Wenn Sie die zugrunde liegende Architektur verstehen, können Sie effektivere Implementierungen erstellen. Erfahren Sie mehr über [Funktionsweise von Journey Optimizer](../understanding-ajo.md).

1. **XDM-Datenmodelle**: Journey Optimizer verwendet das Experience-Datenmodell (XDM), um Ereignis- und Profildaten zu strukturieren. Als Entwickler müssen Sie verstehen, wie Sie Daten senden, die den von Ihrem/Ihrem [ konfigurierten Schemata ](data-engineer.md). Informationen zu [XDM-Schemata](../../data/get-started-schemas.md).

1. **Authentifizierung und Sicherheit**: Alle Implementierungen erfordern eine ordnungsgemäße Authentifizierung. Erfahren Sie, wie Sie die Authentifizierung für SDKs und APIs einrichten. Erfahren Sie mehr über [API-](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

## Einrichten von Mobile-App-Integrationen {#mobile-integration}

### Konfigurieren der Adobe Experience Platform Mobile SDK

Um Push-Benachrichtigungen, In-App-Nachrichten und andere mobile Funktionen zu aktivieren, integrieren Sie die Adobe Experience Platform Mobile SDK in Ihre Mobile Apps.

1. **Installieren und Konfigurieren der Mobile SDK**: Befolgen Sie die [Dokumentation zu Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"} um mit der SDK-Integration zu beginnen.

1. **Eigenschaft für Mobilgeräte erstellen**: Richten Sie eine Eigenschaft für Mobilgeräte in [!DNL Adobe Experience Platform Data Collection] ein. Erfahren Sie, wie [eine Mobile-Eigenschaft erstellen und konfigurieren](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}.

1. **Konfigurieren von Push-Benachrichtigungen**:
   * Für **iOS-Apps**: Registrieren Sie Ihre App bei APNs (Apple Push Notification Service). Weitere Informationen finden Sie in der Dokumentation zu [Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Für **Android-Apps**: Richten Sie Firebase Cloud Messaging für Ihre Android-App ein. Weitere Informationen finden Sie in der Dokumentation zu [Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Mobile-Integration testen**: Verwenden Sie den [Schnellstart-Workflow für Mobile-Onboarding](../../push/mobile-onboarding-wf.md), um Ihre Mobile-Einrichtung schnell zu konfigurieren und zu testen.

Detaillierte Schritte zum Konfigurieren von Push-Benachrichtigungen finden Sie auf [dieser Seite](../../push/push-configuration.md).

### Implementieren von Code-basierten Erlebnissen (Mobile SDK)

Für die native Mobile-App-Personalisierung mithilfe von Code-basierten Erlebnissen:

* Folgen Sie [diesem Tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} für die Implementierung von Mobile SDK
* Überprüfen Sie die Beispielimplementierungen für [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} und [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}

## Implementieren von Web-Erlebnissen {#web-implementation}

### Einrichten der Adobe Experience Platform Web SDK

Bei Web-basierten Implementierungen ist die Web-SDK Ihr primärer Integrationspunkt:

1. **Installieren der Web-SDK**: Befolgen Sie die [Implementierungshandbuch für Web-SDK](https://experienceleague.adobe.com/de/docs/platform-learn/implement-web-sdk/overview){target="_blank"}, um die SDK auf Ihrer Website einzurichten.

1. **Datenströme konfigurieren**: Erstellen und konfigurieren Sie einen Datenstrom in [!DNL Adobe Experience Platform Data Collection] mit aktivierter Journey Optimizer. Weitere Informationen finden Sie in der [Dokumentation zu Datenströmen](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=de){target="_blank"}.

1. **Web-Push-Benachrichtigungen aktivieren** (optional): Konfigurieren Sie die [pushNotifications](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"}Eigenschaft in Ihrer Web-SDK-Konfiguration und verwenden Sie den [sendPushSubscription-Befehl](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"} zum Registrieren von Push-Abonnements.

### Implementieren von Code-basierten Erlebnissen (Web SDK)

Code-basierte Erlebnisse ermöglichen es Ihnen, jeden digitalen Touchpoint zu personalisieren:

1. **Wählen Sie Ihre Implementierungsmethode aus** Client-, Server-seitig oder Hybrid. Überprüfen Sie [Implementierungsbeispiele](../../code-based/code-based-implementation-samples.md) für jeden Ansatz.

1. **Oberflächen definieren**: Identifizieren Sie die Stellen in Ihrer Anwendung, an denen Sie personalisierte Inhalte bereitstellen möchten. Erfahren Sie mehr über [Oberflächenkonfiguration](../../code-based/code-based-surface.md).

1. **Implementieren des Content-Renderings**: Verwenden Sie die Web-SDK, um Personalisierungsinhalte abzurufen und anzuwenden. Siehe [Code-basierte Implementierungstutorials](../../code-based/code-based-decisioning-implementations.md).

1. **Anzeige- und Interaktionsereignisse senden**: Verfolgen Sie, wann Inhalte angezeigt werden und wann Benutzer damit interagieren, um sie zu analysieren und zu optimieren.

Erkunden Sie [Beispielimplementierungen auf GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}, um Code-basierte Erlebnisse in Aktion zu sehen.

Weitere Informationen über [Erste Schritte mit Code-basierten Erlebnissen](../../code-based/get-started-code-based.md).

## Ereignis-Streaming implementieren {#event-streaming}

### Ereignisse an Trigger-Journey senden

Als Entwickler implementieren Sie den Code zum Senden von Ereignissen, die Trigger-Journey senden. Ihr [Dateningenieur](data-engineer.md) konfiguriert die Ereignisschemata und -definitionen in Journey Optimizer.

1. **Ereignis-Payload verstehen**: Wenden Sie sich an Ihren Dateningenieur, um das Ereignisschema und die erforderliche Payload-Struktur zu erhalten. Die Payload muss dem konfigurierten XDM-Schema entsprechen. Erfahren Sie mehr über [Anforderungen an Ereignisschemas](../../event/experience-event-schema.md).

1. **Ereignis-Streaming implementieren**: Senden von Ereignissen an Adobe Experience Platform mithilfe der [Streaming-Aufnahme-APIs](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=de){target="_blank"}. Erfahren Sie [Schritte zum Senden von Ereignissen](../../event/additional-steps-to-send-events-to-journey.md).

1. **Ereignistypen verarbeiten**:
   * **Unitäre Ereignisse**: Implementieren des Ereignisversands für personenspezifische Aktionen (z. B. Button-Klick, Kaufabschluss)
   * **Geschäftsereignisse**: Senden von geschäftlichen Ereignissen (z. B. Bestandsaktualisierungen, Preisänderungen)

1. **Ereignisversand testen**: Überprüfen Sie, ob die Ereignisse ordnungsgemäß empfangen wurden und die Trigger-Journey wie erwartet funktionieren. Erfahren Sie mehr über [Fehlerbehebung bei Ereignissen](../../building-journeys/troubleshooting-inbound.md).

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

Weitere Informationen über [Arbeiten mit Journey-Ereignissen](../../event/about-events.md).

## Entwickeln benutzerdefinierter Aktionsendpunkte {#custom-actions}

Benutzerdefinierte Aktionen ermöglichen es Journey, Ihre APIs aufzurufen. Als Entwickler erstellen Sie die API-Endpunkte, die durch benutzerdefinierte Aktionen aufgerufen werden:

1. **API-Endpunkt erstellen**: Erstellen Sie RESTful-API-Endpunkte, die Journey Optimizer während der Journey-Ausführung aufruft. Ihr Endpunkt sollte:
   * Akzeptieren von JSON-Payloads
   * Authentifizierungsanfragen (OAuth, API-Schlüssel oder JWT)
   * Anforderungen innerhalb angemessener Zeitlimits verarbeiten
   * Antworten im erwarteten Format zurückgeben

1. **Grundlegendes zu den** von benutzerdefinierten Aktionen: Benutzerdefinierte Aktionen können eine Verbindung zu Drittanbietersystemen wie Epsilon, Slack, Firebase oder Ihren eigenen Services herstellen. Weitere Informationen über [benutzerdefinierte Aktionen](../../action/action.md).

1. **Arbeiten mit Aktionskonfigurationen**: Ihr [Administrator](administrator.md) oder [Datentechniker](data-engineer.md) konfiguriert die benutzerdefinierte Aktion in Journey Optimizer und definiert die API-Endpunkt-URL, Authentifizierungsmethode und Parameter. Sie geben ihnen Ihre API-Spezifikation. Erfahren Sie mehr über [Konfiguration benutzerdefinierter Aktionen](../../action/about-custom-action-configuration.md).

1. **Verwertbare Daten zurückgeben**: Entwerfen Sie Ihre API, um Daten zurückzugeben, die in nachfolgenden Journey-Schritten verwendet werden können. Erfahren Sie mehr [Aktionsantworten](../../action/action-response.md).

1. **Ratenbegrenzung implementieren**: Stellen Sie sicher, dass Ihre Endpunkte das erwartete Volumen verarbeiten können. Journey Optimizer begrenzt die Anzahl der Aufrufe pro Sekunde auf 5.000. Ihr System sollte jedoch robust sein. Erfahren Sie mehr [Begrenzung und Drosselung](../../configuration/external-systems.md).

**Anwendungsbeispiel**: [Schreiben von Journey-Ereignissen in Experience Platform](../../building-journeys/custom-action-aep.md) Verwenden benutzerdefinierter Aktionen.

## Arbeiten mit Journey Optimizer-APIs {#apis}

Journey Optimizer bietet umfassende REST-APIs für den programmgesteuerten Zugriff:

1. **Grundlegendes zu API** Funktionen: Mit Journey Optimizer-APIs können Sie verschiedene Ressourcen programmgesteuert erstellen, lesen, aktualisieren und löschen. Erfahren Sie mehr über [Journey Optimizer-](../../configuration/ajo-apis.md).

1. **Authentifizierung**: Befolgen Sie [dieses Tutorial](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}, um die API-Authentifizierung mit Adobe Developer Console einzurichten.

1. **API-Referenzen erkunden**: Durchsuchen Sie die vollständige API-Dokumentation und probieren Sie APIs direkt in der [Adobe Journey Optimizer-API-Referenz](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"} aus.

1. **API-ausgelöste**: Erstellen Sie Transaktionsnachrichten mit API-ausgelösten Kampagnen. Bei Szenarien mit hohem Volumen (bis zu 5.000 TPS) sollten Sie den [Hochdurchsatzmodus“ ](../../campaigns/api-triggered-high-throughput.md)Add-on-Lizenz erforderlich).

1. **Entscheidungs-Management-**: Verwenden Sie spezielle APIs für Angebotsverwaltung und Entscheidungsfindung. Weitere Informationen finden Sie im [Handbuch zur Entscheidungs-Management-API](../../offers/api-reference/getting-started.md).

## Testen und Debuggen {#testing}

1. **SDK-Implementierung debuggen**: Verwenden Sie Adobe Experience Platform Assurance, um SDK-Ereignisse zu untersuchen, die Datenerfassung zu validieren und Integrationsprobleme in Echtzeit zu beheben. [Weitere Informationen zu Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=de){target="_blank"}.

1. **Ereignisversand testen**: Überprüfen Sie, ob Ereignisse aus Ihrer Anwendung von Adobe Experience Platform und den Trigger-Journey korrekt und wie erwartet empfangen werden. Überwachen der Ereignisaufnahme und Überprüfen der Payload-Struktur.

1. **Validieren von API-Integrationen**: Testen Sie Ihre benutzerdefinierten Aktionsendpunkte, um sicherzustellen, dass sie Journey Optimizer-Anfragen korrekt verarbeiten, innerhalb der Zeitüberschreitungsgrenzen reagieren und die erwarteten Datenformate zurückgeben.

1. **Testmodus mit Testprofilen verwenden**: Wenden Sie sich an Ihren [Dateningenieur](data-engineer.md), um Zugriff auf Testprofile zu erhalten, und validieren Sie dann Ihre Implementierung mithilfe des Journey-Testmodus. Erfahren Sie, wie [Journey testen](../../building-journeys/testing-the-journey.md).

1. **SDK-Protokolle überwachen**: Aktivieren Sie die Debug-Protokollierung in Ihrer SDK-Implementierung, um Probleme während der Entwicklung zu beheben:
   * **Mobile SDK**: Aktivieren der Protokollierung, um SDK-Ereignisse und API-Aufrufe anzuzeigen
   * **Web SDK**: Verwenden Sie die Browser-Konsole, um die Aktivität von SDK zu überwachen

1. **Überprüfen der Datenstromkonfiguration**: Stellen Sie sicher, dass Ihr Datenstrom ordnungsgemäß konfiguriert ist, um Daten an Journey Optimizer zu senden. Überprüfen Sie, ob Ereignisse durch den Datenstrom zu den richtigen Zielen fließen.

1. **Abfrage von Journey-Daten für die Analyse**: Verwenden Sie SQL-Abfragen im Data Lake, um Journey-Schrittereignisse zu analysieren, Probleme zu debuggen und die Leistung benutzerdefinierter Aktionen zu überwachen. Erkunden Sie [Abfragebeispiele für die Journey-Analyse](../../reports/query-examples.md) einschließlich:
   * Tracking von Profileintritten/Austritten und Verwerfen von Gründen
   * Leistungsmetriken für benutzerdefinierte Aktionen (Latenz, Durchsatz, Fehler)
   * Ereignisversand- und Fehlermuster
   * Journey-Instanzstatus

## Fortgeschrittene Entwicklerthemen {#advanced-topics}

### Arbeiten mit kontextuellen Daten und Anreicherungen

* **Iteration über Arrays**: Verwenden Sie die Handlebars-Syntax, um dynamische Listen aus Ereignissen, benutzerdefinierten Aktionsantworten und Datensatzsuchen in Nachrichten anzuzeigen. Erfahren Sie mehr über [Iterieren von kontextuellen Daten](../../personalization/iterate-contextual-data.md).
* **Datensatzsuche**: Implementieren von Datensatzsuchen zur Anreicherung von Journey-Daten aus Adobe Experience Platform-Datensätzen. Arbeiten Sie bei der Konfiguration mit Ihrem Dateningenieur zusammen. Weitere Informationen [Datensatzsuche](../../building-journeys/dataset-lookup.md).

### Arbeiten mit Einverständnis und Governance

Implementieren von Data Governance- und Einverständnisrichtlinien in Ihre Integrationen:

* **Data Governance**: Wenden Sie Datennutzungsrichtlinien auf benutzerdefinierte Aktionen an. Weitere Informationen zu [Data Governance](../../action/action-privacy.md).
* **Einverständnisverwaltung**: Handhabung der Voreinstellungen für das Kundeneinverständnis in Ihren Implementierungen. Weitere Informationen zu [Zustimmung](../../action/consent.md).

### Optimierung und Best Practices

* **Begrenzung und Drosselung**: Machen Sie sich mit den Ratenbeschränkungen vertraut und implementieren Sie geeignete Drosselungen. Informationen zu [externen Systemen](../../configuration/external-systems.md).
* **Journey-Optimierung**: Befolgen Sie die Best Practices für die [Journey-Optimierung](../../building-journeys/optimize.md).
* **Fehlerbehandlung**: Implementieren Sie eine robuste Fehlerbehandlung. Lesen Sie [Fehlercodes](../../building-journeys/error-codes-reference.md) und [Handbücher zur Fehlerbehebung](../../building-journeys/troubleshooting.md).

## Weitere Ressourcen {#additional-resources}

* **Developer Console**: Greifen Sie auf die [Adobe Developer Console](https://developer.adobe.com){target="_blank"} zu, um Integrationen zu erstellen und API-Anmeldeinformationen zu verwalten.
* **Beispielcode**: Erkunden Sie [Beispielimplementierungen auf GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **Anleitungsvideos**: Lernen Sie durch praktische Tutorials zu [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=de){target="_blank"}.
* **Entwickler-Community**: Treten Sie mit anderen Entwicklern in Kontakt und erhalten Sie Unterstützung in den Adobe-Community-Foren.

## Rollenübergreifend zusammenarbeiten {#next-steps}

Ihre Implementierungsarbeit überschneidet sich mit anderen Team-Mitgliedern:

**Arbeiten mit [Dateningenieuren](data-engineer.md):**

* Abrufen der XDM-Schemata und Ereignisstrukturen, die Sie implementieren müssen
* Verstehen, welche Ereignisse gesendet werden müssen, und deren erforderliches Payload-Format
* Angleichung der Anforderungen an die Datenerfassung und der Datenqualitätsstandards
* Gemeinsames Testen des Versands und der Datenaufnahme

**Arbeiten mit [Administratoren](administrator.md):**

* Angeben von API-Spezifikationen für benutzerdefinierte Aktionen, die sie konfigurieren werden
* Erforderliche Berechtigungen und API-Anmeldedaten anfordern
* Koordinieren der Anforderungen an die Kanalkonfiguration (z. B. Push-Zertifikate)
* Ausrichtung an Testumgebungen und Sandbox-Strategie

**Arbeiten mit [Marketern](marketer.md):**

* Verstehen, welche Benutzerinteraktionen Trigger-Ereignisse auslösen sollen
* Implementieren des Trackings für Content-Performance und Benutzerinteraktion
* Unterstützen von Tests von Journey mit Ihren implementierten Funktionen
* Fehlerbehebung bei Problemen beim Nachrichtenversand oder bei der Personalisierung

## Auf dem Laufenden bleiben

Halten Sie sich über die neuesten Journey Optimizer-Funktionen und technischen Änderungen auf dem Laufenden:

* **[Versionshinweise](../../rn/release-notes.md)** Überprüfen Sie jeden Monat neue Funktionen, API-Änderungen, SDK-Updates und Fehlerbehebungen
* **[Dokumentationsaktualisierungen](../../rn/documentation-updates.md)**: Verfolgen Sie aktuelle Änderungen an der technischen Dokumentation, einschließlich neuer Implementierungshandbücher und Code-Beispiele
* **Produktbenachrichtigungen**: Aktivieren Sie Benachrichtigungen in Ihrem [Adobe Experience Cloud-Profil](https://experience.adobe.com/preferences){target="_blank"} um Warnhinweise zu erhalten:
   * Neue SDK-Versionen und API-Aktualisierungen
   * Umfassende Änderungen und Veraltungen
   * Wartungsfenster mit Auswirkung auf Integrationen
   * Wichtige Sicherheits-Updates

  Um Benachrichtigungen zu aktivieren, klicken Sie auf Ihr Profilsymbol oben rechts in Adobe Experience Cloud, gehen Sie zu **Voreinstellungen > Benachrichtigungen** und konfigurieren Sie Ihre Journey Optimizer-Benachrichtigungseinstellungen.

## Mit der Implementierung beginnen

Bereit mit dem Bau zu beginnen? Wählen Sie Ihren ersten Implementierungsbereich aus den obigen Abschnitten:

1. **Mobile App?** Schritte mit der [Mobile SDK-Integration](#mobile-integration)
2. **Website?** Erste Schritte mit [Einrichten von Web SDK](#web-implementation)
3. **API-Integration?** Wechseln zu [Arbeiten mit APIs](#apis)
4. **Benutzerdefiniertes System?** Auschecken [benutzerdefinierte Aktionen](#custom-actions)

Jeder Abschnitt enthält Links zu detaillierten technischen Dokumentationen, Code-Beispielen und Tutorials, die Sie bei der Implementierung unterstützen.
