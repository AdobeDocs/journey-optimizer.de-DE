---
product: journey optimizer
title: startWith
description: Erfahren Sie mehr über die Funktion „startWith“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWith, Funktion, Ausdruck, Journey
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# startWith {#startWith}

Gibt „true“ zurück, wenn der zweite Parameter ein Präfix des ersten Parameters ist.

## Kategorie

Zeichenfolge

## Funktionssyntax

`startWith(<parameters>)`

## Parameter

| Parameter | Typ |
|-------------|--------|
| string | string |
| prefix | string |

## Signatur und zurückgegebener Typ

`startWith(<string>,<string>)`

Geben einen booleschen Wert zurück.

## Beispiel

`startWith("Hello World", "Hello")`

Gibt „true“ zurück.

`startWith("Hello World", "World")`

Gibt „false“ zurück.
