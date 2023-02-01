---
product: journey optimizer
title: inNextDays
description: Erfahren Sie mehr über die Funktion „inNextDays“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextDays, Funktion, Ausdruck, Journey
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: ht
source-wordcount: '48'
ht-degree: 100%

---

# inNextDays {#inNextDays}

Gibt „true“ zurück, wenn der angegebene Datums- bzw. Datum/Uhrzeit-Wert zwischen jetzt und jetzt + delta Tagen liegt.

## Kategorie

Datum

## Funktionssyntax

`inNextDays(<dateTime>,<delta>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

## Signaturen und zurückgegebener Typ

`inNextDays(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

## Beispiele

`inNextDays(toDateTime('2010-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.
