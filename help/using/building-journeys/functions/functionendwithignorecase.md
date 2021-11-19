---
product: adobe campaign
title: endWithIgnoreCase
description: Erfahren Sie mehr über die Funktion „endWithIgnoreCase“
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 100%

---

# endWithIgnoreCase {#endWithIgnoreCase}

Überprüft, ob die erste Argumentzeichenfolge mit einer bestimmten Zeichenfolge endet (zweite Argumentzeichenfolge), wobei Groß-/Kleinschreibung nicht berücksichtigt wird.

## Kategorie

Zeichenfolge

## Funktionssyntax

`endWithIgnoreCase(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| string | Zeichenfolge |
| suffix | Zeichenfolge |

## Signatur und zurückgegebener Typ

`endWithIgnoreCase(<string>,<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`endWithIgnoreCase("rowing is great", "AT")`

Gibt „true“ zurück.
