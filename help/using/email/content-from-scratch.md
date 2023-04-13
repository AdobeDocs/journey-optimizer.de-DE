---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen von neuen Inhalten in Journey Optimizer
description: Erfahren Sie, wie Sie Ihren Inhalt von Grund auf neu erstellen
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: Inhalt, Editor, E-Mail, Start
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: 4ce8573aa76ceae807d404e736b2d780f687aa56
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 40%

---

# Neuen Inhalt erstellen {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der E-Mail. Ziehen und Ablegen eines **Struktur** in die Arbeitsfläche, um mit der Erstellung Ihres E-Mail-Inhalts zu beginnen."

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der Landingpage. Ziehen und Ablegen eines **Struktur** in die Arbeitsfläche, um mit der Erstellung des Inhalts Ihrer Landingpage zu beginnen."

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout des Fragments. Ziehen und Ablegen eines **Struktur** in die Arbeitsfläche, um mit der Erstellung des Inhalts Ihres Fragments zu beginnen."

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="Hinzufügen von Strukturkomponenten"
>abstract="Strukturkomponenten definieren das Layout der Vorlage. Ziehen und Ablegen eines **Struktur** in die Arbeitsfläche, um mit der Erstellung des Inhalts Ihrer Vorlage zu beginnen."


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="E-Mail-Spalten definieren"
>abstract="Mit Email Designer können Sie das Layout Ihrer E-Mail einfach definieren, indem Sie die Spaltenstruktur auswählen."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="Landingpage-Spalten definieren"
>abstract="Mit Designer können Sie das Layout Ihrer Landingpage einfach definieren, indem Sie die Spaltenstruktur auswählen."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="Fragmentspalten definieren"
>abstract="Mit Designer können Sie das Layout Ihres Fragments einfach definieren, indem Sie die Spaltenstruktur auswählen."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="Vorlagenspalten definieren"
>abstract="Mit Designer können Sie das Layout Ihrer Vorlage einfach definieren, indem Sie die Spaltenstruktur auswählen."


Verwenden Sie Adobe Journey Optimizer Designer, um die Inhaltsstruktur einfach zu definieren. Durch das Hinzufügen und Verschieben von Strukturelementen mit einfachen Drag &amp; Drop-Aktionen können Sie die Form Ihres Inhalts innerhalb von Sekunden entwerfen.

Gehen Sie wie folgt vor, um mit der Erstellung des Inhalts Ihrer zu beginnen:

1. Wählen Sie auf der Startseite von Designer die Option **[!UICONTROL Erstellen von neuen Inhalten]** aus.

   ![](assets/email_designer.png)

1. Beginnen Sie mit der Erstellung Ihres Inhalts durch Drag &amp; Drop **[!UICONTROL Strukturen]** in die Arbeitsfläche, um das Layout Ihrer E-Mail zu definieren.

   >[!NOTE]
   >
   >Die Stapelung von Spalten ist nicht mit allen E-Mail-Programmen kompatibel. Wenn dies nicht unterstützt wird, werden Spalten nicht gestapelt.

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. Fügen Sie so viele hinzu wie **[!UICONTROL Strukturen]** nach Bedarf und bearbeiten Sie die Einstellungen im dedizierten Bereich auf der rechten Seite.

   ![](assets/email_designer_structure_components.png)

   Wählen Sie die Komponente **[!UICONTROL n:n Spalte]** aus, um die Anzahl der Spalten zu definieren (3 bis 10). Sie können auch die Breite jeder Spalte ändern, indem Sie den Pfeil am unteren Rand einer jeden Spalte verschieben.

   >[!NOTE]
   >
   >Die Größe einer Spalte muss immer mindestens 10 % der Gesamtbreite der Strukturkomponente betragen. Sie können nur leere Spalten entfernen.

1. Erweitern Sie die **[!UICONTROL Inhalt]** und fügen Sie beliebig viele Elemente zu einer oder mehreren Strukturkomponenten hinzu. [Weitere Informationen zu Inhaltskomponenten](content-components.md)

1. Jede Komponente kann mithilfe der **[!UICONTROL Einstellungen]** oder **[!UICONTROL Stil]** Registerkarten im rechten Menü. Beispielsweise können Sie den Textstil, den Abstand oder den Rand jeder Komponente ändern. [Erfahren Sie mehr über Ausrichtung und Abstand](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. Über die **[!UICONTROL Asset-Auswahl]** können Sie direkt Assets auswählen, die in der **[!UICONTROL Asset-Bibliothek]** gespeichert sind. [Weitere Informationen über Asset-Management](assets-essentials.md)

   Klicken Sie doppelt auf den Ordner, der Ihre Assets enthält. Ziehen Sie sie per Drag-and-Drop in eine Strukturkomponente.

   ![](assets/email_designer_asset_picker.png)

1. Fügen Sie Personalisierungsfelder ein, um Ihren Inhalt aus Profilattributen, Segmentmitgliedschaften, Kontextattributen und mehr anzupassen. [Weitere Informationen über die Personalisierung von Inhalten](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. Klicken **[!UICONTROL Bedingungsinhalt aktivieren]** um dynamischen Inhalt hinzuzufügen und den Inhalt auf der Grundlage von bedingten Regeln an die Zielprofile anzupassen. [Erste Schritte mit dynamischen Inhalten](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Links]** im linken Bereich, um die Liste aller zu verfolgenden URLs Ihres Inhalts anzuzeigen. Sie können bei Bedarf deren **[!UICONTROL Tracking-Typ]** oder **[!UICONTROL Beschriftung]** ändern und **[!UICONTROL Tags]** hinzufügen. [Weitere Informationen zu Links und Tracking](message-tracking.md)

   ![](assets/email_designer_links.png)

1. Bei Bedarf können Sie den Inhalt weiter personalisieren, indem Sie auf **[!UICONTROL Wechseln zum Code-Editor]** von oben **Mehr** Schaltfläche. [Erfahren Sie mehr über den Code-Editor](code-content.md)

   ![](assets/email_designer_switch-to-code.png)

   >[!CAUTION]
   >
   >Sie können den visuellen Designer für diesen Inhalt nicht wiederherstellen, nachdem Sie zum Code-Editor gewechselt haben.

1. Sobald Ihr Inhalt fertig ist, klicken Sie auf die **[!UICONTROL Inhalt simulieren]** -Schaltfläche, um das Rendering zu überprüfen. Sie können zwischen der Desktop- oder der mobilen Ansicht wählen. [Erfahren Sie mehr über die Vorschau Ihrer E-Mail](preview.md)

   ![](assets/email_designer_simulate_content.png)

1. Wenn Ihr Inhalt fertig ist, klicken Sie auf **[!UICONTROL Speichern]**.

