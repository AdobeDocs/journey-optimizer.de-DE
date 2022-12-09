---
product: journey optimizer
title: endWith
description: Erfahren Sie mehr über die Funktion endWith
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 0%

---

# endWith {#endWith}

Gibt &quot;true&quot;zurück, wenn der zweite Parameter ein Suffix des ersten Parameters ist.

## Kategorie

Zeichenfolge

## Funktionssyntax

`endWith(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Zeichenfolge | Zeichenfolge |
| Suffix | Zeichenfolge |

## Signatur und zurückgegebener Typ

`endWith(<string>,<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`endWith("Hello World", "World")`

Gibt &quot;true&quot;zurück.

`endWith("Hello World", "Hello")`

Gibt false zurück.
