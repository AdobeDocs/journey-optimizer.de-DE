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
TQID: https://experienceleague.adobe.com/CC56E9rV4TImjLBbm-fsq2a4JKLnEA4wJB2DVLgOAfM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: a5683ded-e5d5-4ec6-b9fd-e1b56a94ab96id: d595a60b-bcf5-4a63-a189-66a0be755cc7id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: a4e4f5ca5c3eb9dbfb5691cb5de420009ed7e5a5
workflow-type: tm+mt
source-wordcount: 218
ht-degree: 95%

---

# Testen von E-Mail-Inhaltsvorlagen {#test-template}

Sie können das Rendering einiger Ihrer E-Mail-Vorlagen testen, unabhängig davon, ob diese von Grund auf neu oder aus vorhandenen Inhalten erstellt wurde. Gehen Sie dazu wie folgt vor.

1. Rufen Sie die Inhaltsvorlagenliste über das Menü **[!UICONTROL Content-Management]** > **[!UICONTROL Inhaltsvorlagen]** auf und wählen Sie eine beliebige E-Mail-Vorlage aus.

1. Klicken Sie in den **[!UICONTROL Vorlageneigenschaften]** auf **[!UICONTROL Inhalt bearbeiten]**.

1. Klicken Sie auf **[!UICONTROL Inhalt simulieren]**, um eine Vorschau anzuzeigen und Ihren Inhalt zu testen. [Erfahren Sie, wie Sie Inhalte in der Vorschau anzeigen und testen können](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

1. Sie können einen Testversand durchführen, um Ihren Inhalt zu testen und ihn von einigen internen Benutzern genehmigen zu lassen, bevor Sie ihn in einer Journey oder Kampagne verwenden.

   * Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Testversand durchführen]** und folgen Sie den Schritten, die in [diesem Abschnitt](../content-management/proofs.md) beschrieben werden.

   * Vor dem Testversand müssen Sie die [E-Mail-Konfiguration](../configuration/channel-surfaces.md) auswählen, die zum Testen Ihres Inhalts verwendet wird.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Derzeit wird Tracking beim Testen von E-Mail-Inhaltsvorlagen nicht unterstützt, d. h. die Nachverfolgung von Ereignissen, UTM-Parametern und Landingpage-Links ist in den Testsendungen, die von einer Vorlage gesendet werden, nicht wirksam. [Verwenden Sie zum Testen des Trackings die Inhaltsvorlage](../email/use-email-templates.md) in einer E-Mail und führen Sie einen Testversand mit Testprofilen oder Beispieleingabedaten durch, die aus einer CSV- oder JSON-Datei hochgeladen oder manuell hinzugefügt wurden. [Erfahren Sie, wie Sie eine Vorschau der Inhalte anzeigen und die Inhalte testen](../content-management/preview-test.md)
