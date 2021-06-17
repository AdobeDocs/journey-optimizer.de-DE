---
title: Auswahl von Angeboten in Entscheidungen konfigurieren
description: Erfahren Sie, wie Sie die Auswahl von Angeboten in Entscheidungen verwalten.
feature: Angebote
topic: Integrationen
role: User
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 95%

---

# Auswahl von Angeboten in Entscheidungen konfigurieren {#offers-selection-in-activities}

## Informationen zur Priorität von Angeboten {#about-offers-priority}

Wenn in einer Entscheidung (früher als „Angebotsaktivität“ bezeichnet) mehrere Angebote für eine bestimmte Platzierung geeignet sind, werden standardmäßig zuerst die Angebote mit der höchsten **Priorität** an die Kunden gesendet. Die Prioritätswerte für Angebote werden beim Erstellen eines Angebots zugewiesen (siehe [Erstellen eines personalisierten Angebots](../offer-library/creating-personalized-offers.md)).

![](../../assets/offer-priority.png)

Darüber hinaus können Sie mit Journey Optimizer **Rangfolgenformeln** erstellen. Dabei handelt es sich um Formeln, die bestimmen, welches Angebot für eine bestimmte Platzierung zuerst präsentiert werden soll, anstatt die Prioritätswerte der Angebote zu berücksichtigen.

Sie können beispielsweise die Priorität aller Angebote erhöhen, deren Enddatum weniger als 24 Stunden entfernt ist, oder die Priorität von Angeboten aus der Kategorie „Laufen“ erhöhen, wenn das Interesse eines Profils „Laufen“ ist.

Weiterführende Informationen zur Erstellung einer Regel für Rangfolgen finden Sie in [diesem Abschnitt](../offer-library/create-ranking-formulas.md).

## Einer Platzierung eine Rangfolgenformel zuweisen {#assign-ranking-formula}

Nachdem eine Rangfolgenformel erstellt wurde, können Sie sie einer Platzierung in einer Entscheidung zuweisen. Gehen Sie dazu wie folgt vor:

1. Erstellen Sie eine Entscheidung oder bearbeiten Sie eine vorhandene, und erstellen Sie dann die Platzierungen, die Ihre Angebote enthalten (siehe [Entscheidungen erstellen](../offer-activities/create-offer-activities.md)).

1. Wählen Sie für jede Platzierung **[!UICONTROL Ranking]** aus der Dropdownliste aus.

1. Klicken Sie auf **[!UICONTROL Ranking]** hinzufügen.

   ![](../../assets/offer-activity-ranking.png)

1. Wählen Sie die gewünschte Rangfolgenformel aus und klicken Sie dann auf **[!UICONTROL Auswählen]**.

   ![](../../assets/ranking-selection.png)

Die Rangfolgenformel ist nun mit der Platzierung verknüpft.

Wenn mehrere Angebote für diese Platzierung geeignet sind, verwendet die Entscheidung die Rangfolgenformel, um zu berechnen, welches Angebot zuerst bereitgestellt werden soll.
