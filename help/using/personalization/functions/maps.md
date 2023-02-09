---
title: Bibliothek mit Zuordnungsfunktionen
description: Bibliothek mit Zuordnungsfunktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 100%

---

# Zuordnungsfunktionen{#maps}

Verwenden Sie Zuordnungsfunktionen in der Personalisierung, um die Interaktion mit Zuordnungen zu erleichtern.

## Abrufen{#get}

Mit der `get`-Funktion wird der Wert einer Zuordnung für einen bestimmten Schlüssel abgerufen.

**Syntax**

```sql
{%= get(map, string) %}
```

**Beispiel**

Die folgende Operation ruft den Wert der Identitätszuordnung für den Schlüssel `example@example.com` ab.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Schlüssel{#keys}

Die `keys`-Funktion wird zum Abrufen aller Schlüssel einer gegebenen Zuordnung verwendet.

**Syntax**

```sql
{%= keys(map) %}
```

**Beispiel**

Die folgende Operation ruft alle Schlüssel für die Zuordnung `identityMap` ab.

```sql
{%= keys(identityMap) %}
```

## Werte{#values}

Die `values`-Funktion wird zum Abrufen aller Werte einer gegebenen Zuordnung verwendet.

**Syntax**

```sql
{%= values(map) %}
```

**Beispiel**

Die folgende Operation ruft alle Werte für die Zuordnung `identityMap` ab.

```sql
{%= values(identityMap) %}
```
