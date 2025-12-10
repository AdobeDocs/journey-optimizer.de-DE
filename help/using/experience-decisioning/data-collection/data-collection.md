---
title: Datenerfassung
description: Erfahren Sie mehr über die Erfassung von Feedback-Daten zum Entscheidungs-Management
feature: Datasets, Decisioning
topic: Integrations
role: User, Developer
level: Experienced
hide: true
hidefromtoc: true
exl-id: 32e3a5b9-0633-48df-95b5-c03536be23a1
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 100%

---

# Datenerfassung für das Entscheidungs-Management {#data-collection}

## Grundlagen der Datenerfassung

Sie können Feedback zu Angebotsentscheidungen in Adobe Experience Platform erfassen, einschließlich der angezeigten Angebote und der Benutzerinteraktion mit ihnen. Diese Daten können für Folgendes verwendet werden:

* Erstellen von [Entscheidungsberichten](../cja-reporting.md);
* Verwenden von Regeln zur [Begrenzung](../items.md#capping);
* Erstellen von [KI-Modellen](../ranking/ai-models.md), die als Ranking-Methode verwendet werden können.

## Ereignistypen

Die Art der Datenerfassung variiert je nach Ereignistyp, der erfasst werden soll.

### Entscheidungsereignisse

Jedes Mal, wenn die Entscheidungsfindung eine Entscheidung trifft, werden Informationen zu diesem Entscheidungsereignis **automatisch** an Adobe Experience Platform gesendet. <!--TBC + link-->

### Impressions- und Klickereignisse

Impressions und Klicks für das Entscheidungs-Management werden wie folgt definiert:

* Ein **Impressions**-Ereignis liegt vor, wenn einer Benutzerin bzw. einem Benutzer ein Angebot angezeigt wird.

* Ein **Klick**-Ereignis liegt vor, wenn eine Benutzerin bzw. ein Benutzer auf ein Angebot klickt oder mit ihm interagiert.

Feedback zu Impressions und Klicks wird je nach verwendetem [!DNL Journey Optimizer]-Kanal erfasst.

**E-Mails**, die von [!DNL Journey Optimizer] verfasst werden, verfolgen Impressionen und Klicks **automatisch** nach.

Allerdings müssen bei den **meisten Kanälen** Impressions- und Klick-Daten als ein **Erlebnisereignis** an Adobe Experience Platform gesendet werden. Dazu gehören:

* Web-Seiten, die das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de){target="_blank"} zum Rendern von Angeboten verwenden

* Apps, die das [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=de){target="_blank"} zum Rendern von Angeboten verwenden ([Weitere Informationen](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"})
* Kiosks
* Nachrichten, die über Anwendungen von Drittanbietern gesendet werden

<!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>Kanäle, die eine Entscheidung-API-Anfrage verwenden, um Angebote zu empfangen, benötigen Feedback, das als Erlebnisereignis gesendet wird. Mit anderen Worten: Wenn das Angebot Anweisungen zum Rendern erfordert, ist davon auszugehen, dass Feedback in Form von Erlebnisereignissen gesendet werden sollte.

### Benutzerspezifische Ereignisse

Feedback zu benutzerspezifischen Ereignissen, die mit einem Angebot verknüpft sind, kann gemäß den eigenen Vorlieben an Adobe Experience Platform gesendet werden. Wenn beispielsweise ein Angebot über mehrere Schaltflächen verfügt (*Interesse*, *Kein Interesse* usw.), können Sie diese Ereignisse separat senden. Sie können aber auch als Erlebnisereignisse gesendet werden.

## Senden von Feedback-Daten

Um Feedback-Daten zu senden, müssen Sie einen Datensatz zur Erfassung von Ereignissen erstellen und für jeden Ereignistyp ein Erlebnisereignis definieren, das an Adobe Experience Platform gesendet wird.

* Erfahren Sie in [diesem Abschnitt](create-dataset.md), wie Sie einen Datensatz erstellen, in dem die Erlebnisereignisse erfasst werden.

* Erfahren Sie in [diesem Abschnitt](schema-requirement.md), wie Sie Erlebnisereignisse definieren, die in Feedback-Daten gesendet werden können.
