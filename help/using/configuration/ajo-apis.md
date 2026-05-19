---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden von Journey Optimizer-APIs
description: Journey Optimizer stellt RESTful-APIs bereit, mit denen Sie wichtige Vorgänge in Ihren Anwendungen programmgesteuert ausführen können. Erfahren Sie, wie Sie auf diese APIs zugreifen und diese verwenden.
feature: Integrations, Data Ingestion
role: Developer
level: Intermediate
exl-id: 4c897c52-6eb2-4d6e-aaa9-9bd83608b2b6
TQID: https://experienceleague.adobe.com/VkGKC5I4qSBcxCQQdjTJTYNNGvUoBRFUfUxs3nbIjtQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 582
ht-degree: 87%

---

# Arbeiten mit [!DNL Journey Optimizer]-APIs {#apis-gs}

## Schnellzugriff {#quick-access}

Durchsuchen Sie die [vollständige API-Referenz](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}, um auf alle Journey Optimizer-APIs zuzugreifen, und testen Sie sie direkt. Zunächst müssen Sie die [Authentifizierung einrichten](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}, um die erforderlichen Anmeldedaten zu erfassen.

## Überblick {#overview}

Mit Adobe Journey Optimizer-APIs können Sie personalisierte, vernetzte und zeitnahe Kundenerlebnisse in allen Anwendungen, Geräten oder Kanälen bereitstellen und so die End-to-End-Customer Journey effektiv verwalten. Die Customer Journey umfasst die gesamte Kundeninteraktion mit einer Marke, von der ersten Kontaktaufnahme bis zum Verlassen der Kundschaft. Sie beginnt mit der Wahrnehmungsphase, in der die Kundin bzw. der Kunde die Marke kennenlernt und mit ihr zu interagieren beginnt. Die Kundin oder der Kunde vertieft dann die Interaktion mit der Marke weiter, besucht die Website und physische Filialen, tätigt Käufe, sendet Nachrichten oder postet Kundenrezensionen.

Adobe Journey Optimizer basiert nativ auf Adobe Experience Platform und kombiniert ein einheitliches Echtzeit-Kundenprofil, ein API-First Open Framework, zentralisierte Angebotsentscheidungen und künstliche Intelligenz (KI) sowie maschinelles Lernen (ML) zur Personalisierung und Optimierung. Durch Integrieren mit Journey Optimizer-APIs können Marken die nächstbeste Interaktion skaliert, schnell und flexibel über die gesamte Customer Journey hinweg intelligent zu bestimmen.

**Erste Schritte mit Journey Optimizer-APIs:**

* **[Durchsuchen der vollständigen API-Referenz](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}** – Greifen Sie auf alle Journey Optimizer-APIs zu und testen Sie sie direkt
* **[Einrichten der Authentifizierung](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}** – Erfassen Sie die erforderlichen Anmeldedaten, um mit der Verwendung der APIs zu beginnen
* **[Entscheidungs-Management-APIs](../offers/api-reference/getting-started.md)** – Verwalten Sie Angebote und Entscheidungen programmgesteuert
* **[Erlebnis-Entscheidungs-APIs](../experience-decisioning/api-reference/getting-started.md)** – Stellen Sie personalisierte Entscheidungselemente mithilfe von Code-basierten Erlebnissen bereit

## Authentifizierung {#authentication}

Bevor Sie Journey Optimizer-APIs verwenden können, müssen Sie die Authentifizierung einrichten, um auf die API-Endpunkte zuzugreifen.

Befolgen Sie den [Leitfaden zur Authentifizierung](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}, um die erforderlichen Anmeldedaten für alle Journey Optimizer-APIs zu erfassen.

## API-Dokumentation {#api-documentation}

Die vollständige Dokumentation zur Adobe Journey Optimizer-API enthält detaillierte Informationen zu allen verfügbaren Endpunkten, Anfrage-/Antwortformaten und interaktiven Testfunktionen.

Rufen Sie die [Dokumentation zur Adobe Journey Optimizer-API](https://developer.adobe.com/journey-optimizer-apis){target="_blank"} auf und durchsuchen Sie das Menü **API-Referenzen**, um alle verfügbaren APIs zu erkunden.

## Entscheidungs-Management-APIs {#decision-management-apis}

Journey Optimizer bietet dedizierte APIs für das Entscheidungs-Management, mit denen Sie Angebote, Entscheidungen und Platzierungen programmgesteuert verwalten können.

Lesen Sie die [Entwicklerhandbuch zur Entscheidungs-Management-API](../offers/api-reference/getting-started.md), um sich mit den Angebotsentscheidungs-APIs vertraut zu machen.

## Experience Decisioning-APIs {#experience-decisioning-apis}

Journey Optimizer bietet außerdem Erlebnis-Entscheidungs-APIs zur Bereitstellung personalisierter Entscheidungselemente über Code-basierte Erlebnisse. Die Erlebnis-Entscheidung bietet einen vereinfachten Ansatz für die Personalisierung mit Entscheidungselementen, Eignungsregeln und Auswahlstrategien.

**Verfügbare API-Vorgänge:**

* **Entscheidungselemente** – Erstellen, lesen, aktualisieren und löschen Sie Entscheidungselemente
* **Auswahlstrategien** – Definieren Sie, wie Entscheidungselemente ausgewählt und geordnet werden
* **Eignungsregeln** – Legen Sie Bedingungen für die Eignung von Elementen fest
* **Elementsammlungen** – Organisieren Sie Entscheidungselemente in Sammlungen
* **Rangfolgenformeln** – Konfigurieren Sie eine benutzerdefinierte Rangfolgenlogik
* **Platzierungen** – Definieren Sie, wo Entscheidungselemente angezeigt werden können

Erhalten Sie weitere Informationen in der [Erlebnis-Entscheidungs-API-Referenz](../experience-decisioning/api-reference/getting-started.md) und erfahren Sie, wie Sie [Angebote mithilfe von Code-basierten Erlebnissen bereitstellen](../experience-decisioning/gs-experience-decisioning.md).

## Verwandte Themen {#related-topics}

**API-Dokumentation und -Handbücher**

* [Adobe Journey Optimizer-API-Referenz](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}
* [Authentifizierungshandbuch](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}
* [Entwicklerhandbuch für die Entscheidungs-Management-API](../offers/api-reference/getting-started.md)
* [Erlebnis-Entscheidungs-API-Referenz](../experience-decisioning/api-reference/getting-started.md)

**Journey Optimizer-Integration**

* [Integrationen mit anderen Lösungen](../integrations/ajo-integrations.md)
* [Integrieren mit Adobe Analytics](../event/about-analytics.md)
* [Integrieren mit Adobe Campaign](../building-journeys/using-adobe-campaign-v7-v8.md)

**Entwicklerressourcen**

* [Adobe Experience Platform-APIs](https://developer.adobe.com/experience-platform-apis){target="_blank"}
* [Adobe Developer Console](https://developer.adobe.com/console){target="_blank"}
* [Benutzerdefinierte Aktionen in Journeys](../action/about-custom-action-configuration.md)
