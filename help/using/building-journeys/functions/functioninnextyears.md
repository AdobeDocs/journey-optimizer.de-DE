---
product: journey optimizer
title: inNextYears
description: Erfahren Sie mehr über die Funktion „inNextYears“
feature: Journeys
role: Developer
level: Experienced
keywords: inNextYears, Funktion, Ausdruck, Journey
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 100%

---

# inNextYears {#inNextYears}

Gibt „true“ zurück, wenn der angegebene Datums- bzw. Datum/Uhrzeit-Wert zwischen jetzt und jetzt + delta Jahren liegt.

## Kategorie

Datum

## Funktionssyntax

`inNextYears(<dateTime>,<delta>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

## Signaturen und zurückgegebener Typ

`inNextYears(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

## Beispiele

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.
