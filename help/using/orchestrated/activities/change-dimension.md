---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Dimensionsänderung“
description: Erfahren Sie, wie Sie die Aktivität „Dimensionsänderung“ verwenden
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 62%

---

# Ändern der Dimension {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Erzeugen eines Komplements"
>abstract="Sie können eine zusätzliche ausgehende Transition mit der verbleibenden Population generieren, die als Duplikat ausgeschlossen wurde. Schalten Sie dazu die Option **Komplement erzeugen** ein"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Aktivität „Dimensionsänderung“"
>abstract="Mithilfe dieser Aktivität können Sie die Zielgruppendimension beim Erstellen einer Zielgruppe ändern. Diese Aktivität verschiebt die Achse je nach Datenvorlage und der Eingabedimension. Beispielsweise können Sie von der Dimension „Verträge“ zur Dimension „Kundinnen und Kunden“ wechseln."

+++ Inhaltsverzeichnis

| Willkommen bei orchestrierten Kampagnen | Starten der ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](../gs-schemas.md)</li><li>[Manuelles Schema](../manual-schema.md)</li><li>[Datei-Upload-Schema](../file-upload-schema.md)</li><li>[Daten aufnehmen](../ingest-data.md)</li></ul>[Zugreifen auf und Verwalten von orchestrierten Kampagnen](../access-manage-orchestrated-campaigns.md) | [Wichtige Schritte zum Erstellen einer orchestrierten Kampagne](../gs-campaign-creation.md)<br/><br/>[Erstellen und Planen der Kampagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](../orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](../orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](../build-query.md)<br/><br/>[Bearbeiten von Ausdrücken](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) – [Zielgruppe erstellen](build-audience.md) – <b>[Dimensionsänderung](change-dimension.md)</b> – [Kanalaktivitäten](channels.md) – [Kombinieren](combine.md) – [Deduplizierung](deduplication.md) – [Anreicherung](enrichment.md) – [Verzweigung](fork.md) – [Abstimmung](reconciliation.md) – [Zielgruppe speichern](save-audience.md) – [Aufspaltung](split.md) – [Warten](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Als Marketing-Experte können Sie die Audience-Zielgruppenbestimmung verbessern, indem Sie innerhalb einer orchestrierten Kampagne von einer Datenentität zu einer verwandten wechseln. Auf diese Weise können Sie über Benutzerprofile hinausgehen und sich auf bestimmte Verhaltensweisen wie Käufe, Buchungen oder andere Interaktionen konzentrieren.

Verwenden Sie dazu die Aktivität **[!UICONTROL Dimensionsänderung]**. Damit können Sie die Zielgruppendimension während der orchestrierten Kampagne anpassen.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Konfigurieren der Aktivität „Dimensionsänderung“ {#configure}

Gehen Sie folgendermaßen vor, um die Aktivität **[!UICONTROL Dimensionsänderung]** zu konfigurieren:

1. Fügen Sie **[!UICONTROL orchestrierten Kampagne]** Aktivität „Dimension ändern“ hinzu.

   ![](../assets/orchestrated-change-dimension.png)

1. Definieren Sie die **[!UICONTROL neue Zielgruppendimension]**. Bei einer Dimensionsänderung werden alle Einträge beibehalten.


## Beispiel {#example}

Dieser Anwendungsfall konzentriert sich auf den Versand einer SMS an Profile, die innerhalb des letzten Monats eine Wunschliste erstellt haben.

Beginnen Sie mit einer Aktivität des Typs **[!UICONTROL Zielgruppe erstellen]** und verwenden Sie die Zielgruppendimension **[!UICONTROL Wunschliste]**, um alle relevanten Wunschlisten zu ermitteln.

Fügen Sie dann eine Aktivität des Typs **[!UICONTROL Dimensionsänderung]** hinzu, um die Zielgruppendimension von **[!UICONTROL Wunschliste]** auf **[!UICONTROL Empfängerin oder Empfänger] umzustellen.** Dieser Schritt stellt sicher, dass die orchestrierte Kampagne die richtigen Profile anspricht, die mit diesen Wunschlisten verknüpft sind, sodass die SMS an die gewünschten Profile gesendet werden kann.

![](../assets/orchestrated-change-dimension-example.png)
