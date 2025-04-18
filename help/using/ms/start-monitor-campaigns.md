---
solution: Journey Optimizer
product: journey optimizer
title: Planen und Starten von orchestrierten Kampagnen mit Adobe Journey Optimizer
description: Erfahren Sie, wie Sie mit Adobe Journey Optimizer koordinierte Kampagnen planen und starten
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 36%

---

# Planen und Starten von koordinierten Kampagnen {#start-monitor}



>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Veröffentlichen einer orchestrierten Kampagne"
>abstract="Um Ihre Kampagne zu starten, müssen Sie sie veröffentlichen. Stellen Sie sicher, dass alle Warnungen vor der Veröffentlichung gelöscht wurden."

Nachdem Sie Ihre koordinierten und entworfenen Aufgaben auf der Arbeitsfläche erstellt haben, können Sie sie veröffentlichen und ihre Ausführung überwachen.

## Planungsoptionen

>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Planungsaktivität"
>abstract="Die Kampagne **Planung** ermöglicht es Ihnen, den Beginn der orchestrierten Kampagne zu planen. Diese Aktivität sollte als geplanter Start betrachtet werden. Sie kann nur als erste Aktivität der koordinierten Kampagne verwendet werden."

Als Kampagnen-Manager können Sie Kampagnen so planen, dass sie zu bestimmten Zeiten automatisch gestartet werden, was einen präzisen Zeitpunkt und genaue Zielgruppendaten für Marketing-Nachrichten ermöglicht.

### Best Practices {#scheduler-best-practices}

* Planen Sie keine orchestrierte Kampagne, die öfter als alle 15 Minuten ausgeführt wird, da die Gesamtleistung des Systems beeinträchtigt werden kann und Blockierungen in der Datenbank entstehen können.
* Wenn Sie eine einmalige Nachricht in Ihrer orchestrierten Kampagne senden möchten, können Sie sie auf „Einmal **&quot;**.
* Wenn Sie in einer orchestrierten Kampagne eine wiederkehrende Nachricht senden möchten, müssen Sie eine **Planung**-Option verwenden und die Ausführungsfrequenz festlegen. Die Aktivität „Wiederkehrender Versand“ ermöglicht keine Festlegung eines Zeitplans.

### Kampagnenzeitplan konfigurieren {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_validity"
>title="Gültigkeit der Planung"
>abstract="Sie können einen Gültigkeitszeitraum für die Planung definieren. Er kann dauerhaft sein (Standard) oder bis zu einem bestimmten Datum gültig sein."


>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_options"
>title="Planungsoptionen"
>abstract="Definieren Sie die Häufigkeit der Planung. Er kann zu einem bestimmten Zeitpunkt, einmal oder mehrmals pro Tag, Woche oder Monat, ausgeführt werden."

![Planungsbildschirm mit monatlichen Optionen](assets/scheduler-screen.png)

Führen Sie die folgenden Schritte aus, um den **Zeitplan für koordinierte Kampagnen** zu konfigurieren:

1. Klicken Sie auf **Schaltfläche** So bald wie möglich“ oben auf der Arbeitsfläche Ihrer orchestrierten Kampagne.

1. Konfigurieren Sie die **Ausführungshäufigkeit**:

   * **Einmal**: Die orchestrierte Kampagne wird ein einziges Mal ausgeführt.

   * **Täglich**: Die orchestrierte Kampagne wird zu einem bestimmten Zeitpunkt einmal täglich ausgeführt.

   * **Mehrmals am Tag:** die orchestrierte Kampagne wird regelmäßig mehrmals am Tag ausgeführt. Sie können Ausführungen zu bestimmten Zeiten oder in regelmäßigen Abständen einrichten.

   * **Wöchentlich**: Die orchestrierte Kampagne wird zu einem bestimmten Zeitpunkt, ein- oder mehrmals pro Woche ausgeführt.

   * **Monatlich**: Die orchestrierte Kampagne wird zu einem bestimmten Zeitpunkt, ein- oder mehrmals im Monat ausgeführt. Sie können Monate auswählen, in denen die orchestrierte Kampagne ausgeführt werden soll. Sie können für die Ausführung von Workflows auch bestimmte Wochentage des Monats auswählen, z. B. am zweiten Dienstag des Monats.

     ![Planer-Bildschirm mit Beispiel für die tägliche Ausführung](assets/scheduler-daily-sample.png){width="50%" align="left"}

1. Definieren Sie die Ausführungsdetails. Die Detailfelder variieren je nach verwendeter Häufigkeit (Zeit, Wiederholungshäufigkeit, angegebene Tage usw.).

1. Klicken Sie **Startzeiten in der Vorschau**, um den Zeitplan der nächsten zehn Ausführungen Ihrer orchestrierten Kampagne zu überprüfen.

1. Definieren des Gültigkeitszeitraums des Zeitplans:

   * **Dauerhaft (läuft nie ab)**: Die orchestrierte Kampagne wird entsprechend der angegebenen Häufigkeit ohne Begrenzung des Zeitrahmens oder der Anzahl der Iterationen ausgeführt.

   * **Gültigkeitszeitraum**: Die orchestrierte Kampagne wird entsprechend der angegebenen Häufigkeit bis zu einem bestimmten Datum ausgeführt. Sie müssen Start- und Enddaten angeben.

1. Klicken Sie **Bestätigen**, um Ihre Einstellungen zu speichern. Die Ausführungsfrequenz wird über der orchestrierten Kampagnen-Arbeitsfläche angezeigt.

>[!TIP]
>
>Wenn Sie die orchestrierte Kampagne sofort starten möchten, behalten Sie den Standardwert **So bald wie möglich** bei.

## Beispiel {#scheduler-example}

Im folgenden Beispiel wird die Aktivität so konfiguriert, dass die orchestrierte Kampagne zweimal täglich um 9 Uhr und um 12 Uhr täglich zwischen dem 1. Oktober 2025 und dem 1. Januar 2026 ausgeführt wird.

![Planung konfiguriert, um die Kampagne zweimal täglich um 9 und 12 Uhr auszuführen](assets/scheduler-sample.png){width="50%" align="left"}


## Starten einer orchestrierten Kampagne {#start}

Um eine orchestrierte Kampagne zu starten, gehen Sie zur Registerkarte **[!UICONTROL Orchestrierung]** des Menüs **[!UICONTROL Kampagnen]** und wählen Sie die zu startende Kampagne aus und klicken Sie dann auf die **[!UICONTROL Play]**-Schaltfläche in der oberen rechten Ecke der Arbeitsfläche.

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
