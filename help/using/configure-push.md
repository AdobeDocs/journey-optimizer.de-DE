---
title: Push-Benachrichtigung konfigurieren
description: Erfahren Sie, wie Sie eine Push-Benachrichtigung in Journey Optimizer erstellen
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 11%

---

# Push-Benachrichtigung {#create-push-notification} konfigurieren

![](assets/do-not-localize/badge.png)

Push-Benachrichtigungen werden beim Erstellen einer Nachricht auf der Registerkarte **[!UICONTROL Push Notification]** konfiguriert (siehe [Eine Nachricht erstellen](create-message.md)).

Sie können Inhalte von Push-Benachrichtigungen für iOS- oder Android-Betriebssysteme mithilfe der dedizierten Registerkarten konfigurieren.

![](assets/create-content-push.png)

## Titel und Einrichtung

Um eine Nachricht zu erstellen, klicken Sie auf die Felder **[!UICONTROL Titel]** und **[!UICONTROL Körper]**. Mit dem Ausdruck-Editor können Sie Inhalts- und Personalisierungsdaten definieren.

Weiterführende Informationen zur Personalisierung finden Sie in [diesem Abschnitt](personalization/personalize.md).

Verwenden Sie den zentralen Abschnitt, um zu veranschaulichen, wie die Push-Benachrichtigung in iOS- und Android-Terminals angezeigt wird.

>[!NOTE]
>
>Der Abschnitt **[!UICONTROL Nachricht erstellen]** ist sowohl auf den Registerkarten **[!UICONTROL iOS]** als auch **[!UICONTROL Android]** verfügbar. Jede Änderung in diesem Abschnitt gilt für beide Betriebssysteme.

## Klickverhalten {#on-click-behavior}

Wählen Sie das Verhalten aus, wenn ein Empfänger auf den Text der Push-Benachrichtigung klickt:

* Verwenden Sie die Option **[!UICONTROL App öffnen]**, um die mit der Meldung **[!UICONTROL Vorgabe]** verknüpfte Anwendung zu öffnen.
* Verwenden Sie die Option **[!UICONTROL Deeplink]**, um den Empfänger zu einem bestimmten Inhalt innerhalb der Anwendung umzuleiten. Geben Sie den Deeplink in das entsprechende Feld ein.
* Verwenden Sie die Option **[!UICONTROL Web-URL]**, um den Empfänger zu einer externen URL umzuleiten. Geben Sie die URL in das entsprechende Feld ein.

## Eine Benachrichtigung senden

Eine automatische Push-Benachrichtigung (oder Hintergrundbenachrichtigung) ist eine versteckte Anweisung, die an die Anwendung gesendet wird. Es wird beispielsweise verwendet, um Ihre Anwendung über die Verfügbarkeit neuer Inhalte zu informieren oder einen Download im Hintergrund zu starten.

Wählen Sie die Option **[!UICONTROL Silent Notification]**, um die Anwendung unbeaufsichtigt zu benachrichtigen: in diesem Fall wird die Anmeldung direkt auf den Antrag übertragen. Auf dem Gerätebildschirm wird keine Warnung angezeigt.

Verwenden Sie den Abschnitt **[!UICONTROL Benutzerspezifische Daten]**, um Schlüssel/Wert-Paare hinzuzufügen.

## Erweiterte Optionen

Konfigurieren Sie die erweiterten Optionen **[!UICONTROL a1/>.]** Verfügbare Parameter sind:

| Parameter | Verfügbarkeit | Beschreibung |
|---------|----------|---------|
| **[!UICONTROL Reduzierbar]** | iOS/Android | Eine ausblendbare Meldung ist eine Meldung, die durch eine neue ersetzt werden kann. Beispielsweise eine Anwendung, die Benutzer mit den neuesten Nachrichten zu einem Thema aktualisiert. In diesem Fall ist nur die letzte Meldung relevant. Bei nicht ausblendbaren Nachrichten ist jede Nachricht hingegen wichtig für die Client-App und muss ausgeliefert werden. |
| **[!UICONTROL Benutzerdefinierter Sound]** | iOS/Android | Der Klang, der vom Mobilterminal beim Empfang der Benachrichtigung wiedergegeben wird. Der Sound muss in der App gebündelt werden. |
| **[!UICONTROL Abzeichen]** | iOS/Android | Mit einem Badge wird die Anzahl der neuen ungelesenen Nachrichten direkt auf dem App-Symbol angezeigt. <br/>Der Badge-Wert verschwindet, sobald der Benutzer den neuen Inhalt in der Anwendung öffnet oder liest. Wenn eine Benachrichtigung auf einem Gerät empfangen wird, kann der Badge-Wert für die entsprechende App aktualisiert oder hinzugefügt werden.<br/>Wenn Sie z. B. die Anzahl der ungelesenen Artikel Ihrer Kunden speichern, können Sie die Personalisierung nutzen, um den eindeutigen Wert für das Zeichen für ungelesene Artikel für jeden Kunden zu senden. Weitere Informationen zur Personalisierung finden Sie in [diesem Abschnitt](personalization/personalize.md). |
| **[!UICONTROL Benachrichtigungsgruppe]** / | iOS | Verknüpfen Sie eine Benachrichtigungsgruppe mit der Push-Benachrichtigung.<br/>Ab iOS 12 können Sie mit Benachrichtigungsgruppen Nachrichten- und Benachrichtigungsthemen in Thread-IDs konsolidieren. Eine Marke kann beispielsweise Marketingbenachrichtigungen unter einer Gruppen-ID senden und gleichzeitig mehr Typbenachrichtigungen unter einer oder mehreren verschiedenen IDs verwalten.<br/>Um dies zu veranschaulichen, können Sie eine groupID haben: 123 &quot;Check out the new spring collection of sweaters&quot; and groupID: 456 Benachrichtigungsgruppen &quot;Ihr Paket wurde bereitgestellt&quot;. In diesem Beispiel würden alle Versand-Benachrichtigungen unter der Gruppen-ID gebündelt: 456. |
| **[!UICONTROL Benachrichtigungs-Kanal]** | Android | Verknüpfen Sie einen Benachrichtigungs-Kanal mit der Push-Benachrichtigung.<br/>Ab Android 8.0 (API-Stufe 26) müssen alle Benachrichtigungen einem Kanal zugewiesen werden, damit sie angezeigt werden. Weitere Informationen finden Sie in der [Android-Entwicklerdokumentation](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Kennzeichen Hinzufügen Verfügbarkeit von Inhalten]** | iOS | Sendet das Flag &quot;Inhalt verfügbar&quot;in der Push-Nutzlast, um sicherzustellen, dass die App nach Eingang der Push-Benachrichtigung aktiviert wird, d. h., die App kann auf die Nutzlastdaten zugreifen.<br/> Dies funktioniert auch, wenn die App im Hintergrund ausgeführt wird und keine Benutzerinteraktion erforderlich ist (z. B. Tippen auf die Push-Benachrichtigung). Dies gilt jedoch nicht, wenn die App nicht ausgeführt wird. Weitere Informationen finden Sie in der [Apple-Entwicklerdokumentation](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Flag für Hinzufügen veränderbaren Inhalt]** | iOS | Sendet das Flag für veränderbare Inhalte in der Push-Nutzlast und ermöglicht die Änderung des Inhalts der Push-Benachrichtigung durch eine im iOS-SDK bereitgestellte Anwendungserweiterung des Benachrichtigungsdiensts. Weitere Informationen finden Sie in der [Apple-Entwicklerdokumentation](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Sie können dann Ihre mobilen App-Erweiterungen nutzen, um den Inhalt oder die Darstellung ankommender Push-Benachrichtigungen, die von gesendet werden, weiter zu ändern.  [!DNL Journey Optimizer] Beispielsweise können Benutzer diese Option nutzen, um Daten zu entschlüsseln, den Text oder Titeltext einer Benachrichtigung zu ändern, eine Thread-ID zu einer Benachrichtigung hinzuzufügen usw. |
| **[!UICONTROL Benachrichtigungsebene]** | Android | Definiert die Sichtbarkeit der Push-Benachrichtigung. <b></b> privatewill die Benachrichtigung auf allen Schlossbildschirmen anzeigen, aber vertrauliche oder private Informationen auf sicheren Schrankbildschirmen verbergen. <b>In </b> Publicwill wird die Benachrichtigung in ihrer Gesamtheit auf allen Schrankbildschirmen angezeigt. <b>Das </b> Sekretariat gibt keinen Teil der Notifizierung auf einem sicheren Schließfach preis. Weitere Informationen finden Sie in der [Android-Entwicklerdokumentation](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Benachrichtigungspriorität]** | Android | Definiert die Wichtigkeit der Push-Benachrichtigung von &quot;Niedrig&quot;bis &quot;Maximal&quot;. Dadurch wird bestimmt, wie &quot;störend&quot;die Push-Benachrichtigung beim Ausgeben sein wird. Weitere Informationen finden Sie in der [Android-Entwicklerdokumentation](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** | Android | Legt eine hohe oder normale Priorität für Ihre Push-Benachrichtigungen fest. Weiterführende Informationen zur Priorität von Nachrichten finden Sie im [Handbuch für Google-Entwickler](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |

## Benutzerspezifische Daten

Im Abschnitt **[!UICONTROL Benutzerspezifische Daten]** können Sie der Nutzlast je nach Konfiguration Ihrer mobilen Anwendung benutzerdefinierte Variablen hinzufügen. Weitere Informationen zum Einrichten von Push-Benachrichtigungen in Adobe Experience Platform und zum Starten der Adobe finden Sie in [diesem Abschnitt](push-configuration.md)

