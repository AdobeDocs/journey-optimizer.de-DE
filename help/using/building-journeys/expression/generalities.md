---
solution: Journey Optimizer
product: journey optimizer
title: Syntax
description: Erfahren Sie mehr über den erweiterten Ausdruckseditor
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# Syntax des erweiterten Ausdruckseditors {#syntax}

## Klammern und Priorität von Ausdrücken{#parentheses-and-expression-priority}

Klammern können verwendet werden, um einen komplexen Ausdruck lesbarer zu machen. _(&lt;expression>)_ entspricht _&lt;expression>_. Mit Klammern können auch die Auswertungsreihenfolge und die Assoziativität definiert werden.

Die Ausdrücke werden von links nach rechts ausgewertet. Die Assoziativität bei arithmetischen Operatoren muss angewendet werden: Multiplikationen und Divisionen haben Vorrang vor Additionen und Subtraktionen. Um eine bestimmte Reihenfolge durchzusetzen, müssen Klammern hinzugefügt werden, um die Vorgänge zu begrenzen. Beispiel:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Ausdruck | Auswertung |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&#39;*&#39; hat Vorrang vor &#39;+&#39;: 2 * 10 wird ausgewertet → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>Die Klammern ändern die Priorität: (4 + 2) wird ausgewertet als → 6</li><li> 6 * 10 → 60</li></ul> |

## Groß-/Kleinschreibung{#case-sensitivity}

Im Folgenden finden Sie die unterschiedlichen Regeln zur Groß-/Kleinschreibung:

* Alle Operatoren (und, oder usw.) sollte in Kleinbuchstaben geschrieben werden. Beispiel: _`<expression1>`und`<expression2>`_ ist ein gültiger Ausdruck, während der Ausdruck _`<expression1>`UND`<expression2>`_ ist nicht.
* Bei allen Funktionsnamen wird zwischen Groß- und Kleinschreibung unterschieden. Beispiel: _inSegment()_ ist gültig, während die Funktion _INSEGMENT()_ ist nicht.
* Bei Feldverweisen und konstanten Werten wird zwischen Groß- und Kleinschreibung unterschieden: sie sind keine integrierten Elemente der Sprache (im Gegensatz zu Operatoren und Funktionen), werden sie vom Endbenutzer verfasst.

## Zurückgegebener Ausdruckstyp{#returned-expression-type}

Je nach Verwendungskontext kann der Ausdruckseditor unterschiedliche Werte zurückgeben.

| Verwendung des erweiterten Ausdruckseditors | Erwarteter zurückgegebener Ausdruckstyp |
|--- |--- |
| Bedingung (Bedingung der Datenquelle, Bedingung des Datums) | boolean |
| Benutzerdefinierter Timer | dateTimeOnly |
| Zuordnung von Aktionsparametern | Alle |
