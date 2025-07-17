---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurationsschritte
description: Erfahren Sie, wie Sie in Adobe Experience Platform ein relationales Schema erstellen, indem Sie eine DDL hochladen
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 5%

---

# Erste Schritte mit Schemata und Datensätzen{#gs-schemas}

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[ Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Ausdrücke bearbeiten](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimension ändern](activities/change-dimension.md) - [Kanalaktivitäten](activities/channels.md) - [Kombinieren](activities/combine.md) - [Anreicherung](activities/deduplication.md) - [Formulare](activities/enrichment.md) - [Abstimmung](activities/fork.md) [ ](activities/reconciliation.md) [ ](activities/save-audience.md) [ ](activities/split.md) ->Zielgruppe speichern[ -AufspaltungWarten](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

Der Inhalt

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Dieses Handbuch führt Sie durch den Prozess der Erstellung eines relationalen Schemas, der Konfiguration eines Datensatzes für orchestrierte Kampagnen, der Aufnahme von Daten über eine S3-Quelle und der Abfrage der aufgenommenen Daten in der AP-Plattform.

In diesem Beispiel umfasst die Einrichtung die Integration zweier wichtiger Entitäten, **Treuetransaktionen** und **Treueprämien** und deren Verknüpfung mit vorhandenen Kernentitäten **Empfänger** und **Marken**.

![](assets/do-not-localize/schema_admin.png)

1. [Erstellen eines relationalen Schemas und eines zugehörigen Datensatzes](#schema)

   Definieren Sie das relationale Datenmodell für orchestrierte Kampagnen, einschließlich der **Treueprogramm-**-, **Treuetransaktionen** und **Treueprämien**-Entitäten sowie der erforderlichen Schlüssel und Versionierungsattribute.

1. [Verknüpfungsschema](#link-schema)

   Verknüpfen Sie die Entität **Treuetransaktionen** mit **Empfängern** und **Treueprämien** mit **Marken**, um ein verbundenes Datenmodell zu erstellen, das personalisierte Kunden-Journey unterstützt.

1. [Aufnehmen von Daten](#ingest)

   Importieren Sie Daten aus unterstützten Quellen wie SFTP, Cloud-Speicher oder Datenbanken in Adobe Experience Platform.


<!--### Setting Up Change data capture ingestion {#cdc-ingestion}

If you need to change the data source, you must delete the existing dataflow and create a new one pointing to the same dataset with the new source.

When using Change Data Capture (CDC), it is essential that the source and dataset remain in sync to ensure accurate incremental updates. Follow the steps below:

1. **Schema Requirements**
   - Your schema must include:
     - A **primary key** (e.g., `transaction_id`)
     - A **versioning field** (e.g., `lastmodified` or an incrementing `version_id`)
   - Enable the dataset for **Orchestrated Campaigns** if needed.

2. **CDC Dataflow Setup**
   - During dataflow creation, after choosing your source and files:
     - **Enable the CDC option**
     - Select your CDC-ready dataset
     - Confirm field mappings (especially version field)

3. **Keep Source and Target in Sync**
   - The source system must consistently update the version field so the platform can detect changes accurately.

Once set up, the platform will automatically ingest **only changed or new records** each time the flow runs.
-->
