---
product: journey optimizer
title: serializeList
description: Erfahren Sie mehr über die Funktion „serializeList“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: serializeList, Funktion, Ausdruck, Journey
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: ht
source-wordcount: '88'
ht-degree: 100%

---

# serializeList {#serializeList}

Konvertiert eine angegebene Liste (alle Typen außer listObject) in eine Zeichenfolge.

## Kategorie

Liste

## Funktionssyntax

`serializeList(<parameters>)`

## Parameter

| Parameter | Typ | Beschreibung |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Liste zur Konvertierung in eine Zeichenfolge. |
| Trennzeichen | Zeichenfolge | Trennzeichen zwischen den einzelnen Listenelementen in der Ausgabezeichenfolge. |
| addQuotes | Boolescher Wert | Dieser Parameter gibt an, ob jedes Element der Ausgabezeichenfolge Anführungszeichen enthalten soll (true) oder nicht (false). |

## Signatur und zurückgegebener Typ

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

Gibt eine Zeichenfolge zurück.

## Beispiel

`serializeList(["Hello","World"], " ", false)`

Gibt „Hello World“ zurück.

`serializeList(["Hello", "World"], ",", true)`

Gibt „&quot;Hello&quot;,&quot;World&quot;“ zurück.
