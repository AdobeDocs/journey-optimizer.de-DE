---
solution: Journey Optimizer
product: journey optimizer
title: Grundlegende Prinzipien der mehrstufigen Kampagnenerstellung
description: Grundlegende Prinzipien mehrstufiger Kampagnen mit Adobe Journey Optimizer kennenlernen
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 271c4739a5537a99da981913606bc9eb099b5139
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 28%

---

# Grundlegende Prinzipien einer koordinierten Kampagne {#ms-campaign-creation}

Mit Adobe Journey Optimizer können Sie mehrstufige Kampagnen in eine visuelle Arbeitsfläche integrieren, um kanalübergreifende Prozesse wie Segmentierung, Kampagnenausführung und Dateiverarbeitung zu entwerfen.

## Erstellen einer Abfrage

## Personalization-Richtlinien

## Was verbirgt sich in einer mehrstufigen Kampagne? {#gs-ms-campaign-inside}

Die mehrstufige Kampagnen-Arbeitsfläche ist eine Darstellung dessen, was passieren soll. Es beschreibt die verschiedenen Aufgaben, die ausgeführt und miteinander verknüpft werden sollen.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

Jede mehrstufige Kampagne enthält:

* **Aktivitäten**: Eine Aktivität ist eine Aufgabe, die ausgeführt werden soll. Die verschiedenen verfügbaren Aktivitäten werden im Diagramm durch Symbole dargestellt. Jede Aktivität verfügt über bestimmte Eigenschaften sowie andere Eigenschaften, die für alle Aktivitäten gelten.

  In einem mehrstufigen Kampagnendiagramm kann eine bestimmte Aktivität mehrere Aufgaben auslösen, insbesondere wenn eine Schleife oder wiederkehrende Aktionen vorliegen.

* **Transitionen**: Transitionen verknüpfen eine Quellaktivität mit einer Zielaktivität und definieren deren Sequenz.

* **Arbeitstabellen**: Die Arbeitstabelle enthält alle von der Transition übermittelten Informationen. Jede mehrstufige Kampagne verwendet mehrere Arbeitstabellen. Die in diesen Tabellen übermittelten Daten können während des gesamten Lebenszyklus einer mehrstufigen Kampagne verwendet werden.

## Wichtige Schritte zum Erstellen einer mehrstufigen Kampagne {#gs-ms-campaign-steps}

Die wichtigsten Schritte zum Erstellen einer mehrstufigen Kampagne sind:

![](assets/workflow-creation-process.png){zoomable="yes"}

## Status und Lebenszyklus

Kampagnen können mehrere Status aufweisen:

* **[!UICONTROL Entwurf]**: Die mehrstufige Kampagne wurde erstellt und gespeichert.
* **[!UICONTROL In Bearbeitung]**: Die mehrstufige Kampagne wird derzeit ausgeführt.
* **[!UICONTROL Beendet]**: Die mehrstufige Kampagnenausführung ist abgeschlossen.
* **[!UICONTROL Ausgesetzt]**: Die mehrstufige Kampagne wurde angehalten.
* **[!UICONTROL Fehlerhaft]**: Bei der mehrstufigen Kampagne ist ein Fehler aufgetreten. Öffnen Sie die mehrstufige Kampagne und greifen Sie auf die Protokolle und Aufgaben zu, um den Fehler zu identifizieren und zu beheben.

