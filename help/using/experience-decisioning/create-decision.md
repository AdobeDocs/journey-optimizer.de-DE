---
title: Erstellen von Entscheidungsrichtlinien
description: Informationen dazu, wie Sie Entscheidungsrichtlinien erstellen
feature: Experience Decisioning
topic: Integrations
role: User
level: Experienced
badge: label="Eingeschränkte Verfügbarkeit"
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: 5ffa0937bd9f23f29c8f02d2951cccac73d75f1b
workflow-type: tm+mt
source-wordcount: '1794'
ht-degree: 71%

---

# Erstellen von Entscheidungsrichtlinien {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="Was ist eine Entscheidung?"
>abstract="Entscheidungsrichtlinien enthalten die gesamte Auswahllogik, mit der die Entscheidungs-Engine den besten Inhalt auswählt. Entscheidungsrichtlinen sind kampagnenspezifisch. Ihr Ziel ist es, die besten Angebote für jedes Profil auszuwählen, während Sie bei der Kampagnenerstellung angeben können, wie die ausgewählten Entscheidungselemente dargestellt werden sollen, einschließlich der in die Nachricht aufzunehmenden Elemente."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Über die Erlebnis-Entscheidung"

Entscheidungsrichtlinien sind Container für Angebote, die die Erlebnis-Entscheidungs-Engine nutzen, um je nach Zielgruppe die besten bereitzustellenden Inhalte auszuwählen.

Entscheidungsrichtlinien enthalten die gesamte Auswahllogik, mit der die Entscheidungs-Engine den besten Inhalt auswählt. Entscheidungsrichtlinen sind kampagnenspezifisch. Ihr Ziel ist es, die besten Angebote für jedes Profil auszuwählen, während Sie bei der Kampagnenerstellung angeben können, wie die ausgewählten Entscheidungselemente dargestellt werden sollen, einschließlich der in die Nachricht aufzunehmenden Elemente.

>[!NOTE]
>
>In der [!DNL Journey Optimizer]Benutzeroberfläche werden Entscheidungsrichtlinien als Entscheidungen gekennzeichnet<!--but they are decision policies. TBC if this note is needed-->.

Die wichtigsten Schritte zur Nutzung von Entscheidungsrichtlinien in Code-basierten Kampagnen sind:

1. [Entscheidungsrichtlinie in eine code-basierte Kampagne erstellen](#add-decision)
1. [Verwenden der Entscheidungsrichtlinie in der code-basierten Kampagne](#use-decision-policy)
1. [Benutzerdefinierte Customer Journey Analytics-Reporting-Dashboards erstellen](#cja)

## Hinzufügen einer Entscheidungsrichtlinie zu einer Code-basierten Kampagne {#add-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="Festlegen der Anzahl der zurückzugebenden Elemente"
>abstract="Wählen Sie die Anzahl der Entscheidungselemente, die zurückgegeben werden sollen. Wenn Sie beispielsweise „2“ auswählen, werden die zwei am besten geeigneten Angebote für die aktuelle Konfiguration angezeigt."

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="Auswählen eines Fallbacks"
>abstract="Ein Fallback-Element wird dem Benutzenden angezeigt, wenn keine der für diese Entscheidungsrichtlinie definierten Auswahlstrategien qualifiziert ist."

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="Was ist eine Strategie?"
>abstract="Die Abfolge der Auswahlstrategie bestimmt, welche Strategie zuerst bewertet wird. Es ist mindestens eine Strategie erforderlich. Entscheidungspunkte in kombinierten Strategien werden gemeinsam bewertet."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Erstellen von Strategien"
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Bewertungsreihenfolge"

Um den Besucherinnen und Besuchern auf Ihrer Website oder in Ihrer Mobile App das beste dynamische Angebot und Erlebnis zu präsentieren, fügen Sie einer Code-basierten Kampagne eine Entscheidungsrichtlinie hinzu. Gehen Sie dazu wie folgt vor.

### Entscheidungsrichtlinie erstellen {#add}

1. Erstellen Sie eine Kampagne und wählen Sie die Aktion **[!UICONTROL Code-basiertes Erlebnis]** aus. [Weitere Informationen](../code-based/create-code-based.md)

1. Wählen Sie im [Code-Editor](../code-based/create-code-based.md#edit-code) das Symbol **[!UICONTROL Entscheidungsrichtlinie]** aus und klicken Sie auf **[!UICONTROL Entscheidungsrichtlinie hinzufügen]**.

   ![](assets/decision-code-based-create.png)

1. Füllen Sie die Details für Ihre Entscheidungsrichtlinie aus: Fügen Sie einen Namen hinzu und wählen Sie einen Katalog.

   >[!NOTE]
   >
   >Derzeit ist nur der Standardkatalog für **[!UICONTROL Angebote]** verfügbar.

1. Wählen Sie die Anzahl der Elemente, die zurückgegeben werden sollen. Wenn Sie beispielsweise „2“ auswählen, werden die zwei am besten geeigneten Angebote für die aktuelle Konfiguration angezeigt. Klicken Sie auf **[!UICONTROL Weiter]**.

   ![](assets/decision-code-based-details.png)

### Auswählen von Elementen und Auswahlstrategien {#select}

Im Abschnitt **[!UICONTROL Strategiesequenz]** können Sie die Entscheidungselemente und Auswahlstrategien auswählen, die der Entscheidungsrichtlinie angezeigt werden sollen.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Hinzufügen]** und wählen Sie dann den Typ des Objekts aus, das in die Richtlinie aufgenommen werden soll:

   * **[!UICONTROL Auswahlstrategie]**: Fügen Sie eine oder mehrere Auswahlstrategien hinzu. Entscheidungsstrategien nutzen Sammlungen, die mit Eignungsbegrenzungen verknüpft sind, und Rangmethoden, um die anzuzeigenden Elemente zu bestimmen. Sie können eine vorhandene Auswahlstrategie auswählen oder mithilfe der Schaltfläche **[!UICONTROL Auswahlstrategie erstellen]** eine neue erstellen.[Erfahren Sie, wie Sie Auswahlstrategien erstellen](selection-strategies.md)

   * **[!UICONTROL Entscheidungselement]**: Fügen Sie einzelne Entscheidungselemente hinzu, die angezeigt werden sollen, ohne eine Auswahlstrategie durchlaufen zu müssen. Sie können jeweils nur ein Entscheidungselement auswählen. Alle für das Element festgelegten Eignungsbegrenzungen gelten.

   ![](assets/decision-code-based-strategy-sequence.png)

   >[!NOTE]
   >
   >Es ist mindestens ein Entscheidungselement oder eine Strategie erforderlich. Es können nicht mehr als 10 Strategien hinzugefügt werden.

1. Beim Hinzufügen mehrerer Entscheidungselemente und/oder Strategien werden diese in einer bestimmten Reihenfolge bewertet. Das erste Objekt, das der Sequenz hinzugefügt wurde, wird zuerst ausgewertet usw.     Um die Standardreihenfolge zu ändern, können Sie die Objekte und/oder Gruppen per Drag-and-Drop verschieben, um sie nach Bedarf neu anzuordnen. [Erfahren Sie mehr über die Reihenfolge der Entscheidungsrichtlinienauswertung](#evaluation-order)

### Verwalten von Auswertungsreihenfolgen in Entscheidungsrichtlinien {#evaluation-order}

Nachdem Sie Ihrer Richtlinie Entscheidungselemente und Auswahlstrategien hinzugefügt haben, können Sie ihre Reihenfolge so festlegen, dass ihre Auswertungsreihenfolge festgelegt wird, und Auswahlstrategien kombinieren, um sie gemeinsam zu bewerten.

Die **sequenzielle Reihenfolge**, in der Elemente und Strategien ausgewertet werden, wird mit Zahlen links neben jedem Objekt oder jeder Gruppe von Objekten angegeben. Um die Position einer Auswahlstrategie (oder einer Gruppe von Strategien) innerhalb der Sequenz zu verschieben, ziehen Sie sie an eine andere Position.

>[!NOTE]
>
>Es können nur Auswahlstrategien in eine Sequenz gezogen und dort abgelegt werden. Um die Position eines Entscheidungselements zu ändern, müssen Sie es entfernen und mithilfe der Schaltfläche **[!UICONTROL Hinzufügen]** wieder hinzufügen, nachdem Sie die anderen Elemente hinzugefügt haben, die zuvor ausgewertet werden sollen.

![](assets/decision-code-based-strategy-groups.png)

Sie können auch **mehrere Auswahlstrategien in Gruppen kombinieren, sodass sie zusammen und nicht getrennt ausgewertet werden.** Klicken Sie dazu unter einer Auswahlstrategie auf die Schaltfläche **`+`** , um sie mit einer anderen zu kombinieren. Sie können auch eine Auswahlstrategie per Drag-and-Drop auf eine andere ziehen, um die beiden Strategien in einer Gruppe zu gruppieren.

>[!NOTE]
>
>Entscheidungselemente können nicht mit anderen Elementen oder Auswahlstrategien gruppiert werden.

Mehrere Strategien und ihre Gruppierung bestimmen die Priorität der Strategien und die Rangfolge der geeigneten Angebote. Die erste Strategie hat die höchste Priorität, und die Strategien, die in derselben Gruppe zusammengefasst sind, haben dieselbe Priorität.

Sie haben beispielsweise zwei Sammlungen – eine mit Strategie A und eine mit Strategie B. Die Anfrage sieht die Rücksendung von zwei Entscheidungselementen vor. Angenommen, es gibt zwei geeignete Angebote nach Strategie A und drei geeignete Angebote nach Strategie B.

* Wenn die beiden Strategien **nicht kombiniert** und/oder in sequenzieller Reihenfolge (1 und 2) sind, werden die beiden geeignetsten Angebote nach der ersten Strategie in der ersten Zeile zurückgegeben. Gibt es für die erste Strategie keine zwei geeigneten Angebote, geht die Entscheidungs-Engine zur nächsten Strategie in der Reihenfolge über, um so viele Angebote zu finden, wie noch benötigt werden, und gibt schließlich bei Bedarf einen Fallback zurück.

  ![](assets/decision-code-based-consecutive-strategies.png)

* Werden die beiden Sammlungen **gleichzeitig ausgewertet**, da es zwei geeignete Angebote für Strategie A und drei geeignete Angebote für Strategie B gibt, werden alle fünf Angebote anhand des von den jeweiligen Ranking-Methoden ermittelten Wertes zusammengefasst. Es werden zwei Angebote angefordert, so dass von diesen fünf Angeboten die beiden geeignetsten zurückgegeben werden.

  ![](assets/decision-code-based-combined-strategies.png)

+++ **Beispiel mit mehreren Strategien**

Betrachten wir nun ein Beispiel, bei dem mehrere Strategien in verschiedene Gruppen unterteilt sind.

Sie haben drei Strategien definiert. Strategie 1 und 2 befinden sich beide in Gruppe 1, während Strategie 3 unabhängig ist (Gruppe 2).

Die geeigneten Angebote für jede Strategie und ihre Priorität (die bei der Auswertung der Ranglistenfunktion verwendet wird) sind wie folgt:

* Gruppe 1:
   * Strategie 1 – (Angebot 1, Angebot 2, Angebot 3) – Priorität 1
   * Strategie 2 – (Angebot 3, Angebot 4, Angebot 5) – Priorität 1

* Gruppe 2:
   * Strategie 3 – (Angebot 5, Angebot 6) – Priorität 0

Die Angebote mit der höchsten Priorität werden zuerst ausgewertet und zur Rangfolgeliste der Angebote hinzugefügt.

**Iteration 1:**

Angebote mit Strategie 1 und 2 werden gemeinsam ausgewertet (Angebot 1, Angebot 2, Angebot 3, Angebot 4, Angebot 5). Nehmen wir an, das Ergebnis lautet:

Angebot 1 – 10
Angebot 2 – 20
Angebot 3 – 30 aus Strategie 1, 45 aus Strategie 2. Der höchste Wert von beiden wird berücksichtigt, also 45.
Angebot 4 - 40
Angebot 5 - 50

Die Rangfolge der Angebote lautet nun wie folgt: Angebot 5, Angebot 3, Angebot 4, Angebot 2, Angebot 1.

**Iteration 2:**

Angebote mit Strategie 3 werden ausgewertet (Angebot 5, Angebot 6). Nehmen wir an, das Ergebnis lautet:

* Angebot 5 - wird nicht ausgewertet, da es bereits im obigen Ergebnis enthalten ist.
* Angebot 6 - 60

Die Rangfolge der Angebote ist nun wie folgt: Angebot 5, Angebot 3, Angebot 4, Angebot 2, Angebot 1, Angebot 6.

+++

### Fallback-Angebote hinzufügen {#fallback}

Nachdem Sie Entscheidungselemente und/oder Auswahlstrategien ausgewählt haben, können Sie Fallback-Angebote hinzufügen, die Benutzern angezeigt werden, wenn keines der oben genannten Elemente oder Auswahlstrategien qualifiziert ist.

![](assets/decision-code-based-strategy-fallback.png)

Es können beliebige Elemente aus der Liste ausgewählt werden, die alle in der aktuellen Sandbox erstellten Entscheidungselemente anzeigt. Wenn keine Auswahlstrategie qualifiziert ist, wird den Benutzenden unabhängig von den Datumsangaben und den auf das ausgewählte Element angewendeten Eignungsbegrenzungen der Fallback angezeigt<!--nor frequency capping when available - TO CLARIFY-->.

>[!NOTE]
>
>Ein Fallback ist optional. Wenn kein Fallback ausgewählt ist und keine Strategie qualifiziert ist, wird nichts von [!DNL Journey Optimizer] angezeigt. Sie können die Anzahl der Elemente addieren, die die Entscheidungsrichtlinie anfordert. Dadurch wird eine bestimmte Anzahl von Artikeln garantiert, die bei Bedarf für den Anwendungsfall zurückgegeben werden.

Wenn Ihre Entscheidungsrichtlinie fertig ist, speichern Sie sie und klicken Sie auf **[!UICONTROL Erstellen]**. Nachdem die Entscheidungsrichtlinie erstellt wurde, können die Entscheidungsattribute im Code-basierten Erlebnisinhalt verwendet werden. [Weitere Informationen](#use-decision-policy)

![](assets/decision-code-based-decision-added.png)

## Entscheidungsrichtlinie im Code-Editor verwenden {#use-decision-policy}

Nach der Erstellung kann die Entscheidungsrichtlinie im [Personalisierungseditor](../code-based/create-code-based.md#edit-code) verwendet werden. Gehen Sie dazu wie folgt vor.

>[!NOTE]
>
>Ein Code-basiertes Erlebnis nutzt den Personalisierungseditor von [!DNL Journey Optimizer] mit allen Personalisierungs- und Bearbeitungsfunktionen. [Weitere Informationen](../personalization/personalization-build-expressions.md)

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Richtlinie einfügen]**. Der Code, der der Entscheidungsrichtlinie entspricht, wird hinzugefügt.

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >Diese Sequenz wird so oft wiederholt, wie Sie die Entscheidungsrichtlinie zurückgeben möchten. Wenn Sie beispielsweise bei der [Erstellung der Entscheidung](#add-decision) 2 Elemente zurückgeben möchten, wird dieselbe Sequenz zweimal wiederholt.

1. Jetzt können Sie alle gewünschten Entscheidungsattribute zu diesem Code hinzufügen.  Die verfügbaren Attribute werden im Schema des Katalogs **[!UICONTROL Angebote]** gespeichert. Benutzerdefinierte Attribute werden im Ordner **`_<imsOrg`>** und Standardattribute im Ordner **`_experience`** gespeichert. [Weitere Informationen zum Schema des Angebotskatalogs](catalogs.md)

   ![](assets/decision-code-based-decision-attributes.png)

   >[!NOTE]
   >
   >Für das Tracking von Entscheidungsrichtlinienelementen muss das Attribut `trackingToken`wie folgt für den Inhalt der Entscheidungsrichtlinie hinzugefügt werden:
   >`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

1. Klicken Sie auf den gewünschten Ordner, um ihn zu erweitern. Platzieren Sie den Cursor an der gewünschten Position und klicken Sie auf das Symbol „+“ neben dem Attribut, das Sie hinzufügen möchten. Sie können beliebig viele Attribute zum Code hinzufügen.

   ![](assets/decision-code-based-add-decision-attributes.png)

1. Sie können auch jedes beliebige Attribut hinzufügen, das im Personalisierungseditor verfügbar ist, z. B. Profilattribute.

   ![](assets/decision-code-based-decision-profile-attribute.png)

## Reporting in Customer Journey Analytics {#cja}

Wenn Sie mit Customer Journey Analytics arbeiten, können Sie benutzerdefinierte Reporting-Dashboards für Ihre Code-basierten Kampagnen erstellen, die Erlebnis-Entscheidung nutzen.

Die wichtigsten Schritte sind unten aufgeführt. Ausführliche Informationen über die Arbeit mit Customer Journey Analytics finden Sie in der [Customer Journey Analytics-Dokumentation](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Erstellen und konfigurieren Sie eine **Verbindung** in Customer Journey Analytics. So können Sie eine Verbindung zu dem Datensatz herstellen, für den Sie Berichte erstellen möchten. [Erfahren Sie, wie Sie eine Verbindung herstellen](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Erstellen Sie eine **Datenansicht** und verknüpfen Sie sie mit der zuvor erstellten Verbindung. Wählen Sie auf der Registerkarte **[!UICONTROL Komponenten]** die entsprechenden Schemafelder aus, die im Reporting angezeigt werden sollen. Stellen Sie sicher, dass Sie für die Erlebnis-Entscheidung die Felder **propositioninteract** und **propositiondisplay** einschließen. [Erfahren Sie, wie Sie Datenansichten erstellen und konfigurieren können](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Kombinieren Sie Datenkomponenten, Tabellen und Visualisierungen in **Workspace-Projekten**, um Berichte für Ihre Code-basierte Kampagne zu erstellen und gemeinsam zu nutzen.[Erfahren Sie, wie Sie Workspace-Projekte erstellen können](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
