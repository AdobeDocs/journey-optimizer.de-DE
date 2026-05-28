---
title: Rangfolgenmethoden
description: Weitere Informationen zur Arbeit mit Rangfolgemethoden
feature: Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/1qUj05fLaRqqJGfaoL-y5uwtknp7HDkWKocHMde-8lc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 205
ht-degree: 100%

---

# Rangfolgenmethoden {#rankings}

Mit Rangfolgenmethoden können Elemente, die für ein bestimmtes Profil angezeigt werden sollen, nach Rang geordnet werden. Nachdem eine Rangfolgenmethode erstellt wurde, kann sie einer Entscheidungsstrategie zugewiesen werden, um festzulegen, welche Elemente zuerst ausgewählt werden sollen.

Es stehen zwei Arten von Rangfolgemethoden zur Verfügung:

* Mithilfe von **Formeln** kann festgelegt werden, welches Element zuerst angezeigt werden soll, anstatt die Prioritätswerte der Elemente zu berücksichtigen.

* **KI-Modelle** ermöglichen es, trainierte Modellsysteme zu verwenden, die mehrere Datenpunkte nutzen, um zu bestimmen, welches Element zuerst angezeigt werden soll.

## Erstellen von Rangfolgenmethoden {#create}

Gehen Sie wie folgt vor, um eine Rangfolgenmethode zu erstellen:

1. Navigieren Sie zum Menü **[!UICONTROL Strategie-Setup]** und wählen Sie dann das Menü **[!UICONTROL Formeln]** oder **[!UICONTROL KI-Modelle]** je nach dem Rangfolgentyp aus, den Sie verwenden möchten.

   ![](../assets/ranking-create.png)

1. Klicken Sie oben rechts im Bildschirm auf die Schaltfläche **[!UICONTROL Formel erstellen]** oder **[!UICONTROL KI-Modell erstellen]**.

   Detaillierte Informationen zum Erstellen von Rangfolgenformeln und KI-Modellen finden Sie in den folgenden Abschnitten:

   * [Rangfolgenformeln](ranking-formulas.md)
   * [KI-Modelle](ai-models.md)

1. Konfigurieren Sie die Formel oder das KI-Modell entsprechend Ihren Anforderungen und speichern Sie die Formel bzw. das Modell dann.

Ihre Rangfolgenmethode kann nun in einer [Auswahlstrategie](../selection-strategies.md) verwendet werden, um die geeigneten Entscheidungselemente zu ordnen.


