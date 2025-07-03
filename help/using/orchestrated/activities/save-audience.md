---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Zielgruppe speichern“
description: Erfahren Sie, wie Sie die Aktivität „Zielgruppe speichern“ in einer koordinierten Kampagne verwenden
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 8a5026cdeb63b7b261ec0dfa690c5bd41d7de772
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 48%

---

# Speichern einer Zielgruppe {#save-audience}

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](../configuration-steps.md)<br/><br/>[Zugreifen auf und Verwalten von orchestrierten Kampagnen](../access-manage-orchestrated-campaigns.md) | [Wichtige Schritte für die orchestrierte Kampagnenerstellung](../gs-campaign-creation.md)<br/><br/>[Erstellen und Planen der Kampagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](../orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](../orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](../build-query.md)<br/><br/>[Ausdrücke bearbeiten](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) - [Zielgruppe aufbauen](build-audience.md) - [Dimension ändern](change-dimension.md) - [Kanalaktivitäten](channels.md) - [Kombinieren](combine.md) - [Anreicherung](deduplication.md) - [Formulare](enrichment.md) - [Abstimmung](fork.md) [ ](reconciliation.md) <b>[ ](save-audience.md)</b> [ ](split.md) ->Zielgruppe speichern[ -AufspaltungWarten](wait.md) |

{style="table-layout:fixed"}

+++


Die Aktivität **[!UICONTROL Zielgruppe speichern]** ist eine **[!UICONTROL Zielgruppenbestimmungs]**-Aktivität, mit der Sie eine vorhandene Zielgruppe aktualisieren oder eine neue Zielgruppe aus der zuvor in der orchestrierten Kampagne generierten Population erstellen können. Nach der Erstellung werden diese Zielgruppen zur Liste der Anwendungszielgruppen hinzugefügt und können über das Menü **[!UICONTROL Zielgruppen]** aufgerufen werden.

Diese Aktivität ist besonders nützlich, um Zielgruppensegmente beizubehalten, die innerhalb derselben orchestrierten Kampagne berechnet werden, und sie für die Wiederverwendung in zukünftigen Kampagnen verfügbar zu machen. Sie ist normalerweise mit anderen Zielgruppenbestimmungsaktivitäten verbunden, wie **[!UICONTROL Zielgruppe aufbauen]** oder **[!UICONTROL Kombinieren]**, um die resultierende Population zu erfassen und zu speichern.

## Konfigurieren der Aktivität „Zielgruppe speichern“ {#save-audience-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **Zielgruppe aufbauen** zu konfigurieren:

1. Fügen Sie **orchestrierten Kampagne** Aktivität „Zielgruppe speichern“ hinzu.

1. Wählen Sie im Dropdown **Modus** die Aktion aus, die ausgeführt werden soll:

   * **Zielgruppe erstellen oder aktualisieren**: Definieren Sie ein **Zielgruppen-Label**. Wenn die Zielgruppe bereits existiert, wird sie aktualisiert. Andernfalls wird eine neue Zielgruppe erstellt.

   * **Existierende Zielgruppe aktualisieren**: Wählen Sie die zu aktualisierende **Zielgruppe** in der Liste der vorhandenen Zielgruppen aus.

1. Wählen Sie die **Update-Methode** aus, der für vorhandene Zielgruppen gelten soll:

   * **Zielgruppen-Inhalt durch die neuen Daten ersetzen**: Alle Zielgruppeninhalte werden ersetzt und alte Daten gehen verloren. Nur die in der eingehenden Transition der Aktivität **Zielgruppe speichern** übermittelten Daten werden beibehalten. Bei dieser Option werden Zielgruppendimension und -typ der aktualisierten Zielgruppe gelöscht.

   * **Zielgruppen-Inhalt mit den neuen Daten ergänzen**: Der alte Zielgruppeninhalt wird beibehalten und die Daten der eingehenden Transition der Aktivität **Zielgruppe speichern** werden hinzugefügt.

1. Aktivieren Sie die Option **Ausgehende Transition erzeugen**, wenn Sie eine Transition nach der Aktivität **Zielgruppe speichern** hinzufügen möchten.

Der Inhalt der gespeicherten Zielgruppe ist anschließend in der Detailansicht der Zielgruppe verfügbar, auf die Sie im Menü **Zielgruppen** zugreifen können. Die in dieser Ansicht verfügbaren Spalten entsprechen den Spalten der eingehenden Transition der orchestrierten Kampagne **Zielgruppe speichern**.

## Beispiel {#save-audience-example}

Im folgenden Beispiel wird eine einfache Zielgruppenaktualisierung von der Zielgruppenbestimmung aus gezeigt. Eine Planung führt die orchestrierte Kampagne einmal monatlich aus. Eine Abfrage ruft alle Profile ab, die für die verschiedenen verfügbaren Anwendungen angemeldet sind. Die Aktivität **Zielgruppe speichern** aktualisiert die Zielgruppe, indem sie Profile entfernt, die sich seit der letzten orchestrierten Kampagnenausführung vom Service abgemeldet haben, und neu abonnierte Profile hinzufügt.
