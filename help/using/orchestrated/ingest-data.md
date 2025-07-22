---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurationsschritte
description: Erfahren Sie, wie Sie Daten aus unterstützten Quellen wie SFTP, Cloud-Speicher oder Datenbanken in Adobe Experience Platform importieren.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
source-git-commit: a4337df949d25740f75204fe4530837dda1af3dd
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 7%

---

# Aufnehmen von Daten {#ingest-data}

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[ Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Ausdrücke bearbeiten](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimension ändern](activities/change-dimension.md) - [Kanalaktivitäten](activities/channels.md) - [Kombinieren](activities/combine.md) - [Anreicherung](activities/deduplication.md) - [Formulare](activities/enrichment.md) - [Abstimmung](activities/fork.md) [&#128279;](activities/reconciliation.md) [&#128279;](activities/save-audience.md) [&#128279;](activities/split.md) ->Zielgruppe speichern[ -AufspaltungWarten](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Adobe Experience Platform ermöglicht die Aufnahme von Daten aus externen Quellen und bietet Ihnen die Möglichkeit, die eingehenden Daten mithilfe von Experience Platform-Services zu strukturieren, zu kennzeichnen und anzureichern. Daten können aus verschiedensten Quellen aufgenommen werden, darunter etwa Adobe-Anwendungen, Cloud-basierte Datenspeicher und Datenbanken.

## Mit Cloud-Speicher {#ingest}


>[!IMPORTANT]
>
>Um die Datenquelle für einen Datensatz zu ändern, müssen Sie zunächst den vorhandenen Datenfluss löschen, bevor Sie einen neuen erstellen, der auf denselben Datensatz und die neue Quelle verweist.
>
>Adobe Experience Platform erzwingt eine strikte Eins-zu-eins-Beziehung zwischen Datenflüssen und Datensätzen. Auf diese Weise können Sie die Synchronisierung zwischen Quelle und Datensatz für eine genaue inkrementelle Aufnahme aufrechterhalten.


Sie können einen Datenfluss konfigurieren, um Daten aus einer Amazon S3-Quelle in Adobe Experience Platform aufzunehmen. Nach der Konfiguration ermöglicht der Datenfluss die automatisierte, geplante Aufnahme strukturierter Daten und unterstützt Echtzeit-Aktualisierungen.

1. Rufen Sie **[!UICONTROL Menü]** Verbindungen“ das Menü **[!UICONTROL Quellen]** auf.

1. Wählen Sie die Kategorie **[!UICONTROL Cloud-]**) und dann Amazon S3 aus und klicken Sie auf **[!UICONTROL Daten hinzufügen]**.

   ![](assets/admin_sources_1.png)

1. Verbinden Sie Ihr S3-Konto:

   * Mit vorhandenem Konto

   * Mit einem neuen Konto

   [Weitere Informationen hierzu finden Sie in der Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#connect).

   ![](assets/admin_sources_2.png)

1. Wählen Sie Ihren Ordner **[!UICONTROL Datenformat]**, **[!UICONTROL Trennzeichen]** und **[!UICONTROL Komprimierungstyp]**.

1. Navigieren Sie durch die verbundene S3-Quelle, bis Sie die gewünschten Ordner finden, z **B. „Treueprämien** und **Treuetransaktionen**.

1. Wählen Sie den Ordner aus, der Ihre Daten enthält.

   Durch die Auswahl eines Ordners wird sichergestellt, dass alle aktuellen und zukünftigen Dateien mit derselben Struktur automatisch verarbeitet werden. Für die Auswahl einer einzelnen Datei muss jedoch jedes neue Dateninkrement manuell hochgeladen werden.

   ![](assets/S3_config_2.png)

1. Wählen Sie Ihren Ordner **[!UICONTROL Datenformat]**, **[!UICONTROL Trennzeichen]** und **[!UICONTROL Komprimierungstyp]**. Überprüfen Sie Ihre Beispieldaten auf Genauigkeit und klicken Sie dann auf **[!UICONTROL Weiter]**.

   ![](assets/S3_config_1.png)

1. Aktivieren **[!UICONTROL Ändern der Datenerfassung]**, um nur Datensätze anzuzeigen, die relationalen Schemata zugeordnet sind und sowohl einen Primärschlüssel als auch einen Versionsdeskriptor enthalten.

   ![](assets/S3_config_6.png)

1. Wählen Sie den zuvor erstellten Datensatz aus und klicken Sie auf **[!UICONTROL Weiter]**.

   ![](assets/S3_config_3.png)

1. Überprüfen Sie **[!UICONTROL Fenster]** Zuordnung“, ob jedes Quelldateiattribut den entsprechenden Feldern im Zielschema korrekt zugeordnet ist.

   Klicken **[!UICONTROL abschließend]** Weiter“.

   ![](assets/S3_config_4.png)

1. Konfigurieren Sie den Datenfluss **[!UICONTROL Zeitplan]** basierend auf Ihrer gewünschten Häufigkeit.

1. Klicken Sie **[!UICONTROL Beenden]**, um den Datenfluss zu erstellen. Er wird automatisch nach dem festgelegten Zeitplan ausgeführt.

1. Wählen Sie im Menü **[!UICONTROL Verbindungen]** die Option **[!UICONTROL Quellen]** und greifen Sie auf die Registerkarte **[!UICONTROL Datenflüsse]** zu, um die Flussausführung zu verfolgen, aufgenommene Datensätze zu überprüfen und Fehler zu beheben.

   ![](assets/S3_config_5.png)

