---
solution: Journey Optimizer
product: journey optimizer
title: Mobile-Nachrichten überprüfen und testen
description: Erfahren Sie, wie Sie Ihre Mobile-Nachrichten in Journey Optimizer überprüfen und senden
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
TQID: https://experienceleague.adobe.com/JPjBxyZzo13tgSLo0dqd5bFOwn9C6MHkA-DjLzlAdEI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c41e8697-e629-4c38-96b3-564faaa17acf
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 537
ht-degree: 63%

---

# Mobiltelefon-Nachricht überprüfen und senden {#send-sms}

## Mobile-Nachricht in der Vorschau anzeigen {#preview-sms}

Sobald der Nachrichteninhalt definiert wurde, können Sie mithilfe von Testprofilen oder Beispieleingabedaten (aus einer CSV- oder JSON-Datei hochgeladen oder manuell hinzugefügt) eine Vorschau des Inhalts anzeigen. Wenn Sie personalisierte Inhalte eingefügt haben, können Sie überprüfen, wie diese Inhalte in der Nachricht angezeigt werden.

Klicken Sie dazu auf **[!UICONTROL Inhalt simulieren]** und überprüfen Sie dann die Nachricht mithilfe der Testprofildaten.

![](assets/sms_preview_2.png)

Detaillierte Informationen zur Vorschau und zum Test des Inhalts finden Sie im Abschnitt [Content-Management](../content-management/preview-test.md).

### Zeichenkodierung und Beschränkungen {#sms-character-limits}

Beim Zugriff auf das Menü **[!UICONTROL Inhalt simulieren]** wird eine Zeichenanzahl angezeigt, um die Planung und Verwaltung Ihrer Mobile-Nachrichten zu unterstützen.

![](assets/sms_preview_3.png)

Journey Optimizer verwendet UTF-8-Kodierung im SMS-Editor, sodass Sie Doppel-Byte- oder Unicode-Zeichen eingeben oder einfügen können. Diese Zeichen werden dann zum Versand an den Dienstleister übermittelt. Die meisten SMS-Anbieter verwenden für Standardnachrichten eine GSM-7-Bit-Kodierung mit einer Beschränkung auf 160 Zeichen und wechseln zu UTF-16 (UCS-2), wenn Nicht-GSM-Zeichen erkannt werden. Dann gilt eine Beschränkung auf 70 Zeichen.

Beachten Sie, dass die Zeichenanzahl keine Varianten widerspiegelt, die durch dynamische Personalisierung oder Nicht-GSM-7-Bit-Sonderzeichen eingeführt wurden.

>[!IMPORTANT]
>
>Das Reporting zum Journey Optimizer-SMS-Versand berücksichtigt keine verketteten Nachrichten oder dynamische Personalisierung. Daher spiegelt es möglicherweise nicht die tatsächliche Anzahl der vom Anbieter gesendeten Nachrichten wider. Detaillierte Informationen zu Nutzung und Abrechnung erhalten Sie vom Adobe-Support.
>
>Best Practices zur Minimierung von hohen SMS-Rechnungen finden Sie unter [Best Practices für SMS zur Zeichenoptimierung](mobile-cost-optimization.md).

## Validieren Ihres Inhalts {#sms-validate}

>[!NOTE]
>
> Um die Zustellbarkeit zu verbessern, verwenden Sie die Telefonnummern in den vom Anbieter unterstützten Formaten. Beispielsweise unterstützen Twilio und Sinch nur Telefonnummern im E.164-Format.

Sie müssen die Warnmeldungen im oberen Bereich des Editors überprüfen. Einige davon sind einfache Warnungen, aber andere können Sie daran hindern, die Nachricht zu senden. Es gibt zwei Arten von Warnungen: Warnungen und Fehler.

![](assets/sms-alert-button.png)

* **Warnhinweise** geben Hinweise auf Empfehlungen und zeigen Best Practices. Beispielsweise wird eine Warnmeldung angezeigt, wenn Ihre Mobile-Nachricht leer ist oder wenn Zeichenbeschränkungen bei dynamischen Inhalten überschritten werden können.

  **Zeichenbeschränkungen:** 160 Zeichen pro Segment (GSM 7-Bit), 70 Zeichen für Unicode/Emojis, bis zu 1500 Zeichen insgesamt.

* **Fehler** hindern Sie daran, die Journey zu testen oder zu aktivieren oder die Kampagne zu veröffentlichen, bis sie behoben sind. Eine Fehlermeldung warnt Sie zum Beispiel, wenn die Betreffzeile fehlt.

Der Warnhinweis **Die maximale Zeichenanzahl für SMS-Text wurde überschritten“** kann auch dann angezeigt werden, wenn Ihre simulierte Nachricht kürzer ist, da die Validierung die **maximal mögliche Länge)** berechnet, indem alle bedingten Verzweigungen, Personalisierungsfelder und dynamischen Inhalte am längsten ausgewertet werden.

Bei der Validierung wird die maximale Länge für alle möglichen Profildaten berechnet, während bei der Simulation die tatsächliche Ausgabe für ein Testprofil angezeigt wird.

## Mobiltelefon-Nachrichten senden {#sms-send}

>[!IMPORTANT]
>
> Wenn für Ihre Kampagne eine Validierungsrichtlinie gilt, müssen Sie eine Validierung anfordern, um Ihre Mobile-Nachrichten senden zu können. [Weitere Informationen](../test-approve/gs-approval.md)

Wenn Ihre Mobile-Nachricht fertig ist, konfigurieren Sie Ihre [Journey](../building-journeys/journey-gs.md) oder [Kampagne](../campaigns/create-campaign.md), um sie zu versenden.

**Verwandte Themen**

* [Konfigurieren des SMS-Kanals](mobile-configuration.md)
* [SMS-/RCS-/MMS-Berichte](../reports/journey-global-report-cja-sms.md)
* [Erstellen einer Mobile-Nachricht](create-mobile-message.md)
* [Hinzufügen einer Nachricht zu einer Journey](../building-journeys/journey-action.md)
