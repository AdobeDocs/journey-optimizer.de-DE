---
title: Funktionsbibliothek
description: Funktionsbibliothek
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 60%

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
