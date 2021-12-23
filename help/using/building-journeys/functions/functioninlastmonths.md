---
product: adobe campaign
title: inLastMonths
description: Erfahren Sie mehr über die Funktion „inLastMonths“
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: ht
source-wordcount: '44'
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

`inLastMonths(toDateTime('2010-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.
