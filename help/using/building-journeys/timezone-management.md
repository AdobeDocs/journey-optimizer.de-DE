---
title: Zeitzonen-Management
description: Erfahren Sie mehr über das Zeitzonen-Management
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 76%

---

# Zeitzonen-Management {#timezone_management}

![](../assets/do-not-localize/badge.png)

Sie können eine Zeitzone in den [Eigenschaften](../building-journeys/journey-gs.md#change-properties) Ihrer Journey festlegen.

Um die Eigenschaften aufzurufen, klicken Sie auf das Stiftsymbol oben rechts im Bildschirm.

Diese Zeitzone wird für jede Aktivität der Journey verwendet, die ein Zeitelement enthält, z. B.: 

* [Bedingung für die Uhrzeit](../building-journeys/condition-activity.md#time_condition)
* [Bedingung für das Datum](../building-journeys/condition-activity.md#date_condition)
* [Benutzerdefinierte Wartezeit](../building-journeys/wait-activity.md#custom)
* [Wartezeit mit festgelegtem Datum](../building-journeys/wait-activity.md#fixed_date)

Sie können eine Zeitzone auswählen oder die Zeitzone verwenden, die im Benutzerprofil definiert ist.

## Definieren einer festen Zeitzone {#fixed-timezone}

Die Zeitzone kann auch fest definiert werden. Löschen Sie die vordefinierte Zeitzone und wählen Sie eine aus der Dropdown-Liste aus. Wenn Sie eine feste Zeitzone verwenden, ist diese für alle Kontakte gleich, die die Journey beginnen.

Wählen Sie dazu in den **[!UICONTROL Eigenschaften]** eine Zeitzone aus.

![](../assets/journey73.png)

## Verwenden von Profilen zur Definition der Zeitzone einer Journey {#timezone-from-profiles}

Wenn das Ereignis für die Eingabe des Journey einen Namensraum hat, d. h. die Journey den Kundendienst in Echtzeit von Adobe Experience Platform erreichen kann, ist die Zeitzone mit der im Profil des in der Journey fließenden Benutzers festgelegten Zeitzone vordefiniert.

Wenn eine Zeitzone im Adobe Experience Platform-Profil definiert ist, kann sie im Journey abgerufen werden.

Wenn das Profil des Kontakts keine Zeitzone enthält, wird die im Zeitzonenfeld definierte Zeitzone abgerufen.

Aktivieren Sie dazu in den **[!UICONTROL Eigenschaften]** die Option **[!UICONTROL Zeitzone des Profils in Timern und Bedingungen verwenden]**.

![](../assets/journey72.png)

## Verwenden von Zeitzonen in Ausdrücken {#timezone-in-expressions}

Das Start- und Enddatum einer Journey kann nicht mit einer bestimmten Zeitzone verknüpft werden. Es wird automatisch mit der Zeitzone der Instanz verbunden.
