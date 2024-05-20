---
title: Rangfolgenmethoden
description: Weitere Informationen zur Arbeit mit Rangfolgemethoden
feature: Experience Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
badge: label="Eingeschränkte Verfügbarkeit"
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: ht
source-wordcount: '308'
ht-degree: 100%

---

# Rangfolgenmethoden {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="Erstellen von Ranglistenformeln"
>abstract="Mithilfe von Formeln kann festgelegt werden, welches Element zuerst angezeigt werden soll, anstatt die Prioritätswerte der Elemente zu berücksichtigen. Nachdem eine Rangfolgenmethode erstellt wurde, kann sie einer Entscheidungsstrategie zugewiesen werden, um festzulegen, welche Elemente zuerst ausgewählt werden sollen."

Mit Rangfolgenmethoden können Elemente, die für ein bestimmtes Profil angezeigt werden sollen, nach Rang geordnet werden. Nachdem eine Rangfolgenmethode erstellt wurde, kann sie einer Entscheidungsstrategie zugewiesen werden, um festzulegen, welche Elemente zuerst ausgewählt werden sollen.

Es stehen zwei Arten von Rangfolgemethoden zur Verfügung:

* Mithilfe von **Formeln** kann festgelegt werden, welches Element zuerst angezeigt werden soll, anstatt die Prioritätswerte der Elemente zu berücksichtigen.

* **KI-Modelle** ermöglichen es, trainierte Modellsysteme zu verwenden, die mehrere Datenpunkte nutzen, um zu bestimmen, welches Element zuerst angezeigt werden soll.

## Erstellen von Rangfolgenmethoden {#create}

Gehen Sie wie folgt vor, um eine Rangfolgenmethode zu erstellen:

1. Navigieren Sie zum Menü **[!UICONTROL Strategie-Setup]** und wählen Sie dann das Menü **[!UICONTROL Formeln]** oder **[!UICONTROL KI-Modelle]** je nach dem Rangfolgetyp aus, den Sie verwenden möchten.

1. Klicken Sie oben rechts im Bildschirm auf die Schaltfläche **[!UICONTROL Formel erstellen]** oder **[!UICONTROL KI-Modell erstellen]**.

   ![](assets/ranking-create.png)

1. Konfigurieren Sie die Formel oder das KI-Modell entsprechend Ihren Anforderungen und speichern Sie sie die Formel bzw. das Modell.

   Detaillierte Informationen zum Erstellen von Rangfolgeformeln und KI-Modellen finden Sie in der Dokumentation zum Entscheidungs-Management:

   * [Ranking-Formeln](../offers/ranking/create-ranking-formulas.md)
   * [KI-Modelle](../offers/ranking/ai-models.md)


## Nutzen von Entscheidungselementattributen in Formeln {#items}

Rangfolgeformeln werden in **PQL-Syntax** ausgedrückt und können verschiedene Attribute wie Profilattribute, [Kontextdaten](context-data.md) und Attribute im Zusammenhang mit Ihren Entscheidungselementen nutzen.

Um Attribute im Zusammenhang mit Ihren Entscheidungselementen in Formeln zu nutzen, befolgen Sie die unten stehende Syntax im Code Ihrer Rangfolgeformel. Erweitern Sie jeden Abschnitt, um weitere Informationen zu erhalten:

+++Verwenden von Standardattributen von Entscheidungselementen

![](assets/formula-attribute.png)

+++

+++Verwenden benutzerdefinierter Attribute von Entscheidungselementen

![](assets/formula-attribute-custom.png)

+++
