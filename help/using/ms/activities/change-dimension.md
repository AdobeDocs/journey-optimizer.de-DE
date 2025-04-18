---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Dimensionsänderung“
description: Erfahren Sie, wie Sie die Aktivität „Dimensionsänderung“ verwenden
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: f0213f1270e9821b61a5dc396e39f5707f8f4b42
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 60%

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

Die Aktivität **Dimensionsänderung** ist eine Aktivität zur **Zielgruppenbestimmung**. Mit dieser Aktivität können Sie die Zielgruppendimension ändern, während Sie Ihre orchestrierte Kampagne erstellen. Die Achse wird je nach Datenvorlage und der Eingabedimension verschoben.

Sie können beispielsweise die Zielgruppendimension einer orchestrierten Kampagne von „Profil“ in „Verträge“ ändern, um Nachrichten an den ausgewählten Vertragsinhaber zu senden.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Konfigurieren der Aktivität „Dimensionsänderung“ {#configure}

Gehen Sie folgendermaßen vor, um die Aktivität **Dimensionsänderung** zu konfigurieren:

1. Fügen Sie **orchestrierten Kampagne eine** Dimensionsänderung“ hinzu.

   ![](assets/change-dimension.png)

1. Definieren Sie die **neue Zielgruppendimension**. Während der Dimensionsänderung werden alle Datensätze beibehalten.

1. Führen Sie die orchestrierte Kampagne aus, um das Ergebnis anzuzeigen. Vergleichen Sie die Daten in den Tabellen vor und nach der Aktivität Dimensionsänderung und vergleichen Sie die Struktur der orchestrierten Kampagnentabellen.

## Beispiel {#example}

In diesem Beispiel möchten wir einen SMS-Versand an alle Profile senden, die einen Kauf getätigt haben. Dazu verwenden wir zunächst die Aktivität **[!UICONTROL Zielgruppe erstellen]**, die mit einer benutzerdefinierten Zielgruppendimension „Kauf“ verknüpft ist, um alle erfolgten Käufe auszuwählen.

Anschließend verwenden wir die Aktivität **[!UICONTROL Dimensionsänderung]**, um die Zielgruppendimension der orchestrierten Kampagne in „Empfänger“ zu ändern. Auf diese Weise können wir die Empfängerinnen und Empfänger ansprechen, die der Abfrage entsprechen.

![](assets/change-dimension-example.png)
