---
title: Bibliothek mit Funktionen für Datumszeitfunktionen
description: Bibliothek mit Funktionen für Datumszeitfunktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: f06e1e03b3660be36b32437647a8329d0c0d296e
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# Datums-/Uhrzeitfunktionen{#date-time}

Mit Datums- und Uhrzeitfunktionen können Sie Datums- und Uhrzeitvorgänge für Werte in Journey Optimizer durchführen.

## Alter{#age}

Die `age` -Funktion wird verwendet, um das Alter von einem bestimmten Datum abzurufen.

**Format**

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

Die `currentTimeInMillis` -Funktion wird verwendet, um die aktuelle Zeit in Epoch-Millisekunden abzurufen.

**Format**

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

Die `dateDiff` -Funktion wird verwendet, um die Differenz zwischen zwei Daten in Anzahl von Tagen abzurufen.

**Format**

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

Die `dayOfWeek` -Funktion wird zum Abrufen des Wochentags verwendet.

**Format**

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

Die `dayOfYear` -Funktion wird zum Abrufen des Jahrestages verwendet.

**Format**

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

## Datum des Formats{#format-date}

Die `formatDate` -Funktion zum Formatieren eines Datums-/Uhrzeitwerts verwendet. Das Format sollte ein gültiges Java DateTimeFormat-Muster sein.

**Format**

```sql
{%= formatDate(datetime, format) %}
```

Dabei ist die erste Zeichenfolge das Datumsattribut und der zweite Wert, wie das Datum konvertiert und angezeigt werden soll.

>[!NOTE]
>
> Wenn ein Datumsmuster ungültig ist, wird das Datum auf das ISO-Standardformat zurückgesetzt.
>
> Sie können die Java-Funktionen zur Datumsformatierung wie zusammengefasst verwenden [in der Oracle-Dokumentation](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Beispiel**

Der folgende Vorgang gibt das Datum im folgenden Format zurück: MM/TT/JJ.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## Festlegen von Tagen{#set-days}

Die `setDays` -Funktion wird verwendet, um den Tag des Monats für die angegebene Datums-/Uhrzeitangabe festzulegen.

**Format**

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

## Festlegen von Stunden{#set-hours}

Die `setHours` -Funktion verwendet wird, um die Stunde der Datums-/Uhrzeitangabe festzulegen.

**Format**

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


## auf UTC{#to-utc}

Die `toUTC` -Funktion wird verwendet, um einen Datetime in UTC zu konvertieren.


**Format**

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


## Woche UTC des Jahres{#week-of-year}

Die `weekOfYear` -Funktion verwendet wird, um die Woche des Jahres abzurufen.

**Format**

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