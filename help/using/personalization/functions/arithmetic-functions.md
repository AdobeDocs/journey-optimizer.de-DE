---
title: Bibliothek für Arithmetik-Funktionen
description: Bibliothek für Arithmetik-Funktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Arithmetische Funktionen {#maths}

Arithmetische Funktionen dienen der Durchführung grundlegender Berechnungen von Werten.

## Hinzufügen{#add}

Die `+` (Addition) verwendet wird, um die Summe zweier Argumentausdrücke zu finden.

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

Die `*` (Multiplikation) verwendet wird, um das Produkt zweier Argumentausdrücke zu finden.

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

Die `-` (Subtraktion) verwendet wird, um den Unterschied zwischen zwei Argumentausdrücken zu ermitteln.

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

Die `/` (Division) verwendet wird, um den Quotienten zweier Argumentausdrücke zu finden.

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

Die `%` (Modulo/Rest) wird verwendet, um den Rest nach der Division der beiden Argumentausdrücke zu finden.

**Format**

```sql
{%= double % double %}
```

**Beispiel**

Die folgende Operation prüft, ob das Alter der Person durch fünf teilbar ist.

```sql
{%= person.age % 5 = 0 %}
```
