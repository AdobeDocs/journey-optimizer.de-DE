---
solution: Journey Optimizer
product: journey optimizer
title: Entwerfen von E-Mails in Journey Optimizer
description: Erfahren Sie, wie Sie E-Mail-Inhalte  von Grund auf neu entwerfen
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 52%

---

# Von Grund auf neu beginnen {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="Über Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der E-Mail."

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="Über Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der Landingpage."

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="Über Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout des Fragments."

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="Über Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der Vorlage."


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="Definieren von E-Mail-Spalten"
>abstract="Mit Email Designer können Sie das Layout Ihrer E-Mail einfach definieren, indem Sie die Spaltenstruktur definieren."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="Definieren der Spalten für die Landingpage"
>abstract="Mit dem E-Mail-Designer können Sie das Layout Ihrer Landingpage einfach definieren, indem Sie die Spaltenstruktur definieren."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="Definieren der Fragmentspalten"
>abstract="Mit dem E-Mail-Designer können Sie das Layout Ihres Fragments einfach definieren, indem Sie die Spaltenstruktur definieren."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="Definieren der Vorlagenspalten"
>abstract="Mit dem E-Mail-Designer können Sie das Layout Ihrer Vorlage einfach definieren, indem Sie die Spaltenstruktur definieren."


Email Designer bietet eine einfache Möglichkeit, die Struktur Ihrer E-Mail zu bestimmen. Durch das Hinzufügen und Verschieben von strukturellen Elementen durch einfaches Drag &amp; Drop können Sie Ihrer E-Mail in Sekundenschnelle die gewünschte Form verleihen.

Gehen Sie wie folgt vor, um mit der Erstellung Ihres E-Mail-Inhalts zu beginnen:

1. Wählen Sie auf der Startseite von Email Designer die Option **[!UICONTROL Erstellen von neuen Inhalten]** aus.

   ![](assets/email_designer.png)

1. Beginnen Sie mit der Erstellung Ihres E-Mail-Inhalts durch Drag &amp; Drop **[!UICONTROL Strukturkomponenten]** in die Arbeitsfläche, um das Layout Ihrer E-Mail zu definieren.

   >[!NOTE]
   >
   >Die Stapelung von Spalten ist nicht mit allen E-Mail-Programmen kompatibel. Wenn sie nicht unterstützt werden, werden Spalten nicht gestapelt.

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. Fügen Sie so viele hinzu wie **[!UICONTROL Strukturkomponenten]** nach Bedarf und bearbeiten Sie die Einstellungen im dedizierten Bereich auf der rechten Seite.

   ![](assets/email_designer_structure_components.png)

   Wählen Sie die Komponente **[!UICONTROL n:n Spalte]** aus, um die Anzahl der Spalten zu definieren (3 bis 10). Sie können auch die Breite jeder Spalte ändern, indem Sie den Pfeil am unteren Rand einer jeden Spalte verschieben.

   ![](assets/email_designer_structure_n-n-colum.png)

   >[!NOTE]
   >
   >Die Größe einer Spalte muss immer mindestens 10 % der Gesamtbreite der Strukturkomponente betragen. Sie können nur leere Spalten entfernen.

1. Erweitern Sie die **[!UICONTROL Inhaltskomponenten]** und fügen Sie beliebig viele Elemente zu einer oder mehreren Strukturkomponenten hinzu. [Weitere Informationen zu Inhaltskomponenten](content-components.md)

1. Jede Komponente kann mithilfe der **[!UICONTROL Komponenteneinstellungen]** rechts. Sie können beispielsweise den Textstil, den Abstand oder den Rand jeder Komponente ändern. [Erfahren Sie mehr über Ausrichtung und Abstand](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. Aus dem **[!UICONTROL Asset-Auswahl]** können Sie direkt Assets auswählen, die in der **[!UICONTROL Asset-Bibliothek]**. [Weitere Informationen über Asset-Management](assets-essentials.md)

   Doppelklicken Sie auf den Ordner, der Ihre Assets enthält. Ziehen Sie sie per Drag-and-Drop in eine Strukturkomponente.

   ![](assets/email_designer_asset_picker.png)

1. Fügen Sie Personalisierungsfelder ein, um Ihren E-Mail-Inhalt aus Profildaten anzupassen. [Weitere Informationen über die Personalisierung von Inhalt](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. Fügen Sie dynamische Inhalte hinzu, um den Inhalt auf der Grundlage von bedingten Regeln an die Zielprofile anzupassen. [Erste Schritte mit dynamischen Inhalten](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. Klicken Sie auf **[!UICONTROL Links]** im linken Bereich, um alle getrackten URLs Ihres Inhalts anzuzeigen. Sie können die **[!UICONTROL Tracking-Typ]** oder **[!UICONTROL Titel]** und hinzufügen **[!UICONTROL Tags]** bei Bedarf. [Erfahren Sie mehr über Links und Nachrichten-Tracking](message-tracking.md)

   ![](assets/email_designer_links.png)

1. Bei Bedarf können Sie Ihre E-Mail weiter personalisieren, indem Sie auf **[!UICONTROL Wechseln zum Code-Editor]** aus dem erweiterten Menü. [Erfahren Sie mehr über den Code-Editor](code-content.md)

   ![](assets/email_designer_switch-to-code.png)

   >[!CAUTION]
   >
   >Sie können nach dem Wechsel zum Code-Editor nicht zum Visual Designer für diese E-Mail zurückkehren.

1. Sobald Ihr Inhalt fertig ist, klicken Sie auf **[!UICONTROL Inhalt simulieren]** , um Ihr E-Mail-Rendering zu überprüfen. Sie können zwischen der Desktop- oder der mobilen Ansicht wählen. [Erfahren Sie mehr über die Vorschau Ihrer E-Mail](preview.md)

   ![](assets/email_designer_simulate_content.png)

1. Wenn Ihre E-Mail fertig ist, klicken Sie auf **[!UICONTROL Speichern]**.

