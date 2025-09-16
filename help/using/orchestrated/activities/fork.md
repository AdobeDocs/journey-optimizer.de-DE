---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Verzweigung“
description: Informationen zur Verwendung der Aktivität „Verzweigung“ in einer orchestrierten Kampagne
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: ht
source-wordcount: '139'
ht-degree: 100%

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

1. Fügen Sie Ihrer orchestrierten Kampagne eine Aktivität des Typs **[!UICONTROL Verzweigung]** hinzu.

1. Definieren Sie ein **[!UICONTROL Label]**.

1. Weisen Sie jeder ausgehenden Transition ein Label zu. Standardmäßig werden zwei Transitionen bereitgestellt.

1. Um eine Transition zu entfernen, klicken Sie auf das Symbol ![](../assets/do-not-localize/Smock_Delete_18_N.svg).

1. Klicken Sie bei Bedarf auf **[!UICONTROL Transition hinzufügen]**, um eine zusätzliche ausgehende Transition hinzuzufügen.
