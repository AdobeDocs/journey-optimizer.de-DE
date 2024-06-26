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
source-git-commit: ffeaa49cde2871b28c85598469e62f4d9acbf060
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 33%

---

# Erstellen eines Fragments {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Auswählen des visuellen Typs"
>abstract="Erstellen Sie ein eigenständiges visuelles Fragment, um Ihren Inhalt in einer E-Mail innerhalb einer Journey, einer Kampagne oder in einer Inhaltsvorlage wiederzuverwenden."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments" text="Hinzufügen visueller Fragmente zu Ihren E-Mails"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Auswählen des Ausdruckstyps"
>abstract="Erstellen Sie ein komplett neues, eigenständiges Fragment, um Ihre Inhalte für mehrere Journeys und Kampagnen wiederverwenden zu können. Bei Verwendung des Personalisierungseditors können Sie alle Ausdrucksfragmente nutzen, die in der aktuellen Sandbox erstellt wurden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html?lang=de" text="Nutzen von Ausdrucksfragmenten"

Fragmente können von Grund auf aus dem **[!UICONTROL Fragmente]** Menü links. Darüber hinaus können Sie beim Entwerfen von Inhalten auch einen Teil des vorhandenen Inhalts als Fragment speichern. [Weitere Informationen](#save-as-fragment)

Nach dem Speichern ist das Fragment für die Verwendung in einer Journey, Kampagne oder Vorlage verfügbar. Sie können dieses Fragment beim Erstellen von Inhalten in Journey und Kampagnen verwenden. Siehe [Hinzufügen visueller Fragmente](../email/use-visual-fragments.md) und [Nutzen von Ausdrucksfragmenten](../personalization/use-expression-fragments.md)

Gehen Sie wie folgt vor, um ein Fragment zu erstellen.

## Eigenschaften des Fragments definieren {#properties}

1. Greifen Sie im Menü links über **[!UICONTROL Content-Management]** > **[!UICONTROL Fragmente]** auf die Fragmentliste zu.

1. Auswählen **[!UICONTROL Fragment erstellen]** und geben Sie bei Bedarf den Fragmentnamen und die Beschreibung ein.

   ![](assets/fragment-details.png)

1. Wählen oder erstellen Sie Adobe Experience Platform-Tags im Feld **[!UICONTROL Tags]** aus, um Ihr Fragment für eine verbesserte Suche zu kategorisieren. [Erfahren Sie, wie Sie mit Unified Tags arbeiten.](../start/search-filter-categorize.md#tags)

1. Wählen Sie den Fragmenttyp aus: **Visual Fragment** oder **Ausdrucksfragment**. [Weitere Informationen zu visuellen und Ausdrucksfragmenten](../content-management/fragments.md#visual-expression)

   >[!NOTE]
   >
   >Derzeit sind visuelle Fragmente für die **Email** nur -Kanal.

1. Wenn Sie ein Ausdrucksfragment erstellen, wählen Sie den Code-Typ aus, den Sie verwenden möchten: **[!UICONTROL HTML]**, **[!UICONTROL JSON]** oder **[!UICONTROL Text]**.

   ![](assets/fragment-expression-type.png)

1. Um dem Fragment benutzerdefinierte oder Core-Datennutzungsbezeichnungen zuzuweisen, klicken Sie auf das **[!UICONTROL Zugriff verwalten]** im oberen Bereich des Bildschirms. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md).

1. Klicks **[!UICONTROL Erstellen]** , um den Inhalt des Fragments zu erstellen.

## Fragmentinhalt erstellen {#content}

Nachdem Sie die Eigenschaften des Fragments konfiguriert haben, wird je nach Typ des Fragments, das Sie erstellen, die E-Mail-Designer oder der Personalisierungseditor geöffnet.

* Bearbeiten Sie den Inhalt für visuelle Fragmente nach Bedarf auf die gleiche Weise wie für jede E-Mail innerhalb einer Journey oder Kampagne. [Weitere Informationen](../email/get-started-email-design.md)

  ![](assets/fragment-designer.png)

* Verwenden Sie für Ausdrucksfragmente den Personalisierungseditor von [!DNL Journey Optimizer] mit allen Personalisierungs- und Authoring-Funktionen zum Erstellen Ihres Fragmentinhalts. [Weitere Informationen](../personalization/personalization-build-expressions.md)

  ![](assets/fragment-expression-editor.png)

Wenn Ihr Inhalt fertig ist, klicken Sie auf die Schaltfläche **Speichern** Schaltfläche. Das Fragment wird erstellt und mit der **Entwurf** -Status. Sie können eine Vorschau davon anzeigen und sie veröffentlichen, um sie in Journey und Kampagnen verfügbar zu machen.

>[!NOTE]
>
>Die Veröffentlichung von Fragmenten wird im Laufe von mehreren Tagen nach der Journey Optimizer-Version vom Juni schrittweise eingeführt. Einige Benutzer haben zwar sofort Zugriff, bei anderen kann es aber zu einer Verzögerung kommen, bevor sie in ihren Umgebungen verfügbar werden. Wenn diese Verbesserung noch nicht in Ihrer Umgebung verfügbar ist, beachten Sie bitte, dass Fragmente nicht zur Verwendung in Journey und Kampagnen veröffentlicht werden müssen.

## Vorschau erstellen und Fragment veröffentlichen {#publish}

>[!NOTE]
>
>Um ein Fragment zu veröffentlichen, muss die **Publish Fragment** verwandte Berechtigung. [Weitere Informationen zu Berechtigungen](../administration/ootb-permissions.md)

Wenn Ihr Fragment für die Live-Schaltung bereit ist, können Sie es in der Vorschau anzeigen und veröffentlichen, um es in Ihren Journey und Kampagnen verfügbar zu machen. Gehen Sie dazu wie folgt vor:

1. Kehren Sie nach dem Erstellen des Inhalts zum Bildschirm zur Fragmenterstellung zurück oder öffnen Sie ihn in der Liste der Fragmente.

1. Eine Vorschau des Fragments finden Sie unter **Tags** -Feld, um dessen Rendering zu überprüfen. Wenn Sie Änderungen vornehmen müssen, klicken Sie auf die Schaltfläche **Bearbeiten** im oberen Bereich des Bildschirms, um die E-Mail-Designer oder den Personalisierungseditor je nach Fragmenttyp zu öffnen.

   ![](assets/fragment-preview.png)

1. Klicken Sie auf **Publish** in der oberen rechten Ecke, um das Fragment zu veröffentlichen.

   Wenn das Fragment in einer Live-Journey oder Kampagne verwendet wird, wird eine entsprechende Nachricht angezeigt. Klicken Sie auf **Weitere Informationen** -Link, um auf die Liste der Journey und/oder Kampagnen zuzugreifen, auf die verwiesen wird. [Erfahren Sie, wie Sie die Verweise eines Fragments durchsuchen](../content-management/manage-fragments.md#explore-references)

   Klicks **Bestätigen** , um das Fragment zu veröffentlichen und in den Live-Journey/-Kampagnen zu aktualisieren, die es verwenden.

   ![](assets/fragment-publish.png){width="70%" align="center"}

Das Fragment ist jetzt **Live** und ist verfügbar, wenn Sie Inhalte innerhalb der [!DNL Journey Optimizer] Email Designer oder Personalisierungs-Editor:

* [Erfahren Sie, wie Sie visuelle Fragmente verwenden](../email/use-visual-fragments.md)
* [Erfahren Sie, wie Sie Ausdrucksfragmente verwenden](../personalization/use-expression-fragments.md)
