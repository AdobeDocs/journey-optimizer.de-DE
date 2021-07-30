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
ht-degree: 100%

---

# Aggregationsfunktionen {#aggregation}

Aggregationsfunktionen werden verwendet, um mehrere Werte zu gruppieren, sodass ein einziger Zusammenfassungswert gebildet wird.

## Anzahl{#count}

Die Funktion `count` gibt die Anzahl der Elemente innerhalb des angegebenen Arrays zurück.

**Format**

```sql
{%= count(array) %}
```

**Beispiel**

Durch den folgenden Vorgang wird die Anzahl der Bestellungen im Array zurückgegeben.

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

Durch den folgenden Vorgang wird die Summe aller Bestellungen zurückgegeben.

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

Durch den folgenden Vorgang wird der Durchschnittspreis aller Bestellungen zurückgegeben.

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

Durch den folgenden Vorgang wird der niedrigste Preis aller Bestellungen zurückgegeben.

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

Durch den folgenden Vorgang wird der höchste Preis aller Bestellungen zurückgegeben.

```sql
{%=max(orders.order.price)%}
```
