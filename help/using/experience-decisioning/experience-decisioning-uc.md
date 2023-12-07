---
title: Anwendungsfall für Offer Decisioning
description: Erfahren Sie, wie Sie Entscheidungen mithilfe von Experimenten mit dem Code-basierten Kanal erstellen.
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: c13cd73229b2fab80722663afae9fe24b660c0f9
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 92%

---

# Anwendungsfall für Offer Decisioning {#experience-decisioning-uc}

>[!BEGINSHADEBOX &quot;Was Sie in diesem Handbuch finden werden&quot;]

* [Erste Schritte mit Offer Decisioning](gs-experience-decisioning.md)
* Verwalten Sie Ihre Entscheidungselemente: [Konfigurieren des Elementkatalogs](catalogs.md) -[Erstellen von Entscheidungselementen](items.md) - [Verwalten von Elementsammlungen](collections.md)
* Konfigurieren der Elementauswahl: [Entscheidungsregeln erstellen](rules.md) - [Erstellen von Ranking-Methoden](ranking.md)
* [Erstellen von Auswahlstrategien](selection-strategies.md)
* [Erstellen von Entscheidungsrichtlinien](create-decision.md)

>[!ENDSHADEBOX]

In diesem Anwendungsfall definieren Sie zwei Versandabwandlungen, die jeweils eine andere Entscheidungsrichtlinie enthalten, um zu messen, welche die beste Leistung für Ihre Zielgruppe erzielt.

## Erstellen von Elementen und Strategien

Zunächst müssen Sie Elemente erstellen, sie in Sammlungen gruppieren, Regeln einrichten und Rangfolgenmethoden festlegen. Mit diesen Elementen können Sie Auswahlstrategien erstellen.

1. Navigieren Sie zu **[!UICONTROL Offer Decisioning]** > **[!UICONTROL Elemente]** und erstellen Sie mehrere Angebotselemente. Legen Sie Einschränkungen mithilfe von Zielgruppen oder Regeln fest, um jedes Element auf bestimmte Profile zu beschränken. [Weitere Informationen](items.md)

   <!--
   1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)-->

1. Erstellen Sie **Sammlungen**, um Ihre Entscheidungselemente nach Ihren Vorstellungen zu kategorisieren und zu gruppieren. [Weitere Informationen](collections.md)

1. Erstellen Sie **Entscheidungsregeln**, um zu bestimmen, wem ein Entscheidungselement angezeigt werden kann. [Weitere Informationen](rules.md)

1. Erstellen Sie **Rangfolgenmethoden** und wenden Sie sie innerhalb von Entscheidungsstrategien an, um die Prioritätsreihenfolge für die Auswahl von Entscheidungselementen festzulegen. [Weitere Informationen](ranking.md)

1. Erstellen Sie **Auswahlstrategien**, die Sammlungen, Entscheidungsregeln und Rangfolgenmethoden nutzen, um die Entscheidungselemente zu identifizieren, die für die Anzeige in Profilen geeignet sind. [Weitere Informationen](selection-strategies.md)

## Erstellen von Entscheidungsrichtlinien

Um den Besucherinnen und Besuchern auf Ihrer Website oder in Ihrer Mobile App das beste dynamische Angebot und Erlebnis zu präsentieren, fügen Sie einer Code-basierten Kampagne eine Entscheidungsrichtlinie hinzu.

Definieren Sie zwei Versandabwandlungen, die jeweils eine andere Entscheidungsrichtlinie enthalten.

1. Erstellen Sie eine Kampagne und wählen Sie die Aktion **[!UICONTROL Code-basiertes Erlebnis (Beta)]** aus. [Weitere Informationen](../code-based/create-code-based.md)

   >[!NOTE]
   >
   >Die Funktion „Code-basiertes Erlebnis“ ist derzeit nur als Beta-Version für ausgewählte Benutzerinnen und Benutzer verfügbar. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.

1. Wenn Ihr Versand personalisiert wurde, klicken Sie auf der Übersichtsseite der Kampagne auf **[!UICONTROL Experiment erstellen]**, um mit der Konfiguration Ihres Inhaltsexperiments zu beginnen. [Weitere Informationen](../campaigns/content-experiment.md)

1. Wählen Sie das Symbol **[!UICONTROL Entscheidungen]** aus, klicken Sie auf **[!UICONTROL Entscheidung erstellen]** und geben Sie die Entscheidungsdetails ein. [Weitere Informationen](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Definieren Sie die Auswahlstrategien für Ihre Entscheidung. Klicken Sie auf **[!UICONTROL Strategie hinzufügen]**.

1. Klicken Sie auf **[!UICONTROL Erstellen]**. Die neue Entscheidung wird unter **[!UICONTROL Entscheidungen]** hinzugefügt.

   ![](assets/decision-code-based-decision-added.png)

1. Klicken Sie auf das Symbol für weitere Aktionen (drei Punkte) und wählen Sie **[!UICONTROL Hinzufügen]** aus. Jetzt können Sie alle Entscheidungsattribute hinzufügen, die Sie darin haben möchten.

   ![](assets/decision-code-based-add-decision.png)

1. Sie können auch jedes beliebige Attribut hinzufügen, das im Ausdruckseditor verfügbar ist, z. B. Profilattribute.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Erstellen Sie Abwandlung B und wiederholen Sie die oben beschriebenen Schritte, um eine weitere Entscheidung zu erstellen.

1. Speichern Sie Ihren Inhalt.


