---
title: Bibliothek für Helper-Funktionen
description: Bibliothek für Journey Optimizer Helper-Funktionen
feature: Personalisierung
topic: Personalisierung
role: Data Engineer
level: Experienced
source-git-commit: d09eedce833b41037452bb46bc748e7e9f477d0a
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 95%

---


# Bibliothek für Helper-Funktionen{#functionsL}

Verwenden Sie die Vorlagensprache von [!DNL Journey Optimizer], um Datenoperationen wie Berechnungen, Datenformatierung oder Konvertierungen und Bedingungen durchzuführen und bearbeiten Sie Daten im Kontext der Personalisierung. Weitere Informationen zu Richtlinien zur Personalisierungssyntax finden Sie auf [dieser Seite](../personalization-syntax.md).

➡️ [Erfahren Sie, wie Sie Hilfsfunktionen](#video) verwenden (Video)

Die Vorlagensprache wird in Helper-Funktionen verwendet, die in der Dropdown-Liste „Personalisierung“ des Ausdruckseditors verfügbar sind, wie unten gezeigt:

![](../assets/access-helper-functions.png)



Im [!DNL Journey Optimizer]-Ausdruckseditor sind Helper-Funktionen in drei Kategorien unterteilt: [Funktionen](#functions-helper), [Helper](#helper-helper) und [Operatoren](#operators-helper).

## Funktionen{#functions-helper}

**Array-Funktionen**

<table>
    <tr>
        <td><a href="aggregation.md#average">Durchschnitt</a></td><td>Die Funktion gibt das arithmetische Mittel aller ausgewählten Werte im Array zurück</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">Enthalten</a></td><td>Mit dieser Funktion wird bestimmt, ob ein Element einem Array oder einer Liste angehört</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimum</a></td><td>Die Funktion gibt den kleinsten aller ausgewählten Werte im Array zurück</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Anzahl</a></td><td>Diese Funktion gibt die Anzahl der Elemente innerhalb des angegebenen Arrays zurück</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Enthält</a></td><td>Diese Funktion bestimmt, ob ein Array oder eine Liste ein bestimmtes Element enthält</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Nicht enthalten</a></td><td>Diese Funktion bestimmt, ob ein Element nicht in einem Array oder einer Liste enthalten ist</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Eindeutig</a></td><td>Diese Funktion ruft Werte aus einem Array oder einer Liste ab, wobei doppelte Werte entfernt werden</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Schnittmengen</a></td><td>Diese Funktion bestimmt, ob zwei Arrays oder Listen mindestens ein gemeinsames Element aufweisen</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Teilmenge von</a></td><td>Diese Funktion bestimmt, ob ein bestimmtes Array (Array A) eine Teilmenge eines anderen Arrays (Array B) ist, d. h. ob alle Elemente in Array A Elemente von Array B sind</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Erstes Element</a></td><td>Diese Funktion gibt das erste Element in einem Array oder einer Liste zurück</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Letzte n in Array</a></td><td>Diese Funktion gibt die letzten n Elemente in einem Array zurück, wenn sie anhand des angegebenen numerischen Ausdrucks in aufsteigender Reihenfolge sortiert werden</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Summe</a></td><td>Diese Funktion gibt die Summe aller ausgewählten Werte im Array zurück</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Erste n in Array</a></td><td>Diese Funktion gibt die ersten n Elemente in einem Array zurück, wenn sie anhand des angegebenen numerischen Ausdrucks in aufsteigender Reihenfolge sortiert werden</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Maximum</a></td><td>Diese Funktion gibt den größten aller ausgewählten Werte im Array zurück</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Obermenge</a></td><td>Diese Funktion bestimmt, ob ein bestimmtes Array (Array A) eine Obermenge eines anderen Arrays (Array B) ist, d. h. wenn dieses Array A alle Elemente in Array B enthält</td>
    </tr>
</table>


**Zuordnungsfunktionen**

<table>
    <tr>
        <td><a href="maps.md#get">Abrufen</a></td><td>Mit dieser Funktion wird der Wert einer Zuordnung für einen bestimmten Schlüssel abgerufen</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Schlüssel</a></td><td>Mit dieser Funktion werden alle Schlüssel einer angegebenen Zuordnung abgerufen</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Werte</a></td><td>Diese Funktion ruft alle Werte einer angegebenen Zuordnung ab</td>
    </tr>
</table>

**Objektfunktionen**

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Ist nicht null</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Objektreferenz vorhanden ist</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">Ist null</a></td><td>Mit dieser Funktion wird bestimmt, ob keine Objektreferenz vorhanden ist</td>
    </tr>
</table>

**Zeichenfolgen-Funktionen**

<table>
    <tr>
        <td><a href="string.md#camelCase">Binnenmajuskel</a></td><td>Mit dieser Funktion wird der erste Buchstabe jedes Wortes einer Zeichenfolge großgeschrieben</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Verknüpfen</a></td><td>Mit dieser Funktion werden zwei Zeichenfolgen zu einer zusammengeführt</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Enthält</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge eine angegebene Unterzeichenfolge enthält</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Enthält nicht</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge eine angegebene Unterzeichenfolge nicht enthält</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">Endet nicht mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge endet</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">Beginnt nicht mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge beginnt</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">Codieren 64</a></td><td>Mit dieser Funktion wird eine Zeichenfolge ver- oder entschlüsselt</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Endet mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge endet</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Gleich</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Zeichenfolge übereinstimmt</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Gleich ohne Groß-/Kleinschreibung</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Zeichenfolge übereinstimmt, Groß-/Kleinschreibung wird nicht beachtet</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">E-Mail-Domain extrahieren</a></td><td>Mit dieser Funktion wird die Domain einer E-Mail-Adresse extrahiert</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">Ist leer</a></td><td>Mit dieser Funktion wird geprüft, ob eine Zeichenfolge oder ein Ausdruck leer ist</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Links kürzen</a></td><td>Diese Funktion entfernt Leerzeichen vom Anfang einer Zeichenfolge</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Länge</a></td><td>Mit dieser Funktion wird die Anzahl der Zeichen in einer Zeichenfolge oder einem Ausdruck zurückgegeben</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Ist wie</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge einem angegebenen Muster entspricht</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Kleinbuchstaben</a></td><td>Diese Funktion wandelt eine Zeichenfolge in Kleinbuchstaben um</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Stimmt überein mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einem bestimmten regulären Ausdruck übereinstimmt</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Ungleich</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge nicht gleich der angegebenen Zeichenfolge ist</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Gruppe regelmäßiger Ausdrücke</a></td><td>Mit dieser Funktion werden spezifische Informationen basierend auf dem bereitgestellten regulären Ausdruck extrahiert</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Ersetzen</a></td><td>Diese Funktion ersetzt eine angegebene Teilzeichenfolge in einer Zeichenfolge durch eine andere Teilzeichenfolge</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">Alle ersetzen</a></td><td>Diese Funktion ersetzt alle Teilzeichenfolgen eines Textes, die mit dem „Ziel“ übereinstimmen, durch die angegebene literale „Ersatz“-Zeichenfolge</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Rechts kürzen</a></td><td>Diese Funktion entfernt Leerzeichen am Ende einer Zeichenfolge </td>
    </tr>
    <tr>
        <td><a href="string.md#split">Teilen</a></td><td>Mit dieser Funktion wird eine Zeichenfolge durch ein bestimmtes Zeichen aufgeteilt</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Beginnt mit</a></td><td>Mit dieser Funktion wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge beginnt</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Titelschreibweise</a></td><td>Diese Funktion wird verwendet, um die ersten Buchstaben jedes Wortes einer Zeichenfolge großzuschreiben</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Kürzen</a></td><td>Diese Funktion entfernt Leerzeichen vom Anfang und vom Ende einer Zeichenfolge</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Großbuchstaben</a></td><td>Diese Funktion wandelt eine Zeichenfolge in Großbuchstaben um</td>
    </tr>
</table>


## Helper{#helper-helper}

Helper werden auf [dieser Seite](helpers.md) näher beschrieben.


<table>
    <tr>
        <td><a href="helpers.md#each">Jeweils</a></td><td>Diese Funktion wird verwendet, um über ein Array zu iterieren</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">Wenn</a></td><td>Mit dieser Funktion wird ein bedingter Block definiert. Wenn die Ausdrucksevaluierung „true“ zurückgibt, wird der Block gerendert</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Zulassen</a></td><td>Diese Funktion ermöglicht das Speichern eines Ausdrucks als Variable, die später in einer Abfrage verwendet werden kann</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">Außer</a></td><td>Mit dieser Funktion wird ein bedingter Block definiert. Wenn die Ausdrucksevaluierung „false“ zurückgibt, wird der Block gerendert</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">Mit</a></td><td>Diese Funktion wird verwendet, um das Evaluierungs-Token des Vorlagenteils zu ändern</td>
    </tr>
</table>

## Operatoren{#operators-helper}

### Arithmetische Funktionen  {#arithmetic-helper}

Mit arithmetischen Funktionen lassen sich einfache Berechnungen für Werte durchführen

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">Addieren</a></td><td>Mit diesem Operator wird die Summe zweier Argumentausdrücke ermittelt</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">Dividieren</a></td><td>Mit diesem Operator wird der Quotient zweier Argumentausdrücke ermittelt</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">Multiplizieren</a></td><td>Mit diesem Operator wird das Produkt zweier Argumentausdrücke ermittelt</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">Rest</a> </td><td>Dieser Operator wird verwendet, um den Rest nach der Division der beiden Argumentausdrücke zu ermitteln</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">Subtrahieren</a> </td><td>Mit diesem Operator wird die Differenz zwischen zwei Argumentausdrücken ermittelt</td>
    </tr>
</table>


### Boolesche Funktionen

Boolesche Funktionen werden verwendet, um eine boolesche Logik auf verschiedene Elemente anzuwenden.

<table>
    <tr>
        <td><a href="operators.md#and">Und</a></td><td>Dieser Operator erstellt eine logische Konjunktion</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Wenn</a></td><td>Dieser Operator löst einen Ausdruck in Abhängigkeit davon auf, ob eine angegebene Bedingung wahr ist</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Nicht</a></td><td>Dieser Operator erstellt eine logische Negation</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">Oder</a></td><td>Dieser Operator erstellt eine logische Disjunktion</td>
    </tr>
</table>


### Vergleichsfunktionen

Vergleichsfunktionen werden verwendet, um zwischen verschiedenen Ausdrücken und Werten zu vergleichen und entsprechend „true“ oder „false“ zurückzugeben.

<table>
    <tr>
        <td><a href="operators.md#and">Gleich</a></td><td>Dieser Vorgang prüft, ob Werte gleich sind</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Größer als</a></td><td>Dieser Operator prüft, ob der erste Wert größer als der zweite Wert ist</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Größer oder gleich</a></td><td>Dieser Operator prüft, ob der erste Wert größer oder gleich dem zweiten Wert ist</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">Ungleich</a></td><td>Dieser Operator prüft, ob ein angegebener Ausdruck ungleich einem angegebenen Wert ist</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Kleiner oder gleich</a> </td><td>Dieser Operator prüft, ob der erste Wert kleiner oder gleich dem zweiten Wert ist</td>
    </tr>
</table>

## Anleitungsvideo{#video}

Erfahren Sie, wie Sie Personalisierungswerte mithilfe von Personalisierungsfunktionen umwandeln und verschiedene Anwendungsfälle für Hilfsfunktionen verstehen.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)