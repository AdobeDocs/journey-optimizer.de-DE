---
title: Erste Schritte
description: Beginn der Nutzung der API einer Angebotsbibliothek, um wichtige Operationen unter Verwendung der Decisioning-Engine durchzuführen.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: ht
source-wordcount: '397'
ht-degree: 100%

---

# Entwicklerhandbuch für die Entscheidungs-Management-API {#decision-management-api-developer-guide}

>[!CONTEXTUALHELP]
>id="od_api_support"
>title="Neue Entscheidungs-Management-APIs"
>abstract="Es sind neue APIs für die Erstellung und Verwaltung von Entscheidungs-Management-Objekten verfügbar. Die alten APIs werden noch bis zum 27.03.2024 unterstützt."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_api_support"
>title="Neue Entscheidungs-Management-APIs"
>abstract="Es sind neue APIs für die Erstellung und Verwaltung von Entscheidungs-Management-Objekten verfügbar. Die alten APIs werden noch bis zum 27.03.2024 unterstützt."

In diesem Entwicklerhandbuch finden Sie Anweisungen, wie Sie mit der Verwendung der [!DNL Offer Library]-API beginnen können. Das Handbuch enthält Beispiel-API-Aufrufe für die Durchführung wichtiger Operationen mit der Decisioning-Engine.

➡️ [Weitere Informationen zu den Komponenten des Entscheidungs-Managements finden Sie in diesem Video](#video)

## Voraussetzungen {#prerequisites}

Dieses Handbuch setzt ein Verständnis der folgenden Komponenten von Adobe Experience Platform voraus:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"}: Das standardisierte Framework, mit dem Kundenerlebnisdaten von [!DNL Experience Platform] organisiert werden.
   * [Grundlagen der Schemakomposition](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=de){target="_blank"}: Erfahren Sie mehr über die Grundbausteine von XDM-Schemata.
* [Entscheidungs-Management](../../../using/offers/get-started/starting-offer-decisioning.md): Beschreibt die Konzepte und Komponenten der Erlebnis-Entscheidungsfindung im Allgemeinen und insbesondere des Entscheidungs-Managements. Veranschaulicht die Strategien zur Auswahl der besten Option, die während eines Kundenerlebnisses angezeigt werden soll.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=de){target="_blank"}: PQL ist eine leistungsstarke Sprache zum Schreiben von Ausdrücken auf XDM-Instanzen. Zur Definition von Entscheidungsregeln wird PQL verwendet.

## Lesen von Beispiel-API-Aufrufen {#reading-sample-api-calls}

In diesem Handbuch wird anhand von Beispielen für API-Aufrufe die korrekte Formatierung von Anfragen aufgezeigt. Dazu gehören Pfade, erforderliche Kopfzeilen und ordnungsgemäß formatierte Anfrage-Payloads. Außerdem wird ein Beispiel für eine von der API im JSON-Format zurückgegebene Antwort bereitgestellt. Informationen zu den Konventionen, die in der Dokumentation für Beispiel-API-Aufrufe verwendet werden, finden Sie im Abschnitt zum [Lesen von Beispiel-API-Aufrufen](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html?lang=de#how-do-i-format-an-api-request){target="_blank"} im Handbuch zur Fehlerbehebung für [!DNL Experience Platform].

## Sammeln von Werten für erforderliche Kopfzeilen {#gather-values-for-required-headers}

Um [!DNL Adobe Experience Platform]-APIs aufzurufen, müssen Sie zunächst das [Authentifizierungs-Tutorial](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=de){target="_blank"} lesen. Durch Abschluss des Authentifizierungs-Tutorials werden die Werte für die einzelnen erforderlichen Header in allen [!DNL Experience Platform]-API-Aufrufen bereitgestellt, wie unten dargestellt:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

Bei allen Anfragen mit einer Payload (POST, PUT, PATCH) ist eine zusätzliche Kopfzeile erforderlich:

* `Content-Type: application/json`

## Nächste Schritte {#next-steps}

Dieses Dokument behandelt die erforderlichen Grundkenntnisse zum Aufrufen der [!DNL Offer Library]-API. Sie können nun mit den Beispielaufrufen in diesem Entwicklungshandbuch fortfahren und den entsprechenden Anweisungen folgen.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = "Mobile_Sheliak"`.
-->

## Anleitungsvideo {#video}

Im folgenden Video werden die Komponenten des Entscheidungs-Managements erklärt.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

