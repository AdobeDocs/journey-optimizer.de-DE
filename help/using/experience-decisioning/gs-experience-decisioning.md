---
title: Erste Schritte mit der Entscheidungsfindung
description: Weitere Informationen zur Entscheidungsfindung
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 5b377982f43902a4549f24c022fa8f4947d896a8
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 87%

---

# Erste Schritte mit der Entscheidungsfindung {#get-started-experience-decisioning}

>[!CONTEXTUALHELP]
>id="ajo_email_enable_experience_decisioning"
>title="Was ist Entscheidung?"
>abstract="Die Entscheidungsfindung ist ein neues Tool neben dem Entscheidungs-Management, mit dem Sie die besten Elemente aus der Entscheidungs-Engine auswählen und für jeden Einzelnen bereitstellen können. Für die Verwendung sind zusätzliche Einstellungen erforderlich."

## Was ist die Entscheidungsfindung? {#about}

Die Entscheidungsfindung vereinfacht die Personalisierung, indem sie einen zentralisierten Katalog von Marketing-Angeboten, die als „Entscheidungselemente“ bezeichnet werden, und eine ausgereifte Entscheidungs-Engine anbietet. Diese Engine nutzt Regeln und Rangfolgekriterien, um die relevantesten Entscheidungselemente für jeden Kontakt auszuwählen und darzustellen.

Diese Entscheidungselemente werden über den neuen [Code-basierten Erlebniskanal“ nahtlos in eine Vielzahl ](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/code-based-experience/get-started-code-based) eingehenden Oberflächen integriert, auf die jetzt über Journey Optimizer-Kampagnen zugegriffen werden kann.

>[!IMPORTANT]
>
>Entscheidungsrichtlinien für die Entscheidungsfindung sind nur zur Verwendung in Code-basierten Erlebniskampagnen verfügbar.

➡️ In diesem Abschnitt wird ein Anwendungsfall vollständig vorgestellt, der zeigt, wie Entscheidungen erstellt und in Inhaltsexperimenten mit dem Code-basierten Erlebniskanal verwendet [](experience-decisioning-uc.md).

## Leitlinien und Einschränkungen {#guardrails}

Um eine optimale Nutzung der Entscheidungsfindung sicherzustellen, sollten Sie die folgenden Leitlinien und Einschränkungen beachten:

### Allgemeine Leitlinien {#general}

* **Angebotselemente**: Jede Elementsammlung kann bis zu 500 Angebotselemente enthalten.
* **Benutzerdefinierte Attribute**: Ein Entscheidungselement kann maximal 100 benutzerdefinierte Attribute enthalten.
* **Auswahlstrategien und Entscheidungselemente pro Richtlinie**: Eine Entscheidungsrichtlinie unterstützt bis zu 10 Auswahlstrategien und Entscheidungselemente zusammen.

### Eignungsregeln {#eligibility}

* **Verschachtelungsebenen**: Die Verschachtelungstiefe ist auf 30 Ebenen beschränkt. Diese wird durch Zählen der schließenden Klammern `)` in der PQL-Zeichenfolge gemessen.
* **Regelzeichenfolgengröße**: Eine Regelzeichenfolge kann für UTF-8-kodierte Zeichen bis zu 15 KB groß sein. Das entspricht 15.000 ASCII-Zeichen (jeweils 1 Byte) oder 3.750 bis 7.500 Nicht-ASCII-Zeichen (jeweils 2 bis 4 Byte).

### Rangfolgeformeln {#ranking}

* **Verschachtelungsebenen**: Die Verschachtelungstiefe ist auf 30 Ebenen beschränkt. Diese wird durch Zählen der schließenden Klammern `)` in der PQL-Zeichenfolge gemessen.
* **Formelzeichenfolgengröße**: Eine Regelzeichenfolge kann für UTF-8-kodierte Zeichen bis zu 8 KB groß sein. Dies entspricht 8.000 ASCII-Zeichen (jeweils 1 Byte) oder 2.000 bis 4.000 Nicht-ASCII-Zeichen (jeweils 2 bis 4 Byte).

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

1. **Erstellen Sie Entscheidungselemente**, um die Zielgruppe anzuzeigen.

   ➡️ [Erfahren Sie, wie Sie Entscheidungselemente erstellen](items.md) ([API-Dokumentation](api-reference/decisions-items/create.md))

1. **Mit Sammlungen organisieren**: Verwenden Sie Sammlungen, um Entscheidungselemente basierend auf attributbasierten Regeln zu kategorisieren. Sammlungen können in Auswahlstrategien integriert werden, um zu bestimmen, welche Sammlung von Entscheidungselementen berücksichtigt werden soll.

   ➡️ [Erfahren Sie, wie Sie Elementsammlungen verwalten](collections.md) ([API-Dokumentation](api-reference/items-collections/create.md))

1. **Entscheidungsregeln erstellen**: Entscheidungsregeln werden in Entscheidungselementen und/oder Auswahlstrategien verwendet, um zu bestimmen, wem ein Entscheidungselement angezeigt werden kann.

   ➡️ [Erfahren Sie, wie Sie Entscheidungsregeln erstellen](rules.md)

1. **Rangfolgemethoden implementieren**: Erstellen Sie Rangfolgemethoden und wenden Sie diese innerhalb von Entscheidungsstrategien an, um die Prioritätsreihenfolge für die Auswahl von Entscheidungselementen festzulegen.

   ➡️ [Erfahren Sie, wie Sie Rangfolgemethoden erstellen](ranking.md)

1. **Auswahlstrategien erstellen**: Erstellen Sie Auswahlstrategien, die Sammlungen, Entscheidungsregeln und Rangfolgemethoden nutzen, um die Entscheidungselemente zu identifizieren, die für die Anzeige in Profilen geeignet sind.

   ➡️ [Erfahren Sie, wie Sie Auswahlstrategien erstellen](selection-strategies.md) ([API-Dokumentation](api-reference/selection-strategies/create.md))

1. **Eine Entscheidungsrichtlinie erstellen und in die Code-basierte Kampagne einbetten**: Entscheidungsrichtlinien kombinieren mehrere Auswahlstrategien, um die für die gewünschte Zielgruppe anzuzeigenden geeigneten Entscheidungselemente zu bestimmen.

   ➡️ [Erfahren Sie, wie Sie mit Entscheidungsrichtlinien arbeiten](create-decision.md)
