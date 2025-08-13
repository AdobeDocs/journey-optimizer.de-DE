---
solution: Journey Optimizer
product: journey optimizer
title: Funktionsbereiche
description: Funktionsbereiche in AJO
feature: Get Started
role: Admin, Data Engineer, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: c9b02ae2-e07b-41f4-90cc-b2c0966f1ed1
hide: true
source-git-commit: 72ff06a7d87d6d9e5bfc0c6462ea4d60a98fc940
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Grundlegende Konzepte

Adobe Journey Optimizer (AJO) umfasst mehrere wichtige Funktionsbereiche, die nahtlos zusammenarbeiten. In diesem Handbuch werden die einzelnen Bereiche erläutert und beschrieben, wie diese Bereiche kombiniert werden, um wirkungsvolle Kundenerlebnisse zu schaffen. Wenn Sie diese Funktionsbereiche verstehen, können Sie AJO nutzen, um personalisierte Omni-Channel-Erlebnisse effizient bereitzustellen.

## Übersicht der Funktionsbereiche

| Funktionsbereich | Primärer Vorteil | Analogie |
|-------------------------|--------------------------------------------------|------------------------|
| Daten-Management | Organisieren der richtigen Kundendaten | Das Fundament |
| Kunden-Management | Verstehen, wer Ihre Kunden sind | Kennen Sie Ihre Audience |
| Content-Management | Konsistente, personalisierte Nachrichten erstellen und verwalten | Erstellen einer Nachricht |
| Entscheidungs-Management | Die beste Nachricht/das beste Angebot in Echtzeit auswählen | Das Gehirn |
| Journey Management | Nahtlose Kundenerlebnisse entwerfen und automatisieren | Dirigent |
| Verbindungen | Verbinden von Datenquellen und Bereitstellen über Kundenkanäle | Die Pfeifen |
| Administration und Datenschutz | Kontrollieren der Einrichtung, des Zugriffs und der Sicherstellung der Datenkonformität | Das Regelwerk |

## Detaillierte Funktionsbereiche

### Daten-Management: The Foundation

**Zweck**: Aufnehmen, Strukturieren und Verwalten der Daten, die der Personalisierung zugrunde liegen. Dieser Prozess umfasst die Definition von Datenstrukturen (Schemata), die Erstellung von Speicher-Containern (Datensätzen) und den Import von Daten aus verschiedenen Systemen.

Behandeln Sie das Daten-Management als Grundlage für alle Kundeninteraktionen. Eine gut strukturierte Datengrundlage stellt sicher, dass jede Entscheidung, jede Nachricht und jedes Journey präzise und organisierte Informationen verwendet.

**Schlüsselkomponenten**:
- **Schemaerstellung und -verwaltung**: Definieren der Struktur von Kundendaten.
   - Beispiel: Erstellen Sie ein Schema mit Feldern wie „Vorname“, „E-Mail-Adresse“ und „Kaufverlauf“.
- **Datensatzkonfiguration**: Organisieren von Daten in logischen Containern.
   - Beispiel: Gruppieren von Transaktionsdaten in einem Datensatz „Verkaufstransaktionen“ für eine einfachere Analyse.
- **Datenaufnahme-Workflows**: Importieren Sie Daten effizient in die Plattform.
   - Beispiel: Verwenden Sie vorgefertigte Source-Connectoren, um Kundendaten aus einem CRM-System (Customer Relationship Management) zu importieren.
- **Datenqualitätstools**: Gewährleistung der Genauigkeit und Vollständigkeit der Daten.

**Vorteil**: Stellt sicher, dass Kundendaten zuverlässig, organisiert und zugänglich sind, was die Grundlage für alle AJO-Aktivitäten bildet. Vorkonfigurierte Source-Connectoren optimieren die Datenaufnahme von gängigen Plattformen aus.



### Kundenmanagement: Kennen Sie Ihre Zielgruppe

**Zweck**: Aufbau und Pflege eines tiefen Verständnisses jedes Kunden. Dazu gehört die Verwendung des Echtzeit-Kundenprofils von Adobe Experience Platform (AEP) , um Daten aus allen Touchpoints in einer einheitlichen Ansicht zusammenzuführen. Es verwaltet auch Identitäten über Geräte und Kanäle hinweg und ermöglicht so die Gruppierung von Einzelpersonen in Zielgruppen basierend auf gemeinsamen Attributen oder Verhaltensweisen.

Customer-Management-Tools verbinden unterschiedliche Datenpunkte, um ein einheitliches Bild jedes Kunden zu liefern. Dadurch wird sichergestellt, dass Sie relevante und personalisierte Erlebnisse bereitstellen können.

**Schlüsselkomponenten**:
- **Echtzeit-Kundenprofil**: Einheitliche Ansicht jedes Kunden.
   - Beispiel: Webbrowserverlauf, App-Interaktionen und Offline-Käufe in einem einzigen Profil kombinieren.
- **Identitätsauflösung**: Verknüpfen von Kundendaten über Geräte und Kanäle hinweg.
   - Beispiel: Abgleichen der E-Mail-Adresse eines Kunden mit seinen App-Nutzungsdaten mithilfe des Identitätsdiagramms.
- **Zielgruppenerstellung und -verwaltung**: Definieren von Gruppen basierend auf Attributen und Verhaltensweisen.
   - Beispiel: Erstellen Sie eine Zielgruppe für „Treue Kunden“, die im letzten Jahr mehr als fünf Käufe getätigt haben.
- **Segmentierung**: Regeln für die dynamische Zielgruppenzugehörigkeit anwenden.
   - Beispiel: Richten Sie ein Segment für „Erstklassige Käufer“ ein, das automatisch aktualisiert wird, wenn Kunden mehr als 500 USD ausgeben.

**Vorteil**: Ermöglicht präzise Zielgruppenbestimmung und Personalisierung durch ein dynamisches Verständnis individueller Vorlieben, Historie und Segmentzugehörigkeiten.



### Content-Management: Nachricht erstellen

**Zweck**: Erstellen, verwalten, personalisieren und wiederverwenden von Marketing-Inhalten über mehrere Kanäle hinweg. Dazu gehören die Verwaltung digitaler Assets, die Erstellung von Nachrichten mit visuellen Editoren oder Code, die Nutzung wiederverwendbarer Inhaltsvorlagen und Fragmente, die Erstellung von Landingpages und die Verwendung künstlicher Intelligenz (KI) zur Inhaltserstellung.

Content-Management-Tools stellen sicher, dass Teams effizient maßgeschneiderte Nachrichten erstellen und bereitstellen und dabei die Konsistenz und Relevanz an jedem Touchpoint gewährleisten.

**Schlüsselkomponenten**:
- **Inhaltseditoren**: Erstellen und formatieren Sie Nachrichten visuell oder mit Code.
   - Beispiel: Verwenden Sie den visuellen Editor, um eine E-Mail-Kampagne zu entwerfen, mit der Verkäufe an Feiertagen beworben werden.
- **Digital Asset Management**: Organisieren und Verwenden von Bildern und anderen Medien.
   - Beispiel: Speichern Sie Produktbilder in einer zentralen Bibliothek, um sie in Kampagnen einfach wiederzuverwenden.
- **Vorlagen und Fragmente**: Erstellen wiederverwendbarer Inhaltskomponenten.
   - Beispiel: Erstellen Sie eine Vorlage „Willkommensnachricht“, die Kundennamen dynamisch einfügt.
- **Personalization-Tools**: Dynamische Anpassung von Inhalten an individuelle Anforderungen.
   - Beispiel: Zeigen Sie personalisierte Produktempfehlungen basierend auf dem Navigationsverlauf an.
- **Landingpage-Builder**: Erstellen von Web-Zielen für Kampagnen.

**Vorteil**: Optimiert die Inhaltserstellung, stellt die Markenkonsistenz sicher und erleichtert die effiziente Bereitstellung hochgradig personalisierter Nachrichten.



### Entscheidungs-Management: Die Gehirne von Personalization

**Zweck**: Wählen Sie für jede Kundin und jeden Kunden zum richtigen Zeitpunkt die beste Nachricht oder das beste Angebot aus. Dies geschieht auf der Grundlage ihres Echtzeit-Profils, Kontexts und vordefinierter Geschäftsregeln oder KI-Modelle. Entscheidungs-Management umfasst die Verwaltung einer zentralen Bibliothek mit Angeboten, die Definition von Eignungsregeln, die Anwendung von Einschränkungen (wie Frequenzlimitierung) und die Einrichtung einer Ranking-Logik.

Entscheidungs-Management stellt sicher, dass die Personalisierung skaliert funktioniert, indem durch intelligente Automatisierung ein maximaler Wert bereitgestellt wird.

**Schlüsselkomponenten**:
- **Angebotsbibliothek**: Zentrales Repository für Marketing-Angebote.
   - Beispiel: Angebote wie „20% Rabatt auf Gutschein“ oder „Kostenloser Versand“ in einer gemeinsamen Bibliothek speichern.
- **Entscheidungsregeln**: Logik für die Auswahl optimaler Inhalte.
   - Beispiel: Zeigen Sie einen „Treuerabatt“ nur für Kunden im Segment „Treue Kunden“ an.
- **Einschränkungen und**: Kontrollieren Sie, wer was und wann erhält.
   - Beispiel: Wenden Sie eine Frequenzlimitierung an, um zu verhindern, dass ein Kunde dasselbe Angebot zweimal in einer Woche erhält.
- **Rangfolgestrategien**: Priorisieren von Angeboten basierend auf Geschäftszielen oder KI.
   - Beispiel: Angebote werden nach Rentabilität sortiert, wobei Produkte mit hoher Marge zuerst angezeigt werden.
- **Simulationstools**: Testen und Validieren von Entscheidungsstrategien.

**Vorteil**: Automatisiert und optimiert die Personalisierung, um sicherzustellen, dass relevante und wirkungsvolle Erlebnisse an jedem Touchpoint bereitgestellt werden.



### Journey-Management: Der Dirigent des Orchesters

**Zweck**: Entwerfen, orchestrieren und automatisieren Sie Kundenerlebnisse in mehreren Schritten und Kanälen. Journey reagieren auf Kundenverhalten und -ereignisse in Echtzeit und führen Personen durch personalisierte Pfade. AJO unterstützt auch Kampagnen zum Versand von geplanten, einmaligen Nachrichten an bestimmte Zielgruppen.

Journey-Management stellt sicher, dass Erlebnisse sich anpassungsfähig und nahtlos anfühlen und Einzelpersonen auf der Grundlage ihrer Vorlieben und Handlungen anleiten.

**Schlüsselkomponenten**:
- **Journey-Designer**: Visuelle Arbeitsfläche zum Erstellen von Kundenpfaden.
   - Beispiel: Entwerfen Sie eine Journey, die eine Begrüßungs-E-Mail sendet, wenn sich ein Kunde anmeldet.
- **Journey-Trigger**: Ereignisse, die Journey auslösen oder voranbringen.
   - Beispiel: Trigger einer Folgenachricht, nachdem ein Kunde seinen Warenkorb verlassen hat.
- **Bedingungsschritte**: Verwenden Sie eine logische Verzweigung.
   - Beispiel: Senden Sie eine andere Nachricht, je nachdem, ob eine Kundin oder ein Kunde eine E-Mail öffnet.
- **Warteaktivitäten**: Kontrollieren Sie den Fortschritt mit Zeitverzögerungen.
   - Beispiel: Drei Tage warten, bevor eine Erinnerungs-E-Mail gesendet wird.
- **Kampagnenverwaltung**: Tools für geplante, einmalige Nachrichten.

**Vorteil**: Erstellt nahtlose, vernetzte Erlebnisse, die sich an individuelle Interaktionen anpassen, Beziehungen pflegen und gewünschte Ergebnisse fördern.



### Anschlüsse: Die Rohre

**Zweck**: Verwalten des Datenflusses in AJO (Quellen) und der Nachrichten- oder Datenbereitstellung aus AJO (Kanäle und Ziele). Datenquellen bringen Daten in Adobe Experience Platform (AEP) ein. Kanäle liefern Nachrichten (per E-Mail, SMS, Push, Web usw.). Ziele ermöglichen den Fluss von Zielgruppen- oder Datensatzinformationen zu externen Plattformen.

Verbindungen stellen sicher, dass Daten effektiv in AJO eingehen und Kunden zuverlässig über die richtigen Touchpoints erreichen.

**Schlüsselkomponenten**:
- **Source-Connectoren**: Importieren Sie Daten in Platform.
   - Beispiel: Verwenden Sie einen Connector, um Kaufdaten von einer E-Commerce-Plattform zu übertragen.
- **Kanalkonfiguration**: Einrichten und Verwalten von Versandmechanismen.
   - Beispiel: SMS-Versand für Werbenachrichten konfigurieren.
- **Zieleinrichtung**: Verbindung zu externen Aktivierungssystemen herstellen.
   - Beispiel: Freigabe von Zielgruppendaten über eine Social-Media-Werbeplattform.
- **Datenflussverwaltung**: Verlagerung von Steuerinformationen.

**Vorteil**: Sorgt für eine effiziente Datenaufnahme und einen zuverlässigen Nachrichtenversand über alle Kanäle hinweg und ermöglicht gleichzeitig die Aktivierung in externen Systemen.



### Administration und Datenschutz: Das Regelwerk

**Zweck**: Systemeinstellungen konfigurieren, Benutzerzugriff und Berechtigungen verwalten, Kommunikationskanäle einrichten, Journey-Parameter definieren und die Einhaltung von Datenschutz- und Governance-Richtlinien sicherstellen. Dazu gehören die Verwaltung des Einverständnisses, die Anwendung von Datennutzungsregeln und die Verarbeitung von Datenzugriffs- oder Löschanfragen.

Administrations- und Datenschutz-Tools stellen sicher, dass die Datenintegrität geschützt ist und alle rechtlichen und organisatorischen Richtlinien eingehalten werden.

**Schlüsselkomponenten**:
- **Benutzer- und Zugriffsverwaltung**: Steuern von Zugriff und Berechtigungen.
   - Beispiel: Marketing- und IT-Teams bestimmte Berechtigungen zuweisen.
- **Sandbox-Konfiguration**: Separate Umgebungen für Entwicklung und Tests.
   - Beispiel: Verwenden Sie eine Sandbox, um neue Journey-Designs zu testen, bevor Sie sie live bereitstellen.
- **Kanaleinrichtung**: Konfigurieren technischer Einstellungen für den Versand.
   - Beispiel: Einrichten von E-Mail-Server-Details für Kampagnen-Messaging.
- **Datenschutztools**: Einverständnis und Datenschutzeinstellungen verwalten.
   - Beispiel: Anfragen zur Löschung von Daten gemäß DSGVO (Datenschutz-Grundverordnung) effizient bearbeiten.
- **Governance-**: Durchsetzen von Datennutzungsrichtlinien.

**Vorteil**: Stellt einen sicheren Plattformbetrieb, die Einhaltung von Vorschriften und die Abstimmung mit den Richtlinien der Organisation sicher.



## Verbinden der Punkte: So funktioniert alles zusammen

Diese Funktionsbereiche arbeiten in einem kontinuierlichen Zyklus, um personalisierte Kundenerlebnisse bereitzustellen und zu optimieren:

1. **Datenaufnahme**: Datenflüsse in AEP, strukturiert nach Daten-Management.
2. **Kundenverständnis**: Echtzeit-Kundenprofile vereinheitlichen diese Daten, während Customer Management die Einblicke durch Profile und Zielgruppen verfeinert.
3. **Content- und Angebotsstrategie**: Content-Management erstellt Nachrichten und Assets. Entscheidungs-Management definiert die Angebote und die Logik für die Auswahl der besten.
4. **Orchestrierung**: Das Journey-Management ordnet Interaktionen kanalübergreifend zu und nutzt dabei Kundenverständnis, Inhalte und Entscheidungen.
5. **Versand**: Verbindungen erleichtern den Nachrichtenversand über ausgewählte Kanäle oder geben Daten an externe Systeme weiter.
6. **Messung und Optimierung**: Leistungsdaten und Kundeninteraktionen geben Einblicke zurück in das System, um Zielgruppen, Inhalte, Entscheidungen und Journey zu verfeinern.
7. **Governance**: Verwaltungs- und Datenschutzkontrollen stellen die Einhaltung von Vorschriften und eine ordnungsgemäße Systemkonfiguration sicher.

Dieser iterative Prozess ermöglicht es Unternehmen, ihre Strategien zur Kundeninteraktion kontinuierlich zu erlernen und zu verbessern.
