---
product: adobe campaign
title: replaceAll
description: Erfahren Sie mehr über die Funktion „replaceAll“
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 87b8056d26fe91a71e92ca346a9811c609d41128
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# replaceAll {#replaceAll}

Ersetzt jedes Auftreten, das mit der Zielzeichenfolge übereinstimmt, in der Basiszeichenfolge durch die Ersatzzeichenfolge.

Die Ersetzung verläuft vom Anfang der Zeichenfolge zum Ende. Wenn Sie z. B. in der Zeichenfolge „aaa“ „aa“ durch „b“ ersetzen, erhalten Sie „ba“ und nicht „ab“.

## Kategorie

Zeichenfolge

## Funktionssyntax

`replaceAll(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|--------------|
| base | string |
| target | Zeichenfolge (RegExp) |
| replacement | Zeichenfolge |

## Signatur und zurückgegebener Typ

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Gibt eine Zeichenfolge zurück.

## Beispiel{#example}

`replaceAll("Hello World", "l", "x")`

Gibt „Hexxo Worxd“ zurück.

Da der Zielparameter eine RegExp ist, müssen Sie je nach der Zeichenfolge, die Sie ersetzen möchten, möglicherweise einige Zeichen maskieren. Siehe Beispiel unter [diese Seite](../functions/functionreplace.md#example_2).
