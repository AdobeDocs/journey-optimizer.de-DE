---
solution: Journey Optimizer
product: journey optimizer
title: Operatoren
description: Erfahren Sie mehr über Operatoren in erweiterten Ausdrücken
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: Ausdruck, Syntax, Operatoren, Editor, Journey
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 100%

---

# Operatoren {#operators}

Es gibt zwei Arten von Operatoren: unäre Operatoren und binäre Operatoren. Es gibt unäre Operatoren auf der linken und auf der rechten Seite.

```json
// left-hand unary operators
// <operator> <operand> 
// operand is an expression
not (@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

// right-hand unary operators
// <operator> <operand> 
// operand is an expression
@{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

// binary operators
// <operand1> <operator> <operand2>
// operand is an expression
(@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or (@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com") 
```

## Wichtige Hinweise{#important-notes}

* Bei Verwendung einer Multiplikation (`*`) müssen beide Operationsfelder denselben Typ aufweisen, entweder Ganzzahl oder Dezimalzahl. Beispiel:
   * Das folgende Beispiel ist korrekt: `3.0 * 4.0`
   * `3 * 4.0` führt zu einem Fehler

## Logisch        {#logical}

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
@{BarBeacon.location} is null
```

### is not null

```json
<expression> is not null
```

Das Ergebnis ist boolesch.

Beachten Sie, dass null bedeutet, dass der Ausdruck keinen ausgewerteten Wert hat.

Beispiel:

```json
@{BarBeacon.location} is not null
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
Für &lt;expression1> und &lt;expression2> gibt es keine Kontrolle des Datentyps.

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

Gibt „Die aktuelle Zeit lautet 2019-09-23T09:30:06.693Z“ zurück.

```json
(now()) + " is the current time"
```

Gibt „2019-09-23T09:30:06.693Z ist die aktuelle Zeit“ zurück.

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
(toDateTime("2011-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

Gibt den _dateTime_-Wert 2011-12-03T15:30:30Z zurück.

```json
(toDateTimeOnly("2011-12-03T15:15:30")) + (toDuration("PT15M"))
```

Gibt den _dateTimeOnly_-Wert 2011-12-03T15:30:30 zurück.

```json
(now()) + (toDuration("PT1H"))
```

Gibt einen _dateTime_-Wert (mit UTC-Zeitzone) eine Stunde später als die aktuelle Zeit zurück.

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

Gibt eine _Dauer_ PT2H zurück.
