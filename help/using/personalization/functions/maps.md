---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Zuordnungsfunktionen {#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) Angebote Funktionen, um die Interaktion mit Karten zu erleichtern.

## Get

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

## Schlüssel

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

## Werte

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
