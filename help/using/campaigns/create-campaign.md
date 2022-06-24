---
title: Erstellen einer Kampagne
description: Erfahren Sie, wie Sie Kampagnen in erstellen [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: b9fa6bff926eb8cee476fa53feb38ed783e048fc
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 4%

---


# Erstellen einer Kampagne {#create-campaign}

>[!NOTE]
>
>Bevor Sie eine neue Kampagne erstellen, stellen Sie sicher, dass Sie über eine Nachrichtenvorgabe und ein Adobe Experience Platform-Segment verfügen, die einsatzbereit sind. Weitere Informationen finden Sie in den folgenden Abschnitten:
>
>* [Erstellen von Nachrichtenvoreinstellungen](../configuration/message-presets.md)
>* [Erste Schritte mit Segmenten](../segment/about-segments.md)


## Kampagnen konfigurieren {#configure}

Gehen Sie zur Erstellung einer Kampagne wie folgt vor:

1. Zugriff auf **[!UICONTROL Kampagnen]** Menü und klicken Sie auf **[!UICONTROL Kampagne erstellen]**.

   ![](assets/create-campaign.png)

<!--1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign:

    * **[!UICONTROL Scheduled]**: execute the campaign immediately or on a specified date,
    * **[!UICONTROL API-triggered]**: execute the campaign using an API call. In this case, profiles to be targeted and triggers for actions need to be set via the API call.-->

1. Im **[!UICONTROL Aktionen]** wählen Sie den Kanal und die Nachrichtenoberfläche (d. h. die Nachrichtenvorgabe) aus, die zum Senden der Nachricht verwendet werden sollen.

   ![](assets/create-campaign-action.png)

1. Geben Sie einen Titel und eine Beschreibung für die Kampagne an.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

   ![](assets/create-campaign-properties.png)

1. Im **[!UICONTROL Aktionen]** konfigurieren Sie die mit der Kampagne zu sendende Nachricht:

   1. Klicken Sie auf **[!UICONTROL Inhalt bearbeiten]** und konfigurieren und entwerfen Sie Ihre Nachricht. [Erfahren Sie, wie Sie Nachrichten konfigurieren](../messages/get-started-content.md).

      Sobald Ihr Inhalt fertig ist, klicken Sie auf den Pfeil, um zum Bildschirm zur Kampagnenerstellung zurückzukehren.

      ![](assets/create-campaign-design.png)

   1. Im **[!UICONTROL Aktionsverfolgung]** geben Sie an, ob Sie verfolgen möchten, wie Ihre Empfänger auf Ihren Versand reagieren.

      Die Tracking-Ergebnisse sind nach Ausführung der Kampagne über den Kampagnenbericht verfügbar. [Weitere Informationen zu Kampagnenberichten](campaign-global-report.md)

      ![](assets/create-campaign-action-properties.png)

1. Definieren Sie die Zielgruppe. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Zielgruppe auswählen]** -Schaltfläche, um die Liste der verfügbaren Adobe Experience Platform-Segmente anzuzeigen. [Weitere Informationen zu Segmenten](../segment/about-segments.md)

   ![](assets/create-campaign-audience.png)

   <!--By default, the targeted audience for in-app messages includes all the users of the selected mobile application.-->

   Im **[!UICONTROL Identitäts-Namespace]** wählen Sie den Namespace aus, der verwendet werden soll, um die Kontakte aus dem ausgewählten Segment zu identifizieren. [Weitere Informationen zu Namespaces](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Einzelpersonen, die zu einem Segment gehören, das nicht die ausgewählte Identität (den ausgewählten Namespace) unter ihren verschiedenen Identitäten hat, werden von der Kampagne nicht als Ziel ausgewählt. <!--info vue dans section journeys, read segment-->

   <!--If you are creating a campaign to send an in-app message, you can choose how and when the message will be shown to the audience using existing mobile app triggers.-->
   <!-- where are triggers configured?-->

1. Konfigurieren Sie das Start- und Enddatum der Kampagne.

   Standardmäßig sind Kampagnen so konfiguriert, dass sie nach der manuellen Aktivierung gestartet und beendet werden, sobald die Nachricht einmal gesendet wurde.

1. Zusätzlich können Sie die Ausführungsfrequenz der in der Kampagne konfigurierten Aktion konfigurieren.

   ![](assets/create-campaign-schedule.png)

Sobald Ihre Kampagne fertig ist, können Sie sie überprüfen und veröffentlichen (siehe [Kampagne überprüfen und aktivieren](#review-activate)).

## Kampagne überprüfen und aktivieren {#review-activate}

Nachdem die Kampagne konfiguriert wurde, müssen Sie deren Parameter und Inhalt überprüfen, bevor Sie sie aktivieren. Gehen Sie dazu wie folgt vor:

1. Klicken Sie im Konfigurationsbildschirm der Kampagne auf **[!UICONTROL Aktivieren]** um eine Zusammenfassung der Kampagne anzuzeigen.

   Mithilfe der Zusammenfassung können Sie bei Bedarf Ihre Kampagne ändern und überprüfen, ob ein Parameter falsch ist oder fehlt.

   >[!IMPORTANT]
   >
   >Bei Fehlern können Sie die Kampagne nicht aktivieren. Beheben Sie die Fehler, bevor Sie fortfahren.

   ![](assets/create-campaign-alerts.png)

1. Vergewissern Sie sich, dass Ihre Kampagne korrekt konfiguriert ist, und klicken Sie dann auf **[!UICONTROL Aktivieren]**.

   ![](assets/create-campaign-review.png)

1. Die Kampagne ist jetzt aktiviert und hat die **[!UICONTROL Live]** status (oder **[!UICONTROL Geplant]**  , wenn Sie ein Startdatum angegeben haben). [Weitere Informationen zum Kampagnenstatus](get-started-with-campaigns.md#statuses)

   Die in der Kampagne konfigurierte Nachricht wird sofort oder am angegebenen Datum ausgeführt.

   >[!NOTE]
   >
   >Nach der Aktivierung einer Kampagne behält sie den Status &quot;Live&quot; auch nach der Ausführung der Nachricht bei. Um den Status zu ändern, müssen Sie ihn manuell beenden. [Erfahren Sie, wie Sie eine Kampagne stoppen](modify-stop-campaign.md)

1. Nach der Aktivierung einer Kampagne können Sie jederzeit deren Informationen überprüfen, indem Sie sie öffnen. Die Zusammenfassung ermöglicht Statistiken über die Anzahl der Zielgruppenprofile sowie der bereitgestellten und fehlgeschlagenen Aktionen.

   Sie können auch zusätzliche Statistiken in dedizierten Berichten abrufen, indem Sie auf **[!UICONTROL Berichte]** Schaltfläche. [Weitere Informationen](campaign-global-report.md)

   ![](assets/create-campaign-summary.png)

   >[!IMPORTANT]
   >
   >In Kampagnen erstellte Nachrichten sind spezifisch für [!DNL Journey Optimizer] Kampagnenfunktionen. Nach der Erstellung sind sie nur über Kampagnen verfügbar und werden nicht in der Variablen **[!UICONTROL Nachrichten]** Menü.