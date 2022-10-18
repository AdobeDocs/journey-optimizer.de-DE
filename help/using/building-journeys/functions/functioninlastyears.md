---
product: journey optimizer
title: inLastYears
description: Erfahren Sie mehr über die Funktion „inLastYears“
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
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
