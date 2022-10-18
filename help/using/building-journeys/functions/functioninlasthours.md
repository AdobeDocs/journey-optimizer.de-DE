---
product: journey optimizer
title: inLastHours
description: Erfahren Sie mehr über die Funktion „inLastHours“
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 100%

---

# inLastHours {#inLastHours}

Gibt „true“ zurück, wenn der angegebene Datum/Uhrzeit-Wert zwischen jetzt und jetzt - delta Stunden liegt.

## Kategorie

Datum

## Funktionssyntax

`inLastHours(<dateTime>,<delta>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

## Signaturen und zurückgegebener Typ

`inLastHours(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

## Beispiele

`inLastHours(toDateTime('2019-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.

`inLastHours(@{MyEvent.timestamp}, 4)`

Gibt „true“ zurück.
