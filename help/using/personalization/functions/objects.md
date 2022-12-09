---
title: Bibliothek mit Objektfunktionen
description: Bibliothek mit Objektfunktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# Objektfunktionen {#objects}

## Is null{#isNull}

Die `isNull` bestimmt, ob keine Objektreferenz vorhanden ist.

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

Die `isNotNull` bestimmt, ob eine Objektreferenz vorhanden ist.

**Format**

```sql
{%= isNotNull(object) %}
```

**Beispiel**

Der folgende Vorgang prüft, ob die Privatadresse der Person vorhanden ist.

```sql
{%= isNotNull(person.homeAddress) %}
```
