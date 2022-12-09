---
product: journey optimizer
title: toDecimal
description: Erfahren Sie mehr über die Funktion toDecimal
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: d761fa4d-5f99-4dee-b747-3eab464c4071
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# toDecimal {#toDecimal}

Konvertiert einen Argumentwert je nach Typ in einen Dezimalwert.

## Kategorie

Konversion

## Funktionssyntax

`toDecimal(<parameter>)`

## Parameter

| Parameter | Beschreibung |
|--- |--- |
| Zeichenfolge | konvertiert den Zeichenfolgenwert in eine Dezimalzahl |
| dateTime | konvertiert das Datum in die Anzahl der Millisekunden (Millisekunden der Epoche) |
| boolean | konvertiert den booleschen Wert in 1, wenn &quot;true&quot;, in 0, wenn &quot;false&quot; |
| integer | konvertiert in eine Dezimalzahl (Beispiel).: 1 wird zu 1,0) |

## Signaturen und zurückgegebene Typen

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Gibt eine Dezimalzahl zurück.

## Beispiele

`toDecimal("4.0")`

Gibt 4.0 zurück.
