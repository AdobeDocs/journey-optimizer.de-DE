---
product: journey optimizer
title: notEqualIgnoreCase
description: Erfahren Sie mehr über die Funktion „notEqualIgnoreCase“.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: notEqualIgnoreCase, Funktion, Ausdruck, Journey
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '41'
ht-degree: 90%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

Überprüft, ob sich die erste Argumentzeichenfolge von der zweiten Argumentzeichenfolge unterscheidet, wobei Groß-/Kleinschreibung ignoriert wird.

## Kategorie

Zeichenfolge

## Funktionssyntax

`notEqualIgnoreCase(<parameters>)`

## Parameter

* string

## Signatur und zurückgegebener Typ

`notEqualIgnoreCase(<string>,<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`
