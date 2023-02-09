---
product: journey optimizer
title: inNextMonths
description: Erfahren Sie mehr über die Funktion „inNextMonths“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextMonths, Funktion, Ausdruck, Journey
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 100%

---

# inNextMonths {#inNextMonths}

Gibt „true“ zurück, wenn der angegebene Datums- bzw. Datum/Uhrzeit-Wert zwischen jetzt und jetzt + delta Monaten liegt.

## Kategorie

Datum

## Funktionssyntax

`inNextMonths(<dateTime>,<delta>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

## Signaturen und zurückgegebener Typ

`inNextMonths(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

## Beispiele

`inNextMonths(toDateTime('2020-01-12T01:11:00Z'), 4)`

Gibt „true“ zurück.
