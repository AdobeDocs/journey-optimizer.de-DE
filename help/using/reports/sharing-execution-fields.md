---
solution: Journey Optimizer
product: journey optimizer
title: Aktionsausführungsfelder für journeyStep-Ereignisse
description: Aktionsausführungsfelder für journeyStep-Ereignisse
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: 190f757853f65b7434319047760c2efb43d2d702
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 77%

---

# Aktionsausführungsfelder für journeyStep-Ereignisse {#sharing-execution-fields}

Diese Feldergruppe wird sowohl von journeyStepEvent als auch journeyStepProfileEvent verwendet.

Wenn für den Schritt eine Aktion verarbeitet werden muss, werden diese Felder der Ereignis-Payload hinzugefügt.

## actionID {#actionid-field}

Kennung der ausgeführten Aktion.

Typ: Zeichenfolge

## actionName {#actionname-field}

Name der Aktion. Wenn kein Name festgelegt wurde, wird der stepName verwendet.

Typ: Zeichenfolge

## actionType {#actionType-field}

Art der Aktion.

Typ: Zeichenfolge

## actionParameterized {#actionparameterized-field}

Gibt an, ob die Aktion parametrisiert wurde oder nicht.

Typ: boolesch

## actionExecutionTime {#actionexecutiontime-field}

Dauer (in Millisekunden), die zum Ausführen einer aktuellen Aktion benötigt wird.

Typ: lang

>[!NOTE]
>
> Das Feld `actionExecutionTime` gibt die Gesamtzeit (in Millisekunden) an, die für die Ausführung der Aktion benötigt wurde, einschließlich der Zeit, die die Anfrage in der Warteschlange verbracht hat (wenn die Drosselung konfiguriert ist und das Ratenlimit erreicht wurde), und der tatsächlichen Ausführungszeit (einschließlich Netzwerklatenz für den externen Endpunkt).
>
> Das Feld `Timestamp` gibt die Endzeit der Aktionsausführung an. Um zu bestimmen, wann das Profil in den benutzerdefinierten Aktionsknoten eingetreten ist, ziehen Sie `actionExecutionTime` von `Timestamp` ab.
>
>Wenn `Timestamp` beispielsweise „2025-02-04 09:39:03 UTC“ lautet und `actionExecutionTime` 1.813.227 ms (~31 Minuten) beträgt, trat das Profil um etwa „2025-02-04 09.:08: UTC“ in den Knoten ein.




## actionExecutionError {#actionexecutionerror-field}

Fehlertyp, der beim Aufrufen der Aktion auftritt.

Typ: Zeichenfolge

Werte:
* http
* capping
* timeout
* error

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

Code für Fehler bei der Ausführung der Aktion. Wird angezeigt, wenn der Fehler einen Code enthält, z. B. HTTP-Code.

Typ: Zeichenfolge

## actionExecutionOriginError {#actionexecutionoriginerror-field}

Eine Zeitüberschreitung kann in zwei Fällen auftreten:

* beim ersten Versuch der Ausführung einer Aktion; in diesem Fall ist die Ausführung noch nicht abgeschlossen, sodass kein zugrunde liegender Fehler vorliegt.
* bei einer Wiederholung; in diesem Fall beschreibt der ActionExecOrigError/actionExecOrigErrorCode den Fehler, der beim Versuch vor der Wiederholung aufgetreten ist.

Beispielsweise wird eine E-Mail gesendet und beim ersten Versuch ein HTTP 500-Fehler zurückgegeben. Der Abruf wird erneut versucht, aber die Dauer der zwei Versuche liegt über der maximalen Wartezeit. Dann wird die Aktionsausführung als Zeitüberschreitung markiert. Der Aktionsteil sieht wie folgt aus:

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

Fehler-Code von actionExecOrigError.

Typ: Zeichenfolge

## actionBusinessType {#actionbusinesstype-field}

Gibt die Art der Aktion an.

Werte:

* builtin
* ACS Email
* ACS SMS
* ACS Push
* Kundin bzw. Kunde
* Epsilon
* ...

Typ: Zeichenfolge

## deliveryJobID {#deliveryjobid-field}

Beschreibt die Versand-Vorgangskennung für die Batch-Journey.

Typ: Zeichenfolge

## batchDeliveryID {#batchdeliveryid-field}

Beschreibt die Versandkennung für die Batch-Journey.

Typ: Zeichenfolge

## fromSegmentTrigger {#fromsegmenttrigger-field}

Beschreibt, ob die Batch-Journey im Zielgruppensegment ausgelöst wird.

Typ: boolesch

## actionSchedulerCount {#actionschedulercount-field}

Anzahl der Planungs-Benachrichtigungsanfragen, die bei der Schrittverarbeitung an den Planungsdienst gesendet werden.

Typ: lang
