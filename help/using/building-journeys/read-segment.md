---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden eines Segments in einer Journey
description: Erfahren Sie, wie Sie ein Segment in einer Journey verwenden
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '1260'
ht-degree: 0%

---

# Verwenden eines Segments in einer Journey {#segment-trigger-activity}

## Hinzufügen der Aktivität Segment lesen {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="Aktivität &quot;Segment lesen&quot;"
>abstract="Mit der Aktivität Segment lesen können Sie alle Kontakte, die zu einem Adobe Experience Platform-Segment gehören, in eine Journey eintreten lassen. Der Eintritt in eine Journey kann entweder einmal oder regelmäßig erfolgen."

Verwenden Sie die **Segment lesen** -Aktivität, damit alle Kontakte eines Segments in die Journey eintreten. Der Eintritt in eine Journey kann entweder einmal oder regelmäßig erfolgen.

Nehmen wir als Beispiel das Segment &quot;Öffnen und Auschecken einer Luma-App&quot;, das im [Segmente erstellen](../segment/about-segments.md) Anwendungsbeispiel. Mit der Aktivität Segment lesen können Sie alle zu diesem Segment gehörenden Kontakte in eine Journey eintreten lassen und sie in individuelle Journeys umwandeln, die alle Journey-Funktionen nutzen: Bedingungen, Timer, Ereignisse, Aktionen.

>[!NOTE]
>
>Für Journeys mit der Aktivität Segment lesen gibt es eine maximale Anzahl von Journeys, die exakt zur gleichen Zeit beginnen können. Weitere Zustellversuche werden vom System durchgeführt. Vermeiden Sie jedoch, dass mehr als fünf Journeys (mit Segment lesen, geplant oder &quot;so bald wie möglich&quot;gestartet werden) exakt zur gleichen Zeit beginnen, indem sie über einen bestimmten Zeitraum verteilt werden, z. B. zwischen 5 und 10 Minuten.
>
>Feldergruppen für Erlebnisereignisse können nicht in Journeys verwendet werden, die mit einem Segment lesen, einer Segmentqualifizierung oder einer Geschäftsereignisaktivität beginnen.

### Konfigurieren der Aktivität {#configuring-segment-trigger-activity}

Die Schritte zum Konfigurieren der Aktivität Segment lesen lauten wie folgt:

1. Entfalten Sie die **[!UICONTROL Orchestration]** Kategorie und legen Sie eine **[!UICONTROL Read Segment]** -Aktivität in Ihre Arbeitsfläche.

   Die Aktivität muss als erster Schritt einer Journey positioniert werden.

1. Hinzufügen einer **[!UICONTROL Label]** zur Aktivität hinzu (optional).

1. Im **[!UICONTROL Segment]** wählen Sie das Adobe Experience Platform-Segment aus, das in die Journey eintreten soll, und klicken Sie dann auf **[!UICONTROL Save]**.

   Beachten Sie, dass Sie die in der Liste angezeigten Spalten anpassen und sortieren können.

   >[!NOTE]
   >
   >Nur Personen mit der **Realisiert** und **Bestehend** Segmentteilnahmestatus in die Journey eintreten. Weiterführende Informationen zur Auswertung eines Segments finden Sie im Abschnitt [Dokumentation zum Segmentierungsdienst](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}.

   ![](assets/read-segment-selection.png)

   Sobald das Segment hinzugefügt wurde, wird die **[!UICONTROL Copy]** -Schaltfläche können Sie den Namen und die Kennung kopieren:

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

1. Im **[!UICONTROL Namespace]** auswählen, den Namespace, der zur Identifizierung der Kontakte verwendet werden soll. [Weitere Informationen zu Namespaces](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Kontakte, die zu einem Segment gehören, das nicht die ausgewählte Identität (den ausgewählten Namespace) hat, können nicht in die Journey eintreten.

1. Legen Sie die **[!UICONTROL Throttling rate]** -Feld zur Durchsatzbegrenzung der Aktivität &quot;Lesesegment&quot;hinzu.

   Dieser Wert wird in der Payload der Journey-Version gespeichert. Der Standardwert ist 20.000 Nachrichten pro Sekunde. Sie können diesen Wert von 500 auf 20.000 Nachrichten pro Sekunde ändern.

   >[!NOTE]
   >
   >Die Gesamtdrosselungsrate pro Sandbox wird auf 20.000 Nachrichten pro Sekunde festgelegt. Daher ergibt die Drosselrate aller Lesesegmente, die gleichzeitig in derselben Sandbox ausgeführt werden, maximal 20.000 Nachrichten pro Sekunde. Sie können diese Mütze nicht ändern.

1. Die **[!UICONTROL Read Segment]** -Aktivität können Sie den Zeitpunkt festlegen, zu dem das Segment in die Journey eintreten wird. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Edit journey schedule]** -Link, um auf die Eigenschaften der Journey zuzugreifen, und konfigurieren Sie dann die **[!UICONTROL Scheduler type]** -Feld.

   ![](assets/read-segment-schedule.png)

   Standardmäßig treten Segmente in die Journey ein **[!UICONTROL As soon as possible]**. Wenn Sie möchten, dass das Segment zu einem bestimmten Datum/zu einer bestimmten Uhrzeit oder wiederholt in die Journey eintritt, wählen Sie den gewünschten Wert aus der Liste aus.

   >[!NOTE]
   >
   >Beachten Sie Folgendes: **[!UICONTROL Schedule]** -Abschnitt ist nur verfügbar, wenn eine **[!UICONTROL Read Segment]** -Aktivität wurde auf der Arbeitsfläche abgelegt.

   ![](assets/read-segment-schedule-list.png)

   **Inkrementelles Lesen** Option: wenn eine Journey mit einer wiederkehrenden **Segment lesen** zum ersten Mal ausgeführt wird, treten alle Profile im Segment in die Journey ein. Mit dieser Option können Sie nach dem ersten Vorkommen nur die Kontakte auswählen, die das Segment seit der letzten Ausführung der Journey aufgerufen haben.

   **Wiedereintritt erzwingen bei Wiederholung**: Mit dieser Option können Sie festlegen, dass alle noch in der Journey vorhandenen Profile bei der nächsten Ausführung automatisch beendet werden. Wenn Sie beispielsweise eine Journey mit zwei Tagen Wartezeit in einer täglich wiederkehrenden Journey haben und diese Option aktivieren, werden Profile immer bei der nächsten Journey-Ausführung verschoben (also am Tag danach), unabhängig davon, ob sie sich in der nächsten ausgeführten Audience befinden oder nicht. Wenn die Lebensdauer Ihrer Profile in dieser Journey möglicherweise länger als die Häufigkeit des erneuten Auftretens ist, aktivieren Sie diese Option nicht, um sicherzustellen, dass Profile ihre Journey beenden können.

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
>Einmalige Lesen von Segment-Journeys werden 30 Tage nach der Ausführung der Journey in den Status Abgeschlossen verschoben. Bei geplanten Read-Segmenten ist es 30 Tage nach der Ausführung des letzten Vorkommens.

### Testen und Veröffentlichen der Journey {#testing-publishing}

Die **[!UICONTROL Read Segment]** -Aktivität können Sie die Journey entweder auf einem unitären Profil oder auf 100 zufällig ausgewählten Testprofilen testen, die unter den für das Segment qualifizierten Profilen ausgewählt wurden.

Aktivieren Sie dazu den Testmodus und wählen Sie dann im linken Bereich die gewünschte Option aus.

![](assets/read-segment-test-mode.png)

Anschließend können Sie den Testmodus wie gewohnt konfigurieren und ausführen. [Erfahren Sie, wie Sie eine Journey testen](testing-the-journey.md).

Sobald der Test ausgeführt wird, wird die **[!UICONTROL Show logs]** -Schaltfläche können Sie die Testergebnisse entsprechend der ausgewählten Testoption anzeigen:

* **[!UICONTROL Single profile at a time]**: Die Testprotokolle zeigen dieselben Informationen an wie bei Verwendung des einheitlichen Testmodus. Weitere Informationen hierzu finden Sie unter [diesem Abschnitt](testing-the-journey.md#viewing_logs)

* **[!UICONTROL Up to 100 profiles at once]**: Mithilfe der Testprotokolle können Sie den Fortschritt des Segmentexports aus Adobe Experience Platform sowie den individuellen Fortschritt aller Personen, die in die Journey eingestiegen sind, verfolgen.

   Beachten Sie, dass Sie beim Testen der Journey mit bis zu 100 Profilen auf einmal nicht den Fortschritt der Kontakte in der Journey mithilfe des visuellen Flusses verfolgen können.

   ![](assets/read-segment-log.png)

Sobald die Tests erfolgreich sind, können Sie Ihre Journey veröffentlichen (siehe [Veröffentlichen der Journey](publishing-the-journey.md)). Kontakte, die zum Segment gehören, treten an dem Datum/zu der Uhrzeit in die Journey ein, die in den Eigenschaften der Journey angegeben ist **[!UICONTROL Scheduler]** Abschnitt.

>[!NOTE]
>
>Bei wiederkehrenden segmentbasierten Journeys wird die Journey automatisch geschlossen, sobald ihr letztes Vorkommen ausgeführt wird. Wenn kein Enddatum/keine Endzeit angegeben wurde, müssen Sie die Journey zu neuen Eintritten manuell schließen, um sie zu beenden.

## Zielgruppen-Targeting in segmentbasierten Journeys

Segmentbasierte Journeys beginnen immer mit einer **Segment lesen** -Aktivität zum Abrufen von Einzelanwendern, die zu einem Adobe Experience Platform-Segment gehören.

Die zum Segment gehörende Zielgruppe wird ein- oder regelmäßig abgerufen.

Nach dem Eintritt in die Journey können Sie Anwendungsfälle für die Zielgruppensorchestrierung erstellen, sodass Kontakte aus dem ursprünglichen Segment in verschiedene Verzweigungen der Journey fließen.

**Segmentierung**

Sie können Bedingungen zum Ausführen der Segmentierung mithilfe der **Bedingung** Aktivität. Sie können beispielsweise VIP-Personen dazu bringen, einen bestimmten Pfad zu verwenden und nicht über VIP in einen anderen Pfad zu gelangen.

Die Segmentierung kann auf Folgendem basieren:

* Datenquellendaten
* den Kontext des Ereignisabschnitts der Journey-Daten, z. B.: Hat eine Person vor einer Stunde auf die Nachricht geklickt?
* ein Datum, z. B.: Sind wir im Juni, wenn eine Person durch die Reise geht?
* einen Zeitpunkt, z. B.: Ist es Morgen in der Zeitzone der Person?
* einen Algorithmus, der die in der Journey fließende Zielgruppe anhand eines Prozentsatzes aufteilt, z. B.: 90 % - 10 % zum Ausschließen einer Kontrollgruppe

![](assets/read-segment-audience1.png)

**Ausschluss**

Dasselbe **Bedingung** Aktivitäten, die für die Segmentierung verwendet werden (siehe oben), ermöglichen es Ihnen auch, einen Teil der Population auszuschließen. Sie können beispielsweise VIP-Personen ausschließen, indem Sie sie direkt danach in eine Zweigstelle mit einem Endschritt eingliedern.

Dieser Ausschluss kann unmittelbar nach dem Segmentabruf, zu Zwecken der Populationszählung oder während einer mehrstufigen Journey erfolgen.

![](assets/read-segment-audience2.png)

**Vereinigung**

Mit Journeys können Sie N Verzweigungen erstellen und diese nach einer Segmentierung verknüpfen.

Daher können Sie zwei Zielgruppen dazu bringen, zu einem gemeinsamen Erlebnis zurückzukehren.

Nachdem Sie beispielsweise zehn Tage in einer Journey ein anderes Erlebnis verfolgt haben, können VIP- und Nicht-VIP-Kunden zum selben Pfad zurückkehren.

Nach einer Vereinigung können Sie die Zielgruppe durch eine Segmentierung oder einen Ausschluss erneut aufteilen.

![](assets/read-segment-audience3.png)
