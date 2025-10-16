---
title: Bibliothek mit den mathematischen Funktionen
description: Bibliothek mit den mathematischen Funktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
source-git-commit: 98202be781bec0b03a9a9f33e93f1b01b7830a37
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 77%

---

# Mathematische Funktionen {#math}

Erfahren Sie, wie Sie im Personalisierungseditor mathematische Funktionen verwenden.

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

Sie können Formatierungen und gültige Gebietsschemata verwenden, die in der [Dokumentation zu Oracle ](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) und [Unterstützte Gebietsschemata](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank} zusammengefasst werden

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

Die Funktion `roundUp` wird verwendet, um eine Zahl aufzurunden.

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

Diese Abfrage gibt den Hexadezimalwert 158 zurück, d. h. 9e.

```sql
{%= toHexString(158) %}
```

## To Int {#to-int}

Die Funktion `toInt` wird verwendet, um einen dieser Typen (number, double, int, long, float, short, byte, boolean, string) in eine Ganzzahl zu konvertieren.

**Syntax**

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**Beispiel**

Diese Abfrage gibt den ganzzahligen Wert von 42,6 zurück, d. h. 42.

```sql
{%= toInt(42.6) %}: integer
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
