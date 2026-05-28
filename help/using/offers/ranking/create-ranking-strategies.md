---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Erstellen von KI-Modellen
description: Erfahren Sie, wie Sie KI-Modelle erstellen, um Angebote in Ranglisten zu sortieren
badge: label="Vorgängerversion" type="Informative"
feature: Ranking, Decision Management
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/B33mvmBY4p0K43oK-NeaWGfbwhvHMyiLkM7dhxT8-WI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 523
ht-degree: 100%

---

# Erstellen von KI-Modellen {#ai-rankings}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../experience-decisioning/gs-experience-decisioning.md)

[!DNL Journey Optimizer] ermöglicht Ihnen die Erstellung von **KI-Modellen**, um Angebote nach Ihren Geschäftszielen zu ordnen.

>[!CAUTION]
>
>Zum Erstellen, Bearbeiten oder Löschen von KI-Modellen benötigen Sie die Berechtigung zur **Verwaltung von Rangfolgestrategien**. [Weitere Informationen](../../administration/high-low-permissions.md#manage-ranking-strategies)

## Erstellen eines KI-Modells {#create-ranking-strategy}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_metric"
>title="Optimierungsmetrik"
>abstract="[!DNL Journey Optimizer] erstellt die Rangfolge von Angeboten anhand der **Konversionsrate** (Konversionsrate = Gesamtanzahl der Konversionsereignisse / Gesamtzahl der Impression-Ereignisse). Die Konversionsrate wird anhand von zwei Metriktypen berechnet: **Impression-Ereignisse** (angezeigte Angebote) und **Konversionsereignisse** (Angebote, die zu Klicks über E-Mail oder Web führen). Diese Ereignisse werden automatisch mit dem Web SDK oder dem bereitgestellten Mobile SDK erfasst."

Gehen Sie wie folgt vor, um ein neues KI-Modell zu erstellen:

1. Erstellen Sie einen Datensatz, in dem Konversionsereignisse erfasst werden. [Weitere Informationen](../data-collection/create-dataset.md)

1. Gehen Sie im Menü **[!UICONTROL Komponenten]** zur Registerkarte **[!UICONTROL Rangfolge]** und wählen Sie **[!UICONTROL KI-Modelle]**.

   ![](../assets/ai-ranking-list.png)

   Alle bisher erstellten KI-Modelle werden aufgelistet.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL KI-Modell erstellen]**.

1. Geben Sie einen eindeutigen Namen und eine Beschreibung für das KI-Modell an und wählen Sie dann die Art des KI-Modells, das Sie erstellen möchten:

   * **[!UICONTROL Automatische Optimierung]** optimiert Angebote basierend auf der bisherigen Angebots-Performance. [Weitere Informationen](auto-optimization-model.md)
   * Die **[!UICONTROL personalisierte Optimierung]** optimiert und personalisiert Angebote auf Grundlage von Zielgruppen und Angebots-Performance. [Weitere Informationen](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >Der Abschnitt **[!UICONTROL Optimierungsmetrik]** enthält Informationen zum Konversionsereignis, das vom KI-Modell zur Berechnung des Angebotsrangs verwendet wird.
   >
   >[!DNL Journey Optimizer] erstellt die Rangfolge von Angeboten anhand der **Konversionsrate** (Konversionsrate = Gesamtanzahl der Konversionsereignisse / Gesamtzahl der Impression-Ereignisse). Die Konversionsrate wird anhand von zwei Metriktypen berechnet:
   >* **Impression-Ereignisse** (angezeigte Angebote)
   >* **Konversionsereignisse** (Angebote per E-Mail oder im Web, die zu Klicks führen).
   >
   >Diese Ereignisse werden automatisch mit dem Web SDK oder dem bereitgestellten Mobile SDK erfasst. Weitere Informationen dazu finden Sie in der [Übersicht über das Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de).

1. Wählen Sie die Datensätze aus, in denen die Konversions- und Impression-Ereignisse erfasst werden. In [diesem Abschnitt](../data-collection/create-dataset.md) erfahren Sie, wie Sie einen solchen Datensatz erstellen.<!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >In der Dropdown-Liste werden nur Datensätze angezeigt, die aus Schemata erstellt wurden, die mit der Feldergruppe (früher als Mixin bezeichnet) **[!UICONTROL Erlebnisereignis – Vorschlagsinteraktionen]** verknüpft sind.

1. Wenn Sie ein KI-Modell für die **[!UICONTROL personalisierte Optimierung]** erstellen, wählen Sie ein oder mehrere Segmente aus, die für das Training des KI-Modells verwendet werden sollen.

   ➡️ [Funktion im Video kennenlernen](#video)

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >Sie können bis zu 5 Zielgruppen auswählen.

1. Speichern und aktivieren Sie das KI-Modell.

   ![](../assets/ai-ranking-save-activate.png)

<!--
At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.
-->

Jedes Mal, wenn ein Angebot angezeigt und/oder angeklickt wird, soll nun das entsprechende Ereignis automatisch von der Feldergruppe **[!UICONTROL Erlebnisereignis – Vorschlagsinteraktionen]** mithilfe des [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=de#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} oder Mobile SDK erfasst werden.

Um Ereignistypen (angezeigtes Angebot oder angeklicktes Angebot) senden zu können, müssen Sie für jeden Ereignistyp in einem Erlebnisereignis, das an Adobe Experience Platform gesendet wird, den richtigen Wert festlegen. [Weitere Informationen](../data-collection/schema-requirement.md)

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie ein personalisiertes Optimierungsmodell erstellen und es auf eine Entscheidung anwenden.

>[!VIDEO](https://video.tv.adobe.com/v/3419954?quality=12)
