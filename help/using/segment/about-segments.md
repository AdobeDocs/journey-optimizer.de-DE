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
ht-degree: 100%

---

# Erste Schritte mit Adobe Experience Platform-Segmenten {#about-segments}

Mit [!DNL Journey Optimizer] können Sie Adobe Experience Platform-Segmente mithilfe von Echtzeit-Kundenprofildaten direkt im Menü **[!UICONTROL Segmente]** erstellen und diese Segmente in Ihre Journeys oder Kampagnen einbinden.

Segmente können auch vom Segmentierungs-Service selbst erstellt werden. Weitere Informationen finden Sie in der [Dokumentation zum Segmentierungs-Service in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de).

## Verwendung von Segmenten in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Sie können Segmente in **[!DNL Journey Optimizer]** auf verschiedene Weise nutzen:

* Wählen Sie ein Segment als **Audience für eine Kampagne** aus: Die Nachricht wird an alle Einzelpersonen gesendet, die zum ausgewählten Segment gehören. [Erfahren Sie, wie Sie die Audience einer Kampagne definieren](../campaigns/create-campaign.md#define-the-audience-audience).

* Verwenden Sie die Orchestrierungsaktivität **Segment lesen** in einer Journey, um alle Einzelpersonen des Segments in die Journey eintreten zu lassen und die in Ihrer Journey enthaltenen Nachrichten zu erhalten.

   Nehmen wir an, Sie verfügen über ein Segment für „Silber-Kundinnen und -Kunden“. Mit dieser Aktivität können Sie dafür sorgen, dass alle Silber-Kundinnen und -Kunden in eine Journey eintreten, und ihnen eine Reihe personalisierter Nachrichten senden. [Erfahren Sie, wie Sie eine Aktivität vom Typ „Segment lesen“ konfigurieren](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Verwenden Sie die Ereignisaktivität **Segmentqualifizierung**, um Einzelpersonen auf der Grundlage von Adobe Experience Platform-Segmenteintritten und -austritten zu veranlassen, in eine Journey einzutreten oder in einer Journey fortzufahren.

   So können Sie z. B. alle neuen Silber-Kundinnen und -Kunden in eine Journey eintreten lassen und ihnen Nachrichten senden. Weiterführende Informationen zur Verwendung dieser Aktivität finden Sie im Abschnitt [Erfahren Sie, wie Sie eine Segmentqualifizierungsaktivität konfigurieren](../building-journeys/segment-qualification-events.md).

* Verwenden Sie die Aktivität **Bedingung** in einer Journey, um Bedingungen zu erstellen, die auf der Segmentzugehörigkeit basieren. [Erfahren Sie, wie Sie Segmente in Bedingungen verwenden](../building-journeys/condition-activity.md#using-a-segment).

## Methoden zur Audience-Auswertung{#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer werden Audiences aus Segmentdefinitionen mithilfe einer der folgenden Auswertungsmethoden generiert:

* **Streaming-Segmentierung:** Die Audience-Liste für das Segment wird in Echtzeit auf dem neuesten Stand gehalten, während neue Daten in das System einfließen.

   Die Streaming-Segmentierung ist ein fortlaufender Datenauswahlprozess, der die Segmente infolge von Benutzeraktivitäten aktualisiert. Nachdem ein Segment erstellt und gespeichert wurde, wird die Segmentdefinition auf Daten angewendet, die in Journey Optimizer eingehen. Das bedeutet, dass Einzelpersonen bei sich ändernden Profildaten zum Segment hinzugefügt oder daraus entfernt werden, sodass Ihre Audience immer relevant ist.

* **Batch-Segmentierung**: Die Audience-Liste für das Segment wird alle 24 Stunden ausgewertet.

   Die Batch-Segmentierung ist eine Alternative zur Streaming-Segmentierung, die alle Profildaten gleichzeitig über Segmentdefinitionen verarbeitet. Dadurch wird ein Schnappschuss der Audience erstellt, der gespeichert und zur Verwendung exportiert werden kann. Im Gegensatz zur Streaming-Segmentierung wird die Audience-Liste bei der Batch-Segmentierung jedoch nicht kontinuierlich in Echtzeit aktualisiert. Neue Daten, die nach dem Batch-Prozess eingehen, werden erst im nächsten Batch-Prozess im Segment angezeigt.“

Die Entscheidung zwischen Batch- und Streaming-Segmentierung wird für jede Segmentdefinition abhängig von der Komplexität und den Kosten für die Auswertung der Segmentregel vom System getroffen. Sie können die Auswertungsmethode für jedes Segment in der Spalte **[!UICONTROL Auswertungsmethode]** der Segmentliste anzeigen.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Wenn die Variable **[!UICONTROL Auswertungsmethode]** nicht angezeigt wird, müssen Sie sie mithilfe der Konfigurationsschaltfläche oben rechts in der Liste hinzufügen.

Nachdem Sie ein Segment zum ersten Mal definiert haben, werden Profile zur Audience hinzugefügt, wenn sie sich qualifizieren.

Das Auffüllen der Audience anhand früherer Daten kann bis zu 24 Stunden dauern. Nachdem die Audience aufgefüllt wurde, wird sie kontinuierlich aktuell gehalten und ist immer für die Zielgruppenbestimmung bereit.
