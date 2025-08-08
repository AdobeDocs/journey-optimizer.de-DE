---
solution: Journey Optimizer
product: journey optimizer
title: Leitplanken und Einschränkungen für koordinierte Kampagnen
description: Erfahren Sie mehr über Schutzmechanismen und Einschränkungen bei orchestrierten Kampagnen
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: a4f3dce91af978bdff2de5beb8b1472f7704bdf2
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---


# Schutzmechanismen und Einschränkungen {#guardrails}

Unten finden Sie zusätzliche Leitplanken und Einschränkungen bei der Verwendung orchestrierter Kampagnen.

## Einschränkungen beim Datenfluss

### Datendesign und -speicherung

* Der relationale Datenspeicher unterstützt **maximal 200 Tabellen** (Schemata).

* Bei orchestrierten Kampagnen darf die Gesamtgröße eines einzelnen Schemas (**100 GB) nicht**.

* Tägliche Aktualisierungen eines Schemas sollten **auf weniger als 20 %** Gesamtzahl der Einträge beschränkt sein, um Leistung und Stabilität zu gewährleisten.

* Relationale Daten sind das primäre Modell, das für Anwendungsfälle der Aufnahme, Datenmodellierung und Segmentierung unterstützt wird.

* Zielgruppenschemata müssen mindestens **ein Identitätsfeld vom Typ`String`** enthalten, das einem definierten Identity-Namespace zugeordnet ist.

### Datenaufnahme

* Profil + relationale Datenerfassung sind erforderlich.

* Alle Aufnahmen müssen über **Change Data Capture)-** erfolgen:

   * Für **dateibasiert** ist `change_type` Feld erforderlich.

   * Für **Cloud-basiert** muss die Tabellenprotokollierung aktiviert sein.

* **Direkte Aktualisierungen an Snowflake oder Datensätzen werden nicht unterstützt**. Das System ist schreibgeschützt. Alle Änderungen müssen über die Änderungsdatenerfassung angewendet werden.

* **ETL-Prozesse werden nicht**. Die Daten müssen vor der Aufnahme vollständig in das erforderliche Format umgewandelt werden.

* **Teilaktualisierungen sind nicht zulässig** muss jede Zeile als vollständiger Datensatz angegeben werden.

* Die Batch-Aufnahme für die Kampagnenorchestrierung ist auf **einmal alle 15 Minuten)**.

* Die Aufnahmelatenz, d. h. die Zeit von der Aufnahme bis zur Verfügbarkeit in Snowflake, **in der Regel zwischen 15 Minuten** 2 Stunden, abhängig von:

   * Datenvolumen

   * Systemparallelität

   * Art des Vorgangs, z. B. Einfügungen sind schneller als Aktualisierungen

### Datenmodellierung

* Alle Schemata, einschließlich Faktentabellen, müssen **einen Versionsdeskriptor** enthalten, um eine ordnungsgemäße Versionskontrolle und Rückverfolgbarkeit zu gewährleisten.

* Jede Tabelle muss über einen definierten **Primärschlüssel) verfügen** um die Datenintegrität und nachgelagerte Vorgänge zu unterstützen.

* Die bei der Erstellung des Datensatzes zugewiesene `table_name` ist dauerhaft und wird in allen Segmentierungs- und Personalisierungsfunktionen verwendet.

* **Feldergruppen werden im** Datenmodellierungs-Framework nicht unterstützt.

## Einschränkungen bei Aktivitäten

* In Zielgruppendefinitionen werden nur **Skalarattribute unterstützt** (**und Arrays sind nicht zulässig**.

* **Segmentierungsaktivitäten basieren hauptsächlich auf relationalen Daten**. Es können zwar Profildaten enthalten sein, die Verwendung großer Profildatensätze kann jedoch die Leistung beeinträchtigen.

* **Beschränkungen werden für die Anzahl der Profilattribute durchgesetzt** die sowohl in Batch- als auch in Streaming-Zielgruppen verwendet werden können, um die Systemeffizienz zu erhalten.

* **Liste der Werte (LOVs** und **Auflistungen** werden vollständig unterstützt.

* **Zielgruppen lesen wird nicht zwischengespeichert** Bei jeder Kampagnenausführung wird eine vollständige Zielgruppenauswertung aus den zugrunde liegenden Daten Trigger.

* **Optimierung wird dringend empfohlen** wenn Sie mit Definitionen für große oder komplexe Zielgruppen arbeiten, um die Leistung sicherzustellen.

* **Gespeicherte Zielgruppenaktivitäten sind statisch** sie spiegeln die zum Zeitpunkt der Kampagnenausführung verfügbaren Daten wider.

* **Das Anhängen an eine Aktivität vom Typ Gespeicherte Zielgruppe wird nicht unterstützt**. Alle Änderungen erfordern eine vollständige Überschreibung der Zielgruppe.

## Kanalbeschränkungen

In orchestrierten Kampagnen werden nur die Kanäle SMS, Push und E-Mail unterstützt.
