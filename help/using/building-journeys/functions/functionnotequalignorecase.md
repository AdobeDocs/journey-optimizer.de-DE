---
product: journey optimizer
title: notEqualIgnoreCase
description: Erfahren Sie mehr über die Funktion „notEqualIgnoreCase“.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: notEqualIgnoreCase, Funktion, Ausdruck, Journey
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: ht
source-wordcount: '41'
ht-degree: 100%

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

`notEqualIgnoreCase(@{iOSPushPermissionAllowed.device.model}, "iPad")`
