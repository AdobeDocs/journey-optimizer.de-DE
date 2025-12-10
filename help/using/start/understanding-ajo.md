---
solution: Journey Optimizer
product: journey optimizer
title: Grundlegendes zu Journey Optimizer
description: Erfahren Sie, wie Adobe Journey Optimizer mit Adobe Experience Platform zusammenarbeitet, um personalisierte Kundenerlebnisse bereitzustellen
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: a956684ab52f9045b5e1f84cc0b8d0071689873b
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 12%

---

# Grundlegendes zu Journey Optimizer {#understanding-ajo}

Adobe Journey Optimizer (AJO) und Adobe Experience Platform (AEP) arbeiten zusammen, um eine skalierte, datengesteuerte Personalisierung im benötigten Umfang zu ermöglichen. Auf dieser Seite wird erläutert, wie diese Systeme funktionieren und wie ihre wichtigsten Funktionsbereiche zusammenwirken, um außergewöhnliche Kundenerlebnisse zu schaffen.

## Funktionsweise von Journey Optimizer {#how-it-works}

Adobe Journey Optimizer fungiert als kontinuierlicher Fluss, in dem Daten erfasst, analysiert und angewendet werden, um personalisierte Kunden-Journey zu erstellen.

![](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform: The Foundation {#aep-foundation}

Adobe Experience Platform dient als Rückgrat, mit dem Marken Kundendaten zentralisieren und für personalisierte Erlebnisse aktivieren können:

* **Datenplattform** - Zentraler Knotenpunkt für die Erfassung, Verwaltung und Strukturierung von Kundendaten, um die systemübergreifende Konsistenz sicherzustellen
* **Datenaufnahme (Quellen)** - Importieren Sie Daten von CRM-Plattformen, Websites, Mobile Apps und Cloud-Speicher mithilfe vordefinierter Connectoren
* **Echtzeit-Kundenprofil** - Erstellt einheitliche Profile, indem Daten aus verschiedenen Quellen (E-Mail-Interaktionen, In-Store-Käufe, Web-Verhalten) zusammengeführt werden
* **Governance-Ebene** - Steuert den Datenzugriff, die Einhaltung von Datenschutzbestimmungen und die Sicherheit bei gleichzeitiger Einhaltung von Vorschriften

### Adobe Journey Optimizer: Die Orchestrierungs-Engine {#ajo-orchestration}

Adobe Journey Optimizer wendet die Daten und Erkenntnisse aus AEP an, um intelligente, personalisierte Kundenerlebnisse bereitzustellen:

* **Kundenverständnis** - Echtzeit-Kundenprofile ermöglichen die Segmentierung in Zielgruppen für zielgerichtetes Messaging
* **Inhalte und Angebote** - Tools zum Erstellen, Verwalten und Personalisieren von Inhalten; Echtzeit-Logik zur Auswahl des besten Angebots für jede Person
* **Journey- und Kampagnenverwaltung** Automatisiert Interaktionssequenzen (Journey) oder plant einmalige zielgerichtete Nachrichten (Kampagnen)
* **Versand (Verbindungen)** : Versendet Nachrichten über Kanäle wie E-Mail, SMS, Push-Benachrichtigungen und Briefpost; exportiert Daten in externe Systeme
* **Messung und Analyse** - Verfolgt Kundeninteraktionen und Kampagnenleistung mit Berichten zur kontinuierlichen Verbesserung

### Der kontinuierliche Optimierungszyklus {#optimization-cycle}

Dieses Ökosystem funktioniert als kontinuierlicher Optimierungszyklus. Daten fördern das Kundenverständnis, das in personalisierte Inhalte und Entscheidungen einfließt. Diese werden in Journeys orchestriert, kanalübergreifend bereitgestellt, auf Effektivität getestet und im Laufe der Zeit verfeinert.

![](../assets/do-not-localize/get-started-flow.png)

## Wichtige Funktionsbereiche {#functional-areas}

Journey Optimizer umfasst sieben wichtige Funktionsbereiche, die nahtlos zusammenarbeiten:

| Funktionsbereich | Zweck | Schlüsselaktivitäten |
|-----------------|---------|----------------|
| **Daten-Management** | Kundendaten organisieren | Schemata definieren, Datensätze erstellen, Daten aus verschiedenen Systemen importieren |
| **Kundenverwaltung** | Verstehen, wer Ihre Kundschaft ist | Einheitliche Profile erstellen, Identitäten auflösen, Audiences erstellen |
| **Content-Management** | Personalisierte Nachrichten erstellen | E-Mails entwerfen, Assets verwalten, Vorlagen und Fragmente erstellen und Inhalte personalisieren |
| **Entscheidungs-Management** | Auswahl des besten Angebots in Echtzeit | Angebotsbibliothek verwalten, Regeln definieren, Einschränkungen anwenden, Rangfolgelogik festlegen |
| **Journey-Verwaltung** | Entwerfen automatisierter Kundenerlebnisse | Erstellen Sie Journey mit Visual Designer, legen Sie Trigger fest, fügen Sie Bedingungen hinzu und warten Sie Schritte |
| **Verbindungen** | Verbinden von Datenquellen und Kanälen | Konfigurieren von Quell-Connectoren, Einrichten von Kanälen, Verbinden mit externen Plattformen |
| **Administration und Datenschutz** | Einrichtung und Konformität von Kontrollen | Benutzer verwalten, Sandboxes konfigurieren, Kanäle einrichten, Datenschutzanfragen bearbeiten |

### So arbeiten diese Bereiche zusammen {#working-together}

Diese Funktionsbereiche arbeiten in einem kontinuierlichen Zyklus:

1. **Datenaufnahme** - Datenflüsse in AEP, strukturiert nach Daten-Management
2. **Kundenverständnis** - Echtzeit-Kundenprofile vereinheitlichen Daten, Customer Management erstellt Zielgruppen
3. **Content- und Angebotsstrategie** - Content-Management erstellt Nachrichten; Entscheidungs-Management definiert Angebotslogik
4. **Orchestrierung** - Das Journey-Management ordnet Interaktionen kanalübergreifend mithilfe von Kundendaten, Inhalten und Entscheidungen zu
5. **Versand** - Verbindungen erleichtern den Nachrichtenversand über Kanäle oder geben Daten an externe Systeme weiter
6. **Messung** - Leistungsdaten liefern Einblicke zurück, um Zielgruppen, Inhalte, Entscheidungen und Journey zu verfeinern
7. **Governance** - Verwaltungs- und Datenschutzkontrollen sorgen für die Einhaltung von

## Architekturdetails {#architecture-details}

Für technische Teams finden Sie hier das detaillierte Architekturdiagramm, das zeigt, wie Journey Optimizer mit Adobe Experience Platform integriert wird:

![Architektur von Adobe Journey Optimizer](assets/ajo-architecture.png)

Vier Programme basieren nativ auf Experience Platform: Adobe Real-Time Customer Data Platform, Journey Optimizer, Customer Journey Analytics und Adobe Mix Modeler. Journey Optimizer arbeitet nahtlos mit diesen Anwendungen zusammen, kann aber auch unabhängig voneinander arbeiten.

### Integrationspunkte {#integration-points}

Journey Optimizer lässt sich auf mehreren Ebenen mit Adobe Experience Platform integrieren:

* **Datenschicht**: Gibt dasselbe Echtzeit-Kundenprofil, Identitätsdiagramm und dieselben Datensätze frei
* **Service-Ebene** - Nutzt die Governance-, Datenschutz- und Abfrage-Services von AEP
* **Anwendungsebene** - Bietet Journey-Orchestrierung, Entscheidungs-Management und Content-Management zusätzlich zu AEP

Weitere Informationen zu [Adobe Journey Optimizer-Blueprints](https://experienceleague.adobe.com/de/docs/blueprints-learn/architecture/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}.

## Datenschutz und Sicherheit {#privacy-security}

Die Datenschutz- und Sicherheitspraktiken von Adobe Experience Cloud gelten auch für Adobe Journey Optimizer. Diese Maßnahmen gewährleisten die Einhaltung von Datenschutzbestimmungen wie der DSGVO, sodass Sie personalisierte Erlebnisse bereitstellen und gleichzeitig das Vertrauen der Kunden bewahren können.

[Weitere Informationen zum Datenschutz in Journey Optimizer](../privacy/get-started-privacy.md)

>[!MORELIKETHIS]
>
>* [Erste Schritte mit Journey Optimizer](get-started.md)
>* [Schlüsselbegriffe](terminology.md)
>* [Handbuch zur Benutzeroberfläche](user-interface.md)
>* [Leitplanken und Einschränkungen](guardrails.md)

