---
product: adobe campaign
title: replace
description: Erfahren Sie mehr über die Funktion „replace“
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 100%

---

# replace {#replace}

Ersetzt das erste Auftreten, das mit der Zielzeichenfolge übereinstimmt, in der Basiszeichenfolge durch die Ersatzzeichenfolge.

Die Ersetzung erfolgt vom Anfang der Zeichenfolge zum Ende, z. B. führt ein Ersetzen von „aa“ in der Zeichenfolge „aaa“ durch „b“ zu „ba“ und nicht zu „ab“.

## Kategorie

Zeichenfolge

## Funktionssyntax

`replace(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|--------------|
| base | Zeichenfolge |
| target | Zeichenfolge |
| replacement | Zeichenfolge |

## Signatur und zurückgegebener Typ

`replace(<base>,<target>,<replacement>)`

Gibt eine Zeichenfolge zurück.

## Beispiel

`replace("Hello World", "l", "x")`

Gibt „Hexlo World“ zurück.
