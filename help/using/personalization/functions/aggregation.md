---
title: Bibliothek mit Aggregationsfunktionen
description: Bibliothek mit Aggregationsfunktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '157'
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
