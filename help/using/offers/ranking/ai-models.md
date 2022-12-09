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
ht-degree: 0%

---

# Erste Schritte mit KI-Modellen {#ai-models}

[!DNL Journey Optimizer] ermöglicht Ihnen die Verwendung eines trainierten Modellsystems, das Angebote nach Rangfolge für ein bestimmtes Profil anzeigt.

Mit dieser Funktion können Sie verschiedene **AI-Modelle** basierend auf Ihren Geschäftszielen. Mithilfe dieser verschiedenen zielbasierten Strategien bei einer Entscheidung hilft Ihnen das trainierte Modellsystem zu verstehen, wie sich die verschiedenen KI-Modelle auf Ihre Ziele auswirken.

Sie können beispielsweise ein KI-Modell für den E-Mail-Kanal und ein anderes für den Push-Kanal auswählen. Für jeden Kanal nutzt das trainierte Modellsystem mehrere Datenpunkte, um zu bestimmen, welches Angebot zuerst für eine bestimmte Platzierung unterbreitet werden soll, anstatt die Prioritätswerte der Angebote oder eine [Rangformel](create-ranking-formulas.md).

## AI-Modelltypen {#ai-model-types}

Zwei Arten von KI-Modellen sind in verfügbar [!DNL Journey Optimizer]:

* **Modelle zur automatischen Optimierung** Ziel ist die Bereitstellung von Angeboten, die die von Geschäftskunden festgelegten Renditen (KPIs) maximieren. Diese KPIs können in Form von Konversionsraten, Umsatz usw. vorliegen. Zu diesem Zeitpunkt konzentriert sich die automatisierte Optimierung auf die Optimierung von Angebotsklicks mit Angebotskonversion als Ziel. Die automatische Optimierung ist nicht personalisiert und wird auf der Grundlage der &quot;globalen&quot;Leistung der Angebote optimiert. [Weitere Infos](auto-optimization-model.md)

* **Personalisierungsmodelle** ermöglichen es Ihnen, Geschäftsziele zu definieren und mithilfe von Kundendaten geschäftsorientierte Modelle zu schulen, um personalisierte Angebote bereitzustellen und KPIs zu maximieren. [Weitere Infos](personalized-optimization-model.md)

   >[!CAUTION]
   >
   >Die Verwendung personalisierter Optimierungsmodelle ist derzeit nur für ausgewählte Benutzer in einem frühen Zugriff verfügbar.

## Erstellen eines KI-Modells {#create-ai-model}

Die wichtigsten Schritte zum Erstellen und Verwenden von AI-Modellen sind:

1. Erstellen Sie einen Datensatz, in dem Konversions- und Impressionsereignisse erfasst werden. [Weitere Infos](create-dataset.md)
1. Erstellen Sie ein KI-Modell, das Ereignisse aus dem Datensatz nutzt, um Angebote zu ordnen. [Weitere Infos](create-ranking-strategies.md)
1. Konfigurieren Sie Ihr Angebotsschema zur automatischen Erfassung von Ereignissen. [Weitere Infos](schema-requirement.md)
1. Weisen Sie das KI-Modell einer Platzierung in einer Entscheidung zu, um geeignete Angebote zu bewerten. [Weitere Infos](../offer-activities/configure-offer-selection.md)
