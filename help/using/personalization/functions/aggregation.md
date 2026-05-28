---
title: Bibliothek mit Aggregationsfunktionen
description: Bibliothek mit Aggregationsfunktionen
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
TQID: https://experienceleague.adobe.com/y1ivXVJe-Y5aIkMu--Tz22U0j-cuGcTUYrdkCkl1xyE
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 100%

---

# Aggregationsfunktionen {#aggregation}

Aggregationsfunktionen werden verwendet, um mehrere Werte zu gruppieren, sodass ein einziger Zusammenfassungswert gebildet wird.

## Durchschnittlicher{#average}

Die Funktion `average` gibt das arithmetische Mittel aller ausgewählten Werte im Array zurück.

**Syntax**

```sql
{%= average(array) %}
```

**Beispiel**

Durch den folgenden Vorgang wird der Durchschnittspreis aller Bestellungen zurückgegeben.

```sql
{%=average(orders.order.price)%}
```

## Anzahl{#count}

Die Funktion `count` gibt die Anzahl der Elemente innerhalb des angegebenen Arrays zurück.

**Syntax**

```sql
{%= count(array) %}
```

**Beispiel**

Durch den folgenden Vorgang wird die Anzahl der Bestellungen im Array zurückgegeben.

```sql
{%= count(orders) %}
```

## Maximum{#max}

Die Funktion `max` gibt den größten der ausgewählten Werte im Array zurück.

**Syntax**

```sql
{%= max(array) %}
```

**Beispiel**

Durch den folgenden Vorgang wird der höchste Preis aller Bestellungen zurückgegeben.

```sql
{%=max(orders.order.price)%}
```

## Minimum{#min}

Die Funktion `min` gibt den kleinsten aller ausgewählten Werte im Array zurück.

**Syntax**

```sql
{%= min(array) %}
```

**Beispiel**

Durch den folgenden Vorgang wird der niedrigste Preis aller Bestellungen zurückgegeben.

```sql
{%=min(orders.order.price) %}
```

## Summe{#sum}

Die Funktion `sum` gibt die Summe aller ausgewählten Werte im Array zurück.

**Syntax**

```sql
{%= sum(array) %}
```

**Beispiel**

Durch den folgenden Vorgang wird die Summe aller Bestellungen zurückgegeben.

```sql
{%=sum(orders.order.price)%}
```
