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
source-wordcount: '0'
ht-degree: 0%

---

# Erste Schritte mit dem Live-Bericht {#live-report}

Verwenden Sie den **[!UICONTROL Live-Bericht]**, um die Wirkung und Leistung Ihrer Journeys und Nachrichten in Echtzeit in einem integrierten Dashboard zu messen und zu visualisieren.
Die Daten sind im Abschnitt **[!UICONTROL Live-Bericht]** unmittelbar nach dem Versand oder der Ausführung Ihrer Journey über die **[!UICONTROL Letzte 24 Stunden]** Registerkarte.

* Wenn Sie eine Journey im Kontext einer Journey ansprechen möchten, können Sie über die **[!UICONTROL Journey]** auf Ihre Journey zugreifen und auf die **[!UICONTROL Bericht anzeigen]** Schaltfläche.

   ![](assets/report_journey.png)

* Wenn Sie eine Kampagne als Ziel auswählen möchten, können Sie über die **[!UICONTROL Kampagnen]** , greifen Sie auf Ihre Kampagne zu und klicken Sie auf **[!UICONTROL Berichte]** Schaltfläche.

   ![](assets/report_campaign.png)

* Wenn Sie von der **[!UICONTROL Gesamtbericht]** der **[!UICONTROL Live-Bericht]** Klicken Sie für Ihren Versand auf **[!UICONTROL Letzte 24 Stunden]** über den Tab-Umschalter aus.

   ![](assets/report_3.png)

Eine detaillierte Liste aller in Adobe Journey Optimizer verfügbaren Metriken finden Sie unter [diese Seite](#list-of-components-live).

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
   <td> Gesamtzahl der Aktionen, die für eine Journey erfolgreich ausgeführt wurden.<br/> </td> 
</tr> 
  <tr> 
   <td> Eingegebene Profile<br/> </td> 
   <td> Gesamtzahl der Kontakte, die das Eintrittsereignis der Journey erreicht haben.<br/> </td> 
</tr>
  <tr> 
   <td> Fehler in Aktion<br/> </td> 
   <td>Gesamtzahl der Fehler, die bei Aktionen aufgetreten sind.<br/> </td> 
</tr> 
  <tr> 
   <td> Ausgehende Profile<br/> </td> 
   <td> Gesamtzahl der Personen, die die Journey verlassen haben.<br/> </td> 
</tr> 
  <tr> 
   <td> Fehlgeschlagene einzelne Journey<br/> </td> 
   <td> Gesamtzahl der einzelnen Journey, die nicht erfolgreich ausgeführt wurden.<br/> </td> 
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
   <td> Prozentsatz der Bounce-E-Mails in Bezug auf die gesendeten E-Mails<br/> </td> 
</tr>
  <tr> 
   <td> Klicks<br/> </td> 
   <td> Anzahl der Klicks auf einen Inhalt in einer E-Mail.<br/> </td> 
</tr> 
  <tr> 
   <td> Zugestellt <br/> </td> 
   <td> Anzahl der erfolgreich gesendeten Nachrichten.<br/></td> 
</tr> 
  <tr> 
   <td> Zustellrate<br/> </td> 
   <td> Prozentsatz der erfolgreich gesendeten Nachrichten<br/> </td> 
</tr>
  <tr> 
   <td> Fehler<br/> </td> 
   <td> Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.<br/> </td> 
</tr> 
  <tr> 
   <td> Fehlerrate<br/> </td> 
   <td> Prozentsatz der Fehler, die während eines Versands aufgetreten sind, der den Versand verhinderte, in Bezug auf die gesendeten E-Mails.<br/> </td> 
</tr>
  <tr> 
   <td> Ausgeschlossen<br/> </td> 
   <td> Anzahl der Profile, die von Adobe Journey Optimizer ausgeschlossen wurden.<br/> </td> 
</tr>
  <tr> 
   <td> Hardbounce<br/> </td> 
   <td> Die Gesamtzahl der permanenten Fehler, z. B. eine falsche E-Mail-Adresse. Dazu gehören Fehlermeldungen, die explizit eine ungültige Adresse anzeigen, wie etwa „Benutzer unbekannt“.<br/> </td>
</tr>
  <tr> 
   <td> Ignoriert<br/> </td> 
   <td> Die Gesamtzahl der temporären Ereignisse, z. B. "Out of office", oder eines technischen Fehlers, z. B. wenn der Absendertyp Postmaster ist.<br/> </td> 
</tr>
   <tr> 
   <td>Klickrate des Angebots<br/> </td> 
   <td>Prozentsatz der Benutzer, die mit dem Angebot interagiert haben.<br/> </td> 
</tr>
   <tr> 
   <td>Impressionsrate des Angebots<br/> </td> 
   <td>Prozentsatz der geöffneten Angebote in Bezug auf die Anzahl der gesendeten Angebote.<br/> </td> 
</tr>
   <tr> 
   <td>Name des Angebots<br/> </td> 
   <td> Name des im Versand hinzugefügten Angebots. Weiterführende Informationen zu Platzierungen finden Sie auf dieser <a href="../offers/offer-library/creating-personalized-offers.md">Seite</a>.<br/> </td> 
</tr>
   <tr> 
   <td>gesendetes Angebot<br/> </td> 
   <td>Gesamtzahl der gesendeten Nachrichten für das Angebot.<br/> </td> 
</tr> 
  <tr>
   <td>Öffnungen<br/> </td> 
   <td> Anzahl der Öffnungen der Nachricht.<br/> </td> 
</tr> 
  <tr> 
   <td> Öffnungsrate<br/> </td> 
   <td> Gesamtzahl der geöffneten E-Mails in Bezug auf die Anzahl der zugestellten E-Mails.<br/> </td> 
</tr>
  <tr> 
   <td>Platzierungsname<br/> </td> 
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
   <td> Gibt an, wie oft eine Nachricht als Spam oder Junk gekennzeichnet wurde.<br/> </td> 
</tr>
  <tr> 
   <td> Targeting<br/> </td> 
   <td> Gesamtzahl der bei der Analyse verarbeiteten Nachrichten.<br/> </td> 
</tr> 
  <tr> 
   <td> Einzelklicks<br/> </td> 
   <td> Anzahl der Empfänger, die einen Inhalt in einer E-Mail angeklickt haben<br/> </td> 
</tr> 
  <tr> 
   <td>Eindeutige Klickrate<br/> </td> 
   <td> Prozentsatz der Benutzer, die mit dem Versand interagiert haben<br/> </td> 
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
   <td>Absprungrate<br/> </td> 
   <td>Anzahl der Personen, die nicht mit der Landingpage interagiert und die Aktion zum Abonnieren nicht abgeschlossen haben.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>Klicks<br/> </td> 
   <td>Anzahl der Klicks auf einen Inhalt auf der Landingpage.<br/> </td> 
</tr>
 <tr> 
   <td>Klickrate<br/> </td> 
   <td>Prozentsatz der Klicks auf die Landingpage<br/> </td>
</tr>
<tr>
<td>Konversion<br/> </td> 
   <td>Anzahl der Personen, die mit der Landingpage interagiert haben, z. B. Abonnenten eines Formulars.<br/> </td> 
</tr>
<tr>
   <td>Konversionsrate<br/> </td> 
   <td>Anzahl der Personen, die mit der Landingpage interagiert haben, z. B. Abonnenten eines Formulars.<br/> </td> 
</tr>
 <tr> 
   <td>Journey<br/> </td> 
   <td>Anzahl der Besuche auf einer Landingpage von einer Journey.<br/> </td> 
</tr>
 <tr> 
   <td>Andere Quellen<br/> </td> 
   <td>Anzahl der Besuche auf Ihrer Landingpage von einer externen Quelle anstelle einer Journey.<br/> </td> 
</tr>
 <tr> 
   <td>Besuche insgesamt<br/> </td> 
   <td> Gesamtzahl der Besuche auf Ihrer Landingpage von Journey und externen Quellen, einschließlich mehrerer Besuche eines Empfängers.<br/> </td> 
</tr>
 <tr> 
   <td>Unique Visitors<br/> </td> 
   <td>Anzahl der Personen, die Ihre Landingpage besucht haben, wobei mehrere Besuche eines Empfängers nicht berücksichtigt werden.<br/> </td> 
</tr>
 <tr> 
   <td>Besuche<br/> </td> 
   <td>Anzahl der Besuche auf Ihrer Landingpage, einschließlich mehrerer Besuche eines Empfängers.<br/> </td> 
</tr>
 </tbody> 
</table>

