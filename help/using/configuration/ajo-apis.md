---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden von Journey Optimizer-APIs
description: Journey Optimizer stellt RESTful-APIs bereit, mit denen Sie wichtige Vorgänge in Ihren Anwendungen programmgesteuert ausführen können. Erfahren Sie, wie Sie auf diese APIs zugreifen und diese verwenden.
feature: Integrations, Data Ingestion
role: Developer
level: Intermediate
exl-id: 4c897c52-6eb2-4d6e-aaa9-9bd83608b2b6
source-git-commit: 7864012ad148c2e52bc38598016e7bd7fac9644e
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 39%

---

# Arbeiten mit [!DNL Journey Optimizer]-APIs {#apis-gs}

## Schnellzugriff {#quick-access}

Durchsuchen Sie die [vollständige API-Referenz](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}, um auf alle Journey Optimizer-APIs zuzugreifen und sie direkt zu testen. Um zu beginnen, stellen Sie sicher, [ Sie „Authentifizierung einrichten](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} , um die erforderlichen Anmeldeinformationen zu erfassen.

## Überblick {#overview}

Mit Adobe Journey Optimizer-APIs können Sie personalisierte, vernetzte und zeitnahe Kundenerlebnisse in allen Anwendungen, Geräten oder Kanälen bereitstellen und so die End-to-End-Customer Journey effektiv verwalten. Die Customer Journey umfasst die gesamte Kundeninteraktion mit einer Marke, von der ersten Kontaktaufnahme bis zum Verlassen der Kundschaft. Sie beginnt mit der Wahrnehmungsphase, in der die Kundin bzw. der Kunde die Marke kennenlernt und mit ihr zu interagieren beginnt. Die Kundin oder der Kunde vertieft dann die Interaktion mit der Marke weiter, besucht die Website und physische Filialen, tätigt Käufe, sendet Nachrichten oder postet Kundenrezensionen.

Adobe Journey Optimizer basiert nativ auf Adobe Experience Platform und kombiniert ein einheitliches Echtzeit-Kundenprofil, ein API-First Open Framework, zentralisierte Angebotsentscheidungen und künstliche Intelligenz (KI) sowie maschinelles Lernen (ML) zur Personalisierung und Optimierung. Durch Integrieren mit Journey Optimizer-APIs können Marken die nächstbeste Interaktion skaliert, schnell und flexibel über die gesamte Customer Journey hinweg intelligent zu bestimmen.

**Erste Schritte mit Journey Optimizer-APIs:**

* **[Durchsuchen Sie die vollständige API-Referenz](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}** - Greifen Sie auf alle Journey Optimizer-APIs zu und testen Sie sie direkt
* **[Authentifizierung einrichten](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}** - Sammeln Sie die erforderlichen Anmeldeinformationen, um mit der Verwendung der APIs zu beginnen
* **[Entscheidungs-Management-APIs](../offers/api-reference/getting-started.md)** - Angebote und Entscheidungen programmgesteuert verwalten
* **[Experience Decisioning-](../experience-decisioning/api-reference/getting-started.md)**: Bereitstellen personalisierter Entscheidungselemente mithilfe von Code-basierten Erlebnissen

## Authentifizierung {#authentication}

Bevor Sie Journey Optimizer-APIs verwenden können, müssen Sie die Authentifizierung einrichten, um auf die API-Endpunkte zuzugreifen.

Folgen Sie [Authentifizierungshandbuch“, ](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} die erforderlichen Authentifizierungsdaten für alle Journey Optimizer-APIs zu erfassen.

## API-Dokumentation {#api-documentation}

Die vollständige Dokumentation zur Adobe Journey Optimizer-API enthält detaillierte Informationen zu allen verfügbaren Endpunkten, Anfrage-/Antwortformaten und interaktiven Testfunktionen.

Rufen Sie die [Adobe Journey Optimizer-API](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}Dokumentation auf und durchsuchen Sie das Menü **API** Referenzen, um alle verfügbaren APIs zu erkunden.

## Entscheidungs-Management-APIs {#decision-management-apis}

Journey Optimizer bietet dedizierte APIs für das Entscheidungs-Management, mit denen Sie Angebote, Entscheidungen und Platzierungen programmgesteuert verwalten können.

Informationen zu den ersten [ mit Offer Decisioning-APIs finden ](../offers/api-reference/getting-started.md) im Entwicklerhandbuch für die Entscheidungs-Management-API .

## Experience Decisioning-APIs {#experience-decisioning-apis}

Journey Optimizer bietet außerdem Experience Decisioning-APIs zur Bereitstellung personalisierter Entscheidungselemente über Code-basierte Erlebnisse. Experience Decisioning bietet einen vereinfachten Ansatz für die Personalisierung mit Entscheidungselementen, Eignungsregeln und Auswahlstrategien.

**Verfügbare API-Vorgänge:**

* **Entscheidungselemente** - Entscheidungselemente erstellen, lesen, aktualisieren und löschen
* **Auswahlstrategien** - Definieren, wie Entscheidungselemente ausgewählt und geordnet werden
* **Eignungsregeln** - Bedingungen für die Artikeleignung festlegen
* **Artikelsammlungen** - Organisieren von Entscheidungselementen in Sammlungen
* **Rangfolgeformeln** - Konfigurieren einer benutzerdefinierten Rangfolgelogik
* **Platzierungen** - Definieren, wo Entscheidungselemente angezeigt werden können

Erfahren Sie mehr in der [API-Referenz zu Experience Decisioning](../experience-decisioning/api-reference/getting-started.md) und erfahren Sie, wie Sie [Angebote mithilfe von Code-basierten Erlebnissen bereitstellen](../experience-decisioning/gs-experience-decisioning.md).

## Verwandte Themen {#related-topics}

**API-Dokumentation und -Handbücher**

* [Adobe Journey Optimizer-API-Referenz](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}
* [Authentifizierungshandbuch](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}
* [Entwicklerhandbuch für die Entscheidungs-Management-API](../offers/api-reference/getting-started.md)
* [Experience Decisioning-API-Referenz](../experience-decisioning/api-reference/getting-started.md)

**Journey Optimizer-Integration**

* [Integrieren von Adobe Analytics](../integrations/integration-ajo-analytics.md)
* [Integrieren von Adobe Target](../integrations/integration-ajo-target.md)
* [Integrieren von Adobe Campaign](../building-journeys/using-adobe-campaign-v7-v8.md)

**Entwicklerressourcen**

* [Adobe Experience Platform-APIs](https://developer.adobe.com/experience-platform-apis/){target="_blank"}
* [Adobe Developer Console](https://developer.adobe.com/console){target="_blank"}
* [Benutzerdefinierte Aktionen in Journey](../action/about-custom-action-configuration.md)
