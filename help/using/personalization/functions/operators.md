---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 5304db1456f0541d18823f862ae420892e46fd89
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 8%

---

# Benutzer {#operators}

![](../../assets/do-not-localize/badge.png)

## Und{#and}

Die Funktion `and` wird zur Erstellung einer logischen Verbindung verwendet.

**Format**

```sql
{QUERY} and {QUERY}
```

**Beispiel**

Die folgende Operation wird alle Menschen mit Heimat-Land als Kanada und Geburtsjahr von 1985.

```sql
homeAddress.countryISO = "CA" and person.birthYear = 1985
```

## Oder{#or}

Die Funktion `or` wird verwendet, um eine logische Trennung zu erstellen.

**Format**

```sql
{QUERY} or {QUERY}
```

**Beispiel**

Die folgende Operation wird alle Menschen mit Heimat-Land als Kanada oder Geburtsjahr von 1985.

```sql
homeAddress.countryISO = "CA" or person.birthYear = 1985
```

## Not{#not}

Die Funktion `not` (oder `!`) wird zum Erstellen einer logischen Negation verwendet.

**Format**

```sql
not ({QUERY})
!({QUERY})
```

**Beispiel**

Mit der folgenden Operation werden alle Personen, die ihr Heimatland nicht als Kanada haben, zurückgeschickt.

```sql
not (homeAddress.countryISO = "CA")
```

## If{#if}

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

Der folgende Vorgang setzt den Wert auf `1`, wenn das Heimatland Kanada ist, und `2`, wenn das Heimatland nicht Kanada ist.

```sql
if (homeAddress.countryISO = "CA", 1, 2)
```

## Gleich{#equals}

Die Funktion `=` (gleich) prüft, ob ein Wert oder Ausdruck gleich einem anderen Wert oder Ausdruck ist.

**Format**

```sql
{EXPRESSION} = {VALUE}
```

**Beispiel**

Der folgende Vorgang überprüft, ob sich das Land mit der Heimatadresse in Kanada befindet.

```sql
homeAddress.countryISO = "CA"
```

## Nicht gleich{#notequal}

Die Funktion `!=` (nicht gleich) prüft, ob ein Wert oder Ausdruck **nicht** einem anderen Wert oder Ausdruck entspricht.

**Format**

```sql
{EXPRESSION} != {VALUE}
```

**Beispiel**

Der folgende Vorgang überprüft, ob sich das Land der Heimatadresse nicht in Kanada befindet.

```sql
homeAddress.countryISO != "CA"
```

## Größer als{#greaterthan}

Mit der Funktion `>` (Größer als) wird überprüft, ob der erste Wert größer als der zweite ist.

**Format**

```sql
{EXPRESSION} > {EXPRESSION} 
```

**Beispiel**

Der folgende Vorgang definiert Personen, deren Geburtstage nicht im Januar oder Februar liegen.

```sql
person.birthMonth > 2
```

## Größer oder gleich{#greaterthanorequal}

Mit der Funktion `>=` (größer oder gleich) wird überprüft, ob der erste Wert größer oder gleich dem zweiten Wert ist.

**Format**

```sql
{EXPRESSION} >= {EXPRESSION} 
```

**Beispiel**

Der folgende Vorgang definiert Personen, deren Geburtstage nicht im Januar oder Februar liegen.

```sql
person.birthMonth >= 3
```

## Niedriger als{#lessthan}

Mit der Vergleichsfunktion `<` (less than) wird geprüft, ob der erste Wert kleiner als der zweite ist.

**Format**

```sql
{EXPRESSION} < {EXPRESSION} 
```

**Beispiel**

Der folgende Vorgang definiert Personen, deren Geburtstag im Januar liegt.

```sql
person.birthMonth < 2
```

## Kleiner oder gleich{#lessthanorequal}

Mit der Vergleichsfunktion `<=` (kleiner oder gleich) wird geprüft, ob der erste Wert kleiner oder gleich dem zweiten Wert ist.

**Format**

```sql
{EXPRESSION} <= {EXPRESSION} 
```

**Beispiel**

Der folgende Vorgang definiert Personen, deren Geburtstag im Januar oder Februar liegt.

```sql
person.birthMonth <= 2
```

## hinzufügen{#add}

Die Funktion `+` (Addition) wird verwendet, um die Summe von zwei Argument-Ausdrücken zu finden.

**Format**

```sql
{NUMBER} + {NUMBER}
```

**Beispiel**

Im Folgenden wird der Preis zweier verschiedener Produkte zusammengefasst.

```sql
product1.price + product2.price
```

## Multiplizieren{#multiply}

Die Funktion `*` (Multiplikation) wird verwendet, um das Produkt zweier Argument-Ausdruck zu finden.

**Format**

```sql
{NUMBER} * {NUMBER}
```

**Beispiel**

Das folgende Verfahren ermittelt das Produkt des Bestandes und den Preis eines Produkts, um den Bruttowert des Produkts zu ermitteln.

```sql
product.inventory * product.price
```

## Subtrahieren{#substract}

Die Funktion `-` (Subtraktion) wird verwendet, um den Unterschied von zwei Argument-Ausdrücken zu ermitteln.

**Format**

```sql
{NUMBER} - {NUMBER}
```

**Beispiel**

Im Folgenden wird der Preisunterschied zwischen zwei verschiedenen Produkten ermittelt.

```sql
product1.price - product2.price
```

## Dividieren{#divide}

Die Funktion `/` (Division) wird verwendet, um den Quotient zweier Argument-Ausdruck zu finden.

**Format**

```sql
{NUMBER} / {NUMBER}
```

**Beispiel**

Im Folgenden wird der Quotient zwischen den insgesamt verkauften Produkten und dem verdienten Gesamtgeld ermittelt, um die durchschnittlichen Kosten pro Artikel zu sehen.

```sql
totalProduct.price / totalProduct.sold
```

## Remainder{#remainder}

Die `%`-Funktion (Modulo/Rest) wird verwendet, um den Rest nach der Teilung der beiden Argument-Ausdruck zu finden.

**Format**

```sql
{NUMBER} % {NUMBER}
```

**Beispiel**

Der folgende Vorgang überprüft, ob das Alter der Person durch fünf teilbar ist.

```sql
person.age % 5 = 0
```
