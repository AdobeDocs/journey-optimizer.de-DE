---
product: journey optimizer
title: in
description: Erfahren Sie mehr über die Funktion in
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 629b7aa3-8904-453b-ba3c-c6a333b13c81
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# in {#in}

Überprüft, ob der erste Argumentwert in der Liste enthalten ist. Die Prüfung wird über einen Gleichheitswert für jeden Argumentwert durchgeführt. Gibt &quot;true&quot;zurück, wenn der Argumentwert gefunden wurde, andernfalls &quot;false&quot;.

Der Typ der `<expression>` muss mit Elementen der Liste übereinstimmen. Zur Erinnerung: Die Typen der Elemente der Liste müssen übereinstimmen.

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

Gibt einen booleschen Wert zurück.

## Beispiel

`in(4,[4,5,3,4])`

Gibt &quot;true&quot;zurück.

`in(8,[4,5,3,4])`

Gibt false zurück.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`
