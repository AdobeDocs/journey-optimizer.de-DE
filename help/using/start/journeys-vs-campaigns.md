---
solution: Journey Optimizer
product: journey optimizer
title: Journey vs. Kampagnen - Wählen Sie den richtigen Ansatz
description: Vergleichen Sie Journey, Kampagnen und orchestrierte Kampagnen, um den richtigen Ansatz für Ihre Marketing-Anforderungen in Adobe Journey Optimizer zu wählen
feature: Journeys, Campaigns, Get Started, Overview
role: User
level: Beginner
keywords: Journey, Kampagne, orchestriert, Vergleich, Auswählen, Entscheidung, Workflow, Echtzeit, Batch, Orchestrierung, mehrstufig, geplant, API-ausgelöst, ereignisgesteuert
hide: true
hidefromtoc: true
source-git-commit: 8ea2a0fe685678d41004d549443a1757eb30c765
workflow-type: tm+mt
source-wordcount: '1344'
ht-degree: 3%

---


# Journey vs. Kampagnen: Wählen Sie den richtigen Ansatz {#journeys-vs-campaigns}

Adobe Journey Optimizer bietet drei leistungsstarke Ansätze, um Ihre Kunden zu erreichen und anzusprechen. Um effektive Marketing-Erlebnisse zu schaffen, ist es von entscheidender Bedeutung, zu verstehen, wann die einzelnen Lösungen verwendet werden.

Dieses Handbuch hilft Ihnen bei der Auswahl zwischen **Journey**, **Kampagnen** (Aktion und API-ausgelöst) und **Orchestrierten Kampagnen** basierend auf Ihren spezifischen Marketing-Anforderungen.

## Übersicht über den Schnellvergleich {#quick-overview}

| Annäherung | Am besten geeignet für | Ausführungsstil |
|----------|----------|-----------------|
| **Journeys** | Mehrstufige Echtzeit-Kundenerlebnisse mit bedingter Logik | 1:1 Orchestrierung - jedes Profil in seinem eigenen Tempo |
| **Kampagnen (Aktion und API)** | Einfacher, geplanter oder ausgelöster Nachrichtenversand | Batch- oder API-gesteuert - alle Profile gleichzeitig |
| **Orchestrierte Kampagnen** | Komplexe Batch-Workflows mit Segmentierung mehrerer Entitäten | Arbeitsfläche für Stapel - Alle Profile werden gemeinsam verarbeitet |

## Detailvergleich {#detailed-comparison}

Verwenden Sie diese umfassende Tabelle, um die wichtigsten Unterschiede zu verstehen:

| Funktion | Journeys | Kampagnen (Aktion und API-ausgelöst) | Orchestrierte Kampagnen |
|---------|----------|-----------------------------------|----------------------|
| **Primärer Zweck** | Mehrstufige 1:1 Orchestrierung mit Echtzeit-Kundenkontext | Einmaliger oder wiederkehrender Nachrichtenversand an Zielgruppen | Mehrstufige Batch-Kampagnen mit komplexen Segmentierungs-Workflows |
| **Canvas-Typ** | 1:1 Arbeitsfläche - Jedes Profil bewegt sich in seinem eigenen Tempo | Keine Arbeitsfläche - Ausführung einer einzelnen Aktion | Arbeitsfläche für Stapel - Alle Profile werden gemeinsam verarbeitet |
| **Ausführungsfluss** | Sequenzielle Aktionen, Profilstatus wird beim Journey beibehalten | Simultane Ausführung für die gesamte Zielgruppe | Mehrstufiger Batch-Workflow mit Aktivitäten und Transitionen |
| **Eingabemechanismus** | Veranstaltungen, Audiences, Qualifikationen, Geschäftsereignisse | Manuelle Aktivierung, geplant oder API-Trigger | Geplante Ausführung des Batch-Workflows |
| **Datenmodell** | Echtzeit-Profil + Ereignisdaten | Profildaten + API-Payload | Relationale Daten mit mehreren Entitäten (Profile, Produkte, Stores, Buchungen) |
| **Segmentierung** | Vordefinierte Zielgruppen + Echtzeitbedingungen | Vordefinierte Zielgruppen aus Experience Platform | Auf der Arbeitsfläche erstellte On-Demand-Zielgruppen mit exakter Anzahl |
| **Profilverarbeitung** | Individuell, in Echtzeit (wenn Ereignisse auftreten) | Batch, alle auf einmal | Batch, alle zusammen mit Unterstützung für mehrere Entitäten |
| **Personalisierung** | Echtzeit-Kontextdaten + Profilattribute | Profilattribute + API-Payload-Daten | Daten mit mehreren Entitäten für Präzisions-Targeting |
| **Komplexität** | Mehrstufig mit Verzweigung, Wartezeiten, Bedingungen | Einzelne Aktion oder einfacher Workflow | Mehrstufige Batch-Workflows mit Segmentierung, Anreicherung, Aufspaltung |
| **Am besten geeignet für** | Customer Lifecycle Journey, Onboarding, Warenkorbabbruch | Werbekampagnen, Newsletter, Ankündigungen, Transaktionsnachrichten | Komplexe saisonale Kampagnen, mehrstufige Werbeaktionen, Produkteinführungen |
| **Timing** | Fortlaufend, immer aktiv, sobald veröffentlicht | Geplante Start-/Enddaten oder API-gesteuert | Batch-Ausführung planmäßig |
| **State-Management** | Behält den Kundenstatus für Echtzeit-Aktionen bei | Staatenlose Ausführung | Stapelverarbeitung mit Tabellen |
| **Verwenden Sie wenn** | Mehrere Touchpoints mit Entscheidungslogik in Echtzeit erforderlich | Einfache Nachricht an Zielgruppe zu einem bestimmten Zeitpunkt | Komplexe Segmentierung, Daten mehrerer Entitäten oder exakte Anzahl der Vorabsendungen erforderlich |
| **Eindeutige Funktionen** | Echtzeit-Reaktionen, Warteaktivitäten, profilbasierte Geschwindigkeit | Einfache Planung, API-Auslösung, Ratensteuerung | Relationale Datensätze, Segmentierung mehrerer Entitäten, exakte Anzahl, Versand auf mehreren Ebenen |

## Entscheidungshandbuch {#decision-guide}

Folgen Sie diesem Entscheidungsbaum, um den richtigen Ansatz zu wählen:

### Schritt 1: Was ist Ihre Ausführungsanforderung?

**Individuelle Antworten in Echtzeit auf das Kundenverhalten?**
→ **Journey verwenden**
- Profile müssen sich in ihrem eigenen Tempo bewegen
- Bedingte Logik basierend auf dem Verhalten
- Der Echtzeit-Kontext ist entscheidend

**Einfacher Nachrichtenversand an eine Zielgruppe?**
→ **Verwenden von Aktionen oder API-ausgelösten Kampagnen**
- Alle Profile erhalten die Nachricht gleichzeitig
- Geplant oder über API ausgelöst
- Keine komplexe mehrstufige Logik erforderlich

**Komplexer Batch-Workflow mit erweiterter Segmentierung?**
→ **Verwenden von orchestrierten Kampagnen**
- Daten mit mehreren Entitäten (Produkte, Geschäfte, Buchungen) benötigen
- Exakte Zählung vor dem Versand verlangen
- Mehrstufige Batch-Verarbeitung mit Aufspaltung und Anreicherung

### Schritt 2: Auswahl validieren

| Ihre Anforderungen | Empfohlener Ansatz | Warum |
|-----------|---------------------|-----|
| Begrüßen Sie neue Kunden mit mehrstufigem Onboarding | Journeys | Echtzeiteingabe, mehrere Touchpoints, bedingte Pfade |
| Monatlichen Newsletter an Abonnenten senden | Aktionskampagne | Einfache geplante Nachricht an Zielgruppe |
| Warenkorbabbruch mit Erinnerungssequenz | Journeys | Echtzeit-Trigger, Wartezeiten, bedingte Nachverfolgung |
| Werbe-Ankündigung an alle Kunden | Aktionskampagne | Einmalige Nachricht, sofortiger Versand |
| Erneutes Ansprechen inaktiver Benutzer auf Grundlage des Verhaltens | Journeys | Ausgelöst durch Zielgruppen-Qualifizierung, personalisierter Pfad |
| Flash-Verkauf ausgelöst durch Geschäftsereignis | Journey (Geschäftsereignis) | Echtzeit-Trigger mit Auswirkung auf mehrere Kunden |
| Saisonale Promotion mit Produktkatalogintegration | Orchestrierte Kampagne | Daten mit mehreren Entitäten, komplexe Segmentierung, genaue Anzahl |
| API-ausgelöste Transaktionsnachricht | API-ausgelöste Kampagne | Trigger externer Systeme, sofortige Lieferung |
| Mehrstufiger Versand pro Buchung | Orchestrierte Kampagne | Beziehungen mit mehreren Entitäten, eine Nachricht pro Buchung |

## Erläuterung der wichtigsten Unterscheidungen {#key-distinctions}

### Journey: 1:1 Echtzeit-Orchestrierung

**Was ihn einzigartig macht:**
- Jedes Profil behält seinen individuellen Status und Kontext bei
- Profile treten in ihrem eigenen Tempo ein und schreiten fort
- Entscheidungsfindung in Echtzeit basierend auf Verhalten und Ereignissen
- Warteaktivitäten erstellen eine personalisierte Zeitplanung
- Bedingte Verzweigungen erstellen eindeutige Pfade pro Profil

**Beispielfluss:**

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Jeder Kunde erlebt seine eigene Journey-Timeline basierend auf seinen Aktionen.

[Weitere Informationen über Journey](../building-journeys/journey.md)

### Kampagnen: Einfacher Batch- oder ausgelöster Versand

**Was ihn einzigartig macht:**
- Alle Profile werden identisch und gleichzeitig verarbeitet
- Staatenlose Ausführung - kein Kontext beibehalten
- Einfache Planung oder API-Auslösung
- Ideal für Broadcast-Kommunikation

**Beispielfluss:**

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

Jeder bekommt die gleiche Botschaft zur gleichen Zeit.

**types:**
- **Aktionskampagnen**: Geplanter Versand (einmalig oder wiederkehrend)
- **API-ausgelöste Kampagnen**: Wird über einen API-Aufruf von externen Systemen ausgelöst

[Weitere Informationen zu Kampagnen](../campaigns/get-started-with-campaigns.md)

### Orchestrierte Kampagnen: Workflows für Batch-Arbeitsflächen

**Was ihn einzigartig macht:**
- Batch-Arbeitsfläche mit Aktivitäten und Transitionen (ähnlich wie Journey-Arbeitsfläche, aber stapelorientiert)
- Unterstützung relationaler Daten mehrerer Entitäten (Profile + Produkte + Geschäfte + Buchungen)
- Erstellung einer On-Demand-Zielgruppe auf der Arbeitsfläche
- Exakte Anzahl vor dem Senden (Sichtbarkeit vor dem Senden)
- Versand auf mehreren Ebenen (eine Nachricht pro Entität, z. B. pro Buchung)
- Alle im Batch verarbeiteten Profile

**Beispielfluss:**

```
Query customers → Filter by purchase history → Split by region → 
Enrich with product data → Build segments → Send personalized offers → All in one batch execution
```

Kombiniert die Komplexität eines Workflows mit der Ausführung einer Batch-Kampagne.

[Weitere Informationen über orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)

## Anwendungsbeispiele {#use-cases}

### Anwendungsfälle für Journeys

&#x200B;* **Wiederherstellung bei Warenkorbabbruch**: Wird durch das Ereignis zum Hinzufügen des Warenkorbs ausgelöst, auf den Checkout warten und Erinnerungen senden, wenn kein Kauf stattfindet
&#x200B;* **Kunden-Onboarding**: Mehrstufige Willkommensserie mit personalisierten Inhalten, die auf Profildaten basieren
&#x200B;* **Upgrade der Treuestufe** Wird ausgelöst, wenn der Kunde eine neue Stufe erreicht, und sendet Glückwünsche und Vorteile
&#x200B;* **Geburtstagskampagnen**: Eingabe basierend auf Geburtsdatum, personalisierte Angebote
&#x200B;* **Rückgewinnung**: Ausgelöst durch Zielgruppen-Qualifizierung (Inaktivität), progressive Kontaktaufnahme

### Anwendungsfälle für Kampagnen (Aktion und API-gesteuert)

**Aktionskampagnen:**
&#x200B;* **Monatliche Newsletter**: Geplanter Batch-Versand an das Abonnentensegment
&#x200B;* **Werbeanzeigen**: Zeitkritische Angebote für Zielgruppen
&#x200B;* **Produkteinführungen**: Koordinierte Ankündigung an alle Kunden
&#x200B;* **Saisonale Grüße**: Feiertagsnachrichten zu bestimmten Terminen

**API-ausgelöste Kampagnen:**
&#x200B;* **Bestellbestätigungen**: Wird vom E-Commerce-System nach dem Kauf ausgelöst
&#x200B;* **Versandbenachrichtigungen**: Ausgelöst durch Logistiksystem
&#x200B;* **Kontowarnungen** Ausgelöst durch ein System zur Betrugserkennung
&#x200B;* **Kennwortzurücksetzung**: Wird durch Benutzeraktion im Programm ausgelöst

### Anwendungsfälle für orchestrierte Kampagnen

&#x200B;* **Saisonale Promotion mit Katalogintegration**: Abfragen eines Produktkatalogs, Identifizieren zugelassener Kunden, Segmentieren nach Voreinstellungen, Senden personalisierter Produktempfehlungen
&#x200B;* **Store-spezifische Kampagnen**: Targeting von Kunden in der Nähe bestimmter Store-Standorte mit Store-Inventardaten
&#x200B;* **Multi-Booking-Kommunikation**: Versand einer Nachricht pro Buchung (Hotelreservierung, Flugbuchungen)
&#x200B;* **Komplexe Segmentorchestrierung**: Erstellen Sie Zielgruppen schrittweise mit einer Anreicherung aus mehreren Datenquellen
&#x200B;* **Validierung vor dem Versand**: Ermitteln der genauen Empfängeranzahl, bevor große Kampagnen gestartet werden

## Funktionsverfügbarkeit {#feature-availability}

### Kanäle

| Kanal | Journeys | Aktionskampagnen | API-ausgelöste Kampagnen | Orchestrierte Kampagnen |
|---------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| E-Mail | ✅ | ✅ | ✅ | ✅ |
| Push-Benachrichtigung | ✅ | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ | ✅ |
| In-App | ✅ | ✅ | ✅ | ❌ |
| Web | ✅ | ✅ | ❌ | ❌ |
| Code-basiert | ✅ | ✅ | ❌ | ❌ |
| Inhaltskarten | ✅ | ✅ | ❌ | ❌ |
| Direkt-Mail | ✅ | ✅ | ❌ | ❌ |

### Erweiterte Funktionen

| Funktion | Journeys | Aktionskampagnen | API-ausgelöste Kampagnen | Orchestrierte Kampagnen |
|-----------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| Mehrstufige Workflows | ✅ | ❌ | ❌ | ✅ |
| Echtzeit-Trigger | ✅ | ❌ | ✅ | ❌ |
| Warteaktivitäten | ✅ | ❌ | ❌ | ✅ |
| bedingte Programmverzweigung | ✅ | ❌ | ❌ | ✅ |
| Geplante Ausführung | ✅ | ✅ | ✅ | ✅ |
| API-Trigger | ❌ | ❌ | ✅ | ❌ |
| Daten mit mehreren Entitäten | ❌ | ❌ | ❌ | ✅ |
| Genaue Anzahl der Vorabsendungen | ❌ | ❌ | ❌ | ✅ |
| On-Demand-Segmentierung | ❌ | ❌ | ❌ | ✅ |
| Optimierung des Versandzeitpunkts | ✅ | ✅ | ✅ | ✅ |
| A/B-Tests | ✅ | ✅ | ❌ | ❌ |
| Genehmigungs-Workflows | ✅ | ✅ | ✅ | ❌ |

## Häufige Fragen {#common-questions}

**F: Kann ich Journey und Kampagnen in meiner Marketing-Strategie kombinieren?**

A: Absolut! Die meisten Unternehmen verwenden alle drei Ansätze für verschiedene Szenarien:
- Journey für verhaltensbezogene Interaktion in Echtzeit
- Aktionskampagnen für geplante Broadcast-Nachrichten
- API-gesteuerte Kampagnen für Transaktionsnachrichten
- Orchestrierte Kampagnen für komplexe, datenintensive Batch-Kampagnen

**F: Kann ich eine Kampagne in eine Journey konvertieren oder umgekehrt?**

A: Nein, Sie müssen das Erlebnis im entsprechenden Format neu erstellen. Sie können jedoch Inhalte, Zielgruppen und Logikkonzepte wiederverwenden.

**F: Welcher Ansatz ist einfacher zu erstellen?**

A.: Aktionskampagnen sind in der Regel die einfachste (eine Nachricht an die Zielgruppe), gefolgt von API-ausgelösten Kampagnen, Journey (komplexer mit Mehrstufenlogik) und orchestrierten Kampagnen (am komplexesten aufgrund des Arbeitsflächen-Workflows und der Funktionen für mehrere Entitäten).

**F: Welche Skalierung ist für große Zielgruppen besser?**

A: Alle drei können gut skalieren, aber:
- **Journey** und **Action-** sind für große Batch-Zielgruppen optimiert
- **Orchestrierte Kampagnen** zeichnen sich durch eine komplexe Segmentierung mit großen Datensätzen aus
- **Unitäre Journey** verarbeiten Profile einzeln, sodass die Skalierung vom Ereignisvolumen abhängt

**F: Kann ich dieselbe Zielgruppe für Journey und Kampagnen verwenden?**

A: Ja, in Adobe Experience Platform erstellte Zielgruppen können für alle drei Ansätze verwendet werden.

## Nächste Schritte {#next-steps}

Bereit mit dem Bau zu beginnen? Informieren Sie sich in der ausführlichen Dokumentation zu Ihrem gewählten Ansatz:

&#x200B;* **[Erste Schritte mit Journey](../building-journeys/journey.md)** - Erfahren Sie mehr über Journey-Typen, Designer und Workflow
&#x200B;* **[Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md)** - Erkunden von Aktionen und API-ausgelösten Kampagnen
&#x200B;* **[Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)** - Entdecken Sie Batch-Arbeitsflächen-Workflows

**Benötigen Sie weitere Hilfe bei der Entscheidungsfindung?**
- [Vergleich der Journey-Typen](../building-journeys/journey.md#journey-types-comparison)
- [Vergleich der Kampagnentypen](../campaigns/get-started-with-campaigns.md#campaign-types)
- [Häufig gestellte Fragen zum Journey](../building-journeys/journey-faq.md)
- [Häufig gestellte Fragen zu orchestrierten Kampagnen](../orchestrated/orchestrated-campaigns-faq.md)

