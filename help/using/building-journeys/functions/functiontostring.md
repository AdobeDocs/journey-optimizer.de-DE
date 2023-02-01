---
product: journey optimizer
title: toString
description: Erfahren Sie mehr über die Funktion „toString“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toString, Funktion, Ausdruck, Journey
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: ht
source-wordcount: '120'
ht-degree: 100%

---

# toString {#toString}

Konvertiert einen Argumentwert je nach Typ in einen Zeichenfolgenwert. Weitere Informationen zu Datentypen finden Sie auf [dieser Seite](../expression/data-types.md).

## Kategorie

Konversion

## Funktionssyntax

`toString(<parameter>)`

## Parameter

| Parameter | Beschreibung |
|--- |--- |
| dateTime | konvertiert das Datum in das UTC-Datumsformat |
| dateTimeOnly | konvertiert das Datum in das UTC-Datumsformat |
| duration | konvertiert in die entsprechende Anzahl von Millisekunden als Zeichenfolge |
| integer | konvertiert den Wert in eine Zeichenfolgendarstellung (1 wird zu &quot;1&quot;) |
| decimal | konvertiert den Wert in eine Zeichenfolgendarstellung (1.5 wird zu &quot;1,5&quot;) |
| boolean | konvertiert den booleschen Wert in &#39;true&#39;, wenn „true“, in &#39;false&#39;, wenn „false“ |

## Signaturen und zurückgegebener Typ

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Gibt eine Zeichenfolge zurück.

## Beispiel

`toString(4)`

Gibt „4“ zurück.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Gibt die Zeichenfolgendarstellung des angegebenen dateOnly-Feldes (XDM-Datumsfeld) zurück, beispielsweise „2016-08-18“.
