---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurationsschritte
description: Erfahren Sie, wie Sie in Adobe Experience Platform ein relationales Schema erstellen, indem Sie eine DDL-Datei hochladen.
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 93%

---


# Erste Schritte mit relationalen Schemata und Datensätzen{#gs-schemas}

Dieses Handbuch führt Sie durch den Prozess der Erstellung eines relationalen Schemas, der Konfiguration eines Datensatzes für orchestrierte Kampagnen und der Aufnahme von Daten.

![](assets/do-not-localize/schema_admin.png)

Ein Datensatz ist ein Konstrukt zur Datenspeicherung und -verwaltung, in dem Daten (in der Regel) in einer Tabelle erfasst werden, die ein Schema (Spalten) und Felder (Zeilen) beinhaltet. Daten, die erfolgreich in Experience Platform aufgenommen werden, werden im Data Lake als Datensätze gespeichert.

Ein Schema stellt die Struktur und das Format von Daten dar und validiert sie. Es bietet eine abstrakte Definition eines realen Objekts (z. B. einer Person) und beschreibt, welche Daten in jeder Instanz dieses Objekts enthalten sein sollen (z. B. Name, Geburtstag usw.).


1. Manuelles Erstellen eines [relationalen Schemas](manual-schema.md) oder Erstellen [mithilfe einer DDL-Datei](file-upload-schema.md)

   Definieren Sie die Struktur Ihres Datenmodells, einschließlich Tabellen, Attributen und Beziehungen. Entscheiden Sie, ob Sie das Schema manuell in der Benutzeroberfläche erstellen oder eine DDL-Datei hochladen möchten, um die Einrichtung zu beschleunigen.

   Wenn Sie das Schema manuell erstellen, muss der Datensatz auch manuell erstellt und aktiviert werden. Bei Verwendung einer DDL-Datei erfolgt die Erstellung und Aktivierung des Datensatzes automatisch.

1. [Verknüpfen eines Schemas](file-upload-schema.md)

   Erstellen Sie Beziehungen zwischen Ihren Schemata, um konsistente Daten zu gewährleisten und entitätsübergreifende Abfragen zu ermöglichen. Sie können beispielsweise Treuetransaktionen mit Empfängerinnen und Empfängern oder Belohnungen mit Marken verknüpfen.

1. [Aufnehmen von Daten](ingest-data.md)

   Nehmen Sie Daten aus unterstützten Quellen wie SFTP, Cloud-Speicher oder Datenbanken in Adobe Experience Platform auf.

