---
product: adobe campaign
title: getListItem
description: Erfahren Sie mehr über die Funktion „gstListItem“.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e995f479-bbaa-45f3-9531-e05680c5a723
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 94%

---

# getListItem {#gestListItem}

Gibt das Element der Liste an der angegebenen Indexposition zurück.

## Kategorie

Liste

## Funktionssyntax

`getListItem(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| list | listString |
| Liste | listBoolean |
| Liste | listInteger |
| Liste | listDecimal |
| Liste | listDuration |
| Liste | listDateTime |
| Liste | listDateTimeOnly |
| Liste | listDateOnly |
| index | integer |

## Signaturen und zurückgegebener Typ

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

## Beispiel

`getListItem([10, 2, 3], 1)`

Gibt „2“ zurück

`getListItem(["A", "B", "C"], 2)`
Gibt „C“ zurück

Beispiele mit dem Ereignisfeld „event.appVersion“ mit dem Wert: 20.45.2.3434

`split(@{event.appVersion}, "\\.")`

Gibt `["20", "45", "2", "3434"]` zurück

`getListItem(split(@{event.appVersion}, "\\."), 0)`

Gibt „20“ zurück
