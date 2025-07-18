---
solution: Journey Optimizer
product: journey optimizer
title: Leitplanken und Einschränkungen für koordinierte Kampagnen
description: Erfahren Sie mehr über Schutzmechanismen und Einschränkungen bei orchestrierten Kampagnen
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 5%

---

# Leitlinien und Einschränkungen {#guardrails}

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[ Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Ausdrücke bearbeiten](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimension ändern](activities/change-dimension.md) - [Kanalaktivitäten](activities/channels.md) - [Kombinieren](activities/combine.md) - [Anreicherung](activities/deduplication.md) - [Formulare](activities/enrichment.md) - [Abstimmung](activities/fork.md) [&#128279;](activities/reconciliation.md) [&#128279;](activities/save-audience.md) [&#128279;](activities/split.md) ->Zielgruppe speichern[ -AufspaltungWarten](activities/wait.md) |

{style="table-layout:fixed"}

+++

## Einschränkungen von Datenfluss zu Datensatz

Jeder Datensatz in Adobe Experience Platform kann jeweils nur einem aktiven Datenfluss zugeordnet werden. Diese 1:1-Kardinalität wird von der Plattform streng durchgesetzt.

Wenn Sie Datenquellen wechseln müssen (z. B. von Amazon S3 zu Salesforce):

Sie müssen den vorhandenen Datenfluss löschen, der mit dem Datensatz verbunden ist.

Erstellen Sie dann einen neuen Datenfluss, wobei die neue Quelle demselben Datensatz zugeordnet ist.

Dies stellt eine zuverlässige Datenaufnahme sicher und ist bei der Verwendung der Änderungsdatenerfassung (CDC), die für inkrementelle Aktualisierungen von einem definierten Primärschlüssel und Versionierungsattribut (z. B. lastModified) abhängt, von entscheidender Bedeutung.


## Relationale Schemata/Einschränkungen bei der Datenaufnahme

* Anzahl der Schemata : Die maximale Anzahl relationaler Schemata (Tabellen im relationalen Datenspeicher) ist 200
* Relationale Schemagröße - Die maximale relationale Schemagröße für die Kampagnenorchestrierung beträgt 100 GB.
* Datenerfassungshäufigkeit : Die Batch-Datenerfassungshäufigkeit für die Kampagnenorchestrierung beträgt maximal eine alle fünfzehn Minuten.
* Änderungen/Aktualisierungen - Tägliche Aktualisierungen/Änderungen sollten unter 20 % der gesamten Datensätze für ein bestimmtes relationales Schema betragen
