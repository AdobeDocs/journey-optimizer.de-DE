---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit orchestrierten Kampagnen
description: Erfahren Sie, wie Sie mit koordinierten Kampagnen beginnen
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: a8265a2e509df0f18db5d8ca36c4298ba020fa38
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 7%

---

# Erste Schritte mit orchestrierten Kampagnen {#orchestrated-camp}

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| <b>[Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)</b><br/><br/>[Konfigurationsschritte](configuration-steps.md)<br/><br/>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Wichtige Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[ Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Ausdrücke bearbeiten](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimension ändern](activities/change-dimension.md) - [Kanalaktivitäten](activities/channels.md) - [Kombinieren](activities/combine.md) - [Anreicherung](activities/deduplication.md) - [Formulare](activities/enrichment.md) - [Abstimmung](activities/fork.md) [&#128279;](activities/reconciliation.md) [&#128279;](activities/save-audience.md) [&#128279;](activities/split.md) ->Zielgruppe speichern[ -AufspaltungWarten](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Die Kampagnenorchestrierung in [!DNL Adobe Journey Optimizer] ermöglicht anspruchsvolle, markeninitiierte Marketing-Kampagnen über alle Kanäle hinweg und hilft Ihnen so, die Interaktion, den Umsatz und die Kundentreue im benötigten Umfang zu steigern.

Obwohl Cross-Channel-Marketing unerlässlich ist, machen orchestrierte Kampagnen es nahtlos. Mit einer visuellen Drag-and-Drop-Oberfläche können Sie komplexe Marketing-Workflows, von der Segmentierung bis zum Nachrichtenversand, über mehrere Kanäle entwerfen und automatisieren. Alles geschieht in einer intuitiven Umgebung, die auf Geschwindigkeit, Kontrolle und Effizienz ausgelegt ist.

![](assets/canvas-example-diagram.png){zoomable="yes"}

## Kernfunktionen

Die Kampagnenorchestrierung basiert auf vier zentralen Säulen:

<table>
<tr style="border: 0;">
<td><img alt="On-Demand-Zielgruppen" src="assets/do-not-localize/icon-audience.svg" width="50px"></a></td><td><b>On-Demand-Zielgruppen</b><br/> Führen Sie sofort Abfragen für mehrere Datensätze durch, um Zielgruppensegmente mithilfe einer beliebigen Kombination von Datentypen und Dimensionen zu erstellen.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentierung mehrerer Entitäten und Versand" src="assets/do-not-localize/icon-entity.svg" width="50px"></a></td><td><b>Segmentierung und Versand mehrerer Entitäten</b><br/>Gehen Sie über personenbasierte Kampagnen hinaus - verwenden Sie Entitäten wie Produktkataloge, Speicherorte oder Service-Daten, um sie präzise anzusprechen.</td></tr>
<tr style="border: 0;">
<td><img alt="Sichtbarkeit und Präzision vor dem Versand" src="assets/do-not-localize/icon-visibility.svg" width="50px"></a></td><td><b>Sichtbarkeit und Präzision vor dem Versand</b><br/> Erhalten Sie vor dem Start exakte Segmentierungszahlen und den vollständigen Kampagnenumfang, um Genauigkeit und Konfidenz sicherzustellen.</td></tr>
<tr style="border: 0;">
<td><img alt="Mehrstufige Kampagnen-Workflows" src="assets/do-not-localize/icon-multistep.svg" width="50px"></a></td><td><b>Mehrstufige Kampagnen-Workflows</b><br/> Entwerfen Sie mehrstufige Kampagnen, von täglichen Nachrichten bis hin zu komplexen Kampagnen wie saisonalen Werbeaktionen oder großen Produkteinführungen.</td></tr>
</table>

## Orchestrierte Kampagnen und Journey

Obwohl die koordinierte Kampagnenvisualisierung mit der von Journey-Kampagnen vergleichbar ist, werden damit verschiedene Zwecke und Anwendungsfälle gelöst:

* **Journey** - 1 bis 1 Arbeitsfläche, auf der jedes Profil die verschiedenen Schritte in seinem eigenen Tempo durchläuft. Der Status jedes Kunden wird innerhalb seines Kontexts beibehalten, um Echtzeit-Aktionen für den Trigger zu ermöglichen.

* **Orchestrierte Kampagnen** - Im Gegensatz zu Journeys verwenden orchestrierte Kampagnen eine Batch-Arbeitsfläche, die Segmente berechnet. Alle Profile werden gleichzeitig verarbeitet.

## Voraussetzungen

Bevor Sie mit orchestrierten Kampagnen arbeiten, müssen Sie unbedingt sicherstellen, dass Sie über die entsprechenden Berechtigungen verfügen. Der Zugriff auf orchestrierte Kampagnen ist auf Benutzer beschränkt, die einem relevanten **[!UICONTROL Produktprofil“ zugewiesen sind]** z. B. „Administrator für orchestrierte Kampagnen“, „Genehmigende Person für orchestrierte Kampagnen“, „Manager für orchestrierte Kampagnen“ oder „Betrachtende für orchestrierte Kampagnen“.

Wenn Sie nicht auf die Funktionen von orchestrierten Kampagnen zugreifen können, wenden Sie sich an Ihren Administrator, um die erforderlichen Berechtigungen anzufordern.

➡️ [Erfahren Sie mehr über Produktprofile im Zusammenhang mit orchestrierten Kampagnen](../administration/ootb-product-profiles.md)

## Tauchen wir tiefer in die Materie ein

Da Sie nun wissen, was koordinierte Kampagnen sind, ist es an der Zeit, sich näher mit den Dokumentationsabschnitten zu befassen, um mit der Funktion zu arbeiten.

&lt;table“><tr style="border: 0; text-align: center;">
<td>
<a href="gs-campaign-creation.md">
<img alt="Zugriff auf Workflows und deren Verwaltung" src="assets/do-not-localize/workflow-access.jpeg">
</a>
<div>
<a href="gs-campaign-creation.md"><strong>Konfigurationsschritte</strong></a>
</div>
<p>
</td>
<td>
<a href="create-orchestrated-campaign.md">
<img alt="Lead" src="assets/do-not-localize/workflow-create.jpeg">
</a>
<div><a href="create-orchestrated-campaign.md"><strong>Erstellen einer orchestrierten Kampagne</strong>
</div>
<p>
</td>
<td>
<a href="activities/about-activities.md">
<img alt="Gelegentlich" src="assets/do-not-localize/workflow-activities.jpeg">
</a>
<div>
<a href="activities/about-activities.md"><strong>Arbeiten mit Aktivitäten</strong></a>
</div>
<p></td>
</tr></table>
