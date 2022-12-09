---
solution: Journey Optimizer
product: journey optimizer
title: Gesamtbericht
description: Erfahren Sie, wie Sie Daten aus dem globalen Bericht verwenden
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: 7c7faa5e672d5ed6d7a083db50b206d11ecc4184
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 0%

---

# Erste Schritte mit dem globalen Bericht {#global-report}

>[!NOTE]
>
> Wenn bei Verwendung des Query-Dienstes benutzerdefinierte Abfragen über APIs durchgeführt werden, erwarten Sie einige Verzögerungen bei Ihren Berichten.

Verwenden Sie die **[!UICONTROL Global report]** , um die Wirkung Ihrer Journeys und Sendungen über einen ausgewählten Zeitraum zu messen.

* Wenn Sie eine Journey oder Sendungen im Kontext einer Journey als Ziel auswählen möchten, können Sie über die **[!UICONTROL Journeys]** , greifen Sie auf Ihre Journey zu und klicken Sie auf **[!UICONTROL View report]** Schaltfläche. Anschließend finden Sie die globalen Berichte Journey, E-Mail, SMS und Push .

   ![](assets/report_journey.png)

* Wenn Sie eine Kampagne als Ziel auswählen möchten, können Sie über die **[!UICONTROL Campaigns]** , greifen Sie auf Ihre Kampagne zu und klicken Sie auf **[!UICONTROL Reports]** Schaltfläche.

   ![](assets/report_campaign.png)

* Wenn Sie von der **[!UICONTROL Live report]** der **[!UICONTROL Global report]** Klicken Sie für Ihren Versand auf **[!UICONTROL All time]** über den Tab-Umschalter aus.

   ![](assets/report_5.png)

Eine detaillierte Liste aller in Adobe Journey Optimizer verfügbaren Metriken finden Sie unter [diese Seite](#list-of-components-global)

## Dashboard anpassen {#modify-dashboard}

Jedes Berichts-Dashboard kann durch Ändern des Zeitraums und Ändern der Größe oder Entfernung von Widgets geändert werden. Das Ändern der Widgets wirkt sich nur auf das Dashboard des aktuellen Benutzers aus. Andere Benutzer sehen ihre eigenen Dashboards oder die standardmäßig festgelegten Dashboards.

1. Wählen Sie aus Ihrem globalen Bericht eine Start- und Endzeit aus, um bestimmte Daten auszuwählen.

   ![](assets/report_modify_1.png)

1. Wählen Sie mit der Umschalter-Leiste aus, ob Sie Testereignisse aus Ihren Berichten ausschließen möchten. Weitere Informationen zu Testereignissen finden Sie unter [diese Seite](../building-journeys/testing-the-journey.md).

   Beachten Sie Folgendes: **[!UICONTROL Exclude test events]** ist nur für Journey-Berichte verfügbar.

   ![](assets/report_modify_2.png)

1. Klicken **[!UICONTROL Modify]** , um mit der Anpassung Ihres Dashboards zu beginnen.

   ![](assets/report_modify_3.png)

1. Passen Sie die Größe der Widgets an, indem Sie die untere rechte Ecke ziehen.

   ![](assets/report_modify_4.png)

1. Klicken **[!UICONTROL Remove]** um alle Widgets zu entfernen, die Sie nicht benötigen.

   ![](assets/report_modify_5.png)

1. Wenn Sie mit der Anzeigereihenfolge und der Größe Ihrer Widgets zufrieden sind, klicken Sie auf **[!UICONTROL Save]**.

Ihr Dashboard wurde jetzt gespeichert. Ihre verschiedenen Änderungen werden für eine spätere Verwendung Ihrer Live-Berichte erneut angewendet. Verwenden Sie bei Bedarf die **[!UICONTROL Reset]** -Option, um die Reihenfolge der Standard-Widgets und -Widgets wiederherzustellen.

## Liste von Komponenten {#list-of-components-global}

In den Tabellen unten finden Sie die Liste der Metriken, die in Berichten verwendet werden, sowie ihre Definitionen je nach Versandtyp.

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
   <td> Gesamtzahl der Kontakte, die die Journey verlassen haben.<br/> </td> 
</tr> 
  <tr> 
   <td> Fehlgeschlagene individuelle Journey<br/> </td> 
   <td> Gesamtzahl der einzelnen Journeys, die nicht erfolgreich ausgeführt wurden.<br/> </td> 
</tr> 
 </tbody> 
</table>

### E-Mail- und SMS-Metriken {#email-and-sms-metrics}

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
   <td> Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.<br/> </td> 
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
   <td> Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten<br/></td> 
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
   <td> Die Gesamtzahl der permanenten Fehler, z. B. eine falsche E-Mail-Adresse. Dies beinhaltet eine Fehlermeldung, die explizit angibt, dass die Adresse ungültig ist, z. B. "Unbekannter Benutzer".<br/> </td>
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
   <td>Angebotsname<br/> </td> 
   <td> Name des im Versand hinzugefügten Angebots. Weiterführende Informationen zur Platzierung finden Sie in diesem Abschnitt <a href="../offers/offer-library/creating-personalized-offers.md">page</a>.<br/> </td> 
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
   <td> Name der Platzierung, die zur Anzeige Ihres Angebots verwendet wird. Weiterführende Informationen zur Platzierung finden Sie in diesem Abschnitt <a href="../offers/offer-library/creating-placements.md">page</a>. </td> 
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
   <td> Gesamtzahl der temporären Fehler, z. B. einer vollen Inbox.<br/> </td> 
</tr>
  <tr> 
   <td> Beschwerden wegen Spam<br/> </td> 
   <td> Gibt an, wie oft eine Nachricht als Spam oder Junk gekennzeichnet wurde.<br/> </td> 
</tr>
  <tr> 
   <td> Targeting<br/> </td> 
   <td> Gesamtzahl der bei der Versandanalyse verarbeiteten Nachrichten.<br/> </td> 
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
   <td> Einzelöffnungen<br/> </td> 
   <td>Anzahl der Empfänger, die den Versand geöffnet haben<br/> </td> 
</tr> 
  <tr> 
   <td> Abmeldungen<br/> </td> 
   <td> Anzahl der Klicks auf den Abmelde-Link.<br/> </td> 
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

### Metriken zu Push-Benachrichtigungen

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
   <td> Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.<br/> </td> 
</tr> 
  <tr> 
   <td> Absprungrate<br/> </td> 
   <td> Prozentsatz der Bounce-Push-Benachrichtigungen in Bezug auf die gesendeten Push-Benachrichtigungen<br/> </td>
</tr>
  <tr> 
   <td> Zugestellt<br/> </td> 
   <td> Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten<br/> </td> 
</tr> 
  <tr> 
   <td> Zustellrate<br/> </td> 
   <td> Prozentsatz der erfolgreich gesendeten Push-Benachrichtigungen<br/> </td> 
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
   <td> Gesamtzahl der Push-Benachrichtigungen, die an das Gerät gesendet und von Benutzern angeklickt wurden, sodass die App geöffnet wurde. Dies ähnelt dem Push-Klick , bis auf die Tatsache, dass keine Push-Öffnung ausgelöst wird, wenn die Benachrichtigung verworfen wird.<br/> </td> 
</tr> 
  <tr> 
   <td> Öffnungsrate<br/> </td> 
   <td> Prozentsatz der geöffneten Push-Benachrichtigungen<br/> </td> 
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
   <td>Journey(s)<br/> </td> 
   <td>Anzahl der Besuche Ihrer Landingpage von einer Journey.<br/> </td> 
</tr>
 <tr> 
   <td>Andere Quellen<br/> </td> 
   <td>Anzahl der Besuche auf Ihrer Landingpage, die von einer externen Quelle statt von einer Journey stammen.<br/> </td> 
</tr>
 <tr> 
   <td>Besuche insgesamt<br/> </td> 
   <td> Gesamtzahl der Besuche Ihrer Landingpage durch Journeys und externe Quellen, einschließlich mehrerer Besuche eines Empfängers.<br/> </td> 
</tr>
 <tr> 
   <td>Unique Visitors<br/> </td> 
   <td>Anzahl der Personen, die Ihre Landingpage besucht haben, mehrere Besuche eines Empfängers werden nicht berücksichtigt.<br/> </td> 
</tr>
 <tr> 
   <td>Besuche<br/> </td> 
   <td>Anzahl der Besuche auf Ihrer Landingpage, einschließlich mehrerer Besuche eines Empfängers.<br/> </td> 
</tr>
 </tbody> 
</table>

### Metriken zu Push-Benachrichtigungen

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
   <td> Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.<br/> </td> 
</tr> 
  <tr> 
   <td> Absprungrate<br/> </td> 
   <td> Prozentsatz der Bounce-Push-Benachrichtigungen in Bezug auf die gesendeten Push-Benachrichtigungen<br/> </td>
</tr>
  <tr> 
   <td> Zugestellt<br/> </td> 
   <td> Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten<br/> </td> 
</tr> 
  <tr> 
   <td> Zustellrate<br/> </td> 
   <td> Prozentsatz der erfolgreich gesendeten Push-Benachrichtigungen<br/> </td> 
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
   <td> Gesamtzahl der Push-Benachrichtigungen, die an das Gerät gesendet und von Benutzern angeklickt wurden, sodass die App geöffnet wurde. Dies ähnelt dem Push-Klick , bis auf die Tatsache, dass keine Push-Öffnung ausgelöst wird, wenn die Benachrichtigung verworfen wird.<br/> </td> 
</tr> 
  <tr> 
   <td> Öffnungsrate<br/> </td> 
   <td> Prozentsatz der geöffneten Push-Benachrichtigungen<br/> </td> 
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

<!--
### In-app metrics {#inapp-metrics}
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
   <td>Click rate<br/> </td> 
   <td>Percentage of users who interacted with the buttons included in the In-app message compared to users who saw the message.<br/> </td> 
</tr> 
  <tr> 
   <td>Dismiss rate<br/> </td> 
   <td> Percentage of In-app messages that recipients dismissed.<br/> </td> 
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
