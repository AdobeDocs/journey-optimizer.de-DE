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
source-git-commit: 6bceccc561daac594f5c84d3d3250d887a349b7b
workflow-type: ht
source-wordcount: '2664'
ht-degree: 100%

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
* [Push-Benachrichtigung Benachrichtigungen](#push)
* [SMS](#sms)
* [In-App](#inapp)
* [Web](#web)
* [Briefpost](#direct-mail)

➡️ [Entdecken Sie diese Funktion im Video](#channel-report-video)

## E-Mail {#email}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics"
>title="Gesamtstatistik E-Mail – Versand"
>abstract="Die KPIs „Gesamtstatistik E-Mail – Versand“ fassen die wichtigsten Daten zu Ihren Push-Benachrichtigungen, wie z. B. „Angesprochen“ oder „Zugestellte Nachrichten“."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics"
>title="Gesamtstatistik E-Mail – Tracking"
>abstract="Die KPIs „Gesamtstatistik E-Mail – Tracking“ liefern Daten zur Profilaktivität für Ihre E-Mails."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics_overtime"
>title="E-Mail – Versandstatistik im Zeitverlauf"
>abstract="Der Graph „E-Mail – Versandstatistik im Zeitverlauf“ enthält Daten zu gesendeten E-Mails, aufgeschlüsselt nach Stunden, Tagen, Wochen oder Monaten."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics_overtime"
>title="E-Mail – Tracking-Statistik im Zeitverlauf"
>abstract="Der Graph „E-Mail – Tracking-Statistik im Zeitverlauf“ enthält Daten zur Profilaktivität Ihrer E-Mails, aufgeschlüsselt nach Stunden, Tagen, Wochen oder Monaten."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_categories"
>title="Bounce-Kategorien"
>abstract="Die Graphen und die Tabelle „Bounce-Kategorien“ enthalten Daten zu temporären und permanenten Fehlern."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons"
>title="Bounce-Gründe"
>abstract="Die Graphen und die Tabelle „Bounce-Gründe“ enthalten die verfügbaren Daten zu Bounce-Nachrichten."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_error_reasons"
>title="Fehlerursachen"
>abstract="Anhand der Graphen und der Tabelle „Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs aufgetreten sind."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_excluded_reasons"
>title="Ausgeschlossene Gründe"
>abstract="Die Graphen und die Tabelle „Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu führten, dass Benutzerprofile aus der Zielgruppe ausgeschlossen wurden und die Nachricht nicht erhielten."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_delivered_domains"
>title="Von Domains gesendet und bereitgestellt"
>abstract="Der Graph und die Tabelle „Von Domains gesendet und bereitgestellt“ stellen die Verteilung der wichtigsten E-Mail-Versanddaten auf Domain-Ebene dar."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounces_errors_domains"
>title="Bounces und Fehler nach Domains"
>abstract="Der Graph und die Tabelle „Bounces und Fehler nach Domains“ zeigen die Verteilung der während des Versandvorgangs aufgetretenen spezifischen Fehler auf Domain-Ebene."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_open_clicks_domains"
>title="Aufrufe und Klicks nach Domains"
>abstract="Der Graph und die Tabelle „Aufrufe und Klicks nach Domains“ zeigen eine Aufschlüsselung der Interaktionen Ihrer Besucherinnen und Besucher mit Ihrer E-Mail auf Domain-Ebene."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons_domains"
>title="Bounce-Gründe nach Domain"
>abstract="Der Graph und die Tabelle „Bounce-Gründe nach Domain“ zeigen eine Aufschlüsselung temporärer sowie permanenter Fehlerdaten auf Domain-Ebene."

In den Kanalberichten werden im Menü „E-Mail“ die wichtigsten Informationen zu E-Mails aufgeführt, die in den Kampagnen und Journeys gesendet werden. Die Metriken werden nachfolgend beschrieben.

![](assets/email_channel_1.png)

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den E-Mail-Bericht verfügbar sind.

Das Diagramm **[!UICONTROL E-Mail - Gesamtstatistiken Versand]** gibt Aufschluss über den Erfolg Ihrer E-Mails:

* **[!UICONTROL Angesprochen]**: Gesamtzahl der verarbeiteten E-Mails.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten E-Mails in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Versandrate]**: Prozentsatz der erfolgreich gesendeten E-Mails.

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler und automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der E-Mails, die nicht erfolgreich zugestellt wurden, im Vergleich zur Zahl der gesendeten E-Mails.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die die Zustellung an Profile verhindert haben.

* **[!UICONTROL Fehlerrate]**: Prozentsatz der Fehler, die auftraten und die Zustellung verhinderten, im Vergleich zur Zahl der gesendeten E-Mails.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

* **[!UICONTROL Ausschlussrate]**: Prozentsatz der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

Das Widget **[!UICONTROL Gesamtstatistik E-Mail – Nachverfolgung]** enthält die verfügbaren Daten zur Profilaktivität Ihrer E-Mails:

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen der Nachricht.

* **[!UICONTROL Öffnungsrate]**: Gesamtzahl der geöffneten E-Mails im Vergleich zu den versendeten E-Mails.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in einer Nachricht.

* **[!UICONTROL Klickrate]**: Prozentsatz der Benutzenden, die mit der E-Mail interagiert haben.

* **[!UICONTROL Beschwerden wegen Spam]**: Gibt an, wie oft eine Nachricht als Spam oder Junk gekennzeichnet wurde.

* **[!UICONTROL Spam-Beschwerderate]**: Prozentsatz der als Spam oder Junk deklarierten Nachrichten in Bezug auf die Anzahl der gesendeten E-Mails.

* **[!UICONTROL Abo beenden]**: Zahl der Klicks auf den Abo-Link.

* **[!UICONTROL Abmelderate]**: Prozentsatz der Abmeldungen in Bezug auf die Anzahl der gesendeten E-Mails.

Der Graph **[!UICONTROL Versandstatistiken im Zeitverlauf]** enthält die Daten, die für gesendete E-Mails verfügbar sind, z. B.:

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten E-Mails in Bezug auf die Gesamtzahl der gesendeten E-Mails.

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler und automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten E-Mails.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die die Zustellung an Profile verhindert haben.

Der Graph **[!UICONTROL E-Mail-Tracking-Statistiken im Zeitverlauf]** enthält die Daten, die für Öffnungen und Klicks verfügbar sind.

Die Widgets **[!UICONTROL Bounce-Gründe]** und **[!UICONTROL Bounce-Kategorien]** enthalten die verfügbaren Daten zu unzustellbaren Nachrichten wie:

* **[!UICONTROL Hardbounce]**: die Gesamtzahl der permanenten Fehler, wie eine falsche E-Mail-Adresse. Dazu gehören Fehlermeldungen, die explizit eine ungültige Adresse anzeigen, wie etwa „Benutzer unbekannt“.

* **[!UICONTROL Softbounce]**: die Gesamtzahl der temporären Fehler, wie ein voller Posteingang.

* **[!UICONTROL Ignoriert]**: Die Gesamtzahl der temporären Ereignisse, beispielsweise Abwesenheit, oder technischer Fehler, zum Beispiel wenn der Absendertyp Postmaster ist.

Weitere Informationen zu Bounces finden Sie auf der Seite [ Unterdrückungslisten](../reports/suppression-list.md).

Der Graph und die Tabelle **[!UICONTROL Fehlergründe]** zeigen, welcher Fehler während des Versands aufgetreten ist.

Der Graph und die Tabelle **[!UICONTROL Ausschlussgründe]** zeigen die verschiedenen Gründe an, die verhindert haben, dass Nutzerprofile, die von den Zielprofilen ausgeschlossen wurden, die Nachricht erhalten haben.

Die Tabellen und Graphen **[!UICONTROL Bounce-Gründe nach Domain]**, **[!UICONTROL Gesendet und zugestellt nach Domain]**, **[!UICONTROL Öffnungen und Klicks nach Domain]** und **[!UICONTROL Bounces und Fehler nach Domain]** bieten eine Aufschlüsselung aller E-Mail-Versand- und Tracking-Daten auf Domain-Ebene.
+++

## Push-Benachrichtigung {#push}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics"
>title="Gesamtstatistik Push-Benachrichtigungen – Versand"
>abstract="Die KPIs „Gesamtstatistik Push-Benachrichtigungen – Versand“ fassen wichtige Daten zu Ihren Push-Benachrichtigungen zusammen, z. B.  „Angesprochen“ oder „Zugestellt“."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics"
>title="Gesamtstatistik Push-Benachrichtigung – Tracking"
>abstract="Die Gesamtstatistik „Push-Benachrichtigung – Tracking“ liefert Daten zur Profilaktivität für Ihre Push-Benachrichtigungen."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_overtime"
>title="Push-Benachrichtigungen – Versandstatistik im Zeitverlauf"
>abstract="Das Diagramm „Push-Benachrichtigung – Versandstatistik im Zeitverlauf“ enthält Daten zu gesendeten Push-Benachrichtigungen, aufgeschlüsselt nach Stunden, Tagen, Wochen oder Monaten."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_overtime"
>title="Push-Benachrichtigungen – Tracking-Statistik im Zeitverlauf"
>abstract="Das Diagramm „Push-Benachrichtigungen – Tracking-Statistik im Zeitverlauf“ liefert Daten zur Profilaktivität Ihrer Push-Benachrichtigungen, aufgeschlüsselt nach Stunden, Tagen, Wochen oder Monaten."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_excluded_reasons"
>title="Ausgeschlossene Gründe"
>abstract="Die Graphen und die Tabelle „Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu führten, dass Benutzerprofile aus der Zielgruppe ausgeschlossen wurden und die Nachricht nicht erhielten."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_error_reasons"
>title="Fehlerursachen"
>abstract="Anhand der Graphen und der Tabelle „Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs aufgetreten sind."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_platform"
>title="Tracking-Statistik nach Plattform"
>abstract="Der Graph und die Tabelle „Tracking-Statistik nach Plattform“ enthalten je nach Betriebssystem Ihres Profils Daten zur Profilaktivität Ihrer Push-Benachrichtigungen."

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_platform"
>title="Tracking-Statistik nach Plattform"
>abstract="Der Graph und die Tabelle „Tracking-Statistik nach Plattform“ enthalten Daten zu gesendeten Push-Benachrichtigungen."

In Ihren Kanalberichten werden im Menü „Push-Benachrichtigung“ die wichtigsten Informationen zu Push-Benachrichtigungen aufgeführt, die in Ihren Kampagnen und Journeys gesendet werden. Die Metrik wird nachfolgend beschrieben.

![](assets/push_channel_1.png)

+++  Erfahren Sie mehr über die verschiedenen für den Push-Bericht verfügbaren Metriken und Widgets.

Die Tabelle **[!UICONTROL Push-Benachrichtigung – Gesamte Sendestatistiken]** enthält die wichtigsten Informationen zu Ihren Push-Benachrichtigungen mit Graph und KPIs:

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

Die **[!UICONTROL Gesamtstatistik Push-Benachrichtigung – Tracking]** enthält die verfügbaren Daten zur Profilaktivität für Ihre Push-Benachrichtigungen:

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft eine Push-Benachrichtigung geöffnet wurde.

* **[!UICONTROL Öffnungsrate]**: Prozentsatz der geöffneten Push-Benachrichtigungen.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf Schaltfläche oder Abbruch.

* **[!UICONTROL Aktionsrate]**: Prozentsatz der Aktionen, die bei zugestellten Push-Benachrichtigungen durchgeführt wurden, im Vergleich zu gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Interaktionsrate]**: Prozentsatz der Öffnungen und Aktionen für diese Push-Benachrichtigung, d. h. wenn das Profil die Push-Benachrichtigung geöffnet hat oder auf eine Schaltfläche geklickt wurde.

Der Graph **[!UICONTROL Push-Benachrichtigungen – Versandstatistiken im Zeitverlauf]** enthält die Daten, die für gesendete Push-Benachrichtigungen verfügbar sind, z. B.:

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Push-Benachrichtigungen in Bezug auf die Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler und automatischen Rücksendungen, bezogen auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die die Zustellung an Profile verhindert haben.

Der Graph und die Tabelle **[!UICONTROL Ausschlussgründe]** zeigen die verschiedenen Gründe an, die verhindert haben, dass Nutzerprofile, die von den Zielprofilen ausgeschlossen wurden, die Nachricht erhalten haben.

Der Graph und die Tabelle **[!UICONTROL Fehlergründe]** zeigen, welcher Fehler aufgetreten ist.

Die Graphen und Tabellen **[!UICONTROL Tracking nach Plattform]** und **[!UICONTROL Versand nach Plattform]** geben einen Überblick über den Erfolg Ihrer Push-Benachrichtigung, aufgeschlüsselt nach dem Betriebssystem Ihres Profils.
+++

## SMS {#sms}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics"
>title="Gesamtstatistik SMS – Versand"
>abstract="Die KPIs „Gesamtstatistik SMS – Versand“ enthalten wichtige Daten zu Ihren SMS-Nachrichten, wie „Angesprochen“ oder „Zugestellt“."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics"
>title="Gesamtstatistik SMS – Nachverfolgung"
>abstract="Die Gesamtstatistik „SMS – Nachverfolgung“ liefert Daten zur Profilaktivität Ihrer SMS-Nachrichten."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics_overtime"
>title="SMS – Versandstatistik im Zeitverlauf"
>abstract="Der Graph „SMS – Versandstatistik im Zeitverlauf“ zeigt Daten zu gesendeten SMS-Nachrichten an, aufgeschlüsselt nach Stunden, Tagen, Wochen oder Monaten."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics_overtime"
>title="SMS – Tracking-Statistik im Zeitverlauf"
>abstract="Der Graph „SMS – Tracking-Statistik im Zeitverlauf“ enthält Daten zur Profilaktivität Ihrer SMS-Nachrichten, aufgeschlüsselt nach Stunden, Tagen, Wochen oder Monaten."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_excluded_reasons"
>title="Ausgeschlossene Gründe"
>abstract="Die Graphen und die Tabelle „Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu führten, dass Benutzerprofile aus der Zielgruppe ausgeschlossen wurden und die Nachricht nicht erhielten."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_bounce_reasons"
>title="Bounce-Gründe"
>abstract="Die Graphen und die Tabelle „Bounce-Gründe“ enthalten die verfügbaren Daten zu Bounce-Nachrichten."

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_error_reasons"
>title="Fehlerursachen"
>abstract="Anhand der Graphen und der Tabelle „Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs aufgetreten sind."

In den Kanalberichten werden im Menü „SMS“ die wichtigsten Informationen zu SMS-Nachrichten aufgeführt, die in Ihren Kampagnen und Journeys versendet wurden. Die Metriken werden nachfolgend beschrieben.

![](assets/sms_channel_1.png)

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den SMS-Bericht verfügbar sind.

Die Tabelle **[!UICONTROL SMS – Gesamte Sendestatistiken]** gibt Auskunft über den Erfolg des SMS-Versands:

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

Das Widget **[!UICONTROL SMS – Tracking-Statistiken gesamt]** enthält die wichtigsten Informationen zur Interaktion der Besucherinnen und Besucher mit den URLs.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in einer SMS-Nachricht.

* **[!UICONTROL Klickrate]**:Anzahl der Benutzenden, die mit der SMS-Nachricht interagiert haben, in Prozent.

Das Widget **[!UICONTROL SMS – Versandstatistiken im Zeitverlauf]** enthält die wichtigsten Informationen zu den Nachricht in Form eines Graphen:

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten SMS-Nachrichten in Bezug auf die Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der Fehler und automatischen Rücksendeverarbeitungen im Verhältnis zur Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die die Zustellung an Profile verhindert haben.

Die Graphen und Tabellen **[!UICONTROL Ausschlussursachen]**, **[!UICONTROL Bounce-Ursachen]** und **[!UICONTROL Fehlerursachen]** zeigen, welche Fehler und Ausschlüsse aufgetreten sind.

+++

## Briefpost {#direct-mail}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_sending_statistics"
>title="Briefpost – Gesamtstatistik Versand"
>abstract="Die KPIs „Briefpost – Gesamtstatistik Versand“ enthalten wichtige Daten zu Ihren Nachrichten per Briefpost, wie „Angesprochen“ oder „Zugestellt“."

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_excluded_reasons"
>title="Ausgeschlossene Gründe"
>abstract="Die Graphen und die Tabelle „Ausgeschlossene Gründe“ veranschaulichen die verschiedenen Faktoren, die dazu führten, dass Benutzerprofile aus der Zielgruppe ausgeschlossen wurden und die Nachricht nicht erhielten."

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_error_reasons"
>title="Fehlerursachen"
>abstract="Anhand der Graphen und der Tabelle „Fehlerursachen“ können Sie die spezifischen Fehler identifizieren, die während des Versandvorgangs aufgetreten sind."

In den Kanalberichten werden im Menü „Briefpost“ die wichtigsten Informationen zu Briefpost-Nachrichten aufgeführt, die in Ihren Kampagnen und Journeys gesendet werden. Die Metriken werden nachfolgend beschrieben.

![](assets/direct_mail_channel_1.png)

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Briefpost-Bericht verfügbar sind.

Die Tabelle **[!UICONTROL Briefpost – Versandstatistiken gesamt]** gibt Auskunft über den Erfolg Ihrer Nachrichten:

* **[!UICONTROL Angesprochen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für die Briefpost-Nachrichten eignen.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die den Versand an Profile verhindert haben.

* **[!UICONTROL Fehlerrate]**: Prozentualer Anteil der aufgetretenen Fehler, die den Versand verhindert haben, im Vergleich zu den gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

* **[!UICONTROL Ausschlussrate]**: Prozentsatz der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

In den Graphen und Tabellen **[!UICONTROL Ausschlussursachen]** und **[!UICONTROL Fehlergründen]** wird angezeigt, welche Fehler und Ausschlüsse aufgetreten sind.
+++

## In-App {#in-app}

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement"
>title="In-App – Interaktionen insgesamt"
>abstract="Die KPIs „In-App – Interaktionen Insgesamt“ liefern umfassende Informationen über die Interaktion Ihrer Besucherinnen und Besucher mit Ihren In-App-Nachrichten, einschließlich Metriken wie „Impressions“ und „Interaktionen“."

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement_overtime"
>title="In-App – Interaktionen im Zeitverlauf"
>abstract="Der Graph „In-App – Interaktionen im Zeitverlauf“ verfolgt In-App-Impressions und Interaktionen, aufgeschlüsselt nach Stunden, Tagen, Wochen und Monaten."

In den Kanalberichten werden im Menü „In-App“ die wichtigsten Informationen zu In-App-Nachrichten aufgeführt, die in den Kampagnen und Journeys gesendet werden. Die Metriken werden nachfolgend beschrieben.

![](assets/inapp_channel_1.png)

+++  Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den In-App-Bericht verfügbar sind.

Die KPIs der **[!UICONTROL In-App-Interaktionen gesamt]** geben die wichtigsten Informationen bezüglich der Interaktion der Besucherinnen und Besucher mit den In-App-Nachrichten an, z. B.:

* **[!UICONTROL Impressions]**: Gesamtzahl der an alle Benutzenden gesendeten In-App-Nachrichten.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit der In-App-Nachricht. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks, Abbrechen oder andere Interaktionen.

* **[!UICONTROL Abbrüche]**: Gesamtzahl der In-App-Nachrichten, die von Profilen über die Schaltfläche „Schließen“ oder die automatische Verwerfungsfunktion verworfen wurden.

* **[!UICONTROL Abbruchrate]**: Prozentsatz der In-App-Nachrichten, die von Profilen verworfen wurden.

Die Grafik **[!UICONTROL In-App-Interaktionen im Zeitverlauf]** zeigt die Entwicklung der In-App-Impressions und -Interaktionen für den jeweiligen Zeitraum an, indem Impressions, Abbrechen oder Interaktionen verfolgt werden.

+++

## Web {#web}

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement"
>title="Web – Interaktionen insgesamt"
>abstract="Die KPIs „Web – Interaktionen insgesamt“ liefern umfassende Informationen über die Interaktion Ihrer Besucherinnen und Besucher mit Ihren Web-Seiten, einschließlich Metriken wie „Impressions“ und „Interaktionen“."

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement_overtime"
>title="Web – Gesamtinteraktionen im Zeitverlauf"
>abstract="Der Graph „Web – Interaktionen im Zeitverlauf“ verfolgt die Impressions und Interaktionen Ihrer Web-Seiten, aufgeschlüsselt nach Stunden, Tagen, Wochen und Monaten."

In den Kanalberichten werden im Menü „Web“ die wichtigsten Informationen zu Web-Seiten aufgeführt, die in Ihren Kampagnen und Journeys versendet wurden. Die Metriken werden nachfolgend beschrieben.

![](assets/web_channel_1.png)

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Web-Bericht verfügbar sind.

Die KPIs der **[!UICONTROL Web-Interaktionen gesamt]** geben die wichtigsten Informationen bezüglich der Interaktion der Besucherinnen und Besucher mit Ihren Web-Erlebnissen an, z. B.:

* **[!UICONTROL Impressions]**: Gesamtanzahl der für alle Benutzenden bereitgestellten Web-Erlebnisse.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit Ihrer Web-Seite. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks oder andere Interaktionen.

* **[!UICONTROL Abbrüche]**: Gesamtzahl der Web-Seiten, die von Profilen verworfen wurden.

* **[!UICONTROL Abbruchrate]**: Prozentsatz der Web-Seiten, die von Profilen verworfen wurden.

Der Graph **[!UICONTROL Web-Interaktion im Zeitverlauf]** enthält die wichtigsten Informationen zur Interaktion der Besucherinnen und Besucher mit Ihren Web-Seiten.

+++

## Kanalbericht (Video) {#channel-report-video}

In diesem Video gibt es weitere Informationen dazu, wie auf Kanalebene auf Berichte zugegriffen, darin navigiert und diese exportiert werden können.

>[!VIDEO](https://video.tv.adobe.com/v/3424537?quality=12)
