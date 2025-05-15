---
solution: Journey Optimizer
product: journey optimizer
title: Verbesserte E-Mail-Authoring-Erfahrung
description: Erfahren Sie, wie Sie die E-Mail-Erstellung mit wiederverwendbaren Designs und Modulen optimieren können, um die Konsistenz und Effizienz des Designs Ihrer Kampagnen sicherzustellen.
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: E-Mail-Designs, Module, Wiederverwendbarkeit, Markenkonsistenz, E-Mail-Design, benutzerdefiniertes CSS, Optimierung für Mobilgeräte
exl-id: e81d9634-bbff-44d0-8cd7-e86f85075c06
source-git-commit: bfe0ce29a30cff7ba876b43d9ed7858ffaab6bb5
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 3%

---

# Anwenden von Designs auf E-Mail-Inhalte {#apply-email-themes}

>[!CONTEXTUALHELP]
>id="ajo_use_theme"
>title="Anwenden eines Designs auf Ihre E-Mail"
>abstract="Wählen Sie ein Design für Ihre E-Mail aus, um schnell einen bestimmten Stil anzuwenden, der zu Ihrer Marke und Ihrem Design passt."

<!--This documentation provides a comprehensive guide to using themes to streamline your email creation process. With the ability to define reusable themes and leverage pre-designed modules, marketers can create professional, brand-aligned emails faster and with less effort.-->

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der Beta-Version und steht nur der Beta-Kundschaft zur Verfügung. Wenden Sie sich an den Adobe-Support, um am Beta-Programm teilzunehmen.

Mit Designs können technisch nicht versierte Benutzende wiederverwendbare Inhalte erstellen, die zu einer bestimmten Marke und Designsprache passen, indem sie zusätzlich zu den Standardvorlagen benutzerdefinierte Stile hinzufügen<!-- to achieve brand specific results-->.

Diese Funktion ermöglicht es Marketing-Experten, visuell ansprechende, markenkonsistente E-Mails schneller und mit weniger Aufwand zu nutzen und gleichzeitig erweiterte Anpassungsoptionen für individuelle Design-Anforderungen bereitzustellen.

<!--What is the Enhanced Email Authoring Experience?

This feature introduces two key components to simplify and enhance email creation:

* **Theme Management System**: A centralized system for creating, customizing, and applying reusable themes to emails. Themes ensure consistent styling across campaigns and eliminate the need for repetitive manual styling.

* **Modules**: Pre-designed, reusable content blocks that abstract common email elements (e.g., titles, descriptions, images, and links). Modules are built using customizable low-level components, offering flexibility while maintaining design standards.

Key Benefits:

- **Consistency**: Ensure all emails align with your brand's design guidelines.
- **Efficiency**: Save time by reusing themes and modules across campaigns.
- **Customization**: Add custom CSS and mobile-specific styles for advanced designs.
- **Scalability**: Eliminate repetitive styling tasks, enabling faster email creation.-->

## Schutzmechanismen und Einschränkungen {#themes-guardrails}

* Wenn Sie eine E-Mail von Grund auf neu erstellen, können Sie mit der Erstellung Ihres Inhalts beginnen, indem Sie ein Design verwenden, um schnell einen bestimmten Stil anzuwenden, der zu Ihrer Marke und Ihrem Design passt.

  Wenn Sie den klassischen Modus wählen, können Sie keine Designs anwenden, es sei denn, Sie setzen Ihre E-Mail zurück.

* [Fragmente](../content-management/fragments.md) sind zwischen dem Design-Modus und dem klassischen Modus nicht kreuzkompatibel.

  Um ein Fragment in einem Inhalt verwenden zu können, auf den ein Design angewendet wird, muss dieses Fragment im Design-Modus erstellt werden.

* Wenn Sie einen in HTML erstellten Inhalt verwenden, befinden Sie sich im [Kompatibilitätsmodus](existing-content.md) und Sie können keine Designs auf diesen Inhalt anwenden.

  Um alle Funktionen der E-Mail-Designer, einschließlich Designs, vollständig zu nutzen, müssen Sie entweder einen neuen Inhalt im Design-Modus erstellen oder Ihren importierten HTML-Inhalt konvertieren. [Weitere Informationen](existing-content.md)

<!--If using a content created in Classic mode or HTML, you cannot apply themes to this content. You must create a new content in Theme mode.

If you apply a theme to a content using a [fragment](../content-management/fragments.md) created in Classic mode, the rendering may not be optimal.-->

## Erstellen eines Designs {#create-and-edit-themes}

Gehen Sie wie folgt vor, um ein Design zu definieren, das Sie in künftigen E-Mail-Inhalten nutzen können.

1. Erstellen Sie zunächst eine neue [Inhaltsvorlage](../content-management/create-content-templates.md).

1. Wählen Sie die **[!UICONTROL Erstellen oder Bearbeiten von Designs]** aus.

   ![](assets/theme-create.png)

1. Sie können entweder das Standarddesign auswählen oder eine Adobe- oder benutzerdefinierte Vorlage verwenden. Wählen Sie in diesem Beispiel das Standarddesign aus und klicken Sie auf **[!UICONTROL Erstellen]**.

   ![](assets/theme-select.png)

1. Beginnen Sie auf **[!UICONTROL Registerkarte]** Allgemeine Einstellungen“ mit der Definition Ihres Designs, indem Sie ihm einen bestimmten Namen für Ihre Marke geben. Sie können die Standardbreite für Ihre E-Mails anpassen und auch das aktuelle Design exportieren, um [es über Sandboxes hinweg freizugeben](../configuration/copy-objects-to-sandbox.md).

   <!--![](assets/theme-general-settings.png)-->

1. Verwenden Sie die Leiste rechts, um durch die verschiedenen Registerkarten zu navigieren und Ihre Designeinstellungen zu aktualisieren.

   ![](assets/theme-right-pane.png)

1. Auf der Registerkarte **[!UICONTROL Farben]**:

   * Verwenden Sie die **[!UICONTROL Bearbeiten]**, um eine **[!UICONTROL Farbpalette]** mit Standardfarben für Ihre Marke einzurichten. Wählen Sie **[!UICONTROL Vorgabe]** aus, um schnell ein Farbschema zu erstellen oder jede Farbe Ihres Designs individuell anzupassen. Sie können auch eine Kombination aus beiden verwenden.

     ![](assets/theme-colors.gif)

   * Klicken Sie **[!UICONTROL Variante hinzufügen]**, um mehrere Farbvarianten zu erstellen, z. B. den Hell- und Dunkelmodus, wobei jede Variante über eine eigene Farbpalette und Nuancensteuerelemente verfügt.

     ![](assets/theme-colors-variant.png)

   * Klicken Sie für jede Variante auf das Symbol Bearbeiten , um ein einzelnes Element zu bearbeiten. Sie können die von Ihnen erstellte Standardpalette oder beliebige benutzerdefinierte Farben verwenden.

     ![](assets/theme-colors-edit-variant.gif)

1. In den **[!UICONTROL Texteinstellungen]** können Sie die globale Schriftart festlegen, die Sie für Ihr gesamtes Design verwenden möchten. Für ein detaillierteres Steuerelement können Sie auch jede Überschrift und jeden Absatztyp bearbeiten, um die Schriftart, die Größe, den Stil usw. anzupassen.

   ![](assets/theme-text.png)

1. Wählen Sie auf der Registerkarte **[!UICONTROL Abstand]** ein einzelnes Element aus der Liste aus, um es ordnungsgemäß zwischen den verschiedenen Komponenten aufzuteilen.

   <!--![](assets/theme-spacing.png)-->

1. Mit den anderen Registerkarten auf der rechten Seite können Sie jedes Schaltflächenelement, jede Trennlinie, zusätzliche Bildformatierung und den Rasterlayoutabstand für dieses Design separat verwalten.

   <!--![](assets/theme-buttons.png)-->

1. Klicken Sie **[!UICONTROL Speichern]**, um dieses Design für die zukünftige Verwendung zu speichern.

## Anwenden von Designs auf eine E-Mail {#apply-themes}

Gehen Sie wie folgt vor, um standardmäßige oder benutzerdefinierte Stildesigns auf eine E-Mail anzuwenden.

1. Fügen Sie [!DNL Journey Optimizer] die Aktion [E-Mail hinzufügen](create-email.md) zu einer Journey oder Kampagne hinzu und [bearbeiten Sie den Textkörper Ihrer E-Mail](get-started-email-design.md#key-steps).

1. Sie können eine der folgenden Aktionen auswählen:

   * Wählen Sie eine integrierte [E-Mail-Vorlage](use-email-templates.md) aus, um die E-Mail-Designer zu öffnen. Ein für jede Vorlage spezifisches Standarddesign wird automatisch angewendet.

   * Entwerfen Sie [neuen Inhalt von Grund auf](content-from-scratch.md) und wählen Sie **[!UICONTROL Design]**, um mit einem vordefinierten Stildesign zu beginnen.

     ![](assets/theme-from-scratch.png)

     >[!CAUTION]
     >
     >Wenn Sie den klassischen Modus wählen, können Sie keine Designs anwenden, es sei denn, Sie setzen Ihre E-Mail zurück.
     >
     >Um ein [Fragment](../content-management/fragments.md) im Design-Modus zu verwenden, muss dieses Fragment selbst im Design-Modus erstellt worden sein.

1. Klicken Sie in der E-Mail-Designer in der rechten Leiste auf **[!UICONTROL Designs]**-Schaltfläche. Das Standarddesign oder das Design der Vorlage wird angezeigt. Sie können zwischen den beiden Farbvarianten für dieses Design wechseln.

   ![](assets/theme-default-hero.png)

1. Klicken Sie auf den Pfeil neben dem aktuell verwendeten Design. Die Liste der verfügbaren benutzerdefinierten und Adobe-Designs wird angezeigt.

   ![](assets/theme-hero-change.png)

1. Klicken Sie **[!UICONTROL Benutzerdefinierte Designs]** und wählen Sie das von Ihnen erstellte Design aus.

   ![](assets/theme-select-custom.png)

1. Klicken Sie außerhalb der Dropdown-Liste. Das neu ausgewählte benutzerdefinierte Design wendet seine Stile automatisch auf alle E-Mail-Komponenten an. Sie können zwischen den beiden Farbvarianten wechseln.

1. Wenn eine Komponente ausgewählt wird, können Sie ihren Stil immer noch über das entsprechende Symbol entsperren.

   ![](assets/theme-unlock-style.png)

Sie können jederzeit zwischen Designs wechseln. Der E-Mail-Inhalt bleibt unverändert, aber die Stile werden aktualisiert, um das neue Design widerzuspiegeln.

<!--
>[!NOTE]
> - Themes apply styles globally. Ensure your theme is finalized before applying it to multiple emails.
> - Switching themes may override custom styles applied to individual components.

>[!CAUTION]
> - When using fragments, the email's theme will override the fragment's styles. A warning will be displayed in the editor if there is a conflict.

## Example Use Cases {#example-use-cases}

### 1. Creating a New Theme
- A marketer creates a theme with their brand's colors, fonts, and button styles.
- The theme is saved and reused across multiple email campaigns.

### 2. Switching Themes
- A marketer applies a holiday-themed design to an existing email by switching to a pre-designed holiday theme.-->
