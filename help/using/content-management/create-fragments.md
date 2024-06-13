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
source-git-commit: f47160f40abd9427cb9b9c793ee0ab402bf9f65b
workflow-type: ht
source-wordcount: '401'
ht-degree: 100%

---

# Erstellen eines Fragments von Grund auf {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Auswählen des visuellen Typs"
>abstract="Erstellen Sie ein eigenständiges visuelles Fragment, um Ihren Inhalt in einer E-Mail innerhalb einer Journey, einer Kampagne oder in einer Inhaltsvorlage wiederzuverwenden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments.html?lang=de" text="Hinzufügen visueller Fragmente zu Ihren E-Mails"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Auswählen des Ausdruckstyps"
>abstract="Erstellen Sie ein komplett neues, eigenständiges Fragment, um Ihre Inhalte für mehrere Journeys und Kampagnen wiederverwenden zu können. Bei Verwendung des Personalisierungseditors können Sie alle Ausdrucksfragmente nutzen, die in der aktuellen Sandbox erstellt wurden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html?lang=de" text="Nutzen von Ausdrucksfragmenten"

Fragmente werden im Menü **[!UICONTROL Fragmente]** auf der linken Seite erstellt. Darüber hinaus können Sie beim Entwerfen von Inhalten auch einen Teil des vorhandenen Inhalts als Fragment speichern. [Weitere Informationen](#save-as-fragment)

Nach dem Speichern ist das Fragment für die Verwendung in einer Journey, Kampagne oder Vorlage verfügbar. Sie können dieses Fragment nun beim Erstellen von Inhalten in [!DNL Journey Optimizer] verwenden. Siehe [Hinzufügen visueller Fragmente](../email/use-visual-fragments.md) und [Nutzen von Ausdrucksfragmenten](../personalization/use-expression-fragments.md)

Gehen Sie wie folgt vor, um ein Fragment komplett neu zu erstellen.

1. [](#access-manage-fragments)Greifen Sie im Menü links über **[!UICONTROL Content-Management]** > **[!UICONTROL Fragmente]** auf die Fragmentliste zu.

1. Wählen Sie **[!UICONTROL Fragment erstellen]** aus.

1. Füllen Sie die Fragmentdetails aus, d. h., geben Sie den Namen und (falls erforderlich) eine Beschreibung ein.

   ![](assets/fragment-details.png)

1. Wählen oder erstellen Sie Adobe Experience Platform-Tags im Feld **[!UICONTROL Tags]** aus, um Ihr Fragment für eine verbesserte Suche zu kategorisieren. [Weitere Informationen](../start/search-filter-categorize.md#tags)

1. Wählen Sie den Fragmenttyp aus: [Visuelles Fragment](#create-visual-fragment) oder [Ausdrucksfragment](#create-expression-fragment).

   >[!NOTE]
   >
   >Derzeit wird für visuelle Fragmente nur der Kanal **E-Mail** unterstützt.

1. Wenn Sie ein Ausdrucksfragment erstellen, wählen Sie den Code-Typ aus, den Sie verwenden möchten: **[!UICONTROL HTML]**, **[!UICONTROL JSON]** oder **[!UICONTROL Text]**.

   ![](assets/fragment-expression-type.png)

1. Um dem Fragment benutzerdefinierte oder zentrale Datennutzungskennzeichnungen zuzuweisen, wählen Sie **[!UICONTROL Zugriff verwalten]** aus. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md).

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

1. Je nach Typ des Fragments, das Sie erstellen, wird der [E-Mail-Designer](../email/get-started-email-design.md) oder der Personalisierungseditor geöffnet.

   * Bearbeiten Sie die Inhalte Ihrer visuellen Fragmente nach Bedarf, so wie Sie es bei jeder E-Mail innerhalb einer Journey oder einer Kampagne tun würden.

     >[!NOTE]
     >
     >Sie können Personalisierungsfelder und dynamische Inhalte hinzufügen, doch werden in Fragmenten keine kontextuellen Attribute unterstützt.

     ![](assets/fragment-designer.png)

   * Verwenden Sie für Ausdrucksfragmente den Personalisierungseditor von [!DNL Journey Optimizer] mit allen Personalisierungs- und Authoring-Funktionen zum Erstellen Ihres Fragmentinhalts. [Weitere Informationen](../personalization/personalization-build-expressions.md)

     ![](assets/fragment-expression-editor.png)

1. Sobald Ihr Fragment fertig ist, klicken Sie auf **[!UICONTROL Speichern]**.

Das Fragment wird zur [Fragmentliste](#access-manage-fragments) hinzugefügt. Es kann jetzt zur Erstellung von Inhalten im E-Mail-Designer oder Personalisierungseditor von [!DNL Journey Optimizer] verwendet werden.

* [Erfahren Sie, wie Sie visuelle Fragmente verwenden](../email/use-visual-fragments.md)
* [Erfahren Sie, wie Sie Ausdrucksfragmente verwenden](../personalization/use-expression-fragments.md)
