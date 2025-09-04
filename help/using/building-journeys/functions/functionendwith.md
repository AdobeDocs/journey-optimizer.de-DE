---
product: journey optimizer
title: endWith
description: Erfahren Sie mehr über die Funktion „endWith“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWith, Funktion, Ausdruck, Journey
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 100%

---

# endWith {#endWith}

Gibt „true“ zurück, wenn der zweite Parameter ein Suffix des ersten Parameters ist.

## Kategorie

Zeichenfolge

## Funktionssyntax

`endWith(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| string | string |
| suffix | string |

## Signatur und zurückgegebener Typ

`endWith(<string>,<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`endWith("Hello World", "World")`

Gibt „true“ zurück.

`endWith("Hello World", "Hello")`

Gibt „false“ zurück.
