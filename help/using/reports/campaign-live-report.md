---
solution: Journey Optimizer
product: journey optimizer
title: Kampagnen-Live-Bericht
description: Erfahren Sie, wie Sie Daten aus dem Live-Bericht in Campaign verwenden
feature: Reporting, Campaigns
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 03c714833930511fa734662b637d2416728073c2
workflow-type: tm+mt
source-wordcount: '2095'
ht-degree: 100%

---

# Kampagnen-Live-Bericht {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="Kampagnen-Live-Bericht"
>abstract="Mit dem Kampagnen-Live-Bericht kann die Wirkung und Performance von Kampagnen nur in den letzten 24 Stunden in Echtzeit gemessen und visualisiert werden. Der Bericht ist in verschiedene Widgets unterteilt, die den Erfolg und die Fehler der Kampagne detailliert darstellen. Jedes Reporting-Dashboard kann durch Ändern der Größe oder Entfernen von Widgets verändert werden."

Live-Berichte, auf die über die Registerkarte „Letzte 24 Std.“ zugegriffen werden kann, zeigen Ereignisse an, die innerhalb der letzten 24 Stunden stattgefunden haben. Der Zeitraum ab dem Auftreten des Ereignisses beträgt mindestens zwei Minuten. Im Vergleich dazu konzentrieren sich globale Berichte auf Ereignisse, die vor mindestens zwei Stunden aufgetreten sind, und decken Ereignisse über einen ausgewählten Zeitraum ab.

Über die Schaltfläche **[!UICONTROL Live-Ansicht]** können Sie direkt in Ihrer Campaign-Instanz auf den Live-Bericht in Campaign zugreifen.

Die Seite **[!UICONTROL Live-Bericht]** in Campaign wird mit den folgenden Registerkarten angezeigt:

* [Campaign](#campaign-live)
* [E-Mail](#email-live)
* [In-App](#inapp-live)
* [Push-Benachrichtigung](#push-live)
* [SMS](#sms-live)
* [Web](#web-tab)
* [Briefpost](#direct-mail-tab)

Der **[!UICONTROL Live-Bericht]** in Campaign ist in verschiedene Widgets unterteilt, die Erfolge und Fehler bei Ihrer Kampagne detailliert beschreiben. Jedes Widget kann bei Bedarf angepasst und gelöscht werden. Weiterführende Informationen dazu finden Sie in diesem [Abschnitt](../reports/live-report.md#modify-dashboard).

Eine detaillierte Liste aller in Adobe Journey Optimizer verfügbaren Metriken finden Sie auf [dieser Seite](live-report.md#list-of-components-live).

## Registerkarte „Kampagne“ {#campaign-live}

### Versand {#delivery-live}

Das Widget **[!UICONTROL Kampagnenstatistiken]** enthält die wichtigsten Informationen zu Ihrer Kampagne:

* **[!UICONTROL Eingetretene Profile]**: Anzahl der Profile, die mit der Journey begonnen haben.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## Registerkarte „E-Mail“ {#email-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_sending_statistics"
>title="E-Mail – Versandstatistiken"
>abstract="Der Graph „E-Mail – Versandstatistik“ fasst wichtige Daten zu Ihren E-Mails, z. B. „Angesprochen“ oder „Zugestellt“, aus den letzten 24 Stunden zusammen."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_statistics"
>title="E-Mail – Statistiken"
>abstract="Die Tabelle „E-Mail – Statistik“ enthält Daten zur Profilaktivität Ihrer E-Mail aus den letzten 24 Stunden."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_categories"
>title="E-Mail – Bounce-Kategorien"
>abstract="Die Graphen und die Tabelle „E-Mail – Bounce-Kategorien“ enthalten sowohl temporäre als auch permanente Fehler aus den letzten 24 Stunden."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_performance_bydate"
>title="E-Mail – Performance nach Datum"
>abstract="Der Graph „E-Mail – Performance nach Datum“ präsentiert umfassende Daten aus den letzten 24 Stunden zu gesendeten E-Mails und bietet Einblicke in wichtige Metriken wie Sendungen und Bounces, sodass eine detaillierte Analyse des E-Mail-Versandprozesses möglich ist."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_reasons"
>title="E-Mail – Bounce-Gründe"
>abstract="Die Graphen und die Tabelle „E-Mail – Bounce-Gründe“ enthalten die verfügbaren Daten, die für Bounce-Nachrichten aus den letzten 24 Stunden verfügbar waren."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_error_reasons"
>title="E-Mail – Fehlerursachen"
>abstract="Anhand der Graphen und der Tabelle „E-Mail – Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs in den letzten 24 Stunden aufgetreten sind."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_excluded_reasons"
>title="E-Mail – Ausgeschlossene Gründe"
>abstract="Die Graphen und die Tabelle „E-Mail – Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu geführt haben, dass Benutzerprofile, die von der Zielgruppe ausgeschlossen waren, die Nachricht in den letzten 24 Stunden nicht erhalten haben."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_best_recipient"
>title="E-Mail – Beste Empfänger-Domain"
>abstract="Der Graph und die Tabelle „E-Mail – Beste Empfänger-Domain“ enthalten eine detaillierte Aufschlüsselung der Domains, die Empfängerinnen und Empfänger am häufigsten zum Öffnen der E-Mail verwenden, und bieten wertvolle Einblicke in das Empfängerverhalten aus den letzten 24 Stunden."

In Ihrem **[!UICONTROL Live-Bericht]** in Campaign finden Sie auf der Registerkarte **[!UICONTROL E-Mail]** die wichtigsten Informationen zu den E-Mails, die in Ihrer Kampagne gesendet wurden.

![](assets/campaign_report_live_1.png)

+++Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den E-Mail-Bericht verfügbar sind.

Das Widget **[!UICONTROL E-Mail-Versandstatistik]** enthält die wichtigsten Informationen zu Ihrer Nachricht:

* **[!UICONTROL Zugestellt]**: Die Anzahl der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

Die Tabelle **[!UICONTROL Versandmetriken nach E-Mail]** und der Graph **[!UICONTROL E-Mail-Zusammenfassung]** zeigen, wie erfolgreich Ihr Versand war:

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge.

* **[!UICONTROL Zugestellt]**: Die Anzahl der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler während des Versandvorgangs und der automatischen Rücksendungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft eine Nachricht geöffnet wurde.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt.

* **[!UICONTROL Abo beenden]**: Zahl der Klicks auf den Abmelde-Link.

* **[!UICONTROL Beschwerden wegen Spam]**: Gibt an, wie oft eine Nachricht als Spam oder Junk gekennzeichnet wurde.

Die Widgets **[!UICONTROL Bounce-Gründe]** und **[!UICONTROL Bounce-Kategorien]** enthalten die verfügbaren Daten zu unzustellbaren Nachrichten wie:

* **[!UICONTROL Hardbounce]**: die Gesamtzahl der permanenten Fehler, wie eine falsche E-Mail-Adresse. Dazu gehören Fehlermeldungen, die explizit eine ungültige Adresse anzeigen, wie etwa „Benutzer unbekannt“.

* **[!UICONTROL Softbounce]**: die Gesamtzahl der temporären Fehler, wie ein voller Posteingang.

* **[!UICONTROL Ignoriert]**: Die Gesamtzahl der temporären Ereignisse, beispielsweise Abwesenheit, oder technischer Fehler, zum Beispiel wenn der Absendertyp Postmaster ist.

In den Graphen und Tabellen **[!UICONTROL Fehlerursachen]** und **[!UICONTROL Ausschlussursachen]** sehen Sie, welche Fehler und Ausschlüsse während des Versandvorgangs aufgetreten sind.

Der Graph und die Tabelle **[!UICONTROL E-Mail – beste Empfänger-Domain]** zeigen, welche Domains von Empfängerinnen und Empfängern am häufigsten zum Öffnen der E-Mail verwendet werden.
+++

## Registerkarte „In-App“ {#inapp-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_performance"
>title="In-App-Performance"
>abstract="Die KPIs zur In-App-Performance bieten wichtige Einblicke in die Interaktion Ihrer Besucherinnen und Besucher mit In-App-Nachrichten in den letzten 24 Stunden."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_interactions"
>title="Interaktionen nach Typ"
>abstract="Die Graphen und die Tabelle „Interaktionen nach Typ“ beschreiben, wie Benutzende mit Ihrer In-App-Nachricht interagiert haben, indem Klicks, Abbrechen oder Interaktionen verfolgt werden."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_summary"
>title="In-App-Zusammenfassung"
>abstract="Der In-App-Übersichtsgraph zeigt den Verlauf Ihrer In-App-Impressions und -Interaktionen in den letzten 24 Stunden."

Im **[!UICONTROL Live-Bericht]** Ihrer Kampagne finden Sie auf der Registerkarte **[!UICONTROL In-App]** die wichtigsten Informationen zu den In-App-Nachrichten, die in Ihrer Kampagne versendet wurden.

+++Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den In-App-Bericht verfügbar sind.

Die KPIs der **[!UICONTROL In-App-Performance]** geben die wichtigsten Informationen bezüglich der Interaktion Ihrer Besucherinnen und Besucher mit Ihren In-App-Nachrichten an, z. B.:

* **[!UICONTROL Impressions]**: Gesamtzahl der an alle Benutzenden gesendeten In-App-Nachrichten.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit Ihrer In-App-Nachricht. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks, Abbrechen oder andere Interaktionen.

Das Diagramm **[!UICONTROL In-App-Zusammenfassung]** zeigt die Entwicklung Ihrer In-App-Impressions und Interaktionen für den jeweiligen Zeitraum an.

Das Diagramm und die Tabelle **[!UICONTROL Interaktionen nach Typ]** beschrieben, wie Benutzende mit Ihrer In-App-Nachricht interagiert haben, indem Klicks, Abbrechen oder Interaktionen verfolgt werden.

+++

## Registerkarte „Push-Benachrichtigung“ {#push-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_performance"
>title="Push-Benachrichtigung – Versand-Performance"
>abstract="Der Graph „Push-Benachrichtigung – Versand-Performance“ fasst wichtige Daten zu Ihrer Push-Benachrichtigung zusammen, z. B. „Fehler“ oder „Zugestellte Nachrichten“ aus den letzten 24 Stunden."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_statistics"
>title="Push-Benachrichtigung – Statistiken"
>abstract="Die Tabelle „Push-Benachrichtigung – Statistik“ enthält Daten zur Empfängeraktivität der letzten 24 Stunden für Ihre Push-Benachrichtigung."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_summary"
>title="Push-Benachrichtigung – Sendezusammenfassung"
>abstract="Der Graph „Push-Benachrichtigung – Sendezusammenfassung“ zeigt die Daten an, die für gesendete Push-Benachrichtigungen aus den letzten 24 Stunden verfügbar sind."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_excluded_reasons"
>title="Push-Benachrichtigung – Ausschlussursachen"
>abstract="Die Graphen und die Tabelle „E-Mail – Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu geführt haben, dass Benutzerprofile, die von der Zielgruppe ausgeschlossen waren, die Nachricht in den letzten 24 Stunden nicht erhalten haben."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_error_reasons"
>title="Push-Benachrichtigung – Fehlerursachen"
>abstract="Anhand der Graphen und der Tabelle „Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die in den letzten 24 Stunden des Versandvorgangs aufgetreten sind."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_breakdown_platform"
>title="Push-Benachrichtigung – Aufschlüsselung nach Plattform"
>abstract="Die Graphen und die Tabelle „Aufschlüsselung nach Plattform“ enthalten eine Aufschlüsselung des Erfolgs Ihrer Push-Benachrichtigungen in den letzten 24 Stunden basierend auf dem Betriebssystem der Empfängerin bzw. des Empfängers."

In Ihrem **[!UICONTROL Live-Bericht]** in Campaign finden Sie auf der Registerkarte **[!UICONTROL Push-Benachrichtigung]** die wichtigsten Informationen zu den Push-Benachrichtigungen, die in Ihrer Kampagne gesendet wurden.

![](assets/campaign_report_live_2.png)

+++Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Push-Bericht verfügbar sind.

Die Widgets **[!UICONTROL Push-Benachrichtigung – Versand-Performance]**, **[!UICONTROL Push-Benachrichtigung – Zusammenfassung]** und **[!UICONTROL Push-Benachrichtigung – Statistiken]** zeigen Details zu den wichtigsten Informationen in Bezug auf Ihre Nachricht:

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge.

* **[!UICONTROL Zugestellt]**: Die Anzahl der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft eine Nachricht geöffnet wurde.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf Schaltfläche oder Abbruch.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Öffnungen und Aktionen für diese Push-Benachrichtigung, d. h. wenn das Profil die Push-Benachrichtigung geöffnet hat oder wenn auf eine Schaltfläche geklickt wurde.

In den Graphen und Tabellen **[!UICONTROL Fehlerursachen]** und **[!UICONTROL Ausschlussgründe]** sehen Sie, welche Fehler und Ausschlüsse während des Versandvorgangs aufgetreten sind.

Mit dem Widget **[!UICONTROL Sendestatistiken – Fehlgeschlagen]** können Sie sehen, wie viele Fehler und Bounces aufgetreten sind.

Die Diagramme und Tabellen **[!UICONTROL Tracking nach Plattform]**, **[!UICONTROL Senden nach Plattform]** und **[!UICONTROL Aufschlüsselung nach Plattform]** geben einen Überblick über den Erfolg Ihrer Push-Benachrichtigung, aufgeschlüsselt nach Betriebssystem.
+++

## Registerkarte „SMS“ {#sms-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_statistics"
>title="SMS – Statistiken"
>abstract="Die Tabelle „SMS – Versandstatistik“ enthält eine Zusammenfassung der wichtigsten Daten zu Ihren SMS-Nachrichten, wie z. B. „Angesprochen“ oder „Zugestellte Nachrichten aus den letzten 24 Stunden“."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_performance"
>title="SMS – Performance nach Datum"
>abstract="Das Widget „SMS – Performance nach Datum“ liefert wichtige Informationen aus den letzten 24 Stunden über Ihre Nachrichten in einer grafischen Darstellung."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_error_reasons"
>title="SMS – Fehlerursachen"
>abstract="Die Graphen und die Tabelle „SMS – Fehlerursachen“ ermöglichen es Ihnen, die spezifischen Fehler zu identifizieren, die in den letzten 24 Stunden während des Versandvorgangs aufgetreten sind."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_excluded_reasons"
>title="SMS – Ausschlussursachen"
>abstract="Die Graphen und die Tabelle „E-Mail – Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu geführt haben, dass Benutzerprofile, die von der Zielgruppe ausgeschlossen waren, die Nachricht in den letzten 24 Stunden nicht erhalten haben."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_bounces_reasons"
>title="SMS – Bounce-Ursachen"
>abstract="Die Graphen und die Tabelle „Bounce-Ursachen“ enthalten die Daten aus den letzten 24 Stunden bezüglich Bounce-Nachrichten."

In Ihrem **[!UICONTROL Live-Bericht]** in Campaign finden Sie auf der Registerkarte **[!UICONTROL SMS]** die wichtigsten Informationen zu den SMS-Nachrichten, die in Ihrer Kampagne gesendet wurden.

![](assets/campaign_report_live_3.png)

+++Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den SMS-Bericht verfügbar sind.

Die Tabelle **[!UICONTROL SMS – Statistik]** gibt Auskunft über den Erfolg Ihrer SMS-Nachricht:

* **[!UICONTROL Angesprochen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für diesen Versand eignen.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

* **[!UICONTROL Klicks]**: Gesamtzahl der URL-Besuche.

Das Widget **[!UICONTROL SMS-Performance nach Datum]** enthält die wichtigsten Informationen zu Ihrer Nachricht in Form eines Graphen:

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

In den Graphen und Tabellen **[!UICONTROL Ausschlussgründe]**, **[!UICONTROL Bounce-Gründe]** und **[!UICONTROL Fehlerursachen]** sehen Sie, welche Fehler und Ausschlüsse während des Versandvorgangs aufgetreten sind.
+++

## Registerkarte „Web“ {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_performance"
>title="Web-Performance"
>abstract="Die Web-Performance-KPIs bieten umfassende Informationen über die Interaktion Ihrer Besucherinnen und Besucher mit Ihren Web-Erlebnissen aus den letzten 24 Stunden."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_summary"
>title="Web-Zusammenfassung"
>abstract="Das Diagramm „Web-Zusammenfassung“ zeigt die Entwicklung Ihrer Web-Erlebnisse (Impressions, eindeutige Impressions und Interaktionen) für die letzten 24 Stunden."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_interactions"
>title="Interaktionen nach Element"
>abstract="Die Tabelle „Interaktionen nach Element“ enthält wichtige Informationen zur Interaktion Ihrer Besucherinnen und Besucher mit verschiedenen Elementen auf Ihren Web-Seiten in den letzten 24 Stunden."

Im **[!UICONTROL Live-Bericht]** Ihrer Kampagne werden auf der Registerkarte **[!UICONTROL Web]** die wichtigsten Informationen zu Ihren Web-Seiten aufgeführt.

+++Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Web-Bericht verfügbar sind.

Die KPIs der **[!UICONTROL Web-Performance]** geben die wichtigsten Informationen bezüglich der Interaktion Ihrer Besucherinnen und Besucher mit Ihren Web-Erlebnissen an, z. B.:

* **[!UICONTROL Impressions]**: Gesamtanzahl der für alle Benutzerinnen und Benutzer bereitgestellten Web-Erlebnisse.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit Ihrer Web-Seite. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks oder andere Interaktionen.

Das Diagramm **[!UICONTROL Web-Zusammenfassung]** zeigt die Entwicklung Ihrer Web-Erlebnisse (Impressions, eindeutige Impressions und Interaktionen) für die letzten 24 Stunden.

Die Tabelle **[!UICONTROL Interaktionen nach Element]** enthält die wichtigsten Informationen zur Interaktion Ihrer Besucherinnen und Besucher mit den verschiedenen Elementen auf Ihren Web-Seiten.
+++

## Registerkarte „Briefpost“ {#direct-mail-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_sending_statistics"
>title="Briefpost – Versandstatistik"
>abstract="Die Tabelle „Briefpost – Versandstatistik“ enthält eine Zusammenfassung der wichtigsten Daten aus den letzten 24 Stunden zu Ihren Briefpost-Nachrichten, z. B. „Angesprochen“ oder „Zugestellte Nachrichten“."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_error_reasons"
>title="Briefpost – Fehlerursachen"
>abstract="Die Graphen und die Tabelle „Briefpost – Fehlerursachen“ ermöglichen es Ihnen, die spezifischen Fehler zu identifizieren, die in den letzten 24 Stunden aufgetreten sind."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_excluded_reasons"
>title="Briefpost – Ausschlussgründe"
>abstract="Die Graphen und die Tabelle „Briefpost – Ausschlussgründe“ veranschaulichen die verschiedenen Faktoren, die dazu geführt haben, dass Benutzerprofile, die von der Zielgruppe ausgeschlossen waren, die Nachricht in den letzten 24 Stunden nicht erhalten haben."

Im **[!UICONTROL Live-Bericht]** in Campaign werden auf der Registerkarte **[!UICONTROL Briefpost]** die wichtigsten Informationen zu Ihrer Briefpost aufgeführt.

![](assets/direct-mail-report_2.png)

+++Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Briefpost-Bericht verfügbar sind.

Die Tabelle **[!UICONTROL Briefpost – Versandstatistiken]** gibt Auskunft über den Erfolg Ihrer Briefpost:

* **[!UICONTROL Angesprochen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für diesen Versand eignen.

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielprofilen ausgeschlossen waren und Ihre Briefpost nicht erhalten haben.

In den Graphen und Tabellen **[!UICONTROL Briefpost – Ausschlussgründe]** und **[!UICONTROL Briefpost – Fehlerursachen]** sehen Sie, welche Fehler und Ausschlüsse während des Versandvorgangs aufgetreten sind.
+++

## Weitere Ressourcen

* [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md)
* [Erstellen einer Kampagne](../campaigns/create-campaign.md)
* [Erstellen von API-ausgelösten Kampagnen](../campaigns/api-triggered-campaigns.md)
* [Ändern oder Stoppen einer Kampagne](../campaigns/modify-stop-campaign.md)
* [Globaler Bericht zu Kampagnen](campaign-global-report.md)
