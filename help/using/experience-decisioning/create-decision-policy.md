---
title: Erstellen von Entscheidungsrichtlinien
description: Informationen dazu, wie Sie Entscheidungsrichtlinien erstellen
feature: Decisioning
topic: Integrations
role: User
level: Experienced
version: Journey Orchestration
source-git-commit: 2dfc9c2db5af1b9b74f7405a68e85563f633a54f
workflow-type: tm+mt
source-wordcount: '2108'
ht-degree: 68%

---


# Erstellen von Entscheidungsrichtlinien {#create-decision}

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

Um Ihren Kundinnen und Kunden das beste dynamische Angebot und Erlebnis zu bieten, fügen Sie Ihrem Inhalt in einer Kampagne oder auf einer Journey eine Entscheidungsrichtlinie hinzu. Konfigurieren Sie dann die zurückzugebenden Elemente und die zu verwendende Auswahlstrategie. Gehen Sie dazu wie folgt vor:

1. [Hinzufügen einer Entscheidungsrichtlinie](#add)
1. [Entscheidungsrichtlinie konfigurieren](#configure) - Fügen Sie einen Namen hinzu und geben Sie die Anzahl der Elemente an, die für den E-Mail-Kanal zurückgegeben werden sollen.
1. [Einrichten einer Strategiesequenz](#strategy): Wählen Sie die Elemente aus, die mit der Entscheidungsrichtlinie zurückgegeben werden sollen.
1. [Auswählen von Fallback-Angeboten](#fallback) (optional): Wählen Sie Elemente aus, die angezeigt werden sollen, wenn keine Elemente oder Auswahlstrategien qualifiziert sind.
1. [Überprüfen und Speichern](#review) der Auswahlstrategie
1. [Platzierung zuweisen](#placement) (E-Mail-Kanal)

>[!AVAILABILITY]
>
>Entscheidungsrichtlinien stehen allen Kunden für die Kanäle **Code-basiertes Erlebnis**, **Push-Benachrichtigung** und SMS zur Verfügung.
>
>Die Entscheidungsfindung für den E-Mail-Kanal ist in begrenzter Verfügbarkeit verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

## Hinzufügen einer Entscheidungsrichtlinie {#add}

Um eine Entscheidungsrichtlinie zu Ihrer Nachricht hinzuzufügen, öffnen Sie eine Journey oder Kampagne und wählen Sie eine [Kanalaktion](../building-journeys/journeys-message.md) aus.

Bearbeiten Sie den Inhalt Ihrer Nachricht und navigieren Sie zu den folgenden Registerkarten, um weitere Informationen zum Hinzufügen der Entscheidungsrichtlinie basierend auf dem ausgewählten Kanal zu erhalten.

>[!BEGINTABS]

>[!TAB Code-basiertes Erlebnis]

Bei Code-basierten Erlebnissen können Sie eine neue Entscheidungsrichtlinie entweder mit dem **Code-Editor** oder dem Menü **Decisioning** im Eigenschaftenbereich hinzufügen.

+++Hinzufügen einer Entscheidungsrichtlinie aus dem Code-Editor

1. Öffnen Sie den Code-Editor mithilfe der Schaltfläche **[!UICONTROL Code bearbeiten]**.

1. Navigieren Sie zum Menü **[!UICONTROL Entscheidungsrichtlinie]** und klicken Sie auf die Schaltfläche **[!UICONTROL Entscheidungsrichtlinie hinzufügen]**.

   ![](assets/decision-policy-add-code-editor.png)

+++

+++Hinzufügen einer Entscheidungsrichtlinie über das Menü Entscheidungsfindung .

1. Klicken Sie auf das Symbol ![](assets/do-no-localize/decisioning-icon.png) im Bereich Eigenschaften , um auf das Menü **[!UICONTROL Entscheidung]** zuzugreifen.

1. Klicken Sie auf die **[!UICONTROL Entscheidungsrichtlinie hinzufügen]**.

   ![](assets/decision-policy-add-code.png)

+++

>[!TAB E-Mail]

1. Schalten Sie die Option **[!UICONTROL Entscheidungsfindung aktivieren]** um.

   ![](assets/decision-policy-enable.png)

   >[!IMPORTANT]
   >
   >Durch Aktivierung der Entscheidungsfindung werden vorhandene E-Mail-Inhalte gelöscht. Wenn Sie Ihre E-Mail bereits entworfen haben, stellen Sie also sicher, dass Sie Ihren Inhalt zuvor als Vorlage speichern.

1. Fügen Sie eine neue Entscheidungsrichtlinie hinzu, indem Sie entweder den **Personalisierungseditor** oder das Menü **Entscheidung** verwenden, das im E-Mail-Designer verfügbar ist.

   +++Hinzufügen einer Entscheidungsrichtlinie aus dem Personalization-Editor

   1. Öffnen Sie den Personalisierungseditor mithilfe des ![](assets/do-no-localize/editor-icon.svg)-Symbols im Feld Betreffzeile oder in einem beliebigen Feld im E-Mail-Textkörper, in dem Sie eine Personalisierung hinzufügen können.

   1. Navigieren Sie zum Menü **[!UICONTROL Entscheidungsrichtlinien]** und klicken Sie auf die Schaltfläche **[!UICONTROL Entscheidungsrichtlinie hinzufügen]**.

      ![](assets/decision-policy-add-email-editor.png)

   +++

   +++Hinzufügen einer Entscheidungsrichtlinie über das Menü Entscheidungsfindung .

   1. Öffnen Sie die E-Mail-Designer und wählen Sie eine beliebige Komponente in der E-Mail-Struktur aus.

   1. Klicken Sie auf das Symbol ![](assets/do-no-localize/decisioning-icon.png) im Bereich Eigenschaften , um auf das Menü **[!UICONTROL Entscheidung]** zuzugreifen.

   1. Klicken Sie auf **[!UICONTROL Schaltfläche „Neue Richtlinie hinzufügen]**.

      ![](assets/decision-policy-add-email-add.png)

   >[!NOTE]
   >
   >Wählen Sie **[!UICONTROL Entscheidungsausgabe wiederverwenden]** aus, um eine Entscheidungsrichtlinie wiederzuverwenden, die bereits in dieser E-Mail erstellt wurde.

>[!TAB SMS]

Für SMS können Sie eine neue Entscheidungsrichtlinie entweder über den **Personalisierungseditor** oder das Menü **Decisioning** im Eigenschaftenbereich hinzufügen.

+++Hinzufügen einer Entscheidungsrichtlinie aus dem Personalisierungseditor

1. Öffnen Sie den Personalisierungseditor mithilfe des ![](assets/do-no-localize/editor-icon.svg).
1. Navigieren Sie zum Menü **[!UICONTROL Entscheidungsrichtlinien]** und klicken Sie auf die Schaltfläche **[!UICONTROL Entscheidungsrichtlinie hinzufügen]**.

   ![](assets/decision-policy-add-sms-editor.png)

+++

+++Hinzufügen einer Entscheidungsrichtlinie über das Menü Entscheidungsfindung .

1. Klicken Sie auf das Symbol ![](assets/do-no-localize/decisioning-icon.png) im Bereich Eigenschaften , um auf das Menü **[!UICONTROL Entscheidung]** zuzugreifen.

1. Klicken Sie auf die **[!UICONTROL Entscheidungsrichtlinie hinzufügen]**.

   ![](assets/decision-policy-add-sms.png)

>[!TAB Push-Benachrichtigung]

Für Push-Benachrichtigungen können Sie eine neue Entscheidungsrichtlinie entweder über den **Personalisierungseditor** oder das Menü **Entscheidungsfindung** im Eigenschaftenbereich hinzufügen.

+++Hinzufügen einer Entscheidungsrichtlinie aus dem Personalisierungseditor

1. Öffnen Sie den Personalisierungseditor mithilfe des ![](assets/do-no-localize/editor-icon.svg).
1. Navigieren Sie zum Menü **[!UICONTROL Entscheidungsrichtlinien]** und klicken Sie auf die Schaltfläche **[!UICONTROL Entscheidungsrichtlinie hinzufügen]**.

   ![](assets/decision-policy-add-push.png)

+++

+++Hinzufügen einer Entscheidungsrichtlinie über das Menü Entscheidungsfindung .

1. Klicken Sie auf das Symbol ![](assets/do-no-localize/decisioning-icon.png) im Bereich Eigenschaften , um auf das Menü **[!UICONTROL Entscheidung]** zuzugreifen.

1. Klicken Sie auf die **[!UICONTROL Entscheidungsrichtlinie hinzufügen]**.

   ![](assets/decision-policy-add-push-menu.png)

>[!IMPORTANT]
>
>Für Experience Decisioning mit Push-Benachrichtigungen ist eine bestimmte Version der Mobile SDK erforderlich. Bevor Sie diese Funktion implementieren, überprüfen Sie die [Versionshinweise](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"}, um die erforderliche Version zu identifizieren und sicherzustellen, dass Sie das Upgrade entsprechend durchgeführt haben. Sie können auch alle verfügbaren SDK-Versionen für Ihre Plattform in [diesem Abschnitt](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"} anzeigen.

>[!ENDTABS]

## Konfigurieren der Entscheidungsrichtlinie {#configure}

Nachdem Sie eine neue Entscheidungsrichtlinie zu Ihrem Inhalt hinzugefügt haben, wird der Konfigurationsbildschirm für Entscheidungsrichtlinien geöffnet. Führen Sie die folgenden Schritte aus, um die Entscheidungsrichtlinie zu konfigurieren:

1. Geben Sie einen Namen für die Entscheidungsrichtlinie an und wählen Sie einen Katalog aus (derzeit beschränkt auf den Standardkatalog **[!UICONTROL Angebote]**).

   ![](assets/decision-code-based-details.png)

1. Im Feld **[!UICONTROL Anzahl der Elemente]** können Sie die Anzahl der Entscheidungselemente definieren, die mit der Entscheidungsrichtlinie zurückgegeben werden sollen. Wenn Sie beispielsweise „2“ auswählen, werden die zwei am besten geeigneten Angebote für die aktuelle Konfiguration angezeigt.

   >[!NOTE]
   >
   >Diese Option ist nur für die Kanäle E-Mail und Code-basiertes Erlebnis verfügbar. Für alle anderen Kanäle kann pro Aktion nur ein Entscheidungselement zurückgegeben werden.

   Um mehrere Elemente für den E-Mail-Kanal zurückzugeben, müssen Sie die Entscheidungsrichtlinie innerhalb einer **[!UICONTROL Wiederholungsraster]**-Komponente hinzufügen. Erweitern Sie den folgenden Abschnitt, um weitere Informationen zu erhalten:

   +++Zurückgeben mehrerer Entscheidungselemente in E-Mails

   1. Ziehen Sie eine Komponente vom Typ **[!UICONTROL Wiederholungsraster]** in Ihre E-Mail und konfigurieren Sie sie wie gewünscht mithilfe des Bereichs **[!UICONTROL Einstellungen]**.

      ![](assets/decision-policy-repeat.png)

   1. Klicken Sie auf das Symbol **[!UICONTROL Entscheidungsfindung]** auf der Symbolleiste der Arbeitsfläche oder öffnen Sie den Bereich **[!UICONTROL Entscheidungsfindung]** und wählen Sie **[!UICONTROL Entscheidungsrichtlinie hinzufügen]** aus.

   1. Geben Sie im Feld **[!UICONTROL Anzahl der Elemente]** die Anzahl der zurückzugebenden Elemente ein und konfigurieren Sie dann die Entscheidungsrichtlinie wie unten beschrieben. Die maximale Anzahl von Elementen, die Sie auswählen können, ist durch die Anzahl der Kacheln begrenzt, die in der Komponente **[!UICONTROL Wiederholungsraster]** definiert sind.

   ![](assets/decision-policy-repeat-number.png)

   +++

1. Klicken Sie auf **[!UICONTROL Weiter]**.

## Einrichten einer Strategiesequenz {#strategy}

Im Bereich **[!UICONTROL Strategiesequenz]** können Sie die Entscheidungselemente und Auswahlstrategien auswählen, die mit der Entscheidungsrichtlinie angezeigt werden sollen.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Hinzufügen]** und wählen Sie anschließend den Objekttyp aus, der in die Richtlinie aufgenommen werden soll:

   ![](assets/decision-code-based-strategy-sequence.png)

   * **[!UICONTROL Auswahlstrategie]**: Entscheidungsstrategien nutzen Sammlungen, die mit Eignungsbegrenzungen verknüpft sind, und Rangfolgemethoden, um die anzuzeigenden Elemente zu bestimmen. Sie können eine vorhandene Auswahlstrategie auswählen oder mithilfe der Schaltfläche **[!UICONTROL Auswahlstrategie erstellen]** eine neue erstellen. [Informationen zum Erstellen von Auswahlstrategien](selection-strategies.md)

   * **[!UICONTROL Entscheidungselement]**: Wählen Sie einzelne Entscheidungselemente aus, ohne eine Auswahlstrategie durchlaufen zu müssen. Sie können jeweils nur ein Entscheidungselement auswählen. Es werden alle für das Element festgelegten Eignungsbegrenzungen angewendet.

   >[!NOTE]
   >
   >Eine Entscheidungsrichtlinie unterstützt bis zu 10 Auswahlstrategien und Entscheidungselemente zusammen. [Weitere Informationen zu den Leitlinien und Einschränkungen für die Entscheidungsfindung](gs-experience-decisioning.md#guardrails)

1. Wenn mehrere Entscheidungselemente und/oder Strategien hinzugefügt werden, werden diese in einer bestimmten Reihenfolge ausgewertet. Das erste Objekt, das der Sequenz hinzugefügt wurde, wird zuerst ausgewertet und die Auswertung wird in dieser Reihenfolge fortgeführt. Die Objekte und/oder Gruppen können nach Bedarf per Drag-and-Drop verschoben werden, um die Standardsequenz zu ändern.  Erweitern Sie den folgenden Abschnitt, um weitere Informationen zu erhalten.

   +++Verwalten der Auswertungsreihenfolge in einer Entscheidungsrichtlinie

   Sobald Sie Entscheidungselemente und Auswahlstrategien zu Ihrer Richtlinie hinzugefügt haben, können Sie ihre Reihenfolge anpassen, um die Auswertungsreihenfolge festzulegen, und Auswahlstrategien miteinander kombinieren, um sie gemeinsam auszuwerten.

   Die **sequenzielle Reihenfolge**, in der Elemente und Strategien ausgewertet werden, wird mit Zahlen links neben jedem Objekt oder jeder Objektgruppe angegeben. Um die Position einer Auswahlstrategie (oder einer Gruppe von Strategien) innerhalb der Sequenz zu verschieben, ziehen Sie sie per Drag-and-Drop an eine andere Position.

   ![](assets/decision-code-based-strategy-groups.png)

   >[!NOTE]
   >
   >Nur Auswahlstrategien können per Drag-and-Drop innerhalb einer Sequenz verschoben werden. Um die Position eines Entscheidungselements zu ändern, müssen Sie es entfernen und mithilfe der Schaltfläche **[!UICONTROL Hinzufügen]** wieder hinzufügen, nachdem Sie die anderen Elemente hinzugefügt haben, die vorher ausgewertet werden sollen.

   Sie können auch mehrere Auswahlstrategien in Gruppen **kombinieren**, sodass sie zusammen und nicht getrennt ausgewertet werden. Klicken Sie dazu unter einer Auswahlstrategie auf die Schaltfläche **`+`**, um sie mit einer anderen Strategie zu kombinieren. Sie können eine Auswahlstrategie auch per Drag-and-Drop auf eine andere ziehen, um die beiden Strategien zu einer Gruppe zusammenzuführen.

   >[!NOTE]
   >
   >Entscheidungselemente können nicht mit anderen Elementen oder Auswahlstrategien gruppiert werden.

   Mehrere Strategien und ihre Gruppierung bestimmen die Priorität der Strategien und die Rangfolge der geeigneten Angebote. Die erste Strategie hat die höchste Priorität, und die Strategien, die in derselben Gruppe zusammengefasst sind, haben dieselbe Priorität.

   Sie haben beispielsweise zwei Sammlungen – eine mit Strategie A und eine mit Strategie B. Die Anfrage sieht die Rücksendung von zwei Entscheidungselementen vor. Angenommen, es gibt zwei geeignete Angebote nach Strategie A und drei geeignete Angebote nach Strategie B.

   * Wenn die beiden Strategien **nicht kombiniert** und/oder in sequenzieller Reihenfolge (1 und 2) sind, werden die beiden geeignetsten Angebote nach der ersten Strategie in der ersten Zeile zurückgegeben. Gibt es für die erste Strategie keine zwei geeigneten Angebote, geht die Entscheidungs-Engine zur nächsten Strategie in der Reihenfolge über, um so viele Angebote zu finden, wie noch benötigt werden, und gibt schließlich bei Bedarf einen Fallback zurück.

     ![](assets/decision-code-based-consecutive-strategies.png)

   * Werden die beiden Sammlungen **gleichzeitig ausgewertet**, da es zwei geeignete Angebote für Strategie A und drei geeignete Angebote für Strategie B gibt, werden alle fünf Angebote anhand des von den jeweiligen Ranking-Methoden ermittelten Wertes zusammengefasst. Es werden zwei Angebote angefordert, so dass von diesen fünf Angeboten die beiden geeignetsten zurückgegeben werden.

     ![](assets/decision-code-based-combined-strategies.png)

   **Beispiel mit mehreren Strategien**

   Betrachten wir nun ein Beispiel, bei dem mehrere Strategien in verschiedene Gruppen unterteilt sind. Sie haben drei Strategien definiert. Strategie 1 und 2 befinden sich beide in Gruppe 1, während Strategie 3 unabhängig ist (Gruppe 2). Die geeigneten Angebote für jede Strategie und ihre Priorität (die bei der Auswertung der Ranglistenfunktion verwendet wird) sind wie folgt:

   * Gruppe 1:
      * Strategie 1 – (Angebot 1, Angebot 2, Angebot 3) – Priorität 1
      * Strategie 2 – (Angebot 3, Angebot 4, Angebot 5) – Priorität 1

   * Gruppe 2:
      * Strategie 3 – (Angebot 5, Angebot 6) – Priorität 0

   Die Angebote mit der höchsten Priorität werden zuerst ausgewertet und zur Rangfolgeliste der Angebote hinzugefügt.

   * **Iteration 1:**

     Angebote mit Strategie 1 und 2 werden gemeinsam ausgewertet (Angebot 1, Angebot 2, Angebot 3, Angebot 4, Angebot 5). Nehmen wir an, das Ergebnis lautet:

     Angebot 1 – 10
Angebot 2 – 20
Angebot 3 – 30 aus Strategie 1, 45 aus Strategie 2. Der höchste Wert von beiden wird berücksichtigt, also 45.
Angebot 4 - 40
Angebot 5 - 50

     Die Rangfolge der Angebote lautet nun wie folgt: Angebot 5, Angebot 3, Angebot 4, Angebot 2, Angebot 1.

   * **Iteration 2:**

     Angebote mit Strategie 3 werden ausgewertet (Angebot 5, Angebot 6). Nehmen wir an, das Ergebnis lautet:

      * Angebot 5 - wird nicht ausgewertet, da es bereits im obigen Ergebnis enthalten ist.
      * Angebot 6 - 60

     Die Rangfolge der Angebote ist nun wie folgt: Angebot 5, Angebot 3, Angebot 4, Angebot 2, Angebot 1, Angebot 6.

   +++

1. Wenn Ihre Auswahlstrategie fertig ist, klicken Sie auf **[!UICONTROL Weiter]**.

## Hinzufügen von Fallback-Angeboten {#fallback}

Sobald Sie Entscheidungselemente und/oder Auswahlstrategien ausgewählt haben, können Sie Fallback-Angebote hinzufügen, die angezeigt werden, wenn keines der oben genannten Elemente oder keine der oben genannten Auswahlstrategien qualifiziert ist.

Es können beliebige Elemente aus der Liste ausgewählt werden, die alle in der aktuellen Sandbox erstellten Entscheidungselemente anzeigt. Wenn keine Auswahlstrategie qualifiziert ist, wird den Benutzenden unabhängig von den Datumsangaben und den auf das ausgewählte Element angewendeten Eignungsbegrenzungen der Fallback angezeigt<!--nor frequency capping when available - TO CLARIFY-->.

![](assets/decision-code-based-strategy-fallback.png)

>[!NOTE]
> Fallbacks sind optional. Es können maximal so viele Elemente ausgewählt werden, wie angefordert wurden. Wenn es keine geeigneten gibt und kein Fallback festgelegt ist, wird nichts angezeigt.

## Überprüfen und Speichern der Entscheidungsrichtlinie {#review}

Nachdem Sie eine Auswahlstrategie konfiguriert und Fallback-Angebote hinzugefügt haben, klicken Sie auf **[!UICONTROL Weiter]**, um Ihre Entscheidungsrichtlinie zu überprüfen und zu speichern, und dann auf **[!UICONTROL Erstellen]**, um die Richtlinienerstellung zu bestätigen.

>[!IMPORTANT]
>
>Nachdem eine Entscheidungsrichtlinie erstellt wurde, kann es bis zu 15 Minuten dauern, bis Änderungen an ihr in allen Datenregionen propagiert werden, und bis zu 30 Minuten für Kanada. Dazu gehören Änderungen, z. B. das Hinzufügen eines neuen Entscheidungselements zu einer Sammlung, das Ändern einer Regel in einem Element, das Ändern des Elementinhalts oder das Aktualisieren einer Formel.

Sie können eine Entscheidungsrichtlinie jederzeit mithilfe der Schaltfläche mit den Auslassungspunkten im Personalisierungseditor oder im Menü **[!UICONTROL Entscheidungsfindung]** im Bereich der Komponenteneigenschaften bearbeiten oder löschen.

>[!BEGINTABS]

>[!TAB Bearbeiten oder Löschen einer Richtlinie im Personalisierungseditor]

![](assets/decision-policy-edit.png)

>[!TAB Bearbeiten oder Löschen einer Richtlinie aus dem Menü Entscheidung]

![](assets/decision-policy-edit-properties.png)

>[!ENDTABS]

## Zuweisen einer Platzierung (E-Mail) {#placement}

Für E-Mails müssen Sie eine Platzierung für die Komponente definieren, die mit der Entscheidungsrichtlinie verknüpft ist. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Entscheidungsfindung]** im Bereich mit Komponenteneigenschaften und wählen Sie **[!UICONTROL Platzierung zuweisen]** aus. [Informationen zum Arbeiten mit Platzierungen](../experience-decisioning/placements.md)

![](assets/decision-policy-rail.png)

## Nächste Schritte {#next-steps}

Nachdem Sie nun wissen, wie Sie eine Entscheidungsrichtlinie erstellen, können Sie sie in [!DNL Journey Optimizer]-Kanälen verwenden, um Angebote zu unterbreiten.

➡️ [Informationen zum Verwenden von Entscheidungsrichtlinien in Nachrichten](../experience-decisioning/use-decision-policy.md)
