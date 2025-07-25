---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Zielgruppe lesen“
description: Informationen zur Verwendung der Aktivität „Zielgruppe lesen“ in einer orchestrierten Kampagne
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ef8eba57-cd33-4746-8eb4-5214ef9cbe2f
source-git-commit: c040ad5433d041f0f4f83fce46bc02662b77648f
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 37%

---

# Lesen der Zielgruppe {#read-audience}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_read_audience"
>title="Aktivität „Zielgruppe erstellen“"
>abstract="Mit der Aktivität **Zielgruppe erstellen** können Sie die Zielgruppe auswählen, die in die orchestrierte Kampagne eintreten wird. Bei dieser Zielgruppe kann es sich um eine bestehende Adobe Experience Platform-Zielgruppe oder um eine aus einer CSV-Datei abgerufene Zielgruppe handeln. Beim Senden von Nachrichten im Rahmen einer orchestrierten Kampagne wird die Nachrichtenzielgruppe nicht in der Kanalaktivität, sondern in der Aktivität **Zielgruppe lesen** oder in der Aktivität **Zielgruppe erstellen** definiert."


+++ Inhaltsverzeichnis

| Willkommen bei orchestrierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](../gs-schemas.md)</li><li>[Manuelles Schema](../manual-schema.md)</li><li>[Datei-Upload-Schema](../file-upload-schema.md)</li><li>[Daten aufnehmen](../ingest-data.md)</li></ul>[Zugreifen auf und Verwalten von orchestrierten Kampagnen](../access-manage-orchestrated-campaigns.md) | [Wichtige Schritte beim Erstellen einer orchestrierten Kampagne](../gs-campaign-creation.md)<br/><br/>[Erstellen und Planen der Kampagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](../orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](../orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](../build-query.md)<br/><br/>[Bearbeiten von Ausdrücken](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) – [Zielgruppe erstellen](build-audience.md) – [Dimensionsänderung](change-dimension.md) – [Kanalaktivitäten](channels.md) – [Kombinieren](combine.md) – [Deduplizierung](deduplication.md) – [Anreicherung](enrichment.md) – [Verzweigung](fork.md) – [Abstimmung](reconciliation.md) – [Zielgruppe speichern](save-audience.md) – [Aufspaltung](split.md) – [Warten](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Mit **[!UICONTROL Aktivität „Zielgruppe lesen]** können Sie eine vorhandene Zielgruppe abrufen - zuvor gespeichert oder importiert - und sie in einer orchestrierten Kampagne wiederverwenden. Diese Aktivität ist besonders nützlich, um einen vordefinierten Satz von Profilen anzusprechen, ohne dass ein neuer Segmentierungsprozess ausgeführt werden muss.

Nachdem die Zielgruppe geladen wurde, können Sie sie optional einschränken, indem Sie ein Feld für eine eindeutige Identität auswählen und die Zielgruppe mit zusätzlichen Profilattributen für Targeting-, Personalisierungs- oder Berichtszwecke anreichern.

## Konfigurieren der Aktivität „Zielgruppe lesen“ {#read-audience-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **[!UICONTROL Zielgruppe lesen]** zu konfigurieren:

1. Fügen Sie **[!UICONTROL orchestrierten Kampagne]** Aktivität „Zielgruppe lesen“ hinzu.

   ![](../assets/read-audience-1.png)

1. Geben Sie **[!UICONTROL Aktivität einen]** Titel“ ein.

1. Klicken Sie auf ![Ordnersuchsymbol](../assets/do-not-localize/folder-search.svg), um die Audience auszuwählen, die Sie für Ihre orchestrierte Kampagne ansprechen möchten.

   ![](../assets/read-audience-2.png)

1. Wählen Sie eine **[!UICONTROL Entität&#x200B;]** Ihrer Zielgruppendimension aus.

   ➡️ [Führen Sie die auf dieser Seite beschriebenen Schritte aus, um Ihre Zielgruppendimension für Campaign zu erstellen](../target-dimension.md)

   ![](../assets/read-audience-3.png)

1. Wählen Sie **[!UICONTROL Attribut hinzufügen]** aus, um Ihre ausgewählte Zielgruppe mit zusätzlichen Daten anzureichern. Die resultierende Audience enthält eine Liste von Empfängern, die jeweils mit den ausgewählten Profilattributen angereichert sind.

1. Wählen Sie **[!UICONTROL Attribute]** aus, die Sie Ihrer Audience hinzufügen möchten.

   ![](../assets/read-audience-4.png)

## Beispiel

Im folgenden Beispiel wird die Aktivität **[!UICONTROL Zielgruppe lesen]** verwendet, um eine zuvor erstellte und gespeicherte Zielgruppe von Profilen abzurufen, die sich für den Newsletter angemeldet haben. Die Zielgruppe wird dann mit dem Attribut **Treuemitgliedschaft** angereichert, um die Zielgruppenbestimmung für Benutzende zu ermöglichen, die registrierte Mitglieder des Treueprogramms sind.

![](../assets/read-audience-5.png)
