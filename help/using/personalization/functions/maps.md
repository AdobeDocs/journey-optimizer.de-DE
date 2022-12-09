---
title: Bibliothek mit Zuordnungsfunktionen
description: Bibliothek mit Zuordnungsfunktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# Zuordnungsfunktionen{#maps}

Verwenden Sie Zuordnungsfunktionen in der Personalisierung, um die Interaktion mit Karten zu erleichtern.

## Get{#get}

Die `get` -Funktion wird verwendet, um den Wert einer Zuordnung für einen bestimmten Schlüssel abzurufen.

**Format**

```sql
{%= get(map, string) %}
```

**Beispiel**

Der folgende Vorgang ruft den Wert der Identitätszuordnung für den Schlüssel ab `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Schlüssel{#keys}

Die `keys` -Funktion verwendet wird, um alle Schlüssel für eine bestimmte Zuordnung abzurufen.

**Format**

```sql
{%= keys(map) %}
```

**Beispiel**

Der folgende Vorgang ruft alle Schlüssel für die Zuordnung ab `identityMap`.

```sql
{%= keys(identityMap) %}
```

## Werte{#values}

Die `values` -Funktion verwendet wird, um alle Werte einer gegebenen Zuordnung abzurufen.

**Format**

```sql
{%= values(map) %}
```

**Beispiel**

Der folgende Vorgang ruft alle Werte für die Zuordnung ab `identityMap`.

```sql
{%= values(identityMap) %}
```
