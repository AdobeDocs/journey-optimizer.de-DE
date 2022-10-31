---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren einer Push-Benachrichtigung
description: Erfahren Sie, wie Sie in Journey Optimizer eine Push-Benachrichtigung erstellen
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '1651'
ht-degree: 100%

---

# Erstellen einer Push-Benachrichtigung {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="Erstellen von Push-Benachrichtigungen"
>abstract="Fügen Sie Ihre Push-Benachrichtigung hinzu und personalisieren Sie sie mit dem Ausdruckseditor."

Push-Benachrichtigungen helfen Ihnen, Ihre Mobile-App-Benutzer jederzeit zu erreichen – insbesondere dann, wenn sie Ihre Mobile App nicht aktiv verwenden. Push-Benachrichtigungen können Ihnen dabei helfen, eine Vielzahl von Anwendungsfällen abzudecken, z. B. Updates zu Ihrem Service bereitzustellen, einen Benutzer zu einer Aktion aufzufordern, den Benutzer auf ein neues Angebot hinzuweisen usw. Geräteplattformen erfordern ein Opt-in, bevor Endbenutzer Ihre Benachrichtigungen empfangen oder anzeigen können. Das Opt-in des Benutzers kann bereits nach dem ersten Start der App nach der Installation oder in einer nachfolgenden Sitzung oder einem nachfolgendem Workflow erfolgen.

[!DNL Journey Optimizer] unterstützt Push-Benachrichtigungen und hilft Ihnen, hochrelevante Benachrichtigungen mit branchenführenden Übertragungsraten zu senden. Push-Benachrichtigungen können Personalisierung und Journey-basierten Kontext enthalten, um die Erkenntnisse aus Daten zu nutzen, die Ihre Marke dank Adobe Experience Cloud hat.

Push-Benachrichtigungen können erstellt werden:

* In einer **Journey**: Nachdem Sie eine Push-Aktivität zu Ihrer Journey hinzugefügt und die Grundeinstellungen festgelegt haben, verwenden Sie den rechten Fensterbereich **[!UICONTROL Aktionen: Push]**, um den Inhalt für die Push-Benachrichtigungen zu erstellen.

   Weitere Informationen zur Konfiguration der Journey auf [dieser Seite](../building-journeys/journey-gs.md).

* In einer **Kampagne**: Nachdem Sie eine Kampagne erstellt haben, wählen Sie „Push-Benachrichtigung“ als Aktion aus und definieren Sie die Grundeinstellungen.

   Weitere Informationen zur Konfiguration einer Kampagne auf [dieser Seite](../campaigns/create-campaign.md#configure).

Verwenden Sie die zugehörigen Registerkarten, um die Push-Benachrichtigungs-Einstellungen für die Betriebssysteme **iOS** und **Android** zu definieren.

![](assets/create-content-push.png)

Wenn Sie zum ersten Mal eine Push-Benachrichtigung erstellen, überprüfen Sie, ob zuvor der Push-Kanal konfiguriert wurde. [Weitere Informationen](../configuration/push-gs.md).

>[!NOTE]
>
>Der Bereich **[!UICONTROL Nachricht erstellen]** ist auf den Registerkarten **[!UICONTROL iOS]** und **[!UICONTROL Android]** verfügbar. Jede Änderung in diesem Abschnitt wird auf beide Einstellungen angewendet.

## Titel und Textkörper {#push-title-body}

Um eine Nachricht zu erstellen, klicken Sie auf die Felder **[!UICONTROL Titel]** und **[!UICONTROL Textkörper]**. Verwenden Sie den Ausdruckseditor, um Inhalte zu definieren, Daten zu personalisieren und dynamische Inhalte hinzuzufügen. Weitere Informationen zu [Personalisierung](../personalization/personalize.md) und [dynamischen Inhalten](../personalization/get-started-dynamic-content.md) finden Sie im Ausdruckseditor.

Im Bereich für die Gerätevorschau sehen Sie, wie die Push-Benachrichtigung auf iOS- und Android-Geräten dargestellt wird.

## Klickverhalten {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Über das Klickverhalten"
>abstract="Wählen Sie das Verhalten, wenn ein Empfänger auf den Hauptteil der Push-Benachrichtigung klickt."

Sie können das Verhalten bestimmen, wenn ein Empfänger auf den Hauptteil der Push-Benachrichtigung klickt.

![](assets/title-body-push.png)

* Um die App zu öffnen, wählen Sie die Option **[!UICONTROL App öffnen]**. Die mit der Benachrichtigung verknüpfte App wird in der [Kanaloberfläche](../configuration/channel-surfaces.md) definiert (d. h. Nachrichtenvoreinstellung).
* Um den Benutzer zu einem bestimmten Inhaltselement innerhalb einer App umzuleiten, wählen Sie die Option **[!UICONTROL Deeplink]**.  Der bestimmte Inhalt kann eine Ansicht, ein Abschnitt einer Seite oder eine Registerkarte sein. Geben Sie nach Auswahl der Option den Deeplink in das entsprechende Feld ein.
* Um den Benutzer zu einer externen URL umzuleiten, verwenden Sie die Option **[!UICONTROL Web-URL]**. Geben Sie nach Auswahl der Option die URL in das entsprechende Feld ein.

## Hinzufügen von Medien {#add-media-push}

In der iOS-Version Ihrer Push-Benachrichtigung können Sie ein Bild, ein Video oder ein GIF hinzufügen, das in Ihrer Benachrichtigung angezeigt wird.

In der Android-Version können Sie nur ein Bildsymbol und ein Bild für erweiterte Benachrichtigungen hinzufügen.

![](assets/push-config-add-media.png)

Dazu sind zwei Optionen verfügbar. Sie haben folgende Möglichkeiten:

* Klicken Sie auf die Schaltfläche **[!UICONTROL Medien hinzufügen]**, um ein Asset in **[!DNL Adobe Experience Manager Assets Essentials]** auszuwählen.

   Wie Sie **[!DNL Adobe Experience Manager Assets Essentials]** verwenden, erfahren Sie auf [dieser Seite](../design/assets-essentials.md).

* Oder geben Sie die URL des Mediums im Feld **[!UICONTROL Medien hinzufügen]** ein. In diesem Fall können Sie die URL personalisieren.

Nach dem Hinzufügen werden die Medien rechts neben dem Textkörper der Benachrichtigung angezeigt.

## Hinzufügen von Schaltflächen {#add-buttons-push}

Erstellen Sie eine verwertbare Benachrichtigung, indem Sie Ihrem Push-Inhalt Schaltflächen hinzufügen.

Wenn der Gerätebildschirm gesperrt ist, werden diese Schaltflächen nicht angezeigt: Nur der **Titel** und die **Nachricht** der Benachrichtigung sind sichtbar. Wenn das Gerät entsperrt ist, sehen die Empfänger die Schaltflächen.

In der iOS-Version können Sie bis zu vier Schaltflächen hinzufügen. In der Android-Version können Sie bis zu drei Schaltflächen hinzufügen.

>[!NOTE]
>
>Verwenden Sie unter iOS das Feld **[!UICONTROL iOS-Kategorie]**, um Aktionen einer Benachrichtigungskategorie zuzuordnen.

1. Klicken Sie auf die **[!UICONTROL Schaltfläche „Hinzufügen“]**, um die Einstellungen zu definieren: den Titel und die zugehörige Aktion. Mögliche Aktionen sind die gleichen wie für das [Verhalten bei Klick](#on-click-behavior).

1. Verwenden Sie für eine Vorschau Ihrer personalisierten Schaltflächen das Symbol **[!UICONTROL Ansicht erweitern]** unter dem zentralen Vorschaubild.

![](assets/push_buttons.png)

## Senden einer stillen Benachrichtigung {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="Über stille Benachrichtigungen"
>abstract="Senden Sie Benachrichtigungen, ohne den Benutzer zu stören, denn die Benachrichtigungen werden nicht im Benachrichtigungszentrum oder in der Benachrichtigungsleiste angezeigt."

Eine stille Push-Benachrichtigung (oder Hintergrundbenachrichtigung) ist eine versteckte Anweisung, die an die Mobile App gesendet wird. Sie wird beispielsweise verwendet, um Ihre Mobile App über die Verfügbarkeit von neuem Inhalt zu informieren oder einen Download im Hintergrund zu starten.

Wählen Sie die Option **[!UICONTROL Stille Benachrichtigung]** aus, um die Mobile App im Hintergrund zu benachrichtigen. In diesem Fall wird die Benachrichtigung direkt auf die Mobile App übertragen. Auf dem Bildschirm des Geräts wird dabei kein Warnhinweis angezeigt.

Verwenden Sie den Abschnitt **[!UICONTROL Benutzerdefinierte Daten]**, um Schlüssel-Wert-Paare hinzuzufügen.

## Benutzerspezifische Daten

Im Abschnitt **[!UICONTROL Benutzerdefinierte Daten]** können Sie der Payload je nach Konfiguration Ihrer Mobile App benutzerdefinierte Variablen hinzufügen. Weitere Informationen zum Einrichten von Push-Benachrichtigungen in Adobe Experience Platform und zu Adobe Launch finden Sie in [diesem Abschnitt](../configuration/push-gs.md)

## Erweiterte Optionen {#advanced-options-push}

Sie können **[!UICONTROL Erweiterte Optionen]** für Ihre Push-Benachrichtigung konfigurieren. Die verfügbaren Parameter sind unten aufgeführt:

| Parameter | Beschreibung |
|---------|---------|
| **[!UICONTROL Reduzierbar]** (iOS/Android) | Eine ausblendbare Nachricht ist eine Nachricht, die durch eine neue Nachricht ersetzt werden kann, wenn sie veraltet ist. Häufig werden ausblendbare Nachrichten verwendet, um eine Mobile App anzuweisen, Daten vom Server zu synchronisieren. Ein Beispiel wäre eine Sport-App, die Benutzer über den aktuellen Spielstand auf dem Laufenden hält. Nur die neueste Nachricht ist relevant. Bei nicht ausblendbaren Nachrichten ist hingegen jede Nachricht wichtig für die Mobile App und muss zugestellt werden. |
| **[!UICONTROL Benutzerdefinierter Benachrichtigungston]**  (iOS/Android) | Der Ton, der beim Empfang der Benachrichtigung vom Mobilgerät wiedergegeben wird. Der Ton muss in der Mobile App verfügbar sein. |
| **[!UICONTROL Badges]**  (iOS/Android) | Mit einem Badge wird die Anzahl der neuen ungelesenen Nachrichten direkt auf dem Mobile-App-Symbol angezeigt. <br/>Der Badge-Wert verschwindet, sobald der Benutzer den neuen Inhalt in der Mobile App öffnet oder liest. Wenn eine Benachrichtigung auf einem Gerät empfangen wird, kann der Badge-Wert für die entsprechende Mobile App aktualisiert oder hinzugefügt werden.<br/>Beispiel: Wenn Sie die Anzahl der ungelesenen Artikel Ihrer Kunden erfassen, können Sie eine Personalisierung anwenden, um für jeden Kunden den entsprechenden Wert für das Badge der ungelesenen Artikel zu senden. Weitere Informationen zur Personalisierung finden Sie in [diesem Abschnitt](../personalization/personalize.md). |
| **[!UICONTROL Benachrichtigungsgruppe]** (nur iOS) | Verknüpfen Sie eine Benachrichtigungsgruppe mit der Push-Benachrichtigung.<br/>Ab iOS 12 ermöglichen Benachrichtigungsgruppen die Konsolidierung von Nachrichten-Threads und Benachrichtigungsthemen als Thread-IDs. Dadurch kann eine Marke beispielsweise Marketing-Benachrichtigungen unter einer Gruppen-ID und Benachrichtigungen mit betrieblichen Informationen unter einer oder mehreren anderen IDs senden.<br/>Beispielsweise können Sie folgende Benachrichtigungsgruppen erstellen: groupID: 123 „Die neue Sweatshirt-Frühlingskollektion ist da“ und groupID: 456 „Ihr Paket wurde zugestellt“. Bei diesem Beispiel würden alle Versandbenachrichtigungen unter der Gruppen-ID 456 gebündelt. |
| **[!UICONTROL Benachrichtigungskanal]**  (Nur Android) | Weisen Sie der Push-Benachrichtigung einen Benachrichtigungskanal zu.<br/>Ab Android 8.0 (API-Stufe 26) müssen alle Benachrichtigungen einem Kanal zugewiesen werden, damit sie angezeigt werden. Weiterführende Informationen zu diesem Thema finden Sie in der [Dokumentation für Android-Entwickler](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Hinzufügen einer Markierung für Inhaltsverfügbarkeit]**  (nur iOS) | Wenn der Inhalt verfügbar ist, wird die Markierung für Inhaltsverfügbarkeit in der Push-Payload gesendet. Dies aktiviert die Mobile App sofort beim Empfang der Push-Benachrichtigung, sodass die Mobile App auf die Payload-Daten zugreifen kann.<br/> Dies ist auch dann möglich, wenn die Mobile App im Hintergrund läuft und ohne dass der Benutzer eingreifen muss (z. B. durch Tippen auf die Push-Benachrichtigung). Diese Möglichkeit besteht jedoch nicht, wenn die Mobile App nicht geöffnet ist. Weiterführende Informationen dazu finden Sie in der [Dokumentation für Apple-Entwickler](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Hinzufügen einer Markierung für veränderbaren Inhalt]**  (nur iOS) | Sendet die Markierung für veränderbaren Inhalt als Teil der Push-Payload und ermöglicht die Änderung des Inhalts der Push-Benachrichtigung durch eine im iOS-SDK bereitgestellte Anwendungserweiterung des Benachrichtigungs-Service. Weiterführende Informationen dazu finden Sie in der [Dokumentation für Apple-Entwickler](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Sie können die Erweiterungen Ihrer Mobile App nutzen, um den Inhalt oder die Darstellung eintreffender Push-Benachrichtigungen, die von [!DNL Journey Optimizer] versandt werden, nachträglich zu ändern. Beispielsweise können Benutzer diese Option nutzen, um Daten zu entschlüsseln, den Textkörper oder Titel einer Benachrichtigung zu ändern, eine Thread-Kennung zu einer Benachrichtigung hinzuzufügen usw. |
| **[!UICONTROL Benachrichtigungssichtbarkeit]**  (Nur Android) | Definiert die Sichtbarkeit der Push-Benachrichtigung. <br/><b>Privat</b>: Die Benachrichtigung wird auf allen Sperrbildschirmen angezeigt, vertrauliche oder private Informationen werden jedoch auf gesicherten Sperrbildschirmen ausgeblendet. <br/><b>Public</b>: Die Benachrichtigung wird vollständig auf allen Sperrbildschirmen angezeigt. <br/><b>Secret</b>: Auf einem gesicherten Sperrbildschirm wird kein Teil der Benachrichtigung angezeigt. <br/>Weiterführende Informationen zu diesem Thema finden Sie in der [Dokumentation für Android-Entwickler](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Benachrichtigungspriorität]** (nur Android) | Definiert die Wichtigkeit der Push-Benachrichtigung von „niedrig“ bis „maximal“. Dadurch wird festgelegt, wie „aufdringlich“ die Push-Benachrichtigung bei der Zustellung ist. Weiterführende Informationen zu diesem Thema finden Sie in der [Dokumentation für Android-Entwickler](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance). |
| **[!UICONTROL Versandpriorität]**  (Nur Android) | Weist Ihren Push-Benachrichtigungen eine hohe oder normale Priorität zu. Weiterführende Informationen zur Priorität von Nachrichten finden Sie in der [Dokumentation für Google-Entwickler](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |


## Validieren der Push-Benachrichtigung{#push-preview}

Sobald der Inhalt der Nachricht festgelegt wurde, können Sie mithilfe von Testprofilen eine Vorschau erstellen und einen Testversand durchführen. Wenn Sie [personalisierte Inhalte](../personalization/personalize.md) eingefügt haben, können Sie überprüfen, wie diese Inhalte in der Nachricht angezeigt werden, indem Sie Testprofildaten verwenden.

Um zu sehen, wie Ihre Push-Benachrichtigung auf mobilen Geräten angezeigt wird, klicken Sie auf die Registerkarte **[!UICONTROL Inhalt simulieren]**. Weiterführende Informationen zum Simulieren von Inhalten finden Sie in [diesem Abschnitt](../design/preview.md).

Sie müssen auch Warnhinweise im oberen Bereich des Editors überprüfen.  Einige davon sind einfache Warnhinweise, andere können die Verwendung der Nachricht verhindern. Weiterführende Informationen finden Sie in [diesem Abschnitt](alerts.md).

![](assets/push-alert-button.png)

**Verwandte Themen**

<!--
* [Understand push notification flow](push-gs.md)
-->

* [Konfigurieren des Push-Kanals](../configuration/push-gs.md)
* [Erstellen einer neuen Nachricht](get-started-content.md)
* [Hinzufügen einer Nachricht zu einer Journey](../building-journeys/journeys-message.md)
