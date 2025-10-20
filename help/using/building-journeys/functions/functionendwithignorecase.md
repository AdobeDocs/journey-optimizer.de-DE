---
product: journey optimizer
title: endWithIgnoreCase
description: Erfahren Sie mehr über die Funktion „endWithIgnoreCase“
feature: Journeys
role: Engineer
level: Experienced
keywords: endWithIgnoreCase, Funktion, Ausdruck, Journey
exl-id: 278ef1a4-571c-4b5f-b4de-0cfc644ac7d7
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '52'
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
