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
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/PdwGEuWqJcncbkokE0eOhMaEk9L0AmCJ--VZBxxtDDU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44feid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 378
ht-degree: 78%

---

# Zeitzonen-Management {#timezone_management}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_time_zone"
>title="Journey-Zeitzone"
>abstract="Wählen Sie die Zeitzone der Journey aus. Wenn Sie eine feste Zeitzone verwenden, ist diese für alle Kontakte gleich, die in die Journey eintreten."


Sie können eine Zeitzone in den [Eigenschaften](../building-journeys/journey-properties.md#timezone) Ihrer Journey festlegen.

Um die Eigenschaften der Journey aufzurufen, wählen Sie das Stiftsymbol oben rechts im Bildschirm aus.

Diese Zeitzone wird für jede Aktivität der Journey verwendet, die ein Zeitelement enthält, z. B.:

* [Zeitbedingung](../building-journeys/conditions.md#time_condition)
* [Bedingung für das Datum](../building-journeys/conditions.md#date_condition)
* [Benutzerdefinierte Wartezeit](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

Sie können eine [feste Zeitzone](#fixed-timezone) auswählen oder die Zeitzone verwenden, die [im Benutzerprofil definiert ist](#timezone-from-profiles).

## Definieren einer festen Zeitzone {#fixed-timezone}

Die Zeitzone kann fest definiert werden. Löschen Sie die vordefinierte Zeitzone und wählen Sie eine aus der Dropdown-Liste aus. Wenn Sie eine feste Zeitzone verwenden, ist diese für alle Kontakte gleich, die die Journey beginnen.

Wählen Sie dazu im Bereich **[!UICONTROL Journey-Eigenschaften]** eine Zeitzone aus.

![Dropdown-Liste zur Zeitzonenauswahl in Journey-Eigenschaften](assets/journey72.png)

## Zeitzone des Profils verwenden {#timezone-from-profiles}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_profile_time_zone"
>title="Zeitzone des Profils verwenden"
>abstract="Aktivieren Sie diese Option, um bei den Aktivitäten **Warten** und **Bedingung** die Zeitzone des Echtzeitprofils zu verwenden. Wenn für ein Profil eine Zeitzone definiert wurde, wird diese abgerufen und in der Journey verwendet. Andernfalls wird die im Zeitzonenfeld definierte Zeitzone verwendet."

Wenn das Eintrittsereignis der Journey über einen Namespace verfügt, d. h. die Journey den Echtzeit-Kundenprofil-Service von [!DNL Adobe Experience Platform] erreichen kann, empfiehlt es sich, die auf Profilebene definierte Zeitzone zu verwenden. Aktivieren Sie dazu in den **Eigenschaften** die Option **Zeitzone des Profils für Wartezeiten und Bedingungen verwenden**. Diese Option ist nicht standardmäßig aktiviert.

Wenn für ein Profil eine Zeitzone definiert wurde, wird diese abgerufen und von der Journey verwendet. Ist dies nicht der Fall, wird die im Zeitzonenfeld definierte Zeitzone verwendet.

![Konfiguration der Zeitzone des Profils in Datenquellen für personalisierte Zeitplanung](assets/journey73.png)

>[!NOTE]
>
>Die Zeitzone des Profils verwendet das Feld **timeZone** in der Feldergruppe **Voreinstellungsdetails**.

## Verwenden von Zeitzonen in Ausdrücken {#timezone-in-expressions}

Das Start- und Enddatum einer Journey kann nicht mit einer bestimmten Zeitzone verknüpft werden. Es wird automatisch mit der Zeitzone der Instanz verbunden.
