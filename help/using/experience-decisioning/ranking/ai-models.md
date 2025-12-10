---
solution: Journey Optimizer
product: Journey Optimizer
title: Erste Schritte mit KI-Modellen
description: Erfahren Sie mehr über KI-Modelle, mit denen Angebote nach Rang geordnet werden können
feature: Ranking, Decision Management
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 07679823-2288-4528-b09a-12fd76a69482
version: Journey Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 100%

---

# Erste Schritte mit KI-Modellen {#ai-models}

Mit [!DNL Journey Optimizer] können Sie ein System mit trainierten Modellen verwenden, das die für ein Profil anzuzeigenden Angebote in eine bestimmte Reihenfolge bringt.

Mit dieser Funktion können Sie auf der Grundlage Ihrer Geschäftsziele verschiedene **KI-Modelle** erstellen. Wenn Sie diese verschiedenen zielbasierten Strategien in einer Entscheidung verwenden, hilft Ihnen das trainierte Modellsystem zu verstehen, wie sich die verschiedenen KI-Modelle auf Ihre Ziele auswirken.

<!--For example, you can select an AI model for the email channel and another one for the push channel. For each channel, the trained model system will leverage multiple data points to determine which offer should be presented first for a given decision policy?, rather than taking into account the offers' priority scores or a [ranking formula](create-ranking-formulas.md).

>[!IMPORTANT]
>
>For now, ranking models are not supported in Journey Optimizer authored channels.-->

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
