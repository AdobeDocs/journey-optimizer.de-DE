---
solution: Journey Optimizer
product: journey optimizer
title: Globaler Bericht zur Journey
description: Erfahren Sie, wie Sie Daten aus dem globalen Bericht zur Journey verwenden
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: 5671f510d8be80b53d57b1ff90a101e500773243
workflow-type: tm+mt
source-wordcount: '4368'
ht-degree: 79%

---

# Globaler Bericht zur Journey {#journey-global-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_global_report"
>title="Globaler Bericht zur Journey"
>abstract="Der globale Bericht zur Journey ermöglicht die Messung der Wirkung von Journeys über einen ausgewählten Zeitraum. Der Bericht ist in verschiedene Widgets unterteilt, die den Erfolg und die Fehler der Journey detailliert darstellen. Jedes Reporting-Dashboard kann durch Ändern der Größe oder Entfernen von Widgets verändert werden."

Globale Berichte, auf die über die Registerkarte „Gesamte Zeit“ zugegriffen werden kann, zeigen Ereignisse an, die vor mindestens zwei Stunden aufgetreten sind, und decken Ereignisse über einen ausgewählten Zeitraum ab. Im Vergleich dazu konzentrieren sich Live-Berichte auf Ereignisse, die innerhalb der letzten 24 Stunden stattgefunden haben. Der Zeitraum ab dem Auftreten des Ereignisses beträgt mindestens zwei Minuten.

Über die Schaltfläche **[!UICONTROL Bericht anzeigen]** können Sie direkt von Ihrer Journey auf den globalen Bericht zur Journey zugreifen.

![](assets/report_journey.png)

Die Seite **[!UICONTROL Globaler Bericht]** zur Journey wird mit den folgenden Registerkarten angezeigt:

* [Journey](#journey-global)
* [E-Mail](#email-global)
* [Push-Benachrichtigung](#push-global)
* [SMS](#sms-global)
* [In-App](#in-app-global)

Der **[!UICONTROL globale Bericht]** zur Journey ist in verschiedene Widgets unterteilt, die den Erfolg und die Fehler Ihrer Journey detailliert beschreiben. Jedes Widget kann bei Bedarf angepasst und gelöscht werden. Weiterführende Informationen dazu finden Sie in diesem [Abschnitt](global-report.md#modify-dashboard).

Eine detaillierte Liste aller in Adobe Journey Optimizer verfügbaren Metriken finden Sie auf [dieser Seite](global-report.md#list-of-components-global).

## Registerkarte „Journey“ {#journey-global}

In Ihrem **[!UICONTROL globalen Bericht]** zur Journey erhalten Sie auf der Registerkarte **[!UICONTROL Journey]** eine übersichtliche Darstellung der wichtigsten Tracking-Daten zu Ihrer Journey.

### Journey-Performance {#journey-perfomance}

>[!CONTEXTUALHELP]
>id="ajo_journey_performance"
>title="Journey-Performance"
>abstract="Mit dem Journey Performance-Widget können Sie den Pfad Ihrer Zielprofile visuell verfolgen, während sie durch Ihre Journey laufen."

![](assets/journey_performance.png)

Mit dem Widget **[!UICONTROL Journey-Performance]** können Sie den Weg Ihrer Zielprofile durch Ihre Journey visuell verfolgen.

### Journey-Statistiken {#journey-statistics}

>[!CONTEXTUALHELP]
>id="ajo_journey_statistics"
>title="Journey-Statistiken"
>abstract="Die Journey Statistics Key Performance Indicators (KPIs) dienen als umfassendes Dashboard, das eine umfassende Analyse der wichtigsten Metriken im Zusammenhang mit Ihrer Journey ermöglicht."

![](assets/journey_statistics.png)

Die KPIs (Key Performance Indicators) zur **[!UICONTROL Journey-Statistik]** dienen als allumfassendes Dashboard und liefern eine Analyse der wesentlichen Metriken, die mit Ihrer Journey verknüpft sind. Dies umfasst Details wie die Anzahl der eingegebenen Profile und die Anzahl der fehlgeschlagenen einzelnen Journeys und bietet einen umfassenden Einblick in die Effektivität und den Grad der Interaktion Ihrer Journeys.

+++ Weitere Informationen zu den Journey-Statistik-Metriken

* **[!UICONTROL Eingestiegene Profile]**: Gesamtzahl der Personen, die das Eintrittsereignis der Journey erreicht haben.

* **[!UICONTROL Ausgestiegene Profile]**: Gesamtzahl der Personen, die die Journey verlassen haben.

* **[!UICONTROL Fehlgeschlagene individuelle Journey]**: Gesamtzahl der individuellen Journeys, die nicht erfolgreich ausgeführt wurden.

+++

### Aktionsleistung {#action-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_performance"
>title="Aktionsleistung"
>abstract="Das Widget Aktionsleistung veranschaulicht die erfolgreichsten Aktionen, die beim Initiieren Ihrer Aktionen stattgefunden haben."

![](assets/journey_action_performance.png)

Die **[!UICONTROL Aktionsleistung]** Widget stellt die erfolgreichsten Aktionen dar, die beim **[!UICONTROL Aktionen]** ausgelöst wurden.

### Top-Aktionen {#top-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_top_actions"
>title="Top-Aktionen"
>abstract="Die Tabelle Top-Aktionen enthält wichtige Informationen zu Ihren Aktionen und bietet kurze Beobachtungen zur Häufigkeit und Wirksamkeit jeder Aktion."

![](assets/journey_top_actions.png)

In der Tabelle **[!UICONTROL Top-Aktionen]** sind wichtige Daten zu Ihren **[!UICONTROL Aktionen]** zusammengestellt. Sie bietet prägnante Einblicke in die Häufigkeit und Leistung der einzelnen Aktionen.

+++ Mehr Informationen zu den Metriken der Top-Aktionen

* **[!UICONTROL Erfolgreich ausgeführte Aktionen]**: Gesamtanzahl der **[!UICONTROL Aktionen]**, die für eine Journey erfolgreich ausgeführt wurden.

* **[!UICONTROL Fehler in Aktion]**: Gesamtanzahl der Fehler, die bei **[!UICONTROL Aktionen]** aufgetreten sind.

+++

### Gründe für Aktionsfehler {#action-error}

>[!CONTEXTUALHELP]
>id="ajo_journey_actions_error_reasons"
>title="Gründe für Aktionsfehler"
>abstract="Die Tabelle mit den Ursachen für Aktionsfehler und das Diagramm enthalten eine ausführliche Zusammenfassung der bei der Ausführung Ihrer Aktionen aufgetretenen Fehler und einen umfassenden Überblick über möglicherweise aufgetretene Probleme."

![](assets/journey_action_error.png)

Die **[!UICONTROL Gründe für Aktionsfehler]** Tabellen und Grafiken bieten einen umfassenden Überblick über Fehler, die während der Ausführung Ihrer **[!UICONTROL Aktionen]**.

### Ereignisse nach Herkunft {#events-origin}

>[!CONTEXTUALHELP]
>id="ajo_journey_events_origin"
>title="Ereignisse nach Herkunft"
>abstract="Die Tabelle Events by Origin und die Diagramme bieten einen Überblick über den erfolgreichen Empfang Ihrer Veranstaltungen. Diese visuellen Darstellungen ermöglichen es Ihnen, die tatsächlich erhaltenen Ereignisse genau zu identifizieren und wertvolle Einblicke in die Leistung und Wirkung der einzelnen Ereignisse innerhalb Ihrer Journey zu erhalten."

![](assets/journey_events_origin.png)

Die **[!UICONTROL Ereignisse nach Ursprung]** Tabellen und Grafiken bieten einen detaillierten Überblick über den erfolgreichen Empfang Ihrer **[!UICONTROL events]**. Durch diese visuellen Darstellungen können Sie genau erkennen, welche Ihrer **[!UICONTROL events]** wurden effektiv empfangen und bieten wertvolle Einblicke in die Performance und Wirkung einzelner Veranstaltungen innerhalb Ihrer Journey.

### Empfangene Ereignisse nach Ereignis {#events-received}

>[!CONTEXTUALHELP]
>id="ajo_journey_events_received"
>title="Empfangene Ereignisse nach Ereignis"
>abstract="Mit dem Ereignisdiagramm Erhalten von Ereignissen können Sie die spezifischen Ereignisse innerhalb Ihrer Journey identifizieren und analysieren, die effektiv ausgeführt wurden. So erhalten Sie wertvolle Einblicke in die Performance und Erfolgsraten einzelner Ereignisse."

![](assets/journey_event_received.png)

Die **[!UICONTROL Vom Ereignis empfangene Ereignisse]** -Diagramm ermöglicht es Ihnen, die spezifischen **[!UICONTROL event]** innerhalb Ihrer Journey effektiv ausgeführt wurde, was wertvolle Einblicke in die Performance und Erfolgsraten einzelner Ereignisse bietet.

### Top-Ereignisse {#top-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_top_events"
>title="Top-Ereignisse"
>abstract="Die Tabelle Top-Ereignisse fasst wichtige Daten zu Ihren Ereignissen zusammen und bietet präzise Beobachtungen zur Häufigkeit und Leistung jedes einzelnen Ereignisses."

![](assets/journey_top_events.png)

Die Tabelle **[!UICONTROL Top-Ereignisse]** kompiliert wichtige Daten zu Ihren **[!UICONTROL Ereignissen]**. Sie bietet prägnante Einblicke in die Häufigkeit und Leistung jedes einzelnen **[!UICONTROL Ereignisses]**.

### Einverständniserklärungen {#consent-policies}

>[!CONTEXTUALHELP]
>id="ajo_journey_consent_policies"
>title="Einverständniserklärungen"
>abstract="Die Tabelle &quot;Einwilligungsrichtlinien&quot;und das Diagramm zeigen die Anzahl der Profile an, die von den einzelnen Richtlinien in Ihren benutzerdefinierten Aktionen ausgeschlossen sind. Diese Präsentation bietet einen klaren Einblick in den Einfluss der einzelnen Zustimmungsrichtlinien auf Profilausschlüsse."

![](assets/journey_consent.png)

Die Tabelle und der Graph **[!UICONTROL Einverständniserklärungen]** zeigen die Anzahl der Profile an, die aus den einzelnen Erklärungen in Ihren benutzerdefinierten Aktionen ausgeschlossen sind. Dies bietet einen klaren Einblick in die Auswirkungen der einzelnen Einverständniserklärungen auf Profilausschlüsse.

Weitere Informationen zur Anpassung von Aktionen finden Sie in [der entsprechenden Dokumentation](../action/about-custom-action-configuration.md).

Damit diese Widgets in Ihren Journey-Berichten angezeigt werden, müssen Sie Ihre Dashboards zurücksetzen. Klicken Sie dazu auf **[!UICONTROL Ändern]** und dann oben in Ihrem Bericht auf **[!UICONTROL Zurücksetzen]**.

## Registerkarte „E-Mail“ {#email-global}

In Ihrem **[!UICONTROL globalen Bericht]** zur Journey finden Sie auf der Registerkarte **[!UICONTROL E-Mail]** die wichtigsten Informationen zu den E-Mails, die in Ihrer Journey gesendet wurden.

### E-Mail – Versandstatistiken {#email-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sending_statistics"
>title="E-Mail – Versandstatistiken"
>abstract="Die Tabelle „E-Mail – Versandstatistik“ enthält wichtige Daten zu Ihrem E-Mail-Kanal, z. B. „Angesprochen“ oder „Zugestellt“."

![](assets/journey_email_statistics.png)

Die Tabelle **[!UICONTROL E-Mail – Sendestatistik]** bietet eine umfassende Zusammenfassung wichtiger Daten zu E-Mails in Ihren Journeys. Sie enthält wichtige Metriken wie die Größe der Zielgruppe und die Anzahl der erfolgreich zugestellten E-Mails. Außerdem bietet sie wertvolle Einblicke in die Effektivität und Reichweite Ihrer E-Mails und Journeys.

+++ Weitere Informationen zu Metriken für die E-Mail-Versandstatistiken

* **[!UICONTROL Ausführungszeit]**: Startzeit jeder Journey-Ausführung bei wiederkehrenden Journeys. Um nur eine oder mehrere Wiederholungen festzulegen, wählen Sie sie die gewünschte Option in der Dropdown-Liste **[!UICONTROL Ausführungszeit]**.

* **[!UICONTROL Zielgruppe]**: Anzahl der Profile, die bei einer Aktion wie etwa E-Mail- oder SMS-Versand angesprochen werden.

* **[!UICONTROL Gesendet]**: Gesamtzahl der für die Journey gesendeten E-Mails.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten E-Mails im Verhältnis zur Gesamtzahl der gesendeten E-Mails.

* **[!UICONTROL Versandrate]**: Prozentsatz der erfolgreich gesendeten E-Mails.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen im Verhältnis zur Gesamtzahl der gesendeten E-Mails.

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der E-Mails, die nicht erfolgreich zugestellt wurden, im Vergleich zur Zahl der gesendeten E-Mails.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

* **[!UICONTROL Fehlerrate]**: Prozentsatz der Fehler, die während des Versandvorgangs auftraten und die Zustellung verhinderten, im Vergleich zur Zahl der gesendeten E-Mails.

* **[!UICONTROL Weitere Zustellversuche]**: Anzahl der E-Mails in der Warteschlange für weitere Zustellversuche.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

+++

### E-Mail – Tracking-Statistiken {#email-tracking}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_tracking_statistics"
>title="E-Mail – Tracking-Statistiken"
>abstract="Die Tabelle „E-Mail – Tracking-Statistik“ enthält Daten zur Profilaktivität für Ihre E-Mail."

![](assets/journey_email_tracking.png)

Die Tabelle **[!UICONTROL E-Mail – Tracking-Statistiken]** bietet einen detaillierten Überblick über die Profilaktivität in Bezug auf E-Mails, die in Ihrer Journey enthalten sind. Dazu gehören Metriken zu Öffnungen, Klicks und andere relevante Interaktionsindikatoren, die einen umfassenden Überblick darüber bieten, wie Profile mit Ihrem E-Mail-Inhalt interagieren.

+++ Weitere Informationen über E-Mails – Metriken zu Tracking-Statistiken

* **[!UICONTROL Ausführungszeit]**: Startzeit jeder Ausführung der wiederkehrenden E-Mail in Ihrer Journey. Um nur eine oder mehrere wiederkehrende E-Mails festzulegen, wählen Sie die gewünschte Option in der Dropdown-Liste **[!UICONTROL Ausführungszeit]**.

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen Ihrer E-Mails in einer Journey

* **[!UICONTROL Eindeutige Öffnungen]**: Prozentsatz der geöffneten E-Mails.

* **[!UICONTROL Rate der Einzelöffnungen]**: Gesamtzahl der geöffneten E-Mails im Verhältnis zur Zahl der versendeten E-Mails.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf Inhalte Ihrer E-Mails

* **[!UICONTROL Einzelklicks]**: Anzahl der Empfängerinnen und Empfänger, die auf Inhalte in Ihren E-Mails geklickt haben

* **[!UICONTROL Klickrate]**: Prozentsatz der Benutzenden, die mit der Journey interagiert haben.

* **[!UICONTROL Abmeldungen]**: Zahl der Klicks auf den Abmelde-Link.

* **[!UICONTROL Spam-Beschwerden]**: Gibt an, wie oft Ihre E-Mails als Spam oder Junk gekennzeichnet wurden

+++

### E-Mail – Versandleistung {#email-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sending_performance"
>title="E-Mail – Versandleistung"
>abstract="Der Graph „E-Mail – Versandleistung“ enthält umfassende Daten zu gesendeten E-Mails und bietet Einblicke in Schlüsselmetriken wie zugestellte Nachrichten und Bounces, sodass eine detaillierte Analyse des E-Mail-Versandprozesses möglich ist."

![](assets/journey_email_performance.png)

Der Graph **[!UICONTROL E-Mail – Versandleistung]** bietet einen umfassenden Überblick über Daten zu gesendeten E-Mails in Ihrer Journey und liefert Einblicke in Schlüsselmetriken wie zugestellte Nachrichten und Bounces. Dies ermöglicht eine detaillierte Analyse des E-Mail-Sendevorgangs und liefert wertvolle Informationen über die Effizienz und Performance Ihrer Journeys.

+++ Weitere Informationen zu Metriken von „E-Mail – Versandleistung“

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten E-Mails im Verhältnis zur Gesamtzahl der gesendeten E-Mails.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Weitere Zustellversuche]**: Anzahl der E-Mails in der Warteschlange für weitere Zustellversuche.

* **[!UICONTROL Fehler]**: Gesamtanzahl der während eines Sendevorgangs aufgetretenen Fehler, die das Senden an Profile verhindert haben

+++

### E-Mail – Bounce-Kategorien und -Gründe {#email-bounce-categories}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces"
>title="E-Mail – Bounce-Kategorien und -Gründe"
>abstract="Die Widgets E-Mail - Bounce-Kategorien und -Gründe aggregieren die Daten zu Bounce Messages und bieten tiefgründige Einblicke in die spezifischen Gründe und Kategorien, die zu E-Mail-Bounces beitragen"

![](assets/journey_email_bounce_categories.png)

Die Widgets **[!UICONTROL Bounce-Gründe]** und **[!UICONTROL Bounce-Kategorien]** kompilieren die verfügbaren Daten zu nicht zugestellten Nachrichten und bieten detaillierte Einblicke in die Gründe und Kategorien nicht zugestellter E-Mails.

Weitere Informationen zu Bounces finden Sie auf der Seite [ Unterdrückungsliste](../reports/suppression-list.md).

+++ Weitere Informationen zu den Metriken von E-Mail-Bounce-Kategorien

* **[!UICONTROL Hardbounce]**: die Gesamtzahl der permanenten Fehler, wie eine falsche E-Mail-Adresse. Dazu gehören Fehlermeldungen, die explizit eine ungültige Adresse anzeigen, wie etwa „Benutzer unbekannt“.

* **[!UICONTROL Softbounce]**: die Gesamtzahl der temporären Fehler, wie ein voller Posteingang.

* **[!UICONTROL Ignoriert]**: Die Gesamtzahl der temporären Ereignisse, beispielsweise Abwesenheit, oder technischer Fehler, zum Beispiel wenn der Absendertyp Postmaster ist.

+++

### E-Mail – Fehlergründe {#email-errors}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_error_reasons"
>title="E-Mail – Fehlergründe"
>abstract="Anhand der Graphen und der Tabelle „E-Mail – Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs aufgetreten sind."

![](assets/journey_email_error.png)

Die Graphen und die Tabelle **[!UICONTROL Fehlergründe]** bieten einen detaillierten Überblick über die Fehler, die während des Sendevorgangs aufgetreten sind, und liefern wertvolle Informationen über Art und Auftreten von Fehlern.

### E-Mail – Gründe für Ausschluss {#email-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_excluded_reasons"
>title="E-Mail – Gründe für Ausschluss"
>abstract="Die Graphen und die Tabelle „Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu führten, dass Benutzerprofile aus der Zielgruppe ausgeschlossen wurden und die Nachricht nicht erhielten."

![](assets/journey_email_excluded.png)

Die Graphen und die Tabelle **[!UICONTROL Gründe für Ausschluss]** bieten einen umfassenden Überblick über die verschiedenen Faktoren, die zum Ausschluss von Nutzerprofilen aus der Zielgruppe geführt haben, sodass die Nachricht nicht empfangen wurde.

Auf [dieser Seite](exclusion-list.md) finden Sie eine umfassende Liste der Ausschlussgründe.

### Gesendet und zugestellt nach Domains {#sent-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sent_delivered_domains"
>title="Gesendet und zugestellt nach Domains"
>abstract="Die Tabelle Gesendet und zugestellt nach Domains liefert eine Aufschlüsselung der E-Mails, die nach Domains kategorisiert sind, und bietet umfassende Einblicke in die Gesamtleistung Ihrer E-Mail-Kommunikation."

![](assets/journey_email_sent_domains.png)

Die **[!UICONTROL Gesendet und von Domänen bereitgestellt]** Tabellen und Diagramme enthalten eine detaillierte Aufschlüsselung der E-Mails auf Domänenebene und bieten umfassende Einblicke in die Leistung Ihrer E-Mails.

+++ Weitere Informationen zu den Metriken zu „Gesendet und zugestellt nach Domains“

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge für Ihre E-Mails.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten E-Mails im Verhältnis zur Gesamtzahl der gesendeten E-Mails.

+++

### Öffnungen und Klicks nach Domains {#open-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_open_clicks_domains"
>title="Öffnungen und Klicks nach Domains"
>abstract="Das Diagramm &quot;Öffnungen und Klicks nach Domänen&quot;und die Tabelle bieten eine detaillierte Aufschlüsselung auf Domänenebene, die einen umfassenden Überblick darüber bietet, wie Ihre Zielgruppe mit Ihren E-Mails interagiert."

![](assets/journey_email_open_domains.png)

Die **[!UICONTROL Öffnungen und Klicks nach Domänen]** Diagramm und Tabelle zeigen eine Aufschlüsselung der Interaktion Ihrer Profile mit Ihrer E-Mail auf Domänenebene, die wertvolle Einblicke in die Interaktion verschiedener Domänen mit Ihrem Inhalt bietet.

+++ Weitere Informationen zu den Metriken zu „Öffnungen und Klicks nach Domains“

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen der E-Mail.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf den Inhalt in einer E-Mail.

+++

### Bounces und Fehler nach Domains {#bounces-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces_errors_domains"
>title="Bounces und Fehler nach Domains"
>abstract="Das Diagramm und die Tabelle &quot;Bounces &amp; Fehler nach Domänen&quot;bieten eine granulare Aufschlüsselung auf Domänenebene und bieten Einblicke in spezifische Fehler, die beim E-Mail-Versand aufgetreten sind."

![](assets/journey_email_bounce_domains.png)

Die **[!UICONTROL Bounces und Fehler nach Domänen]** Diagramm und Tabelle bieten eine Aufschlüsselung der spezifischen Fehler, die während des Versandvorgangs auf Domänenebene aufgetreten sind, und enthalten eine detaillierte Analyse der aufgetretenen Probleme.

+++ Weitere Informationen zu den Metriken zu „Bounces und Fehler nach Domains“

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen im Verhältnis zur Gesamtzahl der gesendeten E-Mails.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Sendevorgangs aufgetretenen Fehler, die das Senden an Profile verhindert haben.

+++

### Bounce-Gründe nach Domain {#bounce-reasons-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces_reasons_domains"
>title="Bounce-Gründe nach Domain"
>abstract="Die Absprunggründe nach Domänendiagramm und Tabelle bieten eine Aufschlüsselung auf Domänenebene, die umfassende Einblicke in temporäre und permanente Fehler bietet. Diese detaillierte Analyse liefert Ihnen wertvolle Informationen über die spezifischen Gründe für nicht zugestellte Nachrichten."

![](assets/journey_email_bounce_reasons_domain.png)

Die **[!UICONTROL Bounce-Gründe nach Domain]** Diagramme und Tabellen bieten eine Aufschlüsselung der Daten auf Domänenebene bezüglich temporärer und permanenter Fehler und bieten detaillierte Einblicke in die Ursachen für abgespeckte Nachrichten.

### E-Mail – Top-URL {#email-top}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_top_url"
>title="E-Mail – Top-URL"
>abstract="Der Graph und die Tabelle „E-Mail – Beste URL“ bieten einen umfassenden Überblick über die URLs in Ihrer E-Mail, die den höchsten Besucher-Traffic erhalten, sodass Sie die beliebtesten Links identifizieren können."

![](assets/journey_email_top.png)

Der Graph und die Tabelle **[!UICONTROL E-Mail – Top-URL]** bieten einen umfassenden Überblick über die URLs in Ihren E-Mails, die den meisten Besucher-Traffic anziehen. Auf diese Weise können Sie die beliebtesten Links identifizieren und priorisieren und Ihr Verständnis der Profilinteraktion mit bestimmten Inhalten in Ihren E-Mails verbessern.

### E-Mail – Optimierung {#email-sto}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_optimization"
>title="E-Mail – Optimierung"
>abstract="Die Widgets Sendezeitoptimierung und Optimierte bzw. Nicht-optimierte Sendungen enthalten detaillierte Informationen zu Ihren Nachrichten und heben hervor, ob sie optimiert wurden oder nicht."

![](assets/journey_email_sto.png)

>[!NOTE]
>
>Die Widgets **[!UICONTROL Versandzeitoptimierung]** und **[!UICONTROL Optimiert vs. nicht optimiert]** sind nur verfügbar, wenn die Option „Versandzeitoptimierung“ für Ihren Versand aktiviert ist. Weitere Informationen zur Versandzeitoptimierung finden Sie auf [dieser Seite](../building-journeys/journeys-message.md#send-time-optimization).

Die Widgets **[!UICONTROL Versandzeitoptimierung]** und **[!UICONTROL Optimiert vs. nicht optimiert]** zeigen den Erfolg Ihrer E-Mails in Abhängigkeit von der Versandmethode an: optimiert oder normal.

+++ Mehr Informationen zur Versandzeitoptimierung und zu Metriken „Optimiert vs. nicht optimiert“

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.
* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Gesendet]**: Gesamtzahl der für die Journey gesendeten E-Mails.

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft Ihre E-Mails in der Journey geöffnet wurden.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf Inhalte in Ihren E-Mails.

+++

### E-Mail – Angebote {#email-offers}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_offers"
>title="E-Mail – Angebote"
>abstract="Die Widgets Angebotsstatistik und Angebote bieten umfassende Statistiken über die Leistung Ihrer Angebote, eine detaillierte Analyse ihrer Wirkung im Zeitverlauf und detaillierte Statistiken für ein tieferes Verständnis."

>[!NOTE]
>
>Die Angebots-Widgets und -Metriken sind nur verfügbar, wenn eine Entscheidung in eine E-Mail eingefügt wurde. Weiterführende Informationen zum Entscheidungs-Management finden Sie auf dieser [Seite](../offers/get-started/starting-offer-decisioning.md).

Die Widgets **[!UICONTROL Angebotsstatistik]** und **[!UICONTROL Detaillierte Angebotsstatistik]** messen im Zeitverlauf den Erfolg und die Wirkung Ihres Angebots auf Ihre Zielgruppe. Sie enthalten die wichtigsten Informationen zu Ihrer Nachricht in Form von KPIs.

+++ Weitere Informationen über E-Mails – Angebotsmetriken

* **[!UICONTROL Gesendete Angebote]**: Gibt an, wie oft das Angebot gesendet wurde.

* **[!UICONTROL Angebots-Impression]**: Gibt an, wie oft das Angebot in Ihren E-Mails geöffnet wurde.

* **[!UICONTROL Angebots-Klicks]**: Gibt an, wie oft ein Angebot in Ihren E-Mails angeklickt wurde.

* **[!UICONTROL Platzierungsname]**: Name der Platzierung, die zur Anzeige Ihres Angebots verwendet wird. Weiterführende Informationen zu Platzierungen finden Sie auf dieser [Seite](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Angebotsname]**: Name des Angebots, das Ihren E-Mails hinzugefügt wurde. Weiterführende Informationen zu Platzierungen finden Sie auf dieser [Seite](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Angebot versendet]**: Gibt an, wie oft das Angebot insgesamt versendet wurde.

* **[!UICONTROL Impressionsrate des Angebots]**: Prozentsatz der geöffneten Angebote im Verhältnis zur Anzahl der gesendeten Angebote.

* **[!UICONTROL Klickrate des Angebots]**: Prozentsatz der Benutzer, die mit dem Angebot interagiert haben.

+++

## Registerkarte „Push-Benachrichtigung“ {#push-global}

In dem **[!UICONTROL globalen Bericht]** Ihrer Journey finden Sie auf der Registerkarte **[!UICONTROL Push-Benachrichtigungen]** die wichtigsten Informationen zu den Push-Benachrichtigungen, die in Ihrer Journey gesendet wurden.

### Push-Benachrichtigung – Sendestatistik {#push-sending-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_sending_statistics"
>title="Push-Benachrichtigung – Sendestatistik"
>abstract="Die Tabelle „Push-Benachrichtigung – Sendestatistik“ fasst wesentliche Daten über Ihre Push-Benachrichtigungen zusammen, z. B. „Angesprochen“ oder „Zugestellte Nachrichten“."

![](assets/journey_push_sending.png)

Die Tabelle **[!UICONTROL Push-Benachrichtigung – Sendestatistik]** bietet eine übersichtliche Zusammenfassung der wichtigsten Daten zu Ihren Push-Benachrichtigungen, einschließlich wichtiger Schlüsselmetriken wie der Anzahl der gezielten Nachrichten und der Anzahl der erfolgreich zugestellten Nachrichten.

+++ Weitere Informationen zu Metriken für „Push-Benachrichtigungen – Versandstatistiken“

* **[!UICONTROL Ausführungszeit]**: Startzeit jeder Journey-Ausführung bei wiederkehrenden Journeys. Um nur eine oder mehrere Wiederholungen festzulegen, wählen Sie sie die gewünschte Option in der Dropdown-Liste **[!UICONTROL Ausführungszeit]**.

* **[!UICONTROL Zielgruppe]**: Anzahl der Profile, die bei einer Aktion wie etwa E-Mail- oder SMS-Versand angesprochen werden.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Benachrichtigungen

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Push-Benachrichtigungen in Bezug auf die Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Versandrate]**: Prozentsatz der erfolgreich gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen im Verhältnis zur Gesamtzahl der gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der Push-Benachrichtigungen, die unzustellbar waren, im Verhältnis zu den gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Sendevorgangs aufgetretenen Fehler, die das Senden an Profile verhindert haben.

* **[!UICONTROL Fehlerrate]**: Prozentsatz der Fehler, die während des Sendevorgangs auftraten und das Senden verhindert haben, im Verhältnis zur Zahl der gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

+++

### Push-Benachrichtigung – Tracking-Statistiken {#push-tracking-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_tracking_statistics"
>title="Push-Benachrichtigung – Tracking-Statistiken"
>abstract="Die Tracking-Statistik für Push-Benachrichtigungen bietet Daten zur Profilaktivität für Ihre Push-Benachrichtigung."

Das Widget **[!UICONTROL Push-Benachrichtigung – Tracking-Statistiken]** bietet einen detaillierten Überblick über die Profilaktivität im Zusammenhang mit Ihren Push-Benachrichtigungen und liefert wichtige Erkenntnisse über die Interaktion und die Effektivität von Push-Benachrichtigungen.

+++ Weitere Informationen zu Metriken für „Push-Benachrichtigungen – Tracking-Statistiken“

* **[!UICONTROL Ausführungszeit]**: Startzeit jeder Journey-Ausführung bei wiederkehrenden Journeys. Um nur eine oder mehrere Wiederholungen festzulegen, wählen Sie sie die gewünschte Option in der Dropdown-Liste **[!UICONTROL Ausführungszeit]**.

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft Ihre Push-Benachrichtigungen in der Journey geöffnet wurden.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf eine Schaltfläche oder Abbruch.

+++

### Push-Benachrichtigung – Sendezusammenfassung {#push-summary}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_sending_summary"
>title="Push-Benachrichtigung – Sendezusammenfassung"
>abstract="Der Graph „Push-Benachrichtigung – Sendezusammenfassung“ zeigt die Daten an, die für gesendete Push-Benachrichtigungen verfügbar sind."

![](assets/journey_push_summary.png)

Das Diagramm **[!UICONTROL Push-Benachrichtigung – Sendezusammenfassung]** bietet eine dynamische Darstellung, die eine Analyse Ihrer Push-Benachrichtigungsaktivitäten anzeigt. Diese grafische Darstellung bietet eine umfassende Aufschlüsselung gesendeter Push-Benachrichtigungen.

+++ Weitere Informationen zu Push-Benachrichtigungen – Metriken zur Sendezusammenfassung

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft Ihre Push-Benachrichtigungen in der Journey geöffnet wurden.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf eine Schaltfläche oder Abbruch.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen im Verhältnis zur Gesamtzahl der gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Push-Benachrichtigungen im Verhältnis zur Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Sendevorgangs aufgetretenen Fehler, die das Senden an Profile verhindert haben.

+++

### Push-Benachrichtigung – Fehlergründe {#push-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_error_reasons"
>title="Push-Benachrichtigung – Fehlergründe"
>abstract="Anhand der Diagramme und Tabellen mit Fehlerursachen können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs aufgetreten sind"

![](assets/journey_push_error.png)

Die Tabelle und die Graphen **[!UICONTROL Fehlergründe]** bieten Ihnen die Möglichkeit, die spezifischen Fehler zu identifizieren, die während des Sendevorgangs Ihrer Push-Benachrichtigungen aufgetreten sind, und geben Ihnen einen detaillierten Einblick in die dabei aufgetretenen Probleme.

### Push-Benachrichtigung – Gründe für Ausschluss {#push-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_excluded_reasons"
>title="Push-Benachrichtigung – Gründe für Ausschluss"
>abstract="Die Diagramme und die Tabelle Ausgeschlossene Gründe veranschaulichen die verschiedenen Faktoren, die den Empfang von Nachrichten durch aus der Zielgruppe ausgeschlossene Benutzerprofile verhindert haben."

![](assets/journey_push_excluded.png)

Die Graphen und die Tabelle **[!UICONTROL Ausschlussgründe]** zeigen die verschiedenen Gründe an, die verhindert haben, dass Nutzerprofile, die von den Zielprofilen ausgeschlossen wurden, die Push-Benachrichtigung erhalten haben.

Auf [dieser Seite](exclusion-list.md) finden Sie die umfassende Liste der Ausschlussgründe.

### Push-Benachrichtigung – Aufschlüsselung nach Plattform {#push-breakdown}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_breakdown_platform"
>title="Push-Benachrichtigung – Aufschlüsselung nach Plattform"
>abstract="Die Tabelle Push-Benachrichtigung - Aufschlüsselung nach Platform-Diagrammen und -Tabellen enthält eine Aufschlüsselung des Erfolgs Ihrer Push-Benachrichtigungen nach dem Betriebssystem des Profils."

![](assets/journey_push_breakdown.png)

Der Graph und die Tabelle **[!UICONTROL Aufschlüsselung nach Plattform]** liefern eine detaillierte Analyse des Erfolgs Ihrer Push-Benachrichtigungen und bieten Einblicke auf der Grundlage des Betriebssystems Ihres Profils. Diese Aufschlüsselung verbessert Ihr Verständnis der Leistung Ihrer Push-Benachrichtigungen auf verschiedenen Plattformen.

### Push-Benachrichtigungen – Optimierung {#push-sto}

>[!NOTE]
>
>Die **[!UICONTROL Optimiert vs. nicht optimiert]** und **[!UICONTROL Versandzeitoptimierung]** -Widgets sind nur verfügbar, wenn die Option Sendezeitoptimierung für Ihren Versand aktiviert ist. Weitere Informationen zur Versandzeitoptimierung finden Sie auf [dieser Seite](../building-journeys/journeys-message.md#send-time-optimization).

Die **[!UICONTROL Optimiert vs. nicht optimiert]** und **[!UICONTROL Versandzeitoptimierung]** Widgets zeigen die wichtigsten Informationen bezüglich Ihrer Nachricht an, ob sie optimiert wurden oder nicht.

+++ Weitere Informationen zu den Metriken für Push-Benachrichtigung – Optimierung

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft Ihre Push-Benachrichtigungen in der Journey geöffnet wurden.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf eine Schaltfläche oder Abbruch.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten Nachrichten.

+++

## Registerkarte „SMS“ {#sms-global}

### SMS – Sendestatistik {#sms-sending-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_sending_statistics"
>title="SMS – Sendestatistik"
>abstract="Die Tabelle SMS - Versandstatistiken enthält eine Zusammenfassung der wichtigsten Daten zu Ihren SMS-Nachrichten, z. B. Zielgerichtete oder zugestellte Nachrichten."

![](assets/journey_sms_sending.png)

Die Tabelle **[!UICONTROL SMS – Versandstatistiken]** bietet eine kurze Zusammenfassung wichtiger Daten zu Ihren SMS-Nachrichten und umfasst wichtige Metriken wie die Anzahl der gezielten Nachrichten und die Anzahl der erfolgreich zugestellten Nachrichten.

+++ Weitere Informationen zu Metriken für „SMS – Versandstatistiken“

* **[!UICONTROL Ausführungszeit]**: Startzeit jeder Journey-Ausführung bei wiederkehrenden Journeys. Um nur eine oder mehrere Wiederholungen festzulegen, wählen Sie sie die gewünschte Option in der Dropdown-Liste **[!UICONTROL Ausführungszeit]**.

* **[!UICONTROL Zielgruppe]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für die SMS-Nachrichten eignen.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die SMS-Nachricht nicht erhalten haben.

* **[!UICONTROL Gesendet]**: Gesamtzahl der für die Journey gesendeten SMS-Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen im Verhältnis zur Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Sendevorgangs aufgetretenen Fehler, die das Senden an Profile verhindert haben.

+++

### SMS – Tracking-Statistiken {#sms-tracking-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_tracking_statistics"
>title="SMS – Tracking-Statistiken"
>abstract="Das Widget SMS - Trackingstatistiken bietet einen umfassenden Überblick über die wichtigsten Informationen zur Interaktion Ihrer Besucher mit Ihrer URL."

![](assets/journey_sms_tracking.png)

Das Widget **[!UICONTROL SMS – Tracking-Statistiken]** bietet einen detaillierten Überblick über wichtige Informationen zur Interaktion Ihrer Besucherinnen und Besucher mit Ihren URLs und bietet Einblicke in die Effektivität Ihrer SMS-Nachrichten.

* **[!UICONTROL Ausführungszeit]**: Startzeit jeder Ausführung der wiederkehrenden SMS-Nachrichten. Um nur eine oder mehrere wiederkehrende SMS-Nachrichten festzulegen, wählen Sie die gewünschte Option in der Dropdown-Liste **[!UICONTROL Ausführungszeit]** aus.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in Ihren SMS-Nachrichten.

### SMS – Leistung nach Datum {#sms-performance-date}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_perfomance_date"
>title="SMS – Leistung nach Datum"
>abstract="Das Widget SMS - Leistung nach Datum bietet wichtige Informationen über Ihre Nachrichten in einer grafischen Darstellung."

![](assets/journey_sms_performance.png)

Das Widget **[!UICONTROL SMS – Leistung nach Datum]** bietet einen detaillierten Überblick über wichtige Informationen zu Ihren Nachrichten, die in einem Diagramm dargestellt werden und einen Einblick in die Leistungs-Trends über bestimmte Zeiträume geben.

+++ Weitere Informationen zu SMS – Metriken zur Leistung nach Datum

* **[!UICONTROL Gesendet]**: Gesamtzahl der für die Journey gesendeten SMS-Nachrichten

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen im Verhältnis zur Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Sendevorgangs aufgetretenen Fehler, die das Senden an Profile verhindert haben.

+++

### SMS – Bounce-Gründe {#sms-bounce}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_bounces_reasons"
>title="SMS – Bounce-Gründe"
>abstract="Die Graphen und die Tabelle „Bounce-Gründe“ enthalten die verfügbaren Daten zu Bounce-Nachrichten."

![](assets/journey_sms_bounce_reasons.png)

Die Graphen und die Tabelle **[!UICONTROL Bounce-Gründe]** bieten einen umfassenden Überblick über Daten zu nicht zugestellten SMS-Nachrichten und liefern wertvolle Einblicke in die spezifischen Gründe von nicht zugestellten SMS-Nachrichten.

### SMS – Fehlergründe {#sms-error}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_error_reasons"
>title="SMS – Fehlergründe"
>abstract="Anhand der Graphen und der Tabelle „SMS – Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs aufgetreten sind."

![](assets/journey_sms_error.png)

Anhand der Graphen und der Tabelle **[!UICONTROL Fehlergründe]** können Sie die Fehler genau identifizieren, die während des Sendevorgangs Ihrer SMS-Nachrichten aufgetreten sind. Dies ermöglicht eine gründliche Analyse aller aufgetretenen Probleme.

### SMS – Gründe für Ausschluss {#sms-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_excluded_reasons"
>title="SMS – Gründe für Ausschluss"
>abstract="Die Graphen und die Tabelle „Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu führten, dass Benutzerprofile aus der Zielgruppe ausgeschlossen wurden und die Nachricht nicht erhielten."

![](assets/journey_sms_excluded.png)

Die Graphen und die Tabelle **[!UICONTROL Gründe für Ausschluss]** zeigen visuell die verschiedenen Faktoren an, die zum Ausschluss von Benutzerprofilen aus der Zielgruppe geführt haben, sodass diese keine SMS-Nachrichten erhalten konnten.

Auf [dieser Seite](exclusion-list.md) finden Sie eine umfassende Liste der Ausschlussgründe.

### SMS – Klicks nach Links {#sms-clicks}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_clicks"
>title="SMS – Klicks nach Links"
>abstract="Das Widget SMS - Klicks nach Links bietet wichtige Einblicke in die Interaktion Ihrer Besucher mit den URLs in Ihren Nachrichten."

![](assets/journey_sms_clicks.png)

Das Widget **[!UICONTROL SMS – Klicks nach Links]** bietet Ihnen wichtige Einblicke in die Interaktion Ihrer Besucherinnen und Besucher mit den URLs in Ihren Nachrichten und liefert wertvolle Informationen darüber, welche Links die meisten Interaktionen anziehen.

## Registerkarte „In-App“ {#in-app-global}

Im **[!UICONTROL globalen Bericht]** Ihrer Journey finden Sie auf der Registerkarte **[!UICONTROL In-App]** die wichtigsten Informationen zu den In-App-Nachrichten, die in Ihren Journeys versendet wurden.

### In-App-Leistung {#inapp-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_performance"
>title="In-App-Leistung"
>abstract="Die KPIs zur In-App-Leistung bieten wichtige Einblicke in die Interaktion Ihrer Besuchenden mit In-App-Nachrichten."

![](assets/journey_inapp_performance.png)

Die **[!UICONTROL In-App-Leistung]** KPIs bieten wichtige Einblicke in die Interaktion Ihrer Profile mit In-App-Nachrichten und liefern wichtige Metriken, mit denen Sie die Effektivität und die Wirkung der in Ihrer Journey enthaltenen In-App-Nachrichten bewerten können.

+++ Weitere Informationen zu In-App – Metriken zur Leistung nach Datum

* **[!UICONTROL Eindeutige Impressions]**: Anzahl der eindeutigen Benutzenden, an die die In-App-Nachricht gesendet wurde.

* **[!UICONTROL Impressions]**: Gesamtzahl der an alle Benutzenden gesendeten In-App-Nachrichten.

  >[!NOTE]
  >
  >Um sicherzustellen, dass eine Impression gezählt wird, muss die Benutzerin bzw. der Benutzer zwei Kriterien erfüllen:
  >* Qualifizierung innerhalb des In-App-Erlebnisses, das durch Erreichen der spezifischen In-App-Aktivität in ihrer bzw. seiner Journey erreicht wird.
  >* Erfüllung der in den Auslöseregeln festgelegten Bedingungen.
  > 
  >Aufgrund des zweiten Kriteriums kann es erhebliche Unterschiede zwischen der Anzahl der angesprochenen Profile und der Anzahl der eindeutigen Impressions geben.

* **[!UICONTROL Interaktionen]**: Zahl der Interaktionen mit Ihrer In-App-Nachricht. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks, Abbrüche oder andere Interaktionen.
+++

### In-App-Zusammenfassung {#inapp-summary}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_summary"
>title="In-App-Zusammenfassung"
>abstract="Der Graph „In-App – Zusammenfassung“ zeigt die Entwicklung Ihrer In-App-Impressions und -Interaktionen für den jeweiligen Zeitraum an."

![](assets/journey_inapp_summary.png)

Die **[!UICONTROL In-App-Zusammenfassung]** veranschaulicht die Entwicklung Ihrer In-App-Impressions und -Interaktionen über den angegebenen Zeitraum und bietet einen umfassenden Überblick über die Leistung Ihrer In-App-Nachrichten.

### Interaktionen nach Typ {#interactions-type}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_interactions"
>title="Interaktionen nach Typ"
>abstract="Der Graph und die Tabelle „Interaktionen nach Typ“ beschreiben, wie Benutzende mit Ihrer In-App-Nachricht interagiert haben, indem Klicks, Abbrechen oder Interaktionen verfolgt werden."

![](assets/journey_inapp_interactions.png)

Die Graphen und die Tabelle **[!UICONTROL Interaktionen nach Typ]** bieten einen detaillierten Überblick darüber, wie Profile mit Ihrer In-App-Nachricht interagiert haben, indem sie Aktionen wie Klicks, Abbrüche oder andere Formen der Interaktion verfolgen.
