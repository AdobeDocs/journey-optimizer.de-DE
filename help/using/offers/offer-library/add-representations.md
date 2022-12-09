---
title: Hinzufügen von Darstellungen zu Angeboten
description: Erfahren Sie, wie Sie Ihren Angeboten Darstellungen hinzufügen.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 0%

---

# Hinzufügen von Darstellungen zu Angeboten {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="Darstellungen"
>abstract="Fügen Sie Darstellungen hinzu, um festzulegen, wo Ihr Angebot in der Nachricht angezeigt werden soll. Je mehr Darstellungen ein Angebot hat, desto mehr Möglichkeiten gibt es, das Angebot in verschiedenen Platzierungskontexten zu verwenden."

Ein Angebot kann an verschiedenen Stellen in einer Nachricht angezeigt werden: in einem oberen Banner mit einem Bild, als Text in einem Absatz, als HTML-Block usw. Je mehr Darstellungen ein Angebot hat, desto mehr Möglichkeiten gibt es, das Angebot in verschiedenen Platzierungskontexten zu verwenden.

## Angebotsdarstellungen konfigurieren {#representations}

Gehen Sie wie folgt vor, um eine oder mehrere Darstellungen zu Ihrem Angebot hinzuzufügen und sie zu konfigurieren.

1. Wählen Sie für die erste Darstellung zunächst die **[!UICONTROL Channel]** verwendet wird.

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >Nur die verfügbaren Platzierungen für den ausgewählten Kanal werden im **[!UICONTROL Placement]** Dropdown-Liste.

1. Wählen Sie eine Platzierung aus der Liste aus.

   Sie können auch die Schaltfläche neben dem **[!UICONTROL Placement]** Dropdownliste, um alle Platzierungen zu durchsuchen.

   ![](../assets/browse-button-placements.png)

   Dort können Sie die Platzierungen nach Kanal und/oder Inhaltstyp filtern. Wählen Sie eine Platzierung aus und klicken Sie auf **[!UICONTROL Select]**.

   ![](../assets/browse-placements.png)

1. Fügen Sie Ihrer Darstellung Inhalt hinzu. Erfahren Sie mehr über [diesem Abschnitt](#content).

1. Wenn Sie Inhalte wie ein Bild oder eine URL hinzufügen, können Sie eine **[!UICONTROL Destination link]**: die Benutzer, die auf das Angebot klicken, werden zur entsprechenden Seite weitergeleitet.

   ![](../assets/offer-destination-link.png)

1. Wählen Sie abschließend die Sprache Ihrer Wahl aus, um zu ermitteln und zu verwalten, welche Inhalte den Benutzern angezeigt werden sollen.

1. Um eine weitere Darstellung hinzuzufügen, verwenden Sie die **[!UICONTROL Add representation]** und fügen Sie beliebig viele Darstellungen hinzu.

   ![](../assets/offer-add-representation.png)

1. Nachdem Sie alle Ihre Darstellungen hinzugefügt haben, wählen Sie **[!UICONTROL Next]**.

## Inhalte für Ihre Darstellungen definieren {#content}

Sie können einer Darstellung verschiedene Inhaltstypen hinzufügen.

>[!NOTE]
>
>Es können nur Inhalte verwendet werden, die dem Inhaltstyp der Platzierung entsprechen.

### Bilder hinzufügen {#images}

Wenn es sich bei der ausgewählten Platzierung um einen Bildtyp handelt, können Sie Inhalte aus der **Adobe Experience Cloud-Asset** Bibliothek, ein zentralisiertes Repository von Assets, die von [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> So arbeiten Sie mit [Grundlagen zu Adobe Experience Manager Assets](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target=&quot;_blank&quot;}, müssen Sie [!DNL Assets Essentials] für Ihre Organisation verwenden und sicherstellen, dass Benutzer Teil der **Assets Essentials Consumer Users** oder/und **Assets Essentials-Benutzer** Produktprofile. Weitere Informationen finden Sie unter [diese Seite](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html){target=&quot;_blank&quot;}.

1. Wählen Sie die **[!UICONTROL Asset library]** -Option.

1. Auswählen **[!UICONTROL Browse]**.

   ![](../assets/offer-browse-asset-library.png)

1. Durchsuchen Sie die Assets, um das Bild Ihrer Wahl auszuwählen.

1. Klicken **[!UICONTROL Select]**.

   ![](../assets/offer-select-asset.png)

### HTML- oder JSON-Dateien hinzufügen {#html-json}

Wenn es sich bei der ausgewählten Platzierung um HTML-Inhalt handelt, können Sie auch HTML- oder JSON-Inhalte aus der [Adobe Experience Cloud-Asset-Bibliothek](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target=&quot;_blank&quot;}).

Sie haben beispielsweise eine HTML-E-Mail-Vorlage in [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target=&quot;_blank&quot;} und Sie möchten diese Datei für Ihren Angebotsinhalt verwenden. Anstatt eine neue Datei zu erstellen, können Sie die Vorlage einfach in die **Asset-Bibliothek** , um sie in den Darstellungen Ihres Angebots wiederverwenden zu können.

Um Ihren Inhalt in einer Darstellung wiederzuverwenden, navigieren Sie zum **Asset-Bibliothek** wie in [diesem Abschnitt](#images) und wählen Sie die gewünschte HTML- oder JSON-Datei aus.

![](../assets/offer-browse-asset-library-json.png)

### URLs hinzufügen {#urls}

Um Inhalte von einem externen öffentlichen Speicherort hinzuzufügen, wählen Sie **[!UICONTROL URL]** und geben Sie dann die URL-Adresse des hinzuzufügenden Inhalts ein.

![](../assets/offer-content-url.png)

### Hinzufügen von benutzerdefiniertem Text {#custom-text}

Sie können auch Textinhalte einfügen, wenn Sie eine kompatible Platzierung auswählen.

1. Wählen Sie die **[!UICONTROL Custom]** und klicken Sie auf **[!UICONTROL Add content]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >Diese Option ist nicht für Platzierungen vom Typ Bild verfügbar.

1. Geben Sie den Text ein, der im Angebot angezeigt werden soll.

   ![](../assets/offer-text-content.png)

   Sie können Ihren Inhalt mit dem Ausdruckseditor personalisieren. Weitere Informationen finden Sie unter [Personalisierung](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >Nur die **[!UICONTROL Profile attributes]**, **[!UICONTROL Segment memberships]** und **[!UICONTROL Helper functions]** -Quellen sind für die Entscheidungsverwaltung verfügbar.

