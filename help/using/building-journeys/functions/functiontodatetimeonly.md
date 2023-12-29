---
product: journey optimizer
title: toDateTimeOnly
description: Erfahren Sie mehr über die Funktion „toDateTime“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateTimeOnly, Funktion, Ausdruck, Journey
exl-id: db54c119-5080-403a-b254-43645be6b4a8
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 100%

---

# toDateTimeOnly{#toDateTimeOnly}

Konvertiert einen Argumentwert in einen Datum/Uhrzeit-Wert ohne Zeitzone.

## Kategorie

Konversion

## Funktionssyntax

`toDateTimeOnly(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit im ISO-8601-Format oder im XDM-Datumsformat &quot;JJJJ-MM-TT&quot; | Zeichenfolge |
| Datum/Uhrzeit | dateTime |

## Signaturen und zurückgegebene Typen

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`
<!--`toDateTimeOnly(<integer>,<integer>,<integer>)`
`toDateTimeOnly(<integer>,<integer>,<integer>,<integer>,<integer>,<integer>)`-->

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

## Beispiele

`toDateTimeOnly ("2016-08-18")`

gibt einen Datum/Uhrzeit-Wert zurück, der 2016-08-18T00:00:00.000 entspricht.

`toDateTimeOnly(now())`

<!--`toDateTimeOnly(2016,8,18,23,17,59)`

Returns 2016-08-18T23:17:59.000.

`toDateTimeOnly(2016,8,18)`

Returns 2016-08-18T00:00:00.000.-->
