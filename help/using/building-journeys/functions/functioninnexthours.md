---
product: journey optimizer
title: inNextHours
description: Erfahren Sie mehr über die Funktion „inNextHours“
feature: Journeys
role: Engineer
level: Experienced
keywords: inNextHours, Funktion, Ausdruck, Journey
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 100%

---

# inNextHours {#inNextHours}

Gibt „true“ zurück, wenn der angegebene Datums- bzw. Datum/Uhrzeit-Wert zwischen jetzt und jetzt + delta Stunden liegt.

## Kategorie

Datum

## Funktionssyntax

`inNextHours(<dateTime>,<delta>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

## Signaturen und zurückgegebener Typ

`inNextHours(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

## Beispiele

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.
