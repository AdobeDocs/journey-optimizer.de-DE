---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Verzweigung“
description: Erfahren Sie, wie Sie die Aktivität Verzweigung in einer koordinierten Kampagne verwenden
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 86%

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

Die Aktivität **[!UICONTROL Verzweigung]** ist eine Komponente des Typs **[!UICONTROL Flusskontrolle]**, mit der Sie mehrere ausgehende Transitionen erstellen können, um mehrere Aktivitäten parallel auszuführen.

## Konfigurieren der Verzweigungsaktivität{#fork-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **[!UICONTROL Verzweigung]** zu konfigurieren:

![](../assets/workflow-fork.png)

1. Fügen Sie **[!UICONTROL orchestrierten Kampagne]** Aktivität Verzweigung hinzu.

1. Definieren Sie ein **[!UICONTROL Label]**.

1. Weisen Sie jeder ausgehenden Transition ein Label zu. Standardmäßig werden zwei Transitionen bereitgestellt.

1. Um eine Transition zu entfernen, klicken Sie auf das Symbol ![](../assets/do-not-localize/Smock_Delete_18_N.svg).

1. Klicken Sie bei Bedarf auf **[!UICONTROL Transition hinzufügen]**, um eine zusätzliche ausgehende Transition hinzuzufügen.
