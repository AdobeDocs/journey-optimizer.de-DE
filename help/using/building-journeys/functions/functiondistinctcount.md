---
product: journey optimizer
title: distinctCount
description: Erfahren Sie mehr über die Funktion „distinctCount“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCount, Funktion, Ausdruck, Journey
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: ht
source-wordcount: '138'
ht-degree: 100%

---

# distinctCount{#distinctCount}

Zählt die Anzahl verschiedener Werte, wobei Nullwerte ignoriert werden.

## Kategorie

Aggregation

## Funktionssyntax

`distinctCount(<listAny>)`

## Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly oder listObject | Zu verarbeitende Liste. Bei listObject muss es sich um einen Feldverweis handeln. |
| keyAttributeName | Zeichenfolge | Dieser Parameter ist optional und nur für listObject. Wenn der Parameter nicht angegeben wird, wird ein Objekt als doppelt betrachtet, wenn alle Attribute dieselben Werte aufweisen. Andernfalls wird ein Objekt als doppelt betrachtet, wenn das angegebene Attribut denselben Wert aufweist. |

## Signatur und zurückgegebener Typ

`distinctCount(<listAny>)`

Gibt eine Ganzzahl zurück.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

Gibt eine Liste mit Objekten zurück.


## Beispiel

`distinctCount([10,2,10,null])`

Gibt 2 zurück.

`distinctCount(@event{my_event.productListItems})`

Gibt die Anzahl der eindeutig voneinander unabhängigen Objekte im angegebenen Array von Objekten (listObject-Typ) zurück.

`distinctCount(@event{my_event.productListItems}, "SKU")`

Gibt die Anzahl der Objekte mit einem eindeutigen „SKU“-Attributwert{} zurück.
