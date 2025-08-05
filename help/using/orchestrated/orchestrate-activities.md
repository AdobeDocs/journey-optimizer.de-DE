---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen von orchestrierten Kampagnen mit Adobe Journey Optimizer
description: Erfahren Sie, wie Sie mit Adobe Journey Optimizer koordinierte Kampagnen erstellen
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 56%

---


# Orchestrieren von Kampagnenaktivitäten {#orchestrate}

Nachdem Sie [eine orchestrierte Kampagne erstellt haben](gs-campaign-creation.md) können Sie mit der Orchestrierung der verschiedenen Aufgaben beginnen, die sie ausführen soll. Dazu wird eine visuelle Arbeitsfläche bereitgestellt, über die Sie ein orchestriertes Kampagnendiagramm erstellen können. Innerhalb dieses Diagramms können Sie verschiedene Aktivitäten hinzufügen und sie in einer sequentiellen Reihenfolge verbinden.

## Hinzufügen von Aktivitäten {#add}

In diesem Schritt der Konfiguration wird das Diagramm mit einem Startsymbol angezeigt, das den Anfang Ihrer orchestrierten Kampagne darstellt. Um Ihre erste Aktivität hinzuzufügen, klicken Sie auf die Schaltfläche **+**, die mit dem Startsymbol verbunden ist.

Es erscheint eine Liste von Aktivitäten, die dem Diagramm hinzugefügt werden können. Die verfügbaren Aktivitäten hängen von Ihrer Position im Diagramm Orchestrierte Kampagne ab. Wenn Sie Ihre erste Aktivität hinzufügen, können Sie beispielsweise Ihre orchestrierte Kampagne starten, indem Sie eine Audience ansprechen, den Pfad der orchestrierten Kampagne aufteilen oder eine **Warten**-Aktivität festlegen, um die Ausführung der orchestrierten Kampagne zu verzögern. Andererseits können Sie nach einer Aktivität **Zielgruppe aufbauen** Ihre Zielgruppe mit Zielgruppenbestimmungsaktivitäten verfeinern, einen Versand an Ihre Zielgruppe mit Kanalaktivitäten durchführen oder den orchestrierten Kampagnenprozess mit Flusssteuerungsaktivitäten organisieren.

![](assets/orchestrated-start.png){zoomable="yes"}

Sobald eine Aktivität zum Diagramm hinzugefügt wurde, erscheint rechts ein Bereich, in dem Sie die Aktivität mit spezifischen Einstellungen konfigurieren können. Detaillierte Informationen über die Konfiguration jeder Aktivität finden Sie in [diesem Abschnitt](activities/about-activities.md).

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

Wiederholen Sie diesen Vorgang, um je nach den Aufgaben, die Ihre orchestrierte Kampagne ausführen soll, beliebig viele Aktivitäten hinzuzufügen. Beachten Sie, dass Sie auch eine neue Aktivität zwischen zwei Aktivitäten einfügen können. Klicken Sie dazu auf die Schaltfläche **+** an der Transition zwischen den Aktivitäten, wählen Sie die gewünschte Aktivität aus und konfigurieren Sie sie im rechten Bereich.

Sie haben die Möglichkeit, den Namen der Transitionen zwischen den einzelnen Aktivitäten anzupassen. Wählen Sie dazu die Transition aus und ändern Sie das Label im rechten Bereich.

![](assets/canvas-transition.png)

### Die Arbeitsflächensymbolleiste {#toolbar}

Die Symbolleiste der Arbeitsfläche bietet Optionen zum einfachen Bearbeiten der Aktivitäten und zum Navigieren auf der Arbeitsfläche:

![](assets/orchestrated-toolbar.png)

![Symbol „Mehrfachauswahlmodus“](assets/do-not-localize/canvas-multiple.svg) Wählen Sie mehrere Aktivitäten aus, um sie alle gleichzeitig zu löschen oder zu kopieren und einzufügen. [Weitere Informationen zum Kopieren und Einfügen von Aktivitäten](#copy)

![Symbol „Drehen“](assets/do-not-localize/canvas-rotate.svg) Spiegelt die Arbeitsfläche vertikal.

![Symbol „An Bildschirm anpassen“](assets/do-not-localize/canvas-fit.svg) Passt die Größe der Arbeitsfläche an Ihren Bildschirm an.

![Symbol „Verkleinern“](assets/do-not-localize/canvas-zoomout.svg)/![Symbol „Vergrößern“](assets/do-not-localize/canvas-zoomin.svg): Verkleinert bzw. vergrößert die Arbeitsfläche.

![Symbol „Kampagneneinstellungen“](assets/do-not-localize/canvas-map.svg): Öffnet eine Momentaufnahme der Arbeitsfläche, auf der Sie sich befinden.

### Verwalten von Aktivitäten {#manage}

Beim Hinzufügen von Aktivitäten sind im Eigenschattenbereich Aktionsschaltflächen verfügbar, mit denen Sie mehrere Vorgänge ausführen können. 

![](assets/activity-action.png)

![Symbol „Löschen“](assets/do-not-localize/activity-delete.svg) Löscht die Aktivität von der Arbeitsfläche aus.

![Symbol „Deaktivieren“](assets/do-not-localize/activity-disable.svg) ![Symbol „Aktivieren“](assets/do-not-localize/activity-enable.svg) Deaktiviert bzw. aktiviert die Aktivität. Wenn die orchestrierte Kampagne ausgeführt wird, werden deaktivierte Aktivitäten und die folgenden Aktivitäten auf demselben Pfad nicht ausgeführt und die orchestrierte Kampagne wird gestoppt.

![Symbol „Pausieren“](assets/do-not-localize/activity-pause.svg) ![Symbol „Fortsetzen“](assets/do-not-localize/activity-resume.svg) Pausiert die Aktivität bzw. setzt sie fort. Wenn die orchestrierte Kampagne ausgeführt wird, wird sie bei der angehaltenen Aktivität angehalten. Die entsprechende Aufgabe und alle ihr im gleichen Pfad folgenden Aufgaben werden nicht ausgeführt.

Sie können jede Aktivität auf der Arbeitsfläche als Haltepunkt verwenden, um die Kampagnenausführung anzuhalten. Das bedeutet, dass die Kampagne nur bis zu dieser Aktivität ausgeführt wird und dann die Ausführung anhält. Beim Anhalten der Ausführung hält die Segmentierungs-Engine temporäre Daten für Sie zur Vorschau bereit. Sie können die eingehende Transition direkt vor der pausierten Aktivität auswählen, um die übertragenen Daten anzuzeigen. Weitere Informationen finden Sie in diesem Abschnitt: [Visuelle Flussüberwachung](../orchestrated/start-monitor-campaigns.md#flow)

![Symbol „Kopieren“](assets/do-not-localize/activity-copy.svg) Kopiert die Aktivität. [Weitere Informationen zum Kopieren und Einfügen von Aktivitäten](#copy)

![Symbol „Protokolle und Aufgaben“](assets/do-not-localize/activity-logs.svg) Greifen Sie auf die Protokolle und Aufgaben der Aktivität zu.

Bei mehreren **Zielgruppenbestimmungsaktivitäten**, z. B. **Kombinieren** oder **Deduplizierung**, können Sie die verbleibende Population verarbeiten und in eine zusätzliche ausgehende Transition einschließen. Wenn Sie beispielsweise eine Aktivität des Typs **Aufspaltung** verwenden, besteht das Komplement aus der Population, die keiner der zuvor definierten Teilmengen entsprochen hat. Um diese Funktion zu verwenden, aktivieren Sie die Option **[!UICONTROL Komplement erzeugen]**.

### Kopieren und Einfügen von Aktivitäten {#copy}

Sie können Aktivitäten kopieren und in eine beliebige orchestrierte Kampagnen-Arbeitsfläche einfügen. Die Zielkampagne kann sich auf einem anderen Browser-Tab befinden.

* Um eine Aktivität zu kopieren, klicken Sie auf die Schaltfläche ![Symbol „Kopieren“](assets/do-not-localize/activity-copy.svg) im Bereich mit den Eigenschaften der Aktivität.
* Um mehrere Aktivitäten zu kopieren, klicken Sie auf das Symbol ![Symbol „Mehrfachauswahlmodus“](assets/do-not-localize/canvas-multiple.svg) in der Symbolleiste der Arbeitsfläche.

| Kopieren einer Aktivität | Kopieren mehrerer Aktivitäten |
|  ---  |  ---  |
| ![](assets/orchestrated-copy-1.png){width="200" align="center" zoomable="yes"} | ![](assets/orchestrated-copy-2.png){width="200" align="center" zoomable="yes"} |

Um die kopierten Aktivitäten einzufügen, klicken Sie auf die Schaltfläche **+** auf einer Transition und wählen Sie „Aktivität x einfügen“ aus.

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

## Beispiel für ein Diagramm {#example}

Im Folgenden finden Sie ein Beispiel für eine orchestrierte Kampagne, die eine E-Mail an alle Kunden senden soll, die einen Kauf von mindestens 100 $ getätigt haben, während alle Kunden ausgeschlossen werden, die weniger als 50 Treuepunkte haben.

![](assets/canvas-example-diagram.png){zoomable="yes"}

Um dies zu bewerkstelligen, wurden die folgenden Aktivitäten hinzugefügt:

* Eine Aktivität **[!UICONTROL Verzweigung]** unterteilt die orchestrierte Kampagne in drei Pfade.
* Aktivitäten des Typs **[!UICONTROL Zielgruppe erstellen]** sprechen die drei Kundengruppen an:

   * Kundinnen und Kunden mit einer E-Mail-Adresse,
   * Kundinnen und Kunden, die einen Kauf in der Höhe von mindestens 100 $ getätigt haben,
   * Kundinnen und Kunden mit weniger als 50 Treuepunkten.

* Eine Aktivität des Typs **[!UICONTROL Kombinieren]** gruppiert Kundinnen und Kunden mit einer E-Mail und Kundinnen und Kunden, die einen Kauf in der Höhe von mindestens 100 $ getätigt haben.
* Eine Aktivität des Typs **[!UICONTROL Kombinieren]** schließt Kundinnen und Kunden mit weniger als 50 Treuepunkten aus.
* Eine Aktivität des Typs **[!UICONTROL E-Mail-Versand]** sendet eine E-Mail an die resultierenden Kundinnen und Kunden.

## Nächste Schritte {#next}

Nachdem Sie das Diagramm für die orchestrierte Kampagne erfolgreich erstellt haben, können Sie die orchestrierte Kampagne ausführen und den Fortschritt der verschiedenen Aufgaben verfolgen. [Erfahren Sie, wie Sie eine orchestrierte Kampagne starten und ihre Ausführung überwachen](start-monitor-campaigns.md)
