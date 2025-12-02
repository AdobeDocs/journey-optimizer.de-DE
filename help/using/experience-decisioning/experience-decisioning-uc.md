---
title: Anwendungsfall für die Entscheidungsfindung
description: Erfahren Sie, wie Sie mit dem Code-basierten Erlebniskanal Entscheidungen erstellen und in Inhaltsexperimenten verwenden.
feature: Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
exl-id: 09770df2-c514-4217-a71b-e31c248df543
version: Journey Orchestration
source-git-commit: 17c8bc8b37c4bdf7c93735e152eedf7e0bbaf62a
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 96%

---

# Verwenden der Entscheidungsfindung in einem Code-basierten Erlebnis mit Inhaltsexperimenten {#experience-decisioning-uc}

In diesem Anwendungsfall werden alle Schritte vorgestellt, die zur Verwendung der Entscheidungsfindung mit dem Code-basierten [!DNL Journey Optimizer]-Kanal erforderlich sind.

>[!NOTE]
>
>Die alte Entscheidungs-Management-Funktion wird vom Code-basierten Erlebniskanal nicht unterstützt.

In diesem Beispiel ist nicht sicher, ob eine bestimmte Rangfolgenformel besser funktioniert als die vorab zugewiesenen Angebotsprioritäten. Um zu messen, welche Option für die Zielgruppe am besten geeignet ist, erstellen Sie mit der Funktion [Inhaltsexperiment](../content-management/content-experiment.md) eine Kampagne, bei der Sie zwei Abwandlungen für den Versand definieren:

* Die erste Abwandlung verwendet die **Priorität** als Rangfolgenmethode.
* Die zweite Abwandlung verwendet eine **Formel** als Rangfolgenmethode.

>[!NOTE]
>
>Implementierungsdetails für Tests und Deduplizierung bei Verwendung von Decisioning in Code-basierten Erlebnissen finden Sie [dieser Seite](../code-based/code-based-decisioning-implementations.md).

## Erstellen von Auswahlstrategien

Zunächst müssen Sie zwei Auswahlstrategien erstellen: eine mit der Priorität und eine mit einer Formel als Rangfolgenmethode.

>[!NOTE]
>
>Sie können auch einzelne Entscheidungselemente erstellen, ohne eine Auswahlstrategie durchlaufen zu müssen. Es wird die für jedes Element festgelegte Priorität angewendet.

### Erstellen einer Strategie mithilfe der Priorität

Erstellen Sie die erste Auswahlstrategie mit der Priorität als Rangfolgenmethode anhand der folgenden Schritte.

1. Erstellen Sie ein Entscheidungselement. [Weitere Informationen](items.md)

1. Legen Sie die **[!UICONTROL Priorität]** des Entscheidungselements im Vergleich zu anderen fest. Wenn ein Profil für mehrere Elemente qualifiziert ist, gewährt eine höhere Priorität dem Element Vorrang vor anderen.

   ![](assets/exd-uc-item-priority.png){width="90%"}

   >[!NOTE]
   >
   >Die Priorität ist ein ganzzahliger Datentyp. Alle Attribute, bei denen es sich um ganzzahlige Datentypen handelt, sollten ganzzahlige Werte (ohne Dezimalstellen) enthalten.

1. Legen Sie die Eignung des Entscheidungselements fest:

   * Legen Sie mithilfe von Zielgruppen oder Regeln Einschränkungen fest, um jedes Element auf bestimmte Profile zu beschränken. [Weitere Informationen](items.md#eligibility)

   * Legen Sie mithilfe von Begrenzungsregeln fest, wie oft ein Angebot maximal unterbreitet werden kann. [Weitere Informationen](items.md#capping)

1. Wiederholen Sie bei Bedarf die obigen Schritte, um zusätzliche Entscheidungselemente zu erstellen.

1. Erstellen Sie eine **Sammlung**, in der die Entscheidungselemente enthalten sein werden. [Weitere Informationen](collections.md)

1. Erstellen Sie eine [Auswahlstrategie](selection-strategies.md#create-selection-strategy) und wählen Sie die [Sammlung](collections.md) aus, die die zu berücksichtigenden Angebote enthält.

1. [Wählen Sie die Rangfolgenmethode](#select-ranking-method), die zur Auswahl des besten Angebots für jedes Profil verwendet werden soll. Wählen Sie in diesem Fall **[!UICONTROL Angebotspriorität]** aus: Wenn mehrere Angebote für diese Strategie infrage kommen, verwendet die Entscheidungsfindungs-Engine den Wert, der in den Angeboten als **[!UICONTROL Priorität]** festgelegt wurde. [Weitere Informationen](selection-strategies.md#offer-priority)

   ![](assets/exd-uc-strategy-priority.png){width="90%"}

### Erstellen einer anderen Strategie mithilfe einer Formel

Um die zweite Auswahlstrategie mit einer Formel als Rangfolgenmethode zu erstellen, gehen Sie wie folgt vor.

1. Erstellen Sie ein Entscheidungselement. [Weitere Informationen](items.md)

   <!--Do you need to set the same **[!UICONTROL Priority]** as for the first decision item, or it won't be considered at all?-->

1. Legen Sie die Eignung des Entscheidungselements fest:

   * Legen Sie mithilfe von Zielgruppen oder Regeln Einschränkungen fest, um jedes Element auf bestimmte Profile zu beschränken. [Weitere Informationen](items.md#eligibility)

   * Legen Sie mithilfe von Begrenzungsregeln fest, wie oft ein Angebot maximal unterbreitet werden kann. [Weitere Informationen](items.md#capping)

1. Wiederholen Sie bei Bedarf die obigen Schritte, um zusätzliche Entscheidungselemente zu erstellen.

1. Erstellen Sie eine **Sammlung**, in der die Entscheidungselemente enthalten sein werden. [Weitere Informationen](collections.md)

1. Erstellen Sie eine [Auswahlstrategie](selection-strategies.md#create-selection-strategy) und wählen Sie die [Sammlung](collections.md) aus, die die zu berücksichtigenden Angebote enthält.

1. [Wählen Sie die Rangfolgenmethode](#select-ranking-method), die Sie zur Auswahl des besten Angebots für jedes Profil verwenden möchten. Wählen Sie in diesem Fall **[!UICONTROL Formel]**, um anhand eines bestimmten berechneten Ergebnisses zu bestimmen, welches geeignete Angebot bereitgestellt werden soll. [Weitere Informationen](selection-strategies.md#ranking-formula)

   ![](assets/exd-uc-strategy-formula.png){width="90%"}

## Erstellen einer Code-basierten Erlebniskampagne

<!--To present the best dynamic offer and experience to your visitors on your website or mobile app, add a decision policy to a code-based campaign.

Define two delivery treatments each containing a different decision policy.-->

Nachdem Sie die beiden Auswahlstrategien konfiguriert haben, erstellen Sie eine Code-basierte Erlebniskampagne, bei der Sie für jede Strategie eine andere Abwandlung definieren, um zu vergleichen, welche am besten funktioniert.

1. Erstellen Sie eine Kampagne und wählen Sie die Aktion **[!UICONTROL Code-basiertes Erlebnis]** aus. [Weitere Informationen](../code-based/create-code-based.md)

1. Klicken Sie auf der Übersichtsseite der Kampagne auf **[!UICONTROL Experiment erstellen]**, um Ihr Inhaltsexperiment zu konfigurieren. [Weitere Informationen](../content-management/content-experiment.md)

   ![](assets/exd-uc-create-experiment.png){width="90%"}

1. Wählen Sie auf der Übersichtsseite der Kampagne eine Code-basierte Konfiguration aus und klicken Sie auf **[!UICONTROL Inhalt bearbeiten]**.

   ![](assets/exd-uc-edit-cbe-content.png){width="90%"}

1. Um im Fenster zur Inhaltsbearbeitung **Abwandlung A** zu personalisieren, klicken Sie auf **[!UICONTROL Code bearbeiten]**.

   ![](assets/exd-uc-experiment-treatment-a.png){width="90%"}

1. Wählen Sie im [Code-Editor](../code-based/create-code-based.md#edit-code) die Option **[!UICONTROL Entscheidungsrichtlinie]** aus, klicken Sie auf **[!UICONTROL Entscheidungsrichtlinie hinzufügen]** und geben Sie die Entscheidungsdetails ein. [Weitere Informationen](create-decision.md#add)

   ![](assets/decision-code-based-create.png){width="90%"}

1. Klicken Sie im Abschnitt **[!UICONTROL Strategiesequenz]** auf die Schaltfläche **[!UICONTROL Hinzufügen]** und wählen Sie **[!UICONTROL Auswahlstrategie]**. [Weitere Informationen](create-decision.md#select)

   ![](assets/decision-code-based-strategy-sequence.png){width="80%"}

   >[!NOTE]
   >
   >Sie können auch **[!UICONTROL Entscheidungselement]** auswählen, um einzelne Elemente hinzuzufügen, ohne eine Auswahlstrategie durchlaufen zu müssen. Es wird die für jedes Element festgelegte Priorität angewendet.

1. Wählen Sie die erste Strategie aus, die Sie erstellt haben – die Strategie mit „Priorität“ als Rangfolgenmethode.

   ![](assets/exd-uc-experiment-strategy-priority.png){width="90%"}

1. Speichern Sie Ihre Änderungen und klicken Sie auf **[!UICONTROL Erstellen]**. Die neue Entscheidung wird unter **[!UICONTROL Entscheidungsrichtlinie]** hinzugefügt.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Richtlinie einfügen]**. Der Code, der der Entscheidungsrichtlinie entspricht, wird hinzugefügt. Fügen Sie dann alle gewünschten Attribute zum Code hinzu, einschließlich Profilattributen. [Weitere Informationen](create-decision.md#create-decision)

   ![](assets/exd-uc-experiment-insert-policy.png){width="90%"}

1. Speichern Sie Ihre Änderungen.

1. Gehen Sie zurück zum Fenster zur Inhaltsbearbeitung, wählen Sie die Plusschaltfläche (+) aus, um **Abwandlung B** hinzuzufügen, wählen Sie sie aus und klicken Sie auf **[!UICONTROL Code bearbeiten]**.

   ![](assets/exd-uc-experiment-treatment-b.png){width="90%"}

1. Wiederholen Sie die Schritte 5 und 6 oben, um eine weitere Entscheidungsrichtlinie zu erstellen, und wählen Sie die zweite von Ihnen erstellte Auswahlstrategie aus: die Strategie mit der Formel als Rangfolgenmethode. <!--Do you need to create exactly the same content to compare only the ranking method?-->

   ![](assets/exd-uc-experiment-strategy-formula.png){width="90%"}

1. Bearbeiten Sie Ihre Entscheidungsrichtlinie nach Bedarf (siehe Schritte 8 und 9 oben).

1. Speichern Sie Ihre Änderungen und [veröffentlichen Sie Ihre Code-basierte Erlebniskampagne](../code-based/publish-code-based.md).

Verfolgen Sie nach dem Experiment mit dem [Experimentkampagnenbericht](../reports/campaign-global-report-cja-experimentation.md), wie Ihre Kampagnenabwandlungen funktionieren.<!-- and [report on decisioning](cja-reporting.md).--> Sie können dann die Ergebnisse Ihres Experiments auslegen. [Weitere Informationen](../content-management/get-started-experiment.md#interpret-results)

Bei schlüssigem Ergebnis:

* Sie können die Abwandlung mit der Rangfolge veröffentlichen, die für alle Ihre Kundinnen und Kunden am besten funktioniert. 
* Sie können auch eine neue Kampagne mit der Auswahlstrategie erstellen, bei der die Rangfolgenmethode repliziert wird, die am besten funktioniert.