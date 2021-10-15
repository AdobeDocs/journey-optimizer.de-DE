---
title: Auswahl von Angeboten in Entscheidungen konfigurieren
description: Erfahren Sie, wie Sie die Auswahl von Angeboten in Entscheidungen verwalten.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: 43fb98a08555e6b889ad537e79dba78286dafeb9
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 100%

---

# Auswahl von Angeboten in Entscheidungen konfigurieren {#offers-selection-in-activities}

Wenn mehrere Angebote für eine bestimmte Platzierung infrage kommen, können Sie bei der Konfiguration einer Entscheidung (zuvor als Angebotsaktivität bezeichnet) die Methode auswählen, die das beste Angebot für jedes Profil auswählt. Sie können Angebote nach folgenden Kriterien sortieren:
* Angebotspriorität
* Rangfolgenformel
* [KI-Rangfolge](#use-ranking-strategy) (derzeit nur für ausgewählte Benutzer)

![](../../assets/offer-rank-by.png)

## Angebotspriorität {#about-offers-priority}

Wenn in einer Entscheidung (früher als „Angebotsaktivität“ bezeichnet) mehrere Angebote für eine bestimmte Platzierung geeignet sind, werden standardmäßig zuerst die Angebote mit der höchsten **Priorität** an die Kunden gesendet.

![](../../assets/offer-priority.png)

Die Prioritätswerte der Angebote werden bei der Erstellung eines Angebots zugewiesen. Näheres dazu, wie Sie ein personalisiertes Angebot erstellen, finden Sie in [diesem Abschnitt](../offer-library/creating-personalized-offers.md).

## Rangfolgenformel {#assign-ranking-formula}

Zusätzlich zur Angebotspriorität können Sie mit Journey Optimizer **Rangfolgenformeln** erstellen. Dabei handelt es sich um Formeln, die bestimmen, welches Angebot für eine bestimmte Platzierung zuerst präsentiert werden soll, anstatt die Prioritätswerte der Angebote zu berücksichtigen.

Sie können beispielsweise die Priorität aller Angebote erhöhen, deren Enddatum weniger als 24 Stunden entfernt ist, oder die Priorität von Angeboten aus der Kategorie „Laufen“ erhöhen, wenn das Interesse eines Profils „Laufen“ ist.

Näheres dazu, wie Sie eine Rangfolgenformel erstellen, finden Sie in [diesem Abschnitt](../offer-library/create-ranking-formulas.md).

Nachdem eine Rangfolgenformel erstellt wurde, können Sie sie einer Platzierung in einer Entscheidung (früher als Angebotsaktivität bezeichnet) zuweisen. Gehen Sie dazu wie folgt vor:

1. Erstellen Sie eine Entscheidung oder bearbeiten Sie eine bestehende. Siehe [Erstellen von Entscheidungen](../offer-activities/create-offer-activities.md).

1. Fügen Sie die Platzierungen hinzu, die Ihre Angebote enthalten werden. Siehe [Erstellen von Platzierungen](../offer-library/creating-placements.md).

1. Fügen Sie für jede Platzierung eine Kollektion hinzu. Siehe [Erstellen von Kollektionen](../offer-library/creating-collections.md).

1. Wählen Sie aus der Dropdown-Liste die Option, Angebote nach **[!UICONTROL Rangfolge]** zu sortieren, und klicken Sie dann auf **[!UICONTROL Rangfolge hinzufügen]**.

   ![](../../assets/offer-activity-ranking.png)

1. Wählen Sie die gewünschte Rangfolgenformel aus und klicken Sie dann auf **[!UICONTROL Auswählen]**.

   ![](../../assets/ranking-selection.png)

Die Rangfolgenformel ist nun mit der Platzierung verknüpft.

Wenn mehrere Angebote für diese Platzierung geeignet sind, verwendet die Entscheidung die Rangfolgenformel, um zu berechnen, welches Angebot zuerst bereitgestellt werden soll.

## KI-Rangfolge {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->You can also use an trained model system that automatically ranks offers to display for a given profile by selecting a ranking strategy. Learn how to create a ranking strategy in [this section](../offer-library/create-ranking-strategies.md).

>[!CAUTION]
>
>Die Verwendung der KI-Rangfolge ist derzeit nur für ausgewählte Benutzer verfügbar.

Nachdem eine Rangfolgestrategie erstellt wurde, können Sie sie einer Platzierung in einer Entscheidung (früher als Angebotsaktivität bezeichnet) zuweisen. Gehen Sie dazu wie folgt vor:

1. Erstellen Sie eine Entscheidung oder bearbeiten Sie eine bestehende. Siehe [Erstellen von Entscheidungen](../offer-activities/create-offer-activities.md).

1. Fügen Sie die Platzierungen hinzu, die Ihre Angebote enthalten werden. Siehe [Erstellen von Platzierungen](../offer-library/creating-placements.md).

1. Fügen Sie für jede Platzierung eine Kollektion hinzu. Siehe [Erstellen von Kollektionen](../offer-library/creating-collections.md).

1. Wählen Sie aus der Dropdown-Liste aus, dass Sie Angebote nach **[!UICONTROL KI-Rangfolge]** sortieren möchten.

   ![](../../assets/ranking-selection-ai-ranking.png)

1. Klicken Sie auf **[!UICONTROL Rangfolge hinzufügen]**.

   ![](../../assets/ranking-selection-ai-ranking-add.png)

1. Wählen Sie die von Ihnen erstellte Rangfolgestrategie aus. Alle Details der Rangfolgestrategie werden angezeigt.

   ![](../../assets/ranking-selection-ai-ranking-selected.png)

1. Klicken Sie auf **[!UICONTROL Auswählen]**.

Die Rangfolgestrategie ist nun mit der Platzierung verknüpft.

Wenn mehrere Angebote geeignet sind, bestimmt das System mit trainierten Modellen, welches Angebot zuerst für eine bestimmte Platzierung gezeigt werden soll.

<!--Result? Describe the impact for the user, i.e. what's the effect of selecting this ranking strategy for this collection/placement.-->

<!--Click **[!UICONTROL Next]** to confirm and save your decision.-->
