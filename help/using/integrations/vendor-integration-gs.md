---
solution: Journey Optimizer
product: journey optimizer
title: Anbieterintegration
description: Verwenden Sie Adobe Journey Optimizer-Integrationen mit jeder externen Plattform, die eine gültige API bereitstellt, sowie technisch getestete Anbietermuster, um die Sicherheit beim Entwurf Ihres Setups zu gewährleisten.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: Integration, Anbieter, Drittanbieter
source-git-commit: 8a2c90b22dbe68de57bbdbe06123a957e54648a6
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 1%

---


# Erste Schritte mit der Vendors-Integration {#vendor-integration}

>[!BEGINSHADEBOX]

Inhaltsverzeichnis:

* [Arbeiten mit Integrationen](external-sources.md)
* **[Erste Schritte mit der Vendors-Integration](vendor-integration-gs.md)**
* [Verfügbare Anbieter](vendor-integration.md)
* [FAQs](vendor-integration-faq.md)

>[!ENDSHADEBOX]

Sie können **Integrationen** in Adobe Journey Optimizer verwenden, um **externe Systeme über HTTP** aufzurufen, wenn jedes System einen **API-Endpunkt)**, der Ihrem Anwendungsfall entspricht und damit kompatibel ist, wie Integrations Anfragen ausgibt und Antworten nutzt. Einen vollständigen Workflow finden Sie unter [Arbeiten mit Integrationen](external-sources.md).

Die Liste der beschriebenen Lösungen von Drittanbietern ist anschaulich, nicht vollständig. Andere Plattformen können verwendet werden, wenn sie die Produktanforderungen erfüllen.

## Leitplanken für Operationen {#operational-guardrails}

Wenden Sie Folgendes an, wenn Sie eine Integration in diesem Handbuch oder einem ähnlichen Anbieter konfigurieren:

* **Antwortformat: Zuordnungsfelder von** Integrationen aus **JSON**-Antworten. Design-Aufrufe so, dass die API JSON zurückgibt, das zur Authoring-Zeit für die Zuordnung geeignet ist.
* **Payload und Felder:** Fordern Sie nur die benötigten Attribute an und ordnen Sie sie zu. Kleinere Antworten reduzieren die Latenz und begrenzen die Verfügbarkeit sensibler Daten.
* **Endpunktform:** Sie einen stabilen **-Einzelressourcen-**-Abruf (z. B. einen Eintrag, ein Produkt oder ein Mitglied) gegenüber Endpunkten für eine umfassende Liste oder Paginierung, wenn das Produkt zielgerichtete Suchen erwartet. Siehe [Einschränkungen und Ausschlüsse](#limitations-exclusions) und [Arbeiten mit Integrationen](external-sources.md).
* **Volumen und Zuverlässigkeit** Einhaltung der **des Anbieters**. Konfigurieren Sie **Zeitüberschreitung**, **Wiederholen** und **Cache**-Richtlinie für Ihren Kanal (z. B. Batch-E-Mail vs. Transaktionsnachrichten) und validieren Sie unter Last.
* **Sicherheit:** Speichern und Drehen von Token, API-Schlüsseln und OAuth-Anmeldeinformationen gemäß den Richtlinien Ihrer Organisation. Betten Sie keine Geheimnisse in den Nachrichteninhalt ein.

## Einschränkungen und Ausschlüsse {#limitations-exclusions}

Die Liste der Lösungen von Drittanbietern ist **(**) nicht vollständig. Anbieter-APIs, Hosts, Ratenbeschränkungen und JSON-Antwort-Shapes können sich ändern. Bestätigen Sie Endpunkte, Authentifizierung und Feldzuordnung mit der aktuellen Dokumentation des Anbieters und Ihrem Abonnement. Muster gehen dabei von **leseorientierten** für die Personalisierung geeigneten Aufrufen aus. Writeback, Batch-Exporte oder Nicht-JSON-Antworten können außerhalb des Gültigkeitsbereichs liegen, es sei denn, dies wird angegeben.

## Schnellnavigation {#quick-navigation}

Verwenden Sie diese gruppierten Links, um schnell zum entsprechenden Anbietermuster zu gelangen:

* **Content und CMS:** [Content](#contentful), [SiteCore](#sitecore), [Salsify](#salsify), [ContentStack](#contentstack), [Akeneo](#akeneo), [Magnolia](#magnolia)
* **Treue und Prämien:** [Gutschein](#voucherify), [Talon.One](#talon-one), [Antavo](#antavo), [Salesforce-Treue](#salesforce-loyalty), [Kapillare](#capillary)
* **Vorlagen und Nachrichten:** [Stensul](#stensul), [Ringelblume](#marigold), [Adobe Target Recommendations](#adobe-target-recommendations)
* **Daten, Wetter und Betrieb:** [AccuWeather](#accuweather), [ShipStation](#shipstation), [RevenueCat](#revenuecat), [Databricks](#databricks)
* **Bewertungen, Einverständnis und Social:** [Bynder](#bynder), [Trustpilot](#trustpilot), [Bazaarvoice](#bazaarvoice), [OneTrust](#onetrust), [Meta](#meta), [Aprimo](#aprimo), [Epsilon (Epsilon3)](#epsilon)
