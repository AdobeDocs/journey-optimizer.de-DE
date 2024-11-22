---
title: Erste Schritte mit der Entscheidungsfindung
description: Weitere Informationen zur Entscheidungsfindung
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 616e1dd9fbfd029f7209356d5c19cfff9d4b4f06
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 56%

---

# Erste Schritte mit der Entscheidungsfindung {#get-started-experience-decisioning}

## Was ist die Entscheidungsfindung? {#about}

Die Entscheidungsfindung vereinfacht die Personalisierung, indem sie einen zentralisierten Katalog von Marketing-Angeboten, die als „Entscheidungselemente“ bezeichnet werden, und eine ausgereifte Entscheidungs-Engine anbietet. Diese Engine nutzt Regeln und Rangfolgekriterien, um die relevantesten Entscheidungselemente für jeden Kontakt auszuwählen und darzustellen.

Diese Entscheidungselemente sind über den [neuen Code-basierten Erlebniskanal](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/code-based-experience/get-started-code-based), der jetzt in Journey Optimizer-Kampagnen verfügbar ist, nahtlos in eine breite Palette eingehender Oberflächen integriert. Entscheidungsrichtlinien für die Entscheidungsfindung sind nur zur Verwendung in Code-basierten Erlebniskampagnen verfügbar.

## Leitlinien und Einschränkungen {#guardrails}

Um eine optimale Nutzung von Decisioning sicherzustellen, sollten Sie die folgenden Limits und Einschränkungen beachten:

### Allgemeine Limits {#general}

* **Angebotselemente**: Jede Artikelsammlung kann bis zu 500 Angebotselemente enthalten.
* **Benutzerdefinierte Attribute**: Ein Entscheidungselement kann maximal 100 benutzerdefinierte Attribute enthalten.
* **Auswahlstrategien und Entscheidungselemente pro Richtlinie**: Eine Entscheidungsrichtlinie unterstützt bis zu 10 Auswahlstrategien und Entscheidungselemente zusammen.

### Eignungsregeln {#eligibility}

* **Verschachtelungsebenen**: Die Verschachtelungstiefe ist auf 30 Ebenen beschränkt. Dies wird durch Zählen der `)` schließenden Klammern in der PQL-Zeichenfolge gemessen.
* **Regelzeichenfolgengröße**: Eine Regelzeichenfolge kann für UTF-8-kodierte Zeichen bis zu 15 KB groß sein. Dies entspricht 15.000 ASCII-Zeichen (jeweils 1 Byte) oder 3.750-7.500 Nicht-ASCII-Zeichen (jeweils 2-4 Byte).

### Ranking-Formeln {#ranking}

* **Verschachtelungsebenen**: Die Verschachtelungstiefe ist auf 30 Ebenen beschränkt. Dies wird durch Zählen der `)` schließenden Klammern in der PQL-Zeichenfolge gemessen.
* **Formelzeichenfolgengröße**: Eine Regelzeichenfolge kann für UTF-8-kodierte Zeichen bis zu 8 KB groß sein. Dies entspricht 8.000 ASCII-Zeichen (jeweils 1 Byte) oder 2.000-4.000 Nicht-ASCII-Zeichen (jeweils 2-4 Byte).

## Wichtige Schritte bei der Entscheidungsfindung {#steps}

Die wichtigsten Schritte für die Arbeit mit der Entscheidungsfindung sind:

1. **Zuweisen entsprechender Berechtigungen**. Die Entscheidungsfindung steht nur Benutzenden mit Zugriff auf eine Entscheidungfindungs-bezogene **[!UICONTROL Rolle]** zur Verfügung, z. B. Entscheidungsträgern. Wenn Sie nicht auf die Entscheidungsfindung zugreifen können, müssen Ihre Berechtigungen erweitert werden.

   +++Erfahren Sie, wie Sie die Rolle „Entscheidungsträger“ zuweisen

   1. Um Benutzenden eine Rolle im Produkt [!DNL Permissions] zuzuweisen, navigieren Sie zur Registerkarte **[!UICONTROL Rollen]** und wählen Sie „Entscheidungsträger“ aus.

      ![](assets/decision_permission_1.png)

   1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

      ![](assets/decision_permission_2.png)

   1. Geben Sie den Namen oder die E-Mail-Adresse der jeweiligen Person ein oder wählen Sie sie aus der Liste aus und klicken Sie auf **[!UICONTROL Speichern]**.

      Wenn die Benutzerin bzw. der Benutzer vorher noch nicht erstellt wurde, lesen Sie die [Dokumentation zum Hinzufügen von Benutzenden](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   Ihre Benutzenden sollten dann eine E-Mail mit einer Umleitung zu Ihrer Instanz erhalten.

+++

1. **Benutzerdefinierte Attribute konfigurieren**: Der Katalog der Elemente kann an spezifische Anforderungen angepasst werden, indem benutzerdefinierte Attribute im Schema des Katalogs eingerichtet werden.

   ➡️ [Erfahren Sie, wie Sie den Elementkatalog konfigurieren](catalogs.md)

1. **Entscheidungselemente erstellen**, um die Zielgruppe anzuzeigen.

   ➡️ [Erfahren Sie, wie Sie Entscheidungselemente erstellen](items.md) ([API-Dokumentation](api-reference/decisions-items/create.md))

1. **Mit Sammlungen organisieren**: Verwenden Sie Sammlungen, um Entscheidungselemente basierend auf attributbasierten Regeln zu kategorisieren. Sammlungen können in Auswahlstrategien integriert werden, um zu bestimmen, welche Sammlung von Entscheidungselementen berücksichtigt werden soll.

   ➡️ [Erfahren Sie, wie Sie Elementkollektionen verwalten](collections.md) ([API-Dokumentation](api-reference/items-collections/create.md))

1. **Entscheidungsregeln erstellen**: Entscheidungsregeln werden in Entscheidungselementen und/oder Auswahlstrategien verwendet, um zu bestimmen, wem ein Entscheidungselement angezeigt werden kann.

   ➡️ [Erfahren Sie, wie Sie Entscheidungsregeln erstellen](rules.md)

1. **Rangfolgemethoden implementieren**: Erstellen Sie Rangfolgemethoden und wenden Sie diese innerhalb von Entscheidungsstrategien an, um die Prioritätsreihenfolge für die Auswahl von Entscheidungselementen festzulegen.

   ➡️ [Erfahren Sie, wie Sie Rangmethoden erstellen](ranking.md)

1. **Auswahlstrategien erstellen**: Erstellen Sie Auswahlstrategien, die Sammlungen, Entscheidungsregeln und Rangfolgemethoden nutzen, um die Entscheidungselemente zu identifizieren, die für die Anzeige in Profilen geeignet sind.

   ➡️ [Erfahren Sie, wie Sie Auswahlstrategien erstellen](selection-strategies.md) ([API-Dokumentation](api-reference/selection-strategies/create.md))

1. **Erstellen Sie eine Entscheidungsrichtlinie und betten Sie sie in Ihre code-basierte Kampagne ein**: Entscheidungsrichtlinien kombinieren mehrere Auswahlstrategien, um die für die gewünschte Zielgruppe anzuzeigenden Entscheidungselemente zu bestimmen.

   ➡️ [Erfahren Sie, wie Sie mit Entscheidungsrichtlinien arbeiten](create-decision.md)
