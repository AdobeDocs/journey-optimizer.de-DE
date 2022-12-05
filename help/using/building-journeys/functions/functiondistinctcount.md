---
product: journey optimizer
title: distinctCount
description: Erfahren Sie mehr über die Funktion „distinctCount“
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 100%

---

# distinctCount{#distinctCount}

Zählt die Anzahl verschiedener Werte, wobei Nullwerte ignoriert werden.

## Kategorie

Aggregation

## Funktionssyntax

`distinctCount(<listAny>)`

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

`distinctCount(<listAny>)`

Gibt eine Ganzzahl zurück.

## Beispiel

`distinctCount([10,2,10,null])`

Gibt 2 zurück.
