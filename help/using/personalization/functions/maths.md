---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: ae0d32c271a77a859ee04d678c884e0203b6a256
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 5%

---

# Maths-Funktionen {#math}

![](../../assets/do-not-localize/badge.png)

Arithmetische Funktionen werden verwendet, um grundlegende Berechnungen für Werte in [!DNL Profile Query Language] (PQL) durchzuführen.

## hinzufügen{#add}

Die Funktion `+` (Addition) wird verwendet, um die Summe von zwei Argument-Ausdrücken zu finden.

**Format**

```sql
{NUMBER} + {NUMBER}
```

**Beispiel**

Im Folgenden wird der Preis zweier verschiedener Produkte zusammengefasst.

```
{%=product1.price + product2.price%}
```

## Multiplizieren{#multiply}

Die Funktion `*` (Multiplikation) wird verwendet, um das Produkt zweier Argument-Ausdruck zu finden.

**Format**

```sql
{NUMBER} * {NUMBER}
```

**Beispiel**

Das folgende Verfahren ermittelt das Produkt des Bestandes und den Preis eines Produkts, um den Bruttowert des Produkts zu ermitteln.

```
{%=product.inventory * product.price%}
```

## Subtrahieren{#substract}

Die Funktion `-` (Subtraktion) wird verwendet, um den Unterschied von zwei Argument-Ausdrücken zu ermitteln.

**Format**

```sql
{NUMBER} - {NUMBER}
```

**Beispiel**

Im Folgenden wird der Preisunterschied zwischen zwei verschiedenen Produkten ermittelt.

```
{%=product1.price - product2.price%}
```

## Dividieren{#divide}

Die Funktion `/` (Division) wird verwendet, um den Quotient zweier Argument-Ausdruck zu finden.

**Format**

```sql
{NUMBER} / {NUMBER}
```

**Beispiel**

Im Folgenden wird der Quotient zwischen den insgesamt verkauften Produkten und dem verdienten Gesamtgeld ermittelt, um die durchschnittlichen Kosten pro Artikel zu sehen.

```
{%=totalProduct.price / totalProduct.sold%}
```

## Remainder{#remainder}

Die `%`-Funktion (Modulo/Rest) wird verwendet, um den Rest nach der Teilung der beiden Argument-Ausdruck zu finden.

**Format**

```sql
{NUMBER} % {NUMBER}
```

**Beispiel**

Der folgende Vorgang überprüft, ob das Alter der Person durch fünf teilbar ist.

```
{%=person.age % 5 = 0%}
```
