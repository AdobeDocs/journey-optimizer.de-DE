---
solution: Journey Optimizer
product: journey optimizer
title: Datentypen
description: Erfahren Sie mehr über Datentypen in erweiterten Ausdrücken
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: fdfc3287-d733-45fb-ad11-b4238398820a
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---

# Datentypen {#data-types}

Technisch gesehen enthält eine Konstante immer einen Datentyp. Im Literalausdruck wird nur der Wert angegeben. Der Datentyp kann aus dem Wert abgeleitet werden (z. B. Zeichenfolge, Ganzzahl, Dezimalzahl usw.). Für bestimmte Fälle, z. B. Datum und Uhrzeit, verwenden wir spezielle Funktionen für die Darstellung.

Die folgenden Abschnitte enthalten Informationen zu den verschiedenen Datentypausdrücken und dazu, wie sie dargestellt werden.

## Zeichenfolge {#string}

**Beschreibung**

Allgemeine Zeichenfolge. Es hat keine bestimmte Größe außer der impliziten Größe, die aus der Umgebung stammt, wie z. B. die verfügbare Speichermenge.

JSON-Format: Zeichenfolge

Serialisierungsformat: UTF-8

**Wörtliche Darstellung**

```json
"<value>"
```

```json
'<value>'
```

**Beispiel**

```json
"hello world"
```

```json
'hello world'
```

## integer {#integer}

**Beschreibung**

Ganzzahlwert von -2^63 bis 2^63-1.

JSON-Format: Zahl

**Wörtliche Darstellung**

```json
<integer value>
```

**Beispiel**

```json
42
```

## decimal {#decimal}

**Beschreibung**

Dezimalzahl. Sie stellt einen Gleitkommawert dar:

* größter positiver endlicher Wert des Typs &quot;double&quot;, (2-2^-52)x2^1023
* kleinster positiver Normalwert des Typs &quot;double&quot;, 2-1022
* kleinster positiver Wert ungleich null des Typs &quot;double&quot;, 2 p-1074

JSON-Format: Zahl

Serialisierungsformat: mit &#39;.&#39; als Dezimaltrennzeichen.

**Wörtliche Darstellung**

```json
<integer value>.<integer value>
```

**Beispiel**

```json
3.14
```

## boolean {#boolean}

**Beschreibung**

Boolescher Wert in Kleinbuchstaben geschrieben: true oder false

JSON-Format: Boolesch

**Wörtliche Darstellung**

```json
true
```

```json
false
```

**Beispiel**

```json
true
```

## dateOnly {#date-only}

**Beschreibung**

Stellt ein Datum nur ohne Zeitzone dar, das als Jahr-Monat-Tag betrachtet wird.

Es handelt sich um eine Beschreibung des Datums, das zum Geburtstag verwendet wird.

JSON-Format: Zeichenfolge.

Format: JJJJ-MM-TT (ISO-8601), z. B.: &quot;2021-03-11&quot;.

Sie kann in einer toDateOnly -Funktion gekapselt werden.

Es verwendet DateTimeFormatter ISO_LOCAL_DATE_TIME , um den Wert zu deserialisieren und zu serialisieren. [Weitere Infos](https://datatracker.ietf.org/doc/html/rfc3339#section-5.6)

**Wörtliche Darstellung**

```json
date("<dateOnly in ISO-8601 format>")  
```

**Beispiel**

```json
date("2021-02-19")
```

## dateTimeOnly {#date-time-only}

**Beschreibung**

Stellt eine Datum-/Uhrzeit-Uhrzeit ohne Zeitzone dar, die als Jahr-Monat-Tag-Stunde-Minute-Sekunde-Millisekunde angezeigt wird.

JSON-Format: Zeichenfolge.

Es wird keine Zeitzone gespeichert oder dargestellt. Stattdessen handelt es sich um eine Beschreibung des Datums, das zum Geburtstag verwendet wird, kombiniert mit der Ortszeit, wie sie auf einer Wanduhr angezeigt wird.

Ohne zusätzliche Informationen wie Versatz oder Zeitzone kann kein Zeitpunkt auf der Zeitachse dargestellt werden.

Sie kann in einer toDateTimeOnly -Funktion gekapselt werden.

Serialisierungsformat: ISO-8601 erweitertes Versatz-Datum-Uhrzeit-Format.

Es verwendet DateTimeFormatter ISO_LOCAL_DATE_TIME , um den Wert zu deserialisieren und zu serialisieren. [Weitere Infos](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_LOCAL_DATE_TIME&quot;)

**Wörtliche Darstellung**

```json
date("<dateTimeOnly in ISO-8601 format>")  
```

**Beispiele**

```json
date("2021-02-19T00.00.000")
date("2021-02-19T00.00")
```

## dateTime {#date-time}

**Beschreibung**

Datum/Uhrzeit-Konstante, die auch die Zeitzone berücksichtigt. Sie stellt eine Datum/Uhrzeit mit einem Versatz von UTC dar.

Sie kann mit den zusätzlichen Informationen zum Versatz als zeitlicher Zeitpunkt betrachtet werden. Es ist eine Möglichkeit, einen bestimmten &quot;Moment&quot;an einem bestimmten Ort der Welt darzustellen.

JSON-Format: Zeichenfolge.

Sie kann in einer toDateTime -Funktion eingekapselt werden.

Serialisierungsformat: ISO-8601 erweitertes Versatz-Datum-Uhrzeit-Format.

Es verwendet DateTimeFormatter ISO_OFFSET_DATE_TIME , um den Wert zu deserialisieren und zu serialisieren. [Weitere Infos](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_OFFSET_DATE_TIME)

Sie können auch eine Ganzzahl übergeben, die einen Epochenwert übergibt. [Mehr dazu](https://www.epochconverter.com)

Die Zeitzone kann durch einen Versatz oder einen Zeitzonencode angegeben werden (Beispiel: Europa/Paris, Z - bedeutet UTC).

**Wörtliche Darstellung**

```json
toDateTime("<dateTime in ISO-8601 format>")
```

```json
date("<dateTime in ISO-8601 format>")
```

```json
toDateTime(<integer value of an epoch in milliseconds>)
```

**Beispiele**

```json
date("2021-02-19T00.00.000Z")
```

```json
toDateTime("1977-04-22T06:00:00Z")
```

```json
toDateTime("2011-12-03T15:15:30Z")
```

```json
toDateTime("2011-12-03T15:15:30.123Z")
```

```json
toDateTime("2011-12-03T15:15:30.123+02:00")
```

```json
toDateTime("2011-12-03T15:15:30.123-00:20")
```

```json
toDateTime(1560762190189)
```

## duration {#duration}

**Beschreibung**

Es stellt einen zeitbasierten Zeitraum dar, z. B. &quot;34,5 Sekunden&quot;. Modelliert eine Menge oder Zeit in Millisekunden.

Folgende Zeiteinheiten werden unterstützt: Millisekunden, Sekunden, Minuten, Stunden, Tage, bei denen ein Tag 24 Stunden entspricht. Jahre und Monate werden nicht unterstützt, da es sich nicht um einen festen Zeitraum handelt.

JSON-Format: Zeichenfolge.

Sie muss in einer toDuration -Funktion gekapselt sein.

Serialisierungsformat: Zur Deserialisierung einer Zeitzonen-ID wird die Java-Funktion java.time verwendet.

Duration.parse: Die akzeptierten Formate basieren auf dem ISO-8601-Dauerformat PnDTnHnMn.nS, wobei Tage als genau 24 Stunden betrachtet werden. [Weitere Infos](https://docs.oracle.com/javase/8/docs/api/java/time/Duration.html#parse-java.lang.CharSequence-)

**Wörtliche Darstellung**

```json
toDuration("<duration in ISO-8601 format>")
```

```json
toDuration(<duration in milliseconds>)
```

**Beispiel**

```json
toDuration("PT5S") -- parses as 5 seconds
```

```json
toDuration(500) -- parses as 500ms
```

```json
toDuration("PT20.345S") -- parses as "20.345 seconds"
```

```json
toDuration("PT15M") -- parses as "15 minutes" (where a minute is 60 seconds)
```

```json
toDuration("PT10H")  -- parses as "10 hours" (where an hour is 3600 seconds)
```

```json
toDuration("P2D") -- parses as "2 days" (where a day is 24 hours or 86400 seconds)
```

```json
toDuration("P2DT3H4M") -- parses as "2 days, 3 hours and 4 minutes"
```

```json
toDuration("P-6H3M") -- parses as "-6 hours and +3 minutes"
```

```json
toDuration("-P6H3M") -- parses as "-6 hours and -3 minutes"
```

```json
toDuration("-P-6H+3M") -- parses as "+6 hours and -3 minutes"
```

## Liste {#list}

**Beschreibung**

Kommagetrennte Liste von Ausdrücken mit eckigen Klammern als Trennzeichen.

Polymorphismus wird nicht unterstützt. Daher sollten alle in der Liste enthaltenen Ausdrücke denselben Typ aufweisen.

**Wörtliche Darstellung**

```json
[<expression>, <expression>, ... ]
```

**Beispiel**

```json
["value1","value2"]
```

```json
[3,5]
```

```json
[toDuration(500),toDuration(800)]
```
