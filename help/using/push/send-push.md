---
solution: Journey Optimizer
product: journey optimizer
title: Vorschau erstellen und Push-Benachrichtigung testen
description: Erfahren Sie, wie Sie Ihre Push-Benachrichtigung in Journey Optimizer in der Vorschau anzeigen und testen können.
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 77%

---

# Vorschau erstellen und Push-Benachrichtigung testen {#send-push}

## Vorschau der Push-Benachrichtigung {#preview-push}

Sobald der Inhalt der Nachricht erstellt wurde, können Sie mithilfe von Testprofilen eine Vorschau erstellen und einen Testversand durchführen. Wenn Sie personalisierten Inhalt eingefügt haben, können Sie mithilfe von Testprofildaten überprüfen, wie dieser Inhalt in der Nachricht angezeigt wird.

1. Klicken Sie auf **[!UICONTROL Inhalt simulieren]**.

1. Klicken Sie auf **[!UICONTROL Testprofile verwalten]**, um ein Testprofil hinzuzufügen.

1. Suchen Sie Ihr Testprofil mit den Feldern **[!UICONTROL Identity-Namespace]** und **[!UICONTROL Identitätswert]**. Klicken Sie anschließend auf **[!UICONTROL Profil hinzufügen]**.

   ![](assets/push_preview_1.png)

1. Nachdem Sie Ihr Testprofil ausgewählt haben, können Sie das Fenster **[!UICONTROL Testprofil hinzufügen]** schließen.

1. Aus dem **Vorschau und Test** -Fenster werden dem Nachrichteninhalt Testprofildaten hinzugefügt.

   Wählen Sie den Gerätetyp aus, um Inhalte in der Vorschau anzuzeigen: **[!UICONTROL iOS]** oder **[!UICONTROL Android]**.

   ![](assets/push_preview_3.png)

## Validieren der Push-Benachrichtigung {#push-validate}


Warnhinweise müssen im oberen Abschnitt des Editors überprüft werden. Bei einigen handelt es sich um einfache Warnungen, bei anderen können Sie jedoch den Versand der Nachricht verhindern. Es können zwei Arten von Warnhinweisen auftreten: Warnungen und Fehler.

* **Warnhinweise** geben Hinweise auf Empfehlungen und zeigen Best Practices.

* **Fehler** verhindern, dass Sie die Journey testen oder aktivieren, solange nicht alle Fehler behoben sind.

   * **[!UICONTROL Die Push-Version der Nachricht ist leer]**: Dieser Fehler wird angezeigt, wenn der Text oder Titel der Push-Benachrichtigung fehlt. In [diesem Abschnitt](create-push.md) erfahren Sie, wie Sie den Inhalt einer Push-Benachrichtigung definieren.

   * **[!UICONTROL Oberfläche ist nicht vorhanden]**: Sie können Ihre Nachricht nicht veröffentlichen, wenn die gewählte Oberfläche nach der Erstellung der Nachricht gelöscht wurde. Wenn dieser Fehler auftritt, wählen Sie in den **[!UICONTROL Eigenschaften]** der Nachricht eine andere Oberfläche aus. Weitere Informationen zu Kanaloberflächen finden Sie in [diesem Abschnitt](../configuration/channel-surfaces.md).

   * **[!UICONTROL Die Payload für Push-Benachrichtigungen an iOS-/Android überschreitet die Beschränkung von 4 KB]**: Die Größe der Push-Benachrichtigung darf 4 KB nicht überschreiten. Um diese Grenze zu beachten, versuchen Sie, die Verwendung von Bildern oder Emojis zu reduzieren. In [diesem Abschnitt](../push/create-push.md) erfahren Sie, wie Sie Ihre Push-Benachrichtigungsinhalte verwalten.

   ![](assets/push_alert.png)


>[!NOTE]
>
> Zur besseren Zustellbarkeit sollte stets die Telefonnummern in den vom Provider unterstützten Formaten verwendet werden. Beispielsweise unterstützen Twilio und Sinch nur Telefonnummern im E.164-Format.

## Senden der Push-Benachrichtigung{#push-send}

Wenn Ihre Push-Nachricht fertig ist, konfigurieren Sie Ihre [Journey](../building-journeys/journey-gs.md) oder [Kampagne](../campaigns/create-campaign.md) , um es zu versenden.

**Verwandte Themen**

* [Konfigurieren des Push-Kanals](push-configuration.md)
* [Bericht zu Push-Benachrichtigungen](../reports/journey-global-report.md#push-global)
* [Erstellen einer Push-Benachrichtigung](create-push.md)
* [Hinzufügen einer Nachricht zu einer Journey](../building-journeys/journeys-message.md)
* [Hinzufügen einer Nachricht in einer Kampagne](../campaigns/create-campaign.md)

