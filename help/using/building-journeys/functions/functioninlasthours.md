---
product: journey optimizer
title: inLastHours
description: Erfahren Sie mehr über die Funktion „inLastHours“
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastHours, Funktion, Ausdruck, Journey
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '49'
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

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.

`inLastHours(@event{MyEvent.timestamp}, 4)`

Gibt „true“ zurück.
