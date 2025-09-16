---
product: journey optimizer
title: countWithNull
description: Erfahren Sie mehr über die Funktion „countWithNull“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull, Funktion, Ausdruck, Journey
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: ht
source-wordcount: '57'
ht-degree: 100%

---

# countWithNull {#countWithNull}

Zählt alle Elemente der Liste, einschließlich Nullwerten.

Beachten Sie, dass der Parameter `<listObject>` in dieser Funktion nicht unterstützt wird.

## Kategorie

Aggregation

## Funktionssyntax

`countWithNull(<listAny>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Signatur und zurückgegebener Typ

`countWithNull(<listAny>)`

Gibt eine Ganzzahl zurück.

## Beispiel

`countWithNull([10,2,10,null])`

Gibt 4 zurück.
