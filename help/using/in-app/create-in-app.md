---
title: Erstellen einer In-App-Benachrichtigung
description: Erfahren Sie, wie Sie in Journey Optimizer eine In-App-Nachricht erstellen.
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: In-App, Nachricht, Erstellung, Starten
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: c70b782b077b57485e7a40ec9f159832604f76e5
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 63%

---

# Erstellen einer In-App-Nachricht {#create-in-app}

Gehen Sie wie folgt vor, um eine neue In-App-Nachricht zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Kampagnen]** auf und klicken Sie auf **[!UICONTROL Kampagne erstellen]**.

1. Geben Sie im Abschnitt **[!UICONTROL Eigenschaften]** an, wann Sie die Kampagne ausführen möchten.

1. Wählen Sie im Bereich **[!UICONTROL Aktionen]** die **[!UICONTROL In-App-Nachricht]** und die **[!UICONTROL Programmoberfläche]** aus, die Sie zuvor für Ihre In-App-Nachricht konfiguriert haben. Klicken Sie dann auf **[!UICONTROL Erstellen]**.

   [Weitere Informationen zur In-App-Konfiguration](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. Bearbeiten Sie im Bereich **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** Ihrer Kampagne.

1. Um der In-App-Nachricht benutzerdefinierte oder Core-Datennutzungsbezeichnungen zuzuweisen, wählen Sie **[!UICONTROL Zugriff verwalten]**. [Weitere Informationen](../administration/object-based-access.md).

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Audience auswählen]**, um die Audience aus der Liste der verfügbaren Adobe Experience Platform-Segmente zu definieren. [Weitere Informationen](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. Wählen Sie im Feld **[!UICONTROL Identity-Namespace]** den Namespace aus, der zur Identifizierung der Personen im ausgewählten Segment verwendet werden soll. [Weitere Informationen](../event/about-creating.md#select-the-namespace).

1. Klicken **[!UICONTROL Trigger bearbeiten]** um die Ereignisse und Kriterien auszuwählen, die für den Trigger Ihrer Nachricht gelten:

   1. Klicken **[!UICONTROL Hinzufügen] Bedingung** , wenn Sie möchten, dass der Trigger mehrere Ereignisse oder Kriterien berücksichtigt.
   1. Wählen Sie die Art der Verknüpfung Ihrer Ereignisse aus, z. B. **[!UICONTROL Und]**, wenn Sie möchten, dass **beide** Auslöser erfüllt sind, damit eine Nachricht angezeigt wird. Wählen Sie stattdessen **[!UICONTROL Oder]**, wenn Sie möchten, dass die Nachricht angezeigt, dass **einer** der Auslöser erfüllt ist.
   1. Klicken **[!UICONTROL Gruppe erstellen]** um Trigger zusammenzufassen.

   ![](assets/in_app_create_3.png)

1. Wählen Sie die Häufigkeit Ihres Auslösers aus, wenn Ihre In-App-Nachricht aktiv ist:

   * **[!UICONTROL alwaysTime]**: Zeigt immer die Nachricht an, wenn die Ereignisse im **[!UICONTROL App-Trigger]** angezeigt.
   * **[!UICONTROL Einmal]**: Zeigen Sie diese Nachricht nur zum ersten Mal an, wenn die in der **[!UICONTROL App-Trigger]** angezeigt.
   * **[!UICONTROL Bis zum Clickthrough]**: Diese Meldung anzeigen, wenn die Ereignisse im **[!UICONTROL App-Trigger]** Dropdown-Liste wird angezeigt, bis das SDK ein Interaktionsereignis mit der Aktion &quot;angeklickt&quot;sendet.
   * **[!UICONTROL X Häufigkeit]**: Zeigen Sie diese Meldung X Mal an.

1. Wählen Sie bei Bedarf aus, **[!UICONTROL Wochentag]** oder **[!UICONTROL Tageszeit]** wird die In-App-Nachricht angezeigt.

1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie in [diesem Abschnitt](../campaigns/create-campaign.md#schedule), wie Sie den **[!UICONTROL Zeitplan]** der Kampagne konfigurieren können.

   ![](assets/in-app-schedule.png)

1. Sie können jetzt über die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** mit der Erstellung Ihrer Inhalte beginnen. [Weitere Informationen](design-in-app.md)

   ![](assets/in_app_create_4.png)


## Anleitungsvideo{#video}

Das folgende Video zeigt, wie Sie In-App-Nachrichten in Ihren Kampagnen erstellen, konfigurieren und veröffentlichen können.

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**Verwandte Themen:**

* [Entwerfen der In-App-Nachricht](design-in-app.md)
* [In-App-Nachricht testen und senden](send-in-app.md)
* [In-App-Bericht](../reports/campaign-global-report.md#inapp-report)
* [In-App-Konfiguration](inapp-configuration.md)