---
title: Bibliothek für Hilfsfunktionen
description: Journey Optimizer Helper-Funktionsbibliothek
feature: Personalisierung
topic: Personalisierung
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 6%

---


# Vorlagensprache und Hilfsfunktionen {#functionsL}

![](../../assets/do-not-localize/badge.png)

Verwenden Sie die Vorlagensprache [!DNL Journey Optimizer], um Datenvorgänge wie Berechnungen, Datenformatierung oder Konvertierungen, Bedingungen und deren Bearbeitung im Kontext der Personalisierung durchzuführen. Hier erfahren Sie die Richtlinien zur Personalisierungssyntax in [dieser Seite](../personalization-syntax.md).

Die Vorlagensprache wird in Hilfsfunktionen verwendet, die in der Dropdown-Liste &quot;Personalisierung&quot;des Ausdruckseditors verfügbar sind, wie unten gezeigt:

![](../assets/access-helper-functions.png)

Im Ausdruckseditor sind Hilfsfunktionen in drei Kategorien unterteilt: [Funktionen](#functions-helper), [Helfer](#helper-helper) und [Operatoren](#operators-helper).[!DNL Journey Optimizer]

## Funktionen{#functions-helper}

**Array-Funktionen**

<table>
    <tr>
        <td><a href="aggregation.md#average">Durchschnitt</a></td><td>Diese Funktion gibt das arithmetische Mittel aller im Array ausgewählten Werte zurück</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">Enthalten</a></td><td>Mit dieser Funktion wird bestimmt, ob ein Element einem Array oder einer Liste angehört</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimum</a></td><td>Diese Funktion gibt die kleinsten aller ausgewählten Werte im Array zurück</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Anzahl</a></td><td>Diese Funktion gibt die Anzahl der Elemente innerhalb des angegebenen Arrays zurück</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Enthält</a></td><td>Diese Funktion bestimmt, ob ein Array oder eine Liste ein bestimmtes Element enthält</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Nicht enthalten</a></td><td>Diese Funktion bestimmt, ob ein Element nicht Mitglied eines Arrays oder einer Liste ist</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Verschieden</a></td><td>Diese Funktion ruft Werte aus einem Array oder einer Liste mit entfernten doppelten Werten ab</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Schnittmengen</a></td><td>Diese Funktion ermittelt, ob zwei Arrays oder Listen mindestens ein gemeinsames Element aufweisen</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Teilmenge von</a></td><td>Diese Funktion bestimmt, ob ein bestimmtes Array (Array A) eine Teilmenge eines anderen Arrays (Array B) ist, d. h. ob alle Elemente in Array A Elemente des Arrays B sind</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Erstes Element</a></td><td>Diese Funktion gibt das erste Element in einem Array oder einer Liste zurück</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Letzte n im Array</a></td><td>Diese Funktion gibt die letzten N-Elemente in einem Array zurück, wenn sie anhand des angegebenen numerischen Ausdrucks in aufsteigender Reihenfolge sortiert werden</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Summe</a></td><td>Diese Funktion gibt die Summe aller im Array ausgewählten Werte zurück</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Erste n im Array</a></td><td>Diese Funktion gibt die ersten "N"-Elemente in einem Array zurück, wenn sie anhand des angegebenen numerischen Ausdrucks in aufsteigender Reihenfolge sortiert werden</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Maximum</a></td><td>Diese Funktion gibt den größten aller ausgewählten Werte innerhalb eines Arrays zurück</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Obermenge</a></td><td>Diese Funktion wird beendet, wenn ein bestimmtes Array (Array A) eine Obermenge eines anderen Arrays (Array B) ist, d. h. wenn dieses Array A alle Elemente in Array B enthält</td>
    </tr>
</table>


**Zuordnungsfunktionen**

<table>
    <tr>
        <td><a href="maps.md#get">Abrufen</a></td><td>Mit dieser Funktion wird der Wert einer Zuordnung für einen bestimmten Schlüssel abgerufen</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Schlüssel</a></td><td>Mit dieser Funktion werden alle Schlüssel für eine bestimmte Zuordnung abgerufen</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Werte</a></td><td>Diese Funktion ruft alle Werte einer gegebenen Zuordnung ab</td>
    </tr>
</table>

**Objektfunktionen**

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Is not null</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Objektreferenz vorhanden ist</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">Is null</a></td><td>Mit dieser Funktion wird bestimmt, ob keine Objektreferenz vorhanden ist</td>
    </tr>
</table>

**Zeichenfolgen-Funktionen**

<table>
    <tr>
        <td><a href="string.md#camelCase">Camel Case</a></td><td>Mit dieser Funktion wird der erste Buchstabe jedes Wortes einer Zeichenfolge großgeschrieben</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concat</a></td><td>Mit dieser Funktion werden zwei Zeichenfolgen zu einer</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Enthält</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge eine angegebene Unterzeichenfolge enthält</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Enthält nicht</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge keine angegebene Unterzeichenfolge enthält</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">Endet nicht mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge endet.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">Beginnt nicht mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge nicht mit einer angegebenen Teilzeichenfolge beginnt</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">Kodierung 64</a></td><td>Mit dieser Funktion wird eine Zeichenfolge kodiert oder dekodiert</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Endet mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge endet.</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Gleich</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge beginnt, wobei Groß-/Kleinschreibung berücksichtigt wird.</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Entspricht Groß-/Kleinschreibung ignorieren</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge ohne Groß-/Kleinschreibung nicht mit einer angegebenen Unterzeichenfolge beginnt</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">E-Mail-Domäne extrahieren</a></td><td>Mit dieser Funktion wird die Domain einer E-Mail-Adresse extrahiert.</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>Mit dieser Funktion wird geprüft, ob eine Zeichenfolge oder ein Ausdruck leer ist.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Linker Schnitt</a></td><td>Diese Funktion entfernt Leerzeichen vom Anfang einer Zeichenfolge</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Length</a></td><td>Mit dieser Funktion wird die Anzahl der Zeichen in einer Zeichenfolge oder einem Ausdruck abgerufen</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Ist wie</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einem angegebenen Muster übereinstimmt</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Kleinbuchstabe</a></td><td>Diese Funktion konvertiert eine Zeichenfolge in Kleinbuchstaben</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Stimmt überein mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einem bestimmten regulären Ausdruck übereinstimmt</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Ungleich</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge nicht mit der angegebenen Zeichenfolge übereinstimmt</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Gruppe regelmäßiger Ausdrücke</a></td><td>Diese Funktion wird verwendet, um spezifische Informationen basierend auf dem bereitgestellten regulären Ausdruck zu extrahieren.</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Ersetzen</a></td><td>Diese Funktion ersetzt eine angegebene Teilzeichenfolge in einer Zeichenfolge durch eine andere Teilzeichenfolge</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">Alle ersetzen</a></td><td>Diese Funktion ersetzt alle Teilzeichenfolgen eines Textes, der mit der "target"übereinstimmt, durch die angegebene literale "replacement"-Zeichenfolge</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Rechter Schnitt</a></td><td>Diese Funktion entfernt Leerzeichen am Ende einer Zeichenfolge </td>
    </tr>
    <tr>
        <td><a href="string.md#split">Split</a></td><td>Mit dieser Funktion wird eine Zeichenfolge durch ein bestimmtes Zeichen aufgeteilt</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Beginnt mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge beginnt</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Titelschreibweise</a></td><td>Diese Funktion wird verwendet, um die ersten Buchstaben jedes Wortes einer Zeichenfolge großzuschreiben</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Zuschneiden</a></td><td>Diese Funktion entfernt Leerzeichen vom Anfang und vom Ende einer Zeichenfolge</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Großbuchstabe</a></td><td>Diese Funktion konvertiert eine Zeichenfolge in Großbuchstaben</td>
    </tr>
</table>


## Helper{#helper-helper}

Die Helfer werden auf [dieser Seite](helpers.md) beschrieben.


<table>
    <tr>
        <td><a href="helpers.md#each">Each</a></td><td>Diese Funktion wird verwendet, um über ein Array zu iterieren.</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">Wenn </a></td><td>Mit dieser Funktion wird ein bedingter Block definiert. Wenn die Ausdrucksauswertung "true"zurückgibt, wird der Block gerendert</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Let</a></td><td>Diese Funktion ermöglicht die Speicherung eines Ausdrucks als Variable, die später in einer Abfrage verwendet werden kann</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">Unless</a></td><td>Mit dieser Funktion wird ein bedingter Block definiert. Wenn die Ausdrucksauswertung "false"zurückgibt, wird der Block gerendert</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">With</a></td><td>Mit dieser Funktion wird das Bewertungstoken des Vorlagenteils geändert</td>
    </tr>
</table>

## Operatoren{#operators-helper}

### Arithmetische Funktionen {#arithmetic-helper}

Arithmetische Funktionen dienen der Durchführung grundlegender Berechnungen von Werten.

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">Zusatz</a></td><td>Dieser Operator wird verwendet, um die Summe zweier Argumentausdrücke zu finden.</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">Dividieren</a></td><td>Dieser Operator wird verwendet, um den Quotienten zweier Argumentausdrücke zu finden.</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">Multiplikation</a></td><td>Dieser Operator wird verwendet, um das Produkt zweier Argumentausdrücke zu finden.</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">Rest</a> </td><td>Dieser Operator wird verwendet, um den Rest nach der Division der beiden Argumentausdrücke zu finden.</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">Subtraktion</a> </td><td>Dieser Operator findet den Unterschied zwischen zwei Ausdrücken</td>
    </tr>
</table>


### Boolesche Funktionen

Boolesche Funktionen werden verwendet, um eine boolesche Logik für verschiedene Elemente durchzuführen.

<table>
    <tr>
        <td><a href="operators.md#and">Und</a></td><td>Dieser Operator erstellt ein logisches Bindeglied</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Wenn </a></td><td>Dieser Operator löst einen Ausdruck in Abhängigkeit davon auf, ob eine angegebene Bedingung wahr ist</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Nicht</a></td><td>Dieser Operator erstellt eine logische Negation</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">Oder</a></td><td>Dieser Operator erstellt eine logische Trennung</td>
    </tr>
</table>


### Vergleichsfunktionen

Vergleichsfunktionen werden verwendet, um zwischen verschiedenen Ausdrücken und Werten zu vergleichen und &quot;true&quot;oder &quot;false&quot;entsprechend zurückzugeben.

<table>
    <tr>
        <td><a href="operators.md#and">Gleich</a></td><td>Dieser Vorgang prüft, ob die Werte gleich sind</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Größer als</a></td><td>Dieser Operator prüft, ob der erste Wert größer als der zweite Wert ist</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Größer oder gleich</a></td><td>Dieser Operator prüft, ob der erste Wert größer oder gleich dem zweiten Wert ist</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">Ungleich</a></td><td>Dieser Operator prüft, ob der angegebene Ausdruck nicht gleich dem Wert gibt</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Kleiner oder gleich</a> </td><td>Dieser Operator prüft, ob der erste Wert kleiner oder gleich dem zweiten Wert ist</td>
    </tr>
</table>

