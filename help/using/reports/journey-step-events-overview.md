---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit Journey-Schrittereignissen
description: Erfahren Sie, wie Sie mit Journey-Schrittereignissen in Adobe Journey Optimizer arbeiten - verstehen Sie, was sie sind, warum sie wichtig sind und wie Sie sie für Analysen und Optimierungen verwenden können
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin, User
level: Intermediate, Experienced
keywords: Journey, Schrittereignisse, Analysen, Reporting, Überwachung, XDM
hide: true
hidefromtoc: true
exl-id: 9f8e7d6c-5b4a-3928-1756-849302a11c2b
source-git-commit: df3abb7da17eb21e5e4120b55bdeb61fec3e202d
workflow-type: tm+mt
source-wordcount: '875'
ht-degree: 3%

---

# Arbeiten mit Journey-Schrittereignissen {#work-with-journey-step-events}

Journey-Schrittereignisse sind automatisch generierte Ereignisse, die detaillierte Informationen zu jedem Schritt erfassen, den ein Profil unternimmt, während es eine Journey in Adobe Journey Optimizer durchläuft. Diese Ereignisse bieten umfassende Einblicke in die Journey-Leistung und ermöglichen leistungsstarke Analysefunktionen.

## Was sind Journey-Schrittereignisse? {#what-are-step-events}

Journey-Schrittereignisse sind systemgenerierte XDM-Ereignisse (Experience-Datenmodell), die Adobe Journey Optimizer automatisch erstellt und an Adobe Experience Platform sendet, wenn ein Profil auf einer Journey von einem Knoten zu einem anderen wechselt. Jedes Ereignis entspricht einer bestimmten Aktion oder Transition im Journey-Erlebnis des Kunden.

Es gibt zwei Haupttypen von Journey-Schrittereignissen:

- **journeyStepEvent**: Ereignisse im Zusammenhang mit dem Fortschritt einzelner Profile durch Journey-Schritte
- **journeyStepProfileEvent**: Ereignisse, die zusätzliche Profilkontextinformationen enthalten

### Welche Trigger Journey-Schrittereignisse? {#event-triggers}

Journey-Schrittereignisse werden automatisch für verschiedene Journey-Aktivitäten generiert:

- **Eintrittsereignisse**: Wenn ein Profil auf eine Journey zugreift
- **Aktionsausführung**: Wenn Nachrichten gesendet oder benutzerdefinierte Aktionen ausgeführt werden
- **Bedingungsauswertung**: Wenn Profile Entscheidungspunkte durchlaufen
- **Warteaktivitäten**: Wenn Profile in Warteknoten eintreten und diese verlassen
- **Exit-Ereignisse**: Wenn Profile eine Journey abgeschlossen oder beendet haben
- **Fehlerbehandlung**: Wenn bei der Journey-Ausführung Fehler auftreten

>[!NOTE]
>
>Journey-Schrittereignisse sind standardmäßig auf allen Instanzen aktiviert. Sie können die Schemata und Datensätze, die bei der Bereitstellung für Schrittereignisse erstellt wurden, nicht ändern oder aktualisieren. Diese Schemata und Datensätze befinden sich im schreibgeschützten Modus.

## Warum Journey-Schrittereignisse wichtig sind {#why-step-events-matter}

Journey-Schrittereignisse bieten einen entscheidenden Wert für Unternehmen, die Adobe Journey Optimizer verwenden:

### Echtzeit-Analyse und -Überwachung {#real-time-analytics}

- **Journey-Leistungs-Tracking**: Überwachen Sie, wie Profile Ihre Journey in Echtzeit durchlaufen
- **Konversionsanalyse**: Dropdown-Punkte und erfolgreiche Konversionspfade verstehen
- **Fehlererkennung**: Probleme sofort identifizieren und beheben

### Datenintegration und Erkenntnisse {#data-integration}

- **Plattformübergreifende Analyse**: Kombinieren von Journey-Daten mit anderen Adobe Experience Platform-Datenquellen
- **Kunden-360-Ansicht**: Erstellen Sie umfassende Kundenprofile, die Journey-Interaktionen beinhalten
- **Attributionsmodellierung**: Verbinden von Journey-Touchpoints mit nachgelagerten Geschäftsergebnissen

### Optimierungsmöglichkeiten {#optimization}

- **A/B-Test-Insights**: Analysieren der Performance verschiedener Journey-Pfade
- **Personalization-Verbesserung**: Verwenden Sie Journey-Verhaltensdaten, um zukünftige Erlebnisse zu verbessern
- **Betriebseffizienz**: Engpässe identifizieren und Journey-Design optimieren

## Verwenden von Journey-Schrittereignissen {#how-to-use-step-events}

### Zugreifen auf Journey-Schritt-Ereignisdaten {#accessing-data}

Journey-Schrittereignisdaten werden automatisch in Adobe Experience Platform gespeichert und können wie folgt aufgerufen werden:

1. **Data Lake-Abfragen**: Verwenden Sie SQL, um den `journey_step_events` Datensatz abzufragen
2. **Customer Journey Analytics**: Analysieren von Journey-Daten mit erweiterten Analyse-Tools
3. **Echtzeit-Reporting**: Zugriff auf Daten über die integrierten Reporting-Funktionen von Journey Optimizer
4. **APIs**: Programmgesteuerter Zugriff auf Ereignisdaten für benutzerdefinierte Programme

### Wichtige verfügbare Datenpunkte {#key-data-points}

Journey-Schrittereignisse erfassen umfassende Informationen, darunter:

- **Journey-Identifizierung**: Journey-ID, Version und Name
- **Profilinformationen**: Profil-ID und zugehörige Identitäten
- **Schrittdetails**: Knotenname, Schritttyp und Ausführungsstatus
- **Zeitstempel**: Präzise Zeitplanung für jeden Journey-Schritt
- **Aktionsergebnisse**: Erfolgs-/Fehlerstatus und Ausführungsdetails
- **Fehlerinformationen**: Detaillierte Fehler-Codes und Beschreibungen, wenn Probleme auftreten

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

- Verwenden Sie `journeyVersionID` statt `journeyVersionName`, um die Abfrageleistung zu verbessern.
- Filtern nach Datumsbereichen, um die Abfrageschwindigkeit für große Datensätze zu verbessern
- Nutzen Sie Profilidentitäten, die Ihrer Journey-Namespace-Konfiguration entsprechen

**Datenqualität**

- Regelmäßige Überwachung auf [verworfene Ereignisse](sharing-field-list.md#discarded-events) um Datenprobleme zu identifizieren
- Überprüfen, ob Ereignisschemata Ihren Analyseanforderungen entsprechen
- Implementieren einer ordnungsgemäßen Fehlerbehandlung in benutzerdefinierten Abfragen

**Analytics-Strategien**

- Journey-Schrittereignisse mit Nachrichten-Feedback-Daten für vollständige Attribution kombinieren
- Zeitbasierte Analyse zum Verständnis der Journey-Geschwindigkeit und von Engpässen
- Erstellen von Kohortenanalysen zum Vergleich verschiedener Journey-Varianten

### Erweiterte Analysefunktionen {#advanced-analytics}

**Customer Journey Analytics-Integration**
Journey-Schrittereignisse können mit Customer Journey Analytics analysiert werden für:

- Erweiterte Attributionsmodellierung
- Kanalübergreifende Journey-Visualisierung
- Predictive Analytics beim Journey von Ergebnissen

**Echtzeit-**
Verwenden Sie Journey-Schritt-Ereignismuster für Folgendes:

- Echtzeit-Personalisierung für Trigger
- Implementieren der Dynamic Journey-Optimierung
- Aktivieren von kontextbezogenen Empfehlungen für die nächste beste Aktion

## Weitere Ressourcen {#additional-resources}

### Links zur Dokumentation {#documentation-links}

- **[Übersicht über die Freigabe von Journey-Schritten](sharing-overview.md)**: So fließen Journey-Daten in Adobe Experience Platform
- **[Wörterbuch zu integrierten Schemata](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=de)**: Vollständige XDM-Schemareferenz
- **[Journey Optimizer-Reporting](report-gs-cja.md)**: Übersicht über die Reporting-Funktionen in Journey Optimizer

### Integrationshandbücher {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)**: Analysieren von Journey Optimizer-Daten in CJA
- **[Daten-Management](../data/export-datasets.md)**: Exportieren und Verwalten von Journey-Daten
- **[Datenschutz und Governance](../privacy/audit-logs.md)**: Überlegungen zur Data Governance bei Journey-Ereignissen

Journey-Schrittereignisse bilden die Grundlage für erweiterte Journey-Analysen in Adobe Journey Optimizer. Indem Sie diese Ereignisse effektiv verstehen und nutzen, können Sie tiefgehende Einblicke in das Kundenverhalten gewinnen, die Journey-Performance optimieren und personalisiertere Erlebnisse für Ihre Kunden erstellen.
