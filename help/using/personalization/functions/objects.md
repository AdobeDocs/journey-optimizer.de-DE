---
title: Bibliothek mit Objektfunktionen
description: Bibliothek mit Objektfunktionen
feature: Personalisierung
topic: Personalisierung
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 52%

---

# Objektfunktionen {#objects}

![](../../assets/do-not-localize/badge.png)

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
