---
product: journey optimizer
title: inLastDays
description: Erfahren Sie mehr über die Funktion „inLastDays“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastDays, Funktion, Ausdruck, Journey
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
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

`inLastDays(toDateTime('2019-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.
