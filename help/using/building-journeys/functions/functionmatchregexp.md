---
product: journey optimizer
title: matchRegExp
description: Erfahren Sie mehr über die Funktion „matchRegExp“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: matchRegExp, Funktion, Ausdruck, Journey
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: 9e6b3fc5c91e360a9bd7e727949ac5445cd79654
workflow-type: ht
source-wordcount: '56'
ht-degree: 100%

---

# matchRegExp {#matchRegExp}

Gibt „true“ zurück, wenn die Zeichenfolge im ersten Parameter mit dem regulären Ausdruck im zweiten Parameter übereinstimmt. Weitere Informationen finden Sie auf [dieser Seite](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## Kategorie

Zeichenfolge

## Funktionssyntax

`matchRegExp(<parameters>)`

## Parameter

| Parameter | Typ |
|--- |--- |
| string | string |
| regexp | string |

## Signatur und zurückgegebener Typ

`matchRegExp(<string>,<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`matchRegExp("12345", "\\d+")`

Gibt „true“ zurück.
