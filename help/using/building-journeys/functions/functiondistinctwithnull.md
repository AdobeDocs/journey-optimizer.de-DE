---
product: journey optimizer
title: distinctWithNull
description: Erfahren Sie mehr über die Funktion „distinctWithNull“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctWithNull, Funktion, Ausdruck, Journey
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 79%

---

# distinctWithNull {#distinctWithNull}

Gibt die unterschiedlichen Werte oder Objekte einer angegebenen Liste zurück. Wenn die Liste mindestens einen Nullwert enthält, wird ein Nullwert in der zurückgegebenen Liste angezeigt.

Beachten Sie, dass der Parameter `<listObject>` wird in dieser Funktion nicht unterstützt.

## Kategorie

Liste

## Funktionssyntax

`distinctWithNull(<parameters>)`

## Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Zu verarbeitende Liste. |

## Signaturen und zurückgegebene Typen

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

## Beispiele

`distinctWithNull([10,2,10,null])`

Gibt [10, 2, null] zurück.
