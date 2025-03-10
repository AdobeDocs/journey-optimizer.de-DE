---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen eines Fragments
description: Erfahren Sie, wie Sie Fragmente erstellen, um Inhalte in Journey Optimizer-Kampagnen und -Journeys wiederzuverwenden.
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: da3ffe9c-a244-4246-b4b5-a3a1d0508676
source-git-commit: b7cd42f89ea6fb4c0359b2be6c75202d5e1ea001
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 100%

---

# Erstellen eines Fragments {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Auswählen des visuellen Typs"
>abstract="Erstellen Sie ein eigenständiges visuelles Fragment, um Ihren Inhalt in einer E-Mail innerhalb einer Journey, einer Kampagne oder in einer Inhaltsvorlage wiederzuverwenden."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/channels/email/design-email/add-content/use-visual-fragments" text="Hinzufügen visueller Fragmente zu Ihren E-Mails"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Auswählen des Ausdruckstyps"
>abstract="Erstellen Sie ein komplett neues, eigenständiges Fragment, um Ihre Inhalte für mehrere Journeys und Kampagnen wiederverwenden zu können. Bei Verwendung des Personalisierungseditors können Sie alle Ausdrucksfragmente nutzen, die in der aktuellen Sandbox erstellt wurden."


Fragmente können über das Menü **[!UICONTROL Fragmente]** links von Grund auf neu erstellt werden. Darüber hinaus können Sie beim Entwerfen von Inhalten auch einen Teil des vorhandenen Inhalts als Fragment speichern. [Weitere Informationen](#save-as-fragment)

Nach dem Speichern ist das Fragment für die Verwendung in einer Journey, Kampagne oder Vorlage verfügbar. Sie können dieses Fragment beim Erstellen von Inhalten in Journeys und Kampagnen verwenden. Siehe [Hinzufügen visueller Fragmente](../email/use-visual-fragments.md) und [Nutzen von Ausdrucksfragmenten](../personalization/use-expression-fragments.md).

Gehen Sie wie folgt vor, um ein Fragment zu erstellen:

## Definieren der Fragmenteigenschaften {#properties}

1. Greifen Sie im Menü links über **[!UICONTROL Content-Management]** > **[!UICONTROL Fragmente]** auf die Fragmentliste zu.

1. Wählen Sie **[!UICONTROL Fragment erstellen]** aus und geben Sie bei Bedarf den Namen und eine Beschreibung des Fragments ein.

   ![](assets/fragment-details.png)

1. Wählen Sie Adobe Experience Platform-Tags im Feld **[!UICONTROL Tags]** aus oder erstellen Sie welche, um Ihr Fragment für eine verbesserte Suche zu kategorisieren. [Informationen zum Arbeiten mit einheitlichen Tags](../start/search-filter-categorize.md#tags)

1. Wählen Sie den Fragmenttyp aus: **Visuelles Fragment** oder **Ausdrucksfragment**. [Weitere Informationen](../content-management/fragments.md#visual-expression)

   >[!NOTE]
   >
   >Visuelle Fragmente sind nur für den Kanal **E-Mail** verfügbar.

1. Wenn Sie ein Ausdrucksfragment erstellen, wählen Sie den Code-Typ aus, den Sie verwenden möchten: **[!UICONTROL HTML]**, **[!UICONTROL JSON]** oder **[!UICONTROL Text]**.

   ![](assets/fragment-expression-type.png)

1. Um dem Fragment benutzerdefinierte oder grundlegende Datennutzungskennzeichnungen zuzuweisen, klicken Sie oben im Bildschirm auf die Schaltfläche **[!UICONTROL Zugriff verwalten]**. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md).

1. Klicken Sie auf **[!UICONTROL Erstellen]**, um den Inhalt Ihres Fragments zu entwerfen.

## Entwerfen des Fragmentinhalts {#content}

Nachdem Sie die Eigenschaften des Fragments konfiguriert haben, wird je nach Typ des Fragments, das Sie erstellen, der E-Mail-Designer oder der Personalisierungseditor geöffnet.

* Bearbeiten Sie die Inhalte Ihrer visuellen Fragmente nach Bedarf, so wie Sie es bei jeder E-Mail innerhalb einer Journey oder einer Kampagne tun würden.  [Weitere Informationen](../email/get-started-email-design.md)

  ![](assets/fragment-designer.png)

* Verwenden Sie für Ausdrucksfragmente den Personalisierungseditor von [!DNL Journey Optimizer] mit allen Personalisierungs- und Authoring-Funktionen zum Erstellen Ihres Fragmentinhalts. [Weitere Informationen](../personalization/personalization-build-expressions.md)

  ![](assets/fragment-expression-editor.png)

Wenn Ihr Inhalt fertig ist, klicken Sie auf die Schaltfläche **[!UICONTROL Speichern]**. Das Fragment wird erstellt und mit dem Status **[!UICONTROL Entwurf]** zur Fragmentliste hinzugefügt. Sie können eine Vorschau davon anzeigen und es veröffentlichen, um es in Journeys und Kampagnen verfügbar zu machen.

## Erstellen einer Vorschau und Veröffentlichen des Fragments {#publish}

>[!NOTE]
>
>Um ein Fragment veröffentlichen zu können, müssen Sie über die Benutzerberechtigung [Fragment veröffentlichen](../administration/ootb-product-profiles.md#content-library-manager) verfügen.

Wenn Ihr Fragment zur Live-Schaltung bereit ist, können Sie es in einer Vorschau anzeigen und veröffentlichen, damit es in Ihren Journeys und Kampagnen verfügbar wird. Gehen Sie dazu wie folgt vor.

1. Kehren Sie nach dem Entwerfen des Inhalts zum Bildschirm für die Fragmenterstellung zurück oder öffnen Sie es in der Liste der Fragmente.

1. Eine Vorschau des Fragments finden Sie unter dem Feld **[!UICONTROL Tags]**. Anhand dieser können Sie überprüfen, wie es gerendert wird. Wenn Sie Änderungen vornehmen müssen, klicken Sie oben im Bildschirm auf die Schaltfläche **[!UICONTROL Bearbeiten]**, um je nach Fragmenttyp den E-Mail-Designer oder den Personalisierungseditor zu öffnen. [Weitere Informationen](manage-fragments.md#edit-fragments)

   ![](assets/fragment-preview.png)

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Veröffentlichen]**, um das Fragment zu veröffentlichen.

1. Wenn das Fragment in einer Live-Journey oder Kampagne verwendet wird, wird eine entsprechende Nachricht angezeigt. Klicken Sie auf den Link **[!UICONTROL Mehr anzeigen]**, um auf die Liste der Journeys und/oder Kampagnen zuzugreifen, auf die verwiesen wird. [Informationen zum Durchsuchen von Verweisen eines Fragments](../content-management/manage-fragments.md#explore-references)

   ![](assets/fragment-publish.png){width="70%" align="center"}

   Klicken Sie auf **[!UICONTROL Bestätigen]**, um das Fragment zu veröffentlichen und in den Live-Journeys/Kampagnen zu aktualisieren, die es verwenden.

Das Fragment ist jetzt **[!UICONTROL live]** und bei der Erstellung von Inhalten im E-Mail-Designer oder Personalisierungseditor von [!DNL Journey Optimizer] verfügbar.

* [Erfahren Sie, wie Sie visuelle Fragmente verwenden](../email/use-visual-fragments.md)
* [Erfahren Sie, wie Sie Ausdrucksfragmente verwenden](../personalization/use-expression-fragments.md)
