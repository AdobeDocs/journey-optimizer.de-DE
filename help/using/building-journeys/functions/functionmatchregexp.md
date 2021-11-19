---
product: adobe campaign
title: matchRegExp
description: Erfahren Sie mehr über die Funktion „matchRegExp“
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 4695c88b4372a0f2a804bef268ae6f2d39eb2f0b
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 100%

---

# matchRegExp {#matchRegExp}

Gibt „true“ zurück, wenn die Zeichenfolge im ersten Parameter mit dem regulären Ausdruck im zweiten Parameter übereinstimmt. Weiterführende Informationen finden Sie auf [dieser Seite](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## Kategorie

Zeichenfolge

## Funktionssyntax

`matchRegExp(<parameters>)`

## Parameter

| Parameter | Typ |
|--- |--- |
| string | Zeichenfolge |
| regexp | Zeichenfolge |

## Signatur und zurückgegebener Typ

`matchRegExp(<string>,<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`matchRegExp("username@adobe.com", "*adobe")`

Gibt „true“ zurück.
