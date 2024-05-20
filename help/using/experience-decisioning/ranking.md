---
title: Rangfolgemethoden
description: Weitere Informationen zur Arbeit mit Rangfolgemethoden
feature: Experience Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
badge: label="Eingeschränkte Verfügbarkeit"
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 51%

---

# Rangfolgemethoden {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="Erstellen von Ranglistenformeln"
>abstract="Mithilfe von Formeln kann festgelegt werden, welches Element zuerst angezeigt werden soll, anstatt die Prioritätswerte der Elemente zu berücksichtigen. Nachdem eine Rangfolgenmethode erstellt wurde, kann sie einer Auswahlstrategie zugewiesen werden, um festzulegen, welche Elemente zuerst ausgewählt werden sollen."

Mit Rangfolgemethoden können Elemente nach Rang geordnet werden, die für ein bestimmtes Profil angezeigt werden sollen. Nachdem eine Rangfolgenmethode erstellt wurde, kann sie einer Auswahlstrategie zugewiesen werden, um festzulegen, welche Elemente zuerst ausgewählt werden sollen.

Es stehen zwei Arten von Rangfolgemethoden zur Verfügung:

* Mithilfe von **Formeln** kann festgelegt werden, welches Element zuerst angezeigt werden soll, anstatt die Prioritätswerte der Elemente zu berücksichtigen.

* **KI-Modelle** ermöglichen es, trainierte Modellsysteme zu verwenden, die mehrere Datenpunkte nutzen, um zu bestimmen, welches Element zuerst angezeigt werden soll.

## Erstellen von Rangfolgemethoden {#create}

Gehen Sie wie folgt vor, um eine Rangmethode zu erstellen:

1. Navigieren Sie zum **[!UICONTROL Strategiekonfiguration]** und wählen Sie dann **[!UICONTROL Formeln]** oder **[!UICONTROL AI-Modelle]** -Menü abhängig vom gewünschten Ranking-Typ.

1. Klicken Sie auf **[!UICONTROL Formel erstellen]** oder **[!UICONTROL Erstellen eines KI-Modells]** in der oberen rechten Ecke des Bildschirms.

   ![](assets/ranking-create.png)

1. Konfigurieren Sie die Formel oder das AI-Modell entsprechend Ihren Anforderungen und speichern Sie sie.

   Detaillierte Informationen zum Erstellen von Ranking-Formeln und AI-Modellen finden Sie in der Dokumentation zur Entscheidungsverwaltung:

   * [Ranking-Formeln](../offers/ranking/create-ranking-formulas.md)
   * [KI-Modelle](../offers/ranking/ai-models.md)


## Nutzung von Entscheidungsobjektattributen in Formeln {#items}

Ranking-Formeln werden in **PQL-Syntax** und kann verschiedene Attribute wie Profilattribute nutzen, [Kontextdaten](context-data.md) und -Attributen im Zusammenhang mit Ihren Entscheidungselementen.

Um Attribute zu Ihren Entscheidungselementen in Formeln zu nutzen, befolgen Sie die unten stehende Syntax im Code Ihrer Rangformel. Erweitern Sie jeden Abschnitt, um weitere Informationen zu erhalten:

++ + Verwenden von Standardattributen für Entscheidungselemente

![](assets/formula-attribute.png)

+++

++ + Verwenden benutzerdefinierter Attribute von Entscheidungselementen

![](assets/formula-attribute-custom.png)

+++
