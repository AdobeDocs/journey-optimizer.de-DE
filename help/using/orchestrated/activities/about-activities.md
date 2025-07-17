---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit orchestrierten Kampagnenaktivitäten
description: Erfahren Sie, wie Sie Kampagnenaktivitäten koordinieren
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: 1aa4f3e24a4cb7594232c0b25da8c9fd2e62c1de
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 42%

---

# Über orchestrierte Kampagnenaktivitäten {#orchestrated-campaign-activities}


+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul><br/><br/>[Zugreifen auf und Verwalten von orchestrierten Kampagnen](../access-manage-orchestrated-campaigns.md) | [Wichtige Schritte zum Erstellen einer orchestrierten Kampagne](../gs-campaign-creation.md)<br/><br/>[Erstellen und Planen der Kampagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](../orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](../orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](../build-query.md)<br/><br/>[Ausdrücke bearbeiten](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | <b>[Erste Schritte mit Aktivitäten](about-activities.md)</b><br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) - [Zielgruppe aufbauen](build-audience.md) - [Dimension ändern](change-dimension.md) - [Kanalaktivitäten](channels.md) - [Kombinieren](combine.md) - [Anreicherung](deduplication.md) - [Formulare](enrichment.md) - [Abstimmung](fork.md) [&#128279;](reconciliation.md) [&#128279;](save-audience.md) [&#128279;](split.md) ->Zielgruppe speichern[ -AufspaltungWarten](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Orchestrierte Kampagnenaktivitäten werden in drei Kategorien unterteilt. Je nach Kontext können die verfügbaren Aktivitäten unterschiedlich sein.

Alle Aktivitäten werden in den folgenden Abschnitten beschrieben:

* [Aktivitäten zur Zielgruppenbestimmung](#targeting)
* [Kanalaktivitäten](#channel)
* [Aktivitäten zur Flusssteuerung](#flow-control)

![Liste der auf der Arbeitsfläche verfügbaren Aktivitäten](../assets/orchestrated-activities.png){width="80%" align="left"}

## Aktivitäten zur Zielgruppenbestimmung {#targeting}

Diese Aktivitäten sind spezifisch für die Zielgruppenbestimmung. Sie ermöglichen es Ihnen, ein oder mehrere Ziele zu erstellen, indem Sie eine Zielgruppe definieren und diese Zielgruppen mithilfe von Schnittmenge, Vereinigung oder Ausschluss aufteilen oder kombinieren.

![Liste der Zielgruppenaktivitäten](../assets/targeting-activities.png){width="40%" align="left"}

* [Zielgruppe erstellen](build-audience.md): Mit dieser Aktivität definieren Sie Ihre Zielpopulation. Sie können entweder eine bestehende Zielgruppe auswählen oder den Abfrage-Modeler verwenden, um Ihre eigene Abfrage zu definieren.
* [Dimensionsänderung](change-dimension.md): Ändern Sie die Zielgruppendimension beim Erstellen Ihrer orchestrierten Kampagne.
* [Kombinieren](combine.md): Mit dieser Aktivität segmentieren Sie Ihre eingehende Population. Sie können eine Vereinigung, eine Schnittmenge oder einen Ausschluss verwenden.
* [Deduplizierung](deduplication.md): Mit dieser Aktivität löschen Sie Dubletten in Ergebnissen aus eingehenden Aktivitäten.
* [Anreicherung](enrichment.md): Definieren Sie zusätzliche Daten, die in Ihrer orchestrierten Kampagne verarbeitet werden sollen. Mit dieser Aktivität können Sie die eingehende Transition nutzen und die Aktivität so konfigurieren, dass sie die ausgehende Transition mit zusätzlichen Daten ergänzt.
* [Abstimmung](reconciliation.md) Definieren Sie die Relation zwischen den Daten in Journey Optimizer und den Daten in einer Arbeitstabelle, z. B. Daten aus einer externen Datei.
* [Aufspaltung](split.md): Segmentieren Sie die eingehende Population in mehrere Teilmengen.

## Kanalaktivitäten {#channel}

Mit Adobe Journey Optimizer können Sie Marketing-Kampagnen über mehrere Kanäle hinweg automatisieren und ausführen. Sie können Kanalaktivitäten in der Arbeitsfläche kombinieren, um eine kanalübergreifende orchestrierte Kampagne zu erstellen, mit der Trigger-Aktionen basierend auf dem Kundenverhalten erstellt werden können. Die folgenden **Kanal**-Aktivitäten sind verfügbar: E-Mail und SMS. [Erfahren Sie, wie Sie im Kontext einer orchestrierten Kampagne eine Kanalaktion erstellen](channels.md).

## Aktivitäten zur Flusssteuerung {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Endaktivität"
>abstract="Mit der Aktivität **Ende** können Sie das Ende einer orchestrierten Kampagne grafisch markieren. Diese Aktivität hat keine funktionalen Auswirkungen und ist daher optional."

![Liste der Flusssteuerungsaktivitäten](../assets/flow-control-activities.png){width="30%" align="left"}

Die folgenden Aktivitäten sind spezifisch für die Organisation und Ausführung orchestrierter Kampagnen. Ihre Hauptaufgabe ist es, die anderen Aktivitäten zu koordinieren:

* [Und-Verknüpfung](and-join.md): Synchronisieren Sie mehrere Ausführungszweige einer orchestrierten Kampagne.
* [Verzweigung](fork.md): Erstellen Sie ausgehende Transitionen, um mehrere Aktivitäten gleichzeitig zu starten.
* [Warten](wait.md): Hält die Ausführung eines Teils einer orchestrierten Kampagne vorübergehend an.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>Die **Ende**-Aktivität markiert grafisch das Ende einer orchestrierten Kampagne. Diese Aktivität hat keine funktionalen Auswirkungen und ist daher optional.
