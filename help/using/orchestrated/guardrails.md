---
solution: Journey Optimizer
product: journey optimizer
title: Leitlinien und Einschränkungen bei orchestrierten Kampagnen
description: Grundlegendes über Leitlinien und Einschränkungen bei orchestrierten Kampagnen
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/ViPJaOPo-AT-naQqq-PaPw-BI5YupYuYAEy56AUEp2A
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
topic_v2:
  - id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12b
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 18f6b23dbbe53e486e5af76ef7cc61fa1784475d
workflow-type: tm+mt
source-wordcount: 734
ht-degree: 12%

---

# Leitlinien und Einschränkungen {#guardrails}

Unten finden Sie zusätzliche Leitlinien und Einschränkungen bei der Verwendung von orchestrierten Kampagnen.

## Einschränkungen beim Datenfluss

### Datendesign und -speicherung

* **Maximale Tabellen** - Der relationale Datenspeicher unterstützt maximal 200 Tabellen (Schemata).

* **Schemagröße** - Bei orchestrierten Kampagnen darf die Gesamtgröße eines einzelnen Schemas 100 GB nicht überschreiten.

* **Tägliches Aktualisierungsvolumen** - Tägliche Aktualisierungen eines Schemas sollten auf weniger als 20 % der gesamten Datensatzanzahl beschränkt sein, um die Leistung und Stabilität zu gewährleisten.

* **Relationales Datenmodell** - Relationale Daten sind das primäre Modell, das für die Aufnahme, Datenmodellierung und Segmentierung von Anwendungsfällen unterstützt wird.

* **Identitätsfeld** - Schemata, die für die Zielgruppenbestimmung verwendet werden, müssen mindestens ein Identitätsfeld vom Typ `String` enthalten, das einem definierten Identity-Namespace zugeordnet ist.

* **Attribute pro Schema** - Die durchschnittliche Anzahl von Attributen pro Schema sollte 50 Spalten nicht überschreiten, um Verwaltbarkeit und Leistung zu erhalten.

* **Profilaktivierung** - Relationale Schemata können nicht für Adobe Experience Platform-Profile aktiviert werden. Für Adobe Experience Platform-Profile werden nur standardmäßige XDM-Schemata unterstützt. Relationale Schemata können für orchestrierte Kampagnen oder Aktionskampagnen aktiviert werden. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/experience-platform/catalog/datasets/user-guide#enable-profile)

### Datenaufnahme {#data-ingestion}

* **Profil- und relationale Aufnahme** - Die Aufnahme von Profil und relationalen Daten ist erforderlich.

* **Ändern von Datenerfassungsquellen** - Alle Aufnahmen müssen über eine Änderung der Datenerfassungsquellen erfolgen:

   * **Dateibasierte Quellen** - Das `_change_request_type` Feld ist erforderlich. Unterstützte Werte sind `u` (upsert) oder `d` (delete). Diese Werte müssen kleingeschrieben sein (`u` und `d`), nicht großgeschrieben (`U` und `D`).

   * **Cloud-basierte Quellen** - Die Tabellenprotokollierung muss aktiviert sein.

* **Nur vollständige Datensätze** - Teilweise Aktualisierungen von Datensätzen sind nicht zulässig; jede Zeile muss als vollständiger Datensatz bereitgestellt werden.

* **Batch-Aufnahme** - Die Batch-Aufnahme für die Kampagnenorchestrierung ist auf einmal alle 15 Minuten beschränkt.

* **Aufnahmelatenz** - Die Aufnahmelatenz im relationalen Speicher liegt in der Regel zwischen 15 Minuten und 2 Stunden, abhängig von:

   * Datenvolumen

   * System-Parallelität

   * Art des Vorgangs (z. B. sind Einfügungen schneller als Aktualisierungen)

* **Datenfluss-Datensatz-Beziehung** - Die Beziehung zwischen Datenfluss und Datensatz ist 1-1. Es kann jeweils nur eine Quelle für einen Datensatz verwendet werden. Um die Quelle zu wechseln, löschen Sie den vorhandenen Datenfluss und erstellen Sie einen neuen Datenfluss mit der neuen Quelle.

### Datenmodellierung

* **Versionsdeskriptor** - Alle Schemata, einschließlich Faktentabellen, müssen einen Versionsdeskriptor enthalten, um eine ordnungsgemäße Versionskontrolle und Rückverfolgbarkeit sicherzustellen.

* **Primärer Schlüssel** - Jede Tabelle muss über einen definierten Primärschlüssel verfügen, um die Datenintegrität und nachgelagerte Vorgänge zu unterstützen.

* **Dauerhafter Tabellenname** - Die während der Datensatzerstellung zugewiesene `table_name` ist dauerhaft und wird in allen Segmentierungs- und Personalisierungsfunktionen verwendet.

* **Feldergruppen** - Feldergruppen werden im aktuellen Datenmodellierungs-Framework nicht unterstützt.

* **Zusammengesetzte Primärschlüssel** - Die Unterstützung für zusammengesetzte Primärschlüssel mit Datei-Upload-Flüssen ist derzeit nicht verfügbar.

## Einschränkungen bei Aktivitäten {#activities-limitations}

* **Kanalaktivitätslimit** - Eine orchestrierte Kampagne unterstützt maximal 10 Kanalaktivitäten (E-Mail, SMS, Push oder Briefpost). Für dieses Limit zählen nur Kanalaktivitäten. Zielgruppenbestimmungs- und Flusssteuerungsaktivitäten werden nicht gezählt (z. B. Zielgruppe aufbauen, Warten, Aufspaltung, Anreicherung, Abstimmung, Verzweigung, Ende oder Test).

  Wenn Sie das Limit beim Speichern oder Veröffentlichen überschreiten, schlägt der Vorgang fehl. Um innerhalb des Limits zu bleiben, reduzieren Sie die Anzahl der Kanalaktivitäten oder teilen Sie den Nachrichtenversand auf mehrere orchestrierte Kampagnen auf.

* **Limit für Canvas** - Die Anzahl der Aktivitäten auf einer orchestrierten Kampagnen-Arbeitsfläche ist auf 500 begrenzt. Diese Beschränkung gilt für alle Aktivitätstypen auf der Arbeitsfläche. Dies ist vom Kanalaktivitätslimit, das bei der Veröffentlichung erzwungen wird, getrennt. Halten Sie Workflows aus Gründen der Wartbarkeit und Leistung in der Praxis unter 100 Aktivitäten.

* **Nur Skalarattribute** - In Zielgruppendefinitionen werden nur Skalarattribute unterstützt. Zuordnungen und Arrays sind nicht zulässig.

* **Relationale Daten für die Segmentierung** - Segmentierungsaktivitäten basieren hauptsächlich auf relationalen Daten. Es können zwar Profildaten enthalten sein, doch kann die Verwendung großer Profildatensätze die Leistung beeinträchtigen.

* **Profilattributbeschränkungen** - Beschränkungen werden für die Anzahl der Profilattribute erzwungen, die sowohl in Batch- als auch in Streaming-Zielgruppen verwendet werden können, um die Systemeffizienz zu erhalten.

* **Auflistungen** - Auflistungen werden vollständig unterstützt.

* **Zielgruppen lesen nicht zwischengespeichert** - Zielgruppen lesen werden nicht zwischengespeichert; bei jeder Kampagnenausführung wird eine vollständige Zielgruppenauswertung aus den zugrunde liegenden Daten Trigger.

* **Zielgruppenoptimierung** - Eine Optimierung wird dringend empfohlen, wenn Sie mit großen oder komplexen Zielgruppendefinitionen arbeiten, um die Leistung sicherzustellen.

* **Gespeicherte Zielgruppen sind statisch** - Gespeicherte Zielgruppenaktivitäten sind statisch und spiegeln die zum Zeitpunkt der Kampagnenausführung verfügbaren Daten wider.

* **An gespeicherte Zielgruppe nicht anhängen** - Das Anfügen an eine Aktivität vom Typ „Gespeicherte Zielgruppe“ wird nicht unterstützt. Jede Änderung erfordert eine vollständige Überschreibung der Zielgruppe.

## Kanalbeschränkungen

In orchestrierten Kampagnen werden nur die Kanäle SMS, Push, E-Mail und Briefpost unterstützt.
