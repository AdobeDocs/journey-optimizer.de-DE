---
product: journey optimizer
title: containIgnoreCase
description: Erfahren Sie mehr über die Funktion „containIgnoreCase“.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: containIgnoreCase, Funktion, Ausdruck, Journey
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 100%

---

# containIgnoreCase {#containIgnoreCase}

Überprüft, ob die zweite Argumentzeichenfolge in der ersten Argumentzeichenfolge enthalten ist, ohne Groß-/Kleinschreibung zu berücksichtigen.

## Kategorie

Zeichenfolge

## Funktionssyntax

`containIgnoreCase(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| string | string |
| string searched | string |

## Signatur und zurückgegebener Typ

`containIgnoreCase(<string>,<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`containIgnoreCase("rowing is great", "GREAT")`

Gibt „true“ zurück.
