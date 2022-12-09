---
solution: Journey Optimizer
product: journey optimizer
title: Globaler Journey-Bericht
description: Erfahren Sie, wie Sie Daten aus dem globalen Journey-Bericht verwenden.
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1732'
ht-degree: 0%

---

# Globaler Journey-Bericht {#journey-global-report}

Der globale Journey-Bericht ist direkt von Ihrer Journey aus mit dem **[!UICONTROL View report]** Schaltfläche.

![](assets/report_journey.png)

Die Journey **[!UICONTROL Global report]** wird mit den folgenden Registerkarten angezeigt:

* [Journey](#journey-global)
* [Email](#email-global)
* [Push](#push-global)
* [SMS](#sms-global)

Die Journey **[!UICONTROL Global report]** ist in verschiedene Widgets unterteilt, die den Erfolg und die Fehler Ihrer Journey detailliert beschreiben. Jedes Widget kann bei Bedarf in der Größe angepasst und gelöscht werden. Weitere Informationen hierzu finden Sie in diesem Abschnitt [Abschnitt](global-report.md#modify-dashboard).

Eine detaillierte Liste aller in Adobe Journey Optimizer verfügbaren Metriken finden Sie unter [diese Seite](global-report.md#list-of-components-global).

## Registerkarte &quot;Journey&quot; {#journey-global}

Von Ihrer Reise aus **[!UICONTROL Global report]**, die **[!UICONTROL Journey]** bietet einen klaren Überblick über die wichtigsten Tracking-Daten zu Ihrer Journey.

![](assets/journey_global_1.png)

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Journey-Bericht verfügbar sind.

Die **[!UICONTROL Journey Performance]** -Widget ermöglicht es Ihnen, den Pfad Ihrer Zielprofile Schritt für Schritt durch Ihre Journey anzuzeigen.

Die **[!UICONTROL Journey Statistics]** Widget zeigt die folgenden KPIs an:

* **[!UICONTROL Entered profiles]**: Gesamtzahl der Kontakte, die das Eintrittsereignis der Journey erreicht haben.

* **[!UICONTROL Exited profiles]**: Gesamtzahl der Kontakte, die die Journey verlassen haben.

* **[!UICONTROL Failed individual journey]**: Gesamtzahl der einzelnen Journeys, die nicht erfolgreich ausgeführt wurden.

Die **[!UICONTROL Events received by event]**, **[!UICONTROL Events by origin]** und **[!UICONTROL Top events]** Widgets ermöglichen es Ihnen zu sehen, welche Ihrer **[!UICONTROL Events]** wurde erfolgreich über Diagramme und Tabellen ausgeführt.

**[!UICONTROL Action Performance]**, **[!UICONTROL Action Error Reasons]** und **[!UICONTROL Top Actions]** Widgets stellen die erfolgreichste Aktion und Fehler dar, die beim **[!UICONTROL Actions]** ausgelöst wurden.

Die **[!UICONTROL Top Actions]** -Tabelle enthält die verfügbaren Daten für **[!UICONTROL Actions]**, z. B.:

* **[!UICONTROL Actions successfully executed]**: Gesamtzahl der **[!UICONTROL Actions]** für eine Journey erfolgreich ausgeführt wurde.

* **[!UICONTROL Error in action]**: Gesamtzahl der aufgetretenen Fehler für **[!UICONTROL Actions]**.

Die **[!UICONTROL Consent policies]** Tabelle und Diagramm zeigen die Anzahl der Profile an, die aus den einzelnen Richtlinien in Ihren benutzerdefinierten Aktionen ausgeschlossen sind.
Weitere Informationen zu benutzerdefinierten Aktionen finden Sie unter [die ausführliche Dokumentation](../action/about-custom-action-configuration.md).

Damit diese Widgets in Ihren Journeys-Berichten angezeigt werden, müssen Sie Ihre Dashboards zurücksetzen. Klicken Sie dazu auf **[!UICONTROL Modify]** then **[!UICONTROL Reset]** oben in Ihrem Bericht.
+++

## Email-Tab {#email-global}

Von Ihrer Reise aus **[!UICONTROL Global report]**, die **[!UICONTROL Email]** enthält die wichtigsten Informationen zu den in Ihrer Journey gesendeten E-Mail-Sendungen.

![](assets/journey_global_2.png)

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den E-Mail-Bericht verfügbar sind.

Die **[!UICONTROL Email Sending Statistics]** -Diagramm zeigt den Erfolg Ihres Versands:

* **[!UICONTROL Targeted]**: Anzahl der Profile, die von Adobe Journey Orchestration für beliebige Aktionen wie das Senden von E-Mails oder SMS ausgewählt werden.

* **[!UICONTROL Sent]**: Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivery Rate]**: Prozentsatz der erfolgreich gesendeten Nachrichten

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounce Rate]**: Prozentsatz der Bounce-E-Mails in Bezug auf die gesendeten E-Mails

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

* **[!UICONTROL Error Rate]**: Prozentsatz der Fehler, die während eines Versands aufgetreten sind, der den Versand verhinderte, in Bezug auf die gesendeten E-Mails.

Die **[!UICONTROL Email - Tracking statistics]** enthält die für die Empfängeraktivität für Ihren Versand verfügbaren Daten:

* **[!UICONTROL Opens]**: Anzahl der Öffnungen des Versands in einem Versand.

* **[!UICONTROL Unique Opens]**: Prozentsatz der geöffneten Sendungen

* **[!UICONTROL Unique Open Rate]**: Gesamtzahl der geöffneten E-Mails in Bezug auf die Anzahl der zugestellten E-Mails.

* **[!UICONTROL Clicks]**: Anzahl der Klicks auf einen Inhalt in einer E-Mail.

* **[!UICONTROL Unique Clicks]**:Anzahl der Empfänger, die einen Inhalt in einer E-Mail angeklickt haben

* **[!UICONTROL Click through rate]**: Prozentsatz der Benutzer, die mit der Journey interagiert haben.

* **[!UICONTROL Unsubscribe]**: Anzahl der Klicks auf den Abmelde-Link.

* **[!UICONTROL Spam complaints]**: Gibt an, wie oft eine Nachricht als Spam oder Junk gekennzeichnet wurde.

Die **[!UICONTROL Sending Statistics]** -Diagramm enthält die Daten, die für gesendete E-Mails verfügbar sind, z. B.:

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

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

>[!NOTE]
>
>Die Widgets Angebote und Metriken sind nur verfügbar, wenn eine Entscheidung in eine E-Mail eingefügt wurde. Weiterführende Informationen zur Entscheidungsverwaltung finden Sie in diesem [page](../offers/get-started/starting-offer-decisioning.md).

Die **[!UICONTROL Offers statistic]** und **[!UICONTROL Offers statistics]** über Widgets vom Typ Zeit hinweg messen Sie den Erfolg und die Wirkung Ihres Angebots auf Ihre Zielgruppe. Sie enthalten die wichtigsten Informationen zu Ihrer Nachricht mit KPIs:

* **[!UICONTROL Offer sent]**: Gesamtzahl der gesendeten Nachrichten für das Angebot.

* **[!UICONTROL Offer impression]**: Anzahl der Öffnungen des Angebots in einem Versand.

* **[!UICONTROL Offer clicks]**: Anzahl der Klicks auf ein Angebot in einem Versand.

Die **[!UICONTROL Offers detailed statistic]** enthält die für die Empfängeraktivität mit Ihrem Angebot verfügbaren Daten:

* **[!UICONTROL Placement name]**: Name der Platzierung, die zur Anzeige Ihres Angebots verwendet wird. Weiterführende Informationen zur Platzierung finden Sie in diesem Abschnitt [page](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Offer name]**: Name des im Versand hinzugefügten Angebots. Weiterführende Informationen zur Platzierung finden Sie in diesem Abschnitt [page](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offer sent]**: Gesamtzahl der gesendeten Nachrichten für das Angebot.

* **[!UICONTROL Offer impression rate]**: Prozentsatz der geöffneten Angebote in Bezug auf die Anzahl der gesendeten Angebote.

* **[!UICONTROL Offer click rate]**: Prozentsatz der Benutzer, die mit dem Angebot interagiert haben.
+++

## Tab Push notification {#push-global}

Von Ihrer Reise aus **[!UICONTROL Global report]**, die **[!UICONTROL Push notification]** im Tab werden die wichtigsten Informationen zu den in Ihrer Journey gesendeten Push-Nachrichten aufgeführt.

![](assets/journey_global_3.png)

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Push-Bericht verfügbar sind.

Die **[!UICONTROL Push notification - Sending statistics]** -Tabelle enthält die wichtigsten Informationen zu Ihren Push-Benachrichtigungen mit Diagrammen und KPIs:

* **[!UICONTROL Targeted]**: Anzahl der Profile, die von Adobe Journey Orchestration für beliebige Aktionen wie das Senden von E-Mails oder SMS ausgewählt werden.

* **[!UICONTROL Sent]**: Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivery Rate]**: Prozentsatz der erfolgreich gesendeten Nachrichten

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounce Rate]**: Prozentsatz der Bounce-Push-Benachrichtigungen in Bezug auf die gesendeten Push-Benachrichtigungen

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

* **[!UICONTROL Error Rate]**: Prozentsatz der Fehler, die während eines Versands aufgetreten sind, der den Versand verhinderte, in Bezug auf die gesendeten Push-Benachrichtigungen.

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

SMS **[!UICONTROL Global report]** ist in verschiedene Widgets unterteilt, in denen der Erfolg und die Fehler Ihres Versands detailliert beschrieben werden. Jedes Widget kann bei Bedarf in der Größe angepasst und gelöscht werden. Weitere Informationen hierzu finden Sie in diesem Abschnitt [Abschnitt](global-report.md#modify-dashboard).
+++

## SMS-Tab {#sms-global}

![](assets/journey_global_4.png)

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den SMS-Bericht verfügbar sind.

Die **[!UICONTROL SMS - Sending statistics]** -Tabelle zeigt den Erfolg Ihres Versands:

* **[!UICONTROL Targeted]**: Anzahl der Benutzerprofile, die als Zielprofile für diesen Versand gelten.

* **[!UICONTROL Excluded]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

* **[!UICONTROL Sent]**: Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

Die **[!UICONTROL SMS summary]** Widget erläutert die wichtigsten Informationen zu Ihrer Nachricht mit einem Diagramm:

* **[!UICONTROL Sent]**: Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

Die **[!UICONTROL Exclude Reasons]** Mit Diagrammen und Tabellen können Sie sehen, welcher Fehler und welche Ausschlüsse während des Versands aufgetreten sind.
+++
