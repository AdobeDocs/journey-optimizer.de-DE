---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit API-ausgelösten Kampagnen
description: Erfahren Sie, wie Sie mit Journey Optimizer-APIs Trigger erstellen können.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: Kampagnen, API-ausgelöst, REST, Optimizer, Nachrichten
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 15f5fdfde0e9f7c93739a624918838dbd6787833
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 25%

---


# Arbeiten mit API-ausgelösten Kampagnen {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="API-ausgelöste Kampagnen"
>abstract="**Von der Transaktions-API ausgelöste Kampagnen**<br/> Echtzeit-Nachrichten von Triggern über API-Aufrufe <br/><br/>**Marketing-Nachrichten**<br/> Werbeinhalte (erfordert Opt-in, unterliegt Geschäftsregeln)<br/><br/>**Transaktionsnachrichten**<br/> Service-bezogene Inhalte (Bestätigung, Warnhinweise, nicht vorbehaltlich der Marketing-Zustimmung)<br/><br/>**Verfügbare Kanäle**<br/> E-Mail, SMS, Push-Benachrichtigungen"

## Über API-ausgelöste Kampagnen {#about}

API-ausgelöste Kampagnen ermöglichen es, dass Marketing-Nachrichten eine Zielgruppe zum richtigen Zeitpunkt ansprechen oder dass Transaktions-/Betriebsnachrichten an einen Kontakt gerichtet werden, z. B. zum Zurücksetzen des Kennworts. Dabei kann eine Personalisierung erforderlich sein, indem nicht nur das Profilattribut, sondern auch die Echtzeit-Kontextdaten im Trigger verwendet werden, der eine REST-API-Payload ist.

Dazu müssen Sie zunächst in Journey Optimizer eine von einer API ausgelöste Kampagne erstellen und deren Ausführung dann über einen API-Aufruf mithilfe der [Interactive Message Execution REST-API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution) starten.

Für von einer API ausgelöste Kampagnen stehen die Kanäle E-Mail, SMS und Push-Benachrichtigungen zur Verfügung.

➡️ [Funktion im Video kennenlernen](#video)

## Wichtige Schritte für die Erstellung von API-ausgelösten Kampagnen {#steps}

1. [Definieren der Kampagneneigenschaften](api-triggered-campaign-properties.md)
1. [Konfigurieren der Kampagnenaktion](api-triggered-campaign-action.md)
1. [Bearbeiten des Kampagneninhalts](api-triggered-campaign-content.md)
1. [Definieren der Zielgruppe einer Kampagne](api-triggered-campaign-audience.md)
1. [Planen der Kampagne](api-triggered-campaign-schedule.md)
1. [Kampagne überprüfen und aktivieren](review-activate-api-triggered-campaign.md)
1. [Trigger bei der Kampagnenausführung](trigger-campaigns.md)

## Anleitungsvideos {#video}

Erfahren Sie, wie Sie eine Kampagne erstellen und sie von einem externen System aus basierend auf Benutzerinteraktionen auslösen, indem Sie die REST-API zur Ausführung interaktiver Nachrichten verwenden.

>[!VIDEO](https://video.tv.adobe.com/v/3452734?quality=12&captions=ger)
