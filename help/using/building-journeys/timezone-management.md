---
solution: Journey Optimizer
product: journey optimizer
title: Zeitzonen-Management
description: Erfahren Sie mehr über das Zeitzonen-Management
feature: Journeys, Profiles
topic: Content Management
role: User
level: Intermediate
keywords: Zeitzone, Eigenschaften, Journey, Bedingung, Uhrzeit, Datum, benutzerdefiniert
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: ht
source-wordcount: '360'
ht-degree: 100%

---

# Zeitzonen-Management {#timezone_management}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_time_zone"
>title="Zeitzone"
>abstract="Wählen Sie die Zeitzone der Journey aus. Wenn Sie eine feste Zeitzone verwenden, ist diese für alle Kontakte gleich, die in die Journey eintreten."


Sie können eine Zeitzone in den [Eigenschaften](../building-journeys/journey-properties.md#timezone) Ihrer Journey festlegen.

Um die Eigenschaften der Journey aufzurufen, wählen Sie das Stiftsymbol oben rechts im Bildschirm aus.

Diese Zeitzone wird für jede Aktivität der Journey verwendet, die ein Zeitelement enthält, z. B.:

* [Bedingung für die Uhrzeit](../building-journeys/condition-activity.md#time_condition)
* [Bedingung für das Datum](../building-journeys/condition-activity.md#date_condition)
* [Benutzerdefinierte Wartezeit](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

Sie können eine [feste Zeitzone](#fixed-timezone) auswählen oder die Zeitzone verwenden, die [im Benutzerprofil definiert ist](#timezone-from-profiles).

## Definieren einer festen Zeitzone {#fixed-timezone}

Die Zeitzone kann fest definiert werden. Löschen Sie die vordefinierte Zeitzone und wählen Sie eine aus der Dropdown-Liste aus. Wenn Sie eine feste Zeitzone verwenden, ist diese für alle Kontakte gleich, die die Journey beginnen.

Wählen Sie dazu im Bereich **[!UICONTROL Journey-Eigenschaften]** eine Zeitzone aus.

![](assets/journey72.png)

## Verwenden der Zeitzone von Profilen {#timezone-from-profiles}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_profile_time_zone"
>title="Zeitzone des Profils verwenden"
>abstract="Aktivieren Sie das Kontrollkästchen, um bei Warte- und Bedingungsaktivitäten die Zeitzone des Profils in Echtzeit zu verwenden. Wenn für ein Profil eine Zeitzone definiert wurde, wird diese von der Journey abgerufen und verwendet.  Andernfalls wird die im Zeitzonenfeld definierte Zeitzone verwendet."

Wenn das Eintrittsereignis der Journey einen Namespace hat, was bedeutet, dass die Journey Zugriff auf den Echtzeit-Kundenprofil-Service von Adobe Experience Platform hat, könnten Sie die auf Profilebene definierte Zeitzone verwenden. Aktivieren Sie dazu in den **Eigenschaften** die Option **Zeitzone des Profils für Wartezeiten und Bedingungen verwenden**. Diese Option ist nicht standardmäßig aktiviert.

Wenn für ein Profil eine Zeitzone definiert wurde, wird diese von der Journey abgerufen und verwendet.  Ist dies nicht der Fall, wird die im Zeitzonenfeld definierte Zeitzone verwendet.

![](assets/journey73.png)

>[!NOTE]
>
>Die Zeitzone des Profils verwendet das Feld **timeZone** in der Feldergruppe **Voreinstellungsdetails**.

## Verwenden von Zeitzonen in Ausdrücken {#timezone-in-expressions}

Das Start- und Enddatum einer Journey kann nicht mit einer bestimmten Zeitzone verknüpft werden. Es wird automatisch mit der Zeitzone der Instanz verbunden.
