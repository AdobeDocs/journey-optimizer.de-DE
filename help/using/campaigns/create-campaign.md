---
title: Erstellen einer Kampagne
description: Erfahren Sie, wie Sie Kampagnen in erstellen [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6177a33edeb3b8381c3eb5609762b4d974dc93e3
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 6%

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

1. Im **[!UICONTROL Eigenschaften]** Geben Sie an, wann die Kampagne ausgeführt werden soll:

   * **[!UICONTROL Geplant]**: die Kampagne sofort oder an einem bestimmten Datum ausführen. Geplante Kampagnen zielen auf den Versand ab **Marketing** Geben Sie Meldungen ein.
   * **[!UICONTROL API-ausgelöst]**: die Kampagne mithilfe eines API-Aufrufs ausführen. API-gesteuerte Kampagnen zielen auf das Senden von **transactional** Nachrichten, d. h. Nachrichten, die aufgrund einer von einer Person durchgeführten Aktion gesendet werden: Zurücksetzen des Kennworts, Abbruch der Karte usw. [Erfahren Sie, wie Sie eine Kampagne mit APIs Trigger haben.](api-triggered-campaigns.md)

1. Im **[!UICONTROL Aktionen]** wählen Sie den Kanal und die Nachrichtenoberfläche (d. h. die Nachrichtenvorgabe) aus, die zum Senden der Nachricht verwendet werden sollen, und klicken Sie auf **[!UICONTROL Erstellen]**.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >In der Dropdown-Liste werden nur die mit dem Kampagnentyp (Marketing oder Transaktionsnachrichten) kompatiblen Oberflächen aufgelistet.

1. Geben Sie einen Titel und eine Beschreibung für die Kampagne an.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. Im **[!UICONTROL Aktionen]** konfigurieren Sie die mit der Kampagne zu sendende Nachricht:

   1. Klicken Sie auf **[!UICONTROL Inhalt bearbeiten]** und konfigurieren und entwerfen Sie Ihre Nachricht. [Erfahren Sie, wie Sie Nachrichten konfigurieren](../messages/get-started-content.md).

      Sobald Ihr Inhalt fertig ist, klicken Sie auf den Pfeil, um zum Bildschirm zur Kampagnenerstellung zurückzukehren.

      ![](assets/create-campaign-design.png)

   1. Im **[!UICONTROL Aktionsverfolgung]** geben Sie an, ob Sie verfolgen möchten, wie Ihre Empfänger auf Ihren Versand reagieren.

      Die Tracking-Ergebnisse sind nach Ausführung der Kampagne über den Kampagnenbericht verfügbar. [Weitere Informationen zu Kampagnenberichten](campaign-global-report.md)

1. Definieren Sie die Zielgruppe. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Zielgruppe auswählen]** -Schaltfläche, um die Liste der verfügbaren Adobe Experience Platform-Segmente anzuzeigen. [Weitere Informationen zu Segmenten](../segment/about-segments.md)

   >[!NOTE]
   >
   >Für API-gesteuerte Kampagnen muss die Zielgruppe über API-Aufruf festgelegt werden. [Weitere Informationen](api-triggered-campaigns.md)

   Im **[!UICONTROL Identitäts-Namespace]** wählen Sie den Namespace aus, der verwendet werden soll, um die Kontakte aus dem ausgewählten Segment zu identifizieren. [Weitere Informationen zu Namespaces](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Einzelpersonen, die zu einem Segment gehören, das nicht die ausgewählte Identität (den ausgewählten Namespace) unter ihren verschiedenen Identitäten hat, werden von der Kampagne nicht als Ziel ausgewählt.

1. Konfigurieren Sie das Start- und Enddatum der Kampagne. Standardmäßig sind Kampagnen so konfiguriert, dass sie nach der manuellen Aktivierung gestartet und beendet werden, sobald die Nachricht einmal gesendet wurde.

1. Darüber hinaus können Sie die Ausführungsfrequenz der in der Kampagne konfigurierten Aktion festlegen.

   >[!NOTE]
   >
   >Für API-gesteuerte Kampagnen ist die Planung zu einem bestimmten Datum und zu einer bestimmten Uhrzeit mit Wiederholung nicht verfügbar, da die Aktion über die API ausgelöst wird. Das Start- und Enddatum sind jedoch relevant, um sicherzustellen, dass, wenn vor dem Fenster ein API-Aufruf erfolgt, diese fehlerhaft werden.

   ![](assets/create-campaign-schedule.png)

1. Wenn Sie eine API-gesteuerte Kampagne erstellen, wird die **[!UICONTROL cURL-Anfrage]** -Abschnitt ermöglicht Ihnen, die **[!UICONTROL Kampagnen-ID]** , um im API-Aufruf zu verwenden. [Weitere Informationen](api-triggered-campaigns.md)

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

## Weitere Ressourcen

* [Erste Schritte mit Kampagnen](get-started-with-campaigns.md)
* [API-gesteuerte Kampagnen erstellen](api-triggered-campaigns.md)
* [Ändern oder Stoppen einer Kampagne](modify-stop-campaign.md)
* [Live-Bericht einer Kampagne](campaign-live-report.md)
* [Globaler Kampagnenbericht](campaign-global-report.md)
