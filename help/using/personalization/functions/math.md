---
title: Bibliothek mit den mathematischen Funktionen
description: Bibliothek mit den mathematischen Funktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: dc313d7cbee9e412b9294b644fddbc7840f90339
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 100%

---

# Mathematische Funktionen {#math}

Erfahren Sie, wie Sie im Ausdruckseditor mathematische Funktionen verwenden.

## Absolut {#absolute}

Die Funktion `absolute` wird verwendet, um eine Zahl in ihren absoluten Wert zu konvertieren.

**Syntax**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

Die Funktion `formatNumber` wird verwendet, um eine beliebige Zahl in eine sprachabhängige Darstellung zu formatieren.

Sie akzeptiert eine Zahl und eine Zeichenfolge, die das Gebietsschema darstellt, und gibt eine formatierte Zeichenfolge der Zahl im gewünschten Gebietsschema zurück.

**Syntax**

```sql
{%= formatNumber(number/double,string) %}: string
```

Sie können Formatierungen und gültige Gebietsschemata verwenden, die in der [Oracle-Dokumentation](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) und in [Unterstützte Gebietsschemata](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank} zusammengefasst werden.

**Beispiel**

Diese Abfrage gibt eine formatierte Zeichenfolge auf Arabisch zurück, die der Eingabenummer 123456.789 entspricht.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Zufällig {#random}

Die Funktion `random` wird verwendet, um einen zufälligen Wert zwischen 0 und 1 zurückzugeben.

**Syntax**

```sql
{%= random() %}: double
```

## Abrunden {#round-down}

Die Funktion `roundDown` wird verwendet, um eine Zahl abzurunden.

**Syntax**

```sql
{%= roundDown(double) %}: double
```

## Aufrunden {#round-up}

Die Funktion `Count only null`wird verwendet, um eine Zahl aufzurunden.

**Syntax**

```sql
{%= roundUp(double) %}: double
```

## In hexadezimale Zeichenfolge {#to-hex-string}

Die Funktion `toHexString` konvertiert eine beliebige Zahl in ihre hexadezimale Zeichenfolge.

**Syntax**

```sql
{%= toHexString(number) %}: string
```

**Beispiel**

Diese Abfrage gibt den hexadezimalen Wert von 158 zurück, also 9e.

```sql
{%= toHexString(158) %}
```

## Zu Prozentwert {#to-percentage}

Die Funktion `toPercentage` wird verwendet, um eine Zahl in einen Prozentwert zu konvertieren.

**Syntax**

```sql
{%= toPercentage(double) %}: string
```

## Zu Präzision {#to-precision}

Die Funktion `toPrecision` wird verwendet, um eine Zahl in die erforderliche Präzision zu konvertieren.

**Syntax**

```sql
{%= toPrecision(double,int) %}: string
```

## In Zeichenfolge {#to-string}

Die Funktion **toString** konvertiert eine beliebige Zahl in ihre Zeichenfolgendarstellung.

**Syntax**

```sql
{%= toString(string) %}: string
```

**Beispiel**

Diese Abfrage gibt „12“ zurück.

```sql
{%= toString(12) %} 
```
