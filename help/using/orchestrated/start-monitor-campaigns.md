---
solution: Journey Optimizer
product: journey optimizer
title: Starten und Überwachen orchestrierter Kampagnen mit Adobe Journey Optimizer
description: Erfahren Sie, wie Sie mit Adobe Journey Optimizer orchestrierte Kampagnen starten und überwachen.
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 18%

---

# Starten und Überwachen von orchestrierten Kampagnen {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Veröffentlichen einer orchestrierten Kampagne"
>abstract="Um Ihre Kampagne zu starten, müssen Sie sie veröffentlichen. Stellen Sie sicher, dass alle Fehler vor der Veröffentlichung gelöscht wurden."

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/><b>[ Starten und Überwachen der Kampagne](start-monitor-campaigns.md)</b><br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Ausdrücke bearbeiten](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimension ändern](activities/change-dimension.md) - [Kanalaktivitäten](activities/channels.md) - [Kombinieren](activities/combine.md) - [Anreicherung](activities/deduplication.md) - [Formulare](activities/enrichment.md) - [Abstimmung](activities/fork.md) [&#128279;](activities/reconciliation.md) [&#128279;](activities/save-audience.md) [&#128279;](activities/split.md) ->Zielgruppe speichern[ -AufspaltungWarten](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Nachdem Sie Ihre koordinierten und entworfenen Aufgaben auf der Arbeitsfläche erstellt haben, können Sie sie veröffentlichen und ihre Ausführung überwachen.

Sie können die Kampagne auch im Testmodus ausführen, um ihre Ausführung und das Ergebnis der verschiedenen Aktivitäten zu überprüfen.

## Testen der Kampagne vor der Veröffentlichung {#test}

Mit [!DNL Journey Optimizer] können Sie orchestrierte Kampagnen testen, bevor Sie live gehen. Wenn eine Kampagne erstellt wird, wechselt sie standardmäßig in **Status** Entwurf“. In diesem Zustand können Sie die Kampagne manuell ausführen, um den Fluss zu testen.

Alle Aktivitäten auf der Arbeitsfläche werden ausgeführt, mit Ausnahme von **[!UICONTROL Zielgruppe speichern]** Aktivitäten und Kanalaktivitäten. Es gibt keine funktionalen Auswirkungen auf Ihre Daten oder Zielgruppe.

So testen Sie eine Kampagne:

1. Öffnen Sie die orchestrierte Kampagne.
2. Klicken Sie auf **[!UICONTROL Starten]**.

![](assets/campaign-start.png){zoomable="yes"}

Jede Aktivität in der Kampagne wird sequenziell ausgeführt, bis das Ende des Diagramms erreicht ist.

Während des Tests können Sie die Ausführung der Kampagne über die Aktionsleiste auf der Arbeitsfläche steuern. Dort haben Sie folgende Möglichkeiten:

* **Beenden** Sie die Ausführung jederzeit.
* **Starten** die Ausführung erneut.
* **Fortsetzen** Die Ausführung, wenn sie zuvor aufgrund eines Problems angehalten wurde.

Wenn während der Ausführung ein Fehler oder eine Warnung auftritt, werden Sie über das Symbol **[!UICONTROL Warnhinweise]** / **[!UICONTROL Warnung]** in der Symbolleiste der Arbeitsfläche benachrichtigt.

![](assets/campaign-warning.png){zoomable="yes"}

Fehlgeschlagene Aktivitäten können auch schnell mithilfe der [visuellen Statusindikatoren](#activities) erkannt werden, die direkt auf jeder Aktivität angezeigt werden. Eine ausführliche Fehlerbehebung finden Sie in den [Kampagnenprotokollen](#logs-tasks) die detaillierte Informationen zum Fehler und seinem Kontext enthalten.

Nach der Validierung kann die Kampagne veröffentlicht werden.

## Veröffentlichen der Kampagne {#publish}

Sobald Ihre Kampagne getestet und bereit ist, klicken Sie auf **[!UICONTROL Veröffentlichen]**, um sie live zu schalten.

![](assets/campaign-publish.png){zoomable="yes"}

>[!NOTE]
>
>Wenn die Schaltfläche **[!UICONTROL Veröffentlichen]** deaktiviert (ausgegraut) ist, greifen Sie über die Aktionsleiste auf die Protokolle zu und überprüfen Sie die Fehlermeldungen. Alle Fehler müssen behoben werden, bevor eine Kampagne veröffentlicht werden kann.

Der visuelle Fluss wird neu gestartet, und echte Profile beginnen, in Echtzeit durch den Journey zu fließen.

Wenn die Veröffentlichungsaktion fehlschlägt (z. B. wegen fehlenden Nachrichteninhalts), werden Sie benachrichtigt und müssen das Problem beheben, bevor Sie es erneut versuchen. Nach erfolgreicher Veröffentlichung beginnt die Kampagne mit der Ausführung (sofort oder planmäßig), wechselt von **Entwurf** in **Live**-Status und wird zu „Schreibgeschützt“.

## Kampagnenausführung überwachen {#monitor}

### Visuelle Flussüberwachung {#flow}

Während der Ausführung (im Test- oder Live-Modus) zeigt der visuelle Fluss an, wie sich Profile in Echtzeit durch den Journey bewegen. Die Anzahl der Profile, die zwischen Aufgaben wechseln, wird angezeigt.

![](assets/workflow-execution.png){zoomable="yes"}

Daten, die über Transitionen von einer Aktivität zur anderen übertragen werden, werden in einer temporären Arbeitstabelle gespeichert. Diese Daten können für jede Transition angezeigt werden. So überprüfen Sie die zwischen den Aktivitäten übergebenen Daten:

1. Transition auswählen.
1. Klicken Sie im Eigenschaftenbereich auf **[!UICONTROL Vorschau des]**), um das Arbeitstabellenschema anzuzeigen. Wählen Sie **[!UICONTROL Vorschau der Ergebnisse]** aus, um die übertragenen Daten anzuzeigen.

![](assets/transition.png){zoomable="yes"}

### Indikatoren für die Aktivitätsausführung {#activities}

Visuelle Statusindikatoren helfen zu verstehen, wie jede Aktivität funktioniert:

| Visueller Indikator | Beschreibung |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | Die Aktivität wird derzeit ausgeführt. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | Die Aktivität erfordert Ihre Aufmerksamkeit. Dies kann die Bestätigung eines Versands oder die Ergreifung einer notwendigen Maßnahme beinhalten. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | Bei der Aktivität ist ein Fehler aufgetreten. Um das Problem zu beheben, öffnen Sie die orchestrierten Kampagnenprotokolle, um weitere Informationen zu erhalten. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | Die Aktivität wurde erfolgreich ausgeführt. |

### Logs und Aufgaben {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="Logs und Aufgaben"
>abstract="Der Bildschirm **Logs und Aufgaben** enthält einen Verlauf zur Ausführung der orchestrierten Kampagne, in dem alle Benutzeraktionen und aufgetretenen Fehler aufgezeichnet werden. "

Die Überwachung von Protokollen und Aufgaben ist ein wichtiger Schritt, um Ihre orchestrierten Kampagnen zu analysieren und sicherzustellen, dass sie ordnungsgemäß ausgeführt werden. Auf Protokolle und Aufgaben kann über die Schaltfläche **[!UICONTROL Protokolle]** zugegriffen werden, die sowohl im Test- als auch im Live-Modus in der Symbolleiste der Arbeitsfläche oder im Eigenschaftenbereich jeder Aktivität verfügbar ist.

Der Bildschirm **[!UICONTROL Protokolle und Aufgaben]** enthält einen vollständigen Verlauf der Kampagnenausführung, in dem alle Benutzeraktionen und aufgetretenen Fehler aufgezeichnet werden.

![](assets/workflow-logs.png){zoomable="yes"}

Es stehen zwei Arten von Informationen zur Verfügung:

* Die **[!UICONTROL Log]** enthält den chronologischen Verlauf aller Vorgänge und Fehler.
* Auf **[!UICONTROL Registerkarte]** Aufgaben“ wird die Ausführungssequenz der Aktivitäten Schritt für Schritt beschrieben.

In beiden Registerkarten können Sie die angezeigten Spalten und ihre Reihenfolge auswählen, Filter anwenden und das Suchfeld verwenden, um die gewünschten Informationen schnell zu finden.
