---
title: Funktionsbibliothek
description: Funktionsbibliothek
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 54%

---

# Aggregationsfunktionen {#aggregation}

![](../../assets/do-not-localize/badge.png)

Aggregationsfunktionen dienen dazu, mehrere Werte zu gruppieren, um einen einzigen Zusammenfassungswert zu bilden.

## Anzahl{#count}

Die Funktion `count` gibt die Anzahl der Elemente innerhalb des angegebenen Arrays zurück.

**Format**

```sql
{%= count(array) %}
```

**Beispiel**

Der folgende Vorgang gibt die Anzahl der Bestellungen im Array zurück.

```sql
{%= count(orders) %}
```

## Summe{#sum}

Die Funktion `sum` gibt die Summe aller ausgewählten Werte im Array zurück.

**Format**

```sql
{%= sum(array) %}
```

**Beispiel**

Der folgende Vorgang gibt die Summe aller Bestellpreise zurück.

```sql
{%=sum(orders.order.price)%}
```

## Durchschnitt{#average}

Die Funktion `average` gibt das arithmetische Mittel aller ausgewählten Werte im Array zurück.

**Format**

```sql
{%= average(array) %}
```

**Beispiel**

Der folgende Vorgang gibt den Durchschnittspreis aller Bestellungen zurück.

```sql
{%=average(orders.order.price)%}
```

## Minimum{#min}

Die Funktion `min` gibt den kleinsten aller ausgewählten Werte im Array zurück.

**Format**

```sql
{%= min(array) %}
```

**Beispiel**

Der folgende Vorgang gibt den niedrigsten Preis aller Bestellungen zurück.

```sql
{%=min(orders.order.price)%}
```

## Maximum{#max}

Die Funktion `max` gibt den größten der ausgewählten Werte im Array zurück.

**Format**

```sql
{%= max(array) %}
```

**Beispiel**

Der folgende Vorgang gibt den höchsten Preis aller Bestellungen zurück.

```sql
{%=max(orders.order.price)%}
```
