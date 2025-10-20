---
product: journey optimizer
title: inLastYears
description: Erfahren Sie mehr über die Funktion „inLastYears“
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastYears, Funktion, Ausdruck, Journey
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
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

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.
