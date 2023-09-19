---
title: Erstellen von Entscheidungen
description: Erfahren Sie, wie Sie Entscheidungen erstellen
feature: Offers
topic: Integrations
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: 69a2ef17b6f5ccd40c08858f7b434029964d544d
workflow-type: tm+mt
source-wordcount: '1245'
ht-degree: 11%

---

# Entscheidungsrichtlinien erstellen {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="Was ist eine Entscheidung?"
>abstract="Entscheidungsrichtlinien nutzen die Entscheidungs-Engine für Erlebnisse, um je nach Zielgruppe die besten bereitzustellenden Inhalte auszuwählen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html?lang=de" text="Über Experience Decisioning"

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
* **[Entscheidungsrichtlinien erstellen](create-decision.md)**

>[!ENDSHADEBOX]

Entscheidungsrichtlinien sind Container für Ihre Angebote, die die Experience Decisioning-Engine nutzen, um je nach Zielgruppe die besten bereitzustellenden Inhalte auszuwählen.

>[!NOTE]
>
>Im [!DNL Journey Optimizer] Benutzeroberfläche verwenden, werden Entscheidungsrichtlinien als Entscheidungen bezeichnet<!--but they are decision policies. TBC if this note is needed-->.

## Eine Entscheidungsrichtlinie zu einer code-basierten Kampagne hinzufügen {#add-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="Definieren der Anzahl der zurückzugebenden Elemente"
>abstract="Wählen Sie die Anzahl der Entscheidungselemente aus, die zurückgegeben werden sollen. Wenn Sie beispielsweise &quot;2&quot;auswählen, werden die 2 besten geeigneten Angebote für die aktuelle Oberfläche angezeigt."

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="Fallback auswählen"
>abstract="Ein Fallback-Element wird dem Benutzer angezeigt, wenn keine der für diese Entscheidungsrichtlinie definierten Auswahlstrategien qualifiziert ist."

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="Was ist eine Strategie?"
>abstract="Die Abfolge der Auswahlstrategie bestimmt, welche Strategie zuerst bewertet wird. Es ist mindestens eine Strategie erforderlich. Entscheidungspunkte in kombinierten Strategien werden gemeinsam bewertet."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html?lang=de" text="Strategien erstellen"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html?lang=de" text="Testreihenfolge"

Um Ihren Besuchern auf Ihrer Website oder in Ihrer mobilen App das beste dynamische Angebot und Erlebnis zu präsentieren, fügen Sie einer code-basierten Kampagne eine Entscheidungsrichtlinie hinzu. Gehen Sie dazu wie folgt vor.

1. Erstellen Sie eine Kampagne und wählen Sie die **[!UICONTROL Codebasiertes Erlebnis (Beta)]** Aktion. [Weitere Informationen](../code-based/create-code-based.md)

   >[!NOTE]
   >
   >Die code-basierte Erlebnisfunktion ist derzeit als Beta-Version verfügbar, um nur Benutzer auszuwählen.

1. Aus dem [Code-Editor](../code-based/create-code-based.md#edit-code), wählen Sie die **[!UICONTROL Entscheidungen]** Symbol und klicken Sie auf **[!UICONTROL Entscheidung erstellen]**.

   ![](assets/decision-code-based-create.png)

1. Füllen Sie die Details für Ihre Entscheidungsrichtlinie aus: Fügen Sie einen Namen hinzu und wählen Sie einen Katalog aus.

   >[!NOTE]
   >
   >Derzeit ist nur die Standardeinstellung **[!UICONTROL Angebote]** Katalog verfügbar.

   ![](assets/decision-code-based-details.png)

1. Wählen Sie die Anzahl der Elemente aus, die zurückgegeben werden sollen. Wenn Sie beispielsweise &quot;2&quot;auswählen, werden die 2 besten geeigneten Angebote für die aktuelle Oberfläche angezeigt. Klicken Sie auf **[!UICONTROL Weiter]**

1. Verwenden Sie die **[!UICONTROL Strategie hinzufügen]** -Schaltfläche, um die Auswahlstrategien für Ihre Entscheidungsrichtlinie zu definieren. Jede Strategie besteht aus einer Angebotskollektion, die einer Eignungsbegrenzung zugeordnet ist, und einer Rangmethode zur Bestimmung der anzuzeigenden Angebote. [Weitere Informationen](selection-strategies.md)

   ![](assets/decision-code-based-strategies.png)

   >[!NOTE]
   >
   >Es ist mindestens eine Strategie erforderlich. Sie können nicht mehr als 10 Strategien hinzufügen.

1. Aus dem **[!UICONTROL Strategie hinzufügen]** -Bildschirm können Sie auch eine Strategie erstellen. Die **[!UICONTROL Auswahlstrategie erstellen]** Die Schaltfläche leitet Sie zum **[!UICONTROL Erlebnisentscheidung]** > **[!UICONTROL Konfigurationen]** Menü. [Weitere Informationen](selection-strategies.md)

   ![](assets/decision-code-based-add-strategy.png)

1. Beim Hinzufügen mehrerer Strategien werden diese in einer bestimmten Reihenfolge bewertet. Die erste Strategie, die der Sequenz hinzugefügt wurde, wird zuerst ausgewertet usw. [Weitere Informationen](#evaluation-order)

   Um die Standardreihenfolge zu ändern, können Sie die Strategien und/oder Gruppen per Drag-and-Drop verschieben, um sie nach Bedarf neu anzuordnen.

   ![](assets/decision-code-based-strategy-groups.png)

1. Fügen Sie einen Fallback hinzu. Ein Fallback-Element wird Benutzern angezeigt, wenn keine der oben genannten Auswahlstrategien qualifiziert ist.

   ![](assets/decision-code-based-strategy-fallback.png)

   Sie können ein beliebiges Element aus der Liste auswählen, das alle in der aktuellen Sandbox erstellten Entscheidungselemente anzeigt. Wenn keine Auswahlstrategie qualifiziert ist, wird dem Benutzer unabhängig von den Datumsangaben und den auf das ausgewählte Element angewendeten Eignungsbeschränkungen der Fallback angezeigt<!--nor frequency capping when available - TO CLARIFY-->.

   >[!NOTE]
   >
   >Ein Fallback ist optional. Wenn kein Fallback ausgewählt ist und keine Strategie qualifiziert ist, wird nichts angezeigt durch [!DNL Journey Optimizer].

1. Speichern Sie Ihre Auswahl und klicken Sie auf **[!UICONTROL Erstellen]**. Die neue Entscheidungspolitik wird unter **[!UICONTROL Entscheidungen]**.

   ![](assets/decision-code-based-decision-added.png)

Nachdem die Entscheidungsrichtlinie erstellt wurde, können Sie die Entscheidungsattribute in Ihrem code-basierten Erlebnisinhalt verwenden. [Weitere Informationen](#use-decision-policy)

## Testreihenfolge {#evaluation-order}

Wie oben beschrieben, besteht eine Strategie aus einer Sammlung, einer Ranking-Methode und Eignungsbegrenzungen.

Sie haben folgende Möglichkeiten:

* Legen Sie die sequenzielle Reihenfolge fest, in der die Strategien ausgewertet werden sollen.
* Kombinieren Sie mehrere Strategien, sodass sie zusammen und nicht getrennt ausgewertet werden.

Mehrere Strategien und ihre Gruppierung bestimmen die Priorität der Strategien und die Rangfolge der infrage kommenden Angebote. Die erste Strategie hat die höchste Priorität, und die in derselben Gruppe zusammengefassten Strategien haben dieselbe Priorität.

Sie haben beispielsweise zwei Sammlungen, eine in Strategie A und eine in Strategie B. Die Anfrage besteht darin, zwei Entscheidungselemente zurückzusenden. Angenommen, es gibt zwei förderfähige Angebote aus Strategie A und drei förderfähige Angebote aus Strategie B.

* Wenn die beiden Strategien **nicht kombiniert** oder in sequenzieller Reihenfolge (1 und 2) werden die ersten beiden in Frage kommenden Angebote aus der ersten Strategie in der ersten Zeile zurückgegeben. Wenn es für die erste Strategie nicht zwei infrage kommende Angebote gibt, wird die Entscheidungs-Engine nacheinander zur nächsten Strategie übergehen, um so viele Angebote zu finden, wie noch erforderlich sind, und letztendlich bei Bedarf einen Fallback zurückgeben.

  ![](assets/decision-code-based-consecutive-strategies.png)

* Wenn die beiden Sammlungen **gleichzeitig ausgewertet** Da es zwei berechtigte Angebote aus Strategie A und drei in Frage kommende Angebote aus Strategie B gibt, werden die fünf Angebote alle auf der Grundlage des durch die jeweiligen Ranking-Methoden bestimmten Werts in einem bestimmten Bereich zusammengefasst. Es werden zwei Angebote angefordert, so dass von diesen fünf Angeboten die beiden geeignetsten zurückgegeben werden.

  ![](assets/decision-code-based-combined-strategies.png)

+++ **Beispiel mit mehreren Strategien**

Betrachten wir nun ein Beispiel, bei dem mehrere Strategien in verschiedene Gruppen unterteilt sind.

Sie haben drei Strategien definiert. Strategie 1 und Strategie 2 werden in Gruppe 1 kombiniert und Strategie 3 ist unabhängig (Gruppe 2).

Die für die einzelnen Strategien infrage kommenden Angebote und ihre Priorität (in der Bewertung der Ranking-Funktion verwendet) lauten wie folgt:

* Gruppe 1:
   * Strategie 1 - (Angebot 1, Angebot 2, Angebot 3) - Priorität 1
   * Strategie 2 - (Angebot 3, Angebot 4, Angebot 5) - Priorität 1

* Gruppe 2:
   * Strategie 3 - (Angebot 5, Angebot 6) - Priorität 0

Die Angebote mit der höchsten Priorität werden zuerst ausgewertet und der Liste der bewerteten Angebote hinzugefügt.

**Iteration 1:**

Strategie 1- und Strategie 2-Angebote werden zusammen ausgewertet (Angebot 1, Angebot 2, Angebot 3, Angebot 4, Angebot 5). Nehmen wir an, das Ergebnis lautet:

Angebot 1 - 10 Angebot 2 - 20 Angebot 3 - 30 aus Strategie 1, 45 aus Strategie 2. Der höchste Wert von beiden wird berücksichtigt, also 45.
Angebot 4 - 40
Angebot 5 - 50

Die bewerteten Angebote lauten nun wie folgt: Angebot 5, Angebot 3, Angebot 4, Angebot 2, Angebot 1.

**Iteration 2:**

Strategie 3-Angebote werden ausgewertet (Angebot 5, Angebot 6). Nehmen wir an, das Ergebnis lautet:

* Angebot 5 - wird nicht ausgewertet, da es bereits im obigen Ergebnis enthalten ist.
* Angebot 6 - 60

Die Rangfolge der Angebote ist nun wie folgt: Angebot 5, Angebot 3, Angebot 4, Angebot 2, Angebot 1, Angebot 6.

+++

## Entscheidungsrichtlinie im Code-Editor verwenden {#use-decision-policy}

Nach der Erstellung kann die Entscheidungsrichtlinie im [Code-Editor](../code-based/create-code-based.md#edit-code). Gehen Sie dazu wie folgt vor.

>[!NOTE]
>
>Der Code-Editor nutzt die [!DNL Journey Optimizer] Ausdruckseditor mit allen Personalisierungs- und Bearbeitungsfunktionen. [Weitere Informationen](../personalization/personalization-build-expressions.md)

1. Klicken Sie auf das Symbol + . Der Code, der der Entscheidungsrichtlinie entspricht, wird hinzugefügt. Jetzt können Sie alle Entscheidungsattribute hinzufügen, die Sie in diesem Code hinzufügen möchten.

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >Diese Sequenz wird wiederholt, wie oft die Entscheidungsrichtlinie zurückgegeben werden soll. Wenn Sie beispielsweise 2 Elemente zurückgeben möchten, wenn Sie [Entscheidung erstellen](#add-decision), wird dieselbe Sequenz zweimal wiederholt.

1. Klicken Sie auf die Entscheidungsrichtlinie. Die Entscheidungsattribute werden angezeigt.

   Diese Attribute werden im **[!UICONTROL Angebote]** -Schema des Katalogs. Benutzerdefinierte Attribute werden im **_cjmstage** Ordner- und Standardattribute in **_experience** Ordner. [Weitere Informationen zum Schema des Angebotskatalogs](catalogs.md)

   ![](assets/decision-code-based-decision-attributes.png)

1. Klicken Sie auf jeden Ordner, um ihn zu erweitern. Platzieren Sie den Cursor an der gewünschten Position und klicken Sie auf das Symbol + neben dem Attribut, das Sie hinzufügen möchten. Sie können dem Code beliebig viele Attribute hinzufügen.

   ![](assets/decision-code-based-add-decision-attributes.png)

1. Um zurück zum Entscheidungsrichtlinienstamm zu navigieren, klicken Sie auf das Ordnersymbol.

   ![](assets/decision-code-based-decision-folder.png)

1. Sie können auch jedes andere Attribut hinzufügen, das im Ausdruckseditor verfügbar ist, z. B. Profilattribute.

   ![](assets/decision-code-based-decision-profile-attribute.png)
