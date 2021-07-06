---
title: Erstellen eines Segments
description: Erfahren Sie, wie Sie ein Segment erstellen
feature: Journeys
topic: Content-Management
role: User
level: Intermediate
source-git-commit: 9e93a97ff793fec9fdf4aecd645f1df95b65b31a
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 96%

---

# Erstellen von Segmenten {#build-segments}

In diesem Beispiel erstellen wir ein Segment für alle in Atlanta, San Francisco oder Seattle wohnenden und nach 1980 geborenen Kunden. Alle diese Kunden sollten das Programm Luma innerhalb der letzten 7 Tage geöffnet und dann innerhalb von 2 Stunden nach dem Öffnen eine Bestellung abgeschlossen haben.

1. Rufen Sie das Menü **[!UICONTROL Segmente]** auf und klicken Sie dann auf die Schaltfläche **[!UICONTROL Segment erstellen]**.

   ![](../assets/create-segment.png)

   Im Bildschirm für die Segmentdefinition können Sie alle erforderlichen Felder konfigurieren, um Ihr Segment einzurichten. Erfahren Sie in der Dokumentation zum [Segmentierungs-Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=de), wie Sie Segmente konfigurieren.

   ![](../assets/segment-builder.png)

1. Geben Sie im Bereich **[!UICONTROL Segmenteigenschaften]** einen Namen und eine Beschreibung (optional) für das Segment ein.

   ![](../assets/segment-properties.png)

1. Ziehen Sie per Drag-and-Drop die gewünschten Felder aus dem linken Bereich in den mittleren Arbeitsbereich und konfigurieren Sie die Felder dann entsprechend Ihren Anforderungen.

   >[!NOTE]
   >
   >Beachten Sie, dass die Felder im linken Bereich je nach Konfiguration der Schemas **XDM Individual Profile** und **XDM ExperienceEvent** für Ihr Unternehmen abweichen.  Weitere Informationen finden Sie in der [Dokumentation zum Experience-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de).

   ![](../assets/drag-fields.png)

   In diesem Beispiel müssen für die Segmenterstellung die Felder **Attribute** und **Ereignisse** verwendet werden:

   * **Attribute**: Profile, die in Atlanta, San Francisco oder Seattle leben und nach 1980 geboren wurden

      ![](../assets/add-attributes.png)

   * **Ereignisse**: Profile, die das Luma-Programm innerhalb der letzten 7 Tage geöffnet und innerhalb von 2 Stunden nach dem Öffnen eine Bestellung abgeschlossen haben.

      ![](../assets/add-events.png)

1. Wenn Sie dem Arbeitsbereich neue Felder hinzufügen und diese konfigurieren, wird der Bereich **[!UICONTROL Segmenteigenschaften]** automatisch mit Informationen zum geschätzten Bestand an Profilen dieses Segments aktualisiert.

   ![](../assets/segment-estimate.png)

1. Wenn das Segment fertig ist, klicken Sie auf **[!UICONTROL Speichern]**. Es wird nun in der Liste von Adobe Experience Platform-Segmenten angezeigt. Mithilfe der Suchleiste können Sie ein bestimmtes Segment in der Liste suchen.

Das Segment kann jetzt in Ihren Journeys verwendet werden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../segment/about-segments.md).

## Tutorial{#create-segment-video}

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
