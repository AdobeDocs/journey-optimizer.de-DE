---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit WhatsApp-Nachrichten
description: Erfahren Sie, wie Sie in Journey Optimizer WhatsApp-Nachrichten erstellen und versenden
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 22df2bfa-4d86-464e-ad83-3aa457e3a747
TQID: https://experienceleague.adobe.com/uHzRC9X6rB9EXH4gIFiRxFaeNcrTD0-40RrxZkN4XFg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b8df23d2-98a2-4406-86cc-2babe8728d36id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 409
ht-degree: 94%

---

# Erste Schritte mit WhatsApp-Nachrichten {#get-started-whatsapp}

Sie können jetzt direkt in Journey Optimizer WhatsApp-Nachrichten über das [Cloud-API](https://developers.facebook.com/docs/whatsapp/cloud-api/) von Meta senden. Diese Funktion ermöglicht die nahtlose Integration von WhatsApp in Journeys und Kampagnen und verbessert die Kommunikation und Interaktion mit Empfängerinnen und Empfängern.

* In einer **Journey**. Erstellen Sie eine Journey, fügen Sie eine **WhatsApp**-Aktivität hinzu und legen Sie die Grundeinstellungen fest. Wechseln Sie dann in den rechten Bereich **[!UICONTROL Aktionen: WhatsApp]**, um den Inhalt für die WhatsApp-Nachricht zu erstellen. Weitere Informationen zum Erstellen einer Journey finden Sie auf [dieser Seite](../building-journeys/journey-gs.md).

* In einer **Kampagne**. Erstellen Sie eine Kampagne, wählen Sie **WhatsApp** als Aktion aus und legen Sie die Grundeinstellungen fest. Bearbeiten Sie dann den Nachrichteninhalt, um die zu versendende WhatsApp-Nachricht zu erstellen. Erfahren Sie, wie Sie [eine Aktionskampagne](../campaigns/campaign-action.md#action-campaign-action) | [eine durch API ausgelöste Kampagne](../campaigns/api-triggered-campaigns.md) | [eine orchestrierte Kampagne](../orchestrated/create-orchestrated-campaign.md#create) erstellen können

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## Voraussetzungen {#prereq}

Die Integration von WhatsApp mit Journey Optimizer erfordert Folgendes:

* Meta Business Manager-Konto
* [WhatsApp Business-Konto mit verifiziertem Absendernamen und Telefonnummer](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [Benutzerautorisierungs-Token mit entsprechenden Berechtigungen](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [Genehmigte Meta-Vorlagen](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

Sie müssen außerdem Folgendes bestätigen, bevor Sie mit der Integration fortfahren:

* [WhatsApp-Inhaltsregeln](https://www.whatsapp.com/legal/messaging-guidelines)
* [Einhaltung der Meta-Richtlinien](https://www.whatsapp.com/legal)
* [24-Stunden-Gesprächsbeschränkungen](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## Einschränkungen {#limitations}

Für den WhatsApp-Kanal gelten die folgenden Einschränkungen:

* Der WhatsApp-Kanal in Adobe Journey Optimizer ist HIPAA-fähig, aber Drittanbieter werden durch die BAA von Adobe nicht abgedeckt. Kundinnen und Kunden sind für ihre Compliance und Anbietervalidierung selbst verantwortlich.

* Beachten Sie, dass automatisierte oder vordefinierte Antwortnachrichten noch nicht unterstützt werden.

* Seit April 2025 ist der Versand aller Nachrichten aus Marketing-Vorlagen an WhatsApp-Benutzende, die eine US-Telefonnummer haben (eine Nummer bestehend aus einer +1-Landesvorwahl und einer US-Vorwahlnummer), vorübergehend ausgesetzt. [Weitere Informationen in der Meta-Dokumentation](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* Die native Integrationsfunktion ermöglicht keine Integration mit einem Business Service Provider (BSP) eines Drittanbieters.

## Anleitungsvideo {#video}

Das folgende Video zeigt, wie Sie WhatsApp als nativen Kanal in Adobe Journey Optimizer integrieren, um sichere, personalisierte Echtzeit-Nachrichten im benötigten Umfang bereitzustellen.

+++ Video ansehen

>[!VIDEO](https://video.tv.adobe.com/v/3470244?learn=on)

+++

## Zusätzliche Lernressourcen

Sehen Sie sich weitere Video-Tutorials zu WhatsApp-Messaging und -Konfigurationen an.

➡️ [Tutorials zum WhatsApp-Kanal](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/channels/whatsapp/whatsapp-introduction){target="_blank"}

