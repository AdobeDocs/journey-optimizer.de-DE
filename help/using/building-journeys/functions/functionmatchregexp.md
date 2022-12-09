---
product: journey optimizer
title: matchRegExp
description: Erfahren Sie mehr über die Funktion matchRegExp
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 0%

---

# matchRegExp {#matchRegExp}

Gibt &quot;true&quot;zurück, wenn die Zeichenfolge im ersten Parameter mit dem regulären Ausdruck im zweiten Parameter übereinstimmt. Weitere Informationen finden Sie unter [diese Seite](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## Kategorie

Zeichenfolge

## Funktionssyntax

`matchRegExp(<parameters>)`

## Parameter

| Parameter | Typ |
|--- |--- |
| Zeichenfolge | Zeichenfolge |
| regexp | Zeichenfolge |

## Signatur und zurückgegebener Typ

`matchRegExp(<string>,<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`matchRegExp("username@adobe.com", "*adobe")`

Gibt &quot;true&quot;zurück.
