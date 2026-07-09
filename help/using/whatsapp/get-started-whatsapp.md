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
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b8df23d2-98a2-4406-86cc-2babe8728d36
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 686
ht-degree: 65%

---

# Erste Schritte mit WhatsApp-Nachrichten {#get-started-whatsapp}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie der WhatsApp-Kanal in Journey Optimizer funktioniert und welche Voraussetzungen und Einschränkungen er aufweist, damit Sie entscheiden können, wie Sie Ihren Journeys und Kampagnen WhatsApp hinzufügen.

>[!ENDSHADEBOX]

Sie können jetzt direkt in Journey Optimizer WhatsApp-Nachrichten über das [Cloud-API](https://developers.facebook.com/docs/whatsapp/cloud-api/) von Meta senden. Diese Funktion ermöglicht die nahtlose Integration von WhatsApp in Journeys und Kampagnen und verbessert die Kommunikation und Interaktion mit Empfängerinnen und Empfängern.

* In einer **Journey**. Erstellen Sie eine Journey, fügen Sie eine **WhatsApp**-Aktivität hinzu und legen Sie die Grundeinstellungen fest. Wechseln Sie dann in den rechten Bereich **[!UICONTROL Aktionen: WhatsApp]**, um den Inhalt für die WhatsApp-Nachricht zu erstellen. Weitere Informationen zum Erstellen einer Journey finden Sie auf [dieser Seite](../building-journeys/journey-gs.md).

* In einer **Kampagne**. Erstellen Sie eine Kampagne, wählen Sie **WhatsApp** als Aktion aus und legen Sie die Grundeinstellungen fest. Bearbeiten Sie dann den Nachrichteninhalt, um die zu versendende WhatsApp-Nachricht zu erstellen. Erfahren Sie, wie Sie [eine Aktionskampagne](../campaigns/campaign-action.md#action-campaign-action) | [eine durch API ausgelöste Kampagne](../campaigns/api-triggered-campaigns.md) | [eine orchestrierte Kampagne](../orchestrated/create-orchestrated-campaign.md#create) erstellen können

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## Anwendungsszenarien {#use-cases}

WhatsApp funktioniert am besten, wenn Ihre Zielgruppe bereits die Plattform verwendet und Sie Rich-Content mit einer echten Zwei-Wege-Konversation kombinieren möchten.

| Vorteil | Warum | Beispielhafte Anwendungsfälle |
| --- | --- | --- |
| Hohes globales Engagement | Häufig verwendete Messaging-Plattform mit starker Akzeptanz in vielen Regionen | Internationale Zielgruppen erreichen, die bereits auf WhatsApp aktiv sind |
| Reichhaltige, interaktive Nachrichten | Unterstützt Bilder, Videos, Schaltflächen und schnelle Antworten | Produktkataloge, Terminbestätigungen mit Schnellantwortoptionen |
| Zwei-Wege-Gesprächserlebnisse | Empfänger können im selben Thread antworten | Kundensupport-Gespräche, Fragen zur Bestellverfolgung |
| Compliance und Vertrauen über offizielle API | Wird über die verifizierte Cloud-API von Meta mit Absenderverifizierung bereitgestellt | Markenverifizierte Kommunikation, die das Vertrauen der Empfänger stärkt |
| Integration mit anderen Kanälen | Ebenenweise können Journey und Kampagnen neben anderen Kanälen verwendet werden | Multi-Channel-Journey, die WhatsApp als ergänzenden Touchpoint verwenden |

## Verwendung {#when-not-to-use}

WhatsApp hängt von der Akzeptanz der Zielgruppe und der expliziten Zustimmung ab, daher ist es nicht für jedes Szenario geeignet. Betrachten Sie in den folgenden Situationen einen anderen Kanal:

* Ihre Zielgruppe verwendet WhatsApp nicht, da die Akzeptanz je nach Region und Demografie stark variiert
* Die Empfängerinnen und Empfänger haben kein explizites Opt-in angegeben, was für die Messaging-Richtlinien von Meta erforderlich ist
* Die Nachricht ist dringend und benötigt einen garantierten Versand, den SMS oder Push angesichts der Beschränkungen für die Versand- und Vorlagenüberprüfung von WhatsApp besser handhabt
* Der Inhalt ist lang oder komplex und besser für E-Mails geeignet, was mehr Platz und eine umfassendere Formatierung bietet
* Die Unterstützung von Gesprächen in Echtzeit ist auf Ihrer Seite nicht möglich, da bidirektionale WhatsApp-Threads die Erwartung einer zeitnahen Antwort wecken

## Voraussetzungen {#prereq}

Die Integration von WhatsApp mit Journey Optimizer erfordert Folgendes:

* Meta Business Manager-Konto
* [WhatsApp-Unternehmenskonto mit verifiziertem Absendernamen und Telefonnummer](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [Benutzerautorisierungs-Token mit entsprechenden Berechtigungen](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [Genehmigte Meta-Vorlagen](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

Sie müssen außerdem Folgendes bestätigen, bevor Sie mit der Integration fortfahren:

* [WhatsApp-Inhaltsregeln](https://www.whatsapp.com/legal/messaging-guidelines)
* [Konformität mit Meta-Richtlinien](https://www.whatsapp.com/legal)
* [24-Stunden-Konversations-Limits](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

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

