---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Journeys
description: Erste Schritte mit Journeys – Erfahren Sie mehr über Journey-Typen, Workflows, Funktionen und Best Practices für die Erstellung personalisierter Kundenerlebnisse in Adobe Journey Optimizer
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: Journey, Entdecken, Erste Schritte, Unitär, Zielgruppe lesen, Zielgruppen-Qualifizierung, Geschäftsereignis, Echtzeit, Geplant, Batch, Ereignisgesteuert, Workflow, Orchestrierung, Personalisierung, Multi-Channel
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 522dba0516268a17e72f56c0f28205ba60709d78
workflow-type: ht
source-wordcount: '1448'
ht-degree: 100%

---


# Erste Schritte mit Journeys{#jo-general-principle}

In Adobe Journey Optimizer können Sie personalisierte, mehrstufige Customer Journeys erstellen, die sich in Echtzeit an das Verhalten und die Bedürfnisse Ihrer Zielgruppe anpassen. Mithilfe einer intuitiven Drag-and-Drop-Arbeitsfläche können Sie Nachrichten und Aktionen über mehrere Kanäle hinweg orchestrieren und dabei kontextuelle Daten und Zielgruppen-Targeting nutzen, um maximale Wirkung zu erzielen.

Dieses Handbuch bietet eine klare Roadmap, die Ihnen hilft, die Grundlagen von Journeys zu verstehen, den richtigen Journey-Typ für Ihren Anwendungsfall auszuwählen und Journeys zu entwerfen, die aussagekräftige, zeitnahe Kundenerlebnisse bieten.

## Was sind Journeys?

**Journeys** sind automatisierte, mehrstufige Kundenerlebnisse, die als Reaktion auf Kundenverhalten, Geschäftsereignisse oder geplante Kampagnen personalisierte Interaktionen kanalübergreifend orchestrieren.

Verwenden Sie [!DNL Journey Optimizer] für Folgendes:

* Erstellen von Anwendungsfällen für die **Echtzeit-Orchestrierung** mithilfe von kontextuellen Daten, die in Ereignissen oder Datenquellen gespeichert sind
* Entwerfen **mehrstufiger fortgeschrittener Szenarien**, die dynamisch auf Kundenverhalten und Geschäftsereignisse reagieren
* Bereitstellen von **1:1 personalisierten Erlebnisse** im benötigten Umfang über E-Mail, Push, SMS, In-App, Web und mehr

![Benutzeroberfläche des Journey-Designers mit Palette, Arbeitsfläche und Eigenschaftenbereich](assets/journey38.png)

➡️ **Bereit, mit dem Erstellen zu beginnen?** [Erstellen Sie Ihre erste Journey](journey-gs.md) in 5 Minuten.

### Journeys vs. Kampagnen: Verwendungszwecke {#journeys-vs-campaigns-intro}

Adobe Journey Optimizer bietet drei Ansätze, um Kundinnen und Kunden zu erreichen: **Journeys** (1:1 Echtzeit-Orchestrierung), **Kampagnen** (einfacher Batch- oder durch API ausgelöster Versand) und **orchestrierte Kampagnen** (Batch-Arbeitsflächen-Workflows mit Daten aus mehreren Entitäten).

**Schnelle Entscheidung:**

* Verwenden Sie **Journeys** für mehrstufige, verhaltensgesteuerte Erlebnisse, bei denen jede Kundin und jeder Kunde im eigenen Tempo Fortschritte macht
* Verwenden Sie **Aktions/API-Kampagnen** für einen einfachen, geplanten oder ausgelösten Nachrichtenversand an Zielgruppen
* Verwenden Sie **orchestrierte Kampagnen** für komplexe Batch-Workflows, die eine Segmentierung mehrerer Entitäten und exakte Zählungen vor dem Versand erfordern

<!-- waiting for DOCAC-13912
➡️ **[View detailed comparison: Journeys vs Campaigns](../start/journeys-vs-campaigns.md)** - Includes decision guide, use cases, and feature availability-->

## Auswählen Ihres Journey-Typs {#journey-types}

Adobe Journey Optimizer unterstützt vier Journey-Typen, die jeweils für unterschiedliche Eintrittsmechanismen und Geschäftsszenarien konzipiert sind:

* **Unitäre Journeys**: Ereignisgesteuerte Erlebnisse in Echtzeit (Auftragsbestätigungen, Willkommens-E-Mails)
* **Journeys des Typs „Zielgruppe lesen“**: Geplante Batch-Nachrichten an Zielgruppensegmente (Newsletter, Werbekampagnen)
* **Journeys des Typs „Zielgruppen-Qualifizierung“**: Echtzeit-Reaktionen auf Änderungen bei der Zielgruppenzugehörigkeit (VIP-Upgrades, Rückgewinnung)
* **Journeys des Typs „Geschäftsereignis“**: Geschäftsbedingungen, die mehrere Kundinnen und Kunden gleichzeitig betreffen (Inventar-Warnhinweise, Flash-Verkäufe)

<!-- waiting for DOCAC-13912 
➡️ **[Journey types and selection guide](journey-types-selection.md)** - Detailed comparison, decision tree, and feature compatibility matrix -->

## Erstellen mit dem Journey-Designer {#journey-designer}

Der **[Journey-Designer](using-the-journey-designer.md)** ist Ihre visuelle Arbeitsfläche zum Erstellen von Kundenerlebnissen. Mit einer intuitiven Drag-and-Drop-Oberfläche können Sie jeden Schritt Ihrer Journey orchestrieren, ohne Code schreiben zu müssen.

![Benutzeroberfläche des Journey-Designers mit Palette, Arbeitsfläche und Eigenschaftenbereich](assets/journey38.png)

### Was Sie im Designer tun können:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Eintrittspunkte definieren**

Wählen Sie aus, wie Kundinnen und Kunden eintreten: über ein Ereignis, ein Zielgruppensegment oder eine Zielgruppen-Qualifizierung.

[Informationen zur Eintrittsverwaltung](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

**Nachrichten senden**

Verwenden Sie integrierte Kanalaktionen für E-Mail, Push, SMS/MMS, In-App, Web und mehr – alle in Journey Optimizer erstellt.

[Senden von Nachrichten in Journeys](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**Logik und Bedingungen hinzufügen**

Verzweigen Sie Ihre Journey basierend auf Profilattributen, Zielgruppenzugehörigkeit oder Echtzeit-Ereignissen.

[Verwenden von Bedingungen](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**Daten verwenden**

Verwenden Sie kontextuelle Daten aus Ereignissen, Adobe Experience Platform oder API-Services von Drittanbietern.

[Arbeiten mit Datenquellen](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Externe Systeme anschließen**

Erstellen Sie benutzerdefinierte Aktionen, um Drittanbietersysteme für den Versand von Nachrichten oder das Auslösen von Workflows zu integrieren.

[Benutzerdefinierter Aktionen konfigurieren](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Orchestrierungsaktivitäten hinzufügen**

Verwenden Sie Wartezeiten, Sprünge, Profilaktualisierungen und Zielgruppen-Management, um komplexe Flüsse zu erstellen.

[Erkunden aller Aktivitäten](about-journey-activities.md)
:::

::::

➡️ **Praxisnahes Lernen:** [Sehen Sie sich das Video zum Journey-Designer](#video) an oder [erkunden Sie End-to-End-Anwendungsfälle](jo-use-cases.md)

## Workflow zur Erstellung von Journeys {#workflow}

Das Erstellen erfolgreicher Journeys folgt einem klaren, wiederholbaren Prozess. Im Folgenden finden Sie den Schritt-für-Schritt-Workflow:

**1. Planung** → **2. Gestaltung** → **3. Testen** → **4. Veröffentlichung** → **5. Überwachung** → **6. Optimierung**

### &#x200B;1. Planen Ihrer Journey {#plan}

Bevor Sie den Designer öffnen, klären Sie Ihre Ziele:

* **Was ist das Ziel?** (z. B. Onboarding neuer Kundschaft, Rückgewinnung inaktiver Benutzender)
* **Wer ist die Zielgruppe?** (spezifisches Segment, ereignisgesteuerte Kontakte)
* **Welcher Journey-Typ ist am besten geeignet?** (siehe [Journey-Typen](#journey-types) oben)
* **Welche Kanäle möchten Sie verwenden?** (E-Mail, Push, SMS usw.)

### &#x200B;2. Gestalten auf der Arbeitsfläche {#design}

Verwenden Sie den Journey-Designer, um Ihren Fluss zu erstellen:

* **Festlegen von Eintrittsbedingungen** – Definieren Sie, wie Profile eintreten (Ereignis, Zielgruppe, Qualifizierung)
* **Hinzufügen von Orchestrierungslogik** – Schließen Sie Wartezeiten, Bedingungen und Entscheidungspunkte ein
* **Konfigurieren von Nachrichten** – Erstellen Sie Ihre Nachrichten oder verwenden Sie vorhandene Vorlagen
* **Einrichten von Aktionen** – Konfigurieren Sie integrierte oder benutzerdefinierte Aktionen, die ausgeführt werden sollen
* **Definieren von Austrittskriterien** – Geben Sie an, wann und wie Profile die Journey abschließen

[Informationen zur Verwendung des Journey-Designers -→](using-the-journey-designer.md)

### &#x200B;3. Testen vor der Live-Schaltung {#test}

Testen Sie Ihren Journey immer gründlich, um Probleme zu beheben, bevor Ihre Kundinnen und Kunden diese bemerken:

* Verwenden Sie **Testmodus**, um die Journey mit Testprofilen zu simulieren
* Verwenden Sie **Probelauf**, um die Journey-Ausführung in der Vorschau anzuzeigen, ohne die echten Daten zu beeinflussen oder Nachrichten zu senden
* Überprüfen Sie, ob alle Bedingungen, Nachrichten und Aktionen erwartungsgemäß funktionieren
* Überprüfen Sie Timing, Datenflüsse und Personalisierung

[Testen der Journey →](testing-the-journey.md) | [Informationen zum Probelauf →](journey-dry-run.md)

### &#x200B;4. Veröffentlichen Ihrer Journey {#publish}

Sobald die Tests abgeschlossen sind, veröffentlichen Sie Ihre Journey, um sie live zu schalten:

* Überprüfen Sie die endgültigen Einstellungen und Eigenschaften
* Veröffentlichen Sie die Journey, um sie für echte Kundinnen und Kunden zu aktivieren
* Hinweis: Live-Journeys können gestoppt, aber nicht bearbeitet werden (dazu müssen Sie eine neue Version erstellen)

[Veröffentlichen der Journey →](publish-journey.md)

### &#x200B;5. Überwachen der Leistung {#monitor}

Verfolgen Sie, wie Ihre Journey in der Praxis abschneidet:

* Zeigen Sie Journey-Berichte und -Analysen an
* Überwachen Sie Eintritts-, Abschluss- und Fehlerraten
* Richten Sie Warnhinweise für kritische Probleme ein

[Überwachen und Berichte →](report-journey.md) | [Einrichten von Warnhinweisen →](../reports/alerts.md)

### &#x200B;6. Optimieren und Iterieren {#optimize}

Nutzen Sie Erkenntnisse zur Verbesserung:

* Analysieren Sie die Interaktionsmetriken und Konversionsraten
* Testen Sie die Versandzeitoptimierung
* Erstellen Sie neue Journey-Versionen mit Verbesserungen
* Verwenden Sie KI-gestützte Empfehlungen

[Optimieren Ihrer Journeys →](optimize.md) | [Versandzeitoptimierung →](send-time-optimization.md)

➡️ **Bereit zum Loslegen?** [Erstellen Sie jetzt Ihre erste Journey →](journey-gs.md)

## Anwendungsfälle aus der Praxis {#use-cases}

Lernen Sie aus Praxisbeispielen, die zeigen, wie sich Journey-Konzepte zur Lösung gängiger Marketing-Herausforderungen einsetzen lassen:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

**Neue Abonnierende willkommen heißen**

Wenn sich eine Kundin oder ein Kunde für Ihren Service anmeldet, lösen Sie eine Begrüßungs-Journey aus, die die Kundinnen und Kunden dazu ermutigt, die Onboarding-Schritte abzuschließen.

[Anzeigen des Anwendungsfalls →](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg)

**Versandzeitoptimierung**

Verwenden Sie KI, um E-Mails genau dann zu senden, wenn die Interaktionswahrscheinlichkeit für jede Kundin und jeden Kunden am höchsten ist, um Öffnungs- und Klickraten zu maximieren.

[Anzeigen des Anwendungsfalls →](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Versandaktivität steigern**

Erhöhen Sie das Nachrichtenvolumen schrittweise, um Ihre Reputation beim Versand aufzubauen und Probleme mit der Zustellbarkeit zu vermeiden.

[Anzeigen des Anwendungsfalls →](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**Targeting nach Wochentag**

Senden Sie unterschiedliche Inhalte basierend auf dem Wochentag, an dem Kundinnen und Kunden in Ihre Journey eintreten, um eine höhere Relevanz zu erzielen.

[Anzeigen des Anwendungsfalls →](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Multi-Channel-Kampagnen**

Orchestrieren Sie nahtlose Erlebnisse über E-Mail, Push, SMS und Web-Kanäle hinweg in einer einzigen Journey.

[Anzeigen des Anwendungsfalls →](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg)

**Alle Anwendungsfälle:**

Erkunden Sie die vollständige Bibliothek von Journey-Anwendungsfällen mit Schritt-für-Schritt-Anleitungen zur Implementierung.

[Alle durchsuchen →](jo-use-cases.md) | [Anwendungsfallbibliothek →](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Erkunden von Journey-Funktionen {#capabilities}

Sobald Sie mit der Erstellung von Journeys vertrauter sind, können Sie diese leistungsstarken Funktionen erkunden, um anspruchsvolle Kundenerlebnisse zu schaffen:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Erweiterte Ausdrücke**

Erstellen Sie dynamische Bedingungen und Personalisierungen mithilfe des Ausdruckseditors für Datenbearbeitung und komplexe Logik.

[Mehr zu Ausdrücken](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg)

**Zeitzonen**

Bedienen Sie globale Zielgruppen mit automatischer Zeitzonenanpassung und optimalen Versandzeiten.

[Verwalten von Zeitzonen](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

**Testmodus und Probelauf**

Validieren Sie Journeys vor der Live-Schaltung mit Testprofilen und zeigen Sie die Ausführung in der Vorschau an, ohne echte Daten zu beeinträchtigen.

[Verwenden von Probelauf](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**In Sandbox kopieren**

Duplizieren Sie Journeys in Sandboxes, um Test- und Bereitstellungs-Workflows zu optimieren.

[Journeys kopieren](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg)

**Tags und Organisation**

Verwenden Sie Tags, um Journeys zu kategorisieren und zu filtern, damit Sie diese auch in großem Umfang verwalten können.

[Mit Tags organisieren](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Durchsatzsteuerung**

Begrenzen Sie den Nachrichtendurchsatz, um die Reputation beim Versand zu verwalten und eine Überlastung der Systeme zu vermeiden.

[Steuern des Durchsatzes](limit-throughput.md)
:::

::::

[Alle Journey-Funktionen anzeigen →](/help/rp_landing_pages/manage-journey-landing-page.md)

## Lernen per Video {#video}

Erhalten Sie eine visuelle Einführung in Journey-Komponenten und lernen Sie die Grundlagen der Journey-Erstellung auf der Arbeitsfläche kennen:

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

➡️ **Möchten Sie mehr Videos sehen?** [Erkunden von Video-Tutorials für Journeys](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## Häufige Fragen {#common-questions}

+++ Was ist der Unterschied zwischen einer Journey und einer Kampagne?

Adobe Journey Optimizer bietet drei Ansätze:

* **Journeys** – 1:1 Echtzeitorchestrierung, wobei jedes Profil die Schritte in seinem eigenen Tempo durchläuft. Ideal für verhaltensgesteuerte, mehrstufige Erlebnisse mit bedingter Logik (z. B. Onboarding, Warenkorbabbruch).

* **Kampagnen (Aktion und durch API ausgelöst)**: Einfacher Nachrichtenversand an Zielgruppen, der gleichzeitig für alle Profile ausgeführt wird, entweder nach Zeitplan oder über API-Auslösung. Ideal für Werbekampagnen, Newsletter und Transaktionsnachrichten.

* **Orchestrierte Kampagnen**: Mehrstufige Batch-Workflows mit komplexer Segmentierung unter Verwendung relationaler Daten (Profile + Produkte/Geschäfte/Buchungen). Alle Profile werden mit exakten Zählungen vor dem Versand gemeinsam verarbeitet. Ideal für saisonale Werbeaktionen, Produkteinführungen und Kampagnen, die Daten aus mehreren Entitäten erfordern.

**Hauptunterschied**: Journeys halten den individuellen Kundenstatus für Echtzeit-Aktionen fest; Aktions-/API-Kampagnen versenden einfache Nachrichten im Batch-Verfahren; orchestrierte Kampagnen bieten eine Arbeitsfläche für Batch-Workflows mit Funktionen zur Segmentierung mehrerer Entitäten.

<!-- waiting for DOCAC-13912 - [See detailed comparison](#journeys-vs-campaigns) -->
[Informationen zu orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)

+++

<!-- Waiting for DOCAC-13912
+++ Which journey type should I use?

Use the [decision guide](#decision-guide) or [comparison table](#journey-types-comparison) to choose between Unitary, Read Audience, Audience Qualification, and Business Event journeys based on your trigger mechanism and use case.

+++
-->

+++ Kann ich eine Live-Journey bearbeiten?

Sie können eingeschränkte Elemente bearbeiten (Name, Nachrichteninhalt), strukturelle Änderungen erfordern jedoch die Erstellung einer neuen Version. [Informationen zu Journey-Versionen](publish-journey.md#journey-versions)

+++

➡️ **Haben Sie weitere Fragen?** [Zeigen Sie eine vollständige Übersicht der häufig gestellten Fragen zu Journeys](journey-faq.md) mit mehr als 40 detaillierten Antworten an

## Benötigen Sie Hilfe? {#help}

### Schnell-Links für häufige Aufgaben

* **[Erstellen Ihrer ersten Journey](journey-gs.md)** – Schritt-für-Schritt-Anleitung, wenn Sie gerade erst beginnen
* **[Häufig gestellte Fragen zu Journeys](journey-faq.md)** – Antworten auf häufig gestellte Fragen
* **[Fehlerbehebung](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** – Probleme diagnostizieren und beheben
* **[Referenz zu Fehler-Codes](error-codes-reference.md)** – Fehlermeldungen verstehen
* **[Leitlinien und Einschränkungen](../start/guardrails.md)** – Technische Grenzen und Best Practices

### Benachrichtigung bei Problemen

Richten Sie **[Journey-Warnhinweise](../reports/alerts.md)** ein, um Echtzeitbenachrichtigungen zu erhalten, wenn in Journeys Fehler oder ungewöhnliche Muster auftreten.

### Weitere Ressourcen

* **[Journey-Management-Hub](/help/rp_landing_pages/manage-journey-landing-page.md)** – Tools für Filterung, Optimierung und Profilverwaltung
* **[Referenz für Journey-Aktivitäten](/help/rp_landing_pages/about-journey-building-landing-page.md)** – Vollständige Anleitung zu allen Aktivitätstypen
* **[Fehlerbehebung bei Ausführungsproblemen](troubleshooting-execution.md)** – Debuggen von Journey-Ausführungsproblemen
* **[Fehlerbehebung bei eingehende Aktivitäten](troubleshooting-inbound.md)** – Beheben von Eintritts- und Qualifizierungsproblemen

**Sind Sie bereit, Ihre erste Journey zu erstellen?** [Legen Sie jetzt los](journey-gs.md)
