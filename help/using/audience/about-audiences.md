---
solution: Journey Optimizer
product: journey optimizer
title: Über Adobe Experience Platform-Zielgruppen
description: Erfahren Sie, wie Sie mit Adobe Experience Platform-Zielgruppen arbeiten.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 28%

---

# Erste Schritte mit Adobe Experience Platform-Zielgruppen {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Zielgruppe "
>abstract="Mithilfe von Echtzeit-Kundenprofildaten können Sie mit Adobe Experience Platform Segmentdefinitionen einfach erstellen, um zielgerichtete Zielgruppen zu erstellen, die das einzigartige Verhalten und die Vorlieben Ihrer Kunden erfassen."

[!DNL Journey Optimizer] ermöglicht Ihnen die Erstellung und Nutzung von Adobe Experience Platform-Zielgruppen mithilfe von Echtzeit-Kundenprofildaten direkt über die **[!UICONTROL Zielgruppen]** und verwenden Sie sie in Ihren Journey oder Kampagnen.

Weitere Informationen finden Sie in der [Dokumentation zum Segmentierungs-Service in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de).

## Verwenden von Zielgruppen in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Sie können Zielgruppen in **[!DNL Journey Optimizer]** auf unterschiedliche Weise:

* Auswählen einer Zielgruppe für eine **Kampagne**: Nachricht wird an alle Kontakte gesendet, die zur ausgewählten Audience gehören. [Erfahren Sie, wie Sie die Audience einer Kampagne definieren](../campaigns/create-campaign.md#define-the-audience-audience).

* Verwenden Sie eine **Audience lesen** Orchestrierungsaktivität in einer Journey, um alle Personen in der Audience dazu zu bringen, in die Journey einzutreten und die in Ihrer Journey enthaltenen Nachrichten zu erhalten.

  Nehmen wir an, Sie haben eine Audience vom Typ &quot;Silber-Kunde&quot;. Mit dieser Aktivität können Sie dafür sorgen, dass alle Silber-Kundinnen und -Kunden in eine Journey eintreten, und ihnen eine Reihe personalisierter Nachrichten senden. [Erfahren Sie, wie Sie eine Audience lesen -Aktivität konfigurieren](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Verwenden Sie die **Zielgruppenqualifikation** -Ereignisaktivität in einer Journey, um Einzelpersonen dazu zu bringen, je nach Eintritten und Austritten der Adobe Experience Platform-Zielgruppe in die Journey einzutreten oder in der Zukunft fortzufahren.

  So können Sie z. B. alle neuen Silber-Kundinnen und -Kunden in eine Journey eintreten lassen und ihnen Nachrichten senden. Weiterführende Informationen zur Verwendung dieser Aktivität finden Sie im Abschnitt [Erfahren Sie, wie Sie eine Aktivität vom Typ Zielgruppenqualifizierung konfigurieren](../building-journeys/audience-qualification-events.md).

* Verwenden Sie die **Bedingung** -Aktivität in einer Journey, um Bedingungen zu erstellen, die auf der Zielgruppenmitgliedschaft basieren. [Erfahren Sie, wie Sie Zielgruppen in Bedingungen verwenden können.](../building-journeys/condition-activity.md#using-a-segment).

## Methoden zur Audience-Auswertung{#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer werden Audiences aus Segmentdefinitionen mithilfe einer der folgenden Auswertungsmethoden generiert:

* **Streaming-Segmentierung**: Die Profilliste für die Audience wird in Echtzeit auf dem neuesten Stand gehalten, da neue Daten in das System fließen.

  Streaming-Segmentierung ist ein fortlaufender Datenauswahlprozess, der Ihre Zielgruppen als Reaktion auf Benutzeraktivitäten aktualisiert. Nachdem eine Segmentdefinition erstellt und die resultierende Zielgruppe gespeichert wurde, wird die Segmentdefinition auf eingehende Daten in Journey Optimizer angewendet. Das bedeutet, dass Kontakte zur Zielgruppe hinzugefügt oder daraus entfernt werden, wenn sich ihre Profildaten ändern. Dadurch wird sichergestellt, dass Ihre Zielgruppe immer relevant ist.

* **Batch-Segmentierung**: Die Profilliste für die Audience wird alle 24 Stunden ausgewertet.

  Die Batch-Segmentierung ist eine Alternative zur Streaming-Segmentierung, die alle Profildaten gleichzeitig über Segmentdefinitionen verarbeitet. Dadurch wird ein Schnappschuss der Audience erstellt, der gespeichert und zur Verwendung exportiert werden kann. Im Gegensatz zur Streaming-Segmentierung wird die Zielgruppenliste bei der Batch-Segmentierung jedoch nicht kontinuierlich in Echtzeit aktualisiert. Neue Daten, die nach dem Batch-Prozess eingehen, werden erst im nächsten Batch-Prozess in der Zielgruppe übernommen.&quot;

Die Bestimmung zwischen Batch-Segmentierung und Streaming-Segmentierung erfolgt durch das System für jede Zielgruppe, basierend auf der Komplexität und den Kosten der Auswertung der Segmentdefinitionsregel. Sie können die Auswertungsmethode für jede Zielgruppe im **[!UICONTROL Auswertungsmethode]** der Zielgruppenliste.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Wenn die Variable **[!UICONTROL Auswertungsmethode]** nicht angezeigt wird, müssen Sie sie mithilfe der Konfigurationsschaltfläche oben rechts in der Liste hinzufügen.

Nachdem Sie eine Audience zum ersten Mal definiert haben, werden Profile zur Audience hinzugefügt, wenn sie sich qualifizieren.

Das Auffüllen der Audience anhand früherer Daten kann bis zu 24 Stunden dauern. Nachdem die Audience aufgefüllt wurde, wird sie kontinuierlich aktuell gehalten und ist immer für die Zielgruppenbestimmung bereit.
