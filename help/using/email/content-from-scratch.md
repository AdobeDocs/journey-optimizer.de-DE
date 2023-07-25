---
solution: Journey Optimizer
product: journey optimizer
title: Inhalte in Journey Optimizer von Grund auf gestalten
description: Erfahren Sie, wie Sie Ihre Inhalte von Grund auf neu gestalten
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: Inhalt, Editor, E-Mail, Start
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 100%

---

# Inhalte von Grund auf gestalten {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der E-Mail. Ziehen Sie eine **Struktur**-Komponente per Drag-and-Drop auf die Arbeitsfläche, um mit der Gestaltung Ihres E-Mail-Inhalts zu beginnen."

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der Landingpage. Ziehen Sie eine **Struktur**-Komponente per Drag-and-Drop auf die Arbeitsfläche, um mit der Gestaltung Ihres Landingpage-Inhalts zu beginnen."

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout des Fragments. Ziehen Sie eine **Struktur**-Komponente per Drag-and-Drop auf die Arbeitsfläche, um mit der Gestaltung Ihres Fragmentinhalts zu beginnen."

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der Vorlage. Ziehen Sie eine **Struktur**-Komponente per Drag-and-Drop auf die Arbeitsfläche, um mit der Gestaltung Ihres Vorlageninhalts zu beginnen."


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="Definieren von E-Mail-Spalten"
>abstract="Mit dem E-Mail-Designer können Sie das Layout einer E-Mail einfach definieren, indem Sie die Spaltenstruktur auswählen."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="Definieren der Spalten für die Landingpage"
>abstract="Mit dem E-Mail-Designer können Sie das Layout Ihrer Landingpage einfach definieren, indem Sie die Spaltenstruktur auswählen."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="Definieren von Fragmentspalten"
>abstract="Mit dem E-Mail-Designer können Sie das Layout Ihres Fragments einfach definieren, indem Sie die Spaltenstruktur auswählen."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="Definieren von Vorlagenspalten"
>abstract="Mit dem E-Mail-Designer können Sie das Layout Ihrer Vorlage einfach definieren, indem Sie die Spaltenstruktur auswählen."


Verwenden Sie den Adobe Journey Optimizer-Designer, um die Struktur Ihrer Inhalte einfach zu definieren. Durch das Hinzufügen und Verschieben von strukturellen Elementen mit einfachem Drag-and-Drop können Sie Ihrer E-Mail in Sekundenschnelle die gewünschte Form verleihen.

Gehen Sie wie folgt vor, um mit der Erstellung des Ihrers Inhalts zu beginnen:

1. Wählen Sie auf der Startseite von Designer die Option **[!UICONTROL Erstellen von neuen Inhalten]** aus.

   ![](assets/email_designer.png)

1. Beginnen Sie mit der Gestaltung Ihres Inhalts, indem Sie **[!UICONTROL Strukturen]** per Drag-and-Drop auf die Arbeitsfläche ziehen, um das Layout Ihrer E-Mail zu definieren.

   >[!NOTE]
   >
   >Die Stapelung von Spalten ist nicht mit allen E-Mail-Programmen kompatibel. Wenn dies nicht unterstützt wird, werden Spalten nicht gestapelt.

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. Fügen Sie so viele **[!UICONTROL Strukturen]** hinzu, wie benötigt werden, und bearbeiten Sie deren Einstellungen im entsprechenden Bereich auf der rechten Seite.

   ![](assets/email_designer_structure_components.png)

   Wählen Sie die Komponente **[!UICONTROL n:n Spalte]** aus, um die Anzahl der Spalten zu definieren (3 bis 10). Sie können auch die Breite jeder Spalte ändern, indem Sie den Pfeil am unteren Rand einer jeden Spalte verschieben.

   >[!NOTE]
   >
   >Die Größe einer Spalte muss immer mindestens 10 % der Gesamtbreite der Strukturkomponente betragen. Sie können nur leere Spalten entfernen.

1. Erweitern Sie den Abschnitt **[!UICONTROL Inhalte]** und fügen Sie beliebig viele Elemente zu einer oder mehreren Strukturkomponenten hinzu. [Weitere Informationen zu Inhaltskomponenten](content-components.md)

1. Jede Komponente kann mithilfe der Registerkarten **[!UICONTROL Einstellungen]** oder **[!UICONTROL Stil]** im rechten Menü angepasst werden. Beispielsweise können Sie den Textstil, den Abstand oder den Rand jeder Komponente ändern. [Erfahren Sie mehr über Ausrichtung und Abstand](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. Über die **[!UICONTROL Asset-Auswahl]** können Sie direkt Assets auswählen, die in der **[!UICONTROL Asset-Bibliothek]** gespeichert sind. [Weitere Informationen über Asset-Management](assets-essentials.md)

   Klicken Sie doppelt auf den Ordner, der Ihre Assets enthält. Ziehen Sie sie per Drag-and-Drop in eine Strukturkomponente.

   ![](assets/email_designer_asset_picker.png)

1. Fügen Sie Personalisierungsfelder ein, um Ihren Inhalt aus Profilattributen, Zielgruppenzugehörigkeiten, Kontextattributen und mehr anzupassen. [Weitere Informationen über die Personalisierung von Inhalten](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. Klicken Sie auf **[!UICONTROL Bedingten Inhalt aktivieren]**, um dynamischen Inhalt hinzuzufügen und den Inhalt auf der Grundlage von bedingten Regeln an die Zielprofile anzupassen. [Erste Schritte mit dynamischen Inhalten](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Links]** im linken Bereich, um die Liste aller zu verfolgenden URLs Ihres Inhalts anzuzeigen. Sie können bei Bedarf deren **[!UICONTROL Tracking-Typ]** oder **[!UICONTROL Beschriftung]** ändern und **[!UICONTROL Tags]** hinzufügen. [Erfahren Sie mehr über Links und Tracking](message-tracking.md)

   ![](assets/email_designer_links.png)

1. Bei Bedarf können Sie Ihre E-Mail weiter personalisieren, indem Sie im erweiterten Menü auf **[!UICONTROL Zum Code-Editor wechseln]** klicken. Auf diese Weise können Sie den E-Mail-Quell-Code bearbeiten, z. B. um Tracking- oder benutzerdefinierte HTML-Tags hinzuzufügen. [Erfahren Sie mehr über den Code-Editor](code-content.md)

   >[!CAUTION]
   >
   >Nach dem Wechsel zum Code-Editor können Sie für diese E-Mail nicht mehr zum visuellen Designer zurückkehren.

1. Wenn Ihr Inhalt fertig ist, klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt simulieren]**, um das Rendering zu überprüfen. Sie können zwischen der Desktop- oder der mobilen Ansicht wählen. [Erfahren Sie mehr über die Vorschau Ihrer E-Mail](preview.md)

   ![](assets/email_designer_simulate_content.png)

1. Wenn Ihre E-Mail fertig ist, klicken Sie auf **[!UICONTROL Speichern]**.

