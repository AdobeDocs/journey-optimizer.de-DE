---
solution: Journey Optimizer
product: journey optimizer
title: Beispiele für Datensatzabfragen
description: Beispiele für Datensatzabfragen
feature: Reporting
topic: Content Management
role: User
level: Intermediate
keywords: Datensatz, Optimizer, Anwendungsfälle
exl-id: 26ba8093-8b6d-4ba7-becf-b41c9a06e1e8
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 100%

---

# Anwendungsfälle für Datensätze {#tracking-datasets}

Auf dieser Seite finden Sie die Liste der Adobe Journey Optimizer-Datensätze und der zugehörigen Anwendungsfälle:

[E-Mail-Tracking-Erfahrungs-Ereignisdatensatz](#email-tracking-experience-event-dataset)
[Nachrichten-Feedback-Ereignisdatensatz](#message-feedback-event-dataset)
[Push-Tracking-Erfahrungs-Ereignisdatensatz](#push-tracking-experience-event-dataset)
[Journey-Step-Ereignis](#journey-step-event)
[Decisioning-Ereignisdatensatz](#ode-decisionevents)
[Einverständnisdienst-Datensatz](#consent-service-dataset)
[BCC-Feedback-Ereignisdatensatz](#bcc-feedback-event-dataset)
[Entitätsdatensatz](#entity-dataset)

## E-Mail-Tracking-Erfahrung-Ereignisdatensatz{#email-tracking-experience-event-dataset}

_Name in der Benutzeroberfläche: CJM-E-Mail-Tracking-Erfahrung-Ereignisdatensatz_

Systemdatensatz für die Aufnahme von E-Mail-Tracking-Erlebnisereignissen aus Journey Optimizer.

Das zugehörige Schema ist das CJM-E-Mail-Tracking-Erlebnisereignis-Schema.

Diese Abfrage zeigt die Anzahl der verschiedenen E-Mail-Interaktionen (Öffnungen, Klicks) für eine bestimmte Nachricht:

```sql
select
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageInteraction.interactionType
```

Diese Abfrage zeigt die Aufschlüsselung der Anzahl der verschiedenen E-Mail-Interaktionen (Öffnungen, Klicks) nach Nachricht für eine bestimmte Journey:

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
limit 100;
```

## Nachrichten-Feedback-Ereignisdatensatz{#message-feedback-event-dataset}

_Name in der Benutzeroberfläche: CJM-Nachrichten-Feedback-Ereignisdatensatz_

Datensatz zur Aufnahme von E-Mail- und Push-Anwendungs-Feedback-Ereignissen aus Journey Optimizer.

Das zugehörige Schema ist das CJM-Nachrichten-Feedback-Ereignis-Schema.

Diese Abfrage zeigt die Anzahl unterschiedlicher E-Mail-Feedback-Status (gesendet, gebounct usw.) für eine bestimmte Nachricht:

```sql
select
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus;
```

Diese Abfrage zeigt die Aufschlüsselung der Anzahl unterschiedlicher E-Mail-Feedback-Status (gesendet, gebounct etc.) nach Nachricht für eine bestimmte Journey:

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
limit 100;
```

Auf aggregierter Ebene Bericht auf Domain-Ebene (sortiert nach Top-Domains): Domain-Name, gesendete Nachricht, Bounces

```sql
SELECT split_part(_experience.customerJourneyManagement.emailChannelContext.address, '@', 2) AS recipientDomain, SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END)AS sentCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' THEN 1 ELSE 0 END )AS bounceCount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY recipientDomain ORDER BY sentCount DESC;
```

E-Mail-Sendungen täglich:

```sql
SELECT date_trunc('day', TIMESTAMP) AS rolluptimestamp, SUM( CASE WHEN _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent' THEN 1 ELSE 0 END) AS deliveredcount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY date_trunc('day', TIMESTAMP) ORDER BY rolluptimestamp ASC;
```

Finden Sie heraus, ob eine bestimmte E-Mail-ID eine E-Mail erhalten hat oder nicht. Wenn nicht, was war dann der Fehler, die Bounce-Kategorie oder der Code:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.emailchannelcontext.address = 'user@domain.com' AND TIMESTAMP >= now() - INTERVAL '7' DAY ORDER BY status ASC
```

Finden Sie die Liste aller individuellen E-Mail-IDs, die in den letzten x Stunden/Tagen einen bestimmten Fehler, eine Bounce-Kategorie oder einen Code hatten oder mit einer bestimmten Nachrichtenübermittlung verbunden waren:

```sql
SELECT _experience.customerjourneymanagement.emailchannelcontext.address AS emailid, _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus != 'sent' AND TIMESTAMP >= now() - INTERVAL '10' HOUR AND _experience.customerjourneymanagement.messageexecution.messageexecutionid = 'BMA-45237824' ORDER BY emailid
```

Hard-Bounce-Rate auf aggregierter Ebene:

```sql
select hardBounceCount, case when sentCount > 0 then(hardBounceCount/sentCount)*100.0 else 0 end as hardBounceRate from ( select SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' AND _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.type = 'Hard' THEN 1 ELSE 0 END)AS hardBounceCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END )AS sentCount from cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' )
```

Ständige Fehler, gruppiert nach Bounce-Code:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, COUNT(*) AS hardbouncecount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type = 'Hard' AND _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY failurereason
```

## Push-Tracking-Erlebnisereignis-Datensatz {#push-tracking-experience-event-dataset}

_Name in der Benutzeroberfläche: CJM-Push-Tracking-Erlebnisereignis-Datensatz_

Datensatz für die Aufnahme von Mobile-Tracking-Erlebnisereignissen für Push von Journey Optimizer.

Das zugehörige Schema ist das CJM-Push-Tracking-Erlebnisereignis-Schema.

Abfragebeispiel:

```sql
select _experience.customerJourneyManagement.pushChannelContext.platform, sum(pushNotificationTracking.customAction.value)  from cjm_push_tracking_experience_event_dataset
group by _experience.customerJourneyManagement.pushChannelContext.platform

select  _experience.customerJourneyManagement.pushChannelContext.platform, SUM (_experience.customerJourneyManagement.messageInteraction.offers.offerCount) from cjm_email_tracking_experience_event_dataset
  group by _experience.customerJourneyManagement.pushChannelContext.platform
```

## Journey-Schritt-Ereignis{#journey-step-event}

_Interner Name: Journey-Schritt-Ereignisse (Systemdatensatz)_

Datensatz für die Aufnahme von Schritt-Ereignissen in der Journey.

Das zugehörige Schema ist das Journey-Schritt-Ereignis-Schema zur Journey Orchestration.

Diese Abfrage zeigt die Aufschlüsselung der Aktionserfolgszahlen nach Aktionsbezeichnung für eine bestimmte Journey:

```sql
select
    _experience.journeyOrchestration.stepEvents.actionName AS actionLabel,
    count(1) actionSuccessCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.actionID IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionType IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode IS NULL
group by
    _experience.journeyOrchestration.stepEvents.actionName;   
```

Diese Abfrage zeigt die Aufschlüsselung der eingegebenen Schrittzahlen nach nodeId und nodeLabel für eine bestimmte Journey. nodeId ist hier enthalten, da nodeLabel für verschiedene Journey-Knoten identisch sein kann.

```sql
select
    _experience.journeyOrchestration.stepEvents.nodeID AS nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName AS nodeLabel,
    count(1) stepEnteredCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = TRUE
     AND _experience.journeyOrchestration.stepEvents.eventID IS DISTINCT FROM 'createInstance'
group by
    _experience.journeyOrchestration.stepEvents.nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName; 
```

## Decisioning-Ereignisdatensatz{#ode-decisionevents}

_Name in der Benutzeroberfläche: ODE DecisionEvents (Systemdatensatz)_

Datensatz für die Aufnahme von Angebotsvorschlägen an die Benutzenden.

Das zugehörige Schema ist ODE DecisionEvents.

Diese Abfrage zeigt alle Angebote an, die am Vortag zurückgegeben wurden:

```sql
SELECT date_format(Decision.Timestamp, 'MM/dd/yyyy') as Date
,HOUR(Decision.timestamp) as Hour
,COUNT(*)  as Count
FROM ode_decisionevents_b699fa78_efec_41b1_99fa_78efecc1b1ef_decision AS Decision
WHERE date_format(Decision.timestamp, 'MM/dd/yyyy') = date_format(CURRENT_DATE, 'MM/dd/yyyy') and Decision._experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:13ab41890a335ad6'
GROUP BY date_format(Decision.Timestamp, 'MM/dd/yyyy')
,HOUR(Decision.timestamp)
ORDER BY 1, 2 DESC;
```

Diese Abfrage zeigt die Anzahl der Angebote, die in den letzten 30 Tagen für eine bestimmte Aktivität/Entscheidung vorgeschlagen wurden, und die damit verbundene Angebotspriorität.

```sql
select proposedOffers.id,proposedOffers.name, po._experience.decisioning.ranking.priority, count(proposedOffers.id) as ProposedCount from (
select explode(propositionexplode.selections) AS proposedOffers from
(select explode(_experience.decisioning.propositionDetails) AS propositionexplode,timestamp FROM ode_decisionevents_itca_decisioning_20200925_235340_379  where date_format(timestamp, 'MM/dd/yyyy') >= date_format(DATE_ADD(CURRENT_DATE, -30), 'MM/dd/yyyy') and _experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:12ae6f35a055c6f0')) a, decision_object_repository_personalized_offers po where proposedOffers.id LIKE 'xcore:personalized-offer%' and po._id=proposedOffers.id
group by proposedOffers.id, proposedOffers.name, po._experience.decisioning.ranking.priority;
```

## Einverständnisdienst-Datensatz{#consent-service-dataset}

_Name in der Benutzeroberfläche: CJM-Einverständnisdienst-Datensatz (Systemdatensatz)_

Datensatz für den Journey Optimizer-Einverständnisdienst.

Das zugehörige Schema ist das CJM-Einverständnisdienst-Schema.

Abfrage zur Auflistung von E-Mail-IDs, die dem Empfang von E-Mails zugestimmt haben:

```sql
select key as email FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
)
where value.marketing.email.val == 'y'
```

Abfrage zur Rückgabe des Einverständniswerts für eine E-Mail-ID, wobei die E-Mail-ID die Eingabe ist:

```sql
select value.marketing.email.val FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
```

## BCC-Feedback-Ereignisdatensatz{#bcc-feedback-event-dataset}

_Name in der Benutzeroberfläche: AJO-BCC-Feedback-Ereignisdatensatz (Systemdatensatz)_

Datensatz zum Speichern von Informationen für BCC-Nachrichten.

Abfrage aller BCC-Nachrichten innerhalb von 2 Tagen (für eine bestimmte Kampagne):

```sql
SELECT bcc.*
FROM ajo_bcc_feedback_event_dataset AS bcc
WHERE 
    bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID = '<message-execution-id>' AND 
    bcc.timestamp >= now() - INTERVAL '2' day; 
```

Abfrage mit Feedback-Datensatz, um die Benutzenden anzuzeigen, die nicht (alle Bounces und Unterdrückungen) empfangen haben und die einen BCC-Eintrag für eine bestimmte Nachricht haben:

```sql
SELECT 
    distinct bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS OriginalRecipientAddress 
FROM ajo_bcc_feedback_event_dataset  AS bcc 
WHERE 
    bcc.timestamp > now() - INTERVAL '2' DAY AND     bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND      bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress != '' AND
    ( 
            bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress NOT IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
            mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent'
        )  
    OR     bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
        mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND 
            mfe._experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.category = 'async' AND 
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus
```

## Entitätsdatensatz{#entity-dataset}

_Name in der Schnittstelle: ajo_entity_dataset (Systemdatensatz)_

Datensatz zum Speichern von Entitätsmetadaten für Nachrichten, die an den Endbenutzer gesendet werden.

Das zugehörige Schema ist das AJO-Entitätsschema.

Mit diesem Datensatz erhalten Sie Zugriff auf von Marketing-Experten definierte Metadaten. So können Sie für bessere Insights bei der Berichterstellung sorgen, wenn Journey Optimizer-Datensätze zur Visualisierung von Berichten in externen Tools exportiert werden. Das wird mithilfe des Attributs „messageID“ erzielt, das bei der Zuordnung verschiedener Datensätze wie dem Nachrichten-Feedback-Datensatz und Erlebnisereignis-Tracking-Datensätzen hilft, sodass Details zu einem Nachrichtenversand vom Versand bis zum Tracking auf Profilebene verfügbar werden.

**Wichtige Hinweise**

* Ein Eintrag für eine Nachricht wird erst nach der Veröffentlichung von Journey oder Kampagne erstellt.

* Sie können den Eintrag 30 Minuten nach der Veröffentlichung der Kampagne/Journey sehen.

>[!NOTE]
>
>Um dafür zu sorgen, dass auch in Zukunft die Kompatibilität gesichert ist, gibt es derzeit im Entitätsdatensatz zwei Einträge für jede Nachrichtenveröffentlichung. Dies wirkt sich nicht auf Ihre Fähigkeit aus, bei Bedarf Join-Abfragen für Datensätze zu verwenden, um die gewünschten Informationen abzurufen.

Wenn Sie die von einer bestimmten Journey gesendeten E-Mails in Ihren Berichten nach der Aktion sortieren möchten, die sie gesendet hat, können Sie den Nachrichten-Feedback-Datensatz mit dem Entitäts-Datensatz verbinden. Die zu verwendenden Felder sind `_experience.decisioning.propositions.scopeDetails.correlationID` und `_id field in entity dataset`.

Mit der folgenden Abfrage können Sie die zugehörige Nachrichtenvorlage für eine bestimmte Kampagne abrufen:

```sql
SELECT
  AE._experience.customerJourneyManagement.entities.channelDetails.template
from
  ajo_entity_dataset AE
    WHERE AE._experience.customerJourneyManagement.entities.campaign.campaignVersionID = 'd7a01136-b113-4ef2-8f59-b6001f7eef6e'
```

Mit der folgenden Abfrage können Sie die Journey-Details und den E-Mail-Betreff abrufen, die mit allen Feedback-Ereignissen verbunden sind:

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject 
from 
  ajo_entity_dataset AE 
  INNER JOIN cjm_message_feedback_event_dataset MF ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```

Sie können Journey-Schrittereignisse, Nachrichten-Feedback und Tracking-Datensätze zuordnen, um die Statistiken für ein bestimmtes Profil zu erhalten:

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject,
    JE._EXPERIENCE.JOURNEYORCHESTRATION.STEPEVENTS.PROFILEID,
    JE._EXPERIENCE.JOURNEYORCHESTRATION.STEPEVENTS.NODENAME
from 
  ajo_entity_dataset AE 
  INNER JOIN cjm_message_feedback_event_dataset MF 
    ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
    INNER JOIN journey_step_events JE
    ON AE._experience.customerJourneyManagement.entities.journey.journeyActionID = JE._experience.journeyOrchestration.stepEvents.actionID
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```
