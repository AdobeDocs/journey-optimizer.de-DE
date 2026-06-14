---
solution: Journey Optimizer
product: journey optimizer
title: Anbieterintegration
description: Verwenden Sie Adobe Journey Optimizer-Integrationen mit jeder externen Plattform, die eine gültige API bereitstellt, sowie technisch getestete Anbietermuster, um die Sicherheit beim Entwurf Ihres Setups zu gewährleisten.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: Integration, Anbieter, Drittanbieter
subfeature_v2: []
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 6dbdae6edd95d97e039565ed5c6e3cab9f4a19d8
workflow-type: tm+mt
source-wordcount: 401
ht-degree: 0%

---


# Vendors-Integration {#vendor-integration}

>[!BEGINSHADEBOX]

**Auf dieser Seite finden Sie** Beispiel für von Adobe getestete Konfigurationen zum Verbinden von Adobe Journey Optimizer-Integrationen mit Drittanbieteranbietern über Inhalts-, Treueprogramm-, Recommendations-, Daten- und Einverständnisplattformen.

>[!ENDSHADEBOX]

Sie können **Integrationen** in Adobe Journey Optimizer verwenden, um **externe Systeme über HTTP** aufzurufen, wenn jedes System einen **API-Endpunkt)**, der Ihrem Anwendungsfall entspricht und damit kompatibel ist, wie Integrations Anfragen ausgibt und Antworten nutzt. Einen vollständigen Workflow finden Sie unter [Arbeiten mit Integrationen](integrations.md).

Die Liste der beschriebenen Lösungen von Drittanbietern ist anschaulich, nicht vollständig. Andere Plattformen können verwendet werden, wenn sie die Produktanforderungen erfüllen.

## Leitplanken für Operationen {#operational-guardrails}

Wenden Sie Folgendes an, wenn Sie eine Integration in diesem Handbuch oder einem ähnlichen Anbieter konfigurieren:

* **Antwortformat: Zuordnungsfelder von** Integrationen aus **JSON**- oder **HTML**-Antworten. Design-Aufrufe, sodass die API JSON oder HTML zurückgibt, die zum Zeitpunkt der Erstellung für die Zuordnung geeignet sind.
* **Payload und Felder:** Fordern Sie nur die benötigten Attribute an und ordnen Sie sie zu. Kleinere Antworten reduzieren die Latenz und begrenzen die Verfügbarkeit sensibler Daten.
* **Endpunktform:** Sie einen stabilen **-Einzelressourcen-**-Abruf (z. B. einen Eintrag, ein Produkt oder ein Mitglied) gegenüber Endpunkten für eine umfassende Liste oder Paginierung, wenn das Produkt zielgerichtete Suchen erwartet. Siehe [Einschränkungen und Ausschlüsse](#limitations-exclusions) und [Arbeiten mit Integrationen](integrations.md).
* **Volumen und Zuverlässigkeit** Einhaltung der **des Anbieters**. Konfigurieren Sie **Zeitüberschreitung**, **Wiederholen** und **Cache**-Richtlinie für Ihren Kanal (z. B. Batch-E-Mail vs. Transaktionsnachrichten) und validieren Sie unter Last.
* **Sicherheit:** Speichern und Drehen von Token, API-Schlüsseln und OAuth-Anmeldeinformationen gemäß den Richtlinien Ihrer Organisation. Betten Sie keine Geheimnisse in den Nachrichteninhalt ein.


## Einschränkungen und Ausschlüsse {#limitations-exclusions}

Die Liste der Lösungen von Drittanbietern ist **(**) nicht vollständig. Anbieter-APIs, Hosts, Ratenbeschränkungen und JSON- oder HTML-Antwort-Shapes können sich ändern. Bestätigen Sie Endpunkte, Authentifizierung und Feldzuordnung mit der aktuellen Dokumentation des Anbieters und Ihrem Abonnement. Muster gehen dabei von **leseorientierten** für die Personalisierung geeigneten Aufrufen aus. Integrationen unterstützen nur die Zuordnung von **JSON**- und **HTML**-Antworten. **Writeback**, **Batch-Exporte** und Antworten in einem anderen Format werden nicht unterstützt.

## Schnellnavigation {#quick-navigation}

Verwenden Sie diese gruppierten Links, um schnell zum entsprechenden Anbietermuster zu gelangen:

* **Content-Management-System:** [Content](vendor-integration.md#contentful), [SiteCore](vendor-integration.md#sitecore), [Salsify](vendor-integration.md#salsify), [ContentStack](vendor-integration.md#contentstack), [Akeneo](vendor-integration.md#akeneo), [Magnolia](vendor-integration.md#magnolia)
* **Treue und Prämien:** [Gutschein](vendor-integration.md#voucherify), [Talon.One](vendor-integration.md#talon-one), [Antavo](vendor-integration.md#antavo), [Salesforce-Treue](vendor-integration.md#salesforce-loyalty), [Kapillare](vendor-integration.md#capillary)
* **Vorlagen, Personalisierung und Empfehlungen:** [Stensul](vendor-integration.md#stensul), [Marigold](vendor-integration.md#marigold), [Adobe Target Recommendations](vendor-integration.md#adobe-target-recommendations)
* **Daten, Wetter und Betrieb:** [AccuWeather](vendor-integration.md#accuweather), [ShipStation](vendor-integration.md#shipstation), [RevenueCat](vendor-integration.md#revenuecat), [Databricks](vendor-integration.md#databricks)
* **Bewertungen, Einverständnis und Social:** [Bynder](vendor-integration.md#bynder), [Trustpilot](vendor-integration.md#trustpilot), [Bazaarvoice](vendor-integration.md#bazaarvoice), [OneTrust](vendor-integration.md#onetrust), [Meta](vendor-integration.md#meta), [Aprimo](vendor-integration.md#aprimo), [Epsilon (Epsilon3)](vendor-integration.md#epsilon)
