---
title: Bibliothek mit Array-Funktionen
description: Bibliothek mit Array-Funktionen
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
TQID: https://experienceleague.adobe.com/CUiT5GFH9o4q-oOSWuKC8ZyLbRbH9lj88M92LhMIX9E
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: c5ecc28ec44a9c608f4fe5011e061cad62d92e2b
workflow-type: tm+mt
source-wordcount: 742
ht-degree: 0%

---

# Arrays und Listenfunktionen {#arrays}

Verwenden Sie diese Funktionen, um die Interaktion mit Arrays, Listen und Zeichenfolgen zu erleichtern.

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

## Unterschiedlich{#distinct}

Die Funktion `distinct` wird verwendet, um Werte aus einem Array oder einer Liste abzurufen, aus denen doppelte Werte entfernt wurden.

**Syntax**

```sql
{%= distinct(array) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen angegeben, die Bestellungen in mehr als einem Geschäft aufgegeben haben.

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

Mit dem folgenden Vorgang wird die erste der fünf häufigsten Bestellungen mit dem höchsten Preis zurückgegeben. Weitere Informationen zur Funktion `topN` finden Sie im Abschnitt [Erste `n` im Array](#first-n) .

```sql
{%= head(topN(orders,price, 5)) %}
```

## Sortieren und Abrufen der ersten N in Array {#first-n}

Die Funktion `topN` sortiert ein Array in absteigender Reihenfolge basierend auf dem angegebenen numerischen Ausdruck und gibt die ersten `N` Elemente zurück. Wenn die Array-Größe kleiner als `N` ist, wird das gesamte sortierte Array zurückgegeben.

Diese Funktion
**Syntax**

```sql
{%= topN(array, value, amount) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{ARRAY}` | Das Array oder die Liste, das bzw. die sortiert werden soll. |
| `{VALUE}` | Die Eigenschaft, in der das Array oder die Liste sortiert werden soll. |
| `{AMOUNT}` | Die Anzahl der zurückzugebenden Elemente. |

**Beispiel**

Mit dem folgenden Vorgang werden die ersten fünf Bestellungen mit dem niedrigsten Preis zurückgegeben.

```sql
{%= topN(orders,price, 5) %}
```

## in{#in}

Mit der Funktion `in` wird bestimmt, ob ein Element Mitglied eines Arrays oder einer Liste ist.

**Syntax**

```sql
{%= in(value, array) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die im März, Juni oder September Geburtstag haben.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## Beinhaltet{#includes}

Mit der Funktion `includes` wird bestimmt, ob ein Array oder eine Liste ein bestimmtes Element enthält.

**Syntax**

```sql
{%= includes(array,item) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, zu deren Lieblingsfarben Rot gehört.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## Überschneidet{#intersects}

Mit der Funktion `intersects` wird bestimmt, ob zwei Arrays oder Listen mindestens ein gemeinsames Element aufweisen.

**Syntax**

```sql
{%= intersects(array1, array2) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, deren Lieblingsfarben mindestens eine der folgenden Farben umfassen: Rot, Blau oder Grün.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!--
## Intersection{#intersection}

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

## Sortieren und Letzte N in Array abrufen {#last-n}

Die Funktion `bottomN` sortiert ein Array in aufsteigender Reihenfolge basierend auf dem angegebenen numerischen Ausdruck und gibt die ersten `N` Elemente zurück. Wenn die Array-Größe kleiner als `N` ist, wird das gesamte sortierte Array zurückgegeben.

**Syntax**

```sql
{%= bottomN(array, value, amount) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{ARRAY}` | Das Array oder die Liste, das bzw. die sortiert werden soll. |
| `{VALUE}` | Die Eigenschaft, in der das Array oder die Liste sortiert werden soll. |
| `{AMOUNT}` | Die Anzahl der zurückzugebenden Elemente. |

**Beispiel**

Mit dem folgenden Vorgang werden die letzten fünf Bestellungen mit dem höchsten Preis zurückgegeben.

```sql
{%= bottomN(orders,price, 5) %}
```

## Nicht in{#notin}

Mit der Funktion `notIn` wird bestimmt, ob ein Element nicht Mitglied eines Arrays oder einer Liste ist.

>[!NOTE]
>
>Die `notIn`-Funktion *auch* stellt sicher, dass keiner der Werte null ist. Daher sind die Ergebnisse keine exakte Negation der `in`.

**Syntax**

```sql
{%= notIn(value, array) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die nicht im März, Juni oder September Geburtstag haben.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Untergruppe von{#subset}

Mit der Funktion `subsetOf` wird bestimmt, ob ein bestimmtes Array (Array A) eine Teilmenge eines anderen Arrays (Array B) ist. Mit anderen Worten, dass alle Elemente in Array A Elemente von Array B sind.

**Syntax**

```sql
{%= subsetOf(array1, array2) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die alle ihre Lieblingsstädte besucht haben.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## Obermenge von{#superset}

Mit der Funktion `supersetOf` wird bestimmt, ob ein bestimmtes Array (Array A) eine Obermenge eines anderen Arrays (Array B) ist. Mit anderen Worten: Array A enthält alle Elemente in Array B.

**Syntax**

```sql
{%= supersetOf(array1, array2) %}
```

**Beispiel**

Mit dem folgenden Vorgang werden Personen definiert, die mindestens einmal Sushi und Pizza gegessen haben.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

## Iteration über ein Array {#each-loop}

Verwenden Sie den Handlebars-`{{#each}}`-Block-Helper, um ein Array zu durchlaufen und Inhalte für jedes Element in **personalisierten Inhalt“ (E-**, SMS, Push) zu rendern.

>[!NOTE]
>
>`{{#each}}` ist nur im **Personalisierungseditor)** E-Mail-Textkörper, SMS, Push-Inhalt). Sie **in** Aktivität Journey-Bedingung nicht unterstützt. Um Elemente aus einem Array innerhalb einer Journey-Bedingung zu filtern oder zuzuordnen, verwenden Sie stattdessen [Sammlungsverwaltungsfunktionen](../../building-journeys/expression/collection-management-functions.md).

**Syntax**

```handlebars
{{#each arrayAttribute}}
  {{this}}
{{/each}}
```

+++Beispiel - Listet alle Elemente in einem Array auf

```handlebars
{{#each profile.purchases.items}}
  - {{this.name}}: {{this.price}}€
{{/each}}
```

Ausgabe (Beispiel):

```
- Running shoes: 89€
- Water bottle: 15€
- Gym bag: 45€
```

+++

+++Beispiel - Zugriff auf den Schleifenindex

Verwenden Sie `@index`, um auf die aktuelle Schleifenposition zuzugreifen (0-basiert):

```handlebars
{{#each profile.preferences.languages}}
  {{@index}}: {{this}}
{{/each}}
```

Ausgabe (Beispiel):

```
0: English
1: French
2: Spanish
```

+++

+++Beispiel - Bedingtes Rendering in einer Schleife

Verwenden Sie den `{%#if%}`-Block innerhalb von `{{#each}}`, um Inhalte nur dann zu rendern, wenn eine Bedingung erfüllt ist:

>[!NOTE]
>
>`{% if %}`/`{% endif %}` werden nicht unterstützt. Verwenden Sie stattdessen `{%#if%}`/`{%/if%}`. Außerdem funktioniert `this.<field>` nicht in PQL-Bedingungsausdrücken - referenzieren Sie das Feld direkt mithilfe des Attributnamens (z. B. `order.status`).

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Your order {{order.id}} is still pending.
  {%/if%}
{{/each}}
```

Dies ist das empfohlene Muster, um einen „Bruch unter Bedingung“ zu simulieren - nur die Elemente, die der Bedingung entsprechen, erzeugen eine Ausgabe.

+++
