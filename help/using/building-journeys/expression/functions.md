---
solution: Journey Optimizer
product: journey optimizer
title: Funktionen
description: Erfahren Sie mehr über Funktionen
feature: Journeys
role: Developer
level: Experienced
keywords: Funktion, Ausdrücke, Editor, Journey
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 0331f8fe2439d41c08ad88a6d0bd95dd150bab90
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 100%

---

# Funktionen {#functions}

Eine Funktion kann verschiedene Signaturen haben (einen jeweils anderen Satz geordneter Parameter). Eine Funktionssignatur kann 0-N Ausdrücke als geordnete Parameter haben.

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, ... ,`<expression as param N>`)

Jede Funktion weist einen bestimmten Rückgabetyp auf.

Im Folgenden finden Sie eine Liste der unterstützten Funktionen.

## Hauptfunktionen

| Kategorie | Funktion |
|-------------|-----------------------|
| Adobe Experience Platform | [inAudience](../functions/functioninaudience.md) |
| Aggregation | [avg](../functions/aggregation-functions.md#avg) |
| Aggregation | [count](../functions/aggregation-functions.md#count) |
| Aggregation | [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) |
| Aggregation | [countWithNull](../functions/aggregation-functions.md#countWithNull) |
| Aggregation | [distinctCount](../functions/aggregation-functions.md#distinctCount) |
| Aggregation | [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) |
| Aggregation | [max](../functions/aggregation-functions.md#max) |
| Aggregation | [min](../functions/aggregation-functions.md#min) |
| Aggregation | [sum](../functions/aggregation-functions.md#sum) |
| Konversion | [toBool](../functions/conversion-functions.md#toBool) |
| Konversion | [toDateOnly](../functions/conversion-functions.md#toDateOnly) |
| Konversion | [toDateTime](../functions/conversion-functions.md#toDateTime) |
| Konversion | [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) |
| Konversion | [toDecimal](../functions/conversion-functions.md#toDecimal) |
| Konversion | [toDuration](../functions/conversion-functions.md#toDuration) |
| Konversion | [toInteger](../functions/conversion-functions.md#toInteger) |
| Konversion | [toString](../functions/conversion-functions.md#toString) |
| Datum | [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) |
| Datum | [inLastDays](../functions/date-functions.md#inLastDays) |
| Datum | [inLastHours](../functions/date-functions.md#inLastHours) |
| Datum | [inLastMonths](../functions/date-functions.md#inLastMonths) |
| Datum | [inLastYears](../functions/date-functions.md#inLastYears) |
| Datum | [inNextDays](../functions/date-functions.md#inNextDays) |
| Datum | [inNextHours](../functions/date-functions.md#inNextHours) |
| Datum | [inNextMonths](../functions/date-functions.md#inNextMonths) |
| Datum | [inNextYears](../functions/date-functions.md#inNextYears) |
| Datum | [now](../functions/date-functions.md#now) |
| Datum | [nowWithDelta](../functions/date-functions.md#nowWithDelta) |
| Datum | [setHours](../functions/date-functions.md#setHours) |
| Datum | [setDays](../functions/date-functions.md#setDays) |
| Datum | [updateTimeZone](../functions/date-functions.md#updateTimeZone) |
| Liste | [distinct](../functions/list-functions.md#distinct) |
| Liste | [distinctWithNull](../functions/list-functions.md#distinctWithNull) |
| Liste | [filter](../functions/list-functions.md#filter) |
| Liste | [getListItem](../functions/list-functions.md#getListItem) |
| Liste | [in](../functions/list-functions.md#in) |
| Liste | [intersect](../functions/list-functions.md#intersect) |
| Liste | [limit](../functions/list-functions.md#limit) |
| Liste | [listSize](../functions/list-functions.md#listSize) |
| Liste | [serializeList](../functions/list-functions.md#serializeList) |
| Liste | [sort](../functions/list-functions.md#sort) |
| Math | [random](../functions/functionrandom.md) |
| Math | [round](../functions/functionround.md) |
| Zeichenfolge | [concat](../functions/functionconcat.md) |
| Zeichenfolge | [contain](../functions/functioncontain.md) |
| Zeichenfolge | [containIgnoreCase](../functions/functioncontainwithignorecase.md) |
| Zeichenfolge | [endWith](../functions/functionendwith.md) |
| Zeichenfolge | [endWithIgnoreCase](../functions/functionendwithignorecase.md) |
| Zeichenfolge | [equalIgnoreCase](../functions/functionequalignorecase.md) |
| Zeichenfolge | [indexOf](../functions/functionindexof.md) |
| Zeichenfolge | [isEmpty](../functions/functionisempty.md) |
| Zeichenfolge | [isNotEmpty](../functions/functionisnotempty.md) |
| Zeichenfolge | [lastIndexOf](../functions/functionlastindexof.md) |
| Zeichenfolge | [length](../functions/functionlength.md) |
| Zeichenfolge | [lower](../functions/functionlower.md) |
| Zeichenfolge | [matchRegExp](../functions/functionmatchregexp.md) |
| Zeichenfolge | [notEqualIgnoreCase](../functions/functionnotequalignorecase.md) |
| Zeichenfolge | [replace](../functions/functionreplace.md) |
| Zeichenfolge | [replaceAll](../functions/functionreplaceall.md) |
| Zeichenfolge | [split](../functions/functionsplit.md) |
| Zeichenfolge | [startWith](../functions/functionstartwith.md) |
| Zeichenfolge | [startWithIgnoreCase](../functions/functionstartwithignorecase.md) |
| Zeichenfolge | [substr](../functions/functionsubstr.md) |
| Zeichenfolge | [trim](../functions/functiontrim.md) |
| Zeichenfolge | [upper](../functions/functionupper.md) |
| Zeichenfolge | [uuid](../functions/functionuuid.md) |
