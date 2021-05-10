---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: ae0d32c271a77a859ee04d678c884e0203b6a256
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 6%

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

Die folgende PQL-Abfrage ruft den Wert der Identitätskarte für den Schlüssel `example@example.com` ab.

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

Die folgende PQL-Abfrage ruft alle Schlüssel für die Map `identityMap` ab.

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

Die folgende PQL-Abfrage ruft alle Werte für die Zuordnung ab.`identityMap`

```sql
values(identityMap)
```
