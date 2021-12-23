---
product: adobe campaign
title: inLastDays
description: Erfahren Sie mehr über die Funktion „inLastDays“
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: ht
source-wordcount: '44'
ht-degree: 100%

---

# inLastDays {#inLastDays}

Gibt „true“ zurück, wenn der angegebene Datums- bzw. Datum/Uhrzeit-Wert zwischen jetzt und jetzt - delta Tagen liegt.

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

`inLastDays(toDateTime('2019-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.
