---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer – Erste Schritte für Marketing-Experten
description: Informationen zum Arbeiten mit Journey Optimizer für Journey-Anwendende
level: Beginner
feature: Get Started
Role: User
exl-id: 34304142-3ee8-4081-94b9-e914968c75ba
source-git-commit: d1fd0b60ae60c2642108a1eb308564c9d04f5f9e
workflow-type: tm+mt
source-wordcount: '1476'
ht-degree: 98%

---

# Erste Schritte für Marketing-Experten {#get-started-marketers}

Als **Marketing-Fachkraft** oder **Business Anwenderin bzw. -Anwender** entwerfen Sie Customer Journeys, um Kundinnen und Kunden persönliche, kontextuelle Erlebnisse bereitzustellen. Sie können alle verschiedenen Komponenten dieser personalisierten Journeys erstellen und verwalten, einschließlich E-Mail- und Push-Nachrichten, Angeboten und Entscheidungskomponenten zur intelligenten Personalisierung des Nachrichteninhalts. Journey Optimizer bietet ein einheitliches Anwendererlebnis, in dem Sie ganze End-to-End-Anwendungsfälle an einem Ort implementieren können. Sie können die Arbeit mit [!DNL Adobe Journey Optimizer] beginnen, sobald Ihnen die oder der [Systemadmin](administrator.md) und [die Dateningenieurin bzw. der Dateningenieur](data-engineer.md) Zugriff gewährt und Ihre Umgebung vorbereitet haben.

## Erste Schritte mit den Grundlagen

Journey Optimizer fasst Echtzeit-Kundenerkenntnisse, moderne Omni-Channel-Orchestrierung und intelligente Entscheidungen in einer einzigen Anwendung zusammen. Erstellen Sie personalisierte, vernetzte Kundenerlebnisse für E-Mail, SMS, Push, In-App, Web, Inhaltskarten und mehr.

Journey Optimizer bietet zwei leistungsstarke Orchestrierungsansätze:

* **Journeys**: Eins-zu-eins-Interaktion in Echtzeit, bei der sich alle Kundinnen und Kunden in ihrem eigenen Tempo bewegen, ausgelöst durch Verhalten oder Ereignisse
* **Orchestrierte Kampagnen**: Komplexe, mehrstufige Batch-Kampagnen im benötigten Umfang, bei denen Zielgruppen über Workflows zusammenarbeiten; perfekt für markenkonforme Kampagnen wie saisonale Werbeaktionen, Produkteinführungen oder kontobasierte Kommunikation

Arbeiten Sie mit Ihren [Admins](administrator.md) zusammen, um Zugriff zu erhalten, und mit [Dateningenieurinnen und -ingenieuren](data-engineer.md), um Zielgruppen, Daten und relationale Schemata für die erweiterte Segmentierung einzurichten.

Führen Sie die folgenden grundlegenden Schritte aus, um mit der Erstellung von Erlebnissen zu beginnen:

1. **Erstellen von Zielgruppen**. Erstellen Sie Zielgruppen über Segmentdefinitionen, laden Sie CSV-Dateien hoch oder verwenden Sie die Zielgruppenkomposition. Journey Optimizer bietet mehrere Möglichkeiten, die richtigen Kundinnen und Kunden anzusprechen. Erfahren Sie mehr über [Zielgruppen](../../audience/about-audiences.md) und das [Erstellen von Segmentdefinitionen](../../audience/creating-a-segment-definition.md).

1. **Gestalten Sie Inhalte**. Erstellen Sie ansprechende Nachrichten über alle Kanäle hinweg, einschließlich E-Mail, SMS, Push, In-App, Web und Inhaltskarten:
   * Verwenden Sie den **KI-Assistenten**, um E-Mail-Inhalte, Betreffzeilen und Bilder basierend auf Ihren Markenrichtlinien zu generieren. [Weitere Informationen zur Generierung von KI-Inhalten](../../content-management/gs-generative.md)
   * **Personalisieren Sie Nachrichten** mit Kundendaten, dynamischen Inhalten und bedingter Logik. [Informationen zur Personalisierung](../../personalization/personalize.md)
   * **Iterieren Sie über kontextuelle Daten**, um dynamische Listen aus Ereignissen, benutzerdefinierten Aktionen und Datensatzsuchen anzuzeigen. [Weitere Informationen zum Iterieren über kontextuelle Daten](../../personalization/iterate-contextual-data.md)
   * Erstellen Sie wiederverwendbare **Inhaltsvorlagen** und **Fragmente**, um die Markenkonsistenz zu wahren. [Arbeiten mit Vorlagen](../../content-management/content-templates.md)
   * Stellen Sie persistente, nicht aufdringliche **Inhaltskarten** in Apps und Websites bereit. Im Gegensatz zu Push-Benachrichtigungen bleiben Inhaltskarten sichtbar, bis sie verworfen werden. [Weitere Informationen zu Inhaltskarten](../../content-card/create-content-card.md)
   * Verwalten Sie Assets mit der Integration von **Adobe Experience Manager Assets**. [Weitere Informationen zu Assets](../../integrations/assets.md)

   ![](../assets/perso_ee2.png)

1. **Fügen Sie Angebote und Entscheidungsfindung hinzu**. Senden Sie allen Kundinnen und Kunden mithilfe einer KI-gestützten Entscheidungsfindung zur richtigen Zeit das beste Angebot. Erfahren Sie mehr über [Entscheidungs-Management](../../offers/get-started/starting-offer-decisioning.md) und [Erlebnis-Entscheidung](../../experience-decisioning/gs-experience-decisioning.md).

   ![](../assets/offers-e2e-offers-displayed.png)

1. **Testen und Validieren**. Zeigen Sie eine Vorschau an und testen Sie Inhalte vor dem Senden:
   * Verwenden Sie **Testprofile**, um eine Vorschau der Personalisierung anzuzeigen und das Rendering geräteübergreifend zu überprüfen
   * Testen Sie mit **Beispieldaten** aus CSV/JSON-Dateien
   * Zeigen Sie eine Vorschau des **E-Mail-Renderings** in gängigen E-Mail-Clients an
   * Führen Sie **A/B-Tests und Experimente** aus, um Inhaltsvarianten zu optimieren. Verwenden Sie Multi-Armed-Bandit-Experimente, um den erfolgreichsten Varianten in Echtzeit automatisch mehr Traffic zuzuweisen. [Weitere Informationen zu Experimenten](../../content-management/content-experiment.md)
   * Richten Sie **Genehmigungs-Workflows** für Kampagnen und Journeys ein (zusätzliche Lizenz erforderlich). [Weitere Informationen zu Genehmigungen](../../test-approve/gs-approval.md)

   Erfahren Sie, wie Sie [Nachrichten testen und validieren](../../content-management/preview-test.md).

1. **Erstellen Sie Customer Journeys**. Erstellen Sie personalisierte Erlebnisse in Echtzeit auf der Journey-Arbeitsfläche:

   * Lösen Sie Journeys durch **Ereignisse** (Kundenaktionen) oder **Zielgruppen** (Batch-Sendungen) aus
   * Fügen Sie **Bedingungen** hinzu, um personalisierte Pfade basierend auf Kundendaten zu erstellen
   * Verwenden Sie **Warteaktivitäten**, um ein perfektes Timing zwischen Nachrichten zu erstellen
   * Senden Sie Nachrichten über **mehrere Kanäle** innerhalb einer Journey
   * Wenden Sie **A/B-Tests** an und optimieren Sie die Versandzeiten, um die Interaktion zu maximieren
   * Verwenden Sie die **Datensatzsuche**, um Journeys mit Echtzeitdaten aus Adobe Experience Platform anzureichern. [Weitere Informationen zur Datensatzsuche](../../building-journeys/dataset-lookup.md)
   * Nutzen Sie **zusätzliche Kennungen**, damit dasselbe Profil in mehrere Journey-Instanzen (z. B. verschiedene Bestellungen oder Buchungen) eintreten kann. [Weitere Informationen zu zusätzlichen Kennungen](../../building-journeys/supplemental-identifier.md)

   ![](../assets/journey-design.png)

   Erfahren Sie, wie Sie [Journeys entwerfen und ausführen](../../building-journeys/journey-gs.md), und sehen Sie sich [Journey-Anwendungsfälle](../../building-journeys/jo-use-cases.md) an. Erfahren Sie Grundlegendes zu [Eintritts-/Ausstiegskriterien](../../building-journeys/entry-exit-criteria-guide.md), um den Profilfluss zu steuern.

1. **Starten Sie orchestrierte Kampagnen**. Entwerfen Sie komplexe, mehrstufige Batch-Kampagnen im benötigten Umfang mithilfe einer visuellen Arbeitsfläche:

   * Erstellen Sie **On-Demand-Zielgruppen**, indem Sie sofort relationale Abfragen verwenden, um Kundendaten mit Konten, Käufen, Abonnements und anderen Entitäten zu verbinden
   * Erstellen Sie **Segmentierung in mehrere Entitäten** für eine präzise Zielgruppenbestimmung (z. B. „Kundinnen und Kunden mit Abonnements, die in 30 Tagen ablaufen“ oder „Konten mit kürzlich getätigten hochwertigen Käufen“)
   * Erhalten Sie **Sichtbarkeit vor dem Versand** mit präziser Zielgruppengröße, bevor Sie starten
   * Entwerfen Sie **mehrstufige Workflows** für saisonale Werbeaktionen, Produkteinführungen, Treueangebote oder Account-basiertes Marketing
   * Planen Sie Kampagnen für die sofortige Ausführung zu bestimmten Zeiten oder in wiederkehrenden Abständen (täglich, wöchentlich, monatlich)
   * Verarbeiten Sie Zielgruppen im **Batch-Modus**, bei dem sich alle Profile gemeinsam durch den Workflow bewegen

   Erfahren Sie, wie Sie [mit orchestrierten Kampagnen loslegen](../../orchestrated/gs-orchestrated-campaigns.md) und wann Sie [Kampagnen bzw. Journeys verwenden](../../orchestrated/orchestrated-campaigns-faq.md).

1. **Überwachen und optimieren Sie**. Verfolgen Sie Leistung und Verbesserung der Ergebnisse im Zeitverlauf:
   * Überwachen Sie die Leistung von **Live-Journeys** und identifizieren Sie Engpässe
   * Analysieren Sie die Raten des **Nachrichtenversands** und Interaktionsmetriken
   * Verwenden Sie **Reporting-Dashboards** mit Customer Journey Analytics-Integration
   * Verfolgen Sie **Konversion** und geschäftliche Auswirkungen
   * Verwalten Sie **Häufigkeit und Priorisierung von Nachrichten** mithilfe von Regeln für das Konflikt-Management, um übermäßige Kommunikation zu vermeiden. [Weitere Informationen zum Konflikt-Management](../../conflict-prioritization/gs-conflict-prioritization.md)

   Erfahren Sie, wie Sie [Leistung überwachen](../../reports/report-gs-cja.md).

## Best Practices für Erfolg

### Inhaltserstellung

* **Erste Schritte mit Vorlagen**: Verwenden Sie vorkonfigurierte Vorlagen und Inhaltsfragmente, um die Erstellung zu beschleunigen und die Konsistenz zu gewährleisten
* **Frühes und häufiges Testen**: Zeigen Sie Inhalte immer geräteübergreifend in der Vorschau an und verwenden Sie Testprofile zur Validierung der Personalisierung
* **Bedachtes Nutzen von KI**: Verwenden Sie den KI-Assistenten für erste Entwürfe und Varianten, aber überprüfen und verfeinern Sie diese immer mit Ihrer Markensprache
* **Einfache Gestaltung**: Klare, präzise Nachrichten mit aussagekräftigen Aufrufen zum Handeln erzielen eine bessere Leistung als komplexe Layouts

### Journey-Design

* **Definieren von klaren Zielen**: Erstellen Sie Erfolgsmetriken, bevor Sie Ihre Journey erstellen
* **Zuordnen von Kundenerlebnissen**: Visualisieren Sie die gesamte Journey vor der Implementierung
* **Strategisches Verwenden von Warteaktivitäten**: Geben Sie Kundinnen und Kunden Zeit zum Interagieren, bevor sie Folgenachrichten senden
* **Planen von Ausstiegsstrategien**: Legen Sie fest, wann und warum Kundinnen und Kunden aus der Journey aussteigen sollen
* **Testen im Entwurfsmodus**: Validieren Sie die Journey-Logik vor der Aktivierung im Probelauf

[Weitere Informationen zu Best Practices für Journeys](../../building-journeys/entry-exit-criteria-guide.md#best-practices)

### Kampagnenorchestrierung

* **Wählen Sie den richtigen Ansatz**: [Vergleichen Sie Journey-Typen](../../building-journeys/journey.md#journey-types) für verhaltensgesteuerte Erlebnisse in Echtzeit oder [Kampagnentypen](../../campaigns/get-started-with-campaigns.md#campaign-types) für geplante Batch-Kampagnen
* **Definieren von klaren Kampagnenzielen**: Legen Sie Ziele fest, bevor Sie mehrstufige Workflows erstellen
* **Starten mit Pilot-Zielgruppen**: Überprüfen Sie Anzahl und Segmentierungslogik vor der Skalierung
* **Nutzen relationaler Daten**: Verwenden Sie die Segmentierung in mehrere Entitäten, um Kundendaten mit Konten, Käufen und Abonnements zu verbinden und so ein präzises Targeting zu ermöglichen
* **Einfache Segmentierung**: Optimieren Sie Leistung und Transparenz mit klaren, verwaltbaren Regeln
* **Verwenden konsistenter Benennung**: Vereinfachen Sie das Kampagnen-Management durch klare Namenskonventionen

### Zielgruppen-Targeting

* **Überlegtes Segmentieren**: Erstellen Sie spezifische, verwertbare Zielgruppensegmente basierend auf klaren Kriterien
* **Regelmäßiges Aktualisieren**: Stellen Sie sicher, dass die Zielgruppen aktuell bleiben, indem Sie geeignete Auswertungszeitpläne festlegen
* **Ausgleichen von Größe und Präzision**: Sprechen Sie Zielgruppen an, die groß genug für statistische Signifikanz, aber spezifisch genug für Relevanz sind
* **Verwenden von Anreicherungsattributen**: Nutzen Sie berechnete Attribute und Anreicherungsdaten für eine umfassendere Personalisierung

### Häufigkeitsverwaltung

* **Respektieren von Kundenvoreinstellungen**: Berücksichtigen Sie Opt-outs und Kommunikationsvoreinstellungen
* **Festlegen von Frequenzbegrenzung**: Verwenden Sie Regelsätze, um eine kanalübergreifende Nachrichtenermüdung zu verhindern
* **Koordinieren von Kampagnen**: Verwenden Sie Konflikt-Management, um sicherzustellen, dass Kundinnen und Kunden die richtige Nachricht zur richtigen Zeit erhalten
* **Überwachen von Interaktion**: Achten Sie auf Anzeichen von Ermüdung (sinkende Öffnungsraten, steigende Abmeldungen)

[Weitere Informationen zur Frequenzbegrenzung](../../conflict-prioritization/channel-capping.md)

## Erkunden von Anwendungsfällen

Lernen Sie aus praktischen Beispielen, die die Funktionen von Journey Optimizer veranschaulichen:

**Journey-Anwendungsfälle** (Echtzeit, Eins-zu-eins):

* **Willkommensserie**: Führen Sie ein Onboarding neuer Kundinnen und Kunden mit personalisierten, mehrstufigen Journeys durch. [Anwendungsfall anzeigen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* **Wiederherstellen abgebrochener Warenkörbe**: Nehmen Sie erneut Kontakt mit Kundinnen und Kunden auf, die Artikel in ihrem Warenkorb hinterlassen haben. [Anwendungsfall anzeigen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* **Ereignisgesteuertes Messaging**: Reagieren Sie auf Kundenaktionen in Echtzeit
* **Geburtstagskampagnen**: Senden Sie personalisierte Geburtstagsnachrichten, die durch Profildaten ausgelöst werden
* **Produktempfehlungen**: Schlagen Sie relevante Produkte basierend auf Such- und Kaufverlauf vor

**Anwendungsfälle für orchestrierte Kampagnen** (Batch, Eins-zu-viele):

* **Saisonale Werbeaktionen**: Starten Sie koordinierte Kampagnen über Kundensegmente hinweg (z. B. Weihnachtsabverkäufe, Angebote zum Schulbeginn)
* **Produkteinführungen**: Kündigen Sie ausgewählten Zielgruppen neue Produkte mit sequenziellem Messaging an
* **Angebote im Rahmen des Treueprogramms**: Belohnen Sie hochwertige Kundschaft mit mehrstufigen Angeboten, die auf ihrem Kaufverlauf basieren
* **Account-basiertes Marketing**: Sprechen Sie Konten mit bestimmten Merkmalen und zugehörige Kontakten an
* **Abonnementverlängerungen**: Erreichen Sie Kundinnen und Kunden mit Abonnements, die bald ablaufen, indem Sie Abfragen mit mehreren Entitäten verwenden
* **Rückgewinnungskampagnen**: Gewinnen Sie inaktive Kundinnen und Kunden mit zielgerichteten Angeboten im Batch-Modus zurück. [Anwendungsfall anzeigen](https://experienceleague.adobe.com/de/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)

**Journey-Muster:**

* [Senden von Nachrichten an Abonnierende](../../building-journeys/message-to-subscribers-uc.md): Sprechen Sie Abonnement-Listen mit personalisierten Inhalten an
* [Multi-Channel-Messaging](../../building-journeys/journeys-uc.md): Kombinieren Sie E-Mail und Push mit Reaktionsereignissen
* [Senden von E-Mails nur an Wochentagen](../../building-journeys/weekday-email-uc.md): Planen Sie die Kommunikation unter Verwendung zeitbasierter Bedingungen

Sehen Sie sich die vollständige [Bibliothek mit Journey-Anwendungsfällen](../../building-journeys/jo-use-cases.md) an und erfahren Sie mehr über [orchestrierte Kampagnen](../../orchestrated/gs-orchestrated-campaigns.md).

## Rollenübergreifendes Zusammenarbeiten

Ihre Marketing-Arbeit ist mit anderen Teams verbunden:

>[!BEGINTABS]

>[!TAB Arbeiten mit Dateningenieurinnen und -ingenieuren]

Arbeiten Sie mit [Dateningenieurinnen und -ingenieuren](data-engineer.md) bei Daten und Zielgruppenkonfigurationen zusammen:

* Anfordern neuer berechneter Attribute für Personalisierung und Segmentierung
* Koordinieren relationaler Schemata für orchestrierte Kampagnen
* Bereitstellen von Feedback zur Zielgruppenqualität und Datengenauigkeit
* Abstimmen der Datenanforderungen für mehrere Entitäten für die erweiterte Segmentierung

>[!TAB Arbeiten mit Entwickelnden]

Arbeiten Sie mit [Entwickelnden](developer.md) bei Ereignis-Tracking und Implementierung zusammen:

* Abstimmen, durch welche Benutzerinteraktionen Journey-Ereignisse ausgelöst werden sollen
* Testen von Mobile- und Web-Implementierungen vor dem Launch
* Überprüfen des Trackings auf Inhaltsleistung und Benutzerinteraktion
* Beheben von Problemen beim Nachrichtenversand oder bei der Personalisierung

>[!TAB Arbeiten mit Admins]

Arbeiten Sie mit [Admins](administrator.md) bei Zugriff und Konfigurationen zusammen:

* Anfordern von Kanalkonfigurationen für Kampagnen und Journeys
* Bestätigen des Lizenzzugriffs für orchestrierte Kampagnen und andere Funktionen
* Melden von Problemen mit Berechtigungen oder Zugriff
* Koordinieren der Aktivierung von neuen Funktionen und Testumgebungen

>[!ENDTABS]

## Nächste Schritte

1. **Starten im kleinen Umfang** Erstellen Sie eine einfache Willkommens-Journey oder Einzelnachrichtenkampagne, um die Plattform kennenzulernen
2. **Nutzen von KI**: Verwenden Sie den KI-Assistenten, um Fragen zu stellen und die Inhaltserstellung zu beschleunigen
3. **Beitreten zur Community**: Treten Sie mit anderen Journey Optimizer-Benutzenden in der [Experience League-Community](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=de){target="_blank"} in Kontakt
4. **Erkunden von Tutorials**: Sehen Sie sich detaillierten Videos auf [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=de){target="_blank"} an
