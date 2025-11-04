---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit Journey-Schrittereignissen
description: Erfahren Sie, wie Sie mit Journey-Schrittereignissen in Adobe Journey Optimizer arbeiten - verstehen Sie, was sie sind, warum sie wichtig sind und wie Sie sie für Analysen und Optimierungen verwenden können
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin, User
level: Intermediate, Experienced
keywords: Journey, Schrittereignisse, Analysen, Reporting, Überwachung, XDM
source-git-commit: 9320777cfb75fd1370c11b601908644ba17ff21e
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 2%

---

# Arbeiten mit Journey-Schrittereignissen {#work-with-journey-step-events}

Journey-Schrittereignisse sind automatisch generierte Ereignisse, die detaillierte Informationen zu jedem Schritt erfassen[&#x200B; den ein &#x200B;](../audience/get-started-profiles.md) durchläuft, während sie eine [Journey](../building-journeys/journey.md) in Adobe Journey Optimizer durchlaufen. Diese Ereignisse bieten umfassende Einblicke in die [Journey-Leistung](../building-journeys/report-journey.md) und ermöglichen leistungsstarke Analysefunktionen.

## Was sind Journey-Schrittereignisse? {#what-are-step-events}

Journey-Schrittereignisse sind systemgenerierte [XDM (Experience-Datenmodell)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"}-Ereignisse, die Adobe Journey Optimizer automatisch erstellt und an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=de){target="_blank"} sendet, wenn ein Profil auf einem Journey von einem Knoten zu einem anderen wechselt. Jedes Ereignis entspricht einer bestimmten [Journey-Aktivität &#x200B;](../building-journeys/about-journey-activities.md) Transition im Journey-Erlebnis des Kunden.

Es gibt zwei Haupttypen von Journey-Schrittereignissen:

- **journeyStepEvent**: Ereignisse im Zusammenhang mit dem Fortschritt einzelner Profile durch Journey-Schritte
- **journeyStepProfileEvent**: Ereignisse, die zusätzliche Profilkontextinformationen enthalten

### Welche Trigger Journey-Schrittereignisse? {#event-triggers}

Journey-Schrittereignisse werden automatisch für verschiedene Journey-Aktivitäten generiert:

- **Eintrittsereignisse**: Wenn ein Profil [auf eine Journey gelangt](../building-journeys/entry-management.md)
- **Aktionsausführung**: Wenn [Nachrichten gesendet werden](../building-journeys/journeys-message.md) oder [benutzerdefinierte Aktionen](../building-journeys/using-custom-actions.md) ausgeführt werden
- **Bedingungsauswertung**: Wenn Profile [Bedingungen](../building-journeys/condition-activity.md) und Entscheidungspunkte durchlaufen
- **Warteaktivitäten**: Beim Eintreten und Verlassen von Profilen [Warteknoten](../building-journeys/wait-activity.md)
- **Beendigungsereignisse**: Wenn Profile abgeschlossen sind oder [eine Journey beenden](../building-journeys/end-journey.md)
- **Fehlerbehandlung**: Wenn bei der Journey-Ausführung Fehler auftreten

>[!NOTE]
>
>Journey-Schrittereignisse sind standardmäßig auf allen Instanzen aktiviert. Sie können die ([&#x200B; und Datensätze), &#x200B;](sharing-overview.md) bei der Bereitstellung für Schrittereignisse erstellt wurden, nicht ändern oder aktualisieren. Diese Schemata und Datensätze befinden sich im schreibgeschützten Modus.

Weitere Informationen zu [Journey-Schrittereignisschemata](sharing-field-list.md).

## Warum Journey-Schrittereignisse wichtig sind {#why-step-events-matter}

Journey-Schrittereignisse bieten einen entscheidenden Wert für Unternehmen, die Adobe Journey Optimizer verwenden:

### Echtzeit-Analyse und -Überwachung {#real-time-analytics}

- **Journey-Leistungs-Tracking**: Überwachen Sie mithilfe von Live[Berichten in Echtzeit, wie Profile durch Ihre Journey fließen](live-report.md)
- **Konversionsanalyse**: Mit [Journey-Analysen lernen Sie Abbruchpunkte und erfolgreiche Konversionspfade kennen](journey-global-report-cja.md)
- **Fehlererkennung**: Identifizieren und Beheben von Problemen, während sie durch [Überwachung und Warnhinweise](alerts.md) auftreten

### Datenintegration und Erkenntnisse {#data-integration}

- **Plattformübergreifende Analyse**: Kombinieren Sie Journey-Daten mit anderen [Adobe Experience Platform-Datenquellen](../datasource/adobe-experience-platform-data-source.md)
- **Kunden-360-Ansicht**: Erstellen Sie umfassende [Kundenprofile](../audience/get-started-profiles.md) die Journey-Interaktionen beinhalten
- **Attributionsmodellierung**: Verbinden von Journey-Touchpoints mit nachgelagerten Geschäftsergebnissen mithilfe von [Customer Journey Analytics](cja-ajo.md)

### Optimierungsmöglichkeiten {#optimization}

- **A/B-Testeinblicke**: Analysieren der Performance verschiedener Journey-Pfade mithilfe von [Experimentieren](campaign-global-report-cja-experimentation.md)
- **Personalization-Verbesserung**: Verwenden Sie Journey-Verhaltensdaten, um zukünftige Erlebnisse mit ([&#x200B; Inhalten) &#x200B;](../personalization/dynamic-content.md) verbessern
- **Betriebseffizienz**: Ermittlung von Engpässen und Optimierung des [Journey-Designs](../building-journeys/using-the-journey-designer.md)

## Verwenden von Journey-Schrittereignissen {#how-to-use-step-events}

### Zugreifen auf Journey-Schritt-Ereignisdaten {#accessing-data}

Journey-Schrittereignisdaten werden automatisch in Adobe Experience Platform gespeichert und können wie folgt aufgerufen werden:

1. **Data Lake-Abfragen**: Verwenden Sie SQL, um den `journey_step_events`-Datensatz mit dem [Abfrage-Service) &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=de){target="_blank"}
2. **Customer Journey Analytics**: Analysieren von Journey-Daten mit [erweiterten Analyse-Tools](cja-ajo.md)
3. **Echtzeit-Reporting**: Zugriff auf Daten über die [&#x200B; Reporting-Funktionen von Journey Optimizer](gs-reports.md)
4. **APIs**: Programmgesteuerter Zugriff auf Ereignisdaten für benutzerdefinierte Programme

Weitere Informationen über [Zugriff auf Datensätze](../data/datasets-query-examples.md).

### Wichtige verfügbare Datenpunkte {#key-data-points}

Journey-Schrittereignisse erfassen umfassende Informationen, darunter:

- **Journey-Identifizierung**: [Journey-ID, Version und Name](sharing-journey-fields.md)
- **Profilinformationen**: [Profil-ID und zugehörige Identitäten](sharing-identity-fields.md)
- **Schrittdetails**: [Knotenname, Schritttyp und Ausführungsstatus](sharing-common-fields.md)
- **Zeitstempel**: Präzise Zeitplanung für jeden Journey-Schritt
- **Aktionsergebnisse**: [Erfolgs-/Fehlerstatus und Ausführungsdetails](sharing-execution-fields.md)
- **Fehlerinformationen**: Detaillierte [Fehlercodes und -beschreibungen](sharing-field-list.md#discarded-events) wenn Probleme auftreten

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

**Journey funnel Analysis**

- Konversionsraten bei jedem Journey-Schritt verfolgen
- Identifizieren Sie, wo Profile am häufigsten die Journey verlassen
- Messen der Besuchszeit in verschiedenen Journey-Phasen

Weitere Informationen [Abfragetechniken für die funnel-Analyse](query-examples.md#common-queries).

## Beispiele und Ressourcen {#samples-resources}

### Abfragebeispiele und Vorlagen {#query-examples}

Erkunden Sie umfassende Abfragebeispiele für die gängige Journey-Schrittereignisanalyse:

- **[Beispiele für Journey-Schrittereignisabfragen](query-examples.md)**: Einsatzbereite SQL-Abfragen für gängige Analyseszenarien
- **[Beispiele für Datensatzabfragen](../data/datasets-query-examples.md#journey-step-event)**: Beispiele für das Abfragen von Journey-Schritt-Ereignisdatensätzen
- **[Profilbasierte Abfragen](query-examples.md#profile-based-queries)**: Verfolgen Sie einzelne Journey und Interaktionen des Profils

### Felddokumentation {#field-documentation}

Machen Sie sich mit der vollständigen Datenstruktur von Journey-Schrittereignissen vertraut:

- **[Journey-Schritt-Ereignisfeldliste](sharing-field-list.md)**: Umfassende Referenz aller verfügbaren Felder
- **[Gemeinsame Felder](sharing-common-fields.md)**: Freigegebene Felder in journeyStepEvent und journeyStepProfileEvent
- **[Aktionsausführungsfelder](sharing-execution-fields.md)**: Felder, die für das Tracking der Aktionsausführung spezifisch sind
- **[Journey-Felder](sharing-journey-fields.md)**: Journey-spezifische Metadaten und Kennungen

### Best Practices und Fehlerbehebung {#best-practices}

**Leistungsoptimierung**

- Verwenden Sie `journeyVersionID` anstelle von `journeyVersionName` für eine bessere Abfrageleistung ([&#x200B; Sie mehr über Journey-Eigenschaften](../building-journeys/expression/journey-properties.md))
- Filtern nach Datumsbereichen, um die Abfrageschwindigkeit für große Datensätze zu verbessern
- Nutzen Sie Profilidentitäten, die Ihrer [Journey-Namespace-Konfiguration entsprechen](../building-journeys/entry-management.md)

**Datenqualität**

- Regelmäßige Überwachung auf [verworfene Ereignisse](sharing-field-list.md#discarded-events) um Datenprobleme zu identifizieren
- Überprüfen, ob Ereignisschemata Ihren Analyseanforderungen entsprechen
- Implementieren einer ordnungsgemäßen Fehlerbehandlung in benutzerdefinierten Abfragen

**Analytics-Strategien**

- Kombinieren von Journey-Schrittereignissen mit [Nachrichten-Feedback-Daten](../data/datasets-query-examples.md#message-feedback-event-dataset) für eine vollständige Attribution
- Zeitbasierte Analyse zum Verständnis der Journey-Geschwindigkeit und von Engpässen

### Erweiterte Analysefunktionen {#advanced-analytics}

**Customer Journey Analytics-Integration**
Journey-Schrittereignisse können mit [Customer Journey Analytics](cja-ajo.md) analysiert werden für:

- Erweiterte Attributionsmodellierung
- Kanalübergreifende Journey-Visualisierung
- Predictive Analytics beim Journey von Ergebnissen

Erfahren Sie, wie [Customer Journey Analytics konfigurieren](report-gs-cja.md) für Journey Optimizer-Daten.

## Weitere Ressourcen {#additional-resources}

### Links zur Dokumentation {#documentation-links}

- **[Übersicht über die Freigabe von Journey-Schritten](sharing-overview.md)**: So fließen Journey-Daten in Adobe Experience Platform
- **[Wörterbuch zu integrierten Schemata](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=de){target="_blank"}**: Vollständige XDM-Schemareferenz
- **[Journey Optimizer-Reporting](report-gs-cja.md)**: Übersicht über die Reporting-Funktionen in Journey Optimizer

### Integrationshandbücher {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)**: Analysieren von Journey Optimizer-Daten in CJA
- **[Daten-Management](../data/export-datasets.md)**: Exportieren und Verwalten von Journey-Daten
- **[Datenschutz und Governance](../privacy/audit-logs.md)**: Überlegungen zur Data Governance bei Journey-Ereignissen


**Nächste Schritte:**

- Beginnen Sie mit [Erstellen Ihrer ersten Journey-Berichte](sharing-overview.md)
- Erkunden Sie [Abfragebeispiele](query-examples.md) für bestimmte Anwendungsfälle
- Erfahren Sie mehr über Best Practices für die [Journey-Verwaltung](../building-journeys/journey.md)
