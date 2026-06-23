---
solution: Journey Optimizer
product: journey optimizer
title: Operatoren
description: Erfahren Sie mehr über Operatoren in erweiterten Ausdrücken
feature: Journeys
role: Developer
level: Experienced
keywords: Ausdruck, Syntax, Operatoren, Editor, Journey
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sK2GNHkkiJ4M5V99Uucc-b68iESNW7kCNBjHVNT-dMs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1001
ht-degree: 54%

---

# Operatoren {#operators}

Es gibt zwei Arten von Operatoren: unäre Operatoren und binäre Operatoren. Es gibt unäre Operatoren auf der linken und auf der rechten Seite.

```json
// left-hand unary operators
// <operator> <operand> 
// operand is an expression
not (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

// right-hand unary operators
// <operator> <operand> 
// operand is an expression
@event{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

// binary operators
// <operand1> <operator> <operand2>
// operand is an expression
(@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com") 
```

## Wichtige Hinweise{#important-notes}

* Bei Verwendung einer Multiplikation (`*`) müssen beide Operationsfelder denselben Typ aufweisen, entweder Ganzzahl oder Dezimalzahl. Beispiel:
   * Das folgende Beispiel ist korrekt: `3.0 * 4.0`
   * `3 * 4.0` führt zu einem Fehler

* Wenn Sie den Operator `+` verwenden, muss der Ausdruck zwischen Klammern eingeschlossen sein. Beispiel:
   * `toDateTimeOnly(toDateTime((currentTimeInMillis()) + 1))` Ist richtig
   * `toDateTimeOnly(toDateTime(currentTimeInMillis() + 1))` führt zu einem Fehler

## Logisch  {#logical}

### und

```json
<expression1> and <expression2>
```

Sowohl &lt;Ausdruck1> als auch &lt;Ausdruck2> müssen boolesch sein. Das Ergebnis ist boolesch.

Beispiel:

```json
3.14 > 2 and 3.15 < 1
```

### oder

```json
<expression1> or <expression2>
```

Sowohl &lt;Ausdruck1> als auch &lt;Ausdruck2> müssen boolesch sein. Das Ergebnis ist boolesch.

Beispiel:

```json
3.14 > 2 or 3.15 < 1
```

### not

```json
not <expression>
```

&lt;Ausdruck> muss boolesch sein. Das Ergebnis ist boolesch.

Beispiel:

```json
not 3.15 < 1
```

## Vergleich {#comparison}

### is null

```json
<expression> is null
```

Das Ergebnis ist boolesch.

Beachten Sie, dass null bedeutet, dass der Ausdruck keinen ausgewerteten Wert hat.

Beispiel:

```json
@event{BarBeacon.location} is null
```

### is not null

```json
<expression> is not null
```

Das Ergebnis ist boolesch.

Beachten Sie, dass null bedeutet, dass der Ausdruck keinen ausgewerteten Wert hat.

Beispiel:

```json
@event{BarBeacon.location} is not null
```

### has null

```json
<expression> has null
```

&lt;Ausdruck> muss eine Liste sein. Das Ergebnis ist boolesch.

Nützlich, um zu ermitteln, dass eine Liste mindestens einen Nullwert enthält.

Beispiel:

```json
["foo", "bar", null] has null
```

Gibt „true“ zurück

```json
["foo", "bar", ""] has null
```

Gibt „false“ zurück, da &quot;&quot; nicht als null betrachtet wird.

### ==

```json
<expression1> == <expression2>
```

>[!NOTE]
>
>Für &lt;expression1> und &lt;expression2> gibt es keine Kontrolle des Datentyps.

Beispiel:

```json
3.14 == 42
```

```json
"foo" == "bar"
```

### !=

```json
<expression1> != <expression2>
```

>[!NOTE]
>
>Für &lt;expression1> und &lt;expression2> gibt es keine Kontrolle des Datentyps.

Das Ergebnis ist boolesch.

Beispiel:

```json
3.14 != 42
```

```json
"foo" != "bar"
```

### >

```json
<expression1> > <expression2>
```

Datum/Uhrzeit kann mit Datum/Uhrzeit verglichen werden.

Datum/Uhrzeit ohne Zeitzone kann mit Datum/Uhrzeit ohne Zeitzone verglichen werden.

Sowohl Ganzzahl als auch Dezimalzahl können mit Ganzzahl oder Dezimalzahl verglichen werden.

Jede andere Kombination ist unzulässig.

Das Ergebnis ist boolesch.

Beispiel:

```json
3.14 > 42
```

### >=

```json
<expression1> >= <expression2>
```

Datum/Uhrzeit kann mit Datum/Uhrzeit verglichen werden.

Datum/Uhrzeit ohne Zeitzone kann mit Datum/Uhrzeit ohne Zeitzone verglichen werden.

Sowohl Ganzzahl als auch Dezimalzahl können mit Ganzzahl oder Dezimalzahl verglichen werden.

Jede andere Kombination ist unzulässig.

Das Ergebnis ist boolesch.

Beispiel:

```json
42 >= 3.14
```

### &lt;

```json
<expression1> < <expression2>
```

Datum/Uhrzeit kann mit Datum/Uhrzeit verglichen werden.

Datum/Uhrzeit ohne Zeitzone kann mit Datum/Uhrzeit ohne Zeitzone verglichen werden.

Sowohl Ganzzahl als auch Dezimalzahl können mit Ganzzahl oder Dezimalzahl verglichen werden.

Jede andere Kombination ist unzulässig.

Das Ergebnis ist boolesch.

Beispiel:

```json
42 < 3.14
```

### &lt;=

```json
<expression1> <= <expression2>
```

Datum/Uhrzeit kann mit Datum/Uhrzeit verglichen werden.

Datum/Uhrzeit ohne Zeitzone kann mit Datum/Uhrzeit ohne Zeitzone verglichen werden.

Sowohl Ganzzahl als auch Dezimalzahl können mit Ganzzahl oder Dezimalzahl verglichen werden.

Jede andere Kombination ist unzulässig.

Das Ergebnis ist boolesch.

Beispiel:

```json
42 <= 3.14
```

## Arithmetisch {#arithmetic}

### +

```json
<expression1> + <expression2>
```

Beide Ausdrücke müssen numerischer Art sein (Ganzzahl oder Dezimalzahl).

Das Ergebnis ist ebenfalls numerisch.

Beispiel:

```json
1 + 2
```

Gibt 3 zurück

### –

```json
<expression1> - <expression2>
```

Beide Ausdrücke müssen numerischer Art sein (Ganzzahl oder Dezimalzahl).

Das Ergebnis ist ebenfalls numerisch.

Beispiel:

```json
2 - 1 
```

Gibt 1 zurück

### /

```json
<expression1> / <expression2>
```

Beide Ausdrücke müssen numerischer Art sein (Ganzzahl oder Dezimalzahl).

Das Ergebnis ist ebenfalls numerisch.

&lt;Ausdruck2> darf nicht gleich 0 sein (gibt 0 zurück).

Beispiel:

```json
4 / 2
```

Gibt 2 zurück

### *

```json
<expression1> * <expression2>
```

Beide Ausdrücke müssen numerischer Art sein (Ganzzahl oder Dezimalzahl).

Das Ergebnis ist ebenfalls numerisch.

Beispiel:

```json
3 * 4
```

Gibt 12 zurück

### %

```json
<expression1> % <expression2>
```

Beide Ausdrücke müssen numerischer Art sein (Ganzzahl oder Dezimalzahl).

Das Ergebnis ist ebenfalls numerisch.

Beispiel:

```json
3 % 2
```

Gibt 1 zurück.

## Math {#math}

### is numeric

```json
<expression> is numeric
```

Der Typ des Ausdrucks ist Ganzzahl oder Dezimalzahl.

Beispiel:

```json
@ is numeric
```

### is integer

```json
<expression> is integer
```

Der Typ des Ausdrucks ist Ganzzahl.

Beispiel:

```json
@ is integer
```

### is decimal

```json
<expression> is decimal
```

Der Typ des Ausdrucks ist Dezimalzahl.

Beispiel:

```json
@ is decimal
```

## Zeichenfolge {#string}

### +

```json
<string> + <expression>
```

```json
<expression> + <string>
```

Damit werden zwei Ausdrücke verkettet.

Ein Ausdruck muss eine verkettete Zeichenfolge sein.

Beispiel:

```json
"the current time is " + (now())
```

Gibt „Die aktuelle Zeit lautet 2023-09-23T09:30:06.693Z“ zurück.

```json
(now()) + " is the current time"
```

Gibt „2023-09-23T09:30:06.693Z ist die aktuelle Zeit“ zurück.

```json
"a" + "b" + "c" + 1234
```

Gibt „abc1234“ zurück.

## Datum {#date}

### +

```json
<expression> + <duration>
```

Anhängen einer Dauer an einen „dateTime“, einen „dateTimeOnly“ oder eine Dauer.

Beispiel:

```json
(toDateTime("2023-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

Gibt den _dateTime_-Wert 2023-12-03T15:30:30Z zurück.

```json
(toDateTimeOnly("2023-12-03T15:15:30")) + (toDuration("PT15M"))
```

Gibt den _dateTimeOnly_-Wert 2023-12-03T15:30:30 zurück.

```json
(now()) + (toDuration("PT1H"))
```

Gibt einen _dateTime_-Wert (mit UTC-Zeitzone) eine Stunde später als die aktuelle Zeit zurück.

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

Gibt eine _Dauer_ PT2H zurück.

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Diese Seite enthält eine vollständige Referenz der im erweiterten Ausdruckseditor von Journey verfügbaren Operatoren und behandelt logische (`and`, `or`, `not`), Vergleiche (`==`, `!=`, `>`, `>=`, `<`, `<=`,,,,,,,, `%`), arithmetische (`is numeric` `is integer` `is decimal`, `*`, `is null`, `is not null` `has null` `+` `-` `/`), Zeichenfolgenverkettung und arithmetische Datumsoperatoren.

**intents:**

* Kombinieren Sie boolesche Bedingungen mithilfe der logischen Operatoren `and`, `or` und `not`
* Überprüfen, ob ein Feld- oder Ausdruckswert null oder nicht null ist, mithilfe von `is null`/`is not null`
* Erkennen von Nullwerten innerhalb einer Liste mithilfe des `has null` Operators
* Vergleichen Sie numerische, datetime- und datetimeonly-Werte mithilfe von `>`, `>=`, `<`, `<=`, `==` und `!=`
* Ausführen von Berechnungen für numerische Werte mithilfe von `+`, `-`, `/`, `*` und `%`
* Hinzufügen einer Dauer zu einem dateTime-, dateTimeOnly- oder duration-Wert mit dem `+` Operator

**Glossar:**

* **Unärer Operator** Ein Operator, der auf einen einzelnen Operanden angewendet wird. Kann links (z. B. `not`) oder rechts (z. B. `is null`) *(produktspezifisch) sein*
* **Binärer Operator** Ein Operator, der zwischen zwei Operanden angewendet wird (z. B. `and`, `==`, `+`) *(produktspezifisch)*
* **Hat null**: Ein unärer Operator auf der rechten Seite, der „true“ zurückgibt, wenn eine Liste mindestens ein Null-Element enthält *(produktspezifisch)*
* **ist numerisch / ist Ganzzahl / ist Dezimalzahl**: Typprüfungsoperatoren, die einen booleschen Wert zurückgeben, basierend auf dem numerischen Untertyp des Ausdrucks *(produktspezifisch)*

**Leitplanken:**

* Bei Verwendung der Multiplikation (`*`) müssen beide Operanden denselben numerischen Typ aufweisen (sowohl Ganzzahl als auch beide Dezimalzahlen). Beim Mischen wird ein Fehler verursacht
* Bei Verwendung des `+` Operators für die Datumsarithmetik muss der Ausdruck in Klammern eingeschlossen werden, um Parsing-Fehler zu vermeiden
* Vergleichsoperatoren (`>`, `>=`, `<`, `<=`) sind nur zwischen kompatiblen Typen gültig: „Datetime“ mit „Datetime“, „DatetimeOnly“ mit „DatetimeOnly“ oder „numerisch“ mit „numerisch“. Jede andere Kombination ist verboten
* Eine leere Zeichenfolge `""` wird nicht als null betrachtet, `has null` für eine Liste mit `""` „false“ zurückgibt.
* Die `==`- und `!=`-Operatoren führen keine Datentypsteuerung zwischen Operanden durch

**Terminologie:**

* Kanonischer Name: Operatoren — Akronym: none — Varianten: Ausdrucksoperatoren, Journey-Operatoren
* Synonyme: `and` = „Logical AND“; `or` = „Logical OR“; `not` = „Logical NOT“; `%` = „modulo“
* Verwechseln Sie nicht: `is null` (Ausdruck hat keinen ausgewerteten Wert) ≠ `== null` (keine gültige Syntax); `has null` (Liste enthält null) ≠ `is null` (Ausdruck selbst ist null)

**FAQ:**

* **F: Kann ich eine Ganzzahl direkt mit einer Dezimalzahl multiplizieren?** — Nein; beide Operanden von `*` müssen vom gleichen Typ sein. Verwenden Sie `3.0 * 4.0` (beide Dezimalzahlen) oder `3 * 4` (beide Ganzzahlen).
* **F: Wie füge ich 15 Minuten zu einer Uhrzeit hinzu?** — `(toDateTime("...")) + (toDuration("PT15M"))` verwenden.
* **F: Was ist der Unterschied zwischen `is null` und `has null`?** — `is null` prüft, ob ein einzelner Ausdruck keinen ausgewerteten Wert hat; `has null` prüft, ob eine Liste mindestens ein Null-Element enthält.
* **F: Gibt `"" has null` „true“ zurück?** — Nein; eine leere Zeichenfolge wird nicht als null betrachtet, sodass das Ergebnis „false“ ist.
* **F: Warum verursacht `3 * 4.0` einen Fehler?** — Der `*` Operator erfordert, dass beide Operanden vom gleichen numerischen Typ sind; das Mischen von Ganzzahl und Dezimalzahl ist nicht zulässig.

+++
