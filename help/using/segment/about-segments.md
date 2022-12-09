---
solution: Journey Optimizer
product: journey optimizer
title: Über Adobe Experience Platform-Segmente
description: Erfahren Sie, wie Sie ein Adobe Experience Platform-Segment konfigurieren
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: bfd262db2fd12afbb7df6c73c68b29d18a1abf98
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Erste Schritte mit Adobe Experience Platform-Segmenten {#about-segments}

[!DNL Journey Optimizer]  ermöglicht Ihnen das Erstellen von Adobe Experience Platform-Segmenten mithilfe von Echtzeit-Kundenprofildaten direkt aus dem **[!UICONTROL Segments]** und nutzen Sie sie für Ihre Journeys.

Beachten Sie, dass Segmente auch über den Segmentierungsdienst selbst erstellt werden können. Weitere Informationen finden Sie unter [Dokumentation zu Adobe Experience Platform Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

Sie können Segmente in Journeys auf unterschiedliche Weise nutzen:

* Verwenden Sie eine **Segment lesen** Orchestrierungsaktivität , damit alle Kontakte, die zum angegebenen Segment gehören, in die Journey eintreten. In Ihrer Journey enthaltene Nachrichten werden an die Kontakte gesendet, die zum Segment gehören. Nehmen wir an, Sie haben ein Segment &quot;Silber-Kunde&quot;. Mit dieser Aktivität können Sie alle Silber-Kunden in eine Journey eintreten lassen und ihnen eine Reihe personalisierter Nachrichten senden.

   Weitere Informationen zur Verwendung der **[!UICONTROL Read segment]** Aktivität, siehe [diesem Abschnitt](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Verwenden Sie die **Segmentqualifizierung** Ereignisaktivität , um Kontakte dazu zu bringen, basierend auf den Ein- und Austritten von Adobe Experience Platform-Segmenten in eine Journey einzutreten oder in einer Journey fortzufahren. Sie können beispielsweise alle neuen Silber-Kunden in eine Journey eintreten lassen und ihnen Nachrichten senden. Weiterführende Informationen zur Verwendung dieser Aktivität finden Sie im Abschnitt [diesem Abschnitt](../building-journeys/segment-qualification-events.md).

* Build **komplexe Bedingungen** in Ihren Journeys mit dem einfachen oder erweiterten Ausdruckseditor verwenden. Weitere Informationen finden Sie unter [diesem Abschnitt](../building-journeys/condition-activity.md#using-a-segment).

## Methoden zur Zielgruppenbewertung{#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer werden Zielgruppen aus Segmentdefinitionen mithilfe einer der folgenden Auswertungsmethoden generiert:

* Streaming-Segmentierung : Die Zielgruppenliste für das Segment wird in Echtzeit auf dem neuesten Stand gehalten, während neue Daten in das System fließen. Streaming-Segmentierung ist ein fortlaufender Datenauswahlprozess, der Ihre Segmente als Reaktion auf Benutzeraktivitäten aktualisiert. Nachdem ein Segment erstellt und gespeichert wurde, wird die Segmentdefinition auf eingehende Daten an Journey Optimizer angewendet. Segmentzufügungen und -entfernungen werden regelmäßig verarbeitet, um sicherzustellen, dass Ihre Zielgruppe relevant bleibt.

* Batch-Segmentierung - die Zielgruppenliste für das Segment wird alle 24 Stunden ausgewertet. Als Alternative zu einem laufenden Datenauswahlprozess verschiebt die Batch-Segmentierung alle Profildaten gleichzeitig durch Segmentdefinitionen, um entsprechende Zielgruppen zu erstellen. Nach der Erstellung wird dieses Segment gespeichert, sodass Sie es zur Verwendung exportieren können.

Die Bestimmung zwischen Batch-Segmentierung und Streaming-Segmentierung erfolgt durch das System für jede Segmentdefinition, basierend auf der Komplexität und den Kosten der Auswertung der Segmentregel.

Sie können die Auswertungsmethode für jedes Segment im **[!UICONTROL Evaluation method]** der Segmentliste.

Nachdem Sie ein Segment zum ersten Mal definiert haben, werden Profile zur Audience hinzugefügt, wenn sie sich qualifizieren.

Das Aufstocken der Audience aus vorherigen Daten kann bis zu 24 Stunden dauern. Nachdem die Audience aufgestockt wurde, wird die Audience kontinuierlich auf dem neuesten Stand gehalten und ist immer für das Targeting bereit.
