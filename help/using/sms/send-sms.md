---
solution: Journey Optimizer
product: journey optimizer
title: Textnachrichten überprüfen und testen
description: Erfahren Sie, wie Sie Ihre Textnachrichten in Journey Optimizer überprüfen und senden können.
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 9ac8a3ddad165f728c09baacb9d380d4611fd58a
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 71%

---

# Textnachricht prüfen und senden (SMS/MMS) {#send-sms}

## Vorschau der Textnachricht anzeigen {#preview-sms}

Sobald der Inhalt der Nachricht definiert wurde, können Sie mithilfe von Testprofilen eine Vorschau anzeigen. Wenn Sie personalisierte Inhalte eingefügt haben, können Sie mithilfe von Testprofildaten überprüfen, wie diese Inhalte in der Nachricht angezeigt werden.

Klicken Sie dazu auf **[!UICONTROL Inhalt simulieren]** und fügen Sie dann ein Testprofil hinzu, um Ihre Nachricht mithilfe der Testprofildaten zu überprüfen.

![](assets/sms_preview_2.png)

Detaillierte Informationen zur Auswahl von Testprofilen und zur Vorschau Ihres Inhalts finden Sie im Abschnitt [Content-Management](../content-management/preview-test.md).

## Inhalt validieren {#sms-validate}

Sie müssen die Warnmeldungen im oberen Bereich des Editors überprüfen. Einige davon sind einfache Warnungen, aber andere können Sie daran hindern, die Nachricht zu senden. Es gibt zwei Arten von Warnungen: Warnungen und Fehler.

![](assets/sms-alert-button.png)

* **Warnhinweise** geben Hinweise auf Empfehlungen und zeigen Best Practices. Wenn Ihre Textnachricht beispielsweise leer ist, wird eine Warnmeldung angezeigt.

* **Fehler** hindern Sie daran, die Journey zu testen oder zu aktivieren oder die Kampagne zu veröffentlichen, bis sie behoben sind. Eine Fehlermeldung warnt Sie zum Beispiel, wenn die Betreffzeile fehlt.


>[!NOTE]
>
> Um die Zustellbarkeit zu verbessern, verwenden Sie die Telefonnummern in den vom Anbieter unterstützten Formaten. Beispielsweise unterstützen Twilio und Sinch nur Telefonnummern im E.164-Format.

## Textnachrichten senden {#sms-send}

Wenn Ihre Textnachricht fertig ist, schließen Sie die Konfiguration Ihrer [Journey](../building-journeys/journey-gs.md) oder [Kampagne](../campaigns/create-campaign.md) , um es zu versenden.

**Verwandte Themen**

* [Konfigurieren des SMS-Kanals](sms-configuration.md)
* [SMS/MMS-Berichte](../reports/journey-global-report.md#sms-global)
* [Textnachrichten erstellen](create-sms.md)
* [Eine Nachricht zu einer Journey hinzufügen](../building-journeys/journeys-message.md)
