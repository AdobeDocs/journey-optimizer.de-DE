---
title: Erste Schritte mit der Entscheidungsfindung
description: Weitere Informationen zur Entscheidungsfindung
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/z-9FSXpQNMyy0KcGaLWgDYHqAx-BWhIEJYAq4wVqmv4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a653cc2e-bc85-4353-a306-399e5b247978id: fe338112-e2ce-4876-8989-fc4d497613f1id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 717
ht-degree: 80%

---

# Erste Schritte mit der Entscheidungsfindung {#get-started-experience-decisioning}

>[!CONTEXTUALHELP]
>id="ajo_email_enable_experience_decisioning"
>title="Was ist die Entscheidungsfindung?"
>abstract="Die Entscheidungsfindung ist ein neues Tool neben dem Entscheidungs-Management, mit dem Sie die besten Elemente aus der Entscheidungs-Engine auswählen und jedem Kontakt bereitstellen können. Für die Verwendung sind zusätzliche Einstellungen erforderlich."

## Was ist die Entscheidungsfindung? {#about}

Die Entscheidungsfindung vereinfacht die Personalisierung, indem sie einen zentralisierten Katalog von Marketing-Angeboten, die als „Entscheidungselemente“ bezeichnet werden, und eine ausgereifte Entscheidungs-Engine anbietet. Diese Engine nutzt Regeln und Rangfolgekriterien, um die relevantesten Entscheidungselemente für jeden Kontakt auszuwählen und darzustellen.

Diese Entscheidungselemente werden nahtlos in Nachrichten und Erlebnisse auf [!DNL Adobe Journey Optimizer] Kanälen integriert: [Code-basiertes Erlebnis](../code-based/get-started-code-based.md), E-Mail, SMS und Push-Benachrichtigungen.

>[!IMPORTANT]
>
>Entscheidungsrichtlinien stehen allen Kunden für die Kanäle **Code-basiertes Erlebnis**, **Push-Benachrichtigung** und **SMS** zur Verfügung. Die Entscheidungsfindung für den **E-Mail**-Kanal ist nur in begrenzter Verfügbarkeit verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](../rn/releases.md).

➡️ [Funktion im Video kennenlernen](#video)

➡️ In [diesem Abschnitt](experience-decisioning-uc.md) wird ein Anwendungsfall vollständig vorgestellt, der zeigt, wie Entscheidungen erstellt und in Inhaltsexperimenten mit dem Code-basierten Erlebniskanal verwendet werden können.

## Wichtige Schritte bei der Entscheidungsfindung {#steps}

Die wichtigsten Schritte für die Arbeit mit der Entscheidungsfindung sind:

1. **Zuweisen entsprechender Berechtigungen**. Die Entscheidungsfindung steht nur Benutzenden mit Zugriff auf eine Entscheidungfindungs-bezogene **[!UICONTROL Rolle]** zur Verfügung, z. B. Entscheidungsträgern. Wenn Sie nicht auf die Entscheidungsfindung zugreifen können, müssen Ihre Berechtigungen erweitert werden.

   +++Erfahren Sie, wie Sie die Rolle „Entscheidungstragende“ zuweisen

   1. Um Benutzenden eine Rolle im Produkt [!DNL Permissions] zuzuweisen, navigieren Sie zur Registerkarte **[!UICONTROL Rollen]** und wählen Sie „Entscheidungsträger“ aus.

      ![](assets/decision_permission_1.png)

   1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

      ![](assets/decision_permission_2.png)

   1. Geben Sie Name oder E-Mail-Adresse der jeweiligen Benutzenden ein oder wählen Sie die Person aus der Liste aus und klicken Sie auf **[!UICONTROL Speichern]**.

      Wenn die Benutzerin bzw. der Benutzer vorher noch nicht erstellt wurde, lesen Sie die [Dokumentation zum Hinzufügen von Benutzenden](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   Ihre Benutzenden sollten dann eine E-Mail mit einer Umleitung zu Ihrer Instanz erhalten.

   +++

1. **Benutzerdefinierte Attribute konfigurieren**: Der Katalog der Elemente kann an spezifische Anforderungen angepasst werden, indem benutzerdefinierte Attribute im Schema des Katalogs eingerichtet werden.

   ➡️ [Informationen zum Konfigurieren des Elementkatalogs](catalogs.md)

1. **Erstellen Sie Entscheidungselemente**, um die Zielgruppe anzuzeigen.

   ➡️ [Informationen zum Erstellen von Entscheidungselementen](items.md) in der Benutzeroberfläche (und in der [API-Dokumentation](api-reference/decisions-items/create.md))

1. **Mit Sammlungen organisieren**: Verwenden Sie Sammlungen, um Entscheidungselemente basierend auf attributbasierten Regeln zu kategorisieren. Sammlungen können in Auswahlstrategien integriert werden, um zu bestimmen, welche Sammlung von Entscheidungselementen berücksichtigt werden soll.

   ➡️ [Informationen zum Verwalten von Elementsammlungen](collections.md) in der Benutzeroberfläche (und in der [API-Dokumentation](api-reference/items-collections/create.md))

1. **Entscheidungsregeln erstellen**: Entscheidungsregeln werden in Entscheidungselementen und/oder Auswahlstrategien verwendet, um zu bestimmen, wem ein Entscheidungselement angezeigt werden kann.

   ➡️ [Informationen zum Erstellen von Entscheidungsregeln](rules.md)

1. **Rangfolgemethoden implementieren**: Erstellen Sie Rangfolgemethoden und wenden Sie diese innerhalb von Auswahlstrategien an, um die Prioritätsreihenfolge für die Auswahl von Entscheidungselementen festzulegen.

   ➡️ [Informationen zum Erstellen von Rangfolgemethoden](ranking/ranking.md)

1. **Auswahlstrategien erstellen**: Erstellen Sie Auswahlstrategien, die Sammlungen, Entscheidungsregeln und Rangfolgemethoden nutzen, um die Entscheidungselemente zu identifizieren, die für die Anzeige in Profilen geeignet sind.

   ➡️ [Informationen zum Erstellen von Auswahlstrategien in der Benutzeroberfläche](selection-strategies.md) in der Benutzeroberfläche (und in der [API-Dokumentation](api-reference/selection-strategies/create.md))

1. **Erstellen Sie eine Entscheidungsrichtlinie und betten Sie sie in Ihre Journey oder Kampagne ein** (Code-basiertes Erlebnis, E-Mail, SMS oder Push): Entscheidungsrichtlinien kombinieren mehrere Auswahlstrategien, um die geeigneten Entscheidungselemente zu bestimmen, die für die vorgesehene Audience angezeigt werden sollen.

   ➡️ [Erfahren Sie, wie Sie mit Entscheidungsrichtlinien arbeiten](create-decision.md)
➡️ Um das Angebot erfolgreich über den Code-basierten Erlebniskanal bereitzustellen, folgen Sie den Implementierungsschritten in [diesem Abschnitt](../code-based/code-based-implementation-samples.md).

## Zusätzliche Ressourcen

* **[Erstellen von Entscheidungselementen](items.md)**: Erfahren Sie, wie Sie Entscheidungselemente einschließlich Angebote, Inhaltsvarianten und Erlebnisse erstellen und verwalten.
* **[Konfigurieren von Entscheidungskatalogen](catalogs.md)**: Erfahren Sie, wie Sie Entscheidungselemente zur Verbesserung der Verwaltung in Katalogen organisieren.
* **[Definieren von Auswahlstrategien](selection-strategies.md)**: Erfahren Sie, wie Sie Auswahlstrategien mit Eignungsregeln und Rangfolgenmethoden erstellen.
* **[Erstellen von Entscheidungsrichtlinien](create-decision-policy.md)**: Erfahren Sie, wie Sie Entscheidungsrichtlinien erstellen, in denen Strategien und Einschränkungen kombiniert werden.
* **[Rangfolge und KI-Modelle](ranking/ranking.md)**: Setzen Sie übergeordnete Rangfolgenformeln und KI-Modelle für personalisierte Entscheidungsfindung ein.
* **[Migration vom Entscheidungs-Management](migrate-to-decisioning.md)** - Erfahren Sie mehr über die Vorteile der Migration zu Decisioning und verwenden Sie die APIs der Migrations-Tools.
* **[Entscheidungsleitlinien](decisioning-guardrails.md)**: Lernen Sie wichtige Einschränkungen und Best Practices bei der Implementierung von Entscheidungsfindung kennen.
* **[Tutorials zur Entscheidungsfindung](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/decision-capabilities/decisioning/introduction-to-decisioning){target="_blank"}**: Erkunden Sie Video-Tutorials mit detaillierten Anleitungen zu Entscheidungsfunktionen und Best Practices.

## Anleitungsvideo {#video}

Erfahren Sie mehr über die Entscheidungsfunktionen in Adobe Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3451101?quality=12)
