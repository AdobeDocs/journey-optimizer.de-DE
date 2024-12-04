---
title: Anwendungsfall für die Entscheidungsfindung
description: Erfahren Sie, wie Sie Entscheidungen mithilfe von Experimenten mit dem Code-basierten Kanal erstellen.
feature: Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
exl-id: 09770df2-c514-4217-a71b-e31c248df543
source-git-commit: 196caffc918ef4f8fd97c2eb2c790ae4583aa311
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 87%

---

# Anwendungsfall für die Entscheidungsfindung {#experience-decisioning-uc}

Sie sind sich nicht sicher, ob eine bestimmte Rangformel bessere Leistungen erbringt als die vorab zugewiesenen Angebotsprioritäten.

In diesem Anwendungsfall erstellen Sie eine Kampagne, in der Sie zwei Versandabwandlungen definieren, die jeweils eine andere Entscheidungsrichtlinie enthalten, um zu messen, welche die beste Leistung für Ihre Zielgruppe erzielt.

Richten Sie das Experiment so ein, dass

* Die erste Behandlung enthält eine Auswahlstrategie mit Priorität als Ranking-Methode.
* Die zweite Behandlung enthält eine andere Auswahlstrategie, für die eine Formel die Rangmethode ist.


## Erstellen von Entscheidungselementen und Auswahlstrategien

Zunächst müssen Sie Elemente erstellen, sie in Sammlungen gruppieren, Regeln einrichten und Rangfolgenmethoden festlegen. Mit diesen Elementen können Sie Auswahlstrategien erstellen.

1. Navigieren Sie zu **[!UICONTROL Entscheidungsfindung]** > **[!UICONTROL Kataloge]** und erstellen Sie mehrere Entscheidungselemente. Legen Sie Einschränkungen mithilfe von Zielgruppen oder Regeln fest, um jedes Element auf bestimmte Profile zu beschränken. [Weitere Informationen](items.md)

   <!--
   1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)-->

1. Erstellen Sie **Sammlungen**, um Ihre Entscheidungselemente nach Ihren Vorstellungen zu kategorisieren und zu gruppieren. [Weitere Informationen](collections.md)

1. Erstellen Sie **Entscheidungsregeln**, um zu bestimmen, wem ein Entscheidungselement angezeigt werden kann. [Weitere Informationen](rules.md)

1. Erstellen Sie **Rangfolgenmethoden** und wenden Sie sie innerhalb von Entscheidungsstrategien an, um die Prioritätsreihenfolge für die Auswahl von Entscheidungselementen festzulegen. [Weitere Informationen](ranking.md)

1. Erstellen Sie **Auswahlstrategien**, die Sammlungen, Entscheidungsregeln und Rangfolgenmethoden nutzen, um die Entscheidungselemente zu identifizieren, die für die Anzeige in Profilen geeignet sind. [Weitere Informationen](selection-strategies.md)

## Erstellen von Entscheidungsrichtlinien

Um den Besucherinnen und Besuchern auf Ihrer Website oder in Ihrer Mobile App das beste dynamische Angebot und Erlebnis zu präsentieren, fügen Sie einer Code-basierten Kampagne eine Entscheidungsrichtlinie hinzu.

<!--Define two delivery treatments each containing a different decision policy.-->

1. Erstellen Sie eine Kampagne und wählen Sie die Aktion **[!UICONTROL Code-basiertes Erlebnis]** aus. [Weitere Informationen](../code-based/create-code-based.md)

1. Beginnen Sie im Fenster **[!UICONTROL Inhalt bearbeiten]** mit der Personalisierung der Abwandlung A.

1. Wählen Sie das Symbol **[!UICONTROL Entscheidungen]** aus, klicken Sie auf **[!UICONTROL Entscheidung erstellen]** und geben Sie die Entscheidungsdetails ein. [Weitere Informationen](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Definieren Sie die Auswahlstrategien für Ihre Entscheidung. Klicken Sie auf **[!UICONTROL Strategie hinzufügen]**.

1. Klicken Sie auf **[!UICONTROL Erstellen]**. Die neue Entscheidung wird unter **[!UICONTROL Entscheidungen]** hinzugefügt.

   ![](assets/decision-code-based-decision-added.png)

1. Klicken Sie auf das Symbol für weitere Aktionen (drei Punkte) und wählen Sie **[!UICONTROL Hinzufügen]** aus. Jetzt können Sie alle Entscheidungsattribute hinzufügen, die Sie darin haben möchten.

   ![](assets/decision-code-based-add-decision.png)

1. Sie können auch jedes beliebige Attribut hinzufügen, das im Personalisierungseditor verfügbar ist, z. B. Profilattribute.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Wenn Ihr Versand personalisiert wurde, klicken Sie auf der Übersichtsseite der Kampagne auf **[!UICONTROL Experiment erstellen]**, um mit der Konfiguration Ihres Inhaltsexperiments zu beginnen. [Weitere Informationen](../content-management/content-experiment.md)

1. Wählen Sie im Fenster **[!UICONTROL Inhalt bearbeiten]** Ihre Abwandlung B aus, um den Inhalt zu ändern, und wiederholen Sie die obigen Schritte, um eine weitere Entscheidung zu erstellen.

1. Speichern Sie Ihren Inhalt.
