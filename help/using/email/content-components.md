---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden von Inhaltskomponenten von E-Mail-Designer
description: Erfahren Sie, wie Sie Inhaltskomponenten in Ihren E-Mails verwenden
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: Komponenten, E-Mail-Designer, Editor, E-Mail
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '1383'
ht-degree: 99%

---

# Verwenden der Inhaltskomponenten des E-Mail-Designers {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components_email"
>title="Über Inhaltskomponenten"
>abstract="Inhaltskomponenten sind leere Platzhalter für Inhalt, die Sie zum Erstellen des E-Mail-Layouts verwenden können."

>[!CONTEXTUALHELP]
>id="ac_content_components_landing_page"
>title="Über Inhaltskomponenten"
>abstract="Inhaltskomponenten sind leere Platzhalter für Inhalte, mit denen Sie das Layout einer Landingpage erstellen können."

>[!CONTEXTUALHELP]
>id="ac_content_components_fragment"
>title="Über Inhaltskomponenten"
>abstract="Inhaltskomponenten sind leere Platzhalter für Inhalte, die Sie zum Erstellen eines Fragment-Layouts verwenden können."

>[!CONTEXTUALHELP]
>id="ac_content_components_template"
>title="Über Inhaltskomponenten"
>abstract="Inhaltskomponenten sind leere Platzhalter für Inhalte, die Sie zum Erstellen eines Vorlagen-Layouts verwenden können."

Bei der Erstellung von E-Mail-Inhalt ermöglichen **[!UICONTROL Inhaltskomponenten]** die Personalisierung Ihrer E-Mail mit unbearbeiteten Komponenten. Diese können nach dem Einfügen in eine E-Mail bearbeitet werden.

Sie können beliebig viele Strukturkomponenten zu einer oder mehreren Strukturkomponenten hinzufügen. Diese definieren das Layout Ihrer E-Mail.

## Hinzufügen von Inhaltskomponenten {#add-content-components}

Um zu Ihrer E-Mail Inhaltskomponenten hinzuzufügen und sie an Ihre Anforderungen anzupassen, führen Sie die folgenden Schritte aus.

1. Verwenden Sie zum Definieren des Layouts Ihrer E-Mail einen vorhandenen Inhalt im E-Mail-Designer oder platzieren Sie per Drag-and-Drop **[!UICONTROL Strukturkomponenten]** in leerem Inhalt.
[Weitere Informationen](content-from-scratch.md)

1. Um auf den Abschnitt **[!UICONTROL Inhaltskomponenten]** zuzugreifen, wählen Sie die entsprechende Schaltfläche im linken Fensterbereich des E-Mail-Designers aus.

   ![](assets/email_designer_content_components.png)

1. Platzieren Sie die Inhaltskomponenten Ihrer Wahl mittels Drag-and-Drop in den relevanten Strukturkomponenten.

   ![](assets/email_designer_add_content_components.png)

   >[!NOTE]
   >
   >Sie können zu einer einzelnen Strukturkomponente und zu jeder Spalte einer Strukturkomponente mehrere Komponenten hinzufügen.

1. Passen Sie die Stilattribute für jede Komponente im Bereich **[!UICONTROL Komponenteneinstellungen]** auf der rechten Seite an. Beispielsweise können Sie den Textstil, den Abstand oder den Rand jeder Komponente ändern. [Erfahren Sie mehr über Ausrichtung und Abstand](alignment-and-padding.md)

   ![](assets/email_designer_content_components_settings.png)

## Container {#container}

Sie können einen einfachen Container hinzufügen, in dem Sie eine weitere Inhaltskomponente hinzufügen können. Auf diese Weise können Sie einen bestimmten Stil auf den Container anwenden, der sich von der darin verwendeten Komponente unterscheidet.

Fügen Sie beispielsweise die Komponente **[!UICONTROL Container]** hinzu, und fügen Sie anschließend die Komponente [Schaltfläche](#button) innerhalb dieses Containers hinzu. Sie können einen bestimmten Hintergrund für den Container und einen anderen für die Schaltfläche verwenden.

![](assets/email_designer_container_component.png)

## Schaltfläche {#button}

Verwenden Sie die Komponente **[!UICONTROL Schaltfläche]**, um eine oder mehrere Schaltflächen in Ihre E-Mail einzufügen und Ihre E-Mail-Audience auf eine andere Seite weiterzuleiten.

1. Platzieren Sie in **[!UICONTROL Inhaltskomponenten]** die Komponente **[!UICONTROL Schaltfläche]** per Drag-and-Drop in eine **[!UICONTROL Strukturkomponente]**.

1. Klicken Sie auf die neu hinzugefügte Schaltfläche, um den Text anzupassen und auf die **[!UICONTROL Komponenteneinstellungen]** im rechten Bereich des E-Mail-Designers zugreifen zu können.

   ![](assets/email_designer_button_component.png)

1. Fügen Sie im Feld **[!UICONTROL Link]** die URL hinzu, zu der Sie Benutzende beim Anklicken der Schaltfläche umleiten möchten.

1. Wählen Sie mit der Dropdown-Liste **[!UICONTROL Zielgruppe]** aus, wie Ihre Audience umgeleitet werden soll:

   * **[!UICONTROL None]**: öffnet den Link in demselben Frame, in dem er angeklickt wurde (Standardwert).
   * **[!UICONTROL Blank]**: öffnet den Link in einem neuen Fenster oder auf einer neuen Registerkarte.
   * **[!UICONTROL Self]**: öffnet den Link in demselben Frame, in dem er angeklickt wurde.
   * **[!UICONTROL Parent]**: öffnet den Link im übergeordneten Frame.
   * **[!UICONTROL Top]**: öffnet den Link im gesamten Fenster.

   ![](assets/email_designer_button_link.png)

1. Sie können Ihre Schaltfläche weiter personalisieren, indem Sie Stilattribute wie etwa **[!UICONTROL Rahmen]**, **[!UICONTROL Größe]** und **[!UICONTROL Rand]** im Bereich **[!UICONTROL Komponenteneinstellungen]** ändern.

## Text {#text}

Verwenden Sie die Komponente **[!UICONTROL Text]**, um Text in Ihre E-Mail einzufügen und den Stil (Rahmen, Größe, Abstand usw.) im Bereich **[!UICONTROL Komponenteneinstellungen]** anzupassen.

![](assets/email_designer_text_component.png)

1. Platzieren Sie die Komponente **[!UICONTROL Text]** in **[!UICONTROL Inhaltskomponenten]** per Drag-and-Drop in eine **[!UICONTROL Strukturkomponente]**.

1. Klicken Sie auf die neu hinzugefügte Komponente, um den Text zu personalisieren und um Zugriff auf die **[!UICONTROL Komponenteneinstellungen]** im rechten Fenster des E-Mail-Designers zu erhalten.


1. Ändern Sie den Text mit folgenden Optionen in der Symbolleiste:

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Textstil ändern]**: Anwendung von Fett, Kursiv, Unterstrichen oder Durchgestrichen auf den Text.
   * **Ausrichtung ändern**: Auswahl von linker, rechter, zentrierter oder Blocksatz-Ausrichtung für Ihren Text.
   * **[!UICONTROL Liste erstellen]**: Einfügen einer Liste mit Aufzählungszeichen oder Nummerierung.
   * **[!UICONTROL Überschrift festlegen]**: Definition von bis zu sechs Überschriftsebenen in Ihrem Text.
   * **Schriftgröße**: Auswahl der Schriftgröße des Textes in Pixel.
   * **[!UICONTROL Bild bearbeiten]**: Einfügen eines Bildes oder Assets in Ihre Textkomponente. [Weitere Informationen über das Asset-Management](assets-essentials.md)
   * **[!UICONTROL Quellcode anzeigen]**: Anzeigen des Quell-Codes Ihres Textes (keine Änderungen möglich).
   * **[!UICONTROL Duplizieren]**: Hinzufügen einer Kopie Ihrer Textkomponente.
   * **[!UICONTROL Löschen]**: Entfernen einer ausgewählten Textkomponente aus Ihrer E-Mail.
   * **[!UICONTROL Personalisierung hinzufügen]**: Einfügen von Personalisierungsfeldern zur Inhaltsanpassung auf der Basis von Profildaten. [Weitere Informationen über die Personalisierung von Inhalten](../personalization/personalize.md)
   * **[!UICONTROL Bedingten Inhalt aktivieren]**: Fügen Sie bedingte Inhalte hinzu, um den Inhalt der Komponente an die Zielprofile anzupassen. [Erfahren Sie mehr über dynamische Inhalte](../personalization/get-started-dynamic-content.md)

1. Passen Sie die anderen Stilattribute wie Textfarbe, Schriftfamilie, Rahmen, Abstand, Rand usw. im Bedienfeld **[!UICONTROL Komponenteneinstellungen]** an.

## Trennlinie {#divider}

Verwenden Sie die Komponente **[!UICONTROL Trennlinie]**, um das Layout und den Inhalt Ihrer E-Mail durch eine Trennlinie zu strukturieren.

Sie können Stilattribute wie Linienfarbe, Stil und Höhe im Bedienfeld **[!UICONTROL Komponenteneinstellungen]** anpassen.

![](assets/email_designer_divider.png)

## HTML {#HTML}

Verwenden Sie die **[!UICONTROL HTML]**-Komponente, um die unterschiedlichen Teile Ihres vorhandenen HTML-Inhalts zu kopieren und einzufügen. Damit können Sie kostenlose modulare HTML-Komponenten erstellen, um externe Inhalte wiederzuverwenden.

1. Ziehen Sie die **[!UICONTROL HTML]**-Komponente in den **[!UICONTROL Inhaltskomponenten]** per Drag-and-Drop in eine **[!UICONTROL Strukturkomponente]**.

1. Klicken Sie auf die neu hinzugefügte Komponente und dann auf **[!UICONTROL Quellcode anzeigen]** in der kontextuellen Symbolleiste, um Ihren HTML-Code hinzuzufügen.

   ![](assets/email_designer_html_component.png)

1. Kopieren Sie den HTML-Code, den Sie Ihrer E-Mail hinzufügen möchten, und fügen Sie ihn ein, und klicken Sie auf **[!UICONTROL Speichern]**.

   ![](assets/email_designer_html_content.png)

>[!NOTE]
>
>Um die Kompatibilität von externem Inhalt mit dem E-Mail-Designer zu gewährleisten, empfiehlt Adobe, eine neue Nachricht zu erstellen und den Inhalt aus der existierenden E-Mail in Komponenten einzufügen.

## Bild {#image}

Verwenden Sie die Komponente **[!UICONTROL Bild]**, um eine Bilddatei von Ihrem Computer in Ihre E-Mail einzufügen.

1. Ziehen Sie die Komponente **[!UICONTROL Bild]** in den **[!UICONTROL Inhaltskomponenten]** per Drag-and-Drop in eine **[!UICONTROL Strukturkomponente]**.

1. Klicken Sie auf **[!UICONTROL Durchsuchen]**, um eine in Ihren Assets gespeicherte Bilddatei auszuwählen.

   Weitere Informationen zu [!DNL Assets Essentials] finden Sie in der [Dokumentation zu Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=de){target="_blank"}.

1. Klicken Sie auf die neu hinzugefügte Komponente und richten Sie Ihre Bildeigenschaften mithilfe des Bedienfelds **[!UICONTROL Komponenteneinstellungen]** ein:

   * **[!UICONTROL Bildtitel]** erlaubt Ihnen, den Titel für das Bild zu definieren.
   * Mit **[!UICONTROL Alt-Text]** legen Sie die Bildunterschrift fest. Dies entspricht dem HTML-Attribut „alt“.

   ![](assets/email_designer_10.png)

1. Passen Sie die anderen Stilattribute wie Rand, Rahmen usw. an. oder durch Hinzufügen eines Links zur Umleitung Ihrer Audience zu einem anderen Inhalt über das Bedienfeld **[!UICONTROL Komponenteneinstellungen]**.

## Video {#Video}

>[!CONTEXTUALHELP]
>id="ac_edition_video_email"
>title="Videoeinstellungen"
>abstract="Verwenden Sie diese Komponente, um ein Video in Ihre E-Mail einzufügen. Beachten Sie, dass Videos nicht auf allen E-Mail-Clients funktionieren. Wir empfehlen, ein Reservebild festzulegen."

>[!CONTEXTUALHELP]
>id="ac_edition_video_landing_page"
>title="Videoeinstellungen"
>abstract="Verwenden Sie diese Komponente, um zu Ihrer Landingpage ein Video hinzuzufügen. Beachten Sie, dass Videos nicht auf allen Nachrichten-Clients funktionieren. Wir empfehlen, ein Reservebild festzulegen."

>[!CONTEXTUALHELP]
>id="ac_edition_video_fragment"
>title="Videoeinstellungen"
>abstract="Verwenden Sie diese Komponente, um ein Video in Ihr Fragment einzufügen. Beachten Sie, dass Videos nicht auf allen Nachrichten-Clients funktionieren. Wir empfehlen, ein Reservebild festzulegen."

>[!CONTEXTUALHELP]
>id="ac_edition_video_template"
>title="Videoeinstellungen"
>abstract="Verwenden Sie diese Komponente, um ein Video in Ihre Vorlage einzufügen. Beachten Sie, dass Videos nicht auf allen Nachrichten-Clients funktionieren. Wir empfehlen, ein Reservebild festzulegen."

Verwenden Sie die Komponente **[!UICONTROL Video]**, um über einen URL-Link ein Video in Ihre E-Mail einzufügen.

1. Ziehen Sie die Komponente **[!UICONTROL Video]** aus den **[!UICONTROL Inhaltskomponenten]** per Drag-and-Drop in eine **[!UICONTROL Strukturkomponente]**.

   ![](assets/email_designer_17.png)

1. Klicken Sie auf die neu hinzugefügte Komponente.

1. Gegben Sie in das Feld **[!UICONTROL Video-Link]** des Bedienfelds **[!UICONTROL Komponenteneinstellungen]** Ihre Video-URL ein.

   ![](assets/email_designer_18.png)

1. Sie können dem Video ein **[!UICONTROL Standbild]** hinzufügen, das angezeigt wird, bis Ihre Audience auf die Wiedergabe-Schaltfläche klickt.

1. Passen Sie die anderen Stilattribute wie Stil, Rand, Rahmen usw. an. über das Bedienfeld **[!UICONTROL Komponenteneinstellungen]**.

## Social Media {#social}

Verwenden Sie die Komponente **[!UICONTROL Social]**, um Links zu Social-Media-Seiten in Ihre E-Mail einzufügen.

1. Ziehen Sie die Komponente **[!UICONTROL Social]** von den **[!UICONTROL Inhaltskomponenten]** in eine **[!UICONTROL Strukturkomponente]**.

1. Klicken Sie auf die neu hinzugefügte Komponente.

1. Im Feld **[!UICONTROL Social]** der **[!UICONTROL Komponenteneinstellungen]** können Sie auswählen, welche Social Media Sie hinzufügen oder entfernen möchten.

   ![](assets/email_designer_20.png)

1. Wählen Sie die Größe Ihrer Symbole im entsprechenden Feld aus.

1. Klicken Sie auf jedes Ihrer Social-Media-Symbole, um die **[!UICONTROL URL]** zu konfigurieren, zu der Ihre Audience weitergeleitet wird.

   ![](assets/email_designer_21.png)

1. Bei Bedarf können Sie auch die Symbole der einzelnen Social Media im Feld **[!UICONTROL Bild]** ändern.

1. Passen Sie die anderen Stilattribute wie Stil, Rand, Rahmen usw. an. über das Bedienfeld **[!UICONTROL Komponenteneinstellungen]**.

## Angebotsentscheidung {#offer-decision}

Verwenden Sie die Komponente **[!UICONTROL Angebotsentscheidung]**, um Angebote in Ihre Nachrichten einzufügen. Die [Entscheidungs-Management](../offers/get-started/starting-offer-decisioning.md)-Engine wählt das beste Angebot aus, das Sie Ihren Kunden unterbreiten können.

Weitere Informationen dazu, wie Sie einer E-Mail personalisierte Angebote hinzufügen können, finden Sie in [diesem Abschnitt](add-offers-email.md).

