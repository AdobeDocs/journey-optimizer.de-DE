---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen von Inhaltsvorlagen
description: Erfahren Sie, wie Sie Vorlagen erstellen, um Inhalte in Journey Optimizer-Kampagnen und -Journeys wiederzuverwenden
feature: Templates
topic: Content Management
role: User
level: Beginner
exl-id: 327de13a-1c99-4d5e-86cf-8180fb7aaf23
source-git-commit: 1cfe9f6cb6e7c3e9a5d9b808c10ae4dfe77a92a2
workflow-type: ht
source-wordcount: '1105'
ht-degree: 100%

---

# Arbeiten mit Inhaltsvorlagen {#content-templates}

Für einen beschleunigten und verbesserten Design-Prozess können Sie eigenständige Vorlagen erstellen, um benutzerdefinierte Inhalte in [!DNL Journey Optimizer]-Kampagnen und -Journeys einfach wiederzuverwenden.

Diese Funktion ermöglicht inhaltsorientierten Benutzenden die Arbeit an Vorlagen außerhalb von Kampagnen oder Journeys. Personen, die Marketing betreiben, können diese eigenständigen Inhaltsvorlagen dann in ihren eigenen Journeys oder Kampagnen wiederverwenden und anpassen.

![](../rn/assets/do-not-localize/content-template.gif)


>[!NOTE]
>
>Derzeit werden nur die **E-Mail**-Inhaltsvorlagen unterstützt.

Zum Beispiel: Eine Person in Ihrem Unternehmen ist nur für Inhalte zuständig und hat daher keinen Zugriff auf Kampagnen oder Journeys. Diese Person kann jedoch eine E-Mail-Vorlage erstellen, die die Marketing-Fachleute Ihrer Organisation für die Verwendung in allen E-Mails als Ausgangspunkt auswählen können.

Sie können Inhaltsvorlagen auch mithilfe von APIs erstellen und verwalten. Weiterführende Informationen finden Sie in der [Dokumentation zu Journey Optimizer-APIs](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}.

➡️ [Erfahren Sie in diesem Video, wie Sie Vorlagen definieren und verwenden](#video-templates).

>[!CAUTION]
>
>Zum Erstellen, Bearbeiten und Löschen von Inhaltsvorlagen benötigen Sie die Berechtigung **[!DNL Manage library items]** im **[!DNL Content Library Manager]**-Produktprofil. [Weitere Informationen](../administration/ootb-product-profiles.md#content-library-manager)

## Zugreifen auf und Verwalten von Vorlagen {#access-manage-templates}

Um auf die Liste der Inhaltsvorlagen zuzugreifen, wählen Sie **[!UICONTROL Content-Management]** > **[!UICONTROL Inhaltsvorlagen]** aus dem linken Menü aus.

![](../email/assets/content-template-list.png)

Alle Vorlagen, die in der aktuellen Sandbox erstellt wurden – entweder aus einer Journey oder einer Kampagne, die die Option [Als Vorlage speichern](#save-as-template) verwendet, oder aus dem Menü **[!UICONTROL Inhaltsvorlagen]** – werden angezeigt.

Sie können Inhaltsvorlagen nach Erstellungs- oder Änderungsdatum sortieren. Sie können auch festlegen, dass nur die von Ihnen erstellten oder geänderten Elemente angezeigt werden.

![](../email/assets/content-template-list-filters.png)

Um einen Vorlageninhalt zu bearbeiten, klicken Sie in der Liste auf das gewünschte Element und wählen Sie **[!UICONTROL Inhalt bearbeiten]** aus.

![](../email/assets/content-template-edit.png)

Um eine Vorlage zu löschen, wählen Sie das Papierkorbsymbol neben der gewünschten Vorlage aus.

![](../email/assets/content-template-list-delete.png)

>[!NOTE]
>
>Wenn eine Vorlage bearbeitet oder gelöscht wird, sind Kampagnen oder Journeys, einschließlich mit dieser Vorlage erstellter E-Mails, nicht betroffen.

## Erstellen von Inhaltsvorlagen {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="Eigene Inhaltsvorlage definieren"
>abstract="Erstellen Sie eine komplett neue, benutzerdefinierte Vorlage, damit Sie Ihre Inhalte für mehrere Journeys und Kampagnen wiederverwenden können."

Es gibt zwei Möglichkeiten, Inhaltsvorlagen zu erstellen:

* Erstellen Sie eine neue Inhaltsvorlage mithilfe des Menüs **[!UICONTROL Inhaltsvorlagen]** in der linken Leiste. [Weitere Informationen](#create-template-from-scratch)

* Speichern Sie beim Entwerfen einer E-Mail innerhalb einer Kampagne oder Journey Ihren E-Mail-Inhalt als Vorlage. [Weitere Informationen](#save-as-template)

Nach der Speicherung ist Ihre Inhaltsvorlage für Kampagnen oder Journeys verfügbar. Unabhängig davon, ob sie von Grund auf neu oder von einer vorherigen E-Mail erstellt wurden, können Sie diese Vorlage jetzt beim Erstellen von [E-Mails](../email/get-started-email-design.md) in [!DNL Journey Optimizer] verwenden. [Weitere Informationen](../email/use-email-templates.md)

>[!NOTE]
>
>* Änderungen an Inhaltsvorlagen werden nicht an Kampagnen oder Journeys weitergegeben, unabhängig davon, ob sie live oder als Entwurf vorliegen.
>
>* Wenn Vorlagen in einer Kampagne oder einer Journey verwendet werden, wirken sich Änderungen am Kampagnen- und Journey-Inhalt ebenso nicht auf die zuvor verwendete Inhaltsvorlage aus.

### Erstellen einer Vorlage von Grund auf {#create-template-from-scratch}

Gehen Sie wie folgt vor, um eine Inhaltsvorlage von Grund auf zu erstellen.

1. Greifen Sie über das linke Menü **[!UICONTROL Content-Management]** > **[!UICONTROL Inhaltsvorlagen]** auf die Inhaltsvorlagenliste zu.

1. Wählen Sie **[!UICONTROL Vorlage erstellen]** aus.

1. Füllen Sie die Vorlagendetails aus.

   ![](../email/assets/content-template-details.png)

   >[!NOTE]
   >
   >Derzeit werden nur der Kanal **E-Mail** und der Typ **HTML** unterstützt.

1. Um der Vorlage benutzerdefinierte oder grundlegende Datennutzungskennzeichnungen zuzuweisen, wählen Sie **[!UICONTROL Zugriff verwalten]** aus. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md).

1. Wählen oder erstellen Sie Adobe Experience Platform-Tags im Feld **[!UICONTROL Tags]**, um Ihre Vorlage für eine verbesserte Suche zu kategorisieren. [Weitere Informationen](../start/search-filter-categorize.md#tags)

1. Klicken Sie auf **[!UICONTROL Erstellen]** und wählen Sie aus den verschiedenen Optionen aus, wie Sie Ihre Vorlage gestalten möchten:

   * [Erstellen Sie Ihre E-Mail von Grund auf](../email/content-from-scratch.md) über die Benutzeroberfläche von E-Mail-Designer.

   * [Codieren Sie oder fügen Sie rohen HTML-Code](../email/code-content.md) direkt in den E-Mail-Designer ein.

   * [Importieren Sie vorhandene HTML-Inhalte](../email/existing-content.md) aus einer Datei oder einem ZIP-Ordner.

   * Wählen Sie aus einer Liste integrierter oder benutzerdefinierter Vorlagen einen existierenden Inhalt aus. Die Schritte zur Verwendung einer Inhaltsvorlage in einer E-Mail werden in [diesem Abschnitt](../email/use-email-templates.md) beschrieben.

   ![](../email/assets/content-template-design.png)

1. Der [E-Mail-Designer](../email/get-started-email-design.md) wird angezeigt. Bearbeiten Sie den Inhalt nach Bedarf auf die gleiche Weise wie für jede E-Mail innerhalb einer Journey oder Kampagne, je nach ausgewählter Option.

   Bei Bedarf können Sie Ihren Inhalt testen. [Weitere Informationen](#test-template)

1. Sobald Ihre Vorlage fertig ist, klicken Sie auf **[!UICONTROL Speichern]**.

1. Klicken Sie bei Bedarf auf den Pfeil neben dem Vorlagennamen, um zum Bildschirm **[!UICONTROL Details]** zurückzukehren und die Vorlage zu bearbeiten.

   ![](../email/assets/content-template-designer-back.png)

Diese Vorlage kann jetzt beim Erstellen von E-Mails in [!DNL Journey Optimizer] verwendet werden. [Weitere Informationen](../email/use-email-templates.md)

### Als Vorlage speichern {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Hier erfahren Sie, wie Sie Ihre Nachrichten migrieren können"
>abstract="Seit dem 25. Juli 2022 wird das Nachrichtenmenü nicht mehr angezeigt. Nachrichten werden nun direkt von einer Journey aus verfasst. Wenn Sie Ihre alten Nachrichten in Journeys wiederverwenden möchten, müssen Sie sie als Vorlagen speichern."

Beim Entwerfen einer [E-Mail](../email/get-started-email-design.md) in einer Kampagne oder einer Journey können Sie Ihren E-Mail-Inhalt für die spätere Wiederverwendung speichern. Gehen Sie dazu wie folgt vor.

1. Klicken Sie im E-Mail-Designer oben rechts im Bildschirm auf die Auslassungspunkte.

1. Wählen Sie im Dropdown-Menü **[!UICONTROL Als Inhaltsvorlage speichern]** aus.

   ![](../email/assets/email_designer-save-template.png)

1. Fügen Sie dieser Vorlage einen Namen hinzu.

   ![](../email/assets/email_designer-template-name.png)

1. Um der Vorlage benutzerdefinierte oder grundlegende Datennutzungskennzeichnungen zuzuweisen, wählen Sie **[!UICONTROL Zugriff verwalten]** aus. [Weitere Informationen](../administration/object-based-access.md).

1. Wählen oder erstellen Sie ein Adobe Experience Platform-Tag im Feld **Tags**, um Ihre Vorlage zu kategorisieren. [Weitere Informationen](../start/search-filter-categorize.md#tags)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

1. Die Vorlage wird auf der Liste der **[!UICONTROL Inhaltsvorlagen]** gespeichert, auf die über das dedizierte [!DNL Journey Optimizer]-Menü zugegriffen werden kann. Sie wird zu einer eigenständigen Inhaltsvorlage, auf die wie jedes andere Element in der Liste zugegriffen werden kann und die bearbeitet und gelöscht werden kann. [Weitere Informationen](#access-manage-templates)

Sie können diese Vorlage jetzt beim Erstellen von [E-Mails](../email/get-started-email-design.md) in [!DNL Journey Optimizer] verwenden. [Weitere Informationen](../email/use-email-templates.md)

>[!NOTE]
>
>Änderungen an dieser neuen Vorlage wirken sich nicht auf die E-Mail aus, aus der die Vorlage hervorgegangen ist. Wenn der ursprüngliche Inhalt in dieser E-Mail bearbeitet wird, wird die neue Vorlage ebenfalls nicht geändert.

## Testen der Inhaltsvorlage {#test-template}

Sie können das Rendering einer beliebigen E-Mail-Inhaltsvorlage testen, unabhängig davon, ob sie von Grund auf neu oder aus einer E-Mail erstellt wurde. Gehen Sie dazu wie folgt vor.

1. Sie können über das Menü **[!UICONTROL Content-Management]** > **[!UICONTROL Inhaltsvorlagen]** auf die Inhaltsvorlagenliste zugreifen und eine beliebige Vorlage auswählen.

1. Klicken Sie in den **[!UICONTROL Vorlageneigenschaften]** auf **[!UICONTROL Inhalt bearbeiten]**.

1. Klicken Sie auf **[!UICONTROL Inhalt simulieren]** und wählen Sie ein Testprofil aus, um Ihr E-Mail-Rendering zu überprüfen. Sie können zwischen der Desktop- oder der Mobile-Ansicht wählen. [Weitere Informationen](../content-management/preview-test.md)

   ![](../email/assets/content-template-stimulate.png)

1. Sie können einen Testversand durchführen, um Ihren Inhalt zu testen und ihn von einigen internen Benutzern genehmigen zu lassen, bevor Sie ihn in einer Journey oder Kampagne verwenden.

   * Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Testversand durchführen]** und folgen Sie den Schritten, die in [diesem Abschnitt](../content-management/proofs.md) beschrieben werden.

   * Vor dem Testversand müssen Sie die [E-Mail-Oberfläche](../configuration/channel-surfaces.md) auswählen, die zum Testen Ihres Inhalts verwendet wird.

     ![](../email/assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Derzeit wird Tracking beim Testen von E-Mail-Inhaltsvorlagen nicht unterstützt, d. h. die Nachverfolgung von Ereignissen, UTM-Parametern und Landingpage-Links ist in den Testsendungen, die von einer Vorlage gesendet werden, nicht wirksam. Um Tracking zu testen, [verwenden Sie die Inhaltsvorlage](../email/use-email-templates.md) in einer E-Mail und [führen Sie einen Testversand durch](../content-management/preview-test.md#send-proofs).

## Anleitungsvideo {#video-templates}

Erfahren Sie, wie Sie Inhaltsvorlagen in [!DNL Journey Optimizer] erstellen, bearbeiten und verwenden.

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)
