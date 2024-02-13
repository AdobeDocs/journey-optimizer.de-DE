---
product: journey optimizer
title: listSize
description: Erfahren Sie mehr über die Funktion „listSize“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: listSize, Funktion, Ausdruck, Journey
exl-id: dd378e4d-f65a-495c-ac10-b4209d6b6b88
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: ht
source-wordcount: '78'
ht-degree: 100%

---

# listSize {#listSize}

Zählt die Zahl der Elemente in der Liste.

## Kategorie

Liste

## Funktionssyntax

`listSize(<parameters>)`

## Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly oder listObject | Zu verarbeitende Liste. Bei listObject muss es sich um einen Feldverweis handeln. Ein listObject kann kein Null-Objekt enthalten. |

## Signaturen und zurückgegebener Typ

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

Gibt eine Ganzzahl zurück.

`listSize(<listObject>)`

## Beispiel

`listSize([10,2,3])`

Gibt 3 zurück.

`listSize(@event{my_event.productListItems})`

Gibt die Anzahl der Objekte im angegebenen Array von Objekten zurück (listObject-Typ).
