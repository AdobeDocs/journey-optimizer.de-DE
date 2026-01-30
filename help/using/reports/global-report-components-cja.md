---
solution: Journey Optimizer
product: journey optimizer
title: Liste von Komponenten
description: Erfahren Sie, wie Sie Daten aus Ihrem Bericht verwenden.
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: aa060d8e-23e2-4bab-b709-636077eb5d20
source-git-commit: 7945ab9369498f23685aa2f727542c7367c2d830
workflow-type: tm+mt
source-wordcount: '2189'
ht-degree: 97%

---

# Liste der Metriken {#list-of-components-global}

In den Tabellen unten finden Sie nach Versandtyp geordnet die Liste der Metriken, die in Berichten verwendet werden, sowie ihre Definitionen.

## Journey-Metriken {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrik<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody> 
<tr> 
<td>Journey-Interaktion</td> 
<td>Gesamtzahl der eindeutigen Kontakte, die über die Journey gesendete Nachrichten empfangen haben und bestimmte Profile repräsentieren, die einen bestimmten Aktionspunkt in der Journey erreicht haben.</td> 
</tr> 
<tr> 
<td>Journey-Eintritte</td> 
<td>Gesamtzahl der Kontakte, die das Eintrittsereignis der Journey erreicht haben.</td> 
</tr>
<tr> 
<td>Journey-Austritte</td> 
<td>Gesamtzahl der Kontakte, die die Journey verlassen haben.</td> 
</tr>
<tr> 
<td>Journey-Fehler</td> 
<td>Gesamtzahl der einzelnen Journeys, die nicht erfolgreich ausgeführt wurden.</td> 
</tr>
<tr> 
<td>Eindeutige Journey-Eintritte</td> 
<td>Gesamtzahl der Kontakte, die das Eintrittsereignis der Journey erreicht haben, wobei mehrfache Interaktionen desselben Profils nicht gezählt werden.</td> 
</tr>
<tr> 
<td>Eindeutige Journey-Austritte</td> 
<td>Gesamtzahl der Kontakte, die die Journey verlassen haben, wobei mehrfache Interaktionen desselben Profils nicht gezählt werden.</td> 
</tr>
<tr> 
<td>Eindeutige Journey-Fehler</td> 
<td>Gesamtzahl der individuellen Journeys, die nicht erfolgreich ausgeführt wurden, wobei mehrfache Interaktionen desselben Profils nicht gezählt werden.</td> 
</tr>
 </tbody> 
</table>

## E-Mail-Metriken {#email-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrik<br/> </th> 
   <th> Definition<br/> </th> 
  </tr>
 </thead> 
 <tbody>
  <tr> 
   <td> Bounces<br/> </td> 
   <td> Summe der kumulierten Fehler während des Sendevorgang und der automatischen Rücksendeverarbeitung im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.<br/> </td> 
  </tr>
  <tr> 
   <td> Bounce-Rate<br/> </td> 
   <td> Prozentsatz der E-Mails, die nicht erfolgreich zugestellt wurden, im Verhältnis zur Gesamtzahl der gesendeten E-Mails.<br/> </td> 
  </tr> 
  <tr> 
   <td> Klick-Öffnungsrate (CTOR)<br/> </td> 
   <td> Die Anzahl, wie oft die E-Mail geöffnet wurde.<br/> </td> 
  </tr>
  <tr> 
   <td> Klickrate (CTR)<br/> </td> 
   <td> Prozentsatz der Benutzenden, die mit der E-Mail interagiert haben.<br/> </td> 
  </tr>
  <tr> 
   <td> Klicks<br/> </td> 
   <td> Anzahl der Klicks auf einen Inhalt in einer E-Mail.<br/> </td> 
  </tr> 
  <tr> 
   <td> Zugestellt <br/> </td> 
   <td> Zahl der erfolgreich gesendeten Nachrichten im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.<br/></td> 
  </tr> 
  <tr> 
   <td> Zustellungsrate<br/> </td> 
   <td> Prozentsatz der erfolgreich gesendeten Nachrichten<br/> </td> 
  </tr>
  <tr> 
   <td> Fehlerursache<br/> </td> 
   <td> Name der spezifischen ursprünglichen Fehlerursache. <a href="exclusion-list.md">Weitere Informationen zu Fehlerursachen</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Geschätzte Öffnungen von E-Mails<br/> </td> 
   <td>Geschätzte Gesamtzahl der E-Mail-Öffnungen, die sowohl direkte Öffnungen durch Profile als auch automatisierte Öffnungen durch Mail-Server berücksichtigt. Diese Metrik wird um Öffnungen angepasst, die von E-Mail-Servern für Datenschutz- oder Sicherheitsprüfungen ausgelöst werden. Hierzu wird eine Öffnungsrate angewendet, die anhand von Empfangenden berechnet wird, die die E-Mail manuell geöffnet haben, sowie anhand von Empfangenden, deren E-Mails nur von E-Mail-Servern geöffnet wurden.<br/> </td> 
  </tr>
  <tr> 
   <td> Klickrate des Angebots<br/> </td> 
   <td> Prozentsatz der Benutzenden, die mit dem Angebot interagiert haben.<br/> </td> 
  </tr>
  <tr> 
   <td> Impressionsrate des Angebots<br/> </td> 
   <td> Prozentsatz der geöffneten Angebote im Verhältnis zur Anzahl der gesendeten Angebote.<br/> </td> 
  </tr>
  <tr> 
   <td> Name des Angebots<br/> </td> 
   <td> Name des im Versand hinzugefügten Angebots. Weiterführende Informationen zu Platzierungen finden Sie auf dieser <a href="../offers/offer-library/creating-personalized-offers.md">Seite</a>.<br/> </td> 
  </tr>
  <tr> 
   <td> Gesendetes Angebot<br/> </td> 
   <td> Gesamtzahl der Sendevorgänge für das Angebot.<br/> </td> 
  </tr> 
  <tr> 
   <td> Öffnungen<br/> </td> 
   <td> Die Anzahl, wie oft die Nachricht geöffnet wurde.<br/> </td> 
  </tr> 
  <tr> 
   <td> Sendefehler<br/> </td> 
   <td> Gesamtzahl der Fehler, die während des Sendevorgangs aufgetreten sind und den Versand an die Profile verhindert haben.<br/> </td> 
  </tr> 
  <tr> 
   <td> Sendeausschlüsse<br/> </td> 
   <td> Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden. <a href="exclusion-list.md">Erfahren Sie mehr darüber, wie Ausschlüsse gezählt werden</a>.<br/> </td> 
  </tr>
  <tr> 
   <td> Name der Platzierung<br/> </td> 
   <td> Name der Platzierung, die zur Anzeige Ihres Angebots verwendet wird. Weiterführende Informationen zu Platzierungen finden Sie auf dieser <a href="../offers/offer-library/creating-placements.md">Seite</a>. </td> 
  </tr>
  <tr> 
   <td> Spam-Beschwerden<br/> </td> 
   <td> Anzahl der Fälle, in denen eine Nachricht als Spam oder Junk deklariert wurde.<br/> </td> 
  </tr> 
  <tr> 
   <td> Zielgruppe<br/> </td> 
   <td> Anzahl der Profile, die sich für die Zielgruppe qualifiziert haben, bevor Ausschlüsse, Unterdrückungen oder Einverständnisentnahmen angewendet wurden. In Journey mit aktiviertem erneuten Eintritt kann ein Profil mehrmals angesprochen werden.<br/> </td> 
  </tr>
  <tr> 
   <td>Eindeutige Bounces<br/> </td> 
   <td> Anzahl der eindeutigen Profile, an die mindestens eine E-Mail nicht erfolgreich zugestellt wurde.</td> 
  </tr>
  <tr> 
   <td>Eindeutige Bounce-Rate<br/> </td> 
   <td>Prozentsatz der eindeutigen Profile, deren E-Mail mindestens einmal nicht erfolgreich zugestellt wurde, im Verhältnis zur Gesamtzahl der eindeutigen Sendungen.</td> 
  </tr>
  <tr> 
   <td> Einzelklicks<br/> </td> 
   <td> Die Anzahl der Profile, die auf Inhalt in einer E-Mail geklickt haben.<br> Beachten Sie, dass bei der Berechnung von Einzelklicks die letzten 10 Tage berücksichtigt werden. Wenn ein Profil mehrere Klicks innerhalb des Zeitraums von 10 Tagen registriert, werden diese als Einzelklicks gezählt. Wenn jedoch ein Profil zwei Klicks im Abstand von mehr als 10 Tagen aufweist, werden diese nicht als Einzelklicks betrachtet.<br/> </td> 
  </tr>
  <tr> 
   <td>Eindeutige Klick-Öffnungsrate<br/> </td> 
   <td> Prozentsatz der eindeutigen Profile, die nach Öffnen der E-Mail auf einen Link geklickt haben, im Verhältnis zu den eindeutigen Öffnungen. </td> 
  </tr>
  <tr> 
   <td> Eindeutige Klickrate<br/> </td> 
   <td> Prozentsatz der eindeutigen Profile, die auf mindestens einen Link in der E-Mail geklickt haben, im Verhältnis zur Anzahl der eindeutigen zugestellten E-Mails. </td> 
  </tr>
  <tr> 
   <td> Eindeutige Zustellungen<br/> </td> 
   <td> Anzahl der eindeutigen Profile, die mindestens eine E-Mail erfolgreich erhalten haben.</td> 
  </tr>
  <tr> 
   <td> Eindeutige E-Mail-Abo-Stornierungen<br/> </td> 
   <td> Anzahl der Profile, die sich vom Erhalt Ihrer E-Mails abgemeldet haben.<br/> </td> 
  </tr>
  <tr> 
   <td> Geschätzte Einzelöffnungen von E-Mails<br/> </td> 
   <td> Geschätzte Anzahl der eindeutigen E-Mail-Empfangenden, die die E-Mail wahrscheinlich geöffnet haben. Diese Metrik zielt darauf ab, eine genauere Anzahl der individuellen Interaktionen bereitzustellen, die von E-Mail-Servern zur Datenschutz- oder Sicherheitsprüfung ausgelöst werden. Hierzu wird eine eindeutige Öffnungsrate angewendet, die anhand eindeutiger Profile berechnet wird, welche die E-Mail manuell geöffnet haben, sowie denjenigen, deren E-Mails nur von E-Mail-Servern geöffnet wurden.<br/> </td> 
  </tr>
  <tr> 
   <td> Einzelöffungen<br/> </td> 
   <td> Anzahl der Profile, die den Versand geöffnet haben. <br> Beachten Sie, dass bei der Berechnung von Einzelöffnungen die letzten 10 Tage berücksichtigt werden. Wenn ein Profil mehrere Öffnungen innerhalb des Zeitraums von 10 Tagen registriert, werden diese als Einzelöffnungen gezählt. Wenn ein Profil jedoch zwei Öffnungen hat, die mehr als 10 Tage voneinander entfernt sind, werden sie nicht als Einzelöffnungen betrachtet.<br/> </td> 
  </tr> 
  <tr>
  <tr> 
   <td> Eindeutige Sendungen<br/> </td> 
   <td>Anzahl der eindeutigen Profile, für die mindestens eine E-Mail gesendet werden sollte.<br/> </td> 
  </tr>
  <tr> 
   <td> Eindeutige Sendefehler<br/> </td> 
   <td>Anzahl der eindeutigen Profile, bei denen während des ausgehenden Prozesses mindestens ein Sendefehler aufgetreten ist.<br/> </td> 
  </tr>
  <tr> 
   <td> Eindeutige Sendeausschlüsse<br/> </td> 
   <td>Anzahl der eindeutigen Profile, die aufgrund von Eignungsregeln, Zielgruppensegmentierung oder Profilstatus vom Nachrichtenempfang ausgeschlossen sind. <a href="exclusion-list.md">Erfahren Sie mehr darüber, wie Ausschlüsse gezählt werden</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Eindeutige Zielgruppe<br/> </td> 
   <td>Anzahl der eindeutigen Profile, die sich für die Zielgruppe qualifiziert haben, bevor Ausschlüsse, Unterdrückungen oder Einverständnisentnahmen angewendet wurden.<br/> </td> 
  </tr> 
  <tr> 
   <td> Abmeldungen<br/> </td> 
   <td> Gesamtanzahl der Klicks auf den Abmelde-Link.<br/> </td> 
  </tr> 
 </tbody> 
</table>

## SMS-Metriken

<table> 
  <thead> 
    <tr> 
      <th> SMS-Metrik </th> 
      <th> Definition </th> 
    </tr>
  </thead> 
  <tbody> 
    <tr> 
      <td>zugestellt</td> 
      <td>Anzahl der erfolgreich gesendeten SMS-Nachrichten im Verhältnis zur Gesamtzahl der SMS-Nachrichten.</td> 
    </tr>
    <tr> 
      <td>Klicks</td> 
      <td>Anzahl der Klicks auf einen Link innerhalb einer SMS-Nachricht.</td> 
    </tr>
    <tr> 
      <td>Bounces bei ausgehenden SMS-Nachrichten</td> 
      <td>Gesamtzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen im Verhältnis zur Gesamtzahl der gesendeten SMS-Nachrichten.</td> 
    </tr>
    <tr> 
      <td>Ausgehende SMS-Fehler</td> 
      <td>Gesamtzahl der aufgetretenen Fehler, die den Versand der SMS-Nachricht an Empfängerinnen und Empfänger verhindert haben.</td> 
    </tr>
    <tr> 
      <td>Ausgehende SMS-Ausschlüsse</td> 
      <td>Anzahl der Profile, die vom Empfang von SMS-Nachrichten durch Adobe Journey Optimizer ausgeschlossen wurden. <a href="exclusion-list.md">Erfahren Sie mehr darüber, wie Ausschlüsse gezählt werden</a>.</td> 
    </tr>
    <tr> 
      <td>Einzelklicks</td> 
      <td>Die Anzahl der eindeutigen Empfängerinnen und Empfänger, die auf Inhalt in einer E-Mail geklickt haben.</td> 
    </tr>
    <tr> 
      <td>Anzeigen</td> 
      <td>Anzahl, wie oft eine SMS-Nachricht angezeigt oder geöffnet wurde.</td> 
    </tr>
    <tr> 
      <td>Eindeutige Anzeigen</td> 
      <td>Anzahl der eindeutigen Empfängerinnen und Empfänger, die die SMS-Nachricht geöffnet haben, wobei mehrfache Interaktionen derselben Person nicht gezählt werden.</td> 
    </tr>
    <tr> 
      <td>Personen</td> 
      <td>Anzahl eindeutiger Benutzerprofile, die eine SMS-Nachricht erhalten oder mit ihr interagiert haben.</td> 
    </tr>
  </tbody> 
</table>

<!--
## Experimentation metrics {#experimentation-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td>App installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>App launches<br/> </td> 
   <td><br/> </td> 
</tr>
 <tr> 
   <td>Average lift<br/> </td> 
   <td> Percentage improvement in conversion rate of a given treatment over the baseline.<a href="../campaigns/experiment-calculations.md#understand-lift">Learn more</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Confidence<br/> </td> 
   <td>Evidence that a given treatment is the same as the baseline treatment. <a href="../campaigns/experiment-calculations.md#understand-confidence">Learn more</a>.<br/> </td> 
</tr>
  <tr> 
   <td>Confidence interval<br/> </td> 
   <td>Percentage difference in performance between the baseline and the best performing treatment. <a href="../campaigns/experiment-calculations.md#understand-intervals">Learn more</a>.<br/> </td> 
</tr> 
  <tr> 
   <td>Count per profile<br/> </td> 
   <td>Total value of the Experiment objective metric divided by the number of profiles.<br/> </td> 
</tr>
  <tr> 
   <td>Email Opens<br/> </td> 
   <td>Number of times the email was opened.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td>Number of clicks on the unsubscription link.<br/> </td> 
</tr>
  <tr> 
   <td>First app launches<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Outbound Clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Profiles<br/> </td> 
   <td>Number of profiles targeted for this treatment.<br/> </td> 
</tr>
  <tr> 
   <td>Unique email opens<br/> </td> 
   <td>Number of profiles who opened the email.<br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td>Number of profiles who clicked on the unsubscription link.<br/> </td>
</tr>
  <tr> 
   <td>Unique installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique launches<br/> </td> 
   <td><br/> </td> 
</tr> 
  <tr> 
   <td>Unique outbound clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique upgrades<br/> </td> 
   <td><br/> </td> 
</tr>
   <td>Upgrades<br/> </td> 
   <td><br/> </td> 
</tr> 
</tbody> 
</table>
-->

## In-App-Metriken {#inapp-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrik<br/> </th> 
   <th> Definition<br/> </th> 
  </tr>
 </thead> 
 <tbody>
  <tr> 
   <td>Klicks<br/> </td> 
   <td>Gesamtzahl der Profile, die mit den in der In-App-Nachricht enthaltenen Schaltflächen interagiert haben.<br/> </td> 
  </tr>
  <tr> 
   <td>Klickrate<br/> </td> 
   <td>Prozentualer Anteil der Benutzenden, die mit den in der In-App-Nachricht enthaltenen Schaltflächen interagiert haben, im Verhältnis zur Zahl der Benutzenden, die die Nachricht gesehen haben.<br/> </td> 
  </tr>
  <tr> 
   <td>Abbruchrate<br/> </td> 
   <td>Prozentsatz der In-App-Nachrichten, die von Profilen verworfen wurden.<br/> </td> 
  </tr>
  <tr> 
   <td>Impressions<br/> </td> 
   <td>Gesamtzahl der an alle Benutzenden gesendeten In-App-Nachrichten.<br/> </td>
  </tr>
  <tr> 
   <td>Einzel-Impressions<br/> </td> 
   <td>Anzahl der eindeutigen Benutzenden, an die die In-App-Nachricht gesendet wurde.<br/> </td>
  </tr>
  <tr> 
   <td>Anzeigen<br/> </td>
   <td>Anzahl, wie oft die In-App-Nachricht geöffnet wurde.<br/> </td>
  </tr>
  <tr> 
   <td>Einzelanzeigen<br/> </td>
   <td>Anzahl, wie oft die In-App-Nachricht geöffnet wurde, wobei mehrfache Interaktionen desselben Profils nicht gezählt werden.<br/> </td>
  </tr>
  <tr> 
   <td>Einzelklicks<br/> </td>
   <td>Die Anzahl der Profile, die auf Inhalt in Ihren In-App-Nachrichten geklickt haben.<br/> </td>
  </tr>
  <tr> 
   <td>Klicks<br/> </td>
   <td>Anzahl der Klicks auf Inhalt in Ihren In-App-Nachrichten.<br/> </td>
  </tr>
  <tr> 
   <td>Klickrate (CTR)<br/> </td>
   <td>Prozentsatz der Benutzenden, die mit den In-App-Nachrichten interagiert haben.<br/> </td>
  </tr>
  <tr> 
   <td>Klick-Öffnungsrate (CTOR)<br/> </td>
   <td>Anzahl, wie oft die In-App-Nachricht geöffnet wurde.<br/> </td>
  </tr>
  <tr> 
   <td>Sendungen<br/> </td>
   <td>Gesamtzahl der gesendeten In-App-Nachrichten.<br/> </td>
  </tr>
  <tr> 
   <td>Eingehend ausgelöst<br/> </td>
   <td>Anzahl, wie oft eine In-App-Nachricht durch eine Benutzerinteraktion oder ein vordefiniertes Ereignis ausgelöst wurde.<br/> </td>
  </tr>
  <tr> 
   <td>Eingehende Abweisungen<br/> </td>
   <td>Anzahl, wie oft Benutzende die In-App-Nachricht verworfen haben, ohne damit zu interagieren.<br/> </td>
  </tr>
 </tbody> 
</table>

## Metriken zu Push-Benachrichtigungen

<table> 
 <thead> 
  <tr> 
   <th> Metrik<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Aktionen<br/> </td> 
   <td> Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, beispielsweise Klicken auf eine Schaltfläche oder Abbrechen.<br/> </td> 
</tr>
  <tr> 
   <td>Bounces<br/> </td> 
   <td> Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.<br/> </td> 
</tr> 
  <tr> 
   <td> Bounce-Rate<br/> </td> 
   <td> Prozentsatz der Bounce-Push-Benachrichtigungen in Bezug auf die gesendeten Push-Benachrichtigungen.<br/> </td>
</tr>
  <tr> 
   <td> Zugestellt<br/> </td> 
   <td> Zahl der erfolgreich gesendeten Nachrichten im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.<br/> </td> 
</tr> 
  <tr> 
   <td> Zustellungsrate<br/> </td> 
   <td> Anzahl der erfolgreich gesendeten Push-Benachrichtigungen.<br/> </td> 
</tr>
  <tr> 
   <td>Interaktionen<br/> </td> 
   <td> Gesamtzahl der Öffnungen und Aktionen für diese Push-Benachrichtigung, also ob das Profil die Push-Benachrichtigung geöffnet hat oder ob eine Schaltfläche angeklickt wurde.<br/> </td> 
</tr> 
  <tr> 
   <td> Interaktionsrate<br/> </td> 
   <td> Prozentualer Anteil der Öffnungen und Aktionen für diese Push-Benachrichtigung, also ob das Profil die Push-Nachricht geöffnet hat oder ob eine Schaltfläche angeklickt wurde.<br/> </td> 
</tr>
  <tr> 
   <td> Fehler<br/> </td> 
   <td> Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.<br/> </td> 
</tr>
  <tr> 
   <td> Fehlerrate<br/> </td> 
   <td> Prozentualer Anteil der Fehler, die während eines Versands aufgetreten sind und den Versand verhindert haben, im Vergleich zu den gesendeten Push-Benachrichtigungen.<br/> </td> 
</tr>
  <tr> 
   <td> Fehlerursache<br/> </td> 
   <td> Name der spezifischen ursprünglichen Fehlerursache. <a href="exclusion-list.md">Weitere Informationen zu Fehlerursachen</a>.<br/> </td> 
</tr>
  <tr> 
   <td> Ausgeschlossen<br/> </td> 
   <td> Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.<br/> </td> 
</tr>
  <tr> 
   <td> Öffnungen<br/> </td> 
   <td> Gesamtzahl der Push-Benachrichtigungen, die an das Gerät gesendet und vom Benutzer angeklickt wurden, sodass die App geöffnet wurde. Dies ist ähnlich der Klick-Kategorie mit dem Unterschied, dass keine Push-Öffnung ausgelöst wird, wenn die Benachrichtigung verworfen wird.<br/> </td> 
</tr> 
  <tr> 
   <td> Öffnungsrate<br/> </td> 
   <td> Prozentsatz der geöffneten Push-Benachrichtigungen.<br/> </td> 
</tr>
  <tr> 
   <td> Benutzerdefinierte Push-Aktionen<br/> </td> 
   <td>Anzahl der benutzerdefinierten Aktionen, die von Profilen als Reaktion auf die Push-Benachrichtigungen ausgeführt wurden.<br/> </td> 
</tr>
  <tr> 
   <td> Gesendet<br/> </td> 
   <td> Gesamtzahl der gesendeten Nachrichten<br/> </td> 
</tr> 
  <tr> 
   <td> Zielgruppe<br/> </td> 
   <td> Gesamtzahl der Push-Nachrichten, die während der Versandanalyse verarbeitet wurden.<br/> </td> 
</tr>  
 </tbody> 
</table>

## Landingpage-Metriken {#landing-page-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrik<br/> </th> 
   <th> Definition<br/> </th> 
  </tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Bounce-Rate<br/> </td> 
   <td>Prozentualer Anteil der Personen, die die Landingpage angezeigt, aber nicht interagiert oder abonniert haben, im Verhältnis zur Gesamtzahl der Besuche.<br/> </td> 
</tr>
 <tr> 
   <td>Klicks<br/> </td> 
   <td>Anzahl der Klicks auf einen Inhalt der Landingpage.<br/> </td> 
</tr>

<tr> 
   <td>Landingpage-Konversionen<br/> </td> 
   <td>Anzahl der Personen, die mit der Landingpage interagiert haben, beispielsweise ein Formular ausgefüllt haben.<br/> </td> 
</tr>
<tr> 
   <td>Landingpage-Konversionsrate<br/> </td> 
   <td>Anzahl der Personen, die mit der Landingpage interagiert haben, beispielsweise ein Formular ausgefüllt haben, im Verhältnis zur Gesamtzahl der Besuche.<br/> </td> 
</tr>
 <tr> 
   <td>Landingpage-Ansichten<br/> </td> 
   <td>Gesamtzahl der Besuche auf Ihrer Landingpage, die von Journeys und externen Quellen stammen, einschließlich mehrfacher Besuche desselben Profils.<br/> </td> 
</tr>
<tr> 
   <td>Eindeutige Landingpage-Konversionen<br/> </td> 
   <td>Anzahl eindeutiger Personen, die mit der Landingpage interagiert haben, wobei mehrfache Interaktionen desselben Profils nicht gezählt werden.<br/> </td> 
</tr>
 <tr> 
   <td>Eindeutige Landingpage-Aufrufe<br/> </td> 
   <td>Anzahl eindeutiger Personen, die Ihre Landingpage besucht haben, wobei mehrfache Besuche desselben Profils nicht gezählt werden.<br/> </td> 
</tr>
 </tbody> 
</table>

## Direkt-Mail {#direct-mail}

<table> 
 <thead> 
  <tr> 
   <th> Metrik<br/> </th> 
   <th> Definition<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>Zugestellt<br/> </td> 
   <td>Anzahl der Direkt-Mail-Nachrichten, die Empfängerinnen und Empfängern erfolgreich zugestellt wurden.<br/> </td> 
</tr>
<tr> 
   <td>Ausgehende Fehler<br/> </td> 
   <td>Anzahl der Direkt-Mail-Nachrichten, bei denen während der Verarbeitung oder des Versands Fehler aufgetreten sind, was einen erfolgreichen Versand verhindert hat.<br/> </td> 
</tr>
<tr> 
   <td>Ausgehende Ausschlüsse<br/> </td> 
   <td>Anzahl der Profile, die aufgrund vordefinierter Kriterien oder Filterung durch Adobe Journey Optimizer vom Direkt-Mail-Empfang ausgeschlossen wurden. <a href="exclusion-list.md">Erfahren Sie mehr darüber, wie Ausschlüsse gezählt werden</a>.<br/> </td> 
</tr>
<tr> 
   <td>Profile<br/> </td> 
   <td>Anzahl der Benutzerprofile, die als Zielgruppe für die Direkt-Mail-Kampagne identifiziert wurden.<br/> </td> 
</tr>
<tr> 
   <td>Gesendet<br/> </td> 
   <td>Gesamtzahl der Direkt-Mail-Nachrichten, die im Rahmen der Kampagne erfolgreich gesendet wurden.<br/> </td> 
</tr>
<tr> 
   <td>Zielgruppe<br/> </td> 
   <td>Gesamtzahl der für den Versand vorbereiteten und verarbeiteten Direkt-Mail-Nachrichten.<br/> </td> 
</tr>
 </tbody> 
</table>


## Inhaltskarten-Metriken {#content-based}

<table> 
 <thead> 
  <tr> 
   <th> Metrik<br/> </th> 
   <th> Definition<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>Klickrate (CTR)<br/> </td> 
   <td>Prozentsatz der Benutzenden, die mit der Inhaltskarte interagiert haben.<br/> </td> 
</tr>
<tr> 
   <td>Klicks<br/> </td> 
   <td>Anzahl der Klicks auf Inhalt auf Ihrer Inhaltskarte.<br/> </td> 
</tr>
<tr> 
   <td>Anzeigen<br/> </td> 
   <td>Die Anzahl, wie oft die Nachricht geöffnet wurde.<br/> </td> 
</tr>
<tr> 
   <td>Personen<br/> </td> 
   <td>Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für Ihre Inhaltskarten eignen.<br/> </td> 
</tr>
<tr> 
   <td>Einzelklicks<br/> </td> 
   <td>Die Anzahl der Profile, die auf Inhalt auf Ihrer Inhaltskarte geklickt haben.<br/> </td> 
</tr>
<tr> 
   <td>Einzelanzeigen<br/> </td> 
   <td>Anzahl, wie oft die Nachricht geöffnet wurde, wobei mehrfache Interaktionen eines Profils nicht gezählt werden.<br/> </td> 
</tr>
 </tbody> 
</table>

## Web-Seiten-Metriken {#web}

<table> 
 <thead> 
  <tr> 
   <th> Metrik<br/> </th> 
   <th> Definition<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>Klicks<br/> </td> 
   <td>Anzahl der Klicks auf Inhalt auf Ihren Web-Seiten.<br/> </td> 
</tr>
<tr> 
   <td>Klickrate (CTR)<br/> </td> 
   <td>Prozentsatz der Benutzenden, die mit den Web-Seiten interagiert haben.<br/> </td> 
</tr>
<tr> 
   <td>Anzeigen<br/> </td> 
   <td>Anzahl, wie oft die Web-Seite geöffnet wurde.<br/> </td> 
</tr>
<tr> 
   <td>Personen<br/> </td> 
   <td>Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für Ihre Web-Seiten eignen.<br/> </td> 
</tr>
<tr> 
   <td>Einzelklicks<br/> </td> 
   <td>Anzahl der Profile, die auf Inhalt auf Ihren Web-Seiten geklickt haben.<br/> </td> 
</tr>
<tr> 
   <td>Einzelanzeigen<br/> </td> 
   <td>Anzahl, wie oft die Web-Seite geöffnet wurde, wobei mehrfache Interaktionen eines Profils nicht gezählt werden.<br/> </td> 
</tr>
 </tbody> 
</table>

## Code-basierte Erlebnismetriken {#code-based}

<table> 
 <thead> 
  <tr> 
   <th> Metrik<br/> </th> 
   <th> Definition<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>Klicks<br/> </td> 
   <td>Anzahl, wie oft Benutzende auf personalisierte Erlebnisse geklickt haben, die ihnen angezeigt wurden.<br/> </td> 
</tr>
<tr> 
   <td>Klickrate (CTR)<br/> </td> 
   <td>Prozentualer Anteil der Benutzenden, die auf einen Link, eine Anzeige oder eine Empfehlung klicken, verglichen mit der Häufigkeit, mit der Links, Anzeigen oder Empfehlungen angezeigt wurden.<br/> </td> 
</tr>
<tr> 
   <td>Konversionsrate<br/> </td> 
   <td>Prozentsatz der Anzeigen, die zu Benutzeraktionen (z. B. Klicks) geführt haben. Gibt an, wie erfolgreich das Modell Benutzende angesprochen hat.<br/> </td> 
</tr>
<tr> 
   <td>Leistung des Entscheidungselements<br/> </td> 
   <td>Wertet aus, wie gut die einzelnen Elemente Benutzende ansprechen und die gewünschten Aktionen fördern, z. B. Käufe, Klicks oder andere Reaktionen.<br/> </td> 
</tr>
<tr> 
   <td>Entscheidungsfindungs-KPIs<br/> </td> 
   <td>Wichtige Erkenntnisse zur Interaktion der Besuchenden mit Erlebnissen, einschließlich Gesamtelementen, Gesamtklicks, Gesamtanzeigen und Fallback-Rate.<br/> </td> 
</tr>
<tr> 
   <td>Anzeigen<br/> </td> 
   <td>Anzahl, wie oft personalisierte Erlebnisse für Benutzende über verschiedene Touchpoints angezeigt oder präsentiert wurden.<br/> </td> 
</tr>
<tr> 
   <td>Interaktionstrichter<br/> </td> 
   <td>Überwacht die Leistung personalisierter Erlebnisse, indem bewertet wird, wie effektiv jede Phase des Trichters Benutzerinteraktionen fördert.<br/> </td> 
</tr>
<tr> 
   <td>Interaktionstrichter nach Auswahlstrategie<br/> </td> 
   <td>Überwacht und analysiert, wie effektiv verschiedene Auswahlstrategien Benutzende mit personalisierten Erlebnissen ansprechen.<br/> </td> 
</tr>
<tr> 
   <td>Personen<br/> </td> 
   <td>Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für Ihre Code-basierten Erlebnisse eignen.<br/> </td> 
</tr>
<tr> 
   <td>Ranking-Strategie<br/> </td> 
   <td>Erkenntnisse zur Leistung von KI-gesteuerten Ranking-Modellen, die zwei Traffic-Typen vergleichen: „Modellgesteuert“ und „Holdout“.<br/> </td> 
</tr>
<tr> 
   <td>Top-Entscheidungselemente nach Klickrate<br/> </td> 
   <td>Hebt die Leistung einzelner Elemente basierend auf ihrer Klickrate hervor, um zu bewerten, mit welchen Elementen Benutzende am effektivsten angesprochen werden.<br/> </td> 
</tr>
<tr> 
   <td>Einzelklicks<br/> </td> 
   <td>Anzahl der Profile, die auf Inhalt in Ihren Code-basierten Erlebnissen geklickt haben.<br/> </td> 
</tr>
<tr> 
   <td>Einzelanzeigen<br/> </td> 
   <td>Anzahl, wie oft das Erlebnis geöffnet wurde, wobei mehrfache Interaktionen eines Profils nicht gezählt werden.<br/> </td> 
</tr>
 </tbody> 
</table>
