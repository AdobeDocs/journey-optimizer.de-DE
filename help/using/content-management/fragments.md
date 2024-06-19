---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Fragmenten
description: Erfahren Sie, wie Sie mit Inhaltsfragmenten arbeiten, um Inhalte in Journey Optimizer-Kampagnen und -Journeys wiederzuverwenden
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
source-git-commit: 893f7146b358da48153b1e6bc74b8f622028df76
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 88%

---

# Erste Schritte mit Fragmenten {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="Definieren Ihrer eigenen Fragmente"
>abstract="Erstellen und verwalten Sie eigenständige Fragmente, um Ihre Inhalte über mehrere Journeys und Kampagnen hinweg wiederzuverwenden."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/content-management/fragments/create-fragments" text="Erstellen von Fragmenten"

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="Fragmente aktualisieren Kampagnen"
>abstract="Fragmente aktualisieren Kampagnen"

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="Fragmente aktualisieren Journeys"
>abstract="Fragmente aktualisieren Journeys"

Ein Fragment ist eine wiederverwendbare Komponente, die in einer oder mehreren E-Mails in [!DNL Journey Optimizer]-Kampagnen und -Journeys referenziert werden kann. Mit dieser Funktion können Sie mehrere benutzerdefinierte Inhaltsbausteine vorab erstellen, mit denen Marketing-Fachleute E-Mail-Inhalte schnell in einem verbesserten Design-Prozess zusammenstellen können.

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [In diesem Video erfahren Sie, wie Sie Fragmente verwalten, erstellen und verwenden](#video-fragments)

So nutzen Sie Fragmente am besten:

* **Erstellen eigener Fragmente**: Erstellen Sie visuelle Fragmente oder Ausdrucksfragmente, indem Sie sie von Grund auf neu erstellen oder Inhalte als Fragment speichern. [Erfahren Sie, wie Sie ein Fragment erstellen](#create-fragments).  Darüber hinaus können Sie Inhaltsfragmente mit der **Inhalts-REST API** von Journey Optimizer verwalten. Weiterführende Informationen finden Sie in der [Dokumentation zu Journey Optimizer-APIs](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}.
* **Wiederverwenden eigener Fragmente:** Diese können beliebig oft in Ihren Inhalten verwendet werden. Siehe [Hinzufügen visueller Fragmente](../email/use-visual-fragments.md) und [Nutzen von Ausdrucksfragmenten](../personalization/use-expression-fragments.md)

## Bevor Sie beginnen {#fragment-prerequisites}

Zum Erstellen, Bearbeiten und Archivieren von Fragmenten benötigen Sie die Berechtigung **[!DNL Manage library items]** im **[!DNL Content Library Manager]**-Produktprofil. [Weitere Informationen](../administration/ootb-product-profiles.md#content-library-manager)

In dieser Version gelten folgende Einschränkungen:

* **Visuelle Fragmente** sind nur für den E-Mail-Kanal verfügbar.
* **Ausdrucksfragmente** sind nicht für den In-App-Kanal verfügbar.

## Visuelle Fragmente und Ausdrucksfragmente {#visual-expression}

Es stehen zwei Arten von Fragmenten zur Verfügung:

* **Visuelle Fragmente** sind vordefinierte visuelle Bausteine, die Sie über mehrere E-Mail-Sendungen hinweg mithilfe des [E-Mail-Designers](../email/get-started-email-design.md) oder in [Inhaltsvorlagen](../email/use-email-templates.md) wiederverwenden können.
* **Ausdrucksfragmente** sind vordefinierte Ausdrücke, die über einen dedizierten Eintrag im [Personalisierungseditor](../personalization/personalization-build-expressions.md) verfügbar sind.

Alle erstellten Fragmente können über die **[!UICONTROL Content Management]** > **[!UICONTROL Fragmente]**  Menü links. [Erfahren Sie, wie Sie Fragmente verwalten](../content-management/manage-fragments.md)

![](assets/fragment-list.png)

## Anleitungsvideo {#video-fragments}

Erfahren Sie, wie Sie verwalten, verfassen und verwenden **visuelle Fragmente** in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

Erfahren Sie, wie Sie verwalten, verfassen und verwenden **Ausdrucksfragmente** in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
