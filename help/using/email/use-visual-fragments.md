---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden von visuellen Fragmenten
description: Erfahren Sie, wie Sie visuelle Fragmente zur Erstellen von E-Mails in Journey Optimizer-Kampagnen und -Journeys verwenden
feature: Email Design, Fragments
topic: Content Management
role: User
level: Beginner
exl-id: 25a00f74-ed08-479c-9a5d-4185b5f3c684
source-git-commit: e6924928e03d494817a2368b33997029ca2eca1c
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 52%

---

# Hinzufügen visueller Fragmente zu Ihren E-Mails {#use-visual-fragments}

Ein Fragment ist eine wiederverwendbare Komponente, die in einer oder mehreren E-Mails in allen Journey Optimizer-Kampagnen, -Journey oder -Inhaltsvorlagen referenziert werden kann. Mit dieser Funktion können Sie mehrere benutzerdefinierte Inhaltsbausteine vorab erstellen, die von Marketing-Benutzern verwendet werden können, um E-Mail-Inhalte schnell in einem verbesserten Designprozess zusammenzustellen. [Erfahren Sie, wie Sie Fragmente erstellen und verwalten](../content-management/fragments.md).

➡️ [In diesem Video erfahren Sie, wie Sie Fragmente verwalten, erstellen und verwenden.](../content-management/fragments.md#video-fragments)

## Verwenden eines Fragments {#use-fragment}

Gehen Sie wie folgt vor, um ein Fragment in eine E-Mail zu integrieren.

>[!NOTE]
>
>Sie können bis zu 30 Fragmente in einem Versand hinzufügen. Fragmente können nur bis zu einer Ebene verschachtelt werden.


1. Öffnen Sie eine beliebige E-Mail oder Inhaltsvorlage mit dem [E-Mail-Designer](get-started-email-design.md).

1. Wählen Sie in der linken Leiste das Symbol **[!UICONTROL Fragmente]** aus.

   ![](assets/fragments-in-designer.png)

1. Es wird eine Liste aller in der aktuellen Sandbox erstellten Fragmente angezeigt. Sie werden nach Erstellungsdatum sortiert: Kürzlich hinzugefügte visuelle Fragmente werden zuerst in der Liste angezeigt. Sie haben folgende Möglichkeiten:

   * Suchen Sie nach einem bestimmten Fragment, indem Sie mit der Eingabe der zugehörigen Kennzeichnung beginnen.
   * Sortieren Sie Fragmente in auf- oder absteigender Reihenfolge.
   * Ändern Sie die Anzeige der Fragmente (Karten- oder Listenansicht).
   * Aktualisieren Sie die Liste.

   >[!NOTE]
   >
   >Wenn einige Fragmente während der Bearbeitung des Inhalts geändert oder hinzugefügt wurden, wird die Liste mit den neuesten Änderungen aktualisiert.

1. Ziehen Sie ein beliebiges Fragment aus der Liste in den Bereich, in den Sie es einfügen möchten.

   ![](assets/fragment-insert.png)

   >[!CAUTION]
   >
   >Sie können jede **Entwurf** oder **Live** zu Ihrem Inhalt hinzufügen. Sie können Ihre Journey oder Kampagne jedoch nicht aktivieren, wenn ein Fragment mit dem Status Entwurf darin verwendet wird. Bei der Journey- oder Kampagnenveröffentlichung wird ein Fehler bei Fragmententwürfen angezeigt, die Sie zur Veröffentlichung validieren müssen.

1. Wie jede andere Komponente können Sie das Fragment in Ihrem Inhalt verschieben.

1. Wählen Sie das Fragment aus, um den entsprechenden Bereich auf der rechten Seite anzuzeigen. Dort können Sie das Fragment aus Ihrem Inhalt löschen oder duplizieren. Sie können diese Aktionen auch direkt über das Kontextmenü ausführen, das über dem Fragment angezeigt wird.

   ![](assets/fragment-right-pane.png)

1. Auf der Registerkarte **[!UICONTROL Einstellungen]** haben Sie folgende Möglichkeiten:

   * Wählen Sie die Geräte aus, auf denen das Fragment angezeigt werden soll.
   * Öffnen Sie das Fragment auf einer neuen Registerkarte, um es bei Bedarf zu bearbeiten. [Weitere Informationen](../content-management/fragments.md#edit-fragments)
   * Erkunden Sie Verweise. [Weitere Informationen](../content-management/fragments.md#explore-references)

1. Sie können Ihr Fragment mit der Registerkarte **[!UICONTROL Stile]** weiter anpassen.

1. Bei Bedarf können Sie die Vererbung vom ursprünglichen Fragment unterbrechen. [Weitere Informationen](#break-inheritance)

1. Fügen Sie beliebig viele Fragmente hinzu und **[!UICONTROL speichern]** Sie Ihre Änderungen.

## Anpassen bearbeitbarer Felder {#customize-fields}

Wenn bestimmte Teile des ausgewählten Fragments bearbeitbar gemacht wurden, können Sie deren Standardwert überschreiben, nachdem Sie das Fragment zum Inhalt hinzugefügt haben. [Erfahren Sie, wie Sie Ihre Fragmente anpassen können.](../content-management/customizable-fragments.md)

Gehen Sie wie folgt vor, um bearbeitbare Felder in einem Fragment anzupassen:

1. Fügen Sie das Fragment zum Inhalt hinzu und wählen Sie es aus, um den Eigenschaftenbereich auf der rechten Seite zu öffnen.

1. Alle bearbeitbaren Felder im Fragment werden im **Einstellungen** Registerkarte unter **Fragment** Abschnitt.

   Bearbeitbare Felder werden im Vorschaufenster grün hervorgehoben, wenn sie im rechten Bereich ausgewählt wurden. So können Sie die Position der Felder in Ihrem Inhalt leicht identifizieren.

   Im folgenden Beispiel wird das Bild **source** und **Alternativtext** kann bearbeitet werden, sowie die Schaltfläche &quot;Hier klicken&quot; **URL**.

   ![](assets/fragment-editable.png)

## Unterbrechen der Vererbung {#break-inheritance}

Wenn Sie ein visuelles Fragment bearbeiten, werden die Änderungen synchronisiert. Sie werden automatisch an alle Entwürfe oder Live-Journey und Inhaltsvorlagen weitergeleitet, die dieses Fragment enthalten.

Wenn Fragmente zu einer E-Mail oder einer Inhaltsvorlage hinzugefügt werden, werden sie standardmäßig synchronisiert. Sie können allerdings die Vererbung vom ursprünglichen Fragment unterbrechen. In diesem Fall wird der Inhalt des Fragments in das aktuelle Design kopiert, die Änderungen jedoch nicht mehr synchronisiert.

Gehen Sie wie folgt vor, um die Vererbung zu unterbrechen:

1. Wählen Sie das Fragment aus.

1. Klicken Sie in der kontextbezogenen Symbolleiste auf das Entsperrsymbol.

   ![](assets/fragment-break-inheritance.png)

1. Dieses Fragment wird dann zu einem eigenständigen Element, das nicht mehr mit dem ursprünglichen Fragment verknüpft ist. Bearbeiten Sie es wie jede andere Inhaltskomponente in Ihrem Inhalt. [Weitere Informationen](content-components.md)
