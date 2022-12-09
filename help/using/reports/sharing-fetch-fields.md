---
solution: Journey Optimizer
product: journey optimizer
title: Datenabruffelder für journeyStep-Ereignisse
description: Datenabruffelder für journeyStep-Ereignisse
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Datenabruffelder für journeyStep-Ereignisse {#sharing-fetch-fields}

Diese Feldergruppe wird von journeyStepEvent und journeyStepProfileEvent gemeinsam genutzt.

Während einer Schrittverarbeitung können wir keinen Datenabruf für Feldergruppen durchführen.

## fetchTotalTime {#fetchtotaltime-field}

Gesamtbesuchszeit für den Datenabruf in Millisekunden während der Schrittverarbeitung.

Typ: long

## fetchTypeInError {#fetchtypeinerror-field}

Definiert, ob sich der Abruffehler in Adobe Experience Platform oder einer benutzerdefinierten Datenquelle befindet.

Typ: Zeichenfolge

Werte:
* aep
* custom

## fetchError {#fetcherror-field}

Fehlertyp, der bei der Verarbeitung des Datenabrufs auftritt.

Typ: Zeichenfolge

Werte:
* http
* capping
* timedout
* error

## fetchErrorCode {#fetcherrorcode-field}

Code für den Abruffehler. Vorhanden, wenn der Fehler einen Code enthält, z. B. einen HTTP-Code. Wenn der actionExecError beispielsweise http lautet, stellt der Code 404 den HTTP 404-Fehler dar.

Typ: Zeichenfolge

## fetchOriginError {#fetchoriginerror-field}

In zwei Fällen kann es zu einer Zeitüberschreitung kommen:

* beim ersten Versuch der Ausführung der Aktion. In diesem Fall ist die Ausführung noch nicht abgeschlossen, sodass kein zugrunde liegender Fehler vorliegt
* bei einem erneuten Versuch: In diesem Fall beschreibt der actionExecOrigError/actionExecOrigErrorCode den Fehler, der beim Versuch vor dem erneuten Versuch aufgetreten ist.

Beispielsweise werden Daten vom Unified Profile Service abgerufen und beim ersten Versuch wird ein HTTP 500-Fehler zurückgegeben. Der Abruf wird erneut versucht, aber die Dauer der beiden Versuche überschreitet die Zeitüberschreitung. Anschließend wird die Aktionsausführung als Zeitüberschreitung markiert. Der Aktionsteil sieht wie folgt aus:

```
    ...
    "fetchTypeInError": "aep",
    "fieldgroupIdInError": "MyProfileFieldgroup",
    "fetchError": "timedout",
    "fetchOrigError": "http",
    "fetchOrigErrorCode": "500"
```

Typ: Zeichenfolge

## fetchOriginErrorCode {#fetchoriginerrorcode-field}

Der vom System bereitgestellte Fehlercode [!DNL Journey Optimizer] fragt. Beispielsweise kann es sich um einen 404-, 500- usw.-Wert handeln.

Typ: Zeichenfolge

## fetchCount {#fetchcount-field}

Wie oft die Daten abgerufen werden, unabhängig vom Typ der Quelle.

Typ: long

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

Gesamtdauer, die zum Abrufen der Daten von Adobe Experience Platform benötigt wird (in Millisekunden). Bemerkung: wird diese Zeitdauer berechnet von dem Zeitpunkt, zu dem die Engine das Anreicherungsereignis an den Anreicherungsdienst sendet, und die Antwort erhält.

Typ: long

## fetchPlatformCount {#fetchplatformcount-field}

Wie oft die Daten von Adobe Experience Platform abgerufen werden.

Typ: long

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

Dauer des Abrufs der benutzerdefinierten Daten in Millisekunden. Bemerkung: diese Zeitdauer berechnet wird von dem Zeitpunkt an, zu dem die Engine das Anreicherungsereignis an den Anreicherungsdienst sendet, und die Antwort erhält

Typ: long

## fetchCustomCount {#fetchcustomcount-field}

Wie oft die benutzerdefinierten Daten von externen Systemen abgerufen werden.

Typ: long
