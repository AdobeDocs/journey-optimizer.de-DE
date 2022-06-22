---
title: Globaler Kampagnenbericht
description: Erfahren Sie, wie Sie Daten aus dem globalen Kampagnenbericht verwenden.
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: cc20ecf0a019cecb8a4ae9420c5dbdcb28443c91
workflow-type: tm+mt
source-wordcount: '1390'
ht-degree: 82%

---

# Globaler Kampagnenbericht {#campaign-global-report}

Der globale Kampagnenbericht kann direkt über Ihre Kampagne mit dem **[!UICONTROL Globale Ansicht]** Schaltfläche.

Die Kampagne **[!UICONTROL Gesamtbericht]** wird mit den folgenden Registerkarten angezeigt:

* [Campaign](#campaign-global)
* [E-Mail](#email-global)
* [Push-Benachrichtigung](#push-global)

Die Kampagne **[!UICONTROL Gesamtbericht]** ist in verschiedene Widgets unterteilt, die den Erfolg und die Fehler Ihrer Kampagne detailliert beschreiben. Jedes Widget kann bei Bedarf angepasst und gelöscht werden. Weiterführende Informationen dazu finden Sie in diesem [Abschnitt](../reports/global-report.md#modify-dashboard).

## Tab Kampagne {#campaign-global}

### Bereitstellung {#delivery-global}

![](assets/campaign_report_global_1.png)

Die **[!UICONTROL Kampagnenstatistiken]** -Widget beschreibt die wichtigsten Informationen zu Ihrer Kampagne:

* **[!UICONTROL Eingegebene Profile]**: Anzahl der Profile, die die Journey gestartet haben.

* **[!UICONTROL Ausgeführte Aktionen]**: Gesamtzahl der einmaligen Bereitstellungen einer Aktion auf der Journey.

* **[!UICONTROL Fehlgeschlagene Aktionen in %]**: Gesamtzahl der eindeutigen Male, wenn eine Aktion auf der Journey fehlgeschlagen ist, in Bezug auf die Gesamtzahl der einmaligen Bereitstellungen einer Aktion.

<!--
### Experimentation tab (#experimentation-global)

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## Registerkarte „E-Mail“  {#email-global}

In Ihrer Kampagne **[!UICONTROL Gesamtbericht]**, die **[!UICONTROL Email]** im Tab werden die wichtigsten Informationen bezüglich der in Ihrer Kampagne gesendeten E-Mail-Sendungen aufgeführt.

Einen ausführlichen Bericht zu einem bestimmten E-Mail-Versand finden Sie im Abschnitt [Globaler E-Mail-Bericht](../reports/email-global-report.md).

Im Diagramm **[!UICONTROL E-Mail-Sendestatistik]** wird der Erfolg Ihres Versands beschrieben:

* **[!UICONTROL Targeting]**: Gesamtzahl der bei der Versandanalyse verarbeiteten Nachrichten.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zustellbarkeitsrate]**: Prozentsatz der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der E-Mails, die nicht erfolgreich zugestellt wurden, im Vergleich zur Zahl der gesendeten E-Mails.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.

* **[!UICONTROL Fehlerrate]**: Prozentsatz der Fehler, die während des Versands auftraten und die Zustellung verhinderten, im Vergleich zur Zahl der gesendeten E-Mails.

* **[!UICONTROL Weitere Zustellversuche]**: Anzahl der E-Mails in der Warteschlange für weitere Zustellversuche.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die von Adobe Journey Optimizer ausgeschlossen wurden.

Die **[!UICONTROL E-Mail-Tracking-Statistiken]** enthalten die verfügbaren Daten für die Aktivität der Empfänger für Ihren Versand:

* **[!UICONTROL Öffnungen]**: Gibt die Zahl der Öffnungen eines Versands an.

* **[!UICONTROL Eindeutige Öffnungen]**: Prozentsatz der geöffneten zugestellten Nachrichten.

* **[!UICONTROL Öffnungsrate]**: Gesamtzahl der geöffneten Nachrichten im Vergleich zu den versendeten E-Mails.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf Inhalt einer E-Mail.

* **[!UICONTROL Einzelklicks]**: Die Anzahl der Empfänger, die auf Inhalt in einer E-Mail geklickt haben.

* **[!UICONTROL Eindeutige Klickrate]**: Prozentsatz der Benutzer, die mit dem Versand interagiert haben

* **[!UICONTROL Kündigungen von Abos]**: Zahl der Klicks auf den Abmelde-Link.

* **[!UICONTROL Beschwerden wegen Spam]**: Gibt an, wie oft eine Nachricht als Spam oder Junk gekennzeichnet wurde.

Das Diagramm **[!UICONTROL Sendestatistiken]** enthält die Daten, die für gesendete E-Mails verfügbar sind, z. B.:

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Weitere Zustellversuche]**: Anzahl der E-Mails in der Warteschlange für weitere Zustellversuche.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.

Die Widgets **[!UICONTROL Bounce-Gründe]** und **[!UICONTROL Bounce-Kategorien]** enthalten die verfügbaren Daten zu unzustellbaren Nachrichten wie:

* **[!UICONTROL Hardbounce]**: die Gesamtzahl der permanenten Fehler, wie eine falsche E-Mail-Adresse. Dazu gehören Fehlermeldungen, die explizit eine ungültige Adresse anzeigen, wie etwa „Benutzer unbekannt“.

* **[!UICONTROL Softbounce]**: die Gesamtzahl der temporären Fehler, wie ein voller Posteingang.

* **[!UICONTROL Ignoriert]**: Die Gesamtzahl der temporären Ereignisse, beispielsweise Abwesenheit, oder technischer Fehler, zum Beispiel wenn der Absendertyp Postmaster ist.

Weitere Informationen zu Bounces finden Sie auf der Seite [ Unterdrückungslisten](../reports/suppression-list.md).

In der Grafik **[!UICONTROL Fehlergründe]** und der Tabelle unten können Sie sehen, welcher Fehler während des Versands aufgetreten ist.

Das Diagramm und die Tabelle **[!UICONTROL Ausschlussgründe]** zeigen die verschiedenen Gründe an, die verhindert haben, dass Nutzerprofile, die von den Zielprofilen ausgeschlossen wurden, die Nachricht erhalten haben.

Das Diagramm **[!UICONTROL E-Mail – Top-URL]** und die Tabelle zeigen, welche URLs Ihres Versands am häufigsten besucht werden.

Das Diagramm **[!UICONTROL E-Mail – beste Empfänger-Domain]** und die Tabelle zeigen, welche Domains von Empfängern am häufigsten zum Öffnen der E-Mail verwendet werden.

>[!NOTE]
>
>Die Widgets **[!UICONTROL Optimiert vs. nicht optimiert]** und **[!UICONTROL Versandzeitoptimierung]** sind nur verfügbar, wenn die Option „Sendezeitoptimierung“ für Ihren Versand aktiviert ist. Weitere Informationen zur Sendezeitoptimierung finden Sie auf [dieser Seite](../building-journeys/journeys-message.md#send-time-optimization).

Das Diagramm **[!UICONTROL Optimiert vs. nicht optimiert]** zeigt die wichtigsten Informationen bezüglich Ihrer Nachricht an, egal ob sie optimiert wurden oder nicht:

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge für den Versand.
* **[!UICONTROL Öffnungen]**: Gibt an, wie oft die Sendung in einem Versand geöffnet wurde.
* **[!UICONTROL Klicks]**: Gibt an, wie oft ein Inhalt in einer E-Mail angeklickt wurde.

Die **[!UICONTROL Versandzeitoptimierung]** zeigt den Erfolg Ihres Versands in Abhängigkeit von der Versandmethode an: optimiert oder normal.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.
* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

## Registerkarte „Push-Benachrichtigung“  {#push-global}

In Ihrer Kampagne **[!UICONTROL Gesamtbericht]**, die **[!UICONTROL Push]** im Tab werden die wichtigsten Informationen bezüglich der in Ihrer Kampagne gesendeten Push-Nachrichten aufgeführt.

Einen ausführlichen Bericht zu einem bestimmten Push-Versand finden Sie im [globalen Bericht zu Push-Benachritigungen](../reports/push-global-report.md).

Die Tabelle **[!UICONTROL Push-Benachrichtigung – Sendestatistiken]** enthält die wichtigsten Informationen zu Ihren Push-Benachrichtigungen mit Diagrammen und KPIs:

* **[!UICONTROL Targeting]**: Gesamtzahl der bei der Versandanalyse verarbeiteten Nachrichten.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zustellbarkeitsrate]**: Prozentsatz der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der Push-Benachrichtigungen, die unzustellbar waren, im Vergleich zu den gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.

* **[!UICONTROL Fehlerrate]**: Prozentualer Anteil der Fehler, die während eines Versands aufgetreten sind und den Versand verhindert haben, im Vergleich zu den gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die von Adobe Journey Optimizer ausgeschlossen wurden.

Die **[!UICONTROL Push-Benachrichtigung – Tracking-Statistik]** enthält die verfügbaren Daten zur Aktivität der Empfänger für Ihren Versand:

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen einer Nachricht in einem Versand.

* **[!UICONTROL Öffnungsrate]**: Prozentsatz der geöffneten Push-Benachrichtigungen.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf Schaltfläche oder Abbruch.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Öffnungen und Aktionen für diese Push-Benachrichtigung, d. h. wenn das Profil die Push-Benachrichtigung geöffnet hat oder wenn auf eine Schaltfläche geklickt wurde.

* **[!UICONTROL Interaktionsrate]**: Prozentsatz der Öffnungen und Aktionen für diese Push-Benachrichtigung, d. h. wenn das Profil die Push-Benachrichtigung geöffnet hat oder auf eine Schaltfläche geklickt wurde.

Das Diagramm **[!UICONTROL Zusammenfassung der Push-Benachrichtigung]** enthält die Daten, die für gesendete Push-Benachrichtigungen verfügbar sind, z. B.:

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen einer Nachricht in einem Versand.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf Schaltfläche oder Abbruch.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.

>[!NOTE]
>
>Die Widgets **[!UICONTROL Optimiert vs. nicht optimiert]** und **[!UICONTROL Versandzeitoptimierung]** sind nur verfügbar, wenn die Option „Sendezeitoptimierung“ für Ihren Versand aktiviert ist. Weitere Informationen zur Sendezeitoptimierung finden Sie auf [dieser Seite](../building-journeys/journeys-message.md#send-time-optimization).

Das Diagramm **[!UICONTROL Optimiert vs. nicht optimiert]** zeigt die wichtigsten Informationen bezüglich Ihrer Nachricht an, egal ob sie optimiert wurden oder nicht:

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.
* **[!UICONTROL Öffnungen]**: Gibt an, wie oft die Sendung in einem Versand geöffnet wurde.
* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, z. B. Klick auf Schaltfläche oder Abbruch.

Die **[!UICONTROL Versandzeitoptimierung]** zeigt den Erfolg Ihres Versands in Abhängigkeit von der Versandmethode an: optimiert oder normal.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.
* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

In der Grafik **[!UICONTROL Fehlergründe]** und der Tabelle unten können Sie sehen, welcher Fehler während des Versands aufgetreten ist.

Das Diagramm und die Tabelle **[!UICONTROL Ausschlussgründe]** zeigen die verschiedenen Gründe an, die verhindert haben, dass Nutzerprofile, die von den Zielprofilen ausgeschlossen wurden, die Nachricht erhalten haben.

Die Diagramme und Tabellen **[!UICONTROL Tracking nach Plattform]**, **[!UICONTROL Senden nach Plattform]** und **[!UICONTROL Aufschlüsselung nach Plattform]** geben einen Überblick über den Erfolg Ihrer Push-Benachrichtigung, aufgeschlüsselt nach dem Betriebssystem Ihres Empfängers.
