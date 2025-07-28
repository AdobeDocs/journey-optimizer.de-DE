---
solution: Journey Optimizer
product: journey optimizer
title: Wichtige Schritte zum Erstellen einer orchestrierten Kampagne
description: Grundlegende Prinzipien der koordinierten Kampagnenerstellung mit Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 60%

---


# Wichtige Schritte zum Erstellen einer orchestrierten Kampagne {#orchestrated-campaign-creation}

+++ Inhaltsverzeichnis

| Willkommen bei orchestrierten Kampagnen | Starten der ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/><b>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md)</b> | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Bearbeiten von Ausdrücken](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) – [Zielgruppe erstellen](activities/build-audience.md) – [Dimensionsänderung](activities/change-dimension.md) – [Kanalaktivitäten](activities/channels.md) – [Kombinieren](activities/combine.md) – [Deduplizierung](activities/deduplication.md) – [Anreicherung](activities/enrichment.md) – [Verzweigung](activities/fork.md) – [Abstimmung](activities/reconciliation.md) – [Zielgruppe speichern](activities/save-audience.md) – [Aufspaltung](activities/split.md) – [Warten](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Diese Seite führt Sie durch die wichtigsten Schritte zum Erstellen und Starten einer orchestrierten Kampagne - von der Einrichtung und dem Design bis hin zur Überwachung und Berichterstellung.

<!--
<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="#create"><img alt="Create & schedule your campaign" src="../../channels/assets/do-not-localize/email.png"></a><br/><a href="#create"><strong>Create & schedule your campaign</strong></a></td>
<td><a href="#orchestrate"><img alt="Orchestrate campaign activities" src="../../channels/assets/do-not-localize/sms.png"></a><br/><a href="#orchestrate"><strong>Orchestrate campaign activities</strong></a></td>
<td><a href="#start"><img alt="Start & monitor your campaign" src="../../channels/assets/do-not-localize/push.png"></a><a href="#start"><strong>Start & monitor your campaign</strong></a></td>
<td><a href="#report"><img alt="Analyze & report on results" src="../../channels/assets/do-not-localize/push.png"></a><a href="#report"><strong>Analyze & report on results</strong></a></td>
</tr></table>-->



## Schritt 1: Erstellen und Planen Ihrer Kampagne {#create}

Vor allen anderen Aufgaben müssen Sie eine orchestrierte Kampagne erstellen und festlegen *wann* ausgeführt werden soll. Egal, ob es sich um eine einmalige Push-Benachrichtigung oder eine wiederkehrende Multi-Channel-Kampagne handelt, Sie haben die volle Kontrolle über Timing und Häufigkeit.

➡️ [Weitere Informationen zur Erstellung und Planung einer Kampagne](../orchestrated/create-orchestrated-campaign.md)

## Schritt 2: Orchestrieren von Kampagnenaktivitäten {#orchestrate}

Sobald die Kampagne erstellt ist, ist es an der Zeit, die Logik dahinter zu entwerfen. Auf einer visuellen Arbeitsfläche können Sie Targeting-, Versand- und Flusskontrollaktivitäten kombinieren, um Ihr Kundenerlebnis zu gestalten.

➡️ [Weitere Informationen zur Orchestrierung von Aktivitäten](../orchestrated/orchestrate-activities.md)

## Schritt 3: Starten und Überwachen Ihrer Kampagne {#start}

Du bist fast da! Führen Sie Ihre Kampagne zuerst im Testmodus aus, um etwaige Probleme zu ermitteln. Veröffentlichen Sie sie dann und überwachen Sie die Live-Ausführung in Echtzeit. Verfolgen Sie den Fortschritt, überprüfen Sie die Kampagne auf Fehler und sehen Sie sich an, wie Profile jeden Schritt durchlaufen.

➡️ [Weitere Informationen zum Start und zur Überwachung einer Kampagne](../orchestrated/start-monitor-campaigns.md)

## Schritt 4: Analysieren und Melden von Ergebnissen {#report}

Verwenden Sie nach dem Start integrierte Berichte, um zu verstehen, was funktioniert hat und was verbessert werden könnte. Mit Echtzeit-Dashboards und ausführlichen Analysen können Sie zukünftige Kampagnen optimieren und Ihre Strategie verfeinern.

➡️ [Weitere Informationen zum Reporting](../orchestrated/reporting-campaigns.md)

## Gehen Sie noch weiter: Retargeting basierend auf Interaktion {#retarget}

Nachdem Ihre Kampagne ausgeführt wurde, können Sie einen Schritt weiter gehen, indem Sie Profile erneut ansprechen, je nachdem, wie sie mit Ihrer Nachricht interagiert haben, d. h. ob sie sie geöffnet oder auf einen Link geklickt haben. Auf diese Weise können Sie maßgeschneiderte Folge-Nachrichten senden, inaktive Benutzende erneut kontaktieren oder vorhandenes Interesse vergrößern.

➡️ [Weitere Informationen zum Retargeting basierend auf Feedback-Ereignissen](../orchestrated/retarget.md)
