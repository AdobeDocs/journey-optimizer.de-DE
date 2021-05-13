---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 96%

---

# Arrays und Listen{#arrays}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) Angebot-Funktionen, um die Interaktion mit Arrays, Listen und Zeichenfolgen zu vereinfachen.

## Enthalten

Mit der `in`-Funktion wird bestimmt, ob ein Element einem Array oder einer Liste angehört.

**Format**

```sql
in ({VALUE},{ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, die im März, Juni oder September Geburtstag haben.

```sql
in (person.birthMonth, [3, 6, 9])
```

## Nicht enthalten

Mit der `notIn`-Funktion wird bestimmt, ob ein Element einem Array oder einer Liste nicht angehört.

>[!NOTE]
>
> Die `notIn`-Funktion stellt *außerdem* sicher, dass keiner der Werte null ist. Daher sind die Ergebnisse keine exakte Negation der `in`-Funktion.

**Format**

```sql
notIn ({VALUE},{ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, die nicht im März, Juni oder September Geburtstag haben.

```sql
notIn (person.birthMonth ,[3, 6, 9])
```

## Schnittmengen

Mit der `intersects`-Funktion wird bestimmt, ob zwei Arrays oder Listen mindestens ein gemeinsames Element aufweisen.

**Format**

```sql
intersects({ARRAY},{ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, deren Lieblingsfarben mindestens eine der folgenden Farben beinhalten: Rot, Blau oder Grün.

```sql
intersects(person.favoriteColors,["red", "blue", "green"])
```

## Schnittmenge

Die `intersection`-Funktion dient zur Bestimmung der gemeinsamen Elemente von zwei Arrays oder Listen.

**Format**

```sql
intersection({ARRAY},{ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage definiert, ob unter den Lieblingsfarben von Person 1 und auch Person 2 die Farben Rot, Blau und Grün sind.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```

## Teilmenge von

Mit der `subsetOf`-Funktion wird bestimmt, ob ein bestimmtes Array (Array A) eine Teilmenge eines anderen Arrays (Array B) ist. Mit anderen Worten: ob alle Elemente in Array A Elemente von Array B sind.

**Format**

```sql
subsetOf({ARRAY},{ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, die alle ihrer Lieblingsstädte besucht haben.

```sql
subsetOf(person.favoriteCities,person.visitedCities)
```

## Obermenge

Mit der `supersetOf`-Funktion wird bestimmt, ob ein bestimmtes Array (Array A) eine Obermenge eines anderen Arrays (Array B) ist. Mit anderen Worten: ob Array A alle Elemente in Array B enthält.

**Format**

```sql
supersetOf({ARRAY},{ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, die mindestens einmal Sushi und mindestens einmal Pizza gegessen haben.

```sql
supersetOf(person.eatenFoods,["sushi", "pizza"])
```

## Enthält

Mit der `includes`-Funktion wird bestimmt, ob ein Array oder eine Liste ein bestimmtes Element enthält.

**Format**

```sql
includes({ARRAY},{ITEM})
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, zu deren Lieblingsfarben Rot gehört.

```sql
includes(person.favoriteColors,"red")
```

## Verschieden

Die `distinct`-Funktion dient dazu, doppelt vorhandene Werte aus einem Array oder einer Liste zu entfernen.

**Format**

```sql
distinct({ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage definiert Personen, die Bestellungen in mehr als einem Geschäft aufgegeben haben.

```sql
distinct(person.orders.storeId).count() > 1
```

## Erste `n` in Array {#first-n}

Die `topN`-Funktion gibt die ersten `N` Elemente in einem Array zurück, wenn sie anhand des angegebenen numerischen Ausdrucks in aufsteigender Reihenfolge sortiert werden.

**Format**

```sql
topN({ARRAY},{VALUE}, {AMOUNT})
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{ARRAY}` | Das zu sortierende Array oder die zu sortierende Liste. |
| `{VALUE}` | Die Eigenschaft, in der das Array oder die Liste sortiert werden soll. |
| `{AMOUNT}` | Die Zahl der zurückzugebenden Elemente. |

**Beispiel**

Die folgende PQL-Abfrage gibt die fünf häufigsten Bestellungen mit dem höchsten Preis zurück.

```sql
topN(orders,price, 5)
```

## Letzte `n` in Array

Die `bottomN`-Funktion gibt die letzten `N` Elemente in einem Array zurück, wenn sie anhand des angegebenen numerischen Ausdrucks in aufsteigender Reihenfolge sortiert werden.

**Format**

```sql
bottomN({ARRAY},{VALUE}, {AMOUNT})
```

| Argument | Beschreibung |
| --------- | ----------- | 
| `{ARRAY}` | Das zu sortierende Array oder die zu sortierende Liste. |
| `{VALUE}` | Die Eigenschaft, in der das Array oder die Liste sortiert werden soll. |
| `{AMOUNT}` | Die Zahl der zurückzugebenden Elemente. |

**Beispiel**

Die folgende PQL-Abfrage gibt die fünf häufigsten Bestellungen mit dem niedrigsten Preis zurück.

```sql
bottomN(orders,price, 5)
```

## Erstes Element

Mit der `head`-Funktion wird das erste Element im Array oder in der Liste zurückgegeben.

**Format**

```sql
head({ARRAY})
```

**Beispiel**

Die folgende PQL-Abfrage gibt die erste der fünf häufigsten Bestellungen mit dem höchsten Preis zurück. Weiterführende Informationen zur `topN`-Funktion finden Sie im Abschnitt [Erste `n` in Array](#first-n).

```sql
head(topN(orders,price, 5))
```
