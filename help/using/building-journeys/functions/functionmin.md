---
product: journey optimizer
title: min
description: Erfahren Sie mehr über die Funktion „min“
feature: Journeys
role: Engineer
level: Experienced
keywords: min, Funktion, Ausdruck, Journey
exl-id: 1c425d1d-08b4-446b-83ce-db376b2bf39f
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 100%

---

# min {#min}

Gibt den Minimalwert aus einem Satz von Ausdrücken zurück, entweder als Liste oder in Form von zwei Ausdrücken. Nullwerte werden ignoriert.

## Kategorie

Aggregation

## Funktionssyntax

`min(<parameters>)`

## Parameter

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duration
* integer
* decimal
* dateTime
* dateTimeOnly

## Signaturen und zurückgegebene Typen

`min(<listDuration>)`

Gibt eine Dauer zurück.

`min(<listInteger>)`

Gibt eine Dauer zurück.

`min(<listDateTimeOnly>)`

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

`min(<listDateTime>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

`min(<listDateOnly>)`

Gibt ein Datum zurück.

`min(<listDecimal>)`

Gibt eine Dezimalzahl zurück.

`min(<decimal>,<decimal>)`

Gibt eine Dezimalzahl zurück.

`min(<duration>,<duration>)`

Gibt eine Dauer zurück.

`min(<dateTime>,<dateTime>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

`min(<dateTimeOnly>,<dateTimeOnly>)`

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

`min(<integer>,<integer>)`

Gibt eine Ganzzahl zurück.

## Beispiele

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

Gibt 3 zurück.

`min([10,null,8])`

Gibt 8 zurück.
