---
title: Datenerfassung
description: Erfahren Sie mehr über die Erfassung von Feedback-Daten zum Entscheidungs-Management
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: c9e970bc231fc3d19f0243b71256ea0f5a981af7
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 74%

---

# Datenerfassung für das Entscheidungs-Management {#data-collection}

## Grundlagen der Datenerfassung

Sie können Feedback zu Angebotsentscheidungen in Adobe Experience Platform erfassen, einschließlich der angezeigten Angebote und der Benutzerinteraktion mit ihnen. Diese Daten können für Folgendes verwendet werden:
* Erstellen von [Berichten über das Entscheidungs-Management](../reports/get-started-events.md);
* Verwenden von Regeln zur [Frequenzlimitierung](../offer-library/add-constraints.md#capping);
* Erstellen von [KI-Modellen](../ranking/create-ranking-strategies.md), die als Ranking-Methode verwendet werden können.

## Ereignistypen

Die Art der Datenerfassung variiert je nach Ereignistyp, der erfasst werden soll.

### Entscheidungsereignisse

Jedes Mal, wenn das Entscheidungs-Management eine Entscheidung trifft, werden Informationen zu diesem Entscheidungsereignis **automatisch** für alle Kanäle an Adobe Experience Platform gesendet. [Weitere Informationen](../reports/get-started-events.md)

### Impressions- und Klickereignisse

Impressionen und Klicks für das Entscheidungs-Management werden wie folgt definiert:

* Ein **Impressions**-Ereignis liegt vor, wenn einer Benutzerin bzw. einem Benutzer ein Angebot angezeigt wird.

* Ein **Klick**-Ereignis liegt vor, wenn eine Benutzerin bzw. ein Benutzer auf ein Angebot klickt oder mit ihm interagiert.

Feedback zu Impressionen und Klicks wird je nach verwendetem [!DNL Journey Optimizer]-Kanal erfasst.

**E-Mails** verfasst von [!DNL Journey Optimizer] **automatisch** Impressionen und Klicks verfolgen.

Allerdings **die meisten Kanäle** Impressions- und Klickdaten benötigen, die als **Erlebnisereignis**. Dazu gehören:

* Web-Seiten mithilfe der [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de){target="_blank"} Angebote rendern

* Mobile Apps mit der [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} to render offers - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* Kiosks
* Nachrichten, die über Anwendungen von Drittanbietern gesendet werden
   <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>Kanäle, die eine Entscheidung-API-Anfrage zum Empfang von Angeboten verwenden, benötigen Feedback, das als Erlebnisereignis gesendet wird. Wenn das Angebot also Anweisungen zum Rendern benötigt, können Sie davon ausgehen, dass Sie Feedback als Erlebnisereignisse senden sollten.

### Benutzerspezifische Ereignisse

Feedback zu benutzerspezifischen Ereignissen, die mit einem Angebot verknüpft sind, kann gemäß den eigenen Vorlieben an Adobe Experience Platform gesendet werden. Wenn beispielsweise ein Angebot über mehrere Schaltflächen verfügt (*Interesse*, *Kein Interesse* usw.), können Sie diese Ereignisse separat senden. Sie können aber auch als Erlebnisereignisse gesendet werden. <!--Not sure to get that part. How feedback is collected in the first case, i.e. when events are sent in separately? Does it mean the customer just handles it the wau he wants?-->

## Senden von Feedback-Daten

Um Feedback-Daten zu senden, müssen Sie einen Datensatz zur Erfassung von Ereignissen erstellen und für jeden Ereignistyp ein Erlebnisereignis definieren, das an Adobe Experience Platform gesendet wird.

* Erfahren Sie in [diesem Abschnitt](create-dataset.md), wie Sie einen Datensatz erstellen, in dem die Erlebnisereignisse erfasst werden.

* Erfahren Sie in [diesem Abschnitt](schema-requirement.md), wie Sie Erlebnisereignisse definieren, die in Feedback-Daten gesendet werden können.

