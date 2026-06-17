---
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 43%

---
Die Wiki-Tool-Berechtigungen wurden nicht gewährt. Ich fahre mit den detaillierten Informationen aus dem Ticket selbst fort, das die wichtigsten Spezifikationen enthält (500 TPS-Standard, 1000/1500 TPS-Stufen über das Leistungs-Add-on, Push-only, unterstützt Erhöhungen von Burst/begrenzter Dauer).

---

Lösung: Journey Optimizer
Produkt: Journey Optimizer
Titel: Arbeiten mit API-ausgelösten Kampagnen
Beschreibung: Erfahren Sie, wie Sie mit Journey Optimizer-APIs Trigger erstellen können.
Funktion: Kampagnen, API
Thema: Content-Management
Rolle: Entwickler
Stufe: Erfahren
Schlüsselwörter: Kampagnen, API-ausgelöst, REST, Optimizer, Nachrichten
EXL-ID: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID: https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2:
- Kennung: CB954087-F4FC-4456-AFB9-E939CABCDC79
internal-label: Journey Optimizer
feature_v2:
- Kennung: A653CC2E-BC85-4353-A306-399E5B247978
internal-label: Journey Optimizer-Kampagnen
subfeature_v2:
- ID: F7479FA1-474B-479D-8C98-F6CEE5865A38
internal-label: API-ausgelöste Kampagnen
- Kennung: EE67BD4A-25EE-4CDD-9EAB-0D7549FDE0C6
internal-label: Kampagnenverwaltung
role_v2:
- ID: ff6a42d2-313e-452e-93a6-792e4fad9ff8
internal-label: Entwickler
topic_v2:
- ID: E0EB8757-182F-49F3-94A4-1587D16F5094
internal-label: Personalization

Hier finden Sie die vollständige aktualisierte Markdown-Datei:

---

```
solution: Journey Optimizer
product: journey optimizer
title: Work with API triggered campaigns
description: Learn how to trigger campaigns using Journey Optimizer APIs.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campaigns, API-triggered, REST, optimizer, messages
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID: https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a653cc2e-bc85-4353-a306-399e5b247978
    internal-label: Journey Optimizer campaigns
subfeature_v2:
  - id: f7479fa1-474b-479d-8c98-f6cee5865a38
    internal-label: API triggered campaigns
  - id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
    internal-label: Campaign management
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
```

# Arbeiten mit durch API ausgelösten Kampagnen {#trigger-campaigns}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erstellen und starten Sie API-ausgelöste Kampagnen über einen REST-API-Aufruf, damit Sie Nachrichten aus Echtzeit-Marketing und Transaktionen mithilfe von Profil- und kontextuellen Daten senden können.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="Durch API ausgelöste Kampagnen"
>abstract="**Transaktionskampagnen, die durch API ausgelöst werden**<br/> Lösen Sie Echtzeit-Nachrichten über API-Aufrufe aus <br/><br/>**Marketing-Nachrichten**<br/> Werbeinhalte (erfordert Opt-in, unterliegt Geschäftsregeln)<br/><br/>**Transaktionsnachrichten**<br/> Service-bezogene Inhalte (Bestätigung, Warnhinweise, nicht der Zustimmung zum Marketing unterliegend)<br/><br/>**Verfügbare Kanäle**<br/> E-Mail, SMS, Push-Benachrichtigung"

## Informationen zu Kampagnen, die durch API ausgelöst werden {#about}

Durch API ausgelöste Kampagnen ermöglichen den Versand von Marketing-Nachrichten an eine Zielgruppe zum richtigen Zeitpunkt oder den Versand von Transaktions-/Betriebsnachrichten an einen Kontakt, z. B. zum Zurücksetzen des Passworts. Dabei kann eine Personalisierung erforderlich sein, bei der nicht nur Profilattribute, sondern auch Echtzeit-Kontextdaten im Trigger verwendet werden, der eine REST-API-Payload ist.

Dazu müssen Sie zunächst in Journey Optimizer eine durch API ausgelöste Kampagne erstellen und deren Ausführung dann über einen API-Aufruf starten, der die [REST-API zur Ausführung interaktiver Nachrichten](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution) verwendet.

➡️ [Funktion im Video kennenlernen](#video)

>[!NOTE]
>
>Weitere Informationen zu den unterstützten Kanälen finden Sie in der Tabelle in diesem Abschnitt: [Kanäle in Journeys und Kampagnen](../channels/gs-channels.md#channels).
>
>Die verfügbaren Kanäle variieren je nach Ihrem Lizenzierungsmodell und Ihren Add-ons.

## Durchsatz von Push-Benachrichtigungen {#push-throughput}

Standardmäßig unterstützen API-ausgelöste Kampagnen bis zu **500 Transaktionen pro Sekunde (TPS)** für den Versand von Push-Benachrichtigungen. Unternehmen mit hohen Anforderungen an betriebliche Messaging können diese Beschränkung durch das **Performance-Add-on** erhöhen.

Das -Add-on „Performance“ bietet zwei höhere Durchsatzstufen für Push-Benachrichtigungen:

| Stufe | Durchsatz |
|------|-----------|
| Standard | 500 TPS (für alle Kunden enthalten) |
| Leistungs-Add-on — Stufe 1 | 1.000 TPS |
| Leistungs-Add-on — Stufe 2 | 1.500 TPS |

Ein höherer Durchsatz ist sowohl als permanente vertragliche Erhöhung als auch für eine **Dauer verfügbar** um temporäre Szenarien mit hohem Volumen zu unterstützen, z. B. Produkteinführungen oder groß angelegte Kampagnen.

>[!NOTE]
>
>Erhöhte Durchsatzstufen gelten nur für den **Push-Benachrichtigungskanal** für API-ausgelöste Kampagnen. E-Mail- und SMS-Kanäle sind für dieses Add-on nicht verfügbar.
>
>Wenden Sie sich an Ihr Adobe-Accountteam , um eine höhere Durchsatzstufe für Ihr Unternehmen zu aktivieren.

## Wichtige Schritte beim Erstellen von Kampagnen, die durch API ausgelöst werden {#steps}

Bevor Sie mit Kampagnen beginnen, überprüfen Sie [in diesem Abschnitt](get-started-with-campaigns.md#prerequisites) die folgenden Voraussetzungen. Sobald diese Voraussetzungen erfüllt sind, können Sie mit der Erstellung Ihrer Kampagne beginnen:

1. [Definieren der Kampagneneigenschaften](api-triggered-campaign-properties.md)
1. [Konfigurieren der Kampagnenaktion](api-triggered-campaign-action.md)
1. [Bearbeiten des Kampagneninhalts](api-triggered-campaign-content.md)
1. [Definieren der Zielgruppe einer Kampagne](api-triggered-campaign-audience.md)
1. [Planen der Kampagne](api-triggered-campaign-schedule.md)
1. [Prüfen und Aktivieren der Kampagne](review-activate-api-triggered-campaign.md)
1. [Auslösen der Kampagnenausführung](trigger-campaigns.md)

Weitere Informationen über den [gesamten Workflow der Kampagnenerstellung mit typspezifischen Anleitungen →](get-started-with-campaigns.md#workflow)

## Anleitungsvideos {#video}

Erfahren Sie, wie Sie eine Kampagne erstellen und sie von einem externen System aus basierend auf Benutzerinteraktionen auslösen, indem Sie das REST-API zur Ausführung interaktiver Nachrichten verwenden.

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)

---

Der wichtigste Neuzugang ist der neue Abschnitt **Push** Benachrichtigungs-Durchsatz (`## Push notification throughput {#push-throughput}`) zwischen „Info“ und „Wichtige Schritte“, in dem Folgendes dokumentiert wird:
- Der 500 TPS-Standard ist für alle Kunden enthalten
- Die beiden Performance-Add-on-Stufen (1.000 und 1.500 TPS)
- Unterstützung für dauerhafte und zeitlich begrenzte Erhöhungen
- Der Umfang ist auf den Push-Kanal beschränkt.
- Ein Hinweis, der Kunden zu ihrem Adobe-Account-Team weiterleitet