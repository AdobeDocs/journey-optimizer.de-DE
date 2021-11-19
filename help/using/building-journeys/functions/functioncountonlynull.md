---
product: adobe campaign
title: countOnlyNull
description: Erfahren Sie mehr über die Funktion „countOnlyNull“
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 100%

---

# countOnlyNull {#countOnlyNull}

Zählt die Zahl der Nullwerte in der Liste.

## Kategorie

Aggregation

## Funktionssyntax

`countOnlyNull(<listAny>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Liste | listString |
| Liste | listBoolean |
| Liste | listInteger |
| Liste | listDecimal |
| Liste | listDuration |
| Liste | listDateTime |
| Liste | listDateTimeOnly |
| Liste | listDateOnly |

## Signatur und zurückgegebener Typ

`countOnlyNull(<listAny>)`

Gibt eine Ganzzahl zurück.

## Beispiel

`countOnlyNull([10,2,10,null])`

Gibt 1 zurück.
