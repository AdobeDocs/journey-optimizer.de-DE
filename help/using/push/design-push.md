---
solution: Journey Optimizer
product: journey optimizer
title: Push-Benachrichtigung erstellen
description: Erfahren Sie, wie Sie eine Push-Benachrichtigung in Journey Optimizer erstellen
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 6f6d693d-11f2-48b7-82a8-171829bf8045
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 0%

---

# Push-Benachrichtigung erstellen {#design-push-notification}

## Titel und Hauptteil {#push-title-body}

Um Ihre Nachricht zu erstellen, klicken Sie auf die Schaltfläche **[!UICONTROL Title]** und **[!UICONTROL Body]** -Felder. Verwenden Sie den Ausdruckseditor, um Inhalte zu definieren, Daten zu personalisieren und dynamischen Inhalt hinzuzufügen. Weitere Informationen [Personalisierung](../personalization/personalize.md) und [dynamischer Inhalt](../personalization/get-started-dynamic-content.md) im Ausdruckseditor.

Verwenden Sie den Bereich &quot;Gerätevorschau&quot;, um zu visualisieren, wie die Push-Benachrichtigung auf iOS- und Android-Geräten angezeigt wird.

## Klickverhalten {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Über das Klickverhalten"
>abstract="Wählen Sie das Verhalten aus, wenn ein Empfänger auf den Text der Push-Benachrichtigung klickt."

Sie können das Verhalten auswählen, wenn ein Benutzer auf den Text der Push-Benachrichtigung klickt.

![](assets/title-body-push.png)

* Um die App zu öffnen, wählen Sie die **[!UICONTROL Open app]** -Option. Die mit der Benachrichtigung verknüpfte App wird im [Kanaloberfläche](../configuration/channel-surfaces.md) (d. h. Nachrichtenvorgabe).
* Um den Benutzer zu einem bestimmten Inhaltselement innerhalb einer App umzuleiten, wählen Sie die **[!UICONTROL Deeplink]** -Option.  Der spezifische Inhalt kann eine bestimmte Ansicht, einen bestimmten Abschnitt einer Seite oder eine bestimmte Registerkarte sein. Geben Sie nach Auswahl der Option den Deeplink in das entsprechende Feld ein.
* Um den Benutzer zu einer externen URL umzuleiten, verwenden Sie die **[!UICONTROL Web URL]** -Option. Geben Sie nach Auswahl der Option die URL in das entsprechende Feld ein.

## Medien hinzufügen {#add-media-push}

In der iOS-Version Ihrer Push-Benachrichtigung können Sie ein Bild, ein Video oder ein GIF hinzufügen, das bzw. das in Ihrer Benachrichtigung angezeigt wird.

In der Android-Version können Sie nur ein Bildsymbol und ein Bild für erweiterte Benachrichtigungen hinzufügen.

![](assets/push-config-add-media.png)

Es stehen zwei Optionen zur Verfügung. Sie können:

* Verwenden Sie die **[!UICONTROL Add media]** Schaltfläche zum Auswählen eines Assets in **[!DNL Adobe Experience Manager Assets Essentials]**.

   Erfahren Sie, wie Sie **[!DNL Adobe Experience Manager Assets Essentials]** in [diese Seite](../email/assets-essentials.md).

* Oder geben Sie die URL des Mediums im **[!UICONTROL Add media]** -Feld. In diesem Fall können Sie der URL Personalisierung hinzufügen.

Nach dem Hinzufügen werden die Medien rechts neben dem Benachrichtigungsinhalt angezeigt.

## Schaltflächen hinzufügen {#add-buttons-push}

Erstellen Sie eine verwertbare Benachrichtigung, indem Sie Schaltflächen zu Ihrem Push-Inhalt hinzufügen.

Wenn der Gerätebildschirm gesperrt ist, werden diese Schaltflächen nicht angezeigt: nur die **Titel** und **Nachricht** der Benachrichtigung angezeigt. Wenn das Gerät entsperrt ist, sehen die Empfänger die Schaltflächen.

In der iOS-Version können Sie bis zu vier Schaltflächen hinzufügen. In der Android-Version können Sie bis zu drei Schaltflächen hinzufügen.

>[!NOTE]
>
>Für iOS verwenden Sie die **[!UICONTROL iOS category]** -Feld zum Verknüpfen von Aktionen mit einer Benachrichtigungskategorie.

1. Verwenden Sie die **[!UICONTROL Add button]** zur Definition von Einstellungen: den Titel und die zugehörige Aktion. Die möglichen Aktionen entsprechen denen von [Klick-Verhalten](#on-click-behavior).

1. Verwenden Sie die **[!UICONTROL Expand view]** -Symbol unter dem zentralen Vorschaubild, um eine Vorschau Ihrer personalisierten Schaltflächen anzuzeigen.

![](assets/push_buttons.png)

## Stille Benachrichtigung senden {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="Über stille Benachrichtigungen"
>abstract="Benachrichtigungen senden, ohne den Benutzer zu stören, werden Benachrichtigungen nicht im Benachrichtigungszentrum oder in der Benachrichtigungsleiste angezeigt."

Eine stille Push-Benachrichtigung (oder Hintergrundbenachrichtigung) ist eine versteckte Anweisung, die an die Anwendung gesendet wird. Sie wird beispielsweise verwendet, um Ihre Anwendung über die Verfügbarkeit neuer Inhalte zu informieren oder einen Download im Hintergrund zu starten.

Wählen Sie die **[!UICONTROL Silent Notification]** Option zur stillen Benachrichtigung der Anwendung: in diesem Fall wird die Benachrichtigung direkt an den Antrag übermittelt. Auf dem Gerätebildschirm wird kein Warnhinweis angezeigt.

Verwenden Sie die **[!UICONTROL Custom data]** -Abschnitt, um Schlüssel-Wert-Paare hinzuzufügen.

## Benutzerdefinierte Daten

Im **[!UICONTROL Custom data]** -Abschnitt können Sie der Payload je nach Konfiguration Ihrer Mobile App benutzerdefinierte Variablen hinzufügen. Weitere Informationen zum Einrichten von Push-Benachrichtigungen in Adobe Experience Platform und Adobe Launch finden Sie unter [diesem Abschnitt](push-gs.md)

## Erweiterte Optionen {#advanced-options-push}

Sie können **[!UICONTROL Advanced options]** für Ihre Push-Benachrichtigung. Die verfügbaren Parameter sind unten aufgeführt:

| Parameter | Beschreibung |
|---------|---------|
| **[!UICONTROL Collapsible]** (iOS/Android) | Eine ausblendbare Nachricht ist eine Nachricht, die durch eine neue Nachricht ersetzt werden kann, wenn sie veraltet ist. Häufig werden ausblendbare Nachrichten verwendet, um eine Mobile App anzuweisen, Daten vom Server zu synchronisieren. Ein Beispiel wäre eine Sport-App, die Benutzer mit der neuesten Punktzahl aktualisiert. Nur die neueste Nachricht ist relevant. Andererseits ist bei einer nicht ausblendbaren Nachricht eine sehr Botschaft für die Client-App wichtig und muss bereitgestellt werden. |
| **[!UICONTROL Custom sound]** (iOS/Android) | Der Ton, der vom Mobilgerät bei Erhalt der Benachrichtigung abgespielt werden soll. Der Ton muss in der App gebündelt werden. |
| **[!UICONTROL Badges]** (iOS/Android) | Ein Badge wird verwendet, um direkt auf dem Anwendungssymbol die Anzahl der neuen ungelesenen Informationen anzuzeigen. <br/>Der Badge-Wert verschwindet, sobald der Benutzer den neuen Inhalt in der Anwendung öffnet oder liest. Wenn eine Benachrichtigung auf einem Gerät empfangen wird, kann ein Badge-Wert für die zugehörige App aktualisiert oder hinzugefügt werden.<br/>Wenn Sie beispielsweise die Anzahl der ungelesenen Artikel Ihrer Kunden speichern, können Sie die Personalisierung nutzen, um den eindeutigen Badge-Wert für ungelesene Artikel für jeden Kunden zu senden. Weitere Informationen zur Personalisierung finden Sie unter [diesem Abschnitt](../personalization/personalize.md). |
| **[!UICONTROL Notification group]**  (nur iOS) | Ordnen Sie der Push-Benachrichtigung eine Benachrichtigungsgruppe zu.<br/>Ab iOS 12 können Sie mit Benachrichtigungsgruppen Nachrichten-Threads und Benachrichtigungsthemen in Thread-IDs zusammenfassen. Beispielsweise kann eine Marke Marketing-Benachrichtigungen unter einer Gruppen-ID senden und gleichzeitig betriebliche Typbenachrichtigungen unter einer oder mehreren verschiedenen IDs speichern.<br/>Um dies zu veranschaulichen, können Sie groupID verwenden: 123 &quot;Sehen Sie sich die neue Frühlingskollektion der Pullover an&quot; und groupID: 456 Benachrichtigungsgruppen &quot;Ihr Paket wurde zugestellt&quot;. In diesem Beispiel würden alle Versandbenachrichtigungen unter der Gruppen-ID gebündelt: 456. |
| **[!UICONTROL Notification channel]** (Nur Android) | Weisen Sie der Push-Benachrichtigung einen Benachrichtigungskanal zu.<br/>Ab Android 8.0 (API-Ebene 26) müssen alle Benachrichtigungen einem Kanal zugewiesen werden, damit sie angezeigt werden. Weitere Informationen hierzu finden Sie im Abschnitt [Android-Entwicklerdokumentation](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Add content-availability flag]** (nur iOS) | Sendet das Inhalt-verfügbar-Flag in der Push-Payload, um sicherzustellen, dass die App aktiviert wird, sobald sie die Push-Benachrichtigung erhält. Das bedeutet, dass die App auf die Payload-Daten zugreifen kann.<br/> Dies funktioniert auch, wenn die App im Hintergrund ausgeführt wird und keine Benutzerinteraktion erforderlich ist (z. B. Tippen auf Push-Benachrichtigung). Dies gilt jedoch nicht, wenn die App nicht ausgeführt wird. Weitere Informationen hierzu finden Sie im Abschnitt [Apple-Entwicklerdokumentation](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Add mutable-content flag]** (nur iOS) | Sendet das Flag für veränderlichen Inhalt in der Push-Payload und ermöglicht die Änderung des Inhalts der Push-Benachrichtigung durch eine im iOS SDK enthaltene Erweiterung der Benachrichtigungsdienst-Anwendung. Weitere Informationen hierzu finden Sie unter [Apple-Entwicklerdokumentation](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Sie können dann Ihre Mobile-App-Erweiterungen nutzen, um den Inhalt oder die Darstellung von eingehenden Push-Benachrichtigungen, die von gesendet werden, weiter zu ändern. [!DNL Journey Optimizer]. Beispielsweise können Benutzer diese Option nutzen, um Daten zu entschlüsseln, den Text oder Titel einer Benachrichtigung zu ändern, eine Thread-Kennung zu einer Benachrichtigung hinzuzufügen usw. |
| **[!UICONTROL Notification visibility]** (Nur Android) | Definiert die Sichtbarkeit der Push-Benachrichtigung. <br/><b>Privat</b> zeigt die Benachrichtigung auf allen Schlossbildschirmen an, verbergt jedoch vertrauliche oder private Informationen auf sicheren Schlossbildschirmen. <br/><b>Öffentlich</b> zeigt die Benachrichtigung in ihrer Gesamtheit auf allen Schlossbildschirmen an. <br/><b>Geheimnis</b> zeigt keinen Teil der Benachrichtigung auf einem sicheren Sperrbildschirm an. <br/>Weitere Informationen hierzu finden Sie im Abschnitt [Android-Entwicklerdokumentation](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Notification priority]** (Nur Android) | Definiert die Wichtigkeit der Push-Benachrichtigung von &quot;Niedrig&quot;bis &quot;Maximal&quot;. Dadurch wird bestimmt, wie &quot;störend&quot;die Push-Benachrichtigung beim Versand sein wird. Weitere Informationen hierzu finden Sie im Abschnitt [Android-Entwicklerdokumentation](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** (Nur Android) | Legt eine hohe oder normale Priorität für Ihre Push-Benachrichtigungen fest. Weiterführende Informationen zur Priorität von Nachrichten finden Sie im Abschnitt [Dokumentation für Google-Entwickler](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |
