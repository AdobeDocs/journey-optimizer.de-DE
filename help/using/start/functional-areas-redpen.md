---
solution: Journey Optimizer
product: journey optimizer
title: Funktionsbereiche
description: Funktionsbereiche in AJO
feature: Get Started
role: Admin, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: c9b02ae2-e07b-41f4-90cc-b2c0966f1ed1
hide: true
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: ht
source-wordcount: '1448'
ht-degree: 100%

---

# Grundlegende Konzepte

Adobe Journey Optimizer (AJO) umfasst mehrere wichtige Funktionsbereiche, die nahtlos zusammenarbeiten. In diesem Handbuch werden die einzelnen Bereiche erläutert und beschrieben, wie sich diese Bereiche zusammen nutzen lassen, um beeindruckende Kundenerlebnisse zu schaffen. Wenn Sie diese Funktionsbereiche verstehen, wird sichergestellt, dass Sie AJO nutzen können, um personalisierte Omnichannel-Erlebnisse effizient bereitzustellen.

## Überblick über Funktionsbereiche

| Funktionsbereich | Primärer Vorteil  | Analogie |
|-------------------------|--------------------------------------------------|------------------------|
| Daten-Management | Organisieren der richtigen Kundendaten | Das Fundament |
| Kunden-Management | Verstehen, wer Ihre Kundschaft ist | Kennen Sie Ihre Zielgruppe |
| Content-Management | Erstellen und Verwalten konsistenter, personalisierter Nachrichten | Erstellen einer Nachricht |
| Entscheidungs-Management | Auswählen der besten Nachricht/des besten Angebots in Echtzeit | Das Gehirn |
| Journey-Management | Gestalten und Automatisieren von nahtlosen Kundenerlebnissen | Dirigentin bzw. Dirigent des Orchesters |
| Verbindungen | Verbinden von Datenquellen und Bereitstellen über Kundenkanäle | Die Rohre |
| Administration und Datenschutz | Kontrollieren von Einrichtung sowie Zugriff und Sicherstellen der Datenkonformität | Das Regelwerk |

## Detaillierte Funktionsbereiche

### Daten-Management: Das Fundament

**Zweck**: Aufnehmen, Strukturieren und Verwalten der Daten, die die Personalisierung ermöglichen. Dieser Prozess umfasst die Definition von Datenstrukturen (Schemata), die Erstellung von Speicher-Containern (Datensätze) und den Import von Daten aus verschiedenen Systemen.

Behandeln Sie das Daten-Management als Grundlage für alle Kundeninteraktionen. Durch ein gut strukturiertes Datenfundament wird sichergestellt, dass jede Entscheidung, jede Nachricht und jede Journey präzise und organisierte Daten verwendet.

**Schlüsselkomponenten**:

- **Erstellung und Verwaltung von Schemata**: Definieren Sie die Struktur von Kundendaten.
   - Beispiel: Erstellen Sie ein Schema mit Feldern wie „Vorname“, „E-Mail-Adresse“ und „Kaufverlauf“.
- **Datensatzkonfiguration**: Organisieren Sie Daten in logischen Containern.
   - Beispiel: Gruppieren von Transaktionsdaten in einem Datensatz namens „Verkaufstransaktionen“ für eine einfachere Analyse.
- **Datenaufnahme-Workflows**: Importieren Sie Daten effizient in die Plattform.
   - Beispiel: Verwenden Sie vorkonfigurierte Quell-Connectoren, um Kundendaten aus einem CRM-System (Customer Relationship Management) zu importieren.
- **Datenqualitäts-Tools**: Gewährleisten Sie die Genauigkeit und Vollständigkeit der Daten.

**Vorteil**: Stellt sicher, dass Kundendaten zuverlässig, organisiert und zugänglich sind, was die Grundlage für alle AJO-Aktivitäten bildet. Vorkonfigurierte Quell-Connectoren optimieren die Datenaufnahme aus gängigen Plattformen.



### Kunden-Management: Kennen Sie Ihre Zielgruppe

**Zweck**: Aufbau und Pflege eines gründlichen Verständnisses einzelner Kundinnen und Kunden. Dazu gehört die Verwendung des Echtzeit-Kundenprofils von Adobe Experience Platform (AEP), mit dem sich Daten aus allen Touchpoints in einer einheitlichen Ansicht zusammenführen lassen. Zudem verwaltet es Identitäten über Geräte und Kanäle hinweg und ermöglicht so die Gruppierung von einzelnen Personen in Zielgruppen basierend auf gemeinsamen Attributen oder Verhaltensweisen.

Kunden-Management-Tools verbinden unterschiedliche Datenpunkte, um ein einheitliches Bild jeder Kundin und jedes Kunden zu liefern. So wird sichergestellt, dass Sie für relevante und personalisierte Erlebnisse sorgen können.

**Schlüsselkomponenten**:

- **Echtzeit-Kundenprofil**: Einheitliche Ansicht einzelner Kundinnen und Kunden.
   - Beispiel: Kombinieren von Webbrowser-Verlauf, App-Interaktionen und Offline-Käufe in einem einzigen Profil.
- **Identitätsauflösung**: Verknüpfen von Kundendaten über verschiedene Geräte und Kanäle hinweg.
   - Beispiel: Gleichen Sie mithilfe des Identitätsdiagramms die E-Mail-Adresse einer Person mit ihren App-Nutzungsdaten ab.
- **Zielgruppenerstellung und -verwaltung**: Definieren von Gruppen basierend auf Attributen und Verhaltensweisen.
   - Beispiel: Erstellen Sie eine Zielgruppe für „Treue Kundschaft“, die im letzten Jahr mehr als fünf Käufe getätigt hat.
- **Segmentierung**: Anwenden von Regeln für dynamische Zielgruppenzugehörigkeit.
   - Beispiel: Richten Sie ein Segment für „Ausgabefreudige Käuferschaft“, das automatisch aktualisiert wird, wenn Kundinnen oder Kunden mehr als 500 € ausgeben.

**Vorteil**: Ermöglicht durch ein dynamisches Verständnis individueller Vorlieben, Historie und Segmentzugehörigkeiten eine präzise Zielgruppenbestimmung und Personalisierung.



### Content-Management: Erstellen Ihrer Nachricht

**Zweck**: Erstellen, Verwalten, Personalisieren und Wiederverwenden von Marketing-Inhalten über verschiedene Kanäle hinweg. Das umfasst die Verwaltung digitaler Assets, die Erstellung von Nachrichten mit visuellen Editoren oder Code, die Nutzung wiederverwendbarer Inhaltsvorlagen und Fragmente, die Einrichtung von Landingpages und die Verwendung künstlicher Intelligenz (KI) zur Inhaltserstellung.

Content-Management-Tools stellen sicher, dass Teams effizient maßgeschneiderte Nachrichten definieren und bereitstellen und dabei an jedem Touchpoint für Konsistenz und Relevanz sorgen können.

**Schlüsselkomponenten**:

- **Inhaltseditoren**: Erstellen und Formatieren von Nachrichten visuell oder mit Code.
   - Beispiel: Verwenden Sie den visuellen Editor, um eine E-Mail-Kampagne zu entwerfen, mit der das Weihnachtsgeschäft beworben werden.
- **Digital Asset Management**: Organisieren und Verwenden von Bildern und anderen Medien.
   - Beispiel: Speichern Sie Produktbilder in einer zentralen Bibliothek, um sie in Kampagnen bequem wiederverwenden zu können.
- **Vorlagen und Fragmente**: Erstellen von wiederverwendbaren Inhaltskomponenten.
   - Beispiel: Erstellen Sie eine Vorlage namens „Willkommensnachricht“, die Kundennamen dynamisch einfügt.
- **Personalisierungs-Tools**: Dynamisches Anpassen von Inhalten für Einzelpersonen.
   - Beispiel: Zeigen Sie basierend auf dem Navigationsverlauf personalisierte Produktempfehlungen an.
- **Landingpage-Builder**: Erstellen von Web-Zielen für Kampagnen.

**Vorteil**: Optimiert die Inhaltserstellung, sorgt für Markenkonsistenz und erleichtert den effizienten Versand hochgradig personalisierter Nachrichten.



### Entscheidungs-Management: Das Gehirn der Personalisierung

**Zweck**: Für jede Kundin und jeden Kunden zum richtigen Zeitpunkt die beste Nachricht oder das beste Angebot auswählen. Das geschieht anhand des Echtzeit-Profils der Person, des Kontexts und vordefinierter Geschäftsregeln oder KI-Modelle. Das Entscheidungs-Management umfasst das Verwalten einer zentralen Bibliothek mit Angeboten, das Definieren von Eignungsregeln, das Anwenden von Einschränkungen (wie Frequenzbegrenzung) und das Einrichten einer Ranking-Logik.

Das Entscheidungs-Management stellt sicher, dass die Personalisierung in großem Maßstab funktioniert, indem es durch intelligente Automatisierung einen maximalen Mehrwert liefert.

**Schlüsselkomponenten**:

- **Angebotsbibliothek**: Zentrales Repository für Marketing-Angebote.
   - Beispiel: Speichern Sie Angebote wie „Coupon für 20 % Rabatt“ oder „Kostenloser Versand“ in einer gemeinsamen Bibliothek.
- **Entscheidungsregeln**: Logik für die Auswahl optimaler Inhalte.
   - Beispiel: Zeigen Sie nur der Kundschaft im Segment „Treue Kundschaft“ einen „Treuerabatt“ an.
- **Einschränkungen und Eignung**: Kontrollieren, wer was wann erhält.
   - Beispiel: Wenden Sie eine Frequenzbegrenzung an, um zu verhindern, dass eine Kundin oder ein Kunde dasselbe Angebot zweimal in einer Woche erhält.
- **Ranking-Strategien**: Priorisieren von Angeboten anhand von Geschäftszielen oder mithilfe von KI.
   - Beispiel: Angebote werden nach Rentabilität sortiert, wobei Produkte mit hoher Marge zuerst angezeigt werden.
- **Simulations-Tools**: Testen und Validieren von Entscheidungsstrategien.

**Vorteil**: Automatisiert und optimiert die Personalisierung, um sicherzustellen, dass an jedem Touchpoint relevante und effektive Erlebnisse bereitgestellt werden.



### Journey-Management: Der Dirigent des Orchesters

**Zweck**: Entwerfen, Orchestrieren und Automatisieren von Kundenerlebnisse über mehrere Schritte und Kanäle hinweg. Journeys reagieren in Echtzeit auf Kundenverhalten und -ereignisse und leiten Personen durch personalisierte Pfade. AJO unterstützt zudem Kampagnen zum Versand von geplanten, einmaligen Nachrichten an bestimmte Zielgruppen.

Das Journey-Management stellt sicher, dass Erlebnisse sich adaptiv und nahtlos anfühlen, und leitet einzelne Personen auf der Grundlage ihrer Vorlieben und Handlungen an.

**Schlüsselkomponenten**:

- **Journey-Designer**: Visuelle Arbeitsfläche zum Erstellen von Kundenpfaden.
   - Beispiel: Entwerfen Sie eine Journey, die eine Begrüßungs-E-Mail sendet, wenn sich eine Kundin oder ein Kunde anmeldet.
- **Journey-Auslöser**: Ereignisse, die Journeys auslösen oder voranbringen.
   - Beispiel: Auslösen einer Folgenachricht, nachdem eine Kundin oder ein Kunde ihren bzw. seinen Warenkorb abgebrochen hat.
- **Bedingungsschritte**: Verwenden von logischen Verzweigungen.
   - Beispiel: Senden Sie eine unterschiedliche Nachricht, je nachdem, ob jemand eine E-Mail öffnet oder nicht.
- **Warteaktivitäten**: Kontrollieren des Fortschritts mit Zeitverzögerungen.
   - Beispiel: Drei Tage warten, bevor eine Erinnerungs-E-Mail gesendet wird.
- **Kampagnenverwaltung**: Tools für geplante, einmalige Nachrichten.

**Vorteil**: Erstellt nahtlose, vernetzte Erlebnisse, die sich an individuelle Interaktionen anpassen, was die Beziehungen pflegt und die gewünschten Ergebnisse fördert.



### Verbindungen: Die Rohre

**Zweck**: Verwalten des Datenflusses in AJO (Quellen) und des Nachrichten- oder Datenversands aus AJO (Kanäle und Ziele). Datenquellen speisen Daten in Adobe Experience Platform (AEP) ein. Kanäle stellen Nachrichten bereit (per E-Mail, SMS, Push, Web usw.). Ziele ermöglichen den Fluss von Zielgruppen- oder Datensatzinformationen zu externen Plattformen.

Verbindungen sorgen dafür, dass Daten effektiv in AJO eingespeist werden und die Kundschaft über die richtigen Touchpoints zuverlässig erreichen.

**Schlüsselkomponenten**:

- **Quell-Connectoren**: Dienen dem Importieren von Daten in die Plattform.
   - Beispiel: Verwenden Sie einen Connector, um Kaufdaten von einer E-Commerce-Plattform zu übertragen.
- **Kanalkonfiguration**: Konfigurieren und verwalten von Versandmechanismen.
   - Beispiel: Konfigurieren Sie den SMS-Versand für Werbenachrichten.
- **Zieleinrichtung**: Herstellen einer Verbindung zu externen Aktivierungssystemen.
   - Beispiel: Freigeben von Zielgruppendaten über eine Social-Media-Werbeplattform.
- **Datenflussverwaltung**: Verwaltung von Datenbewegungen.

**Vorteil**: Sorgt für eine effiziente Datenaufnahme und einen zuverlässigen Nachrichtenversand über alle Kanäle hinweg und ermöglicht gleichzeitig eine Aktivierung in externen Systemen.



### Administration und Datenschutz: Das Regelwerk

**Zweck**: Konfigurieren der Systemeinstellungen, Verwalten von Benutzerzugriff und Berechtigungen, Einrichten von Kommunikationskanälen, Definieren von Journey-Parametern und Sicherstellen der Einhaltung von Datenschutz- und Governance-Richtlinien. Dazu gehören die Einverständnisverwaltung, die Anwendung von Datennutzungsregeln und die Verarbeitung von Datenzugriffs- oder Löschanfragen.

Administrations- und Datenschutz-Tools stellen sicher, dass die Datenintegrität gewahrt bleibt und alle rechtlichen und organisatorischen Richtlinien eingehalten werden.

**Schlüsselkomponenten**:

- **Benutzer- und Zugriffsverwaltung**: Steuern von Zugriff und Berechtigungen.
   - Beispiel: Weisen Sie Marketing- und IT-Teams bestimmte Berechtigungen zu.
- **Sandbox-Konfiguration**: Separate Umgebungen für Entwicklung und Tests.
   - Beispiel: Verwenden Sie eine Sandbox, um neue Journey-Designs zu testen, bevor Sie sie live bereitstellen.
- **Kanaleinrichtung**: Konfigurieren technischer Einstellungen für den Versand.
   - Beispiel: Richten Sie Details des E-Mail-Servers für Kampagnen-Messaging ein.
- **Datenschutz-Tools**: Verwalten von Einverständnis und Datenschutz.
   - Beispiel: Bearbeiten Sie Anfragen zur Löschung von Daten gemäß DSGVO (Datenschutz-Grundverordnung) effizient.
- **Governance-Kontrollen**: Durchsetzen von Datennutzungsrichtlinien.

**Vorteil**: Stellt einen sicheren Plattformbetrieb, die Einhaltung von Vorschriften und die Abstimmung mit den Richtlinien des Unternehmens sicher.



## Verbinden der Punkte: So funktioniert alles zusammen

All diese Funktionsbereiche arbeiten in einem kontinuierlichen Zyklus, um personalisierte Kundenerlebnisse bereitzustellen und zu optimieren:

1. **Datenaufnahme**: Datenflüsse in AEP, strukturiert per Daten-Management.
2. **Kundenverständnis**: Echtzeit-Kundenprofile vereinheitlichen diese Daten, während das Kunden-Management Einblicke durch Profile und Zielgruppen verfeinert.
3. **Content- und Angebotsstrategie**: Das Content-Management erstellt Nachrichten und Assets. Das Entscheidungs-Management definiert die Angebote und die Logik für die Auswahl des besten Angebots.
4. **Orchestrierung**: Journey-Management ordnet Interaktionen kanalübergreifend zu und nutzt dabei Kundenverständnis, Inhalte und Entscheidungen.
5. **Versand**: Verbindungen erleichtern den Nachrichtenversand über ausgewählte Kanäle oder geben Daten an externe Systeme weiter.
6. **Messung und Optimierung**: Leistungsdaten und Kundeninteraktionen liefern Erkenntnisse, die in das System zurückgespeist werden, um Zielgruppen, Inhalte, Entscheidungen und Journeys zu verfeinern.
7. **Governance**: Administrations- und Datenschutzkontrollen stellen die Einhaltung der Vorschriften und eine ordnungsgemäße Systemkonfiguration sicher.

Dieser iterative Prozess ermöglicht es Unternehmen, ihre Strategien zur Kundeninteraktion kontinuierlich zu erlernen und zu verbessern.
