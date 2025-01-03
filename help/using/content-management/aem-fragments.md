---
solution: Journey Optimizer
product: journey optimizer
title: AEM-Inhaltsfragmente
description: Erfahren Sie, wie Sie auf AEM-Inhaltsfragmente zugreifen und diese verwalten
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: 3d0576983854b5cc33d8dc956c601b638164a813
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 100%

---

# Inhaltsfragmente in Adobe Experience Manager {#aem-fragments}

Durch die Integration von Adobe Experience Manager mit Adobe Journey Optimizer können Sie jetzt Ihre AEM-Inhaltsfragmente nahtlos in Journey Optimizer in Ihre E-Mail-Inhalte integrieren. Diese optimierte Verbindung vereinfacht den Zugriff auf und die Nutzung von AEM-Inhalten und ermöglicht die Erstellung personalisierter und dynamischer Kampagnen und Journeys.

Weitere Informationen zu AEM-Inhaltsfragmenten finden Sie in der [Dokumentation zu Experience Manager](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/authoring/fragments/content-fragments).

## Einschränkungen {#limitations}

* Nur für den E-Mail-Kanal verfügbar.

* Benutzende können derzeit nicht die AEM-Instanz wechseln, mit der sie verbunden sind, da jede Sandbox auf eine einzige Instanz beschränkt ist.

* Es wird empfohlen, die Anzahl der Benutzenden mit Zugriff auf die Veröffentlichung von Inhaltsfragmenten zu begrenzen, um das Risiko versehentlicher Fehler in E-Mails zu reduzieren.

* Bei mehrsprachigen Inhalten wird nur der manuelle Fluss unterstützt.

* Varianten werden derzeit nicht unterstützt.

* Sie müssen ein Tag speziell für Journey Optimizer erstellen.

+++ Erfahren Sie, wie Sie ein Journey Optimizer-Tag erstellen

   1. Greifen Sie auf Ihre **Experience Manager**-Umgebung zu.

   1. Gehen Sie vom Menü **Tools** zur Registerkarte **Allgemein** und wählen Sie **Tagging**.

   1. Klicken Sie auf **Neues Tag erstellen**.

   1. Stellen Sie sicher, dass die ID der folgenden Syntax entspricht: `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`.

   1. Klicken Sie auf **Erstellen**.

  Jetzt können Sie dieses Journey Optimizer-Tag Ihren Inhaltsfragmenten zuweisen.
+++

## Hinzufügen von AEM-Inhaltsfragmenten {#aem-add}

Nachdem Sie Ihre [AEM-Inhaltsfragmente](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/authoring/fragments/content-fragments) erstellt und personalisiert haben, können Sie sie in Ihre Journey Optimizer-Kampagne oder -Journey importieren.

1. Nachdem Sie Ihre [Kampagne](../email/create-email.md) oder [Journey](../email/create-email.md) mit einer E-Mail-Aktion erstellt haben, greifen Sie auf den E-Mail-Designer zu, um den E-Mail-Inhalt zu konfigurieren. [Weitere Informationen](../email/get-started-email-design.md)

1. Klicken Sie in einen Textblock oder in die Betreffzeile und wählen Sie **[!UICONTROL Personalisierung hinzufügen]** in der kontextbezogenen Symbolleiste aus.

   ![](assets/aem_campaign_2.png)

1. Klicken Sie im Menü **[!UICONTROL AEM-Inhaltsfragment]** im linken Bereich auf **[!UICONTROL AEM-Inhaltsfragmentauswahl öffnen]**.

   ![](assets/aem_campaign_3.png)

1. Wählen Sie ein **[!UICONTROL Inhaltsfragment]** aus der verfügbaren Liste aus, das in Ihren Journey Optimizer-Inhalt importiert werden soll.

   >[!IMPORTANT]
   >
   >Es können nur veröffentlichte **[!UICONTROL Inhaltsfragmente]** verwendet werden.

1. Klicken Sie auf **[!UICONTROL Filter anzeigen]**, um Ihre Inhaltsfragmentliste zu optimieren.

   Die Inhaltsfragmentauswahl enthält vorkonfigurierte Filter:

   * **[!UICONTROL Status]**: Veröffentlicht, Geändert
   * **[!UICONTROL Tag]**: wird automatisch basierend auf Ihrer Journey Optimizer-Umgebung definiert (Organisations-ID und Sandbox)

   ![](assets/aem_campaign_4.png)

1. Nachdem Sie Ihr **[!UICONTROL Inhaltsfragment]** ausgewählt haben, klicken Sie auf **[!UICONTROL Auswählen]**, um es zu öffnen.

   ![](assets/aem_campaign_5.png)

1. Wählen Sie die gewünschten Felder aus Ihrem **[!UICONTROL Inhaltsfragment]** aus, um sie zu Ihrem Inhalt hinzuzufügen.

   ![](assets/aem_campaign_6.png)

1. Klicken Sie auf **[!UICONTROL Speichern]** und überprüfen Sie Ihre Nachricht in der Vorschau. Sie können nun den Inhalt Ihrer Nachricht testen und überprüfen, wie in [diesem Abschnitt](preview.md) beschrieben.

Sobald Sie Ihre Tests durchgeführt und den Inhalt validiert haben, können Sie Ihre E-Mail mit Ihrer [Kampagne](../campaigns/review-activate-campaign.md) oder [Journey](../building-journeys/publishing-the-journey.md) an Ihre Zielgruppe senden.
