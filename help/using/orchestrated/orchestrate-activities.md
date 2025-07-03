---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen von orchestrierten Kampagnen mit Adobe Journey Optimizer
description: Erfahren Sie, wie Sie mit Adobe Journey Optimizer koordinierte Kampagnen erstellen
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 5ebc82f566d416a177a3278816c60d896a10eff6
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 24%

---

# Kampagnenaktivitäten orchestrieren {#orchestrate}

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](configuration-steps.md)<br/><br/>[Zugreifen auf und Verwalten von orchestrierten Kampagnen](access-manage-orchestrated-campaigns.md) | [Wichtige Schritte für die orchestrierte Kampagnenerstellung](gs-campaign-creation.md)<br/><br/>[Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/><b>[Orchestrieren von Aktivitäten](orchestrate-activities.md)</b><br/><br/>[Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Ausdrücke bearbeiten](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimension ändern](activities/change-dimension.md) - [Kanalaktivitäten](activities/channels.md) - [Kombinieren](activities/combine.md) - [Anreicherung](activities/deduplication.md) - [Formulare](activities/enrichment.md) - [Abstimmung](activities/fork.md) [&#128279;](activities/reconciliation.md) [&#128279;](activities/save-audience.md) [&#128279;](activities/split.md) ->Zielgruppe speichern[ -AufspaltungWarten](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Sobald Sie [eine orchestrierte Kampagne erstellt haben](gs-campaign-creation.md) können Sie mit der Orchestrierung der verschiedenen Aufgaben beginnen, die sie ausführen soll. Dazu wird eine visuelle Arbeitsfläche bereitgestellt, mit der Sie ein orchestriertes Kampagnendiagramm erstellen können. Innerhalb dieses Diagramms können Sie verschiedene Aktivitäten hinzufügen und sie in einer sequentiellen Reihenfolge verbinden.

## Hinzufügen von Aktivitäten {#add}

In diesem Schritt der Konfiguration wird das Diagramm mit einem Startsymbol angezeigt, das den Anfang Ihrer orchestrierten Kampagne darstellt. Um Ihre erste Aktivität hinzuzufügen, klicken Sie auf die Schaltfläche **+**, die mit dem Startsymbol verbunden ist.

Es erscheint eine Liste von Aktivitäten, die dem Diagramm hinzugefügt werden können. Die verfügbaren Aktivitäten hängen von Ihrer Position im orchestrierten Kampagnendiagramm ab. Wenn Sie Ihre erste Aktivität hinzufügen, können Sie Ihre orchestrierte Kampagne starten, indem Sie beispielsweise eine Audience ansprechen, den orchestrierten Kampagnenpfad aufteilen oder eine **Warten**-Aktivität festlegen, um die orchestrierte Kampagnenausführung zu verzögern. Andererseits können Sie nach einer Aktivität **Zielgruppe aufbauen** Ihre Zielgruppe mit Zielgruppenbestimmungsaktivitäten verfeinern, einen Versand an Ihre Zielgruppe mit Kanalaktivitäten durchführen oder den orchestrierten Kampagnenprozess mit Flusssteuerungsaktivitäten organisieren.

![](assets/orchestrated-start.png){zoomable="yes"}

Nachdem eine Aktivität zum Diagramm hinzugefügt wurde, wird ein rechter Bereich angezeigt, in dem Sie sie mit bestimmten Einstellungen konfigurieren können. Detaillierte Informationen über die Konfiguration jeder Aktivität finden Sie in [diesem Abschnitt](activities/about-activities.md).

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

Wiederholen Sie diesen Vorgang, um beliebig viele Aktivitäten hinzuzufügen, je nach den Aufgaben, die Ihre koordinierte Kampagne ausführen soll. Beachten Sie, dass Sie auch eine neue Aktivität zwischen zwei Aktivitäten einfügen können. Klicken Sie dazu auf die Schaltfläche **+** an der Transition zwischen den Aktivitäten, wählen Sie die gewünschte Aktivität aus und konfigurieren Sie sie im rechten Bereich.

Sie haben die Möglichkeit, den Namen der Transitionen zwischen den einzelnen Aktivitäten zu personalisieren. Wählen Sie dazu die Transition aus und ändern Sie die Bezeichnung im rechten Bereich.

![](assets/canvas-transition.png)

### Die Arbeitsflächensymbolleiste {#toolbar}

Die Symbolleiste der Arbeitsfläche bietet Optionen zum einfachen Bearbeiten der Aktivitäten und zum Navigieren auf der Arbeitsfläche:

![](assets/orchestrated-toolbar.png)

![Symbol für mehrere Auswahlmodi](assets/do-not-localize/canvas-multiple.svg) Wählen Sie mehrere Aktivitäten aus, um sie alle gleichzeitig zu löschen oder zu kopieren und einzufügen. [Erfahren Sie, wie Sie Aktivitäten kopieren und einfügen](#copy)

![Symbol „Drehen](assets/do-not-localize/canvas-rotate.svg) Wechseln Sie die Arbeitsfläche vertikal.

![Am Bildschirmsymbol anpassen](assets/do-not-localize/canvas-fit.svg) Passen Sie den Zoom der Arbeitsfläche an Ihren Bildschirm an.

![Auszoomen-Symbol](assets/do-not-localize/canvas-zoomout.svg) ![Einzoomen-Symbol](assets/do-not-localize/canvas-zoomin.svg) Auszoomen oder auf der Arbeitsfläche.

![Symbol Kampagneneinstellungen](assets/do-not-localize/canvas-map.svg) Öffnet einen Schnappschuss der Arbeitsfläche, der Ihnen anzeigt, wo Sie sich befinden.

### Verwalten von Aktivitäten {#manage}

Beim Hinzufügen von Aktivitäten sind im Eigenschattenbereich Aktionsschaltflächen verfügbar, mit denen Sie mehrere Vorgänge ausführen können. 

![](assets/activity-action.png)

![Löschsymbol](assets/do-not-localize/activity-delete.svg) Löschen der Aktivität auf der Arbeitsfläche.

![Symbol deaktivieren](assets/do-not-localize/activity-disable.svg) ![Symbol aktivieren](assets/do-not-localize/activity-enable.svg) Aktivität deaktivieren/aktivieren. Wenn die orchestrierte Kampagne ausgeführt wird, werden deaktivierte Aktivitäten und die folgenden Aktivitäten auf demselben Pfad nicht ausgeführt und die orchestrierte Kampagne wird gestoppt.

![Pausensymbol](assets/do-not-localize/activity-pause.svg) ![Fortsetzungssymbol](assets/do-not-localize/activity-resume.svg) Aussetzen/Fortsetzen der Aktivität. Wenn die orchestrierte Kampagne ausgeführt wird, wird sie bei der angehaltenen Aktivität angehalten. Die entsprechende Aufgabe und alle ihr im gleichen Pfad folgenden Aufgaben werden nicht ausgeführt.

![Kopieren-Symbol](assets/do-not-localize/activity-copy.svg) Kopieren Sie die Aktivität. [Erfahren Sie, wie Sie Aktivitäten kopieren und einfügen](#copy)

![Symbol „Protokolle und Aufgaben](assets/do-not-localize/activity-logs.svg) Greifen Sie auf die Protokolle und Aufgaben der Aktivität zu.

Bei mehreren **Zielgruppenbestimmungsaktivitäten**, z. B. **Kombinieren** oder **Deduplizierung**, können Sie die verbleibende Population verarbeiten und in eine zusätzliche ausgehende Transition einschließen. Wenn Sie beispielsweise die Aktivität &quot;**&quot; verwenden** besteht das Komplement aus der Population, die keiner der zuvor definierten Teilmengen entsprach. Um diese Funktion zu verwenden, aktivieren Sie die Option **[!UICONTROL Komplement erzeugen]**.

### Kopieren und Einfügen von Aktivitäten {#copy}

Sie können Aktivitäten kopieren und in eine beliebige orchestrierte Kampagnen-Arbeitsfläche einfügen. Die Zielkampagne kann sich auf einer anderen Browser-Registerkarte befinden.

* Um eine Aktivität zu kopieren, klicken Sie auf ![ Schaltfläche ](assets/do-not-localize/activity-copy.svg)Symbol kopieren“ im Bereich mit den Eigenschaften der Aktivität.
* Um mehrere Aktivitäten zu kopieren, klicken Sie auf das Symbol ![Mehrfachauswahlmodus](assets/do-not-localize/canvas-multiple.svg) in der Symbolleiste der Arbeitsfläche.

| Eine Aktivität kopieren | Mehrere Aktivitäten kopieren |
|  ---  |  ---  |
| ![](assets/orchestrated-copy-1.png){width="200" align="center" zoomable="yes"} | ![](assets/orchestrated-copy-2.png){width="200" align="center" zoomable="yes"} |

Um die Aktivitäten einzufügen, klicken Sie auf die Schaltfläche **+** auf einer Transition und wählen Sie „x Aktivität einfügen“.

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

## Beispiel für ein Diagramm {#example}

Im Folgenden finden Sie ein Beispiel für eine orchestrierte Kampagne, die eine E-Mail an alle Kunden senden soll, die einen Kauf von mindestens 100 $ getätigt haben, während alle Kunden ausgeschlossen werden, die weniger als 50 Treuepunkte haben.

![](assets/canvas-example-diagram.png){zoomable="yes"}

Um dies zu bewerkstelligen, wurden die folgenden Aktivitäten hinzugefügt:

* Eine Aktivität **[!UICONTROL Verzweigung]** unterteilt die orchestrierte Kampagne in drei Pfade.
* **[!UICONTROL Zielgruppe aufbauen]**-Aktivitäten richten sich an die drei Kundengruppen:

   * Kundinnen und Kunden mit einer E-Mail-Adresse,
   * Kunden, die einen Kauf von mindestens 100 $ getätigt haben,
   * Kunden mit weniger als 50 Treuepunkten.

* Eine **[!UICONTROL Kombinieren]**-Aktivität gruppiert Kunden mit einer E-Mail und Kunden, die einen Kauf von mindestens 100 € getätigt haben,
* Eine **[!UICONTROL Kombinieren]**-Aktivität schließt Kunden mit weniger als 50 Treuepunkten aus,
* Eine Aktivität **[!UICONTROL E-Mail]** Versand) sendet eine E-Mail an die resultierenden Kundinnen und Kunden.

## Nächste Schritte {#next}

Nachdem Sie das Diagramm für die orchestrierte Kampagne erfolgreich erstellt haben, können Sie die orchestrierte Kampagne ausführen und den Fortschritt der verschiedenen Aufgaben verfolgen. [Erfahren Sie, wie Sie eine orchestrierte Kampagne starten und ihre Ausführung überwachen](start-monitor-campaigns.md)
