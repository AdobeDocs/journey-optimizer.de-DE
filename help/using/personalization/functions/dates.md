---
title: Bibliothek mit Funktionen für Datum/Uhrzeit
description: Bibliothek mit Funktionen für Datum/Uhrzeit
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 3a4a58f8601c67e8e9a2b606a47c6b4bcc2dab05
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 100%

---

# Funktionen für Datum/Uhrzeit{#date-time}

Mit Datums- und Uhrzeitfunktionen können Datums- und Uhrzeitvorgänge für Werte in Journey Optimizer durchgeführt werden.

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


## Wochentag{#day-week}

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


## Woche des Jahres in UTC{#week-of-year}

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