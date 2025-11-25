---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit Kampagnen, die durch API ausgelöst werden
description: Informationen zum Auslösen von Kampagnen mit Journey Optimizer-APIs.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: Kampagnen, API-ausgelöst, REST, Optimizer, Nachrichten
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 81e54a3e3428d58818805b5dcb397ede4039436a
workflow-type: ht
source-wordcount: '271'
ht-degree: 100%

---


# Arbeiten mit Kampagnen, die durch API ausgelöst werden {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="Kampagnen, die durch API ausgelöst werden"
>abstract="**Transaktionskampagnen, die durch API ausgelöst werden**<br/> Lösen Sie Echtzeit-Nachrichten über API-Aufrufe aus <br/><br/>**Marketing-Nachrichten**<br/> Werbeinhalte (erfordert Opt-in, unterliegt Geschäftsregeln)<br/><br/>**Transaktionsnachrichten**<br/> Service-bezogene Inhalte (Bestätigung, Warnhinweise, nicht der Zustimmung zum Marketing unterliegend)<br/><br/>**Verfügbare Kanäle**<br/> E-Mail, SMS, Push-Benachrichtigung"

## Informationen zu Kampagnen, die durch API ausgelöst werden {#about}

Durch API ausgelöste Kampagnen ermöglichen den Versand von Marketing-Nachrichten an eine Zielgruppe zum richtigen Zeitpunkt oder den Versand von Transaktions-/Betriebsnachrichten an einen Kontakt, z. B. zum Zurücksetzen des Passworts. Dabei kann eine Personalisierung erforderlich sein, bei der nicht nur Profilattribute, sondern auch Echtzeit-Kontextdaten im Trigger verwendet werden, der eine REST-API-Payload ist.

Dazu müssen Sie zunächst in Journey Optimizer eine durch API ausgelöste Kampagne erstellen und deren Ausführung dann über einen API-Aufruf starten, der die [REST-API zur Ausführung interaktiver Nachrichten](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution) verwendet.

➡️ [Funktion im Video kennenlernen](#video)

>[!NOTE]
>
>Weitere Informationen zu den unterstützten Kanälen finden Sie in der Tabelle in diesem Abschnitt: [Kanäle in Journeys und Kampagnen](../channels/gs-channels.md#channels).
>
>Die verfügbaren Kanäle variieren je nach Ihrem Lizenzierungsmodell und Ihren Add-ons.

## Wichtige Schritte beim Erstellen von Kampagnen, die durch API ausgelöst werden {#steps}

Bevor Sie mit Kampagnen beginnen, überprüfen Sie [in diesem Abschnitt](get-started-with-campaigns.md#prerequisites) die folgenden Voraussetzungen. Sobald diese Voraussetzungen erfüllt sind, können Sie mit der Erstellung Ihrer Kampagne beginnen:

1. [Definieren der Kampagneneigenschaften](api-triggered-campaign-properties.md)
1. [Konfigurieren der Kampagnenaktion](api-triggered-campaign-action.md)
1. [Bearbeiten des Kampagneninhalts](api-triggered-campaign-content.md)
1. [Definieren der Zielgruppe einer Kampagne](api-triggered-campaign-audience.md)
1. [Planen der Kampagne](api-triggered-campaign-schedule.md)
1. [Prüfen und Aktivieren der Kampagne](review-activate-api-triggered-campaign.md)
1. [Auslösen der Kampagnenausführung](trigger-campaigns.md)

## Anleitungsvideos {#video}

Erfahren Sie, wie Sie eine Kampagne erstellen und sie von einem externen System aus basierend auf Benutzerinteraktionen auslösen, indem Sie das REST-API zur Ausführung interaktiver Nachrichten verwenden.

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)
