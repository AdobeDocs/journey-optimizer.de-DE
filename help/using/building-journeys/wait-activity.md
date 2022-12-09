---
solution: Journey Optimizer
product: journey optimizer
title: Warteaktivität
description: Erfahren Sie mehr über die Warteaktivität
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Warteaktivität{#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Warteaktivität"
>abstract="Wenn Sie warten möchten, bevor Sie die nächste Aktivität im Pfad ausführen, können Sie eine Warteaktivität verwenden. Damit können Sie den Zeitpunkt festlegen, zu dem die nächste Aktivität ausgeführt werden soll. Es stehen zwei Optionen zur Verfügung: Dauer und benutzerdefiniert."

Wenn Sie warten möchten, bevor Sie die nächste Aktivität im Pfad ausführen, können Sie eine **[!UICONTROL Wait]** Aktivität. Damit können Sie den Zeitpunkt festlegen, zu dem die nächste Aktivität ausgeführt werden soll. Drei Optionen stehen zur Verfügung:

* [Dauer](#duration)
* [Benutzerdefiniert](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Über die Warteaktivität{#about_wait}

Die maximale Wartezeit beträgt 30 Tage. Im Testmodus wird die **[!UICONTROL Wait time in test]** ermöglicht es Ihnen, die Dauer jeder Warteaktivität festzulegen. Die Standardzeit beträgt 10 Sekunden. Dadurch wird sichergestellt, dass Sie die Testergebnisse schnell erhalten. Siehe [diese Seite](../building-journeys/testing-the-journey.md)

Seien Sie vorsichtig bei der Verwendung mehrerer Warteaktivitäten in einer Journey, da das globale Journey-Timeout 30 Tage beträgt. Das bedeutet, dass ein Profil die Journey maximal 30 Tage nach seinem Eintritt immer verlässt.

## Wartezeit mit Dauer{#duration}

Wählen Sie die Dauer der Wartezeit bis zur Ausführung der nächsten Aktivität aus.

![](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

## Benutzerdefinierte Wartezeit{#custom}

Mit dieser Option können Sie ein benutzerdefiniertes Datum definieren, z. B. den 12. Juli 2020 um 17 Uhr, indem Sie einen erweiterten Ausdruck verwenden, der auf einem Feld basiert, das von einem Ereignis oder einer Datenquelle stammt. Sie können keine benutzerdefinierte Dauer festlegen, z. B. 7 Tage. Der Ausdruck im Ausdruckseditor sollte das Format dateTimeOnly aufweisen. Siehe hierzu [page](expression/expressionadvanced.md). Weitere Informationen zum &quot;dateTimeOnly&quot;-Format finden Sie in diesem [page](expression/data-types.md).

>[!NOTE]
>
>Sie können einen &quot;dateTimeOnly&quot;-Ausdruck verwenden oder eine Funktion verwenden, um in einen &quot;dateTimeOnly&quot;-Ausdruck zu konvertieren. Beispiel: toDateTimeOnly(@{Event.offerOpened.activity.endTime}), das Feld im Ereignis weist die Form 2016-08-12T09 auf:46:06Z.
>
>Die **Zeitzone** wird in den Eigenschaften Ihrer Journey erwartet. Aus diesem Grund ist es heute nicht möglich, von der Oberfläche direkt auf eine vollständige ISO-8601-Zeitstempelmischzeit und einen Zeitzonenversatz wie 2016-08-12T09 zu verweisen:46:06.982-05. Siehe [diese Seite](../building-journeys/timezone-management.md).

![](assets/journey57.png)

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you’ll be notified that the default time applies.

>[!NOTE]
>
>The first event of your journey must have a namespace.
>
>This capability is only available after an **[!UICONTROL Email]** activity. You need to have Adobe Campaign Standard.

1. In the **[!UICONTROL Amount of time]** field, define the number of hours to consider to optimize email sending.
1. In the **[!UICONTROL Optimization type]** field, choose if the optimization should increase clicks or opens.
1. In the **[!UICONTROL Default time]** field, define the default time to wait if the predictive send time score is not available.

    >[!NOTE]
    >
    >Note that the send time score can be unavailable because there is not enough data to perform the calculation. In this case, you will be informed, at publication time, that the default time applies.

![](assets/journey57bis.png)-->
