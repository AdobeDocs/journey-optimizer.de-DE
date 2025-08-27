---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurationsschritte
description: Erfahren Sie, wie Sie in Adobe Experience Platform ein relationales Schema erstellen, indem Sie eine DDL hochladen
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
source-git-commit: 1cd98a42d6d30b21ea5fb6f8d6c745bf735b0e6c
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 3%

---


# Erste Schritte mit relationalen Schemata und Datensätzen{#gs-schemas}

Dieses Handbuch führt Sie durch den Prozess der Erstellung eines relationalen Schemas, der Konfiguration eines Datensatzes für orchestrierte Kampagnen und der Aufnahme von Daten.

![](assets/do-not-localize/schema_admin.png)

1. Erstellen [relationalen Schemas manuell](manual-schema.md) oder [mithilfe einer DDL-Datei](file-upload-schema.md)

   Definieren Sie die Struktur Ihres Datenmodells, einschließlich Tabellen, Attributen und Beziehungen. Wählen Sie, das Schema manuell in der Benutzeroberfläche zu erstellen oder eine DDL-Datei hochzuladen, um die Einrichtung zu beschleunigen.

   Wenn Sie das Schema manuell erstellen, muss der Datensatz auch manuell erstellt und aktiviert werden. Bei Verwendung einer DDL-Datei erfolgt die Erstellung und Aktivierung von Datensätzen automatisch.

1. [Verknüpfen eines Schemas](file-upload-schema.md)

   Erstellen Sie Beziehungen zwischen Ihren Schemata, um Datenkonsistenz zu gewährleisten und entitätsübergreifende Abfragen zu ermöglichen. Verknüpfen Sie beispielsweise Treuetransaktionen mit Empfängern oder Belohnungen mit Marken.

1. [Aufnehmen von Daten](ingest-data.md)

   Importieren Sie Daten aus unterstützten Quellen wie SFTP, Cloud-Speicher oder Datenbanken in Adobe Experience Platform.

