---
title: Aktionsausführungsfelder für journeyStep-Ereignisse
description: Aktionsausführungsfelder für Ereignis von "travelStep"
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Aktionsausführungsfelder für journeyStep-Ereignisse {#sharing-execution-fields}

![](../assets/do-not-localize/badge.png)

Dieses Mixin wird von journeyStepEvent und journeyStepProfileEvent geteilt.

Wenn für den Schritt eine Aktion verarbeitet werden muss, werden diese Felder der Ereignis-Payload hinzugefügt.

## actionID

Kennung der ausgeführten Aktion.

Typ: Zeichenfolge

## actionName

Name der Aktion. Wenn kein Name festgelegt wurde, wird der stepName verwendet.

Typ: string

## actionType

Art der Aktion.

Typ: string

## actionParameterized

Gibt an, ob die Aktion parametrisiert wurde oder nicht.

Typ: boolesch

## actionExecutionTime

Dauer (in Millisekunden), die zum Ausführen einer aktuellen Aktion benötigt wird.

Typ: lang

## actionExecutionError

Fehlertyp, der beim Aufrufen der Aktion auftritt.

Typ: string

Werte:
* http
* capping
* timeout
* error

## actionExecutionErrorCode

Code für Fehler bei der Ausführung der Aktion. Wird angezeigt, wenn der Fehler einen Code enthält, z. B. HTTP-Code.

Typ: string

## actionExecutionOriginError

Eine Zeitüberschreitung kann in zwei Fällen auftreten:

* beim ersten Versuch der Ausführung einer Aktion; in diesem Fall ist die Ausführung noch nicht abgeschlossen, sodass kein zugrunde liegender Fehler vorliegt.
* bei einer Wiederholung; in diesem Fall beschreibt der ActionExecOrigError/actionExecOrigErrorCode den Fehler, der beim Versuch vor der Wiederholung aufgetreten ist.

Beispielsweise wird eine E-Mail gesendet und beim ersten Versuch ein HTTP 500-Fehler zurückgegeben. Der Abruf wird erneut versucht, aber die Dauer der zwei Versuche liegt über der Zeitüberschreitung. Dann wird die Aktionsausführung als Zeitüberschreitung markiert. Der Aktionsteil sieht wie folgt aus:

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

Typ: string

## actionExecutionOriginCode

Fehler-Code von actionExecOrigError.

Typ: string

## actionBusinessType

Gibt die Art der Aktion an.

Werte:

* builtin
* ACS Email
* ACS SMS
* ACS Push
* customer
* Epsilon
* ...

Typ: string

## deliveryJobID

Beschreibt die Versand-Vorgangskennung für die Batch-Journey.

Typ: string

## batchDeliveryID

Hier wird die Versand-ID für die Batch-Journey beschrieben.

Typ: string

## fromSegmentTrigger

Beschreibt, ob die Batch-Journey im Zielgruppensegment ausgelöst wird.

Typ: boolean

## actionSchedulerCount

Anzahl der Planungs-Benachrichtigungsanfragen, die bei der Schrittverarbeitung an den Planungsdienst gesendet werden.

Typ: long
