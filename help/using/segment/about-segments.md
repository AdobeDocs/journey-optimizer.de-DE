---
solution: Journey Optimizer
product: journey optimizer
title: Über Adobe Experience Platform-Segmente
description: Erfahren Sie, wie Sie ein Adobe Experience Platformen-Segment konfigurieren
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 78675ca22d8ee9a93d9af128d5708c305523da78
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 37%

---

# Erste Schritte mit Adobe Experience Platform-Segmenten {#about-segments}

[!DNL Journey Optimizer]  ermöglicht Ihnen das Erstellen von Adobe Experience Platform-Segmenten mithilfe von Echtzeit-Kundenprofildaten direkt aus dem **[!UICONTROL Segmente]** und verwenden Sie sie in Ihren Journey oder Kampagnen.

Darüber hinaus können Segmente auch über den Segmentierungsdienst selbst erstellt werden. Weitere Informationen zu Datensätzen finden Sie in der [Dokumentation zum Adobe Experience Platform-Segmentierungs-Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de).

## Verwenden von Segmenten in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Sie können Segmente in **[!DNL Journey Optimizer]** auf unterschiedliche Weise:

* Wählen Sie ein Segment als **Zielgruppe für eine Kampagne**: Die Nachricht wird an alle Kontakte gesendet, die zum ausgewählten Segment gehören. [Hier erfahren Sie, wie Sie die Audience einer Kampagne definieren.](../campaigns/create-campaign.md#define-the-audience-audience).

* Verwenden Sie eine **Segment lesen** Orchestrierungsaktivität in einer Journey, um alle Einzelanwender des Segments dazu zu bringen, in die Journey einzutreten und die in Ihrer Journey enthaltenen Nachrichten zu erhalten.

   Nehmen wir an, Sie verfügen über ein Segment für „Silber-Kunden“. Mit dieser Aktivität können Sie dafür sorgen, dass alle Silber-Kunden in eine Journey eintreten, und ihnen eine Reihe personalisierter Nachrichten senden. [Erfahren Sie, wie Sie eine Aktivität vom Typ Segment lesen konfigurieren](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Verwenden Sie die **Segmentqualifizierung** -Ereignisaktivität in einer Journey, um Einzelpersonen dazu zu bringen, je nach Eintritten und Austritten von Adobe Experience Platform-Segmenten in die Journey einzutreten oder in der Zukunft fortzufahren.

   So können Sie z. B. alle neuen Silber-Kunden in eine Journey eintreten lassen und ihnen Nachrichten senden. Weiterführende Informationen zur Verwendung dieser Aktivität finden Sie im Abschnitt [Erfahren Sie, wie Sie eine Segmentqualifikationsaktivität konfigurieren.](../building-journeys/segment-qualification-events.md).

* Verwenden Sie die **Bedingung** -Aktivität in einer Journey, um Bedingungen zu erstellen, die auf der Segmentzugehörigkeit basieren. [Erfahren Sie, wie Sie Segmente in Bedingungen verwenden](../building-journeys/condition-activity.md#using-a-segment).

## Methoden zur Zielgruppenauswertung{#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer werden Zielgruppen mithilfe einer von zwei Auswertungsmethoden aus Segmentdefinitionen generiert:

* **Streaming-Segmentierung**: Die Zielgruppenliste für das Segment wird in Echtzeit auf dem neuesten Stand gehalten, da neue Daten in das System fließen.

   Die Streaming-Segmentierung ist ein fortlaufender Datenauswahlprozess, der die Segmente infolge von Benutzeraktivitäten aktualisiert. Nachdem ein Segment erstellt und gespeichert wurde, wird die Segmentdefinition auf Daten angewendet, die in Journey Optimizer eingehen. Das bedeutet, dass Personen bei sich ändernden Profildaten zum Segment hinzugefügt oder daraus entfernt werden, sodass Ihre Zielgruppe immer relevant ist.

* **Batch-Segmentierung**: Die Zielgruppenliste für das Segment wird alle 24 Stunden ausgewertet.

   Die Batch-Segmentierung ist eine Alternative zur Streaming-Segmentierung, die alle Profildaten gleichzeitig über Segmentdefinitionen verarbeitet. Dadurch wird ein Schnappschuss der Audience erstellt, die gespeichert und zur Verwendung exportiert werden kann. Im Gegensatz zur Streaming-Segmentierung wird die Zielgruppenliste bei der Batch-Segmentierung jedoch nicht kontinuierlich in Echtzeit aktualisiert. Neue Daten, die nach dem Batch-Prozess eingehen, werden erst im nächsten Batch-Prozess im Segment angezeigt.&quot;

Die Entscheidung zwischen Batch- und Streaming-Segmentierung wird für jede Segmentdefinition abhängig von der Komplexität und den Kosten für die Auswertung der Segmentregel vom System getroffen. Sie können die Auswertungsmethode für jedes Segment in der Spalte **[!UICONTROL Auswertungsmethode]** der Segmentliste anzeigen.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Wenn die Variable **[!UICONTROL Auswertungsmethode]** nicht angezeigt wird, müssen Sie sie mithilfe der Konfigurationsschaltfläche oben rechts in der Liste hinzufügen.

Nachdem Sie ein Segment zum ersten Mal definiert haben, werden Profile zur Audience hinzugefügt, wenn sie sich qualifizieren.

Das Auffüllen der Audience anhand früherer Daten kann bis zu 24 Stunden dauern. Nachdem die Audience aufgefüllt wurde, wird sie kontinuierlich aktuell gehalten und ist immer für die Zielgruppenbestimmung bereit.
