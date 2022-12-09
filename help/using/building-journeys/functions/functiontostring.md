---
product: journey optimizer
title: toString
description: Erfahren Sie mehr über die Funktion toString
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# toString {#toString}

Konvertiert einen Argumentwert je nach Typ in einen Zeichenfolgenwert. Weitere Informationen zu Datentypen finden Sie unter [diese Seite](../expression/data-types.md).

## Kategorie

Konversion

## Funktionssyntax

`toString(<parameter>)`

## Parameter

| Parameter | Beschreibung |
|--- |--- |
| dateTime | konvertiert das Datum in das UTC-Datumsformat |
| dateTimeOnly | konvertiert das Datum in das UTC-Datumsformat |
| duration | in die entsprechende Anzahl von Millisekunden als Zeichenfolge konvertieren |
| integer | konvertiert den Wert in die Zeichenfolgendarstellung (1 wird zu &quot;1&quot;) |
| decimal | konvertiert den Wert in die Zeichenfolgendarstellung (1.5 wird zu &quot;1.5&quot;) |
| boolean | konvertiert den booleschen Wert in &quot;true&quot;, wenn &quot;true&quot;, in &quot;false&quot;, wenn &quot;false&quot; |

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

Gibt &quot;4&quot;zurück.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Gibt die Zeichenfolgendarstellung des angegebenen DatumsOnly-Felds (XDM Date-Feld) zurück, z. B. &quot;2016-08-18&quot;.
