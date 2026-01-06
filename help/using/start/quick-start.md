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
source-git-commit: d3765f66beff13aaf77cd585c5da5f93c44fa1df
workflow-type: ht
source-wordcount: '1724'
ht-degree: 100%

---


# Rollen und Verantwortlichkeiten

Adobe Journey Optimizer ermöglicht es Marken, während der gesamten Customer Journey vernetzte, kontextuelle und personalisierte Erlebnisse bereitzustellen. Journey Optimizer wurde mit einem End-to-End-Fokus auf Skalierbarkeit, Geschwindigkeit und Flexibilität entwickelt und kombiniert drei wichtige Treiber für den Mehrwert in einer einheitlichen Anwendung:

* **Echtzeit-Kundenerkenntnisse und -Interaktion** basierend auf dem Echtzeit-Kundenprofil von Adobe
* **Moderne Omni-Channel-Orchestrierung** durch einheitliche Arbeitsflächen für Echtzeit-Journeys und Batch-Kampagnen sowie einen modernen Nachrichten-Designer
* **Intelligente Entscheidungsfindung und Personalisierung** durch Entscheidungs-Management und KI/ML-Funktionen

Journey Optimizer bietet zwei Orchestrierungsansätze, um verschiedene Marketing-Anforderungen zu erfüllen:

* **Journeys**: Am besten geeignet für Eins-zu-eins-Interaktionen in Echtzeit, bei denen sich alle Kundinnen und Kunden in ihrem eigenen Tempo bewegen, ausgelöst durch Verhalten oder Ereignisse
* **Orchestrierte Kampagnen**: Am besten geeignet für Eins-zu-viele-Kampagnen in Batches, bei denen sich Zielgruppen mithilfe mehrstufiger Workflows nach einem Zeitplan gemeinsam bewegen; ideal für saisonale Werbeaktionen, Produkteinführungen und kontobasierte Kommunikation

Dieses einheitliche Erlebnis ermöglicht es Ihnen, ganze Anwendungsfälle an einem Ort zu implementieren, von der Definition von Zielgruppen und der Gestaltung von Journeys bis hin zur Erstellung personalisierter Inhalte und der Analyse von Ergebnissen. In dieser Dokumentation werden die zentralen Rollen und ihre effektive Verwendung von Journey Optimizer sowie ihre Verantwortlichkeiten und die ersten Schritte erklärt.

**Wichtiger Hinweis:** Adobe Journey Optimizer definiert verschiedene Rollen mit bestimmten Verantwortlichkeiten. Eine einzelne Person kann mehrere oder alle Rollen einnehmen, je nach Struktur Ihrer Organisation.

## Rollenbasierte Schnellstartanleitungen

Um die Implementierung zu vereinfachen, organisiert Adobe Journey Optimizer Aufgaben je nach Fachwissen in bestimmten Rollen. Jede Rolle konzentriert sich auf zentrale Aufgaben, die für ein nahtloses Kundenerlebnis erforderlich sind.

| Rolle | Primäre Verantwortlichkeiten | Wichtige Kenntnisse | Typische Aufgaben |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Administrator** | Einrichten der Umgebung und Zugriffsverwaltung | Systemkonfiguration, Benutzerverwaltung, Sicherheit | Einrichten von Sandboxes, Verwalten von Benutzerberechtigungen, Konfigurieren von Kanälen und Nachrichtenvoreinstellungen |
| **Dateningenieurin/-ingenieur** | Kundenprofildaten und Datenquellen | Datenmodellierung, XDM-Schemata, Quell-Connectoren | Modellieren von Profil- und Geschäftsdaten in Schemata, Konfigurieren von Quell-Connectoren, Überwachen der Datenaufnahme |
| **Entwicklerin/Entwickler** | Technische Implementierung und Integrationen | Mobile/Web-SDK, APIs, ereignisgesteuerte Architektur | Integrieren von SDKs, Implementieren von Ereignissen, Erstellen benutzerdefinierter Aktionsendpunkte |
| **Marketing-Fachkraft** | Journey-Design und personalisierte Erlebnisse | Journey-Orchestrierung, Inhaltserstellung, Zielgruppen-Targeting | Entwerfen von Customer Journeys, Erstellen und Personalisieren von Nachrichten, Verwalten von Angeboten und Entscheidungskomponenten, Definieren von Zielgruppen |

Jede Rolle ist für eine bestimmte Phase der Adobe Journey Optimizer-Implementierung zuständig und sorgt für einen strukturierten und effizienten Bereitstellungsprozess.

## Reihenfolge bei der Implementierung und Rollenabhängigkeiten

Eine erfolgreiche Journey Optimizer-Implementierung folgt normalerweise dieser Sequenz, die die Abhängigkeiten zwischen Rollen widerspiegelt:

1. **Administrator**: Richtet die Umgebung ein\
   Die bzw. der Admin richtet die Grundlage ein, indem sie bzw. er Sandboxes konfiguriert, Zugriffssteuerungen einrichtet und Kanalkonfigurationen vorbereitet. Dies muss zuerst geschehen, damit andere Teams arbeiten können.
   * Konfigurieren der Entwicklungs-, Staging- und Produktions-Sandbox
   * Einrichten von Rollen, Berechtigungen und Zugriffssteuerung auf Objektebene (OLAC)
   * Konfigurieren von Kanalkonfigurationen (E-Mail, SMS, Push, In-App, Web, Inhaltskarten)
   * Delegieren von Subdomains und Einrichten von IP-Pools
   * Konfigurieren von Unterdrückungslisten und Einverständnisrichtlinien

2. **Dateningenieurin/-ingenieur**: Erstellt die Datengrundlage\
   Dateningenieurinnen und Dateningenieure erstellen die Dateninfrastruktur, auf der die Personalisierung basiert, und definieren, wie Kundendaten in und durch das System fließen.
   * Erstellen von Identity-Namespaces zur Kundenidentifizierung 
   * Entwerfen von XDM-Schemata (Profil, Erlebnisereignisse, relational)
   * Einrichten von Datensätzen und Aktivieren dieser für das Echtzeit-Kundenprofil
   * Konfigurieren der Datenaufnahme (Batch und Streaming)
   * Erstellen berechneter Attribute für komplexe Berechnungen
   * Konfigurieren von Ereignissen und Datenquellen für Journeys

3. **Entwickelnde**: Implementieren technische Integrationen\
   Entwicklerinnen und Entwickler verbinden Anwendungen mit Journey Optimizer, indem sie SDKs integrieren, Ereignisse senden und API-Endpunkte erstellen. Diese Implementierungen ermöglichen das Auslösen und Ausführen von Journeys.
   * Integrieren von Mobile SDK (iOS/Android) mit der Einrichtung von Push-Benachrichtigungen
   * Implementieren von Web SDK für Web-Erlebnisse
   * Senden von Ereignissen aus Anwendungen zum Auslösen von Journeys
   * Erstellen benutzerdefinierter Aktionsendpunkte für Integrationen externer Systeme
   * Testen von Implementierungen mit Adobe Experience Platform Assurance

4. **Marketing-Fachleute**: Entwerfen Kundenerlebnisse und führen sie aus\
   Marketing-Fachleute nutzen alle Grundlagen, um kanalübergreifend Journeys zu erstellen, Inhalte zu entwerfen und Kundenerlebnisse zu optimieren.
   * Erstellen von Zielgruppen mithilfe von Segmentierung, CSV-Upload oder Zielgruppenkomposition
   * Gestalten personalisierter Inhalte mit dem KI-Assistenten und Vorlagen
   * Erstellen von Multi-Channel-Journeys mit Ereignis- und Zielgruppen-Triggern
   * Testen mit Genehmigungs-Workflows vor dem Launch
   * Überwachen der Leistung und Optimieren basierend auf Reporting-Erkenntnissen

**Hinweis:** Parallel zu dieser typischen Sequenz können andere Aktivitäten ausgeführt werden. Entwickelnde können beispielsweise an App-Integrationen arbeiten, während Dateningenieure Schemata konfigurieren.

## Erste Schritte je nach Rolle

Jede Rolle beginnt mit bestimmten Aufgaben entsprechend ihres Schwerpunkts. Durch das Durchführen dieser ersten Schritte wird ein reibungsloseres Onboarding und eine Abstimmung mit dem gesamten Implementierungsprozess sichergestellt:

### Für Marketing-Fachleute {#for-marketers}

Als Marketing-Fachkraft oder Business-Anwenderin bzw. -Anwender entwerfen Sie Customer Journeys, um persönliche, kontextuelle Erlebnisse über alle Kontaktpunkte hinweg bereitzustellen. Sie arbeiten in einer einheitlichen Oberfläche, um komplette Anwendungsfälle von Anfang bis Ende zu implementieren.

**Wichtige Funktionen, die Sie dabei verwenden:**

* **Journey-Orchestrierung**: Erstellen Sie Eins-zu-eins-Kundeninteraktionen in Echtzeit, bei denen sich jede Person in ihrem eigenen Tempo bewegt, ausgelöst durch Verhalten oder Ereignisse über alle Kanäle hinweg.
* **Kampagnenorchestrierung**: Entwerfen und automatisieren Sie komplexe, mehrstufige Batch-Kampagnen im benötigten Umfang mithilfe einer visuellen Arbeitsfläche. Perfekt für markenkonforme Kampagnen wie saisonale Werbeaktionen, Produkteinführungen und kontobasierte Kommunikation. Nutzen Sie Segmentierung in mehrere Entitäten, um präzise Zielgruppen durch die Verknüpfung von Kundendaten mit zugehörigen Entitäten (Konten, Käufe, Buchungen) zu erstellen.
* **Moderner Nachrichten-Designer**: Gestalten und personalisieren Sie E-Mail- und Mobile-Nachrichten mit einer Drag-and-Drop-Oberfläche. Bearbeiten Sie vorkonfigurierte Vorlagen zur Beschleunigung der Markteinführungszeit.
* **Entscheidungs-Management**: Erstellen und verwalten Sie in einer zentralen Bibliothek Angebote, Eignungsregeln und andere Komponenten, die in E-Mails und Kundenkontaktpunkte eingebettet werden können.
* **Asset-Management**: Greifen Sie auf Adobe Experience Manager Assets Essentials zu, das vollständig in Journey Optimizer eingebettet ist, für optimierten Asset-Zugriff und optimierte Asset-Bereitstellung.
* **Zielgruppendefinition**: Erstellen Sie On-Demand-Zielgruppen mit sofortiger Verfeinerung mithilfe relationaler Abfragen und Sichtbarkeit vor dem Versand für eine genaue Zielgruppengröße.
* **KI/ML-Dienste**: Nutzen Sie Versandzeitoptimierung und prädiktive Interaktionswerte, um lukrative Kundinnen und Kunden anzusprechen und das Abwanderungsrisiko zu minimieren.

**Erster Schritt::** Verwenden von Anwendungsfallvorlagen und Assistenten zur einfachen Erstellung und Bereitstellung neuer Customer Journeys.

[Erste Schritte als Marketing-Fachkraft →](path/marketer.md)

### Für Dateningenieurinnen und Dateningenieure {#for-data-engineers}

Als Datenarchitektin bzw. -architekt oder Dateningenieurin bzw. -ingenieur richten Sie die Kundenprofildaten und andere Datenquellen ein, auf denen die von Journey Optimizer orchestrierten Erlebnisse basieren, und pflegen diese.

**Wichtigste Verantwortlichkeiten:**

* **Kundenprofildaten**: Modellieren Sie Kundenprofildaten und Geschäftsdaten in Schemata, um eine einheitliche 360-Grad-Sicht auf die Kundin bzw. den Kunden zu erstellen.
* **Relationale Datenmodellierung**: Entwerfen Sie für orchestrierte Kampagnen relationale Schemata, um die Segmentierung in mehrere Entitäten zu aktivieren und Kundendaten mit zugehörigen Entitäten wie Konten, Käufen, Abonnements und Buchungen zu verbinden und so eine flexible Zielgruppenerstellung zu ermöglichen.
* **Quell-Connectoren**: Konfigurieren Sie Quell-Connectoren, um Daten aus Web, CRM, Offline-Quellen und anderen Quellen in Adobe Experience Platform aufzunehmen.
* **Identitätsbestimmung**: Richten Sie Identity-Namespaces ein, um Profile kontinuierlich zu aktualisieren und Kundinnen und Kunden in Echtzeit in Segmente und Journeys bzw. aus ihnen heraus zu verschieben.
* **Datenquellen**: Konfigurieren Sie Datenquellen, um externe Signale während der gesamten Customer Journey in Echtzeit zu überwachen.
* **Profil-Management**: Aktivieren Sie Datensätze für das Echtzeit-Kundenprofil, um personalisierte Erlebnisse zu ermöglichen.
* **Datenqualität** Überwachen Sie die Datenaufnahme, um sicherzustellen, dass alle Daten reibungslos in Journey Optimizer gelangen.

**Erster Schritt:** Modellieren des ersten Kundenprofilschemas und Konfigurieren eines Quell-Connectors, um mit der Datenaufnahme zu beginnen.

[Erste Schritte als Dateningenieurin bzw. -ingenieur →](path/data-engineer.md)

### Für Admins {#for-administrators}

Als Admin richten Sie die Journey Optimizer-Umgebung ein, damit Ihre Teams effizient und sicher arbeiten können.

**Wichtigste Verantwortlichkeiten:**

* **Sandboxes**: Erstellen und verwalten Sie Sandboxes, um Daten und Journeys für verschiedene Benutzergruppen (Entwicklung, Tests, Produktion) zu unterteilen.
* **Benutzerverwaltung**: Richten Sie Benutzergruppen und Berechtigungen ein, um den Zugriff auf verschiedene Funktionen zu steuern.
* **Kanaleinrichtung**: Konfigurieren Sie Versandkanäle und Nachrichtenvoreinstellungen, um ein konsistentes Branding für alle über Journey Optimizer bereitgestellten Nachrichten und Assets sicherzustellen.
* **Sicherheit und Governance**: Wenden Sie die Zugriffssteuerung auf Objektebene (OLAC) an, konfigurieren Sie Einverständnisrichtlinien und implementieren Sie Data-Governance-Richtlinien.
* **Zustellbarkeit**: Delegieren Sie Subdomains, erstellen Sie IP-Pools und verwalten Sie Unterdrückungs- und Zulassungslisten.
* **Journey-Konfigurationen**: Richten Sie Journey-Elemente und -Konfigurationen für Ihre Teams ein.

**Erster Schritt:** Konfigurieren von Sandboxes und Benutzerberechtigungen und Einrichten der ersten Kanalkonfigurationen und Nachrichtenvoreinstellungen.

[Erste Schritte als Admin →](path/administrator.md)

### Für Entwicklende {#for-developers}

Implementieren Sie technische Integrationen, die Journey Optimizer mit Ihren Anwendungen verbinden.

**Wichtigste Verantwortlichkeiten:**

* Integrieren von Adobe Experience Platform Mobile SDK (iOS/Android)
* Implementieren von Web SDK für Web-Erlebnisse und Web-Push-Benachrichtigungen
* Konfigurieren von Anmeldedaten und Zertifikaten für Push-Benachrichtigungen
* Senden von Ereignissen aus Anwendungen zum Auslösen von Journeys
* Erstellen von API-Endpunkten, die von Journey Optimizer über benutzerdefinierte Aktionen aufgerufen werden
* Implementieren von Code-basierten Erlebnissen für Web-, Mobile- und andere Oberflächen
* Testen und Debuggen von Implementierungen mit Adobe Experience Platform Assurance
* Arbeiten mit Journey Optimizer-APIs für programmgesteuerten Zugriff

**Erster Schritt:** Integrieren von Mobile oder Web SDK und Implementieren des ersten Ereignisses, um eine Journey auszulösen.

[Erste Schritte als Entwicklerin bzw. Entwickler →](path/developer.md)

## Rollenübergreifende Zusammenarbeit

Erfolgreiche Journey Optimizer-Implementierungen erfordern die Zusammenarbeit aller Rollen. Jede Rolle arbeitet mit anderen zusammen, um nahtlose Kundenerlebnisse bereitzustellen:

>[!BEGINTABS]

>[!TAB Admins]

**Admins** unterstützen alle Teams durch Verwalten von Zugriff und Konfigurationen. Sie arbeiten mit:

* **Dateningenieurinnen und -ingenieuren**: Erteilen von Berechtigungen für Daten-Management, Genehmigen von Sandbox-Zugriff, Koordinieren von Governance-Richtlinien
* **Entwicklenden**: Bereitstellen von API-Anmeldedaten, Einrichten von Testumgebungen, Genehmigen von Kanalkonfigurationen
* **Marketing-Fachleuten**: Zuweisen von Berechtigungen für Journeys/Kampagnen, Konfigurieren von Kanälen, Unterstützen von Testumgebungen

>[!TAB Dateningenieurinnen und -ingenieure]

**Dateningenieurinnen und -ingenieure** stellen die Datengrundlage für bereit. Sie arbeiten mit:

* **Admins**: Anfordern von Berechtigungen für Daten-Management, Koordinieren von Governance- und Aufbewahrungsrichtlinien
* **Entwickelnden**: Bereitstellen von XDM-Schemata und Ereignisstrukturen, Definieren von Payload-Formaten für Ereignisse, Testen der Datenaufnahme
* **Marketing-Fachleuten**: Erstellen berechneter Attribute für die Personalisierung, Erstellen von Zielgruppen, Konfigurieren relationaler Schemata

>[!TAB Entwickelnde]

**Entwickelnde** implementieren technische Integrationen, auf denen Journeys basieren. Sie arbeiten mit:

* **Dateningenieurinnen und -ingenieuren**: Abrufen von XDM-Schemata und Ereignisstrukturen, Erfüllen der Anforderungen an die Datenerfassung, Testen der Ereignisbereitstellung
* **Admins**: Bereitstellen von API-Spezifikationen, Anfordern von Berechtigungen und Anmeldedaten, Koordinieren der Teststrategie
* **Marketing-Fachleuten**: Verstehen von Ereignis-Triggern, Implementieren von Tracking, Unterstützen von Journey-Tests, Beheben von Problemen

>[!TAB Marketing-Fachleute]

**Marketing-Fachleute** gestalten Kundenerlebnisse und geben Feedback. Sie arbeiten mit:

* **Dateningenieurinnen und -ingenieuren**: Anfordern von berechneten Attributen, Koordinieren der Zielgruppenanforderungen, Bereitstellen von Feedback zur Datenqualität
* **Entwickelnden**: Abstimmen von Ereignis-Triggern, Testen von Implementierungen, Validieren von Tracking
* **Admins**: Anfordern von Kanalkonfigurationen, Bestätigen von Funktionszugriff, Koordinieren der Aktivierung

>[!ENDTABS]

**Best Practice:** Halten Sie regelmäßige funktionsübergreifende Meetings, um Prioritäten abzustimmen, Fortschritte auszutauschen und sich Team-übergreifend mit Hindernissen zu befassen.

## Anleitungsvideo {#video}

Weitere Informationen zu den wichtigsten Funktionen und Personas von Journey Optimizer finden Sie im Einführungsvideo. Das Video führt Sie durch die Benutzeroberfläche und hebt je nach rollenspezifischen Workflows zentrale Funktionen hervor.

>[!VIDEO](https://video.tv.adobe.com/v/3432377?captions=ger&quality=12)

## Weitere Ressourcen

Detailliertere Informationen und Aktualisierungen finden Sie in den folgenden Ressourcen:

>[!BEGINTABS]

>[!TAB Lernmaterialien und Dokumentation]

* [Anleitungsvideos](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=de){target="_blank"}: Detaillierte Video-Tutorials für alle Rollen
* [Journey-Anwendungsfallbibliothek](../building-journeys/jo-use-cases.md): Praxisbeispiele und Implementierungsmuster
* [KI und intelligente Funktionen](ai-features.md): Informationen über den KI-Assistenten, die Versandzeitoptimierung und die Inhaltsgenerierung
* [Handbuch zur Benutzeroberfläche](user-interface.md): Effektive Navigation in Journey Optimizer

>[!TAB Bleiben Sie auf dem Laufenden]

* [Versionshinweise](../rn/release-notes.md): Neueste Funktionen, Verbesserungen und Fehlerbehebungen
* [Aktualisierungen der Dokumentation](../rn/documentation-updates.md): Verfolgen von aktuellen Dokumentationsänderungen
* [Produktbenachrichtigungen](../rn/releases.md#staying-informed): Informationen darüber, wie E-Mail- und produktinterne Benachrichtigungen für Journey Optimizer-Aktualisierungen abonniert werden können

>[!TAB Community und Unterstützung]

* [Experience League-Community](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=de){target="_blank"}: Kontakt zu anderen Benutzenden und Fachleuten
* [Produktforum](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=de){target="_blank"}: Ort für Fragen und zum Teilen von Wissen

>[!ENDTABS]
