---
product: journey optimizer
title: inLastDays
description: Erfahren Sie mehr über die Funktion „inLastDays“
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastDays, Funktion, Ausdruck, Journey
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 100%

---

# inLastDays {#inLastDays}

Gibt „true“ zurück, wenn ein bestimmtes „dateTime“ zwischen jetzt und jetzt-Delta-Tage liegt.

## Kategorie

Datum

## Funktionssyntax

`inLastDays(<dateTime>,<delta>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

## Signaturen und zurückgegebener Typ

`inLastDays(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

## Beispiele

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.
