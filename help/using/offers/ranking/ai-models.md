---
product: experience platform
solution: Experience Platform
title: Erste Schritte mit KI-Modellen
description: Erfahren Sie mehr über KI-Modelle, mit denen Angebote nach Rang geordnet werden können
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 12b01cb9de84399e5ede987866609acc10b64c5f
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 100%

---

# Erste Schritte mit KI-Modellen {#ai-models}

Mit [!DNL Journey Optimizer] können Sie ein System mit trainierten Modellen verwenden, das die für ein Profil anzuzeigenden Angebote in eine bestimmte Reihenfolge bringt.

Mit dieser Funktion können Sie auf der Grundlage Ihrer Geschäftsziele verschiedene **KI-Modelle** erstellen. Wenn Sie diese verschiedenen zielbasierten Strategien in einer Entscheidung verwenden, hilft Ihnen das trainierte Modellsystem zu verstehen, wie sich die verschiedenen KI-Modelle auf Ihre Ziele auswirken.

So können Sie beispielsweise ein KI-Modell für den E-Mail-Kanal und ein anderes für den Push-Kanal auswählen. Für jeden Kanal nutzt das System trainierter Modelle mehrere Datenpunkte, um zu bestimmen, welches Angebot zuerst für eine bestimmte Platzierung angezeigt werden soll, anstatt die Prioritätswerte der Angebote oder eine [Rangfolgenformel](create-ranking-formulas.md) zu berücksichtigen.

## KI-Modelltypen {#ai-model-types}

Aktuell bietet [!DNL Journey Optimizer]** ein KI-Modell, **Automatische Optimierung**, mit dem Angebote basierend auf der bisherigen Angebotsleistung optimiert werden. Detaillierte Informationen zu diesem KI-Modell finden Sie in [diesem Abschnitt](auto-optimization-model.md).

## Erstellen eines KI-Modells {#create-ai-model}

Die wichtigsten Schritte zum Erstellen und Verwenden von KI-Modellen sind:

1. Erstellen Sie einen Datensatz, in dem Konversions- und Impression-Ereignisse erfasst werden. [Weitere Informationen](create-dataset.md)
1. Erstellen Sie ein KI-Modell, das Ereignisse aus dem Datensatz nutzt, um eine Rangliste von Angeboten zu erstellen. [Weitere Informationen](create-ranking-strategies.md)
1. Konfigurieren Sie Ihr Angebotsschema zur automatischen Erfassung von Ereignissen. [Weitere Informationen](schema-requirement.md)
1. Weisen Sie das KI-Modell einer Platzierung in einer Entscheidung zu, um eine Rangliste der geeigneten Angebote zu erstellen. [Weitere Informationen](../offer-activities/configure-offer-selection.md)
