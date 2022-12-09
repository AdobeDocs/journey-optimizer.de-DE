---
solution: Journey Optimizer
product: journey optimizer
title: Journey-Ende
description: Erfahren Sie, wie eine Journey mit Journey Optimizer endet.
feature: Journeys
role: User
level: Beginner
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# Beenden einer Journey{#journey-ending}

Eine Journey kann für eine Person in zwei bestimmten Kontexten enden:

* Die Person kommt bei der letzten Aktivität eines Pfads an.
* Die Person kommt bei einem **Bedingung** -Aktivität (oder **Warten** -Aktivität mit einer Bedingung) und entspricht keiner der Bedingungen.

Die Person kann dann erneut in die Journey eintreten, wenn der erneute Eintritt erlaubt ist. Siehe [diese Seite](../building-journeys/journey-gs.md#change-properties)

Um eine Live-Journey zu beenden, empfehlen wir, sie zu schließen. Der Eintritt neuer Kunden in die Journey wird dann blockiert. Kunden, die bereits an der Journey teilgenommen haben, können diese bis zum Ende erleben. Siehe [diesem Abschnitt](../building-journeys/journey.md#close-journey)

Sie können eine Journey nur stoppen, wenn ein Notfall aufgetreten ist und die gesamte Verarbeitung sofort auf einer Journey beendet werden muss. Personen, die bereits in eine Journey eingestiegen sind, werden in ihrem Fortschritt gestoppt. Siehe [diesem Abschnitt](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>Beachten Sie, dass Sie eine geschlossene oder gestoppte Journey nicht fortsetzen können.

## Journey-End-Tag{#end-tag}

Beim Erstellen einer Journey wird am Ende jedes Pfads ein &quot;end-Tag&quot;angezeigt. Dieser Knoten kann nicht von einem Benutzer hinzugefügt werden, kann nicht entfernt werden und nur die Bezeichnung kann geändert werden. Er markiert das Ende jedes Pfads der Journey. Wenn die Journey mehrere Pfade aufweist, empfehlen wir, jedem Ende eine Bezeichnung hinzuzufügen, damit Berichte leichter lesbar sind. Siehe [diese Seite](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## Schließen einer Journey{#close-journey}

Eine Journey kann aus folgenden Gründen geschlossen werden:

* Die Journey wird manuell über die **[!UICONTROL Close to new entrances]** Schaltfläche.
* Eine auf einem Segment basierende Journey, die die Ausführung abgeschlossen hat.
* Nach dem letzten Vorkommen einer auf wiederkehrenden Segmenten basierenden Journey.

Durch das manuelle Schließen einer Journey stellen Sie sicher, dass Kunden, die bereits in die Journey eingestiegen sind, ihren Pfad beenden können, neue Benutzer jedoch nicht in die Journey eintreten können. Wenn eine Journey geschlossen wird (aus einem der oben genannten Gründe), erhält sie den Status **[!UICONTROL Closed]**. Die Journey ermöglicht es neuen Personen nicht mehr, in die Journey einzutreten. Personen, die sich bereits in der Journey befinden, können die Journey normal beenden. Nach der standardmäßigen globalen Zeitüberschreitung von 30 Tagen wechselt die Journey zur **Abgeschlossen** Status. Siehe dies [Abschnitt](../building-journeys/journey-gs.md#global_timeout).

Eine geschlossene Journey-Version kann nicht neu gestartet oder gelöscht werden. Sie können eine neue Version davon erstellen oder sie duplizieren. Nur beendete Journeys können gelöscht werden.

Um eine Journey aus der Liste der Journeys zu schließen, klicken Sie auf die **[!UICONTROL Ellipsis]** Schaltfläche rechts neben dem Journey-Namen und wählen Sie **[!UICONTROL Close to new entrances]**.

![](assets/journey-finish-quick-action.png)

Sie können auch:

1. Im **[!UICONTROL Journeys]** auflisten, klicken Sie auf die Journey, die Sie schließen möchten.
1. Klicken Sie oben rechts auf den Abwärtspfeil.

   ![](assets/finish_drop_down_list.png)

1. Klicken **[!UICONTROL Close to new entrances]** und bestätigen Sie im Dialogfeld.

## Eine Journey stoppen{#stop-journey}

Wenn Sie den Fortschritt aller Kontakte in der Journey stoppen müssen, können Sie sie stoppen. Beim Anhalten der Journey werden alle Kontakte in der Journey mit einer Zeitüberschreitung beendet. Das Anhalten einer Journey bedeutet jedoch, dass alle Personen, die bereits in eine Journey eingestiegen sind, in ihrem Fortschritt angehalten werden. Die Journey ist im Grunde ausgeschaltet. Wenn Sie eine Journey beenden möchten, empfehlen wir Ihnen, sie zu schließen.

Eine gestoppte Journey-Version kann nicht neu gestartet werden.

Bei Anhalten wird der Journey-Status auf **[!UICONTROL Stopped]**.

Sie können eine Journey stoppen, wenn beispielsweise ein Marketing-Experte erkennt, dass die Journey auf die falsche Audience ausgerichtet ist, oder wenn eine benutzerdefinierte Aktion, mit der Nachrichten gesendet werden sollen, nicht ordnungsgemäß funktioniert. Um eine Journey aus der Liste der Journeys zu stoppen, klicken Sie auf die **[!UICONTROL Ellipsis]** Schaltfläche rechts neben dem Journey-Namen und wählen Sie **[!UICONTROL Stop]**.

![](assets/journey-finish-quick-action.png)

Sie können auch:

1. Im **[!UICONTROL Journeys]** auflisten, klicken Sie auf die Journey, die Sie stoppen möchten.
1. Klicken Sie oben rechts auf den Abwärtspfeil.
   ![](assets/finish_drop_down_list.png)
1. Klicken **[!UICONTROL Stop]** und bestätigen Sie im Dialogfeld.
