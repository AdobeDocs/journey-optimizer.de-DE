---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit dem Regel-Builder
description: Erfahren Sie, wie Sie Regeln für Ihre koordinierten Kampagnen erstellen
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 77%

---


# Arbeiten mit dem Regel-Builder {#orchestrated-rule-builder}

+++ Inhaltsverzeichnis

| Willkommen bei orchestrierten Kampagnen | Starten der ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | <b>[Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)</b><br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Bearbeiten von Ausdrücken](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) – [Zielgruppe erstellen](activities/build-audience.md) – [Dimensionsänderung](activities/change-dimension.md) – [Kanalaktivitäten](activities/channels.md) – [Kombinieren](activities/combine.md) – [Deduplizierung](activities/deduplication.md) – [Anreicherung](activities/enrichment.md) – [Verzweigung](activities/fork.md) – [Abstimmung](activities/reconciliation.md) – [Zielgruppe speichern](activities/save-audience.md) – [Aufspaltung](activities/split.md) – [Warten](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Orchestrierte Kampagnen enthalten einen Regel-Builder, der den Prozess der Filterung der Datenbank anhand verschiedener Kriterien vereinfacht. Der Regel-Builder verwaltet sehr komplexe und lange Abfragen effizient und bietet dabei erhöhte Flexibilität und Genauigkeit. 

Außerdem unterstützt er vordefinierte Filter in Bedingungen, sodass Sie Ihre Abfragen mühelos präzisieren und gleichzeitig erweiterte Ausdrücke und Operatoren für umfassende Zielgruppen-Targeting- und Segmentierungsstrategien nutzen können.

## Zugreifen auf den Regel-Builder

Der Abfrage-Modeler ist in jedem Kontext verfügbar, in dem Sie Regeln zum Filtern von Daten definieren müssen.

| Nutzung | Beispiel |
|  ---  |  ---  |
| **Zielgruppen erstellen**: Geben Sie mit der Aktivität Zielgruppe erstellen die Population an, die Sie in Ihren orchestrierten Kampagnen ansprechen möchten **[!UICONTROL und]** mühelos neue Zielgruppen erstellen, die auf Ihre Bedürfnisse zugeschnitten sind. [Weitere Informationen zum Erstellen von Zielgruppen](../orchestrated/activities/build-audience.md) | ![Bild, das den Zugriff auf die Benutzeroberfläche zur Zielgruppenerstellung zeigt](assets/query-access-audience.png){width="200" align="center" zoomable="yes"} |
| **Erstellen einer Bedingung auf der Kampagnenarbeitsfläche**: Wenden Sie auf der Kampagnenarbeitsfläche mithilfe einer Aktivität des Typs **[!UICONTROL Aufspaltung]** Regeln an, um Anpassungen an Ihre bestimmten Anforderungen vorzunehmen. [Weitere Informationen zur Verwendung der Aktivität „Aufspaltung“](../orchestrated/activities/split.md) | ![Bild, das den Zugriff auf Optionen zur Workflow-Anpassung zeigt](assets/query-access-split.png){width="200" align="center" zoomable="yes"} |
| **Erstellen erweiterter Filter**: Erstellen Sie Regeln, um die in Listen angezeigten Daten wie Workflow-Protokolle oder Zielgruppendimensionen zu filtern. | ![Bild, das die Anpassung von Listenfiltern zeigt](assets/query-access-advanced-filters.png){width="200" align="center" zoomable="yes"} |

## Oberfläche des Regel-Builders {#interface}

Der Regel-Builder bietet eine zentrale Arbeitsfläche zum Erstellen Ihrer Abfrage sowie einen Eigenschaftenbereich mit Informationen zu Ihrer Regel.

![Bild, das die Oberfläche des Regel-Builders zeigt](assets/rule-builder-interface.png)

* Auf der **zentralen Arbeitsfläche** können Sie verschiedenen Komponenten zum Erstellen Ihrer Regel hinzufügen und kombinieren. [Weitere Informationen zur Erstellung einer Regel](../orchestrated/build-query.md)

* Der Bereich **[!UICONTROL Regeleigenschaften]** enthält Informationen zu Ihrer Regel. Hier können Sie verschiedene Vorgänge ausführen, um Ihre Regel zu überprüfen und sicherzustellen, dass sie Ihren Anforderungen entspricht.

  Dieser Bereich wird angezeigt, wenn Sie eine Abfrage zum Erstellen einer Zielgruppe erstellen. [So überprüfen und validieren Sie Ihre Abfrage](build-query.md#check-and-validate-your-query)
