---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Journeys
description: Erste Schritte mit Journey - Erfahren Sie mehr über Journey-Typen, Workflows, Funktionen und Best Practices zum Erstellen personalisierter Kundenerlebnisse in Adobe Journey Optimizer
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: Journey, Entdecken, Erste Schritte, Unitär, Zielgruppe lesen, Zielgruppen-Qualifizierung, Geschäftsereignis, Echtzeit, Geplant, Batch, ereignisausgelöst, Workflow, Orchestrierung, Personalisierung, Multi-Channel
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 8ea2a0fe685678d41004d549443a1757eb30c765
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 4%

---


# Erste Schritte mit Journeys{#jo-general-principle}

Mit Adobe Journey Optimizer können Sie personalisierte, mehrstufige Kunden-Journey erstellen, die sich in Echtzeit an das Verhalten und die Bedürfnisse Ihrer Zielgruppe anpassen. Mithilfe einer intuitiven Drag-and-Drop-Arbeitsfläche können Sie Nachrichten und Aktionen über mehrere Kanäle hinweg orchestrieren und dabei kontextuelle Daten und Audience-Targeting nutzen, um eine maximale Wirkung zu erzielen.

Dieses Handbuch bietet eine klare Roadmap, die Ihnen hilft, die Grundlagen des Journey zu verstehen, den richtigen Journey-Typ für Ihren Anwendungsfall auszuwählen und zuversichtlich Journey zu entwerfen, die aussagekräftige, zeitnahe Kundenerlebnisse bieten.

## Was sind Journey?

**Journey** sind automatisierte, mehrstufige Kundenerlebnisse, die als Reaktion auf Kundenverhalten, Geschäftsereignisse oder geplante Kampagnen personalisierte Interaktionen kanalübergreifend orchestrieren.

Verwenden Sie [!DNL Journey Optimizer] für:

* Erstellen **Echtzeit-Orchestrierung** Anwendungsfälle mit kontextuellen Daten aus Ereignissen oder Datenquellen
* Entwerfen **mehrstufigen erweiterten Szenarien** die dynamisch auf Kundenverhalten und Geschäftsereignisse reagieren
* Bereitstellung von **1:1 personalisierten Erlebnissen** skaliert für E-Mail, Push, SMS, In-App, Web und mehr

![Benutzeroberfläche des Journey-Designers mit Palette, Arbeitsfläche und Eigenschaftenbereich](assets/journey38.png)

➡️ **Bereit zum Bauen?Journey** [Erstellen Sie Ihre erste &#x200B;](journey-gs.md) in 5 Minuten.

### Journey vs. Kampagnen: Verwendung der einzelnen {#journeys-vs-campaigns-intro}

Adobe Journey Optimizer bietet drei Ansätze, um Kundinnen und Kunden zu erreichen: **Journey** (:1 Echtzeit-Orchestrierung), **Kampagnen** (einfacher Batch- oder API-gesteuerter Versand) und **Orchestrierte Kampagnen** (Batch-Arbeitsflächen-Workflows mit Daten aus mehreren Entitäten).

**Schnelle Entscheidung:**

* Verwenden Sie **Journey** für mehrstufige, verhaltensgesteuerte Erlebnisse, bei denen jeder Kunde in seinem eigenen Tempo Fortschritte macht
* Verwenden **Aktion/API-Kampagnen** für einen einfachen, geplanten oder ausgelösten Nachrichtenversand an Zielgruppen
* Verwenden Sie **Orchestrierte Kampagnen** für komplexe Batch-Workflows, die eine Segmentierung mehrerer Entitäten und exakte Zählungen vor dem Versand erfordern

<!-- waiting for DOCAC-13912
➡️ **[View detailed comparison: Journeys vs Campaigns](../start/journeys-vs-campaigns.md)** - Includes decision guide, use cases, and feature availability-->

## Journey-Typ auswählen {#journey-types}

Adobe Journey Optimizer unterstützt vier Journey-Typen, die jeweils für unterschiedliche Einstiegsmechanismen und Geschäftsszenarien entwickelt wurden:

* **Unitäre Journey**: Ereignisgesteuerte Erlebnisse in Echtzeit (Bestellbestätigungen, Willkommens-E-Mails)
* **Audience-Journey lesen**: Geplante Batch-Nachrichten an Zielgruppensegmente (Newsletter, Werbekampagnen)
* **Journey zur Zielgruppenqualifizierung**: Echtzeit-Reaktionen auf Änderungen der Zielgruppenmitgliedschaft (VIP-Upgrades, Rückgewinnung)
* **Geschäftsereignis-Journey**: Geschäftsbedingungen, die mehrere Kunden betreffen (Inventarwarnungen, Flash-Verkäufe)

➡️ **[Journey-Typen und Auswahlhandbuch](journey-types-selection.md)** - Detaillierter Vergleich, Entscheidungsbaum und Funktionskompatibilitätsmatrix

## Erstellen mit dem Journey-Designer {#journey-designer}

Der **[Journey-Designer](using-the-journey-designer.md)** ist Ihre visuelle Arbeitsfläche zum Erstellen von Kundenerlebnissen. Mit einer intuitiven Drag-and-Drop-Oberfläche können Sie jeden Schritt Ihres Journey orchestrieren, ohne Code zu schreiben.

![Benutzeroberfläche des Journey-Designers mit Palette, Arbeitsfläche und Eigenschaftenbereich](assets/journey38.png)

### Was Sie im Designer tun können:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=de)

**Einstiegspunkte definieren**

Wählen Sie aus, wie Kunden eintreten: durch ein Ereignis, ein Zielgruppensegment oder eine Zielgruppen-Qualifizierung.

[Erfahren Sie mehr über die Eintragsverwaltung](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=de)

**Nachrichten senden**

Verwenden Sie integrierte Kanalaktionen für E-Mail, Push, SMS/MMS, In-App, Web und mehr - alle in Journey Optimizer entwickelt.

[Senden von Nachrichten in Journey](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=de)

**Logik und Bedingungen hinzufügen**

Verzweigen Sie Ihren Journey anhand von Profilattributen, Zielgruppenzugehörigkeiten oder Echtzeit-Ereignissen.

[Nutzungsbedingungen](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=de)

**Nutzen von Daten**

Verwenden Sie kontextuelle Daten aus Ereignissen, Adobe Experience Platform oder API-Services von Drittanbietern.

[Arbeiten mit Datenquellen](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=de)

**Externe Systeme anschließen**

Erstellen Sie benutzerdefinierte Aktionen zur Integration von Drittanbietersystemen, um Nachrichten zu senden oder Workflows auszulösen.

[Benutzerdefinierter Aktionen konfigurieren](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=de)

**Orchestrierungsaktivitäten hinzufügen**

Verwenden Sie Wartezeiten, Sprünge, Profilaktualisierungen und Zielgruppen-Management, um komplexe Flüsse zu erstellen.

[Alle Aktivitäten anzeigen](about-journey-activities.md)
:::

::::

➡️ **Praktisches Lernen:** [Sehen Sie sich das Journey Designer-](#video) an oder [erkunden Sie End-to-End-Anwendungsfälle](jo-use-cases.md)

## Workflow zur Erstellung von Journey {#workflow}

Der Aufbau erfolgreicher Journey folgt einem klaren, wiederholbaren Prozess. Hier finden Sie Ihren Schritt-für-Schritt-Workflow:

**1. Plan** → **2. Design** → **3. Test** → **4. Veröffentlichen** → **5. Monitor** → **6. Optimieren**

### &#x200B;1. Journey planen {#plan}

Bevor Sie den Designer öffnen, klären Sie Ihre Ziele:

* **Was ist das Ziel?** (z. B. Aufnahme neuer Kunden, Rückgewinnung inaktiver Benutzer)
* **Wer ist das Publikum?** (spezifisches Segment, ereignisgesteuerte Kontakte)
* **Welcher Journey-Typ passt?** (Siehe [Journey-Typen](#journey-types) oben)
* **Welche Kanäle werden Sie verwenden?** (E-Mail, Push, SMS usw.)

### &#x200B;2. Design auf der Arbeitsfläche {#design}

Verwenden Sie den Journey-Designer, um Ihren Fluss zu erstellen:

1. **Einstiegsbedingungen festlegen** - Definieren, wie Profile eintreten (Ereignis, Audience, Qualifizierung)
2. **Orchestrierungslogik hinzufügen** - Wartezeiten, Bedingungen und Entscheidungspunkte einschließen
3. **Nachrichten konfigurieren** - Gestalten Sie Ihre Kommunikation oder nutzen Sie vorhandene Vorlagen.
4. **Aktionen einrichten** - Konfigurieren von integrierten oder benutzerdefinierten Aktionen, die ausgeführt werden sollen
5. **Beendigungskriterien definieren** - Geben Sie an, wann und wie Profile die Journey abschließen

[Erfahren Sie, wie Sie den Journey-Designer-→ verwenden](using-the-journey-designer.md)

### &#x200B;3. Vor der Live-Schaltung testen {#test}

Testen Sie Ihren Journey immer, um Probleme zu erkennen, bevor diese auftreten:

* Verwenden **Testmodus** um das Journey mit Testprofilen zu simulieren
* Verwenden Sie **Probelauf** um eine Vorschau der Journey-Ausführung anzuzeigen, ohne die echten Daten zu beeinflussen oder Nachrichten zu senden
* Überprüfen Sie, ob alle Bedingungen, Nachrichten und Aktionen erwartungsgemäß funktionieren
* Überprüfen von Timing, Datenflüssen und Personalisierung

[Testen des Journey-→](testing-the-journey.md) | [Erfahren Sie mehr über Probelauf →](journey-dry-run.md)

### &#x200B;4. Veröffentlichen des Journey {#publish}

Nach Abschluss des Tests veröffentlichen Sie , um Ihre Journey live zu schalten:

* Überprüfen der endgültigen Einstellungen und Eigenschaften
* Zur Aktivierung für echte Kunden veröffentlichen
* Hinweis: Live-Journey können angehalten, aber nicht bearbeitet werden (Sie müssen eine neue Version erstellen)

[Journey-→ veröffentlichen](publish-journey.md)

### &#x200B;5. Überwachen der Leistung {#monitor}

Verfolgen Sie, wie Ihr Journey in der realen Welt funktioniert:

* Anzeigen von Journey-Berichten und Analysen
* Überwachen von Eingabe-, Fertigstellungs- und Fehlerquoten
* Einrichten von Warnhinweisen für kritische Probleme

[Überwachen und Berichten von →](report-journey.md) | [Einrichten von Warnhinweisen →](../reports/alerts.md)

### &#x200B;6. Optimieren und iterieren {#optimize}

Nutzung von Einblicken zur Verbesserung:

* Analyse der Interaktionsmetriken und Konversionsraten
* Testen der Sendezeitoptimierung
* Erstellen neuer Journey-Versionen mit Verbesserungen
* KI-gestützte Empfehlungen verwenden

[Optimieren Sie Ihre Journey →](optimize.md) | [Sendezeit-→](send-time-optimization.md)

➡️ **Bereit zum Start?** [Erstellen Sie jetzt Ihre erste Journey →](journey-gs.md)

## Anwendungsfälle aus der Praxis {#use-cases}

Lernen Sie aus Praxisbeispielen, die zeigen, wie sich Journey-Konzepte zur Lösung gängiger Marketing-Herausforderungen einsetzen lassen:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=de)

**Willkommen bei neuen Abonnenten**

Wenn eine Kundin oder ein Kunde sich für Ihren Service anmeldet, legen Sie eine Begrüßungs-Journey als Trigger an, die die Kundinnen und Kunden dazu ermutigt, die Onboarding-Schritte abzuschließen.

[Anwendungsfall-→ anzeigen](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=de)

**Optimierung des Versandzeitpunkts**

Verwenden Sie KI, um E-Mails zu senden, wenn jeder Kunde mit größter Wahrscheinlichkeit interagiert, und maximieren Sie die Öffnungs- und Klickraten.

[Anwendungsfall-→ anzeigen](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=de)

**Steigern der Versandaktivität**

Erhöhen Sie das Nachrichtenvolumen schrittweise, um Ihre Reputation beim Versand zu verbessern und Probleme mit der Zustellbarkeit zu vermeiden.

[Anwendungsfall-→ anzeigen](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=de)

**Target nach Wochentag**

Senden Sie je nach Wochentag, an dem Kunden Ihre Journey eingeben, unterschiedliche Inhalte, um die Relevanz zu erhöhen.

[Anwendungsfall-→ anzeigen](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=de)

**Multi-Channel-Kampagnen**

Orchestrieren Sie nahtlose Erlebnisse für E-Mail, Push, SMS und Web-Kanäle in einer einzigen Journey.

[Anwendungsfall-→ anzeigen](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=de)

**Alle Anwendungsfälle**

Erkunden Sie die vollständige Bibliothek von Journey-Anwendungsfällen mit schrittweisen Implementierungen.

[Alle → durchsuchen](jo-use-cases.md) | [Anwendungsfall-→](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Journey-Funktionen {#capabilities}

Wenn Sie sich mit der Erstellung von Journey vertraut machen, sollten Sie diese leistungsstarken Funktionen erkunden, um anspruchsvolle Kundenerlebnisse zu schaffen:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=de)

**Erweiterte Ausdrücke**

Erstellen Sie dynamische Bedingungen und Personalisierung mit dem Ausdruckseditor für die Datenbearbeitung und komplexe Logik.

[Mehr zu Ausdrücken](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=de)

**Zeitzonen**

Verarbeiten Sie globale Zielgruppen mit automatischen Zeitzonenanpassungen und optimalen Versandzeiten.

[Verwalten von Zeitzonen](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=de)

**Testmodus und Probelauf**

Validieren Sie Journey mit Testprofilen, bevor Sie live gehen, und zeigen Sie eine Vorschau der Ausführung an, ohne die echten Daten zu beeinträchtigen.

[Probelauf verwenden](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=de)

**In Sandbox kopieren**

Duplizieren Sie Journey in Sandboxes, um Test- und Bereitstellungs-Workflows zu optimieren.

[Journey kopieren](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=de)

**Tags und Organisation**

Verwenden Sie Tags, um Journey zu kategorisieren und zu filtern und so eine skaliertere Verwaltung zu ermöglichen.

[Mit Tags organisieren](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=de)

**Durchsatzkontrolle**

Schränken Sie den Nachrichtendurchsatz ein, um die Reputation des Versands zu verwalten und zu vermeiden, dass die Systeme überlastet werden.

[Kontrollieren des Durchsatzes](limit-throughput.md)
:::

::::

[Alle Journey-Funktionen anzeigen →](/help/rp_landing_pages/manage-journey-landing-page.md)

## Lernen durch Beobachten {#video}

Hier erhalten Sie eine visuelle Einführung in das Journey von Komponenten und lernen die Grundlagen des Erstellens von Journey auf der Arbeitsfläche kennen:

>[!VIDEO](https://video.tv.adobe.com/v/3432378?captions=ger&quality=12)

➡️ **Möchten Sie mehr Videos?** [Erkunden von Journey-Video-Tutorials](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## Häufige Fragen {#common-questions}

**F: Was ist der Unterschied zwischen einer Journey und einer Kampagne?**

A: Adobe Journey Optimizer bietet drei Ansätze:

* **Journey**: 1:1 Echtzeit-Orchestrierung, bei der jedes Profil Schritte in seinem eigenen Tempo durchläuft. Optimiert für verhaltensgesteuerte mehrstufige Erlebnisse mit bedingter Logik (z. B. Onboarding, Warenkorbabbruch).

* **Kampagnen (Aktion und API-gesteuert)**: Einfacher Nachrichtenversand an Zielgruppen, gleichzeitige Ausführung an alle Profile entweder planmäßig oder über den API-Trigger. Optimiert für Werbekampagnen, Newsletter, Transaktionsnachrichten.

* **Orchestrierte Kampagnen**: Mehrstufige Batch-Workflows mit komplexer Segmentierung unter Verwendung relationaler Daten (Profile + Produkte/Geschäfte/Buchungen). Alle Profile werden mit exakten Zählungen vor dem Versand verarbeitet. Optimiert für saisonale Promotions, Produkteinführungen und Kampagnen, für die Daten mit mehreren Entitäten erforderlich sind.

**Hauptunterschied**: Journey verwalten den individuellen Kundenstatus für Echtzeit-Aktionen; Aktions-/API-Kampagnen liefern einfache Nachrichten im Batch; Orchestrierte Kampagnen bieten die Arbeitsfläche des Batch-Workflows mit Funktionen für die Segmentierung mehrerer Entitäten.

&#x200B;<!-- waiting for DOCAC-13912 [See detailed comparison](#journeys-vs-campaigns) | -->[Erfahren Sie mehr über orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)

<!-- Waiting for DOCAC-13912
**Q: Which journey type should I use?**

A: Use the [decision guide](#decision-guide) or [comparison table](#journey-types-comparison) to choose between Unitary, Read Audience, Audience Qualification, and Business Event journeys based on your trigger mechanism and use case.
-->

**F: Kann ich eine Live-Journey bearbeiten?**

A.: Sie können eingeschränkte Elemente (Name, Nachrichteninhalt) bearbeiten, aber strukturelle Änderungen erfordern die Erstellung einer neuen Version. [Informationen zu Journey-Versionen](publish-journey.md#journey-versions)

➡️ **Weitere Fragen?** [Vollständige Journey-FAQ anzeigen](journey-faq.md) mit mehr als 40 detaillierten Antworten

## Brauchen Sie Hilfe? {#help}

### Schnelllinks für häufige Aufgaben

* **[Erstellen Sie Ihre erste Journey](journey-gs.md)** - Schritt-für-Schritt-Anleitung für Anfänger
* **[Häufig gestellte Fragen zum Journey](journey-faq.md)** - Häufig gestellte Fragen beantwortet
* **[Fehlerbehebung](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - Diagnose und Behebung von Problemen
* **[Referenz zu Fehlercodes](error-codes-reference.md)** - Fehlermeldungen verstehen
* **[Leitplanken und Einschränkungen](../start/guardrails.md)** - Technische Grenzen und Best Practices

### Über Probleme benachrichtigt werden

Richten Sie **[Journey-Warnhinweise ein](../reports/alerts.md)** um Echtzeitbenachrichtigungen zu erhalten, wenn Journey auf Fehler oder ungewöhnliche Muster stoßen.

### Weitere Ressourcen

* **[Journey-Management-Hub](/help/rp_landing_pages/manage-journey-landing-page.md)** - Tools für Filterung, Optimierung und Profilverwaltung
* **[Journey-Aktivitätenreferenz](/help/rp_landing_pages/about-journey-building-landing-page.md)** - Vollständige Anleitung zu allen Aktivitätstypen
* **[Fehlerbehebung bei Ausführungsproblemen](troubleshooting-execution.md)** - Debuggen von Journey-Ausführungsproblemen
* **[Fehlerbehebung für eingehende Aktivitäten](troubleshooting-inbound.md)** - Beheben von Eingabe- und Qualifizierungsproblemen

**Sind Sie bereit, Ihre erste Journey zu erstellen?** [Erste Schritte jetzt →](journey-gs.md)
