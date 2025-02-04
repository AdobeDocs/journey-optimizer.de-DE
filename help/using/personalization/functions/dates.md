---
title: Bibliothek mit Funktionen für Datum/Uhrzeit
description: Bibliothek mit Funktionen für Datum/Uhrzeit
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 3eab04f28b1daab556c4b4395d67f28d292fc52b
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 46%

---

# Funktionen für Datum/Uhrzeit{#date-time}

Mit Datums- und Uhrzeitfunktionen können Datums- und Uhrzeitvorgänge für Werte in Journey Optimizer durchgeführt werden.

## Tage hinzufügen {#add-days}

Die `addDays`-Funktion passt ein bestimmtes Datum um eine bestimmte Anzahl von Tagen an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.

**Syntax**

```sql
{%= addDays(date, number) %}
```

+++Beispiel

* Eingabe: `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Ausgabe: `2024-11-11T17:19:51Z`

+++

## Stunden hinzufügen {#add-hours}

Die `addHours`-Funktion passt ein bestimmtes Datum um eine bestimmte Anzahl von Stunden an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.

**Syntax**

```sql
{%= addHours(date, number) %}
```

+++Beispiel

* Eingabe: `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* Ausgabe: `2024-11-01T18:19:51Z`

+++

## Minuten hinzufügen {#add-minutes}

Die `addMinutes`-Funktion passt ein bestimmtes Datum um eine angegebene Anzahl von Minuten an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden

**Syntax**

```sql
{%= addMinutes(date, number) %}
```

+++Beispiel

* Eingabe: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Ausgabe: `2024-11-01T18:09:51Z`

+++

## Monate hinzufügen {#add-months}

Die `addMonths`-Funktion passt ein bestimmtes Datum um eine bestimmte Anzahl von Monaten an, wobei positive Werte inkrementiert und negative Werte dekrementiert werden.

**Syntax**

```sql
{%= addMonths(date, number) %}
```

+++Beispiel

* Eingabe: `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Ausgabe: `2025-01-01T17:19:51Z`

+++

## Sekunden hinzufügen {#add-seconds}

Der `addSeconds` passt ein bestimmtes Datum um eine bestimmte Anzahl von Sekunden an, wobei positive Werte zum Erhöhen und negative Werte zum Verringern verwendet werden.

**Syntax**

```sql
{%= addSeconds(date, number) %}
```

+++Beispiel

* Eingabe: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Ausgabe: `2024-11-01T17:20:01Z`

+++

## Jahre hinzufügen {#add-years}

Der `addYears` passt ein bestimmtes Datum um eine bestimmte Anzahl von Jahren an, wobei positive Werte inkrementiert und negative Werte inkrementiert werden.

**Syntax**

```sql
{%= addYears(date, number) %}
```

+++Beispiel

* Eingabe: `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Ausgabe: `2026-11-01T17:19:51Z`

+++

## Alter{#age}

Die `age`-Funktion wird verwendet, um das Alter zu einem bestimmten Datum abzurufen.

**Syntax**

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

## Alter in Tagen {#age-days}

Die `ageInDays` berechnet das Alter eines bestimmten Datums in Tagen, d. h. die Anzahl der Tage, die zwischen dem angegebenen Datum und dem aktuellen Datum verstrichen sind, negativ für zukünftige Datumswerte und positiv für vergangene Datumswerte.

**Syntax**

```sql
{%= ageInDays(date) %}
```

+++Beispiel

currentDate = 2025-01-07T12:17:10.720122+05:30 (Asia/Kolkata)

* Eingabe: `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* Ausgabe: `5`

+++

## Alter in Monaten {#age-months}

Die `ageInMonths` berechnet das Alter eines bestimmten Datums in Monaten, d. h. die Anzahl der Monate, die zwischen dem angegebenen Datum und dem aktuellen Datum vergangen sind, negativ für zukünftige Daten und positiv für vergangene Daten.

**Syntax**

```sql
{%= ageInMonths(date) %}
```

+++Beispiel

currentDate = 2025-01-07T12:22:46.993748+05:30(Asia/Kolkata)

* Eingabe: `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* Ausgabe: `12`

+++

## Daten vergleichen {#compare-dates}

Die `compareDates` vergleicht das erste Eingabedatum mit dem anderen. Gibt 0 zurück, wenn date1 gleich date2 ist, -1, wenn date1 vor date2 liegt, und 1, wenn date1 nach date2 liegt.

**Syntax**

```sql
{%= compareDates(date1, date2) %}
```

+++Beispiel

* Eingabe: `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* Ausgabe: `-1`

+++

## ZonedDateTime konvertieren {#convert-zoned-date-time}

Die `convertZonedDateTime` konvertiert eine Datums-/Uhrzeitangabe in eine bestimmte Zeitzone.

**Syntax**

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

+++Beispiel

* Eingabe: `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* Ausgabe: `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

## Aktuelle Zeit in Millisekunden{#current-time}

Die `currentTimeInMillis`-Funktion wird verwendet, um die aktuelle Zeit in Epochenmillisekunden abzurufen.

**Syntax**

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

## Datumsunterschied{#date-diff}

Die `dateDiff`-Funktion wird verwendet, um die Differenz zwischen zwei Daten als Anzahl von Tagen abzurufen.

**Syntax**

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Tag des Monats {#day-month}

Die `dayOfWeek` gibt die Zahl zurück, die den Tag des Monats darstellt.

**Syntax**

```sql
{%= dayOfMonth(datetime) %}
```

+++Beispiel

* Eingabe: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Ausgabe: `5`

+++


## Wochentag {#day-week}

Die `dayOfWeek`-Funktion wird zum Abrufen des Wochentags verwendet.

**Syntax**

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Tag des Jahres{#day-year}

Die `dayOfYear`-Funktion wird zum Abrufen des Tages des Jahres verwendet.

**Syntax**

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Unterschied in Sekunden {#diff-seconds}

Die `diffInSeconds` gibt die Differenz zwischen zwei Daten in Sekunden zurück.

**Syntax**

```sql
{%= diffInSeconds(endDate, startDate) %}
```

+++Beispiel

* Eingabe: `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* Ausgabe: `50`

+++

## Stunden extrahieren {#extract-hours}

Die Funktion `extractHours` extrahiert die Komponente Stunde aus einem bestimmten Zeitstempel.

**Syntax**

```sql
{%= extractHours(date) %}
```

+++Beispiel

* Eingabe: `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* Ausgabe: `17`

+++

## Minuten extrahieren {#extract-minutes}

Die Funktion `extractMinutes` extrahiert die Minutenkomponente aus einem bestimmten Zeitstempel.

**Syntax**

```sql
{%= extractMinutes(date) %}
```

+++Beispiel

* Eingabe: `{%= extractMinute(stringToDate("2024-11-01T17:19:51Z"))%}`
* Ausgabe: `19`

+++

## Monate extrahieren {#extract-months}

Die Funktion `extractMonth` extrahiert die Komponente Monat aus einem bestimmten Zeitstempel.

**Syntax**

```sql
{%= extractMonths(date) %}
```

+++Beispiel

* Eingabe: `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* Ausgabe: `11`

+++

## Sekunden extrahieren {#extract-seconds}

Die Funktion `extractSeconds` extrahiert die zweite Komponente aus einem bestimmten Zeitstempel.

**Syntax**

```sql
{%= extractSeconds(date) %}
```

+++Beispiel

* Eingabe: `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* Ausgabe: `51`

+++

## Datum formatieren{#format-date}

Die `formatDate`-Funktion wird zum Formatieren eines Datums-/Uhrzeitwerts verwendet. Das Format sollte ein gültiges Java-DateTimeFormat-Muster sein.

**Syntax**

```sql
{%= formatDate(datetime, format) %}
```

Dabei ist die erste Zeichenfolge das Datumsattribut, und der zweite Wert gibt an, wie das Datum konvertiert und angezeigt werden soll.

>[!NOTE]
>
> Wenn ein Datumsformat ungültig ist, wird das Datum auf das ISO-Standardformat zurückgesetzt.
>
> Sie können zur Datumsformatierung die Java-Funktionen verwenden, die in der [Oracle-Dokumentation](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank} zusammengefasst sind.

**Beispiel**

Der folgende Vorgang gibt das Datum in diesem Format zurück: MM/TT/JJ.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

## Formatieren des Datums mit Gebietsschema-Unterstützung{#format-date-locale}

Die Funktion `formatDate` wird verwendet, um einen Datums-/Uhrzeitwert in die entsprechende sprachabhängige Darstellung zu formatieren, d. h. in einem gewünschten Gebietsschema. Das Format sollte ein gültiges Java-DateTimeFormat-Muster sein.

**Syntax**

```sql
{%= formatDate(datetime, format, locale) %}
```

Dabei ist die erste Zeichenfolge das Datumsattribut, der zweite Wert ist die Art, wie das Datum konvertiert und angezeigt werden soll, und der dritte Wert stellt das Gebietsschema im Zeichenfolgenformat dar.

>[!NOTE]
>
> Wenn ein Datumsformat ungültig ist, wird das Datum auf das ISO-Standardformat zurückgesetzt.
>
> Sie können zur Datumsformatierung die Java-Funktionen verwenden, die in der [Oracle-Dokumentation](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html) zusammengefasst sind.
>
> Sie können Formatierungen und gültige Gebietsschemata verwenden, die in der [Oracle-Dokumentation](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) und in den [unterstützten Gebietsschemata](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html) zusammengefasst sind.

**Beispiel**

Der folgende Vorgang gibt das Datum in diesem Format zurück: MM/TT/JJ und Gebietsschema FRANKREICH.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## CurrentZonedDateTime abrufen {#get-current-zoned-date-time}

Die Funktion `getCurrentZonedDateTime` gibt das aktuelle Datum und die aktuelle Uhrzeit mit Informationen zur Zeitzone zurück.

**Syntax**

```sql
{%= getCurrentZonedDateTime() %}
```

+++Beispiel

* Eingabe: `{%= getCurrentZonedDateTime() %}`
* Ausgabe: `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

## Stundendifferenz {#hours-difference}

Die `diffInHours` gibt die Differenz zwischen zwei Daten in Stunden zurück.

**Syntax**

```sql
{%= diffInHours(endDate, startDate) %}
```

+++Beispiel

* Eingabe: `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* Ausgabe: `10`

+++

## Minutendifferenz{#diff-minutes}

Die `diffInMinutes`-Funktion wird verwendet, um die Differenz zwischen zwei Daten in Minuten zurückzugeben.

**Syntax**

```sql
{%= diffInMinutes(endDate, startDate) %}
```

+++Beispiel

* Eingabe: `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* Ausgabe: `60`

+++

## Monatsdifferenz {#months-difference}

Die `diffInMonths` gibt die Differenz zwischen zwei Daten als Monat zurück.

**Syntax**

```sql
{%= diffInMonths(endDate, startDate) %}
```

+++Beispiel

* Eingabe: `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* Ausgabe: `3`

+++

## Tage festlegen{#set-days}

Die `setDays`-Funktion wird verwendet, um den Tag des Monats für die Datums-/Uhrzeitangabe festzulegen.

**Syntax**

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Stunden festlegen{#set-hours}

Die `setHours`-Funktion wird verwendet, um die Stunde der Datums-/Uhrzeitangabe festzulegen.

**Syntax**

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Zu Uhrzeit-/Datumsangabe {#to-date-time}

Die `ToDateTime` konvertiert die Zeichenfolge in ein Datum. Bei einer ungültigen Eingabe wird als Ausgabe das Epoch-Datum zurückgegeben.

**Syntax**

```sql
{%= toDateTime(string, string) %}
```

+++Beispiel

* Eingabe: `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* Ausgabe: `2024-11-01T17:19:51Z`

+++

## In UTC{#to-utc}

Die `toUTC`-Funktion wird verwendet, um eine Datums-/Uhrzeitangabe in UTC zu konvertieren.

**Syntax**

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Auf Tagesanfang kürzen {#truncate-day}

Mit der Funktion `truncateToStartOfDay` wird eine Datums-/Uhrzeitangabe geändert, indem die Uhrzeit auf den Beginn des Tages mit 00:00 Uhr festgelegt wird.

**Syntax**

```sql
{%= truncateToStartOfDay(date) %}
```

+++Beispiel

* Eingabe: `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* Ausgabe: `2024-11-01T00:00Z`

+++

## truncateToStartOfQuarter {#truncate-quarter}

Mit der Funktion `truncateToStartOfQuarter` wird eine Datums-/Uhrzeitangabe auf den ersten Tag des Quartals (z. B. 1. Januar, 1. April, 1. Juli, 1. Oktober) um 0:00 Uhr gekürzt.

**Syntax**

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

+++Beispiel

* Eingabe: `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* Ausgabe: `2024-10-01T00:00Z`

+++

## truncateToStartOfWeek {#truncate-week}

Die `truncateToStartOfWeek`-Funktion ändert eine bestimmte Datums-/Uhrzeitangabe, indem sie sie auf den Beginn der Woche (Montag um 00:00 Uhr) setzt.

**Syntax**

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

+++Beispiel

* Eingabe: `truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* Ausgabe: `2024-11-18T00:00Z // monday`

+++

## truncateToStartOfYear {#truncate-year}

Mit der Funktion `truncateToStartOfYear` wird eine Datums-/Uhrzeitangabe geändert, indem sie auf den ersten Tag des Jahres (1. Januar) um 0:00 Uhr gekürzt wird.

**Syntax**

```sql
{%= truncateToStartOfYear(dateTime) %}
```

+++Beispiel

* Eingabe: `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* Ausgabe: `2024-01-01T00:00Z`

+++

## Woche des Jahres {#week-of-year}

Die `weekOfYear`-Funktion wird verwendet, um die Woche des Jahres abzurufen.

**Syntax**

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Jahresdifferenz {#diff-years}

Die `diffInYears`-Funktion wird verwendet, um die Differenz zwischen zwei Daten als Jahre zurückzugeben.

**Syntax**

```sql
{%= diffInYears(endDate, startDate) %}: int
```

+++Beispiel

* Eingabe: `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* Ausgabe: `5`

+++
