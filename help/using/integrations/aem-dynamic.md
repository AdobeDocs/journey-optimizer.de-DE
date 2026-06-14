---
solution: Journey Optimizer
product: journey optimizer
title: Dynamic Media
description: Verwenden von Dynamic Media mit Journey Optimizer
topic: Content Management
role: User
level: Beginner
exl-id: 3e777cc5-a935-4e68-9de7-60b241e78f63
TQID: https://experienceleague.adobe.com/bgBuZlYcuJ1VpBZIlpGA4WIYZ6ufqNMnxlBoUvPpVqg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: d095671a-1355-40aa-8b5f-06c33c68080bid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 6dbdae6edd95d97e039565ed5c6e3cab9f4a19d8
workflow-type: tm+mt
source-wordcount: 1160
ht-degree: 93%

---

# Arbeiten mit Dynamic Media {#aem-dynamic}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Adobe Experience Manager Dynamic Media, einschließlich Textüberlagerungen und Dynamic Media-Vorlagen, in Journey Optimizer-Inhalte einfügen, anpassen und personalisieren.

>[!ENDSHADEBOX]

## Erste Schritte mit Dynamic Media {#gs-aem-dynamic}

Die Asset-Auswahl unterstützt nun Dynamic Media, sodass Sie genehmigte Dynamic Media-Ausgabedarstellungen in Journey Optimizer nahtlos auswählen und verwenden können. Änderungen an Assets in Adobe Experience Manager werden sofort in Ihren Journey Optimizer-Inhalten übernommen. Es werden also stets die aktuellen Versionen verwendet, ohne dass manuelle Aktualisierungen erforderlich sind.

Beachten Sie, dass diese Integration nur für Kundschaft verfügbar ist, die Dynamic Media Manager as a Cloud Service nutzt.

Weitere Informationen zu Dynamic Media in Adobe Experience Manager as a Cloud Service finden Sie in der [Dokumentation zu Experience Manager](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media){target="_blank"}.

>[!AVAILABILITY]
>
>Für Kundinnen und Kunden im Gesundheitswesen wird die Integration nur bei einer Lizenzierung der Add-on-Angebote Journey Optimizer Healthcare Shield und Adobe Experience Manager Extended Security for Healthcare aktiviert.


## Hinzufügen und Verwalten von Dynamic Media {#dynamic-media}


Verbessern und optimieren Sie Ihre Inhalte für jeden Bildschirm oder Browser, indem Sie dynamische Medien aus Adobe Experience Manager as a Cloud Service direkt in Ihre Journey Optimizer-Inhalte einfügen.  Anschließend können Sie bei Bedarf die Größe ändern, zuschneiden, Verbesserungen und andere Anpassungen vornehmen.


>[!IMPORTANT]
>
>Dynamic Media mit OpenAPI muss in Adobe Experience Manager as a Cloud Service aktiviert sein. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/dynamic-media-open-apis-overview#enable-dynamic-media-open-apis){target="_blank"}.

Die Dynamic Media-Integration mit Adobe Journey Optimizer ist sowohl für den [Scene7-Modus](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/assets/dynamic/config-dms7){target="_blank"} von Dynamic Media als auch [mit OpenAPI](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/dynamic-media-open-apis-overview){target="_blank"} verfügbar.

<!--
>[!AVAILABILITY]
>
>Older versions of Outlook (including 2016) do not support rendering of content with Dynamic Media.  We are actively working on a permanent fix to enhance compatibility. In the meantime, apply the following guidelines:
>
>* For Dynamic Media Scene7 URLs: Append `?bfc=on` to the image URL. This enables automatic format negotiation, ensuring the most compatible image format is delivered based on the client's capabilities.
>
>* For Dynamic Media with Open API: Use the `.avif` format. This format includes built-in fallback mechanisms to deliver a compatible format when necessary.
>
-->

Gehen Sie wie folgt vor, um ein Adobe Experience Manager-Asset zu Ihrem HTML-Inhalt hinzuzufügen:

1. Ziehen Sie eine **[!UICONTROL HTML-Komponente]** per Drag-and-Drop in Ihren Inhalt.

1. Wählen Sie **[!UICONTROL Quell-Code anzeigen]** aus.

   ![](assets/dynamic-media-1.png)

1. Navigieren Sie im Menü **[!UICONTROL HTML bearbeiten]** zu **[!UICONTROL Assets]** und klicken Sie dann auf **[!UICONTROL Asset-Auswahl öffnen]**.

   Alternativ können Sie die URL Ihres Assets kopieren und einfügen.

   ![](assets/dynamic-media-2.png)

1. Durchsuchen Sie Ihre AEM-Assets und wählen Sie das Asset aus, das zu Ihren Inhalten hinzugefügt werden soll.

1. Passen Sie die Bildparameter an (z. B. Höhe, Breite, Drehen, Spiegeln, Helligkeit, Farbton usw.) nach Bedarf, um Ihre Asset-Anforderungen zu erfüllen.

   Eine umfassende Liste der Bildparameter, die der URL hinzugefügt werden können, finden Sie in der [Dokumentation zu Experience Manager](https://experienceleague.adobe.com/de/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/c-command-reference){target="_blank"}.

   ![](assets/dynamic-media-3.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Ihr Inhalt enthält jetzt dynamische Medien. Alle Aktualisierungen, die Sie in Experience Manager vornehmen, werden automatisch in Journey Optimizer angezeigt.

## Personalisieren von Textüberlagerungen {#text-overlay}

Passen Sie dynamische Medien einfach an, indem Sie die vorhandene Textüberlagerung durch neuen Text Ihrer Wahl ersetzen, was nahtlose Aktualisierungen und Personalisierungen ermöglicht.

Beispielsweise können Sie mithilfe der Experimentierfunktion die vorhandene Textüberlagerung aktualisieren, indem Sie sie für jede Abwandlung durch anderen Text ersetzen und sicherstellen, dass sie beim Öffnen einer Nachricht für jedes Profil angepasst wird.

![](assets/dynamic-media-layout-1.png)

>[!AVAILABILITY]
>
>Die **Personalisierung von Textüberlagerungen** ist ausschließlich im [Scene7-Modus](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/assets/dynamic/config-dms7){target="_blank"} von Dynamic Media verfügbar. Da der Scene7-Modus für Kundinnen und Kunden im Gesundheitswesen nicht verfügbar ist, werden Inhalte mithilfe einer Binärkopie des Bildes aus Journey Optimizer gerendert. Wenden Sie sich bei Ausnahmen an den Adobe-Support.

Gehen Sie wie folgt vor, um Ihre Textüberlagerung zu personalisieren:

1. Ziehen Sie eine **[!UICONTROL HTML-Komponente]** per Drag-and-Drop in Ihren Inhalt.

1. Wählen Sie **[!UICONTROL Quell-Code anzeigen]** aus.

1. Greifen Sie über das Menü **[!UICONTROL HTML bearbeiten]** auf **[!UICONTROL Assets]** und dann auf **[!UICONTROL Asset-Auswahl öffnen]** zu.

   Sie können Ihre Assets-URL auch einfach kopieren und einfügen.

1. Durchsuchen Sie Ihre AEM-Assets und wählen Sie das Asset aus, das zu Ihren Inhalten hinzugefügt werden soll.

1. Ersetzen Sie die Überlagerung durch den gewünschten Text.

   ![](assets/do-not-localize/dynamic_media_layout.gif)

1. Aktualisieren Sie die Bildparameter:

   * **Layer**: Geben Sie das Basiselement ein, in dem der Text platziert wird.
   * **Size**: Aktualisieren Sie die Größe des Textblocks.
   * **TextAttr**: Passen Sie die Größe der Textschrift an.
   * **Pos**: Legen Sie die Position des Textes im Bild.

   >[!WARNING]
   >
   >Der Parameter „Layer“ ist erforderlich, um die dynamischen Medien zu aktualisieren.

   ![](assets/dynamic-media-layout-2.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Ihr Inhalt enthält jetzt Ihre aktualisierte Textüberlagerung.

![](assets/dynamic-media-layout-3.png)

## Hinzufügen und Verwalten der Dynamic Media-Vorlage {#dynamic-media-template}

Fügen Sie ganz einfach Ihre Dynamic Media-Vorlage in Journey Optimizer hinzu und aktualisieren Sie Ihre Medieninhalte bei Bedarf. Sie können jetzt Personalisierungsfelder in Ihre Medien integrieren, sodass Sie in Journey Optimizer benutzerfreundlichere und ansprechendere Inhalte erstellen können.

Erfahren Sie mehr über [Dynamic Media-Vorlagen](https://experienceleague.adobe.com/de/docs/dynamic-media-classic/using/template-basics/quick-start-template-basics){target="_blank"}.


>[!AVAILABILITY]
>
>Die **Dynamic Media-Vorlage** ist ausschließlich im [Scene7-Modus](https://experienceleague.adobe.com/de/docs/experience-manager-65/content/assets/dynamic/config-dms7) von Dynamic Media verfügbar. Da der Scene7-Modus für Kundinnen und Kunden im Gesundheitswesen nicht verfügbar ist, werden Inhalte nicht gerendert. Wenden Sie sich bei Ausnahmen an den Experience Manager-Support.


### Mit Bildkomponente {#image-component}

Sie können Ihre dynamische Vorlage mithilfe der Bildkomponente direkt in Ihren Inhalt einfügen:

1. Öffnen Sie Ihre Kampagne oder Journey und greifen Sie auf Ihre Inhalte zu.

1. Ziehen Sie eine **Bildkomponente** per Drag-and-Drop in Ihr Layout.

   Weitere Informationen zur Bildkomponente finden Sie auf [dieser Seite](../email/content-components.md).

   ![](assets/dynamic-media-template-1.png)

1. Durchsuchen Sie Ihre AEM-Assets und wählen Sie die Dynamic Media-Vorlage aus, die zu Ihren Inhalten hinzugefügt werden soll.

   ![](assets/dynamic-media-template-2.png)

1. Navigieren Sie zu den **Bildeinstellungen**, um auf die Parameter Ihrer Dynamic Media-Vorlage zuzugreifen.

   Die verfügbaren Felder hängen von den Parametern ab, die während der [Vorlagenerstellung](https://experienceleague.adobe.com/de/docs/dynamic-media-classic/using/template-basics/creating-template-parameters#creating_template_parameters){target="_blank"} in Adobe Experience Manager hinzugefügt wurden.

   ![](assets/dynamic-media-template-3.png)

1. Füllen Sie die verschiedenen Felder aus und verwenden Sie den Personalisierungseditor, um personalisierte Inhalte hinzuzufügen. Sie können ein beliebiges Attribut verwenden, z. B. Profilname, Stadt oder andere relevante Details, um ein benutzerfreundlicheres Erlebnis zu schaffen.

   Weitere Informationen zur Personalisierung finden Sie auf [dieser Seite](../personalization/personalize.md).

   ![](assets/do-not-localize/dynamic_media_template.gif)

1. Bedingte Inhalte können auf die Dynamic Media-Komponente angewendet werden, um verschiedene Inhaltsvarianten zu generieren. [Weitere Informationen](../personalization/dynamic-content.md)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Sobald Sie Ihre Tests durchgeführt und den Inhalt validiert haben, können Sie Ihre Nachricht an Ihre Zielgruppe senden.

### Mit HTML-Komponente {#html-component}

Sie können Ihre dynamische Vorlage mithilfe der HTML-Komponente direkt in Ihren Inhalt einfügen:

1. Öffnen Sie Ihre Kampagne oder Journey und greifen Sie auf Ihre Inhalte zu.

1. Ziehen Sie eine **HTML-Komponente** per Drag-and-Drop in Ihr Layout.

   ![](assets/dynamic-media-template-4.png)

1. Wählen Sie **[!UICONTROL Quell-Code anzeigen]** aus.

   ![](assets/dynamic-media-template-5.png)

1. Greifen Sie über das Menü **[!UICONTROL HTML bearbeiten]** auf **[!UICONTROL Assets]** und dann auf **[!UICONTROL Asset-Auswahl öffnen]** zu.

   Sie können Ihre Assets-URL auch einfach kopieren und einfügen.

1. Passen Sie die Bildtextparameter nach Bedarf an Ihre Asset-Anforderungen an.

   ![](assets/do-not-localize/dynamic_media_template_html.gif)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Sobald Sie Ihre Tests durchgeführt und den Inhalt validiert haben, können Sie Ihre Nachricht an Ihre Zielgruppe senden.

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie Adobe Experience Manager Dynamic Media mit Adobe Journey Optimizer integrieren, um eine Aktualisierung und Personalisierung von Inhalten in Echtzeit zu ermöglichen.

In diesem Tutorial wird beschrieben, wie Sie Bilder direkt in AJO ändern, im HTML-Modus Textüberlagerungen hinzufügen, Dynamic Media-Vorlagen in AEM zur Hyperpersonalisierung erstellen und Kampagnen personalisieren, indem Sie Inhalte auf verschiedene Zielgruppensegmente zuschneiden. Diese Integration ermöglicht es Marketing-Fachleuten, ansprechende und personalisierte Kampagnen effizient zu erstellen, ohne zwischen Anwendungen wechseln zu müssen.

>[!VIDEO](https://video.tv.adobe.com/v/3457695/?learn=on&enablevpops=&autoplay=true)

