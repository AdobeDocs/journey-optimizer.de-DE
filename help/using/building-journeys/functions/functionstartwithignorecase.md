---
product: journey optimizer
title: startWithIgnoreCase
description: Erfahren Sie mehr über die Funktion „startWithIgnoreCase“
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
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
| string | Zeichenfolge |
| prefix | Zeichenfolge |

## Signatur und zurückgegebener Typ

`startWithIgnoreCase(<string>,<string>)`

Geben einen booleschen Wert zurück.

## Beispiel

`startWithIgnoreCase("rowing is great", "RO")`

Gibt „true“ zurück.
