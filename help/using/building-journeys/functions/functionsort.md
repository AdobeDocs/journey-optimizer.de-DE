---
product: journey optimizer
title: sort
description: Erfahren Sie mehr über die Funktion „sort“
feature: Journeys
role: Developer
level: Experienced
keywords: sort, Funktion, Ausdruck, Journey
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '144'
ht-degree: 100%

---

# sort {#sort}

Sortiert eine Liste von Werten oder Objekten in ihrer natürlichen Reihenfolge.

## Kategorie

Liste

## Funktionssyntax

`sort(<parameters>)`

## Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly oder listObject | Zu sortierende Liste. Bei listObject muss es sich um einen Feldverweis handeln. |
| keyAttributeName | Zeichenfolge | Dieser Parameter ist nur für listObject. Der Attributname in den Objekten der angegebenen Liste wird als Schlüssel zum Filtern verwendet. |
| sortingOrder | Boolescher Wert | Aufsteigend (true) oder absteigend (false) |

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

`sort(<listObject>,<string>,<boolean>)`

Gibt eine Liste mit Objekten zurück.

## Beispiel

`sort(["A", "C", "B"], true)`

Gibt `["A","B","C"]` zurück.

`sort([1, 3, 2], false)`

Gibt `[3, 2, 1]` zurück.

`sort(@event{my_event.productListItems}, "SKU", true)`

Gibt das listObject, geordnet nach SKU-Attribut (aufsteigende Reihenfolge), zurück

