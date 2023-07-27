---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen von Fragmenten
description: Erfahren Sie, wie Sie Fragmente erstellen, um Inhalte in Journey Optimizer-Kampagnen und -Journeys wiederzuverwenden.
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 05f74838-6766-47ea-aaed-a67c174a51a9
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '1495'
ht-degree: 96%

---

# Arbeiten mit Fragmenten {#fragments}

Ein Fragment ist eine wiederverwendbare Komponente, die in einer oder mehreren [!DNL Journey Optimizer]-Kampagnen und -Journeys referenziert werden kann.

Mit dieser Funktion können Sie mehrere benutzerdefinierte Inhaltsbausteine vorab erstellen, die von technisch nicht versierten Personen im Marketing verwendet werden können, um E-Mail-Inhalte schnell in einem verbesserten Design-Prozess zusammenzustellen.

➡️ [In diesem Video erfahren Sie, wie Sie Fragmente verwalten, erstellen und verwenden.](#video-fragments)

>[!CAUTION]
>
>Zum Erstellen, Bearbeiten und Archivieren von Fragmenten benötigen Sie die Berechtigung **[!DNL Manage Library Items]** im **[!DNL Content Library Manager]**-Produktprofil. [Weitere Informationen](../administration/ootb-product-profiles.md#content-library-manager)

So nutzen Sie Fragmente am besten:

* Erstellen Sie Ihre eigenen Fragmente. Siehe [Erstellen von Fragmenten](#create-fragments).
* Diese können beliebig oft in E-Mails verwendet werden. Siehe [Verwenden von Fragmenten](#use-fragments).

>[!NOTE]
>
>Diese Funktion ist derzeit nur für E-Mails verfügbar.

## Zugreifen auf und Verwalten von Fragmenten {#access-manage-fragments}

Um auf die Fragmentliste zuzugreifen, wählen Sie im Menü links **[!UICONTROL Content-Management]** > **[!UICONTROL Fragmente]** aus.

![](assets/fragment-list.png)

Alle Fragmente, die in der aktuellen Sandbox (entweder über das Menü **[!UICONTROL Fragmente]** oder über die Option [Als Fragment speichern](#save-as-fragment)) erstellt wurden, werden angezeigt.

Sie können Fragmente nach dem Erstellungs- oder Änderungsdatum filtern. Sie können wählen, ob alle Fragmente angezeigt werden sollen oder nur die Elemente, die von der Person, die aktuell daran arbeitet, erstellt oder geändert wurden. Sie können auch die **[!UICONTROL archivierten]** Fragmente anzeigen. [Weitere Informationen](#archive-fragments)

![](assets/fragment-list-filters.png)

Über das Symbol **[!UICONTROL Mehr Aktionen]** neben jedem Fragment haben Sie folgende Möglichkeiten:

* Duplizieren Sie ein Fragment.

* Verwenden Sie die Option **[!UICONTROL Verweise erkunden]**, um die Journeys, Kampagnen oder Vorlagen anzuzeigen, in denen es verwendet wird. [Weitere Informationen](#explore-references)

* Archivieren Sie ein Fragment. [Weitere Informationen](#archive-fragments)

![](assets/fragment-list-more-actions.png)

### Bearbeiten von Fragmenten {#edit-fragments}

Gehen Sie wie folgt vor, um ein Fragment zu bearbeiten.

1. Klicken Sie auf das gewünschte Element in der **[!UICONTROL Fragmentliste]**.
1. In den Fragmenteigenschaften können Sie [Erkunden von Verweisen](#explore-references), [Zugriff verwalten](../administration/object-based-access.md)und aktualisieren Sie die Fragmentdetails, einschließlich [tags](../start/search-filter-categorize.md#tags).

   ![](assets/fragment-edit-content.png)

1. Wählen Sie die entsprechende Schaltfläche aus, um den Inhalt zu bearbeiten, wie Sie es bei der kompletten Neuerstellung eines Fragments tun würden. [Weitere Informationen](#create-from-scratch)


>[!NOTE]
>
>Wenn Sie ein Fragment bearbeiten, werden die Änderungen automatisch auf alle E-Mails oder Vorlagen übertragen, die dieses Fragment enthalten, mit Ausnahme der in **[!UICONTROL Live]**-Journeys oder -Kampagnen verwendeten E-Mails. Sie können auch die Vererbung vom ursprünglichen Fragment unterbrechen. [Weitere Informationen](#break-inheritance)

<!--Changes made to a fragment are not propagated to live journeys or campaigns where it is used.-->

<!--When added to an email, if you want to modify a fragment for a specific email, you can break the synchronization with the original fragment. The fragment becomes part of the email content and the changes will not be synchronized anymore. [Learn more](#break-inheritance)-->

### Verweise erkunden {#explore-references}

Sie können die Liste der Journeys, Kampagnen und Inhaltsvorlagen anzeigen, die derzeit ein Fragment verwenden.

Wählen Sie dazu entweder über das Menü **[!UICONTROL Mehr Aktionen]** in der Fragmentliste oder über den Bildschirm mit den Fragmenteigenschaften die Option **[!UICONTROL Verweise erkunden]** aus.

![](assets/fragment-explore-references.png)

Wählen Sie eine Registerkarte aus, um zwischen Journeys, Kampagnen und Vorlagen umzuschalten. Sie können ihren Status anzeigen und auf einen Namen klicken, um zum entsprechenden Element mit dem Fragmentverweis weitergeleitet zu werden.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>Wenn das Fragment in einer Journey, einer Kampagne oder einer Vorlage verwendet wird, die mit einer Kennzeichnung versehen ist, die den Zugriff darauf verhindert, wird oben auf der ausgewählten Registerkarte eine Warnmeldung angezeigt. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md)

### Archivieren von Fragmenten {#archive-fragments}

Sie können aus der Fragmentliste die Elemente löschen, die für Ihre Marke nicht mehr relevant sind.

Klicken Sie dazu auf das Symbol **[!UICONTROL Mehr Aktionen]** neben dem gewünschten Fragment und wählen Sie **[!UICONTROL Archivieren]** aus. Es wird daraufhin nicht länger in der Fragmentliste angezeigt, sodass es in zukünftigen E-Mails oder Vorlagen nicht mehr von Benutzenden verwendet werden kann.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>Wenn Sie ein Fragment archivieren, das in einer E-Mail oder in einer Inhaltsvorlage verwendet wird, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->ist die E-Mail oder Vorlage davon nicht betroffen.

Um die Archivierung eines Fragments aufzuheben, filtern Sie nach **[!UICONTROL archivierten]** Elementen und wählen Sie aus dem Menü **[!UICONTROL Mehr Aktionen]** die Option **[!UICONTROL Archivierung aufheben]** aus. Es ist nun wieder über die Fragmentliste zugänglich und kann in jeder E-Mail oder Vorlage verwendet werden.

![](assets/fragment-list-unarchive.png)

## Erstellen von Fragmenten {#create-fragments}

Es gibt zwei Möglichkeiten, Fragmente zu erstellen:

* Erstellen Sie ein Fragment mithilfe des Menüs für **[!UICONTROL Fragmente]** komplett neu. [Weitere Informationen](#create-template-from-scratch)

* Speichern Sie beim Entwerfen einer E-Mail oder einer Inhaltsvorlage einen Teil Ihres Inhalts als Fragment. [Weitere Informationen](#save-as-template)

Nach dem Speichern ist das Fragment für die Verwendung in einer Journey, Kampagne oder Vorlage verfügbar. Unabhängig davon, ob es komplett neu oder aus vorhandenen Inhalten erstellt wurde, können Sie dieses Fragment jetzt beim Erstellen beliebiger [E-Mails](get-started-email-design.md) oder [Inhaltsvorlagen](content-templates.md) in [!DNL Journey Optimizer] verwenden. [Weitere Informationen](#use-fragments)

### Neuerstellen von Fragmenten {#create-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="Definieren eines eigenen Fragments"
>abstract="Erstellen Sie ein komplett neues, eigenständiges Fragment, damit Sie Ihre Inhalte für mehrere Journeys und Kampagnen wiederverwenden können."

Gehen Sie wie folgt vor, um ein Fragment komplett neu zu erstellen.

1. Greifen Sie im Menü links über **[!UICONTROL Content-Management]** > **[!UICONTROL Fragmente]** auf die Fragmentliste zu.

1. Wählen Sie **[!UICONTROL Fragment erstellen]** aus.

1. Füllen Sie die Fragmentdetails aus, d. h., geben Sie den Namen und (falls erforderlich) eine Beschreibung ein.

   ![](assets/fragment-details.png)

   >[!NOTE]
   >
   >Derzeit werden nur der Typ **[!UICONTROL Visuelles Fragment]** und der **E-Mail**-Kanal unterstützt.

1. Um dem Fragment benutzerdefinierte oder zentrale Datennutzungskennzeichnungen zuzuweisen, wählen Sie **[!UICONTROL Zugriff verwalten]** aus. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md).

1. Adobe Experience Platform-Tags aus dem **[!UICONTROL Tags]** -Feld, um Ihr Fragment für eine verbesserte Suche zu kategorisieren. [Weitere Informationen](../start/search-filter-categorize.md#tags)

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

1. Der [E-Mail-Designer](get-started-email-design.md) wird angezeigt. Bearbeiten Sie Ihre Inhalte nach Bedarf, so wie Sie es bei jeder E-Mail innerhalb einer Journey oder einer Kampagne tun würden.

   >[!NOTE]
   >
   >Sie können Personalisierungsfelder und dynamische Inhalte hinzufügen, doch werden in Fragmenten keine kontextuellen Attribute unterstützt.

   ![](assets/fragment-designer.png)

1. Sobald Ihr Fragment fertig ist, klicken Sie auf **[!UICONTROL Speichern]**.

1. Klicken Sie bei Bedarf auf den Pfeil neben dem Fragmentnamen, um zum Bildschirm **[!UICONTROL Details]** zurückzukehren und das Fragment zu bearbeiten.

   ![](assets/fragment-designer-back.png)

Dieses Fragment kann nun beim Erstellen von [E-Mails](get-started-email-design.md) oder [Inhaltsvorlagen](content-templates.md) in [!DNL Journey Optimizer] verwendet werden. [Weitere Informationen](#use-fragments)

### Speichern als Fragment {#save-as-fragment}

Beim Entwerfen einer [Inhaltsvorlage](content-templates.md) oder [E-Mail](get-started-email-design.md) in einer Kampagne oder Journey können Sie einen Teil des Inhalts zur späteren Wiederverwendung als Fragment speichern. Gehen Sie dazu wie folgt vor.

1. Klicken Sie im [E-Mail-Designer](get-started-email-design.md) oben rechts im Bildschirm auf die Auslassungspunkte.

1. Wählen Sie im Dropdown-Menü die Option **[!UICONTROL Als Fragment speichern]** aus.

   ![](assets/fragment-save-as.png)

1. Der Bildschirm **[!UICONTROL Als Fragment speichern]** wird angezeigt. Hier können Sie die Elemente auswählen, die Sie in Ihr Fragment aufnehmen möchten, darunter Personalisierungsfelder und dynamische Inhalte. Beachten Sie, dass kontextuelle Attribute in Fragmenten nicht unterstützt werden.

   >[!CAUTION]
   >
   >Sie können nur nebeneinander liegende Abschnitte auswählen. Sie können keine leere Struktur und auch kein anderes Fragment auswählen.

   ![](assets/fragment-save-as-screen.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**. Füllen Sie die Fragmentdetails aus, d. h., geben Sie den Namen und (falls erforderlich) eine Beschreibung ein.

   ![](assets/fragment-details.png)

   >[!NOTE]
   >
   >Derzeit werden nur der Typ **[!UICONTROL Visuelles Fragment]** und der **E-Mail**-Kanal unterstützt.

1. Um dem Fragment benutzerdefinierte oder zentrale Datennutzungskennzeichnungen zuzuweisen, wählen Sie **[!UICONTROL Zugriff verwalten]** aus. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md).

1. Adobe Experience Platform-Tags aus dem **Tags** -Feld, um Ihre Vorlage für eine verbesserte Suche zu kategorisieren. [Weitere Informationen](../start/search-filter-categorize.md#tags)

1. Klicken Sie erneut auf **[!UICONTROL Erstellen]**. Das Fragment wird in der **[!UICONTROL Fragmentliste]** gespeichert, auf die über das dedizierte Menü in [!DNL Journey Optimizer] zugegriffen werden kann.

   Es wird zu einem eigenständigen Fragment, für das [Zugriff](#access-manage-fragments), [Bearbeitung](#edit-fragments) und [Archivierung](#archive-fragments) wie für jedes andere Element in dieser Liste möglich sind.

Dieses Fragment kann nun beim Erstellen von [E-Mails](get-started-email-design.md) oder [Inhaltsvorlagen](content-templates.md) in [!DNL Journey Optimizer] verwendet werden. [Weitere Informationen](#use-fragments)

>[!NOTE]
>
>Änderungen an diesem neuen Fragment werden nicht auf die E-Mail oder Vorlage übertragen, aus der das Fragment hervorgegangen ist. Wenn der ursprüngliche Inhalt in dieser E-Mail oder Vorlage bearbeitet wird, wird das neue Fragment ebenfalls nicht geändert.

## Verwenden von Fragmenten {#use-fragments}

Sie können ein Fragment in einer [E-Mail](get-started-email-design.md) innerhalb einer Journey oder Kampagne oder in einer [Inhaltsvorlage](content-templates.md) verwenden.

1. Öffnen Sie eine beliebige E-Mail oder Inhaltsvorlage mit dem [E-Mail-Designer](get-started-email-design.md).

1. Wählen Sie in der linken Leiste das Symbol **[!UICONTROL Fragmente]** aus.

   ![](assets/fragments-in-designer.png)

1. Die Liste aller in der aktuellen Sandbox erstellten Fragmente wird angezeigt. Sie haben folgende Möglichkeiten:

   * Suchen Sie nach einem bestimmten Fragment, indem Sie mit der Eingabe der zugehörigen Kennzeichnung beginnen.
   * Sortieren Sie Fragmente in auf- oder absteigender Reihenfolge.
   * Ändern Sie die Anzeige der Fragmente (Karten- oder Listenansicht).

1. Sie können die Liste auch aktualisieren.

   >[!NOTE]
   >
   >Wenn einige Fragmente während der Bearbeitung des Inhalts geändert oder hinzugefügt wurden, wird die Liste mit den neuesten Änderungen aktualisiert.

1. Ziehen Sie ein beliebiges Fragment aus der Liste in den Bereich, in den Sie es einfügen möchten.

   ![](assets/fragment-insert.png)

1. Wie jede andere Komponente können Sie das Fragment in Ihrem Inhalt verschieben.

1. Wählen Sie das Fragment aus, um den entsprechenden Bereich auf der rechten Seite anzuzeigen. Dort können Sie das Fragment aus Ihrem Inhalt löschen oder duplizieren. Sie können diese Aktionen auch direkt über das Kontextmenü ausführen, das über dem Fragment angezeigt wird.

   ![](assets/fragment-right-pane.png)

1. Auf der Registerkarte **[!UICONTROL Einstellungen]** haben Sie folgende Möglichkeiten:

   * Wählen Sie die Geräte aus, auf denen das Fragment angezeigt werden soll.
   * Öffnen Sie das Fragment auf einer neuen Registerkarte, um es bei Bedarf zu bearbeiten. [Weitere Informationen](#edit-fragments)
   * Erkunden Sie Verweise. [Weitere Informationen](#explore-references)

1. Sie können Ihr Fragment mit der Registerkarte **[!UICONTROL Stile]** weiter anpassen.

1. Bei Bedarf können Sie die Vererbung vom ursprünglichen Fragment unterbrechen. [Weitere Informationen](#break-inheritance)

1. Fügen Sie beliebig viele Fragmente hinzu und **[!UICONTROL speichern]** Sie Ihre Änderungen.

### Unterbrechen der Vererbung {#break-inheritance}

Wenn Sie ein Fragment bearbeiten, werden die Änderungen synchronisiert. Sie werden automatisch an alle **[!UICONTROL Entwürfe]** von Journeys/Kampagnen und Inhaltsvorlagen übertragen, die dieses Fragment enthalten.

>[!NOTE]
>
>Die Änderungen werden nicht auf die in **[!UICONTROL Live]**-Journeys oder -Kampagnen verwendeten E-Mails übertragen.

Wenn Fragmente zu einer E-Mail oder Inhaltsvorlage hinzugefügt werden, werden sie standardmäßig synchronisiert.

Sie können allerdings die Vererbung vom ursprünglichen Fragment unterbrechen. In diesem Fall wird der Inhalt des Fragments in das aktuelle Design kopiert, aber die Änderungen werden nicht mehr synchronisiert.

Gehen Sie wie folgt vor, um die Vererbung zu unterbrechen:

1. Wählen Sie das Fragment aus.

1. Klicken Sie in der kontextbezogenen Symbolleiste auf das Entsperrsymbol.

   ![](assets/fragment-break-inheritance.png)

1. Dieses Fragment wird dann zu einem eigenständigen Element, das nicht mehr mit dem ursprünglichen Fragment verknüpft ist. Bearbeiten Sie es wie jede andere Inhaltskomponente in Ihrem Inhalt. [Weitere Informationen](content-components.md)

## Anleitungsvideo {#video-fragments}

Erfahren Sie, wie Sie in [!DNL Journey Optimizer] Fragmente verwalten, erstellen und verwenden.

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

