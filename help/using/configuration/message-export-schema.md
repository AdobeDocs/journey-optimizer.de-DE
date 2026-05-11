---
solution: Journey Optimizer
product: journey optimizer
title: AJO-Nachrichtenexportschema
description: Erfahren Sie mehr über die Felder, die im AJO-Nachrichtenexportdatensatz verfügbar sind
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: Export, Nachrichten, Datensatz, Schema, E-Mails, SMS
source-git-commit: 15e9700f5c226418ae13ed4991d58c603611136d
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 37%

---

# AJO-Nachrichtenexportschema {#ajo-message-export-schema}

Wenn **Nachrichtenexport** für eine E-Mail- oder SMS-Kanalkonfiguration aktiviert ist, wird der Inhalt der gesendeten Nachricht in den **AJO-** in [!DNL Adobe Experience Platform] geschrieben.

In diesem Abschnitt werden die im exportierten Datensatz verfügbaren Felder aufgelistet.

## Datensatzfelder

+++ _experience

**Feld:** `_experience`\
**Typ:** Objekt

+++

+++ _experience > customerJourneyManagement

**Feld:** `customerJourneyManagement`\
**Typ:** Objekt

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata

**Feld:** `messageDeliveryMetadata`\
**Typ:** Objekt

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > emailMetadata

**Feld:** `emailMetadata`\
**Typ:** Objekt

* Empfänger

  **Feld:** `recipient`\
  **Typ:** Objekt

   * BCC

     **Feld:** `bcc`\
     **Type:** Zeichenfolgen-Array

   * CC

     **Feld:** `cc`\
     **Type:** Zeichenfolgen-Array

   * email

     **Feld:** `email`\
     **Typ:** Zeichenfolge

   * name

     **Feld:** `name`\
     **Typ:** Zeichenfolge

* Absender

  **Feld:** `sender`\
  **Typ:** Objekt

   * email

     **Feld:** `email`\
     **Typ:** Zeichenfolge

   * errorEmail

     **Feld:** `errorEmail`\
     **Typ:** Zeichenfolge

   * name

     **Feld:** `name`\
     **Typ:** Zeichenfolge

   * replyToEmail

     **Feld:** `replyToEmail`\
     **Typ:** Zeichenfolge

   * replyToName

     **Feld:** `replyToName`\
     **Typ:** Zeichenfolge

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > smsMetadata

**Feld:** `smsMetadata`\
**Typ:** Objekt

* Empfänger

  **Feld:** `recipient`\
  **Typ:** Objekt

   * number

     **Feld:** `number`\
     **Typ:** Zeichenfolge

* Absender

  **Feld:** `sender`\
  **Typ:** Objekt

   * Zahlen

     **Feld:** `numbers`\
     **Type:** Zeichenfolgen-Array

+++

+++ _experience > customerJourneyManagement > messageExecution

**Feld:** `messageExecution`\
**Typ:** Objekt

* Zielgruppe

  **Feld:** `audience`\
  **Typ:** Objekt

   * id

     **Feld:** `id`\
     **Typ:** Zeichenfolge

   * type

     **Feld:** `type`\
     **Typ:** Zeichenfolge

* fragmentPublicationIDs

  **Feld:** `fragmentPublicationIDs`\
  **Type:** Zeichenfolgen-Array

* Metadaten

  **Feld:** `metadata`\
  **Typ:** Zuordnung

   * [Map-Schlüssel]

     **Typ:** Zeichenfolge

* parentSourceMeta

  **Feld:** `parentSourceMeta`\
  **Typ:** Objekt

   * sourceActionID

     **Feld:** `sourceActionID`\
     **Typ:** Zeichenfolge

   * sourceID

     **Feld:** `sourceID`\
     **Typ:** Zeichenfolge

   * sourceType

     **Feld:** `sourceType`\
     **Typ:** Zeichenfolge

   * sourceVersionID

     **Feld:** `sourceVersionID`\
     **Typ:** Zeichenfolge

* batchInstanceID

  **Feld:** `batchInstanceID`\
  **Typ:** Zeichenfolge

* campaignActionID

  **Feld:** `campaignActionID`\
  **Typ:** Zeichenfolge

* campaignID

  **Feld:** `campaignID`\
  **Typ:** Zeichenfolge

* campaignVersionID

  **Feld:** `campaignVersionID`\
  **Typ:** Zeichenfolge

* journeyActionID

  **Feld:** `journeyActionID`\
  **Typ:** Zeichenfolge

* journeyVersionID

  **Feld:** `journeyVersionID`\
  **Typ:** Zeichenfolge

* journeyVersionInstanceID

  **Feld:** `journeyVersionInstanceID`\
  **Typ:** Zeichenfolge

* journeyVersionNodeID

  **Feld:** `journeyVersionNodeID`\
  **Typ:** Zeichenfolge

* messageExecutionID

  **Feld:** `messageExecutionID`\
  **Typ:** Zeichenfolge

* messageID

  **Feld:** `messageID`\
  **Typ:** Zeichenfolge

* messagePublicationID

  **Feld:** `messagePublicationID`\
  **Typ:** Zeichenfolge

* messageType

  **Feld:** `messageType`\
  **Typ:** Zeichenfolge

* waveID

  **Feld:** `waveID`\
  **Typ:** Zeichenfolge

+++

+++ _experience > customerJourneyManagement > messageProfile

**Feld:** `messageProfile`\
**Typ:** Objekt

* channel

  **Feld:** `channel`\
  **Typ:** Objekt

   * contentTypes

     **Feld:** `contentTypes`\
     **Type:** Zeichenfolgen-Array

   * locationTypes

     **Feld:** `locationTypes`\
     **Type:** Zeichenfolgen-Array

   * metricTypes

     **Feld:** `metricTypes`\
     **Type:** Zeichenfolgen-Array

   * _id

     **Feld:** `_id`\
     **Typ:** Zeichenfolge

   * _type

     **Feld:** `_type`\
     **Typ:** Zeichenfolge

   * mediaAction

     **Feld:** `mediaAction`\
     **Typ:** Zeichenfolge

   * mediaType

     **Feld:** `mediaType`\
     **Typ:** Zeichenfolge

   * mode

     **Feld:** `mode`\
     **Typ:** Zeichenfolge

   * referrerSource

     **Feld:** `referringSource`\
     **Typ:** Zeichenfolge

   * typeAtSource

     **Feld:** `typeAtSource`\
     **Typ:** Zeichenfolge

* isSendTimeOptimized

  **Feld:** `isSendTimeOptimized`\
  **type:** boolean

* isTestExecution

  **Feld:** `isTestExecution`\
  **type:** boolean

* messageProfileID

  **Feld:** `messageProfileID`\
  **Typ:** Zeichenfolge

* messageProfileTrackingID

  **Feld:** `messageProfileTrackingID`\
  **Typ:** Zeichenfolge

* requestID

  **Feld:** `requestID`\
  **Typ:** Zeichenfolge

* secondaryDimensionID

  **Feld:** `secondaryDimensionID`\
  **Typ:** Zeichenfolge

* secondaryDimensionName

  **Feld:** `secondaryDimensionName`\
  **Typ:** Zeichenfolge

* Variante

  **Feld:** `variant`\
  **Typ:** Zeichenfolge

+++

+++ _experience > customerJourneyManagement > messageRenderedContent

**Feld:** `messageRenderedContent`\
**Typ:** Objekt

* emailContent

  **Feld:** `emailContent`\
  **Typ:** Objekt

   * HTML

     **Feld:** `html`\
     **Typ:** Zeichenfolge

   * Subjekt

     **Feld:** `subject`\
     **Typ:** Zeichenfolge

   * Text

     **Feld:** `text`\
     **Typ:** Zeichenfolge

* smsContent

  **Feld:** `smsContent`\
  **Typ:** Objekt

   * Medien

     **Feld:** `media`\
     **Typ:** Zeichenfolge

   * message

     **Feld:** `message`\
     **Typ:** Zeichenfolge

   * title

     **Feld:** `title`\
     **Typ:** Zeichenfolge

+++

+++ identityMap

**Feld:** `identityMap`\
**Typ:** Zuordnung

* [Map-Schlüssel]

  **Type:** Array von Objekten

   * AuthenticatedState

     **Feld:** `authenticatedState`\
     **Typ:** Zeichenfolge

   * id

     **Feld:** `id`\
     **Typ:** Zeichenfolge

   * primär

     **Feld:** `primary`\
     **type:** boolean

+++

+++ eventType

**Feld:** `eventType`\
**Typ:** Zeichenfolge

+++

+++ produziert von

**Feld:** `producedBy`\
**Typ:** Zeichenfolge

+++

+++ Zeitstempel

**Feld:** `timestamp`\
**Typ:** dateTime

+++


