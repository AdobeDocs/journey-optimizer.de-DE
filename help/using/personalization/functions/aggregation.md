---
title: Bibliothek mit Aggregationsfunktionen
description: Bibliothek mit Aggregationsfunktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Aggregationsfunktionen {#aggregation}

Aggregationsfunktionen dienen dazu, mehrere Werte zu gruppieren, um einen einzigen Zusammenfassungswert zu bilden.

## Durchschnittlich{#average}

Die `average` gibt das arithmetische Mittel aller ausgewählten Werte im Array zurück.

**Format**

```sql
{%= average(array) %}
```

**Beispiel**

Der folgende Vorgang gibt den Durchschnittspreis aller Bestellungen zurück.

```sql
{%=average(orders.order.price)%}
```

## Count{#count}

Die `count` gibt die Anzahl der Elemente innerhalb des angegebenen Arrays zurück.

**Format**

```sql
{%= count(array) %}
```

**Beispiel**

Der folgende Vorgang gibt die Anzahl der Bestellungen im Array zurück.

```sql
{%= count(orders) %}
```

## Maximum{#max}

Die `max` gibt den größten von allen ausgewählten Werten im Array zurück.

**Format**

```sql
{%= max(array) %}
```

**Beispiel**

Der folgende Vorgang gibt den höchsten Preis aller Bestellungen zurück.

```sql
{%=max(orders.order.price)%}
```

## Minimum{#min}

Die `min` gibt die kleinste aller im Array ausgewählten Werte zurück.

**Format**

```sql
{%= min(array) %}
```

**Beispiel**

Der folgende Vorgang gibt den niedrigsten Preis aller Bestellungen zurück.

```sql
{%=min(orders.order.price) %}
```

## Summe{#sum}

Die `sum` -Funktion gibt die Summe aller im Array ausgewählten Werte zurück.

**Format**

```sql
{%= sum(array) %}
```

**Beispiel**

Der folgende Vorgang gibt die Summe aller Bestellpreise zurück.

```sql
{%=sum(orders.order.price)%}
```
