---
title: Bibliothek mit Arrays-Funktionen
description: Bibliothek mit Arrays-Funktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 0%

---

# Arrays und Listenfunktionen {#arrays}

Verwenden Sie diese Funktionen, um die Interaktion mit Arrays, Listen und Zeichenfolgen zu vereinfachen.

## Nur null zählen {#count-only-null}

Die `countOnlyNull` -Funktion verwendet wird, um die Anzahl der Nullwerte in einer Liste zu zählen.

**Format**

```sql
{%= countOnlyNull(array) %}
```

**Beispiel**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Gibt 3 zurück.

## Zählung mit Null {#count-with-null}

Die `countWithNull` -Funktion wird verwendet, um alle Elemente einer Liste einschließlich Nullwerten zu zählen.

**Format**

```sql
{%= countWithNull(array) %}
```

**Beispiel**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Gibt 6 zurück.

## Unterschiedlich{#distinct}

Die `distinct` -Funktion verwendet, um Werte aus einem Array oder einer Liste mit entfernten doppelten Werten abzurufen.

**Format**

```sql
{%= distinct(array) %}
```

**Beispiel**

Der folgende Vorgang gibt Personen an, die Bestellungen in mehr als einem Store aufgegeben haben.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Zählung unterschiedlicher Werte mit Null {#distinct-count-with-null}

Die `distinctCountWithNull` -Funktion wird verwendet, um die Anzahl verschiedener Werte in einer Liste einschließlich der Nullwerte zu zählen.

**Format**

```sql
{%= distinctCountWithNull(array) %}
```

**Beispiel**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Gibt 3 zurück.

## Erstes Element{#head}

Die `head` -Funktion wird verwendet, um das erste Element in einem Array oder einer Liste zurückzugeben.

**Format**

```sql
{%= head(array) %}
```

**Beispiel**

Der folgende Vorgang gibt die erste der fünf häufigsten Bestellungen mit dem höchsten Preis zurück. Weitere Informationen zu `topN` -Funktion finden Sie im Abschnitt [first `n` in Array](#first-n) Abschnitt.

```sql
{%= head(topN(orders,price, 5)) %}
```

## Erste `n` in Array {#first-n}

Die `topN` -Funktion wird verwendet, um die erste `N` Elemente in einem Array, wenn sie anhand des angegebenen numerischen Ausdrucks in aufsteigender Reihenfolge sortiert werden.

**Format**

```sql
{%= topN(array, value, amount) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{ARRAY}` | Das zu sortierende Array oder die zu sortierende Liste. |
| `{VALUE}` | Die Eigenschaft, in der das Array oder die Liste sortiert werden soll. |
| `{AMOUNT}` | Die Anzahl der zurückzugebenden Elemente. |

**Beispiel**

Der folgende Vorgang gibt die fünf häufigsten Bestellungen mit dem höchsten Preis zurück.

```sql
{%= topN(orders,price, 5) %}
```

## In{#in}

Die `in` -Funktion wird verwendet, um zu bestimmen, ob ein Element einem Array oder einer Liste angehört.

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

Die `includes` -Funktion wird verwendet, um zu bestimmen, ob ein Array oder eine Liste ein bestimmtes Element enthält.

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

Die `intersects` -Funktion wird verwendet, um zu bestimmen, ob zwei Arrays oder Listen mindestens ein gemeinsames Element aufweisen.

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

Die `bottomN` -Funktion wird verwendet, um die letzte `N` Elemente in einem Array, wenn sie anhand des angegebenen numerischen Ausdrucks in aufsteigender Reihenfolge sortiert werden.

**Format**

```sql
{%= bottomN(array, value, amount) %}
```

| Argument | Beschreibung |
| --------- | ----------- | 
| `{ARRAY}` | Das zu sortierende Array oder die zu sortierende Liste. |
| `{VALUE}` | Die Eigenschaft, in der das Array oder die Liste sortiert werden soll. |
| `{AMOUNT}` | Die Anzahl der zurückzugebenden Elemente. |

**Beispiel**

Der folgende Vorgang gibt die fünf häufigsten Bestellungen mit dem niedrigsten Preis zurück.

```sql
{%= bottomN(orders,price, 5) %}
```

## Nicht enthalten{#notin}

Die `notIn` -Funktion wird verwendet, um zu bestimmen, ob ein Element nicht Mitglied eines Arrays oder einer Liste ist.

>[!NOTE]
>
>Die `notIn` function *auch* stellt sicher, dass keiner der Werte null ist. Daher stellen die Ergebnisse keine exakte Negation der `in` -Funktion.

**Format**

```sql
{%= notIn(value, array) %}
```

**Beispiel**

Der folgende Vorgang definiert Personen, die nicht im März, Juni oder September Geburtstag haben.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Untergruppe von{#subset}

Die `subsetOf` -Funktion wird verwendet, um zu bestimmen, ob ein bestimmtes Array (Array A) eine Teilmenge eines anderen Arrays (Array B) ist. Anders ausgedrückt: Alle Elemente in Array A sind Elemente des Arrays B.

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

Die `supersetOf` -Funktion wird verwendet, um zu bestimmen, ob ein bestimmtes Array (Array A) eine Obermenge eines anderen Arrays (Array B) ist. Mit anderen Worten, dieses Array A enthält alle Elemente in Array B.

**Format**

```sql
{%= supersetOf(array1, array2) %}
```

**Beispiel**

Die folgende Operation definiert Personen, die mindestens einmal Sushi und Pizza gegessen haben.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
