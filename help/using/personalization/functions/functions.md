---
title: Bibliothek mit Hilfsfunktionen
description: Journey Optimizer Helper-Funktionsbibliothek
translation-type: tm+mt
source-git-commit: e6d736ee9c1b2c83ce510d6ee96a133814a8c463
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 1%

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

Sie sind in drei Kategorien unterteilt: [Funktionen](#functions-helper), [Helper](#helper-helper) und [Operatoren](#operators-helper).

### Funktionen{#functions-helper}

**Array-Funktionen**

<table>
    <tr>
        <td><a href="aggregation.md#average">Durchschnitt</a> (Durchschnitt)</td><td>Diese Funktion gibt das arithmetische Mittel aller ausgewählten Werte im Array zurück</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">In</a> (in)</td><td>Mit dieser Funktion wird bestimmt, ob ein Element Mitglied eines Arrays oder einer Liste ist</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimum</a>  (min)</td><td>Diese Funktion gibt die kleinsten aller ausgewählten Werte im Array zurück</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Anzahl</a>  (Anzahl)</td><td>Diese Funktion gibt die Anzahl der Elemente innerhalb des angegebenen Arrays zurück</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Enthält</a>  (einschließlich)</td><td>Diese Funktion bestimmt, ob ein Array oder eine Liste ein bestimmtes Element enthält</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Not in</a> (notIn)</td><td>Diese Funktion bestimmt, ob ein Element kein Element eines Arrays oder einer Liste ist.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinct</a> (different)</td><td>Diese Funktion ruft Werte aus einem Array oder einer Liste mit entfernten Duplikaten ab.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersects</a> (intersects)</td><td>Diese Funktion ermittelt, ob zwei Arrays oder Listen mindestens ein gemeinsames Mitglied haben</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Untergruppe von</a> (UntergruppeOf)</td><td>Diese Funktion bestimmt, ob ein bestimmtes Array (Array A) eine Untergruppe eines anderen Arrays (Array B) ist, d. h. wenn alle Elemente im Array A Elemente des Arrays B sind</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Erster Posten</a>  (Kopf)</td><td>Diese Funktion gibt das erste Element im Array oder in der Liste zurück</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Letztes n im Array</a>  (lastN)</td><td>Diese Funktion gibt die letzten "N"-Elemente in einem Array zurück, wenn sie in aufsteigender Reihenfolge nach dem angegebenen numerischen Ausdruck sortiert werden</td>
    </tr>
    <tr>
        <td>Sum</td><td></td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Erstes n im Array</a>  (topN)</td><td>Diese Funktion gibt die ersten "N"-Elemente in einem Array zurück, wenn sie in aufsteigender Reihenfolge nach dem angegebenen numerischen Ausdruck sortiert werden</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Maximum</a> (max.)</td><td>Diese Funktion gibt den größten der ausgewählten Werte im Array zurück</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superset of</a> (supersetOf)</td><td>Diese Funktion wird beendet, wenn ein bestimmtes Array (Array A) eine Übermenge eines anderen Arrays (Array B) ist, d. h. wenn dieses Array A alle Elemente im Array B enthält.</td>
    </tr>
</table>


**Funktionen zuordnen**

<table>
    <tr>
        <td><a href="maps.md#get">Get</a> (get)</td><td>Diese Funktion wird zum Abrufen des Wertes einer Zuordnung für einen bestimmten Schlüssel verwendet</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Schlüssel</a> (Schlüssel)</td><td>Mit dieser Funktion werden alle Schlüssel für eine bestimmte Zuordnung abgerufen</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Werte</a> (Werte)</td><td>Diese Funktion ruft alle Werte einer angegebenen Map ab</td>
    </tr>
</table>

**Objektfunktionen**

* [Ist nicht null](objects.md#isNotNull)
* [Ist null](objects.md#isNull)

**Zeichenfolgen-Funktionen**

<table>
    <tr>
        <td>Camel Case</td>
        <td>Concat</td>
        <td>[Enthält](string.md#contains)</td>
    </tr>
    <tr>
        <td>[Enthält nicht](string.md#doesNotContain)</td>
        <td>[Endet nicht mit](string.md#doesNotEndWith)</td>
        <td>[Beginn nicht mit](string.md#doesNotStartWith)</td>
    </tr>
    <tr>
        <td>Encode64</td>
        <td>[Ends with](string.md#endsWith)</td>
        <td>[Gleich](string.md#equals)</td>
    </tr>
    <tr>
        <td>EqualsIgnoreCase</td>
        <td>IsEmpty</td>
        <td>Length</td>
    </tr>
    <tr>
        <td>[like](string.md#like)</td>
        <td>[Kleinbuchstabe](string.md#lower)</td>
        <td>[Übereinstimmungen](string.md#match)</td>
    </tr>
    <tr>
        <td> MD5</td>
        <td>[Nicht gleich](string.md#notEqualTo)</td>
        <td>[Reguläre Ausdruck-Gruppe](string.md#regexGroup) (regexGroup)</td>
    </tr>
    <tr>
        <td>Replace</td><td>ReplaceAll</td>
        <td>Aufspaltung</td>
        <td>[Beginn mit](string.md#startsWith)</td>
    </tr>
    <tr>
        <td>Titelfall</td>
        <td>Beschneiden</td>
        <td>[Großbuchstabe](string.md#upper)</td>
    </tr>
</table>

### Helfer{#helper-helper}

* [Jeder](../personalization-syntax.md#each)
* [if](../personalization-syntax.md#if)
* let
* [not](../personalization-syntax.md#unless)
* [durch](../personalization-syntax.md#with)

### Benutzer{#operators-helper}

Diese Operatoren können nur mit Zahlen verwendet werden.

<table>
    <tr>
        <td>[Zusatz](maths.md#add) (+)</td>
        <td>Dieser Operator fügt zwei Zahlen hinzu</td>
    </tr>
    <tr>
        <td>[Und](operator.md#and) (und)</td>
        <td>Dieser Operator erstellt eine logische Verbindung</td>
    </tr>
    <tr>
        <td>[Division](maths.md#divide) (/)</td>
        <td>Dieser Operator wird verwendet, um die Quotient aus zwei Zahlen zu finden.</td>
    </tr>
    <tr>
        <td>[Entspricht](operator.md#and) (=)</td>
        <td>Dieser Vorgang überprüft, ob Werte gleich sind</td>
    </tr>
    <tr>
        <td>[Größer als](operator.md#greaterthan)</td>
        <td>Dieser Operator prüft, ob der erste Wert größer als der zweite ist</td>
    </tr>
    <tr>
        <td>[Größer oder gleich](operator.md#greaterthanorequal)</td>
        <td>Dieser Operator prüft, ob der erste Wert größer oder gleich dem zweiten Wert ist</td>
    </tr>
    <tr>
        <td>[Multiplikation](maths.md#multiply) (*) </td>
        <td>Dieser Operator multipliziert zwei Zahlen</td>
    </tr>
    <tr>
        <td>[Negation](operator.md#not) (!) </td>
        <td>Dieser Operator erstellt eine logische Negation</td>
    </tr>
    <tr>
        <td>[Nicht gleich](operator.md#notequal) (=!) </td>
        <td>Dieser Operator prüft, ob der angegebene Ausdruck nicht gleich dem Wert gibt</td>
    </tr>
    <tr>
        <td>[Oder](operator.md#or) (oder) </td>
        <td>Dieser Operator erstellt eine logische Trennung</td>
    </tr>
    <tr>
        <td>[Rest](maths.md#rest) (%) </td>
        <td>Dieser Operator wird verwendet, um die verbleibenden Elemente nach der Division zweier Zahlen zu berechnen.</td>
    </tr>
    <tr>
        <td>Kleiner als</td>
        <td>Dieser Operator prüft, ob der erste Wert kleiner als der zweite ist</td>
    </tr>
    <tr>
        <td>Kleiner oder gleich</td>
        <td>Dieser Operator prüft, ob der erste Wert kleiner oder gleich dem zweiten Wert ist</td>
    </tr>
    <tr>
        <td>[Substraction](maths.md#substract) (-) </td>
        <td>Dieser Operator ersetzt zwei Zahlen</td>
    </tr>
</table>
