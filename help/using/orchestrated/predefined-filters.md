---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit vordefinierten Filtern
description: Erfahren Sie, wie Sie vordefinierte Filter in orchestrierten Kampagnen speichern, anwenden und verwalten können
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 11%

---


# Arbeiten mit vordefinierten Filtern {#predefined-filters}

Vordefinierte Filter sind gespeicherte Regeln, die Sie im Regel-Builder wiederverwenden können. Verwenden Sie sie, um zu vermeiden, dass gängige Abfragen neu erstellt werden, und um die Targeting-Logik in orchestrierten Kampagnen zu standardisieren.

Sie können vordefinierte Filter als Favoriten markieren, für andere Benutzer freigeben und Parameter hinzufügen, damit ausgewählte Felder bearbeitet werden können, wenn der Filter angewendet wird.

## Erstellen eines vordefinierten Filters {#create}

Speichern Sie einen benutzerdefinierten Filter aus dem Regel-Builder, um ihn für die zukünftige Verwendung verfügbar zu machen. Führen Sie folgende Schritte aus:

1. Öffnen Sie den Regel-Builder und definieren Sie Ihre Filterbedingungen. [Weitere Informationen zur Erstellung einer Regel](../orchestrated/build-query.md)

1. Optional: Damit bestimmte Felder bei Verwendung des Filters bearbeitet werden können, wählen Sie das Feld aus und schalten Sie **[!UICONTROL Als Parameter festlegen]** um. Wenn Sie den Filter anwenden, können nur diese Felder bearbeitet werden.

   ![](assets/predefined-filter-parameter-enable.png)

1. Klicken Sie zum Speichern des Filters auf **[!UICONTROL Filter auswählen oder]**) und wählen Sie **[!UICONTROL Als Filter speichern]**.

   ![](assets/predefined-filter-save.png)

1. Geben Sie einen Titel und eine Beschreibung für den Filter ein und klicken Sie dann auf **[!UICONTROL Speichern]**.

   * Um den Filter als Favoriten zu speichern, aktivieren Sie die Option **[!UICONTROL Bevorzugte Filter]**. Weiterführende Informationen finden Sie in [diesem Abschnitt](#fav-filter).
   * Um den Filter für andere Benutzer zugänglich zu machen, aktivieren Sie die Option **[!UICONTROL Freigegebener Filter]**. Weiterführende Informationen finden Sie in [diesem Abschnitt](#share-filter).

   ![](assets/predefined-filter-save-name.png)

Ihr benutzerdefinierter Filter ist jetzt in der Liste **Vordefinierte Filter** verfügbar.

## Verwenden eines vordefinierten Filters in einer Regel {#apply}

Vordefinierte Filter sind beim Definieren von Abfragen im Regel-Builder verfügbar.

1. Klicken **[!UICONTROL Bereich &quot;]**&quot; auf **[!UICONTROL Filter auswählen oder speichern]**.

1. Wählen Sie **[!UICONTROL Vordefinierten Filter]** und wählen Sie einen Filter aus. Sie können einen vordefinierten Filter auch direkt aus der Liste auswählen, wenn er zu den Favoriten hinzugefügt wurde.

   ![](assets/predefined-filter-apply.png)

   >[!IMPORTANT]
   >
   >Wenn Sie einen vordefinierten Filter auswählen, wird die auf der Arbeitsfläche erstellte Regel durch den ausgewählten Filter ersetzt.

1. Der Filter wird auf der Arbeitsfläche geöffnet. Fahren Sie mit der Bearbeitung der Bedingung nach Bedarf fort.

   ![](assets/predefined-filter-added.png)

   Wenn der ausgewählte Filter Parameter enthält, können nur die als Parameter markierten Felder bearbeitet werden. Sie werden im Bereich neben dem Bereich **[!UICONTROL Regeleigenschaften]** angezeigt.

   ![](assets/predefined-filter-parameter-apply.png)

   Um den vordefinierten Filter selbst zu bearbeiten, klicken Sie auf die Schaltfläche ![Auslassungspunkte](assets/do-not-localize/rule-builder-icon-more.svg) und wählen Sie **[!UICONTROL Zur Regelbearbeitung wechseln]**. Alle Änderungen gelten nur für die aktuelle Regel, die Sie erstellen. Der vordefinierte Filter wird nicht geändert.

   ![](assets/predefined-filter-parameter-edit.png)

## Filter als Favorit speichern {#fav-filter}

Aktivieren Sie beim Erstellen eines vordefinierten Filters die Option **[!UICONTROL Favoritenfilter]**, um diesen vordefinierten Filter in Ihren Favoriten anzuzeigen.

Wenn ein Filter als Favorit gespeichert wird, wird er im Abschnitt **[!UICONTROL Favoritenfilter]** der Filterliste angezeigt, wie unten dargestellt:

![Abschnitt „Bevorzugte Filter“](assets/predefined-filter-favorites.png)

## Freigeben eines vordefinierten Filters {#share-filter}

Standardmäßig sind vordefinierte Filter, die Sie erstellen, privat und nur für Sie sichtbar. Um anderen Benutzenden in Ihrer Organisation Zugriff auf einen Filter zu gewähren, aktivieren Sie die Option **[!UICONTROL Freigegebener Filter]**.

![Option „Freigegebener Filter“](assets/predefined-filter-shared.png)

Freigegebene Filter werden in der vordefinierten Filterliste für alle Benutzer angezeigt, sodass sie diese Filter in ihren eigenen Regeln verwenden können.

## Vordefinierte Filter verwalten {#manage-predefined-filter}

Gehen Sie wie folgt vor, um vordefinierte Filter zu bearbeiten oder zu löschen:

1. Öffnen Sie die vordefinierte Filterliste mithilfe der Schaltfläche **[!UICONTROL Filter auswählen oder speichern]** im Regelaufbau.

1. Klicken Sie auf ![ Schaltfläche mit ](assets/do-not-localize/rule-builder-icon-more.svg) Auslassungspunkten neben einem Filter und wählen Sie die gewünschte Aktion aus.

![](assets/predefined-filters-edit.png)
