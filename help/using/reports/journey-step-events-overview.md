---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit Journey-Schrittereignissen
description: Informationen zur Arbeit mit Journey-Schrittereignissen in Journey Optimizer und Grundlegendes dazu, was sie sind, wieso sie wichtig sind und wie sie für Analyse und Optimierung verwendet werden
feature: Journeys, Reporting
role: Developer, Admin, User
level: Intermediate, Experienced
keywords: Journey, Schrittereignisse, Analyse, Reporting, Monitoring, XDM
exl-id: 2e7c5ea5-d8c5-416d-ab88-d2bc02043558
TQID: https://experienceleague.adobe.com/PSXSN-31GNlM0zBKcCvdKPciHt5zhQPPCffFrUoIxUs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 937
ht-degree: 98%

---

# Arbeiten mit Journey-Schrittereignissen {#work-with-journey-step-events}

Journey-Schrittereignisse sind automatisch generierte Ereignisse, die detaillierte Informationen zu jedem Schritt erfassen, den ein [Profil](../audience/get-started-profiles.md) beim Fortschreiten in einer [Journey](../building-journeys/journey.md) in Adobe Journey Optimizer durchläuft. Diese Ereignisse bieten umfassende Einblicke in die [Journey-Leistung](../building-journeys/report-journey.md) und ermöglichen leistungsstarke Analysefunktionen.

## Was sind Journey-Schrittereignisse? {#what-are-step-events}

Journey-Schrittereignisse sind systemgenerierte [XDM-Ereignisse (Experience-Datenmodell)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"}, die Adobe Journey Optimizer automatisch erstellt und an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=de){target="_blank"} sendet, wenn ein Profil sich in einer Journey von einem Knoten zu einem anderen bewegt. Jedes Ereignis entspricht einer bestimmten [Journey-Aktivität](../building-journeys/about-journey-activities.md) oder Transition im Journey-Erlebnis der Kundin bzw. des Kunden.

Es gibt zwei Haupttypen von Journey-Schrittereignissen:

- **journeyStepEvent**: Ereignisse im Zusammenhang mit dem Fortschritt einzelner Profile durch Journey-Schritte
- **journeyStepProfileEvent**: Ereignisse, die zusätzliche Profilkontextinformationen enthalten

### Wodurch werden Journey-Schrittereignisse ausgelöst? {#event-triggers}

Journey-Schrittereignisse werden automatisch für verschiedene Journey-Aktivitäten generiert:

- **Eintrittsereignisse**: Wenn ein Profil [in eine Journey eintritt](../building-journeys/entry-management.md)
- **Aktionsausführung**: Wenn [Nachrichten gesendet werden](../building-journeys/journey-action.md) oder [benutzerdefinierte Aktionen](../building-journeys/using-custom-actions.md) ausgeführt werden
- **Bedingungsauswertung**: Wenn Profile [Bedingungen](../building-journeys/conditions.md) und Entscheidungspunkte durchlaufen
- **Warteaktivitäten**: Wenn Profile in [Warteknoten](../building-journeys/wait-activity.md) eintreten und aus ihnen aussteigen
- **Ausstiegsereignisse**: Wenn Profile [aus einer Journey aussteigen](../building-journeys/end-journey.md)
- **Fehlerbehandlung**: Wenn bei der Journey-Ausführung Fehler auftreten

>[!NOTE]
>
>Journey-Schrittereignisse sind standardmäßig auf allen Instanzen aktiviert. Sie können die bei der Bereitstellung für Schrittereignisse erstellten [Schemata und Datensätze](sharing-overview.md) nicht ändern oder aktualisieren. Diese Schemata und Datensätze sind schreibgeschützt.

Erfahren Sie mehr über [Journey-Schrittereignisschemata](sharing-field-list.md).

## Bedeutung von Journey-Schrittereignissen {#why-step-events-matter}

Journey-Schrittereignisse bieten einen entscheidenden Wert für Organisationen, die Adobe Journey Optimizer verwenden:

### Echtzeit-Analyse und -Monitoring {#real-time-analytics}

- **Tracking der Journey-Leistung**: Überwachen Sie mithilfe von [Live-Berichten](live-report.md) in Echtzeit, wie Profile Ihre Journey durchlaufen
- **Konversionsanalyse**: Erfahren Sie durch [Journey-Analysen](journey-global-report-cja.md) mehr zu Abbruchpunkten und erfolgreichen Konversionspfaden
- **Fehlererkennung**: Identifizieren und beheben Sie durch [Monitoring und Warnhinweise](alerts.md) Probleme, sofort nachdem diese auftreten

### Datenintegration und Erkenntnisse {#data-integration}

- **Plattformübergreifende Analyse**: Kombinieren Sie Journey-Daten mit anderen [Adobe Experience Platform-Datenquellen](../datasource/adobe-experience-platform-data-source.md)
- **360-Grad-Kundenansicht**: Erstellen Sie umfassende [Kundenprofile](../audience/get-started-profiles.md), die Journey-Interaktionen beinhalten
- **Attributionsmodellierung**: Verbinden Sie mithilfe von [Customer Journey Analytics](cja-ajo.md) Journey-Touchpoints mit nachgelagerten Geschäftsergebnissen

### Optimierungsmöglichkeiten {#optimization}

- **A/B-Testerkenntnisse**: Analysieren Sie mithilfe von [Experimenten](campaign-global-report-cja-experimentation.md) die Leistung verschiedener Journey-Pfade
- **Verbesserung der Personalisierung**: Verwenden Sie Journey-Verhaltensdaten, um zukünftige Erlebnisse mit [dynamischen Inhalten](../personalization/dynamic-content.md) zu verbessern
- **Betriebliche Effizienz**: Identifizieren Sie Engpässe und optimieren Sie das [Journey-Design](../building-journeys/using-the-journey-designer.md)

## Verwenden von Journey-Schrittereignissen {#how-to-use-step-events}

### Zugreifen auf Daten von Journey-Schrittereignissen {#accessing-data}

Daten von Journey-Schrittereignissen werden automatisch in Adobe Experience Platform gespeichert und können wie folgt aufgerufen werden:

1. **Data-Lake-Abfragen**: Verwenden Sie SQL, um den `journey_step_events`-Datensatz mit dem [Abfrage-Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=de){target="_blank"} abzufragen
2. **Customer Journey Analytics**: Analysieren Sie Journey-Daten mit [erweiterten Analyse-Tools](cja-ajo.md)
3. **Echtzeit-Reporting**: Greifen Sie über die [nativen Reporting-Funktionen](gs-reports.md) von Journey Optimizer auf Daten zu
4. **APIs**: Greifen Sie programmgesteuert auf Ereignisdaten für benutzerdefinierte Anwendungen zu

Erfahren Sie mehr über den [Zugriff auf Datensätze](../data/datasets-query-examples.md).

### Wichtige verfügbare Datenpunkte {#key-data-points}

Journey-Schrittereignisse erfassen umfassende Informationen, darunter:

- **Journey-Identifizierung**: [Journey-ID, -Version und -Name](sharing-journey-fields.md)
- **Profilinformationen**: [Profil-ID und zugehörige Identitäten](sharing-identity-fields.md)
- **Schrittdetails**: [Knotenname, Schritttyp und Ausführungsstatus](sharing-common-fields.md)
- **Zeitstempel**: Präzises Timing für jeden Journey-Schritt
- **Aktionsergebnisse**: [Erfolgs-/Fehlerstatus und Ausführungsdetails](sharing-execution-fields.md)
- **Fehlerinformationen**: Detaillierte [Fehler-Codes und -beschreibungen](sharing-field-list.md#discarded-events) bei Problemen

Erkunden Sie alle [verfügbaren Felddefinitionen](sharing-field-list.md).

### Häufige Anwendungsfälle {#common-use-cases}

**Leistungs-Monitoring**

```sql
-- Example: Count profiles entering a journey in the last 24 hours
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-id>'
AND _experience.journeyOrchestration.stepEvents.nodeType='start'
AND DATE(timestamp) > (now() - interval '24' hour);
```

**Fehleranalyse**

```sql
-- Example: Identify errors by journey node
SELECT _experience.journeyOrchestration.stepEvents.nodeName,
       count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName;
```

**Journey-Trichteranalyse**

- Nachverfolgen von Konversionsraten bei jedem Journey-Schritt
- Identifizieren, wo Profile am häufigsten aus der Journey aussteigen
- Messen der in verschiedenen Journey-Phasen verbrachten Zeit

Weitere Informationen finden Sie unter [Abfragetechniken für die Trichteranalyse](query-examples.md#common-queries).

## Beispiele und Ressourcen {#samples-resources}

### Abfragebeispiele und Vorlagen {#query-examples}

Erkunden Sie umfassende Abfragebeispiele für gängige Journey-Schrittereignisanalysen:

- **[Beispiele für Journey-Schrittereignisabfragen](query-examples.md)**: Einsatzbereite SQL-Abfragen für gängige Analyseszenarien
- **[Beispiele für Datensatzabfragen](../data/datasets-query-examples.md#journey-step-event)**: Beispiele für das Abfragen von Journey-Schrittereignisdatensätzen
- **[Profilbasierte Abfragen](query-examples.md#profile-based-queries)**: Verfolgen von individuellen Profil-Journeys und -Interaktionen

### Felddokumentation {#field-documentation}

Machen Sie sich mit der vollständigen Datenstruktur von Journey-Schrittereignissen vertraut:

- **[Liste mit Journey-Schrittereignisfeldern](sharing-field-list.md)**: Umfassende Sammlung aller verfügbaren Felder
- **[Gemeinsame Felder](sharing-common-fields.md)**: Freigegebene Felder in journeyStepEvent und journeyStepProfileEvent
- **[Aktionsausführungsfelder](sharing-execution-fields.md)**: Für das Tracking der Aktionsausführung spezifische Felder
- **[Journey-Felder](sharing-journey-fields.md)**: Journey-spezifische Metadaten und Kennungen

### Best Practices und Fehlerbehebung {#best-practices}

**Leistungsoptimierung**

- Verwenden Sie `journeyVersionID` anstelle von `journeyVersionName` zum Erzielen einer besseren Abfrageleistung ([Informationen zu Journey-Eigenschaften](../building-journeys/expression/journey-properties.md))
- Filtern Sie nach Datumsbereichen, um die Abfragegeschwindigkeit für große Datensätze zu verbessern
- Nutzen Sie Profilidentitäten, die Ihrer [Journey-Namespace-Konfiguration](../building-journeys/entry-management.md) entsprechen

**Datenqualität**

- Überprüfen Sie regelmäßig auf [verworfene Ereignisse](sharing-field-list.md#discarded-events), um Datenprobleme zu identifizieren
- Überprüfen Sie, ob Ereignisschemata Ihren Analyseanforderungen entsprechen
- Implementieren Sie eine ordnungsgemäße Fehlerbehandlung in benutzerdefinierten Abfragen

**Analysestrategien**

- Kombinieren Sie Journey-Schrittereignisse mit [Nachrichten-Feedback-Daten](../data/datasets-query-examples.md#message-feedback-event-dataset) für vollständige Attribution
- Verwenden Sie zeitbasierte Analysen zum Verstehen von Journey-Geschwindigkeit und Engpässen

### Erweiterte Analysefunktionen {#advanced-analytics}

**Customer Journey Analytics-Integration**
Journey-Schrittereignisse können mit [Customer Journey Analytics](cja-ajo.md) analysiert werden für:

- Erweiterte Attributionsmodellierung
- Cross-Channel-Journey-Visualisierung
- Prädiktive Analyse der Journey-Ergebnisse

Erfahren Sie, wie Sie [Customer Journey Analytics](report-gs-cja.md) für Journey Optimizer-Daten konfigurieren.

## Weitere Ressourcen {#additional-resources}

### Links zur Dokumentation {#documentation-links}

- **[Überblick über die Freigabe von Journey-Schritten](sharing-overview.md)**: Grundlegendes zum Erfassen von Journey-Daten in Adobe Experience Platform
- **[Wörterbuch zu nativen Schemata](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=de){target="_blank"}**: Vollständige XDM-Schemareferenz
- **[Journey Optimizer-Reporting](report-gs-cja.md)**: Überblick über die Reporting-Funktionen in Journey Optimizer

### Integrationsanleitung {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)**: Analysieren von Journey Optimizer-Daten in CJA
- **[Daten-Management](../data/export-datasets.md)**: Exportieren und Verwalten von Journey-Daten
- **[Datenschutz und Governance](../privacy/audit-logs.md)**: Überlegungen zur Data Governance bei Journey-Ereignissen


**Nächste Schritte:**

- Beginnen Sie mit dem [Erstellen Ihrer ersten Journey-Berichte](sharing-overview.md)
- Erkunden Sie [Abfragebeispiele](query-examples.md) für bestimmte Anwendungsfälle
- Weitere Informationen zu [Best Practices für das Journey-Management](../building-journeys/journey.md)
