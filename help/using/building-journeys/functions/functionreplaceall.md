---
product: adobe campaign
title: replaceAll
description: Erfahren Sie mehr über die Funktion „replaceAll“
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: ht
source-wordcount: '75'
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
| target | string |
| replacement | string |

## Signatur und zurückgegebener Typ

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Gibt eine Zeichenfolge zurück.

## Beispiel

`replaceAll("Hello World", "l", "x")`

Gibt „Hexxo Worxd“ zurück.
