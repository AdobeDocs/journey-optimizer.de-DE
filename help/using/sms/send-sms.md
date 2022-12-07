---
solution: Journey Optimizer
product: journey optimizer
title: SMS-Vorschau
description: Erfahren Sie, wie Sie Ihre SMS-Nachricht in Journey Optimizer in der Vorschau anzeigen und testen können.
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 55%

---

# SMS senden {#send-sms}

## SMS-Vorschau {#preview-sms}

Sobald der Inhalt der Nachricht erstellt wurde, können Sie mithilfe von Testprofilen eine Vorschau erstellen und einen Testversand durchführen. Wenn Sie personalisierte Inhalte eingefügt haben, können Sie überprüfen, wie diese Inhalte in der Nachricht angezeigt werden, indem Sie Testprofildaten verwenden.

1. Klicken **[!UICONTROL Inhalt simulieren]**.

1. Klicken **[!UICONTROL Verwalten von Testprofilen]** , um ein Testprofil hinzuzufügen.

1. Suchen Sie Ihr Testprofil mit **[!UICONTROL Identitäts-Namespace]** und **[!UICONTROL Identitätswert]** -Felder. Klicken Sie anschließend auf **[!UICONTROL Profil hinzufügen]**.

   ![](assets/sms_preview_3.png)

1. Nachdem Sie Ihr Testprofil ausgewählt haben, können Sie die **[!UICONTROL Testprofil hinzufügen]** Fenster.

   ![](assets/sms_preview_1.png)

1. Im Fenster Vorschau &amp; Test werden Testprofildaten im Nachrichteninhalt verwendet.

   Beispielsweise sind für diese SMS-Nachricht beide Nachrichteninhalte personalisiert:

   ![](assets/sms_preview_2.png)

## Validieren Ihrer SMS{#sms-preview}

>[!NOTE]
>
> Zur besseren Zustellbarkeit sollte stets die Telefonnummern in den vom Provider unterstützten Formaten verwendet werden. Beispielsweise unterstützen Twilio und Sinch nur Telefonnummern im E.164-Format.

Sie müssen auch Warnhinweise im oberen Bereich des Editors überprüfen.  Einige davon sind einfache Warnhinweise, andere können die Verwendung der Nachricht verhindern. Es können zwei Arten von Warnhinweisen auftreten:

* **Warnhinweise** geben Hinweise auf Empfehlungen und zeigen Best Practices. Beispielsweise wird eine Nachricht angezeigt, wenn Ihre SMS leer ist.

* **Fehler** verhindern, dass Sie die Journey testen oder aktivieren, solange nicht alle Fehler behoben sind. Beispielsweise wird eine Meldung angezeigt, dass die Betreffzeile fehlt.

![](assets/sms-alert-button.png)

Wenn Ihre SMS fertig ist, konfigurieren Sie Ihre [Journey](../building-journeys/journey-gs.md) oder [Kampagne](../campaigns/create-campaign.md) , um es zu versenden.

**Verwandte Themen**

* [Konfigurieren des SMS-Kanals](sms-configuration.md)
* [SMS-Bericht](../reports/journey-global-report.md#sms-global)
* [Erstellen einer SMS-Nachricht](create-sms.md)
* [Hinzufügen einer Nachricht zu einer Journey](../building-journeys/journeys-message.md)
