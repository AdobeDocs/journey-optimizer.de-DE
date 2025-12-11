---
title: Erste Schritte mit Helper-Funktionen
description: Bibliothek für Helper-Funktionen in Journey Optimizer
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: cdf9eadc36d7e7b3538690a7a165bc39eccc40b5
workflow-type: tm+mt
source-wordcount: '2458'
ht-degree: 93%

---

# Erste Schritte mit Helper-Funktionen{#functions}

Helper-Funktionen ermöglichen es Ihnen, Daten in Ihren personalisierten Inhalten zu transformieren und zu bearbeiten. Verwenden Sie sie, um Berechnungen durchzuführen, Daten zu formatieren, Bedingungen anzuwenden und verschiedene Vorgänge auszuführen, um dynamische, maßgeschneiderte Erlebnisse für Ihre Kunden zu erstellen.

Diese Funktionen nutzen die [!DNL Journey Optimizer] Vorlagensprache. Weitere Informationen zu Richtlinien zur Personalisierungssyntax finden [ auf dieser Seite](../personalization-syntax.md).

➡️ [In diesem Video erfahren Sie, wie Sie Hilfsfunktionen verwenden](#video)

## Zugriff auf Helper-Funktionen

Hilfsfunktionen sind im Funktionsmenü des Personalisierungseditors verfügbar:

![](../assets/access-helper-functions.png)

Zur einfachen Navigation sind die Funktionen in drei Kategorien unterteilt:

* **[Funktionen](#functions-helper)** - Datenmanipulations- und -umwandlungsvorgänge
* **[Helper](#helper-helper)** - Bedingte Logik und Dienstprogramm-Funktionen
* **[Operatoren](#operators-helper)** - Vergleich und logische Operatoren

**So verwenden Sie eine Hilfsfunktion:**

1. Kategorie auswählen, um ihre Unterkategorien und verfügbaren Funktionen anzuzeigen
1. Klicken Sie auf das `>`, um Unterkategorien zu erweitern
1. Klicken Sie auf das `+` neben einer Funktion, um sie zu Ihrem Personalisierungs-Code hinzuzufügen
1. Klicken Sie auf das Symbol `...` , um die Funktionsbeschreibung anzuzeigen oder zu Ihren Favoriten hinzuzufügen. [Weitere Informationen](../personalize.md#fav)

>[!NOTE]
>
>Die im Personalisierungseditor verfügbaren Funktionen und Leistungsmerkmale unterscheiden sich von denen im erweiterten Ausdruckseditor [Journey](../../building-journeys/expression/expressionadvanced.md). Beispielsweise ist die `now()` nur in Journey-Ausdrücken verfügbar. [Weitere Informationen](../../email/code-content.md#date-time-limitations)

## Funktionen{#functions-helper}

### Aggregations- und Array-Funktionen

<table>
    <tr>
        <td><a href="aggregation.md#average">Durchschnitt</a></td><td>Die Funktion gibt das arithmetische Mittel aller ausgewählten Werte im Array zurück</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Anzahl</a></td><td>Diese Funktion gibt die Anzahl der Elemente innerhalb des angegebenen Arrays zurück</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-only-null">Nur Null zählen</a></td><td>Diese Funktion zählt die Anzahl der Nullwerte in der Liste.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-with-null">Mit Null zählen</a></td><td>Diese Funktion zählt alle Elemente der Liste einschließlich der Nullwerte.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Eindeutig</a></td><td>Diese Funktion ruft Werte aus einem Array oder einer Liste ab, wobei doppelte Werte entfernt werden</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct-count-with-null">Unterschiedliche Zählung mit Null</a></td><td>Diese Funktion zählt die Anzahl der verschiedenen Werte einschließlich der Nullwerte.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Erstes Element</a></td><td>Diese Funktion gibt das erste Element in einem Array oder einer Liste zurück</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Erste n in Array</a></td><td>Diese Funktion gibt die ersten n Elemente in einem Array zurück, wenn sie anhand des angegebenen numerischen Ausdrucks in aufsteigender Reihenfolge sortiert werden</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">Enthalten</a></td><td>Mit dieser Funktion wird bestimmt, ob ein Element einem Array oder einer Liste angehört</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Umfasst</a></td><td>Diese Funktion bestimmt, ob ein Array oder eine Liste ein bestimmtes Element enthält</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Schnittmengen</a></td><td>Diese Funktion bestimmt, ob zwei Arrays oder Listen mindestens ein gemeinsames Element aufweisen</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Letzte n in Array</a></td><td>Diese Funktion gibt die letzten n Elemente in einem Array zurück, wenn sie anhand des angegebenen numerischen Ausdrucks in aufsteigender Reihenfolge sortiert werden</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Maximum</a></td><td>Diese Funktion gibt den größten aller ausgewählten Werte im Array zurück</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimum</a></td><td>Die Funktion gibt den kleinsten aller ausgewählten Werte im Array zurück</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Nicht enthalten</a></td><td>Diese Funktion bestimmt, ob ein Element nicht in einem Array oder einer Liste enthalten ist</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Teilmenge von</a></td><td>Diese Funktion bestimmt, ob ein bestimmtes Array (Array A) eine Teilmenge eines anderen Arrays (Array B) ist, d. h. ob alle Elemente in Array A Elemente von Array B sind</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Summe</a></td><td>Diese Funktion gibt die Summe aller ausgewählten Werte im Array zurück</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Übergeordnete Gruppe von</a></td><td>Diese Funktion bestimmt, ob ein bestimmtes Array (Array A) eine Obermenge eines anderen Arrays (Array B) ist, d. h. ob das Array A alle Elemente in Array B enthält.</td>
    </tr>
</table>

### Funktionen für Datum/Uhrzeit{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#add-days">Tage hinzufügen</a></td><td>Diese Funktion passt ein bestimmtes Datum um eine angegebene Anzahl von Tagen an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-hours">Stunden hinzufügen</a></td><td>Diese Funktion passt ein bestimmtes Datum um eine angegebene Anzahl von Stunden an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-minutes">Minuten hinzufügen</a></td><td>Diese Funktion passt ein bestimmtes Datum um eine angegebene Anzahl von Minuten an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-months">Monate hinzufügen</a></td><td>Diese Funktion passt ein bestimmtes Datum um eine angegebene Anzahl von Monaten an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-seconds">Sekunden hinzufügen</a></td><td>Diese Funktion passt ein bestimmtes Datum um eine angegebene Anzahl von Sekunden an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-years">Jahre hinzufügen</a></td><td>Diese Funktion passt ein bestimmtes Datum um eine angegebene Anzahl von Jahren an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age">Alter</a></td><td>Diese Funktion ruft das Alter zu einem bestimmten Datum ab.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age-days">Alter in Tagen</a></td><td>Diese Funktion berechnet das Alter eines bestimmten Datums in Tagen, d. h. die Anzahl der Tage, die zwischen dem angegebenen und dem aktuellen Datum verstrichen sind, wobei für zukünftige Datumswerte ein negativer und für vergangene Datumswerte ein positiver Wert gilt.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age-months">Alter in Monaten</a></td><td>Diese Funktion berechnet das Alter eines bestimmten Datums in Monaten, d. h. die Anzahl der Monate, die zwischen dem angegebenen und dem aktuellen Datum verstrichen sind, wobei für zukünftige Datumswerte ein negativer und für vergangene Datumswerte ein positiver Wert gilt.</td>
    </tr>
    <tr>
        <td><a href="dates.md#compare-dates">Daten vergleichen</a></td><td>Diese Funktion vergleicht das erste Eingabedatum mit dem anderen Datum. Gibt 0 zurück, wenn date1 gleich date2 ist, -1, wenn date1 vor date2 liegt, und 1, wenn date1 nach date2 liegt.</td>
    </tr>
    <tr>
        <td><a href="dates.md#convert-zoned-date-time">Uhrzeit-/Datumsangabe in eine bestimmte Zeitzone umwandeln</a></td><td>Diese Funktion wandelt eine Datums-/Uhrzeitangabe in eine bestimmte Zeitzone um.</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">Aktuelle Zeit in Millisekunden</a></td><td>Diese Funktion ruft die aktuelle Zeit in Epochen-Millisekunden ab.</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">Datumsunterschied</a></td><td>Diese Funktion ermittelt die Differenz zwischen zwei Daten in der Anzahl der Tage.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-month">Tag des Monats</a></td><td>Diese Funktion gibt die Zahl zurück, die dem Tag des Monats entspricht.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">Wochentag</a></td><td>Diese Funktion ruft den Wochentag ab.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">Tag des Jahres</a></td><td>Diese Funktion ruft den Tag des Jahres ab.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-seconds">Unterschied in Sekunden</a></td><td>Diese Funktion gibt den Unterschied zwischen zwei Daten in Form von Sekunden zurück.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-hours">Stunden extrahieren</a></td><td>Diese Funktion extrahiert die Stundenkomponente aus einem bestimmten Zeitstempel.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-minutes">Minuten extrahieren</a></td><td>Diese Funktion extrahiert die Minutenkomponente aus einem bestimmten Zeitstempel.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-months">Monate extrahieren</a></td><td>Diese Funktion extrahiert die Monatskomponente aus einem bestimmten Zeitstempel.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-seconds">Sekunden extrahieren</a></td><td>Diese Funktion extrahiert die Sekundenkomponente aus einem bestimmten Zeitstempel.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">Datum formatieren</a></td><td>Diese Funktion formatiert einen Datums-/Uhrzeitwert.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date-locale">Formatieren des Datums mit Gebietsschema-Unterstützung</a></td><td>Diese Funktion formatiert einen Datums-/Uhrzeitwert in die entsprechende sprachabhängige Darstellung, d. h. in einem gewünschten Gebietsschema.</td>
    </tr>
    <tr>
        <td><a href="dates.md#get-current-zoned-date-time">CurrentZonedDateTime abrufen</a></td><td>Diese Funktion gibt das aktuelle Datum und die aktuelle Uhrzeit mit Zeitzoneninformationen zurück.</td>
    </tr>
    <tr>
        <td><a href="dates.md#hours-difference">Stundendifferenz</a></td><td>Diese Funktion gibt den Unterschied zwischen zwei Daten in Form von Stunden zurück.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-minutes">Minutendifferenz</a></td><td>Diese Funktion gibt den Unterschied zwischen zwei Daten in Form von Minuten zurück.</td>
    </tr>
    <tr>
        <td><a href="dates.md#months-difference">Monatsdifferenz</a></td><td>Diese Funktion gibt den Unterschied zwischen zwei Daten in Form von Monaten zurück.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">Tage festlegen</a></td><td>Diese Funktion legt den Tag des Monats für die gegebene Datums-/Uhrzeitangabe fest.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">Stunden festlegen</a></td><td>Diese Funktion legt die Stunde der Datums-/Uhrzeitangabe fest.</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-date-time">Zu Uhrzeit-/Datumsangabe</a></td><td>Diese Funktion wandelt eine Zeichenfolge in ein Datum um. Bei einer ungültigen Eingabe wird als Ausgabe das Epochen-Datum zurückgegeben.</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">In UTC</a></td><td>Diese Funktion wandelt eine Datums-/Uhrzeitangabe in UTC um.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-day">Auf Tagesanfang kürzen</a></td><td>Diese Funktion ändert eine bestimmte Datums-/Uhrzeitangabe, indem sie auf den Tagesanfang gesetzt wird, wobei die Zeit auf 00:00 Uhr eingestellt ist.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-quarter">truncateToStartOfQuarter</a></td><td>Diese Funktion kürzt eine Datums-/Uhrzeitangabe auf den ersten Tag des Quartals (z. B. 1. Januar, 1. April, 1. Juli, 1. Oktober) um 00:00 Uhr.
</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-week">truncateToStartOfWeek</a></td><td>Diese Funktion ändert eine bestimmte Datums-/Uhrzeitangabe, indem sie auf den Wochenanfang (Montag um 00:00 Uhr) gesetzt wird.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-year">truncateToStartOfYear</a></td><td>Diese Funktion ändert eine bestimmte Datums-/Uhrzeitangabe, indem sie auf den ersten Tag des Jahres (1. Januar) um 00:00 Uhr gekürzt wird.</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">Woche des Jahres</a></td><td>Diese Funktion gibt die Woche des Jahres zurück.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-years">Jahresdifferenz</a></td><td>Diese Funktion gibt den Unterschied zwischen zwei Daten in Form von Jahren zurück.</td>
    </tr>
</table>

### Zuordnungsfunktionen {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">Abrufen</a></td><td>Mit dieser Funktion wird der Wert einer Zuordnung für einen bestimmten Schlüssel abgerufen</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Schlüssel</a></td><td>Mit dieser Funktion werden alle Schlüssel einer angegebenen Zuordnung abgerufen</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Werte</a></td><td>Diese Funktion ruft alle Werte einer angegebenen Zuordnung ab</td>
    </tr>
</table>

### Mathematische Funktionen {#math-functions}

<table>
    <tr>
        <td><a href="math.md#absolute">Absolut</a></td><td>Diese Funktion formatiert eine beliebige Zahl in die sprachabhängige Darstellung.</td>
    </tr>
    <tr>
        <td><a href="math.md#format-number">Zahl formatieren</a></td><td>Diese Funktion formatiert eine beliebige Zahl in die sprachabhängige Darstellung.</td>
    </tr>
    <tr>
        <td><a href="math.md#random">Zufällig</a></td><td>Diese Funktion gibt einen Zufallswert zwischen 0 und 1 zurück.</td>
    </tr>
    <tr>
        <td><a href="math.md#round-down">Abrunden</a></td><td>Diese Funktion rundet eine Zahl ab.</td>
    </tr>
    <tr>
        <td><a href="math.md#round-up">Aufrunden</a></td><td>Diese Funktion rundet eine Zahl auf.</td>
    </tr>
    <tr>
    <td><a href="math.md#to-hex-string">In hexadezimale Zeichenfolge</a></td><td>Konvertiert eine beliebige Zahl in ihren hexadezimalen String.</td>
    </tr>
    <tr>
    <td><a href="math.md#to-int">ToInt</a></td><td>Konvertiert jeden dieser Typen (number, double, int, long, float, short, byte, boolean, string) in eine Ganzzahl.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-percentage">Zu Prozentwert</a></td><td>Diese Funktion wandelt eine Zahl in einen Prozentwert um.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-precision">Zu Präzision</a></td><td>Diese Funktion wandelt eine Zahl mit der erforderlichen Präzision um.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-string">In Zeichenfolge</a></td><td>Diese Funktion konvertiert eine beliebige Zahl in ihre Zeichenfolgendarstellung. </td>
    </tr>
</table>

### Objektfunktionen {#object-functions}

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Ist nicht null</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Objektreferenz vorhanden ist</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">Ist null</a></td><td>Mit dieser Funktion wird bestimmt, ob keine Objektreferenz vorhanden ist</td>
    </tr>
</table>

### Zeichenfolgen-Funktionen {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">Binnenmajuskel</a></td><td>Mit dieser Funktion wird der erste Buchstabe jedes Wortes einer Zeichenfolge großgeschrieben</td>
    </tr>
    <tr>
        <td><a href="string.md#char-code-at">Char-Code bei</a></td><td>Diese Funktion gibt den ASCII-Wert eines Zeichens zurück, wie etwa die Funktion charCodeAt in JavaScript</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Verknüpfen</a></td><td>Mit dieser Funktion werden zwei Zeichenfolgen zu einer zusammengeführt</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Enthält</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge eine angegebene Unterzeichenfolge enthält</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Enthält nicht</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge eine angegebene Unterzeichenfolge nicht enthält</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">Endet nicht mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge endet</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">Beginnt nicht mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge beginnt</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">Codieren 64</a></td><td>Diese Funktion wird verwendet, um eine Zeichenfolge zu codieren.</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Endet mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge endet</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Gleich</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Zeichenfolge übereinstimmt</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Gleich ohne Groß-/Kleinschreibung</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Zeichenfolge übereinstimmt, Groß-/Kleinschreibung wird nicht beachtet</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">E-Mail-Domain extrahieren</a></td><td>Mit dieser Funktion wird die Domain einer E-Mail-Adresse extrahiert</td>
    </tr>
    <tr>
        <td><a href="string.md#format-currency">Währung formatieren</a></td><td>Diese Funktion konvertiert eine beliebige Zahl in die entsprechende sprachabhängige Währungsdarstellung, je nachdem, welches Gebietsschema als Zeichenfolge im zweiten Argument übergeben wurde.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-host">URL-Host abrufen</a></td><td>Diese Funktion wird verwendet, um den URL-Host abzurufen.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-path">URL-Pfad abrufen</a></td><td>Diese Funktion wird verwendet, um den URL-Pfad abzurufen.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-protocol">URL-Protokoll abrufen</a></td><td>Diese Funktion wird verwendet, um das URL-Protokoll abzurufen.</td>
    </tr>
    <tr>
        <td><a href="string.md#index-of">Index von</a></td><td>Diese Funktion gibt die Position (im ersten Argument) des ersten Auftretens des zweiten Parameters zurück. Gibt -1 zurück, wenn keine Übereinstimmung vorliegt</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">isEmpty</a></td><td>Mit dieser Funktion wird geprüft, ob eine Zeichenfolge oder ein Ausdruck leer ist</td>
    </tr>
    <tr>
        <td><a href="string.md#is-not-empty">Ist nicht leer</a></td><td>Diese Funktion gibt „true“ zurück, wenn die Zeichenfolge im Parameter nicht leer ist.</td>
    </tr>
    <tr>
        <td><a href="string.md#last-index-of">Letzter Index von</a></td><td>Diese Funktion gibt die Position (im ersten Argument) des letzten Auftretens des zweiten Parameters zurück. Gibt -1 zurück, wenn keine Übereinstimmung vorliegt.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Links kürzen</a></td><td>Diese Funktion entfernt Leerzeichen vom Anfang einer Zeichenfolge</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Länge</a></td><td>Mit dieser Funktion wird die Anzahl der Zeichen in einer Zeichenfolge oder einem Ausdruck zurückgegeben</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Ist wie</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge einem angegebenen Muster entspricht</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Kleinbuchstaben</a></td><td>Diese Funktion wandelt eine Zeichenfolge in Kleinbuchstaben um</td>
    </tr>
    <tr>
        <td><a href="string.md#mask">Maskieren</a></td><td>Diese Funktion wird verwendet, um einen Teil einer Zeichenfolge durch „X“-Zeichen zu ersetzen.</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Stimmt überein mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einem bestimmten regulären Ausdruck übereinstimmt</td>
    </tr>
    <tr>
        <td><a href="string.md#md5">MD5</a></td><td>Diese Funktion gibt den MD5-Hash der Eingabezeichenfolge zurück.</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Ungleich</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge nicht gleich der angegebenen Zeichenfolge ist</td>
    </tr>
    <tr>
        <td><a href="string.md#not-equal-with-ignore-case">Entspricht nicht (Groß-/Kleinschreibung ignorieren)</a></td><td>Diese Funktion vergleicht zwei Zeichenfolgen miteinander, wobei die Groß- und Kleinschreibung ignoriert wird.</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Gruppe regelmäßiger Ausdrücke</a></td><td>Mit dieser Funktion werden spezifische Informationen basierend auf dem bereitgestellten regulären Ausdruck extrahiert</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Ersetzen</a></td><td>Diese Funktion ersetzt eine angegebene Teilzeichenfolge in einer Zeichenfolge durch eine andere Teilzeichenfolge</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">Alle ersetzen</a></td><td>Diese Funktion ersetzt alle Teilzeichenfolgen eines Textes, die mit dem „Ziel“ übereinstimmen, durch die angegebene literale „Ersatz“-Zeichenfolge</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Kürzung rechts</a></td><td>Diese Funktion entfernt Leerzeichen am Ende einer Zeichenfolge </td>
    </tr>
    <tr>
        <td><a href="string.md#sha256">SHA256</a></td><td>Diese Funktion berechnet den SHA256-Hash einer Zeichenfolge und gibt ihn zurück.</td>
    </tr>
    <tr>
        <td><a href="string.md#split">Teilen</a></td><td>Mit dieser Funktion wird eine Zeichenfolge durch ein bestimmtes Zeichen aufgeteilt</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Beginnt mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge beginnt</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-date">Zeichenfolge zu Datum</a></td><td>Diese Funktion konvertiert einen Zeichenfolgenwert in einen Datums-/Uhrzeitwert.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-integer">Zeichenfolge zu Ganzzahl</a></td><td>Diese Funktion wandelt einen Zeichenfolgenwert in einen ganzzahligen Wert um.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-number">Zeichenfolge zu Zahl</a></td><td>Mit dieser Funktion wird eine Zeichenfolge in eine Zahl konvertiert. Bei einer ungültigen Eingabe wird dieselbe Zeichenfolge als Ausgabe zurückgegeben.</td>
    </tr>
    <tr>
        <td><a href="string.md#sub-string">Teilzeichenfolge</a></td><td>Diese Funktion gibt die Teilzeichenfolge des Zeichenfolgenausdrucks zwischen dem Anfangsindex und dem Endindex zurück.</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Titelschreibweise</a></td><td>Diese Funktion wird verwendet, um die ersten Buchstaben jedes Wortes einer Zeichenfolge großzuschreiben</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">Zu booleschem Wert</a></td><td>Diese Funktion wandelt einen Argumentwert abhängig vom Typ in einen booleschen Wert um.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">Zu Uhrzeit-/Datumsangabe</a></td><td>Diese Funktion wird verwendet, um die Zeichenfolge in ein Datum zu konvertieren. Bei einer ungültigen Eingabe wird als Ausgabe das Epochen-Datum zurückgegeben.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time-only">Nur zu Datums-/Uhrzeitangabe</a></td><td>Diese Funktion wandelt einen Argumentwert in einen reinen Datums-/Uhrzeit-Wert um. Bei einer ungültigen Eingabe wird als Ausgabe das Epochen-Datum zurückgegeben.</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Kürzen</a></td><td>Diese Funktion entfernt Leerzeichen vom Anfang und vom Ende einer Zeichenfolge</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Großbuchstaben</a></td><td>Diese Funktion wandelt eine Zeichenfolge in Großbuchstaben um</td>
    </tr>
    <tr>
        <td><a href="string.md#url-decode">URL-Decodierung</a></td><td>Diese Funktion wird verwendet, um eine als URL codierte Zeichenfolge zu decodieren.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">URL-Codierung</a></td><td>Diese Funktion wird verwendet, um eine Zeichenfolge als URL zu codieren.</td>
    </tr>
</table>


## Helper{#helper-helper}

Helper werden auf [dieser Seite](helpers.md) näher beschrieben.


<table>
    <tr>
        <td><a href="helpers.md#default">Standardwert für Fallback</a></td><td>Diese Funktion ermöglicht das Rendern einer Variable mit Standardeinstellungen</td>
    </tr>
    <tr>
        <td><a href="helpers.md#each">Jeweils</a></td><td>Diese Funktion wird verwendet, um über ein Array zu iterieren</td>
    </tr>
    <tr>
        <td><a href="helpers.md#execution-metadata">Ausführungsmetadaten</a></td><td>Diese Hilfsfunktion erfasst benutzerdefinierte Schlüssel-Wert-Metadaten beim Rendern der Nachricht, damit sie im Metadatenobjekt der Laufzeitausführung gespeichert werden können</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">Wenn</a></td><td>Mit dieser Funktion wird ein bedingter Block definiert. Wenn die Ausdrucksauswertung „true“ zurückgibt, wird der Block gerendert</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Zulassen</a></td><td>Diese Funktion ermöglicht das Speichern eines Ausdrucks als Variable, die später in einer Abfrage verwendet werden kann</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">Außer</a></td><td>Mit dieser Funktion wird ein bedingter Block definiert. Wenn die Ausdrucksauswertung „false“ zurückgibt, wird der Block gerendert</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">Mit</a></td><td>Diese Funktion wird verwendet, um das Auswertungs-Token des Vorlagenteils zu ändern</td>
    </tr>
</table>

## Operatoren{#operators-helper}

### Arithmetische Funktionen {#arithmetic-helper}

Mit arithmetischen Funktionen lassen sich einfache Berechnungen für Werte durchführen

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">Addieren</a></td><td>Mit diesem Operator wird die Summe zweier Argumentausdrücke ermittelt</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">Dividieren</a></td><td>Mit diesem Operator wird der Quotient zweier Argumentausdrücke ermittelt</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">Multiplizieren</a></td><td>Mit diesem Operator wird das Produkt zweier Argumentausdrücke ermittelt</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">Rest</a> </td><td>Dieser Operator wird verwendet, um den Rest nach der Division der beiden Argumentausdrücke zu ermitteln</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">Subtrahieren</a> </td><td>Mit diesem Operator wird die Differenz zwischen zwei Argumentausdrücken ermittelt</td>
    </tr>
</table>


### Boolesche Funktionen {#boolean-functions}

Boolesche Funktionen werden verwendet, um eine boolesche Logik auf verschiedene Elemente anzuwenden.

<table>
    <tr>
        <td><a href="operators.md#and">Und</a></td><td>Dieser Operator erstellt eine logische Konjunktion</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">Oder</a></td><td>Dieser Operator erstellt eine logische Disjunktion</td>
    </tr>
</table>


### Vergleichsfunktionen {#comparison-functions}

Vergleichsfunktionen werden verwendet, um zwischen verschiedenen Ausdrücken und Werten zu vergleichen und entsprechend „true“ oder „false“ zurückzugeben.

<table>
    <tr>
        <td><a href="operators.md#equals">Gleich</a></td><td>Dieser Vorgang prüft, ob Werte gleich sind</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Größer als</a></td><td>Dieser Operator prüft, ob der erste Wert größer als der zweite Wert ist</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Größer oder gleich</a></td><td>Dieser Operator prüft, ob der erste Wert größer oder gleich dem zweiten Wert ist</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Kleiner oder gleich</a> </td><td>Dieser Operator prüft, ob der erste Wert kleiner oder gleich dem zweiten Wert ist</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">Ungleich</a></td><td>Dieser Operator prüft, ob ein angegebener Ausdruck ungleich einem angegebenen Wert ist</td>
    </tr>
</table>

## Anleitungsvideo{#video}

Erfahren Sie, wie Sie Personalisierungswerte mithilfe von Hilfsfunktionen zur Personalisierung umwandeln und lernen Sie verschiedene Anwendungsfälle für Hilfsfunktionen kennen.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
