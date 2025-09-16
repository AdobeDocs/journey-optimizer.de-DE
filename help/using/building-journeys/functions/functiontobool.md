---
product: journey optimizer
title: toBool
description: Erfahren Sie mehr über die Funktion „toBool“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: tobool, Funktion, Ausdruck, Journey
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: ht
source-wordcount: '79'
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
