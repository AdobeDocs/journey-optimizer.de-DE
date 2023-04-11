---
title: Bibliothek für arithmetische Funktionen
description: Bibliothek für arithmetische Funktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Arithmetische Funktionen {#maths}

Mit arithmetischen Funktionen lassen sich einfache Berechnungen für Werte durchführen

## Addieren{#add}

Mit der Funktion `+` (Addition) wird die Summe zweier Argumentausdrücke ermittelt.

**Syntax**

```sql
{%= double + double %}
```

**Beispiel**

Die folgende Operation addiert die Preise von zwei verschiedenen Produkten.

```sql
{%= product1.price + product2.price %}
```

## Multiplizieren{#multiply}

Mit der Funktion `*` (Multiplikation) wird das Produkt zweier Argumentausdrücke ermittelt.

**Syntax**

```sql
{%= double * double %}
```

**Beispiel**

Die folgende Operation ermittelt das Produkt im Bestand sowie den Preis eines Produkts, um den Bruttowert des Produkts zu berechnen.

```sql
{%= product.inventory * product.price %}
```

## Subtrahieren{#substract}

Mit der Funktion `-` (Subtraktion) wird der Unterschied zwischen zwei Argumentausdrücken ermittelt.

**Syntax**

```sql
{%= double - double %}
```

**Beispiel**

Die folgende Operation ermittelt den Preisunterschied zwischen zwei verschiedenen Produkten.

```sql
{%= product1.price - product2.price %}
```

## Dividieren{#divide}

Mit der Funktion `/` (Division) wird der Quotient zweier Argumentausdrücke ermittelt.

**Syntax**

```sql
{%= double / double %}
```

**Beispiel**

Die folgende Operation ermittelt den Quotienten zwischen den insgesamt verkauften Produkten und dem insgesamt verdienten Geld, um so die durchschnittlichen Kosten pro Artikel zu berechnen.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## Rest{#remainder}

Mit der Funktion `%` (Modulo/Rest) wird nach der Division der beiden Argumentausdrücke der Rest ermittelt.

**Syntax**

```sql
{%= double % double %}
```

**Beispiel**

Die folgende Operation prüft, ob das Alter der Person durch fünf teilbar ist.

```sql
{%= person.age % 5 = 0 %}
```
