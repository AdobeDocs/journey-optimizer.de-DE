---
product: journey optimizer
title: distinctCount
description: Erfahren Sie mehr über die Funktion „distinctCount“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCount, Funktion, Ausdruck, Journey
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

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
