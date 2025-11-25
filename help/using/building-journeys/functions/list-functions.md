---
product: journey optimizer
title: Listenfunktionen
description: Informationen zu Listenfunktionen
feature: Journeys
role: Developer
level: Experienced
keywords: Liste, Funktionen, Ausdruck, Journey, Array, Sammlung
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: ht
source-wordcount: '1158'
ht-degree: 100%

---

# Listenfunktionen {#list-functions}

Mit Listenfunktionen können Sie Sammlungen von Werten in Ihren Journey-Ausdrücken bearbeiten und verwenden. Diese Funktionen sind für das Filtern, Sortieren, Umwandeln und Analysieren von Arrays und Listen in Ihren Customer Journeys unerlässlich.

Verwenden Sie Listenfunktionen, wenn Sie Folgendes tun müssen:

* Filtern und Extrahieren bestimmter Elemente aus Sammlungen anhand von Kriterien ([filter](#filter), [getListItem](#getListItem))
* Sortieren und Organisieren von Listenelementen in auf- oder absteigender Reihenfolge ([sort](#sort))
* Entfernen von Duplikaten und Abrufen eindeutiger Werte aus Listen ([distinct](#distinct), [distinctWithNull](#distinctWithNull))
* Überprüfen, ob Werte in Sammlungen vorhanden sind ([in](#in))
* Begrenzen der Anzahl der aus einer Liste zurückgegebenen Elemente ([limit](#limit))
* Abrufen der Größe einer Liste ([listSize](#listSize)) oder Umwandeln von Listen in verschiedene Formate ([serializeList](#serializeList))
* Durchführen bestimmter Vorgänge wie das Suchen nach gemeinsamen Elementen verschiedener Listen ([intersect](#intersect))

Listenfunktionen bieten leistungsstarke Tools für die Arbeit mit komplexen Datenstrukturen und ermöglichen so eine ausgefeilte Datenbearbeitung und Bedingungslogik basierend auf Sammlungsinhalten.

## distinct {#distinct}

Gibt die unterschiedlichen Werte oder Objekte einer angegebenen Liste zurück. Einträge mit Null werden ignoriert.

+++Syntax

`distinct(<parameters>)`

+++

+++Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly oder listObject | Zu verarbeitende Liste. Bei listObject muss es sich um einen Feldverweis handeln. |
| keyAttributeName | Zeichenfolge | Dieser Parameter ist optional und nur für listObject. Wenn der Parameter nicht angegeben wird, wird ein Objekt als doppelt betrachtet, wenn alle Attribute dieselben Werte aufweisen. Andernfalls wird ein Objekt als doppelt betrachtet, wenn das angegebene Attribut denselben Wert aufweist. |

+++

+++Signaturen und zurückgegebene Typen

`distinct(<listInteger>)`

Gibt eine Liste mit Ganzzahlen zurück.

`distinct(<listDecimal>)`

Gibt eine Liste mit Dezimalzahlen zurück.

`distinct(<listString>)`

Gibt eine Liste mit Zeichenfolgen zurück.

`distinct(<listDateTimeOnly>)`

Gibt eine Liste mit Datum/Uhrzeit-Werten ohne Berücksichtigung der Zeitzone zurück.

`distinct(<listDateTime>)`

Gibt eine Liste mit Datum/Uhrzeit-Werten zurück.

`distinct(<listDateOnly>)`

Gibt eine Liste mit Datumsangaben zurück.

`distinct(<listBoolean>)`

Gibt eine Liste mit booleschen Werten zurück.

`distinct(<listDuration>)`

Gibt eine Liste der Dauer zurück.

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

Gibt eine Liste mit Objekten zurück.

+++

+++Beispiele

`distinct([10,2,10,null])`

Gibt `[10, 2]` zurück.

+++

## distinctWithNull {#distinctWithNull}

Gibt die unterschiedlichen Werte oder Objekte einer angegebenen Liste zurück. Wenn die Liste mindestens einen Nullwert enthält, wird ein Nullwert in der zurückgegebenen Liste angezeigt.

+++Syntax

`distinctWithNull(<parameters>)`

+++

+++Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Zu verarbeitende Liste. |

+++

+++Signaturen und zurückgegebene Typen

`distinctWithNull(<listInteger>)`

Gibt eine Liste mit Ganzzahlen zurück.

`distinctWithNull(<listDecimal>)`

Gibt eine Liste mit Dezimalzahlen zurück.

`distinctWithNull(<listString>)`

Gibt eine Liste mit Zeichenfolgen zurück.

`distinctWithNull(<listDateTimeOnly>)`

Gibt eine Liste mit Datum/Uhrzeit-Werten ohne Berücksichtigung der Zeitzone zurück.

`distinctWithNull(<listDateTime>)`

Gibt eine Liste mit Datum/Uhrzeit-Werten zurück.

`distinctWithNull(<listDateOnly>)`

Gibt eine Liste mit Datumsangaben zurück.

`distinctWithNull(<listBoolean>)`

Gibt eine Liste mit booleschen Werten zurück.

`distinctWithNull(<listDuration>)`

Gibt eine Liste der Dauer zurück.

+++

+++Beispiele

`distinctWithNull([10,2,10,null])`

Gibt [10, 2, null] zurück.

+++

**Hinweis:** Der Parameter `<listObject>` wird in dieser Funktion nicht unterstützt.

## filter {#filter}

Gibt ein listObject mit Objekten zurück, deren Schlüsselattribut einem der angegebenen Schlüsselwerte entspricht.

+++Syntax

`filter(<parameters>)`

+++

+++Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToFilter | listObject | Liste der zu filternden Objekte. Muss ein Feldverweis sein. |
| keyAttributeName | Zeichenfolge | Attributname in den Objekten der angegebenen Liste, der als Schlüssel zum Filtern verwendet wird |
| keyValueList | list | Schlüsselwerte für die Filterung |

+++

+++Signaturen und zurückgegebene Typen

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

Gibt ein listObject zurück.

+++

+++Beispiele

Hier ist ein Beispiel für eine Payload, die in einem eingehenden Ereignis „myevent“ übergeben wird:

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

Sie können den folgenden Ausdruck verwenden:

```json
filter(
 @event{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

Gibt ein listObject mit den beiden Objekten „product2“ und „product3“ als ID zurück.

+++

## getListItem {#getListItem}

Gibt das Element der Liste am angegebenen Index zurück.

+++Syntax

`getListItem(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| index | integer |

+++

+++Signaturen und zurückgegebener Typ

`getListItem(<listInteger>,<index>)`

Gibt eine Ganzzahl zurück.

`getListItem(<listDecimal>,<index>)`

Gibt eine Dezimalzahl zurück.

`getListItem(<listString>,<index>)`

Gibt eine Zeichenfolge zurück.

`getListItem(<listDateTimeOnly>,<index>)`

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

`getListItem(<listDateTime>,<index>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

`getListItem(<listDateOnly>,<index>)`

Gibt eine Liste mit Datumsangaben zurück.

`getListItem(<listBoolean>,<index>)`

Gibt einen booleschen Wert zurück.

`getListItem(<listDuration>,<index>)`

Gibt eine Dauer zurück.

+++

+++Beispiele

`getListItem([10, 2, 3], 1)`

Gibt „2“ zurück

`getListItem(["A", "B", "C"], 2)`

Gibt „C“ zurück

Beispiele mit dem Ereignisfeld „event.appVersion“ mit dem Wert: 20.45.2.3434

`split(@event{event.appVersion}, "\\.")`

Gibt `["20", "45", "2", "3434"]` zurück

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

Gibt „20“ zurück

+++

## in {#in}

Überprüft, ob sich der erste Argumentwert in der Liste befindet. Die Prüfung wird mithilfe eines Gleichzeichens für jeden Argumentwert durchgeführt. Gibt „true“ zurück, wenn der Argumentwert gefunden wurde, andernfalls „false“.

Der Typ von `<expression>` muss mit Elementen der Liste übereinstimmen. Zur Erinnerung: Typen von Elementen in der Liste müssen miteinander übereinstimmen.

+++Syntax

`in(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| Zeichenfolge | Zeichenfolge |
| Boolesch | Boolesch |
| Ganzzahl | Ganzzahl |
| Dezimal | Dezimal |
| Dauer | Dauer |
| DateTime | DateTime |
| DateTimeOnly | DateTimeOnly |
| Liste | listString |
| Liste | listBoolean |
| Liste | listInteger |
| Liste | listDecimal |
| Liste | listDuration |
| Liste | listDateTime |
| Liste | listDateTimeOnly |
| Liste | listDateOnly |

+++

+++Signatur und zurückgegebener Typ

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

Geben einen booleschen Wert zurück.

+++

+++Beispiele

`in(4,[4,5,3,4])`

Gibt „true“ zurück.

`in(8,[4,5,3,4])`

Gibt „false“ zurück.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`

+++

## intersect {#intersect}

Gibt die gemeinsamen Werte in den beiden Eingabe-Listen zurück. Wenn eine der beiden Listen null ist, wird eine leere Liste zurückgegeben.

+++Syntax

`intersect(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| Liste 1 | Liste |
| Liste 2 | Liste  |

+++

+++Signaturen und zurückgegebene Typen

`intersect(listString,listString)`: listString

`intersect(listDecimal,listDecimal)`: listDecimal

`intersect(listInteger,listInteger)`: listInteger

`intersect(listDateTime,listDateTime)`: listDateTime

`intersect(listDateTimeOnly,listDateTimeOnly)`: listDateTimeOnly

`intersect(listDateOnly,listDateOnly)`: listDateOnly

`intersect(listDuration,listDuration)`: listDuration

`intersect(listBoolean,listBoolean)`: listBoolean

Gibt eine Liste zurück.

+++

+++Beispiele

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

Gibt [&quot;sports&quot;, &quot;news&quot; zurück]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "documentary"]
)
```

Gibt häufige Elemente zwischen Profil-Attributen und der angegebenen Liste von Kategorien zurück.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

Gibt häufige Elemente zwischen Profil-Attributen und angegebenem Ereignis-Feld zurück.

+++

## limit {#limit}

Gibt die ersten oder letzten n Elemente einer Liste zurück.

+++Syntax

`limit(<parameters>)`

+++

+++Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly oder listObject | Zu berücksichtigende Liste.  Bei listObject muss es sich um einen Feldverweis handeln. |
| numberOfItems | integer | Anzahl der aus der angegebenen Liste zurückzugebenden Elemente. |
| firstOrLastItems | Boolescher Wert | Dieser Parameter ist optional (standardmäßig „true“). „True“ gibt die ersten Elemente zurück. „False“ gibt die letzten Elemente zurück. |

+++

+++Signatur und zurückgegebener Typ

`limit(<listString>,<integer>)`

`limit(<listString>,<integer>,<boolean>)`

Gibt eine Liste mit Zeichenfolgen zurück.

`limit(<listInteger>,<integer>)`

`limit(<listInteger>,<integer>,<boolean>)`

Gibt eine Liste mit Ganzzahlen zurück.

`limit(<listDecimal>,<integer>)`

`limit(<listDecimal>,<integer>,<boolean>)`

Gibt eine Liste mit Dezimalzahlen zurück.

`limit(<listBoolean>,<integer>)`

`limit(<listBoolean>,<integer>,<boolean>)`

Gibt eine Liste mit booleschen Werten zurück.

`limit(<listDateOnly>,<integer>)`

`limit(<listDateOnly>,<integer>,<boolean>)`

Gibt eine Liste mit Datumsangaben zurück.

`limit(<listDateTimeOnly>,<integer>)`

`limit(<listDateTimeOnly>,<integer>,<boolean>)`

Gibt eine Liste mit Datum/Uhrzeit-Werten ohne Berücksichtigung der Zeitzone zurück.

`limit(<listDateTime>,integer>)`

`limit(<listDateTime>,<integer>,<boolean>)`

Gibt eine Liste mit Datum/Uhrzeit-Werten zurück.

`limit(<listDuration>,<integer>)`

`limit(<listDuration>,<integer>,<boolean>)`

Gibt eine Liste der Dauer zurück.

`limit(<listObject>,<integer>)`

`limit(<listObject>,<integer>,<boolean>)`

Gibt eine Liste mit Objekten zurück.

+++

+++Beispiele

`limit(["A", "B", "C", "D", "E"], 3)`

Gibt `["A","B","C"]` zurück.

`limit(["A", "B", "C", "D", "E"], 3, false)`

Gibt `["C","D","E"]` zurück.

+++

## listSize {#listSize}

Zählt die Anzahl der Elemente in der Liste.

+++Syntax

`listSize(<parameters>)`

+++

+++Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly oder listObject | Zu verarbeitende Liste. Bei listObject muss es sich um einen Feldverweis handeln. Ein listObject kann kein Null-Objekt enthalten. |

+++

+++Signaturen und zurückgegebener Typ

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

Gibt eine Ganzzahl zurück.

`listSize(<listObject>)`

+++

+++Beispiele

`listSize([10,2,3])`

Gibt 3 zurück.

`listSize(@event{my_event.productListItems})`

Gibt die Anzahl der Objekte im angegebenen Array von Objekten zurück (listObject-Typ).

+++

## serializeList {#serializeList}

Konvertiert eine angegebene Liste (alle Typen außer listObject) in eine Zeichenfolge.

+++Syntax

`serializeList(<parameters>)`

+++

+++Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Liste zur Konvertierung in eine Zeichenfolge. |
| Trennzeichen | Zeichenfolge | Trennzeichen zwischen den einzelnen Listenelementen in der Ausgabezeichenfolge. |
| addQuotes | Boolescher Wert | Dieser Parameter gibt an, ob jedes Element der Ausgabezeichenfolge Anführungszeichen enthalten soll (true) oder nicht (false). |

+++

+++Signatur und zurückgegebener Typ

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

Gibt eine Zeichenfolge zurück.

+++

+++Beispiele

`serializeList(["Hello","World"], " ", false)`

Gibt „Hello World“ zurück.

`serializeList(["Hello", "World"], ",", true)`

Gibt „&quot;Hello&quot;,&quot;World&quot;“ zurück.

+++

## sort {#sort}

Sortiert eine Liste von Werten oder Objekten in ihrer natürlichen Reihenfolge.

+++Syntax

`sort(<parameters>)`

+++

+++Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly oder listObject | Zu sortierende Liste. Bei listObject muss es sich um einen Feldverweis handeln. |
| keyAttributeName | Zeichenfolge | Dieser Parameter ist nur für listObject. Der Attributname in den Objekten der angegebenen Liste wird als Schlüssel zum Filtern verwendet. |
| sortingOrder | Boolescher Wert | Aufsteigend (true) oder absteigend (false) |

+++

+++Signatur und zurückgegebener Typ

`sort(<listInteger>,<boolean>)`

Gibt eine Liste mit Ganzzahlen zurück.

`sort(<listDecimal>,<boolean>)`

Gibt eine Liste mit Dezimalzahlen zurück.

`sort(<listString>,<boolean>)`

Gibt eine Liste mit Zeichenfolgen zurück.

`sort(<listDateTimeOnly>,<boolean>)`

Gibt eine Liste mit Datum/Uhrzeit-Werten ohne Berücksichtigung der Zeitzone zurück.

`sort(<listDateTime>,<boolean>)`

Gibt eine Liste mit Datum/Uhrzeit-Werten zurück.

`sort(<listDateOnly>,<boolean>)`

Gibt eine Liste mit Datumsangaben zurück.

`sort(<listBoolean>,<boolean>)`

Gibt eine Liste mit booleschen Werten zurück.

`sort(<listObject>,<string>,<boolean>)`

Gibt eine Liste mit Objekten zurück.

+++

+++Beispiele

`sort(["A", "C", "B"], true)`

Gibt `["A","B","C"]` zurück.

`sort([1, 3, 2], false)`

Gibt `[3, 2, 1]` zurück.

`sort(@event{my_event.productListItems}, "SKU", true)`

Gibt das listObject, geordnet nach SKU-Attribut (aufsteigende Reihenfolge), zurück

+++

