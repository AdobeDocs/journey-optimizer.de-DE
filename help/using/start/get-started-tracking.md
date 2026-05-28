---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte beim Tracking in Journey Optimizer
description: Erfahren Sie mehr über die in Journey Optimizer verfügbaren Tracking- und Überwachungsfunktionen
feature: Monitoring
topic: Administration
role: User
level: Beginner
keywords: Tracking, Überwachen, Analysen, Reporting, Zustellbarkeit
exl-id: d5e7adb7-8473-4c29-8ae6-ba979aef97f3
TQID: https://experienceleague.adobe.com/jLHTNJlUPQm39EZvTLLBvYT92eGlCBoHpTKBfJ1Zxlk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c1579802-ddd4-4214-8a91-97b2066abe11id: c4147b6e-073b-4d3c-9ab1-d60f2f4434efid: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1964
ht-degree: 95%

---

# Erste Schritte beim Tracking in Journey Optimizer {#get-started-tracking}

Mit dem Tracking können Sie die Effektivität einer Kampagne messen, Kundenerlebnisse optimieren und sicherstellen, dass Nachrichten die vorgesehenen Empfängerinnen und Empfänger erreichen. Journey Optimizer bietet umfassende Tracking-Funktionen, mit denen Kundeninteraktionen, die Versandleistung und der Systemzustand erfasst werden. So können Sie datengestützte Entscheidungen treffen und gleichzeitig den Datenschutz respektieren und die Einhaltung von Vorschriften gewährleisten.

Das Tracking wird beim Erstellen von Nachrichten und Journeys größtenteils automatisch konfiguriert. Bei erweiterten Szenarien können Sie benutzerdefinierte Metriken einrichten, URL-Parameter konfigurieren und eine Integration mit externen Analyseplattformen vornehmen. Greifen Sie über integrierte Berichte auf Ihre Tracking-Daten zu oder exportieren Sie sie zur genaueren Analyse in Customer Journey Analytics.

>[!BEGINSHADEBOX]

Was Sie in Journey Optimizer nachverfolgen können:

📧 **E-Mail-Interaktionen** – Öffnungen, Klicks und Link-Leistung

🌐 **Web-Verhalten** – Seitenansichten, Klicks und Interaktionsmuster

🛤️ **Journey-Leistung** – Benutzerdefinierte Metriken, Schrittereignisse und Konversionspfade

📊 **Zustellbarkeitsstatus** – Bounce-Raten, Spam-Beschwerden und Reputation der Absendenden

⚙️ **Systemvorgänge** – Warnhinweise, Fehler und Leistung benutzerdefinierter Aktionen

>[!ENDSHADEBOX]

Für einen möglichst leichten Einstieg sollten Sie sich mit diesen grundlegenden Themen bezüglich Tracking und Überwachung befassen:

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
    <em>Verfolgen Sie benutzerdefinierter KPIs nach, die auf Ihre Geschäftsziele abgestimmt sind</em>
    <p>
  </td>
  <td>
    <a href="../reports/deliverability.md">
    <img alt="Zustellbarkeit" src="../assets/do-not-localize/deliverability.jpeg">
    </a>
    <div>
    <a href="../reports/deliverability.md"><strong>Überwachen der Zustellbarkeit</strong></a>
    </div>
    <p>
    <em>Stellen Sie sicher, dass Ihre Nachrichten die Posteingänge der Kundschaft erreichen</em>
    <p>
  </td>
  <td>
    <a href="../reports/gs-reports.md">
    <img alt="Reporting" src="../assets/do-not-localize/reporting.jpeg">
    </a>
    <div>
    <a href="../reports/gs-reports.md"><strong>Analysieren von Reporting</strong></a>
    </div>
    <p>
    <em>Greifen Sie auf Live- und Verlaufsberichte für Ihre Journeys und Kampagnen zu</em>
    <p>
  </td>
</tr>
</table>

## Kanalübergreifendes Nachverfolgen von Kundeninteraktionen {#tracking-by-channel}

Journey Optimizer bietet kanalspezifische Tracking-Funktionen. Hier finden Sie Informationen zur Konfiguration und Verwendung von Tracking für jeden Kanal.

+++E-Mail-Tracking

Das E-Mail-Tracking wird beim Erstellen einer E-Mail-Nachricht automatisch aktiviert. Journey Optimizer verfolgt standardmäßig Öffnungen, Klicks und Abmeldungen. Hierfür ist keine zusätzliche Konfiguration erforderlich.

**Konfigurieren von Tracking-Optionen:**

* **Aktivieren/deaktivieren von Tracking** – Steuern Sie das Tracking auf Nachrichtenebene beim Entwerfen Ihrer E-Mail. Sie können Öffnungen, Klicks oder beides nachverfolgen. [Weitere Informationen](../email/message-tracking.md)

* **URL-Tracking-Parameter einrichten** - Konfigurieren von Tracking-Parametern auf Oberflächenebene, um Kampagnenkennungen automatisch anzuhängen (utm_campaign, utm_source usw.) auf alle E-Mail-Links. Dies ermöglicht das Attributions-Tracking über Ihr gesamtes digitales Ökosystem. [Weitere Informationen](../email/url-tracking.md)

* **Tracking von Links in gespeicherten Fragmenten** – Wenn Sie ein Fragment aus Inhalten speichern, für die Tracking aktiviert ist, bleibt das Tracking der Links in diesem Fragment aktiv, wenn Sie es in anderen Journeys oder Kampagnen wiederverwenden. [Weitere Informationen](../content-management/save-fragments.md)

* **Hinzufügen von Mirror-Seiten-Tracking** – Aktivieren Sie die Option für die Mirror-Seite, um eine Web-Version Ihrer E-Mail mit automatischem Tracking der Betrachtenden zu erstellen. [Weitere Informationen](../email/message-tracking.md#mirror-page)

**Überwachen der Leistung:** Zeigen Sie Echtzeitmetriken in Kampagnen- und Journey-Berichten an, einschließlich Öffnungen, Klicks und Leistung auf Link-Ebene. [Kampagnenberichte](../reports/campaign-global-report-cja-email.md) | [Journey-Berichte](../reports/journey-global-report-cja-email.md)

+++

+++Webtracking

Für das Webtracking ist eine explizite Konfiguration erforderlich, um Benutzerinteraktionen mit Ihren Web-Änderungen nachzuverfolgen.

**Einrichten von Klick-Tracking:**

Bei der Erstellung einer Web-Seite können Sie bestimmte Elemente (Schaltflächen, Bilder, Links) auswählen, die Sie nachverfolgen möchten. Dies ermöglicht das Klick-Tracking für diese Elemente, ohne dass zusätzlicher Code erforderlich ist. [Weitere Informationen](../web/monitor-web-experiences.md)

* **Tracking von klickbaren Elementen** – Wählen Sie Schaltflächen, Bilder, Links oder ein beliebiges interaktives Element in Ihrer Web-Personalisierung aus.
* **Automatische Datenerfassung** – Nach der Konfiguration erfasst Journey Optimizer automatisch Klickereignisse und verknüpft sie mit Profilen.
* **Überwachung in Echtzeit** – Verfolgen Sie Benutzerinteraktionen während der Validierung der Personalisierungsffektivität in Echtzeit nach.

**Anzeigen von Tracking-Daten:** Greifen Sie auf Anzeigemetriken, Clickthrough-Raten und die Leistung auf Elementebene in Berichten zu. [Kampagnenberichte](../reports/campaign-global-report-cja-web.md) | [Journey-Berichte](../reports/journey-global-report-cja-web.md)

+++

+++Tracking von Push-Benachrichtigungen

Das Push-Tracking ist automatisch aktiviert und erfasst Impressions (zugestellt), Klicks (angetippt) und Öffnungen (App gestartet). Um den Tracking-Wert zu maximieren, konfigurieren Sie anklickbare Elemente in Ihrem Push-Inhalt.

**Konfigurieren nachverfolgter Elemente:**

* **Textkörper-Klickverhalten** - Legen Sie fest, was passiert, wenn Benutzer auf die Benachrichtigung tippen: Programm öffnen, zu einem Deep-Link navigieren oder eine Web-URL öffnen. Jede Aktion wird automatisch nachverfolgt. [Weitere Informationen](../push/design-push.md#on-click-behavior)

* **Aktionsschaltflächen hinzufügen** - Schließen Sie bis zu 3 Schaltflächen (Android) oder mehrere Schaltflächen (iOS) mit unabhängigem Tracking für jede Schaltflächenaktion ein (offene App, Deep-Link, Web-URL). [Weitere Informationen](../push/design-push.md#add-buttons-push)

* **Aktivieren von Tracking** – Prüfen Sie, ob das Tracking in Ihrer Push-Journey-Aktivität oder in den Kampagnen-Tracking-Einstellungen aktiviert ist. [Weitere Informationen](../push/create-push.md#create)

>[!NOTE]
>
>Für das Push-Tracking ist die Implementierung von Mobile SDK erforderlich. Stellen Sie sicher, dass für Ihre App Adobe Experience Platform Mobile SDK ordnungsgemäß konfiguriert ist. [Weitere Informationen](../push/push-configuration.md#integrate-mobile-app)

**Analysieren der Interaktion:** Zeigen Sie Klickraten, Schaltflächenleistung und verfolgte Link-Details in Berichten an. [Kampagnenberichte](../reports/campaign-global-report-cja-push.md) | [Journey-Berichte](../reports/journey-global-report-cja-push.md)

+++

+++In-App-Nachrichten-Tracking

In-App-Nachrichten verfolgen automatisch Anzeigen und Benutzerinteraktionen nach. Konfigurieren Sie Trigger und Inhalte zur Maximierung der Tracking-Effektivität.

**Einrichten von Tracking:**

* **Definieren von Anzeigeregeln** – Legen Sie fest, wann und wo In-App-Nachrichten mithilfe von Triggern (App-Start, Laden des Bildschirms), Häufigkeitsregeln und Zielgruppenbedingungen angezeigt werden. Die ordnungsgemäße Konfiguration gewährleistet ein genaues Tracking sowohl ausgelöster als auch angezeigter Nachrichten.

* **Hinzufügen nachverfolgter Elemente** – Schließen Sie Schaltflächen, Links und interaktive Elemente in Ihren Nachrichteninhalt ein. Jede Interaktion wird automatisch mit detaillierten Labeln nachverfolgt.

* **Optimieren des Anzeige-Timings** – Konfigurieren Sie Wochentag- und Tageszeitregeln, um die Wahrscheinlichkeit zu maximieren, dass ausgelöste Nachrichten Benutzenden tatsächlich angezeigt werden.

[Weitere Informationen zum Konfigurieren von In-App-Nachrichten](../in-app/create-in-app.md)

**Nachverfolgte Elemente:** Journey Optimizer erfasst automatisch Anzeigen, Schaltflächenklicks, Abbrüche, Metriken zu ausgelösten und angezeigten Nachrichten sowie die Link-Leistung. [Kampagnenberichte](../reports/campaign-global-report-cja-inapp.md) | [Journey-Berichte](../reports/journey-global-report-cja-inapp.md)

+++

+++SMS- und MMS-Tracking

Für das SMS-Tracking ist eine minimale Einrichtung erforderlich: Journey Optimizer verkürzt und verfolgt automatisch Links nach, die Sie in Nachrichten einfügen.

**Funktionsweise:**

* **Automatisches Linktracking** – Fügen Sie Ihrem SMS-Inhalt mithilfe der URL-Helper-Funktion beliebige URLs hinzu. Journey Optimizer verkürzt den Link automatisch und verfolgt Klicks ohne zusätzliche Konfiguration. Um die URL-Verkürzung zu verwenden, müssen Sie zunächst eine SMS-Subdomain konfigurieren. [Weitere Informationen](../mobile/mobile-subdomains.md)

* **Tracking eingehender Nachrichten** – Antworten von Empfangenden werden automatisch erfasst, sodass Sie bidirektionale Konversationen und Antwortmuster überwachen können. [Weitere Informationen](../mobile/mobile-opt-out.md#sms-native-keywords)

**Anzeigen von Metriken:** Greifen Sie auf Link-Klickdaten, Volumina eingehender Nachrichten und Leistungstypen von Nachrichten in Berichten zu. [Kampagnenberichte](../reports/campaign-global-report-cja-sms.md) | [Journey-Berichte](../reports/journey-global-report-cja-sms.md)

+++

+++Tracking Code-basierter Erlebnisse

Code-basierte Erlebnisse erfordern die Einrichtung einer Implementierung, damit Tracking-Daten an Adobe Experience Platform gesendet werden.

**Voraussetzungen:**

Damit das Tracking funktioniert, müssen Sie zunächst Ihre Implementierung so konfigurieren, dass Interaktionsereignisse (Anzeigen, Klicks) an Adobe Experience Platform gesendet werden. Dies erfordert Folgendes:

* Einrichten eines für Adobe Experience Platform konfigurierten Datenstroms. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=de)
* Implementieren der Ereigniserfassung in Ihrem Code mit Web SDK oder Mobile SDK.
* Senden von Anzeige- und Interaktionsereignissen beim Anzeigen von Inhalten oder Klicken auf diese.

[Weitere Informationen zu den Voraussetzungen für die Implementierung](../code-based/code-based-prerequisites.md#reporting-prerequisites)

**Nachverfolgte Elemente:** Nach der Implementierung werden Anzeigen, Klicks, Clickthrough-Raten und die Leistung auf Elementebene an allen digitalen Touchpoints (Websites, Mobile Apps, IoT-Geräte usw.) nachverfolgt. [Kampagnenberichte](../reports/campaign-global-report-cja-code.md) | [Journey-Berichte](../reports/journey-global-report-cja-code.md)

+++

+++Tracking von Inhaltskarten

Inhaltskarten verfolgen Benutzerinteraktionen automatisch. Konfigurieren Sie Inhalts- und Anzeigeregeln zur Steuerung des Tracking-Verhaltens.

**Implementierung:**

* **Entwerfen nachverfolgter Inhalte** – Fügen Sie Ihrer Inhaltskarte Schaltflächen und Links hinzu. Jedes interaktive Element wird automatisch mit Labeln und URLs nachverfolgt.

* **Konfigurieren von Persistenz** – Inhaltskarten bleiben über Anwendungssitzungen hinweg erhalten, sodass Sie langfristige Interaktionsmuster nachverfolgen können. Legen Sie Ablaufregeln fest, um zu steuern, wie lange Karten nachverfolgbar bleiben.

* **Einrichten von Anzeigeregeln** – Legen Sie fest, wann und wo Karten angezeigt werden, um ein genaues Tracking von Anzeigen und Interaktionen sicherzustellen.

[Weitere Informationen zum Konfigurieren von Inhaltskarten](../content-card/create-content-card.md)

**Überwachen von Interaktionen:** Verfolgen Sie Anzeigen, Klicks, Clickthrough-Raten und Interaktionsmuster über mehrere Sitzungen hinweg nach. [Kampagnenberichte](../reports/campaign-global-report-cja-content.md) | [Journey-Berichte](../reports/journey-global-report-cja-content.md)

+++

+++Landingpage-Tracking

Landingpages verfügen über ein integriertes Tracking, das keine zusätzliche Einrichtung erfordert. Journey Optimizer erfasst automatisch Besuche, Konversionen und Bounce-Raten.

**Nachverfolgte Elemente:**

* **Besuche** – Gesamtzahl und Anzahl eindeutiger Besuche zur Messung der Reichweite
* **Konversionen** – Formularübermittlungen, Abonnementbestätigungen oder andere definierte Aktionen
* **Absprungrate** – Prozentsatz der Besucherinnen und Besucher, die den Inhalt ohne Interaktion verlassen
* **Leistungs-Trends** – Zeitreihendaten, die zeigen, wie sich Metriken entwickeln

[Weitere Informationen zum Konfigurieren von Landingpages](../landing-pages/create-lp.md)

**Überwachen der Leistung:** Verfolgen Sie Besuchsmuster, Konversionsraten und Bounce-Raten im Zeitverlauf, um zu verstehen, wie Benutzende mit Ihren Formularen interagieren, und ermitteln Sie Bereiche, in denen Verbesserungen möglich sind. [Kampagnenberichte](../reports/lp-report-global-cja.md)

+++

## Nachverfolgen der Journey- und Kampagnenaktivität {#journey-campaign-tracking}

Konfigurieren Sie nicht nur das Tracking auf Kanalebene, sondern auch das Tracking, um die Gesamtleistung zu messen und das Kundenverhalten über Ihre Marketing-Initiativen hinweg zu verstehen.

* **Definieren von benutzerdefinierten Erfolgsmetriken** - Konfigurieren spezifischer KPIs, die auf Ihre Geschäftsziele ausgerichtet sind (Käufe, Anmeldungen, Erneuerungen usw.) Über Standard-Interaktionsmetriken hinaus. [Weitere Informationen](../building-journeys/success-metrics.md)

* **Aktivieren von Journey-Schrittereignissen** – Aktivieren Sie detailliertes Tracking jeder Aktion, die Kundinnen und Kunden beim Durchlaufen von Journeys ausführen. Dies bietet eine granulare Sichtbarkeit von Eintritts-/Ausstiegspunkten, Pfadauswahl und Absprungorten. [Weitere Informationen](../reports/journey-step-events-overview.md)

* **Einrichten eines Zeitplans** – Konfigurieren Sie die Versandzeitoptimierung, um die Leistung über verschiedene Timing-Strategien hinweg zu verfolgen und optimale Versandfenster zu identifizieren. [Weitere Informationen](../building-journeys/send-time-optimization.md)

* **Konfigurieren von Tracking benutzerdefinierter Aktionen** – Richten Sie das Tracking für Integrationen mit externen Systemen ein, um API-Aufrufe, Antwortzeiten und Fehlermuster zu überwachen. [Weitere Informationen](../action/reporting.md)

* **Erstellen benutzerdefinierter Berichte und Exportieren von Daten** – Erstellen Sie maßgeschneiderte Berichte und exportieren Sie Tracking-Daten zur genaueren Analyse in externe Systeme. [Weitere Informationen](../reports/sharing-overview.md)

* **Anzeigen einheitlicher Leistung:** Greifen Sie auf umfassende Berichte für Kampagnen und Journeys zu, um die Leistung über E-Mail, Push, SMS und andere Kanäle hinweg zu vergleichen und zu verstehen, welche Kombinationen die besten Ergebnisse erzielen. [Kampagnenberichte](../reports/campaign-global-report-cja.md) | [Journey-Berichte](../reports/journey-global-report-cja.md)

## Tracking von Optimierung und Entscheidungsfindungsleistung {#optimization-decisioning-tracking}

Journey Optimizer verfolgt automatisch Optimierungsexperimente, Targeting-Strategien und die Entscheidungsfindungsleistung nach. Konfigurieren Sie Ihre Einstellungen, um eine ordnungsgemäße Datenerfassung sicherzustellen.

### Einrichten von Optimierungs-Tracking {#optimization-tracking}

* **Optimierung in Kampagnen und Journeys:**

   * Definieren Sie beim Erstellen von Experimenten, welche Metriken nachverfolgt werden sollen (Konversionen, Klicks, benutzerdefinierte Ereignisse). Journey Optimizer erfasst automatisch Leistungsdaten für jede Abwandlung. [Weitere Informationen](../content-management/optimization-experimentation.md)

   * Erstellen Sie Targeting-Regeln, um verschiedene Inhalte für verschiedene Zielgruppensegmente bereitzustellen. Journey Optimizer verfolgt die Interaktionsmetriken automatisch für jede Zielgruppe nach, sodass Sie die Leistung segmentübergreifend vergleichen können. [Weitere Informationen](../content-management/optimization-targeting.md)

* **Journey-Pfadoptimierung:** Fügen Sie Ihrer Journey eine Aktivität vom Typ **Optimieren** hinzu und konfigurieren Sie mehrere Pfade. Journey Optimizer verfolgt automatisch nach, welche Pfade Profile verwenden, und misst die Leistung. [Weitere Informationen](../building-journeys/optimize.md)

So analysieren Sie die Ergebnisse: Zeigen Sie Konversionsraten, statistische Signifikanz und Steigerung zwischen Abwandlungen in Experimentberichten an oder vergleichen Sie Interaktionsmetriken über Zielsegmente hinweg. [Experimentkampagnenbericht](../reports/campaign-global-report-cja-experimentation.md) | [Experiment-Journey-Bericht](../reports/journey-global-report-cja-experimentation.md) | [Journey-Targeting-Bericht](../reports/journey-global-report-cja.md#targeting)

### Tracking der Entscheidungsfindungsleistung {#decisioning-tracking}

Bei Verwendung von Entscheidungsfindung zur Personalisierung von Inhalten verfolgt Journey Optimizer automatisch Entscheidungsereignisse, Impressions und Klicks, ohne dass eine zusätzliche Konfiguration erforderlich ist.

* **Automatische Ereigniserfassung** – Journey Optimizer erfasst automatisch Entscheidungsereignisse, wenn ein Entscheidungselement für ein Profil ausgewählt wird.
* **Impression-Tracking** – Bei E-Mails werden Impressions automatisch verfolgt. Für Code-basierte Erlebnisse müssen Sie Vorschlagsanzeigeereignisse in Ihrem Code implementieren. [Weitere Informationen](../code-based/code-based-implementation-samples.md#client-side-how)
* **Klick-Tracking** – Klicks auf Entscheidungselemente werden automatisch in E-Mails nachverfolgt. Code-basierte Erlebnisse erfordern die Implementierung von Klick-Ereignissen.

>[!NOTE]
>
>Um Entscheidungen in **Code-basierten Erlebnissen** nachzuverfolgen, stellen Sie sicher, dass Ihre Implementierung mithilfe von Web SDK oder Mobile SDK Vorschlagsinteraktionsereignisse (Anzeigen und Klicks) an Adobe Experience Platform sendet. [Weitere Informationen](../experience-decisioning/data-collection/schema-requirement.md)

So überwachen Sie die Leistung: Zeigen Sie Entscheidungsfindungs-KPIs an, vergleichen Sie Entscheidungselemente, analysieren Sie Auswahlstrategien und überwachen Sie die Leistung des KI-Modells in Berichten. [Weitere Informationen](../experience-decisioning/cja-reporting.md)

## Steuern der Tracking-Datennutzung {#data-governance}

Mit Data-Governance-Richtlinien können Sie steuern, wie Tracking-Daten in Ihrer gesamten Organisation verwendet werden können:

* **Kennzeichnen sensibler Tracking-Daten** – Wenden Sie Governance-Label auf nachverfolgte Verhaltensdaten an (z. B. Klicks auf Gesundheitsinhalte, Interaktionen mit Finanzprodukten), um sie als sensibel oder reguliert zu kennzeichnen.

* **Beschränken der Datennutzung** – Erstellen Sie Richtlinien, die verhindern, dass gekennzeichnete Tracking-Daten auf bestimmten Kanälen verwendet, in Drittanbietersysteme exportiert oder für bestimmte Personalisierungsszenarien verwendet werden.

* **Automatische Durchsetzung** – Journey Optimizer überprüft automatisch Governance-Richtlinien, wenn Sie Journeys und Kampagnen erstellen, und blockiert die Veröffentlichung, wenn nachverfolgte Daten gegen definierte Richtlinien verwendet werden.

Data Governance stellt die Einhaltung von Vorschriften wie der DSGVO und des CCPA sicher und ermöglicht es Ihnen gleichzeitig, das Kundenverhalten innerhalb genehmigter Grenzen nachzuverfolgen und zu analysieren. [Weitere Informationen](../action/action-privacy.md)

## Überwachen der Zustellbarkeit und des Systemstatus {#monitoring-capabilities}

Konfigurieren Sie neben dem Tracking von Interaktionen auch die Überwachung, um sicherzustellen, dass Nachrichten Posteingänge erreichen und Systeme eine optimale Leistung erzielen.

Die Überwachung der Zustellbarkeit hilft Ihnen, sicherzustellen, dass Ihre Nachrichten die Posteingänge der Empfangenden erreichen und die Reputation der Absendenden gewahrt bleibt, indem wichtige Indikatoren nachverfolgt werden:

* **Überprüfen Sie regelmäßig die Unterdrückungsliste**, um zu verstehen, warum Adressen blockiert werden, und um die Listenhygiene aufrechtzuerhalten. [Weitere Informationen](../reports/suppression-list.md)

* **Analysieren Sie Versandfehlern**, um Fehler zu diagnostizieren und Abhilfemaßnahmen zu ergreifen. [Weitere Informationen](../configuration/email-error-types.md)

* **Befolgen Sie die Best Practices** für DMARC, SPF und DKIM, um die Platzierung im Posteingang zu maximieren. [Weitere Informationen](../reports/deliverability.md)

Richten Sie eine proaktive Überwachung ein, um Echtzeit-Benachrichtigungen zu kritischen Ereignissen und Systemproblemen zu erhalten, sodass Sie schnell reagieren können, bevor diese sich auf Ihre Kundenerlebnisse auswirken:

* **Konfigurieren von Warnhinweisen** – Richten Sie Echtzeitbenachrichtigungen für Journey-Fehler, Fehler bei benutzerdefinierten Aktionen und kritische Probleme ein, um schnell auf Probleme zu reagieren. [Weitere Informationen](../reports/alerts.md)

* **Aktivieren von Auditprotokollen** – Aktivieren Sie die Auditprotokollierung, um alle Aktionen auf Ressourcen für die Compliance und Fehlerbehebung nachzuverfolgen. [Weitere Informationen](../privacy/audit-logs.md)

* **Überwachen von Integrationen** – Verfolgen Sie die Leistung von benutzerdefinierten Aktionen und die externe Systemkonnektivität nach, um Integrationsprobleme frühzeitig zu erkennen. [Weitere Informationen](../action/reporting.md)
