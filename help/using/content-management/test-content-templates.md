---
solution: Journey Optimizer
product: journey optimizer
title: Testen von Inhaltsvorlagen
description: Erfahren Sie, wie Sie das Rendern einiger Ihrer E-Mail-Inhaltsvorlagen testen können.
feature: Templates
topic: Content Management
role: User
level: Beginner
exl-id: 01726ab6-f581-4d19-aedd-2541bc0f27c6
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: ht
source-wordcount: '193'
ht-degree: 100%

---

# Testen von E-Mail-Inhaltsvorlagen {#test-template}

Sie können das Rendering einiger Ihrer E-Mail-Vorlagen testen, unabhängig davon, ob diese von Grund auf neu oder aus vorhandenen Inhalten erstellt wurde. Gehen Sie dazu wie folgt vor.

1. Rufen Sie die Inhaltsvorlagenliste über das Menü **[!UICONTROL Content-Management]** > **[!UICONTROL Inhaltsvorlagen]** auf und wählen Sie eine beliebige E-Mail-Vorlage aus.

1. Klicken Sie in den **[!UICONTROL Vorlageneigenschaften]** auf **[!UICONTROL Inhalt bearbeiten]**.

1. Klicken Sie auf **[!UICONTROL Inhalt simulieren]** und wählen Sie ein Testprofil aus, um Ihr Rendering zu überprüfen. [Weitere Informationen](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

1. Sie können einen Testversand durchführen, um Ihren Inhalt zu testen und ihn von einigen internen Benutzern genehmigen zu lassen, bevor Sie ihn in einer Journey oder Kampagne verwenden.

   * Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Testversand durchführen]** und folgen Sie den Schritten, die in [diesem Abschnitt](../content-management/proofs.md) beschrieben werden.

   * Vor dem Testversand müssen Sie die [E-Mail-Konfiguration](../configuration/channel-surfaces.md) auswählen, die zum Testen Ihres Inhalts verwendet wird.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Derzeit wird Tracking beim Testen von E-Mail-Inhaltsvorlagen nicht unterstützt, d. h. die Nachverfolgung von Ereignissen, UTM-Parametern und Landingpage-Links ist in den Testsendungen, die von einer Vorlage gesendet werden, nicht wirksam. Um Tracking zu testen, [verwenden Sie die Inhaltsvorlage](../email/use-email-templates.md) in einer E-Mail und [führen Sie einen Testversand durch](../content-management/preview-test.md#send-proofs).
