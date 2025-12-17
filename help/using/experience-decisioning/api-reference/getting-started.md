---
title: Erste Schritte mit Decisioning-APIs
description: Hier erfahren Sie, wie Sie mit den Decisioning-APIs Entscheidungselemente programmgesteuert verwalten und personalisierte Angebote bereitstellen können.
feature: API, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 7a4b5d4e-9c1d-4f3a-b8e9-1d5f6e7a8c3a
version: Journey Orchestration
source-git-commit: e46ab0637a0fa4a2b4b8b6ff3b8ab3eb5d38e0f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 5%

---

# Entwicklerhandbuch zur Decisioning-API {#decisioning-api-developer-guide}

Mit Decisioning-APIs können Sie die Komponenten programmgesteuert erstellen und verwalten, die zur Bereitstellung personalisierter Angebote für Ihre Kunden verwendet werden. Diese RESTful-APIs bieten vollständige CRUD-Vorgänge (Erstellen, Lesen, Aktualisieren, Löschen) für Entscheidungselemente, Auswahlstrategien, Eignungsregeln und andere Entscheidungskomponenten.

## Authentifizierung {#authentication}

Bevor Sie Decisioning-APIs verwenden können, müssen Sie die Authentifizierung einrichten, um auf die API-Endpunkte zuzugreifen. Eine schrittweise Anleitung finden Sie [&#x200B; Authentifizierungshandbuch für &#x200B;](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}Journey Optimizer .

## Verfügbare API-Vorgänge {#available-operations}

Die Decisioning-APIs bieten umfassende Verwaltungsfunktionen für Entscheidungskomponenten. Die folgenden Kategorien von Operationen stehen zur Verfügung:

* **Entscheidungselemente** - Erstellen, Lesen, Aktualisieren, Löschen und Auflisten von Entscheidungselementen, die die Angebote oder Inhalte darstellen, die Sie Kunden bereitstellen möchten.

  ➡️ [Erfahren Sie, wie Sie Entscheidungselemente verwalten](decisions-items/create.md)

* **Elementsammlungen** - Organisieren von Entscheidungselementen in Sammlungen, um die Verwaltung und Zielgruppenbestimmung mithilfe von Eignungsregeln zu vereinfachen.

  ➡️ [Erfahren Sie, wie Sie Artikelsammlungen verwalten](items-collections/create.md)

* **Auswahlstrategien** - Definieren Sie, wie Entscheidungselemente ausgewählt und angeordnet werden, wenn mehrere Elemente für den Versand qualifiziert sind.

  ➡️ [Erfahren Sie, wie Sie Auswahlstrategien verwalten](selection-strategies/create.md)

* **Eignungsregeln** - Legen Sie Bedingungen fest, die bestimmen, welche Profile für den Empfang bestimmter Entscheidungselemente geeignet sind.

  ➡️ [Erfahren Sie, wie Sie Eignungsregeln verwalten](eligibility-rules/create.md)

* **Rangfolgeformeln** - Erstellen Sie eine benutzerdefinierte Rangfolgelogik, um die Reihenfolge zu bestimmen, in der Entscheidungselemente angezeigt werden.

  ➡️ [Erfahren Sie, wie Sie Rangfolgeformeln verwalten](ranking-formulas/create.md)

* **Platzierungen** - Definieren Sie die Orte oder Kontexte, an denen Entscheidungselemente in Ihren Erlebnissen angezeigt werden können.

  ➡️ [Erfahren Sie, wie Sie Platzierungen verwalten](exd-placements/create.md)

## Nächste Schritte {#next-steps}

Nachdem Sie nun die Grundlagen der Decisioning-APIs kennen, können Sie mit den spezifischen Vorgängen fortfahren:

* [Erstellen von Entscheidungselementen](decisions-items/create.md)
* [Auflisten von Entscheidungselementen](decisions-items/decision-items-list.md)
* [Erstellen von Auswahlstrategien](selection-strategies/create.md)
* [Erstellen von Eignungsregeln](eligibility-rules/create.md)

Weitere Informationen zur Verwendung der Entscheidungsfindung in Ihren Kampagnen und Journey finden Sie in der [Entscheidungsdokumentation](../gs-experience-decisioning.md).
