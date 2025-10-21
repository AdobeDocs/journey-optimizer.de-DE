---
solution: Journey Optimizer
product: journey optimizer
title: Syntax des erweiterten Ausdruckseditors
description: Weitere Informationen zur im erweiterten Ausdruckseditor verwendete Syntax
feature: Journeys
role: Developer
level: Experienced
keywords: Syntax, Editor, Journey
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 96%

---

# Syntax des erweiterten Ausdruckseditors {#syntax}

Die Grundlagen der Syntax bei der Verwendung des [erweiterten Ausdruckseditors](expressionadvanced.md) sind nachfolgend aufgeführt. <!-- Samples of use of the advanced expression editor are available on [this page](advanced-editor-use-cases.md).-->

## Klammern und Priorität von Ausdrücken {#parentheses-and-expression-priority}

Klammern können verwendet werden, um einen komplexen Ausdruck lesbarer zu machen. _(&lt;Ausdruck>)_ entspricht _&lt;Ausdruck>_. Außerdem können mit Klammern die Auswertungsreihenfolge und die Assoziativität definiert werden.

Ausdrücke werden von links nach rechts ausgewertet. Die Assoziativität bei arithmetischen Operatoren muss angewendet werden: Multiplikationen und Divisionen haben Vorrang vor Additionen und Subtraktionen. Um eine bestimmte Reihenfolge durchzusetzen und die Operationen voneinander abzugrenzen, müssen Klammern hinzugefügt werden. Beispiel:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Ausdruck | Auswertung |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&#39;*&#39; hat Priorität vor &#39;+&#39;: 2 \* 10 wird → 20 ausgewertet</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>Klammern ändern die Priorität: (4 + 2) wird ausgewertet als → 6</li><li> 6 * 10 → 60</li></ul> |

## Groß-/Kleinschreibung {#case-sensitivity}

Im Folgenden finden Sie die verschiedenen Regeln zur Groß- und Kleinschreibung:

* Alle Operatoren (und, oder, usw.) sollten in Kleinbuchstaben geschrieben werden. Beispiel: _`<expression1>`and`<expression2>`_ ist ein gültiger Ausdruck, _`<expression1>`AND`<expression2>`_ hingegen nicht.
* Bei allen Funktionsnamen ist die Groß-/Kleinschreibung zu berücksichtigen. Beispielsweise ist _inAudience()_ gültig, die Funktion _INAUDIENCE()_ dagegen nicht.
* Bei Feldverweisen und konstanten Werten wird zwischen Groß- und Kleinschreibung unterschieden: Sie sind keine integrierten Elemente der Sprache (im Gegensatz zu Operatoren und Funktionen), sondern werden vom Endbenutzer verfasst.

## Zurückgegebener Ausdruckstyp {#returned-expression-type}

Je nach Verwendungskontext kann der Ausdruckseditor verschiedene Werte zurückgeben.

| Verwendung des erweiterten Ausdruckseditors | Erwarteter zurückgegebener Ausdruckstyp |
|--- |--- |
| Bedingung (Bedingung der Datenquelle, Bedingung für das Datum) | boolean |
| Benutzerdefinierter Timer | dateTimeOnly |
| Zuordnung von Aktionsparametern | Beliebig |
