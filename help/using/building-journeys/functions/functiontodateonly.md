---
product: journey optimizer
title: toDateOnly
description: Erfahren Sie mehr über die Funktion „toDateOnly“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateOnly, Funktion, Ausdruck, Journey
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: ht
source-wordcount: '100'
ht-degree: 100%

---

# toDateOnly{#toDateOnly}

Konvertiert ein Argument in einen Wert vom Typ dateOnly. Weiterführende Informationen zu Datentypen finden Sie in diesem [Abschnitt](../expression/data-types.md).

## Kategorie

Konversion

## Funktionssyntax

`toDateOnly(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Zeichenfolgendarstellung eines Datums als „JJJJ-MM-TT“ (XDM-Format). Unterstützt auch das ISO-8601-Format: nur der Teil mit dem **vollständigen Datum** wird berücksichtigt (siehe [RFC 3339, Abschnitt 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | Zeichenfolge |
| Datum/Uhrzeit | dateTime |
| Datum/Uhrzeit ohne Zeitzone | dateTimeOnly |
| ganzzahliger Wert einer Epoche in Millisekunden | integer |

## Signaturen und zurückgegebene Typen

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

Gibt einen Wert vom Typ dateOnly zurück.

## Beispiele

`toDateOnly("2016-08-18")`

`toDateOnly("2016-08-18T00:00:00.000Z")`

`toDateOnly("2016-08-18T00:00:00")`

alle geben ein dateOnly -Objekt zurück, das 2016-08-18 darstellt.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Gibt ein dateOnly zurück.
