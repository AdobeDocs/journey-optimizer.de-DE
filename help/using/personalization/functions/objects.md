---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 5304db1456f0541d18823f862ae420892e46fd89
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 7%

---

# Objektfunktionen {#objects}

![](../../assets/do-not-localize/badge.png)

## Ist null{#isNull}

Die Funktion `isNull` bestimmt, ob keine Objektreferenz vorhanden ist.

**Format**

```sql
isNull({OBJECT})
```

**Beispiel**

Der folgende Vorgang überprüft, ob die Heimatadresse der Person nicht vorhanden ist.

```sql
isNull(person.homeAddress)
```

## Ist nicht null{#isNotNull}

Die Funktion `isNotNull` bestimmt, ob eine Objektreferenz vorhanden ist.

**Format**

```sql
isNotNull({OBJECT})
```

**Beispiel**

Der folgende Vorgang prüft, ob die Privatadresse der Person vorhanden ist.

```sql
isNotNull(person.homeAddress)
```
