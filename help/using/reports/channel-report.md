---
solution: Journey Optimizer
product: journey optimizer
title: Berichte auf Kanalebene
description: Erfahren Sie, wie Sie Daten aus den Kanalberichten verwenden.
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 7c56deac0deb0863fff5ad9416d69f632f92acc8
workflow-type: tm+mt
source-wordcount: '1866'
ht-degree: 26%

---

# Kanalberichte {#channel-report}

>[!CONTEXTUALHELP]
>id="ajo_channel_level_report"
>title="Bericht auf Kanalebene"
>abstract="Die Kanalberichte bieten einen umfassenden Überblick über Traffic- und Interaktionsmetriken über alle Kanäle hinweg. Ihre Berichte sind in verschiedene Widgets unterteilt, in denen Sie Details zu Ihrer Kampagne sowie zu Journey und Erfolgen und Fehlern finden. Jedes Reporting-Dashboard kann durch Ändern der Größe oder Entfernen von Widgets verändert werden."

>[!IMPORTANT]
>
> So greifen Sie auf die **Bericht** Menü, müssen Sie über die **[!UICONTROL Anzeigen von Kanalberichten]** -Berechtigung. [Weitere Informationen](channel-report-gs.md#before-starting-manage-reports-prereq)

Die Kanalberichte bieten Benutzern einen umfassenden Überblick über Traffic- und Interaktionsmetriken auf Kanalebene. Die Metriken werden aggregiert, um konsolidierte Werte für Aktionen aus dem ausgewählten Kanal darzustellen, die sich über verschiedene Kampagnen und Journey erstrecken.

Sie können auf die Kanalberichte zugreifen, indem Sie zur **Berichte** innerhalb des **Journey-Management** Abschnitt. Es ist vollständig anpassbar. Sie können Ihre Daten nach Berichtsdatum oder Aktion filtern. [Weitere Informationen](channel-report-gs.md)

Die Berichtseite wird mit den folgenden Registerkarten angezeigt:

* [E-Mail](#email)
* [Push-Benachrichtigung -Benachrichtigungen](#push)
* [SMS](#sms)
* [In-App](#inapp)
* [Web](#web)
* [Briefpost](#direct-mail)

➡️ [Entdecken Sie diese Funktion im Video](#channel-report-video)


## E-Mail {#email}


In den Kanalberichten werden im Menü E-Mail die wichtigsten Informationen zu E-Mails aufgeführt, die in Ihren Kampagnen und Journey gesendet werden. Die Metriken werden nachfolgend beschrieben.

![](assets/email_channel_1.png)

+++  Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den E-Mail-Bericht verfügbar sind.

Die **[!UICONTROL Versandstatistiken für E-Mail]** -Diagramm zeigt den Erfolg Ihrer E-Mails:

* **[!UICONTROL Targeting]**: Gesamtzahl der verarbeiteten E-Mails.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten E-Mails in Bezug auf die Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zustellrate]**: Prozentsatz der erfolgreich gesendeten E-Mails.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der E-Mails, die nicht erfolgreich zugestellt wurden, im Vergleich zur Zahl der gesendeten E-Mails.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die den Versand an Profile verhinderten.

* **[!UICONTROL Fehlerrate]**: Prozentsatz der Fehler, die den Versand verhindert haben, in Bezug auf die gesendeten E-Mails.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

* **[!UICONTROL Ausschlussrate]**: Prozentsatz der Profile, die von Adobe Journey Optimizer ausgeschlossen wurden.

Die **[!UICONTROL Trackingstatistiken in E-Mails]** -Widget enthält die verfügbaren Daten für die Empfängeraktivität für Ihre E-Mails:

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen der Nachricht.

* **[!UICONTROL Öffnungsrate]**: Gesamtzahl der geöffneten Nachrichten im Vergleich zu den versendeten E-Mails.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in einer Nachricht.

* **[!UICONTROL Klickrate]**: Prozentsatz der Benutzer, die mit der E-Mail interagiert haben.

* **[!UICONTROL Beschwerden wegen Spam]**: Gibt an, wie oft eine Nachricht als Spam oder Junk gekennzeichnet wurde.

* **[!UICONTROL Spam-Beschwerderate]**: Prozentsatz der als Spam oder Junk deklarierten Nachrichten in Bezug auf die Anzahl der gesendeten E-Mails.

* **[!UICONTROL Abmeldungen]**: Anzahl der Klicks auf den Anmelde-Link.

* **[!UICONTROL Abmelderate]**: Prozentsatz der Abmeldungen in Bezug auf die Anzahl der gesendeten E-Mails.

Die **[!UICONTROL Versand von Statistiken im Zeitverlauf]** -Diagramm enthält die für gesendete E-Mails verfügbaren Daten, z. B.:

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten E-Mails in Bezug auf die Gesamtzahl der gesendeten E-Mails.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten E-Mails

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die den Versand an Profile verhinderten.

Die **[!UICONTROL Überstunden der E-Mail-Trackingstatistiken]** -Diagramm enthält die Daten, die für Öffnungen und Klicks verfügbar sind.

Die Widgets **[!UICONTROL Bounce-Gründe]** und **[!UICONTROL Bounce-Kategorien]** enthalten die verfügbaren Daten zu unzustellbaren Nachrichten wie:

* **[!UICONTROL Hardbounce]**: die Gesamtzahl der permanenten Fehler, wie eine falsche E-Mail-Adresse. Dazu gehören Fehlermeldungen, die explizit eine ungültige Adresse anzeigen, wie etwa „Benutzer unbekannt“.

* **[!UICONTROL Softbounce]**: die Gesamtzahl der temporären Fehler, wie ein voller Posteingang.

* **[!UICONTROL Ignoriert]**: Die Gesamtzahl der temporären Ereignisse, beispielsweise Abwesenheit, oder technischer Fehler, zum Beispiel wenn der Absendertyp Postmaster ist.

Weitere Informationen zu Bounces finden Sie auf der Seite [ Unterdrückungslisten](../reports/suppression-list.md).

Die **[!UICONTROL Fehlerursachen]** Anhand von Diagrammen und Tabellen können Sie sehen, welcher Fehler aufgetreten ist.

Das Diagramm und die Tabelle **[!UICONTROL Ausschlussgründe]** zeigen die verschiedenen Gründe an, die verhindert haben, dass Nutzerprofile, die von den Zielprofilen ausgeschlossen wurden, die Nachricht erhalten haben.

Die **[!UICONTROL Bounce-Gründe nach Domain]**, **[!UICONTROL Gesendet und von Domänen bereitgestellt]**, **[!UICONTROL Öffnungen und Klicks nach Domain]**  und **[!UICONTROL Bounce und Fehler nach Domain]** Tabellen und Diagramme stellen die Aufschlüsselung aller wichtigen E-Mail-Versand- und Tracking-Daten auf Domänenebene dar.
+++

## Push-Benachrichtigung {#push}


In Ihren Kanalberichten werden im Menü Push-Benachrichtigung die wichtigsten Informationen zu Push-Benachrichtigungen aufgeführt, die in Ihren Kampagnen und Journey gesendet werden. Die Metrik wird nachfolgend beschrieben.

![](assets/push_channel_1.png)


+++  Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Push-Bericht verfügbar sind.

Die **[!UICONTROL Push-Benachrichtigungen - Versandstatistiken insgesamt]** -Tabelle enthält die wichtigsten Informationen zu Ihren Push-Benachrichtigungen mit Diagrammen und KPIs:

* **[!UICONTROL Targeting]**: Gesamtzahl der verarbeiteten Push-Benachrichtigungen.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Push-Benachrichtigungen in Bezug auf die Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Zustellrate]**: Prozentsatz der erfolgreich gesendeten Push-Benachrichtigungen

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der Push-Benachrichtigungen, die unzustellbar waren, im Vergleich zu den gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die den Versand an Profile verhinderten.

* **[!UICONTROL Fehlerrate]**: Prozentsatz der Fehler, die den Versand verhindert haben, in Bezug auf die gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

* **[!UICONTROL Ausschlussrate]**: Prozentsatz der Profile, die von Adobe Journey Optimizer ausgeschlossen wurden.

Die **[!UICONTROL Push-Benachrichtigung - Tracking-Statistiken insgesamt]** enthält die für die Empfängeraktivität verfügbaren Daten für Ihre Push-Benachrichtigungen:

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft eine Push-Benachrichtigung geöffnet wurde.

* **[!UICONTROL Öffnungsrate]**: Prozentsatz der geöffneten Push-Benachrichtigungen.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der gesendeten Push-Benachrichtigung durchgeführt wurden, d. h. Klick auf Schaltfläche oder Abbruch.

* **[!UICONTROL Aktionsrate]**: Prozentsatz der Aktionen, die bei gesendeten Push-Benachrichtigungen im Vergleich zu gesendeten Push-Benachrichtigungen durchgeführt werden.

* **[!UICONTROL Interaktionsrate]**: Prozentsatz der Öffnungen und Aktionen für diese Push-Benachrichtigung, d. h. wenn das Profil die Push-Benachrichtigung geöffnet hat oder auf eine Schaltfläche geklickt wurde.

Die **[!UICONTROL Push-Benachrichtigungen - Versandstatistiken im Zeitverlauf]** Das Diagramm enthält die Daten, die für gesendete Push-Benachrichtigungen verfügbar sind, z. B.:

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Push-Benachrichtigungen in Bezug auf die Gesamtzahl der gesendeten Push-Benachrichtigungen

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die den Versand an Profile verhinderten.

Das Diagramm und die Tabelle **[!UICONTROL Ausschlussgründe]** zeigen die verschiedenen Gründe an, die verhindert haben, dass Nutzerprofile, die von den Zielprofilen ausgeschlossen wurden, die Nachricht erhalten haben.

Die **[!UICONTROL Fehlerursachen]** Anhand von Diagrammen und Tabellen können Sie sehen, welcher Fehler aufgetreten ist.

Die **[!UICONTROL Tracking nach Plattform]** und **[!UICONTROL Versand nach Plattform]** Grafiken und Tabellen zeigen den Erfolg Ihrer Push-Benachrichtigung in Abhängigkeit vom Betriebssystem Ihres Empfängers.
+++

## SMS {#sms}


In den Kanalberichten werden im Menü SMS die wichtigsten Informationen zu SMS aufgeführt, die in Ihren Kampagnen und Journey versendet wurden. Die Metriken werden nachfolgend beschrieben.

![](assets/sms_channel_1.png)


+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den SMS-Bericht verfügbar sind.

Die **[!UICONTROL SMS - Versandstatistiken insgesamt]** in der Tabelle wird der Erfolg Ihrer SMS beschrieben:

* **[!UICONTROL Targeting]**: Anzahl der Benutzerprofile, die als Zielprofile für den SMS-Kanal gelten.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten SMS-Nachrichten in Bezug auf die Gesamtzahl der gesendeten SMS-Nachrichten

* **[!UICONTROL Zustellrate]**: Prozentsatz der erfolgreich gesendeten SMS-Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten SMS-Nachrichten

* **[!UICONTROL Absprungrate]**: Prozentsatz der Bounce-SMS-Nachrichten in Bezug auf die gesendeten SMS-Nachrichten

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die den Versand an Profile verhinderten.

* **[!UICONTROL Fehlerrate]**: Prozentsatz der Fehler, die den Versand verhindert haben, in Bezug auf die gesendeten SMS-Nachrichten.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

* **[!UICONTROL Ausschlussrate]**: Prozentsatz der Profile, die von Adobe Journey Optimizer ausgeschlossen wurden.

Die **[!UICONTROL SMS - Trackingstatistiken insgesamt]** Widget beschreibt die wichtigsten Informationen zur Interaktion Ihrer Besucher mit Ihren URLs:

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in der SMS-Nachricht.

* **[!UICONTROL Klickrate]**: Prozentsatz der Benutzer, die mit der SMS-Nachricht interagiert haben.

Die **[!UICONTROL SMS - Versandstatistiken im Zeitverlauf]** Widget erläutert die wichtigsten Informationen zu Ihrer Nachricht mit einem Diagramm:

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten SMS-Nachrichten in Bezug auf die Gesamtzahl der gesendeten SMS-Nachrichten

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten SMS-Nachrichten

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die den Versand an Profile verhinderten.

Die **[!UICONTROL Ausschlussgründe]**, **[!UICONTROL Bounces-Gründe]** und **[!UICONTROL Fehlerursachen]** Anhand von Diagrammen und Tabellen können Sie sehen, welcher Fehler und welche Ausschlüsse aufgetreten sind.

+++

## In-App {#in-app}


In Ihren Kanalberichten werden im Menü In-App die wichtigsten Informationen zu In-App-Nachrichten aufgeführt, die in Ihren Kampagnen und Journey gesendet werden. Die Metriken werden nachfolgend beschrieben.

![](assets/inapp_channel_1.png)


+++  Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den In-App-Bericht verfügbar sind.

Die **[!UICONTROL In-App-Gesamtinteraktion]** In KPIs werden die wichtigsten Informationen bezüglich der Interaktion Ihrer Besucher mit Ihren In-App-Nachrichten beschrieben, z. B.:

* **[!UICONTROL Impressionen]**: Gesamtzahl der In-App-Nachrichten, die an alle Benutzer gesendet wurden.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit Ihrer In-App-Nachricht. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks, Abbrechen oder andere Interaktionen.

* **[!UICONTROL Abweisungen]**: Gesamtzahl der In-App-Nachrichten, die von Benutzern verworfen wurden, indem diese entweder die Schließen-Schaltfläche oder die automatische Funktion zum Entfernen der Nachricht verwendet haben.

* **[!UICONTROL Abbruchrate]**: Prozentsatz der In-App-Nachrichten, die von Empfängern verworfen wurden.

Die **[!UICONTROL In-App-Interaktion im Zeitverlauf]** -Diagramm zeigt die Entwicklung Ihrer In-App-Impressionen und -Interaktionen für den betroffenen Zeitraum durch Tracking von Impressionen, Verwerfungen oder Interaktionen.

+++

## Web {#web}


In den Kanalberichten werden im Webmenü die wichtigsten Informationen zu den Webseiten aufgeführt, die in Ihren Kampagnen und Journey enthalten sind. Die Metriken werden nachfolgend beschrieben.

![](assets/web_channel_1.png)


+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Web-Bericht verfügbar sind.

Die **[!UICONTROL Interaktion insgesamt im Web]** In KPIs werden die wichtigsten Informationen im Zusammenhang mit der Interaktion Ihrer Besucher mit Ihren Web-Erlebnissen beschrieben, z. B.:

* **[!UICONTROL Impressionen]**: Gesamtzahl der für alle Benutzer bereitgestellten Weberlebnisse.

* **[!UICONTROL Interaktionen]**: Gesamtzahl der Interaktionen mit Ihrer Webseite. Dazu gehören alle von den Benutzenden durchgeführten Aktionen, wie z. B. Klicks oder andere Interaktionen.

* **[!UICONTROL Abweisungen]**: Gesamtzahl der Webseiten, die von Empfängern verworfen wurden.

* **[!UICONTROL Abbruchrate]**: Prozentsatz der Webseiten, die von Empfängern verworfen wurden.

Die **[!UICONTROL Webinteraktion im Zeitverlauf]** -Diagramm enthält die wichtigsten Informationen zur Interaktion Ihrer Besucher mit Ihren Webseiten.

+++

## Briefpost {#direct-mail}


In Ihren Kanalberichten werden im Menü Briefpost die wichtigsten Informationen zu den in Ihren Kampagnen und Journey gesendeten Briefpost-Nachrichten aufgeführt. Die Metriken werden nachfolgend beschrieben.

![](assets/direct_mail_channel_1.png)


+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Briefpost-Bericht verfügbar sind.
Die **[!UICONTROL Briefpost - Versandstatistiken insgesamt]** -Tabelle zeigt den Erfolg Ihrer Nachrichten:

* **[!UICONTROL Targeting]**: Anzahl der Benutzerprofile, die als Zielprofile für Ihre Briefpost-Nachrichten gelten.

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtzahl der aufgetretenen Fehler, die den Versand an Profile verhinderten.

* **[!UICONTROL Fehlerrate]**: Prozentsatz der Fehler, die den Versand verhindert haben, in Bezug auf die gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

* **[!UICONTROL Ausschlussrate]**: Prozentsatz der Profile, die von Adobe Journey Optimizer ausgeschlossen wurden.

Die **[!UICONTROL Ausschlussgründe]** und **[!UICONTROL Fehlerursachen]** Anhand von Diagrammen und Tabellen können Sie sehen, welcher Fehler und welche Ausschlüsse aufgetreten sind.
+++


## Anleitungsvideo {#channel-report-video}

In diesem Video erfahren Sie, wie Sie auf Kanalebene auf Berichte zugreifen, darin navigieren und diese exportieren können.

>[!VIDEO](https://video.tv.adobe.com/v/3424537?quality=12)
