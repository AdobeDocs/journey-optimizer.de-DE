---
solution: Journey Optimizer
product: journey optimizer
title: Journeys oder Kampagnen – Auswählen des richtigen Ansatzes
description: Vergleichen Sie Journey, Aktionskampagnen, API-ausgelöste Kampagnen und orchestrierte Kampagnen, um den richtigen Ansatz für Ihre Marketing-Anforderungen in Adobe Journey Optimizer zu wählen.
feature: Journeys, Campaigns, Get Started, Overview
topic: Content Management
role: User
level: Beginner
keywords: Journey, Kampagne, orchestriert, Vergleich, Auswählen, Entscheidung, Workflow, Echtzeit, Batch, Orchestrierung, mehrstufig, geplant, API-ausgelöst, ereignisgesteuert
hide: true
hidefromtoc: true
exl-id: 8b4d010e-4278-49fd-a7d3-dcc706829577
source-git-commit: fc2dc5924f4998d1285dee9c19a0d7e71a1e5722
workflow-type: tm+mt
source-wordcount: '1593'
ht-degree: 66%

---

# Journeys oder Kampagnen: Auswählen des richtigen Ansatzes {#journeys-vs-campaigns}

[!DNL Adobe Journey Optimizer] bietet vier Möglichkeiten, Ihre Kundinnen und Kunden zu erreichen und anzusprechen: **Journey**, **Aktionskampagnen**, **API-ausgelöste Kampagnen** und **orchestrierte Kampagnen**. Die Auswahl des richtigen Elements hängt davon ab, ob Sie 1:1 Orchestrierung in Echtzeit, geplante Sendungen, ereignisgesteuerte Nachrichten oder komplexe Batch-Workflows benötigen.

Dieses Handbuch hilft Ihnen bei der Auswahl anhand von Ausführungsstil, Datenanforderungen und Anwendungsfall - mit einem schnellen Vergleich, Entscheidungsbaum und konkreten Beispielen.

## Schnellvergleich – Überblick {#quick-overview}

| Ansatz | Geeignet für | Ausführungsstil |
|----------|----------|-----------------|
| **Journeys** | Mehrstufige Echtzeit-Kundenerlebnisse mit bedingter Logik | 1:1-Orchestrierung – jedes Profil im eigenen Tempo |
| **Aktionskampagnen** | Geplante oder wiederkehrende Sendungen an Zielgruppen | Batch-Ausführung - Zielgruppe zum Versandzeitpunkt gemeinsam verarbeitet |
| **API-ausgelöste Kampagnen** | Ereignisgesteuerte oder Transaktionsnachrichten von externen Systemen | Ausführung auf Anfrage - ausgelöst durch API-Aufruf mit Payload |
| **Orchestrierte Kampagnen** | Komplexe Batch-Workflows mit Segmentierung in mehrere Entitäten | Batch-Arbeitsfläche – alle Profile werden gemeinsam verarbeitet |

>[!TIP]
>
>**Schnelle Faustregel:** muss sich jeder Kunde in seinem eigenen Tempo mit Echtzeit-Logik bewegen? Verwenden Sie **Journey**. Eine Nachricht nach einem Zeitplan an eine Zielgruppe senden? Verwenden Sie **Aktionskampagnen**. Wird von einem externen System über API ausgelöst? Verwenden Sie **API-ausgelöste Kampagnen**. Benötigen Sie Daten mit mehreren Entitäten, exakte Zählungen oder eine Batch-Arbeitsfläche? Verwenden **orchestrierten Kampagnen**.

## Detaillierter Vergleich {#detailed-comparison}

Verwenden Sie diese umfassende Tabelle, um die wichtigsten Unterschiede zu verstehen:

| Funktion | Journeys | Aktionskampagnen | Durch API ausgelöste Kampagnen | Orchestrierte Kampagnen |
|---------|----------|------------------|------------------------|----------------------|
| **Primärer Zweck** | Mehrstufige 1:1-Orchestrierung mit Echtzeit-Kundenkontext | Einmaliger oder wiederkehrender Nachrichtenversand an Zielgruppen | Transaktions- oder ereignisgesteuerte Nachrichten, die von externen Systemen initiiert werden | Mehrstufige Batch-Kampagnen mit komplexen Segmentierungs-Workflows |
| **Typ der Arbeitsfläche** | 1:1-Arbeitsfläche – jedes Profil bewegt sich im eigenen Tempo | Keine Arbeitsfläche – Ausführung einer einzelnen Aktion | Keine Arbeitsfläche – Ausführung einer einzelnen Aktion | Batch-Arbeitsfläche – alle Profile werden gemeinsam verarbeitet |
| **Ausführungsfluss** | Sequenzielle Aktionen, Profilstatus wird während der Journey beibehalten | Simultane Ausführung für die gesamte Zielgruppe | Sofortige Ausführung pro API-Aufruf | Mehrstufiger Batch-Workflow mit Aktivitäten und Transitionen |
| **Eintrittsmechanismus** | Veranstaltungen, Zielgruppen, Qualifizierungen, Geschäftsereignisse | Manuelle Aktivierung und Planung | API-Aufruf aus externem System | Geplante Ausführung des Batch-Workflows |
| **Datenmodell** | Echtzeitprofil und Ereignisdaten | Profildaten aus Experience Platform-Zielgruppen | API-Payload-Daten mit optionaler Profilsuche | Relationale Daten mit mehreren Entitäten (Profile, Produkte, Stores, Buchungen) |
| **Segmentierung** | Vorkonfigurierte Zielgruppen und Echtzeitbedingungen | Vorkonfigurierte Zielgruppen aus Experience Platform | Payload-gesteuertes Targeting (keine geplante Zielgruppe) | Auf der Arbeitsfläche erstellte On-Demand-Zielgruppen mit exakter Anzahl |
| **Profilverarbeitung** | Individuell, in Echtzeit (wenn Ereignisse auftreten) | Batch, alle auf einmal | Per API-Aufruf, Payload-gesteuert | Batch, alle zusammen mit Unterstützung für mehrere Entitäten |
| **Personalisierung** | Echtzeit-Kontextdaten und Profilattribute | Profilattribute | Payload-Daten + optionale Profilattribute | Daten mit mehreren Entitäten für Präzisions-Targeting |
| **Komplexität** | Mehrstufig mit Verzweigung, Wartezeiten, Bedingungen | Einzelne Aktion oder einfacher Workflow | Einzelne Aktion mit Payload-Zuordnung | Mehrstufige Batch-Workflows mit Segmentierung, Anreicherung, Aufspaltung |
| **Geeignet für** | Kundenzyklus-Journeys, Onboarding, Warenkorbabbruch | Werbekampagnen, Newsletter, Ankündigungen | Bestellbestätigungen, Versandwarnungen, Zurücksetzen des Kennworts | Komplexe saisonale Kampagnen, mehrstufige Promotions, Produkteinführungen |
| **Timing** | Fortlaufend, ab Veröffentlichung immer aktiv | Geplante Start-/Enddaten | On-Demand, ereignisgesteuert über API | Batch-Ausführung nach Zeitplan |
| **Status-Management** | Behält den Kundenstatus für Echtzeit-Aktionen bei | Statuslose Ausführung | Staatenlose Ausführung pro Aufruf | Batch-Verarbeitung mit Arbeitstabellen |
| **Verwendung** | Mehrere Touchpoints mit Entscheidungslogik in Echtzeit erforderlich | Einfache Nachricht an eine Audience zu einem bestimmten Zeitpunkt | Das externe System muss sofort einen Trigger für eine Nachricht erstellen | Komplexe Segmentierung, Daten mit mehreren Entitäten oder exakte Anzahl der Vorabsendungen erforderlich |
| **Individuelle Funktionen** | Echtzeit-Reaktionen, Warteaktivitäten, profilbasierte Geschwindigkeit | Planung, Zielgruppen-Targeting, Ratensteuerung | API-Payload-Zuordnung, System-zu-System-Triggerung | Relationale Datensätze, Segmentierung in mehrere Entitäten, exakte Anzahl, Versand auf mehreren Ebenen |

## Entscheidungshilfe {#decision-guide}

Folgen Sie diesem Entscheidungsbaum, um den richtigen Ansatz zu wählen. Viele Marken verwenden mehr als einen Typ. Wählen Sie für jeden Anwendungsfall die am besten geeignete aus.

### Schritt 1: Was ist Ihre Ausführungsanforderung?

**Individuelle Antworten in Echtzeit auf das Kundenverhalten?**
→ **Journeys verwenden**
* Profile müssen sich in ihrem eigenen Tempo bewegen
* Bedingte Logik basierend auf dem Verhalten
* Echtzeitkontext ist entscheidend

**Einfacher Nachrichtenversand an eine Zielgruppe zu einem geplanten Zeitpunkt?**
→ **Verwenden von Aktionskampagnen**
* Alle Profile erhalten die Nachricht gleichzeitig
* Geplante oder wiederkehrende Sendungen
* Keine komplexe mehrstufige Logik erforderlich

**Sofortige Nachricht durch ein externes System ausgelöst?**
→ **API-ausgelöste Kampagnen verwenden**
* Wird bei Bedarf über einen API-Aufruf ausgelöst
* Payload-gesteuerte Personalisierung
* Keine komplexe mehrstufige Logik erforderlich

**Komplexer Batch-Workflow mit erweiterter Segmentierung?**
→ **Orchestrierte Kampagnen verwenden**
* Daten mit mehreren Entitäten (Produkte, Geschäfte, Buchungen) erforderlich
* Exakte Zählung vor dem Versand erforderlich
* Mehrstufige Batch-Verarbeitung mit Aufspaltungen und Anreicherung

### Schritt 2: Prüfen Sie Ihre Auswahl

| Ihre Anforderungen | Empfohlener Ansatz | Warum |
|-----------|---------------------|-----|
| Neue Kundschaft mit mehrstufigem Onboarding begrüßen | Journeys | Eintritt in Echtzeit, mehrere Touchpoints, bedingte Pfade |
| Senden eines monatlichen Newsletters an Abonnentinnen und Abonnenten | Aktionskampagnen | Einfache geplante Nachricht an Zielgruppe |
| Warenkorbabbruch mit Erinnerungssequenz | Journeys | Echtzeit-Trigger, Wartezeiten, bedingte Nachverfolgung |
| Werbeankündigung an alle Kundinnen und Kunden | Aktionskampagnen | Einmalige Nachricht, sofortiger Versand |
| Erneutes Ansprechen inaktiver Benutzender auf Grundlage des Verhaltens | Journeys | Ausgelöst durch Zielgruppenqualifizierung, personalisierter Pfad |
| Blitzverkauf ausgelöst durch Geschäftsereignis | Journeys (Geschäftsereignis) | Echtzeit-Trigger mit Auswirkung auf mehrere Kundinnen und Kunden |
| Saisonale Promotion mit Produktkatalogintegration | Orchestrierte Kampagnen | Daten mit mehreren Entitäten, komplexe Segmentierung, genaue Anzahl |
| Durch API ausgelöste Transaktionsnachricht | Durch API ausgelöste Kampagnen | Externe System-Trigger, sofortiger Versand |
| Mehrstufiger Versand pro Buchung | Orchestrierte Kampagnen | Beziehungen mit mehreren Entitäten, eine Nachricht pro Buchung |

## Erläuterung der wichtigsten Unterschiede {#key-distinctions}

### Journeys: 1:1-Orchestrierung in Echtzeit

**Alleinstellungsmerkmal:**
* Jedes Profil behält seinen individuellen Status und Kontext bei
* Eintritt und Fortschritt jedes Profils im eigenen Tempo
* Entscheidungsfindung in Echtzeit basierend auf Verhalten und Ereignissen
* Warteaktivitäten erstellen eine personalisierte Zeitplanung
* Bedingte Verzweigungen erstellen eindeutige Pfade pro Profil

**Beispielfluss:**

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Jede Person erlebt basierend auf ihren Aktionen ihre eigene Journey-Timeline.

[Weitere Informationen über Journeys](../building-journeys/journey.md)

### Kampagnen: Einfacher Batch-Versand oder ausgelöster Versand

**Alleinstellungsmerkmal:**
* Alle Profile werden identisch und gleichzeitig verarbeitet
* Statuslose Ausführung – kein Kontext beibehalten
* Einfache Planung oder API-Auslösung
* Ideal für Broadcast-Kommunikation

**Beispielfluss:**

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

Jede Person bekommt dieselbe Botschaft zur selben Zeit.

**Typen:**
* **Aktionskampagnen**: Geplanter Versand an Zielgruppen (einmal oder wiederkehrend)
* **API-ausgelöste Kampagnen**: Versand auf Anfrage, ausgelöst durch einen API-Aufruf mit Payload-Daten

[Weitere Informationen zu Kampagnen](../campaigns/get-started-with-campaigns.md)

### Orchestrierte Kampagnen: Batch-Arbeitsflächen-Workflows

**Alleinstellungsmerkmal:**
* Batch-Arbeitsfläche mit Aktivitäten und Transitionen (ähnlich wie Journey-Arbeitsfläche, aber Batch-orientiert)
* Unterstützung relationaler Daten mit mehreren Entitäten (Profile + Produkte + Geschäfte + Buchungen)
* On-Demand-Zielgruppenerstellung auf der Arbeitsfläche
* Exakte Anzahl vor dem Versand (Sichtbarkeit vor dem Versand)
* Versand auf mehreren Ebenen (eine Nachricht pro Entität, z. B. pro Buchung)
* Alle Profile werden im Batch gemeinsam verarbeitetet

**Beispielfluss:**

```
Query customers → Filter by purchase history → Split by region → 
Enrich with product data → Build segments → Send personalized offers → All in one batch execution
```

Kombiniert die Komplexität eines Workflows mit der Batch-Kampagnenausführung.

[Weitere Informationen über orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)

## Beispiele für Anwendungsfälle {#use-cases}

### Anwendungsfälle für Journeys

* **Wiederherstellen abgebrochener Warenkörbe:** Ausgelöst beim Hinzufügen zum Warenkorb, Warten auf Checkout gewartet, Versand von Erinnerungen, wenn kein Kauf stattfindet
* **Kunden-Onboarding:** Mehrstufige Willkommensserie mit personalisierten Inhalten, die auf Profildaten basieren
* **Upgrade der Treuestufe:** Wird ausgelöst, wenn die Person eine neue Stufe erreicht, Versand von Glückwünschen und Vorteilen
* **Geburtstagskampagnen:** Eintritt basierend auf Geburtsdatum, personalisierte Angebote
* **Wiederaufnahme der Interaktion:**: Ausgelöst durch Zielgruppenqualifizierung (Inaktivität), progressive Kontaktaufnahme

### Anwendungsfälle für Kampagnen (durch Aktion und API ausgelöst)

**Aktionskampagnen:**
* **Monatliche Newsletter:** Geplanter Batch-Versand an das Abonnentensegment
* **Werbeankündigungen:** Zeitkritische Angebote für Zielgruppen
* **Produkteinführungen:** Koordinierte Ankündigung an alle Kundinnen und Kunden
* **Saisonale Grüße:** Feiertagsnachrichten zu bestimmten Terminen

**Durch API ausgelöste Kampagnen:**
* **Bestellbestätigungen:** Ausgelöst durch E-Commerce-System nach dem Kauf
* **Versandbenachrichtigungen:** Ausgelöst durch Logistiksystem
* **Kontowarnungen:** Ausgelöst durch ein System zur Betrugserkennung
* **Passwortzurücksetzung:** Ausgelöst durch Benutzeraktion in der Anwendung

### Anwendungsfälle für orchestrierte Kampagnen

* **Saisonale Promotion mit Katalogintegration:** Abfragen des Produktkatalogs, Identifizieren von berechtigten Kundinnen und Kunden, Segmentieren nach Präferenzen, Versand von personalisierten Produktempfehlungen
* **Store-spezifische Kampagnen:** Targeting von Kundinnen und Kunden in der Nähe bestimmter Store-Standorte mit Store-Inventardaten
* **Kommunikation zu mehreren Buchungen:** Versand einer Nachricht pro Buchung (Hotelreservierung, Flugbuchungen)
* **Komplexe Segmentorchestrierung:** Erstellen von Zielgruppen schrittweise durch Anreicherung aus mehreren Datenquellen
* **Validierung vor dem Versand:** Ermitteln der genauen Empfängeranzahl, bevor große Kampagnen gestartet werden

## Funktionsverfügbarkeit {#feature-availability}

### Kanäle

| Kanal | Journeys | Aktionskampagnen | Durch API ausgelöste Kampagnen | Orchestrierte Kampagnen |
|---------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| E-Mail | ✅ | ✅ | ✅ | ✅ |
| Push-Benachrichtigung | ✅ | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ | ✅ |
| In-App | ✅ | ✅ | ✅ | ❌ |
| Web | ✅ | ✅ | ❌ | ❌ |
| Code-basiert | ✅ | ✅ | ❌ | ❌ |
| Inhaltskarten | ✅ | ✅ | ❌ | ❌ |
| Direkt-Mail | ✅ | ✅ | ❌ | ✅ |

### Erweiterte Funktionen

| Funktion | Journeys | Aktionskampagnen | Durch API ausgelöste Kampagnen | Orchestrierte Kampagnen |
|-----------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| Mehrstufige Workflows | ✅ | ❌ | ❌ | ✅ |
| Echtzeit-Trigger | ✅ | ❌ | ✅ | ❌ |
| Warteaktivitäten | ✅ | ❌ | ❌ | ✅ |
| Bedingte Verzweigung | ✅ | ❌ | ❌ | ✅ |
| Geplante Ausführung | ✅ | ✅ | ✅ | ✅ |
| API-Auslösung | ❌ | ❌ | ✅ | ❌ |
| Daten mit mehreren Entitäten | ❌ | ❌ | ❌ | ✅ |
| Genaue Anzahl vor dem Versand | ❌ | ❌ | ❌ | ✅ |
| On-Demand-Segmentierung | ❌ | ❌ | ❌ | ✅ |
| Versandzeitoptimierung | ✅ | ✅ | ✅ | ✅ |
| A/B-Tests | ✅ | ✅ | ❌ | ❌ |
| Genehmigungs-Workflows | ✅ | ✅ | ✅ | ❌ |

## Häufige Fragen {#common-questions}

+++ Kann ich Journeys und Kampagnen in meiner Marketing-Strategie kombinieren?

Ja. Viele Unternehmen verwenden alle vier Ansätze für verschiedene Szenarien:

* **Journey** für verhaltensbezogene Interaktion in Echtzeit
* **Aktionskampagnen** für geplante Broadcast-Nachrichten
* **API-ausgelöste**) für Transaktionsnachrichten
* **Orchestrierte**: für komplexe, datenintensive Batch-Kampagnen

Verwenden Sie für jeden Anwendungsfall das richtige Tool, anstatt für alles einen Ansatz zu erzwingen.

+++

+++ Kann ich eine Kampagne in eine Journey konvertieren oder umgekehrt?

Nein, Sie müssen das Erlebnis im entsprechenden Format neu erstellen. Sie können jedoch Inhalte, Zielgruppen und Logikkonzepte wiederverwenden.

+++

+++ Welcher Ansatz ist einfacher zu erstellen?

Aktionskampagnen sind in der Regel am einfachsten (eine Nachricht an die Zielgruppe), gefolgt von durch API ausgelösten Kampagnen, Journeys (komplexer, mit Mehrstufenlogik) und orchestrierten Kampagnen (am komplexesten aufgrund des Arbeitsflächen-Workflows und der Funktionen für mehrere Entitäten).

+++

+++ Welcher Ansatz ist besser für große Zielgruppen geeignet?

Alle vier können gut skalieren. Die richtige Wahl hängt von Ihrem Muster ab:

* **Audience-Journey lesen** und **Action-** sind für große Batch-Zielgruppen optimiert (eine Nachricht oder ein Fluss zu mehreren Profilen gleichzeitig).
* **Orchestrierte Kampagnen** zeichnen sich durch eine komplexe Segmentierung mit großen Datensätzen und Daten mit mehreren Entitäten aus.
* **Unitäre (ereignisbasierte) Journey** verarbeiten Profile einzeln, wenn Ereignisse auftreten. Die Skalierung hängt daher vom Ereignisvolumen und -durchsatz ab.

+++

+++ Kann ich dieselbe Zielgruppe für Journeys und Kampagnen verwenden?

Ja. In [!DNL Adobe Experience Platform] erstellte Zielgruppen können in Journey-, Aktionskampagnen- und orchestrierten Kampagnen verwendet werden (wobei Zielgruppenlogik auch auf der Arbeitsfläche nach Bedarf erstellt werden kann). API-ausgelöste Kampagnen werden über die Payload gesteuert und verwenden vordefinierte Zielgruppen nicht auf die gleiche Weise.

+++

## Nächste Schritte {#next-steps}

Bereit, mit dem Erstellen zu beginnen? Informieren Sie sich in der ausführlichen Dokumentation zu Ihrem gewählten Ansatz:

* **[Erste Schritte mit Journey](../building-journeys/journey.md)** - Journey-Typen, Designer und Workflow
* **[Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md)** - Aktion und API-ausgelöste Kampagnen
* **[Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)** - Batch-Arbeitsflächen-Workflows

>[!MORELIKETHIS]
>
>* [Vergleich der Journey-Typen](../building-journeys/journey.md#journey-types-comparison)
>* [Vergleich der Kampagnentypen](../campaigns/get-started-with-campaigns.md#campaign-types)
>* [Häufig gestellte Fragen zu Journeys](../building-journeys/journey-faq.md)
>* [Häufig gestellte Fragen zu Orchestrierten Kampagnen](../orchestrated/orchestrated-campaigns-faq.md)
