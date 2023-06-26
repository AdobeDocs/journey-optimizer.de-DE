---
solution: Journey Optimizer
product: journey optimizer
title: Liste von Komponenten
description: Erfahren Sie, wie Sie Daten aus dem Live-Bericht verwenden
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: d6ec55e5-e44e-4773-a561-d1bc0919ea04
source-git-commit: 26456f7c2d879843eb533209377b83fc0ccb5617
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 100%

---

# Liste von Komponenten {#list-of-components-live}

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
   <td>Erfolgreich ausgeführte Aktionen<br/> </td> 
   <td> Gesamtzahl der erfolgreich ausgeführten Aktionen für eine Journey<br/>. </td> 
</tr> 
  <tr> 
   <td> Eingetretene Profile<br/> </td> 
   <td> Gesamtzahl der Einzelanwendenden, die das Eintrittsereignis der Journey erreicht haben.<br/> </td> 
</tr>
  <tr> 
   <td> Fehler bei Aktion<br/> </td> 
   <td>Gesamtzahl der Fehler, die bei Aktionen aufgetreten sind.<br/> </td> 
</tr> 
  <tr> 
   <td> Ausgestiegene Profile<br/> </td> 
   <td> Gesamtzahl der Einzelanwendenden, die die Journey verlassen haben<br/> </td> 
</tr> 
  <tr> 
   <td> Fehlgeschlagene einzelne Journey<br/> </td> 
   <td> Gesamtzahl der einzelnen Journeys, die nicht erfolgreich ausgeführt wurden.<br/> </td> 
</tr> 
 </tbody> 
</table>

## Dimensionen und Metriken für E-Mail und SMS {#email-and-sms-metrics}

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
   <td> Gesamtzahl der kumulierten Fehler beim Versand und der automatischen Bounce-Verarbeitung.<br/> </td> 
</tr> 
  <tr> 
   <td> Bounce-Rate<br/> </td> 
   <td> Prozentsatz der Bounce-E-Mails im Vergleich zu den gesendeten E-Mails<br/> </td> 
</tr>
  <tr> 
   <td> Klicks<br/> </td> 
   <td> Anzahl der Klicks auf einen Inhalt in einer E-Mail.<br/> </td> 
</tr> 
  <tr> 
   <td> Zugestellt <br/> </td> 
   <td> Anzahl der erfolgreich versendeten Nachrichten.<br/></td> 
</tr> 
  <tr> 
   <td> Zustellungsrate<br/> </td> 
   <td> Prozentsatz der erfolgreich gesendeten Nachrichten<br/> </td> 
</tr>
  <tr> 
   <td> Fehler<br/> </td> 
   <td> Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.<br/> </td> 
</tr> 
  <tr> 
   <td> Fehlerrate<br/> </td> 
   <td> Prozentsatz der Fehler, die während des Versands auftraten und die Zustellung verhinderten, im Vergleich zur Zahl der gesendeten E-Mails.<br/> </td> 
</tr>
  <tr> 
   <td> Ausgeschlossen<br/> </td> 
   <td> Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.<br/> </td> 
</tr>
  <tr> 
   <td> Hardbounce<br/> </td> 
   <td> Gesamtzahl der permanenten Fehler, wie beispielsweise eine falsche E-Mail-Adresse. Dazu gehören Fehlermeldungen, die explizit eine ungültige Adresse anzeigen, wie etwa „Benutzer unbekannt“.<br/> </td>
</tr>
  <tr> 
   <td> Ignoriert<br/> </td> 
   <td> Die Gesamtzahl der temporären Fehler, wie beispielsweise Abwesenheit oder technische Fehler, etwa wenn der Absendertyp Postmaster ist.<br/> </td> 
</tr>
   <tr> 
   <td>Klickrate des Angebots<br/> </td> 
   <td>Prozentsatz der Benutzenden, die mit dem Angebot interagiert haben.<br/> </td> 
</tr>
   <tr> 
   <td>Impressionsrate des Angebots<br/> </td> 
   <td>Prozentsatz der geöffneten Angebote im Verhältnis zur Anzahl der gesendeten Angebote.<br/> </td> 
</tr>
   <tr> 
   <td>Name des Angebots<br/> </td> 
   <td> Name des im Versand hinzugefügten Angebots. Weiterführende Informationen zu Platzierungen finden Sie auf dieser <a href="../offers/offer-library/creating-personalized-offers.md">Seite</a>.<br/> </td> 
</tr>
   <tr> 
   <td>Gesendetes Angebot<br/> </td> 
   <td>Gesamtzahl der Sendevorgänge für das Angebot.<br/> </td> 
</tr> 
  <tr>
   <td>Öffnungen<br/> </td> 
   <td> Die Anzahl, wie oft die Nachricht geöffnet wurde.<br/> </td> 
</tr> 
  <tr> 
   <td> Öffnungsrate<br/> </td> 
   <td> Gesamtzahl der geöffneten E-Mails im Vergleich zur Anzahl der zugestellten E-Mails.<br/> </td> 
</tr>
  <tr> 
   <td>Name der Platzierung<br/> </td> 
   <td> Name der Platzierung, die zur Anzeige Ihres Angebots verwendet wird. Weiterführende Informationen zu Platzierungen finden Sie auf dieser <a href="../offers/offer-library/creating-placements.md">Seite</a>. </td> 
</tr> 
  <tr> 
   <td> Weitere Zustellversuche<br/> </td> 
   <td> Anzahl der E-Mails in der Warteschlange für weitere Zustellversuche.<br/> </td> 
</tr> 
  <tr> 
   <td> Gesendet<br/> </td> 
   <td> Gesamtzahl der gesendeten Nachrichten<br/> </td> 
</tr>
  <tr> 
   <td> Softbounce<br/> </td> 
   <td> Gesamtzahl der temporären Fehler, beispielsweise einer vollen Inbox<br/> </td> 
</tr>
  <tr> 
   <td> Spam-Beschwerden<br/> </td> 
   <td> Anzahl der Fälle, in denen eine Nachricht als Spam oder Junk deklariert wurde.<br/> </td> 
</tr>
  <tr> 
   <td> Zielgruppe<br/> </td> 
   <td> Gesamtzahl der bei der Versandanalyse verarbeiteten Nachrichten.<br/> </td> 
</tr> 
  <tr> 
   <td> Einzelklicks<br/> </td> 
   <td> Die Anzahl der Empfänger, die auf einen Inhalt in einer E-Mail geklickt haben.<br/> </td> 
</tr> 
  <tr> 
   <td>Einzelklickrate<br/> </td> 
   <td> Prozentualer Anteil der Benutzenden, die mit dem Versand interagiert haben.<br/> </td> 
</tr>
  <tr> 
   <td> Einzelöffungen<br/> </td> 
   <td>Anzahl der Empfänger, die den Versand geöffnet haben<br/> </td> 
</tr> 
  <tr> 
   <td> Abmeldungen<br/> </td> 
   <td> Gesamtanzahl der Klicks auf den Abmelde-Link.<br/> </td> 
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
  <td>Bounces<br/> </td> 
   <td>Anzahl der Personen, die nicht mit der Landingpage interagiert und die Aktion zum Abonnieren nicht abgeschlossen haben.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>Klicks<br/> </td> 
   <td>Anzahl der Klicks auf einen Inhalt der Landingpage.<br/> </td> 
</tr>
<tr>
<td>Konversion<br/> </td> 
   <td>Anzahl der Personen, die mit der Landingpage interagiert haben, beispielsweise ein Formular ausgefüllt haben.<br/> </td> 
</tr>
 <tr> 
   <td>Journey(s)<br/> </td> 
   <td>Anzahl der Besuche auf einer Landingpage von einer Journey.<br/> </td> 
</tr>
 <tr> 
   <td>Andere Quellen<br/> </td> 
   <td>Anzahl der Besuche auf Ihrer Landingpage, die von einer externen Quelle anstelle einer Journey stammen.<br/> </td> 
</tr>
 <tr> 
   <td>Besuche insgesamt<br/> </td> 
   <td> Gesamtzahl der Besuche auf Ihrer Landingpage, die von Journeys und externen Quellen stammen, einschließlich mehrerer Besuche eines Empfängers.<br/> </td> 
</tr>
 <tr> 
   <td>Unique Visitors<br/> </td> 
   <td>Anzahl der Personen, die Ihre Landingpage besucht haben, wobei mehrfache Besuche eines Empfängers nicht berücksichtigt werden.<br/> </td> 
</tr>
 <tr> 
   <td>Besuche<br/> </td> 
   <td>Anzahl der Besuche auf einer Landingpage, einschließlich mehrfacher Besuche eines Empfängers.<br/> </td> 
</tr>
 </tbody> 
</table>

## Metriken zu Push-Benachrichtigungen             {#push-notification-metrics}

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
   <td> Gesamtzahl der kumulierten Fehler beim Versand und der automatischen Bounce-Verarbeitung.<br/> </td> 
</tr> 
  <tr> 
   <td> Zugestellt<br/> </td> 
   <td> Anzahl der erfolgreich versendeten Nachrichten.<br/> </td> 
</tr> 
  <tr> 
   <td>Interaktionen<br/> </td> 
   <td> Gesamtzahl der Öffnungen und Aktionen für diese Push-Benachrichtigung, also ob das Profil die Push-Benachrichtigung geöffnet hat oder ob eine Schaltfläche angeklickt wurde.<br/> </td> 
</tr> 
  <tr> 
   <td> Fehler<br/> </td> 
   <td> Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.<br/> </td> 
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
   <td> Gesendet<br/> </td> 
   <td> Gesamtzahl der gesendeten Nachrichten<br/> </td> 
</tr> 
  <tr> 
   <td> Zielgruppe<br/> </td> 
   <td> Gesamtzahl der Push-Nachrichten, die während der Versandanalyse verarbeitet wurden.<br/> </td> 
</tr>  
 </tbody> 
</table>

<!--
## In-app metrics {#inapp-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Clicks<br/> </td> 
   <td>Total number of recipients who interacted with the buttons included in the In-app message.<br/> </td> 
</tr>
  <tr> 
   <td>Impressions<br/> </td> 
   <td> Total number of In-app messages delivered to all users.<br/> </td>
</tr>
  <tr> 
   <td>Unique impressions<br/> </td> 
   <td>Number of unique users to whom the In-app message was delivered.<br/> </td>
</tr>
 </tbody> 
</table>
-->
