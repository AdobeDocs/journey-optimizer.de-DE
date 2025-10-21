---
product: journey optimizer
title: limit
description: Erfahren Sie mehr über die Funktion „limit“.
feature: Journeys
role: Developer
level: Experienced
keywords: Limit, Funktion, Ausdruck, Journey
exl-id: 7fa1e393-2912-4392-b759-e54d08d5635a
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 100%

---

# limit {#limit}

Gibt die ersten oder letzten n Elemente einer Liste zurück.

## Kategorie

Liste

## Funktionssyntax

`limit(<parameters>)`

## Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly oder listObject | Zu berücksichtigende Liste.  Bei listObject muss es sich um einen Feldverweis handeln. |
| numberOfItems | integer | Anzahl der aus der angegebenen Liste zurückzugebenden Elemente. |
| firstOrLastItems | Boolescher Wert | Dieser Parameter ist optional (standardmäßig „true“). „True“ gibt die ersten Elemente zurück. „False“ gibt die letzten Elemente zurück. |

## Signatur und zurückgegebener Typ

`limit(<listString>,<integer>)`
`limit(<listString>,<integer>,<boolean>)`

Gibt eine Liste mit Zeichenfolgen zurück.

`limit(<listInteger>,<integer>)`
`limit(<listInteger>,<integer>,<boolean>)`

Gibt eine Liste mit Ganzzahlen zurück.

`limit(<listDecimal>,<integer>)`
`limit(<listDecimal>,<integer>,<boolean>)`

Gibt eine Liste mit Dezimalzahlen zurück.

`limit(<listBoolean>,<integer>)`
`limit(<listBoolean>,<integer>,<boolean>)`

Gibt eine Liste mit booleschen Werten zurück.

`limit(<listDateOnly>,<integer>)`
`limit(<listDateOnly>,<integer>,<boolean>)`

Gibt eine Liste mit Datumsangaben zurück.

`limit(<listDateTimeOnly>,<integer>)`
`limit(<listDateTimeOnly>,<integer>,<boolean>)`

Gibt eine Liste mit Datum/Uhrzeit-Werten ohne Berücksichtigung der Zeitzone zurück.

`limit(<listDateTime>,integer>)`
`limit(<listDateTime>,<integer>,<boolean>)`

Gibt eine Liste mit Datum/Uhrzeit-Werten zurück.

`limit(<listDuration>,<integer>)`
`limit(<listDuration>,<integer>,<boolean>)`

Gibt eine Liste der Dauer zurück.

`limit(<listObject>,<integer>)`
`limit(<listObject>,<integer>,<boolean>)`

Gibt eine Liste mit Objekten zurück.

## Beispiel

`limit(["A", "B", "C", "D", "E"], 3)`

Gibt `["A","B","C"]` zurück.

`limit(["A", "B", "C", "D", "E"], 3, false)`

Gibt `["C","D","E"]` zurück.
