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
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
topic_v2:
  - id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12b
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 534
ht-degree: 94%

---

# Leitlinien und Einschränkungen {#guardrails}

Unten finden Sie zusätzliche Leitlinien und Einschränkungen bei der Verwendung von orchestrierten Kampagnen.

## Einschränkungen beim Datenfluss

### Datendesign und -speicherung

* Der relationale Datenspeicher unterstützt **maximal 200 Tabellen** (Schemata).

* Bei orchestrierten Kampagnen darf die Gesamtgröße eines einzelnen Schemas **100 GB nicht überschreiten**.

* Tägliche Aktualisierungen eines Schemas sollten auf **weniger als 20 %** der Gesamtzahl der Einträge beschränkt werden, um Leistung und Stabilität zu gewährleisten.

* Relationale Daten sind das primäre Modell, das für die Anwendungsszenarien Aufnahme, Datenmodellierung und Segmentierung unterstützt wird.

* Schemata, die dem Targeting dienen, müssen mindestens **ein Identitätsfeld vom Typ`String`** enthalten, das einem definierten Identity-Namespace zugeordnet ist.

* Die durchschnittliche Anzahl von Attributen pro Schema **sollte 50 Spalten nicht überschreiten**, um Verwaltbarkeit und Leistung zu gewährleisten.

* Relationale Schemata können nicht für Adobe Experience Platform-**Profile** aktiviert werden. Bei Adobe Experience Platform-**Profilen** werden nur standardmäßige XDM-Schemata unterstützt. Relationale Schemata können für orchestrierte Kampagnen oder Aktionskampagnen aktiviert werden. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/experience-platform/catalog/datasets/user-guide#enable-profile)

### Datenaufnahme {#data-ingestion}

* Profil und relationale Datenaufnahme sind erforderlich.

* Alle Aufnahmen müssen über **Change Data Capture**-Quellen erfolgen:

   * Falls **dateibasiert**: Das Feld `_change_request_type` ist erforderlich. Unterstützte Werte sind `u` (upsert) oder `d` (delete). Diese Werte müssen kleingeschrieben sein (`u` und `d`), nicht großgeschrieben (`U` und `D`).

   * Falls **Cloud-basiert**: Die Tabellenprotokollierung muss aktiviert sein.

* **Teilaktualisierungen sind nicht zulässig**, sondern jede Zeile muss als vollständiger Eintrag angegeben werden.

* Die Batch-Aufnahme für die Kampagnenorchestrierung ist auf **einmal alle 15 Minuten** begrenzt.

* Die Aufnahmelatenz im relationalen Speicher beträgt in der Regel **15 Minuten bis 2 Stunden**, abhängig von:

   * Datenvolumen

   * System-Parallelität

   * Art des Vorgangs (z. B. sind Einfügungen schneller als Aktualisierungen)

* **Beziehung Datenfluss zu Datensatz ist 1:1**. Dies bedeutet, dass jeweils nur eine Quelle einen Datensatz befüllen kann. Um die Quelle zu wechseln, muss der vorhandene Datenfluss gelöscht und ein neuer Datenfluss mit der neuen Quelle erstellt werden.

### Datenmodellierung

* Alle Schemata, einschließlich Faktentabellen, müssen **einen Versionsdeskriptor** enthalten, um eine ordnungsgemäße Versionskontrolle und Rückverfolgbarkeit zu gewährleisten.

* Jede Tabelle muss über einen definierten **Primärschlüssel** verfügen, um Datenintegrität und nachgelagerte Vorgänge zu unterstützen.

* Der bei der Erstellung des Datensatzes zugewiesene `table_name` ist dauerhaft und wird in allen Segmentierungs- und Personalisierungsfunktionen verwendet.

* Im aktuellen Datenmodellierungs-Framework **werden Feldergruppen nicht unterstützt**.

* Die Unterstützung für zusammengesetzte Primärschlüssel mit Datei-Upload-Flüssen ist derzeit nicht verfügbar.

## Einschränkungen bei Aktivitäten

* In Zielgruppendefinitionen werden nur **Skalarattribute unterstützt** (**Zuordnungen und Arrays sind nicht zulässig**).

* **Segmentierungsaktivitäten basieren hauptsächlich auf relationalen Daten**. Es können zwar Profildaten enthalten sein, doch kann die Verwendung großer Profildatensätze die Leistung beeinträchtigen.

* **Beschränkungen werden für die Anzahl der Profilattribute durchgesetzt**, die sowohl in Batch- als auch in Streaming-Zielgruppen verwendet werden können. Das dient der Wahrung der Systemeffizienz.

* **Auflistungen** werden vollständig unterstützt.

* **Gelesene Zielgruppen werden nicht zwischengespeichert**, sondern bei jeder Kampagnenausführung wird eine vollständige Zielgruppenauswertung aus den zugrundeliegenden Daten ausgelöst.

* Eine **Optimierung wird dringend empfohlen**, wenn Sie mit Definitionen für große oder komplexe Zielgruppen arbeiten, um die Leistung zu wahren.

* **Gespeicherte Zielgruppenaktivitäten sind statisch**. Sie spiegeln die zum Zeitpunkt der Kampagnenausführung verfügbaren Daten wider.

* **Das Anhängen an eine Aktivität vom Typ „Gespeicherte Zielgruppe“ wird nicht unterstützt**. Jede Änderung erfordert eine vollständige Überschreibung der Zielgruppe.

## Kanalbeschränkungen

In orchestrierten Kampagnen werden nur die Kanäle SMS, Push, E-Mail und Briefpost unterstützt.
