---
product: journey optimizer
title: replaceAll
description: Erfahren Sie mehr über die Funktion „replaceAll“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: replaceAll, Funktion, Ausdruck, Journey
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 100%

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
| target | string (RegExp) |
| replacement | string |

## Signatur und zurückgegebener Typ

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Gibt eine Zeichenfolge zurück.

## Beispiel{#example}

`replaceAll("Hello World", "l", "x")`

Gibt „Hexxo Worxd“ zurück.

Da der Zielparameter ein regulärer Ausdruck ist, müssen Sie je nach der Zeichenfolge, die Sie ersetzen möchten, möglicherweise einige Zeichen auslassen. Siehe das Beispiel auf [dieser Seite](../functions/functionreplace.md#example_2).
