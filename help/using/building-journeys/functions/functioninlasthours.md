---
product: journey optimizer
title: inLastHours
description: Erfahren Sie mehr über die Funktion „inLastHours“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastHours, Funktion, Ausdruck, Journey
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: ht
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
