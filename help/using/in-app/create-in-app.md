---
title: Erstellen einer In-App-Benachrichtigung
description: Erfahren Sie, wie Sie in Journey Optimizer eine In-App-Nachricht erstellen.
feature: Overview
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
keywords: In-App, Nachricht, Erstellung, Starten
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 74%

---

# Erstellen einer In-App-Nachricht {#create-in-app}

>[!AVAILABILITY]
>
>Die In-App-Funktion ist derzeit nur als Beta-Version für ausgewählte Benutzerinnen und Benutzer verfügbar. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.

## Erstellen einer Kampagne und einer In-App-Nachricht{#create-in-app-in-a-campaign}

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

1. Sie können jetzt über die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** mit der Erstellung Ihrer Inhalte beginnen.

   ![](assets/in_app_create_4.png)

## Senden Ihrer In-App-Nachrichten{#in-app-send}

### Vorschau auf Gerät {#preview-device}

Sie können eine Vorschau der In-App-Benachrichtigung auf einem bestimmten Gerät anzeigen.

1. Klicken Sie auf **[!UICONTROL Vorschau auf Gerät]**.

   ![](assets/in_app_create_6.png)

1. Klicken Sie im Fenster **[!UICONTROL Mit Gerät verbinden]** auf **[!UICONTROL Start]**.

1. Geben Sie die **[!UICONTROL Basis-URL]** Ihrer Anwendung ein und klicken Sie auf **[!UICONTROL Weiter]**.

   ![](assets/in_app_create_7.png)

1. Scannen Sie den QR-Code mit Ihrem Gerät und geben Sie den angezeigten PIN-Code ein.

Ihre In-App-Nachricht kann jetzt direkt auf Ihrem Gerät ausgelöst werden, sodass Sie Ihre Nachricht auf einem Gerät in der Vorschau anzeigen und überprüfen können.

### Überprüfen und Aktivieren Ihrer In-App-Benachrichtigung{#in-app-review}

Nachdem Sie Ihre In-App-Nachricht erstellt und deren Inhalt definiert und personalisiert haben, können Sie sie überprüfen und aktivieren.

Gehen Sie dazu wie folgt vor:

1. Verwenden Sie die Schaltfläche **[!UICONTROL Zum Aktivieren überprüfen]**, um eine Zusammenfassung Ihrer Nachricht anzuzeigen.

   In der Zusammenfassung können Sie die Kampagne bei Bedarf ändern und überprüfen, ob ein Parameter falsch ist oder fehlt.

   ![](assets/in_app_create_5.png)

1. Vergewissern Sie sich, dass Ihre Kampagne korrekt konfiguriert ist, und klicken Sie dann auf **[!UICONTROL Aktivieren]**.

Ihre Kampagne ist jetzt aktiviert. Die in der Kampagne konfigurierte In-App-Benachrichtigung wird sofort oder zum angegebenen Datum versendet.

Nach dem Versand können Sie die Wirkung Ihrer In-App-Nachrichten in den Kampagnen- oder Journey-Berichten messen. Weiterführende Informationen zum Reporting finden Sie in [diesem Abschnitt](../reports/campaign-global-report.md#inapp-report).

**Verwandte Themen:**

* [Entwerfen der In-App-Nachricht](design-in-app.md)
* [In-App-Bericht](../reports/campaign-global-report.md#inapp-report)
* [In-App-Konfiguration](inapp-configuration.md)

## Anleitungsvideo{#video}

Das folgende Video zeigt, wie Sie In-App-Nachrichten in Ihren Kampagnen erstellen, konfigurieren und veröffentlichen können.

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)
