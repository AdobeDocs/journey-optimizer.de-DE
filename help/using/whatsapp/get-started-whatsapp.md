---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit WhatsApp-Nachrichten
description: Erfahren Sie, wie Sie in Journey Optimizer WhatsApp-Nachrichten erstellen und versenden
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 22df2bfa-4d86-464e-ad83-3aa457e3a747
source-git-commit: 7f507dc0113e85191429c2c48b873112b590e3ce
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 55%

---

# Erste Schritte mit WhatsApp-Nachrichten {#get-started-whatsapp}

>[!BEGINSHADEBOX]

**Inhaltsverzeichnis**

* **[Erste Schritte mit WhatsApp-Nachrichten](get-started-whatsapp.md)**
* [Erste Schritte bei der WhatsApp-Konfiguration](whatsapp-configuration.md)
* [Erstellen einer WhatsApp-Nachricht](create-whatsapp.md)
* [Überprüfen und Senden Ihrer WhatsApp-Nachrichten](send-whatsapp.md)

>[!ENDSHADEBOX]

Sie können jetzt WhatsApp-Nachrichten direkt über Journey Optimizer über die [Cloud-API](https://developers.facebook.com/docs/whatsapp/cloud-api/) von Meta senden. Diese Funktion ermöglicht die nahtlose Integration von WhatsApp in Journey und Kampagnen und verbessert die Kommunikation und Interaktion mit den Empfängerinnen und Empfängern.

* In einer **Journey**.  Erstellen Sie eine Journey, fügen Sie eine **WhatsApp**-Aktivität hinzu und legen Sie die Grundeinstellungen fest. Wechseln Sie dann in den rechten Bereich **[!UICONTROL Aktionen: WhatsApp]**, um den Inhalt für die WhatsApp-Nachricht zu erstellen. Weitere Informationen zum Erstellen einer Journey finden Sie auf [dieser Seite](../building-journeys/journey-gs.md).

* In einer **Kampagne**. Erstellen Sie eine Kampagne, wählen Sie **WhatsApp** als Aktion aus und legen Sie die Grundeinstellungen fest. Bearbeiten Sie dann den Nachrichteninhalt, um die zu versendende WhatsApp-Nachricht zu erstellen. Weitere Informationen zum Erstellen einer Kampagne finden Sie auf [dieser Seite](../campaigns/create-campaign.md#configure).

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## Voraussetzungen {#prereq}

Die Integration von WhatsApp mit Journey Optimizer erfordert Folgendes:

* Meta Business Manager-Konto
* WhatsApp Business-Konto
* WhatsApp-Telefonnummer
* [Benutzerautorisierungs-Token mit entsprechenden Berechtigungen](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [Genehmigte Meta-Vorlagen](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)
* [Konfiguration von Meta-Webhooks](https://developers.facebook.com/docs/whatsapp/webhooks/)


Sie müssen außerdem Folgendes bestätigen, bevor Sie mit der Integration fortfahren:

* [WhatsApp-Inhaltsregeln](https://www.whatsapp.com/legal/messaging-guidelines)
* [Einhaltung von Meta-Richtlinien](https://www.whatsapp.com/legal)
* [24-Stunden-Konversations-Limit](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## Einschränkungen {#limitations}

Die folgenden Einschränkungen gelten für den WhatsApp-Kanal:

* Der WhatsApp-Kanal in Adobe Journey Optimizer ist HIPAA-fähig, aber Drittanbieter werden von Adobes BAA nicht abgedeckt. Kunden sind für ihre eigene Compliance und Anbietervalidierung verantwortlich.

* Beachten Sie, dass automatisierte oder vordefinierte Antwortnachrichten nicht unterstützt werden.

* Seit April 2025 ist der Versand aller Nachrichten aus Marketing-Vorlagen an WhatsApp-Benutzer, die eine US-Telefonnummer haben (eine Nummer bestehend aus einer +1-Wählnummer und einer US-Vorwahlnummer), vorübergehend ausgesetzt. [Weitere Informationen finden Sie in der Meta-Dokumentation](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* Die native Integrationsfunktion ermöglicht keine Integration mit einem Business Service Provider (BSP) eines Drittanbieters.

## Anleitungsvideo {#video}


Das folgende Video zeigt, wie eine Journey mit einer WhatsApp-Aktion erstellt wird.

+++ Siehe Video

>[!VIDEO](https://video.tv.adobe.com/v/3451621?learn=on)

+++
