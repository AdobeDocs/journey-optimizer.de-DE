---
product: journey optimizer
title: toInteger
description: Erfahren Sie mehr über die Funktion toInteger
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 901a91d1-13dd-4283-b87f-223196eb072f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# toInteger {#toInteger}

Konvertiert einen Argumentwert in eine Ganzzahl.

## Kategorie

Konversion

## Funktionssyntax

`toInteger(<parameter>)`

## Parameter

| Parameter | Beschreibung |
|--- |--- |
| Zeichenfolge | konvertiert den Zeichenfolgenwert in einen Integer |
| dateTime | konvertiert das Datum in die Anzahl der Millisekunden (Millisekunden der Epoche) |
| decimal | konvertiert in eine Ganzzahl, indem der Dezimalteil entfernt wird (Beispiel: 1,5 wird zu 1) |
| boolean | konvertiert den booleschen Wert in 1, wenn &quot;true&quot;, in 0, wenn &quot;false&quot; |

## Signaturen und zurückgegebener Typ

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

Gibt eine Ganzzahl zurück.

## Beispiele

`toInteger("4")`

Gibt 4 zurück.
