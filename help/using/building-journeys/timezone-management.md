---
title: Zeitzonenmanagement
description: Informationen zum Zeitzonenmanagement
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Zeitzonenverwaltung {#timezone_management}

![](../assets/do-not-localize/badge.png)

Sie können eine Zeitzone in den [properties](../building-journeys/journey-gs.md#change-properties) Ihrer Journey definieren.

Um Eigenschaften aufzurufen, klicken Sie auf das Stiftsymbol oben rechts im Bildschirm.

Diese Zeitzone wird für jede Aktivität der Journey verwendet, die ein Zeitelement enthält, z. B.:

* [Zeitbedingung](../building-journeys/condition-activity.md#time_condition)
* [Datumsbedingung](../building-journeys/condition-activity.md#date_condition)
* [Benutzerdefinierte Wartezeit](../building-journeys/wait-activity.md#custom)
* [Feste Datumswartung](../building-journeys/wait-activity.md#fixed_date)

Sie können eine Zeitzone auswählen oder die Zeitzone verwenden, die im Profil des Benutzers definiert ist.

## Definieren einer festen Zeitzone {#fixed-timezone}

Die Zeitzone kann auch festgelegt werden. Löschen Sie die vordefinierte Zeitzone und wählen Sie eine aus der Dropdown-Liste. Wenn Sie eine feste Zeitzone verwenden, ist diese für alle Personen gleich, die die Journey betreten.

Wählen Sie dazu in **[!UICONTROL Eigenschaften]** eine Zeitzone aus.

![](../assets/journey73.png)

## Verwenden von Profilen zum Definieren der Journey-Zeitzone {#timezone-from-profiles}

Wenn das Ereignis für die Eingabe des Journey einen Namensraum hat, d. h. die Journey den Kundendienst in Echtzeit von Adobe Experience Platform erreichen kann, ist die Zeitzone mit der im Profil des in der Journey fließenden Benutzers festgelegten Zeitzone vordefiniert.

Wenn eine Zeitzone im Adobe Experience Platform-Profil definiert ist, kann sie im Journey abgerufen werden.

Wenn das Profil des Benutzers keine Zeitzone enthält, wird die im Zeitzonenfeld definierte Zeitzone abgerufen.

Markieren Sie dazu in **[!UICONTROL Properties]** **[!UICONTROL Use Profil timezone in timers and terms]**.

![](../assets/journey72.png)

## Verwenden von Zeitzonen in Ausdrücken {#timezone-in-expressions}

Beginns- und Enddaten einer Journey können nicht mit einer bestimmten Zeitzone verknüpft werden. Sie werden automatisch der Zeitzone der Instanz zugeordnet.
