---
solution: Journey Optimizer
product: journey optimizer
title: Verwalten von Fragmenten
description: Erfahren Sie, wie Sie Ihre Inhaltsfragmente verwalten
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 1fc708e1-a993-4a2a-809c-c5dc08a4bae1
source-git-commit: c32f1e86eb803a0a4b25111d07989872b33a3bed
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 68%

---

# Verwalten von Fragmenten {#manage-fragments}

Um Ihre Fragmente zu verwalten, greifen Sie links über das Menü **[!UICONTROL Content-Management]** > **[!UICONTROL Fragmente]** auf die Fragmentliste zu.

Es werden alle in der aktuellen Sandbox entweder [über das Menü **[!UICONTROL Fragmente]** oder](#create-fragments) die Option [Als Fragment speichern](#save-as-fragment) erstellten Fragmente angezeigt. 

![](assets/fragment-list-filters.png)

Fragmente können nach folgenden Kriterien gefiltert werden:

* Status (Entwurf oder Live)
* Typ (visuell oder Ausdruck)
* Erstellungs- oder Änderungsdatum
* Status (archiviert oder nicht)
* Tags

Sie können auch wählen, ob alle Fragmente angezeigt werden sollen oder nur die Elemente, die von der Person, die aktuell daran arbeitet, erstellt oder geändert wurden.

Über die Schaltfläche **[!UICONTROL Weitere Aktionen]** neben jedem Fragment können Sie Folgendes ausführen:

<!--* Add to package
* Open draft version-->
* Kopieren Sie das Fragment.
* Verwenden Sie die Option **[!UICONTROL Verweise erkunden]**, um die Journeys, Kampagnen oder Vorlagen anzuzeigen, in denen es verwendet wird. [Weitere Informationen](#explore-references)
* Archivieren Sie das Fragment. [Weitere Informationen](#archive-fragments)
* Bearbeiten Sie die Tags des Fragments. [Erfahren Sie, wie Sie mit einheitlichen Tags arbeiten](../start/search-filter-categorize.md#tags)

![](assets/fragment-list-more-actions.png)

## Status von Fragmenten

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="Status von neuen Fragmenten"
>abstract="Da **Entwurf**- und **Live**-Status mit der Journey Optimizer-Version vom Juni eingeführt wurden, haben alle vor dieser Version erstellten Fragmente den **Entwurf**-Status, auch wenn sie auf einer Journey oder Kampagne verwendet werden. Wenn Sie Änderungen an diesen Fragmenten vornehmen, müssen Sie sie veröffentlichen, um sie **Live** zu machen und die Änderungen an die zugehörigen Kampagnen und Journey weiterzugeben. Außerdem müssen Sie eine neue Journey-/Kampagnenversion erstellen und veröffentlichen. <br/>Für die Veröffentlichung ist die Benutzerberechtigung <a href="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manage">Fragment veröffentlichen</a> erforderlich."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manager" text="Weitere Informationen zu den Berechtigungen für Inhaltsfragmente"

Fragmente können mehrere Status aufweisen:

* **[!UICONTROL Entwurf]**: Das Fragment wird noch bearbeitet und wurde noch nicht genehmigt.

* **[!UICONTROL Live]**: Das Fragment wurde genehmigt und ist live. [Informationen zum Veröffentlichen eines Fragments](../content-management/create-fragments.md#publish)

  Wenn ein Live-Fragment bearbeitet wird, wird ein spezifisches Symbol neben seinem Status angezeigt. Klicken Sie auf dieses Symbol, um die Entwurfsversion des Fragments zu öffnen.

* **[!UICONTROL Publishing]**: Das Fragment wurde genehmigt und wird gerade veröffentlicht.
* **[!UICONTROL Archiviert:]**: Das Fragment wurde archiviert. [Informationen zum Archivieren von Fragmenten](#archive-fragments)

>[!CAUTION]
>
>Da **Entwurf**- und **Live**-Status mit der Journey Optimizer-Version vom Juni eingeführt wurden, haben alle vor dieser Version erstellten Fragmente den **Entwurf**-Status, auch wenn sie auf einer Journey oder Kampagne verwendet werden. Wenn Sie Änderungen an diesen Fragmenten vornehmen, müssen Sie sie veröffentlichen, um sie **Live** zu machen und die Änderungen an die zugehörigen Kampagnen und Journey weiterzugeben. Außerdem müssen Sie eine neue Journey-/Kampagnenversion erstellen und veröffentlichen. Für die Veröffentlichung ist die Benutzerberechtigung [Fragment veröffentlichen](../administration/ootb-product-profiles.md#content-library-manager) erforderlich.

## Bearbeiten von Fragmenten {#edit-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="Aktualisieren von Fragmenten in Kampagnen"
>abstract="Diese Kampagne wird nicht aktualisiert, wenn Sie Änderungen an dem Fragment veröffentlichen. Es muss eine neue Version veröffentlicht werden, damit die Funktion zum Aktualisieren von Fragmenten unterstützt werden kann."

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="Aktualisieren von Fragmenten in Journeys"
>abstract="Diese Journey wird nicht aktualisiert, wenn Sie Änderungen an dem Fragment veröffentlichen. Es muss eine neue Version veröffentlicht werden, damit die Funktion zum Aktualisieren von Fragmenten unterstützt werden kann."

Gehen Sie wie folgt vor, um ein Fragment zu bearbeiten.

1. Klicken Sie in der Liste **[!UICONTROL Fragmente]** auf das gewünschte Fragment.

1. Die Fragmenteigenschaften werden mit einer Vorschau des zugehörigen Inhalts geöffnet.

1. Wenn das bearbeitete Fragment den Status **[!UICONTROL Live]** aufweist, klicken Sie auf die Schaltfläche **[!UICONTROL Ändern]**, um eine Entwurfsversion des Fragments zu erstellen.

   >[!NOTE]
   >
   >Die aktuelle Version des Fragments ist weiterhin live, bis Sie die Entwurfsversion veröffentlichen.

1. Nehmen Sie die gewünschten Änderungen am Fragment vor. Um den Inhalt zu bearbeiten, klicken Sie auf die **[!UICONTROL Bearbeiten]**-Schaltfläche und aktualisieren Sie Ihren Inhalt so, wie Sie es bei der Neuerstellung eines Fragments tun würden. [Informationen zum Erstellen eines Fragments](#create-from-scratch)

   >[!NOTE]
   >
   >Beim Bearbeiten eines veröffentlichten Fragments können Sie jedes Personalisierungsfeld entfernen, aber keine neuen zum Fragmentinhalt hinzufügen. Wenn Sie personalisierte Attribute hinzufügen möchten, müssen Sie das Fragment duplizieren. [Weitere Informationen](#adding-new-attributes)

1. Sie können auch die Liste der Journeys, Kampagnen und Inhaltsvorlagen überprüfen, in denen das Fragment derzeit verwendet wird, indem Sie die Option **Explorer-Verweise** auswählen. [Weitere Informationen](#explore-references)

   ![](assets/fragment-edit.png)

1. Sobald Ihre Änderungen fertig sind, klicken Sie auf die Schaltfläche **Veröffentlichen**, um Ihre Änderungen live zu stellen.

Wenn Sie ein Fragment bearbeiten, werden die Änderungen automatisch auf alle Inhalte übertragen, die dieses Fragment verwenden, einschließlich Live-Journey und -Kampagnen - mit Ausnahme von Inhalten, bei denen die Vererbung vom Originalfragment unterbrochen wurde.

>[!NOTE]
>
>Informationen zum Unterbrechen der Vererbung finden Sie in den Abschnitten [Hinzufügen visueller Fragmente zu Ihren E-Mails](../email/use-visual-fragments.md#break-inheritance) und [Nutzen von Ausdrucksfragmenten](../personalization/use-expression-fragments.md#break-inheritance).

## Hinzufügen neuer Attribute zu einem Live-Fragment {#adding-new-attributes}

>[!WARNING]
>
>Das Hinzufügen neuer Attribute zu einem Live-Fragment wird nicht unterstützt.

Nach der Veröffentlichung eines Fragments wird der Satz personalisierter oder kontextueller Attribute für alle Kampagnen und Journey gesperrt, die darauf verweisen.

Gehen Sie wie folgt vor, um zusätzliche Attribute in ein Live-Fragment einzubinden.

1. Duplizieren Sie das vorhandene Fragment.

1. Fügen Sie der duplizierten Entwurfsversion die erforderlichen Attribute hinzu.

1. Publish die neue Version.

1. Aktualisieren Sie alle Kampagnen oder Journey, um auf das aktualisierte Fragment zu verweisen, in dem die neuen Attribute hinzugefügt wurden.

## Erkunden der Verweise {#explore-references}

Sie können die Liste aller Journeys, Kampagnen und Inhaltsvorlagen anzeigen, die derzeit ein Fragment verwenden.  Wählen Sie dazu entweder im Menü **[!UICONTROL Mehr Aktionen]** in der Fragmentliste oder im Bildschirm mit den Fragmenteigenschaften die Option **[!UICONTROL Verweise erkunden]** aus.

![](assets/fragment-explore-references.png)

Wählen Sie eine Registerkarte aus, um zwischen Journeys, Kampagnen und Vorlagen zu wechseln. Sie können ihren Status anzeigen und auf einen Namen klicken, um zum entsprechenden Element mit dem Fragmentverweis weitergeleitet zu werden.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>Wenn das Fragment in einer Journey, einer Kampagne oder einer Vorlage verwendet wird, die mit einer Kennzeichnung versehen ist, die den Zugriff darauf verhindert, wird oben auf der ausgewählten Registerkarte eine Warnmeldung angezeigt. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md)

## Archivieren von Fragmenten {#archive-fragments}

Sie können aus der Fragmentliste die Elemente löschen, die für Ihre Marke nicht mehr relevant sind.

Klicken Sie dazu auf das Symbol **[!UICONTROL Weitere Aktionen]** neben dem gewünschten Fragment und dann auf **[!UICONTROL Archivieren]**. Es wird daraufhin nicht länger in der Fragmentliste angezeigt, sodass es in zukünftigen E-Mails oder Vorlagen nicht mehr von Benutzenden verwendet werden kann.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>Die Archivierung eines Fragments, das in einem Inhalt verwendet wird, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->hat keine Auswirkungen auf diesen Inhalt.

Um die Archivierung eines Fragments aufzuheben, filtern Sie nach **[!UICONTROL archivierten]** Elementen und wählen Sie aus dem Menü **[!UICONTROL Mehr Aktionen]** die Option **[!UICONTROL Archivierung aufheben]** aus. Es ist nun wieder über die Fragmentliste zugänglich und kann in jeder E-Mail oder Vorlage verwendet werden.

![](assets/fragment-list-unarchive.png)

## Exportieren von Fragmenten in eine andere Sandbox {#export}

Mit Journey Optimizer können Sie ein Fragment von einer Sandbox in eine andere kopieren. Sie können beispielsweise ein Fragment aus Ihrer Staging-Sandbox-Umgebung in Ihre Produktions-Sandbox kopieren.

Der Kopiervorgang wird über einen **Paket-Export und -Import** zwischen der Quell- und Ziel-Sandbox durchgeführt. Detaillierte Informationen darüber, wie Sie Objekte exportieren und in eine Ziel-Sandbox importieren, finden Sie in diesem Abschnitt: [Kopieren von Objekten in eine andere Sandbox](../configuration/copy-objects-to-sandbox.md)
