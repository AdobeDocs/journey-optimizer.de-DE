---
product: journey optimizer
title: now
description: Erfahren Sie mehr über die Funktion
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 0%

---

# now {#now}

Gibt das aktuelle Datum im Datum/Uhrzeit-Format zurück. Weitere Informationen zu Datentypen finden Sie unter [diese Seite](../expression/data-types.md).

## Kategorie

Datum

## Funktionssyntax

`now(<parameter>)`

## Parameter

| Parameter | Beschreibung |
|--- |--- |
| Zeichenfolge |  |

## Signaturen und zurückgegebener Typ

`now()`

`now("<timeZone id>")`

Gibt eine dateTime zurück.

## Beispiele

`now()`

Gibt 2019-06-03T06:30Z zurück.

`toString(now())`

Gibt &quot;2019-06-03T06:30Z&quot;zurück

`now("Europe/Paris")`

Gibt 2019-06-03T08:30+02:00 zurück.
