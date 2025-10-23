---
product: journey optimizer
title: inLastMonths
description: Erfahren Sie mehr über die Funktion „inLastMonths“
feature: Journeys
role: Developer
level: Experienced
keywords: inLastMonths, Funktion, Ausdruck, Journey
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '48'
ht-degree: 100%

---

# inLastMonths {#inLastMonths}

Gibt „true“ zurück, wenn der angegebene Datums- bzw. Datum/Uhrzeit-Wert zwischen jetzt und jetzt - delta Monaten liegt.

## Kategorie

Datum

## Funktionssyntax

`inLastMonths(<dateTime>,<delta>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

## Signaturen und zurückgegebener Typ

`inLastMonths(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

## Beispiele

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.
