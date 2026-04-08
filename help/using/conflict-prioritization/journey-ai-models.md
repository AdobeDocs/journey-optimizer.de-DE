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
exl-id: 3e7c3069-b022-4709-936d-acaad56b5882
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 14%

---

# Verwenden von KI-Modellen zum Sortieren von Journey {#journey-ai-models}

>[!AVAILABILITY]
>
>Diese Funktion ist derzeit nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

[!DNL Adobe Journey Optimizer] können Sie steuern, welche Journey ein Profil eingeben kann, wenn diese für mehr qualifiziert sind als das System zulässt. Hierfür können Sie mithilfe von [Regelsätzen](rule-sets.md) Begrenzungen für Journey-Einträge oder gleichzeitige Zugriffe definieren. Wenn ein Profil für mehr Journey geeignet ist, als die Obergrenze zulässt, bestimmt die jedem Journey zugewiesene Priorität, welche Journey ausgewählt werden.

Anstatt Priorität zu verwenden, können Sie auch **KI-Modelle** in Ihren Rangfolgeformeln verwenden, um Journey basierend auf trainierten Modellbewertungen dynamisch zu reihen.

## Erstellen eines KI-Modells {#create-ai-model}

<!--
Do you need specific permissions to create AI models?
>[!CAUTION]
>
>To create, edit, or delete AI models, you must have the **Manage Ranking Strategies** permission. [Learn more](../administration/high-low-permissions.md#manage-ranking-strategies)
-->

Gehen Sie wie folgt vor, um ein KI-Modell für das Journey-Ranking zu erstellen.

1. Erstellen Sie einen Datensatz, in dem Konversionsereignisse erfasst werden. [Weitere Informationen](../experience-decisioning/data-collection/create-dataset.md)

1. Rufen Sie den Abschnitt **[!UICONTROL Orchestrierungs-Rangfolge]** auf und wählen Sie dann die Registerkarte **[!UICONTROL KI-Modelle]** aus. Die Liste der zuvor erstellten KI-Modelle wird angezeigt.

1. Klicken Sie **[!UICONTROL KI-Modell erstellen]**.

1. Geben Sie einen eindeutigen Namen und bei Bedarf eine Beschreibung für das KI-Modell an.

   ![KI-Modelldetails mit den Feldern Name und Beschreibung](assets/journey-model-details.png){width="85%"}

   >[!NOTE]
   >
   >Das Ranking-Objekt ist die Entität, auf die die Rangfolgenformel angewendet wird. Standardmäßig ist das Ranking-Objekt auf **[!UICONTROL Journey]** festgelegt.

<!--
1. Select the type of AI model you want to create:

    * **[!UICONTROL Auto-optimization]** optimizes based on past performance. [Learn more](../experience-decisioning/ranking/auto-optimization-model.md)
    * **[!UICONTROL Personalized optimization]** optimizes and personalizes based on audiences and performance. [Learn more](../experience-decisioning/ranking/personalized-optimization-model.md)
-->

1. Im Abschnitt **[!UICONTROL Optimierungsmetrik]** werden alle Metriken aus Ihrer [!DNL Customer Journey Analytics] ([) ](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-dataviews/data-views){target="_blank"} Liste angezeigt. Wählen Sie die Metrik aus, für die Sie Ihr Modell optimieren möchten.

   ![Dropdown-Liste Optimierungsmetrik mit Customer Journey Analytics-Metriken für das KI-Modell](assets/journey-model-metrics.png){width="70%"}

   [!DNL Journey Optimizer] rangiert auf der Basis **Konversionsrate** (Konversionsrate = Gesamtzahl der Konversionsereignisse / Gesamtzahl der Impression-Ereignisse). Die Konversionsrate wird wie folgt berechnet:

   * **Impression-Ereignisse** (angezeigte Elemente)
   * **Konversionsereignisse** (Elemente, die zu Klicks oder Konversionen führen)

   Diese Ereignisse werden automatisch mit der Web-SDK oder der mobilen SDK erfasst. Weitere Informationen finden Sie im Überblick über das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de).

1. Wählen Sie die Datensätze aus, in denen die Konversions- und Impression-Ereignisse erfasst werden. In [diesem Abschnitt](../experience-decisioning/data-collection/create-dataset.md) erfahren Sie, wie Sie solche Datensätze erstellen.

   ![Datensatzauswahl für Konversions- und Impression-Ereignisse](../experience-decisioning/assets/ai-model-datasets.png){width="85%"}

   >[!CAUTION]
   >
   >In der Dropdown-Liste werden nur Datensätze angezeigt, die aus Schemata erstellt wurden **[!UICONTROL die mit der Feldergruppe]** Erlebnisereignis - Vorschlagsinteraktionen“ verknüpft sind. Sie können bis zu 5 Datensätze auswählen.

1. <!--If you are creating a **[!UICONTROL Personalized optimization]** AI model, -->Wählen Sie die Segmente aus, die zum Trainieren des KI-Modells verwendet werden sollen.

   >[!NOTE]
   >
   >Sie können bis zu 50 Zielgruppen auswählen.

1. Speichern und aktivieren Sie das KI-Modell.

Das KI-Modell kann jetzt ausgewählt werden, wenn Sie eine Rangfolgenformel erstellen.

## Referenzieren des KI-Modells in einer Formel, um Journey zu reihen {#reference-ai-model}

Sie können jetzt das KI-Modell als Referenz festlegen, um eine Rangfolgenformel zu erstellen, dann die Formel einem Regelsatz zuweisen und den Regelsatz auf Ihre Journey anwenden. Gehen Sie dazu wie folgt vor.

1. Erstellen Sie eine Rangfolgenformel. [Weitere Informationen](journey-ranking-formulas.md#create-journey-ranking-formula)

1. Verwenden Sie die **[!UICONTROL KI-Modell auswählen]**, um das KI-Modell auszuwählen, das Sie in der Formel verwenden möchten.

   ![Details der Journey-Rangfolgeformel mit der Schaltfläche KI-Modell auswählen](assets/journey-formula-ai-model.png){width="80%"}

1. Definieren Sie in mindestens einem der Abschnitte **[!UICONTROL Kriterium]** eine Bedingung und wählen Sie **[!UICONTROL KI-Modellwert]** als Rangfolgenmethode aus. Wenn die Journey beispielsweise das Tag „Promo“ aufweist, ist der Rangfolgenwert der KI-Modellwert.

   ![Ein Beispiel für eine Rangfolgenformel, bei dem das Tag-Kriterium „Promo“ den KI-Modellwert als Rangfolgenmethode verwendet](assets/journey-formula-ex-2.png){width="60%"}

1. Klicken Sie **[!UICONTROL Erstellen]**, um Ihre Rangfolgenformel abzuschließen.

1. Erstellen Sie jetzt einen Regelsatz und wählen Sie die Formel aus, die Sie als Rangfolgenmethode erstellt haben. [Weitere Informationen](journey-ranking-formulas.md#assign-formula-to-ruleset)

1. Erstellen Sie die Journey-Begrenzungsregeln und speichern Sie den Regelsatz.

1. Wenden Sie den Regelsatz auf die gewünschten Journey an und speichern Sie sie. [Weitere Informationen](journey-ranking-formulas.md#assign-rule-set-to-journey)

   >[!NOTE]
   >
   >Auf eine Journey kann jeweils nur ein Regelsatz angewendet werden.

Alle Journey, die diesen Regelsatz verwenden, erhalten bei Anwendung der Begrenzung eine Rangfolge mit der Formel, die auf das ausgewählte KI-Modell verweist.
