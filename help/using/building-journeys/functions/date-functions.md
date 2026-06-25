---
product: journey optimizer
title: Datumsfunktionen
description: Informationen zu Datumsfunktionen
feature: Journeys
role: Developer
level: Experienced
keywords: Datum, Funktionen, Ausdruck, Journey, Uhrzeit
version: Journey Orchestration
exl-id: 68c102c1-f1c7-44b7-893f-9a3b7e0854b6
TQID: https://experienceleague.adobe.com/C2Z5SufckUxCNf9TsloziZS-Q3KPzmgMVNGJGiwDQ08
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: []
source-git-commit: 15cd7992e3263d7d2b94cf2efe50850d16e04a5d
workflow-type: tm+mt
source-wordcount: 1384
ht-degree: 60%

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
>Diese Funktion ist nur in Journey-Ausdrücken verfügbar. Verwenden Sie für die Personalisierung von E-Mails und andere Inhalte stattdessen `getCurrentZonedDateTime()`. [Weitere Informationen](../../personalization/functions/dates.md#get-current-zoned-date-time)

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

`nowWithDelta(1, "months", "Asia/Tokyo")`

Wenn am 31.01.2026 ausgewertet, wird der Wert 2026-02-28T zurückgegeben…; wenn er am 31.05.2026 ausgewertet wird, wird der Wert 2026.06.30T zurückgegeben…

`nowWithDelta()` verwendet die Kalendermonatsarithmetik. Wenn der Zielmonat weniger Tage als der aktuelle Tag des Monats hat, wird das Ergebnis auf den letzten gültigen Tag dieses Monats normalisiert. Die Funktion wird nicht auf den folgenden Monat übertragen.

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
| Stunden | integer |

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

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite werden alle Datums- und Uhrzeitfunktionen dokumentiert, die in AJO-Journey-Ausdrücken verfügbar sind. Sie beschreiben, wie Sie die aktuelle Uhrzeit abrufen, überprüfen, ob ein Datum in ein relatives Zeitfenster fällt, und Datums-/Uhrzeitkomponenten ändern.

**intents:**
* Abrufen des aktuellen Datums-/Uhrzeitwerts (mit optionaler Zeitzone) mit `now` oder `nowWithDelta`
* Abrufen der aktuellen Zeit als Epochenzahl mit `currentTimeInMillis`
* Überprüfen Sie mithilfe von `inLastDays`, `inLastHours`, `inLastMonths` oder `inLastYears`, ob ein Datum/eine Uhrzeit in die letzten N Tage, Stunden, Monate oder Jahre fällt.
* Überprüfen Sie mithilfe von `inNextDays`, `inNextHours`, `inNextMonths` oder `inNextYears`, ob ein Datum/eine Uhrzeit in die nächsten N Tage, Stunden, Monate oder Jahre fällt.
* Erzwingen einer bestimmten Stunde oder eines bestimmten Tages des Monats für einen Datums-/Uhrzeitwert mithilfe von `setHours` oder `setDays`
* Konvertieren Sie eine Datums-/Uhrzeitangabe in eine andere Zeitzone, während Sie mit `updateTimeZone` denselben Zeitpunkt beibehalten.

**Glossar:**
* **dateTime**: Ein Datums-/Uhrzeitwert, der Zeitzonenversatzinformationen enthält *(produktspezifisch)*
* **dateTimeOnly**: Ein Datums-/Uhrzeitwert ohne Zeitzoneninformationen *(produktspezifisch)*
* **Epochenmillisekunden**: Eine Ganzzahl, die die Anzahl der seit 1970-01-01T00-00Z :00: Millisekunden darstellt
* **delta**: Ein ganzzahliger Offset (positiv oder negativ), der mit `nowWithDelta` verwendet wird, um die aktuelle Zeit um eine Anzahl von Jahren, Monaten, Tagen, Stunden, Minuten oder Sekunden zu verschieben

**Leitplanken:**
* `now()` ist nur in Journey-Ausdrücken verfügbar. Verwenden Sie stattdessen `getCurrentZonedDateTime()` für die E-Mail-Personalisierung
* Die Zeitzonen-ID in `nowWithDelta` muss eine Zeichenfolgenkonstante sein. Feldverweise und dynamische Ausdrücke werden nicht unterstützt
* Die Zeitzonen-ID in `updateTimeZone` muss eine Zeichenfolgenkonstante sein

**Terminologie:**
* Kanonischer Name: Datumsfunktionen — Akronym: none — Varianten: Datums-/Uhrzeitfunktionen, Zeitfunktionen
* Synonyme: „now()“ = „current datetime“; „currentTimeInMillis()“ = „Aktuelle Epoche Millisekunden“
* Verwechseln Sie nicht: „inLastDays“ (blickt zurück in die Zeit) ≠ „inNextDays“ (blickt in die Zeit)
* Verwechseln Sie nicht: „setHours“ (ersetzt die Stundenkomponente) ≠ „nowWithDelta“ (verschiebt die aktuelle Zeit)
* Verwechseln Sie nicht: „updateTimeZone“ (gleiche Darstellung des Zeitpunkts, andere Zeitzone) ≠ „setHours“ (ändert den Zeitwert selbst)

**FAQ:**
* **F: Kann ich `now()` in E-Mail-Personalisierungsinhalten verwenden?** — Nein, `now()` ist nur in Journey-Ausdrücken verfügbar. Verwenden Sie `getCurrentZonedDateTime()` für die E-Mail-Personalisierung.
* **F: Wie kann ich überprüfen, ob ein Ereignis in den letzten 24 Stunden aufgetreten ist?** — `inLastHours(@event{MyEvent.timestamp}, 24)` verwenden.
* **F: Wie erhalte ich den aktuellen Zeitversatz um 2 Stunden in der Vergangenheit?** — `nowWithDelta(-2, "hours")` verwenden.
* **F: Was unterscheidet `updateTimeZone` von `setHours`?** - `updateTimeZone` behält den Zeitpunkt bei, drückt ihn jedoch in einer anderen Zeitzone aus, während `setHours` die Stundenkomponente des Datetime-Werts tatsächlich ändert.
* **F: Kann der Zeitzonenparameter in `nowWithDelta` ein Profilfeld sein?** — Nein, die Zeitzonen-ID muss eine Zeichenfolgenkonstante sein. Feldverweise werden nicht unterstützt.
* **F: Was passiert, wenn `nowWithDelta()` mit Monaten verwendet wird und das aktuelle Datum ein Monatsenddatum ist?** — Die Funktion verwendet die Kalendermonatsarithmetik und normalisiert das Ergebnis auf den letzten gültigen Tag des Zielmonats. Wenn Sie beispielsweise 1 Monat zum 31. Januar hinzufügen, wird der 28. Februar zurückgegeben (nicht der 3. März).

+++
