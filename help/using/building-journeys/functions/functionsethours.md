---
product: journey optimizer
title: setHours
description: Erfahren Sie mehr über die Funktion „setHours“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setHours, Funktion, Ausdruck, Journey
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 95%

---

# setHours {#setHours}

Legt die Stunden eines Datum/Uhrzeit-Werts oder Datum/Uhrzeit-Werts ohne Zeitzone fest. Wenn Sie beispielsweise morgen bis zu einer bestimmten Stunde warten möchten, können Sie die Stunde erzwingen.

## Kategorie

Datum

## Funktionssyntax

`setHours(<parameter>)`

## Parameter

| Parameter | Typ |
|--- |--- |
| Datum/Uhrzeit | dateTime |
| Datum/Uhrzeit ohne Berücksichtigung der Zeitzone | dateTimeOnly |
| Stunden | Ganzzahl |

## Signaturen und zurückgegebener Typ

`setHours(<dateTime>,<hours>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

`setHours(<dateTimeOnly>,<hours>)`

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

## Beispiele

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Gibt 2023-12-12T04 zurück:11:00Z.

`setHours(nowWithDelta(1, "days"), 20)`

Gibt morgen um 20:XY Uhr zurück, wobei XY die Minuten zum Zeitpunkt der aktuellen Zeitauswertung darstellt. Wenn die Auswertung um 2:45 Uhr erfolgt, lautet die zurückgegebene Zeit 20:45 Uhr.
