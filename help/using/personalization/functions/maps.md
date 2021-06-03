---
title: Funktionsbibliothek
description: Funktionsbibliothek
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 66%

---

# Zuordnungsfunktionen{#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) bietet Funktionen, die die Interaktion mit Zuordnungen erleichtern.

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
