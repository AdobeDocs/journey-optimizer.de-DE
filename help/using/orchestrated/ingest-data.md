---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurationsschritte
description: Erfahren Sie, wie Sie Daten aus unterstützten Quellen wie SFTP, Cloud-Speicher oder Datenbanken in Adobe Experience Platform importieren.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
source-git-commit: 6447f5d1a060037c0ceaa374db20966097585f9c
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 38%

---

# Aufnehmen von Daten {#ingest-data}

+++ Inhaltsverzeichnis

| Willkommen bei orchestrierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Bearbeiten von Ausdrücken](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) – [Zielgruppe erstellen](activities/build-audience.md) – [Dimensionsänderung](activities/change-dimension.md) – [Kanalaktivitäten](activities/channels.md) – [Kombinieren](activities/combine.md) – [Deduplizierung](activities/deduplication.md) – [Anreicherung](activities/enrichment.md) – [Verzweigung](activities/fork.md) – [Abstimmung](activities/reconciliation.md) – [Zielgruppe speichern](activities/save-audience.md) – [Aufspaltung](activities/split.md) – [Warten](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Um die Datenquelle für einen Datensatz zu ändern, müssen Sie zunächst den vorhandenen Datenfluss löschen, bevor Sie einen neuen erstellen, der auf denselben Datensatz und die neue Quelle verweist.
>
>Adobe Experience Platform erzwingt eine strikte Eins-zu-eins-Beziehung zwischen Datenflüssen und Datensätzen. Auf diese Weise können Sie die Synchronisierung zwischen Quelle und Datensatz für eine genaue inkrementelle Aufnahme aufrechterhalten.

Adobe Experience Platform ermöglicht die Aufnahme von Daten aus externen Quellen und bietet spezielle Experience Platform-Services, mittels derer Sie eingehende Daten strukturieren, beschriften und erweitern können. Daten können aus verschiedensten Quellen aufgenommen werden, darunter etwa Adobe-Anwendungen, Cloud-basierte Datenspeicher und Datenbanken.

## Unterstützte Quellen für orchestrierte Kampagnen {#supported}

Die folgenden Quellen werden für die Verwendung mit orchestrierten Kampagnen unterstützt:

<table>
  <thead>
    <tr>
      <th>Typ</th>
      <th>Quelle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">Cloud-Speicherplatz</td>
      <td><a href="https://experienceleague.adobe.com/de/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/s3">Amazon S3</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/de/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/google-cloud-storage">Google Cloud Storage</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/de/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/sftp">SFTP</a></td>
    </tr>
      <td rowspan="4">Cloud Data Warehouses</td>
      <td><a href="https://experienceleague.adobe.com/de/docs/experience-platform/sources/ui-tutorials/create/databases/snowflake">Snowflake</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/de/docs/experience-platform/sources/ui-tutorials/create/databases/bigquery">Google BigQuery</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/de/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/data-landing-zone">Data Landing Zone<a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/de/docs/experience-platform/sources/ui-tutorials/create/databases/databricks">Azure Databricks</a></td>
    </tr>
    <tr>
      <td rowspan="3">Dateibasierte Uploads</td>
      <td><a href="https://experienceleague.adobe.com/de/docs/experience-platform/sources/ui-tutorials/create/local-system/local-file-upload">Lokaler Datei-Upload<a></td>
    </tr>

</tbody>
</table>

## Datenfluss konfigurieren

Dieses Beispiel zeigt, wie ein Datenfluss konfiguriert wird, der strukturierte Daten in Adobe Experience Platform aufnimmt. Der konfigurierte Datenfluss unterstützt eine automatisierte, geplante Aufnahme und ermöglicht Echtzeit-Aktualisierungen.

1. Greifen Sie über das Menü **[!UICONTROL Verbindungen]** auf das Menü **[!UICONTROL Quellen]** zu.

1. Wählen Sie Ihre Quelle abhängig von [Unterstützte Quellen für orchestrierte Kampagnen](#supported).

   ![](assets/admin_sources_1.png)

1. Verbinden Sie Ihr Cloud-Speicher- oder Google Cloud-Speicher-Konto, wenn Sie Cloud-basierte Quellen ausgewählt haben.

   ![](assets/admin_sources_2.png)

1. Wählen Sie die Daten aus, die Sie in Adobe Experience Platform aufnehmen möchten.

   ![](assets/S3_config_1.png)

1. Aktivieren Sie auf der **[!UICONTROL Datensatzdetails]** die Option **[!UICONTROL Änderungsdatenerfassung aktivieren]**, um nur Datensätze anzuzeigen, die relationalen Schemata zugeordnet sind und sowohl einen Primärschlüssel als auch einen Versionsdeskriptor enthalten.

   >[!IMPORTANT]
   >
   > Nur **dateibasierten Quellen** jede Zeile in der Datendatei eine `_change_request_type` Spalte mit den Werten `U` (upsert) oder `D` (delete) enthalten. Ohne diese Spalte erkennt das System die Daten nicht als unterstützendes Änderungs-Tracking, und der Umschalter Orchestrierte Kampagne wird nicht angezeigt, was verhindert, dass der Datensatz für die Zielgruppenbestimmung ausgewählt wird.

   ![](assets/S3_config_6.png)

1. Wählen Sie den zuvor erstellten Datensatz aus und klicken Sie auf **[!UICONTROL Weiter]**.

   ![](assets/S3_config_3.png)

1. Wenn Sie nur dateibasierte Quellen verwenden, laden Sie über das Fenster **[!UICONTROL Daten auswählen]** Ihre lokalen Dateien hoch und zeigen Sie eine Vorschau ihrer Struktur und Inhalte an.

   Beachten Sie, dass die maximal unterstützte Größe 100 MB beträgt.

1. Überprüfen Sie im Fenster **[!UICONTROL Zuordnung]**, ob jedes Quelldateiattribut den entsprechenden Feldern im Zielschema korrekt zugeordnet ist.

   Klicken Sie auf **[!UICONTROL Weiter]**, sobald Sie fertig sind.

   ![](assets/S3_config_4.png)

1. Konfigurieren Sie den Datenfluss **[!UICONTROL Zeitplan]** basierend auf der von Ihnen gewünschten Häufigkeit.

1. Klicken Sie auf **[!UICONTROL Beenden]**, um den Datenfluss zu erstellen. Er wird automatisch nach dem festgelegten Zeitplan ausgeführt.

1. Wählen Sie im Menü **[!UICONTROL Verbindungen]** die Option **[!UICONTROL Quellen]** aus und greifen Sie auf die Registerkarte **[!UICONTROL Datenflüsse]** zu, um die Flussausführung zu verfolgen, aufgenommene Einträge zu überprüfen und Fehler zu beheben.

   ![](assets/S3_config_5.png)

