---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Erste Schritte mit KI-Modellen
description: Erfahren Sie mehr über KI-Modelle, mit denen Angebote nach Rang geordnet werden können
badge: label="Legacy" type="Informative"
feature: Ranking, Decision Management
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
version: Journey Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: ht
source-wordcount: '396'
ht-degree: 100%

---

# Erste Schritte mit KI-Modellen {#ai-models}

Mit [!DNL Journey Optimizer] können Sie ein System mit trainierten Modellen verwenden, das die für ein Profil anzuzeigenden Angebote in eine bestimmte Reihenfolge bringt.

Mit dieser Funktion können Sie auf der Grundlage Ihrer Geschäftsziele verschiedene **KI-Modelle** erstellen. Wenn Sie diese verschiedenen zielbasierten Strategien in einer Entscheidung verwenden, hilft Ihnen das trainierte Modellsystem zu verstehen, wie sich die verschiedenen KI-Modelle auf Ihre Ziele auswirken.

So können Sie beispielsweise ein KI-Modell für den E-Mail-Kanal und ein anderes für den Push-Kanal auswählen. Für jeden Kanal nutzt das System mit trainierten Modellen mehrere Datenpunkte, um zu bestimmen, welches Angebot zuerst für eine bestimmte Platzierung angezeigt werden soll, anstatt die Prioritätswerte der Angebote oder eine [Rangfolgenformel](create-ranking-formulas.md) zu berücksichtigen.

>[!IMPORTANT]
>
>Derzeit werden KI-Modelle in von Journey Optimizer erstellten Kanälen nicht unterstützt.

➡️ [Funktion im Video kennenlernen](#video)

## KI-Modelltypen {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_type"
>title="Auswählen des Modelltyps"
>abstract="Wählen Sie den Typ des KI-Modells aus, das Sie erstellen möchten: Die **automatische Optimierung** optimiert Angebote entsprechend der Leistung früherer Angebote. Die **personalisierte Optimierung** optimiert und personalisiert Angebote hingegen basierend auf Zielgruppen und der Angebotsleistung."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Erstellen eines KI-Modells"

In [!DNL Journey Optimizer] sind zwei Arten von KI-Modellen verfügbar:

* Mit einem **Modell mit automatischer Optimierung** werden Angebote geschaltet, die darauf abzielen, den von Business-Kunden festgelegten Gewinn (KPIs) zu maximieren. Diese KPIs können in Form von Konversionsraten, Umsatz usw. vorliegen. Im Moment bezieht sich die automatische Optimierung auf die Optimierung von Angebotsklicks mit dem Ziel der Angebotskonvertierung. Die automatische Optimierung ist nicht personalisiert und erfolgt auf der Grundlage der „globalen“ Performance der Angebote. [Weitere Informationen](auto-optimization-model.md)

* **Personalisierte Optimierungsmodelle** ermöglichen es Ihnen, Geschäftsziele zu definieren und mithilfe von Kundendaten geschäftsorientierte Modelle zu trainieren, um personalisierte Angebote bereitzustellen und KPIs zu maximieren. [Weitere Informationen](personalized-optimization-model.md)

## Erstellen eines KI-Modells {#create-ai-model}

Die wichtigsten Schritte zum Erstellen und Verwenden von KI-Modellen sind:

1. Erstellen Sie einen Datensatz, in dem Konversions- und Impression-Ereignisse erfasst werden. [Weitere Informationen](../data-collection/create-dataset.md)

1. Erstellen Sie ein KI-Modell, das Ereignisse aus dem Datensatz nutzt, um eine Rangliste von Angeboten zu erstellen. [Weitere Informationen](create-ranking-strategies.md)

1. Konfigurieren Sie Ihr Angebotsschema zur automatischen Erfassung von Ereignissen. [Weitere Informationen](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >KI-Modelle erfordern, dass Feedback-Ereignisse als Erlebnisereignisse gesendet werden, damit sie erfasst werden können. [Weitere Informationen zur Datenerfassung beim Entscheidungs-Management](../data-collection/data-collection.md)

1. Weisen Sie das KI-Modell einer Platzierung in einer Entscheidung zu, um eine Rangliste der geeigneten Angebote zu erstellen. [Weitere Informationen](../offer-activities/configure-offer-selection.md)

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie ein KI-Modell für Angebotsentscheidung erstellen und wie es auf eine Entscheidung angewendet wird.

>[!VIDEO](https://video.tv.adobe.com/v/3419959?quality=12)
