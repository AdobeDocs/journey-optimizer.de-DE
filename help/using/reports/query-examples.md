---
solution: Journey Optimizer
product: journey optimizer
title: Beispiele für Abfragen
description: Beispiele für Abfragen
feature: Reporting, Journeys
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 26ad12c3-0a2b-4f47-8f04-d25a6f037350
source-git-commit: 4a15ee3ac4805880ce80f788e4619b501afb3d8b
workflow-type: tm+mt
source-wordcount: '3337'
ht-degree: 77%

---

# Beispiele für Abfragen{#query-examples}

In diesem Abschnitt werden häufig verwendete Beispiele für die Abfrage von Journey-Schrittereignissen im Data Lake aufgeführt. Bevor Sie sich mit bestimmten Anwendungsfällen befassen, müssen Sie wissen, welche wichtigen Kennungen in Journey-Ereignisdaten verwendet werden.

Stellen Sie sicher, dass die in Ihren Abfragen verwendeten Felder im entsprechenden Schema über zugeordnete Werte verfügen.

## Grundlegendes zu wichtigen Kennungen {#key-identifiers}

+++Was ist der Unterschied zwischen ID, instanceID und profileID?

* ID: eindeutig für alle Schrittereignis-Einträge. Zwei verschiedene Schrittereignisse können nicht dieselbe ID aufweisen.
* instanceID: instanceID ist für alle Schrittereignisse identisch, die einem Profil innerhalb einer Journey-Ausführung zugeordnet sind. Wenn ein Profil erneut in die Journey eintritt, wird eine andere instanceID verwendet. Diese neue instanceID ist für alle Schrittereignisse in der erneut eingetretenen Instanz gleich (von Anfang bis Ende).
* profileID: die Identität des Profils, die dem Namespace der Journey entspricht.

>[!NOTE]
>
>Zur Fehlerbehebung empfehlen wir bei der Abfrage von Journeys die Verwendung von journeyVersionID anstelle von journeyVersionName.  Weitere Informationen über die Attribute von Journey-Eigenschaften finden Sie [in diesem Abschnitt](../building-journeys/expression/journey-properties.md#journey-properties-fields).

+++

## Grundlegende Anwendungsfälle/allgemeine Abfragen {#common-queries}

+++Wie viele Profile sind in einem bestimmten Zeitrahmen in eine Journey eingetreten?

Diese Abfrage gibt die Anzahl eindeutigen Profile an, die im angegebenen Zeitraum in die Journey eingetreten sind.

_Data-Lake-Abfrage_

```sql
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
AND _experience.journeyOrchestration.stepEvents.nodeType='start'
AND _experience.journeyOrchestration.stepEvents.instanceType = 'unitary'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour);
```

Erfahren Sie, wie Sie [Fehler bei verworfenen Ereignistypen in journey_step_events beheben](../reports/sharing-field-list.md#discarded-events).

+++

+++Welche Regel hat dazu geführt, dass ein Profil nicht in eine bestimmte Journey eingetreten ist?

Diese Abfrage gibt die Informationen zum zurückgewiesenen Regelsatz und zur Regel zurück, wenn ein Profil aufgrund von Begrenzungs- oder Eignungsregeln nicht auf eine Journey zugreifen kann.

_Beispiel_

```sql
SELECT 
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType,
    _experience.journeyOrchestration.serviceEvents.dispatcher.rejectedRuleset.ID AS RULESET_ID,
    _experience.journeyOrchestration.serviceEvents.dispatcher.rejectedRuleset.name AS RULESET_NAME,
    _experience.journeyOrchestration.serviceEvents.dispatcher.rejectedRuleset.rejectedRules.ID AS RULE_ID,
    _experience.journeyOrchestration.serviceEvents.dispatcher.rejectedRuleset.rejectedRules.name AS RULE_NAME
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard'
AND
    _experience.journeyOrchestration.stepEvents.journeyVersionID='3855072d-79c3-438a-a5c3-c77fd6843812'
AND
    timestamp >= to_date('2025-05-16')
```

+++

+++Welche Regel hat dazu geführt, dass ein Profil eine bestimmte Journey-Aktion nicht erhalten hat?

Diese Abfrage gibt die Schrittereignisdetails für Profile zurück, die während einer Journey verworfen wurden und keine Journey-Aktion erhalten haben. Auf diese Weise lässt sich erkennen, warum Profile aufgrund von Geschäftsregeln wie beispielsweise Einschränkungen durch Ruhezeiten verworfen wurden.

_Data-Lake-Abfrage_

```sql
SELECT 
    _experience.journeyOrchestration.stepEvents.profileID,
    _experience.journeyOrchestration.stepEvents.instanceID,
    _experience.journeyOrchestration.stepEvents.journeyID,
    _experience.journeyOrchestration.stepEvents.journeyVersionID,
    _experience.journeyOrchestration.stepEvents.actionExecutionError,
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode,
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType,
    DATE(timestamp),
    timestamp
FROM journey_step_events
WHERE
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType = '<eventType>' AND
    _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>' AND
    _experience.journeyOrchestration.stepEvents.instanceID = '<instanceID>';
```

_Beispiel_

```sql
SELECT 
    _experience.journeyOrchestration.stepEvents.profileID,
    _experience.journeyOrchestration.stepEvents.instanceID,
    _experience.journeyOrchestration.stepEvents.journeyID,
    _experience.journeyOrchestration.stepEvents.journeyVersionID,
    _experience.journeyOrchestration.stepEvents.actionExecutionError,
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode,
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType,
    DATE(timestamp),
    timestamp
FROM journey_step_events
WHERE
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
    _experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'quietHours' AND
    _experience.journeyOrchestration.stepEvents.journeyVersionID = '6f21a072-6235-4c39-9f6a-9d9f3f3b2c3a' AND
    _experience.journeyOrchestration.stepEvents.instanceID = 'unitary_089dc93a-1970-4875-9660-22433b18e500';
```


Die Abfrageergebnisse zeigen Schlüsselfelder an, die dabei helfen, den Grund für verworfene Profile zu identifizieren:

* **actionExecutionError** – Die Einstellung `businessRuleProfileDiscarded` bedeutet, dass das Profil aufgrund einer Geschäftsregel verworfen wurde. Das Feld `eventType` enthält zusätzliche Details darüber, welche spezifische Geschäftsregel das Verwerfen verursacht hat.

* **eventType** – Gibt den Typ der Geschäftsregel an, die das Verwerfen verursacht hat:
   * `quietHours`: Profil wurde aufgrund der Konfiguration von Ruhezeiten verworfen
   * `forcedDiscardDueToQuietHours`: Profil wurde zwangsweise verworfen, da das Limit für in Ruhezeiten befindliche Profile erreicht wurde

+++

+++Wie viele Fehler sind in einem bestimmten Zeitraum an den einzelnen Knoten einer bestimmten Journey aufgetreten?

Diese Abfrage zählt die unterschiedlichen Profile, bei denen Fehler an jedem Knoten einer Journey aufgetreten sind, gruppiert nach Knotennamen. Alle Arten von Aktionsausführungsfehlern und Abruffehlern sind enthalten.

_Data Lake-Abfrage_

```sql
SELECT
_experience.journeyOrchestration.stepEvents.nodeName,
count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID='<journeyVersionID>'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour)
AND
  (_experience.journeyOrchestration.stepEvents.actionExecutionError is not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode is not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionOriginCode is not NULL
    OR _experience.journeyOrchestration.stepEvents.actionExecutionOriginError is not NULL
    OR _experience.journeyOrchestration.stepEvents.fetchError is not NULL
    OR _experience.journeyOrchestration.stepEvents.fetchErrorCode is not NULL
  )
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName;
```

+++

+++Wie viele Ereignisse wurden in einem bestimmten Zeitrahmen von einer bestimmten Journey verworfen?

Diese Abfrage zählt die Gesamtzahl der Ereignisse, die von einer Journey verworfen wurden. Sie filtert nach verschiedenen Ereignis-Codes für das Verwerfen, einschließlich Segmentexportauftragsfehlern, Dispatcher-Verwerfungen und Status-Computer-Verwerfungen.

_Data Lake-Abfrage_

```sql
SELECT
count(_id) AS NUMBER_OF_EVENTS_DISCARDED
FROM journey_step_events
WHERE (
   _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'error'
   OR _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard'
   OR _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode = 'discard'
   OR _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode is not null
)
AND _experience.journeyOrchestration.stepEvents.journeyVersionID='<journeyVersionID>'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour);
```

+++

+++Was geschieht mit einem bestimmten Profil in einer bestimmten Journey in einem bestimmten Zeitrahmen?

Diese Abfrage gibt alle Schrittereignisse und Service-Ereignisse für das angegebene Profil und die Journey für die angegebene Uhrzeit in chronologischer Reihenfolge zurück.

_Data-Lake-Abfrage_

```sql
SELECT
timestamp,
_experience.journeyOrchestration.stepEvents.journeyVersionID,
_experience.journeyOrchestration.stepEvents.profileID,
_experience.journeyOrchestration.stepEvents.nodeName,
_experience.journeyOrchestration.stepEvents.journeyNodeProcessed,
_experience.journeyOrchestration.serviceType,
to_json(_experience.journeyOrchestration.profile),
to_json(_experience.journeyOrchestration.serviceEvents)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID='<journeyVersionID>'
AND DATE(timestamp) > (now() - interval '<last x hours>' hour)
AND
  (
    _experience.journeyOrchestration.stepEvents.profileID='<profileID>'
    OR _experience.journeyOrchestration.profile.ID='<profileID>'
  );
ORDER BY timestamp;
```

+++

+++Wie viel Zeit ist zwischen zwei Knoten verstrichen? 

Diese Abfragen können beispielsweise verwendet werden, um die mit einer Warteaktivität verbrachte Zeit zu schätzen. Dadurch können Sie sicherstellen, dass die Warteaktivität korrekt konfiguriert ist.

_Data-Lake-Abfrage_

```sql
WITH

START_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_START,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of node before wait activity>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
),

END_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_END,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of wait activity node>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
)

SELECT 

    T1.INSTANCE_ID AS INSTANCE_ID,
    T1.NODE_NAME AS START_NODE_NAME,
    T2.NODE_NAME AS END_NODE_NAME,
    DATEDIFF(millisecond,T1.TS_START,T2.TS_END) AS ELAPSED_TIME_MS
    
FROM

    START_NODE_INFO AS T1,
    END_NODE_INFO AS T2
    
WHERE

    T1.INSTANCE_ID = T2.INSTANCE_ID
```

_Data-Lake-Abfrage_

```sql
WITH

START_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_START,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of node before wait activity>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
),

END_NODE_INFO AS (

    SELECT 
    
        timestamp AS TS_END,
        _experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        _experience.journeyOrchestration.stepEvents.instanceID AS INSTANCE_ID
        
    FROM 
    
        journey_step_events
    
    WHERE
    
        _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND
        _experience.journeyOrchestration.stepEvents.nodeName = '<name of wait activity node>' AND
        _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = true
        
)

SELECT 

    AVG(DATEDIFF(millisecond,T1.TS_START,T2.TS_END)) AS AVERAGE_ELAPSED_TIME,
    MIN(DATEDIFF(millisecond,T1.TS_START,T2.TS_END)) AS MIN_ELAPSED_TIME,
    MAX(DATEDIFF(millisecond,T1.TS_START,T2.TS_END)) AS MAX_ELAPSED_TIME
    
FROM

    START_NODE_INFO AS T1,
    END_NODE_INFO AS T2
    
WHERE

    T1.INSTANCE_ID = T2.INSTANCE_ID
```

+++

+++Wie werden die Details eines serviceEvents überprüft? 

Der Journey-Schritt-Ereignis-Datensatz enthält alle stepEvents und serviceEvents. stepEvents werden in Berichten verwendet, denn sie beziehen sich auf Aktivitäten (Ereignisse, Aktionen usw.) von Profilen in einer Journey. serviceEvents werden im selben Datensatz gespeichert und geben zusätzliche Informationen zu Debugging-Zwecken an, z. B. den Grund für die Verwerfung eines Erlebnisereignisses.

Im Folgenden finden Sie ein Beispiel für eine Abfrage, um die Details eines serviceEvents zu überprüfen:

_Data-Lake-Abfrage_

```sql
SELECT

     _experience.journeyOrchestration.profile.ID, 
     _experience.journeyOrchestration.journey.versionID, 
     to_json(_experience.journeyOrchestration.serviceEvents) 

FROM journey_step_event 

WHERE _experience.journeyOrchestration.serviceType is not null;
```

## Nachrichten-/Aktionsfehler {#message-action-errors}

+++Liste aller in Journeys aufgetretenen Fehler

Mithilfe dieser Abfrage können Sie jeden in Journeys aufgetretenen Fehler beim Ausführen einer Nachricht/Aktion auflisten.

```sql
SELECT _experience.journeyOrchestration.stepEvents.actionExecutionError, count(distinct _id) AS ERROR_COUNT 
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.nodeName = '<message-name>'
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>'
GROUP BY _experience.journeyOrchestration.stepEvents.actionExecutionError
ORDER BY ERROR_COUNT DESC;
```

_Beispielausgabe_

| actionExecutionError | ERROR_COUNT |
|---|---|
| Zeitüberschreitung | 145 |
| Verbindungsfehler | 87 |
| InvalidResponse | 23 |

Diese Abfrage gibt alle Fehler zurück, die beim Ausführen einer Aktion auf einer Journey aufgetreten sind, zusammen mit der Anzahl der aufgetretenen Fehler, sortiert nach Häufigkeit.

+++

## Profilbasierte Abfragen {#profile-based-queries}

+++Ermitteln, ob ein Profil in eine bestimmte Journey eingetreten ist

Diese Abfrage prüft, ob ein bestimmtes Profil in eine Journey eingetreten ist, indem die mit dieser Kombination aus Journey und Profil verknüpften Ereignisse gezählt werden.

```sql
SELECT count(distinct _id) AS EVENT_COUNT 
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>';
```

_Beispielausgabe_

| EVENT_COUNT |
|---|
| 3 |

Diese Abfrage gibt die genaue Anzahl der Eintritte eines Profils in eine Journey zurück. Ein Ergebnis größer als 0 bestätigt, dass das Profil auf die Journey gelangt ist.

+++

+++Ermitteln, ob eine bestimmte Nachricht an ein Profil gesendet wurde

Methode 1: Wenn der Name Ihrer Nachricht in der Journey nicht eindeutig ist (er wird an mehreren Stellen verwendet).

```sql
SELECT count(distinct _id) AS MESSAGE_SENT_COUNT 
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.nodeID = '<NodeId in the UI corresponding to the message>' 
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL 
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>';
```

_Beispielausgabe_

| MESSAGE_SENT_COUNT |
|---|
| 1 |

Ein Ergebnis größer als 0 bestätigt, dass die Nachrichtenaktion erfolgreich ausgeführt wurde. Diese Abfrage zeigt nur an, ob die Nachrichtenaktion auf der Journey-Seite erfolgreich ausgeführt wurde.

Methode 2: Wenn der Name Ihrer Nachricht in der Journey eindeutig ist.

```sql
SELECT count(distinct _id) AS MESSAGE_SENT_COUNT 
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.nodeName = '<NodeName in the UI corresponding to the message>' 
AND _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL 
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>';
```

_Beispielausgabe_

| MESSAGE_SENT_COUNT |
|---|
| 1 |

Die Abfrage gibt die Anzahl der erfolgreichen Aufrufe der Nachricht für das ausgewählte Profil zurück.

+++

+++Ermitteln aller Nachrichten, die ein Profil in den letzten 30 Tagen erhalten hat

Diese Abfrage ruft alle innerhalb der letzten 30 Tage erfolgreich ausgeführten Nachrichtenaktionen für ein bestimmtes Profil ab, gruppiert nach Nachrichtenname.

```sql
SELECT _experience.journeyOrchestration.stepEvents.nodeName AS MESSAGE_NAME, 
       count(distinct _id) AS MESSAGE_COUNT 
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL 
AND _experience.journeyOrchestration.stepEvents.nodeType = 'action' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>' 
AND timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName
ORDER BY MESSAGE_COUNT DESC;
```

_Beispielausgabe_

| MESSAGE_NAME | MESSAGE_COUNT |
|---|---|
| Willkommens-E-Mail | 1 |
| Produktempfehlung | 3 |
| Warenkorbabbruch-Erinnerung | 2 |
| Wöchentliche Newsletter | 4 |

Die Abfrage gibt die Liste aller Nachrichten zusammen mit der Anzahl der für das ausgewählte Profil aufgerufenen Nachrichten zurück.

+++

+++Ermitteln aller Journeys, in die ein Profil in den letzten 30 Tagen eingetreten ist

Diese Abfrage gibt alle Journeys zurück, in die ein bestimmtes Profil in den letzten 30 Tagen eingetreten ist, sowie die Anzahl der Eintritte für jede Journey.

```sql
SELECT _experience.journeyOrchestration.stepEvents.journeyVersionName AS JOURNEY_NAME, 
       count(distinct _id) AS ENTRY_COUNT 
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.nodeType = 'start' 
AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID corresponding to the namespace used>' 
AND timestamp > (now() - interval '30' day)
GROUP BY _experience.journeyOrchestration.stepEvents.journeyVersionName
ORDER BY ENTRY_COUNT DESC;
```

_Beispielausgabe_

| JOURNEY_NAME | ENTRY_COUNT |
|---|---|
| Begrüßungs-Journey v2 | 1 |
| Produkt Recommendations | 5 |
| Rückgewinnungskampagne | 2 |

Die Abfrage gibt die Liste aller Journey-Namen sowie die Anzahl der Eintritte des abgefragten Profils pro Journey zurück.

+++

+++Anzahl der Profile, die sich täglich für eine Journey qualifiziert haben

Diese Abfrage stellt eine tägliche Aufschlüsselung der Anzahl der individuellen Profile bereit, die in einem bestimmten Zeitraum in eine Journey eingetreten sind.

```sql
SELECT DATE(timestamp) AS ENTRY_DATE, 
       count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS PROFILES_COUNT 
FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '<last x days>' day)
AND _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>'
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) DESC;
```

_Beispielausgabe_

| ENTRY_DATE | PROFILES_COUNT |
|---|---|
| 25.11.2024 | 1.245 |
| 24.11.2024 | 1.189 |
| 23.11.2024 | 15.340 |
| 22.11.2024 | 1.205 |
| 21.11.2024 | 1.167 |

Die Abfrage gibt für den definierten Zeitraum die Anzahl der Profile zurück, die täglich in die Journey eingetreten sind. Wenn ein Profil über mehrere Identitäten eingetreten ist, wird es zweimal gezählt. Wenn der erneute Eintritt aktiviert ist, kann die Profilanzahl über verschiedene Tage hinweg dupliziert werden, wenn das Profil an einem anderen Tag erneut auf die Journey gelangt ist.

Erfahren Sie, wie Sie [Fehler bei verworfenen Ereignistypen in journey_step_events beheben](../reports/sharing-field-list.md#discarded-events).


+++

## Abfragen im Zusammenhang mit „Zielgruppe lesen“ {#read-segment-queries}

+++Dauer bis zum Fertigstellen eines Zielgruppenexportauftrags

Diese Abfrage berechnet die Dauer eines Zielgruppenexportvorgangs, indem sie die Zeitdifferenz zwischen dem Zeitpunkt, zu dem der Auftrag in die Warteschlange gestellt wurde, und dem Zeitpunkt des Auftragsabschlusses ermittelt.

```sql
select DATEDIFF (minute,
              (select timestamp
                where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.status = 'queued') ,
              (select timestamp
                where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.status = 'finished')) AS export_job_runtime;
```

Die Abfrage gibt die Zeitdifferenz in Minuten zurück, die zwischen dem Zeitpunkt liegt, zu dem der Zielgruppenexportauftrag in die Warteschlange gestellt wurde, und dem Zeitpunkt, zu dem er beendet wurde.

+++

+++Anzahl der Profile, die von der Journey verworfen wurden, weil sie Duplikate waren

Diese Abfrage zählt die Anzahl der individuellen Profile, die aufgrund von Fehlern bei der Instanzduplizierung während der Aktivität „Zielgruppe lesen“ verworfen wurden.

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_DUPLICATION'
```

Die Abfrage gibt alle Profil-IDs zurück, die von der Journey verworfen wurden, da es sich um Duplikate handelte.

+++

+++Anzahl der Profile, die von der Journey aufgrund eines ungültigen Namespace verworfen wurden

Diese Abfrage gibt die Anzahl der Profile zurück, die verworfen wurden, weil sie einen ungültigen Namespace oder keine Identität für den erforderlichen Namespace hatten.

```sql
SELECT count(*) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_BAD_NAMESPACE'
```

Die Abfrage gibt alle Profil-IDs zurück, die von der Journey verworfen wurden, da sie einen ungültigen Namespace oder keine Kennung für diesen Namespace hatten.

+++

+++Anzahl der Profile, die von der Journey verworfen wurden, weil keine Identitätszuordnung vorhanden war

Diese Abfrage zählt die Profile, die verworfen wurden, weil ihnen eine für die Journey-Ausführung erforderliche Identitätszuordnung fehlte.

```sql
SELECT count(*) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_NO_IDENTITY_MAP'
```

Die Abfrage gibt alle Profil-IDs zurück, die von der Journey verworfen wurden, da die Identitätszuordnung fehlte.

+++

+++Anzahl der Profile, die von der Journey verworfen wurden, weil sich die Journey im Testmodus befand und das Profil kein Testprofil war

Diese Abfrage identifiziert Profile, die verworfen wurden, als die Journey im Testmodus ausgeführt wurde, aber das Attribut „testProfile“ für das Profil nicht auf „wahr“ eingestellt war.

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_NOT_A_TEST_PROFILE'
```

Die Abfrage gibt die IDs aller Profile zurück, die von der Journey verworfen wurden, da der Exportauftrag im Testmodus ausgeführt wurde, aber das Attribut „testProfile“ für das Profil nicht auf „wahr“ eingestellt war.

+++

+++Anzahl der Profile, die von der Journey aufgrund eines internen Fehlers verworfen wurden

Diese Abfrage gibt die Anzahl der Profile zurück, die aufgrund interner Systemfehler während der Journey-Ausführung verworfen wurden.

```sql
SELECT count(distinct _experience.journeyOrchestration.profile.ID) FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
_experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode = 'ERROR_INSTANCE_INTERNAL'
```

Die Abfrage gibt alle Profil-IDs zurück, die von der Journey aufgrund eines internen Fehlers verworfen wurden.

+++

+++Überblick über „Zielgruppe lesen“ für eine bestimmte Journey-Version

Diese Abfrage bietet einen umfassenden Überblick über die Aktivität „Zielgruppe lesen“, einschließlich Details zum Segmentexportauftrag, Ereignis-Codes, Status und Profilanzahl für alle Phasen des Zielgruppenexportvorgangs.

_Data-Lake-Abfrage_

```sql
SELECT
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode           AS EVENT_CODE,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportSegmentID     AS SEGMENT_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID                  AS EXPORTJOB_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.status              AS EXPORTJOB_STATUS,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal    AS TOTAL_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized AS SUCCESS_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed   AS FAILED_EXPORTED_PROFILES_COUNT
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator'
```

Es werden alle Service-Ereignisse im Zusammenhang mit der angegebenen Journey-Version zurückgegeben. Dabei kann auch die Abfolge der Vorgänge nachvollzogen werden:

* Erstellung des Themas
* Erstellung von Exportaufträgen
* Beendigung der Exportaufträge (mit Metriken zu exportierten Profilen)
* Abbruch der Worker-Verarbeitung

Zusätzlich können Probleme identifiziert werden wie z. B.:

* Fehler bei der Erstellung des Themas oder Exportvorgangs (einschließlich Zeitüberschreitungen bei API-Aufrufen zum Zielgruppenexport)
* Blockierte Exportaufträge (wenn für eine bestimmte Journey-Version kein Ereignis zur Beendigung des Exportauftrags vorhanden ist)
* Worker-Probleme, wenn ein Beendigungsereignis zum Exportauftrag, aber kein Beendigungsereignis zur Worker-Verarbeitung empfangen wurde.

WICHTIG: Wenn von dieser Abfrage kein Ereignis zurückgegeben wird, kann dies einen der folgenden Gründe haben:

* Die Journey-Version hat die Planung nicht erreicht.
* Die Journey-Version hätte den Exportauftrag durch Aufruf des Orchestrators auslösen sollen, aber im vorgelagerten Fluss ist ein Fehler aufgetreten: Problem bei der Journey-Bereitstellung, mit dem Geschäftsereignis oder mit der Planung.

+++


+++Abrufen von Fehlern des Typs „Zielgruppe lesen“ für eine bestimmte Journey-Version

Diese Abfrage filtert nach bestimmten Fehlerereignis-Codes im Zusammenhang mit Fehlern beim Lesen von Zielgruppen, z. B. Fehler bei der Themenerstellung, API-Aufruffehler, Timeouts und fehlgeschlagene Exportaufträge.

_Data-Lake-Abfrage_

```sql
SELECT
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode           AS EVENT_CODE,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportSegmentID     AS SEGMENT_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID                  AS EXPORTJOB_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.status              AS EXPORTJOB_STATUS,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal    AS TOTAL_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized AS SUCCESS_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed   AS FAILED_EXPORTED_PROFILES_COUNT
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
        'ERROR_TOPIC_CREATION',
        'ERROR_EXPORTJOB_APICALL',
        'ERROR_EXPORTJOB_APICALL_TIMEOUT',
        'ERROR_EXPORTJOB_FAILED'
    )
```

+++

+++Abrufen des Verarbeitungsstatus für Exportaufträge

Diese Abfrage ruft den Verarbeitungsstatus von Zielgruppenexportaufträge ab und zeigt an, ob sie erfolgreich waren oder fehlgeschlagen sind, zusammen mit Profilexportmetriken.

_Data-Lake-Abfrage_

```sql
SELECT
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode           AS EVENT_CODE,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportSegmentID     AS SEGMENT_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID                  AS EXPORTJOB_ID,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.status              AS EXPORTJOB_STATUS,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal    AS TOTAL_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized AS SUCCESS_EXPORTED_PROFILES_COUNT,
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed   AS FAILED_EXPORTED_PROFILES_COUNT 
FROM
    journey_step_events
WHERE
    _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
    _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
        'INFO_EXPORTJOB_SUCCEEDED',
        'ERROR_EXPORTJOB_FAILED'
    )
```

Wenn kein Eintrag zurückgegeben wird, bedeutet dies, dass

* bei der Erstellung des Themas oder des Exportauftrags ein Fehler aufgetreten ist
* der Exportauftrag noch ausgeführt wird

+++

+++Abrufen von Metriken zu exportierten Profilen, einschließlich Verwerfen-Aktionen und Exportauftragsmetriken für die einzelnen Exportaufträge

Diese Abfrage kombiniert die Anzahl verworfener Profile mit den Metriken des Exportauftrags, um eine vollständige Ansicht der Leistung des Zielgruppenexports für jeden einzelnen Exportvorgang zu bieten.

_Data-Lake-Abfrage_

```sql
WITH
  
DISCARDED_EXPORTED_PROFILES AS (
  
    SELECT
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID AS EXPORTJOB_ID,
        count(distinct _experience.journeyOrchestration.profile.ID) AS DISCARDED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'ERROR_INSTANCE_DUPLICATION',
            'ERROR_INSTANCE_BAD_NAMESPACE',
            'ERROR_INSTANCE_NO_IDENTITY_MAP',
            'ERROR_INSTANCE_NOT_A_TEST_PROFILE',
            'ERROR_INSTANCE_INTERNAL'
        )
    GROUP BY
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID
 
),
  
SEGMENT_EXPORT_METRICS AS (
  
    SELECT
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID AS EXPORTJOB_ID,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal) AS TOTAL_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized) AS SUCCESS_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed) AS FAILED_EXPORTED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'INFO_EXPORTJOB_SUCCEEDED',
            'ERROR_EXPORTJOB_FAILED'
        )
    GROUP BY
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.ID
  
)
  
SELECT
    sum(T2.TOTAL_EXPORTED_PROFILES_COUNT),
    sum(T2.SUCCESS_EXPORTED_PROFILES_COUNT),
    sum(T2.FAILED_EXPORTED_PROFILES_COUNT),
    sum(T1.DISCARDED_PROFILES_COUNT)
FROM
    DISCARDED_EXPORTED_PROFILES AS T1,
    SEGMENT_EXPORT_METRICS AS T2
WHERE T1.EXPORTJOB_ID = T2.EXPORTJOB_ID
```

+++

+++Abrufen aggregierter Metriken (Zielgruppenexportaufträge und Verwerfen-Aktionen) für alle Exportaufträge

Diese Abfrage aggregiert allgemeine Metriken für alle Exportaufträge für eine bestimmte Journey-Version. Dies ist nützlich für wiederkehrende Journeys oder Journeys mit Themenwiederverwendung, die durch Geschäftsereignisse ausgelöst werden.

_Data-Lake-Abfrage_

```sql
WITH
  
DISCARDED_EXPORTED_PROFILES AS (
  
    SELECT
        _experience.journeyOrchestration.journey.versionID AS JOURNEYVERSION_ID,
        count(distinct _experience.journeyOrchestration.profile.ID) AS DISCARDED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'ERROR_INSTANCE_DUPLICATION',
            'ERROR_INSTANCE_BAD_NAMESPACE',
            'ERROR_INSTANCE_NO_IDENTITY_MAP',
            'ERROR_INSTANCE_NOT_A_TEST_PROFILE',
            'ERROR_INSTANCE_INTERNAL'
        )
    GROUP BY
        _experience.journeyOrchestration.journey.versionID
),
  
SEGMENT_EXPORT_METRICS AS (
  
    SELECT
        _experience.journeyOrchestration.journey.versionID AS JOURNEYVERSION_ID,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountTotal) AS TOTAL_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountRealized) AS SUCCESS_EXPORTED_PROFILES_COUNT,
        sum(_experience.journeyOrchestration.serviceEvents.segmentExportJob.exportCountFailed) AS FAILED_EXPORTED_PROFILES_COUNT
    FROM
        journey_step_events
    WHERE
        _experience.journeyOrchestration.journey.versionID = '<journey-version-id>' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventType = 'segmenttrigger-orchestrator' AND
        _experience.journeyOrchestration.serviceEvents.segmentExportJob.eventCode IN (
            'INFO_EXPORTJOB_SUCCEEDED',
            'ERROR_EXPORTJOB_FAILED'
        )
    GROUP BY
          _experience.journeyOrchestration.journey.versionID
 
)
  
SELECT
    sum(T2.TOTAL_EXPORTED_PROFILES_COUNT),
    sum(T2.SUCCESS_EXPORTED_PROFILES_COUNT),
    sum(T2.FAILED_EXPORTED_PROFILES_COUNT),
    sum(T1.DISCARDED_PROFILES_COUNT)
FROM
    DISCARDED_EXPORTED_PROFILES AS T1,
    SEGMENT_EXPORT_METRICS AS T2
WHERE T1.JOURNEYVERSION_ID = T2.JOURNEYVERSION_ID
```

Diese Abfrage unterscheidet sich von der vorherigen.

Es werden die Gesamtmetriken für eine bestimmte Journey-Version zurückgegeben, unabhängig von den Aufträgen, die dafür ausgeführt wurden (bei wiederkehrenden Journeys lösten Geschäftsereignisse diejenigen aus, die eine erneute Verwendung von Themen nutzten).

+++

## Abfragen im Zusammenhang mit der Zielgruppen-Qualifizierung {#segment-qualification-queries}

+++Profil verworfen, da eine andere als die konfigurierte Zielgruppe realisiert wurde

Diese Abfrage identifiziert Profile, die verworfen wurden, weil ihr Zielgruppen-Realisierungsstatus nicht mit der Zielgruppen-Qualifizierungskonfiguration der Journey übereinstimmte (z. B. wenn das Profil für „Eintritte“ konfiguriert ist, aber „ausgestiegen“ ist).

_Data-Lake-Abfrage_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID
FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = '<journey-version id>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SEGMENT_REALISATION_CONDITION_MISMATCH'
```

_Beispiel_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID
FROM journey_step_events
where
_experience.journeyOrchestration.journey.versionID = 'a868f3c9-4888-46ac-a274-94cdf1c4159d' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SEGMENT_REALISATION_CONDITION_MISMATCH'
```

Diese Abfrage gibt alle Profil-IDs zurück, die von der Journey-Version aufgrund einer falschen Zielgruppenrealisierung verworfen wurden.

+++

+++Zielgruppen-Qualifizierungsereignisse, die aus einem anderen Grund für ein bestimmtes Profil verworfen wurden

Diese Abfrage ruft alle Zielgruppen-Qualifizierungs- oder externen Ereignisse ab, die für ein bestimmtes Profil aufgrund von internen Service-Fehlern verworfen wurden.

_Data-Lake-Abfrage_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID, _experience.journeyOrchestration.serviceEvents.dispatcher.projectionID
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID = '<profile-id>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

_Beispiel_

```sql
SELECT DATE(timestamp),  _experience.journeyOrchestration.profile.ID, _experience.journeyOrchestration.serviceEvents.dispatcher.projectionID
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID = 'mandee@adobe.com' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

Diese Abfrage gibt alle Ereignisse (externe Ereignisse/Zielgruppen-Qualifizierungsereignisse) zurück, die aus einem anderen Grund für ein Profil verworfen wurden.

+++

## Ereignisbasierte Abfragen {#event-based-queries}

+++Überprüfung, ob ein Geschäftsereignis für eine Journey empfangen wurde

Diese Abfrage zählt, wie oft ein Geschäftsereignis in einem bestimmten Zeitraum von einer Journey empfangen wurde, und gruppiert die Ausgabe nach Datum.

```sql
SELECT DATE(timestamp), count(distinct _id)
FROM journey_step_events
where
_experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-version-id>' AND
_experience.journeyOrchestration.stepEvents.nodeName = '<node-name-corresponding-to-business-event>' AND
_experience.journeyOrchestration.stepEvents.nodeType = 'start' AND
WHERE DATE(timestamp) > (now() - interval '<last x hours>' hour)
```

+++

+++Überprüfung, ob ein externes Ereignis eines Profils verworfen wurde, weil keine zugehörige Journey gefunden wurde

Diese Abfrage identifiziert, wann ein externes Ereignis für ein bestimmtes Profil verworfen wurde, da keine aktive oder passende Journey für den Empfang dieses Ereignisses konfiguriert war.

```sql
SELECT _experience.journeyOrchestration.profile.ID, DATE(timestamp) FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.dispatcher.eventID = '<eventId>' AND
_experience.journeyOrchestration.profile.ID = '<profileID>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'EVENT_WITH_NO_JOURNEY'
```

Erfahren Sie, wie Sie [Fehler bei verworfenen Ereignistypen in journey_step_events beheben](../reports/sharing-field-list.md#discarded-events).

+++

+++Überprüfung, ob ein externes Ereignis eines Profils aus einem anderen Grund verworfen wurde

Diese Abfrage ruft externe Ereignisse ab, die für ein bestimmtes Profil aufgrund von internen Service-Fehlern verworfen wurden, sowie die Ereignis-ID und den Fehler-Code.

```sql
SELECT _experience.journeyOrchestration.profile.ID, DATE(timestamp), _experience.journeyOrchestration.serviceEvents.dispatcher.eventID, _experience.journeyOrchestration.serviceEvents.dispatcher.eventCode
FROM journey_step_events
where
_experience.journeyOrchestration.profile.ID='<profileID>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventID='<eventID>' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventCode = 'discard' AND
_experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'ERROR_SERVICE_INTERNAL';
```

Erfahren Sie, wie Sie [Fehler bei verworfenen Ereignistypen in journey_step_events beheben](../reports/sharing-field-list.md#discarded-events).

+++

+++Überprüfung der Anzahl aller von stateMachine verworfenen Ereignisse nach errorCode

Diese Abfrage aggregiert alle Ereignisse, die vom Journey-Status-Computer verworfen wurden, gruppiert nach Fehler-Code, damit die häufigsten Gründe für das Verwerfen ermittelt werden können.

```sql
SELECT _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode, COUNT() FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'discard' GROUP BY _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode
```

Erfahren Sie, wie Sie [Fehler bei verworfenen Ereignistypen in journey_step_events beheben](../reports/sharing-field-list.md#discarded-events).

+++

+++Überprüfung aller verworfenen Ereignisse, bei denen ein Wiedereintritt nicht erlaubt war

Diese Abfrage identifiziert alle Ereignisse, die verworfen wurden, da ein Profil versucht hat, erneut in eine Journey einzutreten, obwohl der erneute Eintritt laut Journey-Konfiguration nicht zulässig war.

```sql
SELECT DATE(timestamp), _experience.journeyOrchestration.profile.ID,
_experience.journeyOrchestration.journey.versionID,
_experience.journeyOrchestration.serviceEvents.stateMachine.eventCode 
FROM journey_step_events
where
_experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'discard' AND _experience.journeyOrchestration.serviceEvents.stateMachine.eventCode='reentranceNotAllowed'
```

Erfahren Sie, wie Sie [Fehler bei verworfenen Ereignistypen in journey_step_events beheben](../reports/sharing-field-list.md#discarded-events).

+++

## Abfragen für kontaktierbare Profile {#engageable-profiles-queries}

Mit diesen Abfragen können Sie die Anzahl Ihrer Engageable Profile überwachen und analysieren. Ein Ansprechbares Profil ist ein eindeutiges Profil, das in den letzten 12 Monaten über Journey oder Kampagnen interagiert hat. Erfahren Sie mehr über [Engageable Profiles und Lizenznutzung](../audience/license-usage.md#what-is-engageable-profile).

>[!IMPORTANT]
>
>**Best Practices für die Abfrage von ansprechbaren Profilen:**
>* Stellen Sie sicher, dass jedes Nicht-Aggregatfeld in der `GROUP BY` enthalten ist
>* Verweisen auf Datensätze, die nicht in der Sandbox vorhanden sind, vermeiden - Bestätigen von Datensatznamen in der Platform-Benutzeroberfläche
>* Verwenden Sie `distinct` beim Zählen eindeutiger Profile, um Duplikate über Identity-Namespaces hinweg zu vermeiden
>* Wenn Sie `LIMIT` verwenden, platzieren Sie sie nach `ORDER BY` Klauseln am Ende der Abfrage

+++Anzahl der eindeutigen Profile, an die eine bestimmte Journey beteiligt ist

Diese Abfrage gibt die Anzahl der eindeutigen Profile zurück, die von einer bestimmten Journey kontaktiert wurden, was zu Ihrer Anzahl von kontaktierbaren Profilen beiträgt.

```sql
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS ENGAGED_PROFILES
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
AND timestamp > (now() - interval '12' month);
```

Diese Abfrage hilft Ihnen zu verstehen, wie viele eindeutige Profile eine bestimmte Journey in den letzten 12 Monaten zu Ihrer [Engageable Profiles](../audience/license-usage.md)-Anzahl beigetragen hat.

+++

+++Anzahl der in den letzten 12 Monaten pro Journey eingesetzten Profile

Diese Abfrage zeigt die Anzahl der eindeutigen Profile an, die von jeder Journey in Ihrem Unternehmen in den letzten 12 Monaten kontaktiert wurden. So können Sie ermitteln, welche Journey am meisten zu Ihrer [Engageable Profiles“ &#x200B;](../audience/license-usage.md).

```sql
SELECT 
    _experience.journeyOrchestration.stepEvents.journeyVersionID AS JOURNEY_VERSION_ID,
    _experience.journeyOrchestration.stepEvents.journeyVersionName AS JOURNEY_NAME,
    count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS ENGAGED_PROFILES
FROM journey_step_events
WHERE timestamp > (now() - interval '12' month)
GROUP BY 
    _experience.journeyOrchestration.stepEvents.journeyVersionID,
    _experience.journeyOrchestration.stepEvents.journeyVersionName
ORDER BY ENGAGED_PROFILES DESC;
```

_Beispielausgabe_

| JOURNEY_VERSION_ID | JOURNEY_NAME | ENGAGED_PROFILES |
|---|---|---|
| 67b14482-143e-4f83-9cf5-cfec0fca3d26 | Willkommen bei Campaign v2 | 125.450 |
| A3C21B89-456D-4E21-B8F3-9A8E7C6D5432 | Journey zur Produkteinführung | 98.230 |
| F9E8D7C6-B5A4-3210-9876-543210FEDCBA | Rückgewinnungsfluss | 45.670 |

Diese Ausgabe hilft Ihnen zu ermitteln, welche Journey am meisten mit Profilen interagieren, und trägt am deutlichsten zur Anzahl der „Interaktionsfähigen Profile“ bei.

>[!NOTE]
>
>Diese Abfrage gruppiert nach `journeyVersionID` und `journeyVersionName`. Beide Felder müssen in der `GROUP BY`-Klausel enthalten sein, da sie in der Abfrage ausgewählt sind. Wenn Felder in der `GROUP BY`-Klausel weggelassen werden, schlägt die Abfrage fehl.

+++

+++Anzahl der Profile, die von Journey in den letzten 30 Tagen täglich kontaktiert wurden

Diese Abfrage liefert eine tägliche Aufschlüsselung der neu interagierenden Profile und hilft Ihnen, Spitzen in der Anzahl [Interaktionsfähigen Profile](../audience/license-usage.md) zu identifizieren.

```sql
SELECT 
    DATE(timestamp) AS ENGAGEMENT_DATE,
    count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS ENGAGED_PROFILES
FROM journey_step_events
WHERE timestamp > (now() - interval '30' day)
GROUP BY DATE(timestamp)
ORDER BY ENGAGEMENT_DATE DESC;
```

_Beispielausgabe_

| ENGAGEMENT_DATE | ENGAGED_PROFILES |
|---|---|
| 25.11.2024 | 8.450 |
| 24.11.2024 | 7.820 |
| 23.11.2024 | 125.340 |
| 22.11.2024 | 9.230 |
| 21.11.2024 | 8.670 |

Mit dieser Ausgabe können Sie tägliche Trends überwachen und erkennen, wann eine große Anzahl von Profilen interagiert. In diesem Beispiel zeigt der 23. November eine signifikante Spitze (125.340 Profile) im Vergleich zur typischen täglichen Interaktion (ca. 8.000 Profile), die eine Untersuchung rechtfertigen würde, um zu verstehen, was Journey oder Kampagne die Zunahme der Anzahl Ihrer [Engageable Profiles“ verursacht &#x200B;](../audience/license-usage.md).

+++

+++Identifizieren von Journey, die kürzlich große Zielgruppen angesprochen haben

Diese Abfrage hilft dabei, festzustellen, welche Journey in den letzten Zeiträumen mit einer großen Anzahl neuer Profile interagiert haben, was einen plötzlichen Anstieg der Anzahl [Engageable Profiles“ &#x200B;](../audience/license-usage.md) kann.

```sql
SELECT 
    _experience.journeyOrchestration.stepEvents.journeyVersionID AS JOURNEY_VERSION_ID,
    _experience.journeyOrchestration.stepEvents.journeyVersionName AS JOURNEY_NAME,
    DATE(timestamp) AS ENGAGEMENT_DATE,
    count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS ENGAGED_PROFILES
FROM journey_step_events
WHERE timestamp > (now() - interval '7' day)
AND _experience.journeyOrchestration.stepEvents.nodeType = 'start'
GROUP BY 
    _experience.journeyOrchestration.stepEvents.journeyVersionID,
    _experience.journeyOrchestration.stepEvents.journeyVersionName,
    DATE(timestamp)
HAVING count(distinct _experience.journeyOrchestration.stepEvents.profileID) > 1000
ORDER BY ENGAGEMENT_DATE DESC, ENGAGED_PROFILES DESC;
```

_Beispielausgabe_

| JOURNEY_VERSION_ID | JOURNEY_NAME | ENGAGEMENT_DATE | ENGAGED_PROFILES |
|---|---|---|---|
| 67b14482-143e-4f83-9cf5-cfec0fca3d26 | Black Friday Campaign | 23.11.2024 | 125.340 |
| A3C21B89-456D-4E21-B8F3-9A8E7C6D5432 | Journey zur Produkteinführung | 22.11.2024 | 45.230 |
| F9E8D7C6-B5A4-3210-9876-543210FEDCBA | Weihnachts-Newsletter | 21.11.2024 | 32.150 |

Diese Abfrage filtert nach Journey, die in den letzten sieben Tagen mehr als 1.000 Profile pro Tag kontaktiert haben. Die Ausgabe zeigt, welche Journey und Daten für große Profilinteraktionen verantwortlich sind. Passen Sie den Schwellenwert der `HAVING` entsprechend Ihren Anforderungen an (ändern Sie z. B. `> 1000` für größere Schwellenwerte in `> 10000`).

+++

+++Gesamtzahl der eindeutigen Profile, die in den letzten 12 Monaten für alle Journey interagiert haben

Diese Abfrage liefert eine Anzahl der eindeutigen Profile, die in den letzten 12 Monaten für alle Journey interagiert haben, und gibt Ihnen einen Überblick über Ihre Journey-basierte Interaktion.

```sql
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID) AS TOTAL_ENGAGED_PROFILES
FROM journey_step_events
WHERE timestamp > (now() - interval '12' month);
```

_Beispielausgabe_

| TOTAL_ENGAGED_PROFILES |
|---|
| 2.547.890 |

Diese einzelne Zahl stellt die Gesamtzahl der eindeutigen Profile dar, die in den letzten 12 Monaten von mindestens einer Journey kontaktiert wurden.

>[!NOTE]
>
>Diese Abfrage zählt verschiedene Profil-IDs im Journey-Schritt-Ereignis-Datensatz. Die tatsächliche Anzahl der kontaktierbaren Profile, die im Dashboard [Lizenznutzung“ angezeigt wird](../audience/license-usage.md) kann leicht abweichen, da sie auch Profile umfasst, die über Kampagnen und andere Journey Optimizer-Funktionen als Journey interagieren.

+++

## Häufige Journey-basierte Abfragen {#journey-based-queries}

+++Anzahl der täglich aktiven Journeys

Diese Abfrage gibt eine tägliche Anzahl der individuellen Journey-Versionen mit Aktivität zurück, damit Sie die Ausführungsmuster von Journeys im Zeitverlauf besser verstehen.

```sql
SELECT DATE(timestamp) AS ACTIVITY_DATE, 
       count(distinct _experience.journeyOrchestration.stepEvents.journeyVersionID) AS ACTIVE_JOURNEYS
FROM journey_step_events
WHERE DATE(timestamp) > (now() - interval '<last x days>' day)
GROUP BY DATE(timestamp)
ORDER BY DATE(timestamp) DESC;
```

_Beispielausgabe_

| ACTIVITY_DATE | ACTIVE_JOURNEY |
|---|---|
| 25.11.2024 | 12 |
| 24.11.2024 | 15 |
| 23.11.2024 | 14 |
| 22.11.2024 | 11 |
| 21.11.2024 | 13 |

Die Abfrage gibt für den definierten Zeitraum die Anzahl der eindeutigen Journeys zurück, die jeden Tag ausgelöst wurden. Eine einzelne Journey, die an mehreren Tagen ausgelöst wird, wird einmal pro Tag gezählt.


+++

## Abfragen auf Journey-Instanzen {#journey-instances-queries}

+++Anzahl der Profile in einem bestimmten Status zu einer bestimmten Zeit

Diese Abfrage verwendet Common Table Expressions (CTEs), um Profile zu identifizieren, die derzeit an einem bestimmten Knoten in einer Journey warten, indem sie nach Profilen sucht, die den Knoten passiert, aber noch nicht zu den nächsten Knoten gewechselt haben.

_Data-Lake-Abfrage_

```sql
WITH
 
INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS (
 
    SELECT
        STEP_EVENTS.timestamp AS TS,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID AS ID
    FROM
        journey_step_events AS STEP_EVENTS
    WHERE
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = '<journey version name>'
 
),
 
INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS (
 
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME = '<specific node name>' AND
        <filter on time for profile in specific node>
 
),
 
INSTANCES_PASSED_IN_NEXT_NODES AS (
     
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME in (<list of next node names from the specific node>)
 
),
 
INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS (
 
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1
 
    EXCEPT
     
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NEXT_NODES AS T1
 
)
 
SELECT
    DATE_FORMAT(T1.TS,'<date pattern>') AS DATETIME,
    count(T1.ID) AS INSTANCES_COUNT
FROM
    INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1,
    INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS T2
WHERE
    T1.ID = T2.ID
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

_Beispiel_

```sql
WITH
 
INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS (
 
    SELECT
        STEP_EVENTS.timestamp AS TS,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID AS ID
    FROM
        journey_step_events AS STEP_EVENTS
    WHERE
        STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = 'Journey20009'
 
),
 
INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS (
 
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME = 'slack_bso_tests - test1' AND
        T1.TS > (now() - interval '18 hour')
 
),
 
INSTANCES_PASSED_IN_NEXT_NODES AS (
     
    SELECT
        T1.TS AS TS,
        T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_ALL_NODES_WITH_DETAILS AS T1
    WHERE
        T1.NODE_NAME in ('slack_bso_tests - test2')
 
),
 
INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS (
 
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1
 
    EXCEPT
     
    SELECT
        distinct T1.ID AS ID
    FROM
        INSTANCES_PASSED_IN_NEXT_NODES AS T1
 
)
 
SELECT
    DATE_FORMAT(T1.TS,'yyyy/MM/dd HH:mm') AS DATETIME,
    count(T1.ID) AS INSTANCES_COUNT
FROM
    INSTANCES_PASSED_IN_NODE_WITH_DETAILS AS T1,
    INSTANCES_PASSED_IN_NODE_NOT_PASSED_IN_NODES AS T2
WHERE
    T1.ID = T2.ID
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

+++

+++Anzahl der Profile, die in einem bestimmten Zeitraum aus der Journey austraten

Diese Abfrage zählt die Journey-Instanzen, die während eines bestimmten Zeitraums beendet wurden, einschließlich der Beendigungen aufgrund von Abschlüssen, Fehlern, Timeouts oder Begrenzungsfehlern.

_Data-Lake-Abfrage_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = '<journey version name>' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    <timestamp filter>
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

_Beispiel_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = 'Journey20009' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    STEP_EVENTS.timestamp > (now() - interval '22 hour')
GROUP BY
    DATETIME
ORDER BY
    DATETIME DESC
```

+++

+++Anzahl der Profile, die in einem bestimmten Zeitraum mit einem bestimmten Knoten/Status aus der Journey austraten

Diese Abfrage bietet eine detaillierte Aufschlüsselung der Journey-Ausstiege, wobei der Knotenname und der Ausstiegsstatus für jede beendete Instanz angezeigt werden, um zu ermitteln, wo und warum Profile die Journey verlassen haben.

_Data-Lake-Abfrage_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus AS EXIT_STATUS,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = '<journey version name>' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    <timestamp filter>
GROUP BY
    DATETIME, NODE_NAME, EXIT_STATUS
ORDER BY
    DATETIME DESC
```

_Beispiel_

```sql
SELECT
    DATE_FORMAT(STEP_EVENTS.timestamp,'yyyy/MM/dd HH:mm') AS DATETIME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.nodeName AS NODE_NAME,
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus AS EXIT_STATUS,
    count(STEP_EVENTS._experience.journeyOrchestration.stepEvents.instanceID) AS EXITED_INSTANCES_COUNT
FROM
    journey_step_events AS STEP_EVENTS
WHERE
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.journeyVersionName = 'Journey20009' AND
    STEP_EVENTS._experience.journeyOrchestration.stepEvents.stepStatus in ('endStep', 'error', 'timedOut', 'cappingError') AND
    STEP_EVENTS.timestamp > (now() - interval '22 hour')
GROUP BY
    DATETIME, NODE_NAME, EXIT_STATUS
ORDER BY
    DATETIME DESC
```

+++

## Abfragen im Zusammenhang mit Leistungsmetriken für benutzerdefinierte Aktionen {#query-custom-action}

+++ Gesamtzahl erfolgreicher Aufrufe, Fehler und Anfragen pro Sekunde an jedem Endpunkt über einen bestimmten Zeitraum

Diese Abfrage liefert Leistungsmetriken für benutzerdefinierte HTTP-Aktionen, einschließlich Gesamtzahl der Aufrufe, erfolgreiche Aufrufe, Anzahl der Fehler nach Typ (4xx, 5xx, Timeouts, Begrenzungen) und Durchsatz in Anfragen pro Sekunde für jeden Endpunkt.

_Data-Lake-Abfrage_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS TOTAL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL THEN 1 END) AS SUCCESSFUL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '4%' THEN 1 END) AS "4xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '5%' THEN 1 END) AS "5xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'timedout' THEN 1 END) AS TIMEOUTS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' THEN 1 END) AS CAPPED_CALLS,
    ROUND(COUNT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime) / 
        COUNT(DISTINCT DATE_TRUNC('second', _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime)), 0) AS THROUGHPUT_RPS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    (<actionExecutionOriginStartTime filter> OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND <timestamp filter>))
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

_Beispiel_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS TOTAL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL THEN 1 END) AS SUCCESSFUL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '4%' THEN 1 END) AS "4xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '5%' THEN 1 END) AS "5xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'timedout' THEN 1 END) AS TIMEOUTS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' THEN 1 END) AS CAPPED_CALLS,
    ROUND(COUNT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime) / 
        COUNT(DISTINCT DATE_TRUNC('second', _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime)), 0) AS THROUGHPUT_RPS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    (_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day) OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND timestamp > (now() - interval '1' day)))
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

+++

+++ Zeitreihe erfolgreicher Aufrufe, Fehler und Durchsätze an jedem Endpunkt über einen bestimmten Zeitraum

Diese Abfrage liefert dieselben Leistungsmetriken wie die vorherige Abfrage, ist jedoch als Zeitreihe organisiert. Sie zeigt mit minutengenauer Granularität auf, wie sich die Endpunktleistung im Zeitverlauf verändert.

_Data-Lake-Abfrage_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    DATE_FORMAT(COALESCE(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, timestamp), 'yyyy/MM/dd HH:mm') AS SPAN,
    COUNT(1) AS TOTAL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL THEN 1 END) AS SUCCESSFUL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '4%' THEN 1 END) AS "4xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '5%' THEN 1 END) AS "5xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'timedout' THEN 1 END) AS TIMEOUTS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' THEN 1 END) AS CAPPED_CALLS,
    ROUND(COUNT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime) / 
        COUNT(DISTINCT DATE_TRUNC('second', _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime)), 0) AS THROUGHPUT_RPS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    (<actionExecutionOriginStartTime filter> OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND
           <timestamp filter>))
GROUP BY 
    ENDPOINT, SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

_Beispiel_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    DATE_FORMAT(COALESCE(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, timestamp), 'yyyy/MM/dd HH:mm') AS SPAN,
    COUNT(1) AS TOTAL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL THEN 1 END) AS SUCCESSFUL_CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '4%' THEN 1 END) AS "4xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'http' AND
                    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode LIKE '5%' THEN 1 END) AS "5xx_ERRORS",
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'timedout' THEN 1 END) AS TIMEOUTS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' THEN 1 END) AS CAPPED_CALLS,
    ROUND(COUNT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime) / 
        COUNT(DISTINCT DATE_TRUNC('second', _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime)), 0) AS THROUGHPUT_RPS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    (_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day) OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND
           timestamp > (now() - interval '1' day)))
GROUP BY 
    ENDPOINT, SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

+++

+++Antwortlatenz an jedem Endpunkt im 50., 95., 99. und 99,9. Perzentil über einen bestimmten Zeitraum

Diese Abfrage berechnet die Antwortzeit-Perzentile für benutzerdefinierte Aktionsendpunkte, damit Sie die Latenzverteilung erkennen und Leistungsausreißer mit unterschiedlichen Perzentil-Schwellenwerten identifizieren können.

_Data-Lake-Abfrage_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS SUCCESSFUL_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P50_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P95_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.99) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P99_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.999) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P999_LATENCY_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime IS NOT NULL
    <actionExecutionOriginStartTime filter>
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

_Beispiel_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS SUCCESSFUL_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P50_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P95_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.99) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P99_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.999) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P999_LATENCY_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day)
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

+++

+++Zeitreihe der Perzentile der Antwortlatenz an jedem Endpunkt über einen bestimmten Zeitraum

Diese Abfrage liefert Latenzperzentile, die als Zeitreihe organisiert sind. So können Sie auf verschiedenen Perzentilebenen verfolgen, wie sich die Endpunkt-Antwortzeiten im Zeitverlauf ändern.

_Data-Lake-Abfrage_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,    
    COUNT(1) AS SUCCESSFUL_CALLS,
    DATE_FORMAT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, 'yyyy/MM/dd HH:mm') AS SPAN,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P50_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P95_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.99) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P99_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.999) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P999_LATENCY_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime IS NOT NULL
    <actionExecutionOriginStartTime filter>
GROUP BY 
    ENDPOINT,
    SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

_Beispiel_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,    
    COUNT(1) AS SUCCESSFUL_CALLS,
    DATE_FORMAT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, 'yyyy/MM/dd HH:mm') AS SPAN,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P50_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P95_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.99) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P99_LATENCY_MS,
    ROUND(PERCENTILE_CONT(0.999) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime),0) AS P999_LATENCY_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginTime IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day)
GROUP BY 
    ENDPOINT,
    SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

+++

+++ Wartezeit in der Warteschlange für gedrosselte Endpunkte beim 50. und 95. Perzentil über einen bestimmten Zeitraum

Diese Abfrage analysiert die Warteschlangenwartezeiten für gedrosselte Endpunkte und zeigt die Wartezeiten im 50. und 95. Perzentil an, damit Sie die Auswirkungen der Drosselung auf Ihre benutzerdefinierten Aktionen besser verstehen.

_Data-Lake-Abfrage_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS THROTTLED_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P50_QUEUE_TIME_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P95_QUEUE_TIME_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionIsThrottled = 'true' AND
    _experience.journeyOrchestration.stepEvents.actionWaitTime IS NOT NULL AND
    <actionExecutionOriginStartTime filter>
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

_Beispiel_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    COUNT(1) AS THROTTLED_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P50_QUEUE_TIME_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P95_QUEUE_TIME_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionIsThrottled = 'true' AND
    _experience.journeyOrchestration.stepEvents.actionWaitTime IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day)
GROUP BY 
    ENDPOINT
ORDER BY
    ENDPOINT;
```

+++

+++ Zeitreihe der Perzentile der Wartezeit in der Warteschlange für jeden gedrosselten Endpunkt

Diese Abfrage liefert die Wartezeit-Perzentile in der Warteschlange als Zeitreihe, damit Sie überwachen können, wie sich eine Drosselung auf die Wartezeiten für jeden Endpunkt im Zeitverlauf auswirkt.

_Data-Lake-Abfrage_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    DATE_FORMAT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, 'yyyy/MM/dd HH:mm') AS SPAN,
    COUNT(1) AS THROTTLED_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P50_QUEUE_TIME_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P95_QUEUE_TIME_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionIsThrottled = 'true' AND
    _experience.journeyOrchestration.stepEvents.actionWaitTime IS NOT NULL AND
    <actionExecutionOriginStartTime filter>
GROUP BY 
    ENDPOINT,
    SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

_Beispiel_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint AS ENDPOINT,
    DATE_FORMAT(_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime, 'yyyy/MM/dd HH:mm') AS SPAN,
    COUNT(1) AS THROTTLED_CALLS,
    ROUND(PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P50_QUEUE_TIME_MS,
    ROUND(PERCENTILE_CONT(0.95) WITHIN GROUP (ORDER BY _experience.journeyOrchestration.stepEvents.actionWaitTime),0) AS P95_QUEUE_TIME_MS
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionIsThrottled = 'true' AND
    _experience.journeyOrchestration.stepEvents.actionWaitTime IS NOT NULL AND
    _experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day)
GROUP BY 
    ENDPOINT,
    SPAN
ORDER BY
    ENDPOINT,
    SPAN;
```

+++

+++ Anzahl der Fehler nach Typ und Code für einen bestimmten Endpunkt über einen bestimmten Zeitraum

Diese Abfrage bietet eine detaillierte Aufschlüsselung der Fehler für einen bestimmten Endpunkt, gruppiert nach Fehlertyp und Fehler-Code, einschließlich Informationen zu Wiederholungsversuchen.

_Data-Lake-Abfrage_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionExecutionError AS ERROR_TYPE,
    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode AS ERROR_CODE,
    COUNT(1) AS CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionOriginError IS NOT NULL THEN 1 END) AS CALLS_WITH_RETRY
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint = '<endpoint URI>' AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL AND
    (<actionExecutionOriginStartTime filter>) OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND <timestamp filter>))
GROUP BY 
    ERROR_TYPE, ERROR_CODE
ORDER BY
    ERROR_TYPE, ERROR_CODE;
```

_Beispiel_

```sql
SELECT
    _experience.journeyOrchestration.stepEvents.actionExecutionError AS ERROR_TYPE,
    _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode AS ERROR_CODE,
    COUNT(1) AS CALLS,
    COUNT(CASE WHEN _experience.journeyOrchestration.stepEvents.actionExecutionOriginError IS NOT NULL THEN 1 END) AS CALLS_WITH_RETRY
FROM 
    journey_step_events
WHERE 
    _experience.journeyOrchestration.stepEvents.actionType = 'customHttpAction' AND
    _experience.journeyOrchestration.stepEvents.actionOriginEndpoint = 'https://example.com/my/endpoint' AND
    _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL AND
    (_experience.journeyOrchestration.stepEvents.actionExecutionOriginStartTime > (now() - interval '1' day) OR
        (_experience.journeyOrchestration.stepEvents.actionExecutionError = 'capped' AND timestamp > (now() - interval '1' day)))
GROUP BY 
    ERROR_TYPE, ERROR_CODE
ORDER BY
    ERROR_TYPE, ERROR_CODE;
```

+++

