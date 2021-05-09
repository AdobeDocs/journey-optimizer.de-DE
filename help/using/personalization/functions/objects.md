---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# Objektfunktionen {#objects}

![](../../assets/do-not-localize/badge.png)

## Ist null

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

## Ist nicht null

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
