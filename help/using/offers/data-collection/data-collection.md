---
title: Datenerfassung
description: Erfahren Sie mehr über die Erfassung von Feedback-Daten zur Entscheidungsverwaltung
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 6%

---

# Entscheidungsmanagement-Datenerfassung {#data-collection}

## Grundlagen zur Datenerfassung

Sie können offer decisioning-Feedback in Adobe Experience Platform erfassen, einschließlich der angezeigten Angebote und der Interaktion der Benutzer mit ihnen. Diese Daten können für Folgendes verwendet werden:
* Zusammensetzung [Entscheidungsberichte](../reports/get-started-events.md);
* Verwenden [Frequenzlimitierung](../offer-library/add-constraints.md#capping) Regeln;
* Erstellen [AI-Modelle](../ranking/create-ranking-strategies.md) , die als Ranking-Methode verwendet werden kann.

## Ereignistypen

Die Art der Datenerfassung variiert je nach Ereignistyp, den Sie erfassen möchten.

### Entscheidungsereignisse

Jedes Mal, wenn die Entscheidungsverwaltung eine Entscheidung trifft, werden Informationen zu diesem Entscheidungsereignis **automatisch** für alle Kanäle an Adobe Experience Platform gesendet. [Weitere Informationen](../reports/get-started-events.md)

### Impression- und Klickereignisse

Impressionen und Klicks zur Entscheidungsverwaltung werden wie folgt definiert:

* Ein **Impression** -Ereignis ist, wenn einem Benutzer ein Angebot angezeigt wird.

* A **click** -Ereignis ist, wenn ein Benutzer auf ein Angebot klickt oder mit ihm interagiert.

Feedback zu Impressionen und Klicks wird je nach [!DNL Journey Optimizer] verwendeter Kanal.

1. Auf der einen Seite einige Kanäle **automatisch** Impressionen und Klicks verfolgen. Diese sind wie folgt:

   * Von verfasste E-Mails [!DNL Journey Optimizer]
   * Mobile Push-Benachrichtigungen, die von [!DNL Journey Optimizer]
   * Mobile Apps mit der [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=de#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} oder Mobile SDK<!--TBC--> Angebote rendern <!--need more info + link-->

   >[!NOTE]
   >
   >Wenn Adobe das Angebot visuell an den Endbenutzer im Kanal rendert, können Sie davon ausgehen, dass die Adobe das Feedback automatisch sendet.

1. Einige Kanäle erfordern dagegen, dass Impressions- und Klickdaten als **Erlebnisereignis**.

   Außer Apps, die die [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=de#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} oder Mobile SDK<!--TBC-->, benötigen alle Kanäle, die eine Entscheidungsfindungs-API-Anfrage zum Empfang von Angeboten verwenden, Feedback, das als Erlebnisereignis gesendet wird. Dazu gehören:

   * Webseiten
   * Kiosk
   * Nachrichten, die über Anwendungen von Drittanbietern gesendet werden

   >[!NOTE]
   >
   >Wenn das Angebot Anweisungen zum Rendern benötigt, können Sie davon ausgehen, dass Sie Feedback als Erlebnisereignisse senden sollten.

### Benutzerspezifische Ereignisse

Feedback zu benutzerspezifischen Ereignissen, die mit einem Angebot verknüpft sind, können gemäß Ihren eigenen Voreinstellungen an Adobe Experience Platform gesendet werden. Wenn beispielsweise ein Angebot über mehrere Schaltflächen verfügt, z. B. *Interessant*, *Nicht interessiert* usw.), können Sie diese Ereignisse separat senden, diese können aber auch als Erlebnisereignisse gesendet werden. <!--Not sure to get that part. How feedback is collected in the first case, i.e. when events are sent in separately? Does it mean the customer just handles it the wau he wants?-->

## Senden von Feedback-Daten

Um Feedback-Daten zu senden, müssen Sie einen Datensatz zur Erfassung von Ereignissen erstellen und für jeden Ereignistyp ein Erlebnisereignis definieren, das an Adobe Experience Platform gesendet wird.

* Erfahren Sie, wie Sie einen Datensatz erstellen, in dem die Erlebnisereignisse erfasst werden in [diesem Abschnitt](create-dataset.md).

* Erfahren Sie, wie Sie Erlebnisereignisse definieren, die in Feedback-Daten gesendet werden können. [diesem Abschnitt](schema-requirement.md).

