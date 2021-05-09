---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Aggregationsfunktionen {#aggregation}

![](../../assets/do-not-localize/badge.png)

Aggregationsfunktionen werden verwendet, um mehrere Werte innerhalb von [!DNL Profile Query Language] (PQL)-Arrays zu gruppieren, um einen einzigen Zusammenfassungswert zu bilden.

## Count

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

## Sum

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

## Durchschnittlich

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

## Minimum

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

## Maximum

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
