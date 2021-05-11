---
title: Bibliothek mit Hilfsfunktionen
description: Journey Optimizer Helper-Funktionsbibliothek
translation-type: tm+mt
source-git-commit: 3fa63e103c2185062ff779c35d19387aea523f62
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---


# Vorbereiten von Sprache- und Hilfsfunktionen {#functionsL}

![](../../assets/do-not-localize/badge.png)


## Grundlagen zur Vorlagensprache

Verwenden Sie die Journey Optimizer-Vorlagensprache, um Vorgänge mit Daten wie Berechnungen, Datenformatierungen oder Konvertierungen, Bedingungen und deren Bearbeitung im Zusammenhang mit der Personalisierung durchzuführen.

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

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Ist nicht null</a> (isNotNull)</td><td>Mit dieser Funktion wird bestimmt, ob eine Objektreferenz vorhanden ist</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">Ist null</a> (isNull)</td><td>Mit dieser Funktion wird bestimmt, ob keine Objektreferenz vorhanden ist</td>
    </tr>
</table>

**Zeichenfolgen-Funktionen**

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Camel Case</a> (camelCase)</td><td>Diese Funktion wird verwendet, um</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">Concat</a> (Concat)</td><td>Diese Funktion wird verwendet, um</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Enthält</a> (enthält)</td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge eine angegebene Unterzeichenfolge enthält</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Enthält</a>  nicht (doesNotContain)</td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge keine angegebene Unterzeichenfolge enthält</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">endet nicht mit</a> (doesNotEndWith)</td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge endet</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">Beginn nicht mit</a> (doesNotStartWith)</td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge Beginn</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Encode64</a> ()</td><td>Diese Funktion wird verwendet, um</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Endet mit</a> (endsWith)</td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge endet.</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Gleich</a> (=)</td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge Beginn</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">EqualsIgnoreCase</a> ()</td><td>Diese Funktion wird verwendet, um</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">IsEmpty</a> ()</td><td>Diese Funktion wird verwendet, um </td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Length</a> ()</td><td>Diese Funktion wird verwendet, um</td>
    </tr>
    <tr>
        <td><a href="string.md#like">like</a>  (like)</td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge einem angegebenen Muster entspricht</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Kleinbuchstabe</a> (Kleinbuchstabe)</td><td>Diese Funktion konvertiert eine Zeichenfolge in Kleinbuchstaben</td>
    </tr>
    </tr>
    <tr>
        <td><a href="string.md#matches">Übereinstimmungen</a>  (Übereinstimmungen)</td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einem bestimmten regulären Ausdruck übereinstimmt</td>
    </tr>
    <tr>
        <td><a href="string.md#like">MD5</a> ()</td><td>Diese Funktion wird verwendet, um </td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">ungleich</a> (notEqualsTo)</td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge nicht der angegebenen Zeichenfolge entspricht</td>
    </tr>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Reguläre Ausdruck-Gruppe</a> (regexGroup)</td><td>Diese Funktion wird verwendet, um spezifische Informationen basierend auf dem regulären Ausdruck zu extrahieren, der bereitgestellt wird.</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Ersetzen</a>  (Ersetzen)</td><td>Diese Funktion wird verwendet, um </td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Alle</a>  ersetzen(replaceAll)</td><td>Diese Funktion wird verwendet, um</td>
    </tr>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Teilen</a>  (geteilt)</td><td>Diese Funktion wird verwendet, um</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Beginn mit</a> (startsWith)</td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge Beginn</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Fall</a>  des Titels (titleCase)</td><td>Diese Funktion wird verwendet, um</td>
    </tr>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Trim</a> (trim)</td><td>Diese Funktion wird verwendet, um</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Großbuchstabe</a> (Großbuchstabe)</td><td>Diese Funktion konvertiert eine Zeichenfolge in Großbuchstaben</td>
    </tr>
</table>

### Helfer{#helper-helper}

* Alle - [Weitere Informationen](../personalization-syntax.md#each)
* If - [Weitere Informationen](../personalization-syntax.md#if)
* Let - Weitere Informationen
* Außer - [Weitere Informationen](../personalization-syntax.md#unless)
* Mit - [Weitere Informationen](../personalization-syntax.md#with)

### Benutzer{#operators-helper}

Diese Operatoren können nur mit Zahlen verwendet werden.

<table>
    <tr>
        <td><a href="operators.md#add">Zusatz</a> ('+')</td><td>Dieser Operator fügt zwei Zahlen hinzu</td>
    </tr>
    <tr>
        <td><a href="operators.md#and">Und</a> (und)</td><td>Dieser Operator erstellt eine logische Verbindung</td>
    <tr>
        <td><a href="operators.md#divide">Divide</a> (/)</td><td>Dieser Operator wird verwendet, um die Quotient aus zwei Zahlen zu finden.</td>
    </tr>
    <tr>
        <td><a href="operators.md#and">Entspricht</a> (=)</td><td>Dieser Vorgang überprüft, ob Werte gleich sind</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Größer als</a> ()</td><td>Dieser Operator prüft, ob der erste Wert größer als der zweite ist</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Größer oder gleich</a>  (=&gt;)</td><td>Dieser Operator prüft, ob der erste Wert größer oder gleich dem zweiten Wert ist</td>
    </tr>
    <tr>
        <td><a href="operators.md#multiply">Multiplikation</a> (*)</td><td>Dieser Operator multipliziert zwei Zahlen</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Negation</a> (!)</td><td>Dieser Operator erstellt eine logische Negation</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">Nicht gleich</a>  (=!)</td><td>Dieser Operator prüft, ob der angegebene Ausdruck nicht gleich dem Wert gibt</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">Oder</a> (oder)</td><td>Dieser Operator erstellt eine logische Trennung</td>
    </tr>
    <tr>
        <td><a href="operators.md#remainder">Remainder</a> (%)</td><td>Dieser Operator wird verwendet, um die verbleibenden Elemente nach der Division zweier Zahlen zu berechnen.</td>
    </tr>
    <tr>
        <td><a href="operators.md#remainder">Kleiner als</a> ()</td><td>Dieser Operator prüft, ob der erste Wert kleiner als der zweite ist</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Kleiner oder gleich</a> ()</td><td>Dieser Operator prüft, ob der erste Wert kleiner als oder gleich dem zweiten Wert ist</td>
    </tr>
    <tr>
        <td><a href="operators.md#substract">Substraction</a> ()</td><td>Dieser Operator ersetzt zwei Zahlen</td>
    </tr>
</table>
