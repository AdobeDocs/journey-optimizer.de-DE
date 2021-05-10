---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: ae0d32c271a77a859ee04d678c884e0203b6a256
workflow-type: tm+mt
source-wordcount: '57'
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

Die folgende PQL-Abfrage prüft, ob die Privatadresse der Person nicht vorhanden ist.

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

Die folgende PQL-Abfrage prüft, ob die Privatadresse der Person vorhanden ist.

```sql
isNotNull(person.homeAddress)
```
