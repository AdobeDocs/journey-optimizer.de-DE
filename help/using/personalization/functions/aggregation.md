---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: ae0d32c271a77a859ee04d678c884e0203b6a256
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 7%

---

# Aggregationsfunktionen {#aggregation}

![](../../assets/do-not-localize/badge.png)

Aggregationsfunktionen werden verwendet, um mehrere Werte innerhalb von [!DNL Profile Query Language] (PQL)-Arrays zu gruppieren, um einen einzigen Zusammenfassungswert zu bilden.

## Count{#count}

Die Funktion `count` gibt die Anzahl der Elemente innerhalb des angegebenen Arrays zurück.

**Format**

```sql
count({ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage gibt die Anzahl der Bestellungen im Array zurück.

```sql
count(orders)
```

## Sum{#sum}

Die Funktion `sum` gibt die Summe aller ausgewählten Werte im Array zurück.

**Format**

```sql
sum({ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage gibt die Summe aller Bestellpreise zurück.

```sql
sum(orders.order.price)
```

## Durchschnitt{#average}

Die Funktion `average` gibt das arithmetische Mittel aller ausgewählten Werte im Array zurück.

**Format**

```sql
average({ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage gibt den Durchschnittspreis aller Bestellungen zurück.

```sql
average(orders.order.price)
```

## Minimum{#min}

Die Funktion `min` gibt die kleinsten aller ausgewählten Werte im Array zurück.

**Format**

```sql
min({ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage gibt den niedrigsten Preis aller Bestellungen zurück.

```sql
min(orders.order.price)
```

## Maximum{#max}

Die Funktion `max` gibt den größten der ausgewählten Werte im Array zurück.

**Format**

```sql
max({ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage gibt den höchsten Preis aller Bestellungen zurück.

```sql
max(orders.order.price)
```
