---
solution: Journey Optimizer
product: journey optimizer
title: E-Mail erstellen
description: Erfahren Sie, wie Sie in Journey Optimizer eine E-Mail erstellen
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# E-Mail erstellen {#create-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="Email-Erstellung"
>abstract="Definieren Sie Ihre E-Mail-Parameter in drei einfachen Schritten."

So erstellen Sie eine E-Mail in [!DNL Journey Optimizer]führen Sie die folgenden Schritte aus.

## E-Mail in einer Journey oder Kampagne erstellen {#create-email-journey-campaign}

Hinzufügen einer **[!UICONTROL Email]** Aktionen auf eine Journey oder eine Kampagne anwenden und entsprechend Ihrem Fall die folgenden Schritte ausführen.

>[!BEGINTABS]

>[!TAB Hinzufügen einer E-Mail zu einer Journey]

1. Öffnen Sie Ihre Journey und ziehen Sie eine **[!UICONTROL Email]** -Aktivität aus **[!UICONTROL Actions]** in der Palette.

1. Geben Sie grundlegende Informationen zu Ihrer Nachricht an (Titel, Beschreibung, Kategorie).

1. Wählen Sie die [E-Mail-Oberfläche](email-settings.md) verwendet werden.

   ![](assets/email_journey.png)

>[!NOTE]
>
>Wenn Sie eine E-Mail aus einer Journey senden, können Sie die Sendezeitoptimierungsfunktion von Adobe Journey Optimizer nutzen, um die beste Sendezeit für die Nachricht vorherzusagen und so die Interaktion basierend auf historischen Öffnungs- und Klickraten zu maximieren. [Erfahren Sie, wie Sie mit der Sendezeitoptimierung arbeiten.](../building-journeys/journeys-message.md#send-time-optimization)

Weitere Informationen zum Konfigurieren einer Journey finden Sie unter [diese Seite](../building-journeys/journey-gs.md).

>[!TAB Hinzufügen einer E-Mail zu einer Kampagne]

1. Erstellen Sie eine neue geplante oder API-gesteuerte Kampagne und wählen Sie **[!UICONTROL Email]** als Aktion.

1. Wählen Sie die [E-Mail-Oberfläche](email-settings.md) verwendet werden.

   ![](assets/email_campaign.png)

1. Klicken **[!UICONTROL Create]**.

1. Führen Sie die Schritte zur Erstellung einer E-Mail-Kampagne aus, z. B. die Kampagneneigenschaften, [audience](../segment/about-segments.md)und [Zeitplan](../campaigns/create-campaign.md#schedule).

   ![](assets/email_campaign_steps.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->

Weitere Informationen zur Konfiguration einer Kampagne finden Sie unter [diese Seite](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## E-Mail-Inhalt definieren {#define-email-content}

1. Klicken Sie im Konfigurationsbildschirm der Journey oder Kampagne auf das **[!UICONTROL Edit content]** zum Konfigurieren des E-Mail-Inhalts. [Weitere Infos](get-started-email-design.md)

   ![](assets/email_campaign_edit_content.png)

1. Im **[!UICONTROL Header]** Abschnitt **[!UICONTROL Edit content]** -Bildschirm, die **[!UICONTROL From name]**, **[!UICONTROL From email]** und **[!UICONTROL BCC]** -Feld von der von Ihnen ausgewählten E-Mail-Oberfläche stammen. [Weitere Infos](email-settings.md) <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. Sie können eine Betreffzeile hinzufügen. Geben Sie Text direkt in das entsprechende Feld ein oder verwenden Sie die [Ausdruckseditor](../personalization/personalization-build-expressions.md) um die Betreffzeile zu personalisieren.

1. Klicken Sie auf **[!UICONTROL Edit email body]** Schaltfläche zum Erstellen Ihres Inhalts mithilfe der [!DNL Journey Optimizer] Email Designer. [Weitere Infos](get-started-email-design.md)

   ![](assets/email_designer_edit_email_body.png)

1. Wenn Sie sich in einer Kampagne befinden, können Sie auch auf die **[!UICONTROL Code Editor]** -Schaltfläche, um Ihren eigenen Inhalt in einfachem HTML mit dem angezeigten Popup-Fenster zu kodieren.

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >Wenn Sie Inhalte bereits mit Email Designer erstellt oder importiert haben, wird dieser Inhalt im HTML-Format angezeigt.

## Warnungen überprüfen {#check-email-alerts}

Während Sie Ihre Nachrichten entwerfen, werden Warnhinweise in der Benutzeroberfläche (oben rechts auf dem Bildschirm) angezeigt, wenn wichtige Einstellungen fehlen.

![](assets/email_journey_alerts_details.png)

>[!NOTE]
>
>Wenn diese Schaltfläche nicht angezeigt wird, wurde kein Warnhinweis erkannt.

Die vom System geprüften Einstellungen und Elemente sind unten aufgeführt. Sie finden außerdem Informationen zur Anpassung Ihrer Konfiguration, um die entsprechenden Probleme zu beheben.

Es können zwei Arten von Warnhinweisen auftreten:

* **Warnungen** Empfehlungen und Best Practices, z. B.:

   * **[!UICONTROL The opt-out link is not present in the email body]**: Es empfiehlt sich, einen Abmelde-Link in Ihren E-Mail-Textkörper einzufügen. Erfahren Sie, wie Sie es konfigurieren in [diesem Abschnitt](../privacy/opt-out.md#opt-out-management).

      >[!NOTE]
      >
      >E-Mail-Nachrichten vom Typ Marketing müssen einen Ausschluss-Link enthalten, der für Transaktionsnachrichten nicht erforderlich ist. Die Kategorie der Nachricht (**[!UICONTROL Marketing]** oder **[!UICONTROL Transactional]**) definiert wird unter [Kanaloberfläche](email-settings.md#email-type) Ebene und Zeitpunkt [Nachricht erstellen](#create-email-journey-campaign) aus einer Journey oder einer Kampagne.

   * **[!UICONTROL Text version of HTML is empty]**: Vergessen Sie nicht, eine Textversion Ihres E-Mail-Textkörpers zu definieren, da diese verwendet wird, wenn kein HTML-Inhalt angezeigt werden kann. Erfahren Sie, wie Sie die Textversion in [diesem Abschnitt](text-version-email.md).

   * **[!UICONTROL Empty link is present in email body]**: Überprüfen Sie, ob alle Links in Ihrer E-Mail korrekt sind. Erfahren Sie, wie Sie Inhalte und Links in [diesem Abschnitt](content-from-scratch.md).

   * **[!UICONTROL Email size has exceeded the limit of 100KB]**: Um einen optimalen Versand zu gewährleisten, sollten Sie sicherstellen, dass die Größe Ihrer E-Mail 100 KB nicht überschreitet. Erfahren Sie, wie Sie E-Mail-Inhalte in bearbeiten [diesem Abschnitt](content-from-scratch.md).

* **Fehler** verhindern, dass Sie die Journey/Kampagne testen oder aktivieren, solange sie nicht aufgelöst sind, z. B.:

   * **[!UICONTROL The subject line is missing]**: E-Mail-Betreffzeile ist obligatorisch. Erfahren Sie, wie Sie sie definieren und personalisieren in [diesem Abschnitt](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

   * **[!UICONTROL The email version of the message is empty]**: wird dieser Fehler angezeigt, wenn der E-Mail-Inhalt nicht konfiguriert wurde. Erfahren Sie, wie Sie E-Mail-Inhalte erstellen in [diesem Abschnitt](get-started-email-design.md).

   * **[!UICONTROL Surface doesn't exist]**: Sie können Ihre Nachricht nicht verwenden, wenn die ausgewählte Oberfläche nach der Nachrichtenerstellung gelöscht wird. Wenn dieser Fehler auftritt, wählen Sie eine andere Stelle in der Nachricht aus **[!UICONTROL Properties]**. Weitere Informationen zu Kanaloberflächen in [diesem Abschnitt](../configuration/channel-surfaces.md).


>[!CAUTION]
>
>Um die Journey/Kampagne mithilfe der E-Mail testen oder aktivieren zu können, müssen Sie alle **error** Warnhinweise.

## Vorschau erstellen und E-Mail senden

Nachdem der Nachrichteninhalt definiert wurde, können Sie eine Vorschau davon anzeigen, um das Rendering Ihrer E-Mail zu steuern, und die Personalisierungseinstellungen mit Testprofilen überprüfen. [Weitere Infos](preview.md)

![](assets/email_designer_edit_simulate.png)

Wenn Ihre E-Mail fertig ist, konfigurieren Sie Ihre [Journey](../building-journeys/journey-gs.md) oder [Kampagne](../campaigns/create-campaign.md)und aktivieren Sie sie, um die Nachricht zu senden.

>[!NOTE]
>
>Um das Verhalten Ihrer Empfänger über E-Mail-Öffnungen und/oder Interaktionen zu verfolgen, stellen Sie sicher, dass die entsprechenden Optionen in der **[!UICONTROL Tracking]** -Abschnitt in der Journey aktiviert werden. [E-Mail-Aktivität](../building-journeys/journeys-message.md) oder in der E-Mail [Kampagne](../campaigns/create-campaign.md).<!--to move?-->

<!--

## Define your email content {#email-content}

Use [!DNL Journey Optimizer] Email Designer to [design your email from scratch](../email/content-from-scratch.md). If you have an existing content, you can [import it in the Email Designer](../email/existing-content.md), or [code your own content](../email/code-content.md) in [!DNL Journey Optimizer]. 

[!DNL Journey Optimizer] comes with a set of [built-in templates](email-templates.md) to help you start. Any email can also be saved as a template.

Use [!DNL Journey Optimizer] Expression editor to personalize your messages with profiles' data. For more on personalization, refer to [this section](../personalization/personalize.md).

Adapt the content of your messages to the targeted profiles by using [!DNL Journey Optimizer] dynamic content capabilities. [Get started with dynamic content](../personalization/get-started-dynamic-content.md)

## Email tracking {#email-tracking}

If you want to track the behavior of your recipients through openings and/or clicks on links, enable the following options: **[!UICONTROL Email opens]** and **[!UICONTROL Click on email]**. 

Learn more about tracking in [this section](message-tracking.md).

## Validate your email content {#email-content-validate}

Control the rendering of your email, and check personalization settings with test profiles, using the preview section on the left-hand side. For more on this, refer to [this section](preview.md).

![](assets/messages-simple-preview.png)

You must also check alerts in the upper section of the editor.  Some of them are simple warnings, but others can prevent you from using the message. 

-->

