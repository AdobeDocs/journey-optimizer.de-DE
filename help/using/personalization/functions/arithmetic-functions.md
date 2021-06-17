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
ht-degree: 47%

---

# Arithmetische Funktionen {#maths}

Arithmetische Funktionen dienen der Durchführung grundlegender Berechnungen von Werten.

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
