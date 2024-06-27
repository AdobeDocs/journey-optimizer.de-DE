---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden von Ausdrucksfragmenten
description: Erfahren Sie, wie Sie im Personalisierungseditor von  [!DNL Journey Optimizer]  Ausdrucksfragmente verwenden können.
feature: Personalization, Fragments
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: Ausdruck, Editor, Bibliothek, Personalisierung
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: e6924928e03d494817a2368b33997029ca2eca1c
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 56%

---

# Nutzen von Ausdrucksfragmenten {#use-expression-fragments}

Bei Verwendung des **Personalisierungseditors** können Sie alle Ausdrucksfragmente nutzen, die in der aktuellen Sandbox erstellt oder gespeichert wurden.

Ein Fragment ist eine wiederverwendbare Komponente, auf die über mehrere [!DNL Journey Optimizer] Kampagnen und Journey. Mit dieser Funktion können Sie mehrere benutzerdefinierte Inhaltsbausteine vorab erstellen, die von Marketing-Benutzern verwendet werden können, um Inhalte schnell in einem verbesserten Designprozess zusammenzustellen. [Erfahren Sie, wie Sie Fragmente erstellen und verwalten](../content-management/fragments.md).

➡️ [In diesem Video erfahren Sie, wie Sie Fragmente verwalten, erstellen und verwenden.](../content-management/fragments.md#video-fragments)

## Verwenden eines Ausdrucksfragments {#use-expression-fragment}

Um Ausdrucksfragmente zu Ihren Inhalten hinzuzufügen, gehen Sie folgendermaßen vor.

>[!NOTE]
>
>Sie können bis zu 30 Fragmente in einem Versand hinzufügen. Fragmente können nur bis zu einer Ebene verschachtelt werden.

1. Öffnen Sie den [Personalisierungseditor](personalization-build-expressions.md) und wählen Sie die Schaltfläche **[!UICONTROL Fragmente]** im linken Bereich aus.

   In der Liste werden alle Ausdrucksfragmente angezeigt, die in der aktuellen Sandbox als Fragmente erstellt oder gespeichert wurden. Sie werden nach Erstellungsdatum sortiert: Kürzlich hinzugefügte Ausdrucksfragmente werden zuerst in der Liste angezeigt. [Weitere Informationen](../content-management/fragments.md#create-expression-fragment)

   ![](assets/expression-fragments-pane.png)

   Sie können diese Liste auch aktualisieren.

   >[!NOTE]
   >
   >Wenn einige Fragmente während der Bearbeitung des Inhalts geändert oder hinzugefügt wurden, wird die Liste mit den neuesten Änderungen aktualisiert.

1. Klicken Sie auf das Symbol „+“ neben einem Ausdrucksfragment, um die entsprechende Fragment-ID in den Editor einzufügen.

   ![](assets/expression-fragment-add.png)

   >[!CAUTION]
   >
   >Sie können jede **Entwurf** oder **Live** zu Ihrem Inhalt hinzufügen. Sie können Ihre Journey oder Kampagne jedoch nicht aktivieren, wenn ein Fragment mit dem Status Entwurf darin verwendet wird. Bei der Journey- oder Kampagnenveröffentlichung wird ein Fehler bei Fragmententwürfen angezeigt, die Sie zur Veröffentlichung validieren müssen.

1. Wenn die Fragment-ID hinzugefügt worden ist, werden die Änderungen synchronisiert, sobald Sie das entsprechende Ausdrucksfragment öffnen und [bearbeiten](../content-management/fragments.md#edit-fragments). Sie werden automatisch an alle Entwürfe oder Live-Journey/Kampagnen weitergeleitet, die diese Fragment-ID enthalten.

1. Klicken Sie auf **[!UICONTROL Mehr Aktionen]** neben einem Fragment. Wählen Sie aus dem sich öffnenden Kontextmenü die Option **[!UICONTROL Fragment anzeigen]** aus, um weitere Informationen zu diesem Fragment zu erhalten. Die **[!UICONTROL Fragment-ID]** wird ebenfalls angezeigt und kann von hier aus kopiert werden.

   ![](assets/expression-fragment-view.png)

1. Sie können das Ausdrucksfragment in einem anderen Fenster öffnen, um seinen Inhalt und seine Eigenschaften zu bearbeiten – entweder im Kontextmenü mithilfe der Option **[!UICONTROL Fragment öffnen]** oder im Bereich **[!UICONTROL Fragmentinformationen]**. [Erfahren Sie, wie ein Fragment bearbeitet wird](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. Anschließend können Sie Ihre Inhalte wie gewohnt mit allen Personalisierungs- und Authoring-Funktionen des [Personalisierungseditors](personalization-build-expressions.md) anpassen und validieren.

>[!NOTE]
>
>Wenn Sie ein Ausdrucksfragment erstellen, das mehrere Zeilenumbrüche enthält, und dieses in [SMS](../sms/create-sms.md#sms-content)- oder [Push](../push/design-push.md)-Inhalten verwenden, bleiben die Zeilenumbrüche erhalten. Testen Sie daher Ihre [SMS](../sms/send-sms.md)- oder [Push](../push/send-push.md)-Nachricht vor dem Versand.

## Anpassen bearbeitbarer Felder {#customize-fields}

Wenn bestimmte Teile eines Ausdrucksfragments mithilfe von Variablen bearbeitbar gemacht wurden, können Sie deren Standardwerte mithilfe einer bestimmten Syntax überschreiben. [Erfahren Sie, wie Sie Ihre Fragmente anpassen können.](../content-management/customizable-fragments.md)

Gehen Sie wie folgt vor, um die Felder anzupassen:

1. Fügen Sie das Fragment aus dem **Fragmente** Menü.

1. Verwenden Sie die `<fieldId>="<value>"` -Code am Ende der Syntax, um den Standardwert der -Variablen zu überschreiben.

   Im folgenden Beispiel wird der Wert einer Variablen überschrieben, deren ID &quot;sports&quot;mit dem Wert &quot;yoga&quot;lautet. Dadurch wird &quot;Yoga&quot;in Ihrem Fragmentinhalt überall dort angezeigt, wo auf die Variable &quot;sport&quot;verwiesen wird.

   ![](../content-management/assets/fragment-expression-use.png)

Ein Beispiel für das Hinzufügen von bearbeitbaren Feldern zu Ausdrucksfragmenten und deren Außerkraftsetzen beim Erstellen einer E-Mail finden Sie unter [diesem Abschnitt](../content-management/customizable-fragments.md#example).

## Unterbrechen der Vererbung {#break-inheritance}

Beim Hinzufügen einer Fragment-ID zum Personalisierungseditor werden die Änderungen am ursprünglichen Ausdrucksfragment synchronisiert.

Sie können jedoch auch den Inhalt eines Ausdrucksfragments in den Editor einfügen. Wählen Sie im Kontextmenü die Option **[!UICONTROL Fragment einfügen]** aus, um diesen Inhalt einzufügen.

![](assets/expression-fragment-paste.png)

In diesem Fall ist die Vererbung aus dem ursprünglichen Fragment fehlerhaft. Der Inhalt des Fragments wird in den Editor kopiert und die Änderungen werden nicht mehr synchronisiert.

Es wird zu einem eigenständigen Element, das nicht mehr mit dem ursprünglichen Fragment verknüpft ist. Sie können es wie jedes andere Element in Ihrem Code bearbeiten.

