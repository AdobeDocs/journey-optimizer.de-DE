---
product: journey optimizer
title: intersect
description: Erfahren Sie mehr über die Funktion „function“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: intersect, Funktion, Ausdruck, Journey
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
source-git-commit: 49c3fd09d23e6394b6eff8ba4da71ed7bab8c82c
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 100%

---

# intersect{#intersect}

Gibt die gemeinsamen Werte in den beiden Eingabe-Listen zurück. Wenn eine der beiden Listen null ist, wird eine leere Liste zurückgegeben.

## Kategorie

Liste

## Funktionssyntax

`intersect(<parameters>)`

## Parameter

| Parameter | Typ |
|-----------|------------------|
| Liste 1 | Liste |
| Liste 2 | Liste  |

## Signaturen und zurückgegebene Typen

`intersect(listString,listString)`: listString
`intersect(listDecimal,listDecimal)`: listDecimal
`intersect(listInteger,listInteger)`: listInteger
`intersect(listDateTime,listDateTime)`: listDateTime
`intersect(listDateTimeOnly,listDateTimeOnly)`: listDateTimeOnly
`intersect(listDateOnly,listDateOnly)`: listDateOnly
`intersect(listDuration,listDuration)`: listDuration
`intersect(listBoolean,listBoolean)`: listBoolean

Gibt eine Liste zurück.

## Beispiele

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

Gibt [&quot;sports&quot;, &quot;news&quot; zurück]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "documentary"]
)
```

Gibt häufige Elemente zwischen Profil-Attributen und der angegebenen Liste von Kategorien zurück.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

Gibt häufige Elemente zwischen Profil-Attributen und angegebenem Ereignis-Feld zurück.
