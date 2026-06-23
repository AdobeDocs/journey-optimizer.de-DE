---
solution: Journey Optimizer
product: journey optimizer
title: Aktivität „Optimieren“
description: Weitere Informationen zur Aktivität „Optimieren“
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: Aktivität, Bedingung, Arbeitsfläche, Journey, Optimierung
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/hbDoGEHdCBcOe-e9h06kGY2Rvb129cIzto6jJAuGkX4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1094
ht-degree: 19%

---

# Erste Schritte mit der Aktivität „Optimieren“ {#journey-path-optimization}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie mit der Aktivität Optimieren mehrere Journey-Pfade erstellen, die auf Experimenten, Targeting und Bedingungen basieren. Dabei wird die frühere Aktivität Bedingung ersetzt.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Aktivität „Optimieren“"
>abstract="Mit der Aktivität **Optimieren** können Sie festlegen, wie Einzelpersonen Ihre Journey durchlaufen, indem Sie mehrere Pfade auf der Grundlage spezifischer Kriterien erstellen, darunter Experimente, Targeting und bestimmte Bedingungen. Beachten Sie, dass die Aktivität **Optimieren** die neue Funktion zum Erstellen bedingter Pfade in Journeys ist. Sie ersetzt die frühere Aktivität **Bedingung**."

>[!IMPORTANT]
>
>Die Aktivität **Optimieren** ist das neue Vehikel zum Erstellen bedingter Pfade in Journey. Sie ersetzt die frühere Aktivität **Bedingung**, die aus der Benutzeroberfläche entfernt wurde. Die gesamte bedingte Logik wird beibehalten und jetzt über die [Bedingungen **der Aktivität** Optimieren](conditions.md) verarbeitet.
>
>Wenn Sie über Journey verfügen, die **[!UICONTROL Bedingungs]**-Aktivitäten verwendet haben, können Sie diese weiterhin wie zuvor verwenden. Sie werden jetzt mit einem neuen Symbol als **[!UICONTROL Optimieren]**-Aktivitäten mit der **[!UICONTROL Bedingung]**-Methode angezeigt, das Verhalten ist jedoch unverändert. Jede benutzerdefinierte Beschriftung, die Sie auf dem Knoten festgelegt hatten, wird beibehalten.

Mit der Aktivität **Optimieren** können Sie festlegen, wie Einzelpersonen Ihre Journey durchlaufen, indem Sie mehrere **Pfade** auf der Grundlage spezifischer Kriterien erstellen, darunter Experimente, Targeting und bestimmte Bedingungen. So gewährleisten Sie ein Höchstmaß an Engagement und Erfolg, um hochgradig personalisierte und effektive Journeys zu erstellen.

![Schaltfläche „Optimieren“ in der Palette „Journey-Aktivität“](assets/journey-optimize.png)

## Was ist ein Journey-Pfad? {#journey-path}

Ein Journey-**Pfad** kann aus beliebigen der folgenden Variablen bestehen: Sequenzierung von Nachrichten, dazwischen liegende Zeit, Anzahl der Nachrichten oder eine beliebige Kombination dieser drei Variablen.

Ein Pfad kann beispielsweise eine E-Mail enthalten, ein anderer zwei SMS-Nachrichten und ein dritter eine E-Mail, einen Knoten, um zwei Stunden zu warten, und dann eine SMS-Nachricht.

## Drei Möglichkeiten zur Optimierung Ihrer Journey {#optimization-methods}

Durch die Aktivität **Optimieren** können Sie die folgenden Aktionen für Ihre Journey-Pfade ausführen:

* [Pfadexperimente ausführen](path-experimentation.md) - Testen Sie verschiedene Pfade basierend auf zufälligen Aufspaltungen, um anhand vordefinierter Erfolgsmetriken (z. B. Konversionsrate, Umsatz, Interaktion) zu bestimmen, welche am besten abschneidet.

* [Nutzen von Zielgruppenregeln](path-targeting.md) - Definieren Sie spezifische Regeln, die erfüllt sein müssen, damit eine Kundin oder ein Kunde auf der Grundlage von Zielgruppensegmenten, Profilattributen oder kontextuellen Daten für die Eingabe eines der Journey-Pfade berechtigt ist. Dadurch wird sichergestellt, dass die richtige Zielgruppe den angegebenen Pfad eingibt.

  >[!AVAILABILITY]
  >
  >Diese Funktion ist derzeit nur eingeschränkt verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern.

* [Bedingungen anwenden](conditions.md) - Erstellen Sie bedingte Pfade basierend auf bestimmten Kriterien wie Datenquellen, Zeit, Datum, Prozentaufspaltungen oder Profilobergrenzen. Dies entspricht der vorherigen Aktivität vom Typ Bedingung .

## Funktionsweise {#how-it-works}

Sobald die Journey live ist, werden die Profile anhand der definierten Kriterien bewertet und basierend auf den passenden Kriterien auf den entsprechenden Pfad der Journey weitergeleitet.

## Nächste Schritte {#next-steps}

Wählen Sie die Optimierungsmethode aus, die am besten zu Ihrem Anwendungsfall passt:

* Möchten Sie testen und erfahren, welcher Pfad am besten funktioniert? → Gehen Sie zu [Pfadexperiment](path-experimentation.md)
* Möchten Sie verschiedene Zielgruppen über bestimmte Pfade senden? → Gehe zu [Pfad-Targeting](path-targeting.md)
* Möchten Sie eine bedingte Logik erstellen (if/then-Szenarien)? → Gehen Sie zu [Bedingungen](conditions.md)

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite wird die Aktivität „Optimieren“ vorgestellt, die die frühere Bedingungsaktivität ersetzt. Damit können Benutzende mithilfe von Experimenten, Zielgruppenbestimmungsregeln oder Bedingungslogiken mehrere Journey-Pfade erstellen.

**intents:**

* Erfahren Sie, was die Aktivität „Optimieren“ tut und wie sie die frühere Aktivität „Bedingung“ ersetzt
* Erstellen mehrerer Journey-Pfade mithilfe von Pfadexperimenten (A/B-Tests)
* Definieren Sie Zielgruppenbestimmungsregeln, um bestimmte Zielgruppensegmente oder Profilattribute über separate Pfade zu routen
* Anwenden von Bedingungslogik (if/then) mithilfe der Bedingungsmethode in der Aktivität „Optimieren“
* Migrieren Sie vorhandene Journey, die die Aktivität Bedingung verwendet haben, in die neue Aktivität Optimieren .

**Glossar:**

* **Aktivität optimieren**: Die Journey-Arbeitsflächen-Aktivität, die die frühere Bedingungsaktivität ersetzt und die Erstellung mehrerer Pfade über Experimentieren, Targeting oder Bedingungen ermöglicht. *(produktspezifisch)*
* **Journey-Pfad**: Eine Sequenz innerhalb eines Journey, die aus Kommunikationen, Wartezeiten, der Anzahl von Nachrichten oder einer beliebigen Kombination bestehen kann. Profile werden auf der Grundlage von in der Aktivität „Optimieren“ definierten Kriterien an einen Pfad weitergeleitet. *(produktspezifisch)*
* **Pfadexperiment**: Eine Optimieren-Methode, die Profile nach dem Zufallsprinzip auf Pfade aufteilt, um zu bestimmen, welche am besten mit vordefinierten Erfolgsmetriken wie Konversionsrate oder Umsatz abschneidet. *(produktspezifisch)*
* **Pfad-Targeting**: Eine Optimierungsmethode (derzeit eingeschränkt verfügbar), die Profile basierend auf Zielgruppensegmenten, Profilattributen oder kontextuellen Daten an Pfade weiterleitet. *(produktspezifisch)*
* **Bedingungen**: Eine Optimize-Methode, die der vorherigen Bedingungsaktivität entspricht, das Erstellen bedingter Pfade basierend auf Datenquellen, Zeit, Datum, Prozentaufspaltungen oder Profilbegrenzungen. *(produktspezifisch)*

**Leitplanken:**

* Pfad-Targeting ist derzeit nur eingeschränkt verfügbar — Adobe-Support kontaktieren, um Zugang zu erhalten
* Die vorherige Aktivität Bedingung wurde aus der Benutzeroberfläche entfernt. Bestehende Journey, die sie verwenden, funktionieren weiterhin und werden jetzt mit einem neuen Symbol als Aktivitäten optimieren unter Verwendung der Methode Bedingungen angezeigt
* Benutzerdefinierte Kennzeichnungen, die auf früheren Bedingungsknoten festgelegt wurden, bleiben nach der Migration zu „Optimieren“ erhalten

**Terminologie:**

* Kanonischer Name: Aktivität optimieren — Akronym: none — Varianten: Journey-Pfadoptimierung, Knoten optimieren
* Synonyme: „Aktivität optimieren (Bedingungsmethode)“ = „frühere Bedingungsaktivität“
* Nicht verwechseln: „Pfadexperiment“ ≠ „Pfadzielgruppenbestimmung“ - Beim Pfadexperiment wird per zufälliger Aufteilung getestet, welcher Pfad am besten funktioniert. Beim Pfadzielgruppenbestimmung werden definierte Regeln verwendet, um bestimmte Zielgruppen zu bestimmten Pfaden zu leiten

**FAQ:**

* **F: Was ist mit der Aktivität Bedingung passiert?** — Sie wurde durch die Aktivität Optimieren ersetzt und aus der Benutzeroberfläche entfernt. Bestehende Journey, die Bedingungsaktivitäten verwendet haben, funktionieren weiterhin unverändert. Sie werden jetzt mit einem neuen Symbol als Optimierungsaktivitäten mithilfe der Bedingungsmethode angezeigt.
* **F: Welche drei Methoden stehen in der Aktivität „Optimieren“ zur Verfügung?** — Pfadexperiment (zufällige A/B-Aufspaltung zur Ermittlung des Pfads mit der besten Leistung), Pfadzielgruppenbestimmung (regelbasiertes Routing nach Zielgruppen- oder Profilattributen, derzeit eingeschränkt verfügbar) und Bedingungen (wenn/dann Bedingungslogik, die der vorherigen Bedingungsaktivität entspricht).
* **F: Wie unterscheidet sich das Pfadexperiment vom Pfad-Targeting?** — Durch Pfadexperimente werden Profile nach dem Zufallsprinzip aufgeteilt, um die Leistung des Pfads mit Erfolgsmetriken zu testen und zu vergleichen. Beim Pfad-Targeting werden bestimmte Zielgruppen oder Profiltypen auf der Grundlage definierter Kriterien durch bestimmte Pfade geleitet.
* **F: Ist das Pfad-Targeting allgemein verfügbar?** — Nein, es ist derzeit nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.
* **F: Was ist ein Journey-Pfad?** - Ein Pfad ist eine Sequenz innerhalb einer Journey, die eine Kombination aus Nachrichten, Wartezeiten und der Anzahl der Nachrichten enthalten kann. Profile werden anhand der Aktivitätskriterien „Optimieren“ ausgewertet und zum entsprechenden Pfad weitergeleitet.

+++
