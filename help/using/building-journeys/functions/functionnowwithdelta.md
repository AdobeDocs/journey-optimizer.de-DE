---
product: journey optimizer
title: nowWithDelta
description: Erfahren Sie mehr über die Funktion nowWithDelta
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cb1eb221-8532-4637-ac6c-8e058463ac94
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# nowWithDelta {#nowWithDelta}

Gibt den aktuellen Datum/Uhrzeit-Wert einschließlich Versatz zurück. Wenn eine Zeitzonen-ID angegeben wird, wird der Zeitzonenversatz angewendet. Weitere Informationen zu Datentypen finden Sie unter [diese Seite](../expression/data-types.md).

## Kategorie

Datum

## Funktionssyntax

`nowWithDelta(<parameters>)`

## Parameter

| Parameter | Beschreibung |
|--- |--- |
| delta | positiver oder negativer ganzzahliger Wert |
| date part | Jahre, Monate, Tage, Stunden, Minuten oder Sekunden als Zeichenfolge |
| Zeitzonen-ID | Zeichenfolgendarstellung des Zeitzonenwerts. Weitere Informationen finden Sie unter [Datentypen](../expression/data-types.md). Die Zeitzonen-ID muss eine Zeichenfolgenkonstante sein. Es darf sich weder um einen Feldverweis noch um einen Ausdruck handeln. |

## Signaturen und zurückgegebener Typ

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Gibt eine dateTime zurück.

## Beispiele

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Gibt eine dateTime genau vor 2 Stunden zurück.
