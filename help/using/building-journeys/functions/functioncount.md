---
product: journey optimizer
title: count
description: Erfahren Sie mehr über die Funktion „count“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: count, Funktion, Ausdruck, Journey
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: ht
source-wordcount: '90'
ht-degree: 100%

---

# count {#count}

Zählt die Elemente der Liste, wobei Nullwerte nicht berücksichtigt werden.

## Kategorie

Aggregation

## Funktionssyntax

`count(<listAny>)`

`count(<listObject>)`

## Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly oder listObject | Zu verarbeitende Liste. Bei listObject muss es sich um einen Feldverweis handeln. Ein listObject kann kein Null-Objekt enthalten. |

## Signaturen und zurückgegebener Typ

`count(<listAny>)`

Gibt eine Ganzzahl zurück.

## Beispiel

`count([10,2,10,null])`

Gibt 3 zurück.

`count(@event{my_event.productListItems})`

Gibt die Anzahl der Objekte im angegebenen Array von Objekten zurück (listObject-Typ). Anmerkung: Ein listObject kann kein Null-Objekt enthalten.
