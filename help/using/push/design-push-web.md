---
solution: Journey Optimizer
product: journey optimizer
title: Gestalten einer Push-Benachrichtigung
description: Erfahren Sie, wie Sie eine Web-Push-Benachrichtigung in Journey Optimizer erstellen
feature: Push
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
source-git-commit: 36056208cd1e435c4801bd178bdc5f2d74068dc5
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 13%

---

# Gestalten einer Web-Push-Benachrichtigung {#design-push-notification}

>[!AVAILABILITY]
>
>Derzeit unterstützen Web-Push-Benachrichtigungen in Journey Optimizer nicht die Funktionen **Stille Benachrichtigung** und **Inhalt simulieren**, sie werden jedoch zu einem späteren Zeitpunkt verfügbar sein.

Nachdem Sie Ihre Web-Push-Benachrichtigungskampagne oder Ihren Journey erstellt haben, können Sie den Inhalt und die Struktur entsprechend Ihren Anforderungen gestalten. Beachten Sie, dass vor dem Senden einer Web-Push-Benachrichtigung dieser Kanal zunächst in Ihrer [Kanalkonfiguration“ konfiguriert ](push-configuration-web.md) muss.

<!--
## Send a silent notification {#silent-notification}

A silent push notification (also called a background notification) is a hidden message sent to your web application without alerting the user.

To enable a silent notification, enable the **[!UICONTROL Silent Notification]** option. When this option is used, the notification is delivered directly to the application, and no alert, banner, or sound is shown to the user.

Use the **Custom Data** section to include additional information in the form of key-value pairs. 

![](assets/web-silent.png)
-->

## Titel und Textkörper {#push-title-body}

Um eine Nachricht zu erstellen, klicken Sie auf die Felder **[!UICONTROL Titel]** und **[!UICONTROL Textkörper]**. Verwenden Sie den Personalisierungseditor, um Inhalte zu definieren[ Daten zu ](../personalization/personalize.md) und [dynamische Inhalte) ](../personalization/get-started-dynamic-content.md).

Klicken Sie **[!UICONTROL Text bearbeiten mit dem KI-]**), um Ihre Inhalte mithilfe des Journey Optimizer-KI-Assistenten einfach zu generieren.

![](assets/web-design-body.png)

## Klickverhalten {#on-click-behavior}

Verwenden Sie das Feld **[!UICONTROL Textkörper-Klickverhalten]** um einen Deep-Link zu definieren, der bestimmt, was passiert, wenn ein Benutzer auf den Benachrichtigungstext klickt. Auf diese Weise können Sie Benutzer direkt an eine bestimmte Seite oder einen bestimmten Abschnitt Ihrer Web-Anwendung senden.

![](assets/web-onclick.png)

## Hinzufügen von Medien {#add-media-push}

Geben Sie die Medien-URL in das Feld **[!UICONTROL Medien hinzufügen]** ein. Sie können auch Personalisierungs-Token in die URL aufnehmen, um den Inhalt für jede Benutzerin und jeden Benutzer anzupassen.

Klicken Sie ![Text mit dem KI-Assistenten bearbeiten](assets/do-not-localize/Smock_ImageAdd_18_N.svg), um mithilfe des Journey Optimizer-KI-Assistenten schnell Medien zu generieren.

![](assets/web-media.png)

## Hinzufügen von Schaltflächen {#add-buttons-push}

Gestalten Sie Ihre Web-Push-Benachrichtigungen interaktiv, indem Sie Ihrem Inhalt Schaltflächen hinzufügen.

Beachten Sie, dass Schaltflächen nur sichtbar sind, wenn das Gerät entsperrt ist. Wenn der Bildschirm gesperrt ist, werden nur **[!UICONTROL Titel]** und **[!UICONTROL Nachricht]** angezeigt.

Verwenden Sie die Option **[!UICONTROL Schaltfläche hinzufügen]**, um die Beschriftung jeder Schaltfläche und die zugehörige Aktion zu definieren, wie unten beschrieben:

* **[!UICONTROL Deeplink]**: Benutzer zu einer bestimmten Ansicht, einem bestimmten Abschnitt oder einer bestimmten Registerkarte in Ihrer App weiterleiten. Geben Sie die Deeplink-URL in das entsprechende Feld ein.

* **[!UICONTROL Web-URL]**: Benutzer zu einer externen Webseite weiterleiten. Fügen Sie die URL in das entsprechende Feld ein.

![](assets/push_buttons.png)

## Benutzerspezifische Daten {#custom-data}

Im Abschnitt **[!UICONTROL Benutzerdefinierte Daten]** können Sie der Benachrichtigungs-Payload benutzerdefinierte Schlüssel-Wert-Paare hinzufügen. Diese Werte können von Ihrer Web-Anwendung verwendet werden, um Trigger-spezifische Aktionen auszuführen oder das Benutzererlebnis anzupassen. Weitere Informationen zum Einrichten von Push-Benachrichtigungen in Adobe Experience Platform finden Sie in [diesem Abschnitt](push-gs.md).

![](assets/web-custom.png)

