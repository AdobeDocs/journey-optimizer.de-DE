---
product: journey optimizer
title: toDuration
description: Erfahren Sie mehr über die Funktion toDuration
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c78e30c5-99ee-4dc7-a03a-17f7ee65f83a
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# toDuration {#toDuration}

Konvertiert einen Argumentwert in eine Dauer. Weitere Informationen zu Datentypen finden Sie unter [diese Seite](../expression/data-types.md).

## Kategorie

Konversion

## Funktionssyntax

`toDuration(<parameter>)`

## Parameter

| Parameter | Beschreibung |
|--- |--- |
| Zeichenfolge | Formate, die auf dem ISO 8601-Dauerformat PnDTnHnMn.nS basieren, wobei Tage als genau 24 Stunden betrachtet werden |
| integer | Anzahl der Millisekunden |

If string expression: Die zulässigen Formate basieren auf dem ISO 8601-Dauerformat PnDTnHnMn.nS, wobei Tage als genau 24 Stunden betrachtet werden.

Die Zeichenfolge beginnt mit einem optionalen Zeichen, gekennzeichnet durch das negative oder positive ASCII-Symbol. Bei negativen Werten wird der gesamte Zeitraum negiert. Der ASCII-Buchstabe &quot;P&quot;folgt in Groß- oder Kleinschreibung. Dann gibt es vier Abschnitte, die jeweils aus einer Zahl und einem Suffix bestehen. Die Abschnitte weisen in ASCII die Suffixe &quot;D&quot;, &quot;H&quot;, &quot;M&quot;und &quot;S&quot;für Tage, Stunden, Minuten und Sekunden auf, die in Groß- oder Kleinschreibung akzeptiert werden. Die Suffixe müssen in der richtigen Reihenfolge auftreten. Der ASCII-Buchstabe &quot;T&quot;muss vor dem ersten Vorkommen eines Stunden, einer Minute oder eines zweiten Abschnitts stehen. Mindestens einer der vier Abschnitte muss vorhanden sein, und wenn &quot;T&quot;vorhanden ist, muss mindestens ein Abschnitt nach dem &quot;T&quot;vorhanden sein. Der Zahlenteil jedes Abschnitts muss aus einer oder mehreren ASCII-Ziffern bestehen. Der Zahl kann das negative oder positive ASCII-Symbol vorangestellt werden. Die Anzahl der Tage, Stunden und Minuten muss auf &quot;long&quot;analysiert werden. Die Anzahl der Sekunden muss mit dem optionalen Bruch auf &quot;long&quot;analysiert werden. Der Dezimalpunkt kann ein Punkt oder ein Komma sein. Der Bruchteil kann zwischen null und neun Stellen aufweisen.

## Signaturen und zurückgegebener Typ

`toDuration(<string>)`

`toDuration(<integer>)`

Gibt eine Dauer zurück.

## Beispiele

`toDuration("PT10H")`

Gibt eine Dauer von 10 Stunden zurück.

`toDuration("PT4S")`

Gibt die Dauer von 4 Sekunden zurück.

`toDuration(4000)`

Gibt die Dauer von 4 Sekunden zurück.
