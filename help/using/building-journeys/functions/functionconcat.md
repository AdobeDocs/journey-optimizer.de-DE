---
product: journey optimizer
title: concat
description: Erfahren Sie mehr über die Funktion „concat“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: concat, Funktion, Ausdruck, Journey
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: ht
source-wordcount: '44'
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
| string | Zeichenfolge |

## Signatur und zurückgegebener Typ

`concat(<string>,<string>)`

`concat(<listString>)`

Gibt eine Zeichenfolge zurück.

## Beispiel

`concat("Hello","World")`

Gibt „HelloWorld“ zurück.

`concat(["Hello"," ","World"])`

Gibt „Hello World“ zurück.
