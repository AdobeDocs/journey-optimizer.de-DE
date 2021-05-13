---
title: Auswahl von Angeboten in Entscheidungen konfigurieren
description: Erfahren Sie, wie Sie die Auswahl von Angeboten in Entscheidungen verwalten.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 52%

---

# Auswahl von Angeboten in Entscheidungen konfigurieren {#offers-selection-in-activities}

## Informationen zur Priorität von Angeboten {#about-offers-priority}

Wenn mehrere Angebot für eine bestimmte Platzierung in einer Entscheidung infrage kommen (früher als Angebot-Aktivität bezeichnet), werden die Angebot mit der höchsten **Priorität** standardmäßig zuerst an die Kunden gesendet. Die Prioritätswerte für Angebote werden beim Erstellen eines Angebots zugewiesen (siehe [Erstellen eines personalisierten Angebots](../offer-library/creating-personalized-offers.md)).

![](../../assets/offer-priority.png)

Darüber hinaus können Sie mit Journey Optimizer **Ranking Formeln** erstellen. Dabei handelt es sich um Formeln, die bestimmen, welches Angebot für eine bestimmte Platzierung zuerst präsentiert werden soll, anstatt die Prioritätswerte der Angebote zu berücksichtigen. Sie können beispielsweise die Priorität aller Angebote erhöhen, deren Enddatum weniger als 24 Stunden entfernt ist, oder die Priorität von Angeboten aus der Kategorie „Laufen“ erhöhen, wenn das Interesse eines Profils „Laufen“ ist.

Weiterführende Informationen zur Erstellung einer Regel für Rangfolgen finden Sie in [diesem Abschnitt](../offer-library/create-ranking-formulas.md).

## Einer Platzierung eine Rangfolgenformel zuweisen {#assign-ranking-formula}

Nachdem eine Rangformel erstellt wurde, können Sie sie einer Platzierung in einer Entscheidung zuweisen. Gehen Sie dazu wie folgt vor:

* Erstellen Sie eine Entscheidung oder bearbeiten Sie eine vorhandene, und erstellen Sie dann die Platzierungen, die Ihre Angebot enthalten (siehe [Entscheidungen erstellen](../offer-activities/create-offer-activities.md)).

* Wählen Sie für jede Platzierung **[!UICONTROL Rangliste]** aus der Dropdown-Liste und klicken Sie dann auf **[!UICONTROL Rangliste hinzufügen]**.

   ![](../../assets/offer-activity-ranking.png)

* Wählen Sie die gewünschte Rangfolgenformel aus und klicken Sie dann auf **[!UICONTROL Auswählen]**.

   ![](../../assets/ranking-selection.png)

Die Rangfolgenformel ist nun mit der Platzierung verknüpft. Sind mehrere Angebote für die Darstellung an dieser Stelle geeignet, wird anhand der Formel der Rangliste berechnet, welches Angebot zuerst geliefert werden soll.
