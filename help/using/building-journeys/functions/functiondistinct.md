---
product: journey optimizer
title: distinct
description: Erfahren Sie mehr über den Funktionsunterschied
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# distinct {#distinct}

Gibt die eindeutigen Werte oder Objekte einer angegebenen Liste zurück. Null-Einträge werden ignoriert.

>[!NOTE]
>
>Wenn die Zielliste ein listObject ist, kann diese Funktion nur in benutzerdefinierten Aktionsausdrücken verwendet werden.

## Kategorie

Liste

## Funktionssyntax

`distinct(<parameters>)`

## Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly oder listObject | Zu verarbeitende Liste. Bei listObject muss es sich um einen Feldverweis handeln. |
| keyAttributeName | Zeichenfolge | Dieser Parameter ist optional und nur für listObject. Wenn der Parameter nicht angegeben wird, wird ein Objekt als dupliziert betrachtet, wenn alle Attribute dieselben Werte aufweisen. Andernfalls wird ein Objekt als dupliziert betrachtet, wenn das angegebene Attribut denselben Wert aufweist. |

## Signaturen und zurückgegebene Typen

`distinct(<listInteger>)`

Gibt eine Liste von Ganzzahlen zurück.

`distinct(<listDecimal>)`

Gibt eine Liste mit Dezimalstellen zurück.

`distinct(<listString>)`

Gibt eine Liste von Zeichenfolgen zurück.

`distinct(<listDateTimeOnly>)`

Gibt eine Liste der Uhrzeiten ohne Berücksichtigung der Zeitzone zurück.

`distinct(<listDateTime>)`

Gibt eine Liste der Uhrzeiten zurück.

`distinct(<listDateOnly>)`

Gibt eine Liste mit Datumsangaben zurück.

`distinct(<listBoolean>)`

Gibt eine Liste mit booleschen Werten zurück.

`distinct(<listDuration>)`

Gibt eine Liste der Dauern zurück.

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

Gibt eine Liste von Objekten zurück.


## Beispiele

`distinct([10,2,10,null])`

Rückgabe `[10, 2]`.
