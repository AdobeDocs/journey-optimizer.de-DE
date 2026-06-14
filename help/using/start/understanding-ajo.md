---
solution: Journey Optimizer
product: journey optimizer
title: Grundlegendes zu Journey Optimizer
description: Erfahren Sie, wie Adobe Journey Optimizer mit Adobe Experience Platform zusammenarbeitet, um personalisierte Kundenerlebnisse bereitzustellen
feature: Get Started
topic: Content Management
role: Admin, Developer, User
level: Beginner
keywords: Journey Optimizer, Funktionsweise, Architektur, Experience Platform, Funktionsbereiche
exl-id: 9df179a0-a5f6-4dbd-a9db-a103731b1854
TQID: https://experienceleague.adobe.com/E2ksPVFZBggv1RgEri7jx30G2oSanpmNs77vH9Yuq78
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 46a5a6dc0a3486633a1a71f8bba8a3cd53aaa618
workflow-type: tm+mt
source-wordcount: 986
ht-degree: 58%

---

# Grundlegendes zu Journey Optimizer {#understanding-ajo}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Adobe Journey Optimizer mit Adobe Experience Platform zusammenarbeitet, damit Sie den Daten-zu-Erlebnis-Zyklus, die Funktionsbereiche und die Architektur hinter personalisierten Journeys verstehen können.

>[!ENDSHADEBOX]

Auf dieser Seite wird erläutert, wie Adobe Experience Platform und Journey Optimizer zusammenarbeiten. Sie behandelt den kontinuierlichen Daten-zu-Erlebnis-Zyklus, wichtige Funktionsbereiche, Architekturdetails und Integrationspunkte.

Adobe Journey Optimizer und Adobe Experience Platform arbeiten zusammen, um eine skalierte, datengestützte Personalisierung im benötigten Umfang zu ermöglichen. Auf dieser Seite wird erläutert, wie diese Systeme funktionieren und wie ihre wichtigsten Funktionsbereiche zusammenwirken, um außergewöhnliche Kundenerlebnisse zu erstellen. [Weitere Informationen über die wichtigsten Funktionen](get-started.md) | [Wichtige Terminologie](terminology.md)

## Funktionsweise von Journey Optimizer {#how-it-works}

Ohne eine einheitliche Datengrundlage sind Marken gezwungen, sich auf mehrere kanalspezifische Tools zu verlassen, was es schwierig macht, einen konsistenten Überblick über jeden Kunden zu behalten oder auf sein Verhalten in Echtzeit zu reagieren. Journey Optimizer löst dies, indem es auf Adobe Experience Platform aufbaut, um Kundendaten, Inhaltserstellung und Journey-Orchestrierung in einem einzigen, kontinuierlichen System zu verbinden. Das Ergebnis sind aussagekräftige Markenerlebnisse, die die Kundentreue und den Lebenszeitwert fördern.

Adobe Journey Optimizer fungiert als kontinuierlicher Fluss, in dem Daten erfasst, analysiert und zur Erstellung personalisierter Customer Journeys angewendet werden.

![Abbildung, die Adobe Experience Platform als grundlegende Datenschicht zeigt, wobei Journey Optimizer zusammen mit Real-Time CDP, Customer Journey Analytics und Adobe Mix Modeler auf basiert und alle zentrale Services wie Echtzeit-Kundenprofil, Data Governance und Identitätsauflösung gemeinsam nutzen.](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform: Die Stiftung {#aep-foundation}

Adobe Experience Platform dient als Backbone, mit dem Marken Kundendaten zentralisieren und für personalisierte Erlebnisse aktivieren können.

* **Datenplattform** – Zentrale Drehscheibe für die Erfassung, Verwaltung und Strukturierung von Kundendaten, um systemübergreifende Konsistenz zu gewährleisten. [Weitere Informationen zu Schemata und Datensätzen](../data/get-started-schemas.md)
* **Datenaufnahme (Quellen)** – Marken importieren Daten mithilfe vorkonfigurierter Connectoren aus verschiedenen Systemen wie CRM-Plattformen, Websites, Mobile Apps und Cloud-Speicher. [Weitere Informationen zu Datenquellen](get-started-sources.md)
* **Echtzeit-Kundenprofil** – Erstellt einheitliche Profile, indem Daten aus verschiedenen Quellen (E-Mail-Interaktionen, In-Store-Käufe, Web-Verhalten) zusammengeführt werden. [Weitere Informationen zu Profilen](../audience/get-started-profiles.md)
* **Governance-Ebene** – Steuert den Datenzugriff, die Einhaltung von Datenschutzbestimmungen und die Sicherheit bei gleichzeitiger Einhaltung von Vorschriften. [Dokumentation zu Datenschutz anzeigen](../privacy/get-started-privacy.md)

### Adobe Journey Optimizer: Die Orchestrierungs-Engine {#ajo-orchestration}

Adobe Journey Optimizer wendet die Daten und Erkenntnisse aus Adobe Experience Platform an, um in verschiedenen Kanälen intelligente, personalisierte Kundenerlebnisse bereitzustellen.

* **Kundenverständnis** – Echtzeit-Kundenprofile ermöglichen eine Segmentierung in Zielgruppen für gezieltes Messaging. [Erstellen von Zielgruppen](../audience/about-audiences.md)
* **Inhalte und Angebote** - Ein integrierter visueller Designer, wiederverwendbare Vorlagen und eine zentrale Asset-Bibliothek ermöglichen es Teams, Nachrichten für jeden Kanal zu erstellen und zu personalisieren, ohne die Plattform verlassen zu müssen. Dynamische Personalisierung passt Inhalte basierend auf Kundenattributen, Verhalten und Kontext an. Die Entscheidungslogik in Echtzeit wählt dann für jede Person das beste Angebot aus. [Inhalte entwerfen](../../rp_landing_pages/content-management-landing-page.md) | [Assets verwalten](../integrations/assets.md) | [Angebote verwalten](../offers/get-started/starting-offer-decisioning.md)
* **Journey- und Kampagnen-Management** – Automatisiert Interaktionssequenzen (Journeys) oder plant einmalige gezielte Nachrichten (Kampagnen). [Erstellen von Journeys](../building-journeys/journey-gs.md) | [Erstellen von Kampagnen](../campaigns/get-started-with-campaigns.md)
* **Versand (Verbindungen)** – Versendet Nachrichten über Kanäle wie E-Mail, SMS, Push-Benachrichtigungen und Direkt-Mail; exportiert Daten in externe Systeme. [Konfigurieren der Kanäle](../configuration/get-started-configuration.md)
* **Messung und Analyse** – Verfolgt die Kundeninteraktion und die Kampagnenleistung mit Berichten zur kontinuierlichen Verbesserung. [Anzeigen von Berichten](../reports/campaign-global-report-cja.md)

### Der kontinuierliche Optimierungszyklus {#optimization-cycle}

Dieses Ökosystem funktioniert als kontinuierlicher Optimierungszyklus. Daten fördern das Kundenverständnis, das in personalisierte Inhalte und Entscheidungen einfließt. Diese werden in Journeys orchestriert, kanalübergreifend bereitgestellt, auf Effektivität getestet und im Laufe der Zeit verfeinert.

![Abbildung des kontinuierlichen Optimierungszyklus in Journey Optimizer: Die Datenaufnahme liefert Daten an Kundenprofile, die Informationen zu Inhalts- und Angebotsentscheidungen liefern, in Journey orchestriert, kanalübergreifend bereitgestellt, leistungsgemessen und im Laufe der Zeit verfeinert werden.](../assets/do-not-localize/get-started-flow.png)

## Wichtige Funktionsbereiche {#functional-areas}

Journey Optimizer umfasst sieben wichtige Funktionsbereiche, die nahtlos zusammenarbeiten.

| Funktionsbereich | Zweck | Wichtige Aktivitäten |
|-----------------|---------|----------------|
| **Daten-Management** | Organisieren von Kundendaten | Schemata definieren, Datensätze erstellen, Daten aus verschiedenen Systemen importieren. [Weitere Informationen](../data/get-started-schemas.md) |
| **Kunden-Management** | Verstehen, wer Ihre Kundschaft ist | Einheitliche Profile erstellen, Identitäten auflösen, Zielgruppen erstellen. [Weitere Informationen](../audience/get-started-profiles.md) |
| **Content-Management** | Erstellen personalisierter Nachrichten | E-Mails erstellen, Assets verwalten, Vorlagen und Fragmente erstellen, Inhalte personalisieren. [Weitere Informationen](../../rp_landing_pages/content-management-landing-page.md) |
| **Entscheidungs-Management** | Auswählen des besten Angebots in Echtzeit | Angebotsbibliothek verwalten, Regeln definieren, Einschränkungen anwenden, Rangfolgenlogik einrichten. [Weitere Informationen](../offers/get-started/starting-offer-decisioning.md) |
| **Journey-Management** | Entwerfen automatisierter Kundenerlebnisse | Journeys mit dem visuellen Designer erstellen, Trigger festlegen, Bedingungen und Warteschritte hinzufügen. [Weitere Informationen](../building-journeys/journey-gs.md) |
| **Verbindungen** | Verbinden von Datenquellen und Kanälen | Quell-Connectoren konfigurieren, Kanäle einrichten, Verbindungen zu externen Plattformen herstellen. [Weitere Informationen](../configuration/get-started-configuration.md) |
| **Administration und Datenschutz** | Steuern des Setups und der Konformität | Benutzende verwalten, Sandboxes konfigurieren, Kanäle einrichten, Datenschutzanfragen bearbeiten. [Weitere Informationen](../administration/permissions.md) |

### So arbeiten diese Bereiche zusammen {#working-together}

Diese Funktionsbereiche arbeiten in einem kontinuierlichen Zyklus:

1. **Datenaufnahme** – Daten fließen in Adobe Experience Platform, strukturiert durch Daten-Management.
2. **Kundenverständnis** – Echtzeit-Kundenprofile vereinheitlichen Daten; Kunden-Management erstellt Zielgruppen
3. **Inhalts- und Angebotsstrategie** – Content-Management erstellt Nachrichten; Entscheidungs-Management definiert Angebotslogik
4. **Orchestrierung** – Journey-Management ordnet Interaktionen kanalübergreifend zu und nutzt dabei Kundenverständnis, Inhalte und Entscheidungen
5. **Versand** – Verbindungen erleichtern den Nachrichtenversand über Kanäle oder geben Daten an externe Systeme weiter
6. **Messung** – Leistungsdaten liefern Erkenntnisse zurück, um Zielgruppen, Inhalte, Entscheidungen und Journeys zu verfeinern
7. **Governance** – Administrations- und Datenschutzkontrollen sorgen für durchgehende Konformität

## Architekturdetails {#architecture-details}

Journey Optimizer ist eine von vier nativ auf Adobe Experience Platform aufbauenden Anwendungen neben Real-Time CDP, Customer Journey Analytics und Adobe Mix Modeler. Es nutzt die zentralen Services von AEP - Echtzeit-Kundenprofil, Identitätsdiagramm, Data Governance und Abfrage-Services - gemeinsam, sodass es auf eine einheitliche Kundendatenbasis zugreift, ohne dass separate Integrationen erforderlich sind. Journey Optimizer kann als eigenständige Anwendung ausgeführt werden oder mit anderen AEP-nativen Anwendungen zusammenarbeiten.

Einen tiefen Einblick in die technische Architektur - einschließlich Integrationsmustern, Voraussetzungen und Systemdatenflüssen - finden Sie in den [Adobe Journey Optimizer Blueprints](https://experienceleague.adobe.com/de/docs/blueprints-learn/architecture/architecture-diagrams/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}. Überlegungen zur Implementierung finden [&#x200B; unter (Leitplanken und Einschränkungen überprüfen](guardrails.md).

## Datenschutz und Sicherheit {#privacy-security}

Die Datenschutz- und Sicherheitspraktiken von Adobe Experience Cloud gelten auch für Adobe Journey Optimizer. Diese Maßnahmen gewährleisten die Einhaltung von Datenschutzbestimmungen (z. B. DSGVO) und ermöglichen es Ihnen, für personalisierte Erlebnisse zu sorgen und gleichzeitig das Kundenvertrauen zu wahren. [Weitere Informationen zum Datenschutz in Journey Optimizer](../privacy/get-started-privacy.md)
