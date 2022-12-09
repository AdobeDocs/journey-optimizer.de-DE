---
solution: Journey Optimizer
product: journey optimizer
title: Campaign Global-Bericht
description: Erfahren Sie, wie Sie Daten aus dem Campaign Global-Bericht verwenden.
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1468'
ht-degree: 0%

---

# Campaign Global-Bericht {#campaign-global-report}

Der globale Campaign-Bericht ist direkt über Ihre Kampagne mit der Variablen **[!UICONTROL All time]** Schaltfläche.

![](assets/campaign_report_global_5.png)

Die Kampagne **[!UICONTROL Global report]** wird mit den folgenden Registerkarten angezeigt:

* [Kampagne](#campaign-global)
* [Email](#email-global)
* [Push](#push-global)
* [SMS](#sms-global)

Die Kampagne **[!UICONTROL Global report]** ist in verschiedene Widgets unterteilt, die den Erfolg und die Fehler Ihrer Kampagne detailliert beschreiben. Jedes Widget kann bei Bedarf in der Größe angepasst und gelöscht werden. Weitere Informationen hierzu finden Sie in diesem Abschnitt [Abschnitt](../reports/global-report.md#modify-dashboard).

Eine detaillierte Liste aller in Adobe Journey Optimizer verfügbaren Metriken finden Sie unter [diese Seite](global-report.md#list-of-components-global.md)

## Tab Kampagne {#campaign-global}

### Versand {#delivery-global}

![](assets/campaign_report_global_1.png)

Die **[!UICONTROL Campaign's Statistics]** -Widget beschreibt die wichtigsten Informationen zu Ihrer Kampagne:

* **[!UICONTROL Entered profiles]**: Anzahl der Profile, die die Journey begonnen haben.

* **[!UICONTROL Actions delivered]**: Gesamtzahl der einmaligen Bereitstellungen einer Aktion in der Journey.

* **[!UICONTROL Actions failed in %]**: Gesamtzahl der eindeutigen Male, die eine Aktion in der Journey fehlgeschlagen ist, in Bezug auf die Gesamtzahl der eindeutigen Male, als eine Aktion bereitgestellt wurde.

## Email-Tab {#email-global}

![](assets/campaign_report_global_2.png)

In Ihrer Kampagne **[!UICONTROL Global report]**, die **[!UICONTROL Email]** im Tab werden die wichtigsten Informationen bezüglich der in Ihrer Kampagne gesendeten E-Mail-Sendungen aufgeführt.

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den E-Mail-Bericht verfügbar sind.

Die **[!UICONTROL Email Sending Statistics]** -Diagramm zeigt den Erfolg Ihres Versands:

* **[!UICONTROL Targeted]**: Gesamtzahl der bei der Versandanalyse verarbeiteten Nachrichten.

* **[!UICONTROL Sent]**: Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivery Rate]**: Prozentsatz der erfolgreich gesendeten Nachrichten

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounce Rate]**: Prozentsatz der Bounce-E-Mails in Bezug auf die gesendeten E-Mails

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

* **[!UICONTROL Error Rate]**: Prozentsatz der Fehler, die während eines Versands aufgetreten sind, der den Versand verhinderte, in Bezug auf die gesendeten E-Mails.

* **[!UICONTROL Retries]**: Anzahl der E-Mails in der Warteschlange für weitere Zustellversuche.

* **[!UICONTROL Excluded]**: Anzahl der Profile, die von Adobe Journey Optimizer ausgeschlossen wurden.

Die **[!UICONTROL Email - Tracking statistics]** -Widget enthält die für die Empfängeraktivität für Ihren Versand verfügbaren Daten:

* **[!UICONTROL Opens]**: Anzahl der Öffnungen des Versands in einem Versand.

* **[!UICONTROL Unique Opens]**: Prozentsatz der geöffneten Sendungen

* **[!UICONTROL Open Rate]**: Gesamtzahl der geöffneten E-Mails in Bezug auf die Anzahl der zugestellten E-Mails.

* **[!UICONTROL Clicks]**: Anzahl der Klicks auf einen Inhalt in einer E-Mail.

* **[!UICONTROL Unique Clicks]**:Anzahl der Empfänger, die einen Inhalt in einer E-Mail angeklickt haben

* **[!UICONTROL Unique Click Rate]**: Prozentsatz der Benutzer, die mit dem Versand interagiert haben

* **[!UICONTROL Unsubscriptions]**: Anzahl der Klicks auf den Abmelde-Link.

* **[!UICONTROL Spam complaints]**: Gibt an, wie oft eine Nachricht als Spam oder Junk gekennzeichnet wurde.

Die **[!UICONTROL Sending Statistics]** -Diagramm enthält die Daten, die für gesendete E-Mails verfügbar sind, z. B.:

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Retries]**: Anzahl der E-Mails in der Warteschlange für weitere Zustellversuche.

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

Die **[!UICONTROL Bounce Reasons]** und **[!UICONTROL Bounce categories]** -Widgets enthalten die verfügbaren Daten zu Bounce-Nachrichten, z. B.:

* **[!UICONTROL Hard bounce]**: Die Gesamtzahl der permanenten Fehler, z. B. eine falsche E-Mail-Adresse. Dies beinhaltet eine Fehlermeldung, die explizit angibt, dass die Adresse ungültig ist, z. B. &quot;Unbekannter Benutzer&quot;.

* **[!UICONTROL Soft bounce]**: Die Gesamtzahl der temporären Fehler, z. B. einer vollen Inbox.

* **[!UICONTROL Ignored]**: Die Gesamtzahl der temporären Ereignisse, z. B. &quot;Out of office&quot;, oder eines technischen Fehlers, z. B. wenn der Absendertyp Postmaster ist.

Weiterführende Informationen zu Bounces finden Sie im Abschnitt [Unterdrückungsliste](../reports/suppression-list.md) Seite.

Die **[!UICONTROL Error Reasons]** Anhand von Diagrammen und Tabellen können Sie sehen, welcher Fehler während des Versands aufgetreten ist.

Die **[!UICONTROL Excluded reasons]** Diagramm und Tabelle zeigen die unterschiedlichen Gründe an, die verhindern, dass aus den Zielgruppenprofilen ausgeschlossene Benutzerprofile die Nachricht empfangen.

Die **[!UICONTROL Email - Top Url]** In Diagrammen und Tabellen wird beschrieben, welche URLs aus Ihrem Versand am häufigsten besucht werden.

Die **[!UICONTROL Email - Top recipient domain]** Anhand von Diagrammen und Tabellen wird beschrieben, welche Domänen von den Empfängern am häufigsten zum Öffnen der E-Mail verwendet werden.

>[!NOTE]
>
>Die **[!UICONTROL Optimized vs non optimized]** und **[!UICONTROL Send time optimization]**  -Widgets sind nur verfügbar, wenn die Option Sendezeitoptimierung für Ihren Versand aktiviert ist. Weitere Informationen zur Sendezeitoptimierung finden Sie unter [diese Seite](../building-journeys/journeys-message.md#send-time-optimization).

Die **[!UICONTROL Optimized vs non optimized]** -Diagramm zeigt die wichtigsten Informationen bezüglich Ihrer Nachricht an, ob sie optimiert wurden oder nicht:

* **[!UICONTROL Sent]**: Gesamtzahl der gesendeten Nachrichten
* **[!UICONTROL Opens]**: Anzahl der Öffnungen des Versands in einem Versand.
* **[!UICONTROL Clicks]**: Anzahl der Klicks auf einen Inhalt in einer E-Mail.

Die **[!UICONTROL Send time optimization]** zeigt den Erfolg Ihres Versands in Abhängigkeit von der Versandmethode an: optimiert oder normal.

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten
* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.
+++

## Tab Push notification {#push-global}

In Ihrer Kampagne **[!UICONTROL Global report]**, die **[!UICONTROL Push notification]** im Tab werden die wichtigsten Informationen bezüglich der in Ihrer Kampagne gesendeten Push-Nachrichten aufgeführt.

![](assets/campaign_report_global_3.png)

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Push-Bericht verfügbar sind.

Die **[!UICONTROL Push notification - Sending statistics]** -Tabelle enthält die wichtigsten Informationen zu Ihren Push-Benachrichtigungen mit Diagrammen und KPIs:

* **[!UICONTROL Targeted]**: Gesamtzahl der bei der Versandanalyse verarbeiteten Nachrichten.

* **[!UICONTROL Sent]**: Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivery Rate]**: Prozentsatz der erfolgreich gesendeten Nachrichten

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounce Rate]**: Prozentsatz der Bounce-Push-Benachrichtigungen in Bezug auf die gesendeten Push-Benachrichtigungen

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

* **[!UICONTROL Error Rate]**: Prozentsatz der Fehler, die während eines Versands aufgetreten sind, der den Versand verhinderte, in Bezug auf die gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Excluded]**: Anzahl der Profile, die von Adobe Journey Optimizer ausgeschlossen wurden.

Die **[!UICONTROL Push - Tracking statistics]** enthält die für die Empfängeraktivität für Ihren Versand verfügbaren Daten:

* **[!UICONTROL Opens]**: Anzahl der Öffnungen einer Nachricht in einem Versand.

* **[!UICONTROL Open Rate]**: Prozentsatz der geöffneten Push-Benachrichtigungen

* **[!UICONTROL Actions]**: Gesamtzahl der Aktionen, die mit der gesendeten Push-Benachrichtigung durchgeführt wurden, z. B. Klick auf eine Schaltfläche oder Abweisung.

* **[!UICONTROL Engagements]**: Gesamtzahl der Öffnungen und Aktionen für diese Push-Benachrichtigung, d. h. wenn das Profil die Push-Benachrichtigung geöffnet oder auf eine Schaltfläche geklickt hat.

* **[!UICONTROL Engagement Rate]**: Prozentsatz der Öffnungen und Aktionen für diese Push-Benachrichtigung, d. h. wenn das Profil die Push-Benachrichtigung geöffnet oder auf eine Schaltfläche geklickt hat

Die **[!UICONTROL Push notification summary]** Das Diagramm enthält die Daten, die für gesendete Push-Benachrichtigungen verfügbar sind, z. B.:

* **[!UICONTROL Opens]**: Anzahl der Öffnungen einer Nachricht in einem Versand.

* **[!UICONTROL Actions]**: Gesamtzahl der Aktionen, die mit der gesendeten Push-Benachrichtigung durchgeführt wurden, z. B. Klick auf eine Schaltfläche oder Abweisung.

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

>[!NOTE]
>
>Die **[!UICONTROL Optimized vs non optimized]** und **[!UICONTROL Send time optimization]**  -Widgets sind nur verfügbar, wenn die Option Sendezeitoptimierung für Ihren Versand aktiviert ist. Weitere Informationen zur Sendezeitoptimierung finden Sie unter [diese Seite](../building-journeys/journeys-message.md#send-time-optimization).

Die **[!UICONTROL Optimized vs non optimized]** -Diagramm zeigt die wichtigsten Informationen bezüglich Ihrer Nachricht an, ob sie optimiert wurden oder nicht:

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten
* **[!UICONTROL Opens]**: Anzahl der Öffnungen des Versands in einem Versand.
* **[!UICONTROL Actions]**: Gesamtzahl der Aktionen, die mit der gesendeten Push-Benachrichtigung durchgeführt wurden, z. B. Klick auf eine Schaltfläche oder Abweisung.

Die **[!UICONTROL Send time optimization]** zeigt den Erfolg Ihres Versands in Abhängigkeit von der Versandmethode an: optimiert oder normal.

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten
* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

Die **[!UICONTROL Error Reasons]** Anhand von Diagrammen und Tabellen können Sie sehen, welcher Fehler während des Versands aufgetreten ist.

Die **[!UICONTROL Excluded reasons]** Diagramm und Tabelle zeigen die unterschiedlichen Gründe an, die verhindern, dass aus den Zielgruppenprofilen ausgeschlossene Benutzerprofile die Nachricht empfangen.

Die **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** und **[!UICONTROL Breakdown by platform]** Grafiken und Tabellen zeigen den Erfolg Ihrer Push-Benachrichtigung in Abhängigkeit vom Betriebssystem Ihres Empfängers.
+++

## SMS-Tab {#sms-global}

In Ihrer Kampagne **[!UICONTROL Global report]**, die **[!UICONTROL SMS]** im Tab werden die wichtigsten Informationen bezüglich der in Ihrer Kampagne gesendeten SMS-Sendungen aufgeführt.

![](assets/campaign_report_global_4.png)

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den SMS-Bericht verfügbar sind.

Die **[!UICONTROL SMS - Sending statistics]** -Tabelle zeigt den Erfolg Ihres Versands:

* **[!UICONTROL Targeted]**: Anzahl der Benutzerprofile, die als Zielprofile für diesen Versand gelten.

* **[!UICONTROL Excluded]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

* **[!UICONTROL Sent]**: Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

Die **[!UICONTROL SMS Performance by date]** Widget erläutert die wichtigsten Informationen zu Ihrer Nachricht mit einem Diagramm:

* **[!UICONTROL Sent]**: Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

Die **[!UICONTROL Exclude Reasons]**, **[!UICONTROL Bounces Reasons]** und **[!UICONTROL Error Reasons]** Mit Diagrammen und Tabellen können Sie sehen, welcher Fehler und welche Ausschlüsse während des Versands aufgetreten sind.
+++

## Zusätzliche Ressourcen

* [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md)
* [Kampagne erstellen](../campaigns/create-campaign.md)
* [API-gesteuerte Kampagnen erstellen](../campaigns/api-triggered-campaigns.md)
* [Ändern oder Anhalten einer Kampagne](../campaigns/modify-stop-campaign.md)
* [Campaign-Live-Bericht](campaign-live-report.md)
