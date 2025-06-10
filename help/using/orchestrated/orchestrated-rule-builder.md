---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit dem Regel-Builder
description: Erfahren Sie, wie Sie Regeln für Ihre koordinierten Kampagnen erstellen
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 6574735581de0872e78e8e05efea5c6a50dc59b1
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 19%

---


# Arbeiten mit dem Regel-Builder {#orchestrated-rule-builder}

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten der ersten orchestrierten Kampagne | Abfragen der Datenbank | Orchestrierte Kampagnenaktivitäten |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](configuration-steps.md)<br/><br/>[Zugreifen auf und Verwalten von orchestrierten Kampagnen](access-manage-orchestrated-campaigns.md) | [Wichtige Schritte für die orchestrierte Kampagnenerstellung](gs-campaign-creation.md)<br/><br/>[Erstellen und konfigurieren Sie die ](create-orchestrated-campaign.md)<br/><br/>[-Aktivitäten](orchestrate-activities.md)<br/><br/>[ Senden Sie Nachrichten mit orchestrierten Kampagnen](send-messages.md)<br/><br/>[Starten und überwachen Sie die Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | <b>[Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)</b><br/><br/>[Erstellen Sie Ihre ersten ](build-query.md)<br/><br/>[-Bearbeitungsausdrücke](edit-expressions.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimensionsänderung](activities/change-dimension.md) - [Kombinieren](activities/combine.md) - [Deduplizierung](activities/enrichment.md) - [Verzweigung](activities/fork.md) - [Abstimmung](activities/reconciliation.md) - [Aufspaltung](activities/split.md)[ ](activities/wait.md) Warten](activities/deduplication.md) [ |

{style="table-layout:fixed"}

+++

<br/>

Orchestrierte Kampagnen enthalten einen Regel-Builder, der den Prozess der Filterung der Datenbank anhand verschiedener Kriterien vereinfacht. Der Regel-Builder verwaltet sehr komplexe und lange Abfragen effizient und bietet somit mehr Flexibilität und Präzision.

Außerdem werden vordefinierte Filter in Bedingungen unterstützt, sodass Sie Ihre Abfragen mühelos präzisieren und gleichzeitig erweiterte Ausdrücke und Operatoren für umfassende Zielgruppen-Targeting- und Segmentierungsstrategien nutzen können.

## Zugriff auf den Regel-Builder

Der Regel-Builder ist beim Erstellen einer Abfrage in einer Aktivität **[!UICONTROL Zielgruppe erstellen]** verfügbar, um eine Zielgruppe anzusprechen. Damit können Sie die Population angeben, die Sie ansprechen möchten, und mühelos neue Zielgruppen erstellen, die auf Ihre Bedürfnisse zugeschnitten sind.

![Bild mit der Aktivität „Zielgruppe aufbauen“](assets/rule-builder-query.png)

## Benutzeroberfläche des Regel-Builders {#interface}

Der Regel-Builder bietet eine zentrale Arbeitsfläche, auf der Sie Ihre Abfrage erstellen, und einen Eigenschaftenbereich mit Informationen zur Regel.

![Bild mit der Benutzeroberfläche des Regel-Builders](assets/rule-builder-interface.png)

* Auf der **zentralen Arbeitsfläche** fügen Sie die verschiedenen Komponenten hinzu und kombinieren sie, um Ihre Regel zu erstellen. [Erfahren Sie, wie Sie eine Regel erstellen](../orchestrated/build-query.md)

* Der Bereich **[!UICONTROL Regeleigenschaften]** enthält Informationen zu Ihrer Regel. Damit können Sie verschiedene Vorgänge durchführen, um die Regel zu überprüfen und sicherzustellen, dass sie Ihren Anforderungen entspricht.

  Dieser Bereich wird angezeigt, wenn Sie eine Abfrage zum Erstellen einer Zielgruppe erstellen. [So überprüfen und validieren Sie Ihre Abfrage](build-query.md#check-and-validate-your-query)
