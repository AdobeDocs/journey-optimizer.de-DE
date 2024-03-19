---
product: journey optimizer
title: inLastDays
description: Erfahren Sie mehr über die Funktion „inLastDays“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastDays, Funktion, Ausdruck, Journey
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: ht
source-wordcount: '48'
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

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.
