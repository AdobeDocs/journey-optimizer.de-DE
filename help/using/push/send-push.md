---
solution: Journey Optimizer
product: journey optimizer
title: Push-Benachrichtigung senden
description: Erfahren Sie, wie Sie Ihre Push-Benachrichtigung in Journey Optimizer in der Vorschau anzeigen und testen können.
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Push-Benachrichtigung senden {#send-push}

## Push-Benachrichtigung in der Vorschau anzeigen {#preview-push}

Sobald der Nachrichteninhalt definiert wurde, können Sie mithilfe von Testprofilen die Vorschau anzeigen und testen. Wenn Sie personalisierten Inhalt eingefügt haben, können Sie mithilfe von Testprofildaten prüfen, wie dieser Inhalt in der Nachricht dargestellt wird.

1. Klicken **[!UICONTROL Simulate content]**.

1. Klicken **[!UICONTROL Manage test profiles]** , um ein Testprofil hinzuzufügen.

1. Suchen Sie Ihr Testprofil mit dem **[!UICONTROL Identity namespace]** und **[!UICONTROL Identity value]** -Felder. Klicken Sie anschließend auf **[!UICONTROL Add profile]**.

   ![](assets/push_preview_1.png)

1. Wenden Sie dieselben Schritte wie oben beschrieben an, um ein Testprofil auszuwählen, und

   ![](assets/push_preview_2.png)

1. In der Push-Vorschau werden im Nachrichteninhalt Testprofildaten verwendet.

   Wählen Sie den Gerätetyp aus, um Inhalte in der Vorschau anzuzeigen: **[!UICONTROL iOS]** oder **[!UICONTROL Android]**.

   ![](assets/push_preview_3.png)

## Push-Benachrichtigung validieren {#push-validate}

>[!NOTE]
>
> Für eine bessere Zustellbarkeit sollten Sie stets die Telefonnummern in den vom Provider unterstützten Formaten verwenden. Beispielsweise unterstützen Twilio und Sinch nur Telefonnummern im E.164-Format.

Sie müssen Warnhinweise auch im oberen Bereich des Editors überprüfen.  Bei einigen handelt es sich um einfache Warnungen, andere können Sie jedoch daran hindern, die Nachricht zu verwenden. Es können zwei Arten von Warnhinweisen auftreten:

* **Warnungen** Siehe Empfehlungen und Best Practices.

* **Fehler** verhindern, dass Sie die Journey testen oder aktivieren, solange sie nicht aufgelöst ist, z. B.:

   * **[!UICONTROL The push version of the message is empty]**: Dieser Fehler wird angezeigt, wenn der Text oder Titel der Push-Benachrichtigung fehlt. Erfahren Sie, wie Sie den Inhalt von Push-Benachrichtigungen in [diesem Abschnitt](create-push.md).

   * **[!UICONTROL Surface doesn't exist]**: Sie können Ihre Nachricht nicht verwenden, wenn die ausgewählte Oberfläche nach der Nachrichtenerstellung gelöscht wird. Wenn dieser Fehler auftritt, wählen Sie eine andere Stelle in der Nachricht aus **[!UICONTROL Properties]**. Weitere Informationen zu Kanaloberflächen in [diesem Abschnitt](../configuration/channel-surfaces.md).

   * **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**: Die Größe der Push-Benachrichtigung darf 4 KB nicht überschreiten. Um diese Beschränkung einzuhalten, versuchen Sie, die Verwendung von Bildern oder Emojis zu reduzieren. Erfahren Sie, wie Sie Ihren Push-Benachrichtigungs-Inhalt in [diesem Abschnitt](../push/create-push.md).

![](assets/push_alert.png)

Wenn Ihre Push-Benachrichtigung fertig ist, schließen Sie die Konfiguration Ihrer [Journey](../building-journeys/journey-gs.md) oder [Kampagne](../campaigns/create-campaign.md) , um es zu versenden.
