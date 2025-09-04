---
solution: Journey Optimizer
product: journey optimizer
title: Leitlinien und Einschränkungen bei orchestrierten Kampagnen
description: Grundlegendes über Leitlinien und Einschränkungen bei orchestrierten Kampagnen
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 100%

---


# Leitlinien und Einschränkungen {#guardrails}

Unten finden Sie zusätzliche Leitlinien und Einschränkungen bei der Verwendung von orchestrierten Kampagnen.

## Einschränkungen beim Datenfluss

### Daten-Design- und -Speicherung

* Der relationale Datenspeicher unterstützt **maximal 200 Tabellen** (Schemata).

* Bei orchestrierten Kampagnen darf die Gesamtgröße eines einzelnen Schemas **100 GB nicht überschreiten**.

* Tägliche Aktualisierungen eines Schemas sollten auf **weniger als 20 %** der Gesamtzahl der Einträge beschränkt werden, um Leistung und Stabilität zu gewährleisten.

* Relationale Daten sind das primäre Modell, das für die Anwendungsszenarien Aufnahme, Datenmodellierung und Segmentierung unterstützt wird.

* Schemata, die dem Targeting dienen, müssen mindestens **ein Identitätsfeld vom Typ`String`** enthalten, das einem definierten Identity-Namespace zugeordnet ist.

### Datenaufnahme

* Profil und relationale Datenaufnahme sind erforderlich.

* Alle Aufnahmen müssen über **Change Data Capture**-Quellen erfolgen:

   * Falls **dateibasiert**: Das Feld `_change_request_type` ist erforderlich.

   * Falls **Cloud-basiert**: Die Tabellenprotokollierung muss aktiviert sein.

* **Direkte Aktualisierungen in Snowflake oder Datensätzen werden nicht unterstützt**. Das System ist schreibgeschützt. Alle Änderungen müssen über die Änderungsdatenerfassung (Change Data Capture) angewendet werden.

* **ETL-Prozesse werden nicht unterstützt**. Daten müssen vor der Aufnahme vollständig in das erforderliche Format umgewandelt werden.

* **Teilaktualisierungen sind nicht zulässig**, sondern jede Zeile muss als vollständiger Eintrag angegeben werden.

* Die Batch-Aufnahme für die Kampagnenorchestrierung ist auf **einmal alle 15 Minuten** begrenzt.

* Die Aufnahmelatenz, d. h. die Zeit von der Aufnahme bis zur Verfügbarkeit in Snowflake, variiert in der Regel **zwischen 15 Minuten und 2 Stunden**, je nach:

   * Datenvolumen

   * System-Parallelität

   * Art des Vorgangs (z. B. sind Einfügungen schneller als Aktualisierungen)

### Datenmodellierung

* Alle Schemata, einschließlich Faktentabellen, müssen **einen Versionsdeskriptor** enthalten, um eine ordnungsgemäße Versionskontrolle und Rückverfolgbarkeit zu gewährleisten.

* Jede Tabelle muss über einen definierten **Primärschlüssel** verfügen, um Datenintegrität und nachgelagerte Vorgänge zu unterstützen.

* Der bei der Erstellung des Datensatzes zugewiesene `table_name` ist dauerhaft und wird in allen Segmentierungs- und Personalisierungsfunktionen verwendet.

* Im aktuellen Datenmodellierungs-Framework **werden Feldergruppen nicht unterstützt**.

## Einschränkungen bei Aktivitäten

* In Zielgruppendefinitionen werden nur **Skalarattribute unterstützt** (**Zuordnungen und Arrays sind nicht zulässig**).

* **Segmentierungsaktivitäten basieren hauptsächlich auf relationalen Daten**. Es können zwar Profildaten enthalten sein, doch kann die Verwendung großer Profildatensätze die Leistung beeinträchtigen.

* **Beschränkungen werden für die Anzahl der Profilattribute durchgesetzt**, die sowohl in Batch- als auch in Streaming-Zielgruppen verwendet werden können. Das dient der Wahrung der Systemeffizienz.

* **Wertelisten (List of Values, LOV)** und **Aufzählungen** werden vollständig unterstützt.

* **Gelesene Zielgruppen werden nicht zwischengespeichert**, sondern bei jeder Kampagnenausführung wird eine vollständige Zielgruppenauswertung aus den zugrundeliegenden Daten ausgelöst.

* Eine **Optimierung wird dringend empfohlen**, wenn Sie mit Definitionen für große oder komplexe Zielgruppen arbeiten, um die Leistung zu wahren.

* **Gespeicherte Zielgruppenaktivitäten sind statisch**. Sie spiegeln die zum Zeitpunkt der Kampagnenausführung verfügbaren Daten wider.

* **Das Anhängen an eine Aktivität vom Typ „Gespeicherte Zielgruppe“ wird nicht unterstützt**. Jede Änderung erfordert eine vollständige Überschreibung der Zielgruppe.

## Kanalbeschränkungen

In orchestrierten Kampagnen werden nur die Kanäle SMS, Push und E-Mail unterstützt.
