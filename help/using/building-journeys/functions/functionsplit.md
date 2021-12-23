---
product: adobe campaign
title: split
description: Erfahren Sie mehr über die Funktion „Aufspaltung“.
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: ht
source-wordcount: '63'
ht-degree: 100%

---

# split {#split}

Spaltet die erste Argumentzeichenfolge mit einer Trennzeichenfolge (zweite Argumentzeichenfolge, die ein regulärer Ausdruck sein kann) auf, um eine Liste von Zeichenfolgen (Token) zu erzeugen.

## Kategorie

Zeichenfolge

## Funktionssyntax

`split(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Eingabezeichenfolge | string |
| Trennzeichenfolge | string |

## Signaturen und zurückgegebener Typ

`split(<input string>, <separator string>)`

Gibt eine listString zurück.

## Beispiel

`split(["A_B_C"], "_")`

Gibt `["A","B","C"]` zurück

Beispiel mit dem Ereignisfeld „event.appVersion“ mit dem Wert: 20.45.2.3434

`split(@{event.appVersion}, "\\.")`

Gibt `["20", "45", "2", "3434"]` zurück
