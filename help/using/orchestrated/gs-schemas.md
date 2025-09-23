---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurationsschritte
description: Erfahren Sie, wie Sie in Adobe Experience Platform ein modellbasiertes Schema erstellen, indem Sie eine DDL hochladen
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
version: Campaign Orchestration
source-git-commit: c584ce48029bd298b503a342a1e663eeeedbba42
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 24%

---


# Erste Schritte mit modellbasierten Schemata und Datensätzen{#gs-schemas}

Dieses Handbuch führt Sie durch den Prozess der Erstellung eines modellbasierten Schemas, der Konfiguration eines Datensatzes für orchestrierte Kampagnen und der Aufnahme von Daten.

![schema](assets/do-not-localize/schema_admin.png){zoomable="yes"}

## Schlüsselkonzepte

Im Kontext orchestrierter Kampagnen ist ein **Datensatz** ein Konstrukt zur Speicherung und Verwaltung von Daten, normalerweise einer Tabelle, die ein Schema (Spalten) und Felder (Zeilen) enthält. Daten, die erfolgreich in Experience Platform aufgenommen wurden, werden im Data Lake als Datensätze gespeichert.

Ein **Schema** stellt die Struktur und das Format von Daten dar und validiert sie. Sie bietet eine abstrakte Definition eines realen Objekts (z. B. einer Person) und legt fest, welche Daten in jeder Instanz dieses Objekts enthalten sein sollen (z. B. Name, Geburtsdatum usw.).

Ein **Datenmodell** ist der konzeptionelle Entwurf zur Normalisierung Ihrer Daten

Es beschreibt:

* Die Entitäten (z. B. Kunde, Kampagne, Segment)
* Die Attribute dieser Entitäten (z. B. Kundenname, Startdatum der Kampagne)
* Die Beziehungen zwischen Entitäten (z. B. Kundinnen und Kunden gehören zu Segmenten, Kampagnen oder Zielsegmenten)

Ein Datenmodell ist logisch und konzeptionell und nicht an eine physische Implementierung in Orchestered Campaign gebunden.

In einem **modellbasierten Datenmodell** werden Daten in Tabellen organisiert, die sich auf andere Tabellen beziehen.

* Jede Tabelle verfügt über Zeilen (Datensätze) und Spalten (Attribute)
* Jede Tabelle verfügt über einen Primärschlüssel zur eindeutigen Identifizierung von Zeilen
* Beziehungen zwischen Tabellen werden mithilfe von Fremdschlüsseln ausgedrückt

Ein **modellbasiertes Schema** ist die formale Definition des modellbasierten Datenmodells.

Es wird Folgendes festgelegt:

* Der Satz von Tabellen
* Die Spalten der einzelnen Tabellen
* Die Einschränkungen
* Die Beziehungen zwischen Tabellen

Beim Organisieren von Schemata oder Tabellen in einem modellbasierten Datenmodell geht es um die Strukturierung Ihrer Daten in mehrere Tabellen. Stellen Sie sicher, dass jede Tabelle einen Entitäts-/Schematyp speichert

## Implementierungsschritte {#implementation}

Gehen Sie wie folgt vor, um Daten aufzunehmen und ein modellbasiertes Schema zu erstellen:

1. Erstellen [modellbasierten Schemas manuell](manual-schema.md) oder [mithilfe einer DDL-Datei](file-upload-schema.md)

   Definieren Sie die Struktur Ihres Datenmodells, einschließlich Tabellen, Attributen und Beziehungen. Entscheiden Sie, ob Sie das Schema manuell in der Benutzeroberfläche erstellen oder eine DDL-Datei hochladen möchten, um die Einrichtung zu beschleunigen.

   Wenn Sie das Schema manuell erstellen, muss der Datensatz auch manuell erstellt und aktiviert werden. Bei Verwendung einer DDL-Datei erfolgt die Erstellung und Aktivierung von Datensätzen automatisch.

1. [Verknüpfen eines Schemas](file-upload-schema.md)

   Erstellen Sie Beziehungen zwischen Ihren Schemata, um konsistente Daten zu gewährleisten und entitätsübergreifende Abfragen zu ermöglichen. Sie können beispielsweise Treuetransaktionen mit Empfängerinnen und Empfängern oder Belohnungen mit Marken verknüpfen.

1. [Datensatz erstellen](manual-schema.md#dataset)

   Nachdem Sie Ihr Schema definiert haben, müssen Sie einen Datensatz basierend darauf erstellen. Dieser Datensatz dient als Speicher für Ihre aufgenommenen Daten.

1. [Orchestrierte Kampagne aktivieren](manual-schema.md#enable)

   Der Datensatz speichert Ihre aufgenommenen Daten und muss für orchestrierte Kampagnen aktiviert werden, um sicherzustellen, dass er in Adobe Journey Optimizer verfügbar ist.

1. [Aufnehmen von Daten](ingest-data.md)

   Nehmen Sie Daten aus unterstützten Quellen wie SFTP, Cloud-Speicher oder Datenbanken in Adobe Experience Platform auf.

