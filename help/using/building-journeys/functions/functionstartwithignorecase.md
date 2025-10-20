---
product: journey optimizer
title: startWithIgnoreCase
description: Erfahren Sie mehr über die Funktion „startWithIgnoreCase“
feature: Journeys
role: Engineer
level: Experienced
keywords: startWithIgnoreCase, Funktion, Ausdruck, Journey
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 100%

---

# startWithIgnoreCase {#startWithIgnoreCase}

Gibt „true“ zurück, wenn der zweite Parameter ein Präfix des ersten Parameters ist (ohne Berücksichtigung der Groß-/Kleinschreibung).

## Kategorie

Zeichenfolge

## Funktionssyntax

`startWithIgnoreCase(<parameters>)`

## Parameter

| Parameter | Typ |
|-------------|--------|
| string | string |
| prefix | string |

## Signatur und zurückgegebener Typ

`startWithIgnoreCase(<string>,<string>)`

Geben einen booleschen Wert zurück.

## Beispiel

`startWithIgnoreCase("rowing is great", "RO")`

Gibt „true“ zurück.
