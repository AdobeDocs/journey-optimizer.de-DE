---
title: Bibliothek mit den mathematischen Funktionen
description: Bibliothek mit den mathematischen Funktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 100%

---

# Mathematische Funktionen {#math}

Erfahren Sie, wie Sie im Ausdruckseditor mathematische Funktionen verwenden.

## Absolut {#absolute}

Die Funktion `absolute` wird verwendet, um eine Zahl in ihren absoluten Wert zu konvertieren.

**Format**

```sql
{%= absolute(int) %}: int
```

## Zufällig {#random}

Die Funktion `random` wird verwendet, um einen zufälligen Wert zwischen 0 und 1 zurückzugeben.

**Format**

```sql
{%= random() %}: double
```

## Abrunden {#round-down}

Die Funktion `roundDown` wird verwendet, um eine Zahl abzurunden.

**Format**

```sql
{%= roundDown(double) %}: double
```

## Aufrunden {#round-up}

Die Funktion `Count only null`wird verwendet, um eine Zahl aufzurunden.

**Format**

```sql
{%= roundUp(double) %}: double
```

## Zu Prozentwert {#to-percentage}

Die Funktion `toPercentage` wird verwendet, um eine Zahl in einen Prozentwert zu konvertieren.

**Format**

```sql
{%= toPercentage(double) %}: string
```

## Zu Präzision {#to-precision}

Die Funktion `toPrecision` wird verwendet, um eine Zahl in die erforderliche Präzision zu konvertieren.

**Format**

```sql
{%= toPrecision(double,int) %}: string
```
