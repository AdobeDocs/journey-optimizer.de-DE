---
product: journey optimizer
title: replaceAll
description: Erfahren Sie mehr über die Funktion replaceAll
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# replaceAll {#replaceAll}

Ersetzt alle Vorkommnisse, die mit der Zielzeichenfolge übereinstimmen, durch die Ersatzzeichenfolge in der Basiszeichenfolge.

Die Ersetzung erfolgt vom Anfang der Zeichenfolge bis zum Ende, z. B. führt das Ersetzen von &quot;aa&quot;durch &quot;b&quot;in der Zeichenfolge &quot;aaa&quot;zu &quot;ba&quot;anstelle von &quot;ab&quot;.

## Kategorie

Zeichenfolge

## Funktionssyntax

`replaceAll(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|--------------|
| base | Zeichenfolge |
| target | string (RegExp) |
| replacement | Zeichenfolge |

## Signatur und zurückgegebener Typ

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Gibt eine Zeichenfolge zurück.

## Beispiel{#example}

`replaceAll("Hello World", "l", "x")`

Gibt &quot;Hexxo Worxd&quot;zurück.

Da der Zielparameter eine RegExp ist, müssen Sie je nach der Zeichenfolge, die Sie ersetzen möchten, möglicherweise einige Zeichen maskieren. Siehe Beispiel unter [diese Seite](../functions/functionreplace.md#example_2).
