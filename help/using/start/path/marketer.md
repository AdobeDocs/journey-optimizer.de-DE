---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer – Erste Schritte für Marketing-Experten
description: Informationen zum Arbeiten mit Journey Optimizer für Journey-Anwendende
level: Beginner
feature: Get Started
Role: User
exl-id: 34304142-3ee8-4081-94b9-e914968c75ba
source-git-commit: 344a5509731b455ee283af22bfdd8c67e028b83e
workflow-type: tm+mt
source-wordcount: '1516'
ht-degree: 3%

---

# Erste Schritte für Marketing-Experten {#get-started-marketers}

Als **Marketer** oder **Business Practitioner** entwerfen Sie Kunden-Journey, um Kunden persönliche, kontextuelle Erlebnisse bereitzustellen. Sie können alle Komponenten dieser personalisierten Journey erstellen und verwalten, einschließlich E-Mail- und Push-Nachrichten, Angebote und Entscheidungskomponenten zur intelligenten Personalisierung des Nachrichteninhalts. Journey Optimizer bietet ein einheitliches Benutzererlebnis, in dem Sie ganze End-to-End-Anwendungsfälle an einem Ort implementieren können. Sie können die Arbeit mit [!DNL Adobe Journey Optimizer] beginnen, sobald Ihnen der [Systemadministrator](administrator.md) und der [Datentechniker](data-engineer.md) Zugriff gewährt und Ihre Umgebung vorbereitet haben.

## Erste Schritte mit den Grundlagen

Journey Optimizer fasst Echtzeit-Kundeneinblicke, moderne Omni-Channel-Orchestrierung und intelligente Entscheidungen in einem einzigen Programm zusammen. Erstellen Sie personalisierte, vernetzte Kundenerlebnisse für E-Mail, SMS, Push, In-App, Web, Inhaltskarten und mehr.

Journey Optimizer bietet zwei leistungsstarke Orchestrierungsansätze:

* **Journey**: Eins-zu-eins-Interaktion in Echtzeit, bei der sich jeder Kunde in seinem eigenen Tempo bewegt, ausgelöst durch Verhalten oder Ereignisse
* **Orchestrierte Kampagnen**: Komplexe, mehrstufige Batch-Kampagnen in großem Maßstab, bei denen Zielgruppen über Workflows zusammenarbeiten. Diese eignen sich perfekt für markeninitiierte Kampagnen wie saisonale Werbeaktionen, Produkteinführungen oder kontobasierte Kommunikation

Arbeiten Sie mit Ihren [Administratoren](administrator.md) zusammen, um Zugriff zu erhalten, und mit [Dateningenieuren](data-engineer.md), um Zielgruppen, Daten und relationale Schemata für die erweiterte Segmentierung einzurichten.

Führen Sie die folgenden grundlegenden Schritte aus, um mit der Erstellung von Erlebnissen zu beginnen:

1. **Erstellen von Zielgruppen**. Erstellen Sie Zielgruppen über Segmentdefinitionen, laden Sie CSV-Dateien hoch oder verwenden Sie die Zielgruppenkomposition. Journey Optimizer bietet mehrere Möglichkeiten, die richtigen Kunden anzusprechen. Weitere Informationen zu [Zielgruppen](../../audience/about-audiences.md) und [Erstellen von Segmentdefinitionen](../../audience/creating-a-segment-definition.md).

1. **Inhalte entwerfen**. Erstellen Sie ansprechende Nachrichten über alle Kanäle hinweg, einschließlich E-Mail, SMS, Push, In-App, Web und Inhaltskarten:
   * Verwenden Sie den **KI** Assistenten, um E-Mail-Inhalte, Betreffzeilen und Bilder basierend auf Ihren Markenrichtlinien zu generieren. [Erfahren Sie mehr über die Generierung von KI-Inhalten](../../content-management/gs-generative.md)
   * **Personalisieren von** mit Kundendaten, dynamischen Inhalten und bedingter Logik. [Informationen zur Personalisierung](../../personalization/personalize.md)
   * **Iterieren Sie über kontextuelle**, um dynamische Listen aus Ereignissen, benutzerdefinierten Aktionen und Datensatzsuchen anzuzeigen. [Erfahren Sie mehr über das Iterieren kontextueller Daten](../../personalization/iterate-contextual-data.md)
   * Erstellen Sie wiederverwendbare **Inhaltsvorlagen** und **Fragmente** um die Markenkonsistenz zu wahren. [Arbeiten mit Vorlagen](../../content-management/content-templates.md)
   * Bereitstellen persistenter, nicht aufdringlicher **(Inhaltskarten)** Mobile Apps und Websites. Im Gegensatz zu Push-Benachrichtigungen bleiben Inhaltskarten sichtbar, bis sie verworfen werden. [Erfahren Sie mehr über Inhaltskarten](../../content-card/create-content-card.md)
   * Verwalten von Assets mit der **Adobe Experience Manager Assets**-Integration. [Informationen zu Assets](../../integrations/assets.md)

   ![](../assets/perso_ee2.png)

1. **Hinzufügen von Angeboten und**. Stellen Sie jedem Kunden mithilfe einer KI-gestützten Entscheidungsfindung zur richtigen Zeit das beste Angebot bereit. Erfahren Sie mehr über [Entscheidungs](../../offers/get-started/starting-offer-decisioning.md)Management und [Erlebnisentscheidung](../../experience-decisioning/gs-experience-decisioning.md).

   ![](../assets/offers-e2e-offers-displayed.png)

1. **Testen und Validieren**. Vorschau und Testen von Inhalten vor dem Senden:
   * Verwenden Sie **Testprofile** um eine Vorschau der Personalisierung anzuzeigen und das Rendering geräteübergreifend zu überprüfen
   * Testen mit **Beispieldaten** aus CSV-/JSON-Dateien
   * Vorschau **E-Mail-Rendering** in gängigen E-Mail-Clients
   * Führen Sie **A/B-Tests und Experimente** aus, um Inhaltsvarianten zu optimieren. Verwenden Sie Multi-Armed-Bandit-Experimente , um den erfolgreichsten Varianten in Echtzeit automatisch mehr Traffic zuzuweisen. [Erfahren Sie mehr über Experimente](../../content-management/content-experiment.md)
   * Einrichten **Validierungs-Workflows** für Kampagnen und Journey (zusätzliche Lizenz erforderlich). [Erfahren Sie mehr über Validierungen](../../test-approve/gs-approval.md)

   Erfahren Sie, wie Sie [Nachrichten testen und validieren](../../content-management/preview-test.md).

1. **Kunden-Journey erstellen**. Erstellen Sie personalisierte Erlebnisse in Echtzeit auf der Journey-Arbeitsfläche:

   * Journey von Triggern **Ereignisse** (Kundenaktionen) oder **Zielgruppen** (Batch-Sendungen)
   * Hinzufügen **Bedingungen** um personalisierte Pfade basierend auf Kundendaten zu erstellen
   * Verwenden Sie **Warteaktivitäten** um ein perfektes Timing zwischen Nachrichten zu erstellen
   * Senden von Nachrichten über **mehrere Kanäle** innerhalb einer Journey
   * Wenden Sie **A/B-** an und optimieren Sie die Versandzeiten, um die Interaktion zu maximieren
   * Verwenden Sie **Datensatzsuche** um Journey mit Echtzeitdaten aus Adobe Experience Platform anzureichern. [Erfahren Sie mehr über die Datensatzsuche](../../building-journeys/dataset-lookup.md)
   * Nutzen Sie **zusätzliche IDs**, damit dasselbe Profil in mehrere Journey-Instanzen (z. B. verschiedene Bestellungen oder Buchungen) eintreten kann. [Erfahren Sie mehr über zusätzliche Kennungen](../../building-journeys/supplemental-identifier.md)

   ![](../assets/journey-design.png)

   Erfahren Sie, wie [Journey entwerfen und ausführen](../../building-journeys/journey-gs.md) und [Journey-Anwendungsfälle erkunden](../../building-journeys/jo-use-cases.md). Grundlegendes [Eintritts-/Austrittskriterien](../../building-journeys/entry-exit-criteria-guide.md) um den Profilfluss zu steuern.

1. **Starten von orchestrierten Kampagnen**. Entwerfen Sie komplexe, mehrstufige Batch-Kampagnen im großen Maßstab mithilfe einer visuellen Arbeitsfläche:

   * Erstellen Sie **On-Demand** Zielgruppen, indem Sie sofort relationale Abfragen verwenden, um Kundendaten mit Konten, Käufen, Abonnements und anderen Entitäten zu verbinden
   * Erstellen **Segmentierung mehrerer Entitäten** für eine präzise Zielgruppenbestimmung (z. B. „Kunden mit Abonnements, die in 30 Tagen ablaufen“ oder „Konten mit kürzlich getätigten hochwertigen Käufen„)
   * Sichern Sie **Pre-send-Sichtbarkeit** mit präziser Audience-Anzahl, bevor Sie starten
   * Entwerfen **mehrstufigen Workflows** für saisonale Werbeaktionen, Produkteinführungen, Treueangebote oder Account-basiertes Marketing
   * Planen von Kampagnen für die sofortige Ausführung zu bestimmten Zeiten oder in wiederkehrenden Zeitplänen (täglich, wöchentlich, monatlich)
   * Verarbeiten Sie Zielgruppen im **Batch-Modus** bei dem alle Profile gemeinsam durch den Workflow fortschreiten

   Erfahren Sie, wie Sie [mit orchestrierten Kampagnen beginnen](../../orchestrated/gs-orchestrated-campaigns.md) und verstehen, wann Sie [Kampagnen vs. Journey verwenden](../../orchestrated/orchestrated-campaigns-faq.md).

1. **Überwachen und Optimieren**. Nachverfolgen der Leistung und Verbesserung der Ergebnisse im Zeitverlauf:
   * Überwachen **Live-Journey**-Leistung und Erkennen von Engpässen
   * Analysieren **Nachrichtenversand** Raten und Interaktionsmetriken
   * Verwenden **Reporting-Dashboards** mit Customer Journey Analytics-Integration
   * Nachverfolgen **Konversion** und geschäftliche Auswirkungen
   * Verwalten Sie **Häufigkeit und Priorisierung von Nachrichten** mithilfe von Regeln für das Konfliktmanagement, um Überkommunikation zu vermeiden. [Erfahren Sie mehr über Konfliktmanagement](../../conflict-prioritization/gs-conflict-prioritization.md)

   Erfahren Sie, wie Sie [Leistung überwachen](../../reports/report-gs-cja.md).

## Best Practices für den Erfolg

### Inhaltserstellung

* **Erste Schritte mit Vorlagen**: Verwenden Sie vorgefertigte Vorlagen und Inhaltsfragmente, um die Erstellung zu beschleunigen und die Konsistenz zu gewährleisten
* **Testen Sie früh, häufig**: Zeigen Sie Inhalte immer geräteübergreifend in der Vorschau an und verwenden Sie Testprofile zur Validierung der Personalisierung
* **Nutzen Sie KI mit Bedacht**: Verwenden Sie den KI-Assistenten für erste Entwürfe und Varianten, aber überprüfen und verfeinern Sie ihn immer für Ihre Markensprache
* **Einfach halten**: Klare, präzise Nachrichten mit starken Aktionsaufrufen erzielen eine bessere Leistung als komplexe Layouts

### Journey-Design

* **Klare Ziele definieren**: Erstellen Sie Erfolgsmetriken, bevor Sie Ihren Journey erstellen
* **Kundenerlebnis zuordnen**: Visualisieren Sie die gesamte Journey vor der Implementierung
* **Warteaktivitäten strategisch nutzen**: Kunden Zeit geben, mit ihnen zu interagieren, bevor sie Folgemaßnahmen versenden
* **Ausstiegsstrategien planen**: Festlegen, wann und warum Kunden die Journey beenden sollen
* **Im Entwurfsmodus testen**: Validieren der Journey-Logik mit Probelauf vor der Aktivierung

[Best Practices für Journey](../../building-journeys/entry-exit-criteria-guide.md#best-practices)

### Kampagnen-Orchestrierung

* **Wählen Sie den richtigen Ansatz**: Verwenden Sie Journey-Kampagnen für verhaltensgesteuerte Erlebnisse in Echtzeit; verwenden Sie orchestrierte Kampagnen für geplante Batch-Kampagnen.
* **Definieren Sie klare Kampagnenziele**: Legen Sie Ziele fest, bevor Sie mehrstufige Workflows erstellen
* **Mit Pilot-Zielgruppen beginnen**: Überprüfen der Zählungen und Segmentierungslogik vor der Skalierung
* **Nutzen relationaler Daten**: Verwenden Sie die Segmentierung mehrerer Entitäten, um Kundendaten mit Konten, Käufen und Abonnements zu verbinden und so ein präzises Targeting zu ermöglichen
* **Einfache Segmentierung**: Optimieren Sie Leistung und Transparenz mit klaren, verwaltbaren Regeln
* **Konsistente Benennung verwenden**: Vereinfachung der Kampagnenverwaltung durch klare Benennungskonventionen

### Zielgruppen-Targeting

* **Überlegt segmentieren**: Erstellen Sie spezifische, umsetzbare Zielgruppensegmente basierend auf klaren Kriterien
* **Regelmäßig aktualisieren**: Stellen Sie sicher, dass die Zielgruppen aktuell bleiben, indem Sie geeignete Auswertungszeitpläne festlegen
* **Balance-Größe und Präzision**: Zielgruppen, die groß genug für statistische Signifikanz, aber spezifisch genug für Relevanz sind
* **Anreicherungsattribute verwenden**: Nutzung berechneter Attribute und Anreicherungsdaten für eine tiefere Personalisierung

### Frequenzverwaltung

* **Kundenpräferenzen respektieren**: Opt-outs und Kommunikationsvoreinstellungen berücksichtigen
* **Frequenzlimitierungen festlegen**: Verwenden Sie Regelsätze, um eine kanalübergreifende Nachrichtenermüdung zu verhindern
* **Kampagnen koordinieren**: Verwenden Sie das Konflikt-Management, um sicherzustellen, dass Kunden die richtige Nachricht zur richtigen Zeit erhalten
* **Interaktion überwachen**: Achten Sie auf Anzeichen von Müdigkeit (sinkende Öffnungsraten, steigende Abmeldungen).

[Informationen zur Frequenzlimitierung](../../conflict-prioritization/channel-capping.md)

## Anwendungsfälle erkunden

Lernen Sie aus praktischen Beispielen, die die Funktionen von Journey Optimizer demonstrieren:

**Journey-Anwendungsfälle** (Echtzeit, Eins-zu-eins):

* **Welcome Series**: Lernen Sie neue Kunden mit personalisierten, mehrstufigen Journey kennen. [Anwendungsfall anzeigen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* **Abgebrochene Wiederherstellung des Warenkorbs**: Erneuter Kontakt mit Kunden, die Artikel in ihrem Warenkorb hinterlassen haben. [Anwendungsfall anzeigen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* **Ereignisgesteuertes Messaging**: Reagieren auf Kundenaktionen in Echtzeit
* **Geburtstagskampagnen**: Senden personalisierter Geburtstagsnachrichten, die durch Profildaten ausgelöst werden
* **Produktempfehlungen**: Schlagen Sie relevante Produkte basierend auf dem Browse- und Kaufverlauf vor

**Anwendungsfälle für orchestrierte Kampagnen** (Batch, Eins-zu-Viele):

* **Saisonale Werbeaktionen**: Starten Sie koordinierte Kampagnen über Kundensegmente hinweg (z. B. Weihnachtsumsätze, „Back-to-School„)
* **Produkteinführungen**: Ankündigung neuer Produkte an ausgewählte Zielgruppen mit sequenzieller Nachrichtenübermittlung
* **Treueprogramm-Angebote**: Belohnen Sie hochwertige Kunden mit mehrstufigen Angeboten, die auf dem Kaufverlauf basieren.
* **Account-Based Marketing**: Targeting von Konten mit bestimmten Merkmalen und zugehörigen Kontakten
* **Abonnementverlängerungen**: Kunden mit Abonnements erreichen, die bald ablaufen, indem Abfragen mit mehreren Entitäten verwendet werden
* **Rückgewinnungskampagnen**: Gewinnen Sie inaktive Kunden mit zielgerichteten Angeboten im Batch-Modus zurück. [Anwendungsfall anzeigen](https://experienceleague.adobe.com/de/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)

**Journey-Muster:**

* [Nachrichten an Abonnenten senden](../../building-journeys/message-to-subscribers-uc.md): Targeting von Abonnementlisten mit personalisierten Inhalten
* [Multi-Channel-Messaging](../../building-journeys/journeys-uc.md): Kombinieren von E-Mail und Push mit Reaktionsereignissen
* [Nur-Wochentag-E-Mails](../../building-journeys/weekday-email-uc.md): Planen Sie die Kommunikation unter Verwendung zeitbasierter Bedingungen

Durchsuchen Sie die vollständige Bibliothek mit [Journey-Anwendungsfällen &#x200B;](../../building-journeys/jo-use-cases.md) erfahren Sie mehr über [Orchestrierte Kampagnen](../../orchestrated/gs-orchestrated-campaigns.md).

## Mit anderen Rollen zusammenarbeiten

Ihre Marketing-Arbeit vernetzt sich mit anderen Teams:

* **Arbeiten mit [Dateningenieuren](data-engineer.md)**: Fordern Sie neue berechnete Attribute an, koordinieren Sie relationale Schemata für orchestrierte Kampagnen, geben Sie Feedback zur Zielgruppen-Qualität und stimmen Sie die Datenanforderungen für mehrere Entitäten für die erweiterte Segmentierung ab
* **Arbeiten mit [Entwicklern](developer.md)**: Ausrichten von Ereignis-Triggern, Testen von Mobile-Implementierungen und Validieren des Trackings
* **Arbeiten mit [Administratoren](administrator.md)**: Anfordern von Kanalkonfigurationen, Bestätigen des Lizenzzugriffs für orchestrierte Kampagnen, Melden von Problemen mit Berechtigungen und Koordinieren der Aktivierung neuer Funktionen

## Auf dem Laufenden bleiben

Bleiben Sie auf dem Laufenden mit den neuesten Journey Optimizer-Funktionen und Marketing-Funktionen:

* **[Versionshinweise](../../rn/release-notes.md)** Überprüfen Sie jeden Monat neue Funktionen, Kanal-Updates und Verbesserungen
* **[Dokumentationsaktualisierungen](../../rn/documentation-updates.md)**: Verfolgen Sie aktuelle Änderungen, einschließlich neuer Anwendungsfälle, Best Practices und der Dokumentation zu Funktionen
* **Produktbenachrichtigungen**: Aktivieren Sie Benachrichtigungen in Ihrem [Adobe Experience Cloud-Profil](https://experience.adobe.com/preferences){target="_blank"} um Warnhinweise zu erhalten:
   * Neue Kanäle und Funktionen zur Verfügung
   * Bevorstehende Funktionsstarts und Beta-Programme
   * Best Practices und Schulungsmöglichkeiten
   * Wichtige Ankündigungen, die Ihre Kampagnen betreffen

  Um Benachrichtigungen zu aktivieren, klicken Sie auf Ihr Profilsymbol oben rechts in Adobe Experience Cloud, gehen Sie zu **Voreinstellungen > Benachrichtigungen** und konfigurieren Sie Ihre Journey Optimizer-Benachrichtigungseinstellungen.

## Nächste Schritte

1. **Klein beginnen** Erstellen Sie eine einfache Begrüßungs-Journey oder Einzelnachrichtenkampagne, um die Plattform kennenzulernen.
2. **Nutzen von KI**: Verwenden Sie den KI-Assistenten, um Fragen zu stellen und die Inhaltserstellung zu beschleunigen
3. **Mitglied der Community**: Treten Sie mit anderen Journey Optimizer-Benutzern in der [Experience League-Community in Kontakt](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=de){target="_blank"}
4. **Tutorials erkunden**: Sehen Sie sich Videoanleitungen in [Experience League an](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=de){target="_blank"}
