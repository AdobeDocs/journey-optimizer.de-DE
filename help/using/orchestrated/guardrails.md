---
solution: Journey Optimizer
product: journey optimizer
title: Leitplanken und Einschränkungen für koordinierte Kampagnen
description: Erfahren Sie mehr über Schutzmechanismen und Einschränkungen bei orchestrierten Kampagnen
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 2ad659b391515c193418325c34a9dd56133b90d6
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 3%

---

# Leitlinien und Einschränkungen {#guardrails}

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[ Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Ausdrücke bearbeiten](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimension ändern](activities/change-dimension.md) - [Kanalaktivitäten](activities/channels.md) - [Kombinieren](activities/combine.md) - [Anreicherung](activities/deduplication.md) - [Formulare](activities/enrichment.md) - [Abstimmung](activities/fork.md) [ ](activities/reconciliation.md) [ ](activities/save-audience.md) [ ](activities/split.md) ->Zielgruppe speichern[ -AufspaltungWarten](activities/wait.md) |

{style="table-layout:fixed"}

+++

## Einschränkungen von Datenfluss zu Datensatz

Jeder Datensatz in Adobe Experience Platform kann jeweils nur einem aktiven Datenfluss zugeordnet werden. Diese 1:1-Kardinalität wird von der Plattform streng durchgesetzt.

Wenn Sie Datenquellen wechseln müssen (z. B. von Amazon S3 zu Salesforce):

Sie müssen den vorhandenen Datenfluss löschen, der mit dem Datensatz verbunden ist.

Erstellen Sie dann einen neuen Datenfluss, wobei die neue Quelle demselben Datensatz zugeordnet ist.

Dies stellt eine zuverlässige Datenaufnahme sicher und ist bei der Verwendung der Änderungsdatenerfassung (CDC), die für inkrementelle Aktualisierungen von einem definierten Primärschlüssel und Versionierungsattribut (z. B. lastModified) abhängt, von entscheidender Bedeutung.


## Relationale Schemata/Einschränkungen bei der Datenaufnahme

* Im relationalen Datenspeicher werden bis zu 200 relationale Schemata (Tabellen) unterstützt.

* Die Gesamtgröße eines relationalen Schemas, das für die Kampagnenorchestrierung verwendet wird, sollte 100 GB nicht überschreiten.

* Die Batch-Aufnahme für die Kampagnenorchestrierung sollte nicht öfter als einmal alle 15 Minuten erfolgen.

* Tägliche Änderungen an einem relationalen Schema sollten unter 20 % der gesamten Datensatzanzahl bleiben.

## Datenmodellierung

* Der Versionsdeskriptor ist für alle Schemata obligatorisch, einschließlich Faktentabellen.

* Für jede Tabelle ist ein Primärschlüssel erforderlich.

* Der bei der Erstellung des Datensatzes zugewiesene Tabellenname wird in der Segmentierungs-Benutzeroberfläche und in den Personalisierungsfunktionen verwendet.

  Dieser Name ist dauerhaft und kann nach der Erstellung nicht geändert werden.

* Feldergruppen werden derzeit nicht unterstützt.

## Datenaufnahme

* Profil + relationale Datenerfassung sind erforderlich.

* Für die dateibasierte Aufnahme ist ein Feld vom Typ „Änderung“ erforderlich, während die Tabellenprotokollierung für die Cloud DB-Aufnahme aktiviert sein muss. Dies ist für die Change Data Capture (CDC) erforderlich.

* Die Latenz von der Aufnahme bis zur Datenverfügbarkeit in Snowflake reicht von 15 Minuten bis zu 2 Stunden, je nach Datenvolumen, Gleichzeitigkeit und der Art der Vorgänge (Einfügungen sind schneller als Aktualisierungen).

* Die Datenüberwachung in Snowflake ist in Entwicklung. Derzeit gibt es keine native Bestätigung für eine erfolgreiche Aufnahme.

* Direkte Aktualisierungen an Snowflake oder dem Datensatz werden nicht unterstützt. Alle Änderungen müssen durch CDC-Quellen fließen.

  Der Abfrage-Service ist schreibgeschützt.

* ETL wird nicht unterstützt - Kunden müssen Daten im erforderlichen Format bereitstellen.

* Teilweise Aktualisierungen sind nicht zulässig. Jede Zeile muss als vollständiger Datensatz angegeben werden.

* Die Aufnahme beruht auf dem Abfrage-Service und dem Daten-Distiller.

## Segmentierung

* LOV (List of Values) und Auflistungen sind derzeit verfügbar.

* Gespeicherte Zielgruppen sind statische Listen, deren Inhalt die zum Zeitpunkt der Kampagnenausführung verfügbaren Daten widerspiegelt.

* Das Anhängen an eine gespeicherte Zielgruppe wird nicht unterstützt. Aktualisierungen müssen vollständig überschrieben werden.

* Zielgruppen dürfen nur aus Skalarattributen bestehen. Zuordnungen und Arrays werden nicht unterstützt.

* Die Segmentierung unterstützt in erster Linie relationale Daten. Das Mischen mit Profildaten ist zwar zulässig, das Einbringen großer Profildatensätze kann jedoch die Leistung beeinträchtigen. So verhindern Sie dies:

* Es gibt Schutzmaßnahmen, z. B. die Begrenzung der Anzahl der im Batch oder in Streaming-Zielgruppen ausgewählten Profilattribute.

* Gelesene Zielgruppen werden nicht zwischengespeichert - jede Kampagne führt Trigger einen vollständigen Lesevorgang aus.

  Für große oder komplexe Zielgruppen ist eine Optimierung erforderlich.