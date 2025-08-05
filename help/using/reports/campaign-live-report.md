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
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '3521'
ht-degree: 99%

---

# Kampagnen-Live-Bericht {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="Kampagnen-Live-Bericht"
>abstract="Mit dem Kampagnen-Live-Bericht kann die Wirkung und Performance von Kampagnen nur in den letzten 24 Stunden in Echtzeit gemessen und visualisiert werden. Der Bericht ist in verschiedene Widgets unterteilt, die den Erfolg und die Fehler der Kampagne detailliert darstellen. Jedes Reporting-Dashboard kann durch Ändern der Größe oder Entfernen von Widgets verändert werden."

Live-Berichte, auf die über die Registerkarte „Letzte 24 Std.“ zugegriffen werden kann, zeigen Ereignisse an, die innerhalb der letzten 24 Stunden stattgefunden haben. Der Zeitraum ab dem Auftreten des Ereignisses beträgt mindestens zwei Minuten. Im Vergleich dazu konzentrieren sich Berichte in Customer Journey Analytics auf Ereignisse, die vor mindestens zwei Stunden aufgetreten sind, und decken Ereignisse über einen ausgewählten Zeitraum ab.

Sie können direkt über Ihre Kampagne auf den Live-Kampagnenbericht zugreifen, indem Sie auf die Schaltfläche **[!UICONTROL Berichte]** klicken und dann **[!UICONTROL Bericht für letzte 24 Stunden anzeigen]** auswählen. 

Die Seite **[!UICONTROL Live-Bericht]** in Campaign wird mit den folgenden Registerkarten angezeigt:

* [Campaign](#campaign-live)
* [E-Mail](#email-live)
* [In-App](#inapp-live)
* [Push-Benachrichtigung](#push-live)
* [SMS](#sms-live)
* [Web](#web-tab)
* [Direkt-Mail](#direct-mail-tab)

>[!AVAILABILITY]
>Orchestrierte Kampagnen unterstützen nur die Kanäle SMS, E-Mail und Push. Andere Kanäle (In-App, Web, Briefpost usw.) sind in orchestrierten Kampagnen nicht verfügbar und werden nicht in Berichten angezeigt.

Der **[!UICONTROL Live-Bericht]** in Campaign ist in verschiedene Widgets unterteilt, die Erfolge und Fehler bei Ihrer Kampagne detailliert beschreiben. Jedes Widget kann bei Bedarf angepasst und gelöscht werden. Weiterführende Informationen dazu finden Sie in diesem [Abschnitt](../reports/live-report.md#modify-dashboard).

Eine detaillierte Liste aller in Adobe Journey Optimizer verfügbaren Metriken finden Sie auf [dieser Seite](live-report.md#list-of-components-live).

## Registerkarte „Kampagne“ {#campaign-live}

### Versand {#delivery-live}

![](assets/campaign_live_statistics.png)

Die KPIs **[!UICONTROL Kampagnenstatistiken]** dienen als umfassendes Dashboard, das eine detaillierte Aufschlüsselung wichtiger Metriken aus den letzten 24 Stunden im Zusammenhang mit Ihrer Kampagne bietet. Dazu gehören wichtige Informationen wie die Anzahl der Profile und die durchgeführten Aktionen, die einen umfassenden Einblick in die Leistung und das Engagement Ihrer Kampagne ermöglichen.

+++ Weitere Informationen zu den Metriken „Kampagnenstatistik“

* **[!UICONTROL Zielgruppe]**: Anzahl der Zielgruppenprofile.

* **[!UICONTROL Durchgeführte Aktionen]**: Gesamtzahl der eindeutigen Zeiten, zu denen eine Aktion durchgeführt wurde.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Sendevorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

+++

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## Registerkarte „E-Mail“ {#email-live}

In Ihrem **[!UICONTROL Live-Bericht]** in Campaign finden Sie auf der Registerkarte **[!UICONTROL E-Mail]** die wichtigsten Informationen zu den E-Mails, die in Ihrer Kampagne gesendet wurden.

### E-Mail – Versandleistung {#email-sending-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_sending_statistics"
>title="E-Mail – Versandstatistiken"
>abstract="Der Graph „E-Mail – Versandstatistiken“ fasst wichtige Daten zu Ihren E-Mails, z. B. „Angesprochen“ oder „Zugestellt“, aus den letzten 24 Stunden zusammen."

![](assets/campaign_email_live_sending.png)

**[!UICONTROL E-Mail – Versandleistung]** bietet einen umfassenden Überblick über die Daten zu E-Mails, die innerhalb der letzten 24 Stunden gesendet wurden. Sie erhalten Einblicke in wichtige Metriken wie „Zugestellt“ und „Bounces“, sodass eine detaillierte Prüfung des E-Mail-Sendevorgangs möglich ist.

+++ Weitere Informationen zu den Metriken „E-Mail – Versandleistung“

* **[!UICONTROL Zugestellt]**: Die Anzahl der erfolgreich gesendeten E-Mails.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen.

* **[!UICONTROL Weitere Zustellversuche]**: Anzahl der E-Mails in der Warteschlange für weitere Zustellversuche.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.
+++

### E-Mail – Statistiken

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_statistics"
>title="E-Mail – Statistiken"
>abstract="Die Tabelle „E-Mail – Statistik“ enthält Daten zur Profilaktivität Ihrer E-Mail aus den letzten 24 Stunden."

![](assets/campaign_email_live_statistics.png)

Die Tabelle **[!UICONTROL Versandmetriken nach E-Mail]** bietet eine umfassende Zusammenfassung der Daten aus den letzten 24 Stunden. Sie enthält wichtige Metriken, einschließlich der Größe der Zielgruppe und der Anzahl der erfolgreich zugestellten E-Mails. Dadurch erhalten Sie wertvolle Einblicke in die Effektivität und Reichweite Ihrer E-Mail-Kampagnen.

+++ Weitere Informationen zu den Metriken „E-Mail – Statistiken“

* **[!UICONTROL Ausführungszeit]**: Startzeit jeder Ausführung Ihrer wiederkehrenden E-Mail. Um nur eine oder mehrere wiederkehrende E-Mails als Ziel auszuwählen, wählen Sie diese aus der Dropdown-Liste **[!UICONTROL Ausführungszeit]**.

* **[!UICONTROL Zielgruppe]**: Gesamtzahl der beim Sendevorgang verarbeiteten Nachrichten.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge.

* **[!UICONTROL Zugestellt]**: Die Anzahl der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft eine Nachricht geöffnet wurde.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt.

* **[!UICONTROL Abo beenden]**: Zahl der Klicks auf den Abmelde-Link.

* **[!UICONTROL Beschwerden wegen Spam]**: Gibt an, wie oft eine Nachricht als Spam oder Junk gekennzeichnet wurde.

* **[!UICONTROL Weitere Zustellversuche]**: Anzahl der E-Mails in der Warteschlange für weitere Zustellversuche.
+++

### E-Mail – Bounce-Kategorien und -Gründe {#bounce-categories}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_categories"
>title="E-Mail – Bounce-Kategorien"
>abstract="Die Graphen und die Tabelle „E-Mail – Bounce-Kategorien“ enthalten sowohl temporäre als auch permanente Fehler aus den letzten 24 Stunden."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_reasons"
>title="E-Mail – Bounce-Gründe"
>abstract="Die Graphen und die Tabelle „E-Mail – Bounce-Gründe“ enthalten die verfügbaren Daten, die für Bounce-Nachrichten aus den letzten 24 Stunden verfügbar waren."

![](assets/campaign_live_email_bounce_categories.png)

Die Widgets **[!UICONTROL Bounce-Gründe]** und **[!UICONTROL Bounce-Kategorien]** stellen die verfügbaren Daten der letzten 24 Stunden in Bezug auf Bounce-Nachrichten zusammen und bieten detaillierte Einblicke in die spezifischen Gründe und Kategorien für E-Mail-Bounces.

Weitere Informationen zu Bounces finden Sie auf der Seite [Unterdrückungslisten](../reports/suppression-list.md).

+++ Weitere Informationen zu den Metriken „E-Mail – Bounce-Kategorien“ und „E-Mail – Bounce-Gründe“

* **[!UICONTROL Hardbounce]**: die Gesamtzahl der permanenten Fehler, wie eine falsche E-Mail-Adresse. Dazu gehören Fehlermeldungen, die explizit eine ungültige Adresse anzeigen, wie etwa „Benutzer unbekannt“.

* **[!UICONTROL Softbounce]**: die Gesamtzahl der temporären Fehler, wie ein voller Posteingang.

* **[!UICONTROL Ignoriert]**: Die Gesamtzahl der temporären Ereignisse, beispielsweise Abwesenheit, oder technischer Fehler, zum Beispiel wenn der Absendertyp Postmaster ist.

+++

### E-Mail – Leistung nach Datum {#email-performance-date}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_performance_bydate"
>title="E-Mail – Leistung nach Datum"
>abstract="Der Graph „E-Mail – Leistung nach Datum“ präsentiert umfassende Daten aus den letzten 24 Stunden zu gesendeten E-Mails und bietet Einblicke in wichtige Metriken wie Sendungen und Bounces, sodass eine detaillierte Analyse des E-Mail-Sendevorgangs möglich ist."

![](assets/campaign_email_live_performance.png)

Das Widget **[!UICONTROL Email – Leistung nach Datum]** bietet einen detaillierten Überblick über die wichtigsten Informationen zu Ihren Nachrichten, die in einem Diagramm dargestellt werden und einen Einblick in die Leistungs-Trends über die letzten 24 Stunden geben.

+++ Weitere Informationen zu den Metriken „E-Mail – Leistung nach Datum und Gründen“

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge.

* **[!UICONTROL Zugestellt]**: Die Anzahl der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft eine Nachricht geöffnet wurde.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt.

* **[!UICONTROL Abmeldungen]**: Zahl der Klicks auf den Abmelde-Link.

* **[!UICONTROL Beschwerden wegen Spam]**: Gibt an, wie oft eine Nachricht als Spam oder Junk gekennzeichnet wurde.

+++

### Fehlergründe {#email-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_error_reasons"
>title="E-Mail – Fehlergründe"
>abstract="Anhand der Graphen und der Tabelle „E-Mail – Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs in den letzten 24 Stunden aufgetreten sind."

![](assets/campaign_email_live_error.png)

Die Graphen und Tabellen **[!UICONTROL Fehlergründe]** geben einen Einblick in die spezifischen Fehler, die während des Sendevorgangs in den letzten 24 Stunden aufgetreten sind. Diese Informationen sind nützlich, um die Art und Häufigkeit von Fehlern zu verstehen.

### Gründe für Ausschluss {#email-exclude-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_excluded_reasons"
>title="E-Mail – Gründe für Ausschluss"
>abstract="Die Graphen und die Tabelle „E-Mail – Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu geführt haben, dass Benutzerprofile, die von der Zielgruppe ausgeschlossen waren, die Nachricht in den letzten 24 Stunden nicht erhalten haben."

![](assets/campaign_email_live_excluded.png)

Die Graphen und die Tabelle **[!UICONTROL Gründe für Ausschluss]** bieten einen umfassenden Überblick über die verschiedenen Faktoren, die in den letzten 24 Stunden zum Ausschluss von Nutzerprofilen aus der Zielgruppe geführt haben.

Auf [dieser Seite](exclusion-list.md) finden Sie eine umfassende Liste der Ausschlussgründe.

### E-Mail – beste Empfänger-Domain {#email-best-recipient}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_best_recipient"
>title="E-Mail – beste Empfänger-Domain"
>abstract="Der Graph und die Tabelle „E-Mail – Beste Empfänger-Domain“ enthalten eine detaillierte Aufschlüsselung der Domains, die Empfängerinnen und Empfänger am häufigsten zum Öffnen der E-Mail verwenden, und bieten wertvolle Einblicke in das Empfängerverhalten aus den letzten 24 Stunden."

![](assets/campaign_email_live_recipient.png)

Die Graphen und die Tabelle **[!UICONTROL E-Mail – Beste Empfänger-Domain]** bieten eine gründliche Aufschlüsselung der Domains, die in den letzten 24 Stunden am häufigsten von Profilen zum Öffnen Ihrer E-Mails verwendet wurden. Dies bietet wertvolle Informationen in das Profilverhalten und darüber, welches die bevorzugten Plattformen sind.

### E-Mail – Angebote {#email-offers}

>[!NOTE]
>
>Die Angebots-Widgets und -Metriken sind nur verfügbar, wenn eine Entscheidung in eine E-Mail eingefügt wurde. Weiterführende Informationen zum Entscheidungs-Management finden Sie auf dieser [Seite](../offers/get-started/starting-offer-decisioning.md).

Die Widgets **[!UICONTROL Angebotsstatistiken]** und **[!UICONTROL Angebotsstatistiken im Zeitverlauf]** messen den Erfolg Ihres Angebots und dessen Wirkung auf Ihre Zielgruppe. Sie enthalten die wichtigsten Informationen zu Ihrer Nachricht in Form von KPIs.

+++ Weitere Informationen zu den Metriken „E-Mail – Angebote“

* **[!UICONTROL Gesendete Angebote]**: Gibt an, wie oft das Angebot gesendet wurde.

* **[!UICONTROL Angebots-Impression]**: Gibt an, wie oft das Angebot in Ihren E-Mails geöffnet wurde.

* **[!UICONTROL Angebot-Klicks]**: Gibt an, wie oft ein Angebot in Ihren E-Mails angeklickt wurde.

+++

## Registerkarte „In-App“ {#inapp-live}

Im **[!UICONTROL Live-Bericht]** Ihrer Kampagne finden Sie auf der Registerkarte **[!UICONTROL In-App]** die wichtigsten Informationen zu den In-App-Nachrichten, die in Ihrer Kampagne versendet wurden.

### In-App-Leistung {#inapp-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_performance"
>title="In-App-Leistung"
>abstract="Die KPIs zur In-App-Leistung bieten wichtige Einblicke in die Interaktion Ihrer Besucherinnen und Besucher mit In-App-Nachrichten in den letzten 24 Stunden."

Die KPIs **[!UICONTROL In-App-Leistung]** bieten wichtige Einblicke in die Interaktion Ihrer Profile mit In-App-Nachrichten in den letzten 24 Stunden und liefern wichtige Metriken zur Bewertung der Effektivität und Wirkung Ihrer In-App-Kampagnen.

+++ Weitere Informationen zu den Metriken „In-App-Leistung“

* **[!UICONTROL Impressions]**: Gesamtzahl der an alle Benutzenden gesendeten In-App-Nachrichten.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit Ihrer In-App-Nachricht. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks, Abbrüche oder andere Interaktionen.

+++

### In-App-Zusammenfassung {#inapp-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_summary"
>title="In-App-Zusammenfassung"
>abstract="Der In-App-Übersichtsgraph zeigt den Verlauf Ihrer In-App-Impressions und -Interaktionen in den letzten 24 Stunden."

Der Graph **[!UICONTROL In-App-Zusammenfassung]** veranschaulicht die Entwicklung Ihrer In-App-Impressionen und -Interaktionen in den letzten 24 Stunden und bietet einen umfassenden Überblick über die Leistung Ihrer In-App-Nachrichten.

+++ Weitere Informationen zu den Metriken „In-App-Zusammenfassung“

* **[!UICONTROL Impressions]**: Gesamtzahl der an alle Benutzerinnen und Benutzer gesendeten In-App-Nachrichten.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit Ihrer In-App-Nachricht. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks, Abbrüche oder andere Interaktionen.

+++

### Interaktionen nach Typ {#inapp-interactions}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_interactions"
>title="Interaktionen nach Typ"
>abstract="Die Graphen und die Tabelle „Interaktionen nach Typ“ beschreiben, wie Benutzende mit Ihrer In-App-Nachricht interagiert haben, indem Klicks, Abbrechen oder Interaktionen verfolgt werden."

Die Graphen und die Tabelle **[!UICONTROL Interaktionen nach Typ]** geben einen detaillierten Überblick darüber, wie Profile in den letzten 24 Stunden mit Ihrer In-App-Nachricht interagiert haben, indem sie Aktionen wie Klicks, Abbrüche oder andere Formen der Interaktion verfolgen.

## Registerkarte „Push-Benachrichtigung“ {#push-live}

In Ihrem **[!UICONTROL Live-Bericht]** in Campaign finden Sie auf der Registerkarte **[!UICONTROL Push-Benachrichtigung]** die wichtigsten Informationen zu den Push-Benachrichtigungen, die in Ihrer Kampagne gesendet wurden.

### Push-Benachrichtigung – Versandleistung {#push-sending-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_performance"
>title="Push-Benachrichtigung – Versandleistung"
>abstract="Der Graph „Push-Benachrichtigung – Versand-Performance“ fasst wichtige Daten zu Ihrer Push-Benachrichtigung zusammen, z. B. „Fehler“ oder „Zugestellte Nachrichten“ aus den letzten 24 Stunden."

![](assets/campain_push_live_sending_performance.png)

Das Diagramm **[!UICONTROL Versandleistung für Push-Benachrichtigungen]** bietet einen umfassenden Überblick über die Daten zu den in den letzten 24 Stunden versandten Push-Benachrichtigungen. Es bietet Einblicke in wichtige Metriken wie zugestellte Nachrichten und Bounces, sodass eine detaillierte Prüfung des Sendevorgangs für Push-Benachrichtigungen möglich ist.

+++ Weitere Informationen zu den Metriken „Push-Benachrichtigungen – Versandleistung“

* **[!UICONTROL Zugestellt]**: Die Anzahl der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Sendevorgangs aufgetretenen Fehler, die das Senden an Profile verhindert haben.

+++

### Push-Benachrichtigung – Statistiken {#push-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_statistics"
>title="Push-Benachrichtigung – Statistiken"
>abstract="Die Tabelle „Push-Benachrichtigung – Statistik“ enthält Daten zur Empfängeraktivität der letzten 24 Stunden für Ihre Push-Benachrichtigung."

![](assets/campaign_push_live_statistics.png)

Die Tabelle **[!UICONTROL Push-Benachrichtigung – Statistiken]** bietet eine übersichtliche Zusammenfassung der wichtigsten Daten zu Ihren Push-Benachrichtigungen der letzten 24 Stunden, einschließlich wichtiger Schlüsselmetriken wie der Anzahl der gezielten Nachrichten und der Anzahl der erfolgreich zugestellten Nachrichten.

+++ Weitere Informationen zu den Metriken „Push-Benachrichtigung – Statistiken“

* **[!UICONTROL Ausführungszeit]**: Startzeit jeder Ausführung Ihrer wiederkehrenden Push-Benachrichtigung. Um nur eine oder mehrere wiederkehrende Push-Benachrichtigungen als Ziel auszuwählen, wählen Sie diese aus der Dropdown-Liste **[!UICONTROL Ausführungszeit]**.

* **[!UICONTROL Zielgruppe]**: Gesamtzahl der beim Sendevorgang verarbeiteten Nachrichten.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge.

* **[!UICONTROL Zugestellt]**: Die Anzahl der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft eine Nachricht geöffnet wurde.

+++

### Push-Benachrichtigung – Sendezusammenfassung {#push-sending-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_summary"
>title="Push-Benachrichtigung – Sendezusammenfassung"
>abstract="Der Graph „Push-Benachrichtigung – Sendezusammenfassung“ zeigt die Daten an, die für gesendete Push-Benachrichtigungen aus den letzten 24 Stunden verfügbar sind."

Der Graph **[!UICONTROL Push-Benachrichtigung – Statistiken]** bietet eine dynamische Darstellung, die eine Analyse der Aktivität Ihrer Push-Benachrichtigungen in den letzten 24 Stunden anzeigt. Diese grafische Darstellung bietet eine umfassende Aufschlüsselung gesendeter Push-Benachrichtigungen.

+++ Weitere Informationen zu den Metriken „Push-Benachrichtigung – Sendezusammenfassung“

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft Ihre Push-Benachrichtigung geöffnet wurde.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf Schaltfläche oder Abbruch.

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler und automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die die Zustellung an Profile verhindert haben.

+++

### Push-Benachrichtigung – Gründe für Ausschluss {#push-excluded}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_excluded_reasons"
>title="Push-Benachrichtigung – Gründe für Ausschluss"
>abstract="Die Graphen und die Tabelle „E-Mail – Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu geführt haben, dass Benutzerprofile, die von der Zielgruppe ausgeschlossen waren, die Nachricht in den letzten 24 Stunden nicht erhalten haben."

Die Graphen und die Tabelle **[!UICONTROL Ausschlussgründe]** zeigen die verschiedenen Gründe an, die in den letzten 24 Stunden verhindert haben, dass Benutzerprofile, die von den Zielprofilen ausgeschlossen wurden, Ihre Push-Benachrichtigungen erhalten haben.

Auf [dieser Seite](exclusion-list.md) finden Sie eine umfassende Liste der Ausschlussgründe.

### Push-Benachrichtigung – Fehlergründe {#push-error}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_error_reasons"
>title="Push-Benachrichtigung – Fehlergründe"
>abstract="Anhand der Graphen und der Tabelle „Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die in den letzten 24 Stunden des Versandvorgangs aufgetreten sind."

Die Tabelle und die Graphen **[!UICONTROL Fehlergründe]** bieten Ihnen die Möglichkeit, die spezifischen Fehler zu identifizieren, die während des Sendevorgangs Ihrer Push-Benachrichtigungen in den letzten 24 Stunden aufgetreten sind, und geben Ihnen einen detaillierten Einblick in die dabei aufgetretenen Probleme.

### Push-Benachrichtigung – Aufschlüsselung nach Plattform {#push-breakdown-platform}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_breakdown_platform"
>title="Push-Benachrichtigung – Aufschlüsselung nach Plattform"
>abstract="Die Graphen und die Tabelle „Aufschlüsselung nach Plattform“ enthalten eine Aufschlüsselung des Erfolgs Ihrer Push-Benachrichtigungen in den letzten 24 Stunden basierend auf dem Betriebssystem der Empfängerin bzw. des Empfängers."

Der Graph und die Tabelle **[!UICONTROL Push-Benachrichtigung – Aufschlüsselung nach Plattform]** bieten eine detaillierte Analyse des Erfolgs Ihrer Push-Benachrichtigungen in den letzten 24 Stunden und bieten Einblicke auf der Grundlage des Betriebssystems Ihres Profils. Diese Aufschlüsselung verbessert Ihr Verständnis der Leistung Ihrer Push-Benachrichtigungen auf verschiedenen Plattformen.

+++ Weitere Informationen zu den Metriken „Push-Benachrichtigung – Aufschlüsselung nach Plattform“

* **[!UICONTROL Zielgruppe]**: Gesamtzahl der bei der Analyse verarbeiteten Nachrichten.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft Ihre Push-Benachrichtigung geöffnet wurde.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf Schaltfläche oder Abbruch.

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler und automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die das Senden an Profile verhindert haben.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

+++

## Registerkarte „SMS“ {#sms-live}

In Ihrem **[!UICONTROL Live-Bericht]** in Campaign finden Sie auf der Registerkarte **[!UICONTROL SMS]** die wichtigsten Informationen zu den SMS-Nachrichten, die in Ihrer Kampagne gesendet wurden.

### SMS – Statistiken {#sms-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_statistics"
>title="SMS – Statistiken"
>abstract="Die Tabelle „SMS – Versandstatistik“ enthält eine Zusammenfassung der wichtigsten Daten zu Ihren SMS-Nachrichten, wie z. B. „Angesprochen“ oder „Zugestellte Nachrichten aus den letzten 24 Stunden“."

![](assets/campaign_live_sms_statistics.png)

Die Tabelle **[!UICONTROL SMS – Statistiken]** bietet eine übersichtliche Zusammenfassung der wichtigsten Daten zu Ihren SMS-Nachrichten der letzten 24 Stunden, einschließlich wichtiger Schlüsselmetriken wie der Anzahl der gezielten Nachrichten und der Anzahl der erfolgreich zugestellten Nachrichten.

+++ Weitere Informationen zu den Metriken „SMS – Statistiken“

* **[!UICONTROL Ausführungszeit]**: Startzeit jeder Ausführung Ihrer wiederkehrenden SMS-Nachricht. Um nur eine oder mehrere wiederkehrende SMS-Nachrichten auszuwählen, wählen Sie die gewünschte Option in der Dropdown-Liste **[!UICONTROL Ausführungszeit]** aus.

* **[!UICONTROL Angesprochen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für diesen Versand eignen.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

* **[!UICONTROL Klicks]**: Gesamtzahl der URL-Besuche.

+++

### SMS – Leistung nach Datum {#sms-perfomance-date}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_performance"
>title="SMS – Leistung nach Datum"
>abstract="Das Widget „SMS – Performance nach Datum“ liefert wichtige Informationen aus den letzten 24 Stunden über Ihre Nachrichten in einer grafischen Darstellung."

![](assets/campaign_live_sms_performance_date.png)

Das Widget **[!UICONTROL SMS – Leistung nach Datum]** bietet einen detaillierten Überblick über die wichtigsten Informationen im Zusammenhang mit Ihren Nachrichten, die in einem Diagramm dargestellt werden und einen Einblick in die Leistungs-Trends der letzten 24 Stunden geben.

+++ Weitere Informationen zu den Metriken „SMS – Leistung nach Datum“

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

+++

### SMS – Fehlergründe {#sms-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_error_reasons"
>title="SMS – Fehlergründe"
>abstract="Die Graphen und die Tabelle „SMS – Fehlerursachen“ ermöglichen es Ihnen, die spezifischen Fehler zu identifizieren, die in den letzten 24 Stunden während des Versandvorgangs aufgetreten sind."

Die Graphen und die Tabelle **[!UICONTROL Ausschlussgründe]** ermöglichen es Ihnen, die spezifischen Fehler zu identifizieren, die beim Versand Ihrer SMS-Nachrichten in den letzten 24 Stunden aufgetreten sind, was eine gründliche Analyse der aufgetretenen Probleme erleichtert.

### SMS – Gründe für Ausschluss {#sms-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_excluded_reasons"
>title="SMS – Gründe für Ausschluss"
>abstract="Die Graphen und die Tabelle „E-Mail – Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu geführt haben, dass Benutzerprofile, die von der Zielgruppe ausgeschlossen waren, die Nachricht in den letzten 24 Stunden nicht erhalten haben."

![](assets/campaign_live_sms_excluded.png)

Die Graphen und die Tabelle **[!UICONTROL Gründe für Ausschluss]** veranschaulichen visuell die vielfältigen Faktoren, die zum Ausschluss von Nutzerprofilen aus der Zielgruppe geführt haben, wodurch sie in den letzten 24 Stunden Ihre SMS-Nachrichten nicht erhalten konnten.

Auf [dieser Seite](exclusion-list.md) finden Sie eine umfassende Liste der Ausschlussgründe.

### SMS – Bounce-Gründe {#sms-bounces-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_bounces_reasons"
>title="SMS – Bounce-Gründe"
>abstract="Die Graphen und die Tabelle „Bounce-Ursachen“ enthalten die Daten aus den letzten 24 Stunden bezüglich Bounce-Nachrichten."

Die Graphen und die Tabelle **[!UICONTROL Bounce-Gründe]** bieten einen umfassenden Überblick über die Daten im Zusammenhang mit Bounce-SMS-Nachrichten und liefern wertvolle Einblicke in die spezifischen Gründe für Bounce-SMS-Nachrichten in den letzten 24 Stunden.

## Registerkarte „Web“ {#web-tab}

Im **[!UICONTROL Live-Bericht]** Ihrer Kampagne werden auf der Registerkarte **[!UICONTROL Web]** die wichtigsten Informationen zu Ihren Web-Seiten aufgeführt.

### Web-Performance {#web-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_performance"
>title="Web-Performance"
>abstract="Die Web-Performance-KPIs bieten umfassende Informationen über die Interaktion Ihrer Besucherinnen und Besucher mit Ihren Web-Erlebnissen aus den letzten 24 Stunden."

![](assets/campaign_live_web_performance.png)

Die KPIs **[!UICONTROL Web-Performance]** bieten umfassende Einblicke in die Interaktion Ihrer Besucherinnen und Besucher mit Ihren Web-Seiten in den letzten 24 Stunden und umfassen wichtige Schlüsselmetriken wie Impressionen und Interaktionen.

+++ Weitere Informationen zu den Metriken „Web-Performance“

* **[!UICONTROL Impressions]**: Gesamtanzahl der für alle Benutzerinnen und Benutzer bereitgestellten Web-Erlebnisse.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit Ihrer Web-Seite. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks oder andere Interaktionen.

+++

### Web-Zusammenfassung {#web-summary}

![](assets/campaign_live_web_summary.png)

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_summary"
>title="Web-Zusammenfassung"
>abstract="Das Diagramm „Web-Zusammenfassung“ zeigt die Entwicklung Ihrer Web-Erlebnisse (Impressions, eindeutige Impressions und Interaktionen) für die letzten 24 Stunden."

Der Graph **[!UICONTROL Web-Zusammenfassung]** zeigt die Entwicklung Ihrer Web-Erlebnisse (Impressions, eindeutige Impressions und Interaktionen) für die letzten 24 Stunden.

+++ Weitere Informationen zu den Metriken „Web-Zusammenfassung“

* **[!UICONTROL Impressions]**: Gesamtanzahl der für alle Benutzerinnen und Benutzer bereitgestellten Web-Erlebnisse.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit Ihrer Web-Seite. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks oder andere Interaktionen.

+++

### Interaktionen nach Element {#web-interactions}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_interactions"
>title="Interaktionen nach Element"
>abstract="Die Tabelle „Interaktionen nach Element“ enthält wichtige Informationen zur Interaktion Ihrer Besucherinnen und Besucher mit verschiedenen Elementen auf Ihren Web-Seiten in den letzten 24 Stunden."

Die Tabelle **[!UICONTROL Interaktionen nach Element]** enthält umfassende Informationen darüber, wie Ihre Besuchenden in den letzten 24 Stunden mit den verschiedenen Elementen auf Ihren Web-Seiten umgegangen sind, und bietet wertvolle Einblicke in die Interaktionen und Vorlieben der Benutzenden.

## Registerkarte „Briefpost“ {#direct-mail-tab}

Im **[!UICONTROL Live-Bericht]** in Campaign werden auf der Registerkarte **[!UICONTROL Briefpost]** die wichtigsten Informationen zu Ihrer Briefpost aufgeführt.

### Briefpost – Versandstatistiken {#direct-mail-sending}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_sending_statistics"
>title="Briefpost – Versandstatistiken"
>abstract="Die Tabelle „Briefpost – Versandstatistik“ enthält eine Zusammenfassung der wichtigsten Daten aus den letzten 24 Stunden zu Ihren Briefpost-Nachrichten, z. B. „Angesprochen“ oder „Zugestellte Nachrichten“."

![](assets/campaign_live_directmail_statistics.png)

Die Tabelle **[!UICONTROL Briefpost – Versandstatistiken]** bietet eine übersichtliche Zusammenfassung der wichtigsten Daten zu Ihren Briefpost-Nachrichten. Dazu gehören Schlüsselmetriken wie die Anzahl der gezielten Nachrichten und die Anzahl der erfolgreich zugestellten Nachrichten innerhalb der letzten 24 Stunden.

+++ Weitere Informationen zu Metriken „Direkt-Mail – Versandstatistiken“

* **[!UICONTROL Angesprochen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für diesen Versand eignen.

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielprofilen ausgeschlossen waren und Ihre Briefpost nicht erhalten haben.

+++

### Briefpost – Fehlergründe {#direct-mail-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_error_reasons"
>title="Briefpost – Fehlergründe"
>abstract="Die Graphen und die Tabelle „Briefpost – Fehlerursachen“ ermöglichen es Ihnen, die spezifischen Fehler zu identifizieren, die in den letzten 24 Stunden aufgetreten sind."

![](assets/campaign_live_error_reasons.png)

Die Graphen und die Tabelle **[!UICONTROL Briefpost – Fehlergründe]** bieten die Möglichkeit, spezifische Fehler zu identifizieren, die während des Sendevorgangs Ihrer Briefpost aufgetreten sind. Dies ermöglicht eine detaillierte Analyse aller in den letzten 24 Stunden aufgetretenen Probleme.

### Briefpost – Gründe für Ausschluss {#direct-mail-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_excluded_reasons"
>title="Briefpost – Gründe für Ausschluss"
>abstract="Die Graphen und die Tabelle „Briefpost – Ausschlussgründe“ veranschaulichen die verschiedenen Faktoren, die dazu geführt haben, dass Benutzerprofile, die von der Zielgruppe ausgeschlossen waren, die Nachricht in den letzten 24 Stunden nicht erhalten haben."

![](assets/campaign_live_directmail_excluded.png)

Die Graphen und die Tabelle **[!UICONTROL Briefpost – Fehlergründe]** veranschaulichen die verschiedenen Faktoren, die zum Ausschluss von Benutzerprofilen aus der Zielgruppe geführt haben, sodass diese in den letzten 24 Stunden Ihre Briefpost nicht erhalten konnten.

Auf [dieser Seite](exclusion-list.md) finden Sie eine umfassende Liste der Ausschlussgründe.

## Zusätzliche Ressourcen

* [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md)
* [Erstellen einer Kampagne](../campaigns/create-campaign.md)
* [Erstellen von API-ausgelösten Kampagnen](../campaigns/api-triggered-campaigns.md)
* [Ändern oder Stoppen einer Kampagne](../campaigns/modify-stop-campaign.md)
* [Kampagnenbericht](campaign-global-report-cja.md)
