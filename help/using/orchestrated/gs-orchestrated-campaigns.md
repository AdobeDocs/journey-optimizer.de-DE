---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit orchestrierten Kampagnen
description: Erfahren Sie, wie Sie mit koordinierten Kampagnen beginnen
short-description: Entdecken Sie die wichtigsten Funktionen und Anwendungsfälle einer koordinierten Kampagne.
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 86bd6a100644a0f50aa9e18fd7023dec11c05bfe
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 24%

---


# Erste Schritte mit orchestrierten Kampagnen {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="campaigns_overview_orchestrated"
>abstract="<b>Kampagnenorchestrierung</b><br/>Aufteilen, Kombinieren, Anreichern und Bearbeiten von relationalen Datensätzen zur Definition der Zielgruppe<br/><br/> <b>Nutzen von Daten mehrerer Entitäten</b><br/>Erfahren Sie, wie Sie mit orchestrierten Kampagnen relationale Datensätze nutzen können, um Daten für die Segmentierung und Personalisierung anzureichern<br/><br/><b>Ad-hoc-Segmentierung und genaue Zählungen</b><br/>Erstellen eines Segments Schritt für Schritt mit exakten Zahlen<br/><br/><b>Verfügbare Kanäle</b><br/>E-Mail, SMS, Push-Benachrichtigungen, Direkt-Mail"

Die Kampagnenorchestrierung in [!DNL Adobe Journey Optimizer] ermöglicht anspruchsvolle, markeninitiierte Marketing-Kampagnen über alle Kanäle hinweg und hilft Ihnen so, die Interaktion, den Umsatz und die Kundentreue im benötigten Umfang zu steigern.

Obwohl Cross-Channel-Marketing unerlässlich ist, machen orchestrierte Kampagnen es nahtlos. Mit einer visuellen Drag-and-Drop-Oberfläche können Sie komplexe Marketing-Workflows, von der Segmentierung bis zum Nachrichtenversand, über mehrere Kanäle entwerfen und automatisieren. Alles geschieht in einer intuitiven Umgebung, die auf Geschwindigkeit, Kontrolle und Effizienz ausgelegt ist.

![](assets/canvas-example-diagram.png){zoomable="yes"}

## Kernfunktionen

Die Kampagnenorchestrierung basiert auf vier zentralen Säulen:

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="On-Demand-Zielgruppen" src="assets/do-not-localize/icon-audience.svg" width="150px"></a></td><td><b>On-Demand-Zielgruppen</b><br/> Führen Sie sofort Abfragen für mehrere Datensätze durch, um Zielgruppensegmente mithilfe einer beliebigen Kombination von Datentypen und Dimensionen zu erstellen.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentierung mehrerer Entitäten und Versand" src="assets/do-not-localize/icon-entity.svg" width="150px"></a></td><td><b>Segmentierung und Versand mehrerer Entitäten</b><br/>Gehen Sie über personenbasierte Kampagnen hinaus - verwenden Sie Entitäten wie Produktkataloge, Speicherorte oder Service-Daten, um sie präzise anzusprechen.<br/><br/>
Unterstützt den Versand auf mehreren Ebenen, bei dem pro Profil und zugehöriger sekundärer Entität eine Nachricht gesendet wird. Zu diesen sekundären Entitäten können Kontaktadressen, Buchungen, Abonnements, Verträge oder andere verknüpfte Daten gehören. Dies ermöglicht beispielsweise den Versand von Kampagnen an alle bekannten Adressen eines Profils oder für jede mit diesem Profil verknüpfte Buchung.</td></tr>
<tr style="border: 0;">
<td><img alt="Sichtbarkeit und Präzision vor dem Versand" src="assets/do-not-localize/icon-visibility.svg" width="150px"></a></td><td><b>Sichtbarkeit und Präzision vor dem Versand</b><br/> Erhalten Sie vor dem Start exakte Segmentierungszahlen und den vollständigen Kampagnenumfang, um Genauigkeit und Konfidenz sicherzustellen.</td></tr>
<tr style="border: 0;">
<td><img alt="Mehrstufige Kampagnen-Workflows" src="assets/do-not-localize/icon-multistep.svg" width="150px"></a></td><td><b>Mehrstufige Kampagnen-Workflows</b><br/> Entwerfen Sie mehrstufige Kampagnen, von täglichen Nachrichten bis hin zu komplexen Kampagnen wie saisonalen Werbeaktionen oder großen Produkteinführungen.</td></tr>
</table>

## Orchestrierte Kampagnen und Journey

Obwohl die Visualisierung in „Orchestrierte Kampagnen“ mit der von Journey-Kampagnen vergleichbar ist, werden damit verschiedene Zwecke und Anwendungsfälle gelöst:

* **Journey** - 1 bis 1 Arbeitsfläche, auf der jedes Profil die verschiedenen Schritte in seinem eigenen Tempo durchläuft. Der Status jedes Kunden wird innerhalb seines Kontexts beibehalten, um Echtzeit-Aktionen für den Trigger zu ermöglichen.

* **Orchestrierte Kampagnen** - Im Gegensatz zu Journey verwenden orchestrierte Kampagnen eine Batch-Arbeitsfläche, die Segmente berechnet. Alle Profile werden gleichzeitig verarbeitet.

Beide Arbeitsflächen sind für ihre jeweiligen Anwendungsfälle optimiert: Die Journey-Arbeitsfläche veröffentlicht Journey, die in der Regel länger leben, während die Campaign-Arbeitsfläche für iterative und inkrementelle Ausführungen einer Batch-Kampagne entwickelt wurde.

## Was verbirgt sich in einer orchestrierten Kampagne? {#gs-ms-campaign-inside}

Die Arbeitsfläche der orchestrierten Kampagne ist eine Darstellung dessen, was passieren soll. Sie beschreibt die verschiedenen Aufgaben, die ausgeführt und miteinander verknüpft werden sollen.

![Bild mit einer orchestrierten Kampagnen-Arbeitsfläche](assets/canvas-example.png)

Jede orchestrierte Kampagne enthält:

* **Aktivitäten**: Eine Aktivität ist eine Aufgabe, die ausgeführt werden soll. Die verschiedenen verfügbaren Aktivitäten werden im Diagramm durch Symbole dargestellt. Jede Aktivität verfügt über bestimmte Eigenschaften sowie andere Eigenschaften, die für alle Aktivitäten gelten.

  In einem orchestrierten Kampagnendiagramm kann eine bestimmte Aktivität mehrere Aufgaben hervorrufen, insbesondere wenn eine Schleife oder wiederkehrende Aktionen vorliegen.

* **Transitionen**: Transitionen verknüpfen eine Quellaktivität mit einer Zielaktivität und definieren deren Sequenz.

* **Arbeitstabellen**: Die Arbeitstabelle enthält alle von der Transition übermittelten Informationen. Jede koordinierte Kampagne verwendet mehrere Arbeitstabellen. Die in diesen Tabellen übermittelten Daten können während des gesamten Lebenszyklus der koordinierten Kampagne verwendet werden.

## Tauchen wir tiefer in die Materie ein

Da Sie nun wissen, was koordinierte Kampagnen sind, ist es an der Zeit, sich näher mit den Dokumentationsabschnitten zu befassen, um mit der Funktion zu arbeiten.

<table><tr style="border: 0; text-align: center;">
<td>
<a href="gs-campaign-creation.md">
<img alt="Zugreifen auf und Verwalten von Kampagnen" src="assets/do-not-localize/workflow-access.jpeg">
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
