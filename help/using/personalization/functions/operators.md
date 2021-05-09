---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 0%

---

# Operatoren {#operators}

![](../../assets/do-not-localize/badge.png)

## und

Die Funktion `and` wird zur Erstellung einer logischen Verbindung verwendet.

**Format**

```sql
{QUERY} and {QUERY}
```

**Beispiel**

Die folgende PQL Abfrage wird alle Menschen mit Heimat als Kanada und Geburtsjahr von 1985.

```sql
homeAddress.countryISO = "CA" and person.birthYear = 1985
```

## Oder

Die Funktion `or` wird verwendet, um eine logische Trennung zu erstellen.

**Format**

```sql
{QUERY} or {QUERY}
```

**Beispiel**

Die folgende PQL Abfrage wird alle Menschen mit Heimat als Kanada oder Geburtsjahr von 1985.

```sql
homeAddress.countryISO = "CA" or person.birthYear = 1985
```

## not

Die Funktion `not` (oder `!`) wird zum Erstellen einer logischen Negation verwendet.

**Format**

```sql
not ({QUERY})
!({QUERY})
```

**Beispiel**

Die folgende PQL-Abfrage gibt alle Menschen zurück, die ihr Heimatland nicht als Kanada haben.

```sql
not (homeAddress.countryISO = "CA")
```

## if

Die Funktion `if` wird verwendet, um einen Ausdruck aufzulösen, je nachdem, ob eine angegebene Bedingung wahr ist.

**Format**

```sql
if ({TEST_EXPRESSION}, {TRUE_EXPRESSION}, {FALSE_EXPRESSION})
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{TEST_EXPRESSION}` | Der boolesche Ausdruck, der getestet wird. |
| `{TRUE_EXPRESSION}` | Der Ausdruck, dessen Wert verwendet wird, wenn `{TEST_EXPRESSION}` &quot;true&quot;ist. |
| `{FALSE_EXPRESSION}` | Der Ausdruck, dessen Wert verwendet wird, wenn `{TEST_EXPRESSION}` &quot;false&quot;ist. |

**Beispiel**

Die folgende PQL-Abfrage setzt den Wert auf `1`, wenn das Heimatland Kanada ist, und `2`, wenn das Heimatland nicht Kanada ist.

```sql
if (homeAddress.countryISO = "CA", 1, 2)
```

## Gleich

Die Funktion `=` (gleich) prüft, ob ein Wert oder Ausdruck gleich einem anderen Wert oder Ausdruck ist.

**Format**

```sql
{EXPRESSION} = {VALUE}
```

**Beispiel**

Die folgende PQL-Abfrage prüft, ob sich das Land mit der Heimatadresse in Kanada befindet.

```sql
homeAddress.countryISO = "CA"
```

## ungleich

Die Funktion `!=` (nicht gleich) prüft, ob ein Wert oder Ausdruck **nicht** einem anderen Wert oder Ausdruck entspricht.

**Format**

```sql
{EXPRESSION} != {VALUE}
```

**Beispiel**

Die folgende PQL-Abfrage überprüft, ob das Land der Wohnadresse nicht in Kanada liegt.

```sql
homeAddress.countryISO != "CA"
```

## Größer als

Mit der Funktion `>` (Größer als) wird überprüft, ob der erste Wert größer als der zweite ist.

**Format**

```sql
{EXPRESSION} > {EXPRESSION} 
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, deren Geburtstage nicht im Januar oder Februar liegen.

```sql
person.birthMonth > 2
```

## Größer oder gleich

Mit der Funktion `>=` (größer oder gleich) wird überprüft, ob der erste Wert größer oder gleich dem zweiten Wert ist.

**Format**

```sql
{EXPRESSION} >= {EXPRESSION} 
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, deren Geburtstage nicht im Januar oder Februar liegen.

```sql
person.birthMonth >= 3
```

## Niedriger als

Mit der Vergleichsfunktion `<` (less than) wird geprüft, ob der erste Wert kleiner als der zweite ist.

**Format**

```sql
{EXPRESSION} < {EXPRESSION} 
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, deren Geburtstag im Januar liegt.

```sql
person.birthMonth < 2
```

## Kleiner oder gleich

Mit der Vergleichsfunktion `<=` (kleiner oder gleich) wird geprüft, ob der erste Wert kleiner oder gleich dem zweiten Wert ist.

**Format**

```sql
{EXPRESSION} <= {EXPRESSION} 
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, deren Geburtstag im Januar oder Februar liegt.

```sql
person.birthMonth <= 2
```

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
