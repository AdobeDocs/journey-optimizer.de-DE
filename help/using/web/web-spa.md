---
title: Einzelseitenanwendungen erstellen
description: Erfahren Sie, wie Sie in Journey Optimizer SPA erstellen und Änderungen an verschiedenen Ansichten vornehmen können.
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: b33e4bca-d2e9-4610-9f04-008d47f686d0
source-git-commit: a2d67bbcf9b90c427ea3f755d80e465a3d7b10ec
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 8%

---

# Einzelseitenanwendungen erstellen {#web-author-spas}

## Über Ansichten {#about-views}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications_views"
>title="Anwenden von Änderungen auf ausgewählte Ansichten"
>abstract="Die Änderungen werden nur für ausgewählte Ansichten angewendet. Ansichten können mithilfe des **Durchsuchen** und navigieren Sie zu ihnen. Kann die Ansicht, die Sie suchen, nicht finden?"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de" text="Weitere Informationen"

**Einzelseitenanwendungen** (SPA) kann jetzt im visuellen Editor für Webdesigner erstellt werden. Auf diese Weise können Sie festlegen, welche **views** Sie möchten Ihre Webseitenänderungen auf anwenden.

[In diesem Video erfahren Sie, wie Sie Einzelseitenanwendungen erstellen.](#video)

Eine Ansicht kann als ganze Site oder eine Gruppe visueller Elemente auf einer Site definiert werden, z. B. als Startseite, die gesamte Produktseite oder den Rahmen für Versandvoreinstellungen auf allen Checkout-Seiten.

Zum Definieren der Ansichten in der Adobe Experience Platform Web SDK-Implementierung ist ein einmaliges Entwicklersetup erforderlich. Auf diese Weise können Sie Adobe Journey Optimizer-Webkampagnen auf SPA erstellen und ausführen.

## Ansichten in der Web SDK-Implementierung definieren {#define-views}

XDM-Ansichten können in Adobe genutzt werden [!DNL Journey Optimizer] , damit Marketing-Experten Web-Personalisierungs- und Erlebniskampagnen auf SPA über den Web-Visual-Editor ausführen können. [Weitere Informationen](web-spa-implementation.md)

Um auf Ansichten in der [!DNL Journey Optimizer] müssen Sie die in [diesem Abschnitt](web-spa-implementation.md#implement-xdm-views).

## Ermitteln von Ansichten im Webdesigner {#discover-views}

Nachdem SPA Einrichtung in der Adobe Experience Platform Web SDK-Implementierung durchgeführt wurde, müssen Sie durch alle Ansichten Ihrer Website navigieren, auf die Sie Änderungen anwenden möchten. Führen Sie dazu folgende Schritte durch.

1. [Webkampagne erstellen](create-web.md) und greifen Sie auf [Webdesigner](edit-web-content.md).

   Die Ansicht, in der Sie sich derzeit befinden, wird oben links angezeigt.

   ![](assets/web-designer-view-home.png)

1. Tauschen Sie **[!UICONTROL Durchsuchen]** -Modus. [Weitere Informationen](../web/edit-web-content.md#browse-mode)

   ![](assets/web-designer-view-browse.png)

1. Navigieren Sie zwischen den verschiedenen Seiten der Website, um sie alle zu entdecken. Der oben angezeigte Ansichtsname ändert sich, wenn Sie durch eine andere Seite navigieren.

   ![](assets/web-designer-other-view.png)

## Anwenden von Änderungen auf andere Ansichten {#apply-modifications-views}

Nachdem Sie eine Änderung hinzugefügt haben, während Sie sich in einer bestimmten Ansicht befinden, können Sie sie auf andere ausgewählte Ansichten anwenden. Führen Sie dazu folgende Schritte durch.

>[!CAUTION]
>
>Wenn Sie keine Ansichten mithilfe der **[!UICONTROL Durchsuchen]** -Modus können Sie sie nicht zur Anwendung Ihrer Änderungen auswählen. [Weitere Informationen](#discover-views)

1. Wählen Sie das Symbol **[!UICONTROL Änderungen]** aus, um den entsprechenden Bereich auf der linken Seite anzuzeigen.

   ![](assets/web-designer-view-modifications-pane.png)

1. Wählen Sie eine Änderung aus und klicken Sie auf **[!UICONTROL Mehr Aktionen]** neben der Schaltfläche klicken. Auswählen **[!UICONTROL Anwenden auf weitere Ansichten]**.

   ![](assets/web-designer-modifications-more-actions.png)

1. Wählen Sie die Ansichten aus, auf die Sie Ihre Änderungen anwenden möchten.

   ![](assets/web-designer-modifications-apply-to.png)

1. Klicken Sie auf **[!UICONTROL Übernehmen]**.

1. Tauschen Sie **[!UICONTROL Durchsuchen]** -Modus, um zu überprüfen, ob die Änderungen auf die gewünschten Seiten angewendet werden.

   ![](assets/web-designer-modifications-applied-view.png)

## Anleitungsvideo{#video}

In diesem Video wird Folgendes erläutert:

* SPA mit **[!UICONTROL Durchsuchen]** mode
* Bearbeiten der aktuellen Ansicht
* Anwenden von Website-Änderungen auf mehrere Ansichten oder auf alle erkannten Ansichten
* Massenaktionen für Änderungen durchführen

>[!VIDEO](https://video.tv.adobe.com/v/3424536/?quality=12&learn=on)
