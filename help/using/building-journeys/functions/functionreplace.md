---
product: journey optimizer
title: replace
description: Erfahren Sie mehr über den Funktionsaustausch
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# replace {#replace}

Ersetzt das erste Auftreten, das mit der Zielzeichenfolge übereinstimmt, durch die Ersatzzeichenfolge in der Basiszeichenfolge.

Die Ersetzung erfolgt vom Anfang der Zeichenfolge bis zum Ende, z. B. führt das Ersetzen von &quot;aa&quot;durch &quot;b&quot;in der Zeichenfolge &quot;aaa&quot;zu &quot;ba&quot;anstelle von &quot;ab&quot;.

## Kategorie

Zeichenfolge

## Funktionssyntax

`replace(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|--------------|
| base | Zeichenfolge |
| target | string (RegExp) |
| replacement | Zeichenfolge |

## Signatur und zurückgegebener Typ

`replace(<base>,<target>,<replacement>)`

Gibt eine Zeichenfolge zurück.

## Beispiel 1

`replace("Hello World", "l", "x")`

Gibt &quot;Hexlo World&quot;zurück.

## Beispiel 2 {#example_2}

Da der Zielparameter eine RegExp ist, müssen Sie je nach der Zeichenfolge, die Sie ersetzen möchten, möglicherweise einige Zeichen maskieren. Im Folgenden finden Sie ein Beispiel:

* auszuwertende Zeichenfolge: `|OFFER_A|OFFER_B`
* bereitgestellt von einem Profilattribut `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* Zeichenfolge, die ersetzt werden soll: `|OFFER_A`
* Zeichenfolge ersetzt durch: `''`
* Sie müssen `\\` vor `|` Zeichen.

Der Ausdruck lautet:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

Die zurückgegebene Zeichenfolge lautet: `|OFFER_B`

Sie können auch die Zeichenfolge erstellen, die aus einem bestimmten Attribut ersetzt werden soll:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`
