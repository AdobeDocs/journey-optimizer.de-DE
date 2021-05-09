---
title: Auswahl von Angeboten in Entscheidungen konfigurieren
description: Erfahren Sie, wie Sie die Auswahl von Angeboten in Entscheidungen verwalten.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# Auswahl von Angeboten in Entscheidungen konfigurieren {#offers-selection-in-activities}

## Info zu Angebote-Priorität {#about-offers-priority}

Wenn mehrere Angebot für eine bestimmte Platzierung in einer Entscheidung infrage kommen (früher als Angebot-Aktivität bezeichnet), werden die Angebot mit der höchsten **Priorität** standardmäßig zuerst an die Kunden gesendet. Die Prioritätswerte für Angebote werden beim Erstellen eines Angebots zugewiesen (siehe [Erstellen eines personalisierten Angebots](../offer-library/creating-personalized-offers.md)).

![](../assets/offer-priority.png)

Darüber hinaus können Sie mit Journey Optimizer **Ranking Formeln** erstellen. Dabei handelt es sich um Formeln, die bestimmen, welches Angebot für eine bestimmte Platzierung zuerst präsentiert werden soll, anstatt die Prioritätenwerte der Angebote zu berücksichtigen. Sie können beispielsweise die Priorität aller Angebot erhöhen, deren Enddatum in weniger als 24 Stunden liegt, oder Angebot aus der &quot;laufenden&quot;Kategorie erhöhen, wenn der Zielpunkt des Profils &quot;ausgeführt&quot;ist.

Weitere Informationen zum Erstellen einer Rangformel finden Sie in [diesem Abschnitt](../offer-library/create-ranking-formulas.md).

## Einer Platzierung {#assign-ranking-formula} eine Rangformel zuweisen

Nachdem eine Rangformel erstellt wurde, können Sie sie einer Platzierung in einer Entscheidung zuweisen. Gehen Sie dazu wie folgt vor:

* Erstellen Sie eine Entscheidung oder bearbeiten Sie eine vorhandene, und erstellen Sie dann die Platzierungen, die Ihre Angebot enthalten (siehe [Entscheidungen erstellen](../offer-activities/create-offer-activities.md)).

* Wählen Sie für jede Platzierung **[!UICONTROL Ranking]** aus der Dropdown-Liste und klicken Sie dann auf **[!UICONTROL Hinzufügen Ranking]**.

   ![](../assets/offer-activity-ranking.png)

* Wählen Sie die gewünschte Rangformel aus und klicken Sie dann auf **[!UICONTROL Wählen Sie]**.

   ![](../assets/ranking-selection.png)

Die Rangformel ist nun mit der Platzierung verknüpft. Sind mehrere Angebote für die Darstellung an dieser Stelle geeignet, wird anhand der Formel der Rangliste berechnet, welches Angebot zuerst geliefert werden soll.
