---
product: journey optimizer
title: limit
description: Erfahren Sie mehr über die Funktionsbeschränkung
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 7fa1e393-2912-4392-b759-e54d08d5635a
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# limit {#limit}

Gibt die ersten oder letzten N Elemente einer Liste zurück.

>[!NOTE]
>
>Wenn die Zielliste ein listObject ist, kann diese Funktion nur in benutzerdefinierten Aktionsausdrücken verwendet werden.

## Kategorie

Liste

## Funktionssyntax

`limit(<parameters>)`

## Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly oder listObject | Liste zum Sortieren. Bei listObject muss es sich um einen Feldverweis handeln. |
| numberOfItems | integer | Anzahl der aus der angegebenen Liste zurückzugebenden Elemente. |
| firstOrLastItems | boolean | Dieser Parameter ist optional (standardmäßig &quot;true&quot;). &quot;true&quot;gibt die ersten Elemente zurück. false gibt die letzten Elemente zurück. |

## Signatur und zurückgegebener Typ

`limit(<listString>,<integer>)`
`limit(<listString>,<integer>,<boolean>)`

Gibt eine Liste von Zeichenfolgen zurück.

`limit(<listInteger>,<integer>)`
`limit(<listInteger>,<integer>,<boolean>)`

Gibt eine Liste von Ganzzahlen zurück.

`limit(<listDecimal>,<integer>)`
`limit(<listDecimal>,<integer>,<boolean>)`

Gibt eine Liste mit Dezimalstellen zurück.

`limit(<listBoolean>,<integer>)`
`limit(<listBoolean>,<integer>,<boolean>)`

Gibt eine Liste mit booleschen Werten zurück.

`limit(<listDateOnly>,<integer>)`
`limit(<listDateOnly>,<integer>,<boolean>)`

Gibt eine Liste mit Datumsangaben zurück.

`limit(<listDateTimeOnly>,<integer>)`
`limit(<listDateTimeOnly>,<integer>,<boolean>)`

Gibt eine Liste der Uhrzeiten ohne Berücksichtigung der Zeitzone zurück.

`limit(<listDateTime>,integer>)`
`limit(<listDateTime>,<integer>,<boolean>)`

Gibt eine Liste der Uhrzeiten zurück.

`limit(<listDuration>,<integer>)`
`limit(<listDuration>,<integer>,<boolean>)`

Gibt eine Liste der Dauern zurück.

`limit(<listObject>,<integer>)`
`limit(<listObject>,<integer>,<boolean>)`

Gibt eine Liste von Objekten zurück.

## Beispiel

`limit(["A", "B", "C", "D", "E"], 3)`

Rückgabe `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

Rückgabe `["C","D","E"]`.
