---
product: journey optimizer
title: sum
description: Erfahren Sie mehr über die Funktion „sum“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: Summe, Funktion, Ausdruck, Journey
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

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

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

Gibt 21 zurück.

`sum([10.5,null,8.1])`

Gibt 18.6 zurück.
