---
solution: Journey Optimizer
product: journey optimizer
title: Verwalten von Tags in Journeys
description: Verwalten von Tags in Journeys
feature: Journeys, Tags
topic: Content Management
role: User
level: Intermediate
keywords: Journey, Tags
exl-id: 44c255d1-121c-47d4-b407-161626ca3cb4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/O8Igbj-JJGr0aej8xbSvZ51xkcJq8LeJ9JiveyBjBqQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1152
ht-degree: 22%

---

# Verwalten von Tags in Journeys {#journey_tags}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Sie Journey mit Tags und Tag-Kategorien organisieren können, damit Sie Ihre Journey einfacher klassifizieren, filtern und finden können als mit Namenskonventionen.

>[!ENDSHADEBOX]

Mit Journey Optimizer können Sie Ihre Journeys mithilfe von Tags organisieren. Tags sind eine schnelle und einfache Möglichkeit, Objekte zu klassifizieren, um die Suche zu verbessern.

## Tags vs. Namenskonventionen {#tags-vs-naming}

Teams verwenden häufig komplexe Namenskonventionen, um Metadaten direkt in Journey-Namen zu speichern - z. B.: *Lifecycle Marketing - Bildung - Customer Onboarding V2 - App Education - Q3 2025*. Dieser Ansatz hat zwar gute Absichten, weist jedoch eine wichtige Schwäche auf: Da die Arbeit von Team-Mitgliedern skaliert werden kann, wird die Konvention nur selten konsistent angewendet, und die Navigation auf Journey-Listen wird immer schwieriger.

**Tag-Kategorien** in Journey Optimizer bieten eine bessere Alternative. Anstatt Metadaten im Namen zu kodieren, fügen Sie jedem Journey kategorisierte Tags hinzu (z. B. Team, Ziel, Phase, Quartal) und verwenden Filter, um sie zu finden. Journey-Namen können sich dann auf das konzentrieren, worauf es wirklich ankommt: auf den Meilenstein, der vom Kunden vorangetrieben wird.

Vorteile von Tag-Kategorien gegenüber Namenskonventionen:

* **Konsistenz** - Tags werden aus einer kontrollierten Liste ausgewählt und nicht frei eingegeben.
* **Filterability** - Jede beliebige Kombination von Tag-Werten kann verwendet werden, um die Journey-Liste sofort in Abschnitte zu unterteilen.
* **Clarity** - Journey-Namen bleiben kurz und Meilenstein-fokussiert.
* **Skalierbarkeit** - Das Hinzufügen einer neuen Metadatendimension bedeutet, dass eine neue Tag-Kategorie erstellt wird, anstatt eine Namenskonvention neu zu schreiben.

Informationen zu empfohlenen Setup-Workflows finden Sie [Einrichten von Tag-Kategorien für die Journey-Verwaltung](#tags-setup) unten.

## Hinzufügen von Tags zu einer Journey

Mit dem Feld **Tags** in den Journey-Eigenschaften können Sie Tags für Ihre Journey definieren. Sie können entweder ein vorhandenes Tag auswählen oder ein neues erstellen. Geben Sie den Anfang des Namens des gewünschten Tags ein und wählen Sie es aus der Liste aus. Wenn es nicht verfügbar ist, klicken Sie auf **Erstellen**, um ein neues zu erstellen und zu Ihrer Journey hinzuzufügen. Sie können beliebig viele Tags definieren.

![Panel „Tags“ in den Journey-Eigenschaften für Kategorisierung und Organisation](assets/tags1.png)

Die Liste der definierten Tags wird unter dem Feld **Tags** angezeigt.

>[!NOTE]
>
> Bei Tags wird die Groß-/Kleinschreibung nicht beachtet.
> 
> Wenn Sie eine Journey duplizieren oder eine neue Version einer Journey erstellen, bleiben Tags erhalten.

## Filtern nach Tags

In der Journey-Liste wird eine spezielle Spalte angezeigt, sodass Sie Ihre Tags einfach visualisieren können.

Es ist auch ein Filter verfügbar, um nur Journeys mit bestimmten Tags anzuzeigen.

![Dropdown-Liste zur Tag-Auswahl mit verfügbaren Tags für die Journey-Klassifizierung](assets/tags2.png)

Sie können Tags zu beliebigen Typen von Journeys (Live, Entwurf usw.) hinzufügen oder daraus entfernen. Klicken Sie auf das Symbol **Mehr Aktionen** neben der Journey und wählen Sie **Tags bearbeiten** aus.

![Journey-Liste gefiltert nach Tags mit kategorisierten Journeys](assets/tags3.png)

## Verwalten von Tags

Admins können Tags löschen und mithilfe des Menüs **Tags** unter **ADMINISTRATION** nach Kategorien organisieren. In dieser [Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/overview.html?lang=de) finden Sie weitere Informationen.

>[!NOTE]
>
> In Journeys definierte Tags werden der integrierten Kategorie „Nicht kategorisiert“ hinzugefügt.

## Einrichten von Tag-Kategorien für die Journey-Verwaltung {#tags-setup}

Führen Sie diese Schritte aus, um eine komplexe Namenskonvention durch einen Tag-basierten Ansatz in Ihrem gesamten Team zu ersetzen.

**Schritt 1 - Tag-Kategorien erstellen (Admin)**

Erstellen Sie unter **[!UICONTROL Administration]** > **[!UICONTROL Tags]** eine Kategorie für jedes Metadatenattribut, das Ihr Team derzeit als Journey-Namen kodiert - zum Beispiel: *Team*, *Marketing-Ziel*, *Campaign*, *Phase*, *Quartal*.

**Schritt 2 - Füllen Sie jede Kategorie mit Tag-Werten (Admin)**

Erstellen Sie innerhalb jeder Kategorie die Tags, die alle möglichen Werte darstellen. Beispielsweise könnte die Kategorie *Phase* Folgendes enthalten: *Awareness*, *Onboarding*, *Retention*, *Win-back*.

**Schritt 3 - Tags beim Erstellen von Journeys (Anwendende) anwenden**

Wählen Sie bei jeder Erstellung einer neuen Journey das entsprechende Tag aus jeder Kategorie in den Journey-Eigenschaften aus. Eine Journey trägt in der Regel ein Tag pro Kategorie.

**Schritt 4 - Benennen Sie die Journey für den Meilenstein, filtern Sie nach Tags**

Konzentrieren Sie den Journey-Namen weiterhin auf den zugrunde liegenden Kunden-Meilenstein (z. B. *Erste Treuetransaktion*). Verwenden Sie Tag-Filter in der Journey-Liste, um Journey mithilfe einer beliebigen Kombination von Metadaten zu finden, ohne auf das Parsen von Namen angewiesen zu sein.

>[!TIP]
>
>Eine ausführliche Erläuterung dieses Ansatzes und seiner Vorteile in großem Maßstab finden Sie unter [Best Practices für fortgeschrittene Journey in Journey Optimizer](https://experienceleague.adobe.com/de/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}.

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite wird erläutert, wie Tags in Adobe Journey Optimizer hinzugefügt, gefiltert und verwaltet werden und warum Tag-Kategorien eine bessere Alternative zu komplexen Benennungskonventionen für die Organisation großer Journey-Listen sind.

**intents:**
* Hinzufügen von Tags zu einer Journey über das Feld Journey-Eigenschaften-Tags .
* Filtern Sie die Journey-Liste nach einem oder mehreren Tags, um bestimmte Journey schnell zu finden
* Bearbeiten von Tags in vorhandenen Journey mit beliebigem Status (Live, Entwurf usw.) über weitere Aktionen
* Erstellen und Organisieren von Tag-Kategorien als Administrator, um konsistente Metadaten zu erzwingen
* Ersetzen einer komplexen Journey-Namenskonvention durch einen strukturierten Tag-basierten Ansatz

**Glossar:**
* **Tags**: Beschriftungen, die an Journey angehängt werden, um sie zu klassifizieren und zu filtern; ignoriert die Groß-/Kleinschreibung und wird beibehalten, wenn eine Journey dupliziert oder versioniert wird *(produktspezifisch)*
* **Tag-Kategorien**: Gruppierungen verwandter Tag-Werte, die von Admins unter Administration > Tags erstellt wurden und eine strukturierte Metadaten-Klassifizierung ermöglichen *(produktspezifisch)*
* **Nicht kategorisiert**: Die integrierte Standardkategorie, der direkt in Journey erstellte Tags automatisch zugewiesen werden *(produktspezifisch)*

**Leitplanken:**
* Tags unterscheiden nicht zwischen Groß- und Kleinschreibung
* In Journey definierte Tags werden automatisch der integrierten Kategorie „Nicht kategorisiert“ hinzugefügt, es sei denn, ein Administrator weist sie einer benannten Kategorie zu
* Nur Administratoren können über das Menü Administration > Tags Tags Tags löschen und Tag-Kategorien verwalten
* Tags bleiben erhalten, wenn eine Journey dupliziert oder eine neue Version erstellt wird

**Terminologie:**
* Kanonischer Name: Tags — Akronym: none — Varianten: Journey Tags, administrative Tags
* Kanonischer Name: Tag categories — Akronym: none — Varianten: Tag-Gruppen
* Verwechseln Sie nicht: „Tags“ (Journey-Klassifizierungskennzeichnungen) ≠ „Benennungskonventionen“ (Metadaten, die direkt in Journey-Namen kodiert sind)

**FAQ:**
* **F: Wie füge ich einem Journey ein Tag hinzu?** — Geben Sie in die Journey-Eigenschaften den Tag-Namen in das Feld Tags ein und wählen Sie ihn aus der Liste aus, oder klicken Sie auf Erstellen , um ein neues Tag hinzuzufügen.
* **F: Kann ich einer Live-Journey Tags hinzufügen?** — Ja. Klicken Sie auf das Symbol Mehr Aktionen neben der Journey in der Liste und wählen Sie Tags bearbeiten aus, um unabhängig vom Status Tags auf einer Journey hinzuzufügen oder zu entfernen.
* **F: Wird bei Tags zwischen Groß- und Kleinschreibung unterschieden?** — Nein. Bei Tags wird nicht zwischen Groß- und Kleinschreibung unterschieden.
* **F: Was passiert mit Tags, wenn ich eine Journey dupliziere oder eine neue Version erstelle?** — Tags werden in der Duplikat- oder neuen Version beibehalten.
* **F: Wer kann Tags löschen oder Tag-Kategorien erstellen?** — Nur Administratoren können Tags löschen und Tag-Kategorien über das Menü Administration > Tags verwalten.
* **F: Warum sollten Tag-Kategorien anstelle von Benennungskonventionen verwendet werden?** - Tag-Kategorien erzwingen Konsistenz durch eine kontrollierte Liste, ermöglichen sofortige mehrdimensionale Filterung, halten Journey-Namen kurz und Meilenstein-fokussiert und skalieren einfach durch das Hinzufügen neuer Kategorien ohne das Umschreiben von Benennungsregeln.

+++
