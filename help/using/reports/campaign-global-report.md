---
solution: Journey Optimizer
product: journey optimizer
title: Globaler Bericht zu Kampagnen
description: Erfahren Sie, wie Sie Daten im globalen Bericht in Campaign verwenden
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: cd2fcd36d0f742a1bbe726217b884ae1bec26d82
workflow-type: ht
source-wordcount: '2313'
ht-degree: 100%

---

# Globaler Bericht zu Kampagnen {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="Globaler Bericht zu Kampagnen"
>abstract="Der globale Bericht einer Kampagne ermöglicht die Messung der Wirkung von Kampagnen über einen ausgewählten Zeitraum. Der Bericht ist in verschiedene Widgets unterteilt, die den Erfolg und die Fehler der Kampagne detailliert darstellen. Jedes Reporting-Dashboard kann durch Ändern der Größe oder Entfernen von Widgets verändert werden."

Globale Berichte, auf die über die Registerkarte „Gesamte Zeit“ zugegriffen werden kann, zeigen Ereignisse an, die vor mindestens zwei Stunden aufgetreten sind, und decken Ereignisse über einen ausgewählten Zeitraum ab. Im Vergleich dazu konzentrieren sich Live-Berichte auf Ereignisse, die innerhalb der letzten 24 Stunden stattgefunden haben. Der Zeitraum ab dem Auftreten des Ereignisses beträgt mindestens zwei Minuten.

Über die Schaltfläche **[!UICONTROL Bericht anzeigen]** ist der direkte Zugriff in einer Campaign-Instanz auf den globalen Bericht in Campaign möglich.

![](assets/campaign_report_global_5.png)

Die Seite **[!UICONTROL Globaler Bericht]** in Campaign wird mit den folgenden Registerkarten angezeigt:

* [Campaign](#campaign-global)
* [E-Mail](#email-global)
* [In-App](#inapp-global)
* [Push-Benachrichtigung](#push-global)
* [SMS](#sms-global)
* [Web](#web-tab)

Der **[!UICONTROL Globale Bericht]** in Campaign ist in verschiedene Widgets unterteilt, die Erfolge und Fehler bei Ihrer Kampagne detailliert beschreiben. Jedes Widget kann bei Bedarf angepasst und gelöscht werden. Weiterführende Informationen dazu finden Sie in diesem [Abschnitt](../reports/global-report.md#modify-dashboard).

Eine detaillierte Liste aller in Adobe Journey Optimizer verfügbaren Metriken finden Sie auf [dieser Seite](global-report.md#list-of-components-global.md)

## Registerkarte „Kampagne“ {#campaign-global}

### Versand {#delivery-global}

![](assets/campaign_report_global_1.png)

Das Widget **[!UICONTROL Kampagnenstatistiken]** enthält die wichtigsten Informationen zu Ihrer Kampagne:

* **[!UICONTROL Eingetretene Profile]**: Anzahl der Profile, die mit der Journey begonnen haben.

* **[!UICONTROL Bereitgestellte Aktionen]**: Gesamtzahl der eindeutigen Fälle, in denen eine Aktion in der Journey ausgeführt wurde.

* **[!UICONTROL Fehlgeschlagene Aktionen in %]**: Gesamtzahl der eindeutigen Fälle, in denen eine Aktion in der Journey fehlgeschlagen ist, verglichen mit der Gesamtzahl der eindeutigen Fälle, in denen eine Aktion erfolgreich ausgeführt wurde.

<!--
### Objectives report {#objectives-global}

![](assets/performance_report.gif)

The **[!UICONTROL Objectives]** tab allows you to better fine-tune your deliveries' reports by targeting one specific metric.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of built-in **[!UICONTROL Objectives]** is available but you can add your own by adding new **[!UICONTROL Dataset]**. For the detailed procedure, refer to this [section](../campaigns/reporting-configuration.md).

After selecting the Objectives you want to target on, the two **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets will provide a detailed summary of your delivery performance. 

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your main objective with another metric.
-->

### Experimentationsbericht {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Erfolgsmetrik"
>abstract="Der Gesamtwert der Erfolgsmetrik, die zuvor beim Erstellen der Experimente ausgewählt wurde, dividiert durch die Anzahl der Profile."

![](assets/experimentation_report_3.png)

Die Registerkarte **[!UICONTROL Experimentieren]** bietet wichtige Einblicke in die Leistung der einzelnen Varianten und ermittelt die erfolgreichste Variante.

Beachten Sie, dass es ein wenig dauern kann, um die beste Leistung zu ermitteln. Sie wird durch das Symbol ![](assets/experimentation_report_1.png) gekennzeichnet.

+++Erfahren Sie mehr über die verschiedenen Kennzahlen und Widgets, die für den Experimentierbericht verfügbar sind.

Die Widget **[!UICONTROL Experimentergebnis]** liefert Details zur Leistung der einzelnen Varianten. Sie können Ihre Grundlinie ändern, indem Sie eine der Behandlungen aus der Dropdown-Liste **[!UICONTROL Grundlinie]** auswählen. Die beste Behandlung wird mit einem Sternsymbol gekennzeichnet.

Die Tabelle enthält die folgenden Metriken:

* **[!UICONTROL Steigerung über die Baseline]**: Messung der prozentualen Verbesserung der Konversionsrate einer bestimmten Abwandlung im Vergleich zur Baseline.

* **[!UICONTROL Konfidenz]**: Belege dafür, dass eine bestimmte Behandlung mit der Grundlinienbehandlung identisch ist. [Weitere Informationen](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Ausgehende Einzelklicks]**: Gesamtanzahl der Klicks in allen ausgehenden Kanälen.

* **[!UICONTROL Profile]**: Anzahl der für diese Behandlung ausgewählten Profile.

* **[!UICONTROL Eindeutige ausgehende Klicks/Profile]**: Gesamtwert der Erfolgskennzahl, die zuvor beim Erstellen der Experimente ausgewählt wurde, dividiert durch die Anzahl der Profile.

Der Graph **[!UICONTROL Konfidenzintervall]** misst die Unsicherheit im Zusammenhang mit Verbesserungen. Er beschreibt den prozentualen Leistungsunterschied zwischen der Baseline und der Abwandlung mit der besten Leistung. [Weitere Informationen](../campaigns/experiment-calculations.md#confidence-intervals).
+++

Einen tiefen Einblick in diese Ergebnisse und ihre Interpretation finden Sie auf [dieser Seite](../campaigns/get-started-experiment.md#interpret-results).

## Registerkarte „E-Mail“ {#email-global}

![](assets/campaign_report_global_2.png)

Im **[!UICONTROL globalen Bericht]** in Campaign finden Sie auf der Registerkarte **[!UICONTROL E-Mail]** die wichtigsten Informationen zu den E-Mail-Sendungen, die in Ihrer Journey gesendet wurden.

+++Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den E-Mail-Bericht verfügbar sind.

Im Diagramm **[!UICONTROL E-Mail-Sendestatistik]** wird der Erfolg Ihres Versands beschrieben:

* **[!UICONTROL Zielgruppe]**: Gesamtzahl der bei der Versandanalyse verarbeiteten Nachrichten.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zustellbarkeitsrate]**: Prozentsatz der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der E-Mails, die nicht erfolgreich zugestellt wurden, im Vergleich zur Zahl der gesendeten E-Mails.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.

* **[!UICONTROL Fehlerrate]**: Prozentsatz der Fehler, die während des Versands auftraten und die Zustellung verhinderten, im Vergleich zur Zahl der gesendeten E-Mails.

* **[!UICONTROL Weitere Zustellversuche]**: Anzahl der E-Mails in der Warteschlange für weitere Zustellversuche.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

Das Widget **[!UICONTROL E-Mail – Tracking-Statistik]** enthält die verfügbaren Daten zur Empfängeraktivität für Ihren Versand:

* **[!UICONTROL Öffnungen]**: Gibt die Zahl der Öffnungen eines Versands an.

* **[!UICONTROL Eindeutige Öffnungen]**: Prozentsatz der geöffneten zugestellten Nachrichten.

* **[!UICONTROL Öffnungsrate]**: Gesamtzahl der geöffneten Nachrichten im Vergleich zu den versendeten E-Mails.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf Inhalt einer E-Mail.

* **[!UICONTROL Einzelklicks]**: Die Anzahl der Empfänger, die auf Inhalt in einer E-Mail geklickt haben.

* **[!UICONTROL Rate von Einzelklicks]**: Prozentsatz der Benutzer, die mit der versendeten Nachricht interagiert haben.

* **[!UICONTROL Abmeldungen]**: Zahl der Klicks auf den Abmelde-Link.

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
+++

## Registerkarte „In-App“ {#inapp-global}

Im **[!UICONTROL globalen Bericht]** Ihrer Kampagne finden Sie auf der Registerkarte **[!UICONTROL In-App]** die wichtigsten Informationen zu den In-App-Sendungen, die in Ihrer Kampagne versendet wurden.

![](assets/campaign_report_global_6.png)

+++Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den In-App-Bericht verfügbar sind.

Die KPIs der **[!UICONTROL In-App-Leistung]** geben die wichtigsten Informationen bezüglich der Interaktion Ihrer Besucher mit Ihren In-App-Nachrichten an, z. B.:

* **[!UICONTROL Eindeutige Impressions]**: Anzahl der eindeutigen Nutzer, an die die In-App-Nachricht gesendet wurde.

* **[!UICONTROL Impressions]**: Gesamtzahl der an alle Benutzer gesendeten In-App-Nachrichten.

* **[!UICONTROL Klickrate]**: Prozentualer Anteil der Benutzer, die mit den in der In-App-Nachricht enthaltenen Schaltflächen interagiert haben, im Verhältnis zur Zahl der Benutzer, die die Nachricht gesehen haben.

* **[!UICONTROL Abweisungsrate]**: Prozentsatz der In-App-Nachrichten, die von Empfängern abgewiesen wurden.

Das Diagramm **[!UICONTROL In-App-Zusammenfassung]** zeigt die Entwicklung Ihrer In-App-Impressions für den betroffenen Zeitraum an.

Das Diagramm und die Tabelle **[!UICONTROL Klicks nach Schaltfläche]** enthalten die verfügbaren Daten für das Empfängerverhalten je nach Schaltfläche:

* **[!UICONTROL Klicks]**: Gesamtzahl der Empfänger, die mit den in der In-App-Nachricht enthaltenen Schaltflächen interagiert haben.

* **[!UICONTROL Klickrate]**: Prozentualer Anteil der Benutzer, die mit den in der In-App-Nachricht enthaltenen Schaltflächen interagiert haben, im Verhältnis zur Zahl der Benutzer, die die Nachricht gesehen haben.
+++

## Registerkarte „Push-Benachrichtigung“ {#push-global}

Im **[!UICONTROL Globalen Bericht]** Ihrer Kampagne finden Sie auf der Registerkarte **[!UICONTROL Push-Benachrichtigung]** die wichtigsten Informationen zu den im Rahmen Ihrer Kampagne gesendeten Push-Nachrichten.

![](assets/campaign_report_global_3.png)

+++Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Push-Bericht verfügbar sind.

Die Tabelle **[!UICONTROL Push-Benachrichtigung – Sendestatistiken]** enthält die wichtigsten Informationen zu Ihren Push-Benachrichtigungen mit Diagrammen und KPIs:

* **[!UICONTROL Zielgruppe]**: Gesamtzahl der bei der Versandanalyse verarbeiteten Nachrichten.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zustellbarkeitsrate]**: Prozentsatz der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der Push-Benachrichtigungen, die unzustellbar waren, im Vergleich zu den gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.

* **[!UICONTROL Fehlerrate]**: Prozentualer Anteil der Fehler, die während eines Versands aufgetreten sind und den Versand verhindert haben, im Vergleich zu den gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

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
* **[!UICONTROL Öffnungen]**: Gibt die Zahl der Öffnungen eines Versands an.
* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, z. B. Klick auf Schaltfläche oder Abbruch.

Die **[!UICONTROL Versandzeitoptimierung]** zeigt den Erfolg Ihres Versands in Abhängigkeit von der Versandmethode an: optimiert oder normal.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.
* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

In der Grafik **[!UICONTROL Fehlergründe]** und der Tabelle unten können Sie sehen, welcher Fehler während des Versands aufgetreten ist.

Das Diagramm und die Tabelle **[!UICONTROL Ausschlussgründe]** zeigen die verschiedenen Gründe an, die verhindert haben, dass Nutzerprofile, die von den Zielprofilen ausgeschlossen wurden, die Nachricht erhalten haben.

Die Diagramme und Tabellen **[!UICONTROL Tracking nach Plattform]**, **[!UICONTROL Senden nach Plattform]** und **[!UICONTROL Aufschlüsselung nach Plattform]** geben einen Überblick über den Erfolg Ihrer Push-Benachrichtigung, aufgeschlüsselt nach dem Betriebssystem Ihres Empfängers.
+++

## Registerkarte „SMS“ {#sms-global}

Im **[!UICONTROL Globalen Bericht]** Ihrer Kampagne finden Sie auf der Registerkarte **[!UICONTROL SMS]** die wichtigsten Informationen zu den in Ihrer Kampagne versendeten SMS.

![](assets/campaign_report_global_4.png)

+++Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den SMS-Bericht verfügbar sind.

Die Tabelle **[!UICONTROL SMS – Sendestatistik]** gibt Auskunft über den Erfolg des Versands:

* **[!UICONTROL Ausgewählt]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für diesen Versand eignen.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.

Das Widget **[!UICONTROL SMS-Leistung nach Datum]** enthält die wichtigsten Informationen zu Ihrer Nachricht in Form eines Diagramms:

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler bei Versand und automatischer Bounce-Verarbeitung in Relation zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.

Mit den Diagrammen und Tabellen **[!UICONTROL Ausschlussursachen]**, **[!UICONTROL Bounce-Ursachen]** und **[!UICONTROL Fehlerursachen]** sehen Sie, welche Fehler und Ausschlüsse bei Ihrem Versand aufgetreten sind.

Die Widgets **[!UICONTROL SMS – Klicks nach Links]** und **[!UICONTROL SMS – Tracking-Statistiken]** enthalten die wichtigsten Informationen zur Interaktion Ihrer Besucherinnen und Besucher mit Ihren URLs.

+++

## Registerkarte „Web“ {#web-tab}

Im **[!UICONTROL globalen Bericht]** Ihrer Kampagne werden in der Registerkarte **[!UICONTROL Web]** die wichtigsten Informationen zu Ihren Web-Seiten aufgeführt.

![](assets/web-report.png)

+++Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Web-Bericht verfügbar sind.

Die KPIs der **[!UICONTROL Web-Performance]** enthalten die wichtigsten Informationen zur Interaktion Ihrer Besucher mit Ihren Web-Erlebnissen, z. B.:

* **[!UICONTROL Eindeutige Impressions]**: Anzahl der eindeutigen Benutzer, denen das Web-Erlebnis bereitgestellt wurde.

* **[!UICONTROL Impressions]**: Gesamtanzahl der für alle Benutzer bereitgestellten Web-Erlebnisse.

* **[!UICONTROL Klickrate]**: Prozentsatz der Besuchenden, die mit den verschiedenen Elementen auf Ihren Web-Seiten interagiert haben.

Das Diagramm **[!UICONTROL Web-Zusammenfassung]** zeigt die Entwicklung Ihrer Web-Erlebnisse (Impressions, eindeutige Impressions und Klicks) für den betroffenen Zeitraum.

Die Tabelle **[!UICONTROL Klicks nach Element]** enthält die wichtigsten Informationen zur Interaktion Ihrer Besucherinnen und Besucher mit den verschiedenen Elementen auf Ihren Web-Seiten.
+++

## Weitere Ressourcen

* [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md)
* [Erstellen einer Kampagne](../campaigns/create-campaign.md)
* [Erstellen von API-ausgelösten Kampagnen](../campaigns/api-triggered-campaigns.md)
* [Ändern oder Stoppen einer Kampagne](../campaigns/modify-stop-campaign.md)
* [Kampagnen-Live-Bericht](campaign-live-report.md)
