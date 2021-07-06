---
title: Über Adobe Experience Platform-Segmente
description: Erfahren Sie, wie Sie ein Adobe Experience Platformen-Segment konfigurieren
feature: Journeys
topic: Content-Management
role: User
level: Intermediate
source-git-commit: 9e93a97ff793fec9fdf4aecd645f1df95b65b31a
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 58%

---

# Über Adobe Experience Platform-Segmente {#about-segments}

[!DNL Journey Optimizer]Mit können Sie Adobe Experience Platform-Segmente anhand von Echtzeit-Kundenprofildaten direkt aus dem Menü **[!UICONTROL Segmente]** erstellen und diese in Ihre Journeys einbinden.

Beachten Sie, dass Segmente auch vom Segmentierungs-Service selbst erstellt werden können. Weitere Informationen finden Sie in der [Dokumentation zum Adobe Experience Platform-Segmentierungs-Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de).

Sie können die Segmente in Journeys auf verschiedene Weise nutzen:

* Verwenden Sie eine Orchestrierungsaktivität **Segment lesen**, um alle dem angegebenen Segment angehörenden Personen in die Journey eintreten zu lassen. Die in Ihrer Journey enthaltenen Nachrichten werden an die dem Segment angehörenden Personen gesendet. Nehmen wir an, Sie verfügen über ein Segment für „Silber-Kunden“. Mit dieser Aktivität können Sie dafür sorgen, dass alle Silber-Kunden in eine Journey eintreten, und ihnen eine Reihe personalisierter Nachrichten senden.

   Weiterführende Informationen zur Verwendung der Aktivität **[!UICONTROL Segment lesen]** finden Sie in [diesem Abschnitt](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Verwenden Sie die Ereignisaktivität **Segmentqualifizierung**, um Personen auf der Grundlage von Adobe Experience Platform-Segmenteintritten und -austritten zu veranlassen, in eine Journey einzutreten oder in einer Journey fortzufahren. So können Sie z. B. alle neuen Silber-Kunden in eine Journey eintreten lassen und ihnen Nachrichten senden. Weiterführende Informationen zur Verwendung der Aktivität finden Sie in [diesem Abschnitt](../building-journeys/segment-qualification-events.md).

* Erstellen Sie mithilfe des einfachen oder erweiterten Ausdruckseditors **komplexe Bedingungen** in Ihren Journeys. Weiterführende Informationen finden Sie in diesem [Abschnitt](../building-journeys/condition-activity.md#using-a-segment).

## Auswertungsmethode in Adobe Journey Optimizer {#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer werden Zielgruppen mithilfe einer der folgenden Auswertungsmethoden aus Segmentdefinitionen generiert:

* Streaming-Segmentierung: Die Zielgruppenliste für das Segment wird in Echtzeit auf dem neuesten Stand gehalten, während neue Daten in das System fließen.
* Batch-Segmentierung - Die Zielgruppenliste für das Segment wird stündlich aktualisiert, basierend auf Daten, die in der letzten Stunde erfasst wurden.

Die Bestimmung zwischen Batch-Segmentierung und Streaming-Segmentierung erfolgt durch das System für jede Segmentdefinition, basierend auf der Komplexität und den Kosten der Auswertung der Segmentregel.

Sie können die Auswertungsmethode für jedes Segment in der Spalte **[!UICONTROL Auswertungsmethode]** der Segmentliste anzeigen.

Nachdem Sie ein Segment zum ersten Mal definiert haben, werden Profile zur Audience hinzugefügt, wenn sie sich qualifizieren.

Das Aufstocken der Audience aus vorherigen Daten kann bis zu 24 Stunden dauern. Nachdem die Audience aufgestockt wurde, wird die Audience kontinuierlich auf dem neuesten Stand gehalten und ist immer für das Targeting bereit.
