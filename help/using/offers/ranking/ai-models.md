---
product: experience platform
solution: Experience Platform
title: Erste Schritte mit KI-Modellen
description: Erfahren Sie mehr über KI-Modelle, mit denen Angebote nach Rang geordnet werden können
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 12bc2373ac5c391764df3880c5c87666a19e99b2
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 100%

---

# Erste Schritte mit KI-Modellen {#ai-models}

Mit [!DNL Journey Optimizer] können Sie ein System mit trainierten Modellen verwenden, das die für ein Profil anzuzeigenden Angebote in eine bestimmte Reihenfolge bringt.

Mit dieser Funktion können Sie auf der Grundlage Ihrer Geschäftsziele verschiedene **KI-Modelle** erstellen. Wenn Sie diese verschiedenen zielbasierten Strategien in einer Entscheidung verwenden, hilft Ihnen das trainierte Modellsystem zu verstehen, wie sich die verschiedenen KI-Modelle auf Ihre Ziele auswirken.

So können Sie beispielsweise ein KI-Modell für den E-Mail-Kanal und ein anderes für den Push-Kanal auswählen. Für jeden Kanal nutzt das System trainierter Modelle mehrere Datenpunkte, um zu bestimmen, welches Angebot zuerst für eine bestimmte Platzierung angezeigt werden soll, anstatt die Prioritätswerte der Angebote oder eine [Rangfolgenformel](create-ranking-formulas.md) zu berücksichtigen.

## KI-Modelltypen {#ai-model-types}

In [!DNL Journey Optimizer] sind zwei Arten von KI-Modellen verfügbar:

* Mit einem **Modell mit automatischer Optimierung** werden Angebote geschaltet, die darauf abzielen, den von Business-Kunden festgelegten Gewinn (KPIs) zu maximieren. Diese KPIs können in Form von Konversionsraten, Umsatz usw. vorliegen. Im Moment bezieht sich die automatische Optimierung auf die Optimierung von Angebotsklicks mit dem Ziel der Angebotskonvertierung. Die automatische Optimierung ist nicht personalisiert und erfolgt auf der Grundlage der „globalen“ Leistung der Angebote. [Weitere Informationen](auto-optimization-model.md)

* **Personalisierungsmodelle** ermöglichen es Ihnen, Geschäftsziele zu definieren und mithilfe von Kundendaten geschäftsorientierte Modelle zu trainieren, um personalisierte Angebote bereitzustellen und KPIs zu optimieren. [Weitere Informationen](personalized-optimization-model.md)

   >[!CAUTION]
   >
   >Einigen ausgewählten Benutzenden wird derzeit vorab Zugriff auf die Verwendung von Modellen zur personalisierten Optimierung gewährt.

## Erstellen eines KI-Modells {#create-ai-model}

Die wichtigsten Schritte zum Erstellen und Verwenden von KI-Modellen sind:

1. Erstellen Sie einen Datensatz, in dem Konversions- und Impression-Ereignisse erfasst werden. [Weitere Informationen](create-dataset.md)
1. Erstellen Sie ein KI-Modell, das Ereignisse aus dem Datensatz nutzt, um eine Rangliste von Angeboten zu erstellen. [Weitere Informationen](create-ranking-strategies.md)
1. Konfigurieren Sie Ihr Angebotsschema zur automatischen Erfassung von Ereignissen. [Weitere Informationen](schema-requirement.md)
1. Weisen Sie das KI-Modell einer Platzierung in einer Entscheidung zu, um eine Rangliste der geeigneten Angebote zu erstellen. [Weitere Informationen](../offer-activities/configure-offer-selection.md)
