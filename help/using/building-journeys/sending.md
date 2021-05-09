---
title: Ausführung von Beginn Journey
description: Erfahren Sie, wie Sie Ihren Journey Beginn erstellen und Nachrichten senden
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---


# Journey-Ausführung {#message-execution}

![](../assets/do-not-localize/badge.png)

## Journey testen

Sie können Ihre Journey mit Test-Profilen testen. Dieser Schritt wird zur Überprüfung Ihrer Einstellungen und Meldungen empfohlen.

Weitere Informationen finden Sie in diesem [Abschnitt](testing-the-journey.md).

## Journey aktivieren

Sie müssen Ihre Journey veröffentlichen, um sie zu aktivieren.

![](../assets/jo-journeyuc2_32bis.png)

Weitere Informationen finden Sie in diesem [Abschnitt](publishing-the-journey.md).


Nach der Veröffentlichung können Sie Ihre Journey mit den dedizierten Berichte-Tools überwachen, um die Effektivität Ihrer Journey zu messen.

![](../assets/jo-dynamic_report_journey_12.png)

[Weitere Informationen zu Berichten](../reports/live-report.md)

## Nachrichten senden {#send-messages}

Wenn Ihre Nachricht einen Inhalt definiert hat und veröffentlicht wird, kann sie über eine [Journey](journey.md) gesendet werden.

>[!NOTE]
>
>Sie können einer Journey eine Meldung hinzufügen, die sich noch im Entwurfsmodus befindet, stellen Sie jedoch sicher, dass die Nachricht veröffentlicht wird, bevor Sie die Journey veröffentlichen.

Nachdem eine Nachricht gesendet wurde, können Sie die Ausführung über mehrere Indikatoren überwachen. [Erfahren Sie mehr über die Ausführung](../message-monitoring.md) von Überwachungsmeldungen.

## Terminplanmeldungen {#schedule-messages}

Nachrichten können über die Aktivität **[!UICONTROL Segment lesen]** in einer [Journey](journey.md) geplant werden. Sie können festlegen, wann das Segment in die Journey eintritt. [Erfahren Sie mehr über die Aktivität](read-segment.md) zum Lesen von Segmenten.

Gehen Sie dazu wie folgt vor:

1. Bearbeiten Sie eine Journey, ziehen Sie eine **[!UICONTROL Read segment]**-Aktivität und legen Sie sie durch einen Beginn fest. [Erfahren Sie mehr über die Konfiguration der Aktivität](read-segment.md#configuring-segment-trigger-activity) zum Lesen von Segmenten.

1. Klicken Sie auf den Link **[!UICONTROL Journey-Plan bearbeiten]**, um auf die Journey-Eigenschaften zuzugreifen.

   ![](../assets/message-read-segment-schedule.png)

1. Konfigurieren Sie das Feld **[!UICONTROL Planung type]**: Wählen Sie den gewünschten Wert aus der Liste aus, damit das Segment an einem bestimmten Datum/zu einer bestimmten Uhrzeit oder wiederholt in die Journey aufgenommen wird.

   >[!NOTE]
   >
   >Der Abschnitt **[!UICONTROL Plan]** ist nur verfügbar, wenn eine **[!UICONTROL Aktivität zum Lesen]** auf der Arbeitsfläche abgelegt wurde.

   ![](../assets/message-read-segment-scheduler.png)

1. Wenn Sie **[!UICONTROL Once]** auswählen, definieren Sie ein bestimmtes Datum und eine Uhrzeit, zu der das Segment in die Journey eintritt.

   ![](../assets/message-read-segment-scheduler-once.png)

1. Wenn Sie eine wiederkehrende Methode auswählen, bearbeiten Sie Datum und Uhrzeit des Beginns. Sie können auch ein optionales Enddatum und eine optionale Endzeit definieren.

   ![](../assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >Standardmäßig treten Segmente **[!UICONTROL so bald wie möglich]** in die Journey ein, d. h. eine Stunde nach der Veröffentlichung der Journey.

1. Klicken Sie auf **[!UICONTROL OK]**, um Ihre Änderungen zu speichern.

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
