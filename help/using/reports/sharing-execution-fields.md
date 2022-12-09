---
solution: Journey Optimizer
product: journey optimizer
title: Aktionsausführungsfelder für journeyStep-Ereignisse
description: Aktionsausführungsfelder für journeyStep-Ereignisse
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Aktionsausführungsfelder für journeyStep-Ereignisse {#sharing-execution-fields}

Diese Feldergruppe wird von journeyStepEvent und journeyStepProfileEvent gemeinsam genutzt.

Wenn für den Schritt eine Aktion verarbeitet werden muss, werden diese Felder der Ereignis-Payload hinzugefügt.

## actionID {#actionid-field}

Kennung der ausgeführten Aktion.

Typ: Zeichenfolge

## actionName {#actionname-field}

Name der Aktion. Wenn kein Name festgelegt wurde, wird stepName verwendet.

Typ: Zeichenfolge

## actionType {#actionType-field}

Typ der Aktion.

Typ: Zeichenfolge

## actionParameterized {#actionparameterized-field}

Gibt an, ob die Aktion parametrisiert wurde oder nicht.

Typ: boolean

## actionExecutionTime {#actionexecutiontime-field}

Die Zeit (in Millisekunden), die zum Ausführen einer aktuellen Aktion benötigt wird.

Typ: long

## actionExecutionError {#actionexecutionerror-field}

Fehlertyp, der beim Aufrufen der Aktion auftritt.

Typ: Zeichenfolge

Werte:
* http
* capping
* timeout
* error

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

Code für Fehler bei der Aktionsausführung. Vorhanden, wenn der Fehler einen Code enthält, z. B. einen HTTP-Code.

Typ: Zeichenfolge

## actionExecutionOriginError {#actionexecutionoriginerror-field}

In zwei Fällen kann es zu einer Zeitüberschreitung kommen:

* beim ersten Versuch der Ausführung einer Aktion. In diesem Fall ist die Ausführung noch nicht abgeschlossen, sodass kein zugrunde liegender Fehler vorliegt
* bei einem erneuten Versuch: In diesem Fall beschreibt der actionExecOrigError/actionExecOrigErrorCode den Fehler, der beim Versuch vor dem erneuten Versuch aufgetreten ist.

Beispielsweise wird eine E-Mail gesendet und beim ersten Versuch ein HTTP 500-Fehler zurückgegeben. Der Abruf wird erneut versucht, aber die Dauer der beiden Versuche überschreitet die Zeitüberschreitung. Anschließend wird die Aktionsausführung als Zeitüberschreitung markiert. Der Aktionsteil sieht wie folgt aus:

```
    ...
    "actionId": "myActionId",
    "actionName": "My mail sending",
    "actionType": "acsRestAction",
    "actionParameterized": true,
    "actionExecError": "timedout",
    "actionExecOrigError": "http",
    "actionExecOrigErrorCode": "500"
```

Typ: Zeichenfolge

## actionExecutionOriginCode {#actionexecutionorigincode-field}

Fehlercode des actionExecOrigError.

Typ: Zeichenfolge

## actionBusinessType {#actionbusinesstype-field}

Gibt den Aktionstyp an.

Werte:

* builtin
* ACS Email
* ACS SMS
* ACS Push
* customer
* Epsilon
* ...

Typ: Zeichenfolge

## deliveryJobID {#deliveryjobid-field}

Hier wird die Versand-Auftrags-ID für die Batch-Journey beschrieben.

Typ: Zeichenfolge

## batchDeliveryID {#batchdeliveryid-field}

Hier wird die Versand-ID für die Batch-Journey beschrieben.

Typ: Zeichenfolge

## fromSegmentTrigger {#fromsegmenttrigger-field}

Dies beschreibt, ob die Batch-Journey vom Zielgruppensegment ausgelöst wird.

Typ: boolean

## actionSchedulerCount {#actionschedulercount-field}

Zählung der Planer-Benachrichtigungsanfragen, die während der Schrittverarbeitung an den Planungsdienst gesendet werden.

Typ: long
