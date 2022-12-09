---
product: journey optimizer
title: substr
description: Erfahren Sie mehr über die Funktionsuntergruppe
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 58a3107a-b4f3-43da-b454-5ce597515847
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# substr {#substr}

Gibt die Unterzeichenfolge des Zeichenfolgenausdrucks zwischen dem Anfangsindex und dem Endindex zurück. Wenn der Endindex nicht definiert ist, liegt er zwischen dem Anfangsindex und dem Ende.

## Kategorie

Zeichenfolge

## Funktionssyntax

`substr(<parameters>)`

## Parameter

| Parameter | type |
|-------------|----------|
| Zeichenfolge | Zeichenfolge |
| beginIndex | integer |
| endIndex | integer |

## Signatur und zurückgegebener Typ

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

Gibt eine Zeichenfolge zurück.

## Beispiel

`substr("Hello World",6)`

Gibt &quot;World&quot;zurück.

`substr("Hello World", 0, 5)`

Gibt &quot;Hello&quot;zurück.
