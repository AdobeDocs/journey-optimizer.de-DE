---
product: journey optimizer
title: updateTimeZone
description: Erfahren Sie mehr über die Funktion updateTimeZone
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1bf4662e-55d0-4631-af93-1430ec7ed7e2
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 0%

---

# updateTimeZone {#updateTimeZone}

Gibt eine neue Datum/Uhrzeit mit einer neuen Zeitzone im selben Moment zurück.

## Kategorie

Datum

## Funktionssyntax

`updateTimeZone(<parameters>)`

## Parameter

* Zeitzonen-ID: Zeichenfolge
* dateTime

## Signatur und zurückgegebener Typ

`updateTimeZone(<dateTime>,<timeZone id>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

## Beispiele

`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Gibt 2019-08-28T17 zurück:15:30.123+02:00.

<!--`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), toTimeZone("Europe/Paris")))`
Returns "2019-08-28T17:15:30.123+02:00".-->

`updateTimeZone(@{MyExpEvent.timestamp}, "Australia/Sydney")`

Wenn der Wert des Zeitstempelfelds `2021-11-16T16:55:12.939318+01:00`, gibt die Funktion `2021-11-17T02:55:12.942115+11:00`.
