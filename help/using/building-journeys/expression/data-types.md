---
solution: Journey Optimizer
product: journey optimizer
title: Datentypen
description: Erfahren Sie mehr über die Datentypen in erweiterten Ausdrücken
feature: Journeys
role: Developer
level: Experienced
keywords: Ausdruck, Daten, Datentyp, Journey
exl-id: fdfc3287-d733-45fb-ad11-b4238398820a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/0UKY3G4hyMnSkzh8wlMx-yQ1yymKjs6FuIBdGo1SJqc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1124
ht-degree: 59%

---

# Datentypen {#data-types}

Technisch gesehen enthält eine Konstante immer einen Datentyp. Wörtlich genommen geben wir nur den Wert an. Der Datentyp kann aus dem Wert abgeleitet werden (z. B. Zeichenfolge, Ganzzahl, Dezimalzahl usw.). Für bestimmte Fälle wie Datum und Uhrzeit verwenden wir spezielle Funktionen für die Darstellung.

In den folgenden Abschnitten finden Sie Informationen zu den verschiedenen Ausdrücken von Datentypen und wie sie dargestellt werden.

## Zeichenfolge {#string}

**Beschreibung**

Allgemeine Zeichenfolge. Er hat keine bestimmte Größe außer der impliziten Größe, die aus der Umgebung stammt, z. B. die verfügbare Speicherkapazität.

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

Dezimalzahl. Stellt einen Gleitkommawert dar:

* größter positiver endlicher Wert des Typs „double“, (2-2^-52)x2^1023
* kleinster positiver Normalwert des Typs „double“, 2-1022
* kleinster positiver Wert ungleich null vom Typ „double“, 2 p-1074

JSON-Format: Zahl

Serialisierungsformat: mit „.“ als Dezimaltrennzeichen.

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

Boolescher Wert in Kleinbuchstaben: true (wahr) oder false (falsch)

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

## dateOnly {#date-only}

**Beschreibung**

Stellt ein reines Datum ohne Zeitzone dar, das als Jahr-Monat-Tag angezeigt wird.

Es ist eine Beschreibung des Datums, wie es beispielsweise für den Geburtstag verwendet wird.

JSON-Format: Zeichenfolge.

Format ist: JJJJ-MM-TT (ISO-8601), z. B.: „2021-03-11“.

Kann ausschließlich in einer toDateOnly -Funktion gekapselt sein.

Es wird das DateTimeFormatter ISO_LOCAL_DATE_TIME zur Deserialisierung und Serialisierung des Wertes verwendet. [Weitere Informationen](https://datatracker.ietf.org/doc/html/rfc3339#section-5.6)

**Wörtliche Darstellung**

```json
date("<dateOnly in ISO-8601 format>")  
```

**Beispiel**

```json
date("2021-02-19")
```

## dateTimeOnly {#date-time-only}

**Beschreibung**

Stellt Datum und Uhrzeit ohne Zeitzone dar, die als Jahr-Monat-Tag-Stunde-Minute-Sekunde-Millisekunde interpretiert wird.

JSON-Format: Zeichenfolge.

Es wird keine Zeitzone gespeichert oder dargestellt. Stattdessen handelt es sich um eine Beschreibung des Datums, wie es für Geburtstage verwendet wird, kombiniert mit der Ortszeit, wie sie auf einer Wanduhr angezeigt wird.

Ohne zusätzliche Informationen wie Versatz oder Zeitzone kann kein Zeitpunkt auf der Zeitachse dargestellt werden.

Kann in einer toDateTimeOnly-Funktion gekapselt sein.

Serialisierungsformat: ISO-8601, erweitertes Versatz-Datums-/Uhrzeitformat.

Es wird das DateTimeFormatter ISO_LOCAL_DATE_TIME zur Deserialisierung und Serialisierung des Wertes verwendet. [Weitere Informationen](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_LOCAL_DATE_TIME"){_blank}.

**Wörtliche Darstellung**

```json
date("<dateTimeOnly in ISO-8601 format>")  
```

**Beispiele**

```json
date("2024-02-19T00.00.000")
date("2024-02-19T00.00")
```

## dateTime {#date-time}

**Beschreibung**

Datums-/Zeitkonstante, die auch die Zeitzone berücksichtigt. Es wird Datum + Uhrzeit mit einem Versatz relativ zur UTC dargestellt.

Mit den zusätzlichen Informationen zum Versatz kann ein bestimmter Zeitpunkt dargestellt werden. Sie bieten die Möglichkeit, einen bestimmten Zeitpunkt an einem bestimmten Ort der Welt darzustellen.

JSON-Format: Zeichenfolge.

Kann in einer toDateTime-Funktion gekapselt sein.

Serialisierungsformat: ISO-8601, erweitertes Versatz-Datums-/Uhrzeitformat.

Verwendet das DateTimeFormatter ISO_OFFSET_DATE_TIME zur Deserialisierung und Serialisierung des Wertes. [Weitere Informationen](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_OFFSET_DATE_TIME){_blank}.

Sie können auch eine Ganzzahl übergeben, die einen Epochenwert übergibt. [Weitere Informationen](https://www.epochconverter.com){_blank}.

Die Zeitzone kann durch einen Versatz oder einen Zeitzonen-Code angegeben werden (Beispiel: Europa/Paris, Z – bedeutet UTC).

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
date("2024-02-19T00.00.000Z")
```

```json
toDateTime("1977-04-22T06:00:00Z")
```

```json
toDateTime("2023-12-03T15:15:30Z")
```

```json
toDateTime("2023-12-03T15:15:30.123Z")
```

```json
toDateTime("2023-12-03T15:15:30.123+02:00")
```

```json
toDateTime("2023-12-03T15:15:30.123-00:20")
```

```json
toDateTime(1560762190189)
```

## duration {#duration}

**Beschreibung**

Stellt eine zeitbasierte Dauer dar, z. B. „34,5 Sekunden“. Modelliert eine Menge oder Dauer in Millisekunden.

Folgende Zeiteinheiten werden unterstützt: Millisekunden, Sekunden, Minuten, Stunden, Tage, wobei ein Tag 24 Stunden entspricht. Jahre und Monate werden nicht unterstützt, da sie keine feste Dauer haben.

JSON-Format: Zeichenfolge.

Muss in einer toDuration-Funktion gekapselt sein.

Serialisierungsformat: Zur Deserialisierung einer Zeitzonen-ID wird die Java-Funktion java.time verwendet.

Duration.parse: Die akzeptierten Formate basieren auf dem ISO-8601-Dauerformat „PnDTnHnMn.nS“, wobei Tage als genau 24 Stunden angesehen werden. [Weitere Informationen](https://docs.oracle.com/javase/8/docs/api/java/time/Duration.html#parse-java.lang.CharSequence-){_blank}.

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

## list {#list}

**Beschreibung**

Kommagetrennte Liste von Ausdrücken mit eckigen Klammern als Trennzeichen.

Polymorphismus wird nicht unterstützt. Daher sollten alle in der Liste enthaltenen Ausdrücke denselben Typ haben.

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

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite werden alle Datentypen beschrieben, die im erweiterten Ausdruckseditor von Journey unterstützt werden - Zeichenfolge, Ganzzahl, Dezimalzahl, Boolescher Wert, dateOnly, dateTimeOnly, dateTime, Dauer und Liste -, einschließlich ihrer JSON-Formate, Serialisierungsregeln und literalen Darstellungssyntax.

**intents:**

* Identifizieren Sie beim Schreiben von Journey-Ausdrücken die richtige Literalsyntax für jeden Datentyp
* Verstehen Sie den Unterschied zwischen `dateOnly`-, `dateTimeOnly`- und `dateTime` und wann jeder Typ verwendet werden sollte
* Stellen Sie mit der `toDuration()`-Funktion einen Dauerwert im ISO-8601-Format oder in Millisekunden dar
* Einen Listenausdruck mit eckiger Klammersyntax für die Verwendung in Sammlungsvorgängen erstellen
* Verwenden Sie Konvertierungsfunktionen (`toDateTime`, `toDateTimeOnly`, `toDuration`, `toDateOnly`) zum Erstellen typisierter Konstanten

**Glossar:**

* **dateOnly**: Ein Datum ohne Zeit oder Zeitzone, formatiert als JJJJ-MM-TT; geeignet für Geburtstage oder Kalenderdaten *(produktspezifisch)*
* **dateTimeOnly**: Ein Datum und eine Uhrzeit ohne Zeitzoneninformationen; kann keinen bestimmten Zeitpunkt ohne Offset-*darstellen (produktspezifisch)*
* **dateTime**: Eine Datums-/Zeitkonstante, die einen UTC-Offset enthält, der einen bestimmten Zeitpunkt darstellt. Kann auch aus einer ganzzahligen Epochenzahl *produktspezifisch) erstellt werden*
* **duration**: Ein zeitbasierter Betrag, der in Millisekunden modelliert wird; verwendet das ISO-8601-`PnDTnHnMn.nS`; Jahre und Monate werden nicht unterstützt *(produktspezifisch)*
* **list**: Eine kommagetrennte Sammlung von Ausdrücken desselben Typs, getrennt durch eckige Klammern *(produktspezifisch)*

**Leitplanken:**

* Dauer unterstützt nur Millisekunden, Sekunden, Minuten, Stunden und Tage - Jahre und Monate werden nicht unterstützt, da sie keine festen Zeiträume sind
* Ein `duration` muss in `toDuration()` eingeschlossen sein - er kann nicht als Literal ausgedrückt werden
* Alle Ausdrücke in einem `list` müssen vom gleichen Typ sein - Polymorphismus wird nicht unterstützt
* `dateTimeOnly` kann keinen Zeitpunkt ohne zusätzlichen Offset oder Zeitzone darstellen

**Terminologie:**

* Kanonischer Name: Datentypen — Akronym: none — Varianten: Ausdrucksdatentypen, Journey-Datentypen
* Synonyme: „dateTime“ = „Datum-Uhrzeit mit Zeitzone“; „dateTimeOnly“ = „local date-time“
* Verwechseln Sie nicht: `dateOnly` (keine Zeit) ≠ `dateTimeOnly` (Datum + Zeit, keine Zeitzone) ≠ `dateTime` (Datum + Zeit + Zeitzone/Versatz)

**FAQ:**

* **F: Was ist der Unterschied zwischen `dateTimeOnly` und `dateTime`?** — `dateTimeOnly` hat keine Zeitzone oder keinen Offset und kann keinen genauen Zeitpunkt darstellen; `dateTime` umfasst einen UTC-Offset und stellt einen bestimmten Zeitpunkt dar.
* **F: Wie drücke ich eine Dauer von 2 Tagen und 3 Stunden aus?** — `toDuration("P2DT3H")` verwenden.
* **F: Kann ich in einem Listenausdruck Ganzzahlen und Zeichenfolgen mischen?** — Nein; alle Ausdrücke in einer Liste müssen vom gleichen Typ sein.
* **F: Wie erstelle ich einen `dateTime` aus einem Epochenzeitstempel in Millisekunden?** — Verwenden Sie `toDateTime(<epoch in milliseconds>)`, z. B. `toDateTime(1560762190189)`.
* **F: Ist `true` oder `True` das richtige boolesche Literal?** — `true` oder `false` in Kleinbuchstaben verwenden. Varianten in Großbuchstaben sind nicht gültig.

+++
