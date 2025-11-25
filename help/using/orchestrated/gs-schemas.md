---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurationsschritte
description: Erfahren Sie, wie Sie in Adobe Experience Platform ein relationales Schema erstellen, indem Sie eine DDL-Datei hochladen.
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
version: Campaign Orchestration
source-git-commit: 059670c143595b9cacdf7e82a8a5c3efda78f30b
workflow-type: ht
source-wordcount: '470'
ht-degree: 100%

---


# Erste Schritte mit relationalen Schemata und Datensätzen{#gs-schemas}

Dieses Handbuch führt Sie durch den Prozess der Erstellung eines relationalen Schemas, der Konfiguration eines Datensatzes für orchestrierte Kampagnen und der Aufnahme von Daten.

![Schema](assets/do-not-localize/schema_admin.png){zoomable="yes"}

## Schlüsselkonzepte

Im Kontext orchestrierter Kampagnen ist ein **Datensatz** ein Konstrukt zur Datenspeicherung und -verwaltung, in dem Daten in der Regel in einer Tabelle erfasst werden, die ein Schema (Spalten) und Felder (Zeilen) beinhaltet. Daten, die erfolgreich in Experience Platform aufgenommen wurden, werden im Data Lake als Datensätze gespeichert.

Ein **Schema** stellt die Struktur und das Format von Daten dar und validiert sie. Es bietet eine abstrakte Definition eines realen Objekts (z. B. einer Person) und beschreibt, welche Daten in jeder Instanz dieses Objekts enthalten sein sollen (z. B. Name, Geburtstag usw.).

Ein **Datenmodell** ist die konzeptionelle Blaupause zur Normalisierung Ihrer Daten.

Es beschreibt:

* Die Entitäten (z. B. Kundschaft, Kampagne, Segment)
* Die Attribute dieser Entitäten (z. B. Kundenname, Startdatum der Kampagne)
* Die Beziehungen zwischen Entitäten (z. B. Kundinnen und Kunden gehören zu Segmenten, Kampagnen zielen auf Segmente ab)

Ein Datenmodell ist logisch und konzeptionell und nicht an eine physische Implementierung in einer orchestrierten Kampagne gebunden.

In einem **relationalen Datenmodell** werden Daten in Tabellen organisiert, die sich auf andere Tabellen beziehen.

* Jede Tabelle verfügt über Zeilen (Einträge) und Spalten (Attribute).
* Jede Tabelle verfügt über einen Primärschlüssel zur eindeutigen Identifizierung von Zeilen.
* Beziehungen zwischen Tabellen werden mithilfe von Fremdschlüsseln ausgedrückt.

Ein **relationales Schema** ist die formale Definition des relationalen Datenmodells.

Es gibt an:

* Den Satz von Tabellen
* Die Spalten der einzelnen Tabellen
* Die Einschränkungen
* Die Beziehungen zwischen Tabellen

Beim Organisieren von Schemata oder Tabellen in einem relationalen Datenmodell geht es um die Strukturierung Ihrer Daten in verschiedenen Tabellen. Stellen Sie sicher, dass jede Tabelle einen Entitäts-/Schematyp speichert.

➡️ [Weitere Informationen über Schemata finden Sie in der Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/ui/resources/schemas#create-model-based-schema)

## Implementierungsschritte {#implementation}

Gehen Sie wie folgt vor, um Daten aufzunehmen und ein relationales Schema zu erstellen:

1. Manuelles Erstellen eines [relationalen Schemas](manual-schema.md) oder Erstellen [mithilfe einer DDL-Datei](file-upload-schema.md)

   Definieren Sie die Struktur Ihres Datenmodells, einschließlich Tabellen, Attributen und Beziehungen. Entscheiden Sie, ob Sie das Schema manuell in der Benutzeroberfläche erstellen oder eine DDL-Datei hochladen möchten, um die Einrichtung zu beschleunigen.

   Wenn Sie das Schema manuell erstellen, muss der Datensatz auch manuell erstellt und aktiviert werden. Bei Verwendung einer DDL-Datei erfolgt die Erstellung und Aktivierung des Datensatzes automatisch.

1. [Verknüpfen von Schemata](file-upload-schema.md)

   Erstellen Sie Beziehungen zwischen Ihren Schemata, um konsistente Daten zu gewährleisten und entitätsübergreifende Abfragen zu ermöglichen. Sie können beispielsweise Treuetransaktionen mit Empfängerinnen und Empfängern oder Belohnungen mit Marken verknüpfen.

1. [Erstellen eines Datensatzes](manual-schema.md#dataset)

   Nachdem Sie Ihr Schema definiert haben, besteht der nächste Schritt darin, basierend darauf einen Datensatz zu erstellen. Dieser Datensatz dient als Speicher für Ihre aufgenommenen Daten.

1. [Aktivieren orchestrierter Kampagnen](manual-schema.md#enable)

   Dieser Datensatz speichert Ihre aufgenommenen Daten und muss für orchestrierte Kampagnen aktiviert sein, damit er in Adobe Journey Optimizer verfügbar ist. 

1. [Aufnehmen von Daten](ingest-data.md)

   Nehmen Sie Daten aus unterstützten Quellen wie SFTP, Cloud-Speicher oder Datenbanken in Adobe Experience Platform auf.

