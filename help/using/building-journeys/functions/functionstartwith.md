---
product: journey optimizer
title: startWith
description: Erfahren Sie mehr über die Funktion startWith
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 0%

---

# startWith {#startWith}

Gibt &quot;true&quot;zurück, wenn der zweite Parameter ein Präfix des ersten Parameters ist.

## Kategorie

Zeichenfolge

## Funktionssyntax

`startWith(<parameters>)`

## Parameter

| Parameter | Typ |
|-------------|--------|
| Zeichenfolge | Zeichenfolge |
| prefix | Zeichenfolge |

## Signatur und zurückgegebener Typ

`startWith(<string>,<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`startWith("Hello World", "Hello")`

Gibt &quot;true&quot;zurück.

`startWith("Hello World", "World")`

Gibt false zurück.
