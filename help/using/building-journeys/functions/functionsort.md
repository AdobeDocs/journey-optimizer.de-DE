---
product: adobe campaign
title: sort
description: Erfahren Sie mehr über die Funktion „sort“
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 95%

---

# sort {#sort}

Sortiert eine Liste von Werten in ihrer natürlichen Reihenfolge. Das erste Argument ist die Liste der Werte, das zweite ist ein boolescher Wert, der angibt, ob die Sortierung aufsteigend (true) oder absteigend (false) ist.

## Kategorie

Liste

## Funktionssyntax

`sort(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Liste | listString |
| Liste | listBoolean |
| Liste | listInteger |
| Liste | listDecimal |
| Liste | listDuration |
| Liste | listDateTime |
| Liste | listDateTimeOnly |
| Liste | listDateOnly |
| Boolesch | Boolesch |

## Signatur und zurückgegebener Typ

`sort(<listInteger>,<boolean>)`

Gibt eine Liste mit Ganzzahlen zurück.

`sort(<listDecimal>,<boolean>)`

Gibt eine Liste mit Dezimalzahlen zurück.

`sort(<listString>,<boolean>)`

Gibt eine Liste mit Zeichenfolgen zurück.

`sort(<listDateTimeOnly>,<boolean>)`

Gibt eine Liste mit Datum/Uhrzeit-Werten ohne Berücksichtigung der Zeitzone zurück.

`sort(<listDateTime>,<boolean>)`

Gibt eine Liste mit Datum/Uhrzeit-Werten zurück.

`sort(<listDateOnly>,<boolean>)`

Gibt eine Liste mit Datumsangaben zurück.

`sort(<listBoolean>,<boolean>)`

Gibt eine Liste mit booleschen Werten zurück.

## Beispiel

`sort(["A", "C", "B"], true)`

Rückgabe `["A","B","C"]`.

`sort([1, 3, 2], false)`

Rückgabe `[3, 2, 1]`.
