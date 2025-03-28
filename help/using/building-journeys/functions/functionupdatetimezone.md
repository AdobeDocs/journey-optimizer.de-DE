---
product: journey optimizer
title: updateTimeZone
description: Erfahren Sie mehr über die Funktion „updateTimeZone“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: updateTimeZone, Funktion, Ausdruck, Journey
exl-id: 1bf4662e-55d0-4631-af93-1430ec7ed7e2
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# updateTimeZone {#updateTimeZone}

Gibt einen neuen Datum/Uhrzeit-Wert mit einer neuen Zeitzone zum selben Moment zurück.

## Kategorie

Datum

## Funktionssyntax

`updateTimeZone(<parameters>)`

## Parameter

* Zeitzonen-ID: string
* dateTime

## Signatur und zurückgegebener Typ

`updateTimeZone(<dateTime>,<timeZone id>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

## Beispiele

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Gibt 2023-08-28T17:15:30.123+02:00 zurück.

<!--`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), toTimeZone("Europe/Paris")))`
Returns "2019-08-28T17:15:30.123+02:00".-->

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

Wenn der Wert des Zeitstempelfelds `2021-11-16T16:55:12.939318+01:00` ist, gibt die Funktion `2021-11-17T02:55:12.942115+11:00` zurück.
