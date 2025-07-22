---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Zielgruppe speichern“
description: Erfahren Sie, wie Sie die Aktivität „Zielgruppe speichern“ in einer koordinierten Kampagne verwenden
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
source-git-commit: b575f2363059a24e7192f436fac62001f79a3dbc
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 7%

---

# Speichern einer Zielgruppe {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Audience-Aktivität speichern"
>abstract="Die Aktivität **Zielgruppe speichern** ist eine **Zielgruppenbestimmungs**-Aktivität, mit der Sie eine vorhandene Zielgruppe aktualisieren oder eine neue Zielgruppe aus der zuvor in der orchestrierten Kampagne generierten Population erstellen können. Nach der Erstellung werden diese Zielgruppen zur Liste der Anwendungszielgruppen hinzugefügt und können über das Menü **Zielgruppen** aufgerufen werden."


+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](../gs-schemas.md)</li><li>[Manuelles Schema](../manual-schema.md)</li><li>[Datei-Upload-Schema](../file-upload-schema.md)</li><li>[Daten aufnehmen](../ingest-data.md)</li></ul>[Zugreifen auf und Verwalten von orchestrierten Kampagnen](../access-manage-orchestrated-campaigns.md) | [Wichtige Schritte zum Erstellen einer orchestrierten Kampagne](../gs-campaign-creation.md)<br/><br/>[Erstellen und Planen der Kampagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](../orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](../orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](../build-query.md)<br/><br/>[Ausdrücke bearbeiten](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) - [Zielgruppe aufbauen](build-audience.md) - [Dimension ändern](change-dimension.md) - [Kanalaktivitäten](channels.md) - [Kombinieren](combine.md) - [Anreicherung](deduplication.md) - [Formulare](enrichment.md) - [Abstimmung](fork.md) [&#128279;](reconciliation.md) <b>[&#128279;](save-audience.md)</b> [&#128279;](split.md) ->Zielgruppe speichern[ -AufspaltungWarten](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Die Aktivität **[!UICONTROL Zielgruppe speichern]** ist eine **[!UICONTROL Zielgruppenbestimmungs]**-Aktivität, mit der Sie eine vorhandene Zielgruppe aktualisieren oder eine neue Zielgruppe aus der zuvor in der orchestrierten Kampagne generierten Population erstellen können. Nach der Erstellung werden diese Zielgruppen zur Liste der Anwendungszielgruppen hinzugefügt und können über das Menü **[!UICONTROL Zielgruppen]** aufgerufen werden.

Diese Aktivität ist besonders nützlich, um Zielgruppensegmente beizubehalten, die innerhalb derselben orchestrierten Kampagne berechnet werden, und sie für die Wiederverwendung in zukünftigen Kampagnen verfügbar zu machen. Sie ist normalerweise mit anderen Zielgruppenbestimmungsaktivitäten verbunden, wie **[!UICONTROL Zielgruppe aufbauen]** oder **[!UICONTROL Kombinieren]**, um die resultierende Population zu erfassen und zu speichern.

## Konfigurieren der Aktivität „Zielgruppe speichern“ {#save-audience-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **[!UICONTROL Zielgruppe aufbauen]** zu konfigurieren:

1. Fügen Sie **[!UICONTROL orchestrierten Kampagne]** Aktivität „Zielgruppe speichern“ hinzu.

1. Geben Sie einen **[!UICONTROL Zielgruppentitel]** ein, der die gespeicherte Zielgruppe identifiziert.

1. Klicken Sie **[!UICONTROL Zielgruppenattribut hinzufügen]**, um festzulegen, wie die Zielgruppendaten strukturiert und für die zukünftige Wiederverwendung gespeichert werden.

   ![](../assets/save-audience-1.png)

1. &#x200B; Wählen Sie dann das entsprechende **[!UICONTROL Primäre Identitätsfeld]** (und **[!UICONTROL Identity-Namespace]** aus, um eine genaue Profilauflösung sicherzustellen.

   ![](../assets/save-audience-2.png)

1. Schließen Sie die Einrichtung ab, indem Sie die orchestrierte Kampagne speichern und veröffentlichen. Dadurch wird Ihre Zielgruppe generiert und gespeichert.

Der Inhalt der gespeicherten Zielgruppe ist dann in der Detailansicht der Zielgruppe verfügbar, auf die über das Menü **[!UICONTROL Zielgruppen“ zugegriffen]** kann.

![](../assets/save-audience-3.png)

## Beispiel {#save-audience-example}

Im folgenden Beispiel wird veranschaulicht, wie eine einfache Zielgruppe mithilfe von Targeting erstellt wird. Eine Abfrage identifiziert alle Profile, die in den letzten 30 Tagen einen Kauf getätigt haben. Die **[!UICONTROL Zielgruppe speichern]** erfasst diese Profile, um eine wiederverwendbare Zielgruppe aus aktuellen Käufern zu erstellen.

![](../assets/save-audience-4.png)
