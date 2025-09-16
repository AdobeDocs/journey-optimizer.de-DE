---
product: journey optimizer
title: distinctCountWithNull
description: Erfahren Sie mehr über die Funktion „distinctCountWithNull“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCountWithNull, Funktion, Ausdruck, Journey
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: ht
source-wordcount: '57'
ht-degree: 100%

---

# distinctCountWithNull {#distinctCountWithNull}

Zählt die Anzahl verschiedener Werte einschließlich der Nullwerte.

Beachten Sie, dass der Parameter `<listObject>` in dieser Funktion nicht unterstützt wird.

## Kategorie

Aggregation

## Funktionssyntax

`distinctCountWithNull(<listAny>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Signatur und zurückgegebener Typ

`distinctCountWithNull(<listAny>)`

Gibt eine Ganzzahl zurück.

## Beispiel

`distinctCountWithNull([10,2,10,null])`

Gibt 3 zurück.
