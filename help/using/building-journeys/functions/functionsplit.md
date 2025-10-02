---
product: journey optimizer
title: split
description: Erfahren Sie mehr über die Funktion „Aufspaltung“.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: Aufspaltung, Funktion, Ausdruck, Journey
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '69'
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
| Eingabezeichenfolge | Zeichenfolge |
| Trennzeichenfolge | Zeichenfolge |

## Signaturen und zurückgegebener Typ

`split(<input string>, <separator string>)`

Gibt eine listString zurück.

## Beispiel

`split("A_B_C", "_")`

Gibt `["A","B","C"]` zurück

Beispiel mit dem Ereignisfeld „event.appVersion“ mit dem Wert: 20.45.2.3434

`split(@event{event.appVersion}, "\\.")`

Gibt `["20", "45", "2", "3434"]` zurück
