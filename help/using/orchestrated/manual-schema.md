---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurationsschritte
description: Erfahren Sie, wie Sie relationale Schemata direkt über die Benutzeroberfläche erstellen können.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 8c785431-9a00-46b8-ba54-54a10e288141
source-git-commit: 3dc0bf4acc4976ca1c46de46cf6ce4f2097f3721
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 4%

---

# Einrichten eines manuellen relationalen Schemas {#manual-schema}

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br><ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[ Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Ausdrücke bearbeiten](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimension ändern](activities/change-dimension.md) - [Kanalaktivitäten](activities/channels.md) - [Kombinieren](activities/combine.md) - [Anreicherung](activities/deduplication.md) - [Formulare](activities/enrichment.md) - [Abstimmung](activities/fork.md) [&#128279;](activities/reconciliation.md) [&#128279;](activities/save-audience.md) [&#128279;](activities/split.md) ->Zielgruppe speichern[ -AufspaltungWarten](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Relationale Schemata können direkt über die Benutzeroberfläche erstellt werden, was eine detaillierte Konfiguration von Attributen, Primärschlüsseln, Versionierungsfeldern und Beziehungen ermöglicht.

Im folgenden Beispiel wird das Schema **Treueprogramm-Zugehörigkeit** manuell definiert, um die erforderliche Struktur für orchestrierte Kampagnen zu veranschaulichen.

1. [Erstellen eines relationalen Schemas manuell](#schema) mithilfe der Adobe Experience Platform-Oberfläche.

1. [Attribute hinzufügen](#schema-attributes) wie Kunden-ID, Mitgliedschaftsstufe und Statusfelder.

1. [Verknüpfen Sie Ihr ](#link-schema) mit integrierten Schemata, wie z. B. Empfangende für Kampagnen-Targeting.

1. [Erstellen Sie einen ](#dataset) basierend auf Ihrem Schema und aktivieren Sie ihn für die Verwendung in orchestrierten Kampagnen.

1. [Aufnehmen von ](ingest-data.md) aus unterstützten Quellen in Ihren Datensatz.

## Erstellen eines Schemas {#schema}

Erstellen Sie zunächst manuell ein neues relationales Schema in Adobe Experience Platform. Mit diesem Prozess können Sie die Schemastruktur von Grund auf neu definieren, einschließlich des Namens und Verhaltens.

1. Melden Sie sich bei Adobe Experience Platform an.

1. Navigieren Sie zum Menü **[!UICONTROL Daten]** > **[!UICONTROL Schema]** .

1. Klicken Sie **[!UICONTROL Schema erstellen]**.

1. Wählen Sie **[!UICONTROL Relational]** als **Schematyp** aus.

   ![](assets/admin_schema_1.png){zoomable="yes"}

1. Wählen Sie **[!UICONTROL Manuell erstellen]**, um ein Schema durch manuelles Hinzufügen von Feldern zu erstellen.

1. Geben Sie Ihren **[!UICONTROL Anzeigenamen des Schemas]** ein.

1. Wählen Sie **[!UICONTROL Datensatz]** als **[!UICONTROL Schemaverhalten]** aus.

   ![](assets/schema_manual_8.png){zoomable="yes"}

1. Klicken Sie **Beenden**, um mit der Schemaerstellung fortzufahren.

Sie können jetzt mit dem Hinzufügen von Attributen zu Ihrem Schema beginnen, um dessen Struktur zu definieren.

## Hinzufügen von Attributen zu Ihrem Schema {#schema-attributes}

Fügen Sie als Nächstes Attribute hinzu, um die Struktur Ihres Schemas zu definieren. Diese Felder stellen die wichtigsten Datenpunkte dar, die in orchestrierten Kampagnen verwendet werden, z. B. Kundenkennungen, Mitgliedschaftsdetails und Aktivitätsdaten. Sie genau zu definieren, stellt eine zuverlässige Personalisierung, Segmentierung und Verfolgung sicher.

1. Klicken Sie auf der Arbeitsfläche auf ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) neben Ihrem **Schemanamen**, um Attribute hinzuzufügen.

   ![](assets/schema_manual_1.png){zoomable="yes"}

1. Geben Sie Ihr Attribut **[!UICONTROL Feldname]**, **[!UICONTROL Anzeigename]** und **[!UICONTROL Typ]** ein.

   In diesem Beispiel haben wir die in der folgenden Tabelle beschriebenen Attribute zum Schema **Treueprogramm-**&quot; hinzugefügt.

+++ Beispiele für Attribute

   | Attributname | Datentyp | Zusätzliche Attribute |
   |-|-|-|
   | Kundin bzw. Kunde | ZEICHENFOLGE | Primärschlüssel |
   | Membership_level | ZEICHENFOLGE | Erforderlich |
   | points_balance | GANZZAHL | Erforderlich |
   | enrollment_date | DATUM | Erforderlich |
   | last_status_change | DATUM | Erforderlich |
   | expiration_date | DATUM | – |
   | is_active | BOOLEAN | Erforderlich |
   | zuletzt geändert | DATETIME | Erforderlich |

+++

1. Weisen Sie die entsprechenden Felder als **[!UICONTROL Primären Schlüssel]** und **[!UICONTROL Versionsdeskriptor)]**.

   Der **[!UICONTROL Primäre Schlüssel]** stellt sicher, dass jeder Datensatz eindeutig identifiziert wird, während der **[!UICONTROL Versionsdeskriptor]** im Laufe der Zeit Aktualisierungen erfasst, was eine Änderungsdatenerfassung und eine unterstützende Datenspiegelung ermöglicht.

   ![](assets/schema_manual_2.png){zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Nachdem Attribute erstellt wurden, müssen Sie Ihr neu erstelltes Schema mit einem integrierten Schema verknüpfen.

## Verknüpfen von Schemata {#link-schema}

Wenn Sie eine Beziehung zwischen zwei Schemata erstellen, können Sie Ihre orchestrierten Kampagnen mit Daten anreichern, die außerhalb des primären Profilschemas gespeichert sind.

1. Wählen Sie in Ihrem neu erstellten Schema das Attribut aus, das Sie als Link verwenden möchten, und klicken Sie auf **[!UICONTROL Beziehung hinzufügen]**.

   ![](assets/schema_manual_3.png){zoomable="yes"}

1. Wählen Sie die **[!UICONTROL Referenzschema]** und **[!UICONTROL Referenzfeld]**, mit denen die Beziehung hergestellt werden soll.

   In diesem Beispiel ist das `customer` mit dem `recipients` verknüpft.

   ![](assets/schema_manual_4.png){zoomable="yes"}

1. Geben Sie einen Beziehungsnamen aus dem aktuellen Schema und aus dem Referenzschema ein.

1. Klicken Sie **[!UICONTROL der Konfiguration auf]**&#x200B;Übernehmen“.

Nachdem die Beziehung hergestellt wurde, müssen Sie einen Datensatz basierend auf Ihrem Schema erstellen.

## Erstellen eines Datensatzes für das Schema {#dataset}

Nachdem Sie Ihr Schema definiert haben, besteht der nächste Schritt darin, einen Datensatz basierend darauf zu erstellen. Dieser Datensatz speichert Ihre aufgenommenen Daten und muss für orchestrierte Kampagnen aktiviert sein, damit sie in Adobe Journey Optimizer verfügbar sind. Durch Aktivierung dieser Option wird sichergestellt, dass der Datensatz für die Verwendung in Echtzeit-Orchestrierungs- und Personalisierungs-Workflows erkannt wird.

1. Navigieren Sie zum Menü **[!UICONTROL Daten]** > **[!UICONTROL Datensätze]** und klicken Sie auf **[!UICONTROL Datensatz erstellen]**.

   ![](assets/schema_manual_5.png){zoomable="yes"}

1. Wählen Sie **[!UICONTROL Datensatz aus Schema erstellen]** aus.

1. Wählen Sie Ihr zuvor erstelltes Schema hier **Treueprogramm-Mitgliedschaften** und klicken Sie auf **[!UICONTROL Weiter]**.

   ![](assets/schema_manual_6.png){zoomable="yes"}

1. Geben Sie einen **[!UICONTROL Namen]** für Ihren **[!UICONTROL Datensatz]** ein und klicken Sie auf **[!UICONTROL Beenden]**.

1. Aktivieren Sie die Option **Orchestrierte Kampagnen**, um den Datensatz für die Verwendung in Ihren AJO-Kampagnen verfügbar zu machen.

   Die Aktivierung kann einige Minuten dauern. Die Datenaufnahme ist erst möglich, nachdem die Option vollständig aktiviert wurde.

   ![](assets/schema_manual_7.png){zoomable="yes"}

Sie können jetzt mit der Aufnahme von Daten in Ihr Schema beginnen, indem Sie die Quelle Ihrer Wahl verwenden.

➡️ [Informationen zur Datenaufnahme](ingest-data.md)
