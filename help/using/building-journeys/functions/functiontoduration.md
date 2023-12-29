---
product: journey optimizer
title: toDuration
description: Erfahren Sie mehr über die Funktion „toDuration“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDuration, Funktion, Ausdruck, Journey
exl-id: c78e30c5-99ee-4dc7-a03a-17f7ee65f83a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 100%

---

# toDuration {#toDuration}

Konvertiert einen Argumentwert in eine Dauer. Weitere Informationen zu Datentypen finden Sie auf [dieser Seite](../expression/data-types.md).

## Kategorie

Konversion

## Funktionssyntax

`toDuration(<parameter>)`

## Parameter

| Parameter | Beschreibung |
|--- |--- |
| string | Formate, die auf dem ISO 8601-Dauerformat PnDTnHnMn.nS basieren, wobei Tage als genau 24 Stunden betrachtet werden. |
| integer | Zahl der Millisekunden |

Wenn Zeichenfolgenausdruck: Akzeptierte Formate basieren auf dem ISO 8601-Dauerformat PnDTnHnMn.nS, wobei Tage als genau 24 Stunden betrachtet werden.

Die Zeichenfolge beginnt mit einem optionalen Zeichen, markiert durch das negative oder positive ASCII-Symbol. Bei negativen Werten wird der gesamte Zeitraum negiert. Der ASCII-Buchstabe „P“ folgt in Groß- oder Kleinschreibung. Dann gibt es vier Bereiche, die jeweils aus einer Zahl und einem Suffix bestehen. Die Bereiche weisen die ASCII-Suffixe von „D“, „H“, „M“ und „S“ für Tage, Stunden, Minuten und Sekunden auf, akzeptiert in Groß- oder Kleinschreibung. Die Suffixe müssen in richtiger Reihenfolge erscheinen. Der ASCII-Buchstabe „T“ muss vor dem ersten Auftreten, so vorhanden, einer Stunde, einer Minute oder eines zweiten Bereichs stehen. Es muss mindestens einer der vier Bereiche vorhanden sein und wenn „T“ vorhanden ist, muss mindestens ein Bereich auf das „T“ folgen. Der Zahlenteil der einzelnen Bereiche muss aus einer oder mehreren ASCII-Ziffern bestehen. Der Zahl kann das negative oder positive ASCII-Symbol vorangestellt werden. Die Zahl der Tage, Stunden und Minuten muss zu einem „long“ ausgewertet werden. Die Zahl der Sekunden muss zu einem „long“ mit optionalem Bruch ausgewertet werden. Das Dezimalzeichen kann ein Punkt oder ein Komma sein. Der Bruchteil kann zwischen null und neun Stellen aufweisen.

## Signaturen und zurückgegebener Typ

`toDuration(<string>)`

`toDuration(<integer>)`

Gibt eine Dauer zurück.

## Beispiele

`toDuration("PT10H")`

Gibt eine Dauer von 10 Stunden zurück.

`toDuration("PT4S")`

Gibt eine Dauer von 4 Sekunden zurück.

`toDuration(4000)`

Gibt eine Dauer von 4 Sekunden zurück.
