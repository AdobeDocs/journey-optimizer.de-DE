---
product: adobe campaign
title: in
description: Erfahren Sie mehr über die Funktion „in“
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 100%

---

# in {#in}

Überprüft, ob sich der erste Argumentwert in der Liste befindet. Die Prüfung wird mithilfe eines Gleichzeichens für jeden Argumentwert durchgeführt. Gibt „true“ zurück, wenn der Argumentwert gefunden wurde, andernfalls „false“.

Der Typ von `<expression>` muss mit Elementen der Liste übereinstimmen. Zur Erinnerung: Typen von Elementen in der Liste müssen miteinander übereinstimmen.

## Kategorie

Liste

## Funktionssyntax

`in(<parameters>)`

## Parameter

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

## Signatur und zurückgegebener Typ

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

Geben einen booleschen Wert zurück.

## Beispiel

`in(4,[4,5,3,4])`

Gibt „true“ zurück.

`in(8,[4,5,3,4])`

Gibt „false“ zurück.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`
