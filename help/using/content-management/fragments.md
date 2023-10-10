---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit Fragmenten
description: Erfahren Sie, wie Sie Fragmente erstellen, um Inhalte in Journey Optimizer-Kampagnen und -Journeys wiederzuverwenden.
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
source-git-commit: b00a4e174e978121687428147b5b3861077c5182
workflow-type: tm+mt
source-wordcount: '1548'
ht-degree: 52%

---

# Arbeiten mit Fragmenten {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="Eigene Fragmente definieren"
>abstract="Erstellen und verwalten Sie eigenständige Fragmente, damit Ihre Inhalte über mehrere Journey und Kampagnen hinweg wiederverwendet werden können."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/personalized-dynamic-content/reusable-content/fragments.html#create-fragments" text="Erstellen von Fragmenten"

Ein Fragment ist eine wiederverwendbare Komponente, die in einer oder mehreren [!DNL Journey Optimizer]-Kampagnen und -Journeys referenziert werden kann.

Mit dieser Funktion können Sie mehrere benutzerdefinierte Inhaltsbausteine vorab erstellen, die von Marketing-Benutzern verwendet werden können, um E-Mail-Inhalte schnell in einem verbesserten Designprozess zusammenzustellen.

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [In diesen Videos erfahren Sie, wie Sie Fragmente verwalten, erstellen und verwenden.](#video-fragments)

So nutzen Sie Fragmente am besten:

* Erstellen Sie Ihre eigenen Fragmente. Sie können visuelle Fragmente oder Ausdrucksfragmente erstellen. [Weitere Informationen](#create-fragments)

* Verwenden Sie sie so oft wie nötig in Ihrem Inhalt. Siehe [Hinzufügen visueller Fragmente](../email/use-visual-fragments.md) und [Ausdrucksfragmente nutzen](../personalization/use-expression-fragments.md)

## Vor Beginn {#fragment-prerequisites}

Zum Erstellen, Bearbeiten und Archivieren von Fragmenten benötigen Sie die **[!DNL Manage Library Items]** -Berechtigung im **[!DNL Content Library Manager]** Produktprofil. [Weitere Informationen](../administration/ootb-product-profiles.md#content-library-manager)

In dieser Version gelten die folgenden Einschränkungen:

* Visuelle Fragmente sind nur für den E-Mail-Kanal verfügbar

* Ausdrucksfragmente sind nicht für Web- und In-App-Kanäle verfügbar

## Zugreifen auf und Verwalten von Fragmenten {#access-manage-fragments}

Um auf die Fragmentliste zuzugreifen, wählen Sie im Menü links **[!UICONTROL Content-Management]** > **[!UICONTROL Fragmente]** aus.

![](assets/fragment-list.png)

Alle in der aktuellen Sandbox erstellten Fragmente - entweder [aus dem **[!UICONTROL Fragmente]** Menü](#create-fragments), entweder mithilfe der [Als Fragment speichern](#save-as-fragment) option - angezeigt.

Fragmente können nach folgenden Kriterien gefiltert werden:

* Typ: **[!UICONTROL Visuell]** oder **[!UICONTROL Ausdruck]**
* Tags
* Erstellungs- oder Änderungsdatum

Sie können wählen, ob alle Fragmente angezeigt werden sollen oder nur die Elemente, die von der Person, die aktuell daran arbeitet, erstellt oder geändert wurden.

Sie können auch die **[!UICONTROL archivierten]** Fragmente anzeigen. [Weitere Informationen](#archive-fragments)

![](assets/fragment-list-filters.png)

Aus dem **[!UICONTROL Mehr Aktionen]** neben jedem Fragment können Sie Folgendes tun:

* Duplizieren Sie ein Fragment.

* Verwenden Sie die Option **[!UICONTROL Verweise erkunden]**, um die Journeys, Kampagnen oder Vorlagen anzuzeigen, in denen es verwendet wird. [Weitere Informationen](#explore-references)

* Kopieren Sie ein Fragment in eine andere Sandbox. <!--Learn more?-->

* Archivieren Sie ein Fragment. [Weitere Informationen](#archive-fragments)

* Bearbeiten von [tags](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

### Bearbeiten von Fragmenten {#edit-fragments}

Gehen Sie wie folgt vor, um ein Fragment zu bearbeiten.

1. Klicken Sie auf das gewünschte Element aus der **[!UICONTROL Fragmente]** Liste.
1. Über die Fragmenteigenschaften können Sie [Verweise erkunden](#explore-references), den [Zugriff verwalten](../administration/object-based-access.md) und die Fragmentdetails einschließlich [Tags](../start/search-filter-categorize.md#tags) aktualisieren.

   ![](../email/assets/fragment-edit-content.png)

1. Wählen Sie die entsprechende Schaltfläche aus, um den Inhalt zu bearbeiten, wie Sie es bei der kompletten Neuerstellung eines Fragments tun würden. [Weitere Informationen](#create-from-scratch)

>[!NOTE]
>
>Wenn Sie ein Fragment bearbeiten, werden die Änderungen automatisch an alle Inhalte übertragen, die dieses Fragment verwenden, mit Ausnahme der in **[!UICONTROL Live]** Journey oder Kampagnen. Sie können auch die Vererbung vom ursprünglichen Fragment unterbrechen. Weitere Informationen finden Sie unter [Hinzufügen visueller Fragmente zu E-Mails](../email/use-visual-fragments.md#break-inheritance) und [Ausdrucksfragmente nutzen](../personalization/use-expression-fragments.md#break-inheritance) Abschnitte.

### Verweise erkunden {#explore-references}

Sie können die Liste der Journeys, Kampagnen und Inhaltsvorlagen anzeigen, die derzeit ein Fragment verwenden.

Wählen Sie dazu entweder über das Menü **[!UICONTROL Mehr Aktionen]** in der Fragmentliste oder über den Bildschirm mit den Fragmenteigenschaften die Option **[!UICONTROL Verweise erkunden]** aus.

![](assets/fragment-explore-references.png)

Wählen Sie eine Registerkarte aus, um zwischen Journey, Kampagnen, Vorlagen und Fragmenten zu wechseln. Sie können ihren Status anzeigen und auf einen Namen klicken, um zum entsprechenden Element mit dem Fragmentverweis weitergeleitet zu werden.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>Wenn das Fragment in einer Journey, einer Kampagne oder einer Vorlage verwendet wird, die mit einer Kennzeichnung versehen ist, die den Zugriff darauf verhindert, wird oben auf der ausgewählten Registerkarte eine Warnmeldung angezeigt. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md)

### Archivieren von Fragmenten {#archive-fragments}

Sie können aus der Fragmentliste die Elemente löschen, die für Ihre Marke nicht mehr relevant sind.

Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Mehr Aktionen]** Schaltfläche neben dem gewünschten Fragment und wählen Sie **[!UICONTROL Archivieren]**. Es wird daraufhin nicht länger in der Fragmentliste angezeigt, sodass es in zukünftigen E-Mails oder Vorlagen nicht mehr von Benutzenden verwendet werden kann.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>Wenn Sie ein Fragment archivieren, das in einem Inhalt verwendet wird, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->diese Inhalte nicht betroffen sind.

Um die Archivierung eines Fragments aufzuheben, filtern Sie nach **[!UICONTROL archivierten]** Elementen und wählen Sie aus dem Menü **[!UICONTROL Mehr Aktionen]** die Option **[!UICONTROL Archivierung aufheben]** aus. Es ist nun wieder über die Fragmentliste zugänglich und kann in jeder E-Mail oder Vorlage verwendet werden.

![](assets/fragment-list-unarchive.png)

## Erstellen von Fragmenten {#create-fragments}

Es gibt zwei Möglichkeiten, Fragmente zu erstellen:

* Erstellen Sie ein Fragment mithilfe des Menüs für **[!UICONTROL Fragmente]** komplett neu. [Weitere Informationen](#create-from-scratch)

* Speichern Sie beim Entwerfen von Inhalten einen Teil Ihres Inhalts als Fragment. [Weitere Informationen](#save-as-fragment)

Nach dem Speichern ist das Fragment für die Verwendung in einer Journey, Kampagne oder Vorlage verfügbar. Unabhängig davon, ob es von Grund auf neu oder aus einem vorhandenen Inhalt erstellt wurde, können Sie dieses Fragment jetzt beim Erstellen von Inhalten in [!DNL Journey Optimizer]. Siehe [Hinzufügen visueller Fragmente](../email/use-visual-fragments.md) und [Ausdrucksfragmente nutzen](../personalization/use-expression-fragments.md)

### Neuerstellen von Fragmenten {#create-from-scratch}

Gehen Sie wie folgt vor, um ein Fragment komplett neu zu erstellen.

1. [](#access-manage-fragments)Greifen Sie im Menü links über **[!UICONTROL Content-Management]** > **[!UICONTROL Fragmente]** auf die Fragmentliste zu.

1. Wählen Sie **[!UICONTROL Fragment erstellen]** aus.

1. Füllen Sie die Fragmentdetails aus, d. h., geben Sie den Namen und (falls erforderlich) eine Beschreibung ein.

   ![](assets/fragment-details.png)

1. Wählen Sie den Fragmenttyp aus: [Visual Fragment](#create-visual-fragment) oder [Ausdrucksfragment](#create-expression-fragment).

1. Um dem Fragment benutzerdefinierte oder zentrale Datennutzungskennzeichnungen zuzuweisen, wählen Sie **[!UICONTROL Zugriff verwalten]** aus. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md).

1. Wählen oder erstellen Sie Adobe Experience Platform-Tags im Feld **[!UICONTROL Tags]** aus, um Ihr Fragment für eine verbesserte Suche zu kategorisieren. [Weitere Informationen](../start/search-filter-categorize.md#tags)

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

### Erstellen eines visuellen Fragments {#create-visual-fragment}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Wählen Sie den visuellen Typ"
>abstract="Erstellen Sie ein eigenständiges visuelles Fragment, um Ihren Inhalt in einer E-Mail innerhalb einer Journey, einer Kampagne oder in einer Inhaltsvorlage wiederverwendbar zu machen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments.html" text="Hinzufügen visueller Fragmente zu E-Mails"

1. [Fragment erstellen](#create-from-scratch) aus dem **[!UICONTROL Content Management]** > **[!UICONTROL Fragmente]** Menü links auswählen. **[!UICONTROL Visual Fragment]** Typ.

   >[!NOTE]
   >
   >Derzeit ist für visuelle Fragmente nur der **Email** -Kanal wird unterstützt.

1. Der [E-Mail-Designer](../email/get-started-email-design.md) wird angezeigt. Bearbeiten Sie Ihre Inhalte nach Bedarf, so wie Sie es bei jeder E-Mail innerhalb einer Journey oder einer Kampagne tun würden.

   >[!NOTE]
   >
   >Sie können Personalisierungsfelder und dynamische Inhalte hinzufügen, doch werden in Fragmenten keine kontextuellen Attribute unterstützt.

   ![](assets/fragment-designer.png)

1. Sobald Ihr Fragment fertig ist, klicken Sie auf **[!UICONTROL Speichern]**. Sie wird zum [Fragmentliste](#access-manage-fragments).

1. Klicken Sie bei Bedarf auf den Pfeil neben dem Fragmentnamen, um zum Bildschirm **[!UICONTROL Details]** zurückzukehren und das Fragment zu bearbeiten.

   ![](assets/fragment-designer-back.png)

Dieses Fragment kann nun beim Erstellen von [E-Mails](../email/get-started-email-design.md) oder [Inhaltsvorlagen](content-templates.md) in [!DNL Journey Optimizer] verwendet werden. [Weitere Informationen](../email/use-visual-fragments.md)

### Ausdrucksfragment erstellen {#create-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Wählen Sie den Ausdruckstyp"
>abstract="Erstellen Sie ein eigenständiges Ausdrucksfragment, damit Ihr Inhalt über mehrere Journey und Kampagnen hinweg wiederverwendet werden kann. Bei Verwendung des Ausdruckseditors können Sie alle Ausdrucksfragmente nutzen, die in der aktuellen Sandbox erstellt wurden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/personalized-dynamic-content/personalization/expression-editor/use-expression-fragments.html" text="Ausdrucksfragmente nutzen"

1. [Fragment erstellen](#create-from-scratch) aus dem **[!UICONTROL Content Management]** > **[!UICONTROL Fragmente]** Menü links auswählen. **[!UICONTROL Ausdrucksfragment]** Typ.

1. Wählen Sie den zu verwendenden Code-Typ aus: **[!UICONTROL HTML]**, **[!UICONTROL JSON]** oder **[!UICONTROL Text]**.

   ![](assets/fragment-expression-type.png)

   <!--Expression fragments can be used in any channel.-->

1. Klicken Sie auf **[!UICONTROL Erstellen]**. Der Ausdruckseditor wird geöffnet.

1. Sie können die [!DNL Journey Optimizer] Ausdruckseditor mit allen Personalisierungs- und Bearbeitungsfunktionen. [Weitere Informationen](../personalization/personalization-build-expressions.md)

   ![](assets/fragment-expression-editor.png)

1. Sobald Ihr Fragment fertig ist, klicken Sie auf **[!UICONTROL Speichern]**. Sie wird zum [Fragmentliste](#access-manage-fragments).

1. Klicken Sie bei Bedarf auf den Pfeil neben dem Fragmentnamen, um zum Bildschirm **[!UICONTROL Details]** zurückzukehren und das Fragment zu bearbeiten.

Dieses Fragment kann jetzt beim Erstellen von Inhalten im [!DNL Journey Optimizer] Ausdruckseditor. [Weitere Informationen](../personalization/use-expression-fragments.md)

## Speichern als Fragment {#save-as-fragment}

Beim Bearbeiten von Inhalt in [!DNL Journey Optimizer], können Sie Ihren Inhalt ganz oder teilweise als Fragment speichern, um ihn später wiederzuverwenden.

### Als visuelles Fragment speichern {#save-as-visual-fragment}

Beim Entwerfen einer [Inhaltsvorlage](content-templates.md) oder [email](../email/get-started-email-design.md) in einer Kampagne oder einer Journey können Sie einen Teil Ihres Inhalts als visuelles Fragment speichern. Gehen Sie dazu wie folgt vor.

1. Klicken Sie im [E-Mail-Designer](../email/get-started-email-design.md) oben rechts im Bildschirm auf die Auslassungspunkte.

1. Wählen Sie im Dropdown-Menü die Option **[!UICONTROL Als Fragment speichern]** aus.

   ![](assets/fragment-save-as.png)

1. Der Bildschirm **[!UICONTROL Als Fragment speichern]** wird angezeigt. Hier können Sie die Elemente auswählen, die Sie in Ihr Fragment aufnehmen möchten, darunter Personalisierungsfelder und dynamische Inhalte. Beachten Sie, dass kontextuelle Attribute in Fragmenten nicht unterstützt werden.

   >[!CAUTION]
   >
   >Sie können nur nebeneinander liegende Abschnitte auswählen. Sie können keine leere Struktur und auch kein anderes Fragment auswählen.

   ![](assets/fragment-save-as-screen.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**. Füllen Sie die Fragmentdetails aus, d. h., geben Sie den Namen und (falls erforderlich) eine Beschreibung ein.

1. Um dem Fragment benutzerdefinierte oder zentrale Datennutzungskennzeichnungen zuzuweisen, wählen Sie **[!UICONTROL Zugriff verwalten]** aus. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md).

1. Wählen oder erstellen Sie Adobe Experience Platform-Tags im Feld **Tags**, um Ihre Vorlage für eine verbesserte Suche zu kategorisieren. [Weitere Informationen](../start/search-filter-categorize.md#tags)

1. Klicken Sie erneut auf **[!UICONTROL Erstellen]**. Das Fragment wird in gespeichert und dem [Fragmentliste](#access-manage-fragments), auf die über die [!DNL Journey Optimizer] dediziertes Menü.

   Es wird zu einem eigenständigen Fragment, für das [Zugriff](#access-manage-fragments), [Bearbeitung](#edit-fragments) und [Archivierung](#archive-fragments) wie für jedes andere Element in dieser Liste möglich sind.

Dieses Fragment kann nun beim Erstellen von [E-Mails](../email/get-started-email-design.md) oder [Inhaltsvorlagen](content-templates.md) in [!DNL Journey Optimizer] verwendet werden. [Weitere Informationen](../email/use-visual-fragments.md)

>[!NOTE]
>
>Änderungen an diesem neuen Fragment werden nicht auf die E-Mail oder Vorlage übertragen, aus der das Fragment hervorgegangen ist. Wenn der ursprüngliche Inhalt in dieser E-Mail oder Vorlage bearbeitet wird, wird das neue Fragment ebenfalls nicht geändert.

### Als Ausdrucksfragment speichern {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="Als Ausdrucksfragment speichern"
>abstract="Die [!DNL Journey Optimizer] Mit dem Ausdruckseditor können Sie Inhalte als Ausdrucksfragmente speichern. Diese Ausdrücke stehen dann zur Erstellung personalisierter Inhalte zur Verfügung."

Die [!DNL Journey Optimizer] Mit dem Ausdruckseditor können Sie Inhalte als Ausdrucksfragmente speichern. Diese Ausdrücke stehen dann zur Erstellung personalisierter Inhalte zur Verfügung.

Gehen Sie wie folgt vor, um Inhalte als Ausdrucksfragment zu speichern.

1. Im [Ausdruckseditor](../personalization/personalization-build-expressions.md) -Schnittstelle, einen Ausdruck erstellen und auf **[!UICONTROL Als Fragment speichern]**.

1. Geben Sie im rechten Bereich einen Namen und eine Beschreibung für den Ausdruck ein, damit Benutzer ihn leichter finden können.

   ![](assets/expression-fragment-save-as.png)

1. Klicks **[!UICONTROL Fragment speichern]**.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. Das Ausdrucksfragment wird zum [Fragmentliste](#access-manage-fragments). Jetzt können Sie damit personalisierte Inhalte erstellen.

>[!NOTE]
>
>Ausdrücke dürfen 200 KB nicht überschreiten.

## Anleitungsvideo {#video-fragments}

Erfahren Sie, wie Sie visuelle Fragmente in verwalten, erstellen und verwenden [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

Erfahren Sie, wie Sie Ausdrucksfragmente verwalten, erstellen und verwenden in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
