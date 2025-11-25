---
solution: Journey Optimizer
product: journey optimizer
title: Aktionsausführungsfelder für journeyStep-Ereignisse
description: Aktionsausführungsfelder für journeyStep-Ereignisse
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: b93d2288156713ac7479eef491f6104df1955a18
workflow-type: ht
source-wordcount: '663'
ht-degree: 100%

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

Das Feld `actionExecutionTime` gibt die Gesamtzeit (in Millisekunden) an, die für die Ausführung der Aktion benötigt wurde, einschließlich der Zeit, die die Anfrage in der Warteschlange verbracht hat (wenn die Drosselung konfiguriert ist und das Ratenlimit erreicht wurde), und der tatsächlichen Ausführungszeit (einschließlich Netzwerklatenz für den externen Endpunkt).

Das Feld `Timestamp` gibt die Endzeit der Aktionsausführung an. Um zu bestimmen, wann das Profil in den benutzerdefinierten Aktionsknoten eingetreten ist, ziehen Sie die `actionExecutionTime` vom `Timestamp` ab.

Wenn `Timestamp` beispielsweise „2025-02-04 09:39:03 UTC“ ist und `actionExecutionTime` 1.813.227 ms (ca. 31 Minuten) beträgt, trat das Profil ungefähr zum Zeitpunkt „2025-02-04 09:08:32 UTC“ in den Knoten ein.


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

## actionOriginEndpoint {#actionoriginendpoint}

URI des in der Aktion verwendeten Endpunkts einer benutzerdefinierten Aktion.

Typ: Zeichenfolge

## actionOriginMethod {#actionoriginmethod}

Dies beschreibt die in der HTTP-Anfrage (GET oder POST) verwendete Methode.

Typ: Zeichenfolge

## actionOriginIsMTLS {#actionoriginismtls}

Dies beschreibt, ob MTLS für den Endpunkt aktiviert ist.

Typ: boolesch

## actionIsProxy {#actionisproxy}

Dies beschreibt, ob für den Aufruf ein HTTP-Proxy mit definiertem IP-Adressbereich verwendet wird.

Typ: boolesch

## actionExecutionOriginStartTime {#actionexecutionoriginstarttime}

Dies beschreibt den Zeitstempel, zu dem die HTTP-Anfrage initiiert wird. Bei einem Wiederholungsversuch ist dies der Zeitstempel, mit dem der letzte Wiederholungsversuch gestartet wird. Der Zeitstempel verwendet das ISO8601-Format in der UTC-Zeitzone.

Beachten Sie, dass dieser Zeitpunkt normalerweise kurz nach dem Eintritt des Profils in den Aktionsknoten liegt, oder deutlich später im Falle einer Drosselung.

Typ: Zeitstempel

## actionExecutionOriginTime {#actionexecutionorigintime}

Dies beschreibt die Antwortzeit des HTTP-Aufrufs. Bei einem Wiederholungsversuch ist dies die Zeit, die für den letzten Wiederholungsversuch benötigt wird. Es wird der Zeitraum zwischen dem Start der HTTP-Anfrage und dem Zeitpunkt, zu dem die vollständige Antwort vom Server zurückgegeben wird, gemessen. Beachten Sie, dass dies jegliche Zeit ausschließt, die im Falle einer Drosselung in der Warteschlange verbracht wird.

Typ: lang

## actionIsThrottled {#actionisthrottled}

Dadurch wird beschrieben, ob die Drosselung für den Endpunkt aktiviert ist.

Typ: boolesch

## actionWaitTime {#actionwaittime}

Dies beschreibt, wenn das konfigurierte Ratenlimit für einen gedrosselten Endpunkt erreicht wird und Aufrufe mit der konfigurierten Rate in die Warteschlange gestellt und verarbeitet werden. Dieses Feld zeigt die Zeit an, die der Aufruf in der Warteschlange verbracht hat, bevor er ausgeführt wurde. Nur angegeben, wenn actionIsThrottled == wahr.

Typ: lang

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
