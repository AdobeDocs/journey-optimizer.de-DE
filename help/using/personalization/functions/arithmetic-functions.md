---
title: Funktionsbibliothek
description: Funktionsbibliothek
source-git-commit: cd1b07bbb4b247d1d8c0cc87be9e4bdad22377ed
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 51%

---

# Arithmetische Funktionen {#maths}

![](../../assets/do-not-localize/badge.png)

Arithmetische Funktionen werden verwendet, um grundlegende Berechnungen für Werte durchzuführen.

## Addieren{#add}

Mit der Funktion `+` (Addition) wird die Summe zweier Argumentausdrücke ermittelt.

**Format**

```sql
{%= double + double %}
```

**Beispiel**

Im Folgenden wird der Preis zweier verschiedener Produkte zusammengefasst.

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

Das folgende Verfahren ermittelt das Produkt des Bestands und den Preis eines Produkts, um den Bruttowert des Produkts zu ermitteln.

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

Das folgende Vorhaben ermittelt den Preisunterschied zwischen zwei verschiedenen Produkten.

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

Das folgende Vorhaben ermittelt den Quotienten zwischen den insgesamt verkauften Produkten und dem insgesamt verdienten Geld, um die durchschnittlichen Kosten pro Artikel zu sehen.

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
