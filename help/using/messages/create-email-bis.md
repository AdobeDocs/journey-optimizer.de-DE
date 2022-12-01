---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen einer E-Mail
description: Erfahren Sie, wie Sie in Journey Optimizer eine E-Mail erstellen.
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: b7b333e96e0f4b32a0f94c3f1e67f0f3d3fc2816
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 22%

---

# Erstellen einer E-Mail {#create-email-bis}

Gehen Sie wie folgt vor, um eine E-Mail zu erstellen.

## 1. Erstellen einer E-Mail in einer Journey oder Kampagne

Hinzufügen einer **[!UICONTROL Email]** Aktionen auf eine Journey oder Kampagne anwenden und entsprechend Ihrem Fall die folgenden Schritte ausführen.

>[!BEGINTABS]

>[!TAB E-Mail zu einer Journey hinzufügen]

1. Öffnen Sie Ihre Journey und ziehen Sie eine **[!UICONTROL Email]** -Aktivität aus **[!UICONTROL Aktionen]** in der Palette.

1. Geben Sie grundlegende Informationen zu Ihrer Nachricht an (Titel, Beschreibung, Kategorie).

1. Wählen Sie die [E-Mail-Oberfläche] verwendet werden.

   ![](assets/email_journey.png)

Weitere Informationen zum Konfigurieren einer Journey finden Sie unter [diese Seite](../building-journeys/journey-gs.md).

>[!TAB Hinzufügen einer E-Mail zu einer Kampagne]

1. Erstellen Sie eine neue geplante oder API-gesteuerte Kampagne und wählen Sie **[!UICONTROL Email]** als Aktion.

1. Wählen Sie die [E-Mail-Oberfläche] verwendet werden.

   ![](assets/email_campaign.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

1. Führen Sie die Schritte zum Erstellen einer E-Mail-Kampagne aus.

   ![](assets/email_campaign_steps.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->

Weitere Informationen zur Konfiguration einer Kampagne finden Sie unter [diese Seite](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## Definieren des E-Mail-Inhalts

1. Klicken Sie auf dem Journey- oder Kampagnenkonfigurationsbildschirm auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** zum Konfigurieren des E-Mail-Inhalts. [Weitere Informationen]

   ![](assets/email_campaign_edit_content.png)

1. Im **[!UICONTROL Kopfzeile]** Abschnitt **[!UICONTROL Inhalt bearbeiten]** -Bildschirm, die **[!UICONTROL Name des Empfängers]**, **[!UICONTROL Aus E-Mail]** und **[!UICONTROL BCC]** -Feld von der von Ihnen ausgewählten E-Mail-Oberfläche stammen. [Weitere Informationen] <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. Sie können eine Betreffzeile hinzufügen. Geben Sie Text direkt in das entsprechende Feld ein oder verwenden Sie die [Ausdruckseditor](../personalization/personalization-build-expressions.md) um die Betreffzeile zu personalisieren.

1. Klicken Sie auf **[!UICONTROL Bearbeiten des E-Mail-Hauptteils]** Schaltfläche zum Erstellen Ihres Inhalts mithilfe der [!DNL Journey Optimizer] Email Designer. [Weitere Informationen]

   ![](assets/email_designer_edit_email_body.png)

   Sie können auch auf die **[!UICONTROL Code-Editor]** -Schaltfläche, um Ihren eigenen Inhalt im einfachen HTML zu kodieren, indem Sie das angezeigte Popup-Fenster verwenden.

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >Wenn Sie Inhalte bereits über Email Designer erstellt oder importiert haben, wird dieser Inhalt auf HTML angezeigt.

## Sehen Sie sich die E-Mail in der Vorschau an

Nachdem der Nachrichteninhalt definiert wurde, können Sie eine Vorschau davon anzeigen, um das Rendering Ihrer E-Mail zu steuern, und die Personalisierungseinstellungen mit Testprofilen überprüfen. [Weitere Informationen]

![](assets/email_designer_edit_simulate.png)

Sie müssen auch Warnhinweise im oberen Bereich des Editors überprüfen.  Einige davon sind einfache Warnhinweise, andere können die Verwendung der Nachricht verhindern. [Weitere Informationen](alerts.md).

## Validieren des E-Mail-Inhalts

Wenn Ihre E-Mail fertig ist, konfigurieren Sie Ihre [Journey](../building-journeys/journey-gs.md) oder [Kampagne](../campaigns/create-campaign.md) und aktivieren, um die Nachricht zu senden.

>[!NOTE]
>
>Um das Verhalten Ihrer Empfänger über E-Mail-Öffnungen und/oder Interaktionen zu verfolgen, stellen Sie sicher, dass die entsprechenden Optionen in der **[!UICONTROL Tracking]** -Abschnitt im Journey aktiviert werden. [E-Mail-Aktivität](../building-journeys/journeys-message.md) oder in der E-Mail [Kampagne](../campaigns/create-campaign.md).

Sie müssen auch Warnhinweise im oberen Bereich des Editors überprüfen.  Einige davon sind einfache Warnhinweise, andere können die Verwendung der Nachricht verhindern. [Weitere Informationen](alerts.md)

