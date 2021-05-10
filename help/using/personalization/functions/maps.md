---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 5304db1456f0541d18823f862ae420892e46fd89
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# Zuordnungsfunktionen{#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) Angebote Funktionen, um die Interaktion mit Karten zu erleichtern.

## Get{#get}

Die Funktion `get` wird verwendet, um den Wert einer Zuordnung für einen bestimmten Schlüssel abzurufen.

**Format**

```sql
get({MAP},{STRING})
```

**Beispiel**

Der folgende Vorgang ruft den Wert der Identitätskarte für den Schlüssel `example@example.com` ab.

```sql
get(identityMap,"example@example.com")
```

## Schlüssel{#keys}

Die Funktion `keys` wird zum Abrufen aller Schlüssel für eine bestimmte Map verwendet.

**Format**

```sql
keys({MAP})
```

**Beispiel**

Der folgende Vorgang ruft alle Schlüssel für die Map ab.`identityMap`

```sql
keys(identityMap)
```

## Werte{#values}

Die Funktion `values` wird verwendet, um alle Werte einer angegebenen Map abzurufen.

**Format**

```sql
values({MAP})
```

**Beispiel**

Der folgende Vorgang ruft alle Werte für die Zuordnung ab.`identityMap`

```sql
values(identityMap)
```
