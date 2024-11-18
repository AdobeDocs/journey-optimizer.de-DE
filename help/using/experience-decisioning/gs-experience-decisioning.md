---
title: Erste Schritte mit Decisioning
description: Weitere Informationen zu Entscheidungsfindungen
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 05ce9083d9f45332c718adc9d01ec3410ca84050
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 55%

---

# Erste Schritte mit Decisioning {#get-started-experience-decisioning}

## Was ist Entscheidungsfindung {#about}

Die Entscheidungsfindung vereinfacht die Personalisierung, indem sie einen zentralisierten Katalog von Marketing-Angeboten, die als „Entscheidungselemente“ bezeichnet werden, und eine ausgereifte Entscheidungs-Engine anbietet. Diese Engine nutzt Regeln und Ranking-Kriterien, um die relevantesten Entscheidungselemente für jeden Kontakt auszuwählen und darzustellen.

Diese Entscheidungselemente sind über den [neuen Code-basierten Erlebniskanal](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/code-based-experience/get-started-code-based), der jetzt in Journey Optimizer-Kampagnen verfügbar ist, nahtlos in eine breite Palette eingehender Oberflächen integriert. Entscheidungsrichtlinien sind nur zur Verwendung in code-basierten Erlebniskampagnen verfügbar.

## Leitlinien und Einschränkungen {#guardrails}

Um eine optimale Nutzung von Decisioning sicherzustellen, sollten Sie die folgenden Limits und Einschränkungen beachten:

### Allgemeine Limits {#general}

* **Angebotselemente**: Jede Artikelsammlung kann bis zu 500 Angebotselemente enthalten.
* **Benutzerdefinierte Attribute**: Ein Entscheidungselement kann maximal 100 benutzerdefinierte Attribute enthalten.
* **Auswahlstrategien und manuelle Elemente pro Richtlinie**: Eine Entscheidungsrichtlinie unterstützt bis zu 10 Auswahlstrategien und manuelle Elemente zusammen.

### Eignungsregeln {#eligibility}

* **Verschachtelungsebenen**: Die Verschachtelungstiefe ist auf 30 Ebenen beschränkt. Dies wird durch Zählen der `)` schließenden Klammern in der PQL-Zeichenfolge gemessen.
* **Regelzeichenfolgengröße**: Eine Regelzeichenfolge kann für UTF-8-kodierte Zeichen bis zu 15 KB groß sein. Dies entspricht 15.000 ASCII-Zeichen (jeweils 1 Byte) oder 3.750-7.500 Nicht-ASCII-Zeichen (jeweils 2-4 Byte).

### Ranking-Formeln {#ranking}

* **Verschachtelungsebenen**: Die Verschachtelungstiefe ist auf 30 Ebenen beschränkt. Dies wird durch Zählen der `)` schließenden Klammern in der PQL-Zeichenfolge gemessen.
* **Formelzeichenfolgengröße**: Eine Regelzeichenfolge kann für UTF-8-kodierte Zeichen bis zu 8 KB groß sein. Dies beträgt 8.000 ASCII-Zeichen (1 Byte pro Stück) oder 2.000-4.000 Nicht-ASCII-Zeichen (jeweils 2-4 Byte).

## Wichtige Schritte bei der Entscheidung {#steps}

Die wichtigsten Schritte für die Arbeit mit Decisioning sind:

1. **Zuweisen entsprechender Berechtigungen**. Die Entscheidungsfindung ist nur für Benutzer verfügbar, die Zugriff auf eine Decisioning-bezogene **[!UICONTROL Rolle]** haben, z. B. Entscheidungsmanager. Wenn Sie nicht auf Decisioning zugreifen können, müssen Ihre Berechtigungen erweitert werden.

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

1. **Entscheidungselemente erstellen**, um die Zielgruppe anzuzeigen.

1. **Mit Sammlungen organisieren**: Verwenden Sie Sammlungen, um Entscheidungselemente basierend auf attributbasierten Regeln zu kategorisieren. Sammlungen können in Auswahlstrategien integriert werden, um zu bestimmen, welche Sammlung von Entscheidungselementen berücksichtigt werden soll.

1. **Entscheidungsregeln erstellen**: Entscheidungsregeln werden in Entscheidungselementen und/oder Auswahlstrategien verwendet, um zu bestimmen, wem ein Entscheidungselement angezeigt werden kann.

1. **Rangfolgemethoden implementieren**: Erstellen Sie Rangfolgemethoden und wenden Sie diese innerhalb von Entscheidungsstrategien an, um die Prioritätsreihenfolge für die Auswahl von Entscheidungselementen festzulegen.

1. **Auswahlstrategien erstellen**: Erstellen Sie Auswahlstrategien, die Sammlungen, Entscheidungsregeln und Rangfolgemethoden nutzen, um die Entscheidungselemente zu identifizieren, die für die Anzeige in Profilen geeignet sind.

1. **Eine Entscheidungsrichtlinie in die Code-basierte Kampagne einbetten**: Entscheidungsrichtlinien kombinieren mehrere Auswahlstrategien, um die für die gewünschte Zielgruppe anzuzeigenden geeigneten Entscheidungselemente zu bestimmen.
