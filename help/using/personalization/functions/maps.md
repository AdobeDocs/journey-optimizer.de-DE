---
title: Bibliothek mit Zuordnungsfunktionen
description: Bibliothek mit Zuordnungsfunktionen
feature: Personalisierung
topic: Personalisierung
role: Data Engineer
level: Experienced
source-git-commit: e3b7e80b72e6be71d5b38cd5507d20ad2e8ca8d4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 51%

---

# Zuordnungsfunktionen{#maps}

Verwenden Sie Zuordnungsfunktionen in der Personalisierung, um die Interaktion mit Karten zu erleichtern.

## Abrufen{#get}

Mit der `get`-Funktion wird der Wert einer Zuordnung für einen bestimmten Schlüssel abgerufen.

**Format**

```sql
{%= get(map, string) %}
```

**Beispiel**

Der folgende Vorgang ruft den Wert der Identitätszuordnung für den Schlüssel `example@example.com` ab.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Schlüssel{#keys}

Die `keys`-Funktion wird zum Abrufen aller Schlüssel einer gegebenen Zuordnung verwendet.

**Format**

```sql
{%= keys(map) %}
```

**Beispiel**

Der folgende Vorgang ruft alle Schlüssel für die Zuordnung `identityMap` ab.

```sql
{%= keys(identityMap) %}
```

## Werte{#values}

Die `values`-Funktion wird zum Abrufen aller Werte einer gegebenen Zuordnung verwendet.

**Format**

```sql
{%= values(map) %}
```

**Beispiel**

Der folgende Vorgang ruft alle Werte für die Zuordnung `identityMap` ab.

```sql
{%= values(identityMap) %}
```
