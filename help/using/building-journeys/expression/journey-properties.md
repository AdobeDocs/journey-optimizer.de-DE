---
solution: Journey Optimizer
product: journey optimizer
title: Journey-Eigenschaften
description: Erfahren Sie mehr über die Eigenschaften von Journeys.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: Journey, Ausdruck, Editor, Eigenschaften
exl-id: eb1ab0ed-90bd-4613-b63d-b28693947db2
source-git-commit: 619bcbc16b4117c29c482c85323603a4281298e0
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Attribute der Journey-Eigenschaften {#journey-properties}

Im [einfachen Ausdruckseditor](../condition-activity.md#about_condition)und im [erweiterten Ausdruckseditor](../expression/expressionadvanced.md) können Sie unterhalb der Kategorien **Ereignis** und **Datenquelle** auf die Kategorie **Journey-Eigenschaften** zugreifen. Diese Kategorie enthält technische Felder, die sich auf die Journey eines bestimmten Profils beziehen.  Dies sind die Informationen, die das System von Live-Journeys abruft, wie z. B. die Journey-ID oder die spezifischen aufgetretenen Fehler.

![](../assets/journey-properties.png)

Sie enthält beispielsweise Informationen zu:

* Journey-Version: Journey-UID, Journey-Versions-UID, Instanz-UID usw.
* Fehler: Datenabruf, Aktionsausführung usw.
* aktueller Schritt, letzter aktueller Schritt usw.
* verworfene Profile

  Die Liste der Felder ist [in diesem Abschnitt](#journey-properties-fields) verfügbar.

Sie können diese Felder zum Erstellen von Ausdrücken verwenden. Während der Ausführung einer Journey werden die Werte direkt von der Journey abgerufen.

Im Folgenden finden Sie einige Beispiele für Anwendungsfälle:

* **Verworfene Profile protokollieren**: Sie können alle Profile, die von einer Nachricht ausgeschlossen sind, mit einer Begrenzungsregel zu Protokollierungszwecken an ein Drittanbietersystem senden. Dazu richten Sie bei Zeitüberschreitung und Fehler einen Pfad ein und fügen eine Bedingung zum Filtern nach einem bestimmten Fehlertyp hinzu, z. B.: „Personen nach Begrenzungsregel verwerfen“. Anschließend können Sie die verworfenen Profile über eine benutzerdefinierte Aktion an ein Drittanbietersystem senden.

* **Warnhinweise bei Fehlern senden**: Sie können eine Benachrichtigung an ein Drittanbietersystem senden, sobald ein Fehler in einer Nachricht auftritt. Dazu richten Sie einen Pfad für den Fehlerfall ein, fügen eine Bedingung und eine benutzerdefinierte Aktion hinzu. Sie können beispielsweise eine Benachrichtigung an einen Slack-Kanal mit der Fehlerbeschreibung senden.

* **Fehler in Berichten optimieren**: Statt nur einen Pfad für fehlerhafte Nachrichten zu haben, können Sie eine Bedingung pro Fehlertyp definieren. Auf diese Weise können Sie die Berichte optimieren und alle Daten zu den Fehlertypen anzeigen.

## Liste der Felder {#journey-properties-fields}

| Kategorie | Feldname | Kennzeichnung | Beschreibung |
|---|---|---|------------|
| Journey-Version | journeyUID | Journey-Kennung | |
| | journeyVersionUID | Versionskennung der Journey | |
| | journeyVersionName | Name der Journey-Version | |
| | journeyVersionDescription | Beschreibung der Journey-Version | |
| | journeyVersion | Journey-Version | |
| Journey-Instanz | instanceUID | Kennung der Journey-Instanz | ID der Instanz |
| | externalKey | Externer Schlüssel | Individuelle Kennung, die die Journey auslöst |
| | organizationId | Organisationskennung | Markenorganisation |
| | sandboxName | Sandbox-Name | Name der Sandbox |
| Identität | profileId | Identitätskennung des Profils | Kennung des Profils in der Journey |
| | namespace | Identity-Namespace des Profils | Namespace des Profils in der Journey (Beispiel: ECID) |
| Aktueller Knoten | currentNodeId | Kennung des aktuellen Knotens | Kennung der aktuellen Aktivität (Knoten) |
| | currentNodeName | Name des aktuellen Knotens | Name der aktuellen Aktivität (Knoten) |
| Vorheriger Knoten | previousNodeId | Kennung des vorherigen Knotens | Kennung der vorherigen Aktivität (Knoten) |
| | previousNodeName | Name des vorherigern Knotens | Name der vorherigen Aktivität (Knoten) |
| Fehler | lastNodeUIDInError | Kennung des letzten Knotens im Fehler | Kennung der aktuellen fehlerhaften Aktivität (Knoten) |
| | lastNodeNameInError | Name des letzten Knotens im Fehler | Name der aktuellen fehlerhaften Aktivität (Knoten) |
| | lastNodeTypeInError | Letzter Knotentyp im Fehler | Fehlertyp der aktuellen fehlerhaften Aktivität (Knoten). Mögliche Typen:<ul><li>Ereignisse: Ereignisse, Reaktionen, SQ (Beispiel: Zielgruppen-Qualifizierung)</li><li>Flusssteuerung: Ende, Bedingung, Warten</li><li>Aktionen: ACS-Aktionen, Sprung, benutzerdefinierte Aktion</li></ul> |
| | lastErrorCode | Letzter Fehler-Code | Fehler-Code der aktuellen fehlerhaften Aktivität (Knoten). Mögliche Fehler: <ul><li>HTTP-Fehler-Codes</li><li>capped</li><li>timedOut</li><li>Fehler (Beispiel: Standard bei unerwartetem Fehler. Sollte nicht / äußerst selten vorkommen.)</li></ul> |
| | lastExecutedActionErrorCode | Fehler-Code der letzten ausgeführten Aktion | Fehler-Code der aktuellen Aktion im Fehler |
| | lastDataFetchErrorCode | Fehler-Code beim letzten Datenabruf | Fehler-Code beim aktuellen Datenabruf aus Datenquellen |
| Zeit | lastActionExecutionElapsedTime | Verstrichene Zeit der letzten Aktionsausführung | Zeitaufwand für die Ausführung der aktuellen Aktion |
| | lastDataFetchElapsedTime | Verstrichene Zeit des letzten Datenabrufs | Zeitaufwand für die Ausführung des aktuellen Datenabrufs aus Datenquellen |
