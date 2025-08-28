---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurationsschritte
description: Erfahren Sie, wie Sie Daten aus unterstützten Quellen wie SFTP, Cloud-Speicher oder Datenbanken in Adobe Experience Platform importieren.
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
source-git-commit: c1201025af216f8f3019e7696b6eb906962b681b
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 22%

---


# Aufnehmen von Daten {#ingest-data}

>[!IMPORTANT]
>
>Um die Datenquelle für einen Datensatz zu ändern, müssen Sie zunächst den vorhandenen Datenfluss löschen, bevor Sie einen neuen erstellen, der auf denselben Datensatz und die neue Quelle verweist.
>
>Adobe Experience Platform erzwingt eine strikte Eins-zu-eins-Beziehung zwischen Datenflüssen und Datensätzen. Auf diese Weise können Sie die Synchronisierung zwischen Quelle und Datensatz für eine genaue inkrementelle Aufnahme aufrechterhalten.

Adobe Experience Platform ermöglicht die Aufnahme von Daten aus externen Quellen und bietet spezielle Experience Platform-Services, mittels derer Sie eingehende Daten strukturieren, beschriften und erweitern können. Daten können aus verschiedensten Quellen aufgenommen werden, darunter etwa Adobe-Anwendungen, Cloud-basierte Datenspeicher und Datenbanken.

Ein Datensatz ist ein Konstrukt zur Datenspeicherung und -verwaltung, in dem Daten (in der Regel) in einer Tabelle erfasst werden, die ein Schema (Spalten) und Felder (Zeilen) beinhaltet. Daten, die erfolgreich in Experience Platform aufgenommen werden, werden im Data Lake als Datensätze gespeichert.

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

## Richtlinien für die Datenhygiene von relationalen Schemata {#cdc}

Bei Datensätzen, die mit **[!UICONTROL Datenerfassung ändern]** aktiviert sind, werden alle Datenänderungen, einschließlich Löschungen, automatisch vom Quellsystem in Adobe Experience Platform gespiegelt.

Da für Adobe Journey Optimizer-Kampagnen alle integrierten Datensätze mit der **[!UICONTROL Datenerfassung für Änderungen]** aktiviert werden müssen, ist der Kunde dafür verantwortlich, Löschungen an der Quelle zu verwalten. Jeder aus dem Quellsystem gelöschte Datensatz wird automatisch aus dem entsprechenden Datensatz in Adobe Experience Platform entfernt.

Um Datensätze über die dateibasierte Aufnahme zu löschen, sollte die Datendatei des Kunden den Datensatz mit einem `D` Wert im Feld `Change Request Type` markieren. Dies bedeutet, dass der Datensatz in Adobe Experience Platform gelöscht werden soll, was das Quellsystem widerspiegelt.

Wenn der Kunde nur Datensätze aus Adobe Experience Platform löschen möchte, ohne die ursprünglichen Quelldaten zu beeinflussen, sind die folgenden Optionen verfügbar:

* **Proxy- oder bereinigte Tabelle für die Replikation der Änderungsdatenerfassung**

  Der Kunde kann einen Proxy oder eine bereinigte Quelltabelle erstellen, um zu steuern, welche Datensätze in Adobe Experience Platform repliziert werden. Löschungen können dann selektiv aus dieser Zwischentabelle verwaltet werden.

* **Löschung über Data Distiller**

  Sofern lizenziert, kann **Data Distiller** verwendet werden, um Löschvorgänge direkt in Adobe Experience Platform zu unterstützen, unabhängig vom Quellsystem.

  [Weitere Informationen zu Data Distiller](https://experienceleague.adobe.com/de/docs/experience-platform/query/data-distiller/overview)

## Datenfluss konfigurieren

Dieses Beispiel zeigt, wie ein Datenfluss konfiguriert wird, der strukturierte Daten in Adobe Experience Platform aufnimmt. Der konfigurierte Datenfluss unterstützt eine automatisierte, geplante Aufnahme und ermöglicht Echtzeit-Aktualisierungen.

1. Greifen Sie über das Menü **[!UICONTROL Verbindungen]** auf das Menü **[!UICONTROL Quellen]** zu.

1. Wählen Sie Ihre Quelle abhängig von [Unterstützte Quellen für orchestrierte Kampagnen](#supported).

   ![](assets/admin_sources_1.png)

1. Verbinden Sie Ihr Cloud-Speicher- oder Google Cloud-Speicher-Konto, wenn Sie Cloud-basierte Quellen ausgewählt haben.

   ![](assets/admin_sources_2.png)

1. Wählen Sie die Daten aus, die in Adobe Experience Platform aufgenommen werden sollen.

   ![](assets/S3_config_1.png)

1. Aktivieren Sie auf der **[!UICONTROL Datensatzdetails]** die Option **[!UICONTROL Änderungsdatenerfassung aktivieren]**, um nur Datensätze anzuzeigen, die relationalen Schemata zugeordnet sind und sowohl einen Primärschlüssel als auch einen Versionsdeskriptor enthalten.

[Weitere Informationen zu Richtlinien für relationale Schemata und Datenhygiene](#cdc)

   >[!IMPORTANT]
   >
   > Nur **dateibasierten Quellen** jede Zeile in der Datendatei eine `_change_request_type` Spalte mit den Werten `U` (upsert) oder `D` (delete) enthalten. Ohne diese Spalte erkennt das System die Daten nicht als unterstützendes Änderungs-Tracking, und der Umschalter Orchestrierte Kampagne wird nicht angezeigt, was verhindert, dass der Datensatz für die Zielgruppenbestimmung ausgewählt wird.

   ![](assets/S3_config_6.png)

1. Wählen Sie den zuvor erstellten Datensatz aus und klicken Sie auf **[!UICONTROL Weiter]**.

   ![](assets/S3_config_3.png)

1. Wenn Sie nur dateibasierte Quellen verwenden, laden Sie über das Fenster **[!UICONTROL Daten auswählen]** Ihre lokalen Dateien hoch und zeigen Sie eine Vorschau ihrer Struktur und Inhalte an.

   Beachten Sie, dass die maximal unterstützte Größe 100 MB beträgt.

1. Überprüfen Sie **[!UICONTROL Fenster]** Zuordnung“, ob jedes Quelldateiattribut den entsprechenden Feldern im Zielschema korrekt zugeordnet ist. [Erfahren Sie mehr über Zielgruppendimensionen](target-dimension.md)

   Klicken Sie auf **[!UICONTROL Weiter]**, sobald Sie fertig sind.

   ![](assets/S3_config_4.png)

1. Konfigurieren Sie den Datenfluss **[!UICONTROL Zeitplan]** basierend auf der von Ihnen gewünschten Häufigkeit.

1. Klicken Sie auf **[!UICONTROL Beenden]**, um den Datenfluss zu erstellen. Er wird automatisch nach dem festgelegten Zeitplan ausgeführt.

1. Wählen Sie im Menü **[!UICONTROL Verbindungen]** die Option **[!UICONTROL Quellen]** aus und greifen Sie auf die Registerkarte **[!UICONTROL Datenflüsse]** zu, um die Flussausführung zu verfolgen, aufgenommene Einträge zu überprüfen und Fehler zu beheben.

   ![](assets/S3_config_5.png)


