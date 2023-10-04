---
solution: Journey Optimizer
product: journey optimizer
title: Ausdrucksfragmente verwenden
description: Erfahren Sie, wie Sie Ausdrucksfragmente im [!DNL Journey Optimizer] Ausdruckseditor.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: Ausdruck, Editor, Bibliothek, Personalisierung
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: 623aa2ee317553eaebfb16c350a69672de2866a1
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 10%

---

# Ausdrucksfragmente nutzen {#use-expression-fragments}

Bei Verwendung des Ausdruckseditors können Sie alle Ausdrucksfragmente nutzen, die in der aktuellen Sandbox erstellt oder gespeichert wurden.

Erfahren Sie, wie Sie Fragmente in erstellen und verwalten [diesem Abschnitt](../content-management/fragments.md).

➡️ [In diesem Video erfahren Sie, wie Sie Fragmente verwalten, erstellen und verwenden.](../content-management/fragments.md#video-fragments)

## Ausdrucksfragment verwenden {#use-expression-fragment}

Gehen Sie wie folgt vor, um dem Inhalt Ausdrucksfragmente hinzuzufügen.

1. Öffnen Sie die [Ausdruckseditor](personalization-build-expressions.md) und wählen Sie die **[!UICONTROL Fragmente]** im linken Bereich.

   ![](assets/expression-fragments-pane.png)

   In der Liste werden alle Ausdrucksfragmente angezeigt, die in der aktuellen Sandbox als Fragmente erstellt oder gespeichert wurden. [Weitere Informationen](../content-management/fragments.md#create-expression-fragment)

   >[!NOTE]
   >
   >Fragmente werden nach Erstellungsdatum sortiert: Kürzlich hinzugefügte Ausdrucksfragmente werden zuerst in der Liste angezeigt.

1. Sie können die Liste auch aktualisieren.

   >[!NOTE]
   >
   >Wenn einige Fragmente während der Bearbeitung des Inhalts geändert oder hinzugefügt wurden, wird die Liste mit den neuesten Änderungen aktualisiert.

1. Klicken Sie auf das Symbol + neben einem Ausdrucksfragment, um die entsprechende Fragment-ID in den Editor einzufügen.

   ![](assets/expression-fragment-add.png)

   Wenn Sie das entsprechende Ausdrucksfragment öffnen und [bearbeiten](../content-management/fragments.md#edit-fragments) über die -Benutzeroberfläche werden die Änderungen synchronisiert. Sie werden automatisch an alle **[!UICONTROL Entwurf]** Journey/Kampagnen, die diese Fragment-ID enthalten.

   >[!NOTE]
   >
   >Die Änderungen werden nicht auf Inhalte übertragen, die in **[!UICONTROL Live]** Journey oder Kampagnen.

1. Klicken Sie auf **[!UICONTROL Mehr Aktionen]** neben einem Fragment.

1. Wählen Sie aus dem sich öffnenden Kontextmenü die Option **[!UICONTROL Fragment anzeigen]** , um weitere Informationen zu diesem Fragment zu erhalten. Die **[!UICONTROL Fragment-ID]** wird ebenfalls angezeigt und kann von hier aus kopiert werden.

   ![](assets/expression-fragment-view.png)

1. Sie können das Ausdrucksfragment in einem anderen Fenster öffnen, um seinen Inhalt und seine Eigenschaften zu bearbeiten - entweder mithilfe der **[!UICONTROL Fragment öffnen]** -Option im Kontextmenü oder im Kontextmenü **[!UICONTROL Fragmentinformationen]** -Bereich. [Informationen zum Bearbeiten eines Fragments](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. Anschließend können Sie Ihren Inhalt wie gewohnt anpassen und validieren, indem Sie alle Personalisierungs- und Authoring-Funktionen der [Ausdruckseditor](personalization-build-expressions.md).

>[!NOTE]
>
>Wenn Sie ein Ausdrucksfragment erstellen, das mehrere Zeilenumbrüche enthält, und dieses in [SMS](../sms/create-sms.md#sms-content) oder [push](../push/design-push.md) -Inhalt, bleiben die Zeilenumbrüche erhalten. Testen Sie daher Ihre [SMS](../sms/send-sms.md) oder [push](../push/send-push.md) vor dem Versand.

## Unterbrechen der Vererbung {#break-inheritance}

Beim Hinzufügen einer Fragment-ID zum Ausdruckseditor werden die Änderungen am ursprünglichen Ausdrucksfragment synchronisiert.

Sie können jedoch auch den Inhalt eines Ausdrucksfragments in den Editor einfügen. Wählen Sie im Kontextmenü die Option **[!UICONTROL Fragment einfügen]** um diesen Inhalt einzufügen.

![](assets/expression-fragment-paste.png)

In diesem Fall ist die Vererbung aus dem ursprünglichen Fragment fehlerhaft. Der Inhalt des Fragments wird in den Editor kopiert und die Änderungen werden nicht mehr synchronisiert.

Es wird zu einem eigenständigen Element, das nicht mehr mit dem ursprünglichen Fragment verknüpft ist. Sie können es wie jedes andere Element im Code bearbeiten.

