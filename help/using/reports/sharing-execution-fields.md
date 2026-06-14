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
TQID: https://experienceleague.adobe.com/wX-aqOHlSWGU0gTqyv0nEuSVFL8sstvCMxgiqeFDWIo
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 685
ht-degree: 97%

---

# Aktionsausführungsfelder für journeyStep-Ereignisse {#sharing-execution-fields}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Verweisen Sie auf die Aktionsausführungsfelder, die zum Journey von Schrittereignissen hinzugefügt wurden, wenn ein Schritt eine benutzerdefinierte Aktion verarbeitet.

>[!ENDSHADEBOX]

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

Beispielsweise wird eine E-Mail gesendet und beim ersten Versuch ein HTTP 500-Fehler zurückgegeben. Der Abruf wird erneut versucht, aber die Dauer der zwei Versuche liegt über dem Timeout. Dann wird die Aktionsausführung als Zeitüberschreitung markiert. Der Aktionsteil sieht wie folgt aus:

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

Beschreibt die Versand-Auftragskennung für die Batch-Journey.

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
