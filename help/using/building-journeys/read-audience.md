---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden einer Zielgruppe in einer Journey
description: Erfahren Sie, wie Sie eine Zielgruppe in einer Journey verwenden
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: Aktivität, Journey, Lesen, Zielgruppe, Plattform
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1342'
ht-degree: 49%

---

# Verwenden einer Zielgruppe in einer Journey {#segment-trigger-activity}

## Hinzufügen der Aktivität Audience lesen {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="Aktivität &quot;Audience lesen&quot;"
>abstract="Mit der Aktivität Audience lesen können Sie alle Kontakte, die zu einer Adobe Experience Platform-Audience gehören, in eine Journey eintreten lassen. Der Eintritt in eine Journey kann entweder einmalig oder regelmäßig erfolgen."

Verwenden Sie die **Audience lesen** -Aktivität, um alle Kontakte einer Audience in die Journey einzubinden. Der Eintritt in eine Journey kann entweder einmalig oder regelmäßig erfolgen.

Nehmen wir als Beispiel die Audience &quot;Luma app opens and Checkout&quot;, die in der [Erstellen von Zielgruppen](../audience/about-audiences.md) Anwendungsbeispiel. Mit der Aktivität Audience lesen können Sie alle Kontakte, die zu dieser Audience gehören, in eine Journey eintreten lassen und sie in individuelle Journey umwandeln, die alle Journey-Funktionen nutzen: Bedingungen, Timer, Ereignisse, Aktionen.

>[!NOTE]
>
>Bei Journey, die die Aktivität Audience lesen verwenden, gibt es eine maximale Anzahl von Journey, die exakt zur gleichen Zeit beginnen können. Weitere Zustellversuche werden vom System durchgeführt. Vermeiden Sie jedoch, dass mehr als fünf Journey (mit &quot;Audience lesen&quot;, geplant oder &quot;so bald wie möglich&quot; gestartet werden) exakt gleichzeitig beginnen, indem sie über einen bestimmten Zeitraum verteilt werden, z. B. zwischen 5 und 10 Minuten.
>
>Feldergruppen für Erlebnisereignisse können nicht in Journey verwendet werden, die mit der Aktivität Lesen der Zielgruppe, Zielgruppenqualifizierung oder Geschäftsereignis beginnen.

### Aktivität konfigurieren {#configuring-segment-trigger-activity}

Die Schritte zum Konfigurieren der Aktivität Audience lesen lauten wie folgt:

1. Entfalten Sie die **[!UICONTROL Orchestrierung]** Kategorie und legen Sie eine **[!UICONTROL Audience lesen]** -Aktivität in Ihre Arbeitsfläche.

   Die Aktivität muss als erster Schritt einer Journey positioniert werden.

1. Fügen Sie der Aktivität einen **[!UICONTROL Titel]** hinzu (optional).

1. Im **[!UICONTROL Zielgruppe]** auswählen, die Adobe Experience Platform-Audience auswählen, die die Journey eingeben soll, und klicken Sie dann auf **[!UICONTROL Speichern]**.

   Beachten Sie, dass Sie die in der Liste angezeigten Spalten anpassen und sortieren können.

   >[!NOTE]
   >
   >Nur Personen mit der **Realisiert** und **Bestehend** Der Beteiligungsstatus der Zielgruppe wird in die Journey aufgenommen. Weiterführende Informationen zur Audience-Evaluierung finden Sie im Abschnitt [Dokumentation zum Segmentierungsdienst](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=de#interpret-segment-results){target="_blank"}.

   ![](assets/read-segment-selection.png)

   Nachdem die Audience hinzugefügt wurde, wird die **[!UICONTROL Kopieren]** -Schaltfläche können Sie den Namen und die Kennung kopieren:

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

1. Wählen Sie im Feld **[!UICONTROL Namespace]** den Namespace aus, der zur Identifizierung der Kontakte verwendet werden soll. Standardmäßig ist das Feld mit dem zuletzt verwendeten Namespace vorausgefüllt. [Weitere Informationen über Namespaces](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Einzelpersonen, die zu einer Zielgruppe gehören, die nicht über die ausgewählte Identität (den ausgewählten Namespace) verfügt, können nicht in die Journey eintreten. Sie können nur einen personenbasierten Identity-Namespace auswählen. Wenn Sie einen Namespace für eine Suchtabelle definiert haben (z. B.: Produkt-ID-Namespace für eine Produktsuche), ist er nicht in der Dropdown-Liste **Namespace** verfügbar.

1. Legen Sie die **[!UICONTROL Einschränkungsrate]** -Feld zur Durchsatzbegrenzung der Aktivität Audience lesen hinzu.

   Dieser Wert wird in der Payload der Journey-Version gespeichert. Der Standardwert ist 5.000 Nachrichten pro Sekunde. Sie können diesen Wert zwischen 500 und 20.000 Nachrichten pro Sekunde variieren.

   >[!NOTE]
   >
   >Die Gesamteinschränkungsrate pro Sandbox ist auf 20.000 Nachrichten pro Sekunde festgelegt. Daher ergibt die Drosselungsrate aller gleichzeitig in derselben Sandbox ausgeführten Lesezielgruppen maximal 20.000 Nachrichten pro Sekunde. Sie können diese Begrenzung nicht ändern.

1. Die **[!UICONTROL Audience lesen]** -Aktivität können Sie den Zeitpunkt festlegen, zu dem die Audience an der Journey teilnehmen wird. Klicken Sie dazu auf den Link **[!UICONTROL Journey-Planung bearbeiten]**, um auf die Eigenschaften der Journey zuzugreifen, und konfigurieren Sie dann das Feld **[!UICONTROL Planungstyp]**.

   ![](assets/read-segment-schedule.png)

   Standardmäßig geben Zielgruppen die Journey ein **[!UICONTROL So bald wie möglich]**. Wenn Sie die Audience dazu bringen möchten, an einem bestimmten Datum/zu einer bestimmten Uhrzeit oder wiederholt in die Journey einzutreten, wählen Sie den gewünschten Wert aus der Liste aus.

   >[!NOTE]
   >
   >Beachten Sie Folgendes: **[!UICONTROL Zeitplan]** -Abschnitt ist nur verfügbar, wenn eine **[!UICONTROL Audience lesen]** -Aktivität wurde auf der Arbeitsfläche abgelegt.

   ![](assets/read-segment-schedule-list.png)

   **Inkrementelles Lesen** Option: wenn eine Journey mit einer wiederkehrenden **Audience lesen** zum ersten Mal ausgeführt wird, geben alle Profile der Audience die Journey ein. Mit dieser Option können Sie nach dem ersten Vorkommen nur die Kontakte auswählen, die seit der letzten Ausführung der Journey in die Audience eingestiegen sind.

   **Erneuten Eintritt bei Wiederholung erzwingen**: Mit dieser Option können Sie alle noch in der Journey vorhandenen Profile bei der nächsten Ausführung automatisch austreten lassen. Wenn Sie beispielsweise eine Wartezeit von 2 Tagen in dieser wiederkehrenden Journey haben, werden Profile immer auf die nächste Journey-Ausführung (also am darauffolgenden Tag) verschoben, unabhängig davon, ob sie sich in der Audience der nächsten Ausführung befinden oder nicht. Wenn die Lebensdauer Ihrer Profile in dieser Journey länger als die Häufigkeit der Wiederholungen sein kann, aktivieren Sie diese Option nicht. So stellen Sie sicher, dass die Profile ihre Journey abschließen können.

<!--

### Segment filters {#segment-filters}

[!CONTEXTUALHELP]
>id="jo_segment_filters"
>title="About segment filters"
>abstract="You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week."

You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week. Only the new VIP customers will be targeted. All the customers who were already part of the VIP segment before will be excluded.

To activate this mode, click the **Segment Filters** toggle. Two fields are displayed:

**Segment membership**: choose whether you want to listen to segment entrances or exits. 

**Lookback window**: define when you want to start to listen to entrances or exits. This lookback window is expressed in hours, starting from the moment the journey is triggered.  If you set this duration to 0, the journey will target all members of the segment. For recurring journeys, it will take into account all entrances/exits since the last time the journey was triggered.

-->

>[!NOTE]
>
>Journey mit einer Aufnahme Lesen der Audience wechseln 30 Tage nach der Journey-Ausführung in den Status Abgeschlossen . Bei geplanten Lesen von Zielgruppen ist dies 30 Tage nach der Ausführung des letzten Vorkommens der Fall.

### Testen und Veröffentlichen der Journey {#testing-publishing}

Die **[!UICONTROL Audience lesen]** -Aktivität ermöglicht Ihnen, die Journey entweder in einem Einzelprofil oder in 100 Testprofilen zu testen, die nach dem Zufallsprinzip unter den für die Audience qualifizierten Profilen ausgewählt werden.

Aktivieren Sie dazu den Testmodus und wählen Sie dann im linken Bereich die gewünschte Option aus.

![](assets/read-segment-test-mode.png)

Anschließend können Sie den Testmodus wie gewohnt konfigurieren und ausführen. [Erfahren Sie, wie Sie eine Journey testen](testing-the-journey.md).

Sobald der Test ausgeführt wird, können Sie mit der Schaltfläche Protokolle **[!UICONTROL anzeigen]** die Testergebnisse entsprechend der ausgewählten Testoption anzeigen:

* **[!UICONTROL Jeweils ein Einzelprofil]**: Die Testprotokolle zeigen dieselben Informationen an wie bei Verwendung des einheitlichen Testmodus. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](testing-the-journey.md#viewing_logs)

* **[!UICONTROL Bis zu 100 Profile gleichzeitig]**: Mithilfe der Testprotokolle können Sie den Fortschritt des Zielgruppenexports aus Adobe Experience Platform sowie den individuellen Fortschritt aller Personen, die in die Journey eingestiegen sind, verfolgen.

  Beachten Sie, dass beim Testen der Journey mit bis zu 100 Profilen auf einmal der Fortschritt der einzelnen in der Journey enthaltenen Kontakte nicht über den visuellen Verlauf nachverfolgt werden kann.

  ![](assets/read-segment-log.png)

Nach erfolgreichem Abschluss der Tests können Sie Ihre Journey veröffentlichen (siehe [Veröffentlichen der Journey](publishing-the-journey.md)). Einzelpersonen aus der Audience geben die Journey an dem in den Eigenschaften der Journey angegebenen Datum/Uhrzeit ein. **[!UICONTROL Planung]** Abschnitt.

>[!NOTE]
>
>Bei wiederkehrenden zielgruppenbasierten Journey wird die Journey automatisch geschlossen, sobald ihr letztes Vorkommen ausgeführt wird. Wenn kein Enddatum/keine Endzeit angegeben wurde, müssen Sie die Journey manuell für neue Eintritte schließen, um sie zu beenden.

## Zielgruppen-Targeting in zielgruppenbasierten Journey

Zielgruppenbasierte Journey beginnen immer mit einer **Audience lesen** -Aktivität zum Abrufen von Personen, die zu einer Adobe Experience Platform-Zielgruppe gehören.

Die Audience, die zur Audience gehört, wird ein- oder regelmäßig abgerufen.

Nach Eingabe der Journey können Sie Anwendungsfälle für die Zielgruppen-Orchestrierung erstellen, sodass Kontakte aus der ursprünglichen Zielgruppe in verschiedene Zweige der Journey fließen.

**Segmentierung**

Mithilfe der Aktivität **Bedingung** können Sie eine Segmentierung anhand von Bedingungen durchführen. Sie können beispielsweise VIP-Personen auf einen bestimmten Pfad führen und alle übrigen Personen auf einen anderen Pfad.

Die Segmentierung kann basieren auf:

* Daten aus Datenquellen
* Kontext von Ereignissen, die Teil der Journey-Daten sind – Beispiel: Hat eine Person auf die Nachricht geklickt, die sie vor einer Stunde erhalten hat?
* Datum – Beispiel: Sind wir im Juni, wenn eine Person durch die Journey navigiert?
* Tageszeit – Beispiel: Ist es morgens in der Zeitzone der Person?
* Algorithmus, der die in die Journey geführte Audience auf der Basis eines Prozentsatzes aufteilt – Beispiel: 90 % - 10 % für den Ausschluss einer Kontrollgruppe

![](assets/read-segment-audience1.png)

**Ausschluss**

Die selbe Aktivität **Bedingung**, die für die Segmentierung verwendet wird (siehe oben), ermöglicht es Ihnen auch, einen Teil der Population auszuschließen. Sie können beispielsweise VIP-Personen ausschließen, indem Sie diese in einen Zweig mit direkt anschließendem Beenden-Schritt führen.

Dieser Ausschluss kann unmittelbar nach dem Abrufen der Zielgruppe, zu Zwecken der Populationszählung oder auf einer mehrstufigen Journey erfolgen.

![](assets/read-segment-audience2.png)

**Vereinigung**

Journeys erlauben das Erstellen von n Zweigen, die nach einer Segmentierung zusammengeführt werden.

Daher können Sie zwei Audiences zu einem gemeinsamen Erlebnis zurückkehren lassen.

Ein Beispiel: Im Anschluss an ein zehntägiges differenziertes Erlebnis in einer Journey können VIP- und Nicht-VIP-Kunden zum selben Pfad zurückkehren.

Nach einer Vereinigung können Sie die Audience erneut teilen, indem Sie eine Segmentierung oder einen Ausschluss durchführen.

![](assets/read-segment-audience3.png)
