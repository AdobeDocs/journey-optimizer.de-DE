---
product: journey optimizer
title: listSize
description: Erfahren Sie mehr über die Funktion „listSize“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: listSize, Funktion, Ausdruck, Journey
exl-id: dd378e4d-f65a-495c-ac10-b4209d6b6b88
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 100%

---

# listSize {#listSize}

Zählt die Zahl der Elemente in der Liste.

## Kategorie

Liste

## Funktionssyntax

`listSize(<parameters>)`

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

## Signaturen und zurückgegebener Typ

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

`listSize(<listPoint>)`

Gibt eine Ganzzahl zurück.

## Beispiel

`listSize([10,2,3])`

Gibt 3 zurück.
