---
solution: Journey Optimizer
product: journey optimizer
title: Leitlinien und Einschränkungen bei orchestrierten Kampagnen
description: Grundlegendes über Leitlinien und Einschränkungen bei orchestrierten Kampagnen
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
version: Campaign Orchestration
source-git-commit: 266bf3afde663b17aedce5fb51e7c5f424fee9ad
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 97%

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

* Die durchschnittliche Anzahl von Attributen pro Schema **sollte 50 Spalten nicht überschreiten**, um Verwaltbarkeit und Leistung zu gewährleisten.

* Relationale Schemata können nicht für Adobe Experience Platform-**Profile** aktiviert werden. Bei Adobe Experience Platform-**Profilen** werden nur standardmäßige XDM-Schemata unterstützt. Relationale Schemata können für orchestrierte Kampagnen oder Aktionskampagnen aktiviert werden. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/experience-platform/catalog/datasets/user-guide#enable-profile)

### Datenaufnahme

* Profil und relationale Datenaufnahme sind erforderlich.

* Alle Aufnahmen müssen über **Change Data Capture**-Quellen erfolgen:

   * Falls **dateibasiert**: Das Feld `_change_request_type` ist erforderlich. Unterstützte Werte sind `U` (upsert) oder `D` (delete).

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
