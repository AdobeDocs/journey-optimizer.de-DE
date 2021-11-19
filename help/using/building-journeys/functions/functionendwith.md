---
product: adobe campaign
title: endWith
description: Erfahren Sie mehr über die Funktion „endWith“
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 100%

---

# endWith {#endWith}

Gibt „true“ zurück, wenn der zweite Parameter ein Suffix des ersten Parameters ist.

## Kategorie

Zeichenfolge

## Funktionssyntax

`endWith(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| string | Zeichenfolge |
| suffix | Zeichenfolge |

## Signatur und zurückgegebener Typ

`endWith(<string>,<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`endWith("Hello World", "World")`

Gibt „true“ zurück.

`endWith("Hello World", "Hello")`

Gibt „false“ zurück.
