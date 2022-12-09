---
product: journey optimizer
title: setHours
description: Erfahren Sie mehr über die Funktion setHours
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# setHours {#setHours}

Legt nur die Stunden einer Datum- oder Datum-Uhrzeit fest. Wenn Sie beispielsweise morgen bis zu einer bestimmten Stunde warten möchten, können Sie die Stunde erzwingen.

## Kategorie

Datum

## Funktionssyntax

`setHours(<parameter>)`

## Parameter

| Parameter | Typ |
|--- |--- |
| Datum/Uhrzeit | dateTime |
| Datum/Uhrzeit ohne Berücksichtigung der Zeitzone | dateTimeOnly |
| Stunden | integer |

## Signaturen und zurückgegebener Typ

`setHours(<dateTime>,<hours>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

`setHours(<dateTimeOnly>,<hours>)`

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

## Beispiele

`setHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

Gibt 2010-12-12T04 zurück:11:00Z.

`setHours(nowWithDelta(1, "days"), 20)`

Gibt morgen um 20:XY zurück, wobei XY die Minuten zum Zeitpunkt der aktuellen Zeitbewertung ist. Wenn die Auswertung um 2:45 Uhr erfolgt, ist die zurückgegebene Zeit 20:45 Uhr.
