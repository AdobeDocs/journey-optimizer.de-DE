---
title: Bibliothek mit Arrays-Funktionen
description: Bibliothek mit Arrays-Funktionen
feature: Personalisierung
topic: Personalisierung
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 66%

---

# Arrays und Listenfunktionen {#arrays}

![](../../assets/do-not-localize/badge.png)

Verwenden Sie diese Funktionen, um die Interaktion mit Arrays, Listen und Zeichenfolgen zu vereinfachen.

## Verschieden{#distinct}

Die Funktion `distinct` wird verwendet, um Werte aus einem Array oder einer Liste mit entfernten doppelten Werten abzurufen.

**Format**

```sql
{%= distinct(array) %}
```

**Beispiel**

Der folgende Vorgang gibt Personen an, die Bestellungen in mehr als einem Store aufgegeben haben.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Erstes Element{#head}

Mit der `head`-Funktion wird das erste Element im Array oder in der Liste zurückgegeben.

**Format**

```sql
{%= head({array}) %}
```

**Beispiel**

Der folgende Vorgang gibt die erste der fünf häufigsten Bestellungen mit dem höchsten Preis zurück. Weiterführende Informationen zur `topN`-Funktion finden Sie im Abschnitt [Erste `n` in Array](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

## Erste `n` in Array {#first-n}

Die `topN`-Funktion gibt die ersten `N` Elemente in einem Array zurück, wenn sie anhand des angegebenen numerischen Ausdrucks in aufsteigender Reihenfolge sortiert werden.

**Format**

```sql
{%= topN(array, value, amount) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{ARRAY}` | Das zu sortierende Array oder die zu sortierende Liste. |
| `{VALUE}` | Die Eigenschaft, in der das Array oder die Liste sortiert werden soll. |
| `{AMOUNT}` | Die Zahl der zurückzugebenden Elemente. |

**Beispiel**

Der folgende Vorgang gibt die fünf häufigsten Bestellungen mit dem höchsten Preis zurück.

```sql
{%= topN(orders,price, 5) %}
```

## Enthalten{#in}

Mit der `in`-Funktion wird bestimmt, ob ein Element einem Array oder einer Liste angehört.

**Format**

```sql
{%= in(value, array) %}
```

**Beispiel**

Der folgende Vorgang definiert Personen, die im März, Juni oder September Geburtstag haben.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## Enthält{#includes}

Mit der `includes`-Funktion wird bestimmt, ob ein Array oder eine Liste ein bestimmtes Element enthält.

**Format**

```sql
{%= includes(array,item) %}
```

**Beispiel**

Die folgende Operation definiert Personen, deren Lieblingsfarbe Rot enthält.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## Schnittmengen{#intersects}

Mit der `intersects`-Funktion wird bestimmt, ob zwei Arrays oder Listen mindestens ein gemeinsames Element aufweisen.

**Format**

```sql
{%= intersects(array1, array2) %}
```

**Beispiel**

Der folgende Vorgang definiert Personen, deren Lieblingsfarben mindestens eine der Farben Rot, Blau oder Grün enthalten.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Format**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## Letzte `n` in Array{#last-n}

Die `bottomN`-Funktion gibt die letzten `N` Elemente in einem Array zurück, wenn sie anhand des angegebenen numerischen Ausdrucks in aufsteigender Reihenfolge sortiert werden.

**Format**

```sql
{%= bottomN(array, value, amount) %}
```

| Argument | Beschreibung |
| --------- | ----------- | 
| `{ARRAY}` | Das zu sortierende Array oder die zu sortierende Liste. |
| `{VALUE}` | Die Eigenschaft, in der das Array oder die Liste sortiert werden soll. |
| `{AMOUNT}` | Die Zahl der zurückzugebenden Elemente. |

**Beispiel**

Der folgende Vorgang gibt die fünf häufigsten Bestellungen mit dem niedrigsten Preis zurück.

```sql
{%= bottomN(orders,price, 5) %}
```


## Nicht enthalten{#notin}

Mit der `notIn`-Funktion wird bestimmt, ob ein Element einem Array oder einer Liste nicht angehört.

>[!NOTE]
>
> Die `notIn`-Funktion stellt *außerdem* sicher, dass keiner der Werte null ist. Daher sind die Ergebnisse keine exakte Negation der `in`-Funktion.

**Format**

```sql
{%= notIn(value, array) %}
```

**Beispiel**

Der folgende Vorgang definiert Personen, die nicht im März, Juni oder September Geburtstag haben.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Teilmenge von{#subset}

Mit der `subsetOf`-Funktion wird bestimmt, ob ein bestimmtes Array (Array A) eine Teilmenge eines anderen Arrays (Array B) ist. Mit anderen Worten: ob alle Elemente in Array A Elemente von Array B sind.

**Format**

```sql
{%= subsetOf(array1, array2) %}
```

**Beispiel**

Im Folgenden werden Personen beschrieben, die alle ihrer Lieblingsstädte besucht haben.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## Obermenge{#superset}

Mit der `supersetOf`-Funktion wird bestimmt, ob ein bestimmtes Array (Array A) eine Obermenge eines anderen Arrays (Array B) ist. Mit anderen Worten: ob Array A alle Elemente in Array B enthält.

**Format**

```sql
{%= supersetOf(array1, array2) %}
```

**Beispiel**

Die folgende Operation definiert Personen, die mindestens einmal Sushi und Pizza gegessen haben.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```







