---
product: journey optimizer
title: endWithIgnoreCase
description: Erfahren Sie mehr über die Funktion „endWithIgnoreCase“
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 278ef1a4-571c-4b5f-b4de-0cfc644ac7d7
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
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
| string | string |
| suffix | string |

## Signatur und zurückgegebener Typ

`endWithIgnoreCase(<string>,<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`endWithIgnoreCase("rowing is great", "AT")`

Gibt „true“ zurück.
