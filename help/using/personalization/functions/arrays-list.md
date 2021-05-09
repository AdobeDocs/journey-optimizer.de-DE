---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 0%

---

# Arrays und Listen{#arrays}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) Angebot-Funktionen, um die Interaktion mit Arrays, Listen und Zeichenfolgen zu vereinfachen.

## In

Mit der Funktion `in` wird bestimmt, ob ein Element Mitglied eines Arrays oder einer Liste ist.

**Format**

```sql
in ({VALUE},{ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen mit Geburtstagen im März, Juni oder September.

```sql
in (person.birthMonth, [3, 6, 9])
```

## Not in

Mit der Funktion `notIn` wird bestimmt, ob ein Element nicht Mitglied eines Arrays oder einer Liste ist.

>[!NOTE]
>
>Die Funktion `notIn` *auch* stellt sicher, dass keiner der Werte null ist. Daher handelt es sich bei den Ergebnissen nicht um eine exakte Negation der Funktion `in`.

**Format**

```sql
notIn ({VALUE},{ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen mit Geburtstagen, die nicht im März, Juni oder September leben.

```sql
notIn (person.birthMonth ,[3, 6, 9])
```

## Intersekten

Mit der Funktion `intersects` wird bestimmt, ob zwei Arrays oder Listen mindestens ein gemeinsames Mitglied haben.

**Format**

```sql
intersects({ARRAY},{ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, deren Lieblingsfarben mindestens eine Farbe Rot, Blau oder Grün enthalten.

```sql
intersects(person.favoriteColors,["red", "blue", "green"])
```

## Schnittmenge

Die `intersection`-Funktion wird verwendet, um die gemeinsamen Mitglieder von zwei Arrays oder Listen zu bestimmen.

**Format**

```sql
intersection({ARRAY},{ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage definiert, ob die Farben Rot, Blau und Grün von Person 1 und Person 2 jeweils am liebsten sind.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```

## Untergruppe von

Mit der Funktion `subsetOf` wird bestimmt, ob ein bestimmtes Array (Array A) eine Untergruppe eines anderen Arrays (Array B) ist. Anders ausgedrückt, dass alle Elemente im Array A Elemente des Arrays B sind.

**Format**

```sql
subsetOf({ARRAY},{ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, die alle ihre Lieblingsstädte besucht haben.

```sql
subsetOf(person.favoriteCities,person.visitedCities)
```

## Superset

Mit der Funktion `supersetOf` wird bestimmt, ob ein bestimmtes Array (Array A) eine Übermenge eines anderen Arrays (Array B) ist. Mit anderen Worten, dieses Array A enthält alle Elemente im Array B.

**Format**

```sql
supersetOf({ARRAY},{ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, die mindestens einmal Sushi und Pizza gegessen haben.

```sql
supersetOf(person.eatenFoods,["sushi", "pizza"])
```

## Enthält

Mit der Funktion `includes` wird bestimmt, ob ein Array oder eine Liste ein bestimmtes Element enthält.

**Format**

```sql
includes({ARRAY},{ITEM})
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, deren Lieblingsfarbe Rot enthält.

```sql
includes(person.favoriteColors,"red")
```

## Unterscheiden

Mit der Funktion `distinct` werden Duplikat-Werte aus einem Array oder einer Liste entfernt.

**Format**

```sql
distinct({ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage gibt Personen an, die Bestellungen in mehr als einem Store aufgegeben haben.

```sql
distinct(person.orders.storeId).count() > 1
```

## First `n` in array {#first-n}

Die Funktion `topN` gibt die ersten `N` Elemente in einem Array zurück, wenn sie in aufsteigender Reihenfolge nach dem angegebenen numerischen Ausdruck sortiert werden.

**Format**

```sql
topN({ARRAY},{VALUE}, {AMOUNT})
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{ARRAY}` | Das zu sortierende Array oder die zu sortierende Liste. |
| `{VALUE}` | Die Eigenschaft, in der das Array oder die Liste sortiert werden soll. |
| `{AMOUNT}` | Die Anzahl der zurückzugebenden Elemente. |

**Beispiel**

Die folgende PQL-Abfrage gibt die fünf wichtigsten Bestellungen mit dem höchsten Preis zurück.

```sql
topN(orders,price, 5)
```

## Letztes `n` im Array

Die Funktion `bottomN` gibt die letzten `N` Elemente in einem Array zurück, wenn sie in aufsteigender Reihenfolge nach dem angegebenen numerischen Ausdruck sortiert werden.

**Format**

```sql
bottomN({ARRAY},{VALUE}, {AMOUNT})
```

| Argument | Beschreibung |
| --------- | ----------- | 
| `{ARRAY}` | Das zu sortierende Array oder die zu sortierende Liste. |
| `{VALUE}` | Die Eigenschaft, in der das Array oder die Liste sortiert werden soll. |
| `{AMOUNT}` | Die Anzahl der zurückzugebenden Elemente. |

**Beispiel**

Die folgende PQL-Abfrage gibt die fünf wichtigsten Bestellungen mit dem niedrigsten Preis zurück.

```sql
bottomN(orders,price, 5)
```

## Erster Posten

Mit der Funktion `head` wird das erste Element im Array oder in der Liste zurückgegeben.

**Format**

```sql
head({ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage gibt die erste der fünf Top-Bestellungen mit dem höchsten Preis zurück. Weitere Informationen zur Funktion `topN` finden Sie im Abschnitt [first `n` im Array](#first-n).

```sql
head(topN(orders,price, 5))
```
