---
solution: Journey Optimizer
product: journey optimizer
title: Grundlegende Prinzipien der mehrstufigen Kampagnenerstellung
description: Grundlegende Prinzipien mehrstufiger Kampagnen mit Adobe Journey Optimizer kennenlernen
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 36%

---


# Grundlegende Prinzipien der mehrstufigen Kampagnenerstellung {#ms-campaign-creation}

Mit Adobe Journey Optimizer können Sie mehrstufige Kampagnen in eine visuelle Arbeitsfläche integrieren, um kanalübergreifende Prozesse wie Segmentierung, Kampagnenausführung und Dateiverarbeitung zu entwerfen.

## Was verbirgt sich in einer mehrstufigen Kampagne? {#gs-ms-campaign-inside}

Das mehrstufige Kampagnendiagramm zeigt, was passieren soll. Es beschreibt die verschiedenen Aufgaben, die ausgeführt und miteinander verknüpft werden sollen.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

Jede mehrstufige Kampagne enthält:

* **Aktivitäten**: Eine Aktivität ist eine Aufgabe, die ausgeführt werden soll. Die verschiedenen verfügbaren Aktivitäten werden im Diagramm durch Symbole dargestellt. Jede Aktivität verfügt über bestimmte Eigenschaften sowie andere Eigenschaften, die für alle Aktivitäten gelten.

  In einem mehrstufigen Kampagnendiagramm kann eine bestimmte Aktivität mehrere Aufgaben auslösen, insbesondere wenn eine Schleife oder wiederkehrende Aktionen vorliegen.

* **Transitionen**: Transitionen verknüpfen eine Quellaktivität mit einer Zielaktivität und definieren deren Sequenz.

* **Arbeitstabellen**: Die Arbeitstabelle enthält alle von der Transition übermittelten Informationen. Jede mehrstufige Kampagne verwendet mehrere Arbeitstabellen. Die in diesen Tabellen übermittelten Daten können während des gesamten Lebenszyklus einer mehrstufigen Kampagne verwendet werden.

## Wichtige Schritte zum Erstellen einer mehrstufigen Kampagne {#gs-ms-campaign-steps}

Die wichtigsten Schritte zum Erstellen einer mehrstufigen Kampagne sind:

![](assets/workflow-creation-process.png){zoomable="yes"}

