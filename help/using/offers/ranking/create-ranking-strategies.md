---
product: experience platform
solution: Experience Platform
title: Erstellen von KI-Modellen
description: Erfahren Sie, wie Sie KI-Modelle zum Rang von Angeboten erstellen
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 3188bc97b8103d2a01101a23d8c242a3e2924f76
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Erstellen von KI-Modellen {#ai-rankings}

[!DNL Journey Optimizer] ermöglicht Ihnen die Erstellung von **AI-Modelle** , um Angebote nach Ihren Geschäftszielen zu ordnen.

>[!CAUTION]
>
>Zum Erstellen, Bearbeiten oder Löschen von KI-Modellen benötigen Sie die **Verwalten von Ranking Strategies** Berechtigung. [Weitere Infos](../../administration/high-low-permissions.md#manage-ranking-strategies)

## Erstellen eines KI-Modells {#create-ranking-strategy}

Gehen Sie wie folgt vor, um ein KI-Modell zu erstellen:

1. Im **[!UICONTROL Components]** -Menü, um auf die **[!UICONTROL Ranking]** Registerkarte und wählen Sie **[!UICONTROL AI models]**.

   ![](../assets/ai-ranking-list.png)

   Alle bisher erstellten KI-Modelle sind aufgelistet.

1. Klicken Sie auf **[!UICONTROL Create AI model]** Schaltfläche.

1. Geben Sie einen eindeutigen Namen und eine Beschreibung für das AI-Modell an und wählen Sie dann den Typ des AI-Modells aus, das Sie erstellen möchten:

   * **[!UICONTROL Auto-optimization]** optimiert Angebote basierend auf der bisherigen Angebotsleistung. [Weitere Infos](auto-optimization-model.md)
   * **[!UICONTROL Personalized]** Optimiert und personalisiert Angebote auf der Grundlage von Segmenten und der Angebotsleistung. [Weitere Infos](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >Die **[!UICONTROL Optimization metric]** enthält Informationen zum Konversionsereignis, das vom KI-Modell zur Berechnung des Angebotrangs verwendet wird.
   >
   >[!DNL Journey Optimizer] Angebote anhand der **Konversionsrate** (Konversionsrate = Gesamtanzahl der Konversionsereignisse / Gesamtzahl der Impressionsereignisse). Die Konversionsrate wird anhand von zwei Metriktypen berechnet:
   >* **Impressionsereignisse** (angezeigte Angebote)
   >* **Konversionsereignisse** (Angebote, die zu Klicks per E-Mail oder Web führen).

   >
   >Diese Ereignisse werden automatisch mit dem Web SDK oder dem bereitgestellten Mobile SDK erfasst. Weitere Informationen hierzu finden Sie unter [Übersicht über das Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=en).

1. Wählen Sie die Datensätze aus, in denen die Konversions- und Impressionsereignisse erfasst werden. Erfahren Sie, wie Sie einen solchen Datensatz erstellen in [diesem Abschnitt](#create-dataset). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >Nur Datensätze, die aus Schemata erstellt wurden, die mit dem **[!UICONTROL Experience Event - Proposition Interactions]** Feldergruppe (zuvor Mixin genannt) wird in der Dropdown-Liste angezeigt.

1. Wenn Sie eine **[!UICONTROL Personalization]** AI-Modell wählen Sie die Segmente aus, die zum Trainieren des KI-Modells verwendet werden sollen.

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >Sie können bis zu 5 Segmente auswählen.

1. Speichern und aktivieren Sie das KI-Modell.

   ![](../assets/ai-ranking-save-activate.png)
