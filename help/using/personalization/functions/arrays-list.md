---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 4f097636e059c5d0676b0129cdbdb125e5ad9415
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 4%

---

# Arrays und Listen{#arrays}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) Angebot-Funktionen, um die Interaktion mit Arrays, Listen und Zeichenfolgen zu vereinfachen.

## In{#in}

Mit der Funktion `in` wird bestimmt, ob ein Element Mitglied eines Arrays oder einer Liste ist.

**Format**

```sql
in ({VALUE},{ARRAY})
```

**Beispiel**

Der folgende Vorgang definiert Personen mit Geburtstagen im März, Juni oder September.

```sql
in (person.birthMonth, [3, 6, 9])
```

## Nicht in{#notin}

Mit der Funktion `notIn` wird bestimmt, ob ein Element nicht Mitglied eines Arrays oder einer Liste ist.

>[!NOTE]
>
>Die Funktion `notIn` *auch* stellt sicher, dass keiner der Werte null ist. Daher handelt es sich bei den Ergebnissen nicht um eine exakte Negation der Funktion `in`.

**Format**

```sql
notIn ({VALUE},{ARRAY})
```

**Beispiel**

Der folgende Vorgang definiert Personen mit Geburtstagen, die nicht im März, Juni oder September leben.

```sql
{%=notIn(person.birthMonth ,[3, 6, 9])%}
```

## Überschneidungen{#intersects}

Mit der Funktion `intersects` wird bestimmt, ob zwei Arrays oder Listen mindestens ein gemeinsames Mitglied haben.

**Format**

```sql
intersects({ARRAY},{ARRAY})
```

**Beispiel**

Der folgende Vorgang definiert Personen, deren Lieblingsfarben mindestens eine Farbe Rot, Blau oder Grün enthalten.

```sql
{%=intersects(person.favoriteColors,["red", "blue", "green"])%}
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

## Untergruppe von{#subset}

Mit der Funktion `subsetOf` wird bestimmt, ob ein bestimmtes Array (Array A) eine Untergruppe eines anderen Arrays (Array B) ist. Anders ausgedrückt, dass alle Elemente im Array A Elemente des Arrays B sind.

**Format**

```sql
subsetOf({ARRAY},{ARRAY})
```

**Beispiel**

Die folgende Operation definiert Personen, die alle ihre Lieblingsstädte besucht haben.

```sql
{%=subsetOf(person.favoriteCities,person.visitedCities)%}
```

## Übersatz von{#superset}

Mit der Funktion `supersetOf` wird bestimmt, ob ein bestimmtes Array (Array A) eine Übermenge eines anderen Arrays (Array B) ist. Mit anderen Worten, dieses Array A enthält alle Elemente im Array B.

**Format**

```sql
supersetOf({ARRAY},{ARRAY})
```

**Beispiel**

Die folgende Operation definiert Personen, die mindestens einmal Sushi und Pizza gegessen haben.

```sql
{%=supersetOf(person.eatenFoods,["sushi", "pizza"]%}
```

## Umfasst{#includes}

Mit der Funktion `includes` wird bestimmt, ob ein Array oder eine Liste ein bestimmtes Element enthält.

**Format**

```sql
includes({ARRAY},{ITEM})
```

**Beispiel**

Der folgende Vorgang definiert Personen, deren Lieblingsfarbe Rot enthält.

```sql
{%=includes(person.favoriteColors,"red")%}
```

## Distinct{#distinct}

Mit der Funktion `distinct` werden Duplikat-Werte aus einem Array oder einer Liste entfernt.

**Format**

```sql
distinct({ARRAY})
```

**Beispiel**

Der folgende Vorgang gibt Personen an, die Bestellungen in mehr als einem Store aufgegeben haben.

```sql
{%=distinct(person.orders.storeId).count() > 1%}
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

Der folgende Vorgang gibt die fünf wichtigsten Bestellungen mit dem höchsten Preis zurück.

```sql
{%=topN(orders,price, 5)%}
```

## Letzte `n` in Array{#last-n}

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

Der folgende Vorgang gibt die fünf wichtigsten Bestellungen mit dem niedrigsten Preis zurück.

```sql
{%=bottomN(orders,price, 5)%
```

## Erster Eintrag{#head}

Mit der Funktion `head` wird das erste Element im Array oder in der Liste zurückgegeben.

**Format**

```sql
head({ARRAY})
```

**Beispiel**

Der folgende Vorgang gibt die erste der fünf wichtigsten Bestellungen mit dem höchsten Preis zurück. Weitere Informationen zur Funktion `topN` finden Sie im Abschnitt [first `n` im Array](#first-n).

```sql
{%=head(topN(orders,price, 5))%}
```
