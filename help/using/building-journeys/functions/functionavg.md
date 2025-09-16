---
product: journey optimizer
title: avg
description: Erfahren Sie mehr über die Funktion „avg“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: avg, Funktion, Ausdruck, Journey
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: ht
source-wordcount: '55'
ht-degree: 100%

---

# avg {#avg}

Gibt den Durchschnittswert eines Satzes von Ausdrücken zurück, entweder als Liste oder in Form von zwei Ausdrücken. Nullwerte werden ignoriert.


## Kategorie

Aggregation

## Funktionssyntax

`avg(<parameter>)`

## Parameter

Unterstützte Typen:

* listInteger
* listDecimal
* decimal
* integer

## Signaturen und zurückgegebener Typ

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Gibt eine Dezimalzahl zurück.

## Beispiele

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

Gibt 7.0 zurück.

`avg(10.2, 3)`

Gibt 6.6 zurück.
