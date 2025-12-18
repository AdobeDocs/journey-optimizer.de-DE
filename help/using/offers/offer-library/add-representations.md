---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Hinzufügen von Darstellungen zu Angeboten
description: Erfahren Sie, wie Sie Darstellung zu Ihren Angebote hinzufügen können
badge: label="Legacy" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Hinzufügen von Darstellungen zu Angeboten {#add-representations}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../experience-decisioning/gs-experience-decisioning.md)

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="Darstellungen"
>abstract="Fügen Sie Darstellungen hinzu, um festzulegen, wo in einer Nachricht Ihr Angebot angezeigt werden soll. Je mehr Darstellungen ein Angebot hat, desto mehr Möglichkeiten gibt es, das Angebot in verschiedenen Platzierungskontexten zu verwenden."

Ein Angebot kann in einer Nachricht an verschiedenen Stellen angezeigt werden: in einem oberen Banner mit einem Bild, als Text in einem Absatz, als HTML-Block usw. Je mehr Darstellungen ein Angebot hat, desto mehr Möglichkeiten gibt es, das Angebot in verschiedenen Platzierungskontexten zu verwenden.

## Konfigurieren der Darstellungen des Angebots {#representations}

Gehen Sie wie folgt vor, um eine oder mehrere Darstellungen zu Ihrem Angebot hinzuzufügen und sie zu konfigurieren.

1. Wählen Sie für die erste Darstellung zunächst den zu verwendenden **[!UICONTROL Kanal]** aus.

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >Nur die verfügbaren Platzierungen für den ausgewählten Kanal werden in der Dropdown-Liste **[!UICONTROL Platzierung]** angezeigt.

1. Wählen Sie eine Platzierung aus der Liste aus.

   Sie können auch den Button neben der Dropdown-Liste **[!UICONTROL Platzierung]** verwenden, um alle Platzierungen zu durchsuchen.

   ![](../assets/browse-button-placements.png)

   Dort können Sie die Platzierungen nach Kanal und/oder Content-Typ filtern. Wählen Sie eine Platzierung aus und klicken Sie auf **[!UICONTROL Auswahl]**.

   ![](../assets/browse-placements.png)

1. Fügen Sie für Ihre Darstellung Inhalte hinzu. Mehr dazu erfahren Sie in [diesem Abschnitt](#content).

1. Wenn Sie Inhalte wie ein Bild oder eine URL hinzufügen, können Sie einen **[!UICONTROL Ziel-Link]** angeben: Die Benutzer, die auf das Angebot klicken, werden zur entsprechenden Seite weitergeleitet.

   ![](../assets/offer-destination-link.png)

1. Wählen Sie abschließend eine Sprache, um zu bestimmen, welche Inhalte den Benutzern angezeigt werden sollen.

1. Um eine weitere Darstellung hinzuzufügen, verwenden Sie die Schaltfläche **[!UICONTROL Darstellung hinzufügen]** und fügen Sie beliebig viele Darstellungen hinzu.

   ![](../assets/offer-add-representation.png)

1. Nachdem Sie alle Darstellungen hinzugefügt haben, klicken Sie auf **[!UICONTROL Weiter]**.

## Inhalte für Ihre Darstellungen definieren {#content}

Sie können einer Darstellung verschiedene Inhaltstypen hinzufügen.

>[!NOTE]
>
>Es sind nur Inhalte verfügbar, die dem Content-Typ der Platzierung entsprechen.

### Bilder hinzufügen {#images}

Wenn es sich bei der ausgewählten Platzierung um einen Bildtyp handelt, können Sie Inhalte aus der **Adobe Experience Cloud Assets**-Bibliothek hinzufügen, einem zentralen Repository mit Assets, das von [!DNL Adobe Experience Manager Assets] bereitgestellt wird.

>[!NOTE]
>
> Um [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=de){target="_blank"} verwenden zu können, müssen Sie für Ihr Unternehmen [!DNL Assets Essentials] bereitstellen und sicherstellen, dass die Benutzenden Teil der Produktprofile **Assets Essentials-Endbenutzende** und/oder **Assets Essentials-Benutzende** sind. Erfahren Sie mehr über [diese Seite](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html?lang=de){target="_blank"}.

1. Wählen Sie die Option **[!UICONTROL Assets-Bibliothek]** aus.

1. Klicken Sie auf **[!UICONTROL Durchsuchen]**.

   ![](../assets/offer-browse-asset-library.png)

1. Durchsuchen Sie die Assets, um das Bild Ihrer Wahl auszuwählen.

1. Klicken Sie auf **[!UICONTROL Auswählen]**.

   ![](../assets/offer-select-asset.png)

### Hinzufügen von HTML- oder JSON-Dateien {#html-json}

Wenn die ausgewählte Platzierung vom Typ HTML ist, können Sie auch HTML- oder JSON-Inhalte aus der [Adobe Experience Cloud Asset-Bibliothek](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=de){target="_blank"} hinzufügen.

Sie haben zum Beispiel eine HTML-E-Mail-Vorlage in [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html?lang=de){target="_blank"} erstellt und möchten diese Datei für den Inhalt Ihres Angebots verwenden. Anstatt eine neue Datei zu erstellen, können Sie die Vorlage einfach in die **Asset-Bibliothek** hochladen, um sie für unterschiedliche Darstellungsvarianten Ihres Angebots wiederverwenden zu können.

Um Ihre Inhalte in einer Darstellung wiederzuverwenden, gehen Sie zur **Asset-Bibliothek**, wie in [diesem Abschnitt](#images) beschrieben, und wählen Sie die gewünschte HTML- oder JSON-Datei aus.

![](../assets/offer-browse-asset-library-json.png)

### URLs hinzufügen {#urls}

Um Inhalte von einem externen öffentlichen Speicherort hinzuzufügen, klicken Sie auf **[!UICONTROL URL]** und geben Sie dann die URL-Adresse des hinzuzufügenden Inhalts ein.

Sie können URLs mit dem Personalisierungseditor personalisieren. Erhalten Sie mehr über [Personalisierung](../../personalization/personalize.md#use-expression-editor). 

![](../assets/offer-content-url.png)

Sie möchten zum Beispiel das Bild, das als Angebot angezeigt wird, personalisieren. Sie möchten, dass Benutzende, die einen Stadturlaub bevorzugen, die Skyline von New York sehen und Benutzende, die einen Strandurlaub bevorzugen, die Nordküste von Hawaii sehen.

Verwenden Sie den Personalisierungseditor unter Verwendung von Vereinigungsschemata, um Profilattribute abzurufen, die in Adobe Experience Platform gespeichert sind. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schemas-overview.html?lang=de){target="_blank"}

![](../assets/offer-content-url-personalization.png)

Wenn Sie einen **[!UICONTROL Ziel-Link]** angeben, können Sie auch die URL personalisieren, zu der die Benutzenden, die auf das Angebot klicken, geleitet werden.

### Hinzufügen von benutzerdefiniertem Text {#custom-text}

Sie können auch Textinhalte einfügen, wenn Sie eine kompatible Platzierung auswählen.

1. Wählen Sie die Option **[!UICONTROL Benutzerdefiniert]** aus und klicken Sie auf **[!UICONTROL Inhalt hinzufügen]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >Bei Platzierungen vom Typ „Bild“ ist diese Option nicht verfügbar.

1. Geben Sie den Text ein, der im Angebot angezeigt werden soll.

   ![](../assets/offer-text-content.png)

   Sie können Ihre Inhalte mit dem Personalisierungseditor personalisieren.  Erhalten Sie mehr über [Personalisierung](../../personalization/personalize.md#use-expression-editor). 

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >Nur die Quellen **[!UICONTROL Profilattribute]**, **[!UICONTROL Zielgruppen]** und **[!UICONTROL Helper-Funktionen]** sind für das Entscheidungs-Management verfügbar.

## Personalisieren von Darstellungen basierend auf Kontextdaten{#context-data}

Wenn Kontextdaten im Aufruf von [Edge Decisioning](../api-reference/offer-delivery-api/edge-decisioning-api.md) übergeben werden, können Sie diese Daten nutzen, um Darstellungen dynamisch zu personalisieren. Sie können beispielsweise die Darstellung eines Angebots auf Basis von Echtzeitfaktoren wie aktuellen Wetterbedingungen zum Zeitpunkt der Entscheidungsfindung anpassen.

Um Kontextdaten in Angebotsdarstellungen zu verwenden, binden Sie die Kontextdatenvariable direkt in den Inhalt der Darstellung ein, indem Sie den Namespace `profile.timeSeriesEvents.` verwenden.

Im Folgenden finden Sie ein Syntaxbeispiel, mit dem die Darstellung eines Angebots basierend auf den Betriebssystemen der Benutzenden personalisiert wird:

```
 {%#if profile.timeSeriesEvents.device.model = "Apple"%}ios{%else%}android{%/if%} 
```

Die entsprechende Edge Decisioning-Anfrage einschließlich der Kontextdaten lautet wie folgt:

```
{
    "body": {
        "xdm": {
            "identityMap": {
                "Email": [
                    {
                        "id": "xyz@abc.com"
                    }
                ]
            },
            "device": {
                "model": "Apple"
            }
        },
        "extra": {
            "query": {
                "decisionScopes": [
                    "eyJ4ZG06..."
                ]
            }
        }
    }
}
```
