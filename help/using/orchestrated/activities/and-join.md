---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Und-Verknüpfung“
description: Erfahren Sie, wie Sie die Aktivität „Und-Verknüpfung“ in einer orchestrierten Kampagne verwenden
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 8a5026cdeb63b7b261ec0dfa690c5bd41d7de772
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 38%

---

# Und-Verknüpfung {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Aktivität &quot;Und-Verknüpfung&quot;"
>abstract="Mit der Aktivität **Und-Verknüpfung** können Sie die Ausführung verschiedener Verzweigungen einer orchestrierten Kampagne synchronisieren. Sie wird ausgelöst, sobald alle vorangehenden Aktivitäten beendet sind. Auf diese Weise können Sie sicherstellen, dass bestimmte Aktivitäten abgeschlossen sind, bevor Sie mit der Ausführung der orchestrierten Kampagne fortfahren."


+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](../configuration-steps.md)<br/><br/>[Zugreifen auf und Verwalten von orchestrierten Kampagnen](../access-manage-orchestrated-campaigns.md) | [Wichtige Schritte für die orchestrierte Kampagnenerstellung](../gs-campaign-creation.md)<br/><br/>[Erstellen und Planen der Kampagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](../orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](../orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](../build-query.md)<br/><br/>[Ausdrücke bearbeiten](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/><b>[Und-Verknüpfung](and-join.md)</b> - [Zielgruppe aufbauen](build-audience.md) - [Dimension ändern](change-dimension.md) - [Kanalaktivitäten](channels.md) - [Kombinieren](combine.md) - [Anreicherung](deduplication.md) - [Formulare](enrichment.md) - [Abstimmung](fork.md) [ ](reconciliation.md) [ ](save-audience.md) [ ](split.md) ->Zielgruppe speichern[ -AufspaltungWarten](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Die Aktivität **[!UICONTROL Und-Verknüpfung]** ist eine Aktivität zur **[!UICONTROL Flusskontrolle]**. Dies ermöglicht es, die Ausführung verschiedener Kampagnenzweige zu synchronisieren.

Diese Aktivität löst ihre ausgehende Transition erst aus, wenn alle eingehenden Transitionen aktiviert sind, d. h. wenn alle vorangegangenen Aktivitäten beendet sind. Auf diese Weise können Sie sicherstellen, dass bestimmte Aktivitäten abgeschlossen sind, bevor Sie mit der Ausführung der orchestrierten Kampagne fortfahren.

## Konfigurieren der Aktivität „Und-Verknüpfung“{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Zusammenführungssoptionen"
>abstract="Wählen Sie die Aktivitäten aus, die Sie verknüpfen möchten. Wählen Sie in der Dropdown-Liste **Hauptmenge** die Population der eingehenden Transition aus, die Sie beibehalten möchten."

Führen Sie die folgenden Schritte aus, um die Aktivität **[!UICONTROL Und-Verknüpfung]** zu konfigurieren:

![](../assets/workflow-andjoin.png)

1. Fügen Sie mehrere Aktivitäten hinzu, z. B. Kanalaktivitäten, um mindestens zwei verschiedene Ausführungszweige zu erstellen.

1. Fügen Sie eine **[!UICONTROL AND-Join]**-Aktivität in einen der Zweige ein.

1. Wählen Sie **[!UICONTROL Abschnitt „Zusammenführungsoptionen]** alle vorherigen Aktivitäten aus, die Sie zusammenführen möchten.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL 0}Primäre Transition die Population der eingehenden Transition aus, die Sie beibehalten möchten.]**

## Beispiel{#and-join-example}

Dieses Beispiel zeigt zwei koordinierte Kampagnenzweige, von denen jeder einen E-Mail-Versand aufweist, wobei der eine an Gold-Mitglieder und der andere an Silber gerichtet ist. Die **[!UICONTROL UND-Verknüpfung]** wird aktiviert, sobald beide eingehenden Transitionen ausgelöst werden, und die SMS wird erst nach Abschluss beider E-Mail-Sendungen gesendet, nach einer Verzögerung von 7 Tagen.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
