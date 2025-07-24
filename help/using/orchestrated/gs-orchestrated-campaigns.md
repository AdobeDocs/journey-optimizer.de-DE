---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit orchestrierten Kampagnen
description: Informationen zu den ersten Schritten mit orchestrierten Kampagnen
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 15f5fdfde0e9f7c93739a624918838dbd6787833
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 19%

---

# Erste Schritte mit orchestrierten Kampagnen {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="Orchestrierte Kampagnen"
>abstract="**Kampagnenorchestrierung**<br/> Aufspaltung, Kombination, Anreicherung und Manipulation von relationalen Datensätzen, um Ihre Audience zu definieren<br/><br/>"

**Nutzen von Daten mehrerer Entitäten**<br/> Erfahren Sie, wie orchestrierte Kampagnen relationale Datensätze nutzen können, um Daten für die Segmentierung und Personalisierung anzureichern <br/><br/>**Ad-hoc-Segmentierung und genaue Zählungen**<br/> Erstellen Sie Ihr Segment Schritt für Schritt mit genauen Zählungen <br/><br/>**Verfügbare Kanäle**<br/> E-Mail, SMS, Push-Benachrichtigungen, Briefpost“

+++ Inhaltsverzeichnis

| Willkommen bei orchestrierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| <b>[Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)</b><br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Bearbeiten von Ausdrücken](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) – [Zielgruppe erstellen](activities/build-audience.md) – [Dimensionsänderung](activities/change-dimension.md) – [Kanalaktivitäten](activities/channels.md) – [Kombinieren](activities/combine.md) – [Deduplizierung](activities/deduplication.md) – [Anreicherung](activities/enrichment.md) – [Verzweigung](activities/fork.md) – [Abstimmung](activities/reconciliation.md) – [Zielgruppe speichern](activities/save-audience.md) – [Aufspaltung](activities/split.md) – [Warten](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Die Kampagnenorchestrierung in [!DNL Adobe Journey Optimizer] ermöglicht anspruchsvolle, markeninitiierte Marketing-Kampagnen über alle Kanäle hinweg und hilft Ihnen so, die Interaktion, den Umsatz und die Kundentreue im benötigten Umfang zu steigern.

Obwohl Cross-Channel-Marketing unerlässlich ist, machen orchestrierte Kampagnen es nahtlos. Mit einer visuellen Drag-and-Drop-Oberfläche können Sie komplexe Marketing-Workflows, von der Segmentierung bis zum Nachrichtenversand, über mehrere Kanäle entwerfen und automatisieren. Alles geschieht in einer intuitiven Umgebung, die auf Geschwindigkeit, Kontrolle und Effizienz ausgelegt ist.

![](assets/canvas-example-diagram.png){zoomable="yes"}

## Kernfunktionen

Die Kampagnenorchestrierung basiert auf vier zentralen Säulen:

<table style="table-layout:auto">
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

<table><tr style="border: 0; text-align: center;">
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
