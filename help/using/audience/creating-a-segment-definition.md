---
solution: Journey Optimizer
product: journey optimizer
title: Segmentdefinitionen erstellen
description: Erfahren Sie, wie Sie Zielgruppen mithilfe von Segmentdefinitionen erstellen.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 37%

---

# Segmentdefinitionen erstellen {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="Erstellen einer Regel"
>abstract="Mit der Erstellungsmethode für Regeln erstellen können Sie eine neue Zielgruppendefinition mit dem Adobe Experience Platform-Zielgruppendienst erstellen."

In diesem Beispiel erstellen wir eine Zielgruppe, um alle Kunden in Atlanta, San Francisco oder Seattle anzusprechen, die nach 1980 geboren wurden. Alle diese Kunden sollten das Programm Luma innerhalb der letzten 7 Tage geöffnet und dann innerhalb von 2 Stunden nach dem Öffnen eine Bestellung abgeschlossen haben.

➡️ [In diesem Video erfahren Sie, wie Sie Audiences erstellen.](#video-segment)

1. Zugriff auf **[!UICONTROL Zielgruppen]** und klicken Sie auf das **[!UICONTROL Zielgruppe erstellen]** Schaltfläche.

   ![](assets/create-segment.png)

   Im Bildschirm Segmentdefinition können Sie alle erforderlichen Felder konfigurieren, um Ihre Audience zu definieren. Erfahren Sie, wie Sie Zielgruppen im [Dokumentation zum Segmentierungsdienst](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=de){target="_blank"}.

   ![](assets/segment-builder.png)

1. Im **[!UICONTROL Zielgruppeneigenschaften]** einen Namen und eine Beschreibung (optional) für die Zielgruppe angeben.

   ![](assets/segment-properties.png)

1. Ziehen Sie per Drag-and-Drop die gewünschten Felder aus dem linken Bereich in den mittleren Arbeitsbereich und konfigurieren Sie die Felder dann entsprechend Ihren Anforderungen.

   >[!NOTE]
   >
   >Beachten Sie, dass die Felder im linken Bereich je nach Konfiguration der Schemas **XDM Individual Profile** und **XDM ExperienceEvent** für Ihr Unternehmen abweichen.  Weitere Informationen finden Sie unter [Dokumentation zum Experience-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"}.

   ![](assets/drag-fields.png)

   In diesem Beispiel müssen wir uns auf **Attribute** und **Veranstaltungen** Felder zum Erstellen der Audience:

   * **Attribute**: Profile mit Wohnsitz in Atlanta, San Francisco oder Seattle und mit Geburtsjahr nach 1980

     ![](assets/add-attributes.png)

   * **Ereignisse**: Profile, die das Luma-Programm innerhalb der letzten 7 Tage geöffnet und innerhalb von 2 Stunden nach dem Öffnen eine Bestellung abgeschlossen haben.

     ![](assets/add-events.png)

1. Wenn Sie neue Felder im Arbeitsbereich hinzufügen und konfigurieren, wird die **[!UICONTROL Zielgruppeneigenschaften]** wird automatisch mit Informationen zu den geschätzten Profilen der Audience aktualisiert.

   ![](assets/segment-estimate.png)

1. Sobald die Audience fertig ist, klicken Sie auf **[!UICONTROL Speichern]**. Sie wird in der Liste der Adobe Experience Platform-Zielgruppen angezeigt. Beachten Sie, dass eine Suchleiste verfügbar ist, um Sie bei der Suche nach einer bestimmten Zielgruppe in der Liste zu unterstützen.

Die Audience kann jetzt in Ihren Journey verwendet werden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../audience/about-audiences.md).

## Anleitungsvideo{#video-segment}

Erfahren Sie, wie Sie Zielgruppen erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
