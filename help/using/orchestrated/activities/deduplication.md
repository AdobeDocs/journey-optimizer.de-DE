---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Deduplizierung“
description: Erfahren Sie, wie Sie die Aktivität „Deduplizierung“ verwenden.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 4aa79448-f75a-48d5-8819-f4cb4baad5c7
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 88%

---

# Deduplizierung {#deduplication}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_fields"
>title="Felder zum Identifizieren von Duplikaten"
>abstract="Klicken Sie im Abschnitt **Felder zum Identifizieren von Duplikaten** auf die Schaltfläche **Attribut hinzufügen**, um die Felder anzugeben, für die die Identifizierung von Duplikaten aufgrund identischer Werte möglich ist, wie z. B. E-Mail-Adresse, Vorname, Nachname usw. Durch die Reihenfolge der Felder können Sie angeben, welche Felder zuerst verarbeitet werden sollen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication"
>title="Aktivität „Deduplizierung“"
>abstract="Mithilfe der Aktivität **Deduplizierung** lassen sich Duplikate in Ergebnissen aus eingehenden Aktivitäten löschen. Sie wird hauptsächlich im Anschluss an Zielgruppenbestimmungsaktivitäten und vor Aktivitäten verwendet, die die Verwendung von Zielgruppendaten zulassen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_complement"
>title="Erzeugen eines Komplements"
>abstract="Sie können eine zusätzliche ausgehende Transition mit der verbleibenden Population generieren, die als Duplikat ausgeschlossen wurde. Schalten Sie dazu die Option **Komplement erzeugen** ein"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_settings"
>title="Deduplizierungseinstellungen"
>abstract="Um Duplikate in den eingehenden Daten zu löschen, definieren Sie die Deduplizierungsmethode in den folgenden Feldern. Standardmäßig wird nur ein Eintrag beibehalten. Sie sollten außerdem die Deduplizierungsmethode anhand eines Ausdrucks oder Attributs auswählen. Standardmäßig wird der Eintrag, der von den Duplikaten ausgenommen sein soll, zufällig ausgewählt."


+++ Inhaltsverzeichnis

| Willkommen bei orchestrierten Kampagnen | Starten der ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](../gs-schemas.md)</li><li>[Manuelles Schema](../manual-schema.md)</li><li>[Datei-Upload-Schema](../file-upload-schema.md)</li><li>[Daten aufnehmen](../ingest-data.md)</li></ul>[Zugreifen auf und Verwalten von orchestrierten Kampagnen](../access-manage-orchestrated-campaigns.md) | [Wichtige Schritte zum Erstellen einer orchestrierten Kampagne](../gs-campaign-creation.md)<br/><br/>[Erstellen und Planen der Kampagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](../orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](../orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](../build-query.md)<br/><br/>[Bearbeiten von Ausdrücken](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) – [Zielgruppe erstellen](build-audience.md) – [Dimensionsänderung](change-dimension.md) – [Kanalaktivitäten](channels.md) – [Kombinieren](combine.md) – <b>[Deduplizierung](deduplication.md)</b> – [Anreicherung](enrichment.md) – [Verzweigung](fork.md) – [Abstimmung](reconciliation.md) – [Zielgruppe speichern](save-audience.md) – [Aufspaltung](split.md) – [Warten](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Die **[!UICONTROL Deduplizierungsaktivität]** ist eine **[!UICONTROL Zielgruppenbestimmungsaktivität]**. Mithilfe dieser Aktivität lassen sich Duplikate in Ergebnissen aus eingehenden Aktivitäten löschen, z. B. duplizierte Profile aus der Empfängerliste. Die **[!UICONTROL Deduplizierungsaktivität]** wird im Allgemeinen im Anschluss an Zielgruppenbestimmungsaktivitäten und vor Aktivitäten verwendet, die die Verwendung von Zielgruppendatum zulassen.

## Konfigurieren der Deduplizierungsaktivität{#deduplication-configuration}

Gehen Sie folgendermaßen vor, um die **[!UICONTROL Deduplizierungsaktivität]** zu konfigurieren:


1. Fügen Sie **[!UICONTROL orchestrierten Kampagne]** Aktivität „Deduplizierung“ hinzu.

1. Klicken Sie im Abschnitt **[!UICONTROL Felder zum Identifizieren von Duplikaten]** auf die Schaltfläche **[!UICONTROL Attribut hinzufügen]**, um die Felder anzugeben, für die die Identifizierung von Duplikaten aufgrund identischer Werte möglich ist, wie z. B. E-Mail-Adresse, Vorname, Nachname usw. Durch die Reihenfolge der Felder können Sie angeben, welche Felder zuerst verarbeitet werden sollen.

   ![](../assets/deduplication-1.png)

1. Wählen Sie im Abschnitt **[!UICONTROL Deduplizierungseinstellungen]** über das Feld „Beizubehaltende Duplikate“ aus, wie viele eindeutige Einträge beibehalten werden sollen. Der Standardwert beträgt 1, wobei ein Eintrag pro Duplikatgruppe beibehalten wird. Legen Sie ihn auf 0 fest, um alle Duplikate zu behalten.

   Wenn die Einträge A und B Duplikate von Y sind und der Eintrag C ein Duplikat von Z ist, dann gilt Folgendes:

   * **Wenn der Wert des Feldes 1 beträgt**: Nur die Einträge Y und Z werden beibehalten.
   * **Wenn der Wert des Feldes 0 beträgt**: Alle Einträge (A, B, C, Y, Z) werden beibehalten.
   * **Wenn der Wert des Feldes 2 beträgt**: C und Z werden beibehalten und von den Einträgen A, B und Y werden zwei entweder nach dem Zufallsprinzip oder basierend auf Ihrer Deduplizierungsmethode beibehalten.

1. Wählen Sie eine **[!UICONTROL Deduplizierungsmethode]**, die definiert, wie das System entscheidet, welche Einträge aus jeder Gruppe von Duplikaten beibehalten werden sollen:

   * **[!UICONTROL Zufällige Auswahl]**: Wählt nach dem Zufallsprinzip unter den Duplikaten den Eintrag aus, der beibehalten werden soll.
   * **[!UICONTROL Von einem Ausdruck ausgehend]**: Behält Einträge mit dem höchsten oder niedrigsten Wert basierend auf einem von Ihnen definierten Ausdruck bei.
   * **[!UICONTROL Wert nicht leer]**: Behält Einträge, bei denen das ausgewählte Feld nicht leer ist, z. B. nur Profile mit einer Telefonnummer.
   * **[!UICONTROL Gemäß einer Werteliste]**: Ermöglicht die Priorisierung bestimmter Werte für ein oder mehrere Felder, z. B. können Einträge priorisiert werden, für die der Wert des Feldes „Land“ auf Frankreich festgelegt ist. Klicken Sie auf **[!UICONTROL Attribut]**, um ein Feld auszuwählen oder einen benutzerdefinierten Ausdruck zu erstellen. Verwenden Sie die Schaltfläche **[!UICONTROL Hinzufügen]**, um bevorzugte Werte in der Prioritätsreihenfolge einzugeben.

   ![](../assets/deduplication-2.png)

1. Aktivieren Sie die Option **[!UICONTROL Komplement erzeugen]**, wenn Sie die verbleibende Population verwenden möchten. Das Komplement besteht aus allen Duplikaten. Der Aktivität wird dann eine zusätzliche Transition hinzugefügt.

## Beispiel{#deduplication-example}

Im folgenden Beispiel wird eine Aktivität des Typs **[!UICONTROL Deduplizierung]** verwendet, um doppelte Einträge aus der Zielgruppe zu entfernen, bevor ein Versand durchgeführt wird. Die Zielgruppe wird zunächst so gefiltert, dass nur Profile mit einem ausgefüllten E-Mail-Feld einbezogen werden. Anschließend verwendet die Aktivität **[!UICONTROL Deduplizierung]** die E-Mail-Adresse, um Duplikate zu ermitteln und auszuschließen.

![](../assets/deduplication-3.png)
