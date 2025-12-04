---
product: journey optimizer
title: Konvertierungsfunktionen
description: Erfahren Sie mehr über Konvertierungsfunktionen
feature: Journeys
role: Developer
level: Experienced
keywords: Konvertierung, Funktionen, Ausdruck, Journey, Typ, Umwandlung
version: Journey Orchestration
source-git-commit: 451a9e1e5d5e6e1408849e8d1c5c9644a95359da
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 89%

---

# Konvertierungsfunktionen {#conversion-functions}

Mit Konvertierungsfunktionen können Sie Daten in Ihren Journey-Ausdrücken von einem Typ in einen anderen umwandeln. Diese Funktionen sind für die Gewährleistung der Datenkompatibilität und der ordnungsgemäßen Typverarbeitung bei der Arbeit mit verschiedenen Datenquellen und Vorgängen von entscheidender Bedeutung.

Verwenden Sie Konvertierungsfunktionen für Folgendes:

* Konvertieren von Zeichenfolgewerten in numerische oder boolesche Typen oder Datentypen ([toInteger](#toInteger), [toDecimal](#toDecimal), [toBool](#toBool))
* Umwandeln von Datums- und Zeitangaben zwischen verschiedenen Formaten und Darstellungsweisen ([toDateTime](#toDateTime), [toDateTimeOnly](#toDateTimeOnly), [toDateOnly](#toDateOnly))
* Umrechnen von Zahlenwerten zwischen Ganzzahl und Dezimalzahl ([toInteger](#toInteger), [toDecimal](#toDecimal))
* Konvertieren von Werten in Zeichenfolgenformat ([toString](#toString)) oder Dauer ([toDuration](#toDuration))
* Gewährleisten von Typenkompatibilität bei Vergleichen und Vorgängen
* Verarbeiten von Daten aus externen Quellen, die unterschiedliche Typformate aufweisen können

Jede Konvertierungsfunktion verarbeitet typspezifische Regeln und Randfälle automatisch, wodurch die Datenumwandlung in Ihren Journey-Ausdrücken zuverlässiger und vorhersehbarer wird.

## toBool {#toBool}

Konvertiert einen Argumentwert je nach Typ in einen booleschen Wert.

* Von Zeichenfolge: Versucht, den Zeichenfolgenwert in einen booleschen Wert zu konvertieren, von „true“, wenn der Zeichenfolgenwert „true“ ist, andernfalls „false“
* Von numerisch: „true“, wenn der numerische Wert ungleich 0 ist, andernfalls „false“

+++Syntax

`toBool(<parameter>)`

+++

+++Parameter

* decimal
* boolean
* string
* integer

+++

+++Signaturen und zurückgegebene Typen

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Geben einen booleschen Wert zurück.

+++

+++Beispiele

`toBool("true")`

`toBool(1)`

Gibt „true“ zurück.

`toBool("this is not a boolean")`

Gibt „false“ zurück.

+++

## toDateOnly {#toDateOnly}

Konvertiert ein Argument in einen Wert vom Typ dateOnly. Weitere Informationen zu Datentypen finden Sie in diesem [Abschnitt](../expression/data-types.md).

+++Syntax

`toDateOnly(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| Zeichenfolgendarstellung eines Datums als „JJJJ-MM-TT“ (XDM-Format). Unterstützt auch das ISO-8601-Format: nur der Teil mit dem **vollständigen Datum** wird berücksichtigt (siehe [RFC 3339, Abschnitt 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | Zeichenfolge |
| Datum/Uhrzeit | dateTime |
| Datum/Uhrzeit ohne Zeitzone | dateTimeOnly |
| ganzzahliger Wert einer Epoche in Millisekunden | integer |

+++

+++Signaturen und zurückgegebene Typen

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

Gibt einen Wert vom Typ dateOnly zurück.

+++

+++Beispiele

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

alle geben ein dateOnly-Objekt zurück, das den 18.08.2023 darstellt.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Gibt ein dateOnly zurück.

+++

## toDateTime {#toDateTime}

Konvertiert Parameter je nach Typ in einen Datum-/Uhrzeit-Wert.

+++Syntax

`toDateTime(<parameters>)`

+++

+++Parameter

| Parameter | Beschreibung |
|--- |--- |
| string | Datum/Uhrzeit im ISO-8601-Format. Eine Zeichenfolgendarstellung eines Datums-/Uhrzeitwerts mit Zeitzoneninformationen |
| Zeichenfolge | Zeitzonen-ID. Eine Zeitzonenkennung (z. B. „UTC“, „Europe/Paris„) |
| dateOnly | Stellt ein Datum ohne Zeitzone dar, das als Jahr-Monat-Tag angezeigt wird |
| dateTimeOnly | Stellt einen Datum/Uhrzeit-Wert ohne Zeitzone dar, der als Jahr-Monat-Tag-Stunde-Minute-Sekunde-Millisekunde angezeigt wird |
| integer | ganzzahliger Wert einer Epoche in Millisekunden |

+++

+++Signaturen und zurückgegebene Typen

`toDateTime(<string>)`

`toDateTime(<string>, <dateOnly>)`

`toDateTime(<string>, <dateTimeOnly>)`

`toDateTime(<integer>)`

Gibt einen **Datum/Uhrzeit-Wert** zurück.

+++

+++Beispiele

`toDateTime("2023-08-18T23:17:59.123Z")`

Gibt 2023-08-18T23:17:59.123Z zurück.

Die ISO-8601-Zeichenfolge enthält bereits Zeitzoneninformationen.

`toDateTime("Europe/Paris", toDateOnly("2023-08-18"))`

Gibt 2023-08-18T00:00:00.000+02 :00

Dadurch wird eine dateTime erstellt, indem eine Zeitzone mit einem reinen Datumswert kombiniert wird. Die Uhrzeit wird in der angegebenen Zeitzone auf Mitternacht :00:00:00) festgelegt.

`toDateTime("UTC", toDateTimeOnly("2023-08-18T23:17:59.123"))`

Gibt 2023-08-18T23:17:59.123Z zurück.

Dadurch wird eine dateTime erstellt, indem eine Zeitzone auf einen dateTimeOnly-Wert angewendet wird (der keine Zeitzoneninformationen enthält).

`toDateTime(1560762190189)`

Gibt 2019-06-17T09:03:10.189Z zurück

Konvertiert einen Unix-Zeitstempel in Millisekunden in einen dateTime-Wert.

+++

>[!NOTE]
>
>Die Zeitzonen-ID muss eine Zeichenfolgenkonstante sein. Sie darf weder ein Feldverweis noch ein Ausdruck sein. Weitere Informationen zu Datentypen finden Sie auf [dieser Seite](../expression/data-types.md).

## toDateTimeOnly {#toDateTimeOnly}

Konvertiert einen Argumentwert in einen reinen Datum-/Uhrzeit-Wert.

+++Syntax

`toDateTimeOnly(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit im ISO-8601-Format oder im XDM-Datumsformat &quot;JJJJ-MM-TT&quot; | Zeichenfolge |
| Datum/Uhrzeit | dateTime |

+++

+++Signaturen und zurückgegebene Typen

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

+++

+++Beispiele

`toDateTimeOnly ("2023-08-18")`

Gibt einen Datum/Uhrzeit-Wert zurück, der 2023-08-18T00:00:00.000 entspricht.

`toDateTimeOnly(now())`

+++

## toDecimal {#toDecimal}

Konvertiert einen Argumentwert je nach Typ in einen Dezimalwert.

+++Syntax

`toDecimal(<parameter>)`

+++

+++Parameter

| Parameter | Beschreibung |
|--- |--- |
| string | konvertiert den Zeichenfolgenwert in eine Dezimalzahl |
| dateTime | konvertiert das Datum in die Zahl der Millisekunden (Millisekunden der Epoche) |
| boolean | wandelt den booleschen Wert in 1 um, wenn „true“, und in 0, wenn „false“ |
| integer | konvertiert in eine Dezimalzahl (Beispiel: 1 wird zu 1.0) |

+++

+++Signaturen und zurückgegebene Typen

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Gibt eine Dezimalzahl zurück.

+++

+++Beispiele

`toDecimal("4.0")`

Gibt 4.0 zurück.

+++

## toDuration {#toDuration}

Konvertiert einen Argumentwert in eine Dauer. Weitere Informationen zu Datentypen finden Sie auf [dieser Seite](../expression/data-types.md).

+++Syntax

`toDuration(<parameter>)`

+++

+++Parameter

| Parameter | Beschreibung |
|--- |--- |
| string | Formate, die auf dem ISO 8601-Dauerformat PnDTnHnMn.nS basieren, wobei Tage als genau 24 Stunden betrachtet werden. |
| integer | Zahl der Millisekunden |

Wenn Zeichenfolgenausdruck: Akzeptierte Formate basieren auf dem ISO 8601-Dauerformat PnDTnHnMn.nS, wobei Tage als genau 24 Stunden betrachtet werden.

Die Zeichenfolge beginnt mit einem optionalen Zeichen, markiert durch das negative oder positive ASCII-Symbol. Bei negativen Werten wird der gesamte Zeitraum negiert. Der ASCII-Buchstabe „P“ folgt in Groß- oder Kleinschreibung. Dann gibt es vier Bereiche, die jeweils aus einer Zahl und einem Suffix bestehen. Die Bereiche weisen die ASCII-Suffixe von „D“, „H“, „M“ und „S“ für Tage, Stunden, Minuten und Sekunden auf, akzeptiert in Groß- oder Kleinschreibung. Die Suffixe müssen in richtiger Reihenfolge erscheinen. Der ASCII-Buchstabe „T“ muss vor dem ersten Auftreten, so vorhanden, einer Stunde, einer Minute oder eines zweiten Bereichs stehen. Es muss mindestens einer der vier Bereiche vorhanden sein und wenn „T“ vorhanden ist, muss mindestens ein Bereich auf das „T“ folgen. Der Zahlenteil der einzelnen Bereiche muss aus einer oder mehreren ASCII-Ziffern bestehen. Der Zahl kann das negative oder positive ASCII-Symbol vorangestellt werden. Die Zahl der Tage, Stunden und Minuten muss zu einem „long“ ausgewertet werden. Die Zahl der Sekunden muss zu einem „long“ mit optionalem Bruch ausgewertet werden. Das Dezimalzeichen kann ein Punkt oder ein Komma sein. Der Bruchteil kann zwischen null und neun Stellen aufweisen.

+++

+++Signaturen und zurückgegebener Typ

`toDuration(<string>)`

`toDuration(<integer>)`

Gibt eine Dauer zurück.

+++

+++Beispiele

`toDuration("PT10H")`

Gibt eine Dauer von 10 Stunden zurück.

`toDuration("PT4S")`

Gibt eine Dauer von 4 Sekunden zurück.

`toDuration(4000)`

Gibt eine Dauer von 4 Sekunden zurück.

+++

## toInteger {#toInteger}

Konvertiert einen Argumentwert in eine Ganzzahl.

+++Syntax

`toInteger(<parameter>)`

+++

+++Parameter

| Parameter | Beschreibung |
|--- |--- |
| Zeichenfolge | konvertiert den Zeichenfolgenwert in eine Ganzzahl |
| dateTime | konvertiert das Datum in die Zahl der Millisekunden (Millisekunden der Epoche) |
| decimal | konvertiert in eine Ganzzahl, indem der Dezimalteil entfernt wird (Beispiel: 1.5 wird zu 1) |
| boolean | wandelt den booleschen Wert in 1 um, wenn „true“, und in 0, wenn „false“ |

+++

+++Signaturen und zurückgegebener Typ

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

Gibt eine Ganzzahl zurück.

+++

+++Beispiele

`toInteger("4")`

Gibt 4 zurück.

+++

## toString {#toString}

Konvertiert einen Argumentwert je nach Typ in einen Zeichenfolgenwert. Weitere Informationen zu Datentypen finden Sie auf [dieser Seite](../expression/data-types.md).

+++Syntax

`toString(<parameter>)`

+++

+++Parameter

| Parameter | Beschreibung |
|--- |--- |
| dateTime | konvertiert das Datum in das UTC-Datumsformat |
| dateTimeOnly | konvertiert das Datum in das UTC-Datumsformat |
| duration | konvertiert in die entsprechende Anzahl von Millisekunden als Zeichenfolge |
| integer | konvertiert den Wert in eine Zeichenfolgendarstellung (1 wird zu „1“) |
| decimal | konvertiert den Wert in eine Zeichenfolgendarstellung (1,5 wird zu „1,5“) |
| Boolescher Wert | konvertiert den booleschen Wert in &#39;true&#39;, wenn „true“, in &#39;false&#39;, wenn „false“ |

+++

+++Signaturen und zurückgegebener Typ

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Gibt eine Zeichenfolge zurück.

+++

+++Beispiele

`toString(4)`

Gibt „4“ zurück.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Gibt die Zeichenfolgendarstellung des angegebenen dateOnly-Feldes (XDM-Datumsfeld) zurück, beispielsweise „18.08.2023“.

`toString(toDuration(1520))`

Gibt „PT1.52S“ zurück.

+++

