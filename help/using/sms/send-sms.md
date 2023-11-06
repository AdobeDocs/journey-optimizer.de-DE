---
solution: Journey Optimizer
product: journey optimizer
title: Überprüfen und Testen Ihrer SMS-Nachricht
description: Weitere Informationen dazu, wie Sie Ihre SMS-Nachricht in Journey Optimizer überprüfen und senden können.
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: ht
source-wordcount: '257'
ht-degree: 100%

---

# Überprüfen und Senden Ihrer SMS-Nachricht {#send-sms}

## Vorschau Ihrer SMS {#preview-sms}

Sobald der Inhalt der Nachricht definiert wurde, können Sie mithilfe von Testprofilen eine Vorschau anzeigen. Wenn Sie personalisierte Inhalte eingefügt haben, können Sie mithilfe von Testprofildaten überprüfen, wie diese Inhalte in der Nachricht angezeigt werden.

Klicken Sie dazu auf **[!UICONTROL Inhalt simulieren]** und fügen Sie dann ein Testprofil hinzu, um Ihre Nachricht mithilfe der Testprofildaten zu überprüfen.

![](assets/sms_preview_2.png)

Detaillierte Informationen zur Auswahl von Testprofilen und zur Vorschau Ihres Inhalts finden Sie im Abschnitt [Content-Management](../content-management/preview-test.md).

## Validieren Ihrer SMS{#sms-validate}

Sie müssen die Warnmeldungen im oberen Bereich des Editors überprüfen. Einige davon sind einfache Warnungen, aber andere können Sie daran hindern, die Nachricht zu senden. Es gibt zwei Arten von Warnungen: Warnungen und Fehler.

* **Warnhinweise** geben Hinweise auf Empfehlungen und zeigen Best Practices. So wird beispielsweise eine Warnmeldung angezeigt, wenn Ihre SMS-Nachricht leer ist.

* **Fehler** hindern Sie daran, die Journey zu testen oder zu aktivieren oder die Kampagne zu veröffentlichen, bis sie behoben sind. Eine Fehlermeldung warnt Sie zum Beispiel, wenn die Betreffzeile fehlt.

![](assets/sms-alert-button.png)

>[!NOTE]
>
> Um die Zustellbarkeit zu verbessern, verwenden Sie die Telefonnummern in den vom Anbieter unterstützten Formaten. Beispielsweise unterstützen Twilio und Sinch nur Telefonnummern im E.164-Format.

## Senden Ihrer SMS-Nachricht{#sms-send}

Wenn Ihre SMS-Nachricht fertig ist, konfigurieren Sie Ihre [Journey](../building-journeys/journey-gs.md) oder [Kampagne](../campaigns/create-campaign.md), um sie zu versenden.

**Verwandte Themen**

* [Konfigurieren des SMS-Kanals](sms-configuration.md)
* [SMS-Bericht](../reports/journey-global-report.md#sms-global)
* [Erstellen einer SMS-Nachricht](create-sms.md)
* [Hinzufügen einer Nachricht zu einer Journey](../building-journeys/journeys-message.md)
