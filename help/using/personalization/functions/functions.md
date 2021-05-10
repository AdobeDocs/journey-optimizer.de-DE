---
title: Bibliothek mit Hilfsfunktionen
description: Journey Optimizer Helper-Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 4f097636e059c5d0676b0129cdbdb125e5ad9415
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 8%

---


# Vorbereiten von Sprache- und Hilfsfunktionen {#functionsL}

![](../../assets/do-not-localize/badge.png)


## Grundlagen zur Vorlagensprache

Verwenden Sie die Journey Optimizer-Vorlagensprache, um Vorgänge mit Daten wie Berechnungen, Datenformatierungen oder Konvertierungen, Bedingungen und deren Bearbeitung im Zusammenhang mit der Personalisierung durchzuführen.

Die verfügbaren Funktionen sind auf den folgenden Seiten aufgeführt:

* [Operatoren](operators.md)
* [Aggregation](aggregation.md)
* [Arrays und Listen](arrays-list.md)
* [Mathematisch](maths.md)
* [Karten](maps.md)
* [Objekte](objects.md)
* [String ](string.md)

Die Vorlagensprache wird bei Hilfsfunktionen genutzt, die in der Dropdown-Liste Personalisierung des Ausdruck-Editors verfügbar sind.

![](../assets/access-helper-functions.png)

Sie sind in drei Kategorien unterteilt: Funktionen, Helfer und Bediener

### Funktionen

**Array-Funktionen**

* [Durchschnittlich](aggregation.md#average)
* [Count](aggregation.md#count)
* [Unterscheiden](arrays-list.md#distinct)
* [Erster Posten](arrays-list.md#head)  (Kopf)
* [Erstes n im Array](arrays-list.md#first-n)  (topN)
* [In](arrays-list.md#in)
* [Enthält](arrays-list.md#includes)
* [Intersekten](arrays-list.md#intersects)
* [Letztes n im Array](arrays-list.md#last-n)  (lastN)
* [Maximum](aggregation.md#maximum) (max.)
* [Minimum](aggregation.md#minimum)  (min)
* [Not in](arrays-list.md#notin) (notIn)
* [Untergruppe von](arrays-list.md#subset)
* Sum
* [Superset](arrays-list.md#superset)

**Funktionen zuordnen**

* [Get](maps.md#get)
* [Schlüssel](maps.md#keys)
* [Werte](maps.md#values)

**Objektfunktionen**

* [Ist nicht null](objects.md#isNotNull)
* [Ist null](objects.md#isNull)

**Zeichenfolgen-Funktionen**

* Camel Case
* Concat
* [Enthält](string.md#contains)
* [Enthält nicht](string.md#doesNotContain)
* [Endet nicht mit](string.md#doesNotEndWith)
* [Beginnt nicht mit](string.md#doesNotStartWith)
* Encode64
* [Endet mit](string.md#endsWith)
* [Gleich](string.md#equals)
* EqualsIgnoreCase
* IsEmpty
* Length
* [Ist wie](string.md#like)
* [Kleinbuchstabe](#lower)
* [Übereinstimmungen](string.md#matches)
* MD5
* [Ungleich](string.md#notEqualTo)
* [Reguläre Ausdruck-Gruppe](string.md#regexGroup) (regexGroup)
* Replace
* ReplaceAll
* Aufspaltung
* [Beginnt mit](string.md#startsWith)
* Titelfall
* Beschneiden
* [Großbuchstabe](#upper)

### Helfer

* [Jeder](../personalization-syntax.md#each)
* [if](../personalization-syntax.md#if)
* let
* [not](../personalization-syntax.md#unless)
* [durch](../personalization-syntax.md#with)

### Benutzer

Diese Operatoren können nur mit Zahlen verwendet werden.

* [Addition](maths.md#add) (+) - Dieser Operator fügt zwei Zahlen hinzu
* [Und](operators.md#and) (und) - Dieser Operator erstellt eine logische Verbindung
* [Division](maths.md#divide) (/) - Dieser Operator wird verwendet, um den Quotient aus zwei Zahlen zu finden.
* [Entspricht](operators.md#and) (=) - Dieser Vorgang überprüft, ob die Werte gleich sind
* [Größer als](operators.md#greaterthan) (>) - Dieser Operator prüft, ob der erste Wert größer als der zweite ist
* [Größer oder gleich](operators.md#greaterthanorequal)  (>=) - Dieser Operator prüft, ob der erste Wert größer oder gleich dem zweiten Wert ist
* [Multiplikation](maths.md#multiply) (*) - Dieser Operator multipliziert zwei Zahlen
* [Negation](operators.md#not) (!) - Dieser Operator erstellt eine logische Negation
* [Nicht gleich](operators.md#notequal)  (=!) - Dieser Operator prüft, ob der angegebene Ausdruck nicht gleich dem Wert ist
* [Oder](operators.md#or)  (oder) - Dieser Operator erstellt eine logische Trennung
* [Remainder](maths.md#remainder) (%) - Dieser Operator wird zur Berechnung der verbleibenden Werte nach der Division zweier Zahlen verwendet
* Kleiner als (&lt;) - Dieser Operator prüft, ob der erste Wert kleiner als der zweite ist
* Kleiner oder gleich (&lt;=) - Dieser Operator prüft, ob der erste Wert kleiner oder gleich dem zweiten Wert ist
* [Subtraktion](maths.md#substract) (-) - Dieser Operator ersetzt zwei Zahlen

## Funktionen

### Kleinbuchstabe{#lower}

Die Funktion **lowerCase** wandelt eine Zeichenfolge in Kleinbuchstaben um.

Syntax:

```sql
{%=lowerCase(string)%}
```

Beispiel:

Diese Funktion wandelt den Vornamen des Profils in Kleinbuchstaben um.

```sql
{%=lowerCase(profile.person.name.firstName)%}
```

### Großbuchstabe{#upper}

Die Funktion **upper** wandelt eine Zeichenfolge in Kleinbuchstaben um.

Syntax:

```sql
{%=upperCase(string)%}
```

Beispiel:

Diese Funktion wandelt den Nachnamen des Profils in Großbuchstaben um.

```sql
{%=upperCase(profile.person.name.lastName)%}
```
