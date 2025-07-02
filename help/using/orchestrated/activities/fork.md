---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Verzweigung“
description: Erfahren Sie, wie Sie die Aktivität Verzweigung in einer koordinierten Kampagne verwenden
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: 28284b3d42a0e78add3470ef128dd740f9cc9dfd
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 35%

---

# Verzweigung {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="Aktivität „Verzweigung“"
>abstract="Die Aktivität **Verzweigung** ermöglicht es Ihnen, ausgehende Transitionen zu erstellen, um mehrere Aktivitäten parallel zu starten."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="Transitionen von Verzweigungsaktivitäten"
>abstract="Standardmäßig werden zwei Transitionen mit einer **Verzweigungsaktivität** erstellt. Klicken Sie auf die Schaltfläche **Transition hinzufügen**, um eine zusätzliche ausgehende Transition zu definieren, und geben Sie deren Titel ein."

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](../configuration-steps.md)<br/><br/>[Schlüsselschritte für die orchestrierte Kampagnenerstellung](../gs-campaign-creation.md) | [Erstellen einer orchestrierten Kampagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](../orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit der Abfrage Modeler](../orchestrated-rule-builder.md)<br/><br/>[Erstellen Sie Ihre ersten ](../build-query.md)<br/><br/>[-Bearbeitungsausdrücke](../edit-expressions.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) - [Zielgruppe aufbauen](build-audience.md) - [Dimension ändern](change-dimension.md) - [Kanalaktivitäten](channels.md) - [Kombinieren](combine.md) - [Anreicherung](deduplication.md) - [Verzweigung](enrichment.md) - [Abstimmung](fork.md) [&#128279;](reconciliation.md) [&#128279;](split.md) - Aufspaltung[Warten](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Die Aktivität **[!UICONTROL Verzweigung]** ist eine Komponente **[!UICONTROL Fluss-Steuerung]** mit der Sie mehrere ausgehende Transitionen erstellen können, sodass mehrere Aktivitäten parallel ausgeführt werden können.

## Konfigurieren der Verzweigungsaktivität{#fork-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **[!UICONTROL Verzweigung]** zu konfigurieren:

![](../assets/workflow-fork.png)

1. Fügen Sie **[!UICONTROL orchestrierten Kampagne]** Aktivität Verzweigung hinzu.

1. Definieren Sie ein **[!UICONTROL label]**.

1. Weisen Sie jeder ausgehenden Transition einen Titel zu. Standardmäßig werden zwei Transitionen bereitgestellt.

1. Um eine Transition zu entfernen, klicken Sie auf das Symbol ![](../assets/do-not-localize/Smock_Delete_18_N.svg) .

1. Klicken Sie bei Bedarf auf **[!UICONTROL Transition hinzufügen]**, um eine zusätzliche ausgehende Transition hinzuzufügen.
