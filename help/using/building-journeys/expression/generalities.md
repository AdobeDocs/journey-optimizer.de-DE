---
solution: Journey Optimizer
product: journey optimizer
title: Aufbau
description: Informationen zum erweiterten Ausdruckseditor
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: Syntax, Editor, Journey
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 98%

---

# Aufbau des erweiterten Ausdruckseditors {#syntax}

## Klammern und Priorität von Ausdrücken{#parentheses-and-expression-priority}

Klammern können verwendet werden, um einen komplexen Ausdruck lesbarer zu machen. _(&lt;Ausdruck>)_ entspricht _&lt;Ausdruck>_. Außerdem können mit Klammern die Auswertungsreihenfolge und die Assoziativität definiert werden.

Ausdrücke werden von links nach rechts ausgewertet. Die Assoziativität bei arithmetischen Operatoren muss angewendet werden: Multiplikationen und Divisionen haben Vorrang vor Additionen und Subtraktionen. Um eine bestimmte Reihenfolge durchzusetzen und die Operationen voneinander abzugrenzen, müssen Klammern hinzugefügt werden. Beispiel:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Ausdruck | Auswertung |
|--- |--- |
| `4 + 2 * 10` | <ul><li>„*“ hat Vorrang vor „+“: 2 * 10 wird ausgewertet als → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>Klammern ändern die Priorität: (4 + 2) wird ausgewertet als → 6</li><li> 6 * 10 → 60</li></ul> |

## Groß-/Kleinschreibung{#case-sensitivity}

Im Folgenden finden Sie die verschiedenen Regeln zur Groß- und Kleinschreibung:

* Alle Operatoren (and, or usw.) müssen in Kleinbuchstaben geschrieben werden. Beispiel: _`<expression1>`and`<expression2>`_ ist ein gültiger Ausdruck, _`<expression1>`AND`<expression2>`_ hingegen nicht.
* Bei allen Funktionsnamen ist die Groß-/Kleinschreibung zu berücksichtigen. Beispielsweise ist _inSegment()_ gültig, die Funktion _INSEGMENT()_ dagegen nicht.
* Bei Feldverweisen und konstanten Werten wird zwischen Groß- und Kleinschreibung unterschieden: Sie sind keine integrierten Elemente der Sprache (im Gegensatz zu Operatoren und Funktionen), sondern werden vom Endbenutzer verfasst.

## Zurückgegebener Ausdruckstyp{#returned-expression-type}

Je nach Verwendungskontext kann der Ausdruckseditor verschiedene Werte zurückgeben.

| Verwendung des erweiterten Ausdruckseditors | Erwarteter zurückgegebener Ausdruckstyp |
|--- |--- |
| Bedingung (Bedingung der Datenquelle, Bedingung für das Datum) | boolean |
| Benutzerdefinierter Timer | dateTimeOnly |
| Zuordnung von Aktionsparametern | Beliebig |
