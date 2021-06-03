---
title: Globaler Bericht zur Journey
description: Erfahren Sie, wie Sie Daten aus dem globalen Bericht zur Journey verwenden
source-git-commit: f04e73187439462fc1e22c6c66398a139fbeaa5a
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 98%

---

# Globaler Bericht zur Journey {#journey-global-report}

![](../assets/do-not-localize/badge.png)

Über den Button **[!UICONTROL Globaler Bericht]** können Sie direkt von Ihrer Journey auf den globalen Bericht zur Journey zugreifen.

![](../assets/global_report_1.png)

Die Seite **[!UICONTROL Globaler Bericht]** zur Journey wird mit den folgenden Registerkarten angezeigt:

* [Journey](#journey-global)
* [E-Mail ](#email-global)
* [Push-Benachrichtigung](#push-global)

Der **[!UICONTROL Globale Bericht]** zur Journey ist in verschiedene Widgets unterteilt, die den Erfolg und die Fehler Ihrer Journey detailliert beschreiben. Jedes Widget kann bei Bedarf angepasst oder gelöscht werden. Weiterführende Informationen dazu finden Sie in diesem [Abschnitt](global-report.md#modify-dashboard).

## Registerkarte Journey {#journey-global}

In Ihrem **[!UICONTROL Globalen Bericht]** zur Journey erhalten Sie auf der Registerkarte **[!UICONTROL Journey]** eine übersichtliche Darstellung der wichtigsten Tracking-Daten zu Ihrer Journey.

![](../assets/global_report_2.png)

Mit dem Widget **[!UICONTROL Performance der Journey]** können Sie den Weg Ihrer Zielprofile durch Ihre Journey Schritt für Schritt anzeigen.

Das Widget **[!UICONTROL Statistiken der Journey]** zeigt die folgenden KPIs an:

* **[!UICONTROL Eingetretene Profile]**: Gesamtzahl der Personen, die das Eintrittsereignis der Journey erreicht haben.

* **[!UICONTROL Ausgetretene Profile]**: Gesamtzahl der Personen, die die Journey verlassen haben.

* **[!UICONTROL Fehlgeschlagene individuelle Journey]**: Gesamtzahl der individuellen Journeys, die nicht erfolgreich ausgeführt wurden.

Mit den Widgets **[!UICONTROL Performance des Ereignisses]** und **[!UICONTROL Top-Ereignisse]** können Sie über Diagramme und Tabellen sehen, welches Ihrer **[!UICONTROL Ereignisse]** erfolgreich ausgeführt wurde.

Die Widgets **[!UICONTROL Performance der Aktion]** und **[!UICONTROL Top-Aktionen]** stellen die erfolgreichsten Aktionen und Fehler dar, die beim Auslösen Ihrer  **[!UICONTROL Aktionen]** aufgetreten sind. Die Tabelle **[!UICONTROL Top-Aktionen]** enthält die für **[!UICONTROL Aktionen]** verfügbaren Daten, z. B.:

* **[!UICONTROL Erfolgreich ausgeführte Aktionen]**: Gesamtanzahl der **[!UICONTROL Aktionen]**, die für eine Journey erfolgreich ausgeführt wurden.

* **[!UICONTROL Fehler in Aktion]**: Gesamtanzahl der Fehler, die bei **[!UICONTROL Aktionen]** aufgetreten sind.

Das Diagramm **[!UICONTROL Fehlergründe]** zeigt den Typ der Fehler an, die bei **[!UICONTROL Aktionen]** aufgetreten sind.

<!--Events by origin-->

## Registerkarte „E-Mail“ {#email-global}

In Ihrem **[!UICONTROL Globalen Bericht]** zur Journey finden Sie auf der Registerkarte **[!UICONTROL E-Mail]** die wichtigsten Informationen zu den E-Mail-Versänden, die in Ihrer Journey gesendet wurden.

Einen ausführlichen Bericht zu einem bestimmten E-Mail-Versand finden Sie im Abschnitt [Globaler E-Mail-Bericht](#email-global-report).

Im Diagramm **[!UICONTROL E-Mail-Sendestatistik]** wird der Erfolg Ihres Versands beschrieben:

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten für den Versand.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Versandrate]**: Prozentsatz der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der über den Versand und der automatischen Bounce-Verarbeitung hinweg kumulierten Fehler im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounce-Rate]**: Prozentualer Anteil der E-Mails, die unzustellbar waren, im Vergleich zu den gesendeten E-Mails.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während eines Versands aufgetreten sind und das Versenden an Profile verhinderten.

* **[!UICONTROL Fehlerrate]**: Prozentualer Anteil der Fehler, die bei einem Versand aufgetreten sind und den Versand verhindert haben, im Vergleich zu den versendeten E-Mails.

Die **[!UICONTROL E-Mail-Tracking-Statistiken]** enthalten die verfügbaren Daten für die Aktivität der Empfänger für Ihren Versand:

* **[!UICONTROL Öffnungen]**: Gibt an, wie oft die zugestellte Nachricht in einem Versand geöffnet wurde.

* **[!UICONTROL Eindeutige Öffnungen]**: Prozentsatz der geöffneten zugestellten Nachrichten.

* **[!UICONTROL Öffnungsrate]**: Gesamtzahl der geöffneten Nachrichten im Vergleich zu den versendeten E-Mails.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in einer E-Mail.

* **[!UICONTROL Eindeutige Klicks]**: Die Anzahl der Empfänger, die einen Inhalt in einem Versand angeklickt haben.

* **[!UICONTROL Durchklickrate]**: Prozentsatz der Benutzer, die mit der Journey interagiert haben.

Das Diagramm **[!UICONTROL Sendestatistiken]** enthält die Daten, die für gesendete E-Mails verfügbar sind, z. B.:

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der über den Versand und der automatischen Bounce-Verarbeitung hinweg kumulierten Fehler im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während eines Versands aufgetreten sind und das Versenden an Profile verhinderten.

Die Widgets **[!UICONTROL Gründe für Bounces]** und **[!UICONTROL Bounce-Kategorien]** enthalten die verfügbaren Daten zu unzustellbaren Nachrichten, wie:

* **[!UICONTROL Hardbounce]**: die Gesamtzahl der permanenten Fehler, wie eine falsche E-Mail-Adresse. Dabei handelt es sich um eine Fehlermeldung, die explizit angibt, dass die Adresse ungültig ist, z. B. Unbekannter Benutzer.

* **[!UICONTROL Softbounce]**: die Gesamtzahl der temporären Fehler, wie eine volle Inbox.

* **[!UICONTROL Ignoriert]**: Die Gesamtzahl der temporären Ereignisse, z. B. Abwesenheitsnotiz, oder ein technischer Fehler, z. B. wenn der Absendertyp Postmaster ist.

Weiterführende Informationen zu Bounces finden Sie auf der Seite [Unterdrückungsliste](../suppression-list.md) .

Das Diagramm **[!UICONTROL E-Mail – Top-URL]** und die Tabellendetails, welche URLs aus Ihrem Versand am häufigsten besucht werden.

Das Diagramm **[!UICONTROL E-Mail – Beste Empfänger-Domain]** und die Tabellendetails, welche Domains von Empfängern am häufigsten zum Öffnen der E-Mail verwendet werden.

## Registerkarte „Push-Benachrichtigung“ {#push-global}

In Ihrem **[!UICONTROL Globalen Bericht]** zur Journey finden Sie auf der Registerkarte **[!UICONTROL Push-Benachrichtigung]** die wichtigsten Informationen zu den Push-Versänden, die in Ihrer Journey gesendet wurden.

Einen ausführlichen Bericht zu einem bestimmten Push-Versand finden Sie im [Globalen Bericht zu Push-Benachritigungen](#push-global-report).

Die Tabelle **[!UICONTROL Push-Benachrichtigung – Sendestatistiken]** enthält die wichtigsten Informationen zu Ihren Push-Benachrichtigungen mit Diagrammen und KPIs:

* **[!UICONTROL Gesendet]**: Gesamtzahl der gesendeten Nachrichten für den Versand.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Versandrate]**: Prozentsatz der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der über den Versand und der automatischen Bounce-Verarbeitung hinweg kumulierten Fehler im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounce-Rate]**: Prozentsatz der Push-Benachrichtigungen, die unzustellbar waren, im Vergleich zu den gesendeten Push-Benachrichtigungen.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während eines Versands aufgetreten sind und das Versenden an Profile verhinderten.

* **[!UICONTROL Fehlerrate]**: Prozentualer Anteil der Fehler, die während eines Versands aufgetreten sind und den Versand verhindert haben, im Vergleich zu den gesendeten Push-Benachrichtigungen.

Die **[!UICONTROL Push-Benachrichtigung – Tracking-Statistik]** enthält die verfügbaren Daten zur Aktivität der Empfänger für Ihren Versand:

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen einer Nachricht in einem Versand.

* **[!UICONTROL Öffnungsrate]**: Prozentsatz der geöffneten Push-Benachrichtigungen.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der versendeten Push-Benachrichtigung durchgeführt wurden, z. B. Button-Klick oder Abbruch.

* **[!UICONTROL Interaktionen]**: Gesamtanzahl der Öffnnungen und Aktionen für diese Push-Benachrichtigung, d. h. wenn das Profil die Push-Benachrichtigung geöffnet hat oder auf einen Button geklickt wurde.

* **[!UICONTROL Interaktionsrate]**: Prozentsatz der Öffnungen und Aktionen für diese Push-Benachrichtigung, d. h. wenn das Profil die Push-Benachrichtigung geöffnet hat oder auf einen Button geklickt wurde.

Das Diagramm **[!UICONTROL Zusammenfassung der Push-Benachrichtigung]** enthält die Daten, die für gesendete Push-Benachrichtigungen verfügbar sind, z. B.:

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen einer Nachricht in einem Versand.

* **[!UICONTROL Aktionen]**: Gesamtzahl der Aktionen, die bei der versendeten Push-Benachrichtigung durchgeführt wurden, z. B. Button-Klick oder Abbruch.

* **[!UICONTROL Bounces]**: Gesamtzahl der über den Versand und der automatischen Bounce-Verarbeitung hinweg kumulierten Fehler im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Zugestellt]**: Zahl der erfolgreich gesendeten Nachrichten im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während eines Versands aufgetreten sind und das Versenden an Profile verhinderten.

In der Grafik und Tabelle **[!UICONTROL Fehlergründe]** können Sie sehen, welcher Fehler während des Versands aufgetreten ist.

Die Diagramme und Tabellen **[!UICONTROL Tracking nach Plattform]**, **[!UICONTROL Senden nach Plattform]** und **[!UICONTROL Aufschlüsselung nach Plattform]** geben einen Überblick über den Erfolg Ihrer Push-Benachrichtigung, je nach Betriebssystem Ihres Empfängers.
