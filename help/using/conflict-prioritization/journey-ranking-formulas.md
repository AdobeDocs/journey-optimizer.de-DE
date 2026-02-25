---
title: Journey-Ranking-Formeln für Schlichtungen
description: Erfahren Sie, wie Sie Formeln erstellen, um Journey nach Schlichtung zu ordnen, sodass für jedes Profil basierend auf Regeln und Kontext die beste Journey ausgewählt wird.
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: fe6e8221201ee813251a46c6603d85f0803873c0
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 20%

---

# Formeln verwenden, um Journey zu ordnen {#journey-ranking-formulas}

>[!AVAILABILITY]
>
>Diese Funktion ist derzeit nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

[!DNL Adobe Journey Optimizer] können Sie steuern, welche Journey ein Profil eingeben kann, wenn diese für mehr qualifiziert sind als das System zulässt. Hierfür können Sie mithilfe von [Regelsätzen](rule-sets.md) Begrenzungen für Journey-Einträge oder gleichzeitige Zugriffe definieren. Wenn ein Profil für mehr Journey geeignet ist, als die Obergrenze zulässt, bestimmt die jedem Journey zugewiesene Priorität, welche Journey ausgewählt werden.

Anstatt die Priorität zu verwenden, können Sie auch **Rangfolgeformeln** verwenden, um das Ranking von Journey dynamisch auf der Grundlage von Journey-Attributen, Profilattributen oder KI-Modellbewertungen anzupassen.

Formeln bieten Ihnen mehr Flexibilität als statische Priorität. Sie können beispielsweise eine Journey für Mitglieder des Treueprogramms „Gold“ steigern.

<!--
>[!NOTE]
>
>Journey ranking formulas follow the same guardrails as decisioning ranking formulas (nesting depth, rule string size). [Learn more about Decisioning guardrails & limitations](../experience-decisioning/decisioning-guardrails.md#ranking-formulas).-->

## Erstellen einer Rangfolgenformel {#create-journey-ranking-formula}

Gehen Sie wie folgt vor, um eine Rangfolgenformel für Ihre Journey zu erstellen.

1. Rufen Sie den Abschnitt **[!UICONTROL Orchestrierung]** auf und wählen Sie dann die Registerkarte **[!UICONTROL Rangfolgeformeln]** aus. Es wird die Liste der zuvor erstellten Rangfolgen angezeigt.

1. Klicken Sie auf **[!UICONTROL Formel erstellen]**.

1. Geben Sie den Namen der Formel an und fügen Sie bei Bedarf eine Beschreibung hinzu.

   ![Bereich mit Formeldetails mit Feldern für Name und Beschreibung](assets/journey-formula-details.png){width="80%"}


   >[!NOTE]
   >
   >Das Ranking-Objekt ist die Entität, auf die die Rangfolgenformel angewendet wird. Standardmäßig ist das Ranking-Objekt auf **[!UICONTROL Journey]** festgelegt.

   <!--
    Selecting a formula entity specifies which type of item—such as journeys or other entities—the ranking formula will apply to. This determines the context in which the formula operates, allowing you to define rules that influence how those items are ranked.-->

1. Klicken Sie optional auf **[!UICONTROL KI-Modell auswählen]**, um das Modell festzulegen, das als Referenz zur Erstellung der Rangfolgenformel verwendet wird. 

<!--
    >[!NOTE]
    >
    >[Personalized optimization models](../experience-decisioning/ranking/personalized-optimization-model.md) using continuous metrics are not supported with the AI formula builder.

    Every time you refer to a model score when defining your formula below, the AI model that you selected will be used. [Learn more on AI models](../experience-decisioning/ranking/ai-models.md)-->

1. Geben **[!UICONTROL im Abschnitt]** Kriterium 1“ an, auf welche Journey Sie einen Rangfolgenwert anwenden möchten. Gehen Sie dazu wie folgt vor:

   * Wählen Sie ein [Journey-](../building-journeys/journey-properties.md) aus (z. B. Journey-Name, Tags, Priorität oder andere Journey-Eigenschaften).
   * einen logischen Operator auswählen;
   * Übereinstimmende Bedingung hinzufügen - Sie können entweder einen Wert eingeben/auswählen oder ein Profilattribut auswählen.

   ![Abschnitt „Kriterium 1“ mit Journey-Attribut, Operator und übereinstimmender Bedingung](assets/journey-formula-criterion-1.png){width="70%"}

1. Optional können Sie zusätzliche Elemente angeben, um die übereinstimmenden Bedingungen zu verfeinern, damit Ihre Kriterien erfüllt sind.

   ![Zusätzliche Bedingung zur Verfeinerung von Übereinstimmungskriterien](assets/journey-formula-additional-condition.png){width="70%"}

   Sie haben beispielsweise definiert, *Kriterium 1* wie *Journey-Tags* &quot;*&quot;*. Darüber hinaus können Sie eine weitere Bedingung hinzufügen, z. B. wenn *Treuestatus* gleich *Gold*, dann *Kriterium 1* wahr ist.

1. Erstellen Sie einen Ausdruck, der den Journey einen Rangfolgenwert zuweist, die die oben definierte Bedingung erfüllen. Sie können eine der folgenden Optionen referenzieren:
   * Eine Variable:
      * die Journey-Priorität, bei der es sich um einen manuellen Wert handelt, der der Journey beim [Erstellen einer Journey](../building-journeys/journey-gs.md) zugewiesen wird;
      * den Wert, der aus dem KI-Modell hervorgegangen ist, das Sie oben optional ausgewählt haben;
   * Ein -Attribut:
      * alle Attribute, die im Profil live sein könnten, z. B. jede extern abgeleitete Tendenzbewertung;
      * ein Journey-Attribut;
   * ein statischer Wert, den Sie in einem freien Format zuweisen können;
   * Eine Kombination aus allen oben genannten.

   ![Expression Builder zum Zuweisen eines Rangfolgenwerts mithilfe von Variablen, Attributen oder statischen Werten](assets/journey-formula-expression.png){width="70%"}

1. Klicken Sie auf **[!UICONTROL Kriterium hinzufügen]**, um ein oder mehrere Kriterien beliebig oft hinzuzufügen. Es gilt folgende Logik:
   * Wenn das erste Kriterium für ein bestimmtes Entscheidungselement zutrifft, hat es Vorrang vor den nächsten Kriterien.
   * Wenn dies nicht der Fall ist, wechselt die Entscheidungs-Engine zum zweiten Kriterium usw.

1. Nachdem Sie alle Ihre Kriterien im letzten Feld definiert haben, können Sie einen Ausdruck erstellen, der allen Journey zugewiesen wird, die die oben genannten Kriterien nicht erfüllen.

   ![Ausdrucksfeld für Journey, die keine Kriterien erfüllen](assets/journey-formula-criteria-not-met.png){width="70%"}

1. Klicken Sie **[!UICONTROL Erstellen]**, um Ihre Rangfolgenformel abzuschließen.

Sie können diese Formel jetzt aus der Liste auswählen, um ihre Details anzuzeigen und sie zu bearbeiten oder zu löschen. Sie ist dann verfügbar, wenn Sie einen Regelsatz konfigurieren. [Weitere Informationen](#assign-formula-to-ruleset)

### Beispiele für Rangfolgeformeln {#journey-ranking-formula-example}

Sehen Sie sich die folgenden Beispiele an.

+++Beispiel 1: Verwenden der Journey-Priorität oder des KI-Werts basierend auf Journey-Tags

![Rangfolgeformel: Marketing-Tag verwendet Journey-Priorität](assets/journey-formula-ex-1.png){width="60%"}

Wenn die Journey ein „Marketing“-Tag hat, ist der Rangfolgewert die Journey-Priorität.

![Rangfolgeformel: Promo-Tag verwendet KI-Modellbewertung](assets/journey-formula-ex-2.png){width="60%"}

Wenn die Journey ein „Promo“-Tag hat, ist der Ranking-Score der KI-Modellwert.

+++

+++Beispiel 2: Steigern der Treue von Journey durch Profilstatus


![Rangfolgeformel: Treue-Tag mit Goldstatus verwendet Journey-Priorität plus 5](assets/journey-formula-ex-3.png){width="60%"}

Wenn die Journey das Tag „Loyalty“ aufweist und der Treuestatus des Profils „Gold“ lautet, wird der Rangfolgenwert verwendet, d. h. die Journey-Priorität plus 5.

![Rangfolgeformel: Treue-Tag mit Silberstatus verwendet Journey-Priorität plus 2](assets/journey-formula-ex-4.png){width="60%"}

Wenn die Journey ein „Loyalty“-Tag hat und der Treuestatus des Profils Silber ist, ist der Rangfolgenwert die Journey-Priorität plus 2.

Wenn keine der oben genannten Bedingungen erfüllt ist, wird der Rangfolgenwert als Journey-Priorität verwendet.

+++

### Verwenden des Code-Editors {#journey-ranking-formula-code-editor}

Um Rangfolgenformeln in der **PQL-Syntax** auszudrücken, wechseln Sie mithilfe der entsprechenden Schaltfläche oben rechts auf dem Bildschirm zum Code-Editor. Weiterführende Informationen zur Verwendung der PQL-Syntax finden Sie im [entsprechenden Handbuch](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=de).

>[!CAUTION]
>
>Diese Aktion verhindert ein Zurückkehren zur Standard-Builder-Ansicht für diese Formel.

Anschließend können Sie Journey-Attribute, Profilattribute und statische Werte nutzen, um Ihre Rangfolgenformel zu erstellen.

<!--The code editor is similar to the one used in Decisioning ranking formulas. [Learn more](../experience-decisioning/ranking/ranking-formulas.md#ranking-code-editor)-->

## Zuweisen der Formel zu einem Regelsatz {#assign-formula-to-ruleset}

Um eine Formel zur Rangfolge Ihrer Journey zu verwenden, müssen Sie sie einem Regelsatz zuweisen.

>[!NOTE]
>
>Formeln werden auf der Ebene des Regelsatzes zugewiesen, nicht in den einzelnen Journey.

1. Erstellen Sie im Menü **[!UICONTROL Geschäftsregeln]** einen Regelsatz, den Sie für die Journey-Schlichtung verwenden möchten. [Weitere Informationen](rule-sets.md#Create)

1. Wählen Sie unbedingt die Domain **[!UICONTROL Journey]** aus.

   ![Regelsatz-Eigenschaften mit ausgewählter Journey-Domain](assets/journey-formula-rule-set-journey.png){width="60%"}

1. Legen Sie in den Eigenschaften des Regelsatzes die **[!UICONTROL Rangfolgenmethode]** auf **[!UICONTROL Formel]** fest (anstelle der Standardeinstellung **[!UICONTROL Priorität]**).

1. Wählen Sie die von Ihnen erstellte Rangfolgenformel aus der Dropdown-Liste aus.

   ![Regelsatz mit aus der Dropdown-Liste ausgewählter Rangfolgenformel](assets/journey-rule-set-formula.png){width="60%"}

1. Erstellen Sie die Journey-Begrenzungsregeln, die Sie dem Regelsatz hinzufügen möchten. [Weitere Informationen](journey-capping.md#create-rule)

1. Speichern Sie den Regelsatz.

Jetzt ist die Formel dem Regelsatz zugewiesen. Sie können diesen Regelsatz dann auf Ihre Journey anwenden.

## Anwenden des Regelsatzes auf eine Journey {#assign-rule-set-to-journey}

Gehen Sie wie folgt vor, um den Regelsatz einer Journey zuzuweisen.

1. Erstellen oder öffnen Sie die Journey, der Sie den Regelsatz zuweisen möchten. [Erfahren Sie, wie Sie eine Journey erstellen](../building-journeys/journey-gs.md)

1. Wählen Sie in den Journey-Eigenschaften den Regelsatz aus der Dropdown-Liste aus.  [Weitere Informationen](journey-capping.md#apply-capping).

   >[!NOTE]
   >
   >Auf eine Journey kann jeweils nur ein Regelsatz angewendet werden.

1. Speichern Sie die Journey.

Alle Journey, die diesen Regelsatz verwenden, werden bei der Anwendung der Begrenzung nach der ausgewählten Formel gereiht.

Informationen zur Überwachung der Leistung Ihrer Regelsätze und Rangfolgenformeln finden Sie im Abschnitt [Journey-Begrenzung und ](../reports/channel-report-cja.md#rule-sets)Konflikte“ im Übersichtsbericht.

<!--
## Reporting {#reporting}

Reporting for journey arbitration helps you understand how rule sets and ranking formulas perform:

* **Exclusions** – Whether journeys were excluded from users and which rule set (and reason) prevented entry.
* **Rule set performance** – For each rule set, metrics such as journey enters, journey exclusions, journey engagement, and other optimization metrics.
* **Cross-journey view** – Time-based view of profiles across journeys (e.g. journey enters, failures, exclusions) to see the impact of capping and ranking.

Use these reports to validate that your formulas and caps are behaving as intended and to tune ranking logic over time.-->

