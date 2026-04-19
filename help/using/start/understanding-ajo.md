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
source-git-commit: 83a4b2d85866d5bbad607c6b84d0573f211fad89
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 62%

---

# Grundlegendes zu Journey Optimizer {#understanding-ajo}

Auf dieser Seite wird erläutert, wie Adobe Experience Platform und Journey Optimizer zusammenarbeiten. Sie behandelt den kontinuierlichen Daten-zu-Erlebnis-Zyklus, wichtige Funktionsbereiche, Architekturdetails und Integrationspunkte.

Adobe Journey Optimizer und Adobe Experience Platform arbeiten zusammen, um eine skalierte, datengestützte Personalisierung im benötigten Umfang zu ermöglichen. Auf dieser Seite wird erläutert, wie diese Systeme funktionieren und wie ihre wichtigsten Funktionsbereiche zusammenwirken, um außergewöhnliche Kundenerlebnisse zu erstellen. [Weitere Informationen über die wichtigsten Funktionen](get-started.md) | [Wichtige Terminologie](terminology.md)

## Funktionsweise von Journey Optimizer {#how-it-works}

Ohne eine einheitliche Datengrundlage sind Marken gezwungen, sich auf mehrere kanalspezifische Tools zu verlassen, was es schwierig macht, einen konsistenten Überblick über jeden Kunden zu behalten oder auf sein Verhalten in Echtzeit zu reagieren. Journey Optimizer löst dies, indem es auf Adobe Experience Platform aufbaut, um Kundendaten, Inhaltserstellung und Journey-Orchestrierung in einem einzigen, kontinuierlichen System zu verbinden. Das Ergebnis sind aussagekräftige Markenerlebnisse, die die Kundentreue und den Lebenszeitwert fördern.

Adobe Journey Optimizer fungiert als kontinuierlicher Fluss, in dem Daten erfasst, analysiert und zur Erstellung personalisierter Customer Journeys angewendet werden.

![Abbildung, die Adobe Experience Platform als grundlegende Datenschicht zeigt, wobei Journey Optimizer zusammen mit Real-Time CDP, Customer Journey Analytics und Adobe Mix Modeler auf basiert und alle zentrale Services wie Echtzeit-Kundenprofil, Data Governance und Identitätsauflösung gemeinsam nutzen.](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform: Das Fundament {#aep-foundation}

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

Einen tiefen Einblick in die technische Architektur - einschließlich Integrationsmustern, Voraussetzungen und Systemdatenflüssen - finden Sie in den [Adobe Journey Optimizer Blueprints](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/architecture-diagrams/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}. Überlegungen zur Implementierung finden [&#x200B; unter (Leitplanken und Einschränkungen überprüfen](guardrails.md).

## Datenschutz und Sicherheit {#privacy-security}

Die Datenschutz- und Sicherheitspraktiken von Adobe Experience Cloud gelten auch für Adobe Journey Optimizer. Diese Maßnahmen gewährleisten die Einhaltung von Datenschutzbestimmungen (z. B. DSGVO) und ermöglichen es Ihnen, für personalisierte Erlebnisse zu sorgen und gleichzeitig das Kundenvertrauen zu wahren. [Weitere Informationen zum Datenschutz in Journey Optimizer](../privacy/get-started-privacy.md)
