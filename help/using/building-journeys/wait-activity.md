---
solution: Journey Optimizer
product: journey optimizer
title: Warteaktivität
description: Erfahren Sie, wie Sie die Warteaktivität konfigurieren
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: Warten, Aktivität, Journey, weiter, Arbeitsfläche
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: 6ff54583c729175c74b3a7ea4ab9188505fde897
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 83%

---

# Warteaktivität {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Warteaktivität"
>abstract="Wenn Sie warten möchten, bevor Sie die nächste Aktivität im Pfad ausführen, können Sie eine Warteaktivität verwenden. Sie können den Zeitpunkt festlegen, zu dem die nächste Aktivität ausgeführt wird. Es stehen zwei Optionen zur Verfügung: „Dauer“ und „Benutzerdefiniert“."

Mit einer Aktivität vom Typ **[!UICONTROL Warten]** können Sie eine Dauer definieren, nach deren Ablauf die nächste Aktivität ausgeführt wird.  Die maximale Wartezeit beträgt **30 Tage**.

Sie können zwei Arten der Aktivität vom Typ **Warten** festlegen:

* Eine Wartezeit basierend auf einer relativen Dauer. [Weitere Informationen](#duration)
* Ein benutzerdefiniertes Datum, das mithilfe von Funktionen berechnet wird. [Weitere Informationen](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Empfehlungen {#wait-recommendations}

### Mehrere Warteaktivitäten {#multiple-wait-activities}

Bei Verwendung mehrerer **Warten** -Aktivitäten in einer Journey, beachten Sie, dass die [globales Journey-Timeout](journey-gs.md#global_timeout) 91 Tage beträgt, d. h. Profile werden immer 91 Tage nach ihrem Eintritt aus der Journey ausgeschlossen. Weiterführende Informationen finden Sie auf [dieser Seite](../building-journeys/journey-gs.md#global_timeout).

Eine Person kann **Warten** nur dann aktiviert werden, wenn genügend Zeit im Journey verbleibt, um die Wartezeit vor dem Journey-Timeout von 91 Tagen abzuschließen. Wenn Sie beispielsweise zwei **Warten** Aktivitäten, die auf jeweils 20 Tage festgelegt sind, erkennt das System, dass die zweite **Warten** -Aktivität endet nach Ablauf der 91 Tage. Die zweite Aktivität vom Typ **Warten** wird daher ignoriert und der Kontakt verlässt die Journey, bevor sie oder er diese beginnt. In diesem Beispiel bleibt die Kundin bzw. der Kunde insgesamt 20 Tage in der Journey.

### Warten und Wiedereintritt {#wait-re-entrance}

Eine Best Practice, um keine Aktivitäten vom Typ **Warten** zu verwenden, um den erneuten Eintritt zu blockieren. Verwenden Sie stattdessen die Option **Erneuten Eintritt erlauben** auf der Ebene der Journey-Eigenschaften. Weiterführende Informationen finden Sie auf [dieser Seite](../building-journeys/journey-gs.md#entrance).

### Warten und Testmodus {#wait-test-modd}

Im Testmodus können Sie mit dem Parameter **[!UICONTROL Wartezeit im Test]** die Dauer jeder Aktivität vom Typ **Warten** festlegen. Der Standardwert ist 10 Sekunden. Dadurch erhalten Sie die Testergebnisse schnell. Weiterführende Informationen finden Sie auf [dieser Seite](../building-journeys/testing-the-journey.md).

## Konfiguration {#wait-configuration}

### Dauer der Wartezeit {#duration}

Wählen Sie den Typ **Dauer**, um die relative Dauer der Wartezeit vor der Ausführung der nächsten Aktivität auszuwählen. Die maximale Wartezeit beträgt **29 Tage**.

![Definieren der Wartezeit](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### Benutzerdefinierte Wartezeit {#custom}

Wählen Sie den Typ **Benutzerdefiniert** aus, um ein benutzerdefiniertes Datum zu definieren. Dabei verwenden Sie einen erweiterten Ausdruck, der auf einem von einem Ereignis oder einer benutzerdefinierten Aktion stammenden Feld basiert. Sie können eine relative Dauer nicht direkt definieren, z. B. 7 Tage, aber Sie können Funktionen verwenden, um sie bei Bedarf zu berechnen (z. B. 2 Tage nach Kauf).

![Definieren einer benutzerdefinierten Wartezeit mit einem Ausdruck](assets/journey57.png)

Der Ausdruck im Editor sollte ein `dateTimeOnly`-Format aufweisen. Mehr dazu erfahren Sie auf [dieser Seite](expression/expressionadvanced.md). Weitere Informationen zum Format „TimeOnly“ finden Sie auf [dieser Seite](expression/data-types.md).

Es empfiehlt sich, benutzerdefinierte Datumsangaben zu verwenden, die spezifisch für Ihre Profile sind, und zu vermeiden, dass für alle Profile dasselbe Datum verwendet wird. Definieren Sie beispielsweise nicht `toDateTimeOnly('2024-01-01T01:11:00Z')`, sondern `toDateTimeOnly(@event{Event.productDeliveryDate})`, was für jedes Profil spezifisch ist. Beachten Sie, dass die Verwendung von festen Datumsangaben Probleme bei der Ausführung der Journey verursachen kann.


>[!NOTE]
>
>Sie können einen `dateTimeOnly`-Ausdruck nutzen oder eine Funktion zur Konvertierung in ein `dateTimeOnly`-Format verwenden.  Beispiel: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`, das Feld im Ereignis hat folgende Form: 2023-08-12T09:46:06Z.
>
>Die Angabe der **Zeitzone** ist für die Eigenschaften Ihrer Journey erforderlich. Aus diesem Grund ist es nicht möglich, von direkt der Benutzeroberfläche auf eine Zeitstempelmischzeit nach ISO-8601 und einen Zeitzonenversatz wie 2023-08-12T09:46:06.982-05 zu verweisen. [Weitere Informationen](../building-journeys/timezone-management.md).


Um zu überprüfen, ob die Warteaktivität erwartungsgemäß funktioniert, können Sie Schritt-Ereignisse verwenden. [Weitere Informationen](../reports/query-examples.md#common-queries).

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you'll be notified that the default time applies.

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
