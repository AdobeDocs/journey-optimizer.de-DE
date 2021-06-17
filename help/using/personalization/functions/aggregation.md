---
title: Bibliothek mit Aggregationsfunktionen
description: Bibliothek mit Aggregationsfunktionen
feature: Personalisierung
topic: Personalisierung
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 52%

---

# Aggregationsfunktionen {#aggregation}

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
