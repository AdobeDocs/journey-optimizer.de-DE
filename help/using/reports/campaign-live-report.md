---
title: Live-Bericht in Campaign
description: Erfahren Sie, wie Sie Daten aus dem Live-Bericht in Campaign verwenden
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 95%

---

# Live-Bericht einer Kampagne {#campaign-live-report}

Der Campaign-Live-Bericht ist direkt über Ihre Kampagne mit der Variablen **[!UICONTROL Berichte]** Schaltfläche.

![](assets/campaign_report_1.png)

Nach Auswahl der **[!UICONTROL Letzte 24 Stunden]** im Tab Kampagne **[!UICONTROL Live-Bericht]** wird mit den folgenden Registerkarten angezeigt:

* [Campaign](#campaign-live)
* [E-Mail](#email-live)
* [Push-Benachrichtigung](#push-live)

Der **[!UICONTROL Live-Bericht]** in Campaign ist in verschiedene Widgets unterteilt, die Erfolge und Fehler bei Ihrer Kampagne detailliert beschreiben. Jedes Widget kann bei Bedarf angepasst und gelöscht werden. Weiterführende Informationen dazu finden Sie in diesem [Abschnitt](../reports/live-report.md#modify-dashboard).

## Registerkarte „Kampagne“ {#campaign-global}

### Versand {#delivery-global}

Das Widget **[!UICONTROL Kampagnenstatistiken]** enthält die wichtigsten Informationen zu Ihrer Kampagne:

* **[!UICONTROL Eingetretene Profile]**: Anzahl der Profile, die mit der Journey begonnen haben.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->
## Registerkarte „E-Mail“ {#email-live}

In Ihrem **[!UICONTROL Live-Bericht]** in Campaign finden Sie auf der Registerkarte **[!UICONTROL E-Mail]** die wichtigsten Informationen zu den E-Mail-Nachrichten, die in Ihrer Kampagne gesendet wurden.

Das Widget **[!UICONTROL E-Mail-Versandstatistik]** enthält die wichtigsten Informationen zu Ihrer Nachricht:

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.

Die Tabelle **[!UICONTROL Versandmetriken nach E-Mail]** und das Diagramm **[!UICONTROL E-Mail-Zusammenfassung]** zeigen, wie erfolgreich Ihr Versand war:

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen einer Nachricht in einem Versand.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in einem Versand.

* **[!UICONTROL Abo beenden]**: Zahl der Klicks auf den Abmelde-Link.

* **[!UICONTROL Beschwerden wegen Spam]**: Gibt an, wie oft eine Nachricht als Spam oder Junk gekennzeichnet wurde.

Die Widgets **[!UICONTROL Bounce-Gründe]**, **[!UICONTROL Bounce-Kategorien]** und **[!UICONTROL Hardbounces und Softbounces – nach E-Mail]** enthalten die verfügbaren Daten im Zusammenhang mit unzustellbaren Nachrichten, wie z. B:

* **[!UICONTROL Hardbounce]**: die Gesamtzahl der permanenten Fehler, wie eine falsche E-Mail-Adresse. Dazu gehören Fehlermeldungen, die explizit eine ungültige Adresse anzeigen, wie etwa „Benutzer unbekannt“.

* **[!UICONTROL Softbounce]**: die Gesamtzahl der temporären Fehler, wie ein voller Posteingang.

* **[!UICONTROL Ignoriert]**: Die Gesamtzahl der temporären Ereignisse, beispielsweise Abwesenheit, oder technischer Fehler, zum Beispiel wenn der Absendertyp Postmaster ist.

In den Diagrammen und Tabellen **[!UICONTROL Fehlerursachen]** und **[!UICONTROL Ausschlussgründe]** sehen Sie, welcher Fehler und welche Ausschlüsse während des Versands aufgetreten sind.

Das Diagramm **[!UICONTROL E-Mail – beste Empfänger-Domain]** und die Tabelle zeigen, welche Domains von Empfängern am häufigsten zum Öffnen der E-Mail verwendet werden.

## Registerkarte „Push-Benachrichtigung“ {#push-live}

In Ihrem **[!UICONTROL Live-Bericht]** in Campaign finden Sie auf der Registerkarte **[!UICONTROL Push-Benachrichtigung]** die wichtigsten Informationen zu den Sendungen von Push-Benachrichtigungen, die in Ihrer Kampagne gesendet wurden.

Die Widgets **[!UICONTROL Performance des Push-Benachrichtigungsversandes]**, **[!UICONTROL Push-Benachrichtigungs-Zusammenfassung]** und **[!UICONTROL Sendemetriken – nach Push-Benachrichtigungen]** zeigen Details zu den wichtigsten Informationen in Bezug auf Ihre Nachricht:

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen einer Nachricht in einem Versand.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf Schaltfläche oder Abbruch.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Öffnungen und Aktionen für diese Push-Benachrichtigung, d. h. wenn das Profil die Push-Benachrichtigung geöffnet hat oder wenn auf eine Schaltfläche geklickt wurde.

In den Diagrammen und Tabellen **[!UICONTROL Fehlerursachen]** und **[!UICONTROL Ausschlussgründe]** sehen Sie, welcher Fehler und welche Ausschlüsse während des Versands aufgetreten sind.

Mit dem Widget **[!UICONTROL Sendestatistiken – Fehlgeschlagen]** können Sie sehen, wie viele Fehler und Bounces aufgetreten sind.

Die Diagramme und Tabellen **[!UICONTROL Tracking nach Plattform]**, **[!UICONTROL Senden nach Plattform]** und **[!UICONTROL Aufschlüsselung nach Plattform]** geben einen Überblick über den Erfolg Ihrer Push-Benachrichtigung, aufgeschlüsselt nach Betriebssystem.
