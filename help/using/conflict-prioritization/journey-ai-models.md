---
title: Journey-Schlichtungs-KI-Modelle
description: Erfahren Sie, wie Sie KI-Modelle erstellen und verwenden, um Journey für die Schlichtung zu reihen, sodass für jedes Profil der beste Journey anhand von KI-gesteuerten Scores ausgewählt wird.
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: fe6e8221201ee813251a46c6603d85f0803873c0
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 18%

---

# Verwenden von KI-Modellen zum Sortieren von Journey {#journey-ai-models}

>[!AVAILABILITY]
>
>Diese Funktion ist derzeit nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

[!DNL Adobe Journey Optimizer] können Sie steuern, welche Journey ein Profil eingeben kann, wenn diese für mehr qualifiziert sind als das System zulässt. Hierfür können Sie mithilfe von [Regelsätzen](rule-sets.md) Begrenzungen für Journey-Einträge oder gleichzeitige Zugriffe definieren. Wenn ein Profil für mehr Journey geeignet ist, als die Obergrenze zulässt, bestimmt die jedem Journey zugewiesene Priorität, welche Journey ausgewählt werden.

Anstatt Prioritäts- oder Rangfolgeformeln zu verwenden, können Sie **KI-Modelle** verwenden, um Journey basierend auf trainierten Modellbewertungen dynamisch zu sortieren. Sie können KI-Modelle über den Abschnitt **[!UICONTROL Orchestrierungs-Rangfolge]** in der Benutzeroberfläche erstellen und in Regelsätzen verwenden, um sie auf Journey anzuwenden.

Einen Überblick über die in [!DNL Journey Optimizer] verfügbaren KI-Modelltypen finden Sie unter [Erste Schritte mit KI-Modellen](../experience-decisioning/ranking/ai-models.md#ai-model-types) im Abschnitt Entscheidungsfindung .

## Erstellen eines KI-Modells {#create-ai-model}

>[!CAUTION]
>
>Zum Erstellen, Bearbeiten oder Löschen von KI-Modellen benötigen Sie die Berechtigung zur **Verwaltung von Rangfolgestrategien**. [Weitere Informationen](../administration/high-low-permissions.md#manage-ranking-strategies)

Gehen Sie wie folgt vor, um ein KI-Modell für das Journey-Ranking zu erstellen.

1. Erstellen Sie einen Datensatz, in dem Konversionsereignisse erfasst werden. [Weitere Informationen](../experience-decisioning/data-collection/create-dataset.md)

1. Rufen Sie den Abschnitt **[!UICONTROL Orchestrierungs-Rangfolge]** auf und wählen Sie dann die Registerkarte **[!UICONTROL KI-Modelle]** aus. Die Liste der zuvor erstellten KI-Modelle wird angezeigt.

1. Klicken Sie **[!UICONTROL KI-Modell erstellen]**.

1. Geben Sie einen eindeutigen Namen und bei Bedarf eine Beschreibung für das KI-Modell an.

   ![Detailbereich des KI-Modells mit Namen- und Beschreibungsfeldern](assets/journey-model-details.png){width="80%"}

   >[!NOTE]
   >
   >Das Ranking-Objekt ist die Entität, auf die die Rangfolgenformel angewendet wird. Standardmäßig ist das Ranking-Objekt auf **[!UICONTROL Journey]** festgelegt.

<!--
1. Select the type of AI model you want to create:

    * **[!UICONTROL Auto-optimization]** optimizes based on past performance. [Learn more](../experience-decisioning/ranking/auto-optimization-model.md)
    * **[!UICONTROL Personalized optimization]** optimizes and personalizes based on audiences and performance. [Learn more](../experience-decisioning/ranking/personalized-optimization-model.md)-->

1. Der **[!UICONTROL Optimierungsmetrik]** enthält Informationen zum Konversionsereignis, das vom KI-Modell verwendet wird. [!DNL Journey Optimizer] rangiert auf der Basis **Konversionsrate** (Konversionsrate = Gesamtzahl der Konversionsereignisse / Gesamtzahl der Impression-Ereignisse). Die Konversionsrate wird wie folgt berechnet:

   * **Impression-Ereignisse** (angezeigte Elemente)
   * **Konversionsereignisse** (Elemente, die zu Klicks oder Konversionen führen)

   Diese Ereignisse werden automatisch mit der Web-SDK oder der mobilen SDK erfasst. Weitere Informationen finden Sie im Überblick über das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de).

1. Wählen Sie die Datensätze aus, in denen die Konversions- und Impression-Ereignisse erfasst werden. In [diesem Abschnitt](../experience-decisioning/data-collection/create-dataset.md) erfahren Sie, wie Sie solche Datensätze erstellen.

   ![Datensatzauswahl für Konversions- und Impression-Ereignisse](../experience-decisioning/assets/ai-model-datasets.png){width="85%"}

   >[!CAUTION]
   >
   >In der Dropdown-Liste werden nur Datensätze angezeigt, die aus Schemata erstellt wurden, die mit der Feldergruppe (früher als Mixin bezeichnet) **[!UICONTROL Erlebnisereignis – Vorschlagsinteraktionen]** verknüpft sind.

1. <!--If you are creating a **[!UICONTROL Personalized optimization]** AI model, -->Wählen Sie die Segmente aus, die zum Trainieren des KI-Modells verwendet werden sollen.

   >[!NOTE]
   >
   >Sie können bis zu 5 Zielgruppen auswählen.

1. Speichern und aktivieren Sie das KI-Modell.

Das KI-Modell ist jetzt verfügbar, wenn Sie einen Regelsatz konfigurieren.

## Zuweisen des KI-Modells zu einem Regelsatz {#assign-ai-model-to-ruleset}

Um ein KI-Modell zur Rangfolge Ihrer Journey zu verwenden, müssen Sie es in einer Formel verwenden und diese Formel einem Regelsatz zuweisen.

1. Erstellen Sie eine Rangfolgenformel mit dem von Ihnen erstellten KI-Modell. [Weitere Informationen](journey-ranking-formulas.md#create-journey-ranking-formula)

1. Erstellen Sie im Menü **[!UICONTROL Geschäftsregeln]** einen Regelsatz, den Sie für die Journey-Schlichtung verwenden möchten. [Weitere Informationen](rule-sets.md#Create)

1. Wählen Sie unbedingt die Domain **[!UICONTROL Journey]** aus.

1. Legen Sie in den Eigenschaften des Regelsatzes die **[!UICONTROL Rangfolgenmethode]** auf **[!UICONTROL Formel]** (anstelle von **[!UICONTROL Priorität]**) fest.

1. Wählen Sie aus der Dropdown-Liste die Formel aus, die das von Ihnen erstellte KI-Modell verwendet.

1. Erstellen Sie die Journey-Begrenzungsregeln, die Sie dem Regelsatz hinzufügen möchten. [Weitere Informationen](journey-capping.md#create-rule)

1. Speichern Sie den Regelsatz.

Jetzt wird die Formel mit dem KI-Modell dem Regelsatz zugewiesen. Sie können diesen Regelsatz dann auf Ihre Journey anwenden.

## Anwenden des Regelsatzes auf eine Journey {#assign-rule-set-to-journey}

Gehen Sie wie folgt vor, um den Regelsatz einer Journey zuzuweisen.

1. Erstellen oder öffnen Sie die Journey, der Sie den Regelsatz zuweisen möchten. [Erfahren Sie, wie Sie eine Journey erstellen](../building-journeys/journey-gs.md)

1. Wählen Sie in den Journey-Eigenschaften den Regelsatz aus der Dropdown-Liste aus. [Weitere Informationen](journey-capping.md#apply-capping).

   >[!NOTE]
   >
   >Auf eine Journey kann jeweils nur ein Regelsatz angewendet werden.

1. Speichern Sie die Journey.

Alle Journey, die diesen Regelsatz verwenden, werden mit der ausgewählten Formel anhand des KI-Modells eingestuft, wenn die Begrenzung angewendet wird.
