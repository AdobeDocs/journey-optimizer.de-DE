---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit dem Regel-Builder
description: Erfahren Sie, wie Sie Regeln für Ihre koordinierten Kampagnen erstellen
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 21%

---


# Arbeiten mit dem Regel-Builder {#orchestrated-rule-builder}

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[ Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | <b>[Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)</b><br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Ausdrücke bearbeiten](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimension ändern](activities/change-dimension.md) - [Kanalaktivitäten](activities/channels.md) - [Kombinieren](activities/combine.md) - [Anreicherung](activities/deduplication.md) - [Formulare](activities/enrichment.md) - [Abstimmung](activities/fork.md) [&#128279;](activities/reconciliation.md) [&#128279;](activities/save-audience.md) [&#128279;](activities/split.md) ->Zielgruppe speichern[ -AufspaltungWarten](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Orchestrierte Kampagnen enthalten einen Regel-Builder, der den Prozess der Filterung der Datenbank anhand verschiedener Kriterien vereinfacht. Der Regel-Builder verwaltet sehr komplexe und lange Abfragen effizient und bietet somit mehr Flexibilität und Präzision.

Es unterstützt auch vordefinierte Filter innerhalb von Bedingungen und ermöglicht es Ihnen, Abfragen mühelos zu verfeinern und gleichzeitig erweiterte Ausdrücke und Operatoren für umfassende Zielgruppen-Targeting- und Segmentierungsstrategien zu verwenden.

## Zugriff auf den Regel-Builder

Der Abfrage-Modeler ist in jedem Kontext verfügbar, in dem Sie Regeln zum Filtern von Daten definieren müssen.

| Nutzung | Beispiel |
|  ---  |  ---  |
| **Zielgruppen erstellen**: Geben Sie mit der Aktivität Zielgruppe erstellen die Population an, die Sie in Ihren orchestrierten Kampagnen ansprechen möchten **[!UICONTROL und]** mühelos neue Zielgruppen erstellen, die auf Ihre Bedürfnisse zugeschnitten sind. [Weitere Informationen zum Erstellen von Zielgruppen](../orchestrated/activities/build-audience.md) | ![Bild, das den Zugriff auf die Benutzeroberfläche zur Zielgruppenerstellung zeigt](assets/query-access-audience.png){width="200" align="center" zoomable="yes"} |
| **Bedingung auf der Kampagnen-Arbeitsfläche erstellen**: Wenden Sie Regeln auf der Kampagnen-Arbeitsfläche mithilfe einer **[!UICONTROL Aufspaltung]**-Aktivität an, um sie an Ihre spezifischen Anforderungen anzupassen. [Erfahren Sie, wie Sie eine Aufspaltungsaktivität verwenden](../orchestrated/activities/split.md) | ![Bild, das den Zugriff auf Optionen zur Workflow-Anpassung zeigt](assets/query-access-split.png){width="200" align="center" zoomable="yes"} |
| **Erweiterte Filter erstellen** Regeln erstellen, um die in Listen angezeigten Daten wie Workflow-Protokollen oder Zielgruppendimensionen zu filtern. | ![Bild, das die Anpassung von Listenfiltern zeigt](assets/query-access-advanced-filters.png){width="200" align="center" zoomable="yes"} |

## Benutzeroberfläche des Regel-Builders {#interface}

Der Regel-Builder bietet eine zentrale Arbeitsfläche, auf der Sie Ihre Abfrage erstellen, und einen Eigenschaftenbereich mit Informationen zur Regel.

![Bild mit der Benutzeroberfläche des Regel-Builders](assets/rule-builder-interface.png)

* Auf der **zentralen Arbeitsfläche** fügen Sie die verschiedenen Komponenten hinzu und kombinieren sie, um Ihre Regel zu erstellen. [Erfahren Sie, wie Sie eine Regel erstellen](../orchestrated/build-query.md)

* Der Bereich **[!UICONTROL Regeleigenschaften]** enthält Informationen zu Ihrer Regel. Damit können Sie verschiedene Vorgänge durchführen, um die Regel zu überprüfen und sicherzustellen, dass sie Ihren Anforderungen entspricht.

  Dieser Bereich wird angezeigt, wenn Sie eine Abfrage zum Erstellen einer Zielgruppe erstellen. [So überprüfen und validieren Sie Ihre Abfrage](build-query.md#check-and-validate-your-query)
