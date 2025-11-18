---
solution: Journey Optimizer
product: journey optimizer
title: Funktionen
description: Erfahren Sie mehr über Funktionen beim Journey von Ausdrücken
feature: Journeys
role: Developer
level: Experienced
keywords: Funktion, Ausdrücke, Editor, Journey, Daten, Bearbeitung
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 99053c6c1327818645adc4ab9a5d3dd30eb96b87
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 11%

---

# Funktionen {#functions}

Funktionen sind die Bausteine von Dynamic Journey-Ausdrücken in Adobe Journey Optimizer. Sie ermöglichen es Ihnen, Daten in Echtzeit umzuwandeln, zu berechnen, zu validieren und zu bearbeiten, um personalisierte Kundenerlebnisse zu schaffen. Mit über 60 Funktionen, die in intuitive Kategorien unterteilt sind, können Sie anspruchsvolle Bedingungen erstellen, komplexe Berechnungen durchführen und datengesteuerte Entscheidungen auf jedem Schritt des Kunden-Journey treffen.

## Grundlegendes zu Funktionen

Funktionen in Journey-Ausdrücken folgen einem konsistenten Syntaxmuster:

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, … ,`<expression as param N>`)

**Hauptmerkmale:**

* **Mehrere Signaturen**: Eine Funktion kann verschiedene Signaturen (verschiedene Sätze geordneter Parameter) haben, um verschiedene Anwendungsfälle zu berücksichtigen
* **Typspezifische Rückgaben**: Jede Funktion weist einen bestimmten zurückgegebenen Typ auf (Zeichenfolge, Ganzzahl, boolescher Wert, Datum, Liste usw.)
* **Null- bis N-Parameter**: Funktionen können 0-N-Ausdrücke als geordnete Parameter akzeptieren, was eine flexible Verwendung ermöglicht

## Warum Funktionen verwenden?

Funktionen ermöglichen Ihnen Folgendes:

* **Erstellen dynamischer Bedingungen** - Verzweigen von Journey-Pfaden, die auf der Echtzeitdatenauswertung basieren
* **Personalisieren in großem Maßstab** - Passen Sie Inhalte und Erlebnisse mithilfe von Kundendaten und Verhaltenserkenntnissen an
* **Entscheidungen automatisieren** - Intelligente Logik ohne manuelles Eingreifen erstellen
* **Daten transformieren** - Konvertieren, Formatieren und Bearbeiten von Datentypen, um Kompatibilität zu gewährleisten
* **Berechnungen durchführen** - Mathematische Operationen und statistische Analysen durchführen
* **Eingaben validieren** - Qualität und Vollständigkeit der Daten überprüfen, bevor Maßnahmen ergriffen werden

## Funktionen nach Kategorie

Durchsuchen Sie Funktionen, die nach ihrem Hauptzweck geordnet sind, um schnell das richtige Tool für Ihre Bedürfnisse zu finden.

### Adobe Experience Platform {#aep-functions}

**Zielgruppensegmentierung und Zielgruppenbestimmung**

Bewerten Sie die Zielgruppenzugehörigkeit, um personalisierte Journey-Pfade auf der Grundlage der in Adobe Experience Platform definierten Kundensegmente zu erstellen.

| Funktion | Beschreibung |
|----------|-------------|
| [inAudience](../functions/functioninaudience.md) | Überprüfen, ob ein Kontakt zu einer bestimmten Zielgruppe gehört |

[Anzeigen von Adobe Experience Platform-Funktionsdetails →](../functions/functioninaudience.md)

### Aggregationsfunktionen {#aggregation-functions}

**Statistische Berechnungen und Datenzusammenfassung**

Führen Sie Berechnungen für Wertesätze durch, um Insights wie Durchschnittswerte, Zahlen, Summen und Min-/Max-Werte abzuleiten. Wesentlich für datengestützte Entscheidungsfindung.

| Funktion | Beschreibung |
|----------|-------------|
| [avg](../functions/aggregation-functions.md#avg) | Durchschnittlicher Wert berechnen |
| [count](../functions/aggregation-functions.md#count) | Anzahl der Elemente ungleich null |
| [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) | Nur Nullwerte zählen |
| [countWithNull](../functions/aggregation-functions.md#countWithNull) | Alle Elemente einschließlich NULL zählen |
| [distinctCount](../functions/aggregation-functions.md#distinctCount) | Anzahl eindeutiger Werte ungleich null |
| [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) | Eindeutige Werte einschließlich NULL zählen |
| [max](../functions/aggregation-functions.md#max) | Höchstwert suchen |
| [min](../functions/aggregation-functions.md#min) | Mindestwert suchen |
| [sum](../functions/aggregation-functions.md#sum) | Gesamtsumme berechnen |

[Alle Aggregationsfunktionen anzeigen →](../functions/aggregation-functions.md)

### Konversionsfunktionen {#conversion-functions}

**Datentypumwandlung**

Konvertieren Sie Daten zwischen verschiedenen Typen (Zeichenfolge, Ganzzahl, Dezimalzahl, Boolesch, Datum, Dauer), um die Kompatibilität zwischen Vorgängen und Datenquellen sicherzustellen.

| Funktion | Beschreibung |
|----------|-------------|
| [toBool](../functions/conversion-functions.md#toBool) | In Boolesch konvertieren |
| [toDateOnly](../functions/conversion-functions.md#toDateOnly) | Nur in Datum konvertieren (keine Zeit) |
| [toDateTime](../functions/conversion-functions.md#toDateTime) | In Datum mit Uhrzeit konvertieren |
| [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) | In Datum/Uhrzeit ohne Zeitzone konvertieren |
| [toDecimal](../functions/conversion-functions.md#toDecimal) | In Dezimalzahl konvertieren |
| [toDuration](../functions/conversion-functions.md#toDuration) | In Dauer konvertieren |
| [toInteger](../functions/conversion-functions.md#toInteger) | In Ganzzahl konvertieren |
| [toString](../functions/conversion-functions.md#toString) | In Zeichenfolge konvertieren |

[Alle Konvertierungsfunktionen → anzeigen](../functions/conversion-functions.md)

### Datumsfunktionen {#date-functions}

**Manipulation von Datum und Uhrzeit**

Arbeiten Sie mit Datumsangaben, Uhrzeiten und Zeitzonen, um zeitbasierte Bedingungen zu erstellen, Aktionen zu planen und zeitliche Berechnungen durchzuführen.

| Funktion | Beschreibung |
|----------|-------------|
| [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) | Aktuelle Zeit in Millisekunden abrufen |
| [inLastDays](../functions/date-functions.md#inLastDays) | Überprüfen, ob das Datum innerhalb der letzten N Tage liegt |
| [inLastHours](../functions/date-functions.md#inLastHours) | Überprüfen, ob das Datum innerhalb der letzten N Stunden liegt |
| [inLastMonths](../functions/date-functions.md#inLastMonths) | Überprüfen, ob das Datum innerhalb der letzten N Monate liegt |
| [inLastYears](../functions/date-functions.md#inLastYears) | Überprüfen, ob das Datum innerhalb der letzten N Jahre liegt |
| [inNextDays](../functions/date-functions.md#inNextDays) | Überprüfen, ob das Datum innerhalb der nächsten N Tage liegt |
| [inNextHours](../functions/date-functions.md#inNextHours) | Überprüfen, ob das Datum innerhalb der nächsten N Stunden liegt |
| [inNextMonths](../functions/date-functions.md#inNextMonths) | Überprüfen, ob das Datum innerhalb der nächsten N Monate liegt |
| [inNextYears](../functions/date-functions.md#inNextYears) | Überprüfen, ob das Datum innerhalb der nächsten N Jahre liegt |
| [now](../functions/date-functions.md#now) | Aktuelle Uhrzeit-/Datumsangabe abrufen |
| [nowWithDelta](../functions/date-functions.md#nowWithDelta) | Aktuelle Zeit mit Versatz abrufen |
| [setHours](../functions/date-functions.md#setHours) | Festlegen bestimmter Stunden in „Datum-Uhrzeit“ |
| [setDays](../functions/date-functions.md#setDays) | Festlegen bestimmter Tage im Datum-Uhrzeit-Format |
| [updateTimeZone](../functions/date-functions.md#updateTimeZone) | Zeitzone des Datums/der Uhrzeit aktualisieren |

[Alle Datumsfunktionen anzeigen →](../functions/date-functions.md)

### Auflistungsfunktionen {#list-functions}

**Sammlungsbearbeitung und -analyse**

Filtern, Sortieren, Transformieren und Analysieren von Arrays und Listen für die Arbeit mit komplexen Datenstrukturen und für die Durchführung von Set-Vorgängen.

| Funktion | Beschreibung |
|----------|-------------|
| [distinct](../functions/list-functions.md#distinct) | Eindeutige Werte abrufen (NULL ausschließen) |
| [distinctWithNull](../functions/list-functions.md#distinctWithNull) | Eindeutige Werte abrufen (einschließlich NULL) |
| [filter](../functions/list-functions.md#filter) | Liste nach Kriterien filtern |
| [getListItem](../functions/list-functions.md#getListItem) | Element mit bestimmtem Index abrufen |
| [in](../functions/list-functions.md#in) | Überprüfen, ob Wert in der Liste vorhanden ist |
| [intersect](../functions/list-functions.md#intersect) | Suchen nach gemeinsamen Elementen zwischen Listen |
| [limit](../functions/list-functions.md#limit) | Anzahl der zurückgegebenen Elemente begrenzen |
| [listSize](../functions/list-functions.md#listSize) | Größe der Liste abrufen |
| [serializeList](../functions/list-functions.md#serializeList) | Liste in Zeichenfolge konvertieren |
| [sort](../functions/list-functions.md#sort) | Sortieren von Listenelementen |

[Alle Listenfunktionen anzeigen →](../functions/list-functions.md)

### Mathematische Funktionen {#math-functions}

**Mathematische Operationen**

Durchführen numerischer Berechnungen und Umwandlungen für die Datenverarbeitung und Geschäftslogik.

| Funktion | Beschreibung |
|----------|-------------|
| [random](../functions/math-functions.md#random) | Zufallszahl generieren (0-1) |
| [round](../functions/math-functions.md#round) | Auf nächste Ganzzahl runden |

[Alle mathematischen Funktionen anzeigen →](../functions/math-functions.md)

### Zeichenfolgenfunktionen {#string-functions}

**Textbearbeitung und -validierung**

Verarbeiten, transformieren, suchen und validieren Sie Textdaten für die Erstellung dynamischer Inhalte und bedingte Logik.

| Funktion | Beschreibung |
|----------|-------------|
| [concat](../functions/string-functions.md#concat) | Strings verketten |
| [contain](../functions/string-functions.md#contain) | Prüft, ob die Zeichenfolge Teilzeichenfolge enthält |
| [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) | Überprüfung enthält (ignoriert Groß- und Kleinschreibung) |
| [endWith](../functions/string-functions.md#endWith) | Prüft, ob die Zeichenfolge mit einem Suffix endet |
| [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) | Endet mit (ignoriert Groß- und Kleinschreibung) |
| [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) | Zeichenfolgen vergleichen (ignoriert Groß- und Kleinschreibung) |
| [indexOf](../functions/string-functions.md#indexOf) | Position des ersten Vorkommens suchen |
| [isEmpty](../functions/string-functions.md#isEmpty) | Prüft, ob die Zeichenfolge leer ist |
| [isNotEmpty](../functions/string-functions.md#isNotEmpty) | Überprüfen, ob die Zeichenfolge nicht leer ist |
| [lastIndexOf](../functions/string-functions.md#lastIndexOf) | Position des letzten Vorkommens suchen |
| [length](../functions/string-functions.md#length) | Länge der Zeichenfolge abrufen |
| [lower](../functions/string-functions.md#lower) | In Kleinbuchstaben umwandeln |
| [matchRegExp](../functions/string-functions.md#matchRegExp) | Regulärer Ausdruck für Übereinstimmung |
| [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) | Ungleich markieren (ignoriert Groß- und Kleinschreibung) |
| [replace](../functions/string-functions.md#replace) | Erstes Auftreten ersetzen |
| [replaceAll](../functions/string-functions.md#replaceAll) | Alle Vorkommen ersetzen |
| [split](../functions/string-functions.md#split) | Zeichenfolge in Array teilen |
| [startWith](../functions/string-functions.md#startWith) | Überprüfen, ob die Zeichenfolge mit dem Präfix beginnt |
| [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) | Prüfung beginnt mit (ignoriert Groß- und Kleinschreibung) |
| [substr](../functions/string-functions.md#substr) | Teilzeichenfolge extrahieren |
| [trim](../functions/string-functions.md#trim) | Leerzeichen am Anfang/Ende entfernen |
| [upper](../functions/string-functions.md#upper) | In Großbuchstaben umwandeln |
| [uuid](../functions/string-functions.md#uuid) | UUID generieren |

[Alle Zeichenfolgen-Funktionen anzeigen →](../functions/string-functions.md)

## Nächste Schritte

Nachdem Sie nun die verfügbaren Funktionen kennen, erkunden Sie:

* **[Erweiterter Ausdruckseditor](expressionadvanced.md)** - Erfahren Sie, wie Sie komplexe Ausdrücke mit dem erweiterten Editor erstellen
* **[Ausdruckssyntax](generalities.md)** - Übernimmt die Syntaxregeln für das Schreiben von Journey-Ausdrücken
* **[Operatoren](operators.md)** - Ermitteln Sie Operatoren, die Sie mit Funktionen zum Erstellen von Logiken verwenden können.
* **[Feldverweise](field-references.md)** - Verstehen, wie Datenfelder in Ihren Ausdrücken referenziert werden
