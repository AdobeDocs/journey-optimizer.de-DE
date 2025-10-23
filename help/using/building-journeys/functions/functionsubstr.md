---
product: journey optimizer
title: substr
description: Erfahren Sie mehr über die Funktion „substr“
feature: Journeys
role: Developer
level: Experienced
keywords: substr, Funktion, Ausdruck, Journey
exl-id: 58a3107a-b4f3-43da-b454-5ce597515847
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '68'
ht-degree: 100%

---

# substr {#substr}

Gibt die Unterzeichenfolge des Zeichenfolgenausdrucks zwischen dem Anfangsindex und dem Endindex zurück. Wenn der Endindex nicht definiert ist, wird die Zeichenfolge zwischen dem Anfangsindex und dem Ende zurückgegeben.

## Kategorie

Zeichenfolge

## Funktionssyntax

`substr(<parameters>)`

## Parameter

| Parameter | type |
|-------------|----------|
| string | string |
| beginIndex | integer |
| endIndex | integer |

## Signatur und zurückgegebener Typ

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

Gibt eine Zeichenfolge zurück.

## Beispiel

`substr("Hello World",6)`

Gibt „World“ zurück.

`substr("Hello World", 0, 5)`

Gibt „Hello“ zurück.
