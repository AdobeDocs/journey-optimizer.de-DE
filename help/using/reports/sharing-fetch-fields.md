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
source-wordcount: '0'
ht-degree: 0%

---

# Datenabruffelder für journeyStep-Ereignisse {#sharing-fetch-fields}

Diese Feldergruppe wird sowohl von journeyStepEvent als auch journeyStepProfileEvent verwendet.

Bei einer Schrittverarbeitung kann es N Datenabrufe für Feldergruppen geben.

## fetchTotalTime {#fetchtotaltime-field}

Gesamtdauer, die bei der Schrittverarbeitung für das Abrufen von Daten gebraucht wurde (in Millisekunden).

Typ: lang

## fetchTypeInError {#fetchtypeinerror-field}

Legt fest, ob der Abruffehler bei Adobe Experience Platform oder bei einer benutzerdefinierten Datenquelle liegt.

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

Code für den Fehler beim Abrufen. Wird angezeigt, wenn der Fehler einen Code enthält, z. B. HTTP-Code. Wenn der actionExecError beispielsweise http lautet, stellt der Code 404 den HTTP 404-Fehler dar.

Typ: Zeichenfolge

## fetchOriginError {#fetchoriginerror-field}

Eine Zeitüberschreitung kann in zwei Fällen auftreten:

* beim ersten Versuch der Ausführung der Aktion; in diesem Fall ist die Ausführung noch nicht abgeschlossen, sodass kein zugrunde liegender Fehler vorliegt.
* bei einer Wiederholung; in diesem Fall beschreibt der ActionExecOrigError/actionExecOrigErrorCode den Fehler, der beim Versuch vor der Wiederholung aufgetreten ist.

Beispielsweise werden Daten vom Unified Profil Service abgerufen und wird beim ersten Versuch ein HTTP 500-Fehler zurückgegeben. Der Abruf wird erneut versucht, aber die Dauer der zwei Versuche liegt über der Zeitüberschreitung. Dann wird die Aktionsausführung als Zeitüberschreitung markiert. Der Aktionsteil sieht wie folgt aus:

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

Der vom System, das von [!DNL Journey Optimizer] abgefragt wird, bereitgestellte Fehler-Code. Dieser kann zum Beispiel 404, 500 usw. lauten.

Typ: Zeichenfolge

## fetchCount {#fetchcount-field}

Wie oft die Daten abgerufen werden, unabhängig vom Typ der Quelle.

Typ: lang

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

Gesamtdauer, die zum Abrufen der Daten von Adobe Experience Platform benötigt wird (in Millisekunden). Hinweis: Diese Dauer berechnet sich vom Zeitpunkt, an dem die Engine das Anreicherungsereignis an den Anreicherungsdienst sendet, bis zu dem Zeitpunkt, an dem die Engine die Antwort erhält.

Typ: lang

## fetchPlatformCount {#fetchplatformcount-field}

Wie oft die Daten von Adobe Experience Platform abgerufen werden.

Typ: lang

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

Dauer des Abrufs der benutzerspezifischen Daten (in Millisekunden). Hinweis: Diese Dauer berechnet sich vom Zeitpunkt, an dem die Engine das Anreicherungsereignis an den Anreicherungsdienst sendet, bis zu dem Zeitpunkt, an dem die Engine die Antwort erhält

Typ: lang

## fetchCustomCount {#fetchcustomcount-field}

Wie oft die benutzerdefinierten Daten von externen Systemen abgerufen werden.

Typ: lang
