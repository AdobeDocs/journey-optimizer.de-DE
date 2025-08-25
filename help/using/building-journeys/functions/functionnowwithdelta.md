---
product: journey optimizer
title: nowWithDelta
description: Erfahren Sie mehr über die Funktion „nowWithDelta“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: nowWithDelta, Funktion, Ausdruck, Journey
exl-id: cb1eb221-8532-4637-ac6c-8e058463ac94
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 100%

---

# nowWithDelta {#nowWithDelta}

Gibt den aktuellen Datum/Uhrzeit-Wert einschließlich Verschiebung zurück. Wenn eine Zeitzonen-ID angegeben wird, wird die Zeitzonenverschiebung angewendet. Weitere Informationen zu Datentypen finden Sie auf [dieser Seite](../expression/data-types.md).

## Kategorie

Datum

## Funktionssyntax

`nowWithDelta(<parameters>)`

## Parameter

| Parameter | Beschreibung |
|--- |--- |
| delta | positiver oder negativer Ganzzahlwert |
| date part | Jahre, Monate, Tage, Stunden, Minuten oder Sekunden als Zeichenfolge |
| Zeitzonen-ID | Zeichenfolgendarstellung des Zeitzonenwerts. Weitere Informationen finden Sie unter [Datentypen](../expression/data-types.md). Die Zeitzonen-ID muss eine Zeichenfolgenkonstante sein. Er darf weder ein Feldverweis noch ein Ausdruck sein. |

## Signaturen und zurückgegebener Typ

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Gibt einen Datum/Uhrzeit-Wert zurück.

## Beispiele

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Gibt einen Datum/Uhrzeit-Wert von vor genau 2 Stunden zurück.
