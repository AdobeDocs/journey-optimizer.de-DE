---
title: Bibliothek mit Objektfunktionen
description: Bibliothek mit Objektfunktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 100%

---

# Objektfunktionen {#objects}

## Ist null{#isNull}

Die `isNull`-Funktion ermittelt, ob eine Objektreferenz nicht vorhanden ist.

**Syntax**

```sql
{%= isNull(object) %}
```

**Beispiel**

Mit dem folgenden Vorgang wird geprüft, ob die Privatadresse der Person nicht vorhanden ist.

```sql
{%= isNull(person.homeAddress) %}
```

## Ist nicht null{#isNotNull}

Die `isNotNull`-Funktion ermittelt, ob eine Objektreferenz nicht vorhanden ist.

**Syntax**

```sql
{%= isNotNull(object) %}
```

**Beispiel**

Mit dem folgenden Vorgang wird geprüft, ob die Privatadresse der Person vorhanden ist.

```sql
{%= isNotNull(person.homeAddress) %}
```
