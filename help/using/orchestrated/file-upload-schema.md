---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurationsschritte
description: Erfahren Sie, wie Sie in Adobe Experience Platform ein relationales Schema erstellen, indem Sie eine DDL hochladen
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 88eb1438-0fe5-4a19-bfb6-2968a427e9e8
source-git-commit: 6447f5d1a060037c0ceaa374db20966097585f9c
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 59%

---

# Erstellen relationaler Schemata mithilfe einer DDL-Datei {#file-upload-schema}

+++ Inhaltsverzeichnis

| Willkommen bei orchestrierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Bearbeiten von Ausdrücken](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) – [Zielgruppe erstellen](activities/build-audience.md) – [Dimensionsänderung](activities/change-dimension.md) – [Kanalaktivitäten](activities/channels.md) – [Kombinieren](activities/combine.md) – [Deduplizierung](activities/deduplication.md) – [Anreicherung](activities/enrichment.md) – [Verzweigung](activities/fork.md) – [Abstimmung](activities/reconciliation.md) – [Zielgruppe speichern](activities/save-audience.md) – [Aufspaltung](activities/split.md) – [Warten](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Definieren Sie das relationale Datenmodell, das für orchestrierte Kampagnen erforderlich ist, indem Sie Schemata wie **Treueprogramm-**, **Treuetransaktionen** und **Treueprämien** erstellen. Jedes Schema muss einen Primärschlüssel, ein Versionierungsattribut und geeignete Beziehungen zu Referenzentitäten wie &quot;**&quot;** &quot;**&quot;**.

Schemata können manuell über die Benutzeroberfläche erstellt oder stapelweise mithilfe einer DDL-Datei importiert werden.

In diesem Abschnitt wird Schritt für Schritt erklärt, wie ein relationales Schema in Adobe Experience Platform durch Hochladen einer DDL-Datei (Data Definition Language) erstellt wird. Durch die Verwendung einer DDL-Datei können Sie die Struktur Ihres Datenmodells vorab definieren, einschließlich Tabellen, Attributen, Schlüsseln und Beziehungen.

1. [Laden Sie eine DDL-Datei hoch](#ddl-upload) um relationale Schemata zu erstellen und ihre Struktur zu definieren.

1. [Definieren von ](#relationships) zwischen Tabellen in Ihrem Datenmodell.

1. [Verknüpfen von Schemata](#link-schema) um Ihre relationalen Daten mit vorhandenen Profilentitäten wie Empfängern oder Marken zu verbinden.

1. [Aufnehmen von ](ingest-data.md) aus unterstützten Quellen in Ihren Datensatz.

## DDL-Datei hochladen{#ddl-upload}

Durch Hochladen einer DDL-Datei können Sie die Struktur Ihres Datenmodells vorab definieren, einschließlich Tabellen, Attributen, Schlüsseln und Beziehungen.

Excel-basierte Schemadateiuploads werden unterstützt. Laden Sie die [bereitgestellte Vorlage](assets/template.zip) herunter, um Ihre Schemadefinitionen einfach vorzubereiten.

+++Beim Erstellen relationaler Schemata in Adobe Experience Platform werden die folgenden Funktionen unterstützt

* **ENUM**\
  ENUM-Felder werden sowohl bei der DDL-basierten als auch bei der manuellen Schemaerstellung unterstützt, sodass Sie Attribute mit einem festen Satz zulässiger Werte definieren können.

* **Schemakennzeichnung für Data Governance**\
  Die Kennzeichnung wird auf der Ebene der Schemafelder unterstützt, um Data-Governance-Richtlinien wie Zugriffskontrolle und Nutzungsbeschränkungen durchzusetzen. Weitere Informationen sind in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de) verfügbar.

* **Zusammengesetzter Schlüssel**\
  Zusammengesetzte Primärschlüssel werden in relationalen Schemadefinitionen unterstützt, sodass mehrere Felder zusammen verwendet werden können, um Datensätze eindeutig zu identifizieren.

+++

1. Melden Sie sich bei Adobe Experience Platform an.

1. Navigieren Sie zum Menü **Daten** > **Schema** .

1. Klicken Sie **Schema erstellen**.

1. Wählen Sie **[!UICONTROL Relational]** als **Schematyp** aus.

   ![](assets/admin_schema_1.png)

1. Wählen Sie **[!UICONTROL Hochladen einer DDL-Datei]** aus, um ein Entitätsbeziehungsdiagramm zu definieren und Schemata zu erstellen.

   Die Tabellenstruktur muss Folgendes enthalten:
   * Mindestens einen Primärschlüssel,
   * eine Versionskennung, z. B. ein `lastmodified`-Feld vom Typ `datetime` oder `number`.
   * Bei der Aufnahme von Change Data Capture (CDC) gibt eine spezielle Spalte mit dem Namen `_change_request_type` vom Typ `String` den Typ der Datenänderung an (z. B. Einfügen, Aktualisieren, Löschen) und ermöglicht die inkrementelle Verarbeitung


   >[!IMPORTANT]
   >
   > Jedes für das Targeting verwendete Schema muss mindestens ein Identitätsfeld vom Typ `String` mit einem zugehörigen **Identity-Namespace** enthalten.\
   >Dadurch wird die Kompatibilität mit den Targeting- und Identitätsauflösungsfunktionen von Adobe Journey Optimizer sichergestellt.

1. Ziehen Sie Ihre DDL-Datei per Drag-and-Drop und klicken Sie auf **[!UICONTROL Weiter]**.

   Beachten Sie, dass die maximal unterstützte Größe für eine DDL-Datei 10 MB beträgt.

1. Geben Sie Ihren **[!UICONTROL Schemanamen]** ein.

1. Richten Sie jedes Schema und seine Spalten ein und stellen Sie dabei sicher, dass ein Primärschlüssel angegeben wird.

   Ein Attribut, z. B. `lastmodified`, muss als Versionsdeskriptor angegeben werden. Dieses Attribut, das normalerweise vom Typ `datetime`, `long` oder `int` ist, ist für Aufnahmeprozesse unverzichtbar, da es sicherstellt, dass der Datensatz mit der neuesten Datenversion aktualisiert wird.

   ![](assets/admin_schema_2.png)

1. Klicken Sie auf **[!UICONTROL Fertig]**, sobald Sie fertig sind.

Sie können jetzt die Tabellen- und Felddefinitionen auf der Arbeitsfläche überprüfen. [Weitere Informationen finden Sie im nachfolgenden Abschnitt](#entities)

## Definieren von Beziehungen {#relationships}

Gehen Sie wie folgt vor, um logische Verbindungen zwischen Tabellen innerhalb Ihres Schemas zu definieren.

1. Rufen Sie die Arbeitsflächenansicht Ihres Datenmodells auf und wählen Sie die beiden Tabellen aus, die Sie verknüpfen möchten.

1. Klicken Sie auf die Schaltfläche ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) neben dem Quellen-Join und ziehen Sie den Pfeil in Richtung Ziel-Join, um die Verbindung herzustellen.

   ![](assets/admin_schema_5.png)

1. Füllen Sie das angegebene Formular aus, um den Link zu definieren, und klicken Sie nach der Konfiguration auf **Anwenden**.

   ![](assets/admin_schema_3.png)

   **Kardinalität**:

   * **1:N**: Eine Entität in der Quelltabelle kann mit mehreren Entitäten in der Zieltabelle in Beziehung stehen, aber eine Entität in der Zieltabelle kann nur maximal mit einer Entität in der Quelltabelle in Beziehung stehen.

   * **N:1**: Eine Entität in der Zieltabelle kann mit mehreren Entitäten in der Quelltabelle in Beziehung stehen, aber eine Entität in der Quelltabelle kann nur maximal mit einer Entität in der Zieltabelle in Beziehung stehen.

   * **1:1**: Eine Entität in der Quelltabelle kann maximal mit einer Entität in der Zieltabelle in Beziehung stehen.

1. Alle in Ihrem Datenmodell definierten Links werden in der Arbeitsflächenansicht als Pfeile dargestellt. Klicken Sie auf einen Pfeil zwischen zwei Tabellen, um je nach Bedarf Details anzuzeigen, Änderungen vorzunehmen oder den Link zu entfernen.

   ![](assets/admin_schema_6.png)

1. Verwenden Sie die Symbolleiste, um die Arbeitsfläche anzupassen.

   ![](assets/toolbar.png)

   * **Vergrößern**: Vergrößert die Arbeitsfläche, um Details zu Ihrem Datenmodell deutlicher zu sehen.

   * **Verkleinern**: Verkleinert die Arbeitsfläche, um eine erweiterte Ansicht Ihres Datenmodells zu erhalten.

   * **Ansicht anpassen**: Passt den Zoom so an, dass alle Schemata im sichtbaren Bereich angezeigt werden.

   * **Filter**: Wählen Sie aus, welches Schema auf der Arbeitsfläche angezeigt werden soll.

   * **Automatisches Layout erzwingen**: Lassen Sie Schemata zur besseren Organisation automatisch anordnen.

   * **Zuordnung anzeigen**: Schalten Sie eine Miniatur-Zuordnungsüberlagerung ein, um leichter durch große oder komplexe Schema-Layouts zu navigieren.

1. Klicken Sie auf **Speichern**, sobald Sie fertig sind. Diese Aktion erstellt die Schemata und die zugehörigen Datensätze und ermöglicht die Verwendung des Datensatzes in orchestrierten Kampagnen.

1. Klicken Sie **[!UICONTROL Aufträge öffnen]**, um den Fortschritt des Erstellungsauftrags zu überwachen. Dieser Prozess kann je nach der Anzahl der in der DDL-Datei definierten Tabellen mehrere Minuten dauern.

   Sie können auf Ihre relationalen Aufträge auch zugreifen, indem Sie das Fenster **[!UICONTROL DDL-Datei hochladen]** öffnen und **[!UICONTROL Alle relationalen Aufträge anzeigen]** auswählen.

   ![](assets/admin_schema_4.png)

## Verknüpfen von Schemata {#link-schema}

>[!IMPORTANT]
>
> Das System erkennt nur Beziehungen, die in der DDL-Datei explizit definiert sind. Alle Entitätsbeziehungen, die außerhalb der DDL-Datei vorhanden sind, werden ignoriert und nicht verarbeitet.

Stellen Sie eine Beziehung zwischen dem Schema **Treuetransaktionen** und dem Schema **Empfängerinnen und Empfänger** her, um jede Transaktion mit dem richtigen Kundeneintrag zu verknüpfen.

1. Navigieren Sie zu **[!UICONTROL Schemata]** und öffnen Sie Ihre zuvor erstellten **Treuetransaktionen**.

1. Klicken Sie auf **[!UICONTROL Beziehung hinzufügen]** in den **[!UICONTROL Feldeigenschaften]** der Kundinnen und Kunden.

   ![](assets/schema_1.png)

1. Wählen Sie als **[!UICONTROL Typ]** der Beziehung **[!UICONTROL Viele-zu-eins]**.

1. Verknüpfen Sie das vorhandene Schema **Empfängerinnen und Empfänger**.

   ![](assets/schema_2.png)

1. Geben Sie einen **[!UICONTROL Beziehungsnamen im aktuellen Schema]** und einen **[!UICONTROL Beziehungsnamen im Referenzschema]** ein.

1. Klicken Sie auf **[!UICONTROL Übernehmen]**, um die Änderungen zu speichern.

Erstellen Sie dann eine Beziehung zwischen dem Schema **Treueprämien** und dem Schema **Marken**, um jeden Prämieneintrag mit der entsprechenden Marke zu verknüpfen.

![](assets/schema_3.png)


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
