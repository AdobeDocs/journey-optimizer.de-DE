---
product: journey optimizer
title: setDays
description: Erfahren Sie mehr über die Funktion „setDays“
feature: Journeys
role: Developer
level: Experienced
keywords: setDays, Funktion, Ausdruck, Journey
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '80'
ht-degree: 100%

---

# setDays {#setDays}

Legt den Tag eines Datum/Uhrzeit-Werts oder Datum/Uhrzeit-Werts ohne Zeitzone fest. Wenn Sie beispielsweise bis zu einem bestimmten Tag des Monats warten möchten, können Sie den Tag erzwingen.

## Kategorie

Datum

## Funktionssyntax

`setDays(<parameter>)`

## Parameter

| Parameter | Typ |
|--- |--- |
| Datum/Uhrzeit | dateTime |
| Datum/Uhrzeit ohne Berücksichtigung der Zeitzone | dateTimeOnly |
| Tage | integer |

## Signaturen und zurückgegebener Typ

`setDays(<dateTime>,<days>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

`setDays(<dateTimeOnly>,<days>)`

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

## Beispiele

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

Gibt 2023-12-25T01:11:00Z zurück.

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`
