---
solution: Journey Optimizer
product: journey optimizer
title: Journeys oder Kampagnen – Auswählen des richtigen Ansatzes
description: Vergleichen Sie Journey, Aktionskampagnen und API-ausgelöste Kampagnen, um den richtigen Ansatz für Ihre Marketing-Anforderungen in Adobe Journey Optimizer zu wählen.
feature: Journeys, Campaigns, Get Started, Overview
topic: Content Management
role: User
level: Beginner
hide: true
keywords: Journey, Kampagne, Vergleich, Auswählen, Entscheidung, Workflow, Echtzeit, Batch, Orchestrierung, mehrstufig, geplant, API-ausgelöst, ereignisgesteuert
source-git-commit: ab31811861ccaab22fc787ce3c687204637fbd46
workflow-type: tm+mt
source-wordcount: '1965'
ht-degree: 12%

---


# Journey vs. Kampagnen: Wählen Sie den richtigen Ansatz {#journeys-vs-campaigns}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Vergleichen Sie Journey mit Aktionen und API-ausgelösten Kampagnen, damit Sie für jeden Marketing-Anwendungsfall in Adobe Journey Optimizer den richtigen Ansatz wählen können. Informationen zu orchestrierten Kampagnen finden Sie [Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md).

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] bietet zwei Möglichkeiten, Ihre Kunden zu erreichen und zu kontaktieren: **Journey** und **Kampagnen**. Journey sind für eine mehrstufige Orchestrierung in Echtzeit konzipiert, die durch das Kundenverhalten gesteuert wird, während Kampagnen besser für einmalige oder geplante Sendungen an eine definierte Zielgruppe geeignet sind - oder für die Aktivierung eingehender Kanäle am Edge zur Personalisierung mit geringer Latenz.

>[!NOTE]
>
>**Orchestrierte Kampagnen** weisen unterschiedliche architektonische Merkmale auf (Hub-seitige Batch-Ausführung, relationale Daten mit mehreren Entitäten), die eine dedizierte Anleitung erfordern. Sie sind im folgenden Vergleich nicht enthalten, um eine übermäßige Vereinfachung zu vermeiden. [Erfahren Sie mehr über orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)

## Welchen Ansatz sollten Sie verwenden? {#decision-guide}

Die Antwort läuft gewöhnlich auf eine Frage hinaus *„Was muss passieren und für wen?*

Wenn Sie **jeden Kunden in seinem eigenen Tempo bewegen müssen** - Nachrichten erhalten, die darauf basieren, was er tut, warten und dann auf seine nächste Aktion reagieren - verwenden Sie eine **Journey**. Journey behalten den Überblick darüber, wo jedes Profil ist und was sie getan haben, was sie ideal für mehrstufige Erlebnisse wie Onboarding-Sequenzen, Warenkorbabbrüche oder Treueprogramme macht.

Wenn Sie **eine Nachricht an eine Gruppe von Personen nach einem Zeitplan senden** - einen Newsletter, eine Produktankündigung, eine saisonale Promotion - verwenden Sie eine **Aktionskampagne**. Alle Personen in der Zielgruppe erhalten die Nachricht gleichzeitig, ohne dass eine Logik pro Profil erforderlich ist. Aktionskampagnen unterstützen auch die Aktivierung eingehender Kanäle (In-App-, Web-, Inhaltskarten-, Code-basiert) für Edge-Personalisierung mit geringer Latenz.

Wenn ein **externes System sofort eine Nachricht senden muss** — eine Bestellbestätigung von Ihrer E-Commerce-Plattform, eine Versandwarnung von Ihrem Logistiksystem, ein Zurücksetzen des Passworts von Ihrer App — verwenden Sie eine **API-ausgelöste Kampagne** für eine einzige On-Demand-Nachricht oder eine **Unitäres Ereignis-Journey**, wenn dieser Trigger einen mehrstufigen Trigger starten muss.

Wenn Sie einen **komplexen Batch-Workflow mit erweiterter Segmentierung, Daten aus mehreren Entitäten oder exakte Anzahl der Vorabsendungen** benötigen, finden Sie weitere Informationen unter [Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md).

>[!TIP]
>
>**Sie sind sich nicht sicher, wo Sie anfangen sollen?** Die meisten Teams verwenden Journey für verhaltensbezogene, ereignisgesteuerte Erlebnisse und Aktionskampagnen für geplante Kommunikationen. Diese beiden decken den Großteil der Anwendungsfälle ab.

## Vergleich {#quick-overview}

| Ansatz | Geeignet für | Ausführungsstil |
|----------|----------|-----------------|
| **Journeys** | Mehrstufige Echtzeit-Kundenerlebnisse mit bedingter Logik | 1:1 Orchestrierung - Jedes Profil in seinem eigenen Tempo |
| **Aktionskampagnen** | Geplante oder wiederkehrende Aktivierungen von Audiences | Batch-Ausführung - Zielgruppe zum Versandzeitpunkt gemeinsam verarbeitet |
| **API-ausgelöste Kampagnen** | Ereignisgesteuerte oder Transaktionsnachrichten von externen Systemen | Ausführung auf Anfrage - ausgelöst durch API-Aufruf mit Payload |

## Funktionsweise der einzelnen Ansätze {#key-distinctions}

### Journey: 1:1 Echtzeit-Orchestrierung

Eine Journey ist eine Arbeitsfläche, auf der jedes Profil seinen eigenen Weg in seinem eigenen Tempo geht. AJO verfolgt, wo sich jede Person im Fluss befindet, und reagiert in Echtzeit auf ihr Verhalten - ob es sich um eine Aktion handelt, eine Zeit der Inaktivität oder eine Profiländerung.

Zu den wichtigsten Funktionen gehören Warteaktivitäten, die ein personalisiertes Timing zwischen Schritten erstellen, bedingte Verzweigungen, die Profile an verschiedene Pfade weiterleiten, Frequenzlimitierung zur Steuerung, wie oft ein Kunde Nachrichten erhält, und Testmodus zur Validierung der Logik vor der Live-Schaltung. Journey können Profile auch in prozentuale Gruppen für A/B-Experimente über mehrere Pfade hinweg aufteilen.

Eine Journey zum Warenkorbabbruch veranschaulicht den Unterschied deutlich:

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Jede Kundin und jeder Kunde erfährt einen anderen Zeitplan, basierend auf dem, was sie tatsächlich tun. [Erfahren Sie mehr über Journey](../building-journeys/journey.md)

### Kampagnen: Batch- oder ausgelöster Versand

Eine Kampagne führt eine einzelne Aktion aus - entweder für alle Personen in einer Zielgruppe gleichzeitig oder bei Bedarf, wenn sie von einem externen System aufgerufen wird. Es gibt keine Arbeitsfläche und keinen Status pro Profil: Alle Profile werden identisch verarbeitet.

**Aktionskampagnen** Versand an eine geplante Zielgruppe (einmal oder wiederkehrend) und auch Unterstützung für einen eingehenden Versand mit mehreren Oberflächen - bis zu 10 eingehende Kanalaktionen pro Kampagne, mit Zielgruppenbestimmungsregeln zum Erstellen von Nachrichtenvarianten basierend auf der Zielgruppenzugehörigkeit oder Profilattributen.

**API-ausgelöste Kampagnen** werden sofort ausgelöst, wenn ein externes System die API aufruft, wobei die Nachrichtenpersonalisierung durch die Payload-Daten gesteuert wird, die in diesem Aufruf gesendet werden.

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

[Weitere Informationen zu Kampagnen](../campaigns/get-started-with-campaigns.md)

## Beispiele für Anwendungsfälle {#use-cases}

| Anwendungsfall | Empfohlener Ansatz | Warum |
|----------|---------------------|-----|
| Neue Kundschaft mit mehrstufigem Onboarding begrüßen | Journeys | Eintritt in Echtzeit, mehrere Touchpoints, bedingte Pfade |
| Warenkorbabbruch mit Erinnerungssequenz | Journeys | Echtzeit-Trigger, Wartezeiten, bedingte Nachverfolgung |
| Erneutes Ansprechen inaktiver Benutzender auf Grundlage des Verhaltens | Journeys | Ausgelöst durch Zielgruppenqualifizierung, personalisierter Pfad |
| Flash-Verkauf ausgelöst durch ein Geschäftsereignis | Journeys (Geschäftsereignis) | Echtzeit-Trigger mit Auswirkung auf mehrere Kundinnen und Kunden |
| Monatlicher Newsletter für Abonnenten | Aktionskampagnen | Geplante Nachricht an Zielgruppe |
| Werbeankündigung an alle Kundinnen und Kunden | Aktionskampagnen | Einmalige Nachricht, sofortiger Versand |
| Bestellbestätigung oder Versandwarnung | Durch API ausgelöste Kampagnen | Externer System-Trigger, sofortiger einmaliger Versand |
| API-ausgelöster mehrstufiger Fluss | Journey (Unitäres Ereignis) | Externes System sendet Ereignis über API; Journey koordiniert die Folgeschritte |
| Komplexer Batch-Workflow mit Daten aus mehreren Entitäten | Orchestrierte Kampagnen | Siehe [Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md) |

## Funktionsverfügbarkeit {#feature-availability}

### Kanäle

Alle drei Ansätze unterstützen den vollständigen Satz der ausgehenden AJO-Kanäle: E-Mail, Push, SMS, LINE und WhatsApp. Die nachstehende Tabelle zeigt die Unterschiede für eingehende und digitale Kanäle.

| Kanal | Journeys | Aktionskampagnen | Durch API ausgelöste Kampagnen |
|---------|:--------:|:----------------:|:-----------------------:|
| In-App | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ❌ |
| Code-basiert | ✅ | ✅ | ❌ |
| Inhaltskarten | ✅ | ✅ | ❌ |
| Direkt-Mail | ✅ | ✅ | ❌ |

>[!NOTE]
>
>Informationen zur Verfügbarkeit von Kanälen für orchestrierte Kampagnen finden Sie unter [Kanäle in Journey und Kampagnen](../channels/gs-channels.md#channels).

### Erweiterte Funktionen

| Funktion | Journeys | Aktionskampagnen | Durch API ausgelöste Kampagnen |
|-----------|:--------:|:----------------:|:-----------------------:|
| Mehrstufige Workflows | ✅ | ❌ | ❌ |
| Echtzeit-Trigger | ✅ | ❌ | ✅ |
| Warteaktivitäten | ✅ | ❌ | ❌ |
| Bedingte Verzweigung | ✅ | ❌ | ❌ |
| Geplante Ausführung | ✅ | ✅ | ✅ |
| API-Auslösung | ✅ (nur unitäres Ereignis) | ❌ | ✅ |
| Versandzeitoptimierung | ✅ | ❌ | ❌ |
| A/B-Tests | ✅ | ✅ | ❌ |
| Genehmigungs-Workflows | ✅ | ✅ | ✅ |
| Daten mit mehreren Entitäten | ❌ | ❌ | ❌ |
| Genaue Anzahl vor dem Versand | ❌ | ❌ | ❌ |

>[!NOTE]
>
>Details zu den Funktionen koordinierter Kampagnen - einschließlich Inhaltsexperimenten, Batch-API-Triggern und Segmentierung mehrerer Entitäten - finden Sie unter [Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md).

## Häufige Fragen {#common-questions}

+++ Kann ich Journeys und Kampagnen in meiner Marketing-Strategie kombinieren?

Ja. Viele Unternehmen verwenden alle Ansätze für verschiedene Szenarien:

* **Journey** für verhaltensbezogene Interaktion in Echtzeit
* **Aktionskampagnen** für geplante Nachrichten oder eingehende Aktivierungen
* **API-ausgelöste**) für Transaktionsnachrichten
* **Orchestrierte Kampagnen** für komplexe, datenintensive Batch-Kampagnen - siehe [Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)

Verwenden Sie für jeden Anwendungsfall das richtige Tool, anstatt für alles einen Ansatz zu erzwingen.

+++

+++ Kann ich eine Kampagne in eine Journey konvertieren oder umgekehrt?

Nein, Sie müssen das Erlebnis im entsprechenden Format neu erstellen. Sie können jedoch Inhalte, Zielgruppen und Logikkonzepte wiederverwenden.

+++

+++ Welcher Ansatz lässt sich am einfachsten erstellen?

Aktionskampagnen sind in der Regel die einfachsten (ein einzelner Touchpoint für eine Zielgruppe), gefolgt von API-ausgelösten Kampagnen und dann von Journey-Kampagnen, die aufgrund der Mehrstufenlogik mehr Design-Arbeit erfordern.

+++

+++ Welcher Ansatz ist besser für große Zielgruppen geeignet?

Alle drei können gut skaliert werden. Die richtige Wahl hängt von Ihrem Muster ab:

* **Journey-** lesen **und** sind für große Batch-Zielgruppen optimiert.
* **Unitäre (ereignisbasierte) Journey** verarbeiten Profile einzeln, wenn Ereignisse auftreten. Die Skalierung hängt daher vom Ereignisvolumen und -durchsatz ab.

Informationen zur komplexen Segmentierung mit großen Datensätzen und Daten mit mehreren Entitäten finden Sie unter [Orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md).

+++

+++ Kann ich dieselbe Zielgruppe für Journeys und Kampagnen verwenden?

Ja. In [!DNL Adobe Experience Platform] erstellte Audiences können in Journey-, Aktions- und orchestrierten Kampagnen verwendet werden. API-ausgelöste Kampagnen sind Payload-gesteuert und verwenden vordefinierte Zielgruppen nicht auf die gleiche Weise.

+++

## Nächste Schritte {#next-steps}

Bereit, mit dem Erstellen zu beginnen? Informieren Sie sich in der ausführlichen Dokumentation zu Ihrem gewählten Ansatz:

* **[Erste Schritte mit Journey](../building-journeys/journey.md)** - Journey-Typen, Designer und Workflow
* **[Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md)** - Aktion und API-ausgelöste Kampagnen
* **[Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)** - Batch-Arbeitsflächen-Workflows mit Daten aus mehreren Entitäten (separate Anleitung)

>[!MORELIKETHIS]
>
>* [Vergleich der Journey-Typen](../building-journeys/journey.md#journey-types-comparison)
>* [Vergleich der Kampagnentypen](../campaigns/get-started-with-campaigns.md#campaign-types)
>* [Häufig gestellte Fragen zu Journeys](../building-journeys/journey-faq.md)
>* [Häufig gestellte Fragen zu orchestrierten Kampagnen](../orchestrated/orchestrated-campaigns-faq.md)

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Wählen Sie zwischen Journey, Aktionskampagnen und API-ausgelösten Kampagnen, je nachdem, ob Sie eine Echtzeit-1:1Orchestrierung, eine geplante oder eingehende Batch-Bereitstellung oder eine API-ausgelöste Ausführung auf Anfrage benötigen.

**intents:**
* Machen Sie sich mit den wichtigsten Unterschieden zwischen Journeys, Aktionskampagnen und API-ausgelösten Kampagnen vertraut
* Wählen Sie mithilfe des Entscheidungshandbuchs und Vergleichstabellen den richtigen Ansatz für einen bestimmten Marketing-Anwendungsfall aus
* Verstehen, wann Aktionskampagnen die Aktivierung eingehender Kanäle und ausgehende Sendungen unterstützen
* Wissen, wann an orchestrierte Kampagnen eskaliert werden soll (Ad-hoc-Komposition, Federated Data, Multi-Entity)
* Effektive Kombination mehrerer Ansätze in einer Marketing-Strategie

**Glossar:**
* **Journey**: Ein mehrstufiger Echtzeit-Orchestrierungsfluss, bei dem jedes Profil in seinem eigenen Tempo basierend auf Verhalten und Ereignissen fortschreitet. *(produktspezifisch)*
* **Aktionskampagne** Eine Kampagne, die geplante oder wiederkehrende Aktivierungen für Zielgruppen bereitstellt - Aktivierungen ausgehender Sendungen oder eingehender Kanäle an den Edge zur Personalisierung mit geringer Latenz. *(produktspezifisch)*
* **API-ausgelöste Kampagne** Eine Kampagne, die von einem externen System über einen API-Aufruf initiiert wird und eine einzige On-Demand-Nachricht mit Payload-gesteuerter Personalisierung liefert. *(produktspezifisch)*
* **Orchestrierte Kampagne**: Eine Hub-seitige Batch-Kampagne, die relationale Daten mit mehreren Entitäten, eine Ad-hoc-Zielgruppenkomposition und verknüpfte Datenquellen unterstützt und nicht von den Vergleichstabellen auf dieser Seite abgedeckt wird. *(produktspezifisch)*
* **Unitäres Ereignis-Journey**: Ein Journey, der durch eine Einzelprofilaktion in Echtzeit ausgelöst wird. Wird verwendet, wenn nach einem API-gesendeten Ereignis eine mehrstufige Orchestrierung erforderlich ist. *(produktspezifisch)*
* **Aktivierung eingehender Kanäle**: Bereitstellen personalisierter Erlebnisse am Edge (Code-basiertes Erlebnis, In-App, Inhaltskarte, Web) für Rendering mit geringer Latenz, unterstützt in Aktionskampagnen. *(produktspezifisch)*

**Leitplanken:**
* Bis zu 10 eingehende Kanalaktionen pro Aktionskampagne (feste Grenze) - gilt nur für eingehende Kanäle: Code-basiertes Erlebnis, In-App, Inhaltskarte, Web
* Orchestrierte Kampagnen werden aus den Vergleichstabellen auf dieser Seite ausgeschlossen, um eine übermäßige Vereinfachung zu vermeiden. Weitere Informationen zur Architektur finden Sie in der Dokumentation zu dedizierten orchestrierten Kampagnen .

**Terminologie:**
* Kanonischer Name: Aktionskampagnen — Varianten: „Geplante Kampagnen“, „Broadcast-Kampagnen“
* Kanonischer Name: API-ausgelöste Kampagnen - Varianten: „Transaktionskampagnen“, „ereignisgesteuerte Kampagnen“
* Verwechseln Sie nicht: „Aktionskampagnen“ (geplanter/eingehender Versand an Zielgruppen) ≠ „API-ausgelöste Kampagnen“ (On-Demand, Payload-gesteuert, keine vordefinierte Zielgruppe) ≠ „Orchestrierte Kampagnen“ (Hub-seitiger Batch mit relationalen Daten)
* Verwechseln Sie nicht: „Unitäres Ereignis-Journey&quot; (ausgelöst durch die Echtzeit-Aktion eines Profils) ≠ „Geschäftsereignis-Journey&quot; (ausgelöst durch ein Nicht-Profilereignis, das mehrere Personen über einen internen Schritt „Zielgruppe lesen“ betrifft)
* Synonyme: „Aktivierung des eingehenden Kanals“ = „Aktion des eingehenden Kanals“ (wird auf dieser Seite austauschbar für Edge-bereitgestellte Erlebnisse in Aktionskampagnen verwendet)

**FAQ:**
* **F: Wann sollte ich eine Journey anstelle einer Aktionskampagne verwenden?** - Verwenden Sie Journey-Kampagnen, wenn Kunden mit einer bedingten Echtzeitlogik über mehrere Touchpoints hinweg in ihrem eigenen Tempo agieren müssen; verwenden Sie Aktionskampagnen für den geplanten oder eingehenden Versand an eine vordefinierte Zielgruppe.
* **F: Können Aktionskampagnen an eingehende Kanäle senden?** — Ja. Aktionskampagnen unterstützen die Aktivierung eingehender Kanäle (Code-basiertes Erlebnis, In-App, Inhaltskarte, Web) zum Edge für Personalisierung mit niedriger Latenz, mit bis zu 10 eingehenden Aktionen pro Kampagne und Zielgruppenbestimmungsregeln für Nachrichtenvarianten.
* **F: Was unterscheidet orchestrierte Kampagnen von Aktionskampagnen?** - Orchestrierte Kampagnen führen eine Hub-seitige Batch-Ausführung mit relationalen Daten mehrerer Entitäten, exakter Anzahl vor dem Versand, Ad-hoc-Zielgruppenkomposition und Federated Data-Unterstützung durch. Aktionskampagnen sind statuslose Sendungen mit einer Ausführung an Experience Platform-Zielgruppen.
* **F: Wann sollte ich eine API-ausgelöste Kampagne im Vergleich zu einer unitären Ereignis-Journey verwenden?** - Verwenden Sie eine API-ausgelöste Kampagne, wenn ein externes System eine einzelne Nachricht sofort mit Payload-Daten in Trigger bringen muss. Verwenden Sie eine unitäre Ereignis-Journey, wenn nach dem API-Sendeereignis eine mehrstufige Orchestrierung erforderlich ist.
* **F: Kann ich Journey und Kampagnen in derselben Marketing-Strategie kombinieren?** — Ja. Verwenden Sie Journey für verhaltensbezogene Echtzeit-Interaktionen, Aktionskampagnen für geplante Sendungen oder eingehende Aktivierungen, API-ausgelöste Kampagnen für Transaktionsnachrichten und orchestrierte Kampagnen für komplexe Batch-Workflows.

+++
<!-- ai-accordion-version: 1 | source-hash: 873097f5 -->
