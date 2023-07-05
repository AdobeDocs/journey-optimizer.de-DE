---
title: Bibliothek mit Array-Funktionen
description: Bibliothek mit Array-Funktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 100%

---

# Array- und Listenfunktionen {#arrays}

Verwenden Sie diese Funktionen, um die Interaktion mit Arrays, Listen und Zeichenfolgen zu vereinfachen.

## Nur Null zählen {#count-only-null}

Die Funktion `countOnlyNull` wird verwendet, um die Anzahl der Nullwerte in einer Liste zu zählen.

**Syntax**

```sql
{%= countOnlyNull(array) %}
```

**Beispiel**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Gibt 3 zurück.

## Mit Null zählen {#count-with-null}

Die Funktion `countWithNull` wird verwendet, um alle Elemente einer Liste einschließlich Nullwerten zu zählen.

**Syntax**

```sql
{%= countWithNull(array) %}
```

**Beispiel**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Gibt 6 zurück.

## Eindeutig{#distinct}

Die Funktion `distinct` wird verwendet, um Werte aus einem Array oder einer Liste abzurufen, aus denen doppelte Werte entfernt wurden.

**Syntax**

```sql
{%= distinct(array) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die Bestellungen in mehr als einem Geschäft aufgegeben haben.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Unterschiedliche Zählung mit Null {#distinct-count-with-null}

Die Funktion `distinctCountWithNull` wird verwendet, um die Anzahl verschiedener Werte in einer Liste einschließlich der Nullwerte zu zählen.

**Syntax**

```sql
{%= distinctCountWithNull(array) %}
```

**Beispiel**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Gibt 3 zurück.

## Erstes Element{#head}

Mit der Funktion `head` wird das erste Element im Array oder in der Liste zurückgegeben.

**Syntax**

```sql
{%= head(array) %}
```

**Beispiel**

Mit dem folgenden Vorgang wird die erste der fünf häufigsten Bestellungen mit dem höchsten Preis zurückgegeben. Weiterführende Informationen zur Funktion `topN` finden Sie im Abschnitt [Erste `n` in Array](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

## Erste `n` in Array {#first-n}

Die `topN`-Funktion gibt die ersten `N` Elemente in einem Array zurück, wenn sie anhand des angegebenen numerischen Ausdrucks in aufsteigender Reihenfolge sortiert werden.

**Syntax**

```sql
{%= topN(array, value, amount) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{ARRAY}` | Das zu sortierende Array oder die zu sortierende Liste. |
| `{VALUE}` | Die Eigenschaft, in der das Array oder die Liste sortiert werden soll. |
| `{AMOUNT}` | Die Zahl der zurückzugebenden Elemente. |

**Beispiel**

Mit dem folgenden Vorgang werden die ersten fünf Bestellungen mit dem niedrigsten Preis zurückgegeben.

```sql
{%= topN(orders,price, 5) %}
```

## Enthalten{#in}

Mit der `in`-Funktion wird bestimmt, ob ein Element einem Array oder einer Liste angehört.

**Syntax**

```sql
{%= in(value, array) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die im März, Juni oder September Geburtstag haben.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## Umfasst{#includes}

Mit der `includes`-Funktion wird bestimmt, ob ein Array oder eine Liste ein bestimmtes Element enthält.

**Syntax**

```sql
{%= includes(array,item) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, zu deren Lieblingsfarben Rot gehört.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## Schnittmengen{#intersects}

Mit der `intersects`-Funktion wird bestimmt, ob zwei Arrays oder Listen mindestens ein gemeinsames Element aufweisen.

**Syntax**

```sql
{%= intersects(array1, array2) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, deren Lieblingsfarben mindestens eine der folgenden Farben beinhalten: Rot, Blau oder Grün.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

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

**Syntax**

```sql
{%= bottomN(array, value, amount) %}
```

| Argument | Beschreibung |
| --------- | ----------- | 
| `{ARRAY}` | Das zu sortierende Array oder die zu sortierende Liste. |
| `{VALUE}` | Die Eigenschaft, in der das Array oder die Liste sortiert werden soll. |
| `{AMOUNT}` | Die Zahl der zurückzugebenden Elemente. |

**Beispiel**

Mit dem folgenden Vorgang werden die letzten fünf Bestellungen mit dem höchsten Preis zurückgegeben.

```sql
{%= bottomN(orders,price, 5) %}
```

## Nicht enthalten{#notin}

Mit der `notIn`-Funktion wird bestimmt, ob ein Element einem Array oder einer Liste nicht angehört.

>[!NOTE]
>
> Die `notIn`-Funktion stellt *außerdem* sicher, dass keiner der Werte null ist. Daher sind die Ergebnisse keine exakte Negation der `in`-Funktion.

**Syntax**

```sql
{%= notIn(value, array) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die nicht im März, Juni oder September Geburtstag haben.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Teilmenge von{#subset}

Mit der `subsetOf`-Funktion wird bestimmt, ob ein bestimmtes Array (Array A) eine Teilmenge eines anderen Arrays (Array B) ist. Mit anderen Worten: ob alle Elemente in Array A Elemente von Array B sind.

**Syntax**

```sql
{%= subsetOf(array1, array2) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die alle ihrer Lieblingsstädte besucht haben.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## Übergeordnete Gruppe von{#superset}

Mit der `supersetOf`-Funktion wird bestimmt, ob ein bestimmtes Array (Array A) eine Obermenge eines anderen Arrays (Array B) ist. Mit anderen Worten: ob Array A alle Elemente in Array B enthält.

**Syntax**

```sql
{%= supersetOf(array1, array2) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die mindestens einmal Sushi und mindestens einmal Pizza gegessen haben.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
