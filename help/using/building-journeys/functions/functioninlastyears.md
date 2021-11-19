---
product: adobe campaign
title: inLastYears
description: Erfahren Sie mehr über die Funktion „inLastYears“
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 100%

---

# inLastYears {#inLastYears}

Gibt „true“ zurück, wenn der angegebene Datums- bzw. Datum/Uhrzeit-Wert zwischen jetzt und jetzt - delta Jahren liegt.

## Kategorie

Datum

## Funktionssyntax

`inLastYears(<dateTime>,<delta>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

## Signaturen und zurückgegebener Typ

`inLastYears(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

## Beispiele

`inLastYears(toDateTime('2010-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.
