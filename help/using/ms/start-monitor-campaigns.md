---
solution: Journey Optimizer
product: journey optimizer
title: Starten und Überwachen orchestrierter Kampagnen mit Adobe Journey Optimizer
description: Erfahren Sie, wie Sie mit Adobe Journey Optimizer koordinierte Kampagnen starten und überwachen
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 47%

---

# Starten und Überwachen von orchestrierten Kampagnen {#start-monitor}

<!--
<audio controls><source src="../ms/assets/do-not-localize/sound.mp3" type="audio/mpeg">Your browser does not support the audio element.</audio> -->

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Veröffentlichen einer orchestrierten Kampagne"
>abstract="Um Ihre Kampagne zu starten, müssen Sie sie veröffentlichen. Stellen Sie sicher, dass alle Warnungen vor der Veröffentlichung gelöscht wurden."


Nachdem Sie Ihre koordinierten und entworfenen Aufgaben auf der Arbeitsfläche erstellt haben, können Sie sie veröffentlichen und ihre Ausführung überwachen.

## Starten einer orchestrierten Kampagne {#start}

Um eine orchestrierte Kampagne zu starten, gehen Sie zur Registerkarte **[!UICONTROL Mehrstufig]** des Menüs **[!UICONTROL Kampagne]** und wählen Sie die zu startende Kampagne aus und klicken Sie dann auf die Schaltfläche **[!UICONTROL Starten]** in der oberen rechten Ecke der Arbeitsfläche.

Sobald die orchestrierte Kampagne ausgeführt wird, wird jede Aktivität auf der Arbeitsfläche in sequenzieller Reihenfolge ausgeführt, bis das Ende der orchestrierten Kampagne erreicht ist.

Anhand eines visuellen Flusses können Sie den Fortschritt von Zielgruppenprofilen in Echtzeit verfolgen. Auf diese Weise können Sie den Status jeder Aktivität und die Anzahl der Profile, die zwischen ihnen wechseln, schnell identifizieren.

![](assets/workflow-execution.png){zoomable="yes"}

## Orchestrierte Kampagnenübergänge {#transitions}

In orchestrierten Kampagnen werden Daten, die über Transitionen von einer Aktivität zur anderen übertragen werden, in einer temporären Arbeitstabelle gespeichert. Diese Daten können für jede Transition angezeigt werden. Wählen Sie dazu eine Transition aus, um ihre Eigenschaften auf der rechten Seite des Bildschirms zu öffnen.

* Klicken Sie auf **[!UICONTROL Vorschau für Schema]**, um das Schema der Arbeitstabelle anzuzeigen.
* Klicken Sie auf **[!UICONTROL Ergebnisvorschau]**, um die in der ausgewählten Transition übertragenen Daten zu visualisieren.

![](assets/transition.png){zoomable="yes"}

## Überwachen der Aktivitätsausführung {#activities}

Visuelle Indikatoren in der rechten oberen Ecke eines jeden Aktivitätsfeldes ermöglichen es, die Ausführung zu überprüfen:

| Visueller Indikator | Beschreibung |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | Die Aktivität wird derzeit ausgeführt. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | Die Aktivität erfordert Ihre Aufmerksamkeit. Dies kann die Bestätigung eines Versands oder die Ergreifung einer notwendigen Maßnahme beinhalten. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | Bei der Aktivität ist ein Fehler aufgetreten. Um das Problem zu beheben, öffnen Sie die orchestrierten Kampagnenprotokolle, um weitere Informationen zu erhalten. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | Die Aktivität wurde erfolgreich ausgeführt. |

## Überwachen der Protokolle und Aufgaben {#logs-tasks}

Die Überwachung von Workflow-Protokollen und -Aufgaben ist ein wichtiger Schritt, um Ihre orchestrierten Kampagnen zu analysieren und sicherzustellen, dass sie ordnungsgemäß ausgeführt werden. Sie können über das Symbol **[!UICONTROL Protokolle]** in der Aktionssymbolleiste und im Eigenschaftenbereich jeder Aktivität aufgerufen werden.

Das Menü **[!UICONTROL Protokolle und Aufgaben]** enthält einen Verlauf der orchestrierten Kampagnenausführung, in dem alle Benutzeraktionen und aufgetretenen Fehler aufgezeichnet werden.
![](assets/workflow-logs.png){zoomable="yes"}

Es stehen zwei Arten von Informationen zur Verfügung:

* Die **[!UICONTROL Log]**-Registerkarte enthält den Ausführungsverlauf aller orchestrierten Kampagnenaktivitäten. Sie zeigt in chronologischer Abfolge alle Vorgänge und Ausführungsfehler.
* Die Registerkarte **[!UICONTROL Aufgaben]** liefert Details zur Ausführungsabfolge der Aktivitäten.

In beiden Registerkarten können Sie die angezeigten Spalten und ihre Reihenfolge auswählen, Filter anwenden und das Suchfeld verwenden, um die gewünschten Informationen schnell zu finden.

## Orchestrierte Befehle zur Kampagnenausführung {#execution-commands}

Die Aktionsleiste in der rechten oberen Ecke enthält Befehle, mit denen Sie die koordinierte Kampagnenausführung verwalten können. Sie haben folgende Möglichkeiten:

* **[!UICONTROL Starten]**/**[!UICONTROL Fortsetzen]** der Ausführung von   eine koordinierte Kampagne, die dann den Status In Bearbeitung annimmt. Wenn die orchestrierte Kampagne angehalten wurde, wird sie fortgesetzt, andernfalls wird sie gestartet und die anfänglichen Aktivitäten werden dann aktiviert.

* **[!UICONTROL Pause]** Die Ausführung der orchestrierten Kampagne, die dann den Status „Paused“ annimmt. Bis zur Wiederaufnahme werden keine neuen Aktivitäten aktiviert, laufende Vorgänge werden jedoch nicht abgebrochen.

* **[!UICONTROL Stopp]** eine orchestrierte Kampagne, die ausgeführt wird und dann den Status „Abgeschlossen“ annimmt. Die laufenden Vorgänge werden nach Möglichkeit unterbrochen. Sie können die orchestrierte Kampagne nicht an der Stelle fortsetzen, an der sie gestoppt wurde.
