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
source-git-commit: bfd262db2fd12afbb7df6c73c68b29d18a1abf98
workflow-type: ht
source-wordcount: '460'
ht-degree: 100%

---

# Erste Schritte mit Adobe Experience Platform-Segmenten {#about-segments}

Mit [!DNL Journey Optimizer] können Sie Adobe Experience Platform-Segmente mithilfe von Echtzeit-Kundenprofildaten direkt im Menü **[!UICONTROL Segmente]** erstellen und diese Segmente in Ihre Journeys einbinden.

Beachten Sie, dass Segmente auch vom Segmentierungs-Service selbst erstellt werden können. Weitere Informationen finden Sie in der [Dokumentation zum Adobe Experience Platform-Segmentierungs-Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de).

Sie können die Segmente in Journeys auf verschiedene Weise nutzen:

* Verwenden Sie eine Orchestrierungsaktivität **Segment lesen**, um alle dem angegebenen Segment angehörenden Personen in die Journey eintreten zu lassen. Die in Ihrer Journey enthaltenen Nachrichten werden an die dem Segment angehörenden Personen gesendet. Nehmen wir an, Sie verfügen über ein Segment für „Silber-Kunden“. Mit dieser Aktivität können Sie dafür sorgen, dass alle Silber-Kunden in eine Journey eintreten, und ihnen eine Reihe personalisierter Nachrichten senden.

   Weiterführende Informationen zur Verwendung der Aktivität **[!UICONTROL Segment lesen]** finden Sie in [diesem Abschnitt](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Verwenden Sie die Ereignisaktivität **Segmentqualifizierung**, um Personen auf der Grundlage von Adobe Experience Platform-Segmenteintritten und -austritten zu veranlassen, in eine Journey einzutreten oder in einer Journey fortzufahren. So können Sie z. B. alle neuen Silber-Kunden in eine Journey eintreten lassen und ihnen Nachrichten senden. Weiterführende Informationen zur Verwendung der Aktivität finden Sie in [diesem Abschnitt](../building-journeys/segment-qualification-events.md).

* Erstellen Sie mithilfe des einfachen oder erweiterten Ausdruckseditors **komplexe Bedingungen** in Ihren Journeys. Weiterführende Informationen finden Sie in diesem [Abschnitt](../building-journeys/condition-activity.md#using-a-segment).

## Methoden zur Zielgruppenauswertung{#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer werden Zielgruppen aus Segmentdefinitionen mithilfe einer der folgenden Auswertungsmethoden generiert:

* Streaming-Segmentierung: Die Zielgruppen-Liste für das Segment wird in Echtzeit auf dem neuesten Stand gehalten, während neue Daten in das System fließen. Die Streaming-Segmentierung ist ein fortlaufender Datenauswahlprozess, der die Segmente infolge von Benutzeraktivitäten aktualisiert. Nachdem ein Segment erstellt und gespeichert wurde, wird die Segmentdefinition auf Daten angewendet, die in Journey Optimizer eingehen. Segmenthinzufügungen und -entfernungen werden regelmäßig verarbeitet, damit sichergestellt ist, dass die Zielgruppe relevant bleibt.

* Batch-Segmentierung – die Zielgruppenliste für das Segment wird alle 24 Stunden ausgewertet. Als Alternative zum kontinuierlichen Datenauswahlprozess werden bei der Batch-Segmentierung alle Profildaten gleichzeitig mit Segmentdefinitionen verglichen, um entsprechende Zielgruppen zu erstellen. Nach der Erstellung eines Segments wird es gespeichert, sodass Sie es exportieren und weiterverwenden können.

Die Entscheidung zwischen Batch- und Streaming-Segmentierung wird für jede Segmentdefinition abhängig von der Komplexität und den Kosten für die Auswertung der Segmentregel vom System getroffen.

Sie können die Auswertungsmethode für jedes Segment in der Spalte **[!UICONTROL Auswertungsmethode]** der Segmentliste anzeigen.

Nachdem Sie ein Segment zum ersten Mal definiert haben, werden Profile zur Audience hinzugefügt, wenn sie sich qualifizieren.

Das Auffüllen der Audience anhand früherer Daten kann bis zu 24 Stunden dauern. Nachdem die Audience aufgefüllt wurde, wird sie kontinuierlich aktuell gehalten und ist immer für die Zielgruppenbestimmung bereit.
