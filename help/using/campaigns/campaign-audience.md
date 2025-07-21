---
solution: Journey Optimizer
product: journey optimizer
title: Definieren der Aktionskampagnen-Audience
description: Erfahren Sie, wie Sie die Audience der Aktionskampagne definieren.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: Erstellen, Optimizer, Kampagne, Oberfläche, Nachrichten
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 53%

---


# Definieren der Aktionskampagnen-Audience {#action-campaign-audience}

Definieren Sie auf **[!UICONTROL Registerkarte]** Audience“ die Kampagnentität.

![](assets/campaign-audience.png)

1. **Zielgruppe auswählen**

   Klicken Sie bei Marketing-Kampagnen auf die Schaltfläche **[!UICONTROL Zielgruppe auswählen]**, um die Liste der verfügbaren Adobe Experience Platform-Zielgruppen anzuzeigen. [Weitere Informationen zu Zielgruppen](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >Zielgruppen und Attribute aus der [Zielgruppenkomposition](../audience/get-started-audience-orchestration.md) stehen derzeit nicht zur Verwendung mit Healthcare Shield oder Privacy und Security Shield zur Verfügung

1. **Identitätstyp auswählen**

   Wählen Sie im Feld **[!UICONTROL Identitätstyp]** den Schlüsseltyp aus, der zur Identifizierung der Kontakte in der ausgewählten Zielgruppe verwendet werden soll. Sie können entweder einen vorhandenen Identitätstyp verwenden oder mit dem Identity Service einen neuen erstellen. Standardmäßige Identity-Namespaces werden auf [dieser Seite](https://experienceleague.adobe.com/de/docs/experience-platform/identity/features/namespaces#standard){target="_blank"} aufgeführt.

   Pro Kampagne ist nur ein Identitätstyp zulässig. Kontakte, die zu einem Segment gehören, das nicht den ausgewählten Identitätstyp unter den verschiedenen Identitäten hat, können nicht von der Kampagne angesprochen werden. Weitere Informationen zu Identitätstypen und Namespaces sind in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=de){target="_blank"} verfügbar.

## Nächste Schritte {#next}

Sobald die Audience Ihrer Aktionskampagne fertig ist, können Sie die Kampagne planen. [Weitere Informationen](campaign-schedule.md)
