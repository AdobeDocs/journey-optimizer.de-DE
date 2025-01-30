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
source-git-commit: 69aa2eb79ac5a86c8cc5e27951d3b4edd2a5d8bf
workflow-type: tm+mt
source-wordcount: '1144'
ht-degree: 56%

---

# Verwalten von Fragmenten {#manage-fragments}

Um Ihre Fragmente zu verwalten, greifen Sie links über das Menü **[!UICONTROL Content-Management]** > **[!UICONTROL Fragmente]** auf die Fragmentliste zu.

Es werden alle in der aktuellen Sandbox entweder [über das Menü **[!UICONTROL Fragmente]** oder](#create-fragments) die Option [Als Fragment speichern](#save-as-fragment) erstellten Fragmente angezeigt. 

Fragmente können nach folgenden Kriterien gefiltert werden:

* Status (Entwurf oder Live)
* Typ (visuell oder Ausdruck)
* Erstellungs- oder Änderungsdatum
* Status (archiviert oder nicht)
* Tags

![](assets/fragment-list-filters.png){width="90%" align="left"}

Sie können auch wählen, ob alle Fragmente angezeigt werden sollen oder nur die Elemente, die von der Person, die aktuell daran arbeitet, erstellt oder geändert wurden.

Über die Schaltfläche **[!UICONTROL Weitere Aktionen]** neben jedem Fragment können Sie Folgendes ausführen:

* Fügen Sie es einem Paket für den Export hinzu. [Weitere Informationen](#export)
* Wenn das Fragment live ist, öffnen Sie eine Entwurfsversion, um sie zu bearbeiten. [Weitere Informationen](#edit-fragments)
* Kopieren Sie das Fragment.
* Verwenden Sie die Option **[!UICONTROL Verweise erkunden]**, um die Journeys, Kampagnen oder Vorlagen anzuzeigen, in denen es verwendet wird. [Weitere Informationen](#explore-references)
* Archivieren Sie das Fragment. [Weitere Informationen](#archive-fragments)
* Bearbeiten Sie die Tags des Fragments. [Erfahren Sie, wie Sie mit einheitlichen Tags arbeiten](../start/search-filter-categorize.md#tags)

![](assets/fragment-list-more-actions.png){width="70%" align="left"}

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

## Bearbeiten eines Fragments {#edit-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="Aktualisieren von Fragmenten in Kampagnen"
>abstract="Diese Kampagne wird nicht aktualisiert, wenn Sie Änderungen an dem Fragment veröffentlichen. Es muss eine neue Version veröffentlicht werden, damit die Funktion zum Aktualisieren von Fragmenten unterstützt werden kann."

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="Aktualisieren von Fragmenten in Journeys"
>abstract="Diese Journey wird nicht aktualisiert, wenn Sie Änderungen an dem Fragment veröffentlichen. Es muss eine neue Version veröffentlicht werden, damit die Funktion zum Aktualisieren von Fragmenten unterstützt werden kann."

Gehen Sie wie folgt vor, um ein Fragment zu bearbeiten.

1. Klicken Sie in der Liste „Fragmente **[!UICONTROL auf]** gewünschte Fragment. Der Bildschirm mit den Fragmenteigenschaften wird mit einer Vorschau des Inhalts geöffnet.

1. Sie können die Liste der Journey, Kampagnen und Inhaltsvorlagen überprüfen, in denen das Fragment derzeit verwendet wird. Wählen Sie dazu die Option **[!UICONTROL Verweise erkunden]** aus der Schaltfläche Mehr . [Weitere Informationen](#explore-references)

1. Wenn das in Bearbeitung befindliche Fragment den Status **[!UICONTROL Live]** aufweist, klicken Sie auf die Schaltfläche **[!UICONTROL Ändern]**, um eine Entwurfsversion des Fragments zu erstellen. Klicken Sie auf **[!UICONTROL Bestätigen]**.

   ![](assets/fragment-live-modify.png){width="70%" align="left"}

   >[!NOTE]
   >
   >Die aktuelle Version des Fragments bleibt so lange live, bis Sie die neue aktualisierte Version veröffentlichen.

1. Nehmen Sie bei Bedarf die gewünschten Änderungen an den Fragmentdetails vor.

1. Um den Inhalt des Fragments zu ändern, klicken Sie auf die Schaltfläche **[!UICONTROL Bearbeiten]** und aktualisieren Sie Ihren Inhalt so, wie Sie es bei der Neuerstellung eines Fragments tun würden. [Informationen zum Erstellen eines Fragments](create-fragments.md#content)

   ![](assets/fragment-edit.png){width="70%" align="left"}

   >[!NOTE]
   >
   >Beim Bearbeiten eines veröffentlichten Fragments können Sie jedes Personalisierungsfeld entfernen, aber keine neuen zum Fragmentinhalt hinzufügen. Wenn Sie personalisierte Attribute hinzufügen möchten, müssen Sie das Fragment duplizieren. [Weitere Informationen](#adding-new-attributes)

1. Sobald Ihre Änderungen fertig sind, speichern Sie sie und klicken Sie auf die Schaltfläche **[!UICONTROL Publish]**, um Ihre Änderungen live zu schalten. [Weitere Informationen](create-fragments.md#publish)

Wenn Sie ein Fragment bearbeiten, werden die Änderungen automatisch auf alle Inhalte übertragen, die dieses Fragment verwenden, einschließlich Live-Journey und -Kampagnen - mit Ausnahme von Inhalten, bei denen die Vererbung vom Originalfragment unterbrochen wurde.

>[!NOTE]
>
>Informationen zum Unterbrechen der Vererbung finden Sie in den Abschnitten [Hinzufügen visueller Fragmente zu Ihren E-Mails](../email/use-visual-fragments.md#break-inheritance) und [Nutzen von Ausdrucksfragmenten](../personalization/use-expression-fragments.md#break-inheritance).

## Hinzufügen neuer Attribute zu einem Live-Fragment {#adding-new-attributes}

>[!WARNING]
>
>Das Hinzufügen neuer [personalisierter Attribute](../personalization/personalization-build-expressions.md) zu einem Live-Fragment wird nicht unterstützt.

Nach der Veröffentlichung eines Fragments wird der Satz personalisierter oder kontextueller Attribute für alle Kampagnen und Journey gesperrt, die darauf verweisen.

Gehen Sie wie folgt vor, um zusätzliche Attribute in ein Live-Fragment einzubinden.

1. Duplizieren Sie das vorhandene Fragment mithilfe der Schaltfläche **[!UICONTROL Mehr Aktionen]** .

   ![](assets/fragment-list-more-actions.png){width="70%" align="left"}

1. Wählen Sie das duplizierte Fragment aus, um es zu öffnen, und klicken Sie auf **[!UICONTROL Bearbeiten]**.

1. [Fügen Sie die neuen gewünschten Attribute](../personalization/personalization-build-expressions.md#add) zum duplizierten Fragment hinzu, z. B. Personalisierungsfelder.

   ![](assets/fragment-add-new-attribute.png){width="70%" align="left"}

1. Speichern Sie Ihre Änderungen und veröffentlichen Sie das neue Fragment. [Weitere Informationen](create-fragments.md#publish)

1. Aktualisieren Sie alle Kampagnen oder Journey, um auf das aktualisierte Fragment zu verweisen, in dem die neuen Attribute hinzugefügt wurden.

   * [Erfahren Sie, wie Sie visuelle Fragmente verwenden](../email/use-visual-fragments.md)
   * [Erfahren Sie, wie Sie Ausdrucksfragmente verwenden](../personalization/use-expression-fragments.md)

## Erkunden der Verweise {#explore-references}

Sie können die Liste aller Journeys, Kampagnen und Inhaltsvorlagen anzeigen, die derzeit ein Fragment verwenden.  Wählen Sie dazu **[!UICONTROL Verweise erkunden]** aus dem Menü **[!UICONTROL Mehr Aktionen]** entweder in der Fragmentliste oder im Bildschirm mit den Fragmenteigenschaften.

![](assets/fragment-explore-references.png){width="70%" align="left"}

Wählen Sie eine Registerkarte aus, um zwischen Journeys, Kampagnen und Vorlagen zu wechseln. Sie können ihren Status anzeigen und auf einen Namen klicken, um zum entsprechenden Element mit dem Fragmentverweis weitergeleitet zu werden.

![](assets/fragment-usage-screen.png){width="70%" align="left"}

>[!NOTE]
>
>Wenn das Fragment in einer Journey, einer Kampagne oder einer Vorlage verwendet wird, die mit einer Kennzeichnung versehen ist, die den Zugriff darauf verhindert, wird oben auf der ausgewählten Registerkarte eine Warnmeldung angezeigt. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md)

## Archivieren von Fragmenten {#archive-fragments}

Sie können aus der Fragmentliste die Elemente löschen, die für Ihre Marke nicht mehr relevant sind.

Klicken Sie dazu auf das Symbol **[!UICONTROL Weitere Aktionen]** neben dem gewünschten Fragment und dann auf **[!UICONTROL Archivieren]**. Es wird daraufhin nicht länger in der Fragmentliste angezeigt, sodass es in zukünftigen E-Mails oder Vorlagen nicht mehr von Benutzenden verwendet werden kann.

![](assets/fragment-list-archive.png){width="70%" align="left"}

>[!NOTE]
>
>Die Archivierung eines Fragments, das in einem Inhalt verwendet wird, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->hat keine Auswirkungen auf diesen Inhalt.

Um die Archivierung eines Fragments aufzuheben, filtern Sie nach **[!UICONTROL archivierten]** Elementen und wählen Sie aus dem Menü **[!UICONTROL Mehr Aktionen]** die Option **[!UICONTROL Archivierung aufheben]** aus. Es ist nun wieder über die Fragmentliste zugänglich und kann in jeder E-Mail oder Vorlage verwendet werden.

![](assets/fragment-list-unarchive.png){width="70%" align="left"}

## Exportieren von Fragmenten in eine andere Sandbox {#export}

Mit Journey Optimizer können Sie ein Fragment von einer Sandbox in eine andere kopieren. Sie können beispielsweise ein Fragment aus Ihrer Staging-Sandbox-Umgebung in Ihre Produktions-Sandbox kopieren.

Der Kopiervorgang wird über einen **Paket-Export und -Import** zwischen der Quell- und Ziel-Sandbox durchgeführt. Detaillierte Informationen zum Exportieren von Objekten und Importieren in eine Ziel-Sandbox finden Sie in diesem Abschnitt [Objekte in eine andere Sandbox kopieren](../configuration/copy-objects-to-sandbox.md).
