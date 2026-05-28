---
title: Erstellen von Einzelseitenanwendungen
description: Weitere Informationen dazu, wie SPAs in Journey Optimizer erstellt und Änderungen an verschiedenen Ansichten vorgenommen werden können.
feature: Web Channel
topic: Content Management
role: User
level: Intermediate
exl-id: b33e4bca-d2e9-4610-9f04-008d47f686d0
TQID: https://experienceleague.adobe.com/clX0VeCEzwDOgxyFrzVaBIx-eH90KEYaHGTMzf2xvQc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c618a0dc-1818-4c6d-9916-0d92e6796f24
  - id: d056adbe-402d-4f42-9746-f3d424e598b1
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 500
ht-degree: 100%

---

# Erstellen von Einzelseitenanwendungen {#web-author-spas}

## Über Ansichten {#about-views}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications_views"
>title="Anwenden von Änderungen auf ausgewählte Ansichten"
>abstract="Die Änderungen werden nur für ausgewählte Ansichten angewendet. Mit dem Modus **Durchsuchen** können Sie Ansichten entdecken und zu ihnen navigieren. Ist die gewünschte Ansicht nicht verfügbar?"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de" text="Weitere Informationen"

**Einzelseitenanwendungen** (Single Page Applications, SPAs) können jetzt im visuellen Web-Designer-Editor erstellt werden. Auf diese Weise können Sie auswählen, auf welche **Ansichten** Sie Ihre Änderungen an der Web-Seite anwenden möchten.

[In diesem Video wird erklärt, wie Einzelseitenanwendungen erstellt werden können](#video)

Eine Ansicht kann als ganze Seite oder als Gruppe visueller Elemente auf einer Site definiert werden, z. B. als Startseite, als gesamte Produktseite oder als Rahmen für Versandvoreinstellungen auf allen Checkout-Seiten.

Ein einmaliges Setup auf Entwicklerseite ist erforderlich, um die Ansichten in der Adobe Experience Platform Web SDK-Implementierung zu definieren. Auf diese Weise können Web-Kampagnen mit Adobe Journey Optimizer auf SPAs erstellt und ausgeführt werden.

## Definieren von Ansichten in der Web SDK-Implementierung {#define-views}

XDM-Ansichten können in Adobe [!DNL Journey Optimizer] genutzt werden, damit Marketing-Fachleute Web-Personalisierungs- und Erlebniskampagnen auf SPAs über den visuellen Web-Editor ausführen können. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html?lang=de){target="_blank"}

Um auf die Ansichten in der Benutzeroberfläche von [!DNL Journey Optimizer] zugreifen und welche erstellen zu können, stellen Sie sicher, dass Sie die in [diesem Abschnitt](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html?lang=de#implement-xdm-views){target="_blank"} aufgeführten Schritte befolgen.

## Entdecken von Ansichten im Web-Designer {#discover-views}

Nachdem das Setup des SPAs in der Adobe Experience Platform Web SDK-Implementierung durchgeführt wurde, müssen Sie durch alle Ansichten Ihrer Website navigieren, auf die Sie Änderungen anwenden möchten. Gehen Sie wie folgt vor.

1. [Erstellen Sie eine Web-Journey oder Kampagne](create-web.md) und rufen Sie den [Web-Designer](web-visual-editor.md) auf.

   Die aktuelle Ansicht wird oben links angezeigt.

   ![](assets/web-designer-view-home.png)

1. Wechseln Sie in den Modus **[!UICONTROL Durchsuchen]**. [Weitere Informationen](web-visual-editor.md#browse-mode)

   ![](assets/web-designer-view-browse.png)

1. Navigieren Sie zwischen den verschiedenen Seiten der Website, um sie alle zu entdecken. Der oben angezeigte Ansichtsname ändert sich, wenn Sie durch eine andere Seite navigieren.

   ![](assets/web-designer-other-view.png)

## Anwenden von Änderungen auf andere Ansichten {#apply-modifications-views}

Nachdem eine Änderung in einer bestimmten Ansicht hinzugefügt wurde, kann sie auf andere ausgewählte Ansichten angewendet werden. Gehen Sie wie folgt vor.

>[!CAUTION]
>
>Wenn Sie Ansichten nicht mit dem Modus **[!UICONTROL Durchsuchen]** entdeckt haben, können Sie sie nicht auswählen, um Ihre Änderungen vorzunehmen. [Weitere Informationen](#discover-views)

1. Wählen Sie das Symbol **[!UICONTROL Änderungen]** aus, um den entsprechenden Bereich auf der linken Seite anzuzeigen.

   ![](assets/web-designer-view-modifications-pane.png)

1. Wählen Sie eine Änderung aus und klicken Sie auf die Schaltfläche **[!UICONTROL Mehr Aktionen]** neben der Änderung. Wählen Sie **[!UICONTROL Auf mehr Ansichten anwenden]** aus.

   ![](assets/web-designer-modifications-more-actions.png)

1. Wählen Sie die Ansichten aus, auf die die Änderungen angewendet werden sollen.

   ![](assets/web-designer-modifications-apply-to.png)

1. Klicken Sie auf **[!UICONTROL Übernehmen]**.

1. Wechseln Sie in den Modus **[!UICONTROL Durchsuchen]**, um zu überprüfen, ob die Änderungen auf die gewünschten Seiten angewendet werden.

   ![](assets/web-designer-modifications-applied-view.png)

## Anleitungsvideo{#video}

In diesem Video wird Folgendes erklärt:

* Entdecken von SPA-Ansichten im Modus **[!UICONTROL Durchsuchen]**
* Verfassen in der aktuellen Ansicht
* Anwenden von Website-Änderungen auf mehrere Ansichten oder auf alle entdeckten Ansichten
* Durchführen von Massenaktionen für Änderungen

>[!VIDEO](https://video.tv.adobe.com/v/3424536/?quality=12&learn=on)
