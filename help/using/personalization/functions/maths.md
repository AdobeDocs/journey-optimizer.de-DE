---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Maths-Funktionen {#math}

![](../../assets/do-not-localize/badge.png)

Arithmetische Funktionen werden verwendet, um grundlegende Berechnungen für Werte in [!DNL Profile Query Language] (PQL) durchzuführen.

## hinzufügen

Die Funktion `+` (Addition) wird verwendet, um die Summe von zwei Argument-Ausdrücken zu finden.

**Format**

```sql
{NUMBER} + {NUMBER}
```

**Beispiel**

Die folgende PQL-Abfrage fasst den Preis von zwei verschiedenen Produkten zusammen.

```sql
product1.price + product2.price
```

## Multiplizieren

Die Funktion `*` (Multiplikation) wird verwendet, um das Produkt zweier Argument-Ausdruck zu finden.

**Format**

```sql
{NUMBER} * {NUMBER}
```

**Beispiel**

Die folgende PQL-Abfrage findet das Produkt des Bestandes und den Produktpreis, um den Bruttowert des Produkts zu ermitteln.

```sql
product.inventory * product.price
```

## Subtrahieren

Die Funktion `-` (Subtraktion) wird verwendet, um den Unterschied von zwei Argument-Ausdrücken zu ermitteln.

**Format**

```sql
{NUMBER} - {NUMBER}
```

**Beispiel**

Die folgende PQL-Abfrage ermittelt den Preisunterschied zwischen zwei verschiedenen Produkten.

```sql
product1.price - product2.price
```

## Teilung

Die Funktion `/` (Division) wird verwendet, um den Quotient zweier Argument-Ausdruck zu finden.

**Format**

```sql
{NUMBER} / {NUMBER}
```

**Beispiel**

Die folgende PQL-Abfrage findet den Quotienten zwischen den insgesamt verkauften Produkten und dem gesamten verdienten Geld, um die durchschnittlichen Kosten pro Artikel zu sehen.

```sql
totalProduct.price / totalProduct.sold
```

## Remainer

Die `%`-Funktion (Modulo/Rest) wird verwendet, um den Rest nach der Teilung der beiden Argument-Ausdruck zu finden.

**Format**

```sql
{NUMBER} % {NUMBER}
```

**Beispiel**

Die folgende PQL-Abfrage prüft, ob das Alter der Person durch fünf teilbar ist.

```sql
person.age % 5 = 0
```
