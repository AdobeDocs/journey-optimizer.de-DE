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
TQID: https://experienceleague.adobe.com/-PTYUf-njT3-LsI-A5IKEMDGOl4JecZ-ayM0rU4f2HI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 620
ht-degree: 40%

---

# Syntax des erweiterten Ausdruckseditors {#syntax}

Die Grundlagen der Syntax bei der Verwendung des [erweiterten Ausdruckseditors](expressionadvanced.md) sind nachfolgend aufgeführt. <!-- Samples of use of the advanced expression editor are available on [this page](advanced-editor-use-cases.md).-->

## Klammern und Priorität von Ausdrücken {#parentheses-and-expression-priority}

Klammern können verwendet werden, um einen komplexen Ausdruck lesbarer zu machen. _(&lt;Ausdruck>)_ entspricht _&lt;Ausdruck>_. Außerdem können mit Klammern die Auswertungsreihenfolge und die Assoziativität definiert werden.

Ausdrücke werden von links nach rechts ausgewertet. Die Assoziativität bei arithmetischen Operatoren muss angewendet werden: Multiplikationen und Divisionen haben Vorrang vor Additionen und Subtraktionen. Um eine bestimmte Reihenfolge durchzusetzen und die Operationen voneinander abzugrenzen, müssen Klammern hinzugefügt werden. Beispiel:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Ausdruck | Auswertung |
|--- |--- |
| `4 + 2 * 10` | <ul><li>„*“ hat Vorrang vor „+“: 2 \* 10 wird ausgewertet → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>Klammern ändern die Priorität: (4 + 2) wird ausgewertet als → 6</li><li> 6 * 10 → 60</li></ul> |

## Groß-/Kleinschreibung {#case-sensitivity}

Im Folgenden finden Sie die verschiedenen Regeln zur Groß- und Kleinschreibung:

* Alle Operatoren (and, or usw.) müssen in Kleinbuchstaben geschrieben werden. Beispiel: _`<expression1>`and`<expression2>`_ ist ein gültiger Ausdruck, _`<expression1>`AND`<expression2>`_ hingegen nicht.
* Bei allen Funktionsnamen ist die Groß-/Kleinschreibung zu berücksichtigen. Beispielsweise ist _inAudience()_ gültig, die Funktion _INAUDIENCE()_ dagegen nicht.
* Bei Feldverweisen und konstanten Werten wird zwischen Groß- und Kleinschreibung unterschieden: Sie sind keine integrierten Elemente der Sprache (im Gegensatz zu Operatoren und Funktionen), sondern werden vom Endbenutzer verfasst.

## Zurückgegebener Ausdruckstyp {#returned-expression-type}

Je nach Verwendungskontext kann der Ausdruckseditor verschiedene Werte zurückgeben.

| Verwendung des erweiterten Ausdruckseditors | Erwarteter zurückgegebener Ausdruckstyp |
|--- |--- |
| Bedingung (Bedingung der Datenquelle, Bedingung für das Datum) | boolean |
| Benutzerdefinierter Timer | dateTimeOnly |
| Zuordnung von Aktionsparametern | Beliebig |

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite werden die grundlegenden Syntaxregeln des erweiterten Journey-Ausdruckseditors behandelt: Operatorpriorität mit Klammern, Groß-/Kleinschreibung für Operatoren und Funktionen und der erwartete Rückgabetyp für jeden Editor-Kontext.

**intents:**

* Reihenfolge der Auswertung von Steuerausdrücken durch Einschließen von Unterausdrücken in Klammern
* Schreiboperatoren (`and`, `or`, `not`) in Kleinbuchstaben, um Syntaxfehler zu vermeiden
* Verwenden von Funktionsnamen in richtiger Groß-/Kleinschreibung (z. B. `inAudience()` nicht `INAUDIENCE()`)
* Verstehen Sie, dass Bedingungen einen booleschen Wert zurückgeben müssen, benutzerdefinierte Zeitgeber `dateTimeOnly` zurückgeben müssen und Aktionsparameterzuordnungen jeden Typ zurückgeben können

**Glossar:**

* **Ausdruckspriorität**: Die Reihenfolge, in der Operatoren ausgewertet werden. Multiplikationen und Divisionen haben Vorrang vor Additionen und Subtraktionen *(produktspezifisch)*
* **Groß**/Kleinschreibung: Im erweiterten Editor müssen Operatoren in Kleinbuchstaben geschrieben sein, bei Funktionsnamen wird zwischen Groß- und Kleinschreibung unterschieden und bei Feldverweisen wird zwischen Groß- und Kleinschreibung unterschieden, wie sie vom Benutzer verfasst wurden *(produktspezifisch)*
* **dateTimeOnly**: Der für benutzerdefinierte Timer-Ausdrücke (Warteaktivität) erforderliche Rückgabetyp. Stellt eine Datums-/Uhrzeitangabe ohne Zeitzone *produktspezifisch) dar*

**Leitplanken:**

* Operatoren (`and`, `or`, `not` usw.) Muss in Kleinbuchstaben geschrieben werden — Varianten in Großbuchstaben sind ungültig
* Bei allen Funktionsnamen wird zwischen Groß- und Kleinschreibung unterschieden. `inAudience()` ist gültig, `INAUDIENCE()` jedoch nicht
* Die Arithmetik folgt der Standardpriorität: `*` und `/` werden vor dem `+` und `-` ausgewertet. Verwenden Sie Klammern zum Überschreiben.
* Bedingungen geben immer einen booleschen Wert zurück; benutzerdefinierte Zeitgeber geben immer `dateTimeOnly` zurück

**Terminologie:**

* Kanonischer Name: Advanced Expression Editor Syntax — Akronym: none — Varianten: Ausdruckssyntax, Editor-Syntax
* Synonyme: „Ausdruckspriorität“ = „Operatorpriorität“; „Klammern“ = „Klammern“ (im Ausdruckskontext)
* Verwechseln Sie nicht: Groß-/Kleinschreibung des Benutzers (Benutzer müssen Kleinbuchstaben verwenden) ≠ Groß-/Kleinschreibung bei Feldreferenzen (Feldnamen werden vom Benutzer verfasst und unterscheiden nach Groß-/Kleinschreibung wie geschrieben)

**FAQ:**

* **F: Wird `4 + 2 * 10` auf 60 oder 24 ausgewertet?** — Es wird auf 24 ausgewertet, weil `*` Priorität vor `+` hat. Verwenden Sie `(4 + 2) * 10`, um 60 zu erhalten.
* **F: Kann ich `AND` in einem Ausdruck in Großbuchstaben schreiben?** — Nein; alle Operatoren müssen in Kleinbuchstaben geschrieben werden (`and`, `or`, `not`).
* **F: Wird bei Funktionsnamen zwischen Groß- und Kleinschreibung unterschieden?** — Ja; `inAudience()` ist gültig, aber `INAUDIENCE()` nicht.
* **F: Welchen Typ muss ein Bedingungsausdruck zurückgeben?** — Ein boolescher Wert.
* **F: Welcher Rückgabetyp ist für einen benutzerdefinierten Timer-Ausdruck der Warteaktivität erforderlich?** — `dateTimeOnly`.

+++
