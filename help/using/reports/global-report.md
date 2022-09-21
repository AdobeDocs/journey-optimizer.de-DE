---
title: Globaler Bericht
description: Erfahren Sie, wie Sie Daten aus dem globalen Bericht verwenden
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: aecbf0f8bcfb8f6747ee072d891029a38f8f2ed1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Erste Schritte mit dem globalen Bericht {#global-report}

>[!NOTE]
>
> Wenn benutzerdefinierte Abfragen über APIs unter Verwendung des Abfrage-Service durchgeführt werden, treten bei Ihren Berichten möglicherweise Verzögerungen auf.

Mit dem **[!UICONTROL globalen Bericht]** können Sie die Effektivität Ihrer Journeys und Ihrer Sendungen über einen bestimmten Zeitraum messen.

* Wenn Sie eine Journey oder Sendungen innerhalb einer Journey auswählen möchten, greifen Sie im Menü **[!UICONTROL Journeys]** auf Ihre Journey zu und klicken Sie auf das Symbol **[!UICONTROL Bericht anzeigen]**. Dort finden Sie die globalen Berichte zu Journeys, E-Mail-Nachrichten, SMS und Push-Benachrichtigungen.

   ![](assets/report_journey.png)

* Wenn Sie eine Kampagne als Ziel auswählen möchten, können Sie über die **[!UICONTROL Kampagnen]** , greifen Sie auf Ihre Kampagne zu und klicken Sie auf **[!UICONTROL Berichte]** Schaltfläche.

   ![](assets/report_campaign.png)

* Wenn Sie von der **[!UICONTROL Live-Bericht]** der **[!UICONTROL Gesamtbericht]** Klicken Sie für Ihren Versand auf **[!UICONTROL Ganzzeit]** über den Tab-Umschalter aus.

   ![](assets/report_5.png)

Eine detaillierte Liste aller in Adobe Journey Optimizer verfügbaren Metriken finden Sie unter [diese Seite](#list-of-components-global)

## Anpassen des Dashboards {#modify-dashboard}

Jedes Berichts-Dashboard kann durch das Ändern des Zeitraums und das Ändern der Größe von Widgets oder das Entfernen von Widgets geändert werden. Das Ändern der Widgets wirkt sich nur auf das Dashboard des aktuellen Benutzers aus. Andere Benutzer sehen ihre eigenen Dashboards oder die standardmäßig festgelegten.

1. Wählen Sie aus Ihrem globalen Bericht eine Start- und Endzeit aus, um auf bestimmte Daten zuzugreifen.

   ![](assets/report_modify_1.png)

1. Sie können mit der Umschaltleiste auswählen, ob Sie Testereignisse aus Ihren Berichten ausschließen möchten. Weitere Informationen zu Testereignissen finden Sie auf [dieser Seite](../building-journeys/testing-the-journey.md).

   Beachten Sie, dass die Option **[!UICONTROL Test-Ereignisse ausschließen]** nur für Journey-Berichte verfügbar ist.

   ![](assets/report_modify_2.png)

1. Klicken Sie auf **[!UICONTROL Ändern]**, um mit der Anpassung Ihres Dashboards zu beginnen.

   ![](assets/report_modify_3.png)

1. Sie können die Größe der Widgets durch Ziehen an der rechten unteren Ecke anpassen.

   ![](assets/report_modify_4.png)

1. Klicken Sie auf **[!UICONTROL Entfernen]**, um alle Widgets zu entfernen, die Sie nicht benötigen.

   ![](assets/report_modify_5.png)

1. Wenn Sie mit der Anzeigereihenfolge und der Größe Ihrer Widgets zufrieden sind, klicken Sie auf **[!UICONTROL Speichern]**.

Ihr Dashboard ist jetzt gespeichert. Ihre verschiedenen Änderungen werden bei einer späteren Verwendung Ihrer Live-Berichte erneut angewendet. Verwenden Sie bei Bedarf die Option **[!UICONTROL Zurücksetzen]**, um die Standard-Widgets und ihre Standardreihenfolge wiederherzustellen.

## Liste von Komponenten {#list-of-components-global}

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
   <td> Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.<br/> </td> 
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
   <td> Zahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten.<br/></td> 
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

<!--
### Experimentation metrics {#experimentation-metrics}
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
   <td>.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td><br/> </td> 
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
   <td><br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td><br/> </td>
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

### Metriken zu Push-Benachrichtigungen             {#push-notification-metrics}

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
   <td> Gesamtzahl der Aktionen, die mit der gesendeten Push-Benachrichtigung durchgeführt wurden, z. B. Klick auf eine Schaltfläche oder Abweisung.<br/> </td> 
</tr>
  <tr> 
   <td>Bounces<br/> </td> 
   <td> Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.<br/> </td> 
</tr> 
  <tr> 
   <td> Absprungrate<br/> </td> 
   <td> Prozentsatz der Bounce-Push-Benachrichtigungen in Bezug auf die gesendeten Push-Benachrichtigungen.<br/> </td>
</tr>
  <tr> 
   <td> Zugestellt<br/> </td> 
   <td> Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten<br/> </td> 
</tr> 
  <tr> 
   <td> Zustellrate<br/> </td> 
   <td> Anzahl der erfolgreich gesendeten Push-Benachrichtigungen.<br/> </td> 
</tr>
  <tr> 
   <td>Interaktionen<br/> </td> 
   <td> Gesamtzahl der Öffnungen und Aktionen für diese Push-Benachrichtigung, d. h. wenn das Profil die Push-Benachrichtigung geöffnet oder auf eine Schaltfläche geklickt hat.<br/> </td> 
</tr> 
  <tr> 
   <td> Interaktionsrate<br/> </td> 
   <td> Prozentsatz der Öffnungen und Aktionen für diese Push-Benachrichtigung, d. h. wenn das Profil die Push-Benachrichtigung geöffnet oder auf eine Schaltfläche geklickt hat<br/> </td> 
</tr>
  <tr> 
   <td> Fehler<br/> </td> 
   <td> Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.<br/> </td> 
</tr>
  <tr> 
   <td> Fehlerrate<br/> </td> 
   <td> Prozentsatz der Fehler, die während eines Versands aufgetreten sind, der den Versand verhinderte, in Bezug auf die gesendeten Push-Benachrichtigungen.<br/> </td> 
</tr> 
  <tr> 
   <td> Ausgeschlossen<br/> </td> 
   <td> Anzahl der Profile, die von Adobe Journey Optimizer ausgeschlossen wurden.<br/> </td> 
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
   <td> Gesendet<br/> </td> 
   <td> Gesamtzahl der gesendeten Nachrichten<br/> </td> 
</tr> 
  <tr> 
   <td> Targeting<br/> </td> 
   <td> Gesamtzahl der während der Versandanalyse verarbeiteten Push-Nachrichten.<br/> </td> 
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
   <td>Anzahl der Personen, die nicht mit der Landingpage interagiert haben und die Aktion zum Anmelden nicht abgeschlossen haben, in Bezug auf die Gesamtzahl der Besuche.<br/> </td> 
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
   <td>Anzahl der Personen, die mit der Landingpage interagiert haben, z. B. Benutzer, die sich für ein Formular angemeldet haben, in Bezug auf die Gesamtzahl der Besuche.<br/> </td> 
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

