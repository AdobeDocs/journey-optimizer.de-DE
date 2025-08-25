---
product: journey optimizer
title: inNextYears
description: Erfahren Sie mehr über die Funktion „inNextYears“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextYears, Funktion, Ausdruck, Journey
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
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
