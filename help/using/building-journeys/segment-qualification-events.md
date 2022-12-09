---
solution: Journey Optimizer
product: journey optimizer
title: Segmentqualifikationsereignisse
description: Erfahren Sie mehr über Segmentqualifikationsereignisse
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 0%

---

# Segmentqualifikationsereignisse {#segment-qualification}

## Über Segmentqualifikationsereignisse{#about-segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Segmentqualifikationsereignisse"
>abstract="Mit dieser Aktivität kann Ihre Journey die Ein- und Austritte von Profilen in Adobe Experience Platform-Segmenten überwachen, um Kontakte dazu zu bringen, in eine Journey einzutreten oder in einer Journey fortzufahren."

Mit dieser Aktivität kann Ihre Journey die Ein- und Austritte von Profilen in Adobe Experience Platform-Segmenten überwachen, um Kontakte dazu zu bringen, in eine Journey einzutreten oder in einer Journey fortzufahren. Weiterführende Informationen zur Segmenterstellung finden Sie in diesem Abschnitt [Abschnitt](../segment/about-segments.md).

Nehmen wir an, Sie haben ein Segment &quot;Silber-Kunde&quot;. Mit dieser Aktivität können Sie alle neuen Silber-Kunden in eine Journey eintreten lassen und ihnen eine Reihe personalisierter Nachrichten senden.

Dieser Ereignistyp kann als erster Schritt oder später in der Journey positioniert werden.

>[!IMPORTANT]
>
>Beachten Sie, dass Adobe Experience Platform-Segmente entweder einmal täglich (**Batch** Segmente) oder in Echtzeit (**gestreamt** Segmente mithilfe der Option &quot;Zielgruppen mit hoher Häufigkeit&quot;von Adobe Experience Platform).
>
>Wenn das ausgewählte Segment gestreamt wird, treten die zu diesem Segment gehörenden Kontakte in Echtzeit in die Journey ein. Wenn es sich bei dem Segment um ein Batch-Segment handelt, treten für dieses Segment neu qualifizierte Personen in die Journey ein, wenn die Segmentberechnung in Adobe Experience Platform ausgeführt wird.
>
>Feldergruppen für Erlebnisereignisse können nicht in Journeys verwendet werden, die mit einem Segment lesen, einer Segmentqualifizierung oder einer Geschäftsereignisaktivität beginnen.


1. Entfalten Sie die **[!UICONTROL Events]** Kategorie und legen Sie eine **[!UICONTROL Segment Qualification]** -Aktivität in Ihre Arbeitsfläche.

   ![](assets/segment5.png)

1. Hinzufügen einer **[!UICONTROL Label]** zur Aktivität hinzu. Dieser Schritt ist optional.

1. Klicken Sie in **[!UICONTROL Segment]** und wählen Sie die Segmente aus, die Sie nutzen möchten.

   >[!NOTE]
   >
   >Beachten Sie, dass Sie die in der Liste angezeigten Spalten anpassen und sortieren können.

   ![](assets/segment6.png)

   Sobald das Segment hinzugefügt wurde, wird die **[!UICONTROL Copy]** -Schaltfläche können Sie den Namen und die Kennung kopieren:

   `{"name":"Loyalty membership“,”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. Im **[!UICONTROL Behaviour]** auswählen, ob Sie Segmenteintritte, -austritte oder beides überwachen möchten.

   >[!NOTE]
   >
   >Beachten Sie Folgendes: **[!UICONTROL Enter]** und **[!UICONTROL Exit]** entsprechen **Realisiert** und **Beendet** Status der Segmentbeteiligung von Adobe Experience Platform. Weiterführende Informationen zur Auswertung eines Segments finden Sie im Abschnitt [Dokumentation zum Segmentierungsdienst](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}.

1. Wählen Sie einen Namespace aus. Dies ist nur erforderlich, wenn das Ereignis als erster Schritt der Journey positioniert wird.

   ![](assets/segment7.png)

Die Payload enthält die folgenden Kontextinformationen, die Sie in Bedingungen und Aktionen verwenden können:

* Verhalten (Eintritt, Ausstieg)
* Zeitstempel der Qualifizierung
* die Segment-ID

Wenn Sie den Ausdruckseditor in einer Bedingung oder Aktion verwenden, die auf eine **[!UICONTROL Segment Qualification]** -Aktivität, haben Sie Zugriff auf die **[!UICONTROL SegmentQualification]** Knoten. Sie können zwischen dem **[!UICONTROL Last qualification time]** und **[!UICONTROL status]** (Einstieg oder Ausstieg).

Siehe [Bedingungsaktivität](../building-journeys/condition-activity.md#about_condition).

![](assets/segment8.png)

Eine neue Journey, die ein Segmentqualifikationsereignis enthält, ist zehn Minuten nach der Veröffentlichung funktionsfähig. Dieses Zeitintervall entspricht dem Cache-Aktualisierungsintervall des dedizierten Dienstes. Daher müssen Sie zehn Minuten warten, bevor Sie diese Journey verwenden.

## Best Practices {#best-practices-segments}

Die **[!UICONTROL Segment Qualification]** -Aktivität ermöglicht den sofortigen Eintritt in Journeys von Personen, die sich von einem Adobe Experience Platform-Segment qualifiziert oder disqualifiziert haben.

Die Empfangsgeschwindigkeit dieser Informationen ist hoch. Die durchgeführten Messungen zeigen eine Geschwindigkeit von 10.000 empfangenen Ereignissen pro Sekunde. Daher sollten Sie sich darüber im Klaren sein, wie Eintrittsspitzen auftreten können, wie diese vermieden werden und wie Sie Ihre Reise für sie vorbereitet machen können.

### Batch-Segmente{#batch-speed-segment-qualification}

Beachten Sie bei der Verwendung der Segmentqualifikation für ein Batch-Segment, dass zum Zeitpunkt der täglichen Berechnung eine Spitze des Eintritts auftritt. Die Größe der Spitze hängt von der Anzahl der Kontakte ab, die das Segment täglich aufrufen (oder verlassen).

Wenn das Batch-Segment neu erstellt und sofort in einer Journey verwendet wird, kann der erste Berechnungs-Batch außerdem dazu führen, dass sehr viele Kontakte in die Journey eintreten.

### Streaming-Segmente{#streamed-speed-segment-qualification}

Bei der Verwendung der Segmentqualifikation für Streaming-Segmente besteht aufgrund der kontinuierlichen Auswertung des Segments ein geringeres Risiko, dass es zu großen Spitzen bei Ein-/Austritten kommt. Wenn die Segmentdefinition dazu führt, dass eine große Anzahl von Kunden gleichzeitig qualifiziert wird, kann es auch zu einer Spitze kommen.

Weitere Informationen zur Streaming-Segmentierung finden Sie unter [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/streaming-segmentation.html#api)

### So vermeiden Sie Überlastungen{#overloads-speed-segment-qualification}

Im Folgenden finden Sie einige Best Practices, mit denen Sie verhindern können, dass in Journeys genutzte Systeme überlastet werden (Datenquellen, benutzerdefinierte Aktionen, Kanalaktionsaktivitäten).

Verwenden Sie nicht in einer **[!UICONTROL Segment Qualification]** -Aktivität, ein Batch-Segment unmittelbar nach seiner Erstellung. Dadurch wird die erste Berechnungsspitze vermieden. Beachten Sie, dass die Arbeitsfläche der Journey eine gelbe Warnung enthält, wenn Sie im Begriff sind, ein Segment zu verwenden, das noch nie berechnet wurde.

![](assets/segment-error.png)

Legen Sie eine Begrenzungsregel für Datenquellen und Aktionen fest, die in Journeys verwendet werden, um eine Überlastung zu vermeiden. Weitere Informationen finden Sie unter [Dokumentation zu Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html){target=&quot;_blank&quot;}. Beachten Sie, dass die Begrenzungsregel keinen erneuten Versuch enthält. Wenn Sie es erneut versuchen müssen, müssen Sie einen alternativen Pfad in der Journey verwenden, indem Sie das Kontrollkästchen aktivieren **[!UICONTROL Add an alternative path in case of a timeout or an error]** in Bedingungen oder Aktionen.

Bevor Sie das Segment in einer Produktions-Journey verwenden, bewerten Sie immer zuerst das Volumen der Kontakte, die sich für dieses Segment täglich qualifizieren. Dazu können Sie die **[!UICONTROL Segments]** öffnen Sie das Segment und sehen Sie sich dann die **[!UICONTROL Profiles over time]** Diagramm.

![](assets/segment-overload.png)
