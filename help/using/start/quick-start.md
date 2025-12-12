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
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 20%

---


# Rollen und Verantwortlichkeiten

Adobe Journey Optimizer ermöglicht es Marken, während des gesamten Kundenlebenszyklus vernetzte und kontextualisierte Kunden-Journey bereitzustellen. Teams wird ermöglicht, Interaktionen im benötigten Umfang zu personalisieren und die Erwartungen der Kundschaft an Geschäftszielen auszurichten. In dieser Dokumentation werden die zentralen Rollen und ihre effektive Verwendung von Journey Optimizer sowie ihre Verantwortlichkeiten und die ersten Schritte erklärt.

**Wichtiger Hinweis:** Adobe Journey Optimizer definiert verschiedene Rollen mit bestimmten Verantwortlichkeiten. Eine einzelne Person kann mehrere oder alle Rollen einnehmen, je nach Struktur Ihrer Organisation.

## Rollenbasierte Schnellstartanleitungen

Um die Implementierung zu vereinfachen, organisiert Adobe Journey Optimizer Aufgaben auf der Grundlage von Fachwissen in bestimmte Rollen. Jede Rolle konzentriert sich auf zentrale Aufgaben, die für ein nahtloses Kundenerlebnis erforderlich sind.

| Rolle | Primäre Verantwortlichkeiten | Wichtige Kenntnisse | Typische Aufgaben |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Administrator** | Einrichten der Umgebung und Zugriffsverwaltung | Systemkonfiguration, Benutzerverwaltung, Sicherheit | Konfigurieren von Sandboxes, Verwalten von Berechtigungen, Einrichten von Kanalkonfigurationen |
| **Dateningenieur** | Datengrundlage und Architektur | Datenmodellierung, XDM-Schemata, Datenqualität | Erstellen von Schemata und Datensätzen, Konfigurieren der Datenaufnahme und Verwalten des Datenlebenszyklus |
| **Entwickler** | Technische Implementierung und Integrationen | Mobile/Web-SDK, APIs, ereignisgesteuerte Architektur | SDKs integrieren, Ereignisse implementieren, benutzerdefinierte Aktionsendpunkte erstellen |
| **Marketing-Fachkraft** | Gestaltung und Ausführung von Kundenerlebnissen | Journey-Design, Inhaltserstellung, Datenanalyse | Erstellen Sie Journey, erstellen Sie personalisierte Inhalte, optimieren Sie Kampagnen |

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

Konzentrieren Sie sich auf die Erstellung personalisierter Kundenerlebnisse über alle Kanäle hinweg.

**Wichtige Funktionen, die Sie verwenden werden:**

* Erstellen von Audiences und Erstellen von Segmenten mit mehreren Methoden (Segmentdefinitionen, CSV-Upload, Audience-Komposition)
* Gestalten von Inhalten mit dem KI-Assistenten für die Text- und Bildgenerierung
* Erstellen von kanalübergreifenden Kunden-Journey mit Drag-and-Drop-Designer
* Nutzen der Sendezeitoptimierung und des Konflikt-Managements zur Maximierung der Interaktion
* Testen von Inhalten und Verwenden von Validierungs-Workflows vor der Veröffentlichung
* Überwachen der Leistung mit integrierten Reporting-Dashboards

**Erste Schritte mit:** Erstellen Sie eine einfache Begrüßungs-Journey oder eine Wiederherstellungskampagne für abgebrochene Warenkörbe mit vordefinierten Vorlagen.

[Erste Schritte als Marketing-Experte →](path/marketer.md)

### Für Dateningenieure {#for-data-engineers}

Erstellen Sie die Datengrundlage für personalisierte Erlebnisse.

**Wichtigste Zuständigkeiten:**

* Identity-Namespaces erstellen und Identitätsauflösung konfigurieren
* Entwerfen von XDM-Schemata für Profil- und Ereignisdaten (standardmäßig und relational)
* Datensätze einrichten und für das Echtzeit-Kundenprofil aktivieren
* Konfigurieren von Quell-Connectoren für die Batch- und Streaming-Datenaufnahme
* Erstellen berechneter Attribute zur Vereinfachung der Segmentierung
* Konfigurieren von Ereignissen und Datenquellen für die Journey-Ausführung
* Verwalten von Datenqualität, Governance und Lebenszyklus

**Erste Schritte mit:** Richten Sie Identity-Namespaces ein und erstellen Sie Ihr erstes Profilschema mit den erforderlichen Feldergruppen.

[Erste Schritte als Datentechniker →](path/data-engineer.md)

### Für Administratoren {#for-administrators}

Einrichten und Verwalten der Journey Optimizer-Umgebung für Ihr Unternehmen.

**Wichtigste Zuständigkeiten:**

* Erstellen und Verwalten von Sandboxes für Entwicklung, Tests und Produktion
* Konfigurieren Sie Rollen und Berechtigungen mit standardmäßigen oder benutzerdefinierten Rollen
* Anwenden der Zugriffssteuerung auf Objektebene (OLAC) auf sichere Ressourcen
* Einrichten von Kanalkonfigurationen für E-Mail, SMS, Push, In-App, Web und Inhaltskarten
* Delegieren von Subdomains und Erstellen von IP-Pools für die E-Mail-Zustellbarkeit
* Verwalten von Unterdrückungslisten und Zulassungslisten
* Konfigurieren von Einverständnisrichtlinien und Data Governance (mit Healthcare/Privacy Shield)

**Beginnen Sie mit:** Konfigurieren Sie Sandboxes, richten Sie grundlegende Rollen und Berechtigungen ein und arbeiten Sie dann mit Ihrem Team an Kanalkonfigurationen.

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

>[!VIDEO](https://video.tv.adobe.com/v/3432377?captions=ger&quality=12)

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
* **Produktbenachrichtigungen** - Aktivieren Sie Warnhinweise in Ihrem [Adobe Experience Cloud](https://experience.adobe.com/preferences){target="_blank"}Profil, um Benachrichtigungen über neue Versionen, Wartungsfenster und wichtige Ankündigungen zu erhalten. Klicken Sie zum Konfigurieren auf Ihr Profilsymbol > Voreinstellungen > Benachrichtigungen .

**Community und Support:**

* [Experience League-Community](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=de){target="_blank"} - Kontakt zu anderen Benutzern und Experten
* [Produktforum](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=de){target="_blank"} - Fragen stellen und Wissen teilen
