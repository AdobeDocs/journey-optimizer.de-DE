---
product: journey optimizer
title: toBool
description: Erfahren Sie mehr über die Funktion „toBool“
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: ht
source-wordcount: '74'
ht-degree: 100%

---

# toBool {#toBool}

Konvertiert einen Argumentwert je nach Typ in einen booleschen Wert.

* Von Zeichenfolge: Versucht, den Zeichenfolgenwert in einen booleschen Wert zu konvertieren, von „true“, wenn der Zeichenfolgenwert „true“ ist, andernfalls „false“
* Von numerisch: „true“, wenn der numerische Wert ungleich 0 ist, andernfalls „false“

## Kategorie

Konversion

## Funktionssyntax

`toBool(<parameter>)`

## Parameter

* decimal
* boolean
* string
* integer

## Signaturen und zurückgegebene Typen

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Geben einen booleschen Wert zurück.

## Beispiele

`toBool("true")`

`toBool(1)`

Gibt „true“ zurück.

`toBool("this is not a boolean")`

Gibt „false“ zurück.
