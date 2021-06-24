---
title: Bibliothek für Arithmetik-Funktionen
description: Bibliothek für Arithmetik-Funktionen
feature: Personalisierung
topic: Personalisierung
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 96%

---

# Arithmetische Funktionen  {#maths}

Mit arithmetischen Funktionen lassen sich einfache Berechnungen für Werte durchführen

## Addieren{#add}

Mit der Funktion `+` (Addition) wird die Summe zweier Argumentausdrücke ermittelt.

**Format**

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

**Format**

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

**Format**

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

**Format**

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

**Format**

```sql
{%= double % double %}
```

**Beispiel**

Die folgende Operation prüft, ob das Alter der Person durch fünf teilbar ist.

```sql
{%= person.age % 5 = 0 %}
```
