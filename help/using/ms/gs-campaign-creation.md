---
solution: Journey Optimizer
product: journey optimizer
title: Grundlegende Prinzipien der koordinierten Kampagnenerstellung
description: Grundlegende Prinzipien koordinierter Kampagnen mit Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 26%

---

# Grundlegende Prinzipien {#ms-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Orchestrierte Kampagne"
>abstract="Auf diesem Bildschirm können Sie auf die vollständige Liste der orchestrierten Kampagnen zugreifen, ihren aktuellen Status und das letzte/nächste Ausführungsdatum überprüfen und eine neue orchestrierte Kampagne erstellen."

Mit Adobe Journey Optimizer können Sie orchestrierte Kampagnen in eine visuelle Arbeitsfläche integrieren, um kanalübergreifende Prozesse wie Segmentierung, Kampagnenausführung und Dateiverarbeitung zu entwerfen.

## Was verbirgt sich in einer orchestrierten Kampagne? {#gs-ms-campaign-inside}

Die orchestrierte Kampagnen-Arbeitsfläche ist eine Darstellung dessen, was passieren soll. Es beschreibt die verschiedenen Aufgaben, die ausgeführt und miteinander verknüpft werden sollen.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

Jede orchestrierte Kampagne enthält:

* **Aktivitäten**: Eine Aktivität ist eine Aufgabe, die ausgeführt werden soll. Die verschiedenen verfügbaren Aktivitäten werden im Diagramm durch Symbole dargestellt. Jede Aktivität verfügt über bestimmte Eigenschaften sowie andere Eigenschaften, die für alle Aktivitäten gelten.

  In einem orchestrierten Kampagnendiagramm kann eine bestimmte Aktivität mehrere Aufgaben hervorrufen, insbesondere wenn eine Schleife oder wiederkehrende Aktionen vorliegen.

* **Transitionen**: Transitionen verknüpfen eine Quellaktivität mit einer Zielaktivität und definieren deren Sequenz.

* **Arbeitstabellen**: Die Arbeitstabelle enthält alle von der Transition übermittelten Informationen. Jede koordinierte Kampagne verwendet mehrere Arbeitstabellen. Die in diesen Tabellen übermittelten Daten können während des gesamten Lebenszyklus der orchestrierten Kampagne verwendet werden.

## Wichtige Schritte zum Erstellen einer orchestrierten Kampagne {#gs-ms-campaign-steps}

Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne sind:

![](assets/workflow-creation-process.png){zoomable="yes"}

## Zugriff auf orchestrierte Kampagnen

Navigieren **[!UICONTROL im Menü]** zur Registerkarte Mehrstufige Kampagnen, um auf die vollständige Liste der orchestrierten Kampagnen zuzugreifen.

Jede orchestrierte Kampagne in der Liste zeigt Informationen über ihren aktuellen [Status](#status), das letzte Mal, wann sie ausgeführt oder geändert wurde, sowie das Datum und die Uhrzeit der nächsten geplanten Ausführung an.

Sie können die angezeigten Spalten anpassen, indem Sie auf das Symbol **[!UICONTROL Spalte für ein benutzerdefiniertes Layout konfigurieren]** in der oberen rechten Ecke der Liste klicken. Auf diese Weise können Sie zusätzliche Informationen zur Liste hinzufügen, z. B. die letzte fehlerhafte Aktivität für jede orchestrierte Kampagne oder die angewendete Zielgruppendimension.

Darüber hinaus stehen eine Suchleiste und Filter zur Verfügung, um die Suche innerhalb der Liste zu erleichtern. Sie können beispielsweise die orchestrierten Kampagnen so filtern, dass nur die Kampagnen angezeigt werden, die zu einer Kampagne gehören oder innerhalb eines bestimmten Datumsbereichs verarbeitet wurden.

Um eine orchestrierte Kampagne zu duplizieren oder zu löschen, klicken Sie auf die Schaltfläche mit den Auslassungspunkten und wählen Sie **[!UICONTROL Duplizieren]** oder **[!UICONTROL Löschen]**.

>[!NOTE]
>
>Wenn eine orchestrierte Kampagne in Bearbeitung ist, können Sie sie duplizieren, aber nicht löschen.

## Status und Lebenszyklus {#status}

Kampagnen können mehrere Status aufweisen:

* **[!UICONTROL Entwurf]**: Die koordinierte Kampagne wurde erstellt und gespeichert.
* **[!UICONTROL In]**: Die orchestrierte Kampagne wird derzeit ausgeführt.
* **[!UICONTROL Beendet]**: Die orchestrierte Kampagnenausführung ist abgeschlossen.
* **[!UICONTROL Ausgesetzt]**: Die orchestrierte Kampagne wurde angehalten.
* **[!UICONTROL Fehlerhaft]**: Bei der koordinierten Kampagne ist ein Fehler aufgetreten. Öffnen Sie die orchestrierte Kampagne und greifen Sie auf die Protokolle und Aufgaben zu, um den Fehler zu identifizieren und zu beheben.


## Erstellen einer Abfrage

## Personalization-Richtlinien
