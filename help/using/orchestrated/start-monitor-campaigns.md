---
solution: Journey Optimizer
product: journey optimizer
title: Starten und Überwachen orchestrierter Kampagnen mit Adobe Journey Optimizer
description: Erfahren Sie, wie Sie mit Adobe Journey Optimizer orchestrierte Kampagnen starten und überwachen.
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: f8afef4729e50b7c9899bf7f2fe282347220dfac
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 35%

---

# Starten und Überwachen von orchestrierten Kampagnen {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Veröffentlichen einer orchestrierten Kampagne"
>abstract="Um Ihre Kampagne zu starten, müssen Sie sie veröffentlichen. Stellen Sie sicher, dass alle Warnungen vor der Veröffentlichung gelöscht wurden."

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](configuration-steps.md)<br/><br/>[Zugreifen auf und Verwalten von orchestrierten Kampagnen](access-manage-orchestrated-campaigns.md) | [Wichtige Schritte für die orchestrierte Kampagnenerstellung](gs-campaign-creation.md)<br/><br/>[Erstellen und Planen der Kampagnen](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[ Senden von Nachrichten mit orchestrierten Kampagnen](send-messages.md)<br/><br/><b>[Starten und Überwachen der Kampagne](start-monitor-campaigns.md)</b><br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen Sie Ihre ersten ](build-query.md)<br/><br/>[-Bearbeitungsausdrücke](edit-expressions.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimensionsänderung](activities/change-dimension.md) - [Kombinieren](activities/combine.md) - [Deduplizierung](activities/enrichment.md) - [Verzweigung](activities/fork.md) - [Abstimmung](activities/reconciliation.md) - [Aufspaltung](activities/split.md) [&#128279;](activities/wait.md) Warten[&#128279;](activities/deduplication.md)  |

{style="table-layout:fixed"}

+++

<br/>

Nachdem Sie Ihre koordinierten und entworfenen Aufgaben auf der Arbeitsfläche erstellt haben, können Sie sie veröffentlichen und ihre Ausführung überwachen.

Sie können die Kampagne auch im Testmodus ausführen, um ihre Ausführung und das Ergebnis der verschiedenen Aktivitäten zu überprüfen.

## Testen und Veröffentlichen der orchestrierten Kampagne {#test}

Mit Journey Optimizer können Sie Ihre orchestrierten Kampagnen testen, bevor Sie sie veröffentlichen. Auf diese Weise können Sie die Ausführung und das Ergebnis der verschiedenen Aufgaben überprüfen, aus denen die Kampagne besteht, und das hat keine funktionalen Auswirkungen: Alle Aktivitäten auf der Arbeitsfläche werden ausgeführt, mit Ausnahme der Aktivitäten, die eine Auswirkung haben **[!UICONTROL Audience speichern]** und Kanalaktivitäten.

Um eine orchestrierte Kampagne im Testmodus zu starten, öffnen Sie die orchestrierte Kampagne und klicken Sie dann auf die Schaltfläche **[!UICONTROL Starten]**.

![](assets/campaign-start.png){zoomable="yes"}

Sobald die orchestrierte Kampagne ausgeführt wird, wird jede Aktivität auf der Arbeitsfläche in sequenzieller Reihenfolge ausgeführt, bis das Ende der orchestrierten Kampagne erreicht ist.

Wenn Ihre Kampagne bereit für die Live-Schaltung ist, klicken Sie auf die Schaltfläche **[!UICONTROL Veröffentlichen]**. Der visuelle Fluss auf der Arbeitsfläche wird neu gestartet, sodass Sie den Fortschritt der Profile im Diagramm überprüfen können.

## Orchestrierte Kampagnen - visueller Fluss

Wenn eine orchestrierte Kampagne ausgeführt wird, entweder im Testmodus oder in der Produktion, können Sie den Fortschritt der Zielprofile durch die verschiedenen Aufgaben in Echtzeit mithilfe eines visuellen Flusses verfolgen. Auf diese Weise können Sie den Status jeder Aktivität und die Anzahl der Profile, die zwischen ihnen wechseln, schnell identifizieren.

![](assets/workflow-execution.png){zoomable="yes"}

Daten, die über Transitionen von einer Aktivität zur anderen übertragen werden, werden in einer temporären Arbeitstabelle gespeichert. Diese Daten können für jede Transition angezeigt werden. Wählen Sie dazu eine Transition aus, um ihre Eigenschaften auf der rechten Seite des Bildschirms zu öffnen.

* Klicken Sie auf **[!UICONTROL Vorschau für Schema]**, um das Schema der Arbeitstabelle anzuzeigen.
* Klicken Sie auf **[!UICONTROL Ergebnisvorschau]**, um die in der ausgewählten Transition übertragenen Daten zu visualisieren.

![](assets/transition.png){zoomable="yes"}

## Kampagnenausführung überwachen

### Überwachen der Aktivitätsausführung {#activities}

Visuelle Indikatoren in jedem Aktivitätsfeld ermöglichen es, die Ausführung zu überprüfen:

| Visueller Indikator | Beschreibung |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | Die Aktivität wird derzeit ausgeführt. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | Die Aktivität erfordert Ihre Aufmerksamkeit. Dies kann die Bestätigung eines Versands oder die Ergreifung einer notwendigen Maßnahme beinhalten. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | Bei der Aktivität ist ein Fehler aufgetreten. Um das Problem zu beheben, öffnen Sie die orchestrierten Kampagnenprotokolle, um weitere Informationen zu erhalten. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | Die Aktivität wurde erfolgreich ausgeführt. |

### Überwachen der Protokolle und Aufgaben {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="Protokolle und Aufgaben"
>abstract="Der Bildschirm **Logs und Aufgaben** enthält einen Verlauf zur Ausführung der orchestrierten Kampagne, in dem alle Benutzeraktionen und aufgetretenen Fehler aufgezeichnet werden. "

Die Überwachung von Protokollen und Aufgaben ist ein wichtiger Schritt, um Ihre orchestrierten Kampagnen zu analysieren und sicherzustellen, dass sie ordnungsgemäß ausgeführt werden. Sie können über das Symbol **[!UICONTROL Protokolle]** in der Aktionssymbolleiste und im Eigenschaftenbereich jeder Aktivität aufgerufen werden.

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
