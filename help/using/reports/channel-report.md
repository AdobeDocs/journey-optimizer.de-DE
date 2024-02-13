---
solution: Journey Optimizer
product: journey optimizer
title: Berichte auf Kanalebene
description: Weitere Informationen dazu, wie Daten aus den Kanalberichten verwendet werden können
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ead9359b-cdab-43ed-a469-d98b0ca19a17
source-git-commit: 5671f510d8be80b53d57b1ff90a101e500773243
workflow-type: tm+mt
source-wordcount: '3683'
ht-degree: 96%

---

# Kanalberichte {#channel-report}

>[!CONTEXTUALHELP]
>id="ajo_channel_level_report"
>title="Bericht auf Kanalebene"
>abstract="Die Kanalberichte bieten einen umfassenden Überblick über Traffic- und Interaktionsmetriken über alle Kanäle hinweg. Die Berichte sind in verschiedene Widgets unterteilt, die den Erfolg und die Fehler der Kampagne detailliert darstellen. Jedes Reporting-Dashboard kann durch Ändern der Größe oder Entfernen von Widgets verändert werden."

>[!IMPORTANT]
>
> Um auf das Menü **Bericht** zuzugreifen, müssen Sie die Berechtigung **[!UICONTROL Kanalberichte anzeigen]** haben. [Weitere Informationen](channel-report-gs.md#before-starting-manage-reports-prereq)

Die Kanalberichte bieten Benutzenden einen umfassenden Überblick über Traffic- und Interaktionsmetriken auf Kanalebene. Die Metriken werden aggregiert, um konsolidierte Werte für Aktionen aus dem ausgewählten Kanal darzustellen, die sich über verschiedene Kampagnen und Journeys erstrecken.

Greifen Sie auf die Kanalberichte zu, indem Sie im Abschnitt **Journey-Management** zum Menü **Berichte** navigieren. Es ist vollständig anpassbar. Sie können die Daten nach Berichtsdatum oder Aktion filtern. [Weitere Informationen](channel-report-gs.md)

Die Berichtseite wird mit den folgenden Registerkarten angezeigt:

* [E-Mail](#email)
* [Push-Benachrichtigungen ](#push)
* [SMS](#sms)
* [In-App](#inapp)
* [Web](#web)
* [Briefpost](#direct-mail)

➡️ [Entdecken Sie diese Funktion im Video](#channel-report-video)

## E-Mail {#email}

In den Kanalberichten werden im Menü „E-Mail“ die wichtigsten Informationen zu E-Mails aufgeführt, die in den Kampagnen und Journeys gesendet werden. Die Metriken werden nachfolgend beschrieben.

### E-Mail – Versandstatistiken gesamt {#email-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics"
>title="E-Mail – Versandstatistiken gesamt"
>abstract="Die KPIs „E-Mail – Versandstatistiken gesamt“ fassen wichtige Daten über Ihre E-Mails zusammen, wie z. B. gezielte oder zugestellte Nachrichten."

![](assets/channel_email_total_sending.png)

Das Widget **[!UICONTROL E-Mail – Versandstatistiken gesamt]** bietet einen umfassenden Überblick über Ihre E-Mail-Leistung und zeigt wichtige Leistungsindikatoren (KPIs) an, die wichtige Daten über Ihre E-Mails zusammenfassen.

+++ Weitere Informationen zu Metriken von „E-Mail – Versandstatistiken gesamt“

* **[!UICONTROL Angesprochen]**: Gesamtzahl der verarbeiteten E-Mails.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten E-Mails in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Versandrate]**: Prozentsatz der erfolgreich gesendeten E-Mails.

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler und automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der E-Mails, die nicht erfolgreich zugestellt wurden, im Vergleich zur Zahl der gesendeten E-Mails.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die das Senden an Profile verhindert haben.

* **[!UICONTROL Fehlerrate]**: Prozentsatz der Fehler, die auftraten und die Zustellung verhinderten, im Vergleich zur Zahl der gesendeten E-Mails.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

* **[!UICONTROL Ausschlussrate]**: Prozentsatz der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

+++

### E-Mail – Tracking-Statistiken gesamt {#email-total-tracking}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics"
>title="E-Mail – Tracking-Statistiken gesamt"
>abstract="Die KPIs „Gesamtstatistik E-Mail – Tracking“ liefern Daten zur Profilaktivität für Ihre E-Mails."

![](assets/channel_email_total_tracking.png)

Das Widget **[!UICONTROL E-Mail – Tracking-Statistiken gesamt]** bietet einen detaillierten Überblick über die Profilaktivität, die mit Ihren E-Mails verbunden ist, und liefert wichtige Einblicke in die Interaktion und die Effektivität Ihrer E-Mails.

+++ Weitere Informationen zu Metriken von „E-Mail – Tracking-Statistiken gesamt“

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen der Nachricht.

* **[!UICONTROL Öffnungsrate]**: Gesamtzahl der geöffneten E-Mails im Vergleich zu den versendeten E-Mails.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in einer Nachricht.

* **[!UICONTROL Klickrate]**: Prozentsatz der Benutzenden, die mit der E-Mail interagiert haben.

* **[!UICONTROL Beschwerden wegen Spam]**: Gibt an, wie oft eine Nachricht als Spam oder Junk gekennzeichnet wurde.

* **[!UICONTROL Spam-Beschwerderate]**: Prozentsatz der als Spam oder Junk deklarierten Nachrichten in Bezug auf die Anzahl der gesendeten E-Mails.

* **[!UICONTROL Abo beenden]**: Zahl der Klicks auf den Abo-Link.

* **[!UICONTROL Abmelderate]**: Prozentsatz der Abmeldungen in Bezug auf die Anzahl der gesendeten E-Mails.

+++

### E-Mail – Versandstatistiken im Zeitverlauf {#email-sending-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics_overtime"
>title="E-Mail – Versandstatistiken im Zeitverlauf"
>abstract="Der Graph „E-Mail – Versandstatistik im Zeitverlauf“ enthält Daten zu gesendeten E-Mails, aufgeschlüsselt nach Stunden, Tagen, Wochen oder Monaten."

![](assets/channel_email_sending_statistics.png)

Der Graph **[!UICONTROL E-Mail – Versandstatistiken im Zeitverlauf]** bietet eine dynamische Darstellung, die eine Analyse Ihrer E-Mail-Aktivitäten anzeigt. Diese grafische Darstellung bietet eine umfassende Aufschlüsselung gesendeter E-Mails, mit der Sie Trends und Muster auf stündlicher, täglicher, wöchentlicher oder monatlicher Basis beobachten können.

+++ Weitere Informationen zu Metriken von „E-Mail – Versandstatistiken im Zeitverlauf“

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten E-Mails in Bezug auf die Gesamtzahl der gesendeten E-Mails.

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler und automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten E-Mails.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die die Zustellung an Profile verhindert haben.

+++

### E-Mail – Tracking-Statistiken im Zeitverlauf {#email-tracking-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics_overtime"
>title="E-Mail – Tracking-Statistiken im Zeitverlauf"
>abstract="Der Graph „E-Mail – Tracking-Statistik im Zeitverlauf“ enthält Daten zur Profilaktivität Ihrer E-Mails, aufgeschlüsselt nach Stunden, Tagen, Wochen oder Monaten."

![](assets/channel_email_tracking_overtime.png)

Der Graph **[!UICONTROL E-Mail – Tracking-Statistiken im Zeitverlauf]** bietet einen detaillierten Überblick über die Profilaktivitäten im Zusammenhang mit Ihren E-Mails. Diese grafische Darstellung unterteilt die Daten auf stündlicher, täglicher, wöchentlicher oder monatlicher Basis und bietet wertvolle Einblicke in die Entwicklung der Interaktion der Empfängerinnen und Empfänger im Laufe verschiedener Zeitintervalle.

+++ Weitere Informationen zu Metriken von „E-Mail – Tracking-Statistiken im Zeitverlauf“

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen der Nachricht.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in einer Nachricht.

+++

### E-Mail – Bounce-Kategorien und -Gründe {#bounce-categories}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_categories"
>title="Bounce-Kategorien"
>abstract="Die Graphen und die Tabelle „Bounce-Kategorien“ enthalten Daten zu temporären und permanenten Fehlern."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons"
>title="Bounce-Gründe"
>abstract="Die Graphen und die Tabelle „Bounce-Gründe“ enthalten die verfügbaren Daten zu Bounce-Nachrichten."

![](assets/channel_email_bounce_categories.png)

Die Widgets **[!UICONTROL Bounce-Kategorien]** und **[!UICONTROL Bounce-Gründe]** kapseln die Daten, die mit Bounce-Nachrichten verbunden sind, und bieten einen umfassenden Überblick über die verschiedenen Kategorien und spezifischen Gründe für Bounce-Nachrichten.

Weitere Informationen zu Bounces finden Sie auf der Seite [Unterdrückungslisten](../reports/suppression-list.md).

+++ Weitere Informationen zu Metriken für Bounce-Kategorien

* **[!UICONTROL Hardbounce]**: die Gesamtzahl der permanenten Fehler, wie eine falsche E-Mail-Adresse. Dazu gehören Fehlermeldungen, die explizit eine ungültige Adresse anzeigen, wie etwa „Benutzer unbekannt“.

* **[!UICONTROL Softbounce]**: die Gesamtzahl der temporären Fehler, wie ein voller Posteingang.

* **[!UICONTROL Ignoriert]**: Die Gesamtzahl der temporären Ereignisse, beispielsweise Abwesenheit, oder technischer Fehler, zum Beispiel wenn der Absendertyp Postmaster ist.

+++

### Fehlergründe {#error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_error_reasons"
>title="Fehlergründe"
>abstract="Anhand der Graphen und der Tabelle „Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs aufgetreten sind."

![](assets/channel_email_error.png)

Die Graphen und die Tabelle **[!UICONTROL Fehlergründe]** ermöglichen es Ihnen, die genauen Fehler, die während des Sendevorgangs aufgetreten sind, zu ermitteln, was ein klares Verständnis der aufgetretenen Probleme ermöglicht.

### Gründe für Ausschluss {#excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_excluded_reasons"
>title="Gründe für Ausschluss"
>abstract="Die Graphen und die Tabelle „Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu führten, dass Benutzerprofile aus der Zielgruppe ausgeschlossen wurden und die Nachricht nicht erhielten."

![](assets/channel_email_excluded.png)

Die Graphen und die Tabelle **[!UICONTROL Gründe für Ausschluss]** bieten einen umfassenden Überblick über die verschiedenen Faktoren, die zum Ausschluss von Nutzerprofilen aus der Zielgruppe geführt haben, sodass die Nachricht nicht empfangen wurde.

Auf [dieser Seite](exclusion-list.md) finden Sie eine umfassende Liste der Ausschlussgründe.

### Gesendet und zugestellt nach Domains {#sent-delivered-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_delivered_domains"
>title="Gesendet und zugestellt nach Domains"
>abstract="Der Graph und die Tabelle „Von Domains gesendet und bereitgestellt“ stellen die Verteilung der wichtigsten E-Mail-Versanddaten auf Domain-Ebene dar."

![](assets/channel_email_sent_domains.png)

Die **[!UICONTROL Gesendet und von Domänen bereitgestellt]** Tabellen und Diagramme enthalten eine detaillierte Aufschlüsselung der E-Mail-Sendungen auf Domänenebene und bieten umfassende Einblicke in die Leistung Ihrer E-Mails.

+++ Weitere Informationen zu den Metriken zu „Gesendet und zugestellt nach Domains“

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge für Ihre E-Mail.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.

+++

### Bounces und Fehler nach Domains {#bounces-errors-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounces_errors_domains"
>title="Bounces und Fehler nach Domains"
>abstract="Der Graph und die Tabelle „Bounces und Fehler nach Domains“ zeigen die Verteilung der während des Versandvorgangs aufgetretenen spezifischen Fehler auf Domain-Ebene."

![](assets/channel_email_bounces_domain.png)

Die **[!UICONTROL Bounces und Fehler nach Domänen]** Diagramm und Tabelle bieten eine Aufschlüsselung der spezifischen Fehler, die während des Versandvorgangs auf Domänenebene aufgetreten sind, und enthalten eine detaillierte Analyse der aufgetretenen Probleme.

+++ Weitere Informationen zu den Metriken zu „Bounces und Fehler nach Domains“

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler beim Sendevorgang und der automatischen Rücksendungen im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der während des Sendevorgangs aufgetretenen Fehler, die das Senden an Profile verhindert haben.

+++

### Öffnungen und Klicks nach Domains {#open-clicks-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_open_clicks_domains"
>title="Öffnungen und Klicks nach Domains"
>abstract="Der Graph und die Tabelle „Aufrufe und Klicks nach Domains“ zeigen eine Aufschlüsselung der Interaktionen Ihrer Besucherinnen und Besucher mit Ihrer E-Mail auf Domain-Ebene."

![](assets/channel_email_open_domains.png)

Die **[!UICONTROL Öffnungen und Klicks nach Domänen]** Diagramm und Tabelle zeigen eine Aufschlüsselung der Interaktion Ihrer Besucher mit Ihrer E-Mail auf Domänenebene, die wertvolle Einblicke in die Interaktion verschiedener Domänen mit Ihrem Inhalt bietet.

+++ Weitere Informationen zu den Metriken zu „Öffnungen und Klicks nach Domains“

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen der E-Mail.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in einer E-Mail.

+++

### Bounce-Gründe nach Domain {#bounce-reasons-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons_domains"
>title="Bounce-Gründe nach Domain"
>abstract="Der Graph und die Tabelle „Bounce-Gründe nach Domain“ zeigen eine Aufschlüsselung temporärer sowie permanenter Fehlerdaten auf Domain-Ebene."

![](assets/channel_email_bounce_domain.png)

Die **[!UICONTROL Bounce-Gründe nach Domain]** Diagramme und Tabellen bieten eine Aufschlüsselung der Daten auf Domänenebene bezüglich temporärer und permanenter Fehler und bieten detaillierte Einblicke in die Ursachen für abgespeckte Nachrichten.

Weitere Informationen zu Bounces finden Sie auf der Seite [ Unterdrückungsliste](../reports/suppression-list.md).

## Push-Benachrichtigung {#push}

In Ihren Kanalberichten werden im Menü **Push-Benachrichtigung** die wichtigsten Informationen zu Push-Benachrichtigungen aufgeführt, die in Ihren Kampagnen und Journeys gesendet werden. Die Metriken werden nachfolgend beschrieben.

### Push-Benachrichtigungen – Versandstatistiken gesamt {#push-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics"
>title="Push-Benachrichtigungen – Versandstatistiken gesamt"
>abstract="Die KPIs „Gesamtstatistik Push-Benachrichtigungen – Versand“ fassen wichtige Daten zu Ihren Push-Benachrichtigungen zusammen, z. B. „Angesprochen“ oder „Zugestellt“."

![](assets/channel_push_total_sending.png)

Die KPIs zu **[!UICONTROL Push-Benachrichtigungen – Versandstatistiken gesamt]** dienen als umfassende Zusammenfassung mit wichtigen Daten zu Ihren Push-Benachrichtigungen. Diese Metriken enthalten detaillierte Einblicke in die Zielgruppe und den tatsächlichen Versandstatus und bieten einen umfassenden Überblick über die Effektivität und Reichweite Ihrer Push-Benachrichtigungen.

+++ Weitere Informationen zu Metriken für „Push-Benachrichtigungen – Versandstatistiken gesamt“

* **[!UICONTROL Angesprochen]**: Gesamtzahl der verarbeiteten Push-Benachrichtigungen.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Push-Benachrichtigungen in Bezug auf die Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Versandrate]**: Prozentsatz der erfolgreich gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler und automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der Push-Benachrichtigungen, die unzustellbar waren, im Vergleich zu den gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die die Zustellung an Profile verhindert haben.

* **[!UICONTROL Fehlerrate]**: Prozentualer Anteil der aufgetretenen Fehler, die den Versand verhindert haben, im Vergleich zu den gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

* **[!UICONTROL Ausschlussrate]**: Prozentsatz der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

+++

### Push-Benachrichtigungen – Tracking-Statistiken gesamt {#push-total-tracking}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics"
>title="Push-Benachrichtigungen – Tracking-Statistiken gesamt"
>abstract="Die Gesamtstatistik „Push-Benachrichtigung – Tracking“ liefert Daten zur Profilaktivität für Ihre Push-Benachrichtigungen."

Das Widget **[!UICONTROL Push-Benachrichtigungen – Tracking-Statistiken insgesamt]** bietet eine detaillierte Momentaufnahme der Profilaktivität, die mit Ihren Push-Benachrichtigungen verknüpft ist, sowie wichtige Einblicke in die Interaktion und die Effektivität von Push-Benachrichtigungen.

+++ Weitere Informationen zu Metriken für „Push-Benachrichtigungen – Tracking-Statistiken insgesamt“

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft eine Push-Benachrichtigung geöffnet wurde.

* **[!UICONTROL Öffnungsrate]**: Prozentsatz der geöffneten Push-Benachrichtigungen.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf Schaltfläche oder Abbruch.

* **[!UICONTROL Aktionsrate]**: Prozentsatz der Aktionen, die bei zugestellten Push-Benachrichtigungen durchgeführt wurden, im Vergleich zu gesendeten Push-Benachrichtigungen.

+++

### Push-Benachrichtigungen – Versandstatistiken im Zeitverlauf {#push-sending-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_overtime"
>title="Push-Benachrichtigungen – Versandstatistiken im Zeitverlauf"
>abstract="Das Diagramm „Push-Benachrichtigung – Versandstatistik im Zeitverlauf“ enthält Daten zu gesendeten Push-Benachrichtigungen, aufgeschlüsselt nach Stunden, Tagen, Wochen oder Monaten."

![](assets/channel_push_sending_statistics.png)

Der Graph **[!UICONTROL Push-Benachrichtigungen – Versandstatistiken im Zeitverlauf]** bietet eine dynamische Darstellung mit einer Analyse Ihrer Push-Benachrichtigungs-Aktivitäten. Diese grafische Darstellung bietet eine umfassende Aufschlüsselung gesendeter Push-Benachrichtigungen, mit der Sie Trends und Muster auf stündlicher, täglicher, wöchentlicher oder monatlicher Ebene beobachten können.

+++ Weitere Informationen zu Metriken für „Push-Benachrichtigungen – Versandstatistiken im Zeitverlauf“

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Push-Benachrichtigungen in Bezug auf die Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler und automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die die Zustellung an Profile verhindert haben.

+++

### Push-Benachrichtigungen – Tracking-Statistik im Zeitverlauf {#push-tracking-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_overtime"
>title="Push-Benachrichtigungen – Tracking-Statistik im Zeitverlauf"
>abstract="Das Diagramm „Push-Benachrichtigungen – Tracking-Statistik im Zeitverlauf“ liefert Daten zur Profilaktivität Ihrer Push-Benachrichtigungen, aufgeschlüsselt nach Stunden, Tagen, Wochen oder Monaten."

Der Graph **[!UICONTROL Push-Benachrichtigungen – Tracking-Statistik im Zeitverlauf]** bietet einen detaillierten Überblick über die Profilaktivität in Bezug auf Ihre Push-Benachrichtigungen. Diese grafische Darstellung unterteilt die Daten auf stündlicher, täglicher, wöchentlicher oder monatlicher Basis und bietet wertvolle Einblicke in die Entwicklung der Interaktion der Empfängerinnen und Empfänger im Laufe verschiedener Zeitintervalle.

+++ Weitere Informationen zu Metriken für „Push-Benachrichtigungen – Tracking-Statistik im Zeitverlauf“

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft Ihre Push-Benachrichtigung geöffnet wurde.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf Schaltfläche oder Abbruch.

+++

### Push-Benachrichtigungen – Gründe für Ausschluss {#push-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_excluded_reasons"
>title="Gründe für Ausschluss"
>abstract="Die Graphen und die Tabelle „Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu führten, dass Benutzerprofile aus der Zielgruppe ausgeschlossen wurden und die Nachricht nicht erhielten."

![](assets/channel_push_excluded.png)

Der Graph und die Tabelle **[!UICONTROL Gründe für Ausschluss]** zeigen die verschiedenen Gründe an, die verhindert haben, dass Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen wurden, die Push-Benachrichtigung erhalten haben.

Auf [dieser Seite](exclusion-list.md) finden Sie eine umfassende Liste der Ausschlussgründe.

### Push-Benachrichtigungen – Fehlergründe {#push-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_error_reasons"
>title="Fehlergründe"
>abstract="Anhand der Graphen und der Tabelle „Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs aufgetreten sind."

![](assets/channel_push_error.png)

Die Graphen und die Tabelle **[!UICONTROL Fehlergründe]** bieten Ihnen die Möglichkeit, spezifische Fehler zu identifizieren, die während des Sendevorgangs Ihrer Push-Benachrichtigungen aufgetreten sind. So erhalten Sie detaillierte Einblicke in Probleme, die während des Vorgangs aufgetreten sind.

### Push-Benachrichtigungen – Tracking nach Plattform {#push-tracking-platform}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_platform"
>title="Tracking-Statistik nach Plattform"
>abstract="Der Graph und die Tabelle „Tracking-Statistik nach Plattform“ enthalten je nach Betriebssystem Ihres Profils Daten zur Profilaktivität Ihrer Push-Benachrichtigungen."

Die Graphen und Tabellen **[!UICONTROL Push-Benachrichtigungen – Tracking nach Plattform]** zeigen die Empfängeraktivität für Ihre Push-Benachrichtigung in Abhängigkeit vom Betriebssystem Ihres Profils an.

### Push-Benachrichtigungen – Versand nach Plattform {#push-sending-platform}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_platform"
>title="Tracking-Statistik nach Plattform"
>abstract="Der Graph und die Tabelle „Tracking-Statistik nach Plattform“ enthalten Daten zu gesendeten Push-Benachrichtigungen."

![](assets/channel_push_sending_platform.png)

Die Graphen und Tabellen **[!UICONTROL Push-Benachrichtigungen – Versand nach Plattform]** enthalten eine umfassende Aufschlüsselung, in der der Erfolg Ihrer Push-Benachrichtigungen in Bezug auf die Betriebssysteme Ihrer Profile detailliert beschrieben wird. Diese gründliche Analyse bietet wertvolle Einblicke in die Effektivität Ihrer Push-Benachrichtigungen über verschiedene Plattformen hinweg.

## SMS {#sms}

In den **Kanalberichten** werden im Menü „SMS“ die wichtigsten Informationen zu SMS-Nachrichten aufgeführt, die in Ihren Kampagnen und Journeys versendet wurden. Die Metriken werden nachfolgend beschrieben.

### SMS – Versandstatistiken gesamt {#sms-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics"
>title="SMS – Versandstatistiken gesamt"
>abstract="Die KPIs „Gesamtstatistik SMS – Versand“ enthalten wichtige Daten zu Ihren SMS-Nachrichten, wie „Angesprochen“ oder „Zugestellt“."

![](assets/channel_sms_total_sending.png)

Die KPIs **[!UICONTROL SMS – Versandstatistiken gesamt]** dienen als umfassende Zusammenfassung und enthalten wichtige Daten zu Ihrer SMS. Diese Metriken enthalten detaillierte Einblicke in die Zielgruppe und den tatsächlichen Versandstatus und bieten einen umfassenden Überblick über die Effektivität und Reichweite Ihrer SMS-Nachrichten.

+++ Weitere Informationen zu Metriken für „Push-Benachrichtigungen – Versandstatistiken gesamt“

* **[!UICONTROL Angesprochen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für den SMS-Kanal eignen.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten SMS-Nachrichten in Bezug auf die Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Versandrate]**: Prozentsatz der erfolgreich gesendeten SMS-Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler und automatischen Rücksendeverarbeitungen im Verhältnis zur Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der SMS-Nachrichten, die nicht erfolgreich zugestellt wurden, im Vergleich zur Anzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die die Zustellung an Profile verhindert haben.

* **[!UICONTROL Fehlerrate]**: Prozentsatz der Fehler, die auftraten und die Zustellung verhinderten, im Vergleich zur Zahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

* **[!UICONTROL Ausschlussrate]**: Prozentsatz der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

+++

### SMS – Tracking-Statistik gesamt {#sms-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics"
>title="SMS – Tracking-Statistik gesamt"
>abstract="Die Gesamtstatistik „SMS – Nachverfolgung“ liefert Daten zur Profilaktivität Ihrer SMS-Nachrichten."

![](assets/channel_sms_tracking.png)

Das Widget **[!UICONTROL SMS – Tracking-Statistik gesamt]** bietet einen detaillierten Überblick über wichtige Informationen zur Interaktion Ihrer Besucherinnen und Besucher mit Ihren URLs und bietet Einblicke in die Effektivität Ihrer SMS-Nachrichten:

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in einer SMS-Nachricht.

### SMS – Versandstatistiken im Zeitverlauf {#sms-sending-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics_overtime"
>title="SMS – Versandstatistiken im Zeitverlauf"
>abstract="Der Graph „SMS – Versandstatistik im Zeitverlauf“ zeigt Daten zu gesendeten SMS-Nachrichten an, aufgeschlüsselt nach Stunden, Tagen, Wochen oder Monaten."

![](assets/channel_sms_sending_overtime.png)

Das Diagramm **[!UICONTROL SMS – Versandstatistiken im Zeitverlauf]** bietet einen umfassenden Überblick zu gesendeten SMS-Nachrichten an, wobei die Daten nach Stunden, Tagen, Wochen oder Monaten aufgeschlüsselt sind. Mit dieser grafischen Darstellung können Sie Trends in Ihrer SMS-Nachrichtenaktivität über verschiedene Zeitintervalle hinweg verfolgen und analysieren.

+++ Weitere Informationen zu Metriken für „SMS – Versandstatistiken im Zeitverlauf“

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler und automatischen Rücksendeverarbeitungen im Verhältnis zur Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die die Zustellung an Profile verhindert haben.

+++

### SMS – Tracking-Statistik im Zeitverlauf {#sms-tracking-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics_overtime"
>title="SMS – Tracking-Statistik im Zeitverlauf"
>abstract="Der Graph „SMS – Tracking-Statistik im Zeitverlauf“ enthält Daten zur Profilaktivität Ihrer SMS-Nachrichten, aufgeschlüsselt nach Stunden, Tagen, Wochen oder Monaten."

![](assets/channel_sms_tracking_overtime.png)

Der Graph **[!UICONTROL SMS – Tracking-Statistik im Zeitverlauf]** enthält Daten zur Profilaktivität in Bezug auf Ihre SMS-Nachrichten, aufgeschlüsselt nach Stunden, Tagen, Wochen oder Monaten. Diese grafische Darstellung ermöglicht es Ihnen, Muster in der Benutzerinteraktion über verschiedene Zeitintervalle hinweg zu analysieren und zu verstehen.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in einer SMS-Nachricht.

### Gründe für Ausschluss {#sms-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_excluded_reasons"
>title="Gründe für Ausschluss"
>abstract="Die Graphen und die Tabelle „Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu führten, dass Benutzerprofile aus der Zielgruppe ausgeschlossen wurden und die Nachricht nicht erhielten."

![](assets/channel_sms_excluded.png)

Die Graphen und die Tabelle **[!UICONTROL Gründe für Ausschluss]** zeigen visuell die verschiedenen Faktoren an, die zum Ausschluss von Benutzerprofilen aus der Zielgruppe geführt haben, sodass diese keine SMS-Nachrichten erhalten konnten.

Auf [dieser Seite](exclusion-list.md) finden Sie die umfassende Liste der Ausschlussgründe.

### Bounce-Gründe {#sms-bounce-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_bounce_reasons"
>title="Bounce-Gründe"
>abstract="Die Graphen und die Tabelle „Bounce-Gründe“ enthalten die verfügbaren Daten zu Bounce-Nachrichten."

![](assets/channel_sms_bounce_reasons.png)

Die Graphen und die Tabelle **[!UICONTROL Bounce-Gründe]** bieten einen umfassenden Überblick über Daten zu nicht zugestellten SMS-Nachrichten und liefern wertvolle Einblicke in die spezifischen Gründe von nicht zugestellten SMS-Nachrichten.

### Fehlergründe {#sms-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_error_reasons"
>title="Fehlergründe"
>abstract="Anhand der Graphen und der Tabelle „Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs aufgetreten sind."

Anhand der Graphen und der Tabelle **[!UICONTROL Fehlergründe]** können Sie die spezifischen Fehler identifizieren, die während des Sendevorgangs Ihrer SMS-Nachrichten aufgetreten sind. Dies ermöglicht eine gründliche Analyse aller aufgetretenen Probleme.

## Briefpost {#direct-mail}

In den **Kanalberichten** werden im Menü **Briefpost** die wichtigsten Informationen zu Briefpost-Nachrichten aufgeführt, die in Ihren **Kampagnen** und **Journeys** gesendet werden. Die Metriken werden nachfolgend beschrieben.

### Briefpost – Versandstatistiken gesamt {#direct-mail-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_sending_statistics"
>title="Briefpost – Versandstatistiken gesamt"
>abstract="Die KPIs „Briefpost – Gesamtstatistik Versand“ enthalten wichtige Daten zu Ihren Nachrichten per Briefpost, wie „Angesprochen“ oder „Zugestellt“."

![](assets/channel_direct_sending.png)

Das Widget **[!UICONTROL Briefpost – Versandstatistiken gesamt]** bietet einen umfassenden Überblick über die Leistung Ihrer Briefpost-Nachrichten und zeigt wichtige Leistungsindikatoren (KPIs) an, die wichtige Daten zu Ihren Briefpost-Nachrichten zusammenfassen.

+++ Weitere Informationen zu Metriken für „Briefpost – Versandstatistiken gesamt“

* **[!UICONTROL Angesprochen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für die Briefpost-Nachrichten eignen.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die den Versand an Profile verhindert haben.

* **[!UICONTROL Fehlerrate]**: Prozentualer Anteil der aufgetretenen Fehler, die den Versand verhindert haben, im Vergleich zu den gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

* **[!UICONTROL Ausschlussrate]**: Prozentsatz der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

+++

### Gründe für Ausschluss {#direct-mail-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_excluded_reasons"
>title="Gründe für Ausschluss"
>abstract="Die Graphen und die Tabelle „Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu führten, dass Benutzerprofile aus der Zielgruppe ausgeschlossen wurden und die Nachricht nicht erhielten."

![](assets/channel_direct_excluded.png)

Die Graphen und die Tabelle **[!UICONTROL Briefpost – Gründe für Ausschluss]** veranschaulichen die verschiedenen Faktoren visuell, die zum Ausschluss von Benutzerprofilen aus der Zielgruppe geführt haben, sodass diese keine Briefpostnachrichten erhalten konnten.

Auf [dieser Seite](exclusion-list.md) finden Sie die umfassende Liste der Gründe für den Ausschluss.

### Fehlergründe {#direct-mail-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_error_reasons"
>title="Fehlergründe"
>abstract="Anhand der Graphen und der Tabelle „Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs aufgetreten sind."

![](assets/channel_direct_error.png)

**[!UICONTROL Briefpost – Fehlergründe]** stellt die Mittel bereit, um spezifische Fehler zu identifizieren, die während des Versands Ihrer Briefpostnachrichten aufgetreten sind, sodass Sie etwaige aufgetretene Probleme detailliert analysieren können.

## In-App {#in-app}

In den Kanalberichten werden im Menü „In-App“ die wichtigsten Informationen zu In-App-Nachrichten aufgeführt, die in den Kampagnen und Journeys gesendet werden. Die Metriken werden nachfolgend beschrieben.

### In-App – Interaktionen insgesamt {#inapp-total-engagement}

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement"
>title="In-App – Interaktionen insgesamt"
>abstract="Die KPIs „In-App – Interaktionen Insgesamt“ liefern umfassende Informationen über die Interaktion Ihrer Besucherinnen und Besucher mit Ihren In-App-Nachrichten, einschließlich Metriken wie „Impressions“ und „Interaktionen“."

![](assets/channel_inapp_engagement.png)

Die KPIs **[!UICONTROL In-App – Interaktionen insgesamt]** liefern umfassende Einblicke in die Interaktion Ihrer Besucherinnen und Besucher mit Ihren In-App-Nachrichten, einschließlich wichtiger Metriken wie **Impressions** und **Interaktionen**.

+++ Weitere Informationen zu Metriken für „In-App – Interaktionen insgesamt“

* **[!UICONTROL Impressions]**: Gesamtzahl der an alle Benutzenden gesendeten In-App-Nachrichten.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit der In-App-Nachricht. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks, Abbrüche oder andere Interaktionen.

+++

### In-App – Interaktionen im Zeitverlauf {#inapp-engagement-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement_overtime"
>title="In-App – Interaktionen im Zeitverlauf"
>abstract="Der Graph „In-App – Interaktionen im Zeitverlauf“ verfolgt In-App-Impressions und Interaktionen, aufgeschlüsselt nach Stunden, Tagen, Wochen und Monaten."

![](assets/channel_inapp_engagement_overtime.png)

Der Graph **[!UICONTROL In-App-Interaktionen im Zeitverlauf]** zeigt die Entwicklung der In-App-Impressions und -Interaktionen für den jeweiligen Zeitraum an, indem Impressions, Abbrüche oder Interaktionen verfolgt werden.

+++ Weitere Informationen zu Metriken für „In-App-Interaktionen im Zeitverlauf“

* **[!UICONTROL Impressions]**: Gesamtzahl der an alle Benutzenden gesendeten In-App-Nachrichten.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit der In-App-Nachricht. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks, Abbrüche oder andere Interaktionen.

+++

## Web {#web}

In den **Kanalberichten** werden im Menü „Web“ die wichtigsten Informationen zu Web-Seiten aufgeführt, die in Ihren **Kampagnen** und **Journeys** enthalten sind. Die Metriken werden nachfolgend beschrieben.

### Web – Interaktionen insgesamt {#web-engagement-total}

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement"
>title="Web – Interaktionen insgesamt"
>abstract="Die KPIs „Web – Interaktionen insgesamt“ liefern umfassende Informationen über die Interaktion Ihrer Besucherinnen und Besucher mit Ihren Web-Seiten, einschließlich Metriken wie „Impressions“ und „Interaktionen“."

![](assets/channel_web_engagement.png)

Die KPIs **[!UICONTROL Web – Interaktionen insgesamt]** liefern umfassende Einblicke in die Interaktion Ihrer Besucherinnen und Besucher mit Ihren Web-Seiten, einschließlich Metriken wie „Impressions“ und „Interaktionen“.

+++ Weitere Informationen zu Metriken für „Web – Interaktionen insgesamt“

* **[!UICONTROL Impressions]**: Gesamtanzahl der für alle Benutzenden bereitgestellten Web-Erlebnisse.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit Ihrer Web-Seite. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks oder andere Interaktionen.

+++

### Web – Interaktionen gesamt im Zeitverlauf {#web-engagement-total-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement_overtime"
>title="Web – Interaktionen gesamt im Zeitverlauf"
>abstract="Der Graph „Web – Interaktionen im Zeitverlauf“ verfolgt die Impressions und Interaktionen Ihrer Web-Seiten, aufgeschlüsselt nach Stunden, Tagen, Wochen und Monaten."

![](assets/channel_web_engagement_overtime.png)

Der Graph **[!UICONTROL Web – Interaktionen im Zeitverlauf]** überwacht die **Impressions** und **Interaktionen** Ihrer Web-Seiten und bietet detaillierte Aufschlüsselungen auf stündlicher, täglicher, wöchentlicher und monatlicher Basis.

+++ Weitere Informationen zu Metriken für „Web – Interaktionen im Zeitverlauf“

* **[!UICONTROL Impressions]**: Gesamtanzahl der für alle Benutzenden bereitgestellten Web-Erlebnisse.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit Ihrer Web-Seite. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks oder andere Interaktionen.

+++

## Kanalbericht (Video) {#channel-report-video}

In diesem Video gibt es weitere Informationen dazu, wie auf Kanalebene auf Berichte zugegriffen, darin navigiert und diese exportiert werden können.

>[!VIDEO](https://video.tv.adobe.com/v/3424537?quality=12)
