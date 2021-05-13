---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 37%

---

# Operatoren   {#operators}

![](../../assets/do-not-localize/badge.png)

## Und

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

## Nicht

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

## Wenn 

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

## Ungleich

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

## Kleiner als

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

## Addieren

Mit der Funktion `+` (Addition) wird die Summe zweier Argumentausdrücke ermittelt.

**Format**

```sql
{NUMBER} + {NUMBER}
```

**Beispiel**

Die folgende PQL-Abfrage addiert die Preise von zwei verschiedenen Produkten.

```sql
product1.price + product2.price
```

## Multiplizieren

Mit der Funktion `*` (Multiplikation) wird das Produkt zweier Argumentausdrücke ermittelt.

**Format**

```sql
{NUMBER} * {NUMBER}
```

**Beispiel**

Die folgende PQL-Abfrage ermittelt das Produkt im Bestand sowie den Preis eines Produkts, um den Bruttowert des Produkts zu berechnen.

```sql
product.inventory * product.price
```

## Subtrahieren

Mit der Funktion `-` (Subtraktion) wird der Unterschied zwischen zwei Argumentausdrücken ermittelt.

**Format**

```sql
{NUMBER} - {NUMBER}
```

**Beispiel**

Die folgende PQL-Abfrage ermittelt den Preisunterschied zwischen zwei verschiedenen Produkten.

```sql
product1.price - product2.price
```

## Dividieren

Mit der Funktion `/` (Division) wird der Quotient zweier Argumentausdrücke ermittelt.

**Format**

```sql
{NUMBER} / {NUMBER}
```

**Beispiel**

Die folgende PQL-Abfrage ermittelt den Quotienten zwischen den insgesamt verkauften Produkten und dem insgesamt verdienten Geld, um so die durchschnittlichen Kosten pro Artikel zu berechnen.

```sql
totalProduct.price / totalProduct.sold
```

## Rest

Mit der Funktion `%` (Modulo/Rest) wird nach der Division der beiden Argumentausdrücke der Rest ermittelt.

**Format**

```sql
{NUMBER} % {NUMBER}
```

**Beispiel**

Die folgende PQL-Abfrage prüft, ob das Alter der Person durch fünf teilbar ist.

```sql
person.age % 5 = 0
```
