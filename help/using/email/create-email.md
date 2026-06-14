---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen einer E-Mail
description: Erfahren Sie, wie Sie in Journey Optimizer eine E-Mail erstellen.
feature: Email
topic: Content Management
role: User
level: Beginner
keywords: Erstellen, E-Mail, Starten, Journey, Kampagne
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
TQID: https://experienceleague.adobe.com/EM2msybn-3qaRJz113oIwMOU4Aj9h3BiDeLnl4vpO-Q
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: a5683ded-e5d5-4ec6-b9fd-e1b56a94ab96
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: fae48155-b23f-40d2-a252-a25bce350b4d
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: bc98cb2b61c7c5c8dac78b494fe293a4106a88c4
workflow-type: tm+mt
source-wordcount: 1272
ht-degree: 69%

---

# Erstellen einer E-Mail {#create-email}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie eine E-Mail-Aktion zu einer Journey oder Kampagne in Adobe Journey Optimizer hinzufügen, den Betreff und den Inhalt definieren, Warnhinweise überprüfen und eine Vorschau anzeigen, bevor Sie senden.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="E-Mail-Erstellung"
>abstract="Die Betreffzeile der E-Mail erstellen und den E-Mail-Designer öffnen, um den Inhalt der E-Mail zu erstellen."

## Hinzufügen einer E-Mail-Aktion {#email-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_email"
>title="E-Mail-Aktion"
>abstract="Eine E-Mail-Kanalaktion sendet eine E-Mail an Profile, wenn sie diesen Schritt des Journey erreichen. Die Bezeichnung identifiziert die Aktivität auf der Journey-Arbeitsfläche und die Aktion verweist auf eine E-Mail-Konfiguration, die den bereitgestellten Inhalt definiert. Der Abschnitt **Optimierung** kann Inhaltsexperimente oder Zielgruppenbestimmungsregeln enthalten, der Abschnitt **Mehrsprachig** kann Inhalte in mehreren Sprachen bereitstellen, und der Abschnitt **Zeitüberschreitung oder Fehler** kann einen alternativen Pfad definieren, wenn die Aktion fehlschlägt."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/about-journey-building/journey-action#add-action" text="Erste Schritte mit Kanalaktionen"

Um eine E-Mail in [!DNL Journey Optimizer] zu erstellen, fügen Sie eine **[!UICONTROL E-Mail-Aktion]** auf eine Journey oder eine Kampagne. Führen Sie dann je nach Fall die folgenden Schritte aus.

>[!BEGINTABS]

>[!TAB Hinzufügen einer E-Mail zu einer Journey]

1. Öffnen Sie Ihren Journey und ziehen Sie eine Aktivität **[!UICONTROL Aktion]** per Drag-and-Drop aus dem Bereich **[!UICONTROL Aktionen]** der Palette. Weitere Informationen über die [Aktionsaktivität](../building-journeys/journey-action.md).

   >[!IMPORTANT]
   >
   >Ältere native Kanalaktivitäten (E-Mail, Push, SMS, In-App, Web, Code-basiertes Erlebnis und Inhaltskarte) werden seit der Version vom März 2026 nicht mehr unterstützt. Vorhandene Journey, die diese Aktivitäten verwenden, funktionieren weiterhin unverändert - es ist keine Migration erforderlich.

1. Wählen **[!UICONTROL als]** „E-Mail“ aus.

   ![](assets/email_journey.png)

1. Geben Sie einen **[!UICONTROL Titel]** ein, um Ihre Aktion auf der Journey-Arbeitsfläche zu identifizieren.

1. Klicken Sie auf **[!UICONTROL Schaltfläche „Aktion konfigurieren]**.

1. Sie werden zur Registerkarte **[!UICONTROL Aktionen]** geleitet. Wählen oder erstellen Sie von dort aus die zu verwendende E-Mail-Konfiguration. [Weitere Informationen](email-settings.md)

   ![](assets/email-action-config.png)

1. Zusätzlich gilt:

   * Sie können Begrenzungsregeln auf Ihre E-Mail-Aktion anwenden, indem Sie einen Regelsatz in der Dropdown-Liste **[!UICONTROL Geschäftsregeln]** auswählen. [Weitere Informationen](../conflict-prioritization/channel-capping.md)

   * Sie können die Option **[!DNL Send time optimization]** verwenden, um die beste Versandzeit für die Nachricht vorherzusagen und so die Interaktion basierend auf historischen Öffnungs- und Klickraten zu maximieren. [Weitere Informationen](../building-journeys/send-time-optimization.md)

1. Klicken Sie auf die **[!UICONTROL Inhalt bearbeiten]** und erstellen Sie Ihren Inhalt nach Bedarf mit der E-Mail-Designer. [Weitere Informationen](#define-email-content)

1. Zurück zur Journey-Arbeitsfläche. Schließen Sie bei Bedarf Ihren Journey-Fluss ab, indem Sie zusätzliche Aktionen oder Ereignisse per Drag-and-Drop verschieben. [Weitere Informationen](../building-journeys/about-journey-activities.md)

Weitere Informationen zum Erstellen, Konfigurieren und Veröffentlichen einer Journey finden Sie auf [dieser Seite](../building-journeys/journey-gs.md).

>[!TAB Hinzufügen einer E-Mail zu einer Kampagne]

1. [Erstellen Sie eine Kampagne](../campaigns/create-campaign.md) und wählen Sie **[!UICONTROL E-Mail]** als Aktion aus.

1. Führen Sie die Schritte zur Erstellung einer E-Mail-Kampagne aus, z. B. die Kampagneneigenschaften, [Zielgruppe](../audience/about-audiences.md) und [Zeitplan](../campaigns/campaign-schedule.md).

   ![](assets/email_campaign_steps.png)

1. Wählen Sie die Aktion **[!UICONTROL E-Mail]** aus.

1. Wählen Sie die E-Mail-Konfiguration aus oder erstellen Sie sie. [Weitere Informationen](email-settings.md)

   ![](assets/email_campaign.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->
Weitere Informationen zum Erstellen, Konfigurieren und Aktivieren einer Kampagne finden Sie auf [&#x200B; Seite](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## Definieren des E-Mail-Inhalts {#define-email-content}

<!-- update the quarry component with right ID value-->

>[!CONTEXTUALHELP]
>id="test_id"
>title="Konfigurieren von E-Mail-Inhalten"
>abstract="Erstellen Sie den Inhalt Ihrer E-Mail. Definieren Sie den Betreff und verwenden Sie dann den E-Mail-Designer, um den Text der E-Mail zu erstellen und zu personalisieren."

Nachdem Sie die E-Mail-Aktion zu Ihrer Journey oder Kampagne hinzugefügt haben, müssen Sie den E-Mail-Inhalt einschließlich Betreffzeile, Absenderinformationen und E-Mail-Textkörper mit dem E-Mail-Designer definieren. Führen Sie folgende Schritte aus:

1. Klicken Sie auf dem Konfigurationsbildschirm der Journey oder Kampagne auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]**, um den Inhalt der E-Mail zu konfigurieren. [Weitere Informationen](get-started-email-design.md)

   ![](assets/email_campaign_edit_content.png)

1. Schalten Sie **[!UICONTROL Entscheidungsfindung aktivieren]** ein, wenn Sie Ihrer E-Mail Entscheidungsrichtlinien hinzufügen möchten.

   Entscheidungsrichtlinien sind Container für Ihre Angebote, die die Entscheidungs-Engine nutzen, um dynamisch die besten Inhalte für jedes Zielgruppenmitglied zurückzugeben. [Infomationen zum Hinzufügen einer Entscheidungsrichtlinie in einer E-Mail](../experience-decisioning/create-decision.md#create-decision)

   ![](assets/../../experience-decisioning/assets/decision-policy-enable.png)

   >[!AVAILABILITY]
   >
   >Derzeit ist die Erstellung von Entscheidungsrichtlinien in E-Mails nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

1. Überprüfen Sie im Abschnitt **[!UICONTROL Header]** die Felder **[!UICONTROL Name der Absenderin bzw. des Absenders]**, **[!UICONTROL Von E-Mail]** und **[!UICONTROL BCC]**. Sie werden in der von Ihnen ausgewählten E-Mail-Konfiguration konfiguriert. [Weitere Informationen](email-settings.md) <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. Fügen Sie eine Betreffzeile für Ihre Nachricht hinzu. Um die Betreffzeile mit dem Personalisierungseditor zu konfigurieren und zu personalisieren, klicken Sie auf das Symbol **[!UICONTROL Personalisierungsdialog öffnen]**. [Weitere Informationen](../personalization/personalization-build-expressions.md)

   >[!NOTE]
   >
   >Die Betreffzeile ist obligatorisch. Sie darf keine Zeilenumbrüche enthalten.

1. Klicken Sie auf **[!UICONTROL E-Mail-Text bearbeiten]**, um auf den E-Mail-Designer zugreifen und mit der Erstellung Ihres Inhalts zu beginnen. [Weitere Informationen](get-started-email-design.md)

   ![](assets/email_designer_edit_email_body.png)

1. Wenn Sie sich in einer Kampagne befinden, können Sie auch auf die Schaltfläche **[!UICONTROL Code-Editor]** klicken, um Ihren eigenen Inhalt über das angezeigte Popup-Fenster in HTML zu schreiben.

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >Wenn Sie bereits über den E-Mail-Designer Inhalt erstellt oder importiert haben, wird dieser Inhalt in HTML angezeigt.

## Prüfen von Warnhinweisen {#check-email-alerts}

Während Sie Ihre Nachrichten entwerfen, werden Warnhinweise in der Benutzeroberfläche (oben rechts auf dem Bildschirm) angezeigt, wenn wichtige Einstellungen fehlen.

![](assets/email_journey_alerts_details.png)

>[!NOTE]
>
>Wenn diese Schaltfläche nicht angezeigt wird, wurde kein Warnhinweis erkannt.

Die vom System geprüften Einstellungen und Elemente sind unten aufgeführt. Sie finden hier auch Informationen zur Anpassung Ihrer Konfiguration, um die entsprechenden Probleme zu lösen.

Es können zwei Arten von Warnhinweisen auftreten:

* **Warnhinweise** geben Hinweise auf Empfehlungen und zeigen Best Practices, wie etwa:

   * **[!UICONTROL Der Ausschluss-Link ist nicht im E-Mail-Text vorhanden]**: Es empfiehlt sich, einen Link zur Abmeldung in Ihren E-Mail-Textkörper einzufügen. In [diesem Abschnitt](../privacy/opt-out.md#opt-out-decision-management) erfahren Sie, wie Sie diesen konfigurieren.

     >[!NOTE]
     >
     >E-Mail-Nachrichten vom Typ Marketing müssen einen Ausschluss-Link enthalten, der für Transaktionsnachrichten nicht erforderlich ist. Die Nachrichtenkategorie (**[!UICONTROL Marketing]** oder **[!UICONTROL Transaktion]**) wird auf der Ebene der [Kanalkonfiguration](email-settings.md#email-type) und beim [Erstellen der Nachricht](#create-email-journey-campaign) über eine Journey oder Kampagne definiert.

   * **[!UICONTROL Textversion von HTML ist leer]**: Vergessen Sie nicht, eine Textversion Ihres E-Mail-Textkörpers zu definieren, da diese verwendet wird, wenn HTML-Inhalte nicht angezeigt werden können. In [diesem Abschnitt](text-version-email.md) erfahren Sie, wie Sie die Textversion erstellen.

   * **[!UICONTROL Leerer Link ist im E-Mail-Text vorhanden]**: Überprüfen Sie, ob alle Links in Ihrer E-Mail korrekt sind. In [diesem Abschnitt](content-from-scratch.md) erfahren Sie, wie Sie Inhalte und Links verwalten.

   * **[!UICONTROL Die E-Mail-Größe überschreitet den Grenzwert von 100 KB]**: Stellen Sie sicher, dass die Größe Ihrer E-Mail 100 KB nicht überschreitet, um einen optimalen Versand zu erzielen. In [diesem Abschnitt](content-from-scratch.md) erfahren Sie, wie Sie E-Mail-Inhalte bearbeiten.

* **Fehler** verhindern, dass Sie die Journey bzw. Kampagne testen oder aktivieren, solange nicht alle Fehler behoben sind. Beispiele sind:

   * **[!UICONTROL Die Betreffzeile fehlt]**: Die E-Mail-Betreffzeile ist obligatorisch. In [diesem Abschnitt](create-email.md) erfahren Sie, wie Sie sie definieren und personalisieren.

  <!--HTML is empty when Amp HTML is present-->

   * **[!UICONTROL Die E-Mail-Version der Nachricht ist leer]**: Dieser Fehler wird angezeigt, wenn der E-Mail-Inhalt nicht konfiguriert wurde. In [diesem Abschnitt](get-started-email-design.md) erfahren Sie, wie Sie E-Mail-Inhalte entwerfen.

   * **[!UICONTROL Konfiguration ist nicht vorhanden]**: Sie können Ihre Nachricht nicht veröffentlichen, wenn die gewählte Konfiguration nach der Erstellung der Nachricht gelöscht wurde. Wenn dieser Fehler auftritt, wählen Sie in den **[!UICONTROL Eigenschaften]** der Nachricht eine andere Konfiguration aus. Weitere Informationen zu Kanalkonfigurationen finden Sie in [diesem Abschnitt](../configuration/channel-surfaces.md).

>[!CAUTION]
>
>Um die Journey bzw. Kampagne mithilfe der E-Mail testen oder aktivieren zu können, müssen Sie zunächst alle **Fehler-Warnungen** beheben.

## Überprüfen und Senden der E-Mail

Sobald der Nachrichteninhalt definiert wurde, können Sie den Inhalt mit einer der beiden Simulationsmethoden in der Vorschau anzeigen:

* Klicken Sie **[!UICONTROL Inhalt simulieren]**, um Inhaltsvarianten mit Beispieleingabedaten oder automatischer KI-Generierung zu testen. [Informationen zum Simulieren von Inhaltsvarianten](../test-approve/simulate-sample-input.md)
* Klicken Sie auf **[!UICONTROL Inhalt simulieren]** und wählen Sie dann **[!UICONTROL Inhalt simulieren (AEP-Profile)]** aus dem Dropdown-Menü aus, um eine Vorschau mit Testprofilen anzuzeigen, Testsendungen zu senden und das E-Mail-Rendering zu überprüfen.

Sie können auch die Qualität Ihrer Inhalte überprüfen, um Lesbarkeit, Effektivität und Inhaltskohärenz zu bewerten. [Weitere Informationen zur Validierung der Inhaltsqualität](../content-management/brands-score.md#validate-quality)

![](assets/email_designer_edit_simulate.png)

Detaillierte Informationen zur Auswahl von Testprofilen und zur Vorschau Ihres Inhalts finden Sie im Abschnitt [Content-Management](../content-management/preview-test.md).

Wenn Ihre E-Mail bereit ist, schließen Sie die Konfiguration Ihrer [Journey](../building-journeys/journey-gs.md) oder [Kampagne](../campaigns/create-campaign.md) ab und aktivieren Sie diese, um die Nachricht zu senden.

>[!NOTE]
>
>Um das Verhalten Ihrer Empfänger und Empfängerinnen durch E-Mail-Öffnungen und/oder Interaktionen nachzuverfolgen, stellen Sie sicher, dass die entsprechenden Optionen im Abschnitt **[!UICONTROL Tracking]** in der [E-Mail-Aktivität](../building-journeys/journey-action.md) der Journey oder in der E-Mail-[Kampagne](../campaigns/create-campaign.md) aktiviert sind.<!--to move?-->

<!--
## Define your email content {#email-content}

Use [!DNL Journey Optimizer] Email Designer to [design your email from scratch](../email/content-from-scratch.md). If you have an existing content, you can [import it in the Email Designer](../email/existing-content.md), or [code your own content](../email/code-content.md) in [!DNL Journey Optimizer]. 

[!DNL Journey Optimizer] comes with a set of [built-in templates](email-templates.md) to help you start. Any email can also be saved as a template.

Use [!DNL Journey Optimizer] personalization editor to personalize your messages with profiles' data. For more on personalization, refer to [this section](../personalization/personalize.md).

Adapt the content of your messages to the targeted profiles by using [!DNL Journey Optimizer] dynamic content capabilities. [Get started with dynamic content](../personalization/get-started-dynamic-content.md)

## Email tracking {#email-tracking}

If you want to track the behavior of your recipients through openings and/or clicks on links, enable the following options: **[!UICONTROL Email opens]** and **[!UICONTROL Click on email]**. 

Learn more about tracking in [this section](message-tracking.md).

## Validate your email content {#email-content-validate}

Control the rendering of your email, and check personalization settings with test profiles, using the preview section on the left-hand side. For more on this, refer to [this section](preview.md).

![](assets/messages-simple-preview.png)

You must also check alerts in the upper section of the editor.  Some of them are simple warnings, but others can prevent you from using the message. 
-->

