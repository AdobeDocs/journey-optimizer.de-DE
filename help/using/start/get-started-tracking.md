---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit dem Tracking in Journey Optimizer
description: Erfahren Sie mehr über die in Journey Optimizer verfügbaren Tracking- und Überwachungsfunktionen
feature: Monitoring
topic: Administration
role: User
level: Beginner
keywords: Tracking, Überwachen, Analysen, Reporting, Zustellbarkeit
source-git-commit: 94350929bc9a6c2d33ac551429b844b97be04ae5
workflow-type: tm+mt
source-wordcount: '1837'
ht-degree: 3%

---

# Erste Schritte mit dem Tracking in Journey Optimizer {#get-started-tracking}

Um aussagekräftige Erlebnisse zu schaffen und Ergebnisse zu erzielen, ist es von entscheidender Bedeutung zu verstehen, wie Kunden mit Ihrer Kommunikation interagieren. Journey Optimizer bietet umfassende Tracking- und Überwachungsfunktionen, die Ihnen Einblick in das Kundenverhalten, die Versandleistung und den Systemzustand geben - und dabei den Datenschutz respektieren und die Einhaltung von Vorschriften gewährleisten.

>[!BEGINSHADEBOX]

**Was Sie in Journey Optimizer verfolgen können:**

📧 **E-Mail** Interaktionen - Öffnungen, Klicks und Link-Leistung

🌐 **Webverhalten** - Seitenansichten, Klicks und Interaktionsmuster

🛤️ **Journey-**: Benutzerdefinierte Metriken, Schrittereignisse und Konversionspfade

📊 **Zustellbarkeitsstatus** - Bounce-Raten, Spam-Beschwerden und Reputation des Absenders

⚙️ **Systemvorgänge** - Warnhinweise, Fehler und benutzerdefinierte Aktionsleistung

>[!ENDSHADEBOX]

## Kundeninteraktionen kanalübergreifend verfolgen {#tracking-by-channel}

Journey Optimizer bietet kanalspezifische Tracking-Funktionen. Konfigurieren und verwenden Sie das Tracking für jeden Kanal.

### E-Mail-Tracking {#email-tracking}

Das E-Mail-Tracking wird beim Erstellen einer E-Mail-Nachricht automatisch aktiviert. Journey Optimizer verfolgt standardmäßig Öffnungen, Klicks und Abmeldungen - keine zusätzliche Konfiguration erforderlich.

**Tracking-Optionen konfigurieren:**

* **Tracking aktivieren/deaktivieren** - Kontrollieren Sie das Tracking auf Nachrichtenebene beim Entwerfen Ihrer E-Mail. Sie können Öffnungen, Klicks oder beides verfolgen. [Weitere Informationen](../email/message-tracking.md)

* **URL-Tracking-Parameter einrichten** - Konfigurieren von Tracking-Parametern auf Oberflächenebene, um automatisch Kampagnenkennungen (utm_campaign, utm_source usw.) an alle E-Mail-Links anzuhängen. Dies ermöglicht das Attributions-Tracking über Ihr gesamtes digitales Ökosystem. [Weitere Informationen](../email/url-tracking.md)

* **Verfolgen von Links in Fragmenten** - Alle Links in wiederverwendbaren Inhaltsfragmenten werden automatisch verfolgt, was eine vollständige Ansicht der Interaktion über freigegebene Inhaltskomponenten hinweg bietet.

* **Tracking der Mirrorseite hinzufügen** - Option „Aktivieren der Mirrorseite“, um eine Web-Version Ihrer E-Mail mit automatischem Tracking der Betrachter zu erstellen. [Weitere Informationen](../email/message-tracking.md#mirror-page)

**Überwachen der Leistung:** Echtzeitmetriken in Kampagnen- und Journey-Berichten anzeigen, einschließlich Öffnungen, Klicks und Leistung auf Link-Ebene. [Kampagnenberichte](../reports/campaign-global-report-cja-email.md) | [Journey-Berichte](../reports/journey-global-report-cja-email.md)

### Webtracking {#web-tracking}

Für das Webtracking ist eine explizite Konfiguration erforderlich, um Benutzerinteraktionen mit Ihren Web-Änderungen zu verfolgen.

**Klick-Tracking einrichten:**

Beim Entwerfen einer Web-Änderung können Sie bestimmte Elemente (Schaltflächen, Bilder, Links) auswählen, die Sie verfolgen möchten. Dies ermöglicht das Klick-Tracking für diese Elemente, ohne dass zusätzlicher Code erforderlich ist. [Weitere Informationen](../web/monitor-web-experiences.md)

* **Klickbare Elemente verfolgen** - Wählen Sie Schaltflächen, Bilder, Links oder ein beliebiges interaktives Element in Ihrer Web-Personalisierung aus.
* **Automatische Datenerfassung** - Nach der Konfiguration erfasst Journey Optimizer automatisch Klickereignisse und verknüpft sie mit Profilen
* **In Echtzeit überwachen** - Benutzerinteraktionen während der Überprüfung der Effektivität der Personalisierung verfolgen

**Tracking-Daten anzeigen** Zugriff auf Anzeigemetriken, Clickthrough-Raten und die Leistung auf Elementebene in Berichten. [Kampagnenberichte](../reports/campaign-global-report-cja-web.md) | [Journey-Berichte](../reports/journey-global-report-cja-web.md)

### Tracking von Push-Benachrichtigungen {#push-tracking}

Das Push-Tracking ist automatisch aktiviert und erfasst Impressionen (bereitgestellt), Klicks (getippt) und Öffnungen (App gestartet). Um den Tracking-Wert zu maximieren, konfigurieren Sie anklickbare Elemente in Ihrem Push-Inhalt.

**Konfigurieren von getrackten Elementen:**

* **Textkörper-Klickverhalten** - Legen Sie fest, was passiert, wenn Benutzer auf die Benachrichtigung tippen: Programm öffnen, zu einem Deeplink navigieren oder eine Web-URL öffnen. Jede Aktion wird automatisch verfolgt. [Weitere Informationen](../push/design-push.md#on-click-behavior)

* **Aktionsschaltflächen hinzufügen** - Schließen Sie bis zu 3 Schaltflächen (Android) oder mehrere Schaltflächen (iOS) mit unabhängigem Tracking für jede Schaltflächenaktion ein (offene App, Deeplink, Web-URL). [Weitere Informationen](../push/design-push.md#add-buttons-push)

* **Tracking aktivieren** - Überprüfen Sie, ob das Tracking in Ihrer Push-Journey-Aktivität oder in den Kampagnen-Tracking-Einstellungen aktiviert ist. [Weitere Informationen](../push/create-push.md#create)

>[!NOTE]
>
>Für das Push-Tracking ist die Implementierung von Mobile SDK erforderlich. Stellen Sie sicher, dass für Ihre App Adobe Experience Platform Mobile SDK ordnungsgemäß konfiguriert ist.

**Interaktion analysieren** Klickraten, Schaltflächenleistung und verfolgte Link-Details in Berichten anzeigen. [Kampagnenberichte](../reports/campaign-global-report-cja-push.md) | [Journey-Berichte](../reports/journey-global-report-cja-push.md)

### In-App-Nachrichten-Tracking {#inapp-tracking}

In-App-Nachrichten verfolgen automatisch Displays und Benutzerinteraktionen. Konfigurieren von Triggern und Inhalten zur Maximierung der Tracking-Effektivität

**Konfigurieren des Trackings:**

* **Anzeigeregeln einrichten** - Festlegen, wann und wo In-App-Nachrichten angezeigt werden, mithilfe von Triggern (App-Start, Laden des Bildschirms), Häufigkeitsregeln und Zielgruppenbedingungen. Die ordnungsgemäße Konfiguration gewährleistet eine genaue Verfolgung sowohl ausgelöster als auch angezeigter Nachrichten. [Weitere Informationen](../in-app/create-in-app.md)

* **Getrackte Elemente hinzufügen** - Schließen Sie Schaltflächen, Links und interaktive Elemente in Ihren Nachrichteninhalt ein. Jede Interaktion wird automatisch mit detaillierten Beschriftungen verfolgt.

* **Anzeigezeitpunkt optimieren** - Konfigurieren Sie Wochentag- und Tageszeitregeln, um die Wahrscheinlichkeit zu maximieren, dass ausgelöste Nachrichten Benutzern tatsächlich angezeigt werden.

**Was nachverfolgt wird:** Journey Optimizer erfasst automatisch Displays, Schaltflächenklicks, Abweisungen, ausgelöste und angezeigte Metriken sowie die Link-Performance. [Kampagnenberichte](../reports/campaign-global-report-cja-inapp.md) | [Journey-Berichte](../reports/journey-global-report-cja-inapp.md)

### SMS- und MMS-Tracking {#sms-tracking}

Für das SMS-Tracking ist eine minimale Einrichtung erforderlich: Journey Optimizer verkürzt und verfolgt automatisch Links, die Sie in Nachrichten einfügen.

**Funktionsweise:**

* **Automatisches Linktracking** - Fügen Sie mithilfe der URL-Hilfsfunktion beliebige URLs zu Ihrem SMS-Inhalt hinzu. Journey Optimizer verkürzt den Link automatisch und verfolgt Klicks ohne zusätzliche Konfiguration. Um die URL-Verkürzung zu verwenden, müssen Sie zunächst eine SMS-Subdomain konfigurieren. [Weitere Informationen](../sms/create-sms.md#sms-content)

* **Tracking eingehender Nachrichten** - Antworten von Empfängern werden automatisch erfasst, sodass Sie bidirektionale Konversationen und Antwortmuster überwachen können.

**Anzeigen von Metriken:** Zugriff auf Link-Klickdaten, Volumina eingehender Nachrichten und Leistungstypen von Nachrichten in Berichten. [Kampagnenberichte](../reports/campaign-global-report-cja-sms.md) | [Journey-Berichte](../reports/journey-global-report-cja-sms.md)

### Code-basiertes Erlebnis-Tracking {#code-based-tracking}

Code-basierte Erlebnisse erfordern eine Einrichtung der Implementierung, um Tracking-Daten an Adobe Experience Platform zu senden.

**Voraussetzungen:**

Bevor das Tracking funktioniert, müssen Sie Ihre Implementierung konfigurieren, um Interaktionsereignisse (Anzeigen, Klicks) an Adobe Experience Platform zu senden. Dies erfordert Folgendes:

* Einrichten eines für Adobe Experience Platform konfigurierten Datenstroms
* Implementieren der Ereigniserfassung in Ihrem Code mit Web SDK oder Mobile SDK
* Senden von Interaktionsereignissen bei Vorschlägen, wenn Benutzer personalisierte Inhalte anzeigen oder klicken

[Weitere Informationen zu den Voraussetzungen für die Implementierung](../code-based/code-based-prerequisites.md#reporting-prerequisites)

**Was nachverfolgt wird:** Nach der Implementierung werden Anzeigen, Klicks, Clickthrough-Raten und die Leistung auf Elementebene auf allen digitalen Touchpoints (Websites, Mobile Apps, IoT-Geräte usw.) verfolgt. [Kampagnenberichte](../reports/campaign-global-report-cja-code.md) | [Journey-Berichte](../reports/journey-global-report-cja-code.md)

### Tracking von Inhaltskarten {#content-card-tracking}

Inhaltskarten verfolgen Benutzerinteraktionen automatisch. Konfigurieren Sie Inhalts- und Anzeigeregeln zur Steuerung des Tracking-Verhaltens.

**Implementierung:**

* **Gestalten getrackter Inhalte** - Hinzufügen von Schaltflächen und Links zu Ihrer Inhaltskarte. Jedes interaktive Element wird automatisch mit Kennzeichnungen und URLs verfolgt.

* **Persistenz konfigurieren** - Inhaltskarten bleiben über Anwendungssitzungen hinweg erhalten, sodass Sie langfristige Interaktionsmuster verfolgen können. Legen Sie Ablaufregeln fest, um zu steuern, wie lange Karten verfolgbar bleiben.

* **Anzeigeregeln einrichten** - Legen Sie fest, wann und wo Karten angezeigt werden, um eine genaue Verfolgung von Anzeigen und Interaktionen sicherzustellen.

**Überwachen der Interaktion:** Verfolgen Sie Anzeigen, Klicks, Clickthrough-Raten und Interaktionsmuster über mehrere Sitzungen hinweg. [Kampagnenberichte](../reports/campaign-global-report-cja-content.md) | [Journey-Berichte](../reports/journey-global-report-cja-content.md)

## Überwachen von Landingpages {#landing-page-tracking}

Landingpages verfügen über ein integriertes Tracking, das keine zusätzliche Einrichtung erfordert. Journey Optimizer erfasst automatisch Besuche, Konversionen und Bounce-Raten.

**Was automatisch verfolgt wird:**

* **Besuche** - Gesamtzahl und eindeutige Besuche zur Messung der Reichweite
* **Konversionen** - Formularübermittlungen, Abonnementbestätigungen oder andere definierte Aktionen
* **Absprungrate** - Prozentsatz der Besucherinnen und Besucher, die das Programm verlassen, ohne zu interagieren
* **Leistungstrends** - Zeitreihendaten, die zeigen, wie sich Metriken entwickeln

**Leistung optimieren** Verwenden Sie Tracking-Daten, um Formularfelder zu verfeinern, Inhaltsvarianten zu testen, effektive Traffic-Quellen zu identifizieren und Abbrüche zu reduzieren. [Weitere Informationen](../reports/lp-report-global-cja.md)

## Journey- und Kampagnenaktivitäten tracken {#journey-campaign-tracking}

Konfigurieren Sie nicht nur das Tracking auf Kanalebene, sondern auch das Tracking, um die Gesamtleistung zu messen und das Kundenverhalten über Ihre Marketing-Initiativen hinweg zu verstehen.

**Einrichten des Kampagnen-Trackings:**
<!--
* **Configure optimization** - When setting up campaigns, enable experimentation or targeting to track which content variations perform best. [Learn more](../campaigns/campaigns-message-optimization.md)-->

* **Konversionsmetriken definieren** - Geben Sie an, welche Aktionen als Konversionen (Käufe, Anmeldungen, Downloads) gezählt werden sollen, um die Kampagneneffektivität über die Interaktionsmetriken hinaus zu messen.

* **Zeitplan einrichten** - Konfigurieren der Sendezeitoptimierung, um die Leistung über verschiedene Zeitstrategien hinweg zu verfolgen und optimale Versandfenster zu identifizieren. [Weitere Informationen](../building-journeys/send-time-optimization.md)

**Einrichten des Journey-Trackings:**

* **Definieren von benutzerdefinierten Erfolgsmetriken** - Konfigurieren Sie spezifische KPIs, die neben den standardmäßigen Interaktionsmetriken auch auf Ihre Geschäftsziele (Käufe, Anmeldungen, Erneuerungen usw.) abgestimmt sind. [Weitere Informationen](../building-journeys/success-metrics.md)

* **Journey-Schrittereignisse aktivieren** - Aktiviert das detaillierte Tracking jeder Aktion, die Kundinnen und Kunden beim Durchlaufen von Journeys ausführen. Dies bietet eine granulare Sichtbarkeit von Ein-/Ausstiegspunkten, Pfadauswahl und Ablageorten. [Weitere Informationen](../reports/journey-step-events-overview.md)

* **Überwachung benutzerdefinierter Aktionen konfigurieren** - Richten Sie das Tracking für Integrationen mit externen Systemen ein, um API-Aufrufe, Antwortzeiten und Fehlermuster zu überwachen. [Weitere Informationen](../action/reporting.md)

* **Benutzerdefiniertes Reporting und Datenexport** - Erstellen Sie maßgeschneiderte Berichte und exportieren Sie Tracking-Daten zur genaueren Analyse in externe Systeme. [Weitere Informationen](../reports/sharing-overview.md)

**Einheitliche Leistung anzeigen:** Sie auf umfassende Berichte für -Kampagnen und -Journey zu, um die Leistung über E-Mail, Push, SMS und andere Kanäle hinweg zu vergleichen und zu verstehen, welche Kombinationen die besten Ergebnisse erzielen. [Kampagnenberichte](../reports/campaign-global-report-cja.md) | [Journey-Berichte](../reports/journey-global-report-cja.md)

## Verwalten der Optimierungsleistung {#optimization-tracking}

Journey Optimizer verfolgt Optimierungsexperimente und Zielgruppenbestimmungsstrategien automatisch. Konfigurieren Sie Ihre Optimierungen, um eine ordnungsgemäße Datenerfassung sicherzustellen.

**Optimierungs-Tracking einrichten:**

* **Experiment konfigurieren** - Beim Erstellen von Experimenten oder beim Verwenden von Targeting definieren Sie, welche Metriken verfolgt werden sollen (Konversionen, Klicks, benutzerdefinierte Ereignisse). Journey Optimizer erfasst automatisch Leistungsdaten für jede Abwandlung. [Weitere Informationen](../campaigns/campaigns-message-optimization.md)

* **Pfadoptimierung einrichten** - Fügen Sie eine Aktivität **Optimieren** zu Ihrem Journey hinzu und konfigurieren Sie mehrere Pfade. Journey Optimizer verfolgt automatisch, welche Pfade Profile verwenden, und misst die Leistung. [Weitere Informationen](../building-journeys/optimize.md)

**Ergebnisse analysieren** Konversionsraten, statistische Signifikanz und Steigerung zwischen Behandlungen in Experimentationsberichten anzeigen. [Kampagnenberichte](../reports/campaign-global-report-cja-experimentation.md) | [Journey-Berichte](../reports/journey-global-report-cja-experimentation.md)

## Tracking der Entscheidungsleistung {#decisioning-tracking}

Bei Verwendung von Decisioning zur Personalisierung von Inhalten verfolgt Journey Optimizer automatisch Entscheidungsereignisse, Impressionen und Klicks, ohne dass eine zusätzliche Konfiguration erforderlich ist.

**Funktionsweise des Trackings:**

* **Automatische Ereigniserfassung** - Journey Optimizer erfasst automatisch Entscheidungsereignisse, wenn ein Entscheidungselement für ein Profil ausgewählt wird.
* **Impression-Tracking** - Bei E-Mails werden Impressionen automatisch verfolgt. Für Code-basierte Erlebnisse müssen Sie Vorschlagsanzeigeereignisse in Ihrem Code implementieren.
* **Klick-Tracking** - Klicks auf Entscheidungselemente werden automatisch in E-Mails verfolgt. Codebasierte Erlebnisse erfordern die Implementierung von Klick-Ereignissen.

**Voraussetzungen für das Code-basierte Tracking:**

Um die Entscheidungsfindung in Code-basierten Erlebnissen zu verfolgen, stellen Sie sicher, dass Ihre Implementierung Interaktionsereignisse (Anzeigen und Klicks) für Vorschläge mithilfe von Web SDK oder Mobile SDK an Adobe Experience Platform sendet. [Weitere Informationen](../experience-decisioning/gs-experience-decisioning.md)

**Leistung analysieren:** Anzeigen von Entscheidungs-KPIs, Vergleichen von Entscheidungselementen, Analysieren von Auswahlstrategien und Überwachen der KI-Modellleistung in Berichten. [Weitere Informationen](../experience-decisioning/cja-reporting.md)

## Datennutzung kontrollieren {#data-governance}

Mit Data-Governance-Richtlinien können Sie steuern, wie Tracking-Daten in Ihrer gesamten Organisation verwendet werden können:

* **Kennzeichnen sensibler Tracking-Daten** - Wenden Sie Governance-Kennzeichnungen auf verfolgte Verhaltensdaten an (z. B. Klicks auf Gesundheitsinhalte, Interaktionen mit Finanzprodukten), um sie als sensibel oder reguliert zu kennzeichnen.

* **Datennutzung beschränken** - Erstellen Sie Richtlinien, die verhindern, dass gekennzeichnete Tracking-Daten auf bestimmten Kanälen verwendet, in Drittanbietersysteme exportiert oder für bestimmte Personalisierungsszenarien verwendet werden.

* **Automatische Durchsetzung** - Journey Optimizer überprüft automatisch Governance-Richtlinien, wenn Sie Journey und Kampagnen erstellen, und blockiert die Veröffentlichung, wenn getrackte Daten unter Verstoß gegen definierte Richtlinien verwendet werden.

Data Governance stellt die Einhaltung von Vorschriften wie der DSGVO und des CCPA sicher und ermöglicht es Ihnen gleichzeitig, das Kundenverhalten innerhalb genehmigter Grenzen zu verfolgen und zu analysieren. [Weitere Informationen](../action/action-privacy.md)

## Überwachen der Zustellbarkeit und des Systemstatus {#monitoring-capabilities}

Neben der Verfolgung von Interaktionen konfigurieren Sie die Überwachung, um sicherzustellen, dass Nachrichten Posteingänge erreichen und Systeme eine optimale Leistung erzielen.

**Einrichten einer proaktiven Überwachung:**

* **Warnhinweise konfigurieren** - Richten Sie Echtzeitbenachrichtigungen für Journey-Fehler, Fehler bei benutzerdefinierten Aktionen und kritische Probleme ein, um schnell auf Probleme zu reagieren. [Weitere Informationen](../reports/alerts.md)

* **Auditprotokolle aktivieren** - Aktiviert die Auditprotokollierung, um alle Aktionen auf Ressourcen für die Compliance und Fehlerbehebung zu verfolgen. [Weitere Informationen](../privacy/audit-logs.md)

* **Integrationen überwachen** - Verfolgen Sie die Leistung von benutzerdefinierten Aktionen und die externe Systemkonnektivität, um Integrationsprobleme frühzeitig zu erkennen. [Weitere Informationen](../action/reporting.md)

**Zustellbarkeits-Monitoring:**

* **Unterdrückungslisten überprüfen** regelmäßig, um zu verstehen, warum Adressen blockiert werden, und um die Listenhygiene aufrechtzuerhalten. [Weitere Informationen](../reports/suppression-list.md)

* **Analysieren von Versandfehlern** um Fehler zu diagnostizieren und Abhilfemaßnahmen zu ergreifen. [Weitere Informationen](../configuration/email-error-types.md)

* **Befolgen Sie die Best** für DMARC, SPF und DKIM, um die Platzierung im Posteingang zu maximieren. [Weitere Informationen](../reports/deliverability.md)

## Nächste Schritte: Zugriff auf Tracking-Daten {#access-tracking-data}

Sobald das Tracking konfiguriert ist, können Sie über die integrierten Reporting-Funktionen von Journey Optimizer auf Ihre Daten zugreifen:

* **Echtzeit-Monitoring** - Anzeigen von Live-Metriken während der Ausführung von Journey und Kampagnen, um Probleme schnell zu identifizieren
* **Historische Analyse** - Analysieren Sie die Leistung in der Vergangenheit, um Trends zu verstehen und zukünftige Kampagnen zu optimieren
* **Erweiterte Analyse** - Verbindung zu Customer Journey Analytics für eine ausgefeilte kanalübergreifende Analyse und Attributionsmodellierung

[Erste Schritte mit Reporting](../reports/gs-reports.md) | [Erfahren Sie mehr über die Integration von Customer Journey Analytics](../reports/cja-ajo.md)

## Wichtige Themen erkunden {#explore-topics}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="../building-journeys/success-metrics.md">
    <img alt="Metriken" src="../assets/do-not-localize/success-metrics.jpeg">
    </a>
    <div>
    <a href="../building-journeys/success-metrics.md"><strong>Konfigurieren von Erfolgsmetriken</strong></a>
    </div>
    <p>
    <em>Verfolgen Sie benutzerdefinierte KPIs, die auf Ihre Geschäftsziele abgestimmt sind</em>
    <p>
  </td>
  <td>
    <a href="../reports/deliverability.md">
    <img alt="Zustellbarkeit" src="../assets/do-not-localize/deliverability.jpeg">
    </a>
    <div>
    <a href="../reports/deliverability.md"><strong>Zustellbarkeit überwachen</strong></a>
    </div>
    <p>
    <em>Stellen Sie sicher, dass Ihre Nachrichten die Posteingänge Ihrer Kunden erreichen</em>
    <p>
  </td>
  <td>
    <a href="../reports/gs-reports.md">
    <img alt="Reporting" src="../assets/do-not-localize/reporting.jpeg">
    </a>
    <div>
    <a href="../reports/gs-reports.md"><strong>Erkunden von Berichten</strong></a>
    </div>
    <p>
    <em>Zugreifen auf Live- und Verlaufsberichte für Ihre Journey und Kampagnen</em>
    <p>
  </td>
</tr>
</table>

