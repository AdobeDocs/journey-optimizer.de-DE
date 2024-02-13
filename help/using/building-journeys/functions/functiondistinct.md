---
product: journey optimizer
title: distinct
description: Erfahren Sie mehr über die Funktion „distinct“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinct, function, expression, journey
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: ht
source-wordcount: '155'
ht-degree: 100%

---

# distinct {#distinct}

Gibt die unterschiedlichen Werte oder Objekte einer angegebenen Liste zurück. Einträge mit Null werden ignoriert.

## Kategorie

Liste

## Funktionssyntax

`distinct(<parameters>)`

## Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly oder listObject | Zu verarbeitende Liste. Bei listObject muss es sich um einen Feldverweis handeln. |
| keyAttributeName | Zeichenfolge | Dieser Parameter ist optional und nur für listObject. Wenn der Parameter nicht angegeben wird, wird ein Objekt als doppelt betrachtet, wenn alle Attribute dieselben Werte aufweisen. Andernfalls wird ein Objekt als doppelt betrachtet, wenn das angegebene Attribut denselben Wert aufweist. |

## Signaturen und zurückgegebene Typen

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


## Beispiele

`distinct([10,2,10,null])`

Gibt `[10, 2]` zurück.
