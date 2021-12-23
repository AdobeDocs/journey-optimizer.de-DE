---
product: adobe campaign
title: concat
description: Erfahren Sie mehr über die Funktion „concat“
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: ht
source-wordcount: '40'
ht-degree: 100%

---

# concat {#concat}

Verkettet zwei Zeichenfolgenparameter oder eine Liste von Zeichenfolgen.

## Kategorie

Zeichenfolge

## Funktionssyntax

`concat(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Liste | listString |
| string | string |

## Signatur und zurückgegebener Typ

`concat(<string>,<string>)`

`concat(<listString>)`

Gibt eine Zeichenfolge zurück.

## Beispiel

`concat("Hello","World")`

Gibt „HelloWorld“ zurück.

`concat(["Hello"," ","World"])`

Gibt „Hello World“ zurück.
