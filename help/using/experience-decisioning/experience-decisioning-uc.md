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
source-git-commit: 83ad828a4d342bba10284cdd20d22eb325e3e1f7
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 37%

---

# Anwendungsfall für die Entscheidungsfindung {#experience-decisioning-uc}

In diesem Anwendungsbeispiel werden alle Schritte vorgestellt, die zur Verwendung von Decisioning mit dem [!DNL Journey Optimizer] Code-basierten Kanal erforderlich sind.

<!--In this use case, you create a campaign where you define two delivery treatments - each containing a different decision policy in order to measure which one performs best for your target audience.-->

In diesem Anwendungsfall sind Sie sich nicht sicher, ob eine bestimmte Rangfolgenformel eine bessere Leistung als die vorab zugewiesenen Angebotsprioritäten erzielt.

Um zu messen, welche Zielgruppe die beste Leistung erzielt, erstellen Sie eine Kampagne, in der Sie zwei Versandmethoden definieren:

<!--Set up the experiment such that:-->

* Die erste Abwandlung enthält eine Auswahlstrategie mit Priorität als Rangfolgenmethode.
* Die zweite Abwandlung enthält eine andere Auswahlstrategie, die eine Formel als Rangfolgenmethode verwendet.

## Erstellen von Auswahlstrategien

Zunächst müssen Sie zwei Auswahlstrategien erstellen: eine mit Priorität als Ranking-Methode und eine mit einer Formel als Ranking-Methode.

### Erstellen der ersten Auswahlstrategie

Wählen Sie in der ersten Auswahlstrategie Priorität als Rangfolgenmethode aus. Führen Sie dazu folgende Schritte durch.

1. Erstellen Sie ein Entscheidungselement. [Weitere Informationen](items.md)

1. Legen Sie **[!UICONTROL Priorität]** des Entscheidungselements im Vergleich zu anderen fest. Wenn ein Profil für mehrere Elemente qualifiziert ist, gewährt eine höhere Priorität dem Element Vorrang vor anderen.

   ![](assets/exd-uc-item-priority.png)

   >[!NOTE]
   >
   >Die Priorität ist ein ganzzahliger Datentyp. Alle Attribute, bei denen es sich um ganzzahlige Datentypen handelt, sollten ganzzahlige Werte (ohne Dezimalstellen) enthalten.

1. Audiences oder Regeln definieren, um das Element auf bestimmte Profile zu beschränken. [Erfahren Sie, wie Sie die Eignung des Entscheidungselements festlegen](items.md#eligibility)

1. Legen Sie Begrenzungsregeln fest, um festzulegen, wie oft ein Angebot maximal unterbreitet werden kann. [Weitere Informationen](items.md#capping)

<!--1. If needed, repeat the steps above to create one or more additional decision items.-->

1. Erstellen Sie **Sammlung** in der Ihre Entscheidungselemente enthalten sein werden. [Weitere Informationen](collections.md)

1. Erstellen Sie **Auswahlstrategie**. [Weitere Informationen](selection-strategies.md#create-selection-strategy)

1. Wählen Sie [Sammlung](collections.md) aus, die die zu berücksichtigenden Angebote enthält.

1. [Wählen Sie die Rangfolgenmethode aus](#select-ranking-method) um das beste Angebot für jedes Profil auszuwählen. Wählen Sie in diesem Fall **[!UICONTROL Angebotspriorität]** aus. [Weitere Informationen](selection-strategies.md#offer-priority)

   ![](assets/exd-uc-strategy-priority.png)

   <!--If multiple offers are eligible for this strategy, the [Offer priority](#offer-priority) method uses the value defined in the offers.-->

### Erstellen der zweiten Auswahlstrategie

Wählen Sie in der zweiten Auswahlstrategie eine Formel als Rangfolgenmethode aus. Führen Sie dazu folgende Schritte durch.

1. Erstellen Sie ein Entscheidungselement. [Weitere Informationen](items.md)

<!--1. Set the same **[!UICONTROL Priority]** as for the first decision item. TBC?-->

1. Audiences oder Regeln definieren, um das Element auf bestimmte Profile zu beschränken. [Erfahren Sie, wie Sie die Eignung des Entscheidungselements festlegen](items.md#eligibility)

1. Legen Sie Begrenzungsregeln fest, um festzulegen, wie oft ein Angebot maximal unterbreitet werden kann. [Weitere Informationen](items.md#capping)

<!--1. If needed, repeat the steps above to create one or more additional decision items.-->

1. Erstellen Sie **Sammlung** in der Ihre Entscheidungselemente enthalten sein werden. [Weitere Informationen](collections.md)

1. Erstellen Sie **Auswahlstrategie**. [Weitere Informationen](selection-strategies.md#create-selection-strategy)

1. Wählen Sie [Sammlung](collections.md) aus, die die zu berücksichtigenden Angebote enthält.

1. [Wählen Sie die Rangfolgenmethode aus](#select-ranking-method) mit der Sie das beste Angebot für jedes Profil auswählen möchten. Wählen Sie in diesem Fall **[!UICONTROL Formel]**, um ein bestimmtes berechnetes Ergebnis zu verwenden und auszuwählen, welches geeignete Angebot geliefert werden soll. [Weitere Informationen](selection-strategies.md#ranking-formula)

   ![](assets/exd-uc-strategy-formula.png)

<!--
## Create decision items and selection strategies

You first need to create items, group them together in collections, set up rules and ranking methods. These elements will allow you to build selection strategies.

1. Navigate to **[!UICONTROL Decisioning]** > **[!UICONTROL Catalogs]** and create several decision items. Set constraints using audiences or rules to restrict each item to specific profiles only. [Learn more](items.md)

1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)

1. Create **collections** to categorize and group your decision items according to your preferences. [Learn more](collections.md)

1. Create **decision rules** to determine to whom a decision item can be shown. [Learn more](rules.md)

1. Create **ranking methods** and apply them within decision strategies to determine the priority order for selecting decision items. [Learn more](ranking.md)

1. Build **selection strategies** that leverage collections, decision rules, and ranking methods to identify the decision items suitable for displaying to profiles. [Learn more](selection-strategies.md)
-->

## Erstellen von Entscheidungsrichtlinien

<!--To present the best dynamic offer and experience to your visitors on your website or mobile app, add a decision policy to a code-based campaign.

Define two delivery treatments each containing a different decision policy.-->

1. Erstellen Sie eine Kampagne und wählen Sie die Aktion **[!UICONTROL Code-basiertes Erlebnis]** aus. [Weitere Informationen](../code-based/create-code-based.md)

1. Beginnen Sie im Fenster **[!UICONTROL Inhalt bearbeiten]** mit der Personalisierung der Abwandlung A.

1. Wählen Sie das Symbol **[!UICONTROL Entscheidungen]** aus, klicken Sie auf **[!UICONTROL Entscheidung erstellen]** und geben Sie die Entscheidungsdetails ein. [Weitere Informationen](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Wählen Sie die erste erstellte Strategie aus. Klicken Sie auf **[!UICONTROL Strategie hinzufügen]**.

1. Klicken Sie auf **[!UICONTROL Erstellen]**. Die neue Entscheidung wird unter **[!UICONTROL Entscheidungen]** hinzugefügt.

   ![](assets/decision-code-based-decision-added.png)

1. Klicken Sie auf das Symbol für weitere Aktionen (drei Punkte) und wählen Sie **[!UICONTROL Hinzufügen]** aus. Jetzt können Sie alle Entscheidungsattribute hinzufügen, die Sie darin haben möchten.

   ![](assets/decision-code-based-add-decision.png)

1. Sie können auch jedes beliebige Attribut hinzufügen, das im Personalisierungseditor verfügbar ist, z. B. Profilattribute.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Wenn Ihr Versand personalisiert wurde, klicken Sie auf der Übersichtsseite der Kampagne auf **[!UICONTROL Experiment erstellen]**, um mit der Konfiguration Ihres Inhaltsexperiments zu beginnen. [Weitere Informationen](../content-management/content-experiment.md)

1. Wählen Sie im Fenster **[!UICONTROL Inhalt bearbeiten]** die Abwandlung B aus und wiederholen Sie die obigen Schritte, um eine weitere Entscheidung zu erstellen.

1. Wählen Sie die zweite Strategie aus, die Sie erstellt haben. Klicken Sie auf **[!UICONTROL Strategie hinzufügen]**.

1. Speichern Sie Ihren Inhalt.
