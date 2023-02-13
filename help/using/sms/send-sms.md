---
solution: Journey Optimizer
product: journey optimizer
title: SMS-Vorschau erstellen und testen
description: Erfahren Sie, wie Sie eine Vorschau Ihrer SMS-Nachricht in Journey Optimizer anzeigen und einen Testversand durchführen.
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 53%

---

# SMS-Vorschau erstellen und testen {#send-sms}

## SMS-Vorschau {#preview-sms}

Sobald der Inhalt der Nachricht erstellt wurde, können Sie mithilfe von Testprofilen eine Vorschau erstellen und einen Testversand durchführen. Wenn Sie personalisierten Inhalt eingefügt haben, können Sie mithilfe von Testprofildaten überprüfen, wie dieser Inhalt in der Nachricht angezeigt wird.

1. Klicken Sie auf **[!UICONTROL Inhalt simulieren]**.

1. Klicken Sie auf **[!UICONTROL Testprofile verwalten]**, um ein Testprofil hinzuzufügen.

1. Suchen Sie Ihr Testprofil mit den Feldern **[!UICONTROL Identity-Namespace]** und **[!UICONTROL Identitätswert]**. Klicken Sie anschließend auf **[!UICONTROL Profil hinzufügen]**.

   ![](assets/sms_preview_3.png)

1. Nachdem Sie Ihr Testprofil ausgewählt haben, können Sie das Fenster **[!UICONTROL Testprofil hinzufügen]** schließen.

1. Aus dem **Vorschau und Test** -Fenster werden dem Nachrichteninhalt Testprofildaten hinzugefügt.

   ![](assets/sms_preview_2.png)


## Validieren Ihrer SMS{#sms-validate}

Warnhinweise müssen im oberen Abschnitt des Editors überprüft werden. Bei einigen handelt es sich um einfache Warnungen, bei anderen können Sie jedoch den Versand der Nachricht verhindern. Es können zwei Arten von Warnhinweisen auftreten: Warnungen und Fehler.

* **Warnhinweise** geben Hinweise auf Empfehlungen und zeigen Best Practices. Beispielsweise wird eine Warnmeldung angezeigt, wenn Ihre SMS leer ist.

* **Fehler** verhindern, dass Sie die Journey testen oder aktivieren oder die Kampagne veröffentlichen, solange sie nicht aufgelöst ist. Beispielsweise werden Sie in einer Fehlermeldung gewarnt, wenn die Betreffzeile fehlt.

![](assets/sms-alert-button.png)

>[!NOTE]
>
> Verwenden Sie zur Verbesserung Ihrer Zustellbarkeit die Telefonnummern in den vom Provider unterstützten Formaten. Beispielsweise unterstützen Twilio und Sinch nur Telefonnummern im E.164-Format.

## SMS senden{#sms-send}

Wenn Ihre SMS-Nachricht fertig ist, konfigurieren Sie Ihre [Journey](../building-journeys/journey-gs.md) oder [Kampagne](../campaigns/create-campaign.md), um sie zu versenden.

**Verwandte Themen**

* [Konfigurieren des SMS-Kanals](sms-configuration.md)
* [SMS-Bericht](../reports/journey-global-report.md#sms-global)
* [Erstellen einer SMS-Nachricht](create-sms.md)
* [Hinzufügen einer Nachricht zu einer Journey](../building-journeys/journeys-message.md)
