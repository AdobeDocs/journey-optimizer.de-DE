---
title: Mathematische Funktionsbibliothek
description: Mathematische Funktionsbibliothek
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# Mathematische Funktionen {#math}

Erfahren Sie, wie Sie die Math-Funktionen im Ausdruckseditor verwenden.

## Absolut {#absolute}

Die `absolute` -Funktion verwendet wird, um eine Zahl, deren absoluter Wert ist, zu konvertieren.

**Format**

```sql
{%= absolute(int) %}: int
```

## Random {#random}

Die `random` -Funktion wird verwendet, um einen zufälligen Wert zwischen 0 und 1 zurückzugeben.

**Format**

```sql
{%= random() %}: double
```

## Nach unten {#round-down}

Die `roundDown` -Funktion verwendet wird, um eine Zahl zu runden.

**Format**

```sql
{%= roundDown(double) %}: double
```

## Round Up {#round-up}

Die `Count only null` -Funktion verwendet wird, um eine Zahl aufzurunden.

**Format**

```sql
{%= roundUp(double) %}: double
```

## In Prozent {#to-percentage}

Die `toPercentage` -Funktion verwendet wird, um eine Zahl in einen Prozentsatz zu konvertieren.

**Format**

```sql
{%= toPercentage(double) %}: string
```

## Zur Genauigkeit {#to-precision}

Die `toPrecision` -Funktion verwendet wird, um eine Zahl in die erforderliche Genauigkeit zu konvertieren.

**Format**

```sql
{%= toPrecision(double,int) %}: string
```
