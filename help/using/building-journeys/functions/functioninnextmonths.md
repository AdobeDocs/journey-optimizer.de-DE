---
product: journey optimizer
title: inNextMonths
description: Erfahren Sie mehr über die Funktion „inNextMonths“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextMonths, Funktion, Ausdruck, Journey
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: ht
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

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

Gibt „true“ zurück.
