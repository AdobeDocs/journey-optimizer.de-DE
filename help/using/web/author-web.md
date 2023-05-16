---
title: Verfassen von Web-Seiten
description: Erfahren Sie, wie Sie in Journey Optimizer eine Web-Seite erstellen und ihren Inhalt bearbeiten
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1623'
ht-degree: 100%

---

# Verfassen von Web-Seiten {#author-web}

Nachdem Sie eine [Web-Aktion](create-web.md#create-web-campaign) zu Ihrer Kampagne hinzugefügt haben, können Sie den Inhalt Ihrer Site mit dem Web-Designer bearbeiten.

In [!DNL Journey Optimizer] basiert das Erstellen von Web-Seiten auf der Chrome-Browser-Erweiterung **Adobe Experience Cloud Visual Helper**. [Weitere Informationen](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>Um in der Benutzeroberfläche von [!DNL Journey Optimizer] auf Web-Seiten zuzugreifen oder sie dort zu erstellen, müssen Sie den Voraussetzungen in [diesem Abschnitt](web-prerequisites.md) folgen.

[In diesem Video erfahren Sie, wie Sie eine Web-Kampagne verfassen](#video)

## Bearbeiten der Inhalte von Web-Seiten {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Bestätigen der URL zum Bearbeiten"
>abstract="Bestätigen Sie die URL der spezifischen Web-Seite, die für die Bearbeitung des Inhalts verwendet werden soll, welcher auf die oben definierte Web-Oberfläche angewendet wird. Die Web-Seite muss mithilfe des Adobe Experience Platform Web SDK implementiert werden."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de" text="Weitere Informationen"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Geben Sie die zu bearbeitende URL ein"
>abstract="Geben Sie die URL einer bestimmten Web-Seite ein, die zum Bearbeiten des Inhalts verwendet werden soll. Sie wird auf alle Seiten angewendet, die der Regel entsprechen. Die Web-Seite muss mithilfe des Adobe Experience Platform Web SDK implementiert werden."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de" text="Weitere Informationen"

Gehen Sie wie folgt vor, um mit der Erstellung Ihrer Web-Kampagne zu beginnen.

1. Wählen Sie auf der Registerkarte **[!UICONTROL Aktion]** der [Kampagne](create-web.md#create-web-campaign) die Option **[!UICONTROL Inhalt bearbeiten]** aus.<!--change screen with rule-->

   ![](assets/web-campaign-edit-content.png)

1. Wenn Sie eine Matching-Regel für Seiten erstellt haben, müssen Sie jede URL eingeben, die dieser Regel entspricht: Die Änderungen werden auf allen Seiten angewandt, die mit der Regel übereinstimmen. Der Inhalt der Seite wird angezeigt.

   >[!NOTE]
   >
   >Wenn Sie eine einzelne URL als Web-Oberfläche eingegeben haben, ist die zu personalisierende URL bereits ausgefüllt.

   ![](assets/web-edit-enter-url.png)

   >[!CAUTION]
   >
   >Die Web-Seite muss das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de){target="_blank"} enthalten. [Weitere Informationen](web-prerequisites.md#implementation-prerequisites)

1. Klicken Sie auf **[!UICONTROL Web-Seite bearbeiten]**, um mit dem Erstellen zu beginnen. Der Web-Designer wird angezeigt.

   ![](assets/web-designer.png)

   >[!NOTE]
   >
   >Wenn Sie versuchen, eine Web-Site zu laden, die sich nicht laden lässt, wird eine Meldung mit dem Vorschlag angezeigt, die Browser-Erweiterung [Visual Editing Helper](#install-visual-editing-helper) zu installieren. Tipps zur Fehlerbehebung finden Sie in [diesem Abschnitt](web-prerequisites.md#troubleshooting).

1. Wählen Sie ein beliebiges Element auf der Arbeitsfläche aus, z. B. Bild, Schaltfläche, Absatz, Text, Container, Überschrift, Link usw. [Weitere Informationen](#content-components)

1. Verwenden Sie:

   * das Kontextmenü zur Bearbeitung des Inhalts, des Layouts, der Links oder der Personalisierung usw.

      ![](assets/web-designer-contextual-bar.png)

   * die Symbole oben im rechten Bereich zum Bearbeiten, Duplizieren, Löschen oder Ausblenden der einzelnen Elemente.

      ![](assets/web-designer-right-panel-icons.png)

   * den rechten Bereich, der sich dynamisch entsprechend dem ausgewählten Element ändert. Sie können beispielsweise den Hintergrund, die Typografie, den Rahmen, die Größe, die Position, den Abstand, die Effekte oder Inline-Stile eines Elements bearbeiten.

      ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>Der Web-Content-Designer ähnelt größtenteils E-Mail-Designer. Weitere Informationen finden Sie unter [Inhaltserstellung mit  [!DNL Journey Optimizer]](../email/get-started-email-design.md).

## Verwenden von Komponenten {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Hinzufügen von Komponenten zu einer Web-Seite"
>abstract="Sie können Ihrer Web-Seite eine Reihe von Komponenten hinzufügen und diese nach Bedarf bearbeiten."

1. Wählen Sie im Bereich **[!UICONTROL Komponenten]** auf der linken Seite ein Element aus. Sie können Ihrer Web-Seite die folgenden Komponenten hinzufügen und diese nach Bedarf bearbeiten:

   * [Trennlinie](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [Bild](../email/content-components.md#image)
   * Überschrift – die Verwendung dieser Komponente ähnelt der Verwendung der Komponente **[!UICONTROL Text]** im E-Mail-Designer. [Weitere Informationen](../email/content-components.md#text)
   * Absatz – die Verwendung dieser Komponente ähnelt der Verwendung der Komponente **[!UICONTROL Text]** im E-Mail-Designer. [Weitere Informationen](../email/content-components.md#text)
   * Link
   * [Angebotsentscheidung](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. Bewegen Sie den Mauszeiger über die Seite und klicken Sie auf die Schaltfläche **[!UICONTROL Einfügen vor]** oder **[!UICONTROL Einfügen nach]**, um die Komponente an ein vorhandenes Element auf der Seite anzuhängen.

   ![](assets/web-designer-insert-components.png)

   >[!NOTE]
   >
   >Um die Auswahl einer Komponente aufzuheben, klicken Sie auf die Schaltfläche **[!UICONTROL ESC]** im kontextuellen blauen Banner, das oben auf der Arbeitsfläche angezeigt wird.

1. Bearbeiten Sie die Komponente nach Bedarf direkt im Inhalt Ihrer Seite.

   ![](assets/web-designer-edit-header.png)

1. Passen Sie die Stile an, die im kontextuellen Bereich auf der rechten Seite angezeigt werden, z. B. Hintergrund, Textfarbe, Rahmen, Größe, Position usw., - abhängig von der ausgewählten Komponente.

   ![](assets/web-designer-header-style.png)

## Hinzufügen von Personalisierung und Angeboten

Um eine Personalisierung hinzuzufügen, wählen Sie einen Container aus und klicken Sie auf das Personalisierungssymbol in der angezeigten Kontextmenüleiste. Fügen Sie Ihre Änderungen mithilfe des Ausdruckseditors hinzu. [Weitere Informationen](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

Verwenden Sie die Komponente **[!UICONTROL Angebotsentscheidung]**, um [Angebote](../offers/get-started/starting-offer-decisioning.md) in Ihre Web-Seiten einzufügen. Der Prozess ist der gleiche wie beim [Hinzufügen eines Angebots zu einer E-Mail](../email/add-offers-email.md). Er nutzt das Entscheidungs-Management, um das beste Angebot für Ihre Kunden auszuwählen.

![](assets/web-designer-offer.png)

## Verwalten von Änderungen {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Einfaches Verwalten aller Änderungen"
>abstract="Mithilfe dieses Bereichs können Sie alle Anpassungen und Stile, die Sie Ihrer Web-Seite hinzugefügt haben, durchsuchen und verwalten."

Sie können mühelos alle Komponenten, Anpassungen und Stile verwalten, die Sie Ihrer Web-Seite hinzugefügt haben.

1. Wählen Sie das Symbol **[!UICONTROL Änderungen]** aus, um den entsprechenden Bereich auf der linken Seite anzuzeigen.

   ![](assets/web-designer-modifications-pane.png)

1. Sie können alle Änderungen überprüfen, die Sie an der Seite vorgenommen haben.

1. Wählen Sie eine unerwünschte Änderung aus und klicken Sie auf das Löschsymbol, um sie zu entfernen.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >Gehen Sie beim Löschen einer Aktion vorsichtig vor, da sich dies auf nachfolgende Aktionen auswirken kann.

1. Verwenden Sie die Schaltfläche **[!UICONTROL Mehr Aktionen]** oben im Bereich **[!UICONTROL Änderungen]**, um alle Änderungen gleichzeitig zu löschen.

   ![](assets/web-designer-delete-modifications.png)

1. Über das Menü **[!UICONTROL Mehr Aktionen]** können Sie auch nur die ungültigen Änderungen löschen, d. h. die Änderungen, die durch andere Änderungen überschrieben wurden. Wenn Sie beispielsweise die Farbe eines Textes ändern und diesen Text dann löschen, wird die Farbänderung ungültig, da der Text nicht mehr vorhanden ist.

1. Sie können Aktionen auch mithilfe der Schaltfläche **[!UICONTROL Rückgängig/Wiederholen]** rechts oben auf dem Bildschirm abbrechen und wiederholen.

   ![](assets/web-designer-undo-redo.png)

   Klicken Sie auf die Schaltfläche und halten Sie sie gedrückt, um zwischen den Optionen **[!UICONTROL Rückgängig]** und **[!UICONTROL Wiederholen]** zu wechseln. Klicken Sie dann auf die Schaltfläche selbst, um die gewünschte Aktion anzuwenden.

## Verwenden von Klick-Tracking {#use-click-tracing}

Mit dieser Funktion im Web-Designer können Sie ein beliebiges Element Ihrer Web-Site auswählen und die Klicks auf dieses Element verfolgen.

Sobald Ihre Kampagne aktiv ist, können Sie die Anzahl der Klicks für jedes Element im Kampagnen-Web-Bericht überprüfen. Diese Informationen können zur Verbesserung des Benutzererlebnisses auf Ihrer Web-Site nützlich sein. Wenn beispielsweise die [Web-Berichte](../reports/campaign-global-report.md#web-tab) zeigen, dass häufig auf ein Element geklickt wurde, auf das eigentlich nicht geklickt werden kann, können Sie diesem Element einen Link hinzufügen.

1. Wählen Sie ein Element auf Ihrer Seite und dann **[!UICONTROL Klick-Tracking für Element]** aus dem Kontextmenü aus.

   ![](assets/web-designer-click-track.png)

   >[!NOTE]
   >
   >Jedes Element kann ausgewählt werden, unabhängig davon, ob es klickbar ist.

1. Die entsprechende verfolgte Aktion wird automatisch im Bereich **[!UICONTROL Klick-Tracking]** auf der linken Seite angezeigt.

   ![](assets/web-designer-click-track-pane.png)

1. Fügen Sie eine aussagekräftige Bezeichnung hinzu, um alle verfolgten Elemente zu verwalten und sie in den Berichten leicht auffindbar zu machen. Das Feld **[!UICONTROL CSS-Auswahl]** zeigt Informationen zum Auffinden des ausgewählten Elements an.

1. Wiederholen Sie die obigen Schritte, um nach Bedarf weitere Elemente für das Klick-Tracking auszuwählen. Die entsprechenden Aktionen werden alle im linken Bereich aufgelistet.

   ![](assets/web-designer-click-tracking-actions.png)

1. Um das Klick-Tracking für ein Element zu entfernen, wählen Sie das entsprechende Löschsymbol aus.

Sobald Ihre Kampagne aktiv ist, können Sie im Kampagnenbericht die Registerkarte **[!UICONTROL Web]** überprüfen, um die Anzahl der Impressionen, die Klickrate und die Anzahl der Klicks nach Element zu vergleichen. [Weitere Informationen](../reports/campaign-global-report.md#web-tab)

## Navigieren durch den Web-Designer {#navigate-web-designer}

### Verwenden von Breadcrumbs {#breadcrumbs}

1. Wählen Sie ein beliebiges Element auf der Arbeitsfläche aus.

1. Klicken Sie auf **[!UICONTROL Breadcrumbs erweitern/reduzieren]** auf der linken unteren Bildschirmseite, um Informationen zum ausgewählten Element schnell anzuzeigen.

   ![](assets/web-designer-breadcrumbs.png)

1. Wenn Sie den Mauszeiger über die Breadcrumbs bewegen, wird das entsprechende Element im Editor hervorgehoben.

1. Damit können Sie einfach zu jedem übergeordneten, gleichrangigen oder untergeordneten Element im visuellen Editor navigieren.

### Wechseln in den Durchsuchen-Modus {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="Verwenden des Durchsuchen-Modus"
>abstract="Im Durchsuchen-Modus können Sie von der ausgewählten Oberfläche, die Sie personalisieren möchten, direkt zur gewünschten Seite navigieren."

Sie können über die entsprechende Schaltfläche vom Standardmodus **[!UICONTROL Design]** in den **[!UICONTROL Durchsuchen]**-Modus wechseln.

![](assets/web-designer-browse-mode.png)

Im **[!UICONTROL Durchsuchen]**-Modus können Sie von der ausgewählten Oberfläche, die Sie personalisieren möchten, zur gewünschten Seite navigieren.

Dies ist besonders nützlich, wenn es um Seiten geht, die sich hinter der Authentifizierung befinden oder nicht von Anfang an über eine bestimmte URL verfügbar sind. Sie können sich beispielsweise authentifizieren, zu Ihrer Kontoseite oder zu Ihrer Warenkorbseite navigieren und dann zurück in den **[!UICONTROL Design]**-Modus wechseln, um die Änderungen auf der gewünschten Seite durchzuführen.

### Ändern der Gerätegröße {#change-device-size}

Sie können die Gerätegröße der Web-Designer-Anzeige in eine vordefinierte Größe ändern, z. B. **[!UICONTROL Tablet]** oder **[!UICONTROL Mobilgeräte – Querformat]**. Legen Sie alternativ eine benutzerdefinierte Größe fest, indem Sie die gewünschte Pixelanzahl eingeben.

Sie können auch den Zoom-Fokus ändern – von 25 % bis 400 %.

![](assets/web-designer-device.png)

Die Möglichkeit, die Gerätegröße zu ändern, wurde für responsive Web-Sites entwickelt, die auf verschiedenen Geräten, Fenstern und Bildschirmgrößen gut dargestellt werden. Responsive Web-Sites passen sich automatisch an jede Bildschirmgröße an, einschließlich Desktops, Laptops, Tablets oder Mobiltelefone.

>[!CAUTION]
>
>Sie können ein Web-Erlebnis mit einer bestimmten Gerätegröße bearbeiten. Solange die Selektoren identisch sind, gelten diese Änderungen für alle Größen und Geräte, nicht nur für die Gerätegröße, in der Sie arbeiten. Gleichermaßen werden bei der Bearbeitung eines Erlebnisses in der normalen Desktop-Ansicht die Änderungen auf alle Bildschirmgrößen angewendet, nicht nur auf die Desktop-Ansicht.
>
>Zurzeit unterstützt [!DNL Journey Optimizer] keine Seitenänderungen für bestimmte Gerätegrößen. Wenn Sie also beispielsweise über eine separate mobile Web-Site mit einer separaten Site-Struktur verfügen, müssen Sie die für Ihre mobile Site spezifischen Änderungen in einer anderen Kampagne vornehmen.

## Testen der Web-Kampagne {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Vorschau des Web-Erlebnisses"
>abstract="Betrachten Sie in einer Simulation, wie Ihr Web-Erlebnis aussehen wird."

Gehen Sie wie folgt vor, um eine Vorschau Ihres geänderten Web-Erlebnisses anzuzeigen.

>[!CAUTION]
>
>Sie müssen über Testprofile verfügen, um simulieren zu können, welche Angebote an sie gesendet werden. Hier erfahren Sie, wie Sie [Testprofile erstellen](../segment/creating-test-profiles.md).

1. Wählen Sie auf dem Bildschirm zur Inhaltsbearbeitung der Web-Kampagne die Option **[!UICONTROL Inhalt simulieren]** aus.

   <!--![](assets/web-designer-simulate.png)-->

   ![](assets/web-campaign-simulate.png)

1. Klicken Sie auf **[!UICONTROL Testprofile verwalten]**, um ein oder mehrere Testprofile auszuwählen.
1. Es wird eine Vorschau der geänderten Web-Seite angezeigt.

   ![](assets/web-designer-preview.png)

1. Sie können sie auch im Standard-Browser öffnen oder die Test-URL kopieren, um sie in einen beliebigen Browser einzufügen. Auf diese Weise können Sie den Link für Ihr Team und Ihre Interessensgruppen freigeben, damit sie in der Lage sind, das neue Web-Erlebnis in einem beliebigen Browser in der Vorschau zu betrachten, bevor die Kampagne live geschaltet wird.

   >[!NOTE]
   >
   >Beim Kopieren der Test-URL ist der angezeigte Inhalt derjenige, der für das Testprofil personalisiert wurde, das zum Zeitpunkt der Erstellung der Inhaltsimulation in [!DNL Journey Optimizer] verwendet wurde.

## Anleitungsvideo{#video}

Das folgende Video zeigt, wie Sie ein Web-Erlebnis mit dem Web-Designer in [!DNL Journey Optimizer]-Kampagnen erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)
