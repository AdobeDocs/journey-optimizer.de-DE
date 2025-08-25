---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit orchestrierten Kampagnen
description: Informationen zu den ersten Schritten mit orchestrierten Kampagnen
short-description: Entdecken Sie wichtige Funktionen und Anwendungsfälle von orchestrierten Kampagnen.
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 4510cfde1579fbabe7deb1289f70f13ee21a3d4a
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 100%

---


# Erste Schritte mit orchestrierten Kampagnen {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="campaigns_overview_orchestrated"
>abstract="<b>Kampagnenorchestrierung</b><br/>Aufteilen, Kombinieren, Anreichern und Bearbeiten von relationalen Datensätzen zur Definition der Zielgruppe<br/><br/> <b>Nutzen von Daten mehrerer Entitäten</b><br/>Erfahren Sie, wie Sie mit orchestrierten Kampagnen relationale Datensätze nutzen können, um Daten für die Segmentierung und Personalisierung anzureichern<br/><br/><b>Ad-hoc-Segmentierung und genaue Zählungen</b><br/>Erstellen eines Segments Schritt für Schritt mit exakten Zahlen<br/><br/><b>Verfügbare Kanäle</b><br/>E-Mail, SMS, Push-Benachrichtigungen, Direkt-Mail"

Die Kampagnenorchestrierung in [!DNL Adobe Journey Optimizer] ermöglicht kanalübergreifend anspruchsvolle, markeninitiierte Marketing-Kampagnen und hilft Ihnen so, die Interaktion, den Umsatz und die Kundentreue im gewünschten Umfang zu fördern.

>[!IMPORTANT]
>
>Für einen Zugriff auf die Kampagnenorchestrierung muss die Lizenz entweder das Paket **Journey Optimizer – Kampagnen und Journeys** oder das Paket **Journey Optimizer – Kampagnen** enthalten. Wenden Sie sich an den Adobe-Support, um Ihre Lizenz zu bestätigen und bei Bedarf zu aktualisieren.

Kanalübergreifendes Marketing ist unerlässlich, und orchestrierte Kampagnen machen es nahtlos. Auf einer visuellen Drag-and-Drop-Oberfläche können Sie komplexe Marketing-Workflows, von der Segmentierung bis hin zum Nachrichtenversand, über mehrere Kanäle hinweg entwerfen und automatisieren. Alles geschieht in einer intuitiven Umgebung, die auf Geschwindigkeit, Kontrolle und Effizienz ausgelegt ist.

![](assets/canvas-example-diagram.png){zoomable="yes"}

## Kernfunktionen

Die Kampagnenorchestrierung basiert auf vier zentralen Säulen:

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="On-Demand-Zielgruppen" src="assets/do-not-localize/icon-audience.svg" width="150px"></a></td><td><b>On-Demand-Zielgruppen</b><br/>: Führen Sie sofort Abfragen für mehrere Datensätze durch, um Zielgruppensegmente mithilfe einer beliebigen Kombination von Datentypen und Dimensionen zu erstellen.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentierung und Versand mehrerer Entitäten" src="assets/do-not-localize/icon-entity.svg" width="150px"></a></td><td><b>Segmentierung und Versand mehrerer Entitäten</b><br/>: Gehen Sie über personenbasierte Kampagnen hinaus – nutzen Sie für präzises Targeting Entitäten wie Produktkataloge, Speicherorte oder Service-Daten.<br/><br/>
Unterstützt den Versand auf mehreren Ebenen, bei dem pro Profil und zugehöriger sekundärer Entität eine Nachricht gesendet wird. Zu diesen sekundären Entitäten können Kontaktadressen, Buchungen, Abonnements, Verträge oder andere verknüpfte Daten gehören. Dies ermöglicht beispielsweise den Versand von Kampagnen an alle bekannten Adressen eines Profils oder für jede mit dem betreffenden Profil verknüpfte Buchung.</td></tr>
<tr style="border: 0;">
<td><img alt="Sichtbarkeit und Präzision vor dem Versand" src="assets/do-not-localize/icon-visibility.svg" width="150px"></a></td><td><b>Sichtbarkeit und Präzision vor dem Versand</b><br/>: Erhalten Sie vor dem Start exakte Segmentierungszahlen und den vollständigen Kampagnenumfang, um Genauigkeit und Konfidenz sicherzustellen.</td></tr>
<tr style="border: 0;">
<td><img alt="Mehrstufige Kampagnen-Workflows" src="assets/do-not-localize/icon-multistep.svg" width="150px"></a></td><td><b>Mehrstufige Kampagnen-Workflows</b><br/>: Entwerfen Sie mehrstufige Kampagnen, von täglichen Nachrichten bis hin zu komplexen Kampagnen wie saisonalen Werbeaktionen oder umfangreichen Produkteinführungen.</td></tr>
</table>

## Orchestrierte Kampagnen und Journeys

Obwohl die Visualisierung in „Orchestrierte Kampagnen“ mit der von Journey-Kampagnen vergleichbar ist, werden damit verschiedene Zwecke verfolgt und Anwendungsfälle gelöst:

* **Journeys** – 1-zu-1-Arbeitsfläche, wobei jedes Profil die verschiedenen Schritte in seinem eigenen Tempo durchläuft. Der Status jeder Kundin und jedes Kunden wird innerhalb seines Kontexts beibehalten, was das Auslösen von Echtzeit-Aktionen ermöglicht.

* **Orchestrierte Kampagnen** – Im Gegensatz zu Journeys nutzen orchestrierte Kampagnen eine Batch-Arbeitsfläche, die Segmente berechnet. Alle Profile werden gleichzeitig verarbeitet.

Beide Arbeitsflächen sind für ihre jeweiligen Anwendungsfälle optimiert: Die Journey-Arbeitsfläche veröffentlicht Journeys, die in der Regel länger existieren, während die Campaign-Arbeitsfläche für iterative und inkrementelle Ausführungen einer Batch-Kampagne entwickelt wurde.

## Inhalt einer orchestrierten Kampagne {#gs-ms-campaign-inside}

Die Arbeitsfläche für orchestrierte Kampagnen zeigt, was passieren soll. Sie beschreibt die verschiedenen Aufgaben, die ausgeführt und miteinander verknüpft werden sollen.

![Bild, das die Arbeitsfläche für orchestrierte Kampagnen zeigt](assets/canvas-example.png)

Jede orchestrierte Kampagne enthält:

* **Aktivitäten**: Eine Aktivität ist eine Aufgabe, die ausgeführt werden soll. Die verschiedenen verfügbaren Aktivitäten werden im Diagramm durch Symbole dargestellt. Jede Aktivität verfügt über bestimmte Eigenschaften sowie andere Eigenschaften, die für alle Aktivitäten gelten.

  In einem Diagramm einer orchestrierten Kampagne kann eine bestimmte Aktivität verschiedene Aufgaben auslösen, insbesondere wenn Schleifen oder wiederkehrende Aktionen vorhanden sind.

* **Transitionen**: Transitionen verknüpfen eine Quellaktivität mit einer Zielaktivität und definieren deren Sequenz.

* **Arbeitstabellen**: Die Arbeitstabelle enthält alle von der Transition übermittelten Informationen. Jede orchestrierte Kampagne nutzt mehrere Arbeitstabellen. Die in diesen Tabellen enthaltenen Daten können während des gesamten Lebenszyklus der orchestrierten Kampagne verwendet werden.

## Tauchen wir tiefer in die Materie ein

Jetzt, da Sie über Grundkenntnisse zu orchestrierten Kampagnen verfügen, ist es an der Zeit, diese Dokumentationsabschnitte zu vertiefen und mit der Funktion zu arbeiten.

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
