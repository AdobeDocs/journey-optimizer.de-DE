---
title: Bibliothek mit Objektfunktionen
description: Bibliothek mit Objektfunktionen
feature: Personalisierung
topic: Personalisierung
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 52%

---

# Objektfunktionen {#objects}

## Is null{#isNull}

Die `isNull`-Funktion ermittelt, ob eine Objektreferenz nicht vorhanden ist.

**Format**

```sql
{%= isNull(object) %}
```

**Beispiel**

Der folgende Vorgang prüft, ob die Privatadresse der Person nicht vorhanden ist.

```sql
{%= isNull(person.homeAddress) %}
```

## Is not null{#isNotNull}

Die `isNotNull`-Funktion ermittelt, ob eine Objektreferenz nicht vorhanden ist.

**Format**

```sql
{%= isNotNull(object) %}
```

**Beispiel**

Der folgende Vorgang prüft, ob die Privatadresse der Person vorhanden ist.

```sql
{%= isNotNull(person.homeAddress) %}
```
