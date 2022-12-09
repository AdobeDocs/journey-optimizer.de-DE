---
product: journey optimizer
title: split
description: Informationen zur Funktionsaufteilung
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---

# split {#split}

Teilt die erste Argumentzeichenfolge mit einer Trennzeichenfolge (zweite Argumentzeichenfolge, die ein regulärer Ausdruck sein kann), um eine Liste von Zeichenfolgen (Token) zu erstellen.

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

`split(["A_B_C"], "_")`

Rückgabe `["A","B","C"]`

Beispiel mit dem Ereignisfeld &quot;event.appVersion&quot;mit Wert: &quot;20.45.2.3434&quot;

`split(@{event.appVersion}, "\\.")`

Rückgabe `["20", "45", "2", "3434"]`
