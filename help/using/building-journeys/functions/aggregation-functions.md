---
product: journey optimizer
title: Aggregationsfunktionen
description: Informationen zu Aggregationsfunktionen
feature: Journeys
role: Developer
level: Experienced
keywords: Aggregation, Funktionen, Ausdruck, Journey, Durchschnitt, Anzahl, Max, Min, Summe
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: ht
source-wordcount: '717'
ht-degree: 100%

---

# Aggregationsfunktionen {#aggregation-functions}

Aggregationsfunktionen führen Berechnungen für einen Satz von Werten durch und geben ein einziges zusammengefasstes Ergebnis zurück. Mit diesen Funktionen können Sie Daten innerhalb Ihrer Journey-Ausdrücke analysieren, indem Sie Durchschnittswerte berechnen, Minimal- und Maximalwerte ermitteln, Elemente zählen und numerische Werte summieren.

Verwenden Sie Aggregationsfunktionen, wenn Sie Folgendes tun müssen:

* Berechnen von statistischen Werte aus Listen oder Arrays ([avg](#avg), [sum](#sum), [min](#min), [max](#max))
* Zählen von Elementen in Sammlungen ([count](#count), [countOnlyNull](#countOnlyNull), [countWithNull](#countWithNull)), mit Optionen zum Ein- oder Ausschließen von Nullwerten
* Bestimmen eindeutiger Werte innerhalb von Datensätzen ([distinctCount](#distinctCount), [distinctCountWithNull](#distinctCountWithNull))
* Treffen von datengestützten Entscheidungen basierend auf berechneten Metriken

Aggregationsfunktionen verarbeiten Nullwerte automatisch entsprechend ihrem spezifischen Verhalten und erleichtern so die Arbeit mit realen Daten, die fehlende oder undefinierte Werte enthalten können.


## avg {#avg}

Gibt den Durchschnittswert eines Satzes von Ausdrücken zurück, entweder als Liste oder in Form von zwei Ausdrücken. Nullwerte werden ignoriert.

+++Syntax

`avg(<parameter>)`

+++

+++Parameter

Unterstützte Typen:

* listInteger
* listDecimal
* decimal
* integer

+++

+++Signaturen und zurückgegebener Typ

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Gibt eine Dezimalzahl zurück.

+++

+++Beispiele

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

Gibt 7.0 zurück.

`avg(10.2, 3)`

Gibt 6.6 zurück.

+++

## count {#count}

Zählt die Elemente der Liste, wobei Nullwerte nicht berücksichtigt werden.

+++Syntax

`count(<listAny>)`

`count(<listObject>)`

+++

+++Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly oder listObject | Zu verarbeitende Liste. Bei listObject muss es sich um einen Feldverweis handeln. Ein listObject kann kein Null-Objekt enthalten. |

+++

+++Signaturen und zurückgegebener Typ

`count(<listAny>)`

Gibt eine Ganzzahl zurück.

+++

+++Beispiele

`count([10,2,10,null])`

Gibt 3 zurück.

`count(@event{my_event.productListItems})`

Gibt die Anzahl der Objekte im angegebenen Array von Objekten zurück (listObject-Typ). Anmerkung: Ein listObject kann kein Null-Objekt enthalten.

+++

## countOnlyNull {#countOnlyNull}

Zählt die Zahl der Nullwerte in der Liste.

+++Syntax

`countOnlyNull(<listAny>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Signaturen und zurückgegebener Typ

`countOnlyNull(<listAny>)`

Gibt eine Ganzzahl zurück.

+++

+++Beispiele

`countOnlyNull([10,2,10,null])`

Gibt 1 zurück.

+++

**Hinweis:** Beachten Sie, dass der Parameter `<listObject>` in dieser Funktion nicht unterstützt wird.

## countWithNull {#countWithNull}

Zählt alle Elemente der Liste, einschließlich Nullwerten.

+++Syntax

`countWithNull(<listAny>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Signaturen und zurückgegebener Typ

`countWithNull(<listAny>)`

Gibt eine Ganzzahl zurück.

+++

+++Beispiele

`countWithNull([10,2,10,null])`

Gibt 4 zurück.

+++

**Hinweis:** Beachten Sie, dass der Parameter `<listObject>` in dieser Funktion nicht unterstützt wird.

## distinctCount {#distinctCount}

Zählt die Anzahl verschiedener Werte, wobei Nullwerte ignoriert werden.

+++Syntax

`distinctCount(<listAny>)`

+++

+++Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly oder listObject | Zu verarbeitende Liste. Bei listObject muss es sich um einen Feldverweis handeln. |
| keyAttributeName | Zeichenfolge | Dieser Parameter ist optional und nur für listObject. Wenn der Parameter nicht angegeben wird, wird ein Objekt als doppelt betrachtet, wenn alle Attribute dieselben Werte aufweisen. Andernfalls wird ein Objekt als doppelt betrachtet, wenn das angegebene Attribut denselben Wert aufweist. |

+++

+++Signaturen und zurückgegebener Typ

`distinctCount(<listAny>)`

Gibt eine Ganzzahl zurück.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

Gibt eine Liste mit Objekten zurück.

+++

+++Beispiele

`distinctCount([10,2,10,null])`

Gibt 2 zurück.

`distinctCount(@event{my_event.productListItems})`

Gibt die Anzahl der eindeutig voneinander unabhängigen Objekte im angegebenen Array von Objekten (listObject-Typ) zurück.

`distinctCount(@event{my_event.productListItems}, "SKU")`

Gibt die Anzahl der Objekte mit einem eindeutigen „SKU“-Attributwert{} zurück.

+++

## distinctCountWithNull {#distinctCountWithNull}

Zählt die Anzahl verschiedener Werte einschließlich der Nullwerte.

+++Syntax

`distinctCountWithNull(<listAny>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Signaturen und zurückgegebener Typ

`distinctCountWithNull(<listAny>)`

Gibt eine Ganzzahl zurück.

+++

+++Beispiele

`distinctCountWithNull([10,2,10,null])`

Gibt 3 zurück.

+++

**Hinweis:** Beachten Sie, dass der Parameter `<listObject>` in dieser Funktion nicht unterstützt wird.

## max {#max}

Gibt den Maximalwert aus einem Satz von Ausdrücken zurück, entweder als Liste oder in Form von zwei Ausdrücken. Nullwerte werden ignoriert.

+++Syntax

`max(<parameter>)`

+++

+++Parameter

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duration
* integer
* decimal
* dateTime
* dateTimeOnly

+++

+++Signaturen und zurückgegebene Typen

`max(<listDuration>)`

Gibt eine Dauer zurück.

`max(<listInteger>)`

Gibt eine Dauer zurück.

`max(<listDateTimeOnly>)`

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

`max(<listDateTime>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

`max(<listDateOnly>)`

Gibt ein Datum zurück.

`max(<listDecimal>)`

Gibt eine Dezimalzahl zurück.

`max(<decimal>,<decimal>)`

Gibt eine Dezimalzahl zurück.

`max(<duration>,<duration>)`

Gibt eine Dauer zurück.

`max(<dateTime>,<dateTime>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

`max(<dateTimeOnly>,<dateTimeOnly>)`

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

`max(<integer>,<integer>)`

Gibt eine Ganzzahl zurück.

+++

+++Beispiele

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

Gibt 10 zurück.

`max([10,null,8])`

Gibt 10 zurück.

+++

## min {#min}

Gibt den Minimalwert aus einem Satz von Ausdrücken zurück, entweder als Liste oder in Form von zwei Ausdrücken. Nullwerte werden ignoriert.

+++Syntax

`min(<parameters>)`

+++

+++Parameter

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duration
* integer
* decimal
* dateTime
* dateTimeOnly

+++

+++Signaturen und zurückgegebene Typen

`min(<listDuration>)`

Gibt eine Dauer zurück.

`min(<listInteger>)`

Gibt eine Dauer zurück.

`min(<listDateTimeOnly>)`

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

`min(<listDateTime>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

`min(<listDateOnly>)`

Gibt ein Datum zurück.

`min(<listDecimal>)`

Gibt eine Dezimalzahl zurück.

`min(<decimal>,<decimal>)`

Gibt eine Dezimalzahl zurück.

`min(<duration>,<duration>)`

Gibt eine Dauer zurück.

`min(<dateTime>,<dateTime>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

`min(<dateTimeOnly>,<dateTimeOnly>)`

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

`min(<integer>,<integer>)`

Gibt eine Ganzzahl zurück.

+++

+++Beispiele

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

Gibt 3 zurück.

`min([10,null,8])`

Gibt 8 zurück.

+++

## sum {#sum}

Gibt die Summe der Werte eines Satzes von Ausdrücken zurück. Nullwerte werden ignoriert.

+++Syntax

`sum(<parameters>)`

+++

+++Parameter

* listInteger
* listDecimal
* duration
* integer
* decimal

+++

+++Signaturen und zurückgegebene Typen

`sum(<listDecimal>)`

Gibt eine Dezimalzahl zurück.

`sum(<listInteger>)`

Gibt eine Ganzzahl zurück.

`sum(<integer>,<integer>)`

Gibt eine Ganzzahl zurück.

`sum(<decimal>,<decimal>)`

Gibt eine Dezimalzahl zurück.

+++

+++Beispiele

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

Gibt 21 zurück.

`sum([10.5,null,8.1])`

Gibt 18.6 zurück.

+++
