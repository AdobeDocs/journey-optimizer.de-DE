---
product: journey optimizer
title: countOnlyNull
description: Erfahren Sie mehr über die Funktion „countOnlyNull“
feature: Journeys
role: Engineer
level: Experienced
keywords: countOnlyNull, Funktion, Ausdruck, Journey
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 100%

---

# countOnlyNull {#countOnlyNull}

Zählt die Zahl der Nullwerte in der Liste.

Beachten Sie, dass der Parameter `<listObject>` in dieser Funktion nicht unterstützt wird.

## Kategorie

Aggregation

## Funktionssyntax

`countOnlyNull(<listAny>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Signatur und zurückgegebener Typ

`countOnlyNull(<listAny>)`

Gibt eine Ganzzahl zurück.

## Beispiel

`countOnlyNull([10,2,10,null])`

Gibt 1 zurück.
