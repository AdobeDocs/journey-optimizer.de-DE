---
title: Anwendungsfall für Erlebnisentscheidungen
description: Erfahren Sie, wie Sie Entscheidungen mithilfe von Experimenten mit dem code-basierten Kanal erstellen.
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 4aea5c1434caa07aad26445c49a3d5c6274502ec
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 10%

---

# Anwendungsfall für Erlebnisentscheidungen {#experience-decisioning-uc}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* [Erste Schritte mit Experience Decisioning](gs-experience-decisioning.md)
* Verwalten von Entscheidungselementen
   * [Konfigurieren des Elementkatalogs](catalogs.md)
   * [Erstellen von Entscheidungselementen](items.md)
   * [Verwalten von Elementsammlungen](collections.md)
* Elementauswahl konfigurieren
   * [Erstellen von Entscheidungsregeln](rules.md)
   * [Erstellen von Ranking-Methoden](ranking.md)
* [Erstellen von Auswahlstrategien](selection-strategies.md)
* [Entscheidungsrichtlinien erstellen](create-decision.md)
* **[Anwendungsbeispiele](experience-decisioning-uc.md)**

>[!ENDSHADEBOX]

In diesem Anwendungsfall definieren Sie zwei Versandbehandlungen, die jeweils eine andere Entscheidungsrichtlinie enthalten, um zu messen, welche die beste Leistung für Ihre Zielgruppe erzielt.

## Elemente und Strategien erstellen

Zunächst müssen Sie Elemente erstellen, sie in Sammlungen gruppieren, Regeln einrichten und Rangmethoden festlegen. Mit diesen Elementen können Sie Auswahlstrategien erstellen.

1. Navigieren Sie zu **[!UICONTROL Erlebnisentscheidungen]** > **[!UICONTROL Elemente]** und erstellen Sie mehrere Angebotselemente. Legen Sie Begrenzungen mithilfe von Zielgruppen oder Regeln fest, um jedes Element auf bestimmte Profile zu beschränken. [Weitere Informationen](items.md)

   <!--
   1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)-->

1. Erstellen **Sammlungen** um Ihre Entscheidungselemente zu kategorisieren und nach Ihren Voreinstellungen zu gruppieren. [Weitere Informationen](collections.md)

1. Erstellen **Entscheidungsregeln** , um zu bestimmen, wem ein Entscheidungselement angezeigt werden kann. [Weitere Informationen](rules.md)

1. Erstellen **Ranking methods** und wenden sie innerhalb von Entscheidungsstrategien an, um die Prioritätsreihenfolge für die Auswahl von Entscheidungselementen festzulegen. [Weitere Informationen](ranking.md)

1. Build **Auswahlstrategien** die Sammlungen, Entscheidungsregeln und Rangmethoden nutzen, um die Entscheidungselemente zu identifizieren, die für die Anzeige in Profilen geeignet sind. [Weitere Informationen](selection-strategies.md)

## Entscheidungsrichtlinien erstellen

Um Ihren Besuchern auf Ihrer Website oder in Ihrer mobilen App das beste dynamische Angebot und Erlebnis zu präsentieren, fügen Sie einer code-basierten Kampagne eine Entscheidungsrichtlinie hinzu.

Definieren Sie zwei Versandbehandlungen, die jeweils eine andere Entscheidungsrichtlinie enthalten.

1. Erstellen Sie eine Kampagne und wählen Sie die **[!UICONTROL Codebasiertes Erlebnis (Beta)]** Aktion. [Weitere Informationen](../code-based/create-code-based.md)

   >[!NOTE]
   >
   >Die code-basierte Erlebnisfunktion ist derzeit als Beta-Version verfügbar, um nur Benutzer auszuwählen. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.

1. Klicken Sie auf der Kampagnenübersichtsseite auf **[!UICONTROL Experiment erstellen]** , um mit der Konfiguration Ihres Inhaltsexperiments zu beginnen. [Weitere Informationen](../campaigns/content-experiment.md)

1. Wählen Sie die **[!UICONTROL Entscheidungen]** klicken Sie auf **[!UICONTROL Entscheidung erstellen]** und geben Sie die Entscheidungsdetails ein. [Weitere Informationen](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Definieren Sie die Auswahlstrategien für Ihre Entscheidung. Klicks **[!UICONTROL Strategie hinzufügen]**.

1. Klicken Sie auf **[!UICONTROL Erstellen]**. Der neue Beschluss wird unter **[!UICONTROL Entscheidungen]**.

   ![](assets/decision-code-based-decision-added.png)

1. Klicken Sie auf das Symbol für weitere Aktionen (drei Punkte) und wählen Sie **[!UICONTROL Hinzufügen]**. Jetzt können Sie alle Entscheidungsattribute hinzufügen, die Sie in diesem hinzufügen möchten.

   ![](assets/decision-code-based-add-decision.png)

1. Sie können auch jedes andere Attribut hinzufügen, das im Ausdruckseditor verfügbar ist, z. B. Profilattribute.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Erstellen Sie Behandlung B und wiederholen Sie die oben beschriebenen Schritte, um eine weitere Entscheidung zu erstellen.

1. Speichern Sie Ihren Inhalt.


