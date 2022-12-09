---
solution: Journey Optimizer
product: journey optimizer
title: Benutzer
description: Erfahren Sie mehr über Operatoren in erweiterten Ausdrücken
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Benutzer {#operators}

Es gibt zwei Arten von Operatoren: unäre Operatoren und binäre Operatoren. Es gibt unäre Operatoren auf der linken und auf der rechten Seite.

```json
    // left-hand unary operators
    <operator> <operand> // operand is an expression
    not (@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

    // right-hand unary operators
    <operand> <operator> // operand is an expression
    @{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

    // binary operators
    <operand1> <operator> <operand2>
    (@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or
    (@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com")
```

## Wichtige Hinweise{#important-notes}

* Bei Verwendung einer Multiplikation (`*`), müssen beide Vorgangsfelder denselben Typ aufweisen, entweder Ganzzahl oder Dezimalzahl. Beispiel :
   * das folgende Beispiel stimmt: `3.0 * 4.0`
   * `3 * 4.0` führt zu einem Fehler

## Logisch  {#logical}

### und

```json
<expression1> and <expression2>
```

Beide &lt;expression1> und &lt;expression2> muss boolesch sein. Das Ergebnis ist boolesch.

Beispiel:

```json
3.14 > 2 and 3.15 < 1
```

### oder



```json
<expression1> or <expression2>
```

Beide &lt;expression1> und &lt;expression2> muss boolesch sein. Das Ergebnis ist boolesch.

Beispiel:

```json
3.14 > 2 or 3.15 < 1
```

### not



```json
not <expression>
```

&lt;expression> muss boolesch sein. Das Ergebnis ist boolesch.

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

&lt;expression> muss eine Liste sein. Das Ergebnis ist boolesch.

Nützlich, um zu erkennen, dass eine Liste mindestens einen Nullwert enthält.

Beispiel:

```json
["foo", "bar", null] has null --  returns true.
```

```json
["foo", "bar", ""] has null -- returns false because "" is not considered as null.
```

### ==



```json
<expression1> == <expression2>
```

>[!NOTE]
>
>Für &lt;expression1> und &lt;expression2> Es gibt keine Kontrolle des Datentyps.

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
Für &lt;expression1> und &lt;expression2> Es gibt keine Kontrolle des Datentyps.

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

Datetimeonly kann mit Datetimeonly verglichen werden.

Sowohl Ganzzahl als auch Dezimalzahl können mit Ganzzahl oder Dezimalzahl verglichen werden.

Jede andere Kombination ist verboten.

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

Datetimeonly kann mit Datetimeonly verglichen werden.

Sowohl Ganzzahl als auch Dezimalzahl können mit Ganzzahl oder Dezimalzahl verglichen werden.

Jede andere Kombination ist verboten.

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

Datetimeonly kann mit Datetimeonly verglichen werden.

Sowohl Ganzzahl als auch Dezimalzahl können mit Ganzzahl oder Dezimalzahl verglichen werden.

Jede andere Kombination ist verboten.

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

Datetimeonly kann mit Datetimeonly verglichen werden.

Sowohl Ganzzahl als auch Dezimalzahl können mit Ganzzahl oder Dezimalzahl verglichen werden.

Jede andere Kombination ist verboten.

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

Beide Ausdrücke müssen numerisch sein (Ganzzahl oder Dezimalzahl).

Das Ergebnis ist ebenfalls numerisch.

Beispiel:

```json
1 + 2 -- returns 3
```

### -



```json
<expression1> - <expression2>
```

Beide Ausdrücke müssen numerisch sein (Ganzzahl oder Dezimalzahl).

Das Ergebnis ist ebenfalls numerisch.

Beispiel:

```json
2 - 1 -- returns 1
```

### /



```json
<expression1> / <expression2>
```

Beide Ausdrücke müssen numerisch sein (Ganzzahl oder Dezimalzahl).

Das Ergebnis ist ebenfalls numerisch.

&lt;expression2> darf nicht gleich 0 sein (gibt 0 zurück).

Beispiel:

```json
4 / 2 -- returns 2
```

### *



```json
<expression1> * <expression2>
```

Beide Ausdrücke müssen numerisch sein (Ganzzahl oder Dezimalzahl).

Das Ergebnis ist ebenfalls numerisch.

Beispiel:

```json
3 * 4 -- returns 12
```

### %



```json
<expression1> % <expression2>
```

Beide Ausdrücke müssen numerisch sein (Ganzzahl oder Dezimalzahl).

Das Ergebnis ist ebenfalls numerisch.

Beispiel:

```json
3 % 2 -- returns 1.
```

## Mathematisch {#math}

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

Der Typ des Ausdrucks ist integer.

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

Es verkettet zwei Ausdrücke.

Ein Ausdruck muss eine verkettete Zeichenfolge sein.

Beispiel:

```json
"the current time is " + (now()) -- returns "the current time is 2019-09-23T09:30:06.693Z"
```

```json
(now()) + " is the current time" -- returns "2019-09-23T09:30:06.693Z is the current time"
```

```json
"a" + "b" + "c" + 1234 -- returns "abc1234".
```

## Datum {#date}

### +



```json
<expression> + <duration>
```

Hängen Sie eine Dauer an eine dateTime, eine dateTimeOnly oder eine Dauer an.

Beispiel:

```json
toDateTime("2011-12-03T15:15:30Z") + toDuration("PT15M") -- returns 2011-12-03T15:30:30Z
```

```json
toDateTimeOnly("2011-12-03T15:15:30") + toDuration("PT15M") -- returns 2011-12-03T15:30:30
```

```json
now() + toDuration("PT1H") -- returns a dateTime (with UTC time zone) one hour later from current time
```

```json
toDuration("PT1H") + toDuration("PT1H") -- returns  PT2H
```
