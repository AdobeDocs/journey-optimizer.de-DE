---
product: journey optimizer
title: now
description: Erfahren Sie mehr über die Funktion „now“
feature: Journeys
role: Engineer
level: Experienced
keywords: now, Funktion, Ausdruck, Journey
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 93%

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
| string | Zeitzonenkennung (optional) |

## Signaturen und zurückgegebener Typ

`now()`

`now("<timeZone id>")`

Gibt einen Datum/Uhrzeit-Wert zurück.

## Beispiele

`now()`

Gibt 2023-06-03T06:30Z zurück.

`toString(now())`

Gibt „2023-06-03T06:30Z“ zurück

`now("Europe/Paris")`

Gibt 2023-06-03T08:30+02:00 zurück.
