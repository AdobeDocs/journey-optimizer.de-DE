---
solution: Journey Optimizer
product: journey optimizer
title: Bearbeiten von Ausdrücken
description: Erfahren Sie, wie Sie Ausdrücke bearbeiten.
exl-id: bf0a905f-00af-4ed7-9e4f-bf8cb0af9ea9
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '2034'
ht-degree: 100%

---


# Bearbeiten von Ausdrücken {#edit-expressions}

>[!NOTE]
>
>Im folgenden Abschnitt finden Sie Informationen zum Erstellen von Regeln mit dem Ausdruckseditor. Beachten Sie, dass sich die zum Erstellen von Regeln verwendete Syntax von der für die Personalisierung verwendeten unterscheidet.

## Arbeiten mit dem Ausdruckseditor {#edit}

Die Bearbeitung von Ausdrücken erfolgt durch die manuelle Eingabe von Bedingungen, die in ihrer Gesamtheit eine Regel bilden. Dieser Modus bietet erweiterte Funktionen, mit denen Sie die Werte zur Durchführung bestimmter Abfragen ändern können, z. B. Bearbeitung von Daten, Strings, numerischen Feldern und Sortierungen.

Der Ausdruckseditor steht bei der Konfiguration einer benutzerdefinierten Bedingung im Regel-Builder unter **[!UICONTROL Ausdruck bearbeiten]** für die Felder **[!UICONTROL Attribut]** und **[!UICONTROL Wert]** zur Verfügung.

| Zugriff über das Feld **Attribut** | Zugriff über das Feld **Wert** |
| --- | --- |
| ![Ausdruckseditor für Attributfeld](assets/rule-builder-expression-access-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![Ausdruckseditor für Wertefeld](assets/rule-builder-expression-access-value.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

Der Ausdruckseditor bietet Folgendes:

* ein **Eingabefeld (1)**, in dem der Ausdruck definiert wird,
* eine Liste der verfügbaren **Felder (2)**, die im Ausdruck verwendet werden können und die der Zielgruppendimension der Abfrage entsprechen,
* **Hilfsfunktionen (3)**, sortiert nach Kategorie.

Bearbeiten Sie den Ausdruck, indem Sie ihn direkt in das Eingabefeld eingeben. Um ein Feld oder eine Hilfsfunktion hinzuzufügen, gehen Sie mit dem Cursor zu dem Ausdruck, zu dem Sie es/sie hinzufügen möchten, und klicken Sie auf die Schaltfläche „+“.

![Benutzeroberfläche des Ausdruckseditors](assets/rule-builder-expression-editor.png){zoomable="yes"}

## Hilfsfunktionen

Der Abfrageeditor bietet fortgeschrittene Funktionen zur Erstellung komplexer Filter, je nach den gewünschten Ergebnissen und der Art der bearbeiteten Daten. Folgende Funktionen stehen zur Verfügung:

### Aggregat

Aggregatfunktionen führen Berechnungen für eine Reihe von Werten durch.

<table>
<tbody>
<tr>
<td><strong>Name</strong></td>
<td><strong>Beschreibung</strong></td>
<td><strong>Syntax</strong></td>
</tr>
<tr>
<td><strong>Avg</strong></td>
<td>Gibt den Durchschnittswert einer Spalte vom Typ Zahl aus</td>
<td>Avg(&lt;Wert&gt;)</td>
</tr>
<tr>
<td><strong>Count</strong></td>
<td>Zählt die Werte ungleich null einer Spalte</td>
<td>Count(&lt;Wert&gt;)</td>
</tr>
<tr>
<td><strong>CountAll</strong></td>
<td>Zählt die ausgegebenen Werte (alle Felder)</td>
<td>CountAll()</td>
</tr>
<tr>
<td><strong>Countdistinct</strong></td>
<td>Zählt die unterschiedlichen Werte ungleich null einer Spalte</td>
<td>Countdistinct(&lt;Wert&gt;)</td>
</tr>
<tr>
<td><strong>Max</strong></td>
<td>Gibt den Höchstwert einer Spalte vom Typ Zahl, String oder Datum aus</td>
<td>Max(&lt;Wert&gt;)</td>
</tr>
<tr>
<td><strong>Min</strong></td>
<td>Gibt den Mindestwert einer Spalte vom Typ Zahl, String oder Datum aus</td>
<td>Min(&lt;Wert&gt;)</td>
</tr>
<tr>
<td><strong>StdDev</strong></td>
<td>Gibt die Standardabweichung einer Spalte vom Typ Zahl, String oder Datum aus</td>
<td>StdDev(&lt;Wert&gt;)</td>
</tr>
<tr>
<td><strong>StringAgg</strong></td>
<td>Gibt die Konkatenation der Werte einer Spalte vom String-Typ zurück, getrennt durch das Zeichen im zweiten Argument.</td>
<td>StringAgg(&lt;Wert&gt;, &lt;String&gt;)</td>
</tr>
<tr>
<td><strong>Sum</strong></td>
<td>Gibt die Summe der Werte einer Spalte vom Typ Zahl, String oder Datum aus</td>
<td>Sum(&lt;Wert&gt;)</td>
</tr>
</tbody>
</table>

### Datum

Datumsfunktionen dienen zur Bearbeitung von Datums- oder Zeitwerten.

<table>
<tbody>
<tr>
<td><strong>Name</strong></td>
<td><strong>Beschreibung</strong></td>
<td><strong>Syntax</strong></td>
</tr>
<tr>
<td><strong>AddDays</strong></td>
<td>Fügt dem Datum eine Anzahl an Tagen hinzu</td>
<td>AddDays(&lt;Datum&gt;, &lt;Anzahl&gt;)</td>
</tr>
<tr>
<td><strong>AddHours</strong></td>
<td>Fügt dem Datum eine Anzahl an Stunden hinzu</td>
<td>AddHours(&lt;Datum&gt;, &lt;Anzahl&gt;)</td>
</tr>
<tr>
<td><strong>AddMinutes</strong></td>
<td>Fügt dem Datum eine Anzahl an Minuten hinzu</td>
<td>AddMinutes(&lt;Datum&gt;, &lt;Anzahl&gt;)</td>
</tr>
<tr>
<td><strong>AddMonths</strong></td>
<td>Fügt dem Datum eine Anzahl an Monaten hinzu</td>
<td>AddMonths(&lt;Datum&gt;, &lt;Anzahl&gt;)</td>
</tr>
<tr>
<td><strong>AddSeconds</strong></td>
<td>Fügt dem Datum eine Anzahl an Sekunden hinzu</td>
<td>AddSeconds(&lt;Datum&gt;, &lt;Anzahl&gt;)</td>
</tr>
<tr>
<td><strong>AddYears</strong></td>
<td>Fügt dem Datum eine Anzahl an Jahren hinzu</td>
<td>AddYears(&lt;Datum&gt;, &lt;Anzahl&gt;)</td>
</tr>
<tr>
<td><strong>ConvertNTZ</strong></td>
<td>Konvertiert NTZ-Zeitstempel (Zeitstempel ohne Zeitzone) in TZ (Zeitstempel mit Zeitzone) unter Anwendung der definierten Sitzungszeitzone</td>
<td>ConvertNTZ(&lt;Datum + Uhrzeit&gt;)</td>
</tr>
<tr>
<td><strong>DateCmp</strong></td>
<td>Vergleicht zwei Daten</td>
<td>DateCmp(&lt;Datum&gt;, &lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>DateOnly</strong></td>
<td>Gibt nur das Datum zurück (mit der Uhrzeit 00:00 Uhr)</td>
<td>DateOnly(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>Day</strong></td>
<td>Gibt die Zahl zurück, die dem Tag des Datums entspricht</td>
<td>Day(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>DayOfYear</strong></td>
<td>Gibt die Zahl des Tages im Jahr des angegebenen Datums aus</td>
<td>DayOfYear(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>DaysAgo</strong></td>
<td>Gibt das Datum aus, das dem aktuellen Datum abzüglich n Tage entspricht</td>
<td>DaysAgo(&lt;Zahl&gt;)</td>
</tr>
<tr>
<td><strong>DaysAgoInt</strong></td>
<td>Gibt das Datum (Integer JJJJMMTT) aus, das dem aktuellen Datum abzüglich n Tage entspricht</td>
<td>DaysAgoInt(&lt;Zahl&gt;)</td>
</tr>
<tr>
<td><strong>DaysDiff</strong></td>
<td>Gibt die Anzahl von Tagen zwischen zwei Daten aus</td>
<td>DaysDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)</td>
</tr>
<tr>
<td><strong>DaysOld</strong></td>
<td>Gibt das Alter in Tagen in Bezug auf ein Datum zurück</td>
<td>DaysOld(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>GetDate</strong></td>
<td>Gibt das aktuelle Systemdatum des Servers zurück</td>
<td>GetDate()</td>
</tr>
<tr>
<td><strong>Hour</strong></td>
<td>Gibt die Stunde der im Datum angegebenen Uhrzeit zurück</td>
<td>Hour(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>HoursDiff</strong></td>
<td>Gibt die Anzahl von Stunden zwischen zwei Daten zurück</td>
<td>HoursDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)</td>
</tr>
<tr>
<td><strong>Minute</strong></td>
<td>Gibt die Minuten der im Datum angegebenen Uhrzeit zurück</td>
<td>Minute(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>MinutesDiff</strong></td>
<td>Gibt die Anzahl von Minuten zwischen zwei Daten zurück</td>
<td>MinutesDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)</td>
</tr>
<tr>
<td><strong>Month</strong></td>
<td>Gibt die Zahl zurück, die dem Monat des Datums entspricht</td>
<td>Month(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>MonthsAgo</strong></td>
<td>Gibt das Datum zurück, das dem aktuellen Datum abzüglich n Monate entspricht</td>
<td>MonthsAgo(&lt;Zahl&gt;)</td>
</tr>
<tr>
<td><strong>MonthsDiff</strong></td>
<td>Gibt die Anzahl von Monaten zwischen zwei Daten zurück</td>
<td>MonthsDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)</td>
</tr>
<tr>
<td><strong>MonthsOld</strong></td>
<td>Gibt das Alter in Monaten in Bezug auf ein Datum zurück</td>
<td>MonthsOld(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>Oldest</strong></td>
<td>Gibt das älteste Datum in einem Bereich zurück</td>
<td>Oldest(&lt;Datum, Datum&gt;)</td>
</tr>
<tr>
<td><strong>Second</strong></td>
<td>Gibt die Sekunden der im Datum angegebenen Uhrzeit zurück</td>
<td>Second(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>SecondsDiff</strong></td>
<td>Gibt die Anzahl von Sekunden zwischen zwei Daten zurück</td>
<td>SecondsDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)</td>
</tr>
<tr>
<td><strong>SubDays</strong></td>
<td>Zieht eine Anzahl an Tagen von einem Datum ab</td>
<td>SubDays(&lt;Datum&gt;, &lt;Anzahl&gt;)</td>
</tr>
<tr>
<td><strong>SubHours</strong></td>
<td>Zieht eine Anzahl an Stunden von einem Datum ab</td>
<td>SubHours(&lt;Datum&gt;, &lt;Anzahl&gt;)</td>
</tr>
<tr>
<td><strong>SubMinutes</strong></td>
<td>Zieht eine Anzahl an Minuten von einem Datum ab</td>
<td>SubMinutes(&lt;Datum&gt;, &lt;Anzahl&gt;)</td>
</tr>
<tr>
<td><strong>SubMonths</strong></td>
<td>Zieht eine Anzahl an Monaten von einem Datum ab</td>
<td>SubMonths(&lt;Datum&gt;, &lt;Anzahl&gt;)</td>
</tr>
<tr>
<td><strong>SubSeconds</strong></td>
<td>Zieht eine Anzahl an Sekunden von einem Datum ab</td>
<td>SubSeconds(&lt;Datum&gt;, &lt;Anzahl&gt;)</td>
</tr>
<tr>
<td><strong>SubYears</strong></td>
<td>Zieht eine Anzahl an Jahren von einem Datum ab</td>
<td>SubYears(&lt;Datum&gt;, &lt;Anzahl&gt;)</td>
</tr>
<tr>
<td><strong>ToDate</strong></td>
<td>Konvertiert Datum und Uhrzeit in ein Datum</td>
<td>ToDate(&lt;Datum + Uhrzeit&gt;)</td>
</tr>
<tr>
<td><strong>ToDateTime</strong></td>
<td>Konvertiert einen String in Datum und Uhrzeit</td>
<td>ToDateTime(&lt;String&gt;)</td>
</tr>
<tr>
<td><strong>ToTimestamp</strong></td>
<td>Konvertiert einen String in einen Zeitstempel</td>
<td>ToTimestamp(&lt;String&gt;)</td>
</tr>
<tr>
<td><strong>ToTimeZone</strong></td>
<td>Konvertiert Datum und Uhrzeit in eine Zeitzone</td>
<td>ToTimeZone(&lt;Datum&gt;, &lt;Zeitzone&gt;)</td>
</tr>
<tr>
<td><strong>TruncDate</strong></td>
<td>Kürzt die Angabe des Datums und der Uhrzeit auf Sekunden</td>
<td>TruncDate(@lastModified, &lt;Anzahl Sekunden&gt;)</td>
</tr>
<tr>
<td><strong>TruncDateTZ</strong></td>
<td>Rundet eine Uhrzeit und ein Datum auf eine Genauigkeit von Sekunden</td>
<td>TruncDateTZ(&lt;Datum&gt;, &lt;Anzahl an Sekunden&gt;, &lt;Zeitzone&gt;)</td>
</tr>
<tr>
<td><strong>TruncQuarter</strong></td>
<td>Rundet ein Datum auf das Quartal</td>
<td>TruncQuarter(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>TruncTime</strong></td>
<td>Rundet die Uhrzeit auf die nächste Sekunde auf</td>
<td> TruncTime(&lt;Datum&gt;, &lt;Anzahl an Sekunden&gt;)</td>
</tr>
<tr>
<td><strong>TruncWeek</strong></td>
<td>Rundet ein Datum auf die Woche</td>
<td>TruncWeek(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>TruncYear</strong></td>
<td>Rundet ein Datum und eine Uhrzeit auf den ersten Januar des Jahres</td>
<td>TruncYear(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>WeekDay</strong></td>
<td>Gibt die Zahl des Wochentages in Bezug auf das Datum aus (0=Montag, 6=Sonntag).</td>
<td>WeekDay(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>Year</strong></td>
<td>Gibt die Zahl zurück, die dem Jahr des Datums entspricht</td>
<td>Year(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>YearAndMonth</strong></td>
<td>Gibt die Zahl zurück, die dem Jahr und Monat des Datums entspricht</td>
<td>YearAndMonth(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>YearsAgo</strong></td>
<td>Gibt die Anzahl von Jahren zwischen einem bestimmten Datum und dem aktuellen Datum aus</td>
<td>YearsAgo(&lt;Datum&gt;)</td>
</tr>
<tr>
<td><strong>YearsDiff</strong></td>
<td>Gibt die Anzahl von Jahren zwischen zwei Daten aus</td>
<td>YearsDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)</td>
</tr>
<tr>
<td><strong>YearsOld</strong></td>
<td>Gibt das Alter in Jahren in Bezug auf ein Datum zurück</td>
<td>YearsOld(&lt;Datum&gt;)</td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>Beachten Sie, dass die Funktion **DateOnly** nicht die Zeitzone der bzw. des Benutzenden, sondern des Servers verwendet.


### Geomarketing

Die Geomarketing-Funktionen dienen der Manipulation von geografischen Werten.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Distance</strong><br /> </td> 
   <td> Gibt die Entfernung zwischen zwei durch Längen- und Breitengrad bezeichneten Punkten aus (in Grad).<br /> </td> 
   <td> Distance(&lt;Längengrad A&gt;, &lt;Breitengrad A&gt;, &lt;Längengrad B&gt;, &lt;Breitengrad B&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Numerisch

Die numerischen Funktionen dienen der Konversion von Text in Zahlen.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Abs</strong><br /> </td> 
   <td> Gibt den absoluten Wert einer Zahl aus<br /> </td> 
   <td> Abs(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> Gibt die kleinste ganze Zahl aus, die größer oder gleich der angegebenen Zahl ist<br /> </td> 
   <td> Ceil(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Floor</strong><br /> </td> 
   <td> Gibt die größte ganze Zahl aus, die kleiner oder gleich der angegebenen Zahl ist<br /> </td> 
   <td> Floor(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Greatest</strong><br /> </td> 
   <td> Gibt die größere von zwei Zahlen aus<br /> </td> 
   <td> Greatest(&lt;Zahl 1&gt;, &lt;Zahl 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Least</strong><br /> </td> 
   <td> Gibt die kleinere von zwei Zahlen aus<br /> </td> 
   <td> Least(&lt;Zahl 1&gt;, &lt;Zahl 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> Gibt den Rest der ganzzahligen Division von n1 durch n2 aus<br /> </td> 
   <td> Mod(&lt;Zahl 1&gt;, &lt;Zahl 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Percent</strong><br /> </td> 
   <td> Gibt das Verhältnis zwischen zwei Werten in Prozent aus<br /> </td> 
   <td> Percent(&lt;Zahl 1&gt;, &lt;Zahl 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Random</strong><br /> </td> 
   <td> Gibt einen Zufallswert aus<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Round</strong><br /> </td> 
   <td> Rundet eine Zahl auf n Dezimalstellen<br /> </td> 
   <td> Round(&lt;Zahl&gt;, &lt;Anzahl Dezimalstellen&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Sign</strong><br /> </td> 
   <td> Gibt das Vorzeichen einer Zahl aus<br /> </td> 
   <td> Sign(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> Konvertiert einen Integer in einen Real<br /> </td> 
   <td> ToDouble(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> Konvertiert einen Real in einen 64-Bit-Integer<br /> </td> 
   <td> ToInt64(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> Konvertiert einen Real in einen Integer<br /> </td> 
   <td> ToInteger(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> Kürzt n1 auf n2 Dezimalstellen<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Sonstige

In dieser Tabelle sind die restlichen verfügbaren Funktionen enthalten.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AESEncrypt</strong><br /> </td> 
   <td> Verschlüsselt den im Argument angegebenen String<br /> </td> 
   <td> AESEncrypt(&lt;Wert&gt;)<br /> </td> 
  </tr>
  <tr> 
   <td> <strong>Case</strong><br /> </td> 
   <td> Gibt Wert 1 zurück, wenn die Bedingung zutrifft. Wenn nicht, wird Wert 2 zurückgegeben.<br /> </td> 
   <td> Case(When(&lt;Bedingung&gt;, &lt;Wert 1&gt;), Else(&lt;Wert 2&gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> Löscht das Flag aus dem Wert<br /> </td> 
   <td> ClearBit(&lt;Kennung&gt;, &lt;Flag&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> Gibt den Wert 2 aus, wenn der Wert 1 gleich null oder leer ist, sonst den Wert 1<br /> </td> 
   <td> Coalesce(&lt;Wert 1&gt;, &lt;Wert 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Decode</strong><br /> </td> 
   <td> Gibt Wert 3 zurück, wenn Wert 1 = Wert 2 ist. Wenn nicht, wird Wert 4 zurückgegeben.<br /> </td> 
   <td> Decode(&lt;Wert 1&gt;, &lt;Wert 2&gt;, &lt;Wert 3&gt;, &lt;Wert 4&gt;)<br /> </td>  
  </tr>

<tr> 
   <td> <strong>Else</strong><br /> </td> 
   <td> Gibt den Wert 1 aus (kann nur als Parameter der 'Case'-Funktion verwendet werden)<br /> </td> 
   <td> Else(&lt;Wert 1&gt;, &lt;Wert 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> Extrahiert die Domain einer E-Mail-Adresse<br /> </td> 
   <td> GetEmailDomain(&lt;Wert&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> Ruft die URL des Mirrorseiten-Servers ab<br /> </td> 
   <td> GetMirrorURL(&lt;Wert&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> Gibt Wert 1 aus, wenn die Bedingung zutrifft. Wenn nicht, wird Wert 2 zurückgegeben<br /> </td> 
   <td> Iif(&lt;Bedingung&gt;, &lt;Wert 1&gt;, &lt;Wert 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> Gibt an, ob das Flag im Wert vorkommt<br /> </td> 
   <td> IsBitSet(&lt;Kennung&gt;, &lt;Flag&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> Gibt den Wert 2 aus, wenn der String 1 leer ist, sonst den Wert 3<br /> </td> 
   <td> IsEmptyString(&lt;Wert 1&gt;, &lt;Wert 2&gt;, &lt;Wert 3&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NewUUID</strong><br /> </td> 
   <td> Gibt eine eindeutige ID zurück<br /> </td> 
   <td> NewUUID()<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> Gibt einen Leerstring aus, wenn das Argument gleich null ist<br /> </td> 
   <td> NoNull(&lt;Wert&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> Gibt die Zeilennummer aus<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> Setzt das Flag im Wert<br /> </td> 
   <td> SetBit(&lt;Kennung&gt;, &lt;Flag&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> Konvertiert eine Zahl in einen booleschen Wert<br /> </td> 
   <td> ToBoolean(&lt;Zahl&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>When</strong><br /> </td> 
   <td> Gibt Wert 1 aus, wenn die Bedingung zutrifft. Falls nicht, wird Wert 2 zurückgegeben (kann nur als Parameter der Case-Funktion verwendet werden)<br /> </td> 
   <td> When(&lt;Bedingung&gt;, &lt;Wert 1&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### String

Die String-Funktionen dienen der Manipulation einer Reihe von Strings.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> Gibt an, ob alle Parameter ungleich null und nicht leer sind<br /> </td> 
   <td> AllNonNull2(&lt;String&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> Gibt an, ob alle Parameter ungleich null und nicht leer sind<br /> </td> 
   <td> AllNonNull3(&lt;String&gt;, &lt;String&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ascii</strong><br /> </td> 
   <td> Gibt den ASCII-Wert des ersten Zeichens des Strings aus.<br /> </td> 
   <td> Ascii(&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> Gibt das ASCII-Code-Zeichen 'n' aus<br /> </td> 
   <td> Char(&lt;Zahl&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> Gibt die Position von Zeichenfolge 2 in Zeichenfolge 1 zurück.<br /> </td> 
   <td> Charindex(&lt;String&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>dataLength</strong><br /> </td> 
   <td> Gibt die Größe der Zeichenfolge in Bytes zurück<br /> </td> 
   <td> dataLength(&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> Gibt die n-te Zeile (beginnend bei 1) des Strings aus<br /> </td> 
   <td> GetLine(&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> Gibt den dritten Parameter zurück, wenn die ersten beiden Parameter identisch sind. Wenn nicht, wird der letzte Parameter zurückgegeben<br /> </td> 
   <td> IfEquals(&lt;String&gt;, &lt;String&gt;, &lt;String&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> Gibt an, ob das als Parameter ausgegebene Memo gleich null ist<br /> </td> 
   <td> IsMemoNull(&lt;Memo&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> Verkettet die zwei als Parameter übergebenen Zeichenfolgen. Fügt bei Bedarf Leerzeichen zwischen den Zeichenfolgen hinzu.<br /> </td> 
   <td> JuxtWords(&lt;String&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> Verkettet die zwei als Parameter übergebenen Zeichenfolgen. Fügt bei Bedarf Leerzeichen zwischen den Zeichenfolgen hinzu<br /> </td> 
   <td> JuxtWords3(&lt;String&gt;, &lt;String&gt;, &lt;String&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Left</strong><br /> </td> 
   <td> Gibt die n ersten Zeichen des Strings aus<br /> </td> 
   <td> Left(&lt;String&gt;, &lt;Zahl&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Length</strong><br /> </td> 
   <td> Gibt die Länge des Strings aus<br /> </td> 
   <td> Length(&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Line</strong><br /> </td> 
   <td> Extrahiert Zeile n aus dem String<br /> </td> 
   <td> Line(&lt;String&gt;,&lt;Zahl&gt;)<br /></td> 
  </tr>
  <tr> 
   <td> <strong>Lower</strong><br /> </td> 
   <td> Gibt den String in Kleinbuchstaben aus<br /> </td> 
   <td> Lower(&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> Gibt den String linksseitig aufgefüllt aus<br /> </td> 
   <td> LPad (&lt;String&gt;, &lt;Zahl&gt;, &lt;Zeichen&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> Löscht die Leerstellen links vom String<br /> </td> 
   <td> Ltrim(&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> Gibt eine hexadezimale Darstellung des MD5-Schlüssels eines Strings aus<br /> </td> 
   <td> Md5Digest(&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>MemoContains</strong><br /> </td> 
   <td> Gibt an, ob das Memo den als Parameter übergebenen String enthält<br /> </td> 
   <td> MemoContains(&lt;Memo&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>NodeValue</strong><br /> </td> 
   <td> Extrahiert den Wert eines XML-Felds aus seinem XPath und den Felddaten<br /> </td> 
   <td> NodeValue (&lt;String&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Replace</strong><br /> </td> 
   <td> Ersetzt alle Vorkommen eines angegebenen String-Werts durch einen anderen String-Wert.<br /> </td> 
   <td> Replace(&lt;String&gt;,&lt;String&gt;,&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Right</strong><br /> </td> 
   <td> Gibt die n letzten Zeichen des Strings aus<br /> </td> 
   <td> Right(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> Gibt den String rechtsseitig aufgefüllt aus<br /> </td> 
   <td> RPad(&lt;String&gt;, &lt;Zahl&gt;, &lt;Zeichen&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> Löscht die Leerstellen rechts vom String<br /> </td> 
   <td> Rtrim(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> Hexadezimale Darstellung des SHA256-Schlüssels einer Zeichenfolge.<br /> </td> 
   <td> Sha256Digest (&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> Hexadezimale Darstellung des SHA512-Schlüssels einer Zeichenfolge.<br /> </td> 
   <td> Sha512Digest (&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Smart</strong><br /> </td> 
   <td> Gibt jedes Wort des Strings beginnend mit einem Großbuchstaben aus<br /> </td> 
   <td> Smart(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Substring</strong><br /> </td> 
   <td> Extrahiert aus dem String den Teilstring, der mit dem Zeichen n1 beginnt und die Länge n2 aufweist<br /> </td> 
   <td> Substring(&lt;String&gt;, &lt;Start&gt;, &lt;Länge&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> Konvertiert eine Zahl in einen String<br /> </td> 
   <td> ToString(&lt;Zahl&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Upper</strong><br /> </td> 
   <td> Gibt den String in Großbuchstaben aus<br /> </td> 
   <td> Upper(&lt;String&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> Gibt den Fremdschlüssel einer als erster Parameter übergebenen Relation aus, wenn die beiden anderen Parameter identisch sind<br /> </td> 
   <td> VirtualLink(&lt;Zahl&gt;, &lt;Zahl&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> Gibt den Fremdschlüssel (Text) einer als erster Parameter übergebenen Relation aus, wenn die beiden anderen Parameter identisch sind<br /> </td> 
   <td> VirtualLinkStr(&lt;String&gt;, &lt;Zahl&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Fenster

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>_Over__</strong><br /> </td> 
   <td> Ruft die als ersten Parameter eingegebene SQL-Funktion über die als zweiten Parameter eingegebenen Felder „Partition“ oder „Anordnen nach“ aus<br /> </td> 
   <td> _Over_ (&lt;Wert&gt;, &lt;Wert&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Desc</strong><br /> </td> 
   <td> Absteigende Sortierung<br /> </td> 
   <td> Desc(&lt;Wert 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> Sortiert das Ergebnis innerhalb der Partition<br /> </td> 
   <td> OrderBy(&lt;Wert 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> Partitioniert das Ergebnis einer Abfrage<br /> </td> 
   <td> PartitionBy(&lt;Wert 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>RowNum</strong><br /> </td> 
   <td> Erzeugt eine Zeilennummer in Abhängigkeit von der Tabellenpartition und der Sortierreihenfolge<br /> </td> 
   <td> RowNum(PartitionBy(&lt;Wert 1&gt;), OrderBy(&lt;Wert 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>
