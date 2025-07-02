---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Dimensionsänderung“
description: Erfahren Sie, wie Sie die Aktivität „Dimensionsänderung“ verwenden
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 8a6fc9fca96bfab90a72be329e2ab99c6942a4a7
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 32%

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

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](../configuration-steps.md)<br/><br/>[Schlüsselschritte für die orchestrierte Kampagnenerstellung](../gs-campaign-creation.md) | [Erstellen einer orchestrierten Kampagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](../orchestrate-activities.md)<br/><br/><br/>[Starten und Überwachen der Kampagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit der Abfrage Modeler](../orchestrated-rule-builder.md)<br/><br/>[Erstellen Sie Ihre ersten ](../build-query.md)<br/><br/>[-Bearbeitungsausdrücke](../edit-expressions.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) - [Zielgruppe aufbauen](build-audience.md) - **[Dimension ändern](change-dimension.md)** - [Kanalaktivitäten](channels.md) - [Kombinieren](combine.md) - [Anreicherung](deduplication.md) - [Verzweigung](enrichment.md) - [Abstimmung](fork.md) [ ](reconciliation.md) [ ](split.md) - Aufspaltung[Warten](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Als Marketing-Experte können Sie das Audience-Targeting einschränken, indem Sie innerhalb einer orchestrierten Kampagne von einer Datenentität zu einer anderen verknüpften Entität wechseln. Auf diese Weise können Sie Benutzerprofile nicht mehr auswählen, sondern sich auf bestimmte Aktionen wie Käufe, Buchungen oder andere Interaktionen konzentrieren.

Verwenden Sie dazu die Aktivität **[!UICONTROL Dimensionsänderung]** . Auf diese Weise können Sie die Zielgruppendimension während der orchestrierten Kampagne ändern, basierend auf der Struktur Ihres Datenmodells und der Eingabedimension.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Konfigurieren der Aktivität „Dimensionsänderung“ {#configure}

Gehen Sie folgendermaßen vor, um die Aktivität **[!UICONTROL Dimensionsänderung]** zu konfigurieren:

1. Fügen Sie **[!UICONTROL orchestrierten Kampagne eine]** Dimensionsänderung“ hinzu.

   ![](../assets/change-dimension.png)

1. Definieren Sie die **[!UICONTROL neue Zielgruppendimension]**. Während der Dimensionsänderung werden alle Datensätze beibehalten.

1. Führen Sie die orchestrierte Kampagne aus, um das Ergebnis anzuzeigen. Vergleichen Sie die Daten in den Tabellen vor und nach der Aktivität Dimensionsänderung und vergleichen Sie die Struktur der orchestrierten Kampagnentabellen.

## Beispiel {#example}

Dieser Anwendungsfall umfasst das Senden einer SMS an Profile, die im letzten Monat eine Wunschliste erstellt haben.

Beginnen Sie mit der Aktivität **[!UICONTROL Zielgruppe aufbauen]** , indem Sie die Zielgruppendimension **[!UICONTROL Wunschliste]** verwenden, um alle relevanten Wunschlisten auszuwählen.

Fügen Sie als Nächstes eine Aktivität **[!UICONTROL Dimension ändern]** ein, um die Zielgruppendimension von **[!UICONTROL Wunschliste]** auf **[!UICONTROL Empfänger]** umzustellen. Dies ermöglicht es der orchestrierten Kampagne, die SMS an die mit diesen Wunschlisten verknüpften Profile zu senden.

![](../assets/orchestrated-change-dimension-example.png)
