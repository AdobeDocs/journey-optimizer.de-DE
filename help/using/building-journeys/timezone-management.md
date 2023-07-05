---
solution: Journey Optimizer
product: journey optimizer
title: Zeitzonen-Management
description: Erfahren Sie mehr über das Zeitzonen-Management
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: Zeitzone, Eigenschaften, Journey, Bedingung, Uhrzeit, Datum, benutzerdefiniert
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 100%

---

# Zeitzonen-Management {#timezone_management}

Sie können eine Zeitzone in den [Eigenschaften](../building-journeys/journey-gs.md#change-properties) Ihrer Journey festlegen.

Um die Eigenschaften der Journey aufzurufen, klicken Sie auf das Stiftsymbol oben rechts im Bildschirm.

Diese Zeitzone wird für jede Aktivität der Journey verwendet, die ein Zeitelement enthält, z. B.:

* [Bedingung für die Uhrzeit](../building-journeys/condition-activity.md#time_condition)
* [Bedingung für das Datum](../building-journeys/condition-activity.md#date_condition)
* [Benutzerdefinierte Wartezeit](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

Sie können eine Zeitzone auswählen oder die Zeitzone verwenden, die im Benutzerprofil definiert ist.

>[!NOTE]
>
>Die Zeitzone des Profils verwendet das Feld **timeZone** in der Feldergruppe **Voreinstellungsdetails**.

## Definieren einer festen Zeitzone {#fixed-timezone}

Die Zeitzone kann auch fest definiert werden. Löschen Sie die vordefinierte Zeitzone und wählen Sie eine aus der Dropdown-Liste aus. Wenn Sie eine feste Zeitzone verwenden, ist diese für alle Kontakte gleich, die die Journey beginnen.

Wählen Sie dazu im Bereich **[!UICONTROL Journey-Eigenschaften]** eine Zeitzone aus.

![](assets/journey72.png)

## Verwenden von Profilen zur Definition der Zeitzone einer Journey {#timezone-from-profiles}

Wenn das Eintrittsereignis der Journey einen Namespace hat, was bedeutet, dass die Journey Zugriff auf den Echtzeit-Kundenprofil-Service von Adobe Experience Platform hat, könnten Sie die auf Profilebene definierte Zeitzone verwenden. Aktivieren Sie dazu in den **Eigenschaften** die Option **Zeitzone des Profils für Wartezeiten und Bedingungen verwenden**. Diese Option ist nicht standardmäßig aktiviert.

Wenn für ein Profil eine Zeitzone definiert wurde, wird diese abgerufen und von der Journey verwendet. Ist dies nicht der Fall, wird die im Zeitzonenfeld definierte Zeitzone verwendet.

![](assets/journey73.png)

## Verwenden von Zeitzonen in Ausdrücken {#timezone-in-expressions}

Das Start- und Enddatum einer Journey kann nicht mit einer bestimmten Zeitzone verknüpft werden. Es wird automatisch mit der Zeitzone der Instanz verbunden.
