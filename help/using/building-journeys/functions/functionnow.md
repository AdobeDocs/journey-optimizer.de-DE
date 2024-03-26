---
product: journey optimizer
title: now
description: Erfahren Sie mehr über die Funktion „now“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: now, Funktion, Ausdruck, Journey
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: ht
source-wordcount: '62'
ht-degree: 100%

---

# now {#now}

Gibt das aktuelle Datum im Datum/Uhrzeit-Format zurück. Weitere Informationen zu Datentypen finden Sie auf [dieser Seite](../expression/data-types.md).

## Kategorie

Datum

## Funktionssyntax

`now(<parameter>)`

## Parameter

| Parameter | Beschreibung |
|--- |--- |
| string |  |

## Signaturen und zurückgegebener Typ

`now()`

`now("<timeZone id>")`

Gibt einen Datum/Uhrzeit-Wert zurück.

## Beispiele

`now()`

Gibt 2023-06-03T06:30Z zurück.

`toString(now())`

Gibt „2023-06-03T06:30Z“ zurück.

`now("Europe/Paris")`

Gibt 2023-06-03T08:30+02:00 zurück.
