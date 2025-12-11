---
product: journey optimizer
title: Datumsfunktionen
description: Informationen zu Datumsfunktionen
feature: Journeys
role: Developer
level: Experienced
keywords: Datum, Funktionen, Ausdruck, Journey, Uhrzeit
version: Journey Orchestration
source-git-commit: 8ca1c995bc38b110fa07573f922906c775fd5e6f
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 95%

---

# Datumsfunktionen {#date-functions}

Mit Datumsfunktionen können Sie Datums- und Uhrzeitwerte in Ihren Journey-Ausdrücken bearbeiten. Diese Funktionen sind für zeitbasierte Bedingungen, Zeitpläne und zeitliche Berechnungen in Ihren Customer Journeys unerlässlich.

Verwenden Sie Datumsfunktionen, wenn Sie Folgendes tun müssen:

* Abrufen der aktuellen Zeit oder des aktuellen Datums im Kontext einer bestimmten Zeitzone ([now](#now), [nowWithDelta](#nowWithDelta), [currentTimeInMillis](#currentTimeInMillis))
* Überprüfen, ob ein Datum in einen bestimmten Zeitbereich fällt ([inLastDays](#inLastDays), [inLastHours](#inLastHours), [inLastMonths](#inLastMonths), [inLastYears](#inLastYears), [inNextDays](#inNextDays), [inNextHours](#inNextHours), [inNextMonths](#inNextMonths), [inNextYears](#inNextYears))
* Ändern von Datums- und Zeitkomponenten ([setHours](#setHours), [setDays](#setDays), [updateTimeZone](#updateTimeZone))
* Durchführen von zeitbasierten Berechnungen und Vergleichen
* Konvertieren zwischen verschiedenen Zeitformaten und Darstellungen

Datumsfunktionen bieten eine präzise Kontrolle über die zeitliche Logik, sodass Sie zeitabhängige Journey-Pfade und Bedingungen erstellen können, die auf bestimmte Zeitrahmen und Zeitpläne reagieren.

>[!NOTE]
>
>Die Funktionen auf dieser Seite sind in Journey-Ausdrücken verfügbar. Einige Funktionen wie `now()` sind im Personalisierungseditor für E-Mail-Inhalte nicht verfügbar. [Weitere Informationen](../../personalization/functions/dates.md)

## currentTimeInMillis {#currentTimeInMillis}

Gibt die aktuelle Zeit in Epoch-Millisekunden zurück.

+++Syntax

`currentTimeInMillis()`

+++

+++Parameter

Diese Funktion verwendet keine Parameter.

+++

+++Signaturen und zurückgegebener Typ

`currentTimeInMillis()`

Gibt eine Ganzzahl zurück.

+++

+++Beispiele

`currentTimeInMillis()`

Gibt „1544712617131“ zurück.

+++

## inLastDays {#inLastDays}

Gibt „true“ zurück, wenn ein bestimmtes „dateTime“ zwischen jetzt und jetzt-Delta-Tage liegt.

+++Syntax

`inLastDays(<dateTime>,<delta>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

+++

+++Signaturen und zurückgegebener Typ

`inLastDays(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.

+++

## inLastHours {#inLastHours}

Gibt „true“ zurück, wenn der angegebene Datum/Uhrzeit-Wert zwischen jetzt und jetzt – delta Stunden liegt.

+++Syntax

`inLastHours(<dateTime>,<delta>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

+++

+++Signaturen und zurückgegebener Typ

`inLastHours(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.

`inLastHours(@event{MyEvent.timestamp}, 4)`

Gibt „true“ zurück.

+++

## inLastMonths {#inLastMonths}

Gibt „true“ zurück, wenn der angegebene Datums- bzw. Datum-/Uhrzeit-Wert zwischen jetzt und jetzt – delta Monaten liegt.

+++Syntax

`inLastMonths(<dateTime>,<delta>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

+++

+++Signaturen und zurückgegebener Typ

`inLastMonths(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.

+++

## inLastYears {#inLastYears}

Gibt „true“ zurück, wenn der angegebene Datums- bzw. Datum-/Uhrzeit-Wert zwischen jetzt und jetzt – delta Jahren liegt.

+++Syntax

`inLastYears(<dateTime>,<delta>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

+++

+++Signaturen und zurückgegebener Typ

`inLastYears(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.

+++

## inNextDays {#inNextDays}

Gibt „true“ zurück, wenn der angegebene Datums- bzw. Datum-/Uhrzeit-Wert zwischen jetzt und jetzt + delta Tagen liegt.

+++Syntax

`inNextDays(<dateTime>,<delta>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

+++

+++Signaturen und zurückgegebener Typ

`inNextDays(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.

+++

## inNextHours {#inNextHours}

Gibt „true“ zurück, wenn der angegebene Datums- bzw. Datum-/Uhrzeit-Wert zwischen jetzt und jetzt + delta Stunden liegt.

+++Syntax

`inNextHours(<dateTime>,<delta>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

+++

+++Signaturen und zurückgegebener Typ

`inNextHours(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.

+++

## inNextMonths {#inNextMonths}

Gibt „true“ zurück, wenn der angegebene Datums- bzw. Datum-/Uhrzeit-Wert zwischen jetzt und jetzt + delta Monaten liegt.

+++Syntax

`inNextMonths(<dateTime>,<delta>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

+++

+++Signaturen und zurückgegebener Typ

`inNextMonths(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

Gibt „true“ zurück.

+++

## inNextYears {#inNextYears}

Gibt „true“ zurück, wenn der angegebene Datums- bzw. Datum-/Uhrzeit-Wert zwischen jetzt und jetzt + delta Jahren liegt.

+++Syntax

`inNextYears(<dateTime>,<delta>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| Datum/Uhrzeit | dateTime |
| delta | integer |

+++

+++Signaturen und zurückgegebener Typ

`inNextYears(<dateTime>,<integer>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Gibt „true“ zurück.

+++

## now {#now}

Gibt das aktuelle Datum im Datum/Uhrzeit-Format zurück. Weitere Informationen zu Datentypen finden Sie auf [dieser Seite](../expression/data-types.md).

>[!NOTE]
>
>Diese Funktion ist nur in Journey-Ausdrücken verfügbar. Verwenden Sie stattdessen `getCurrentZonedDateTime()` für die Personalisierung von E-Mails und andere Inhalte. [Weitere Informationen](../../personalization/functions/dates.md#get-current-zoned-date-time)

+++Syntax

`now(<parameter>)`

+++

+++Parameter

| Parameter | Beschreibung |
|--- |--- |
| string | Zeitzonenkennung (optional) |

+++

+++Signaturen und zurückgegebener Typ

`now()`

`now("<timeZone id>")`

Gibt einen Datum/Uhrzeit-Wert zurück.

+++

+++Beispiele

`now()`

Gibt 2023-06-03T06:30Z zurück.

`toString(now())`

Gibt „2023-06-03T06:30Z“ zurück

`now("Europe/Paris")`

Gibt 2023-06-03T08:30+02:00 zurück.

+++

## nowWithDelta {#nowWithDelta}

Gibt den aktuellen Datum/Uhrzeit-Wert einschließlich Verschiebung zurück. Wenn eine Zeitzonen-ID angegeben wird, wird die Zeitzonenverschiebung angewendet. Weitere Informationen zu Datentypen finden Sie auf [dieser Seite](../expression/data-types.md).

+++Syntax

`nowWithDelta(<parameters>)`

+++

+++Parameter

| Parameter | Beschreibung |
|--- |--- |
| delta | positiver oder negativer Ganzzahlwert |
| date part | Jahre, Monate, Tage, Stunden, Minuten oder Sekunden als Zeichenfolge |
| Zeitzonen-ID | Zeichenfolgendarstellung des Zeitzonenwerts. Weitere Informationen finden Sie unter [Datentypen](../expression/data-types.md). Die Zeitzonen-ID muss eine Zeichenfolgenkonstante sein. Er darf weder ein Feldverweis noch ein Ausdruck sein. |

+++

+++Signaturen und zurückgegebener Typ

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Gibt einen Datum/Uhrzeit-Wert zurück.

+++

+++Beispiele

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Gibt einen Datum/Uhrzeit-Wert von vor genau 2 Stunden zurück.

+++

## setHours {#setHours}

Legt die Stunden eines Datum/Uhrzeit-Werts oder Datum/Uhrzeit-Werts ohne Zeitzone fest. Wenn Sie beispielsweise morgen bis zu einer bestimmten Stunde warten möchten, können Sie die Stunde erzwingen.

+++Syntax

`setHours(<parameter>)`

+++

+++Parameter

| Parameter | Typ |
|--- |--- |
| Datum/Uhrzeit | dateTime |
| Datum/Uhrzeit ohne Berücksichtigung der Zeitzone | dateTimeOnly |
| Stunden | Ganzzahl |

+++

+++Signaturen und zurückgegebener Typ

`setHours(<dateTime>,<hours>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

`setHours(<dateTimeOnly>,<hours>)`

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

+++

+++Beispiele

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Gibt 2023-12-12T04:11:00Z zurück.

`setHours(nowWithDelta(1, "days"), 20)`

Gibt morgen um 20::XY Uhr zurück, wobei XY die Minuten zum Zeitpunkt der aktuellen Zeitauswertung darstellt. Wenn die Auswertung um 2::45 Uhr erfolgt, lautet die zurückgegebene Zeit 20::45 Uhr.

+++

## setDays {#setDays}

Legt den Tag eines Datum/Uhrzeit-Werts oder Datum/Uhrzeit-Werts ohne Zeitzone fest. Wenn Sie beispielsweise bis zu einem bestimmten Tag des Monats warten möchten, können Sie den Tag erzwingen.

+++Syntax

`setDays(<parameter>)`

+++

+++Parameter

| Parameter | Typ |
|--- |--- |
| Datum/Uhrzeit | dateTime |
| Datum/Uhrzeit ohne Berücksichtigung der Zeitzone | dateTimeOnly |
| Tage | integer |

+++

+++Signaturen und zurückgegebener Typ

`setDays(<dateTime>,<days>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

`setDays(<dateTimeOnly>,<days>)`

Gibt einen Datum/Uhrzeit-Wert ohne Berücksichtigung der Zeitzone zurück.

+++

+++Beispiele

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

Gibt 2023-12-25T01:11:00Z zurück.

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`

+++

## updateTimeZone {#updateTimeZone}

Gibt einen neuen Datum-/Uhrzeit-Wert mit einer neuen Zeitzone im selben Moment zurück.

+++Syntax

`updateTimeZone(<parameters>)`

+++

+++Parameter

* Zeitzonen-ID: string
* dateTime

+++

+++Signatur und zurückgegebener Typ

`updateTimeZone(<dateTime>,<timeZone id>)`

Gibt einen Datum/Uhrzeit-Wert zurück.

+++

+++Beispiele

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Gibt 2023-08-28T17:15:30.123+02:00 zurück.

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

Wenn der Wert des Zeitstempelfelds `2021-11-16T16:55:12.939318+01:00` ist, gibt die Funktion `2021-11-17T02:55:12.942115+11:00` zurück.

+++

