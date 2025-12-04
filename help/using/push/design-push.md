---
solution: Journey Optimizer
product: journey optimizer
title: Gestalten einer Push-Benachrichtigung
description: Erfahren Sie, wie man in Journey Optimizer eine Push-Benachrichtigung gestaltet
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: 6f6d693d-11f2-48b7-82a8-171829bf8045
source-git-commit: 31f0ff2497b5d3c1211c26e8bcd9a12d072f298d
workflow-type: tm+mt
source-wordcount: '1651'
ht-degree: 90%

---

# Gestalten einer Push-Benachrichtigung {#design-push-notification}

## Titel und Hauptteil {#push-title-body}

>[!CONTEXTUALHELP]
>id="ajo-message-push-compose"
>title="Personalisieren Sie Ihre Push-Benachrichtigung."
>abstract="Um Ihre Nachricht zu erstellen, geben Sie den Inhalt in die Felder **Titel** und **Hauptteil** ein. Um Personalisierungs-Token einzuschließen, öffnen Sie das Personalisierungsdialogfeld."

Um eine Nachricht zu erstellen, klicken Sie auf die Felder **[!UICONTROL Titel]** und **[!UICONTROL Hauptteil]**. Verwenden Sie den Personalisierungseditor, um Inhalte zu definieren, Daten zu personalisieren und dynamische Inhalte hinzuzufügen. Erfahren Sie mehr zu [Personalisierung](../personalization/personalize.md) und [dynamischen Inhalten](../personalization/get-started-dynamic-content.md) im Personalisierungseditor.

Im Bereich für die Gerätevorschau sehen Sie, wie die Push-Benachrichtigung auf iOS- und Android-Geräten dargestellt wird.

Beschleunigen Sie die Inhaltserstellung mit dem KI-Assistenten und generieren Sie mit dem [KI-Assistenten für die Textgenerierung](../content-management/generative-text.md) überzeugenden Push-Benachrichtigungstext oder erstellen Sie vollständige Push-Benachrichtigungen mit dem [KI-Assistenten für die vollständige Inhaltserstellung](../content-management/generative-full-content.md).

## Klickverhalten {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Über das Klickverhalten"
>abstract="Wählen Sie das Verhalten, wenn ein Empfänger auf den Hauptteil der Push-Benachrichtigung klickt."

Sie können das Verhalten bestimmen, wenn ein Empfänger auf den Hauptteil der Push-Benachrichtigung klickt.

![](assets/title-body-push.png)

* Um die App zu öffnen, wählen Sie die Option **[!UICONTROL App öffnen]**. Die mit der Benachrichtigung verknüpfte App wird in der [Kanalkonfiguration](../configuration/channel-surfaces.md) definiert (d. h. Nachrichtenvoreinstellung).
* Um den Benutzer zu einem bestimmten Inhaltselement innerhalb einer App umzuleiten, wählen Sie die Option **[!UICONTROL Deeplink]**.  Der bestimmte Inhalt kann eine Ansicht, ein Abschnitt einer Seite oder eine Registerkarte sein. Geben Sie nach Auswahl der Option den Deeplink in das entsprechende Feld ein.
* Um den Benutzer zu einer externen URL umzuleiten, verwenden Sie die Option **[!UICONTROL Web-URL]**. Geben Sie nach Auswahl der Option die URL in das entsprechende Feld ein.

## Hinzufügen von Medien {#add-media-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-media"
>title="Hinzufügen von Medien zu Push-Benachrichtigungen"
>abstract="Sie können ein Bild, ein Video oder ein GIF hinzufügen, das in Ihrer Benachrichtigung angezeigt wird."

In der iOS-Version Ihrer Push-Benachrichtigung können Sie ein Bild, ein Video oder ein GIF hinzufügen, das in Ihrer Benachrichtigung angezeigt wird.

In der Android-Version können Sie nur ein Bildsymbol und ein Bild für erweiterte Benachrichtigungen hinzufügen.

![](assets/push-config-add-media.png)

Dazu sind zwei Optionen verfügbar. Sie haben folgende Möglichkeiten:

* Klicken Sie auf die Schaltfläche **[!UICONTROL Medien hinzufügen]**, um ein Asset in **[!DNL Adobe Experience Manager Assets]** auszuwählen.

  Wie Sie **[!DNL Adobe Experience Manager Assets]** verwenden, erfahren Sie auf [dieser Seite](../integrations/assets.md).

* Oder geben Sie die URL des Mediums im Feld **[!UICONTROL Medien hinzufügen]** ein. In diesem Fall können Sie die URL personalisieren.

Nach dem Hinzufügen werden die Medien rechts neben dem Textkörper der Benachrichtigung angezeigt.

Beachten Sie, dass Ihre Mobile App beim Einfügen von Medienanlagen in die Payload der Push-Benachrichtigung, wie z. B. Bilder in benutzerdefinierten Datenfeldern wie `adb_media`, eine spezifische Client-seitige Verarbeitung für die Bilder implementieren muss, die auf Geräten gerendert werden sollen:

* **iOS**: Ihre App muss eine [Erweiterung für den Benachrichtigungsdienst](https://developer.apple.com/documentation/usernotifications/modifying_content_in_newly_delivered_notifications){target="_blank"} implementieren, um Medieninhalte aus der Payload herunterzuladen und zu verarbeiten. Darüber hinaus muss **[!UICONTROL Option &quot;]**-Flag für veränderbaren Inhalt hinzufügen[&#x200B; im Abschnitt „Erweiterte Optionen](#advanced-options-push) aktiviert werden.
* **Android**: Ihre App muss den [automatischen Anzeige- und Tracking-Workflow](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/push-notification/android/automatic-display-and-tracking/){target="_blank"} implementieren, um Bildanhänge aus der Payload zu verarbeiten.

## Hinzufügen von Schaltflächen {#add-buttons-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-buttons"
>title="Fügen Sie Schaltflächen hinzu, über die Benutzende mit Ihrer Push-Benachrichtigung interagieren können."
>abstract="Fügen Sie Ihrer Nachricht in diesem Abschnitt CTA-Schaltflächen hinzu. Geben Sie für Apple iOS eine Kennung der Benachrichtigungskategorie an. Für Google Android können Sie für jede Schaltfläche benutzerdefinierten Text und Ziele hinzufügen."

Erstellen Sie eine verwertbare Benachrichtigung, indem Sie Ihrem Push-Inhalt Schaltflächen hinzufügen.

Wenn der Gerätebildschirm gesperrt ist, werden diese Schaltflächen nicht angezeigt und nur der **Titel** und die **Nachricht** der Benachrichtigung sind sichtbar. Wenn das Gerät entsperrt ist, sehen die Empfangenden die Schaltflächen.

In der Android-Version können Sie bis zu drei Schaltflächen hinzufügen.

In der iOS-Version wird eine Kategoriekennung der Benachrichtigung angegeben. Benachrichtigungskategorien müssen in der iOS-App vorkonfiguriert werden. Dadurch werden die anzuzeigenden Schaltflächen und die durchgeführten Aktionen definiert. Weitere Informationen dazu finden Sie in der [Apple-Dokumentation](https://developer.apple.com/documentation/usernotifications/declaring_your_actionable_notification_types).

1. Klicken Sie auf die **[!UICONTROL Schaltfläche „Hinzufügen“]**, um die Einstellungen zu definieren: das Label und die zugehörige Aktion. Mögliche Aktionen sind die gleichen wie für das [Verhalten bei Klick](#on-click-behavior).

1. Verwenden Sie für eine Vorschau Ihrer personalisierten Schaltflächen das Symbol **[!UICONTROL Ansicht erweitern]** unter dem zentralen Vorschaubild.

   ![](assets/push_buttons.png)

## Senden einer stillen Benachrichtigung {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="Über stille Benachrichtigungen"
>abstract="Senden von Benachrichtigungen, ohne den Benutzer bzw. die Benutzerin zu stören, denn die Benachrichtigungen werden nicht im Benachrichtigungszentrum oder in der Benachrichtigungsleiste angezeigt."

Eine stille Push-Benachrichtigung (oder Hintergrundbenachrichtigung) ist eine versteckte Anweisung, die an die Mobile App gesendet wird. Sie wird beispielsweise verwendet, um Ihre Mobile App über die Verfügbarkeit von neuem Inhalt zu informieren oder einen Download im Hintergrund zu starten.

Wählen Sie die Option **[!UICONTROL Stille Benachrichtigung]** aus, um die Mobile App im Hintergrund zu benachrichtigen. In diesem Fall wird die Benachrichtigung direkt auf die Mobile App übertragen. Auf dem Bildschirm des Geräts wird dabei kein Warnhinweis angezeigt.

Verwenden Sie den Abschnitt **[!UICONTROL Benutzerdefinierte Daten]**, um Schlüssel-Wert-Paare hinzuzufügen.

## Benutzerdefinierte Daten {#custom-data}

>[!CONTEXTUALHELP]
>id="ajo-message-push-custom"
>title="Konfigurieren Sie benutzerdefinierte Daten für Ihre Push-Benachrichtigung."
>abstract="Fügen Sie der Payload je nach Konfiguration Ihrer Mobile App benutzerdefinierte Variablen hinzu."

Im Abschnitt **[!UICONTROL Benutzerdefinierte Daten]** können Sie der Payload je nach Konfiguration Ihrer Mobile App benutzerdefinierte Variablen hinzufügen. Weitere Informationen zum Einrichten von Push-Benachrichtigungen in Adobe Experience Platform finden Sie in [diesem Abschnitt](push-gs.md).

## Erweiterte Optionen {#advanced-options-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-advanced"
>title="Konfigurieren Sie erweiterte Optionen für Ihre Push-Benachrichtigung."
>abstract="In diesem Abschnitt können Sie die Personalisierung Ihrer Push-Benachrichtigung optimieren."

Sie können **[!UICONTROL Erweiterte Optionen]** für Ihre Push-Benachrichtigung konfigurieren. Die verfügbaren Parameter sind unten aufgeführt:

| Parameter | Beschreibung |
|---------|---------|
| **[!UICONTROL Reduzierbar]** (iOS/Android) | Eine ausblendbare Nachricht ist eine Nachricht, die durch eine neue Nachricht ersetzt werden kann, wenn sie veraltet ist. Häufig werden ausblendbare Nachrichten verwendet, um eine Mobile App anzuweisen, Daten vom Server zu synchronisieren. Ein Beispiel wäre eine Sport-App, die Benutzer über den aktuellen Spielstand auf dem Laufenden hält. Nur die neueste Nachricht ist relevant. Bei nicht ausblendbaren Nachrichten ist hingegen jede Nachricht wichtig für die Client-App und muss zugestellt werden. |
| **[!UICONTROL Benutzerdefinierter Ton]** (iOS/Android) | Der Ton, der beim Empfang der Benachrichtigung vom Mobilgerät wiedergegeben wird. Der Ton muss in der Mobile App verfügbar sein. |
| **[!UICONTROL Badges]** (iOS/Android) | Mit einem Badge wird die Anzahl der neuen ungelesenen Nachrichten direkt auf dem Mobile-App-Symbol angezeigt. <br/>Der Badge-Wert verschwindet, sobald der Benutzer den neuen Inhalt in der Mobile App öffnet oder liest. Wenn eine Benachrichtigung auf einem Gerät empfangen wird, kann der Badge-Wert für die entsprechende Mobile App aktualisiert oder hinzugefügt werden.<br/>Beispiel: Wenn Sie die Anzahl der ungelesenen Artikel Ihrer Kunden erfassen, können Sie eine Personalisierung anwenden, um für jeden Kunden den entsprechenden Wert für das Badge der ungelesenen Artikel zu senden. Weitere Informationen zur Personalisierung finden Sie in [diesem Abschnitt](../personalization/personalize.md). |
| **[!UICONTROL Benachrichtigungsgruppe]** (nur iOS) | Verknüpfen Sie eine Benachrichtigungsgruppe mit der Push-Benachrichtigung.<br/>Ab iOS 12 ermöglichen Benachrichtigungsgruppen die Konsolidierung von Nachrichten-Threads und Benachrichtigungsthemen als Thread-IDs. Dadurch kann eine Marke beispielsweise Marketing-Benachrichtigungen unter einer Gruppen-ID und Benachrichtigungen mit betrieblichen Informationen unter einer oder mehreren anderen IDs senden.<br/>Beispielsweise können Sie folgende Benachrichtigungsgruppen erstellen: groupID: 123 „Die neue Sweatshirt-Frühlingskollektion ist da“ und groupID: 456 „Ihr Paket wurde zugestellt“. Bei diesem Beispiel würden alle Versandbenachrichtigungen unter der Gruppen-ID 456 gebündelt. |
| **[!UICONTROL Benachrichtigungskanal]** (nur Android) | Weisen Sie der Push-Benachrichtigung einen Benachrichtigungskanal zu.<br/>Ab Android 8.0 (API-Stufe 26) müssen alle Benachrichtigungen einem Kanal zugewiesen werden, damit sie angezeigt werden. Weiterführende Informationen zu diesem Thema finden Sie in der [Dokumentation für Android-Entwickler](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Kennzeichnung für Inhaltsverfügbarkeit hinzufügen]** (nur iOS) | Wenn der Inhalt verfügbar ist, wird die Markierung für Inhaltsverfügbarkeit in der Push-Payload gesendet. Dies aktiviert die Mobile App sofort beim Empfang der Push-Benachrichtigung, sodass die Mobile App auf die Payload-Daten zugreifen kann.<br/> Dies ist auch dann möglich, wenn die Mobile App im Hintergrund läuft und ohne dass der Benutzer eingreifen muss (z. B. durch Tippen auf die Push-Benachrichtigung). Diese Möglichkeit besteht jedoch nicht, wenn die Mobile App nicht geöffnet ist. Weiterführende Informationen dazu finden Sie in der [Dokumentation für Apple-Entwickler](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Kennzeichnung für veränderbaren Inhalt hinzufüge]** (nur iOS) | Sendet die Markierung für veränderbaren Inhalt als Teil der Push-Payload und ermöglicht die Änderung des Inhalts der Push-Benachrichtigung durch eine im iOS-SDK bereitgestellte Anwendungserweiterung des Benachrichtigungs-Service. Weiterführende Informationen dazu finden Sie in der [Dokumentation für Apple-Entwickler](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Sie können die Erweiterungen Ihrer Mobile App nutzen, um den Inhalt oder die Darstellung eintreffender Push-Benachrichtigungen, die von [!DNL Journey Optimizer] versandt werden, nachträglich zu ändern. Beispielsweise können Benutzer diese Option nutzen, um Daten zu entschlüsseln, den Textkörper oder Titel einer Benachrichtigung zu ändern, eine Thread-Kennung zu einer Benachrichtigung hinzuzufügen usw.<br/>**Wichtig**: Dieses Flag muss aktiviert werden, wenn Medienanlagen (Bilder, Videos) über Payload-Felder (wie `adb_media`) eingefügt werden, damit sie auf iOS-Geräten gerendert werden können. Ihre App muss auch eine Erweiterung des Benachrichtigungsdienstes implementieren, um den Medieninhalt aus der Payload herunterzuladen und zu verarbeiten. |
| **[!UICONTROL Hinzufügen des Ablaufs von Push-Benachrichtigungen]** (nur iOS) | Wählen Sie das **Datum und die Uhrzeit** für den Ablauf Ihrer Push-Benachrichtigung aus. Auf iOS wird der Ablauf von Benachrichtigungen als Hardstop erzwungen, d. h. eine Nachricht, die nach Ablauf der Dauer an den Apple Push Notification Service (APNS) gesendet wird, wird nicht zugestellt, sodass Kundinnen und Kunden nie veraltete oder irrelevante Benachrichtigungen erhalten. Weiterführende Informationen dazu finden Sie in der [Dokumentation für Apple-Entwickelnde](https://developer.apple.com/documentation/usernotifications/sending-notification-requests-to-apns). |
| **[!UICONTROL Benachrichtigungssichtbarkeit]** (nur Android) | Definiert die Sichtbarkeit der Push-Benachrichtigung. <br/><b>Privat</b>: Die Benachrichtigung wird auf allen Sperrbildschirmen angezeigt, vertrauliche oder private Informationen werden jedoch auf gesicherten Sperrbildschirmen ausgeblendet. <br/><b>Public</b>: Die Benachrichtigung wird vollständig auf allen Sperrbildschirmen angezeigt. <br/><b>Secret</b>: Auf einem gesicherten Sperrbildschirm wird kein Teil der Benachrichtigung angezeigt. <br/>Weiterführende Informationen zu diesem Thema finden Sie in der [Dokumentation für Android-Entwickler](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Benachrichtigungspriorität]** (nur Android) | Definiert die Wichtigkeit der Push-Benachrichtigung von „niedrig“ bis „maximal“. Dadurch wird festgelegt, wie „aufdringlich“ die Push-Benachrichtigung bei der Zustellung ist. Weiterführende Informationen zu diesem Thema finden Sie in der [Dokumentation für Android-Entwickler](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance). |
| **[!UICONTROL Versandpriorität]** (nur Android) | Weist Ihren Push-Benachrichtigungen eine hohe oder normale Priorität zu. Weiterführende Informationen zur Priorität von Nachrichten finden Sie in der [Dokumentation für Google-Entwickler](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |
| **[!UICONTROL Gültigkeitsdauer]** (nur Android) | Legen Sie die Anzahl der Sekunden fest, nach denen Ihre Nachricht abläuft. In Android wird die Gültigkeit als Versandfenster behandelt: Firebase Cloud Messaging (FCM) konvertiert die Gültigkeitsdauer ab dem Empfang der Nachricht in einen TTL-Wert (Time-to-Live; Gültigkeitsdauer), was bedeutet, dass nicht zugestellte Kampagnen später als erwartet oder sogar außerhalb des gewünschten Zeitraums gesendet werden können. Weiterführende Informationen zu diesem Thema finden Sie in der [Dokumentation für Android-Entwickelnde](https://firebase.google.com/docs/cloud-messaging/concept-options#ttl). |
