---
product: adobe campaign
title: toDateOnly
description: Erfahren Sie mehr über die Funktion „toDateOnly“
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: ht
source-wordcount: '52'
ht-degree: 100%

---

# toDateOnly{#toDateOnly}

Konvertiert einen Argumentwert in einen reinen Datumswert.

## Kategorie

Konversion

## Funktionssyntax

`toDateOnly(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum im ISO-8601-Format oder im XDM-Datumsformat „JJJJ-MM-TT“  | string |
| Datum | date |

## Signaturen und zurückgegebene Typen

`toDateOnly(<date>)`

`toDateOnly(<string>)`

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

## Beispiele

`toDateOnly("2016-08-18")`

gibt ein dateOnly-Objekt zurück, das 2016-08-18 darstellt.
