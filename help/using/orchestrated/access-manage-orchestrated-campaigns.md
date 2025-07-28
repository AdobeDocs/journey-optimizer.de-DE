---
solution: Journey Optimizer
product: journey optimizer
title: Zugriff und Verwaltung einer orchestrierten Kampagne
description: Grundlegende Prinzipien der koordinierten Kampagnenerstellung mit Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b42d317-cd01-4c6a-b61e-5b03e5a8ff3c
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 48%

---

# Zugriff und Verwaltung einer orchestrierten Kampagne {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Orchestrierte Kampagne"
>abstract="Auf diesem Bildschirm können Sie auf die vollständige Liste der orchestrierten Kampagnen zugreifen, ihren aktuellen Status und das letzte/nächste Ausführungsdatum überprüfen und eine neue orchestrierte Kampagne erstellen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="Aktion"
>abstract="In diesem Abschnitt werden alle in der orchestrierten Kampagne verwendeten Aktionen aufgelistet."

+++ Inhaltsverzeichnis

| Willkommen bei orchestrierten Kampagnen | Starten der ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul><br/><br/><b>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)</b><br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Bearbeiten von Ausdrücken](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) – [Zielgruppe erstellen](activities/build-audience.md) – [Dimensionsänderung](activities/change-dimension.md) – [Kanalaktivitäten](activities/channels.md) – [Kombinieren](activities/combine.md) – [Deduplizierung](activities/deduplication.md) – [Anreicherung](activities/enrichment.md) – [Verzweigung](activities/fork.md) – [Abstimmung](activities/reconciliation.md) – [Zielgruppe speichern](activities/save-audience.md) – [Aufspaltung](activities/split.md) – [Warten](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

## Zugriff auf orchestrierte Kampagnen

Navigieren Sie zum Menü **[!UICONTROL Kampagnen]** und wählen Sie die Registerkarte **[!UICONTROL Orchestrierung]**, um auf die vollständige Liste der orchestrierten Kampagnen zuzugreifen.

![Bild mit dem Inventar der orchestrierten Kampagnen](assets/inventory.png){zoomable="yes"}{zoomable="yes"}

Jede orchestrierte Kampagne in der Liste zeigt Informationen wie den aktuellen (Status[ der Kampagne, ](#status) zugehörigen Kanal und Tags oder das letzte Mal, wann sie geändert wurde, an. Sie können die angezeigten Spalten anpassen, indem Sie auf die Schaltfläche ![Layout konfigurieren](assets/do-not-localize/inventory-configure-layout.svg) klicken.

Darüber hinaus stehen eine Suchleiste und Filter zur Verfügung, um die Suche innerhalb der Liste zu erleichtern. Sie können beispielsweise die orchestrierten Kampagnen so filtern, dass nur die mit einem bestimmten Kanal oder Tag verknüpften oder die in einem bestimmten Datumsbereich erstellten Kampagnen angezeigt werden.

Die Schaltfläche ![Bild mit der Schaltfläche „Mehr Aktionen“](assets/do-not-localize/rule-builder-icon-more.svg) im Kampagneninventar ermöglicht die Durchführung der folgenden Vorgänge.

![Bild des Kampagneninventars](assets/inventory-actions.png)

* **[!UICONTROL Bericht für gesamte Zeit anzeigen]**/**[!UICONTROL Bericht für letzte 24 Stunden anzeigen]**: Greifen Sie auf Berichte zu, um die Wirkung und Leistung Ihrer orchestrierten Kampagnen zu messen und zu visualisieren. [Erfahren Sie mehr über die Berichterstellung für orchestrierte Kampagnen](../orchestrated/reporting-campaigns.md)
* **[!UICONTROL Tags bearbeiten]**: Bearbeiten Sie die mit der Kampagne verknüpften Tags.
* **[!UICONTROL Duplizieren]** - In einigen Fällen müssen Sie möglicherweise eine orchestrierte Kampagne duplizieren, um beispielsweise eine gestoppte Kampagne auszuführen oder die Ausführungshäufigkeit einer geplanten Kampagne zu ändern.
* **[!UICONTROL Löschen]**: Löscht die Kampagne. Diese Aktion ist nur für Kampagnen im Status **[!UICONTROL Entwurf]** verfügbar.
* **[!UICONTROL Archivieren]**: Archiviert die Kampagne. Alle archivierten Kampagnen werden rollierend 30 Tage nach dem Datum ihrer letzten Änderung gelöscht. Diese Aktion ist für alle Kampagnen mit Ausnahme von Kampagnen im Status **[!UICONTROL Entwurf]** verfügbar.

## Was verbirgt sich in einer orchestrierten Kampagne? {#gs-ms-campaign-inside}

Die Arbeitsfläche der orchestrierten Kampagne ist eine Darstellung dessen, was passieren soll. Sie beschreibt die verschiedenen Aufgaben, die ausgeführt und miteinander verknüpft werden sollen.

![Bild mit einer orchestrierten Kampagnen-Arbeitsfläche](assets/canvas-example.png)

Jede orchestrierte Kampagne enthält:

* **Aktivitäten**: Eine Aktivität ist eine Aufgabe, die ausgeführt werden soll. Die verschiedenen verfügbaren Aktivitäten werden im Diagramm durch Symbole dargestellt. Jede Aktivität verfügt über bestimmte Eigenschaften sowie andere Eigenschaften, die für alle Aktivitäten gelten.

  In einem orchestrierten Kampagnendiagramm kann eine bestimmte Aktivität mehrere Aufgaben hervorrufen, insbesondere wenn eine Schleife oder wiederkehrende Aktionen vorliegen.

* **Transitionen**: Transitionen verknüpfen eine Quellaktivität mit einer Zielaktivität und definieren deren Sequenz.

* **Arbeitstabellen**: Die Arbeitstabelle enthält alle von der Transition übermittelten Informationen. Jede koordinierte Kampagne verwendet mehrere Arbeitstabellen. Die in diesen Tabellen übermittelten Daten können während des gesamten Lebenszyklus der koordinierten Kampagne verwendet werden.

## Kampagnenstatus {#status}

Orchestrierte Kampagnen können mehrere Status aufweisen:

* **[!UICONTROL Entwurf]**: Die orchestrierte Kampagne wurde erstellt. Sie wurde noch nicht veröffentlicht.
* **[!UICONTROL Veröffentlichen]**: Die orchestrierte Kampagne wird veröffentlicht.
* **[!UICONTROL Live]**: Die orchestrierte Kampagne wurde veröffentlicht und wird ausgeführt.
* **[!UICONTROL Geplant]**: Die Ausführung der orchestrierten Kampagne wurde geplant.
* **[!UICONTROL Abgeschlossen]**: Die Ausführung der orchestrierten Kampagne ist abgeschlossen. Der Status „Abgeschlossen“ wird einer Kampagne automatisch bis zu 3 Tage nach dem fehlerfreien Versand von Nachrichten zugewiesen.
* **[!UICONTROL Geschlossen]**: Dieser Status wird angezeigt, wenn eine wiederkehrende Kampagne geschlossen wurde. Die Kampagne wird ausgeführt, bis alle Aktivitäten abgeschlossen sind, aber es können keine weiteren Profile in die Kampagne eintreten.
* **[!UICONTROL Archiviert]**: Die koordinierte Kampagne wurde archiviert. Alle archivierten Kampagnen werden rollierend 30 Tage nach dem Datum ihrer letzten Änderung gelöscht. Sie können eine archivierte Kampagne bei Bedarf duplizieren, um sie weiter zu bearbeiten.
* **[!UICONTROL Angehalten]**: Die Ausführung der orchestrierten Kampagne wurde angehalten. Um die Kampagne erneut zu starten, müssen Sie sie duplizieren.
