---
solution: Journey Optimizer
product: Journey Optimizer
title: Erste Schritte mit KI-Modellen
description: Erfahren Sie mehr über KI-Modelle, mit denen Angebote nach Rang geordnet werden können
feature: Ranking, Decisioning
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 07679823-2288-4528-b09a-12fd76a69482
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sWJEr5Pm1wl83Q-2HVb-7mqy7hasQ1ffqRDmJsOFomw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: ee394c77b226dd35a9c27f4a02e3b8d7a997ccbd
workflow-type: tm+mt
source-wordcount: 367
ht-degree: 82%

---

# Erste Schritte mit KI-Modellen {#ai-models}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Machen Sie sich mit den KI-Modelltypen für automatische Optimierung und personalisierte Optimierung und den Schritten zu ihrer Erstellung vertraut, damit Sie Angebote nach Ihren Geschäftszielen ordnen können.

>[!ENDSHADEBOX]

Mit [!DNL Journey Optimizer] können Sie ein System mit trainierten Modellen verwenden, das die für ein Profil anzuzeigenden Angebote in eine bestimmte Reihenfolge bringt.

Mit dieser Funktion können Sie auf der Grundlage Ihrer Geschäftsziele verschiedene **KI-Modelle** erstellen. Wenn Sie diese verschiedenen zielbasierten Strategien in einer Entscheidung verwenden, hilft Ihnen das trainierte Modellsystem zu verstehen, wie sich die verschiedenen KI-Modelle auf Ihre Ziele auswirken.

<!--
For example, you can select an AI model for the email channel and another one for the push channel. For each channel, the trained model system will leverage multiple data points to determine which offer should be presented first for a given decision policy?, rather than taking into account the offers' priority scores or a [ranking formula](create-ranking-formulas.md).

>[!IMPORTANT]
>
>For now, ranking models are not supported in Journey Optimizer authored channels.
-->

## KI-Modelltypen {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_exd_ai_model_type"
>title="Auswählen des Modelltyps"
>abstract="Wählen Sie den Typ des KI-Modells aus, das Sie erstellen möchten: Die **automatische Optimierung** optimiert Angebote entsprechend der Leistung früherer Angebote. Die **personalisierte Optimierung** optimiert und personalisiert Angebote hingegen basierend auf Zielgruppen und der Angebotsleistung."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Erstellen eines KI-Modells"

In [!DNL Journey Optimizer] sind zwei Arten von KI-Modellen verfügbar:

* Mit einem **Modell mit automatischer Optimierung** werden Angebote geschaltet, die darauf abzielen, den von Business-Kunden festgelegten Gewinn (KPIs) zu maximieren. Diese KPIs können in Form von Konversionsraten, Umsatz usw. vorliegen. Im Moment bezieht sich die automatische Optimierung auf die Optimierung von Angebotsklicks mit dem Ziel der Angebotskonvertierung. Die automatische Optimierung ist nicht personalisiert und erfolgt auf der Grundlage der „globalen“ Performance der Angebote. [Weitere Informationen](auto-optimization-model.md)

* **Personalisierte Optimierungsmodelle** ermöglichen es Ihnen, Geschäftsziele zu definieren und mithilfe von Kundendaten geschäftsorientierte Modelle zu trainieren, um personalisierte Angebote bereitzustellen und KPIs zu maximieren. [Weitere Informationen](personalized-optimization-model.md)

## Erstellen eines KI-Modells {#create-ai-model}

Die wichtigsten Schritte, um KI-Modelle erstellen und verwenden zu können:

1. Erstellen Sie einen Datensatz, in dem Konversions- und Impression-Ereignisse erfasst werden. [Weitere Informationen](../data-collection/create-dataset.md)

1. Erstellen Sie ein KI-Modell, das Ereignisse aus dem Datensatz nutzt, um eine Rangliste von Angeboten zu erstellen. [Weitere Informationen](create-ai-models.md)

1. Konfigurieren Sie Ihr Angebotsschema zur automatischen Erfassung von Ereignissen. [Weitere Informationen](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >Rangfolgemodelle erfordern, dass Feedback-Ereignisse als Erlebnisereignisse gesendet werden, damit sie erfasst werden können. [Weitere Informationen zur Datenerfassung bei der Entscheidungsfindung](../data-collection/data-collection.md)

1. Weisen Sie das KI-Modell einer Auswahlstrategie zu, um eine Rangliste der geeigneten Angebote zu erstellen. [Weitere Informationen](../selection-strategies.md#select-ranking-method)

1. Überwachen Sie den Trainings-Status und die Leistung Ihres KI-Modells. [Weitere Informationen](ai-model-observability.md)
