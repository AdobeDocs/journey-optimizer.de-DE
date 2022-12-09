---
solution: Journey Optimizer
product: journey optimizer
title: Campaign-Live-Bericht
description: Erfahren Sie, wie Sie Daten aus dem Campaign-Live-Bericht verwenden.
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 0%

---

# Campaign-Live-Bericht {#campaign-live-report}

Der Campaign-Live-Bericht ist direkt über Ihre Kampagne mit der Variablen **[!UICONTROL Live view]** Schaltfläche.

Die Kampagne **[!UICONTROL Live report]** wird mit den folgenden Registerkarten angezeigt:

* [Kampagne](#campaign-live)
* [Email](#email-live)
* [Push](#push-live)
* [SMS](#sms-live)


Die Kampagne **[!UICONTROL Live report]** ist in verschiedene Widgets unterteilt, die den Erfolg und die Fehler Ihrer Kampagne detailliert beschreiben. Jedes Widget kann bei Bedarf in der Größe angepasst und gelöscht werden. Weitere Informationen hierzu finden Sie in diesem Abschnitt [Abschnitt](../reports/live-report.md#modify-dashboard).

Eine detaillierte Liste aller in Adobe Journey Optimizer verfügbaren Metriken finden Sie unter [diese Seite](live-report.md#list-of-components-live).

## Tab Kampagne {#campaign-global}

### Versand {#delivery-global}

Die **[!UICONTROL Campaign Statistics]** -Widget beschreibt die wichtigsten Informationen zu Ihrer Kampagne:

* **[!UICONTROL Entered profiles]**: Anzahl der Profile, die die Journey begonnen haben.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## Email-Tab {#email-live}

In Ihrer Kampagne **[!UICONTROL Live report]**, die **[!UICONTROL Email]** im Tab werden die wichtigsten Informationen bezüglich der in Ihrer Kampagne gesendeten E-Mail-Sendungen aufgeführt.

![](assets/campaign_report_live_1.png)

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den E-Mail-Bericht verfügbar sind.

Die **[!UICONTROL Email Sending Statistics]** Widget beschreibt die wichtigsten Informationen zu Ihrer Nachricht:

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung.

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

Die **[!UICONTROL Sending metrics by Email]** Tabelle und **[!UICONTROL Email Summary]** -Diagramm zeigt den Erfolg Ihres Versands:

* **[!UICONTROL Sent]**: Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung.

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

* **[!UICONTROL Opens]**: Anzahl der Öffnungen einer Nachricht in einem Versand.

* **[!UICONTROL Clicks]**: Anzahl der Klicks auf einen Inhalt in einem Versand.

* **[!UICONTROL Unsubscribe]**: Anzahl der Klicks auf den Abmelde-Link.

* **[!UICONTROL Spam complaints]**: Gibt an, wie oft eine Nachricht als Spam oder Junk gekennzeichnet wurde.

Die **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** und **[!UICONTROL Hard and bounce - by Email]** -Widgets enthalten die verfügbaren Daten zu Bounce-Nachrichten, z. B.:

* **[!UICONTROL Hard bounce]**: Die Gesamtzahl der permanenten Fehler, z. B. eine falsche E-Mail-Adresse. Dies beinhaltet eine Fehlermeldung, die explizit angibt, dass die Adresse ungültig ist, z. B. &quot;Unbekannter Benutzer&quot;.

* **[!UICONTROL Soft bounce]**: Die Gesamtzahl der temporären Fehler, z. B. einer vollen Inbox.

* **[!UICONTROL Ignored]**: Die Gesamtzahl der temporären Ereignisse, z. B. &quot;Out of office&quot;, oder eines technischen Fehlers, z. B. wenn der Absendertyp Postmaster ist.

Die **[!UICONTROL Error Reasons]** und **[!UICONTROL Exclude Reasons]** Mit Diagrammen und Tabellen können Sie sehen, welcher Fehler und welche Ausschlüsse während des Versands aufgetreten sind.

Die **[!UICONTROL Email - Top recipient domain]** Anhand von Diagrammen und Tabellen wird beschrieben, welche Domänen von den Empfängern am häufigsten zum Öffnen der E-Mail verwendet werden.
+++

## Tab Push notification {#push-live}

In Ihrer Kampagne **[!UICONTROL Live report]**, die **[!UICONTROL Push notification]** im Tab werden die wichtigsten Informationen bezüglich der in Ihrer Kampagne gesendeten Push-Nachrichten aufgeführt.

![](assets/campaign_report_live_2.png)

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Push-Bericht verfügbar sind.

**[!UICONTROL Push notification sending performance]**, **[!UICONTROL Push notification summary]** und **[!UICONTROL Sending metrics - by Push]** Widgets zeigen die wichtigsten Informationen zu Ihrer Nachricht an:

* **[!UICONTROL Sent]**: Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung.

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

* **[!UICONTROL Opens]**: Anzahl der Öffnungen einer Nachricht in einem Versand.

* **[!UICONTROL Actions]**: Gesamtzahl der Aktionen, die mit der gesendeten Push-Benachrichtigung durchgeführt wurden, z. B. Klick auf eine Schaltfläche oder Abweisung.

* **[!UICONTROL Engagements]**: Gesamtzahl der Öffnungen und Aktionen für diese Push-Benachrichtigung, d. h. wenn das Profil die Push-Benachrichtigung geöffnet oder auf eine Schaltfläche geklickt hat.

Die **[!UICONTROL Error Reasons]** und **[!UICONTROL Exclude Reasons]** Mit Diagrammen und Tabellen können Sie sehen, welcher Fehler und welche Ausschlüsse während des Versands aufgetreten sind.

Die **[!UICONTROL Sending statistics - Failed]** -Widget können Sie sehen, wie viele Fehler und Bounces aufgetreten sind.

Die **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** und **[!UICONTROL Breakdown by platform]** Grafiken und Tabellen zeigen den Erfolg Ihrer Push-Benachrichtigung in Abhängigkeit vom Betriebssystem.
+++

## SMS-Tab {#sms-live}

In Ihrer Kampagne **[!UICONTROL Live report]**, die **[!UICONTROL SMS]** im Tab werden die wichtigsten Informationen bezüglich der in Ihrer Kampagne gesendeten SMS-Sendungen aufgeführt.

![](assets/campaign_report_live_3.png)

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den SMS-Bericht verfügbar sind.

Die **[!UICONTROL SMS - Sending statistics]** -Tabelle zeigt den Erfolg Ihres Versands:

* **[!UICONTROL Targeted]**: Anzahl der Benutzerprofile, die als Zielprofile für diesen Versand gelten.

* **[!UICONTROL Excluded]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

* **[!UICONTROL Sent]**: Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung.

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

Die **[!UICONTROL SMS Performance by date]** Widget erläutert die wichtigsten Informationen zu Ihrer Nachricht mit einem Diagramm:

* **[!UICONTROL Sent]**: Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Delivered]**: Anzahl der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung.

* **[!UICONTROL Errors]**: Gesamtzahl der bei einem Versand aufgetretenen Fehler, die den Versand an Profile verhinderten.

Die **[!UICONTROL Exclude Reasons]**, **[!UICONTROL Bounces Reasons]** und **[!UICONTROL Error Reasons]** Mit Diagrammen und Tabellen können Sie sehen, welcher Fehler und welche Ausschlüsse während des Versands aufgetreten sind.
+++

## Zusätzliche Ressourcen

* [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md)
* [Kampagne erstellen](../campaigns/create-campaign.md)
* [API-gesteuerte Kampagnen erstellen](../campaigns/api-triggered-campaigns.md)
* [Ändern oder Anhalten einer Kampagne](../campaigns/modify-stop-campaign.md)
* [Globaler Kampagnenbericht](campaign-global-report.md)
