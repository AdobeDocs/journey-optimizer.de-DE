---
title: Live-Bericht
description: Erfahren Sie, wie Sie Daten aus dem Live-Bericht verwenden
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 8dd48bb2-a805-4c46-a16c-c68173a9ac08
source-git-commit: aecbf0f8bcfb8f6747ee072d891029a38f8f2ed1
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 100%

---

# Erste Schritte mit dem Live-Bericht {#live-report}

Verwenden Sie den **[!UICONTROL Live-Bericht]**, um die Wirkung und Leistung Ihrer Journeys und Nachrichten in Echtzeit in einem integrierten Dashboard zu messen und zu visualisieren.
Die Daten sind im **[!UICONTROL Live-Bericht]** verfügbar, sobald Ihr Versand erfolgt ist oder Ihre Journey auf der Registerkarte **[!UICONTROL Letzte 24 Std.]** ausgeführt wurde.

* Wenn Sie eine Journey im Kontext einer Journey anpeilen möchten, rufen Sie über das Menü **[!UICONTROL Journeys]** Ihre Journey auf und klicken Sie auf die Schaltfläche **[!UICONTROL Bericht anzeigen]**.

   ![](assets/report_journey.png)

* Wenn Sie eine Kampagne als Ziel wählen möchten, rufen Sie im Menü **[!UICONTROL Kampagnen]** Ihre Kampagne auf und klicken auf die Schaltfläche **[!UICONTROL Berichte]**.

   ![](assets/report_campaign.png)

* Wenn Sie vom **[!UICONTROL globalen Bericht]** zum **[!UICONTROL Live-Bericht]** für Ihren Versand wechseln möchten, klicken Sie auf **[!UICONTROL Letzte 24 Std.]** im Registerkarten-Umschalter.

   ![](assets/report_3.png)

Eine detaillierte Liste aller in Adobe Journey Optimizer verfügbaren Metriken finden Sie auf [dieser Seite](#list-of-components-live).

## Dashboard anpassen {#modify-dashboard}

Jedes Reporting-Dashboard kann durch Ändern der Größe oder Entfernen von Widgets geändert werden. Das Ändern der Widgets wirkt sich nur auf das Dashboard des aktuellen Benutzers aus. Andere Benutzer sehen ihre eigenen Dashboards oder die standardmäßig festgelegten.

1. Sie können mit der Umschaltleiste auswählen, ob Sie Testereignisse aus Ihren Berichten ausschließen möchten. Weitere Informationen zu Testereignissen finden Sie auf [dieser Seite](../building-journeys/testing-the-journey.md).

   Beachten Sie, dass die Option **[!UICONTROL Test-Ereignisse ausschließen]** nur für Journey-Berichte verfügbar ist.

   ![](assets/report_modify_6.png)

1. Um die Größe von Widgets zu ändern oder sie zu entfernen, klicken Sie auf **[!UICONTROL Ändern]**.

   ![](assets/report_modify_7.png)

1. Sie können die Größe der Widgets durch Ziehen an der rechten unteren Ecke anpassen.

   ![](assets/report_modify_8.png)

1. Klicken Sie auf **[!UICONTROL Entfernen]**, um alle Widgets zu entfernen, die Sie nicht benötigen.

   ![](assets/report_modify_9.png)

1. Wenn Sie mit der Anzeigereihenfolge und der Größe Ihrer Widgets zufrieden sind, klicken Sie auf **[!UICONTROL Speichern]**.

Ihr Dashboard ist jetzt gespeichert. Ihre verschiedenen Änderungen werden bei einer späteren Verwendung Ihrer Live-Berichte erneut angewendet. Verwenden Sie bei Bedarf die Option **[!UICONTROL Zurücksetzen]**, um die Standard-Widgets und ihre Standardreihenfolge wiederherzustellen.

## Liste von Komponenten {#list-of-components-live}

In den Tabellen unten finden Sie nach Versandtyp geordnet die Liste der Metriken, die in Berichten verwendet werden, sowie ihre Definitionen.

### Journey-Metriken {#journey-metrics}

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

### Metriken zu E-Mail und SMS             {#email-and-sms-metrics}

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
   <td> Absprungrate<br/> </td> 
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

### Landingpage-Metriken {#landing-page-metrics}

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
   <td>Bounce-Rate<br/> </td> 
   <td>Anzahl der Personen, die nicht mit der Landingpage interagiert und die Aktion zum Abonnieren nicht abgeschlossen haben.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>Klicks<br/> </td> 
   <td>Anzahl der Klicks auf einen Inhalt der Landingpage.<br/> </td> 
</tr>
 <tr> 
   <td>Klickrate<br/> </td> 
   <td>Prozentsatz der Klicks auf der Landingpage.<br/> </td>
</tr>
<tr>
<td>Konversion<br/> </td> 
   <td>Anzahl der Personen, die mit der Landingpage interagiert haben, beispielsweise ein Formular ausgefüllt haben.<br/> </td> 
</tr>
<tr>
   <td>Konversionsrate<br/> </td> 
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

