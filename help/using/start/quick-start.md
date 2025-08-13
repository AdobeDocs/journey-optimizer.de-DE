---
solution: Journey Optimizer
product: journey optimizer
title: AJO-Rollen und -Zuständigkeiten
description: Erfahren Sie mehr über die verschiedenen Rollen, die in Adobe Journey Optimizer involviert sind, und ihre Verantwortlichkeiten
feature: Get Started
role: Admin, Data Engineer, Developer, User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
source-git-commit: d2cdafef6f2d69ea85d9d042c859a8b1e7654d7d
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 1%

---


# AJO-Rollen und -Zuständigkeiten

Adobe Journey Optimizer (AJO) ermöglicht es Marken, während des gesamten Kundenlebenszyklus vernetzte und kontextualisierte Kunden-Journey bereitzustellen. Sie ermöglicht es Teams, Interaktionen in großem Umfang zu personalisieren und die Kundenerwartungen an den Geschäftszielen auszurichten. In dieser Dokumentation werden die Schlüsselrollen bei der effektiven Verwendung von Journey Optimizer, deren Verantwortlichkeiten und die ersten Schritte erläutert.

**Wichtiger Hinweis:** Adobe Journey Optimizer definiert verschiedene Rollen mit bestimmten Verantwortlichkeiten. Eine einzelne Person kann mehrere oder alle Rollen ausführen, je nach Struktur Ihrer Organisation.

## Rollenbasierte Schnellstartanleitungen

Um die Implementierung zu vereinfachen, organisiert AJO Aufgaben auf der Grundlage von Fachwissen in bestimmte Rollen. Jede Rolle konzentriert sich auf wichtige Aufgaben, die für ein nahtloses Kundenerlebnis erforderlich sind.

| Rolle | Primäre Zuständigkeiten | Schlüsselqualifikationen | Typische Aufgaben |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Administrator** | System-Setup und Berechtigungsverwaltung | Systemkonfiguration, Benutzerverwaltung, Sicherheit | Konfigurieren von Sandboxes, Verwalten von Benutzern und Einrichten von Kanälen |
| **Datentechniker** | Konfigurieren der Datenstruktur und -flüsse | Datenmodellierung, Schema-Design, API-Integration | Einrichten von Schemata, Verwalten von Datensätzen, Konfigurieren von Datenquellen |
| **Entwickler** | Technische Integrationen und Anpassungen | Mobile-Entwicklung, API-Implementierung, Codierung | Mobile Apps integrieren, APIs implementieren, benutzerdefinierte Aktionen erstellen |
| **Marketer** | Entwerfen und Ausführen von Kunden-Journey | Marketing-Strategie, Inhaltserstellung, Journey-Design | Kampagnen erstellen, Journey entwerfen, Berichte analysieren |

Jede Rolle behandelt eine bestimmte Phase der AJO-Implementierung und stellt einen strukturierten und effizienten Bereitstellungsprozess sicher.

## Reihenfolge der Implementierung und Rollenabhängigkeiten

Eine erfolgreiche Journey Optimizer-Implementierung folgt normalerweise dieser Sequenz, die die Abhängigkeiten zwischen Rollen widerspiegelt:

1. **Administrator**: Richtet die Umgebung ein\
   Der Administrator legt die technische Grundlage für das System und stellt sicher, dass alle Benutzer ordnungsgemäß auf das System zugreifen und es konfigurieren können.
   * Konfigurieren von Sandboxes und Berechtigungen
   * Einrichten des Benutzerzugriffs
   * Konfigurieren von Messaging-Kanälen und technischen Einstellungen

2. **Dateningenieur**: Erstellt die Datengrundlage\
   Dateningenieure definieren die Datenstruktur und den Datenfluss, die für personalisierte Erlebnisse unerlässlich sind.
   * Entwerfen und Implementieren von Schemata
   * Einrichten von Identity-Namespaces
   * Konfigurieren der Datenaufnahme
   * Erstellen von Testprofilen

3. **Entwickler**: Verarbeitet technische Integrationen\
   Entwickler ermöglichen AJO die Interaktion mit mobilen Apps, Websites und externen Systemen, indem sie technische Integrationen implementieren. Push-Benachrichtigungen hängen beispielsweise von Konfigurationen ab, die von Entwicklern geleitet werden.
   * Mobile Apps für Push-Benachrichtigungen integrieren
   * Implementieren von Web SDKs
   * Entwickeln benutzerdefinierter Integrationen mithilfe von APIs
   * Erstellen benutzerdefinierter Aktionen für Drittanbietersysteme

4. **Marketer**: Erstellt und startet Journey\
   Marketing-Experten nutzen die Vorarbeit, die andere Rollen für die Gestaltung und Bereitstellung von Kundenerlebnissen bieten. Sie konzentrieren sich auf Zielgruppensegmentierung, personalisierte Inhalte und Journey-Optimierung.
   * Entwerfen von Zielgruppensegmenten
   * Erstellen personalisierter Inhalte
   * Erstellen und Testen von Journey
   * Leistung analysieren und optimieren

**Hinweis:** Diese Sequenz ist zwar typisch, aber einige Aktivitäten können parallel ausgeführt werden. Entwickler können beispielsweise an App-Integrationen arbeiten, während Dateningenieure Schemata konfigurieren.

## Erste Schritte nach Rolle

Jede Rolle beginnt mit spezifischen Aufgaben, die auf ihren Schwerpunkt zugeschnitten sind. Durch das Durchführen dieser ersten Schritte wird ein reibungsloseres Onboarding und die Abstimmung mit dem gesamten Implementierungsprozess sichergestellt:

1. **Für Marketingexperten**: Konzentrieren Sie sich auf die Erstellung von Journey, das Entwerfen von Nachrichten und die Ausführung von Kampagnen.\
   Beispiel: Erstellen Sie zunächst eine Begrüßungs-E-Mail-Kampagne für neue Kunden.

2. **Für Dateningenieure**: Einrichten der Datengrundlage, Konfigurieren von Schemata und Integrieren von Datenquellen.\
   Beispiel: Einrichten eines Schemas zur Verfolgung des Kaufverlaufs von Kunden für personalisierte Empfehlungen.

3. **Für Administratoren**: Einrichten von Umgebungen, Verwalten von Berechtigungen und Konfigurieren von Messaging-Kanälen.\
   Beispiel: Konfigurieren von Sandbox-Umgebungen zum Testen verschiedener Messaging-Strategien.

4. **Für Entwickler**: Integrieren Sie Mobile Apps, implementieren Sie APIs und erstellen Sie benutzerdefinierte Integrationen.\
   Beispiel: Verwenden Sie die AJO-API, um Trigger-Push-Benachrichtigungen basierend auf Kundenaktionen in Ihrer Mobile App zu senden.

Klicken Sie unten auf Ihre Rolle, um auf spezifische Anleitungen zuzugreifen, die auf Ihre Zuständigkeiten zugeschnitten sind:

* [Erste Schritte als Marketing-Experte](path/marketer.md)
* [Erste Schritte als Datentechniker](path/data-engineer.md)
* [Erste Schritte als Administrator](path/administrator.md)

## Anleitungsvideo {#video}

Weitere Informationen zu den wichtigsten Funktionen und Rollen von Journey Optimizer finden Sie im Einführungsvideo. Das Video führt Sie durch die Benutzeroberfläche und hebt wichtige Funktionen hervor, die auf rollenspezifischen Workflows basieren.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## Weitere Ressourcen

Weitere Informationen und Aktualisierungen finden Sie in den folgenden Ressourcen:
* [Versionshinweise](https://experienceleague.adobe.com/docs/journey-optimizer/using/rn/release-notes.html)
* [Anleitungsvideos](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=de)