---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurationsschritte
description: Erfahren Sie, wie Sie in Adobe Experience Platform ein relationales Schema erstellen, indem Sie eine DDL hochladen
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
source-git-commit: 8470791182d2487539d2d2300edb4d6e0cfeadb4
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 5%

---

# Erste Schritte mit Schemata und Datensätzen{#gs-schemas}

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[ Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Ausdrücke bearbeiten](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimension ändern](activities/change-dimension.md) - [Kanalaktivitäten](activities/channels.md) - [Kombinieren](activities/combine.md) - [Anreicherung](activities/deduplication.md) - [Formulare](activities/enrichment.md) - [Abstimmung](activities/fork.md) [&#128279;](activities/reconciliation.md) [&#128279;](activities/save-audience.md) [&#128279;](activities/split.md) ->Zielgruppe speichern[ -AufspaltungWarten](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Dieses Handbuch führt Sie durch den Prozess der Erstellung eines relationalen Schemas, der Konfiguration eines Datensatzes für orchestrierte Kampagnen und der Aufnahme von Daten.

![](assets/do-not-localize/schema_admin.png)

1. Erstellen [relationalen Schemas manuell](manual-schema.md) oder [mithilfe einer DDL-Datei](file-upload-schema.md)

   Definieren Sie die Struktur Ihres Datenmodells, einschließlich Tabellen, Attributen und Beziehungen. Wählen Sie, das Schema manuell in der Benutzeroberfläche zu erstellen oder eine DDL-Datei hochzuladen, um die Einrichtung zu beschleunigen.

1. [Verknüpfungsschema](file-upload-schema.md)

   Erstellen Sie Beziehungen zwischen Ihren Schemata, um Datenkonsistenz zu gewährleisten und entitätsübergreifende Abfragen zu ermöglichen. Verknüpfen Sie beispielsweise Treuetransaktionen mit Empfängern oder Belohnungen mit Marken.

1. [Aufnehmen von Daten](ingest-data.md)

   Importieren Sie Daten aus unterstützten Quellen wie SFTP, Cloud-Speicher oder Datenbanken in Adobe Experience Platform.

