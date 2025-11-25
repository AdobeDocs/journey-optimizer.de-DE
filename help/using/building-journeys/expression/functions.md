---
solution: Journey Optimizer
product: journey optimizer
title: Funktionen
description: Erfahren Sie mehr über Funktionen in Journey-Ausdrücken
feature: Journeys
role: Developer
level: Experienced
keywords: Funktion, Ausdrücke, Editor, Journey, Daten, Bearbeitung
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 99053c6c1327818645adc4ab9a5d3dd30eb96b87
workflow-type: ht
source-wordcount: '855'
ht-degree: 100%

---

# Funktionen {#functions}

Funktionen sind die Bausteine dynamischer Journey-Ausdrücke in Adobe Journey Optimizer. Sie ermöglichen es Ihnen, Daten in Echtzeit umzuwandeln, zu berechnen, zu validieren und zu bearbeiten, um personalisierte Kundenerlebnisse zu schaffen. Mit über 60 Funktionen, die in intuitive Kategorien unterteilt sind, können Sie anspruchsvolle Bedingungen erstellen, komplexe Berechnungen durchführen und datengestützte Entscheidungen in jedem Schritt der Customer Journey treffen.

## Grundlegendes zu Funktionen

Funktionen in Journey-Ausdrücken folgen einem konsistenten Syntaxmuster:

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, … ,`<expression as param N>`)

**Wichtigste Merkmale:**

* **Mehrere Signaturen**: Eine Funktion kann unterschiedliche Signaturen haben (verschiedene Sätze geordneter Parameter), um verschiedene Anwendungsfälle abzudecken
* **Typspezifische Rückgaben**: Jede Funktion hat einen spezifischen Rückgabetyp (Zeichenfolge, Ganzzahl, boolescher Wert, Datum, Liste usw.)
* **Null- bis N-Parameter**: Funktionen können 0-N-Ausdrücke als geordnete Parameter akzeptieren und bieten dadurch Flexibilität bei ihrer Verwendung

## Gründe für die Verwendung von Funktionen

Funktionen ermöglichen Ihnen Folgendes:

* **Erstellen dynamischer Bedingungen**: Verzweigen Sie Journey-Pfade basierend auf Echtzeit-Datenauswertung
* **Personalisieren im benötigten Umfang**: Passen Sie Inhalte und Erlebnisse mithilfe von Kundendaten und Verhaltenserkenntnissen an
* **Automatisieren von Entscheidungen**: Erstellen sie intelligente Logik ohne manuelles Eingreifen
* **Transformieren von Daten**: Konvertieren, formatieren und bearbeiten Sie Datentypen, um Kompatibilität zu gewährleisten
* **Durchführen von Berechnungen**: Führen Sie mathematische Operationen und statistische Analysen durch
* **Validieren von Eingaben**: Überprüfen Sie die Qualität und Vollständigkeit der Daten, bevor Sie Maßnahmen ergreifen

## Funktionen nach Kategorie

Durchsuchen Sie nach ihrem Hauptzweck organisierte Funktionen, um schnell das richtige Tool für Ihre Bedürfnisse zu finden.

### Adobe Experience Platform {#aep-functions}

**Zielgruppensegmentierung und Targeting**

Werten Sie die Zielgruppenzugehörigkeit aus, um personalisierte Journey-Pfade auf der Grundlage der in Adobe Experience Platform definierten Kundensegmente zu erstellen.

| Funktion | Beschreibung |
|----------|-------------|
| [inAudience](../functions/functioninaudience.md) | Überprüft, ob ein Kontakt zu einer bestimmten Zielgruppe gehört |

[Details zu Adobe Experience Platform-Funktionen anzeigen →](../functions/functioninaudience.md)

### Aggregationsfunktionen {#aggregation-functions}

**Statistische Berechnungen und Datenzusammenfassung**

Führen Sie Berechnungen für Sätze von Werten durch, um Erkenntnisse wie Durchschnittswerte, Anzahlen, Summen und Mindest-/Höchstwerte abzuleiten. Unverzichtbar für datengestützte Entscheidungsfindung.

| Funktion | Beschreibung |
|----------|-------------|
| [avg](../functions/aggregation-functions.md#avg) | Berechnet den durchschnittlichen Wert |
| [count](../functions/aggregation-functions.md#count) | Zählt die Elemente, die nicht null sind |
| [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) | Zählt nur Nullwerte |
| [countWithNull](../functions/aggregation-functions.md#countWithNull) | Zählt alle Elemente einschließlich Nullwerten |
| [distinctCount](../functions/aggregation-functions.md#distinctCount) | Zählt eindeutige Werte, die nicht null sind |
| [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) | Zählt eindeutige Werte einschließlich Nullwerten |
| [max](../functions/aggregation-functions.md#max) | Ermittelt den Höchstwert |
| [min](../functions/aggregation-functions.md#min) | Ermittelt den Mindestwert |
| [sum](../functions/aggregation-functions.md#sum) | Berechnet die Gesamtsumme |

[Alle Aggregationsfunktionen anzeigen →](../functions/aggregation-functions.md)

### Konvertierungsfunktionen {#conversion-functions}

**Datentyptransformation**

Konvertieren Sie Daten zwischen verschiedenen Typen (Zeichenfolge, Ganzzahl, Dezimalzahl, boolescher Wert, Datum, Dauer), um die Kompatibilität über Vorgänge und Datenquellen hinweg sicherzustellen.

| Funktion | Beschreibung |
|----------|-------------|
| [toBool](../functions/conversion-functions.md#toBool) | Konvertiert in booleschen Wert |
| [toDateOnly](../functions/conversion-functions.md#toDateOnly) | Konvertiert nur in Datum (ohne Uhrzeit) |
| [toDateTime](../functions/conversion-functions.md#toDateTime) | Konvertiert in Datum mit Uhrzeit |
| [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) | Konvertiert in Datum und Uhrzeit ohne Zeitzone |
| [toDecimal](../functions/conversion-functions.md#toDecimal) | Konvertiert in Dezimalzahl |
| [toDuration](../functions/conversion-functions.md#toDuration) | Konvertiert in Dauer |
| [toInteger](../functions/conversion-functions.md#toInteger) | Konvertiert in Ganzzahl |
| [toString](../functions/conversion-functions.md#toString) | Konvertiert in Zeichenfolge |

[Alle Konvertierungsfunktionen anzeigen →](../functions/conversion-functions.md)

### Datumsfunktionen {#date-functions}

**Datums- und Uhrzeitbearbeitung**

Arbeiten Sie mit Datumsangaben, Uhrzeiten und Zeitzonen, um zeitbasierte Bedingungen zu erstellen, Aktionen zu planen und zeitbezogene Berechnungen durchzuführen.

| Funktion | Beschreibung |
|----------|-------------|
| [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) | Ruft die aktuelle Zeit in Millisekunden ab |
| [inLastDays](../functions/date-functions.md#inLastDays) | Überprüft, ob das Datum innerhalb der letzten N Tage liegt |
| [inLastHours](../functions/date-functions.md#inLastHours) | Überprüft, ob das Datum innerhalb der letzten N Stunden liegt |
| [inLastMonths](../functions/date-functions.md#inLastMonths) | Überprüft, ob das Datum innerhalb der letzten N Monate liegt |
| [inLastYears](../functions/date-functions.md#inLastYears) | Überprüft, ob das Datum innerhalb der letzten N Jahre liegt |
| [inNextDays](../functions/date-functions.md#inNextDays) | Überprüft, ob das Datum innerhalb der nächsten N Tage liegt |
| [inNextHours](../functions/date-functions.md#inNextHours) | Überprüft, ob das Datum innerhalb der nächsten N Stunden liegt |
| [inNextMonths](../functions/date-functions.md#inNextMonths) | Überprüft, ob das Datum innerhalb der nächsten N Monate liegt |
| [inNextYears](../functions/date-functions.md#inNextYears) | Überprüft, ob das Datum innerhalb der nächsten N Jahre liegt |
| [now](../functions/date-functions.md#now) | Ruft die aktuelle Datums-/Uhrzeitangabe ab |
| [nowWithDelta](../functions/date-functions.md#nowWithDelta) | Ruft die aktuelle Zeit mit Verschiebung ab |
| [setHours](../functions/date-functions.md#setHours) | Legt bestimmte Stunden in der Datums-/Uhrzeitangabe fest |
| [setDays](../functions/date-functions.md#setDays) | Legt bestimmte Tage in der Datums-/Uhrzeitangabe fest |
| [updateTimeZone](../functions/date-functions.md#updateTimeZone) | Aktualisiert die Zeitzone der Datums-/Uhrzeitangabe |

[Alle Datumsfunktionen anzeigen →](../functions/date-functions.md)

### Listenfunktionen {#list-functions}

**Sammlungsbearbeitung und -analyse**

Filtern, sortieren, transformieren und analysieren Sie Arrays und Listen, um mit komplexen Datenstrukturen zu arbeiten und festgelegte Vorgänge durchzuführen.

| Funktion | Beschreibung |
|----------|-------------|
| [distinct](../functions/list-functions.md#distinct) | Ruft eindeutige Werte ab (ohne Nullwerte) |
| [distinctWithNull](../functions/list-functions.md#distinctWithNull) | Ruft eindeutige Werte ab (einschließlich Nullwerten) |
| [filter](../functions/list-functions.md#filter) | Filtert Liste nach Kriterien |
| [getListItem](../functions/list-functions.md#getListItem) | Ruft Element an bestimmtem Index ab |
| [in](../functions/list-functions.md#in) | Überprüft, ob der Wert in der Liste vorhanden ist |
| [intersect](../functions/list-functions.md#intersect) | Sucht nach gemeinsamen Elementen in verschiedenen Listen |
| [limit](../functions/list-functions.md#limit) | Beschränkt die Anzahl der zurückgegebenen Elemente |
| [listSize](../functions/list-functions.md#listSize) | Ruft die Größe der Liste ab |
| [serializeList](../functions/list-functions.md#serializeList) | Konvertiert die Liste in eine Zeichenfolge |
| [sort](../functions/list-functions.md#sort) | Sortiert die Listenelemente |

[Alle Listenfunktionen anzeigen →](../functions/list-functions.md)

### Mathematische Funktionen {#math-functions}

**Mathematische Operationen**

Führen Sie numerische Berechnungen und Umwandlungen für die Datenverarbeitung und Geschäftslogik durch.

| Funktion | Beschreibung |
|----------|-------------|
| [random](../functions/math-functions.md#random) | Generiert eine Zufallszahl (0–1) |
| [round](../functions/math-functions.md#round) | Rundet bis zur nächsten Ganzzahl auf |

[Alle mathematischen Funktionen anzeigen →](../functions/math-functions.md)

### Zeichenfolgenfunktionen {#string-functions}

**Textbearbeitung und -validierung**

Verarbeiten, transformieren, durchsuchen und validieren Sie Textdaten, um dynamische Inhalte zu erstellen und bedingte Logik anzuwenden.

| Funktion | Beschreibung |
|----------|-------------|
| [concat](../functions/string-functions.md#concat) | Verkettet Zeichenfolgen |
| [contain](../functions/string-functions.md#contain) | Überprüft, ob eine Zeichenfolge eine Unterzeichenfolge enthält |
| [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) | Überprüft, ob enthalten (Groß-/Kleinschreibung wird nicht berücksichtigt) |
| [endWith](../functions/string-functions.md#endWith) | Überprüft, ob eine Zeichenfolge mit einem Suffix endet |
| [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) | Überprüft, ob mit endet (Groß-/Kleinschreibung wird nicht berücksichtigt) |
| [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) | Vergleicht Zeichenfolgen (Groß-/Kleinschreibung wird nicht berücksichtigt) |
| [indexOf](../functions/string-functions.md#indexOf) | Sucht die Position des ersten Vorkommens |
| [isEmpty](../functions/string-functions.md#isEmpty) | Überprüft, ob eine Zeichenfolge leer ist |
| [isNotEmpty](../functions/string-functions.md#isNotEmpty) | Überprüft, ob eine Zeichenfolge nicht leer ist |
| [lastIndexOf](../functions/string-functions.md#lastIndexOf) | Sucht die Position des letzten Vorkommens |
| [length](../functions/string-functions.md#length) | Ruft die Länge der Zeichenfolge ab |
| [lower](../functions/string-functions.md#lower) | Konvertiert in Kleinbuchstaben |
| [matchRegExp](../functions/string-functions.md#matchRegExp) | Passt regulären Ausdruck an |
| [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) | Überprüft, ob ungleich (Groß-/Kleinschreibung wird nicht berücksichtigt) |
| [replace](../functions/string-functions.md#replace) | Ersetzt das erste Vorkommen |
| [replaceAll](../functions/string-functions.md#replaceAll) | Ersetzt alle Vorkommen |
| [split](../functions/string-functions.md#split) | Spaltet eine Zeichenfolge in Array auf |
| [startWith](../functions/string-functions.md#startWith) | Überprüft, ob eine Zeichenfolge mit einem Präfix beginnt |
| [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) | Überprüft, ob mit beginnt (Groß-/Kleinschreibung wird nicht berücksichtigt) |
| [substr](../functions/string-functions.md#substr) | Extrahiert eine Unterzeichenfolge |
| [trim](../functions/string-functions.md#trim) | Entfernt führende und nachfolgende Leerzeichen |
| [upper](../functions/string-functions.md#upper) | Konvertiert in Großbuchstaben |
| [uuid](../functions/string-functions.md#uuid) | Generiert UUID |

[Alle Zeichenfolgefunktionen anzeigen →](../functions/string-functions.md)

## Nächste Schritte

Nachdem Sie nun die verfügbaren Funktionen kennen, erkunden Sie Folgendes:

* **[Erweiterter Ausdruckseditor](expressionadvanced.md)**: Erfahren Sie, wie Sie komplexe Ausdrücke mit dem erweiterten Editor erstellen
* **[Ausdruckssyntax](generalities.md)**: Machen Sie sich mit den Syntaxregeln für das Schreiben von Journey-Ausdrücken vertraut
* **[Operatoren](operators.md)**: Erkunden Sie Operatoren, die Sie mit Funktionen zum Erstellen von Logiken verwenden können.
* **[Feldverweise](field-references.md)**: Finden Sie heraus, wie Sie in Ihren Ausdrücken auf Datenfelder verweisen
