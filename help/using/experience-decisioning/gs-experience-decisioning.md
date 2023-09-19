---
title: Erste Schritte mit Experience Decisioning
description: Erfahren Sie mehr über Erlebnisentscheidungen
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 9b7280c33ce8238b54f7fd1865545f865ffb72ed
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 5%

---

# Erste Schritte mit Experience Decisioning {#get-started-experience-decisioning}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* **[Erste Schritte mit Experience Decisioning](gs-experience-decisioning.md)**
* Verwalten von Entscheidungselementen
   * [Konfigurieren des Elementkatalogs](catalogs.md)
   * [Erstellen von Entscheidungselementen](items.md)
   * [Verwalten von Elementsammlungen](collections.md)
* Elementauswahl konfigurieren
   * [Erstellen von Entscheidungsregeln](rules.md)
   * [Erstellen von Ranking-Methoden](ranking.md)
* [Erstellen von Auswahlstrategien](selection-strategies.md)
* [Entscheidungsrichtlinien erstellen](create-decision.md)

>[!ENDSHADEBOX]

## Was ist Erlebnisentscheidungen? {#about}

>[!AVAILABILITY]
>
>Die Entscheidungsfunktion für Erlebnisse ist derzeit als Beta-Version verfügbar, um nur Benutzer auszuwählen. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.

Experience Decisioning vereinfacht die Personalisierung, indem es einen zentralisierten Katalog von Marketing-Angeboten, die als &quot;Entscheidungselemente&quot;bezeichnet werden, und eine ausgereifte Entscheidungs-Engine anbietet. Diese Engine nutzt Regeln und Ranking-Kriterien, um die relevantesten Entscheidungselemente für jede Person auszuwählen und darzustellen.

Diese Entscheidungselemente sind über den neuen code-basierten Erlebniskanal, der jetzt in Journey Optimizer-Kampagnen verfügbar ist, nahtlos in eine breite Palette eingehender Oberflächen integriert.

**Einschränkungen:**

* Entscheidungsrichtlinien sind nur zur Verwendung in code-basierten Erlebniskampagnen verfügbar.
* Derzeit ist die Frequenzlimitierung in Experience Decisioning nicht verfügbar.

## Wichtige Schritte bei Experience Decisioning {#steps}

Die wichtigsten Schritte für die Arbeit mit Experience Decisioning sind:

1. **Benutzerdefinierte Attribute konfigurieren**: Passen Sie den Katalog der Entscheidungselemente an Ihre spezifischen Anforderungen an, indem Sie benutzerdefinierte Attribute im Schema des Katalogs einrichten.

1. **Erstellen von Entscheidungselementen** , um Ihrer Zielgruppe zu zeigen.

1. **Organisieren mit Sammlungen**: Verwenden Sie Sammlungen, um Entscheidungselemente basierend auf attributbasierten Regeln zu kategorisieren. Integrieren Sie Sammlungen in Ihre Auswahlstrategien, um zu bestimmen, welche Sammlung von Entscheidungselementen berücksichtigt werden soll.

1. **Entscheidungsregeln erstellen**: Entscheidungsregeln werden in Entscheidungselementen und/oder Auswahlstrategien verwendet, um zu bestimmen, wem ein Entscheidungselement angezeigt werden kann.

1. **Implementieren von Rangmethoden**: Erstellen Sie Rangmethoden und wenden Sie sie innerhalb von Entscheidungsstrategien an, um die Prioritätsreihenfolge für die Auswahl von Entscheidungselementen zu bestimmen.

1. **Erstellen von Auswahlstrategien**: Erstellen Sie Auswahlstrategien, die Sammlungen, Entscheidungsregeln und Rangmethoden nutzen, um die Entscheidungselemente zu identifizieren, die für die Anzeige in Profilen geeignet sind.

1. **Einbetten einer Entscheidungsrichtlinie in Ihre code-basierte Kampagne**: Entscheidungsrichtlinien kombinieren mehrere Auswahlstrategien, um die für die gewünschte Zielgruppe anzuzeigenden Entscheidungselemente zu bestimmen.

<!--## Glossary-->
