---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität Warten in orchestrierten Kampagnen
description: Erfahren Sie, wie Sie die Aktivität Warten in orchestrierten Kampagnen verwenden
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 6eb49e954b7906f668b1c1779c16f3e67003307b
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 12%

---

# Warten {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Aktivität „Warten“"
>abstract="Die Aktivität **Warten** wird verwendet, um die Transition von einer Aktivität zu einer anderen zu verzögern."


+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Manuelles Schema](../manual-schema.md)</li><li>[Datei-Upload-Schema](../file-upload-schema.md)</li><li>[Daten aufnehmen](../ingest-data.md)</li></ul><br/><br/>[Zugreifen auf und Verwalten von orchestrierten Kampagnen](../access-manage-orchestrated-campaigns.md) | [Wichtige Schritte zum Erstellen einer orchestrierten Kampagne](../gs-campaign-creation.md)<br/><br/>[Erstellen und Planen der Kampagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](../orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](../orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](../build-query.md)<br/><br/>[Ausdrücke bearbeiten](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) - [Zielgruppe aufbauen](build-audience.md) - [Dimension ändern](change-dimension.md) - [Kanalaktivitäten](channels.md) - [Kombinieren](combine.md) - [Anreicherung](deduplication.md) - [Formulare](enrichment.md) - [Abstimmung](fork.md) [&#128279;](reconciliation.md) [&#128279;](save-audience.md) [&#128279;](split.md) ->Zielgruppe speichern<b>[ -AufspaltungWarten](wait.md)</b> |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Die **[!UICONTROL Warten]**-Aktivität ist eine **[!UICONTROL Fluss-Kontrolle]**-Komponente, die verwendet wird, um in einer orchestrierten Kampagne eine Verzögerung zwischen zwei Aktivitäten einzuführen. Dadurch können Sie sicherstellen, dass Ihre Folgeaktivitäten zeitlich besser abgestimmt und für die Benutzerinteraktion relevanter sind.

Sie können beispielsweise einige Tage nach einem E-Mail-Versand warten, um Öffnungen und Klicks zu verfolgen, bevor Sie eine Folgenachricht senden.

## Konfiguration{#wait-configuration}

Gehen Sie folgendermaßen vor, um die Aktivität **[!UICONTROL Warten]** zu konfigurieren:

1. Fügen Sie **[!UICONTROL orchestrierten Kampagne]** Aktivität „Warten“ hinzu.

1. Wählen Sie den Wartetyp aus, der Ihren Anforderungen am besten entspricht:

   * **[!UICONTROL Dauer]**: Geben Sie eine Verzögerung in Sekunden, Minuten, Stunden oder Tagen an, bevor Sie mit der nächsten Aktivität fortfahren.

   * **[!UICONTROL Feste Zeit]**: Legen Sie ein bestimmtes Datum und eine bestimmte Uhrzeit fest, nach denen die nächste Aktivität beginnt.

   ![](../assets/wait_activity.png)

## Beispiel{#wait-example}

Das folgende Beispiel veranschaulicht die **[!UICONTROL Warten]**-Aktivität in einem typischen Anwendungsfall.  An Profile, die Geburtstag feiern, wird eine E-Mail mit einem Promo-Code gesendet. Nach 29 Tagen wird eine SMS an dieselbe Gruppe gesendet, um sie daran zu erinnern, dass ihr Geburtstags-Promo-Code bald abläuft.

![](../assets/wait-example.png)
