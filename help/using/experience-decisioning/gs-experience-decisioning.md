---
title: Erste Schritte mit Offer Decisioning
description: Weitere Informationen zu Offer Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: c13cd73229b2fab80722663afae9fe24b660c0f9
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 91%

---

# Erste Schritte mit Offer Decisioning {#get-started-experience-decisioning}

>[!BEGINSHADEBOX &quot;Was Sie in diesem Handbuch finden werden&quot;]

* **[Erste Schritte mit Offer Decisioning](gs-experience-decisioning.md)**
* Verwalten Sie Ihre Entscheidungselemente: [Konfigurieren des Elementkatalogs](catalogs.md) - [Erstellen von Entscheidungselementen](items.md) - [Verwalten von Elementsammlungen](collections.md)
* Konfigurieren der Elementauswahl: [Entscheidungsregeln erstellen](rules.md) - [Erstellen von Ranking-Methoden](ranking.md)
* [Erstellen von Auswahlstrategien](selection-strategies.md)
* [Erstellen von Entscheidungsrichtlinien](create-decision.md)

>[!ENDSHADEBOX]

## Was ist Offer Decisioning? {#about}

>[!AVAILABILITY]
>
>Die Offer Decisioning-Funktion ist derzeit nur als Beta-Version für ausgewählte Benutzerinnen und Benutzer verfügbar. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.

Offer Decisioning vereinfacht die Personalisierung, indem es einen zentralisierten Katalog von Marketing-Angeboten, die als „Entscheidungselemente“ bezeichnet werden und eine ausgereifte Entscheidungs-Engine anbietet. Diese Engine nutzt Regeln und Ranking-Kriterien, um die relevantesten Entscheidungselemente für jeden Kontakt auszuwählen und darzustellen.

Diese Entscheidungselemente sind über den neuen Code-basierten Erlebniskanal, der jetzt in Journey Optimizer-Kampagnen verfügbar ist, nahtlos in eine breite Palette eingehender Oberflächen integriert.

**Einschränkungen:**

* Entscheidungsrichtlinien sind nur zur Verwendung in Code-basierten Erlebniskampagnen verfügbar.
* Derzeit ist die Frequenzlimitierung in Offer Decisioning nicht verfügbar.

## Wichtige Schritte bei Offer Decisioning {#steps}

Die wichtigsten Schritte für die Arbeit mit Offer Decisioning sind:

1. **Benutzerdefinierte Attribute konfigurieren**: Der Katalog der Entscheidungselemente kann an spezifische Anforderungen angepasst werden, indem benutzerdefinierte Attribute im Schema des Katalogs eingerichtet werden.

1. **Entscheidungselemente erstellen**, um die Zielgruppe anzuzeigen.

1. **Mit Sammlungen organisieren**: Verwenden Sie Sammlungen, um Entscheidungselemente basierend auf attributbasierten Regeln zu kategorisieren. Sammlungen können in Auswahlstrategien integriert werden, um zu bestimmen, welche Sammlung von Entscheidungselementen berücksichtigt werden soll.

1. **Entscheidungsregeln erstellen**: Entscheidungsregeln werden in Entscheidungselementen und/oder Auswahlstrategien verwendet, um zu bestimmen, wem ein Entscheidungselement angezeigt werden kann.

1. **Rangfolgemethoden implementieren**: Erstellen Sie Rangfolgemethoden und wenden Sie diese innerhalb von Entscheidungsstrategien an, um die Prioritätsreihenfolge für die Auswahl von Entscheidungselementen festzulegen.

1. **Auswahlstrategien erstellen**: Erstellen Sie Auswahlstrategien, die Sammlungen, Entscheidungsregeln und Rangfolgemethoden nutzen, um die Entscheidungselemente zu identifizieren, die für die Anzeige in Profilen geeignet sind.

1. **Eine Entscheidungsrichtlinie in die Code-basierte Kampagne einbetten**: Entscheidungsrichtlinien kombinieren mehrere Auswahlstrategien, um die für die gewünschte Zielgruppe anzuzeigenden geeigneten Entscheidungselemente zu bestimmen.
