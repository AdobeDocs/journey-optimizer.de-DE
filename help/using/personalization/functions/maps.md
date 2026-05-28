---
title: Bibliothek mit Zuordnungsfunktionen
description: Bibliothek mit Zuordnungsfunktionen
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
TQID: https://experienceleague.adobe.com/KeitEe0NQxxc-snCyWSGlov-OyUgiva6ddzrCTxEKSs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 102
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
