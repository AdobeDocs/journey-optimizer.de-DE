---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen und Planen orchestrierter Kampagnen mit Journey Optimizer
description: Erfahren Sie, wie Sie mit Adobe Journey Optimizer eine koordinierte Kampagne erstellen
badge: label="Alpha"
hide: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: d59643f18a335fe1e094156a1cfee65b717b9fce
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 20%

---


# Erstellen und Planen einer orchestrierten Kampagne {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Liste der orchestrierten Kampagnen"
>abstract="Auf **Registerkarte** Orchestrierung“ werden alle orchestrierten Kampagnen aufgelistet. Klicken Sie auf den Namen einer orchestrierten Kampagne, um sie zu bearbeiten. Über die Schaltfläche **Orchestrierte Kampagne erstellen** können Sie eine neue orchestrierte Kampagne hinzufügen."

## Erstellen der Kampagne {#create}

Gehen Sie wie folgt vor, um eine orchestrierte Kampagne zu erstellen:

1. Navigieren Sie zum Menü **[!UICONTROL Kampagnen]**, wählen Sie die Registerkarte **[!UICONTROL Orchestrierung]** und wählen Sie **[!UICONTROL Kampagne erstellen]** aus.

   ![](assets/inventory-create.png)

1. Geben Sie einen Namen für die orchestrierte Kampagne ein. Darüber hinaus empfehlen wir dringend, eine Beschreibung in das entsprechende Feld einzufügen.

1. (Optional) Verwenden Sie das Feld **Tags**, um Ihrer orchestrierten Kampagne einheitliche Adobe Experience Platform-Tags zuzuweisen. Dies ermöglicht eine einfache Klassifizierung und verbesserte Suche über die Kampagnenliste. [Erfahren Sie, wie Sie mit Tags arbeiten](../start/search-filter-categorize.md#tags).

1. Klicken Sie zur Bestätigung auf **[!UICONTROL Erstellen]**.


Ihre orchestrierte Kampagne wird jetzt erstellt und ist in der Kampagnenliste verfügbar. Sie können diese Eigenschaften jederzeit ändern, indem Sie auf das Symbol ![Kampagneneinstellungen](assets/do-not-localize/campaign-settings.svg) auf der Kampagnenarbeitsfläche klicken.


## Planen der Kampagne {#schedule}

Standardmäßig beginnen orchestrierte Kampagnen, sobald sie manuell aktiviert werden, und enden, sobald ihre Aktivitäten ausgeführt wurden.

Wenn Sie eine orchestrierte Kampagne nicht direkt nach der Aktivierung ausführen möchten, können Sie ein Datum und eine Uhrzeit für die Ausführung angeben. Sie können die Kampagne auch in regelmäßigen Abständen ausführen, basierend auf verschiedenen Kriterien.

Um den Zeitplan der Kampagne zu konfigurieren, öffnen Sie die orchestrierte Kampagne und klicken Sie auf die Schaltfläche **[!UICONTROL So bald wie möglich]**.

![](assets/create-schedule.png)

<!--In the Execution frequency field, select 

time zone

daily, weekly, monthly
several times a day based on specific hours or periodically

recurring frequencies (all except as soon and once)
preview launch times
validity period

>[!NOTE]
>
>When scheduling campaigns in [!DNL Adobe Journey Optimizer], ensure your start date/time aligns with the desired first delivery. For recurring campaigns, if the initial scheduled time has already passed, the campaigns will roll over to the next available time slot according to their recurrence rules.

## Work with orchestrated campaign templates {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Orchestrated campaign templates"
>abstract="Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaign."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Orchestrated campaign properties"
>abstract="Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaigns. In this screen, enter the label of the orchestrated campaign template and configure its settings such as its internal name, folder and execution folders, timezone, and supervisor group."

Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaigns. You can select the template of your orchestrated campaign from the orchestrated campaign properties, when creating an orchestrated campaign. An empty template is provided by default.

You can create a template from an existing orchestrated campaign, or create a new template from scratch. Both methods are detailed below.

>[!BEGINTABS]

>[!TAB Create a template from an existing orchestrated campaign]

To create an orchestrated campaign template from an existing orchestrated campaign, follow these steps:

1. Open to the **Campaign** menu and browse to the orchestrated campaign to save as a template.
1. Click the three dots on the right of the name of the orchestrated campaign, and choose **Copy as template**.
1. In the popup window, confirm the template creation.
1. In the orchestrated campaign template canvas, check, add, and configure the activities as needed.
1. Browse to the settings, from the **Settings** button, to change the name of the orchestrated campaign template, and enter a description.
1. Select the **folder** and **execution folder** of the template. The folder is the location where the orchestrated campaign template is saved. The execution folder is the folder where orchestrated campaigns created based on this template are saved.
1. Save your changes. 

The orchestrated campaign template is now available in the template list. You can create an orchestrated campaign based on this template. This orchestrated campaign will be pre-configured with the settings and activities defined in the template.


>[!TAB Create a template from scratch]


To create an orchestrated campaign template from scratch, follow these steps:

1. Open to the **Campaign** menu and browse to the **Templates** tab. You can see the list of available orchestrated campaign templates.
1. Click the **[!UICONTROL Create template]** button in the upper-right corner of the screen.
1. Enter the label and open the additional options to enter a description of your orchestrated campaign template.
1. Select the folder and execution folder of the template. The folder is the location where the orchestrated campaign template is saved. The execution folder is the folder where orchestrated campaigns created based on this template are saved.
1. Click the **Create** button to confirm your settings.
1. In the orchestrated campaign template canvas, add and configure the activities as needed.

     ![](assets/wf-template-activities.png){zoomable="yes"}

1. Save your changes. 

The orchestrated campaign template is now available in the template list. You can create an orchestrated campaign based on this template. This orchestrated campaign will be pre-configured with the settings and activities defined in the template.

>[!ENDTABS]






## Next steps {#next}

Once your campaign configuration and content are ready, you can review and activate it. [Learn more](review-activate-campaign.md)

-->