---
product: adobe campaign
title: sum
description: Erfahren Sie mehr über die Funktion „sum“
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: ht
source-wordcount: '51'
ht-degree: 100%

---

# sum {#sum}

Gibt die Summe der Werte eines Satzes von Ausdrücken zurück. Nullwerte werden ignoriert.

## Kategorie

Aggregation

## Funktionssyntax

`sum(<parameters>)`

## Parameter

* listInteger
* listDecimal
* duration
* integer
* decimal

## Signaturen und zurückgegebene Typen

`sum(<listDecimal>)`

Gibt eine Dezimalzahl zurück.

`sum(<listInteger>)`

Gibt eine Ganzzahl zurück.

`sum(<integer>,<integer>)`

Gibt eine Ganzzahl zurück.

`sum(<decimal>,<decimal>)`

Gibt eine Dezimalzahl zurück.

## Beispiele

`sum(@{BarBeacon.inventory},5)`

`sum([10,3,8])`

Gibt 21 zurück.

`sum([10.5,null,8.1])`

Gibt 18,6 zurück.
