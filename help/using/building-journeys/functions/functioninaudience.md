---
product: journey optimizer
title: inAudience-Funktion
description: Erfahren Sie mehr über die Funktion „inAudience“ von Adobe Experience Platform
feature: Journeys
role: Developer
level: Experienced
keywords: inAudience, Funktion, Ausdruck, Journey, Zielgruppe, Segmentierung
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DU8HtduB2-GmakiaHBMFU1vzBBPoVTNvrOCPWQrr5SU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1279
ht-degree: 47%

---

# inAudience-Funktion {#inAudience}

Die Funktion `inAudience` ist eine Adobe Experience Platform-Funktion, mit der Sie überprüfen können, ob ein Kontakt in Ihrer Journey zu einer bestimmten Zielgruppe gehört. Mit dieser leistungsstarken Funktion können Sie personalisierte Journey-Pfade basierend auf der Zielgruppenzugehörigkeit erstellen und ermöglichen dadurch anspruchsvolle Segmentierung und anspruchsvolles Targeting in Ihren Kundenerlebnissen.

Verwenden Sie die Funktion `inAudience`, wenn Sie Folgendes tun müssen:

* Journey-Pfade basierend auf der Zielgruppenzugehörigkeit verzweigen. [Weitere Informationen](../conditions.md#using-a-segment)
* Bedingte Logik anwenden, die davon abhängt, ob ein Profil zu einem bestimmten Segment gehört
* Bestimmte Zielgruppen von Kundinnen und Kunden mit personalisierten Erlebnissen ansprechen
* Echtzeit-Zielgruppenbeteiligung unter Journey-Bedingungen auswerten
* Mehrere Zielgruppenprüfungen kombinieren, um komplexe Zielgruppenbestimmungsregeln zu erstellen

Die Funktion wertet die Zielgruppenzugehörigkeit in Echtzeit aus und gibt einen booleschen Wert zurück, wodurch sie sich ideal für Entscheidungsknoten und bedingte Ausdrücke eignet. Zielgruppen werden in [Adobe Experience Platform](https://platform.adobe.com/audience/overview){target="_blank"} definiert und verwaltet (weitere Informationen zum [Arbeiten mit Zielgruppen](../../audience/about-audiences.md) in Journey Optimizer). Der Ausdruckseditor bietet automatische Vervollständigungsvorschläge, um Ihnen eine genaue Referenzierung zu erleichtern.

**Zielgruppenstatus:**

Zielgruppen können zwei Beteiligungsstatus aufweisen:

* **Realisiert**: Der Kontakt qualifiziert sich für die Zielgruppendefinition und ist ein aktives Mitglied
* **Ausgestiegen**: Der Kontakt hat die Zielgruppe verlassen und ist nicht mehr qualifiziert

Nur Kontakte mit dem Status **Realisiert** werden als aktive Zielgruppenmitglieder betrachtet. Wenn die Funktion `true` zurückgibt, bestätigt sie, dass der Kontakt den Status „Realisiert“ hat. Wenn sie `false` zurückgibt, zeigt dies den Status „Ausgestiegen“ an. Weitere Informationen zur Zielgruppenauswertung finden Sie in der [Dokumentation zum Segmentierungs-Service](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/tutorials/evaluate-a-segment#interpret-segment-results){target="_blank"}.

+++Syntax

`inAudience(<parameter>)`

+++

+++Parameter

| Parameter | Beschreibung | Typ |
|--- |--- |--- |
| Zielgruppe | Der Zielgruppenname | `<string>` |

**Wichtige Einschränkungen:**

* Der Zielgruppenname muss eine Zeichenfolgenkonstante sein
* Er kann kein Feldverweis oder Ausdruck sein
* Sie können bis zu 100 Zielgruppen in einer einzelnen Journey abrufen

+++

+++Signatur und zurückgegebener Typ

`inAudience(<string>)`

Gibt einen booleschen Wert zurück:
* `true`: Der Kontakt ist Mitglied der Zielgruppe (Status „Realisiert“)

* `false`: Der Kontakt ist kein Mitglied der Zielgruppe (Status „Ausgestiegen“)

+++

+++Beispiele

`inAudience("men over 50")`

Gibt **wahr** zurück, wenn der Kontakt innerhalb der Journey-Instanz Teil der Adobe Experience Platform-Zielgruppe „men over 50“ (Männer über 50) ist. Andernfalls wird **falsch** zurückgegeben.

**Praktische Anwendungsfälle:**

```
// Simple audience check in a condition
inAudience("Premium Customers") == true

// Multiple audience evaluation
inAudience("High Value Customers") == true AND inAudience("Active Last 30 Days") == true

// Negation check
inAudience("Unsubscribed") == false
```

+++

## Leitlinien und Einschränkungen {#guardrails}

Beachten Sie bei Verwendung der Funktion `inAudience` in Ihren Journeys die folgenden Leitlinien und Einschränkungen:

**Beschränkung für Zielgruppenabrufe:**
* Sie können bis zu 100 Zielgruppen in einer einzelnen Journey abrufen
* Der Ausdruckseditor stellt eine automatisch vervollständigte Liste verfügbarer Zielgruppen bereit, um Ihnen deren korrekte Referenzierung zu erleichtern

**Parametereinschränkungen:**
* Der Zielgruppenname muss eine Zeichenfolgenkonstante sein
* Feldverweise und Ausdrücke werden nicht als Parameter unterstützt

**Änderungen des Zielgruppennamens:**
* Wenn Sie den Namen einer bestehenden Zielgruppe in Adobe Experience Platform ändern, werden die Verweise auf diese Zielgruppe in Ihren Journey-Ausdrücken nicht automatisch aktualisiert.
* Wenn Ihr Bedingungsknoten `inAudience('oldAudienceName')` verwendet, müssen Sie den Ausdruck manuell bearbeiten, damit der neue Name verwendet wird.
* Wenn der Zielgruppenname nicht aktualisiert wird, funktioniert die Journey-Bedingung nicht mehr, was zu falschem Journey-Verhalten führen kann

**Überlegungen zur Zusammenführungsrichtlinie:**
* Beim Verwenden mehrerer Zielgruppen mit der Funktion `inAudience` können Inkonsistenzen mit Zusammenführungsrichtlinien zu Fehlern oder Warnhinweisen führen
* Weitere Informationen zum Verhalten von Zusammenführungsrichtlinien finden Sie unter [Journey-Eigenschaften](../journey-properties.md).

**Ausbreitungszeitpunkt:** {#propagation-timing}

Bei Verwendung von `inAudience()` in einem Bedingungsknoten variiert der Zeitpunkt der Segmentzugehörigkeitsevaluierung je nachdem, wo die Bedingung auf der Journey erscheint:

* **Auf einer Zielgruppen-Journey lesen vor einer Warteaktivität:** Journey Optimizer liest aus der Batch-Projektion des Profils. Die Daten in dieser Projektion werden innerhalb von **2 Stunden** der Aufnahme aktualisiert. Bei Zielgruppen, die auf tägliche oder zeitbasierte Bedingungen angewiesen sind, können zusätzliche Verzögerungen auftreten. Fügen Sie eine [Warteaktivität](../wait-activity.md) am Anfang der Journey hinzu oder lassen Sie eine Pufferzeit zu, um sicherzustellen, dass die neueste Segmentzugehörigkeit widergespiegelt wird.
* **Auf einer Journey mit einem unitären Ereignis oder nach einer Warteaktivität wird** Segmentzugehörigkeit aus der Streaming-(unitären)-Projektion gelesen. Die Daten sind normalerweise innerhalb von **15 Minuten** verfügbar. Weitere Informationen finden Sie in der Dokumentation zur Streaming-Aufnahme in [Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/streaming/overview){target="_blank"}.

## Verwandte Themen

Weitere Informationen zur Verwendung von Zielgruppen in Adobe Journey Optimizer:

* **[Informationen zu Zielgruppen](../../audience/about-audiences.md)**: Erfahren Sie, wie Zielgruppen in Adobe Experience Platform und Journey Optimizer funktionieren, einschließlich ihrer Erstellung und Verwaltung
* **[Aktivität „Zielgruppe lesen“](../read-audience.md)**: Verwenden Sie Zielgruppen, um den Journey-Eintritt auszulösen und alle Mitglieder der Zielgruppe zum Eintritt in eine Journey zu bewegen
* **[Zielgruppenqualifizierungsereignisse](../audience-qualification-events.md)**: Überwachen Sie Zielgruppeneintritte und -austritte von Profilen, um Journey-Aktionen in Echtzeit auszulösen
* **[Verwenden von Zielgruppen in Bedingungen](../conditions.md#using-a-segment)** - Erstellen bedingter Journey-Pfade basierend auf der Zielgruppenzugehörigkeit mithilfe der Aktivität „Optimieren“
* **[Journey-Eigenschaften – Zusammenführungsrichtlinien](../journey-properties.md)**: Erfahren Sie, wie Zusammenführungsrichtlinien funktionieren, wenn mehrere Zielgruppen mit der Funktion „inAudience“ verwendet werden

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite wird die `inAudience` dokumentiert, die in Echtzeit prüft, ob ein Journey-Profil zu einer benannten Adobe Experience Platform-Zielgruppe gehört, und einen booleschen Wert zurückgibt, der in Journey-Bedingungen verwendet wird.

**intents:**
* Verzweigen eines Journey-Pfads basierend darauf, ob ein Profil Mitglied einer bestimmten Zielgruppe ist, mithilfe von `inAudience`
* Kombinieren mehrerer `inAudience` mit UND/ODER-Logik, um komplexe Zielgruppenbestimmungsbedingungen zu erstellen
* Vergewissern Sie sich mithilfe einer Negationsprüfung (`inAudience("...") == false`), dass ein Profil keine bestimmte Zielgruppe betreten hat
* Verstehen Sie die Unterschiede beim Propagierungs-Timing zwischen den Journey der Zielgruppe lesen und den Journey der unitären Ereignisse
* Identifizieren und Beheben von fehlerhaften Zielgruppenverweisen, die durch Zielgruppennamen in Adobe Experience Platform verursacht wurden

**Glossar:**
* **Realisiert**: Status der Zielgruppenbeteiligung, der angibt, welche Person sich derzeit für die Zielgruppendefinition qualifiziert und ein aktives Mitglied ist *(produktspezifisch)*
* **Ausgetreten**: Der Zielgruppen-Teilnahmestatus gibt an, dass die Person die Zielgruppe verlassen hat und nicht mehr *ist (produktspezifisch)*
* **Zusammenführungsrichtlinie**: Eine Regel in Adobe Experience Platform, die bestimmt, wie Profildaten aus mehreren Datensätzen kombiniert werden, wenn die Zielgruppenzugehörigkeit bewertet wird *(produktspezifisch)*
* **Batch-Projektion**: Der Profildatenspeicher wurde nach einem Zeitplan aktualisiert (innerhalb von 2 Stunden nach der Aufnahme), der von „Zielgruppen-Journey lesen“ verwendet wird *(produktspezifisch)*
* **Streaming-Projektion**: Der Echtzeit-Profildatenspeicher (in der Regel innerhalb von 15 Minuten verfügbar), der in unitären Ereignis-Journey und After-Wait-Aktivitäten verwendet wird *(produktspezifisch)*

**Leitplanken:**
* Auf einer einzigen Journey können bis zu 100 Zielgruppen abgerufen werden
* Der Parameter für den Zielgruppennamen muss eine Zeichenfolgenkonstante sein. Feldverweise und dynamische Ausdrücke werden nicht unterstützt
* Beim Umbenennen einer Zielgruppe in Adobe Experience Platform werden `inAudience` Verweise in Journey-Ausdrücken nicht automatisch aktualisiert. Es sind manuelle Aktualisierungen erforderlich
* Inkonsistente Zusammenführungsrichtlinien für mehrere Zielgruppen, die auf derselben Journey verwendet werden, können zu Fehlern oder Warnhinweisen führen

**Terminologie:**
* Kanonischer Name: inAudience — Akronym: none — Varianten: inSegment (veralteter Name)
* Synonyme: „inAudience“ = „Funktion zur Überprüfung der Zielgruppenzugehörigkeit“
* Verwechseln Sie nicht: „Realisiert“ (aktives Mitglied) ≠ „Ausgetreten“ (kein Mitglied mehr)
* Verwechseln Sie nicht: „inAudience“ (aktuelle Funktion) ≠ „inSegment“ (veraltete Funktion)

**FAQ:**
* **F: Was gibt `inAudience` zurück, wenn ein Profil die Zielgruppe verlassen hat?** — Gibt `false` zurück. Nur Profile mit dem Status „Realisiert“ werden als aktive Mitglieder betrachtet und geben `true` zurück.
* **F: Wie viele Zielgruppen kann ich auf einer Journey einchecken?** — Auf einer Journey können bis zu 100 Zielgruppen abgerufen werden.
* **F: Was passiert, wenn ich eine Zielgruppe in Adobe Experience Platform umbenenne, nachdem ich sie auf einer Journey verwendet habe?** — Der Journey-Ausdruck wird nicht automatisch aktualisiert. Sie müssen den `inAudience`-Aufruf manuell bearbeiten, um den neuen Zielgruppennamen zu verwenden. Andernfalls wird die Bedingung beschädigt.
* **F: Wie schnell ist die Zielgruppenzugehörigkeit nach einer Profilaktualisierung auf einer „Zielgruppe lesen“-Journey verfügbar?** — Auf einer Zielgruppen-Journey vor einer Warteaktivität lesen werden Daten aus der Batch-Projektion innerhalb von 2 Stunden nach der Aufnahme aktualisiert.
* **F: Kann ich ein Profilattribut als Parameter für den Zielgruppennamen übergeben?** — Nein, der Zielgruppenname muss eine Zeichenfolgenkonstante sein. Feldverweise und -ausdrücke werden nicht unterstützt.

+++
