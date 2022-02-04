---
title: Konfigurieren einer Push-Benachrichtigung
description: Erfahren Sie, wie Sie in Journey Optimizer eine Push-Benachrichtigung erstellen
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 5866a5ad181b9b745cedc4fa740d131cf7c88863
workflow-type: tm+mt
source-wordcount: '1262'
ht-degree: 99%

---

# Erstellen einer Push-Benachrichtigung {#create-push-notification}

Nachdem Sie [eine Nachricht erstellt](create-message.md) haben, klicken Sie auf die Registerkarte **[!UICONTROL Push-Benachrichtigung]**, um die Einstellungen und den Inhalt der Push-Benachrichtigung zu definieren.

![](assets/create-content-push.png)

Verwenden Sie die zugehörigen Registerkarten, um die Push-Benachrichtigungs-Einstellungen für die Betriebssysteme **iOS** und **Android** zu definieren.

>[!NOTE]
>
>Der Bereich **[!UICONTROL Nachricht erstellen]** ist auf den Registerkarten **[!UICONTROL iOS]** und **[!UICONTROL Android]** verfügbar. Jede Änderung in diesem Abschnitt wird für beide Registerkarten angewendet.

## Titel und Textkörper

Um eine Nachricht zu erstellen, klicken Sie auf die Felder **[!UICONTROL Titel]** und **[!UICONTROL Textkörper]**. Mit dem Ausdruckseditor können Sie Inhalt und Personalisierungsdaten definieren. Weitere Informationen zur Personalisierung im Ausdruckseditor finden Sie in [diesem Abschnitt](personalization/personalize.md).

Im Abschnitt für die Gerätevorschau sehen Sie, wie die Push-Benachrichtigung auf iOS- und Android-Geräten dargestellt wird.

## Klickverhalten {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Über das Klickverhalten"
>abstract="Definieren Sie das Verhalten beim Klicken auf den Textkörper der Push-Benachrichtigung durch einen Empfänger."

Definieren Sie das Verhalten beim Klicken auf den Textkörper der Push-Benachrichtigung durch einen Empfänger.

![](assets/title-body-push.png)

* Verwenden Sie die Option **[!UICONTROL Mobile App öffnen]**, um die Mobile App zu öffnen, die in der **[!UICONTROL Voreinstellung]** der Nachricht definiert ist.
* Verwenden Sie die Option **[!UICONTROL Deeplink]**, um den Empfänger an einen bestimmten Inhalt in der Mobile App weiterzuleiten. Fügen Sie den Deeplink in das entsprechende Feld ein.
* Verwenden Sie die Option **[!UICONTROL Web-URL]**, um den Empfänger an eine externe URL weiterzuleiten. Fügen Sie die URL in das entsprechende Feld ein.

## Hinzufügen von Medien

In der iOS-Version Ihrer Push-Benachrichtigung können Sie ein Bild, ein Video oder ein GIF hinzufügen, das in Ihrer Benachrichtigung angezeigt wird.

In der Android-Version können Sie nur ein Bildsymbol und ein Bild für erweiterte Benachrichtigungen hinzufügen.

![](assets/push-config-add-media.png)

Dazu sind zwei Optionen verfügbar. Sie haben folgende Möglichkeiten:

* Klicken Sie auf die Schaltfläche **[!UICONTROL Medien hinzufügen]**, um ein Asset in **[!DNL Adobe Experience Manager Assets Essentials]** auszuwählen.

   Wie Sie **[!DNL Adobe Experience Manager Assets Essentials]** verwenden, erfahren Sie auf [dieser Seite](assets-essentials.md).

* Oder geben Sie die URL des Mediums ein, indem Sie auf das Feld **[!UICONTROL Medien hinzufügen]** klicken. In diesem Fall können Sie eine Personalisierung hinzufügen.

Nach dem Hinzufügen werden die Medien rechts neben dem Textkörper der Benachrichtigung angezeigt.

## Hinzufügen von Schaltflächen

Sie können eine aktionsfähige Benachrichtigung erstellen, indem Sie Ihrem Push-Inhalt Schaltflächen hinzufügen.

Wenn der Gerätebildschirm gesperrt ist, werden diese Schaltflächen nicht angezeigt: Nur der **Titel** und die **Nachricht** der Benachrichtigung sind sichtbar. Wenn das Gerät entsperrt ist, sehen die Empfänger die Schaltflächen.

In der iOS-Version können Sie bis zu vier Schaltflächen hinzufügen. In der Android-Version können Sie bis zu drei Schaltflächen hinzufügen.

>[!NOTE]
>
>Verwenden Sie für iOS das Feld **[!UICONTROL iOS-Kategorie]**, um Aktionen einer Benachrichtigungskategorie zuzuordnen.

Klicken Sie auf **[!UICONTROL Schaltfläche hinzufügen]**, um die Einstellungen zu definieren: die Bezeichnung und die zugehörige Aktion. Mögliche Aktionen sind dieselben wie für das [Klickverhalten](#on-click-behavior).

Klicken Sie auf **[!UICONTROL Ansicht erweitern]**, um eine Vorschau Ihrer personalisierten Buttons anzuzeigen.

![](assets/push_buttons.png)

## Senden einer stillen Benachrichtigung

Eine stille Push-Benachrichtigung (oder Hintergrundbenachrichtigung) ist eine versteckte Anweisung, die an die Mobile App gesendet wird. Sie wird beispielsweise verwendet, um Ihre Mobile App über die Verfügbarkeit von neuem Inhalt zu informieren oder einen Download im Hintergrund zu starten.

Wählen Sie die Option **[!UICONTROL Stille Benachrichtigung]** aus, um die Mobile App im Hintergrund zu benachrichtigen. In diesem Fall wird die Benachrichtigung direkt auf die Mobile App übertragen. Auf dem Bildschirm des Geräts wird dabei kein Warnhinweis angezeigt.

Verwenden Sie den Abschnitt **[!UICONTROL Benutzerdefinierte Daten]**, um Schlüssel-Wert-Paare hinzuzufügen.

## Benutzerspezifische Daten

Im Abschnitt **[!UICONTROL Benutzerdefinierte Daten]** können Sie der Payload je nach Konfiguration Ihrer Mobile App benutzerdefinierte Variablen hinzufügen. Weitere Informationen zum Einrichten von Push-Benachrichtigungen in Adobe Experience Platform und zu Adobe Launch finden Sie in [diesem Abschnitt](push-gs.md)

## Erweiterte Optionen

Sie können **[!UICONTROL Erweiterte Optionen]** für Ihre Push-Benachrichtigung konfigurieren. Die verfügbaren Parameter sind unten aufgeführt:

| Parameter | Beschreibung |
|---------|---------|
| **[!UICONTROL Reduzierbar]** (iOS/Android) | Eine ausblendbare Nachricht ist eine Nachricht, die durch eine neue Nachricht ersetzt werden kann, wenn sie veraltet ist. Häufig werden ausblendbare Nachrichten verwendet, um eine Mobile App anzuweisen, Daten vom Server zu synchronisieren. Ein Beispiel wäre eine Sport-App, die Benutzer über den aktuellen Spielstand auf dem Laufenden hält. Nur die neueste Nachricht ist relevant. Bei nicht ausblendbaren Nachrichten ist hingegen jede Nachricht wichtig für die Mobile App und muss zugestellt werden. |
| **[!UICONTROL Benutzerdefinierter Benachrichtigungston]**     (iOS/Android) | Der Ton, der beim Empfang der Benachrichtigung vom Mobilgerät wiedergegeben wird. Der Ton muss in der Mobile App verfügbar sein. |
| **[!UICONTROL Badges]**     (iOS/Android) | Mit einem Badge wird die Anzahl der neuen ungelesenen Nachrichten direkt auf dem Mobile-App-Symbol angezeigt. <br/>Der Badge-Wert verschwindet, sobald der Benutzer den neuen Inhalt in der Mobile App öffnet oder liest. Wenn eine Benachrichtigung auf einem Gerät empfangen wird, kann der Badge-Wert für die entsprechende Mobile App aktualisiert oder hinzugefügt werden.<br/>Beispiel: Wenn Sie die Anzahl der ungelesenen Artikel Ihrer Kunden erfassen, können Sie eine Personalisierung anwenden, um für jeden Kunden den entsprechenden Wert für das Badge der ungelesenen Artikel zu senden. Weitere Informationen zur Personalisierung finden Sie in [diesem Abschnitt](personalization/personalize.md). |
| **[!UICONTROL Benachrichtigungsgruppe]** (nur iOS) | Verknüpfen Sie eine Benachrichtigungsgruppe mit der Push-Benachrichtigung.<br/>Ab iOS 12 ermöglichen Benachrichtigungsgruppen die Konsolidierung von Nachrichten-Threads und Benachrichtigungsthemen als Thread-IDs. Dadurch kann eine Marke beispielsweise Marketing-Benachrichtigungen unter einer Gruppen-ID und Benachrichtigungen mit betrieblichen Informationen unter einer oder mehreren anderen IDs senden.<br/>Beispielsweise können Sie folgende Benachrichtigungsgruppen erstellen: groupID: 123 „Die neue Sweatshirt-Frühlungskollektion ist da“ und groupID: 456 „Ihr Paket wurde zugestellt“. Bei diesem Beispiel würden alle Versandbenachrichtigungen unter der Gruppen-ID 456 gebündelt. |
| **[!UICONTROL Benachrichtigungskanal]**     (Nur Android) | Weisen Sie der Push-Benachrichtigung einen Benachrichtigungskanal zu.<br/>Ab Android 8.0 (API-Stufe 26) müssen alle Benachrichtigungen einem Kanal zugewiesen werden, damit sie angezeigt werden. Weiterführende Informationen zu diesem Thema finden Sie in der [Dokumentation für Android-Entwickler](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Hinzufügen einer Markierung für Inhaltsverfügbarkeit]**     (nur iOS) | Wenn der Inhalt verfügbar ist, wird die Markierung für Inhaltsverfügbarkeit in der Push-Payload gesendet. Dies aktiviert die Mobile App sofort beim Empfang der Push-Benachrichtigung, sodass die Mobile App auf die Payload-Daten zugreifen kann.<br/> Dies ist auch dann möglich, wenn die Mobile App im Hintergrund läuft und ohne dass der Benutzer eingreifen muss (z. B. durch Tippen auf die Push-Benachrichtigung). Diese Möglichkeit besteht jedoch nicht, wenn die Mobile App nicht geöffnet ist. Weiterführende Informationen dazu finden Sie in der [Dokumentation für Apple-Entwickler](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Hinzufügen einer Markierung für veränderbaren Inhalt]**     (nur iOS) | Sendet die Markierung für veränderbaren Inhalt als Teil der Push-Payload und ermöglicht die Änderung des Inhalts der Push-Benachrichtigung durch eine im iOS-SDK bereitgestellte Anwendungserweiterung des Benachrichtigungs-Service. Weiterführende Informationen dazu finden Sie in der [Dokumentation für Apple-Entwickler](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Sie können die Erweiterungen Ihrer Mobile App nutzen, um den Inhalt oder die Darstellung eintreffender Push-Benachrichtigungen, die von [!DNL Journey Optimizer] versandt werden, nachträglich zu ändern. Beispielsweise können Benutzer diese Option nutzen, um Daten zu entschlüsseln, den Textkörper oder Titel einer Benachrichtigung zu ändern, eine Thread-Kennung zu einer Benachrichtigung hinzuzufügen usw. |
| **[!UICONTROL Benachrichtigungssichtbarkeit]**     (Nur Android) | Definiert die Sichtbarkeit der Push-Benachrichtigung. <br/><b>Privat</b>: Die Benachrichtigung wird auf allen Sperrbildschirmen angezeigt, vertrauliche oder private Informationen werden jedoch auf gesicherten Sperrbildschirmen ausgeblendet. <br/><b>Public</b>: Die Benachrichtigung wird vollständig auf allen Sperrbildschirmen angezeigt. <br/><b>Secret</b>: Auf einem gesicherten Sperrbildschirm wird kein Teil der Benachrichtigung angezeigt. <br/>Weiterführende Informationen zu diesem Thema finden Sie in der [Dokumentation für Android-Entwickler](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Benachrichtigungspriorität]** (nur Android) | Definiert die Wichtigkeit der Push-Benachrichtigung von „niedrig“ bis „maximal“. Dadurch wird festgelegt, wie „aufdringlich“ die Push-Benachrichtigung bei der Zustellung ist. Weiterführende Informationen zu diesem Thema finden Sie in der [Dokumentation für Android-Entwickler](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance). |
| **[!UICONTROL Versandpriorität]**     (Nur Android) | Weist Ihren Push-Benachrichtigungen eine hohe oder normale Priorität zu. Weiterführende Informationen zur Priorität von Nachrichten finden Sie in der [Dokumentation für Google-Entwickler](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |

**Verwandte Themen**

<!--
* [Understand push notification flow](push-gs.md)
-->

* [Konfigurieren des Push-Kanals](push-gs.md)
* [Erstellen einer neuen Nachricht](create-message.md)
* [Hinzufügen einer Nachricht zu einer Journey](building-journeys/journeys-message.md)
