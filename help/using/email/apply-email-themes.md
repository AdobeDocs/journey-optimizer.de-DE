---
solution: Journey Optimizer
product: journey optimizer
title: Verbessertes Erlebnis bei der Erstellung von E-Mails
description: Erfahren Sie, wie Sie die E-Mail-Erstellung mit wiederverwendbaren Designs und Modulen optimieren können, um die Konsistenz und Effizienz von Designs in Ihren Kampagnen sicherzustellen.
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: E-Mail-Designs, Module, Wiederverwendbarkeit, Markenkonsistenz, E-Mail-Design, benutzerdefiniertes CSS, Optimierung für Mobilgeräte
exl-id: e81d9634-bbff-44d0-8cd7-e86f85075c06
source-git-commit: 8caa8f8e126f062535b5276b4d96de10875a3406
workflow-type: tm+mt
source-wordcount: '1741'
ht-degree: 92%

---

# Anwenden von Designs auf Ihren E-Mail-Inhalt {#apply-email-themes}

>[!CONTEXTUALHELP]
>id="ajo_use_theme"
>title="Anwenden eines Designs auf Ihre E-Mail"
>abstract="Wählen Sie ein Design für Ihre E-Mail aus, um schnell einen bestimmten Stil anzuwenden, der zu Ihrer Marke und Ihrem Design passt."

>[!AVAILABILITY]
>
>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

Mit Designs können technisch nicht versierte Benutzende wiederverwendbare Inhalte erstellen, die zu einer bestimmten Marke und Designsprache passen, indem sie zusätzlich zu den Standardvorlagen benutzerdefinierte Stile hinzufügen<!-- to achieve brand specific results-->.

Diese Funktion ermöglicht es Marketing-Fachleuten, visuell ansprechende, markenkonsistente E-Mails schneller und mit weniger Aufwand zu nutzen und gleichzeitig erweiterte Anpassungsoptionen für individuelle Design-Anforderungen bereitzustellen.

## Leitlinien und Einschränkungen {#themes-guardrails}

* Wenn Sie eine E-Mail von Grund auf neu erstellen, können Sie die Erstellung Ihres Inhalts mit einem Design beginnen, um schnell einen bestimmten Stil anzuwenden, der zu Ihrer Marke und Ihrem Design passt.

  Wenn Sie den Modus „Manuelle Formatierung“ wählen, können Sie keine Designs anwenden, es sei denn, Sie setzen Ihre E-Mail zurück.

* [Fragmente](../content-management/fragments.md) sind zwischen dem Modus „Designs verwenden“ und dem Modus „Manuelle Formatierung“ nicht kreuzkompatibel.

   * Design-Fragmente sind nicht in E-Mail-Inhalten verfügbar, die ohne Designs erstellt wurden.

   * Damit Sie ein [Fragment](../content-management/fragments.md) in einem Design-Inhalt nutzen können, muss das Fragment selbst mit Designs erstellt worden sein. [Weitere Informationen](#leverage-themes-fragment)

   * Wenn Sie ein Fragment im E-Mail-Inhalt verwenden, stellen Sie sicher, dass Sie ein Design anwenden, das Sie für dieses Fragment definiert haben. Anderenfalls kann es zu Anzeigeproblemen kommen, insbesondere in Outlook 2021 und früheren Versionen. [Weitere Informationen](#leverage-themes-fragment)

* Wenn Sie einen in HTML erstellten Inhalt verwenden, befinden Sie sich im [Kompatibilitätsmodus](existing-content.md) und können keine Designs auf diesen Inhalt anwenden.

   * Um Designs anzuwenden, müssen Sie zunächst den importierten Inhalt [als neue Vorlage](../content-management/create-content-templates.md#save-as-template) speichern und diese Vorlage dann in einen Design-kompatiblen Inhalt konvertieren. Anschließend können Sie diese Vorlage verwenden, um Ihren E-Mail-Inhalt zu erstellen. Informationen zum Konvertieren einer mit manueller Formatierung erstellten Vorlage finden Sie [in diesem Abschnitt](#theme-convertor).

   * Sie können auch weiterhin Ihren importierten HTML-Inhalt konvertieren. [Weitere Informationen](existing-content.md)

  <!--To fully leverage all the capabilities of the Email Designer, including themes, you must either create a new content in Use Themes mode, or convert your imported HTML content. [Learn more](existing-content.md)-->

* Wenn Sie benutzerdefinierte Web-Schriftarten (einschließlich Google-Schriftarten) in Ihren Designs verwenden, beachten Sie, dass viele E-Mail-Clients sie nicht unterstützen. Definieren Sie immer geeignete Ersatzschriftarten in Ihrem Design, um die Lesbarkeit für alle E-Mail-Clients sicherzustellen.

   * Gmail und Yahoo! Laden Sie keine externen Web-Schriftarten und greifen Sie auf die Systemschriftarten zurück, unabhängig von der in Ihrem HTML/CSS angegebenen Schriftfamilie.
   * Die einzigen von Gmail unterstützten Google-Schriftarten sind Roboto und Google Sans.
   * E-Mail-Clients *die* Webfonts unterstützen, sind unter anderem Apple Mail, iOS Mail, Android Mail, Thunderbird und Outlook für macOS.

<!--If you apply a theme to a content using a [fragment](../content-management/fragments.md) created with Manual Styling mode, the rendering may not be optimal.-->

## Erstellen eines Designs {#create-and-edit-themes}

Gehen Sie wie folgt vor, um ein Design zu definieren, das Sie in künftigen E-Mail-Inhalten nutzen können.

1. Erstellen Sie zunächst eine neue [Inhaltsvorlage](../content-management/create-content-templates.md).

1. Wählen Sie die Option **[!UICONTROL Designs erstellen oder bearbeiten]** aus.

   ![](assets/theme-create.png)

1. Wählen Sie ein Adobe-Design aus. Wählen Sie in diesem Beispiel das **[!UICONTROL Standard-Design]** aus und klicken Sie auf **[!UICONTROL Erstellen]**.

   ![](assets/theme-select.png)

1. Sie können auch auf der Registerkarte **[!UICONTROL Meine Designs]** eine benutzerdefinierte Vorlage auswählen und auf **[!UICONTROL Bearbeiten]** klicken, um sie zu aktualisieren.

   ![](assets/theme-edit.png)

1. Beginnen Sie auf der Registerkarte **[!UICONTROL Allgemeine Einstellungen]** mit der Definition Ihres Designs, indem Sie ihm einen bestimmten für Ihre Marke angemessenen Namen geben. Sie können die Standardbreite des Ansichtsfensters für Ihre E-Mails anpassen und auch das aktuelle Design exportieren, um es [Sandbox-übergreifend freizugeben](../configuration/copy-objects-to-sandbox.md).

   <!--![](assets/theme-general-settings.png)-->

1. Verwenden Sie die Leiste auf der rechten Seite, um durch die verschiedenen Registerkarten zu navigieren und Ihre Designeinstellungen zu aktualisieren.

   ![](assets/theme-right-pane.png)

1. Führen Sie folgende Schritte auf der Registerkarte **[!UICONTROL Farben]** aus:

   * Verwenden Sie die Schaltfläche **[!UICONTROL Bearbeiten]**, um eine **[!UICONTROL Farbpalette]** mit Standardfarben für Ihre Marke einzurichten. Wählen Sie eine **[!UICONTROL Voreinstellung]** aus, um schnell ein Farbschema zu erstellen oder jede Farbe Ihres Designs individuell anzupassen. Sie können auch eine Kombination aus beidem verwenden.

     ![](assets/theme-colors.gif)

   * Klicken Sie auf **[!UICONTROL Variante hinzufügen]**, um mehrere Farbvarianten zu erstellen, z. B. den hellen und dunklen Modus, wobei jede Variante Ihres Designs über eine eigene Farbpalette und Steuerelemente für Nuancen verfügt.

     ![](assets/theme-colors-variant.png)

   * Klicken Sie für jede Variante auf das Symbol **[!UICONTROL Bearbeiten]**, um ein einzelnes Element zu bearbeiten. Sie können die von Ihnen erstellte Standardpalette oder beliebige benutzerdefinierte Farben verwenden.

     ![](assets/theme-colors-edit-variant.gif)

1. In den **[!UICONTROL Texteinstellungen]** können Sie die globale Schriftart festlegen, die Sie für Ihr gesamtes Design verwenden möchten. Für eine detailliertere Steuerung können Sie auch jede Überschrift und jeden Absatztyp bearbeiten, um die Schriftart, die Größe, den Stil usw. anzupassen.

   ![](assets/theme-text.png)

   >[!NOTE]
   >
   >Beachten Sie bei der Auswahl benutzerdefinierter Web-Schriftarten, dass viele E-Mail-Clients wie Gmail und Yahoo! Externe Web-Schriftarten werden nicht unterstützt, sondern es wird auf die Systemschriftarten zurückgegriffen. Erwägen Sie die Verwendung von Ersatzschriftarten, um sicherzustellen, dass Ihr Inhalt auf allen E-Mail-Clients korrekt angezeigt wird. [Weitere Informationen](#themes-guardrails)

1. Wählen Sie auf der Registerkarte **[!UICONTROL Abstand]** ein einzelnes Element aus der Liste aus, um es mit dem richtigen Abstand zwischen den verschiedenen Komponenten einzufügen.

   <!--![](assets/theme-spacing.png)-->

1. Mit den anderen Registerkarten auf der rechten Seite können Sie jedes Schaltflächenelement, jede Trennlinie, zusätzliche Bildformatierungen und den Abstand des Raster-Layouts für dieses Design separat verwalten.

   ![](assets/theme-buttons.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**, um dieses Design für die zukünftige Verwendung zu speichern. Es wird jetzt auf der Registerkarte **[!UICONTROL Meine Designs]** angezeigt.

<!--A little strange upon hitting Save, because once the theme is created, you need to hit Close to go back to Design your template screen, then click Cancel if you don't want to proceed with template creation.-->

## Anwenden von Designs auf den E-Mail-Inhalt {#apply-themes-email}

Gehen Sie wie folgt vor, um standardmäßige oder benutzerdefinierte Stil-Designs auf eine Inhaltsvorlage oder E-Mail anzuwenden.

1. In [!DNL Journey Optimizer] können Sie eine [E-Mail](create-email.md)-Aktion zu einer Journey oder Kampagne hinzufügen oder eine E-Mail-[Inhaltsvorlage](../content-management/create-content-templates.md#create-template-from-scratch) erstellen und [den E-Mail-Text bearbeiten](get-started-email-design.md#key-steps).

1. Sie können eine der folgenden Aktionen auswählen:

   * Wählen Sie eine integrierte [E-Mail-Vorlage](use-email-templates.md) aus, um E-Mail-Designer zu öffnen. Es wird automatisch ein für jede Vorlage spezifisches Standard-Design angewendet.

   * Entwerfen Sie [neuen Inhalt von Grund auf](content-from-scratch.md) und wählen Sie **[!UICONTROL Designs verwenden]**, um mit einem vordefinierten Stil-Design zu beginnen.

     ![](assets/theme-from-scratch.png)

     >[!CAUTION]
     >
     >Wenn Sie den Modus „Manuelle Formatierung“ wählen, können Sie keine Designs anwenden, es sei denn, Sie setzen Ihr Design zurück.
     >
     >Damit Sie ein [Fragment](../content-management/fragments.md) in einem Design-Inhalt nutzen können, muss das Fragment selbst mit Designs erstellt worden sein. [Weitere Informationen](#leverage-themes-fragment)

1. Klicken Sie im E-Mail-Designer in der rechten Leiste auf die Schaltfläche **[!UICONTROL Designs]**. Es wird das Standard-Design oder das Design der Vorlage angezeigt. Sie können zwischen den beiden Farbvarianten für dieses Design wechseln.

   ![](assets/theme-default-hero.png)

1. Klicken Sie auf den Pfeil neben dem aktuell verwendeten Design. Die Liste der verfügbaren benutzerdefinierten und Adobe-Designs wird angezeigt.

   ![](assets/theme-hero-change.png)

1. Klicken Sie auf **[!UICONTROL Meine Designs]** und wählen Sie das von Ihnen erstellte Design aus.

   ![](assets/theme-select-custom.png)

1. Klicken Sie auf einen Bereich außerhalb der Dropdown-Liste. Das neu ausgewählte benutzerdefinierte Design wendet seine Stile automatisch auf alle E-Mail-Komponenten an. Sie können zwischen den Farbvarianten wechseln, falls vorhanden.

1. Wenn ein Design in einer Inhaltsvorlage ausgewählt ist, können Sie auf die Schaltfläche **[!UICONTROL Design bearbeiten]** klicken, um es zu aktualisieren. [Weitere Informationen](#create-and-edit-themes)

   ![](assets/theme-edit-in-template.png){width="40%"}

   >[!NOTE]
   >
   >Diese Option ist nicht verfügbar, wenn Designs im E-Mail-Inhalt verwendet werden.

1. Wenn Sie ein Design mit mehreren Farbvarianten verwenden, können Sie eine bestimmte Variante für eine bestimmte Strukturkomponente auswählen. Auf diese Weise können Sie eine Farbvariante für den gesamten Inhalt definieren und eine andere Variante nur für eine bestimmte Struktur verwenden.

   >[!NOTE]
   >
   >Diese Aktion kann nicht für Inhaltskomponenten ausgeführt werden.

   Wählen Sie hierzu eine Strukturkomponente aus, klicken Sie auf der Registerkarte **[!UICONTROL Stile]** rechts auf die Option **Variante eines bestimmten Designs verwenden** und wenden Sie die gewünschte Variante auf diese Struktur an.

   ![](assets/theme-structure-variant.png)

   In diesem Beispiel wird die erste Farbvariante des aktuellen Designs auf den gesamten E-Mail-Inhalt angewendet, aber die dritte Farbvariante wird auf die ausgewählte Struktur angewendet. Sie können sehen, dass sich die Hintergrundfarben des Textkörpers und des Ansichtsfensters für diese spezifische Struktur vom Rest des Inhalts unterscheiden.

Sie können jederzeit zwischen Designs wechseln. Der E-Mail-Inhalt bleibt unverändert, aber die Stile werden aktualisiert, um das neue Design widerzuspiegeln.

### Entsperren von Stilen {#unlocking-styles}

Wenn eine Komponente ausgewählt wird, können Sie ihren Stil über das entsprechende Symbol in der Registerkarte **[!UICONTROL Stile]** entsperren.

![](assets/theme-unlock-style.png){width="90%"}

Das ausgewählte Design wird weiterhin auf diese Komponente angewendet, Sie können jedoch die Stilelemente überschreiben. Wenn Sie Designs wechseln, wird das neue Design nur auf die Stilelemente angewendet, die nicht überschrieben wurden.<!--can you revert this action?-->

Wenn Sie beispielsweise eine Textkomponente entsperren, können Sie <!--the font size from 11 to 14 and -->die Schriftfarbe von Schwarz in Rot ändern:

![](assets/theme-unlock-style-ex-white.png){width="80%" align="center" zoomable="yes"}

Wenn Sie das Design ändern, <!--the font size is still 14 and -->ist die Schriftfarbe für diese Komponente weiterhin Rot, aber die Hintergrundfarbe für diese Komponente ändert sich entsprechend des neuen Designs:

![](assets/theme-unlock-style-ex-colored.png){width="80%"}

## Verwenden von Designs in einem Fragment {#leverage-themes-fragment}

Damit Sie ein Fragment in einer Vorlage oder E-Mail mit [angewendeten Designs](#apply-themes-email) nutzen können, muss dieses Fragment selbst mit Designs erstellt worden sein. Anderenfalls können Sie dieses Fragment nicht in Ihrem Design-Inhalt verwenden.

Gehen Sie wie folgt vor, um ein mit Designs kompatibles Fragment zu erstellen:

1. Erstellen Sie in [!DNL Journey Optimizer] ein visuelles Fragment und klicken Sie auf **[!UICONTROL Erstellen]**, um den Inhalt Ihres Fragments zu gestalten. [Weitere Informationen](../content-management/create-fragments.md)

1. Wählen Sie **[!UICONTROL Designs verwenden]** aus, um mit einem vordefinierten Stil-Design zu beginnen.

   ![](assets/fragment-use-themes.png){width="100%"}

   >[!CAUTION]
   >
   >Wenn Sie den Modus „Manuelle Formatierung“ wählen, können Sie keine Designs anwenden, es sei denn, Sie setzen Ihr Fragment-Design zurück.

1. Sobald Sie den E-Mail-Designer geöffnet haben, können Sie mit der Erstellung Ihres Fragments beginnen.

1. Klicken Sie in der rechten Leiste auf die Schaltfläche **[!UICONTROL Designs]**. Das Standard-Design wird angezeigt. Sie können zwischen den verschiedenen Farbvarianten für dieses Design wechseln.

   ![](assets/fragment-default-theme.png){width="100%" align="center" zoomable="yes"}

1. Sie können andere Designs auswählen, um eine Vorschau Ihres Fragmentinhalts anzuzeigen. Wählen Sie dazu den Pfeil neben dem Standard-Design aus und klicken Sie auf **[!UICONTROL Designs auswählen]**.

   ![](assets/fragment-select-themes.png){width="40%"}

1. Sie können zwischen den Registerkarten **[!UICONTROL Adobe]** und **[!UICONTROL Meine Designs]** navigieren und bis zu fünf kompatible Designs (aus beiden Registerkarten) für Ihr Fragment auswählen.

   ![](assets/fragment-select-compatible-themes.png){width=70%}

   >[!CAUTION]
   >
   >Wenn Sie das Fragment in einem E-Mail-Inhalt verwenden, stellen Sie sicher, dass Sie ein [Design anwenden](#apply-themes-email), das Sie für dieses Fragment definiert haben. Anderenfalls kann es zu Anzeigeproblemen kommen, insbesondere in Outlook 2021 und früheren Versionen.

1. Klicken Sie auf **[!UICONTROL Schließen]**.

1. Wählen Sie erneut den Pfeil neben dem **[!UICONTROL Standard-Design]** aus. Sie können nun zwischen den verschiedenen ausgewählten Designs wechseln, um in der Vorschau anzuzeigen, wie jeder Stil gerendert wird.

   ![](assets/fragment-selected-themes.png){width=90%}

1. Klicken Sie erneut auf **[!UICONTROL Designs auswählen]**, um weitere Designs hinzuzufügen oder Ihre Auswahl zu ändern.

## Erstellen einer mit Designs kompatiblen Vorlage {#theme-convertor}

Mit [!DNL Journey Optimizer] können Sie eine Vorlage, die mit manuellen Formatierungen erstellt wurde, in einen Inhalt umwandeln, der mit Designs kompatibel ist. Dies kann besonders dann nützlich sein, wenn Sie Inhaltsvorlagen erstellt haben, bevor Designs in [!DNL Journey Optimizer] eingeführt wurden, oder wenn Sie externe Inhalte importieren.

>[!NOTE]
>
> Nur **E-Mail-Vorlagen** können in Design-kompatible Inhalte konvertiert werden. Einzelne E-Mails können nicht konvertiert werden. Sie müssen den Inhalt zunächst als Vorlage speichern.

1. Öffnen Sie die [Inhaltsvorlage](../content-management/create-content-templates.md) einer E-Mail und bearbeiten Sie den Inhalt mit dem E-Mail-Designer.

1. Wählen Sie das Symbol **[!UICONTROL Designs]** in der rechten Leiste aus und klicken Sie auf die Schaltfläche **[!UICONTROL Design aus Inhalten generieren]**.

   ![](assets/generate-theme.png){width=100%}

1. Das Fenster **[!UICONTROL Design erstellen]** wird geöffnet. [!DNL Journey Optimizer] erkennt die Stilelemente automatisch und konsolidiert sie in einem neuen Design.

   ![](assets/generate-theme-create-window.png){width=90%}

1. Geben Sie einen Namen für Ihr Design ein.

1. Nehmen Sie bei Bedarf eigene Anpassungen vor, wie beim Erstellen eines Designs von Grund auf, z. B. durch Hinzufügen einer Farbvariante, Bearbeiten von Schriften usw. [Weitere Informationen](#create-and-edit-themes)

   ![](assets/generate-theme-colors.png){width=90%}

1. Klicken Sie auf **[!UICONTROL Speichern]**, um dieses neue Design für die Wiederverwendung zu speichern. Sie können dieses Design nun wie jedes andere Design auf Ihre Inhalte anwenden. [Weitere Informationen](#apply-themes-email)