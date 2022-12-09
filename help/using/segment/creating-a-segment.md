---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen eines Segments
description: Erfahren Sie, wie Sie Segmente erstellen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---

# Segmente erstellen {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="Regel erstellen"
>abstract="Mit der Methode zum Erstellen von Regeln können Sie mithilfe des Segmentierungsdienstes von Adobe Experience Platform eine neue Segmentdefinition erstellen."

In diesem Beispiel erstellen wir ein Segment, um alle Kunden in Atlanta, San Francisco oder Seattle anzusprechen, die nach 1980 geboren wurden. Alle diese Kunden hätten die Anwendung Luma innerhalb der letzten sieben Tage öffnen und dann innerhalb von 2 Stunden nach dem Öffnen der Anwendung einen Kauf tätigen sollen.

➡️ [In diesem Video erfahren Sie, wie Sie Segmente erstellen.](#video-segment)

1. Zugriff auf **[!UICONTROL Segments]** und klicken Sie auf das **[!UICONTROL Create segment]** Schaltfläche.

   ![](assets/create-segment.png)

   Im Bildschirm Segmentdefinition können Sie alle erforderlichen Felder konfigurieren, um Ihr Segment zu definieren. Erfahren Sie, wie Sie Segmente im [Dokumentation zum Segmentierungsdienst](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target=&quot;_blank&quot;}.

   ![](assets/segment-builder.png)

1. Im **[!UICONTROL Segment properties]** einen Namen und eine Beschreibung (optional) für das Segment angeben.

   ![](assets/segment-properties.png)

1. Ziehen Sie die gewünschten Felder aus dem linken Bereich in den mittleren Arbeitsbereich und konfigurieren Sie sie dann entsprechend Ihren Anforderungen.

   >[!NOTE]
   >
   >Beachten Sie, dass die im linken Bereich verfügbaren Felder je nach **XDM Individual Profile** und **XDM ExperienceEvent** -Schemata wurden für Ihre Organisation konfiguriert.  Weitere Informationen finden Sie unter [Dokumentation zum Experience-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.

   ![](assets/drag-fields.png)

   In diesem Beispiel müssen wir uns auf **Attribute** und **Veranstaltungen** -Felder zum Erstellen des Segments:

   * **Attribute**: Profile, die in Atlanta, San Francisco oder Seattle leben und nach 1980 geboren wurden

      ![](assets/add-attributes.png)

   * **Veranstaltungen**: Profile, die die Anwendung Luma innerhalb der letzten sieben Tage geöffnet haben, und dann innerhalb von 2 Stunden nach dem Öffnen der Anwendung einen Kauf tätigten.

      ![](assets/add-events.png)

1. Wenn Sie neue Felder im Arbeitsbereich hinzufügen und konfigurieren, wird die **[!UICONTROL Segment Properties]** automatisch mit Informationen zu den geschätzten Profilen aktualisiert, die zum Segment gehören.

   ![](assets/segment-estimate.png)

1. Sobald das Segment fertig ist, klicken Sie auf **[!UICONTROL Save]**. Sie wird in der Liste der Adobe Experience Platform-Segmente angezeigt. Beachten Sie, dass eine Suchleiste verfügbar ist, um Ihnen bei der Suche nach einem bestimmten Segment in der Liste zu helfen.

Das Segment kann jetzt in Ihren Journeys verwendet werden. Weitere Informationen hierzu finden Sie unter [diesem Abschnitt](../segment/about-segments.md).

## Anleitungsvideo{#video-segment}

Erfahren Sie, wie Sie Segmente erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
