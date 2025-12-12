---
solution: Journey Optimizer
product: journey optimizer
title: Rollen und Verantwortlichkeiten
description: Erfahren Sie mehr über die verschiedenen Rollen in Adobe Journey Optimizer und die jeweiligen Verantwortlichkeiten
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
source-git-commit: ed3246d0bd552fee9c4df01babe18a5c1acd3b5f
workflow-type: tm+mt
source-wordcount: '1570'
ht-degree: 14%

---


# Rollen und Verantwortlichkeiten

Mit Adobe Journey Optimizer können Marken auf dem gesamten Kunden-Journey vernetzte, kontextbezogene und personalisierte Erlebnisse bereitstellen. Journey Optimizer wurde mit einem durchgängigen Fokus auf Skalierbarkeit, Geschwindigkeit und Flexibilität entwickelt und kombiniert drei wichtige Treiber für den Mehrwert in einer einheitlichen Anwendung:

* **Echtzeit-Kundeneinblicke und Interaktion** basierend auf dem Echtzeit-Kundenprofil von Adobe
* **Moderne Omni-Channel** Orchestrierung durch einheitliche Arbeitsflächen für Echtzeit-Journey- und Batch-Kampagnen sowie einen modernen Nachrichten-Designer
* **Intelligente Entscheidungsfindung und Personalisierung** durch Entscheidungs-Management und KI/ML-Funktionen

Journey Optimizer bietet zwei Orchestrierungsansätze, um verschiedene Marketing-Anforderungen zu erfüllen:

* **Journey**: Am besten geeignet für Eins-zu-eins-Interaktionen in Echtzeit, bei denen sich jeder Kunde in seinem eigenen Tempo bewegt, ausgelöst durch Verhalten oder Ereignisse
* **Orchestrierte Kampagnen**: Optimiert für Batch-Kampagnen, bei denen Zielgruppen mithilfe mehrstufiger Workflows nach einem Zeitplan zusammenarbeiten. Ideal für saisonale Werbeaktionen, Produkteinführungen und kontobasierte Kommunikation

Dieses einheitliche Erlebnis ermöglicht es Ihnen, ganze Anwendungsfälle an einem Ort zu implementieren, von der Definition von Zielgruppen und der Gestaltung von Journey bis hin zur Erstellung personalisierter Inhalte und der Analyse von Ergebnissen. In dieser Dokumentation werden die zentralen Rollen und ihre effektive Verwendung von Journey Optimizer sowie ihre Verantwortlichkeiten und die ersten Schritte erklärt.

**Wichtiger Hinweis:** Adobe Journey Optimizer definiert verschiedene Rollen mit bestimmten Verantwortlichkeiten. Eine einzelne Person kann mehrere oder alle Rollen einnehmen, je nach Struktur Ihrer Organisation.

## Rollenbasierte Schnellstartanleitungen

Um die Implementierung zu vereinfachen, organisiert Adobe Journey Optimizer Aufgaben auf der Grundlage von Fachwissen in bestimmte Rollen. Jede Rolle konzentriert sich auf zentrale Aufgaben, die für ein nahtloses Kundenerlebnis erforderlich sind.

| Rolle | Primäre Verantwortlichkeiten | Wichtige Kenntnisse | Typische Aufgaben |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Administrator** | Einrichten der Umgebung und Zugriffsverwaltung | Systemkonfiguration, Benutzerverwaltung, Sicherheit | Einrichten von Sandboxes, Verwalten von Benutzerberechtigungen, Konfigurieren von Kanälen und Nachrichtenvoreinstellungen |
| **Dateningenieur** | Kundenprofildaten und Datenquellen | Datenmodellierung, XDM-Schemata, Quell-Connectoren | Profil- und Geschäftsdaten in Schemata modellieren, Quell-Connectoren konfigurieren, Datenaufnahme überwachen |
| **Entwickler** | Technische Implementierung und Integrationen | Mobile/Web-SDK, APIs, ereignisgesteuerte Architektur | SDKs integrieren, Ereignisse implementieren, benutzerdefinierte Aktionsendpunkte erstellen |
| **Marketing-Fachkraft** | Journey-Design und personalisierte Erlebnisse | Journey-Orchestrierung, Inhaltserstellung, Audience-Targeting | Entwerfen Sie Kunden-Journey, erstellen und personalisieren Sie Nachrichten, verwalten Sie Angebote und Entscheidungskomponenten, definieren Sie Audiences |

Jede Rolle behandelt eine bestimmte Phase der Adobe Journey Optimizer-Implementierung und stellt einen strukturierten und effizienten Bereitstellungsprozess sicher.

## Reihenfolge bei der Implementierung und Rollenabhängigkeiten

Eine erfolgreiche Journey Optimizer-Implementierung folgt normalerweise dieser Sequenz, die die Abhängigkeiten zwischen Rollen widerspiegelt:

1. **Administrator**: Richtet die Umgebung ein\
   Der Administrator richtet die Grundlage ein, indem er Sandboxes konfiguriert, Zugriffssteuerungen einrichtet und Kanalkonfigurationen vorbereitet. Dies muss zuerst geschehen, damit andere Teams arbeiten können.
   * Konfigurieren von Entwicklungs-, Staging- und Produktions-Sandboxes
   * Einrichten von Rollen, Berechtigungen und Zugriffssteuerung auf Objektebene (OLAC)
   * Konfigurieren von Kanalkonfigurationen (E-Mail, SMS, Push, In-App, Web, Inhaltskarten)
   * Delegieren von Subdomains und Einrichten von IP-Pools
   * Konfigurieren von Unterdrückungslisten und Einverständnisrichtlinien

2. **Dateningenieur**: Erstellt die Datengrundlage\
   Dateningenieure erstellen die Dateninfrastruktur, die die Personalisierung unterstützt, und definieren, wie Kundendaten in das System fließen und durch es fließen.
   * Identity-Namespaces zur Kundenidentifizierung erstellen
   * Entwerfen von XDM-Schemata (Profil, Erlebnisereignisse, relationale Schemata)
   * Datensätze einrichten und für das Echtzeit-Kundenprofil aktivieren
   * Konfigurieren der Datenaufnahme (Batch und Streaming)
   * Berechnete Attribute für komplexe Berechnungen erstellen
   * Konfigurieren von Ereignissen und Datenquellen für Journey

3. **Entwickler**: Implementiert technische Integrationen\
   Entwicklerinnen und Entwickler verbinden Anwendungen mit Journey Optimizer, indem sie SDKs integrieren, Ereignisse senden und API-Endpunkte erstellen. Diese Implementierungen ermöglichen den Journey-Trigger und die Ausführung.
   * Integrieren von Mobile SDK (iOS/Android) mit der Einrichtung von Push-Benachrichtigungen
   * Implementieren von Web SDK für Web-Erlebnisse
   * Senden von Ereignissen aus Programmen an Trigger-Journey
   * Erstellen benutzerdefinierter Aktionsendpunkte für externe Systemintegrationen
   * Testen von Implementierungen mit Adobe Experience Platform Assurance

4. **Marketer**: Entwirft Kundenerlebnisse und führt sie aus\
   Marketing-Experten nutzen alle grundlegenden Funktionen, um kanalübergreifend Journey zu erstellen, Inhalte zu erstellen und Kundenerlebnisse zu optimieren.
   * Erstellen von Zielgruppen mithilfe von Segmentierung, CSV-Upload oder Zielgruppenkomposition
   * Gestalten personalisierter Inhalte mit KI-Assistenten und Vorlagen
   * Erstellen von Multi-Channel-Journey mit Ereignis- und Audience-Triggern
   * Mit Genehmigungs-Workflows vor dem Start testen
   * Überwachen der Leistung und Optimieren basierend auf Reporting-Insights

**Hinweis:** Parallel zu dieser typischen Sequenz können andere Aktivitäten ausgeführt werden. Entwickelnde können beispielsweise an App-Integrationen arbeiten, während Dateningenieure Schemata konfigurieren.

## Erste Schritte je nach Rolle

Jede Rolle beginnt mit bestimmten Aufgaben entsprechend ihres Schwerpunkts. Durch das Durchführen dieser ersten Schritte wird ein reibungsloseres Onboarding und eine Abstimmung mit dem gesamten Implementierungsprozess sichergestellt:

### Für Marketingexperten {#for-marketers}

Als Marketing-Experte oder Business Practitioner entwerfen Sie Kunden-Journeys, um persönliche, kontextuelle Erlebnisse über alle Touchpoints hinweg bereitzustellen. Sie arbeiten in einer einheitlichen Oberfläche, um ganze Anwendungsfälle von Anfang bis Ende zu implementieren.

**Wichtige Funktionen, die Sie verwenden werden:**

* **Journey Orchestration**: Erstellen Sie Eins-zu-eins-Kundeninteraktionen in Echtzeit, bei denen sich jede Person in ihrem eigenen Tempo bewegt, ausgelöst durch Verhalten oder Ereignisse kanalübergreifend
* **Kampagnenorchestrierung**: Entwerfen und automatisieren Sie komplexe, mehrstufige Batch-Kampagnen im großen Maßstab mithilfe einer visuellen Arbeitsfläche. Perfekt für markeninitiierte Kampagnen wie saisonale Werbeaktionen, Produkteinführungen und kontobasierte Kommunikation. Nutzen Sie die Segmentierung mehrerer Entitäten, um präzise Zielgruppen zu erstellen, indem Sie Kundendaten mit verwandten Entitäten (Konten, Käufe, Buchungen) verbinden
* **Moderner Nachrichten-Designer**: Gestalten und personalisieren Sie E-Mail- und Mobile-Nachrichten mit einer Drag-and-Drop-Oberfläche. Bearbeiten von vordefinierten Vorlagen zur Beschleunigung der Markteinführungszeit
* **Entscheidungs-**: Erstellen und verwalten Sie Angebote, Eignungsregeln und andere Komponenten in einer zentralen Bibliothek, die in E-Mails und Kunden-Touchpoints eingebettet werden kann
* **Asset-Management**: Zugriff auf Adobe Experience Manager Assets Essentials, das vollständig in Journey Optimizer eingebettet ist, für optimierten Asset-Zugriff und -Bereitstellung
* **Zielgruppendefinition**: Erstellen Sie On-Demand-Zielgruppen mit sofortiger Verfeinerung mithilfe relationaler Abfragen, mit Sichtbarkeit vor dem Versand für eine genaue Zielgruppenanzahl
* **KI/ML-Services**: Nutzen Sie die Sendezeitoptimierung und die prädiktiven Interaktionswerte, um hochwertige Kunden anzusprechen und das Abwanderungsrisiko zu minimieren

**Erste Schritte mit:** Anwendungsfallvorlagen und Assistenten zur einfachen Erstellung und Bereitstellung neuer Kunden-Journey.

[Erste Schritte als Marketing-Experte →](path/marketer.md)

### Für Dateningenieure {#for-data-engineers}

Als Datenarchitekt oder -ingenieur richten Sie die Kundenprofildaten und andere Datenquellen ein und pflegen sie, die die von Journey Optimizer orchestrierten Erlebnisse unterstützen.

**Wichtigste Zuständigkeiten:**

* **Kundenprofildaten**: Modellieren Sie Kundenprofildaten und Geschäftsdaten in Schemata, um eine einheitliche 360-Grad-Ansicht des Kunden zu erstellen
* **Relationale Datenmodellierung**: Entwerfen Sie für orchestrierte Kampagnen relationale Schemata, um die Segmentierung mehrerer Entitäten zu ermöglichen und Kundendaten mit verwandten Entitäten wie Konten, Käufen, Abonnements und Buchungen zu verbinden, um eine flexible Zielgruppenerstellung zu ermöglichen
* **Source-Connectoren**: Konfigurieren Sie Quell-Connectoren, um Daten aus dem Web, CRM, Offline-Daten und anderen Quellen in Adobe Experience Platform aufzunehmen
* **Identitätsauflösung**: Richten Sie Identity-Namespaces ein, um Profile kontinuierlich zu aktualisieren und Kunden in Echtzeit in Segmente und Journey bzw. aus ihnen heraus zu verschieben
* **Datenquellen**: Konfigurieren von Datenquellen, um in Echtzeit auf externe Signale auf der Kunden-Journey zu lauschen
* **Profil-Management**: Aktivieren von Datensätzen für das Echtzeit-Kundenprofil, um personalisierte Erlebnisse zu ermöglichen
* **Datenqualität** Überwachen der Datenaufnahme, um sicherzustellen, dass alles reibungslos in Journey Optimizer fließt

**Starten mit:** Modellieren Sie Ihr erstes Kundenprofilschema und konfigurieren Sie einen Quell-Connector, um mit der Datenaufnahme zu beginnen.

[Erste Schritte als Datentechniker →](path/data-engineer.md)

### Für Administratoren {#for-administrators}

Als Administrator richten Sie die Journey Optimizer-Umgebung ein, damit Ihre Teams effizient und sicher arbeiten können.

**Wichtigste Zuständigkeiten:**

* **Sandboxes**: Erstellen und verwalten Sie Sandboxes, um Daten und Journey für verschiedene Benutzergruppen (Entwicklung, Tests, Produktion) zu unterteilen
* **Benutzerverwaltung**: Einrichten von Benutzergruppen und Berechtigungen, um den Zugriff auf verschiedene Funktionen zu steuern
* **Kanaleinrichtung**: Konfigurieren von Versandkanälen und Nachrichtenvoreinstellungen, um ein konsistentes Branding für alle über Journey Optimizer bereitgestellten Nachrichten und Assets sicherzustellen
* **Sicherheit und Governance**: Wenden Sie die Zugriffssteuerung auf Objektebene (OLAC) an, konfigurieren Sie Einverständnisrichtlinien und implementieren Sie Data-Governance-Richtlinien
* **Zustellbarkeit**: Subdomains delegieren, IP-Pools erstellen und Unterdrückungslisten und Zulassungslisten verwalten
* **Journey-**: Richten Sie Journey-Elemente und -Konfigurationen für Ihre Teams ein

**Starten Sie mit** Konfigurieren Sie Sandboxes und Benutzerberechtigungen und richten Sie dann Ihre ersten Kanalkonfigurationen und Nachrichtenvoreinstellungen ein.

[Erste Schritte als Administrator-→](path/administrator.md)

### Für Entwickler {#for-developers}

Implementieren Sie technische Integrationen, die Journey Optimizer mit Ihren Programmen verbinden.

**Wichtigste Zuständigkeiten:**

* Integrieren von Adobe Experience Platform Mobile SDK (iOS/Android)
* Implementieren von Web SDK für Web-Erlebnisse und Web-Push-Benachrichtigungen
* Konfigurieren von Anmeldeinformationen und Zertifikaten für Push-Benachrichtigungen
* Senden von Ereignissen aus Programmen an Trigger-Journey
* Erstellen von API-Endpunkten, die von Journey Optimizer über benutzerdefinierte Aktionen aufgerufen werden
* Implementieren von Code-basierten Erlebnissen für Web-, Mobile- und andere Oberflächen
* Testen und Debuggen von Implementierungen mit Adobe Experience Platform Assurance
* Arbeiten mit Journey Optimizer-APIs für programmgesteuerten Zugriff

**Starten mit:** Integrieren Sie die Mobile- oder Web-SDK und implementieren Sie dann Ihr erstes Ereignis, um eine Journey zum Trigger zu bringen.

[Erste Schritte als Entwickler-→](path/developer.md)

## Cross-Role Collaboration

Erfolgreiche Journey Optimizer-Implementierungen erfordern die Zusammenarbeit aller Rollen:

* **Administratoren** Aktivieren Sie andere Rollen, indem Sie Sandboxes, Berechtigungen und Kanalkonfigurationen einrichten
* **Dateningenieure** stellen die Datengrundlage bereit, auf der Entwickler und Marketing-Experten aufbauen
* **Entwickler** Implementieren der technischen Integrationen, die Marketing-Experten zum Trigger von Journey verwenden
* **Marketer** Bieten Sie allen Teams Feedback zu Datenqualität, Funktionsanfragen und Anwendererlebnis

**Best Practice:** regelmäßige funktionsübergreifende Meetings, um Prioritäten auszurichten, Fortschritte auszutauschen und Blocker über Teams hinweg anzusprechen.

## Anleitungsvideo {#video}

Weitere Informationen zu den wichtigsten Funktionen und Personas von Journey Optimizer finden Sie im Einführungsvideo. Das Video führt Sie durch die Benutzeroberfläche und hebt je nach rollenspezifischen Workflows zentrale Funktionen hervor.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## Weitere Ressourcen

Detailliertere Informationen und Aktualisierungen finden Sie in den folgenden Ressourcen:

**Lernen und Dokumentation:**

* [Anleitungsvideos](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=de){target="_blank"} - Schrittweise Video-Tutorials für alle Rollen
* [Journey-Anwendungsfallbibliothek](../building-journeys/jo-use-cases.md) - Praxisbeispiele und Implementierungsmuster
* [KI und intelligente Funktionen](ai-features.md) - Erfahren Sie mehr über KI-Assistent, Sendezeitoptimierung und Inhaltserstellung
* [Handbuch zur Benutzeroberfläche](user-interface.md) - Effektive Navigation in Journey Optimizer

**Bleiben Sie auf dem Laufenden:**

* [Versionshinweise](../rn/release-notes.md) - Neueste Funktionen, Verbesserungen und Fehlerbehebungen
* [Dokumentationsaktualisierungen](../rn/documentation-updates.md) - Verfolgen Sie aktuelle Dokumentationsänderungen
* [Produktbenachrichtigungen](../rn/releases.md#staying-informed) - Erfahren Sie, wie Sie E-Mail- und produktinterne Benachrichtigungen für Journey Optimizer-Updates abonnieren.

**Community und Support:**

* [Experience League-Community](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=de){target="_blank"} - Kontakt zu anderen Benutzern und Experten
* [Produktforum](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=de){target="_blank"} - Fragen stellen und Wissen teilen
