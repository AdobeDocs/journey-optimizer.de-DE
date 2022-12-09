---
title: Autoren-Webseiten
description: Erfahren Sie, wie Sie eine Webseite erstellen und ihren Inhalt in Journey Optimizer bearbeiten.
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 0%

---

# Autoren-Webseiten {#author-web}

>[!AVAILABILITY]
>
>Die Webkanalfunktion ist derzeit als Beta-Version verfügbar, über die nur Benutzer ausgewählt werden können.

In [!DNL Journey Optimizer] Die Webbearbeitung basiert auf der Chrome-Browsererweiterung Adobe Experience Cloud Visual Helper . [Weitere Infos](visual-editing-helper.md)

So können Sie auf Webseiten im [!DNL Journey Optimizer] Befolgen Sie die unter [diesem Abschnitt](create-web.md#prerequesites).

## Bearbeiten des Webseiteninhalts {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Geben Sie die zu bearbeitende URL ein"
>abstract="Geben Sie die URL einer bestimmten Webseite an, die zur Bearbeitung des Inhalts verwendet werden soll, der auf die oben definierte Weboberfläche angewendet wird. Die Webseite muss mit dem Adobe Experience Platform Web SDK implementiert werden."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html" text="Weitere Infos"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Geben Sie die zu bearbeitende URL ein"
>abstract="Geben Sie die URL einer bestimmten Webseite ein, die zur Bearbeitung des Inhalts verwendet werden soll. Diese Seite wird auf alle Seiten angewendet, die mit der Regel übereinstimmen. Die Webseite muss mit dem Adobe Experience Platform Web SDK implementiert werden."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html" text="Weitere Infos"

<!--Confirm the URL to use for authoring content on the surface. Typically the Authoring URL will be the surface URL itself, but you may include extra parameters if required. The page must include the Adobe Experience Platform Web SDK.-->

Nachdem Sie eine Webaktion aus der Kampagne erstellt haben, können Sie Ihren Inhalt mit dem Webdesigner bearbeiten. Gehen Sie dazu wie folgt vor.

>[!CAUTION]
>
>Zugriff auf [!DNL Journey Optimizer], muss Ihre Webseite mithilfe der [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target=&quot;_blank&quot;}.

1. Aus dem **[!UICONTROL Action]** im Tab der Kampagne, wählen Sie **[!UICONTROL Edit content]** , um mit der Erstellung Ihrer Web-Kampagne zu beginnen.

1. Wenn Sie eine Seitenabgleichregel erstellt haben, müssen Sie jede URL eingeben, die dieser Regel entspricht. Die Änderungen werden auf alle Seiten angewendet, die mit der Regel übereinstimmen.

   >[!NOTE]
   >
   >Wenn Sie eine einzelne URL als Weboberfläche eingegeben haben, ist die zu personalisierende URL bereits ausgefüllt.

   ![](assets/web-edit-enter-url.png)

1. Der Inhalt der Seite wird angezeigt.

   >[!CAUTION]
   >
   >Die Webseite muss die [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target=&quot;_blank&quot;}.

1. Klicken **[!UICONTROL Open web designer]** , um sie zu bearbeiten. [Weitere Infos](author-web.md)

   ![](assets/web-open-designer.png)

1. Der Webdesigner wird angezeigt.

   ![](assets/web-designer.png)

1. Wählen Sie ein beliebiges Element auf der Arbeitsfläche aus, z. B. Bild, Schaltfläche, Absatz, Text, Container, Überschrift, Link usw. und verwenden:

   * Kontextmenü zur Bearbeitung des Inhalts, des Layouts, der Links oder der Personalisierung usw.

      ![](assets/web-designer-contextual-bar.png)

   * Die Symbole oben im rechten Bereich zum Bearbeiten, Duplizieren, Löschen oder Ausblenden der einzelnen Elemente.

      ![](assets/web-designer-right-panel-icons.png)

   * Der rechte Bereich, der sich dynamisch entsprechend dem ausgewählten Element ändert. Sie können beispielsweise den Hintergrund, die Typografie, den Rahmen, die Größe, die Position, den Abstand, die Effekte oder Inline-Stile eines Elements bearbeiten.

      ![](assets/web-designer-right-panel.png)

## Inhaltskomponenten verwenden {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Hinzufügen von Inhaltskomponenten zur Webseite"
>abstract="Sie können Ihrer Webseite eine Reihe von Komponenten hinzufügen und diese nach Bedarf bearbeiten."

1. Aus dem **[!UICONTROL Components]** auf der linken Seite können Sie die folgenden Komponenten zu Ihrer Webseite hinzufügen und sie nach Bedarf bearbeiten:

   * [Trennlinie](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [Bild](../email/content-components.md#image)
   * Überschrift - Die Verwendung dieser Komponente ähnelt der Verwendung der **[!UICONTROL Text]** im E-Mail-Designer. [Weitere Infos](../email/content-components.md#text)
   * Absatz - Die Verwendung dieser Komponente ähnelt der Verwendung der **[!UICONTROL Text]** im E-Mail-Designer. [Weitere Infos](../email/content-components.md#text)
   * Link - Erfahren Sie, wie Sie die Formatierung von Links in [diesem Abschnitt](../email/styling-links.md)
   * [Angebotsentscheidung](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. Bewegen Sie den Mauszeiger auf die Seite und klicken Sie auf die Schaltfläche **[!UICONTROL Insert before]** oder **[!UICONTROL Insert after]** -Schaltfläche, um die Komponente an ein vorhandenes Element auf der Seite anzuhängen.

   ![](assets/web-designer-insert-components.png)

1. Bearbeiten Sie aus dem Container, der für diese Komponente angezeigt wird, den Komponenteninhalt nach Bedarf.

   ![](assets/web-designer-edit-html.png)

1. Passen Sie die Stile an, die über die **[!UICONTROL Container]** -Bereich auf der rechten Seite, z. B. Hintergrund, Textfarbe, Rahmen, Größe, Position usw. abhängig von der ausgewählten Komponente.

   ![](assets/web-designer-html-style.png)

## Navigieren durch den Webdesigner

### Verwenden von Breadcrumbs

1. Wählen Sie ein beliebiges Element auf der Arbeitsfläche aus.

1. Klicken Sie auf **[!UICONTROL Expand/Collapse Breadcrumbs]** auf der linken unteren Bildschirmseite, um Informationen zum ausgewählten Element schnell anzuzeigen.

   ![](assets/web-designer-breadcrumbs.png)

1. Wenn Sie den Mauszeiger über die Breadcrumbs bewegen, wird das entsprechende Element im Editor hervorgehoben.

1. Damit können Sie einfach zu jedem übergeordneten, gleichrangigen oder untergeordneten Element im Visual Editor navigieren.

### Zum Modus &quot;Durchsuchen&quot;wechseln {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="Durchsuchen-Modus verwenden"
>abstract="In diesem Modus können Sie von der ausgewählten Oberfläche, die Sie personalisieren möchten, zur gewünschten Seite navigieren."

Sie können die Standardeinstellung ersetzen **[!UICONTROL Design]** in den **[!UICONTROL Browse]** -Modus über die dedizierte Schaltfläche.

![](assets/web-designer-browse-mode.png)

Aus dem **[!UICONTROL Browse]** -Modus können Sie von der ausgewählten Oberfläche, die Sie personalisieren möchten, zur gewünschten Seite navigieren.

Dies ist besonders nützlich, wenn es um Seiten geht, die hinter der Authentifizierung stehen oder von Anfang an nicht über eine bestimmte URL verfügbar sind. Sie können sich beispielsweise authentifizieren, zu Ihrer Kontoseite oder zu Ihrer Warenkorbseite navigieren und dann zurück zu **[!UICONTROL Design]** -Modus, um die Änderungen auf der gewünschten Seite durchzuführen.

### Ändern der Gerätegröße

Sie können die Gerätegröße in eine vordefinierte Größe ändern, z. B. **[!UICONTROL Tablet]** oder **[!UICONTROL Mobile landscape]** oder legen Sie eine benutzerdefinierte Größe fest. Geben Sie die gewünschte Anzahl Pixel an, um eine benutzerdefinierte Größe zu definieren.

Sie können auch den Zoomfokus von 25 % auf 400 % ändern.

![](assets/web-designer-device.png)

## Änderungen verwalten {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Einfaches Verwalten aller Änderungen"
>abstract="Mithilfe dieses Bereichs können Sie alle Anpassungen und Stile, die Sie Ihrer Webseite hinzugefügt haben, durchsuchen und verwalten."

Sie können mühelos alle Komponenten, Anpassungen und Stile verwalten, die Sie Ihrer Webseite hinzugefügt haben.

1. Wählen Sie die **[!UICONTROL Modifications]** -Schaltfläche, um den entsprechenden Bereich auf der linken Seite anzuzeigen.

   ![](assets/web-designer-modifications-pane.png)

1. Sie können alle Änderungen überprüfen, die Sie an der Seite vorgenommen haben.

1. Wählen Sie eine unerwünschte Änderung aus und klicken Sie auf das Löschsymbol, um sie zu entfernen.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >Gehen Sie beim Löschen einer Aktion mit Vorsicht vor, da sich dies auf nachfolgende Aktionen auswirken kann.

1. Sie können Aktionen auch mithilfe der **[!UICONTROL Undo/Redo]** rechts oben auf dem Bildschirm.

   ![](assets/web-designer-undo-redo.png)

   Klicken Sie auf die Schaltfläche und halten Sie sie gedrückt, um zwischen der **[!UICONTROL Undo]** und **[!UICONTROL Redo]** Optionen. Klicken Sie dann auf die Schaltfläche selbst, um die gewünschte Aktion anzuwenden.

## Personalisierung und Angebote hinzufügen

Um eine Personalisierung hinzuzufügen, wählen Sie einen Container aus und wählen Sie das Personalisierungssymbol in der angezeigten Kontextmenüleiste aus. Fügen Sie Ihre Änderungen mithilfe des Ausdruckseditors hinzu. [Weitere Infos](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

Verwenden Sie die **[!UICONTROL Offer decision]** einzufügende Komponente [Angebote](../offers/get-started/starting-offer-decisioning.md) in Ihre Webseiten einfügen. Der Prozess ist derselbe wie bei [Hinzufügen eines Angebots zu einer E-Mail](../email/add-offers-email.md). Sie nutzt die Entscheidungsverwaltung, um das beste Angebot für Ihre Kunden auszuwählen.

![](assets/web-designer-offer.png)

## Webkampagne testen {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Vorschau des Web-Erlebnisses"
>abstract="Hier erhalten Sie eine Simulation, wie Ihr Web-Erlebnis aussehen wird."

Gehen Sie wie folgt vor, um eine Vorschau Ihres geänderten Web-Erlebnisses anzuzeigen.

>[!CAUTION]
>
>Sie müssen über Testprofile verfügen, um zu simulieren, welche Angebote an sie gesendet werden. Erfahren Sie, wie Sie [Testprofile erstellen](../segment/creating-test-profiles.md).

1. Wählen Sie entweder aus dem **[!UICONTROL Edit content]** Bildschirm oder Webdesigner auswählen **[!UICONTROL Simulate content]**.

   ![](assets/web-designer-simulate.png)

1. Klicken **[!UICONTROL Manage test profiles]** , um ein oder mehrere Testprofile auszuwählen.
1. Es wird eine Vorschau der geänderten Webseite angezeigt.

   ![](assets/web-designer-preview.png)

1. Sie können die Test-URL auch kopieren, um sie in einen beliebigen Browser einzufügen oder im Standardbrowser zu öffnen.
