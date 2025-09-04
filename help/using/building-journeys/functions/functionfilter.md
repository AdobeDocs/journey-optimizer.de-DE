---
product: journey optimizer
title: filter
description: Erfahren Sie mehr über die Funktion „filter“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: filtern, Funktion, Ausdruck, Journey
exl-id: 05e3d2ba-1a27-4f27-88cc-3d83eb3b14af
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 100%

---

# filter{#filter}

Gibt ein listObject mit Objekten zurück, deren Schlüsselattribut einem der angegebenen Schlüsselwerte entspricht.

## Kategorie

Liste

## Funktionssyntax

`filter(<parameters>)`

## Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToFilter | listObject | Liste der zu filternden Objekte. Muss ein Feldverweis sein. |
| keyAttributeName | Zeichenfolge | Attributname in den Objekten der angegebenen Liste, der als Schlüssel zum Filtern verwendet wird |
| keyValueList | list | Schlüsselwerte für die Filterung |

## Signaturen und zurückgegebene Typen

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

Gibt ein listObject zurück.

## Beispiele

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
