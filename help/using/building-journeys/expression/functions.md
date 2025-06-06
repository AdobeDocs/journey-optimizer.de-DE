---
solution: Journey Optimizer
product: journey optimizer
title: Funktionen
description: Erfahren Sie mehr über Funktionen
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: Funktion, Ausdrücke, Editor, Journey
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

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
| Aggregation | [avg](../functions/functionavg.md) |
| Aggregation | [count](../functions/functioncount.md) |
| Aggregation | [countOnlyNull](../functions/functioncountonlynull.md) |
| Aggregation | [countWithNull](../functions/functioncountwithnull.md) |
| Aggregation | [distinctCount](../functions/functiondistinctcount.md) |
| Aggregation | [distinctCountWithNull](../functions/functiondistinctcountwithnull.md) |
| Aggregation | [max](../functions/functionmax.md) |
| Aggregation | [min](../functions/functionmin.md) |
| Aggregation | [sum](../functions/functionsum.md) |
| Konversion | [toBool](../functions/functiontobool.md) |
| Konversion | [toDateOnly](../functions/functiontodateonly.md) |
| Konversion | [toDateTime](../functions/functiontodatetime.md) |
| Konversion | [toDateTimeOnly](../functions/functiontodatetimeonly.md) |
| Konversion | [toDecimal](../functions/functiontodecimal.md) |
| Konversion | [toDuration](../functions/functiontoduration.md) |
| Konversion | [toInteger](../functions/functiontointeger.md) |
| Konversion | [toString](../functions/functiontostring.md) |
| Datum | [currentTimeInMillis](../functions/functioncurrenttimeinmillis.md) |
| Datum | [inLastDays](../functions/functioninlastdays.md) |
| Datum | [inLastHours](../functions/functioninlasthours.md) |
| Datum | [inLastMonths](../functions/functioninlastmonths.md) |
| Datum | [inLastYears](../functions/functioninlastyears.md) |
| Datum | [inNextDays](../functions/functioninnextdays.md) |
| Datum | [inNextHours](../functions/functioninnexthours.md) |
| Datum | [inNextMonths](../functions/functioninnextmonths.md) |
| Datum | [inNextYears](../functions/functioninnextyears.md) |
| Datum | [now](../functions/functionnow.md) |
| Datum | [nowWithDelta](../functions/functionnowwithdelta.md) |
| Datum | [setHours](../functions/functionsethours.md) |
| Datum | [setDays](../functions/functionsetdays.md) |
| Datum | [updateTimeZone](../functions/functionupdatetimezone.md) |
| Liste | [distinct](../functions/functiondistinct.md) |
| Liste | [distinctWithNull](../functions/functiondistinctwithnull.md) |
| Liste | [filter](../functions/functionfilter.md) |
| Liste | [getListItem](../functions/functiongetlistitem.md) |
| Liste | [in](../functions/functionin.md) |
| Liste | [intersect](../functions/functionintersect.md) |
| Liste | [limit](../functions/functionlimit.md) |
| Liste | [listSize](../functions/functionlistsize.md) |
| Liste | [serializeList](../functions/functionserializelist.md) |
| Liste | [sort](../functions/functionsort.md) |
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
