---
product: journey optimizer
title: toBool
description: Erfahren Sie mehr über die Funktion toBool
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# toBool {#toBool}

Konvertiert einen Argumentwert je nach Typ in einen booleschen Wert.

* Aus Zeichenfolge: Versuchen Sie, den Zeichenfolgenwert in einen booleschen Wert zu konvertieren, von &quot;true&quot;, wenn der Zeichenfolgenwert &quot;true&quot; ist, andernfalls von &quot;false&quot;
* Von numerisch: true , wenn der numerische Wert nicht gleich 0 ist, andernfalls false

## Kategorie

Konversion

## Funktionssyntax

`toBool(<parameter>)`

## Parameter

* decimal
* boolean
* Zeichenfolge
* integer

## Signaturen und zurückgegebene Typen

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Gibt einen booleschen Wert zurück.

## Beispiele

`toBool("true")`

`toBool(1)`

Gibt &quot;true&quot;zurück.

`toBool("this is not a boolean")`

Gibt false zurück.
