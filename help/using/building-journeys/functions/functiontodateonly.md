---
product: journey optimizer
title: toDateOnly
description: Erfahren Sie mehr über die Funktion „toDateOnly“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateOnly, Funktion, Ausdruck, Journey
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 1af75a0e6bfc2c3b9c565c3190f46d137a68d32e
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 90%

---

# toDateOnly{#toDateOnly}

Konvertiert ein Argument in einen Wert vom Typ dateOnly. Weitere Informationen zu Datentypen finden Sie in diesem [Abschnitt](../expression/data-types.md).

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

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

alle geben ein dateOnly-Objekt zurück, das den 18.08.2023 darstellt.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Gibt ein dateOnly zurück.
