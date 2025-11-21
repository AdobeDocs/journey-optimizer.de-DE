---
solution: Journey Optimizer
product: journey optimizer
title: AJO-Rollen und -Verantwortlichkeiten
description: Erfahren Sie mehr über die verschiedenen Rollen in Adobe Journey Optimizer und die jeweiligen Verantwortlichkeiten
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 100%

---


# AJO-Rollen und -Verantwortlichkeiten

Adobe Journey Optimizer (AJO) ermöglicht es Marken, während des gesamten Kundenlebenszyklus vernetzte und kontextualisierte Kunden-Journeys bereitzustellen. Teams wird ermöglicht, Interaktionen im benötigten Umfang zu personalisieren und die Erwartungen der Kundschaft an Geschäftszielen auszurichten. In dieser Dokumentation werden die zentralen Rollen und ihre effektive Verwendung von Journey Optimizer sowie ihre Verantwortlichkeiten und die ersten Schritte erklärt.

**Wichtiger Hinweis:** Adobe Journey Optimizer definiert verschiedene Rollen mit bestimmten Verantwortlichkeiten. Eine einzelne Person kann mehrere oder alle Rollen einnehmen, je nach Struktur Ihrer Organisation.

## Rollenbasierte Schnellstartanleitungen

Um die Implementierung zu vereinfachen, organisiert AJO Aufgaben je nach Fachwissen in bestimmten Rollen. Jede Rolle konzentriert sich auf zentrale Aufgaben, die für ein nahtloses Kundenerlebnis erforderlich sind.

| Rolle | Primäre Verantwortlichkeiten | Wichtige Kenntnisse | Typische Aufgaben |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Administrator** | System-Setup und Berechtigungsverwaltung | Systemkonfiguration, Benutzerverwaltung, Sicherheit | Konfigurieren von Sandboxes, Verwalten von Benutzenden und Einrichten von Kanälen |
| **Dateningenieur** | Konfigurieren von Datenstruktur und -flüssen | Datenmodellierung, Schema-Design, API-Integration | Einrichten von Schemata, Verwalten von Datensätzen, Konfigurieren von Datenquellen |
| **Entwickler** | Technische Integrationen und Anpassungen | Mobile-Entwicklung, API-Implementierung, Codierung | Integrieren von Mobile Apps, Implementieren von APIs, Erstellen benutzerdefinierter Aktionen |
| **Marketing-Fachkraft** | Entwerfen und Ausführen von Kunden-Journeys | Marketing-Strategie, Inhaltserstellung, Journey-Design | Erstellen von Kampagnen, Entwerfen von Journeys, Analysieren von Berichten |

Jede Rolle ist für eine bestimmte Phase der AJO-Implementierung zuständig und sorgt für einen strukturierten und effizienten Bereitstellungsprozess.

## Reihenfolge bei der Implementierung und Rollenabhängigkeiten

Eine erfolgreiche Journey Optimizer-Implementierung folgt normalerweise dieser Sequenz, die die Abhängigkeiten zwischen Rollen widerspiegelt:

1. **Administrator**: Richtet die Umgebung ein\
   Admins legen die technische Grundlage für das System und stellen sicher, dass alle Benutzenden ordnungsgemäß auf das System zugreifen und es konfigurieren können.
   * Konfigurieren von Sandboxes und Berechtigungen
   * Einrichten des Benutzerzugriffs
   * Konfigurieren von Nachrichtenkanälen und technischen Einstellungen

2. **Dateningenieur**: Erstellt die Datengrundlage\
   Dateningenieurinnen und Dateningenieure definieren Datenstruktur und -fluss, was für personalisierte Erlebnisse unerlässlich ist.
   * Entwerfen und Implementieren von Schemata
   * Einrichten von Identity-Namespaces
   * Grundlagen der Datenaufnahme
   * Erstellen von Testprofilen

3. **Entwickler**: Ist für technische Integrationen zuständig\
   Entwicklerinnen und Entwickler ermöglichen AJO die Interaktion mit Mobile Apps, Websites und externen Systemen, indem sie technische Integrationen implementieren. Beispielsweise beruhen Push-Benachrichtigungen auf Konfigurationen, die von Entwicklerinnen und Entwicklern vorgenommen wurden.
   * Integrieren von Mobile Apps für Push-Benachrichtigungen
   * Implementieren von Web SDKs
   * Entwickeln benutzerdefinierter Integrationen mithilfe von APIs
   * Erstellen benutzerdefinierter Aktionen für Drittanbietersysteme

4. **Marketing-Fachkraft**: Erstellt und startet Journey\
   Marketing-Fachleute nutzen die Vorarbeit anderer Rollen für die Gestaltung und Bereitstellung von Kundenerlebnissen. Sie konzentrieren sich auf Zielgruppensegmentierung, personalisierte Inhalte und Journey-Optimierung.
   * Festlegen von Zielgruppensegmenten
   * Erstellen von personalisierten Inhalten
   * Erstellen und Testen von Journeys
   * Analysieren und Optimieren der Leistung

**Hinweis:** Parallel zu dieser typischen Sequenz können andere Aktivitäten ausgeführt werden. Entwickelnde können beispielsweise an App-Integrationen arbeiten, während Dateningenieure Schemata konfigurieren.

## Erste Schritte je nach Rolle

Jede Rolle beginnt mit bestimmten Aufgaben entsprechend ihres Schwerpunkts. Durch das Durchführen dieser ersten Schritte wird ein reibungsloseres Onboarding und eine Abstimmung mit dem gesamten Implementierungsprozess sichergestellt:

1. **Für Marketing-Fachleute**: Konzentrieren Sie sich auf die Erstellung von Journeys, das Entwerfen von Nachrichten und die Ausführung von Kampagnen.\
   Beispiel: Als Erstes eine Begrüßungs-E-Mail-Kampagne für neue Kundschaft erstellen.

2. **Für Dateningenieure**: Richten Sie die Datengrundlage ein, konfigurieren Sie Schemata und integrieren Sie Datenquellen.\
   Beispiel: Einrichten eines Schemas zur Verfolgung des Kaufverlaufs von Kundinnen bzw. Kunden für personalisierte Empfehlungen.

3. **Für Admins**: Richten Sie Umgebungen ein, verwalten Sie Berechtigungen und konfigurieren Sie Nachrichtenkanäle.\
   Beispiel: Konfigurieren von Sandbox-Umgebungen zum Testen verschiedener Messaging-Strategien.

4. **Für Entwickelnde**: Integrieren Sie Mobile Apps, implementieren Sie APIs und erstellen Sie benutzerdefinierte Integrationen.\
   Beispiel: Verwenden des AJO-API, um Trigger-Push-Benachrichtigungen basierend auf Kundenaktionen in Ihrer Mobile App zu senden.

Klicken Sie unten auf Ihre Rolle, um auf spezifische Anleitungen zuzugreifen, die auf Ihre Verantwortlichkeiten zugeschnitten sind:

* [Erste Schritte als Marketing-Fachkraft](path/marketer.md)
* [Erste Schritte als Dateningenieur](path/data-engineer.md)
* [Erste Schritte als Admin](path/administrator.md)

## Anleitungsvideo {#video}

Weitere Informationen zu den wichtigsten Funktionen und Personas von Journey Optimizer finden Sie im Einführungsvideo. Das Video führt Sie durch die Benutzeroberfläche und hebt je nach rollenspezifischen Workflows zentrale Funktionen hervor.

>[!VIDEO](https://video.tv.adobe.com/v/3432377?captions=ger&quality=12)

## Weitere Ressourcen

Detailliertere Informationen und Aktualisierungen finden Sie in den folgenden Ressourcen:

* [Versionshinweise](../rn/release-notes.md)
* [Anleitungsvideos](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=de)