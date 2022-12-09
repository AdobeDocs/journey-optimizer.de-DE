---
title: Angebotsauswahl in Entscheidungen konfigurieren
description: Erfahren Sie, wie Sie die Angebotsauswahl in Entscheidungen verwalten.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: b890d7dc2e1508bb68d45a162236483ac6fc76bd
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 0%

---

# Angebotsauswahl in Entscheidungen konfigurieren {#offers-selection-in-decisions}

Wenn mehrere Angebote für eine bestimmte Platzierung infrage kommen, können Sie bei der Konfiguration einer Entscheidung für jedes Profil die Methode auswählen, die das beste Angebot auswählt. Sie können Angebote nach folgenden Kriterien sortieren:
* Angebotspriorität
* Ranking-Formel
* [KI-Ranking](#use-ranking-strategy)

![](../assets/offer-rank-by.png)

## Angebotspriorität {#offer-priority}

Wenn mehrere Angebote für eine bestimmte Platzierung in einer Entscheidung infrage kommen, weisen die Angebote mit der höchsten **priority** werden zuerst an die Kunden geliefert.

![](../assets/offer-priority.png)

Bei der Erstellung eines Angebots werden die Prioritätswerte der Angebote zugewiesen. Erfahren Sie, wie Sie ein personalisiertes Angebot erstellen in [diesem Abschnitt](../offer-library/creating-personalized-offers.md).

## Ranking-Formel {#assign-ranking-formula}

Zusätzlich zur Angebotspriorität können Sie mit Journey Optimizer **Ranking-Formeln**. Diese Formeln bestimmen, welches Angebot zuerst für eine bestimmte Platzierung unterbreitet werden soll, anstatt die Prioritätswerte der Angebote zu berücksichtigen.

Sie können beispielsweise die Priorität aller Angebote erhöhen, deren Enddatum in weniger als 24 Stunden beträgt, oder Angebote aus der Kategorie &quot;Wird ausgeführt&quot; ankurbeln, wenn der Zielpunkt des Profils &quot;Wird ausgeführt&quot; lautet.

Erfahren Sie, wie Sie eine Rangformel in [diesem Abschnitt](../ranking/create-ranking-formulas.md).

Nachdem eine Rangformel erstellt wurde, können Sie sie einer Platzierung in einer Entscheidung zuweisen. Gehen Sie dazu wie folgt vor:

1. Erstellen Sie eine Entscheidung oder bearbeiten Sie eine bestehende. Siehe [Entscheidungen erstellen](../offer-activities/create-offer-activities.md).

1. Fügen Sie die Platzierungen hinzu, die Ihre Angebote enthalten werden. Siehe [Platzierungen erstellen](../offer-library/creating-placements.md).

1. Fügen Sie für jede Platzierung eine Sammlung hinzu. Siehe [Kollektionen erstellen](../offer-library/creating-collections.md).

1. Auswählen **[!UICONTROL Ranking formula]** als Ranking-Methode verwenden, klicken Sie dann auf **[!UICONTROL Add ranking]**.

   ![](../assets/offer-activity-ranking.png)

1. Wählen Sie die gewünschte Rangformel aus und klicken Sie auf **[!UICONTROL Select]**.

   ![](../assets/ranking-selection.png)

Die Rangformel ist jetzt mit der Platzierung verknüpft.

Wenn mehrere Angebote berechtigt sind, in dieser Platzierung unterbreitet zu werden, verwendet die Entscheidung die Formel der Rangformel, um zu berechnen, welches Angebot zuerst bereitgestellt werden soll.

## KI-Ranking {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->

Sie können auch ein trainiertes Modellsystem verwenden, das Angebote, die für ein bestimmtes Profil angezeigt werden sollen, automatisch nach Rang geordnet, indem Sie eine Rangstrategie auswählen. Erfahren Sie, wie Sie eine Rangstrategie in [diesem Abschnitt](../ranking/create-ranking-strategies.md).

Nachdem eine Rangstrategie erstellt wurde, können Sie sie einer Platzierung in einer Entscheidung zuweisen. Gehen Sie dazu wie folgt vor:

1. Erstellen Sie eine Entscheidung oder bearbeiten Sie eine bestehende. Siehe [Entscheidungen erstellen](../offer-activities/create-offer-activities.md).

1. Fügen Sie die Platzierungen hinzu, die Ihre Angebote enthalten werden. Siehe [Platzierungen erstellen](../offer-library/creating-placements.md).

1. Fügen Sie für jede Platzierung eine Sammlung hinzu. Siehe [Kollektionen erstellen](../offer-library/creating-collections.md).

1. Angebote nach **[!UICONTROL AI ranking]** aus der Dropdownliste aus und klicken Sie auf **[!UICONTROL Add ranking]**.

   ![](../assets/ranking-selection-ai-ranking.png)

1. Wählen Sie die von Ihnen erstellte Rangstrategie aus. Alle Details der Rangstrategie werden angezeigt.

   ![](../assets/ranking-selection-ai-ranking-selected.png)

1. Klicken **[!UICONTROL Select]**. Die Rangstrategie ist nun mit der Platzierung verknüpft.

Wenn mehrere Angebote geeignet sind, bestimmt das trainierte Modellsystem, welches Angebot zuerst für eine bestimmte Platzierung unterbreitet werden soll.

