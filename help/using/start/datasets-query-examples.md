---
title: Beispiele für Datensatzabfragen
description: Beispiele für Datensatzabfragen
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 1de18fa479a54c09751324a67793ce50e5657ce3
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 0%

---

# Anwendungsfälle für Datensätze {#tracking-datasets}

Auf dieser Seite finden Sie die Liste der Adobe Journey Optimizer-Datensätze und der zugehörigen Anwendungsfälle:

[Datensatz zum E-Mail-Tracking-Erlebnis](../start/datasets-query-examples.md#email-tracking-experience-event-dataset)
[Datensatz mit Nachrichten-Feedback-Ereignissen](../start/datasets-query-examples.md#message-feedback-event-dataset)
[Datensatz mit Push-Tracking-Erlebnis](../start/datasets-query-examples.md#push-tracking-experience-event-dataset)
[Journey-Schrittereignis](../start/datasets-query-examples.md#journey-step-event)
[Ereignis-Datensatz für Angebotsentscheidungen](../start/datasets-query-examples.md#ode-decisionevents)
[Datensatz des Zustimmungsdienstes](../start/datasets-query-examples.md#consent-service-dataset)
[Datensatz mit BCC-Feedback-Ereignissen](../start/datasets-query-examples.md#bcc-feedback-event-dataset)

## Datensatz zum E-Mail-Tracking-Erlebnis{#email-tracking-experience-event-dataset}

_Name in der Benutzeroberfläche : CJM-E-Mail-Tracking-Erlebnis-Datensatz_

Systemdatensatz für die Aufnahme von E-Mail-Tracking-Erlebnisereignissen aus Journey Optimizer.

Das zugehörige Schema ist das CJM-E-Mail-Tracking-Erlebnisereignis-Schema.

Diese Abfrage zeigt die Anzahl der unterschiedlichen E-Mail-Interaktionen (Öffnungen, Klicks) für eine bestimmte Nachricht:

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

Diese Abfrage zeigt die Zählung der unterschiedlichen E-Mail-Interaktionen (Öffnungen, Klicks) nach Nachricht für eine bestimmte Journey:

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

## Datensatz mit Nachrichten-Feedback-Ereignissen{#message-feedback-event-dataset}

_Name in der Benutzeroberfläche: Datensatz mit CJM-Nachrichten-Feedback-Ereignissen_

Datensatz zur Aufnahme von E-Mail- und Push-App-Feedback-Ereignissen aus Journey Optimizer.

Das zugehörige Schema ist das Schema für CJM-Nachrichten-Feedback-Ereignis.

Diese Abfrage zeigt die Anzahl unterschiedlicher E-Mail-Feedback-Status (gesendet, Bounce usw.) für eine Nachricht an:

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

Diese Abfrage zeigt die Aufschlüsselung der Anzahl unterschiedlicher E-Mail-Feedback-Status (gesendet, Bounce etc.) nach Nachricht für eine bestimmte Journey:

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

Auf aggregierter Ebene Bericht auf Domänenebene (sortiert nach Top-Domänen): Domänenname, gesendete Nachricht, Bounces

```sql
SELECT split_part(_experience.customerJourneyManagement.emailChannelContext.address, '@', 2) AS recipientDomain, SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END)AS sentCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' THEN 1 ELSE 0 END )AS bounceCount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY recipientDomain ORDER BY sentCount DESC;
```

E-Mail-Sendungen täglich:

```sql
SELECT date_trunc('day', TIMESTAMP) AS rolluptimestamp, SUM( CASE WHEN _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent' THEN 1 ELSE 0 END) AS deliveredcount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY date_trunc('day', TIMESTAMP) ORDER BY rolluptimestamp ASC;
```

Finden Sie heraus, ob eine E-Mail-ID eine E-Mail erhalten hat oder nicht und, falls nicht, was der Fehler, die Bounce-Kategorie, der Code war:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.emailchannelcontext.address = 'user@domain.com' AND TIMESTAMP >= now() - INTERVAL '7' DAY ORDER BY status ASC
```

Suchen Sie die Liste aller einzelnen E-Mail-IDs, die in den letzten x Stunden/Tagen einen bestimmten Fehler, eine bestimmte Bounce-Kategorie oder einen bestimmten Code hatten oder die mit einem bestimmten Nachrichtenversand verbunden waren:

```sql
SELECT _experience.customerjourneymanagement.emailchannelcontext.address AS emailid, _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus != 'sent' AND TIMESTAMP >= now() - INTERVAL '10' HOUR AND _experience.customerjourneymanagement.messageexecution.messageexecutionid = 'BMA-45237824' ORDER BY emailid
```

Hardbounce-Rate auf Aggregatebene:

```sql
select hardBounceCount, case when sentCount > 0 then(hardBounceCount/sentCount)*100.0 else 0 end as hardBounceRate from ( select SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' AND _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.type = 'Hard' THEN 1 ELSE 0 END)AS hardBounceCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END )AS sentCount from cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' )
```

Ständige Fehler, gruppiert nach Bounce-Code:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, COUNT(*) AS hardbouncecount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type = 'Hard' AND _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY failurereason
```

## Datensatz mit Push-Tracking-Erlebnis {#push-tracking-experience-event-dataset}

_Name in der Benutzeroberfläche: Datensatz zum CJM-Push-Tracking-Erlebnis_

Datensatz für die Erfassung von Erlebnisereignissen für Mobilgerät-Tracking für Push-Benachrichtigungen von Journey Optimizer.

Das zugehörige Schema ist das Schema für CJM-Push-Tracking-Erlebnis.

Abfragebeispiel:

```sql
select _experience.customerJourneyManagement.pushChannelContext.platform, sum(pushNotificationTracking.customAction.value)  from cjm_push_tracking_experience_event_dataset
group by _experience.customerJourneyManagement.pushChannelContext.platform

select  _experience.customerJourneyManagement.pushChannelContext.platform, SUM (_experience.customerJourneyManagement.messageInteraction.offers.offerCount) from cjm_email_tracking_experience_event_dataset
  group by _experience.customerJourneyManagement.pushChannelContext.platform
```
## Journey-Schrittereignis{#journey-step-event}

_Interner Name: Journey Step Events (System-Datensatz)_

Datensatz für die Aufnahme von Schrittereignissen in der Journey.

Das zugehörige Schema ist das Journey Step Event-Schema zur Journey Orchestration.

Diese Abfrage zeigt die Aufschlüsselung der Erfolgszählungen der Aktion nach Aktionsbezeichnung für eine bestimmte Journey:

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

## Ereignis-Datensatz für Angebotsentscheidungen{#ode-decisionevents}

_Name in der Benutzeroberfläche: ODE DecisionEvents (System-Datensatz)_

Datensatz zur Aufnahme von Angebotsvorschlägen für Benutzer.

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

Diese Abfrage zeigt an, wie oft Angebote in den letzten 30 Tagen einer bestimmten Aktivität/Entscheidung vorgeschlagen wurden und welche Priorität ihnen zugewiesen wurde.

```sql
select proposedOffers.id,proposedOffers.name, po._experience.decisioning.ranking.priority, count(proposedOffers.id) as ProposedCount from (
select explode(propositionexplode.selections) AS proposedOffers from
(select explode(_experience.decisioning.propositionDetails) AS propositionexplode,timestamp FROM ode_decisionevents_itca_decisioning_20200925_235340_379  where date_format(timestamp, 'MM/dd/yyyy') >= date_format(DATE_ADD(CURRENT_DATE, -30), 'MM/dd/yyyy') and _experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:12ae6f35a055c6f0')) a, decision_object_repository_personalized_offers po where proposedOffers.id LIKE 'xcore:personalized-offer%' and po._id=proposedOffers.id
group by proposedOffers.id, proposedOffers.name, po._experience.decisioning.ranking.priority;
```

## Datensatz des Zustimmungsdienstes{#consent-service-dataset}

_Name in der Benutzeroberfläche: Datensatz des CJM Consent Service (Systemdatensatz)_

Datensatz für den Journey Optimizer-Einverständnisdienst.

Das zugehörige Schema ist das CJM Consent Service-Schema.

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

Abfrage zur Rückgabe des Zustimmungswerts für eine E-Mail-ID, wobei die E-Mail-ID die Eingabe sein würde:

```sql
select value.marketing.email.val FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
```

## Datensatz mit BCC-Feedback-Ereignissen{#bcc-feedback-event-dataset}

_Name in der Benutzeroberfläche: AJO BCC Feedback Event Datensatz (Systemdatensatz)_

Datensatz zum Speichern von Informationen für BCC-Nachrichten.

Abfrage für alle BCC-Nachrichten innerhalb von 2 Tagen (für eine bestimmte Kampagne):

```sql
SELECT bcc.*
FROM ajo_bcc_feedback_event_dataset AS bcc
WHERE 
    bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID = '<message-execution-id>' AND 
    bcc.timestamp >= now() - INTERVAL '2' day; 
```

Abfrage mit Feedback-Datensatz, um Benutzer anzuzeigen, die nicht (alle Bounces und Unterdrückungen) erhalten haben und BCC-Eintrag für eine bestimmte Nachricht haben:

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
