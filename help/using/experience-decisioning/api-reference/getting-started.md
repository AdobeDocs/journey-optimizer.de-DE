---
title: Erste Schritte mit Decisioning-APIs
description: Hier erfahren Sie, wie Sie mit den Decisioning-APIs Entscheidungselemente programmgesteuert verwalten und personalisierte Angebote bereitstellen können.
feature: API, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 78ed06a3-7787-4aab-8373-df7eb40c1727
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/01NgEXGvNxeb1MNkjeB55VNFZFuSiTfQMKeNahfuHWE
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 339
ht-degree: 87%

---

# Entwicklerhandbuch zur Decisioning-API {#decisioning-api-developer-guide}

Mit Decisioning-APIs können Sie die Komponenten programmgesteuert erstellen und verwalten, die zur Bereitstellung personalisierter Angebote für Ihre Kundinnen und Kunden verwendet werden. Diese RESTful-APIs bieten vollständige CRUD-Vorgänge (Erstellen, Lesen, Aktualisieren, Löschen) für Entscheidungselemente, Auswahlstrategien, Eignungsregeln und andere Entscheidungskomponenten.

## Authentifizierung {#authentication}

Bevor Sie Decisioning-APIs verwenden können, müssen Sie die Authentifizierung einrichten, um auf die API-Endpunkte zuzugreifen. Eine detaillierte Anleitung finden Sie im [Authentifizierungshandbuch für Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}.

## Verfügbare API-Vorgänge {#available-operations}

Die Decisioning-APIs bieten umfassende Verwaltungsfunktionen für Entscheidungskomponenten. Folgende Vorgangskategorien sind verfügbar:

* **Entscheidungselemente**: Erstellen, Lesen, Aktualisieren, Löschen und Auflisten von Entscheidungselementen, die die Angebote oder Inhalte darstellen, die Sie Kundinnen und Kunden bereitstellen möchten.

  ➡️ [Weitere Informationen zur Verwaltung von Entscheidungselementen](decisions-items/create.md)

* **Elementsammlungen**: Organisieren von Entscheidungselementen in Sammlungen, um die Verwaltung und das Targeting mithilfe von Eignungsregeln zu vereinfachen.

  ➡️ [Weitere Informationen zur Verwaltung von Elementsammlungen](items-collections/create.md)

* **Auswahlstrategien**: Definieren, wie Entscheidungselemente ausgewählt und angeordnet werden, wenn mehrere Elemente für den Versand qualifiziert sind.

  ➡️ [Weitere Informationen zur Verwaltung von Auswahlstrategien](selection-strategies/create.md)

* **Eignungsregeln**: Festlegen von Bedingungen, die bestimmen, welche Profile für den Empfang bestimmter Entscheidungselemente geeignet sind.

  ➡️ [Weitere Informationen zur Verwaltung von Eignungsregeln](eligibility-rules/create.md)

* **Rangfolgenformeln**: Erstellen einer benutzerdefinierten Rangfolgenlogik, um die Reihenfolge zu bestimmen, in der Entscheidungselemente angezeigt werden.

  ➡️ [Weitere Informationen zur Verwaltung von Rangfolgenformeln](ranking-formulas/create.md)

* **Platzierungen**: Definieren der Orte oder Kontexte für die Anzeige von Entscheidungselementen in Ihren Erlebnissen.

  ➡️ [Weitere Informationen zur Verwaltung von Platzierungen](exd-placements/create.md)

## Nächste Schritte {#next-steps}

Nachdem Sie nun die Grundlagen der Decisioning-APIs kennen, können Sie mit den spezifischen Vorgängen fortfahren:

* [Erstellen von Entscheidungselementen](decisions-items/create.md)
* [Auflisten von Entscheidungselementen](decisions-items/decision-items-list.md)
* [Erstellen von Auswahlstrategien](selection-strategies/create.md)
* [Erstellen von Eignungsregeln](eligibility-rules/create.md)

Weitere Informationen zur Verwendung der Entscheidungsfindung in Ihren Kampagnen und Journeys finden Sie in der [Dokumentation zur Entscheidungsfindung](../gs-experience-decisioning.md).

>[!NOTE]
>
>Wenn Sie vorhandene Entscheidungs-Management-Objekte zu Decisioning migrieren müssen, verwenden Sie die dedizierte [Decisioning-Migrations-API](../decisioning-migration-api.md). Diese spezielle API bietet automatisierte Funktionen zur Auflösung von Abhängigkeiten und Rollback, die speziell für die Migration von Entscheidungsentitäten über Sandboxes hinweg entwickelt wurden.
