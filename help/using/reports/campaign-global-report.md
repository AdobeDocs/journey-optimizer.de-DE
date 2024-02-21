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
source-git-commit: 5671f510d8be80b53d57b1ff90a101e500773243
workflow-type: tm+mt
source-wordcount: '4806'
ht-degree: 92%

---

# Globaler Bericht zu Kampagnen {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="Globaler Bericht zu Kampagnen"
>abstract="Der globale Bericht einer Kampagne ermöglicht die Messung der Wirkung von Kampagnen über einen ausgewählten Zeitraum. Der Bericht ist in verschiedene Widgets unterteilt, die den Erfolg und die Fehler der Kampagne detailliert darstellen. Jedes Reporting-Dashboard kann durch Ändern der Größe oder Entfernen von Widgets verändert werden."

Globale Berichte, auf die über die Registerkarte **Gesamte Zeit** zugegriffen werden kann, zeigen Ereignisse an, die vor mindestens zwei Stunden aufgetreten sind, und decken Ereignisse über einen ausgewählten Zeitraum ab. Im Vergleich dazu konzentrieren sich Live-Berichte auf Ereignisse, die innerhalb der letzten 24 Stunden stattgefunden haben. Der Zeitraum ab dem Auftreten des Ereignisses beträgt mindestens zwei Minuten.

Über die Schaltfläche **[!UICONTROL Bericht anzeigen]** ist der direkte Zugriff in einer Campaign-Instanz auf den globalen Bericht in Campaign möglich.

![](assets/campaign_report_global_5.png)

Die Seite **[!UICONTROL Globaler Bericht]** in Campaign wird mit den folgenden Registerkarten angezeigt:

* [Campaign](#campaign-global)
* [E-Mail](#email-global)
* [In-App](#inapp-global)
* [Push-Benachrichtigung](#push-global)
* [SMS](#sms-global)
* [Web](#web-tab)
* [Briefpost](#direct-mail-global)

Der **[!UICONTROL Globale Bericht]** in Campaign ist in verschiedene Widgets unterteilt, die Erfolge und Fehler bei Ihrer Kampagne detailliert beschreiben. Jedes Widget kann bei Bedarf angepasst und gelöscht werden. Weiterführende Informationen dazu finden Sie in diesem [Abschnitt](../reports/global-report.md#modify-dashboard).

Eine detaillierte Liste aller in Adobe Journey Optimizer verfügbaren Metriken finden Sie auf [dieser Seite](global-report.md#list-of-components-global.md)

## Registerkarte „Kampagne“ {#campaign-global}

### Versand {#delivery-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_delivery_global"
>title="Kampagnenstatistiken"
>abstract="Das Statistik-Widget von Campaign enthält die wichtigsten Informationen zu Ihrer Kampagne, wie z. B. eingegebene Profile und durchgeführte Aktionen."

![](assets/campaign_report_global_1.png)

Die KPIs zu den **[!UICONTROL Kampagnenstatistiken]** dienen als umfassendes Dashboard, das eine detaillierte Aufschlüsselung der Schlüsselmetriken für Ihre Kampagne bietet. Dazu gehören wichtige Informationen wie die Anzahl der Profile und die durchgeführten Aktionen, die einen umfassenden Einblick in die Leistung und das Engagement Ihrer Kampagne ermöglichen.

+++ Erfahren Sie mehr über Kampagnenstatistik-Metriken.

* **[!UICONTROL Zielgruppe]**: Anzahl der Zielgruppenprofile.

* **[!UICONTROL Bereitgestellte Aktionen]**: Gesamtzahl der eindeutigen Fälle, in denen eine Aktion ausgeführt wurde.

* **[!UICONTROL Fehlgeschlagene Aktionen in %]**: Gesamtzahl der eindeutigen Fälle, in denen eine Aktion fehlgeschlagen ist, verglichen mit der Gesamtzahl der eindeutigen Fälle, in denen eine Aktion erfolgreich ausgeführt wurde.

+++

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

Die Registerkarte **[!UICONTROL Experimentieren]** bietet wichtige Einblicke in die Performance der einzelnen Varianten und ermittelt die erfolgreichste Variante.

Beachten Sie, dass es ein wenig dauern kann, um die beste Leistung zu ermitteln. Sie wird durch das Symbol ![](assets/experimentation_report_1.png) gekennzeichnet.

+++Erfahren Sie mehr über die verschiedenen Kennzahlen und Widgets, die für den Experimentierbericht verfügbar sind.

Die Widget **[!UICONTROL Experimentergebnis]** liefert Details zur Performance der einzelnen Varianten. Sie können Ihre Baseline ändern, indem Sie eine der Abwandlungen aus der Dropdown-Liste **[!UICONTROL Baseline]** auswählen. Die beste Abwandlung wird mit einem Sternsymbol gekennzeichnet.

Einen tiefen Einblick in diese Ergebnisse und ihre Interpretation finden Sie auf [dieser Seite](../campaigns/get-started-experiment.md#interpret-results).

Die Tabelle enthält die folgenden Metriken:

* **[!UICONTROL Steigerung über die Baseline]**: Messung der prozentualen Verbesserung der Konversionsrate einer bestimmten Abwandlung im Vergleich zur Baseline.

* **[!UICONTROL Konfidenz]**: Belege dafür, dass eine bestimmte Abwandlung mit der Baseline-Abwandlung identisch ist. [Weitere Informationen](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Ausgehende Einzelklicks]**: Gesamtanzahl der Klicks in allen ausgehenden Kanälen.

* **[!UICONTROL Profile]**: Anzahl der für diese Abwandlung ausgewählten Profile.

* **[!UICONTROL Eindeutige ausgehende Klicks/Profile]**: Gesamtwert der Erfolgskennzahl, die zuvor beim Erstellen der Experimente ausgewählt wurde, dividiert durch die Anzahl der Profile.

Der Graph **[!UICONTROL Konfidenzintervall]** misst die Unsicherheit im Zusammenhang mit Verbesserungen. Er beschreibt den prozentualen Performance-Unterschied zwischen der Baseline und der Abwandlung mit der besten Performance. [Weitere Informationen](../campaigns/experiment-calculations.md#confidence-intervals).

![](assets/experimentation_report_4.png)

Das letzte Widget stellt Daten mit Bezug zu der **[!UICONTROL Erfolgsmetrik]** bereit, die Sie zuvor für Ihre Abwandlungen ausgewählt haben. Sie haben die Möglichkeit, eine andere Zielmetrik aus dem Dropdown-Menü **[!UICONTROL Metrik]** auszuwählen, um alternative Daten zu verfolgen.

>[!CAUTION]
>
>Beachten Sie bei der Arbeit mit experimentierungsgefilterten Metriken, dass beim Ändern der Metrikauswahl in der Dropdown-Liste auf der Vergleichsseite für die Experimentierung der Filterwert nicht beibehalten wird. Wenn Sie beispielsweise von „Klicks“ zu „Einzelklicks“ wechseln, geht der angewendete Filter verloren, was den Vergleich ungenau oder ungültig macht.

+++

## Registerkarte „E-Mail“ {#email-global}

### E-Mail – Versandstatistiken {#sending-statistics-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_statistics"
>title="E-Mail – Versandstatistiken"
>abstract="Die Tabelle „E-Mail – Versandstatistik“ enthält wichtige Daten zu Ihrem E-Mail-Kanal, z. B. „Angesprochen“ oder „Zugestellt“."

![](assets/campaign_email_sending.png)

Die Tabelle **[!UICONTROL Statistiken zum E-Mail-Versand]** bietet eine umfassende Zusammenfassung der wichtigsten Daten zu Ihren E-Mail-Kampagnen. Sie enthält Schlüsselmetriken wie die Größe der Zielgruppe und die Anzahl der erfolgreich zugestellten E-Mails und bietet wertvolle Einblicke in die Effektivität und Reichweite Ihrer E-Mails.

+++ Weitere Informationen zu Metriken für die E-Mail-Versandstatistiken

* **[!UICONTROL Zielgruppe]**: Gesamtzahl der während des Sendevorgangs verarbeiteten E-Mails.

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge für Ihre E-Mail.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten E-Mails in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Versandrate]**: Prozentsatz der erfolgreich gesendeten E-Mails.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der E-Mails, die nicht erfolgreich zugestellt wurden, im Vergleich zur Zahl der gesendeten E-Mails.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

* **[!UICONTROL Fehlerrate]**: Prozentsatz der Fehler, die während des Versandvorgangs auftraten und die Zustellung verhinderten, im Vergleich zur Zahl der gesendeten E-Mails.

* **[!UICONTROL Weitere Zustellversuche]**: Anzahl der E-Mails in der Warteschlange für weitere Zustellversuche.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

+++

### E-Mail – Tracking-Statistiken {#tracking-statistics-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_tracking_statistics"
>title="E-Mail – Tracking-Statistiken"
>abstract="Die Tabelle „E-Mail – Tracking-Statistik“ enthält Daten zur Profilaktivität für Ihre E-Mail."

![](assets/campaign_email_tracking.png)

Die Tabelle **[!UICONTROL E-Mail – Tracking-Statistiken]** bietet eine detaillierte Übersicht über die Profilaktivitäten im Zusammenhang mit Ihren E-Mail-Kampagnen. Dazu gehören Metriken zu Öffnungen, Klicks und andere relevante Interaktionsindikatoren, die einen umfassenden Überblick darüber bieten, wie Profile mit Ihrem E-Mail-Inhalt interagieren.

+++ Weitere Informationen über E-Mails – Metriken zu Tracking-Statistiken

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen der E-Mail.

* **[!UICONTROL Eindeutige Öffnungen]**: Prozentsatz der geöffneten E-Mails.

* **[!UICONTROL Öffnungsrate]**: Gesamtzahl der geöffneten E-Mails im Vergleich zu den versendeten E-Mails.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in Ihren E-Mails.

* **[!UICONTROL Einzelklicks]**: Die Anzahl der Profile, die auf einen Inhalt in einer E-Mail geklickt haben.

* **[!UICONTROL Rate von Einzelklicks]**: Prozentsatz der Benutzenden, die mit Ihren E-Mails interagiert haben.

* **[!UICONTROL Abmeldungen]**: Zahl der Klicks auf den Abmelde-Link.

* **[!UICONTROL Beschwerden wegen Spam]**: Gibt an, wie oft eine Nachricht als Spam oder Junk gekennzeichnet wurde.

+++

### E-Mail – Versandleistung {#sending-performance-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_performance"
>title="E-Mail – Versandleistung"
>abstract="Der Graph „E-Mail – Versandleistung“ enthält umfassende Daten zu gesendeten E-Mails und bietet Einblicke in Schlüsselmetriken wie zugestellte Nachrichten und Bounces, sodass eine detaillierte Analyse des E-Mail-Versandprozesses möglich ist."

![](assets/campaign_email_sending_performance.png)

Der Graph **[!UICONTROL E-Mail – Versandleistung]** bietet einen umfassenden Überblick über die Daten zu gesendeten E-Mails und bietet Einblicke in Schlüsselmetriken wie zugestellte Nachrichten und Bounces. Dies ermöglicht eine detaillierte Analyse des E-Mail-Sendevorgangs und liefert wertvolle Informationen über die Effizienz und Leistung Ihrer E-Mail-Kampagnen.

+++ Weitere Informationen zu Metriken von „E-Mail – Versandleistung“

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten E-Mails im Verhältnis zur Gesamtzahl der gesendeten E-Mails.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen im Verhältnis zur Gesamtzahl der gesendeten E-Mails.

* **[!UICONTROL Weitere Zustellversuche]**: Anzahl der E-Mails in der Warteschlange für weitere Zustellversuche.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Versandvorgangs aufgetretenen Fehler, die den Versand an Profile verhindert haben.

+++

### E-Mail – Bounce-Gründe und -Kategorien {#bounces-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_categories"
>title="E-Mail – Bounce-Kategorien"
>abstract="Die Graphen und die Tabelle „E-Mail – Bounce-Kategorien“ bieten Daten zu temporären und permanenten Fehlern."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_reasons"
>title="E-Mail – Bounce-Gründe"
>abstract="Die Graphen und die Tabelle „E-Mail – Ausschlussgründe“ enthalten die für Bounce-Nachrichten verfügbare Daten."

![](assets/campaign_email_bounces.png)

Die Widgets **[!UICONTROL E-Mail – Bounce-Gründe]** und **[!UICONTROL E-Mail – Bounce-Kategorien]** kompilieren die verfügbaren Daten zu unzustellbaren Nachrichten und bieten detaillierte Einblicke in die Gründe und Kategorien, die E-Mail-Bounces zugrunde liegen.

Weitere Informationen zu Bounces finden Sie auf der Seite [ Unterdrückungslisten](../reports/suppression-list.md).

+++ Weitere Informationen zu den Metriken von E-Mail-Bounce-Kategorien

* **[!UICONTROL Hardbounce]**: die Gesamtzahl der permanenten Fehler, wie eine falsche E-Mail-Adresse. Dazu gehören Fehlermeldungen, die explizit eine ungültige Adresse anzeigen, wie etwa „Benutzer unbekannt“.

* **[!UICONTROL Softbounce]**: die Gesamtzahl der temporären Fehler, wie ein voller Posteingang.

* **[!UICONTROL Ignoriert]**: Die Gesamtzahl der temporären Ereignisse, beispielsweise Abwesenheit, oder technischer Fehler, zum Beispiel wenn der Absendertyp Postmaster ist.

+++


### E-Mail – Fehlergründe {#errors-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_error_reasons"
>title="E-Mail – Fehlergründe"
>abstract="Anhand der Graphen und der Tabelle „E-Mail – Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs aufgetreten sind."

![](assets/campaign_email_error_reasons.png)

Die Graphen und die Tabelle **[!UICONTROL Fehlergründe]** bieten einen detaillierten Überblick über die Fehler, die während des Sendevorgangs aufgetreten sind, mit wichtigen Informationen über Art und Auftreten von Fehlern.

Sie können zwischen Tabellen, Balkendiagrammen und Ringdiagrammen wechseln.

### E-Mail – Gründe für Ausschluss {#excluded-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_excluded_reasons"
>title="E-Mail – Gründe für Ausschluss"
>abstract="Die Graphen und die Tabelle „Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu führten, dass Benutzerprofile aus der Zielgruppe ausgeschlossen wurden und die Nachricht nicht erhielten."

![](assets/campaign_email_excluded.png)

Die Graphen und die Tabelle **[!UICONTROL Gründe für Ausschluss]** bieten einen umfassenden Überblick über die verschiedenen Faktoren, die zum Ausschluss von Nutzerprofilen aus der Zielgruppe geführt haben, sodass die Nachricht nicht empfangen wurde.

Auf [dieser Seite](exclusion-list.md) finden Sie eine umfassende Liste der Ausschlussgründe.

### Gesendet und zugestellt nach Domains {#sent-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sent_domains"
>title="Gesendet und zugestellt nach Domains"
>abstract="Die Tabelle Gesendet und zugestellt nach Domains liefert eine Aufschlüsselung der E-Mails, die nach Domains kategorisiert sind, und bietet umfassende Einblicke in die Gesamtleistung Ihrer E-Mail-Kommunikation."

![](assets/campaign_email_sent_domains.png)

Die **[!UICONTROL Gesendet und von Domänen bereitgestellt]** Tabellen und Diagramme enthalten eine detaillierte Aufschlüsselung der E-Mails auf Domänenebene und bieten umfassende Einblicke in die Leistung Ihrer E-Mails.

+++ Weitere Informationen zu den Metriken zu „Gesendet und zugestellt nach Domains“

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge für Ihre E-Mail.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten E-Mails im Verhältnis zur Gesamtzahl der gesendeten E-Mails.

+++

### Bounces und Fehler nach Domains {#bounces-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounces_domains"
>title="Bounces und Fehler nach Domains"
>abstract="Das Diagramm und die Tabelle &quot;Bounces &amp; Fehler nach Domänen&quot;bieten eine granulare Aufschlüsselung auf Domänenebene und bieten Einblicke in spezifische Fehler, die beim E-Mail-Versand aufgetreten sind."

![](assets/campaign_email_bounce_domains.png)

Die **[!UICONTROL Bounces und Fehler nach Domänen]** Diagramm und Tabelle bieten eine Aufschlüsselung der spezifischen Fehler, die während des Versandvorgangs auf Domänenebene aufgetreten sind, und enthalten eine detaillierte Analyse der aufgetretenen Probleme.

+++ Weitere Informationen zu den Metriken zu „Bounces und Fehler nach Domains“

* **[!UICONTROL Bounces]**: Gesamtanzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen im Verhältnis zur Gesamtanzahl der gesendeten E-Mails

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Sendevorgangs aufgetreten sind und das Senden Ihrer E-Mails an Profile verhindert haben.

+++

### Öffnungen und Klicks nach Domains {#opens-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_open_domains"
>title="Öffnungen und Klicks nach Domains"
>abstract="Das Diagramm &quot;Öffnungen und Klicks nach Domänen&quot;und die Tabelle bieten eine detaillierte Aufschlüsselung auf Domänenebene, die einen umfassenden Überblick darüber bietet, wie Ihre Zielgruppe mit Ihren E-Mails interagiert."

![](assets/campaign_email_open_domains.png)

Die **[!UICONTROL Öffnungen und Klicks nach Domänen]** Diagramm und Tabelle zeigen eine Aufschlüsselung der Interaktion Ihrer Profile mit Ihrer E-Mail auf Domänenebene, die wertvolle Einblicke in die Interaktion verschiedener Domänen mit Ihrem Inhalt bietet.

+++ Weitere Informationen zu den Metriken zu „Öffnungen und Klicks nach Domains“

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen der E-Mail.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf Inhalte in einer E-Mail

+++

### Bounce-Gründe nach Domain {#bounce-reasons-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounces_reasons_domains"
>title="Bounce-Gründe nach Domain"
>abstract="Die Absprunggründe nach Domänendiagramm und Tabelle bieten eine Aufschlüsselung auf Domänenebene, die umfassende Einblicke in temporäre und permanente Fehler bietet. Diese detaillierte Analyse liefert Ihnen wertvolle Informationen über die spezifischen Gründe für nicht zugestellte Nachrichten."

![](assets/campaign_email_bounce_reasons_domains.png)

Die **[!UICONTROL Bounce-Gründe nach Domain]** Diagramme und Tabellen bieten eine Aufschlüsselung der Daten auf Domänenebene bezüglich temporärer und permanenter Fehler und bieten detaillierte Einblicke in die Ursachen für abgespeckte Nachrichten.

+++ Weitere Informationen zu Bounce-Gründen nach Domain-Metriken

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen der E-Mail.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf Inhalte in einer E-Mail.

+++

### E-Mail – Top-URL {#top-url-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_top_url"
>title="E-Mail – Top-URL"
>abstract="Der Graph und die Tabelle „E-Mail – Beste URL“ bieten einen umfassenden Überblick über die URLs in Ihrer E-Mail, die den höchsten Besucher-Traffic erhalten, sodass Sie die beliebtesten Links identifizieren können."

![](assets/campaign_email_topurl.png)

Der Graph und die Tabelle **[!UICONTROL E-Mail – Top-URL]** bieten einen umfassenden Überblick über die URLs in Ihren E-Mails, die den meisten Besucher-Traffic anziehen. Auf diese Weise können Sie die beliebtesten Links identifizieren und priorisieren und Ihr Verständnis der Profilinteraktion mit bestimmten Inhalten in Ihren E-Mails verbessern.

### E-Mail – beste Empfänger-Domain {#top-recipient-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_best_recipient"
>title="E-Mail – beste Empfänger-Domain"
>abstract="Der Graph und die Tabelle „E-Mail – Beste Empfänger-Domain“ enthalten eine detaillierte Aufschlüsselung der Domains, die die Empfängerinnen und Empfänger am häufigsten zum Öffnen der E-Mail verwenden, und bieten wertvolle Einblicke in das Empfängerverhalten."

![](assets/campaign_email_best_recipient.png)

>[!CAUTION]
>
> Das Widget **[!UICONTROL E-Mail – beste Empfänger-Domain]** weist eine Genauigkeit von 99,95 % auf.

Der Graph und die Tabelle **[!UICONTROL E-Mail – beste Empfänger-Domain]** bieten eine detaillierte Aufschlüsselung der Domains, die Profile am häufigsten zum Öffnen Ihrer E-Mails verwenden. Dies bietet wertvolle Informationen in das Profilverhalten und darüber, welches die bevorzugten Plattformen sind.

+++ Weitere Informationen zu Metriken für „E-Mail – beste Empfänger-Domain“

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten E-Mails im Verhältnis zur Gesamtzahl der gesendeten E-Mails.

* **[!UICONTROL Versandrate]**: Prozentsatz der erfolgreich gesendeten E-Mails.

* **[!UICONTROL Bounce- und Fehlerrate]**: Prozentsatz der E-Mails, die nicht erfolgreich zugestellt wurden, im Vergleich zur Zahl der gesendeten E-Mails.

+++

### E-Mail – Optimierung {#optimized-email}

![](assets/campaign_email_optimized.png)

>[!NOTE]
>
>Die **[!UICONTROL Optimiert vs. nicht optimiert]** und **[!UICONTROL Versandzeitoptimierung]** Widgets sind nur verfügbar, wenn die Option Sendezeitoptimierung für Ihre E-Mail aktiviert ist. Weitere Informationen zur Sendezeitoptimierung finden Sie auf [dieser Seite](../building-journeys/journeys-message.md#send-time-optimization).

Die Widgets **[!UICONTROL Optimiert vs. nicht optimiert]** und **[!UICONTROL Versandzeitoptimierung]** enthalten die wichtigsten Informationen zu Ihrer Nachricht, unabhängig davon, ob sie optimiert ist oder nicht.

+++ Weitere Informationen zu Versandzeitoptimierungsmetriken

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge.

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen der Nachricht.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf Inhalt einer E-Mail.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Vergleich zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Versandvorgang und der automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten Nachrichten.

+++

### E-Mail – Angebote {#email-offers}

![](assets/campaign_email_offers.png)

Die Widgets **[!UICONTROL Angebotsstatistik]**, **[!UICONTROL Angebotsstatistik im Zeitverlauf]** und **[!UICONTROL Detaillierte Angebotsstatistik]** messen den Erfolg Ihres Angebots und die Wirkung auf Ihre Zielgruppe.

+++ Weitere Informationen über E-Mails – Angebotsmetriken

* **[!UICONTROL Gesendete Angebote]**: Gibt an, wie oft das Angebot gesendet wurde.

* **[!UICONTROL Angebots-Impression]**: Gibt an, wie oft das Angebot in Ihren E-Mails geöffnet wurde.

* **[!UICONTROL Angebots-Klicks]**: Gibt an, wie oft ein Angebot in Ihren E-Mails angeklickt wurde.

* **[!UICONTROL Platzierungsname]**: Name der Platzierung, die zur Anzeige Ihres Angebots verwendet wird. Weiterführende Informationen zu Platzierungen finden Sie auf dieser [Seite](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Angebotsname]**: Name des im Versand hinzugefügten Angebots. Weiterführende Informationen zu Platzierungen finden Sie auf dieser [Seite](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Angebot versendet]**: Gibt an, wie oft das Angebot insgesamt versendet wurde.

* **[!UICONTROL Impressionsrate des Angebots]**: Prozentsatz der geöffneten Angebote im Verhältnis zur Anzahl der gesendeten Angebote.

+++

## Registerkarte „In-App“ {#inapp-global}

Im **[!UICONTROL globalen Bericht]** Ihrer Kampagne finden Sie auf der Registerkarte **[!UICONTROL In-App]** die wichtigsten Informationen zu den In-App-Nachrichten, die im Rahmen Ihrer Kampagne gesendet wurden.

### In-App-Leistung {#in-app-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_performance"
>title="In-App-Leistung"
>abstract="Die KPIs zur In-App-Leistung bieten wichtige Einblicke in die Interaktion Ihrer Besuchenden mit In-App-Nachrichten."

![](assets/campaign_inapp_performance.png)

Die KPIs zur **[!UICONTROL In-App-Leistung]** bieten wichtige Einblicke in die Interaktion Ihrer Besucherinnen und Besucher mit In-App-Nachrichten und liefern wichtige Metriken, mit denen Sie die Effektivität und Wirkung Ihrer In-App-Kampagnen bewerten können.

+++ Weitere Informationen zu In-App-Leistungsmetriken

* **[!UICONTROL Eindeutige Impressions]**: Anzahl der eindeutigen Nutzer, an die die In-App-Nachricht gesendet wurde.

* **[!UICONTROL Impressions]**: Gesamtzahl der an alle Benutzerinnen und Benutzer gesendeten In-App-Nachrichten.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit Ihrer In-App-Nachricht. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks, Abbrüche oder andere Interaktionen.

+++

### Interaktionen nach Typ {#interactions-type}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_interactions"
>title="Interaktionen nach Typ"
>abstract="Der Graph und die Tabelle „Interaktionen nach Typ“ beschreiben, wie Benutzende mit Ihrer In-App-Nachricht interagiert haben, indem Klicks, Abbrechen oder Interaktionen verfolgt werden."

![](assets/campaign_inapp_interactions.png)

Die Graphen und die Tabelle **[!UICONTROL Interaktionen nach Typ]** bieten einen detaillierten Überblick darüber, wie Profile mit Ihrer In-App-Nachricht interagiert haben, indem sie Aktionen wie Klicks, Abbrüche oder andere Formen der Interaktion verfolgen.

### In-App-Zusammenfassung {#in-app-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_summary"
>title="In-App-Zusammenfassung"
>abstract="Der Graph „In-App – Zusammenfassung“ zeigt die Entwicklung Ihrer In-App-Impressions und -Interaktionen für den jeweiligen Zeitraum an."

![](assets/campaign_inapp_summary.png)

Die **[!UICONTROL In-App-Zusammenfassung]** veranschaulicht die Entwicklung Ihrer In-App-Impressions und -Interaktionen über den angegebenen Zeitraum und bietet einen umfassenden Überblick über die Leistung Ihrer In-App-Nachrichten.

+++ Weitere Informationen zu In-App-Zusammenfassungsmetriken

* **[!UICONTROL Eindeutige Impressions]**: Anzahl der eindeutigen Nutzer, an die die In-App-Nachricht gesendet wurde.

* **[!UICONTROL Impressions]**: Gesamtzahl der an alle Benutzerinnen und Benutzer gesendeten In-App-Nachrichten.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit Ihrer In-App-Nachricht. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks, Abbrüche oder andere Interaktionen.

+++

## Registerkarte „Push-Benachrichtigung“ {#push-global}

Im **[!UICONTROL globalen Bericht]** Ihrer Kampagne finden Sie auf der Registerkarte **[!UICONTROL Push-Benachrichtigung]** die wichtigsten Informationen zu den im Rahmen Ihrer Kampagne gesendeten Push-Benachrichtigungen.

### Push-Benachrichtigung – Sendestatistik {#push-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_statistics"
>title="Push-Benachrichtigung – Sendestatistik"
>abstract="Die Tabelle „Push-Benachrichtigung – Sendestatistik“ fasst wesentliche Daten über Ihre Push-Benachrichtigungen zusammen, z. B. „Angesprochen“ oder „Zugestellte Nachrichten“."

![](assets/campaign_push_sending.png)

Die Tabelle **[!UICONTROL Push-Benachrichtigung – Sendestatistik]** bietet eine übersichtliche Zusammenfassung der wichtigsten Daten zu Ihren Push-Benachrichtigungen, einschließlich wichtiger Schlüsselmetriken wie der Anzahl der gezielten Nachrichten und der Anzahl der erfolgreich zugestellten Nachrichten.

+++ Weitere Informationen zu Metriken für „Push-Benachrichtigungen – Versandstatistiken“

* **[!UICONTROL Ausführungszeit]**: Startzeit jeder Ausführung Ihrer wiederkehrenden Push-Benachrichtigung. Um nur eine oder mehrere wiederkehrende Push-Benachrichtigungen als Ziel auszuwählen, wählen Sie diese aus der Dropdown-Liste **[!UICONTROL Ausführungszeit]**.

* **[!UICONTROL Zielgruppe]**: Gesamtzahl der während der Analyse verarbeiteten Push-Benachrichtigungen.

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge für die Push-Benachrichtigung.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Push-Benachrichtigungen in Bezug auf die Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Versandrate]**: Prozentsatz der erfolgreich gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen im Verhältnis zur Gesamtzahl der gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der Push-Benachrichtigungen, die unzustellbar waren, im Vergleich zu den gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die die Zustellung an Profile verhindert haben.

* **[!UICONTROL Fehlerrate]**: Prozentualer Anteil der während des Versandvorgangs aufgetretenen Fehler, die den Versand verhindert haben, im Vergleich zu den gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

+++

### Push-Benachrichtigung – Tracking-Statistiken {#push-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_tracking_statistics"
>title="Push-Benachrichtigung – Tracking-Statistiken"
>abstract="Die Tracking-Statistik für Push-Benachrichtigungen bietet Daten zur Profilaktivität für Ihre Push-Benachrichtigung."

![](assets/campaign_push_tracking.png)

Das Widget **[!UICONTROL Push-Benachrichtigung – Tracking-Statistiken]** bietet einen detaillierten Überblick über die Profilaktivitäten, die mit Ihren Push-Benachrichtigungen verbunden sind, und liefert wichtige Erkenntnisse über Interaktion und Effektivität von Push-Benachrichtigungen.

+++ Weitere Informationen zu Metriken für „Push-Benachrichtigungen – Tracking-Statistiken“

* **[!UICONTROL Ausführungszeit]**: Startzeit jeder Ausführung Ihrer wiederkehrenden Push-Benachrichtigung. Um nur eine oder mehrere wiederkehrende Push-Benachrichtigungen als Ziel auszuwählen, wählen Sie diese aus der Dropdown-Liste **[!UICONTROL Ausführungszeit]**.

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft Ihre Push-Benachrichtigung geöffnet wurde.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf eine Schaltfläche oder Abbruch.

+++

### Push-Benachrichtigung – Sendezusammenfassung {#push-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_summary"
>title="Push-Benachrichtigung – Sendezusammenfassung"
>abstract="Der Graph „Push-Benachrichtigung – Sendezusammenfassung“ zeigt die Daten an, die für gesendete Push-Benachrichtigungen verfügbar sind."

![](assets/campaign_push_sending_summary.png)

Das Diagramm **[!UICONTROL Push-Benachrichtigung – Sendezusammenfassung]** bietet eine dynamische Darstellung, die eine Analyse Ihrer Push-Benachrichtigungsaktivitäten anzeigt. Diese grafische Darstellung bietet eine umfassende Aufschlüsselung gesendeter Push-Benachrichtigungen.

+++ Weitere Informationen zu Push-Benachrichtigungen – Metriken zur Sendezusammenfassung

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft Ihre Push-Benachrichtigung geöffnet wurde.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf Schaltfläche oder Abbruch.

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler und automatischen Rücksendeverarbeitungen im Verhältnis zur Gesamtzahl der gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Push-Benachrichtigungen im Verhältnis zur Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die das Senden an Profile verhindert haben.

+++

### Push-Benachrichtigungen – Optimierung {#push-optimized}

>[!NOTE]
>
>Die **[!UICONTROL Optimiert vs. nicht optimiert]** und **[!UICONTROL Versandzeitoptimierung]** -Widgets sind nur verfügbar, wenn die Option Sendezeitoptimierung für Ihre Push-Benachrichtigung aktiviert ist. Weitere Informationen zur Sendezeitoptimierung finden Sie auf [dieser Seite](../building-journeys/journeys-message.md#send-time-optimization).

Die Widgets **[!UICONTROL Optimiert vs. nicht optimiert]** und **[!UICONTROL Versandzeitoptimierung]** enthalten die wichtigsten Informationen zu Ihrer Nachricht, unabhängig davon, ob sie optimiert ist oder nicht.

+++ Weitere Informationen zu Push-Benachrichtigungen – Optimierungsmetriken zur Versandzeitoptimierung

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Push-Benachrichtigungen im Verhältnis zur Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft Ihre Push-Benachrichtigung geöffnet wurde.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf eine Schaltfläche oder Abbruch.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen im Verhältnis zur Gesamtzahl der gesendeten Push-Benachrichtigungen.

+++

### Push-Benachrichtigung – Fehlergründe {#error-reasons-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_error_reasons"
>title="Push-Benachrichtigung – Fehlergründe"
>abstract="Anhand der Graphen und der Tabelle „Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs aufgetreten sind."

![](assets/campaign_push_error_reasons.png)

Die Tabelle und die Diagramme **[!UICONTROL Fehlergründe]** bieten Ihnen die Möglichkeit, die spezifischen Fehler zu identifizieren, die während des Sendevorgangs Ihrer Push-Benachrichtigungen aufgetreten sind, und geben Ihnen einen detaillierten Einblick in die dabei aufgetretenen Probleme.

### Push-Benachrichtigung – Gründe für Ausschluss {#excluded-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_excluded_reasons"
>title="Push-Benachrichtigung – Gründe für Ausschluss"
>abstract="Die Graphen und die Tabelle „Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu führten, dass Benutzerprofile aus der Zielgruppe ausgeschlossen wurden und die Nachricht nicht erhielten."

![](assets/campaign_push_excluded.png)

Die Graphen und die Tabelle **[!UICONTROL Gründe für Ausschluss]** zeigen die verschiedenen Gründe an, die verhindert haben, dass Nutzerprofile, die von den Zielprofilen ausgeschlossen wurden, die Push-Benachrichtigungen erhalten haben.

Auf [dieser Seite](exclusion-list.md) finden Sie die umfassende Liste der Ausschlussgründe.

### Push-Benachrichtigung – Aufschlüsselung nach Plattform {#breakdown-platform-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_breakdown_platform"
>title="Push-Benachrichtigung – Aufschlüsselung nach Plattform"
>abstract="Die Tabelle Push-Benachrichtigung - Aufschlüsselung nach Platform-Diagrammen und -Tabellen enthält eine Aufschlüsselung des Erfolgs Ihrer Push-Benachrichtigungen nach dem Betriebssystem des Profils."

![](assets/campaign_push_breakdown.png)

Der Graph und die Tabelle **[!UICONTROL Push-Benachrichtigung – Aufschlüsselung nach Plattform]** liefern eine detaillierte Analyse des Erfolgs Ihrer Push-Benachrichtigungen und bieten Einblicke auf der Grundlage des Betriebssystems Ihres Profils. Diese Aufschlüsselung verbessert Ihr Verständnis der Leistung Ihrer Push-Benachrichtigungen auf verschiedenen Plattformen.

+++ Weitere Informationen zu Push-Benachrichtigungen – Aufschlüsselung nach Plattformmetriken

* **[!UICONTROL Zielgruppe]**: Gesamtzahl der bei der Analyse verarbeiteten Push-Benachrichtigungen.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Push-Benachrichtigungen im Verhältnis zur Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft Ihre Push-Benachrichtigung geöffnet wurde.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf Schaltfläche oder Abbruch.

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler und automatischen Rücksendeverarbeitungen im Verhältnis zur Gesamtzahl der gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die das Senden an Profile verhindert haben.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

+++

## Registerkarte „SMS“ {#sms-global}

Im **[!UICONTROL globalen Bericht]** Ihrer Kampagne finden Sie auf der Registerkarte **[!UICONTROL SMS]** die wichtigsten Informationen zu den in Ihrer Kampagne versendeten Push-Benachrichtigungen.

### SMS – Sendestatistik {#sms-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_sending_statistics"
>title="SMS – Sendestatistik"
>abstract="Die Tabelle SMS - Versandstatistiken enthält eine Zusammenfassung der wichtigsten Daten zu Ihren SMS-Nachrichten, z. B. Zielgerichtete oder zugestellte Nachrichten."

![](assets/campaign_sms_sending.png)

Die Tabelle **[!UICONTROL SMS – Versandstatistiken]** bietet eine kurze Zusammenfassung wichtiger Daten zu Ihren SMS-Nachrichten und umfasst wichtige Metriken wie die Anzahl der gezielten Nachrichten und die Anzahl der erfolgreich zugestellten Nachrichten.

+++ Weitere Informationen zu Metriken für „SMS – Versandstatistiken“

* **[!UICONTROL Ausführungszeit]**: Startzeit jeder Ausführung Ihrer wiederkehrenden SMS-Nachricht. Um nur eine oder mehrere wiederkehrende SMS-Nachrichten auszuwählen, wählen Sie die gewünschte Option in der Dropdown-Liste **[!UICONTROL Ausführungszeit]** aus.

* **[!UICONTROL Angesprochen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für diesen Versand eignen.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge für Ihre SMS-Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die das Senden an Profile verhindert haben.

+++

### SMS – Tracking-Statistiken {#sms-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_sms_tracking_statistics"
>title="SMS – Tracking-Statistiken"
>abstract="Das Widget SMS - Trackingstatistiken bietet einen umfassenden Überblick über die wichtigsten Informationen zur Interaktion Ihrer Besucher mit Ihrer URL."

![](assets/campaign_sms_tracking.png)

Das Widget **[!UICONTROL SMS – Tracking-Statistiken]** bietet einen detaillierten Überblick über die wichtigsten Informationen in Bezug auf die Interaktion Ihrer Besucherinnen und Besucher mit Ihren URLs und gibt Aufschluss über die Effektivität Ihrer SMS-Nachrichten.

+++ Weitere Informationen zu Metriken für „SMS – Tracking-Statistik“

* **[!UICONTROL Ausführungszeit]**: Startzeit jeder Ausführung Ihrer wiederkehrenden SMS. Um nur eine oder mehrere wiederkehrende SMS festzulegen, wählen Sie sie die gewünschte Option in der Dropdown-Liste **[!UICONTROL Ausführungszeit]**.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in einer SMS-Nachricht.

+++

### SMS – Leistung nach Datum {#sms-perfomance-date}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_performance"
>title="SMS – Leistung nach Datum"
>abstract="Das Widget - SMS-Leistung nach Datum liefert wichtige Informationen über Ihre Nachrichten in einer grafischen Darstellung."

![](assets/campaign_sms_performance.png)

Das Widget **[!UICONTROL SMS-Leistung nach Datum]** bietet einen detaillierten Überblick über die wichtigsten Informationen zu Ihren Nachrichten, die in einem Diagramm dargestellt werden und einen Einblick in die Leistungs-Trends über bestimmte Zeiträume geben.

+++ Weitere Informationen zu SMS – Metriken zur Leistung nach Datum

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge für Ihre SMS-Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die das Senden an Profile verhindert haben.

+++

### SMS – Fehlergründe {#sms-error}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_error_reasons"
>title="SMS – Fehlergründe"
>abstract="Anhand der Graphen und der Tabelle „SMS – Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs aufgetreten sind."

![](assets/campaign_sms_error_reasons.png)

Anhand der Graphen und der Tabelle **[!UICONTROL Fehlergründe]** können Sie die Fehler genau identifizieren, die während des Sendevorgangs Ihrer SMS-Nachrichten aufgetreten sind. Dies ermöglicht eine gründliche Analyse aller aufgetretenen Probleme.

### SMS – Gründe für Ausschluss {#sms-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_excluded_reasons"
>title="SMS – Gründe für Ausschluss"
>abstract="Die Graphen und die Tabelle „Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu führten, dass Benutzerprofile aus der Zielgruppe ausgeschlossen wurden und die Nachricht nicht erhielten."

![](assets/campaign_sms_excluded.png)

Die Graphen und die Tabelle **[!UICONTROL Gründe für Ausschluss]** zeigen visuell die verschiedenen Faktoren an, die zum Ausschluss von Benutzerprofilen aus der Zielgruppe geführt haben, sodass diese keine SMS-Nachrichten erhalten konnten.

Auf [dieser Seite](exclusion-list.md) finden Sie die umfassende Liste der Ausschlussgründe.

### SMS – Bounce-Gründe {#sms-bounces-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_bounces_reasons"
>title="SMS – Bounce-Gründe"
>abstract="Die Graphen und die Tabelle „Bounce-Gründe“ enthalten die verfügbaren Daten zu Bounce-Nachrichten."

Die Graphen und die Tabelle **[!UICONTROL Bounce-Gründe]** bieten einen detaillierten Überblick über Daten zu nicht zugestellten SMS-Nachrichten und liefern wertvolle Einblicke in die spezifischen Gründe für SMS-Bounces.

### SMS – Klicks nach Links {#sms-clicks-links}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_clicks_links"
>title="SMS – Klicks nach Links"
>abstract="Das Widget SMS - Klicks nach Links bietet wichtige Einblicke in die Interaktion Ihrer Besucher mit den URLs in Ihren Nachrichten."

![](assets/campaign_sms_clicks.png)

Das Widget **[!UICONTROL SMS – Klicks nach Links]** bietet wichtige Einblicke in die Interaktion Ihrer Besucherinnen und Besucher mit den in Ihren Nachrichten enthaltenen URLs und liefert wertvolle Informationen darüber, welche Links die meisten Interaktionen hervorrufen.

## Registerkarte „Web“ {#web-tab}

Im **[!UICONTROL globalen Bericht]** Ihrer Kampagne werden in der Registerkarte **[!UICONTROL Web]** die wichtigsten Informationen zu Ihren Web-Seiten aufgeführt.

### Web-Performance {#web-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_performance"
>title="Web-Performance"
>abstract="Die Web-Performance-KPIs bieten umfassende Informationen über die Interaktion Ihrer Besucherinnen und Besucher mit Ihren Web-Erlebnissen."

![](assets/campaign_web_performance.png)

Die KPIs zur **[!UICONTROL Web-Performance]** liefern umfassende Informationen über die Interaktion Ihrer Besucherinnen und Besucher mit Ihren Web-Seiten, einschließlich Schlüsselmetriken wie „Impressions“ und „Interaktionen“.

+++ Weitere Informationen über Web-Performance-Metriken

* **[!UICONTROL Eindeutige Impressions]**: Anzahl der eindeutigen Benutzer, denen das Web-Erlebnis bereitgestellt wurde.

* **[!UICONTROL Impressions]**: Gesamtanzahl der für alle Benutzer bereitgestellten Web-Erlebnisse.

* **[!UICONTROL Interaktionsrate]**: Prozentsatz der Interaktionen mit Ihrer Web-Seite. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks oder andere Interaktionen.

+++

### Web-Zusammenfassung {#web-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_summary"
>title="Web-Zusammenfassung"
>abstract="Das Diagramm „Web – Zusammenfassung“ zeigt die Entwicklung Ihrer Web-Erlebnisse (Impressions, eindeutige Impressions und Interaktionen) für den jeweiligen Zeitraum."

![](assets/campaign_web_summary.png)

Das Diagramm **[!UICONTROL Web-Zusammenfassung]** zeigt die Entwicklung Ihrer Web-Erlebnisse (Impressions, eindeutige Impressions und Interaktionen) für den jeweiligen Zeitraum.

+++ Weitere Informationen über Web-Zusammenfassungs-Metriken

* **[!UICONTROL Eindeutige Impressions]**: Anzahl der eindeutigen Benutzer, denen das Web-Erlebnis bereitgestellt wurde.

* **[!UICONTROL Impressions]**: Gesamtanzahl der für alle Benutzer bereitgestellten Web-Erlebnisse.

* **[!UICONTROL Interaktionen]**: Gesamtanzahl der Interaktionen mit Ihrer Web-Seite. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks oder andere Interaktionen.

+++

### Interaktionen nach Element {#web-interactions}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_interactions"
>title="Interaktionen nach Element"
>abstract="Die Tabelle „Interaktionen nach Element“ enthält wichtige Informationen zur Interaktion Ihrer Besucherinnen und Besucher mit verschiedenen Elementen auf Ihren Web-Seiten."

![](assets/campaign_web_interactions.png)

Die Tabelle **[!UICONTROL Interaktionen nach Element]** enthält umfassende Informationen zur Interaktion Ihrer Besucherinnen und Besucher mit den verschiedenen Elementen auf Ihren Web-Seiten und bietet wertvolle Einblicke in Benutzerinteraktionen und -präferenzen.

+++ Weitere Informationen zu Metriken für Interaktionen nach Element

* **[!UICONTROL Interaktionen]**: Gesamtanzahl der Interaktionen mit Ihrer Web-Seite Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks oder andere Interaktionen.

* **[!UICONTROL Interaktionsrate]**: Prozentsatz der Interaktionen mit Ihrer Web-Seite. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks oder andere Interaktionen.

+++

## Registerkarte „Briefpost“ {#direct-mail-global}

Im **[!UICONTROL globalen Bericht]** Ihrer Kampagne werden auf der Registerkarte **[!UICONTROL Briefpost]** die wichtigsten Informationen zu Ihren Briefpost-Nachrichten aufgeführt.

### Briefpost – Versandstatistiken {#direct-mail-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_sending_statistics"
>title="Briefpost – Versandstatistiken"
>abstract="Die Tabelle „Briefpost – Versandstatistiken“ enthält eine Zusammenfassung der wichtigsten Daten zu Ihren Briefpost-Nachrichten, wie z. B. „Angesprochen“ oder „Zugestellte Nachrichten“."

![](assets/campaign_direct_sending.png)

Die Tabelle **[!UICONTROL Briefpost – Versandstatistiken]** bietet eine kurze Zusammenfassung wichtiger Daten zu Ihren Briefpost-Nachrichten, die wichtige Metriken wie die Anzahl der gezielten Nachrichten und der zugestellten Nachrichten umfasst.

+++ Weitere Informationen zu Metriken für „Briefpost – Versandstatistiken“

* **[!UICONTROL Ausführungszeit]**: Startzeit jeder Ausführung Ihrer wiederkehrenden Briefpost. Um nur eine oder mehrere wiederkehrende Briefpost festzulegen, wählen Sie die gewünschte Option in der Dropdown-Liste **[!UICONTROL Ausführungszeit]** aus.

* **[!UICONTROL Zielguppe]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für die Briefpost-Nachrichten eignen.

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendungen für Ihre Briefpost-Nachricht.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Sendevorgangs aufgetretenen Fehler, die das Senden an Profile verhindert haben.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und Ihre Briefpost-Nachricht nicht erhalten haben.

+++

### Briefpost – Fehlergründe {#direct-mail-error}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_error_reasons"
>title="Briefpost – Fehlergründe"
>abstract="Die Graphen und die Tabelle „Briefpost – Fehlerursachen“ ermöglichen es Ihnen, die spezifischen Fehler zu identifizieren, die während des Versandvorgangs aufgetreten sind."

![](assets/direct-mail-report_1.png)

Die Graphen und die Tabelle **[!UICONTROL Briefpost – Fehlergründe]** bieten die Möglichkeit, spezifische Fehler zu identifizieren, die während des Sendevorgangs Ihrer Briefpost-Nachrichten aufgetreten sind. So können etwaige aufgetretene Probleme detailliert analysiert werden.

### Briefpost – Gründe für Ausschluss {#direct-mail-excluded}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_excluded_reasons"
>title="Briefpost – Gründe für Ausschluss"
>abstract="Die Graphen und die Tabelle mit Ausschlussgründen für den Direktversand veranschaulichen, warum Benutzerprofile, die von der Zielgruppe ausgeschlossen waren, die Nachricht nicht erhielten."

![](assets/campaign_direct_excluded.png)

Die Graphen und die Tabelle **[!UICONTROL Briefpost – Gründe für Ausschluss]** veranschaulichen visuell die verschiedenen Faktoren, die zum Ausschluss von Benutzerprofilen aus der Zielgruppe führten, sodass diese keine Briefpost-Nachrichten erhalten konnten.

Auf [dieser Seite](exclusion-list.md) finden Sie die umfassende Liste der Ausschlussgründe.

## Zusätzliche Ressourcen

* [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md)
* [Erstellen einer Kampagne](../campaigns/create-campaign.md)
* [Erstellen von API-ausgelösten Kampagnen](../campaigns/api-triggered-campaigns.md)
* [Ändern oder Stoppen einer Kampagne](../campaigns/modify-stop-campaign.md)
* [Kampagnen-Live-Bericht](campaign-live-report.md)
