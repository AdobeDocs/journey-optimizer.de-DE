---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 85%

---

# Zuordnungsfunktionen {#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) Angebote Funktionen, um die Interaktion mit Karten zu erleichtern.

## Abrufen

Mit der `get`-Funktion wird der Wert einer Zuordnung für einen bestimmten Schlüssel abgerufen.

**Format**

```sql
get({MAP},{STRING})
```

**Beispiel**

Die folgende PQL-Abfrage ruft den Wert der dentitätszuordnung für den Schlüssel `example@example.com` ab.

```sql
get(identityMap,"example@example.com")
```

## Schlüssel

Die `keys`-Funktion wird zum Abrufen aller Schlüssel einer gegebenen Zuordnung verwendet.

**Format**

```sql
keys({MAP})
```

**Beispiel**

Die folgende PQL-Abfrage ruft alle Schlüssel für die `identityMap`-Zuordnung ab.

```sql
keys(identityMap)
```

## Werte

Die `values`-Funktion wird zum Abrufen aller Werte einer gegebenen Zuordnung verwendet.

**Format**

```sql
values({MAP})
```

**Beispiel**

Die folgende PQL-Abfrage ruft alle Werte für die `identityMap`-Zuordnung ab.

```sql
values(identityMap)
```
