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
exl-id: 8b4d010e-4278-49fd-a7d3-dcc706829577
TQID: https://experienceleague.adobe.com/RWLVSULVO0idnCs5OVQR1yVvNv1G0JwP3y-3sNXQg50
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: addf009e-030a-4310-8534-776a3e62ed48id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 9dba85545968da9957c42516cb03a4e77ed302f1
workflow-type: tm+mt
source-wordcount: 1904
ht-degree: 55%

---

# Journey vs. Kampagnen: Wählen Sie den richtigen Ansatz {#journeys-vs-campaigns}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Vergleichen Sie Journey mit Aktionen, API-ausgelösten und orchestrierten Kampagnen, damit Sie für jeden Marketing-Anwendungsfall in Adobe Journey Optimizer den richtigen Ansatz wählen können.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] bietet zwei Möglichkeiten, Ihre Kunden zu erreichen und zu kontaktieren: **Journey** und **Kampagnen**. Journey sind für eine mehrstufige Orchestrierung in Echtzeit konzipiert, die vom Kundenverhalten gesteuert wird, während Kampagnen sich besser für einmalige oder geplante Sendungen an eine definierte Zielgruppe eignen. Sobald Sie sich für eine Kampagne entschieden haben, können Sie den Kampagnentyp auswählen, der Ihrem Anwendungsfall am besten entspricht.

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
>**Schnelle Faustregel:** muss sich jeder Kunde in seinem eigenen Tempo mit Echtzeit-Logik bewegen? Verwenden Sie **Journey**. Eine Nachricht nach einem Zeitplan an eine Zielgruppe senden? Verwenden Sie **Aktionskampagnen**. Einzelne Nachricht von einem externen System über API auslösen? Verwenden Sie **API-ausgelöste Kampagnen** - oder eine **Unitäres Ereignis-Journey**, wenn Sie nach dem API-gesendeten Ereignis eine mehrstufige Orchestrierung benötigen. Benötigen Sie Daten mit mehreren Entitäten, exakte Zählungen oder eine Batch-Arbeitsfläche? Verwenden Sie **Orchestrierte Kampagnen**.

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

**Individuelle Reaktionen in Echtzeit auf das Kundenverhalten?**
→ **Journey verwenden**
* Profile müssen sich in ihrem eigenen Tempo bewegen
* Bedingte Logik basierend auf dem Verhalten
* Echtzeitkontext ist entscheidend

**Einfacher Nachrichtenversand an eine Zielgruppe zu einem geplanten Zeitpunkt?**
→ **Verwenden von**
* Alle Profile erhalten die Nachricht gleichzeitig
* Geplante oder wiederkehrende Sendungen
* Keine komplexe mehrstufige Logik erforderlich

**Sofortige Nachricht durch ein externes System ausgelöst?**
→ **API-ausgelöste Kampagnen verwenden** (eine Nachricht) **oder eine unitäre Ereignis-Journey** (mehrstufige Orchestrierung)
* Wird bei Bedarf über einen API-Aufruf ausgelöst: Kampagnen liefern eine Nachricht; unitäre Journey nehmen das Ereignis über eine [Experience Platform-Aufnahme auf ](../event/additional-steps-to-send-events-to-journey.md) führen einen vollständigen Journey-Fluss aus
* Payload-gesteuerte Personalisierung
* Auswählen von Kampagnen, wenn keine mehrstufige Logik erforderlich ist

**Komplexer Batch-Workflow mit erweiterter Segmentierung?**
→ **Verwenden von orchestrierten Kampagnen**
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
| API-ausgelöste Transaktionsnachricht (Einzelversand) | API-ausgelöste Kampagnen | Externer System-Trigger, sofortiger einmaliger Versand |
| API-ausgelöster mehrstufiger Fluss | Journey (Unitäres Ereignis) | Externes System sendet unitäres Ereignis über API; Journey koordiniert die Folgeschritte |
| Mehrstufiger Versand pro Buchung | Orchestrierte Kampagnen | Beziehungen mit mehreren Entitäten, eine Nachricht pro Buchung |

## Erläuterung der wichtigsten Unterschiede {#key-distinctions}

### Journeys: 1:1-Orchestrierung in Echtzeit

**Alleinstellungsmerkmal:**
* Jedes Profil behält seinen individuellen Status und Kontext bei
* Eintritt und Fortschritt jedes Profils im eigenen Tempo
* Entscheidungsfindung in Echtzeit basierend auf Verhalten und Ereignissen
* Warteaktivitäten erstellen eine personalisierte Zeitplanung
* Bedingte Verzweigungen erstellen eindeutige Pfade pro Profil
* Integriertes Aktiv-Listening - Inaktivität für einen definierten Zeitraum kann auch einen Trigger beim nächsten Schritt darstellen, nicht nur bei expliziten Ereignissen. [Erfahren Sie mehr über Warteaktivitäten](../building-journeys/wait-activity.md)
* Frequenzlimitierung : Legt fest, wie oft Kundinnen und Kunden Nachrichten von einer Journey eingeben oder empfangen können. [Erfahren Sie mehr über Journey-Begrenzung](../conflict-prioritization/journey-capping.md)
* Zielgruppenteilung nach Prozentsatz - Teilt Profile in zufällige, prozentualbasierte Gruppen auf, um A/B-Experimente über Journey-Pfade hinweg durchzuführen. [Erfahren Sie mehr über die prozentuale Aufspaltung](../building-journeys/condition-activity.md)
* Testmodus - Validieren der Journey-Logik und des Nachrichtenversands mit Testprofilen vor der Live-Veröffentlichung. [Erfahren Sie mehr über den Testmodus](../building-journeys/testing-the-journey.md)

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
* **Aktionskampagnen**: Geplanter Versand an Zielgruppen (einmalig oder wiederkehrend)
* **API-ausgelöste Kampagnen**: Versand auf Anfrage, ausgelöst durch einen API-Aufruf mit Payload-Daten

[Weitere Informationen zu Kampagnen](../campaigns/get-started-with-campaigns.md)

### Orchestrierte Kampagnen: Workflows für Batch-Arbeitsflächen

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

[Weitere Informationen zu orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)

## Beispiele für Anwendungsfälle {#use-cases}

### Anwendungsfälle für Journeys

* **Wiederherstellen abgebrochener Warenkörbe:** Ausgelöst beim Hinzufügen zum Warenkorb, Warten auf Checkout gewartet, Versand von Erinnerungen, wenn kein Kauf stattfindet
* **Kunden-Onboarding:** Mehrstufige Willkommensserie mit personalisierten Inhalten, die auf Profildaten basieren
* **Upgrade der Treuestufe:** Wird ausgelöst, wenn die Person eine neue Stufe erreicht, Versand von Glückwünschen und Vorteilen
* **Geburtstagskampagnen:** Eintritt basierend auf Geburtsdatum, personalisierte Angebote
* **Wiederaufnahme der Interaktion:**: Ausgelöst durch Zielgruppenqualifizierung (Inaktivität), progressive Kontaktaufnahme

### Anwendungsfälle für Kampagnen (Aktion und API-gesteuert)

**Aktionskampagnen:**
* **Monatliche Newsletter:** Geplanter Batch-Versand an das Abonnentensegment
* **Werbeankündigungen:** Zeitkritische Angebote für Zielgruppen
* **Produkteinführungen:** Koordinierte Ankündigung an alle Kundinnen und Kunden
* **Saisonale Grüße:** Feiertagsnachrichten zu bestimmten Terminen

**API-ausgelöste Kampagnen:**
* **Bestellbestätigungen:** Ausgelöst durch E-Commerce-System nach dem Kauf
* **Versandbenachrichtigungen:** Ausgelöst durch Logistiksystem
* **Kontowarnungen:** Ausgelöst durch ein System zur Betrugserkennung
* **Passwortzurücksetzung:** Ausgelöst durch Benutzeraktion in der Anwendung

### Anwendungsfälle für koordinierte Kampagnen

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
| LINE | ✅ | ✅ | ✅ | ✅ |
| WhatsApp | ✅ | ✅ | ✅ | ✅ |

### Erweiterte Funktionen

| Funktion | Journeys | Aktionskampagnen | Durch API ausgelöste Kampagnen | Orchestrierte Kampagnen |
|-----------|:--------:|:----------------:|:-----------------------:|:---------------------:|
| Mehrstufige Workflows | ✅ | ❌ | ❌ | ✅ |
| Echtzeit-Trigger | ✅ | ❌ | ✅ | ❌ |
| Warteaktivitäten | ✅ | ❌ | ❌ | ✅ |
| Bedingte Verzweigung | ✅ | ❌ | ❌ | ✅ |
| Geplante Ausführung | ✅ | ✅ | ✅ | ✅ |
| API-Auslösung | ✅ (Nur unitäres Ereignis - Ereignis, das über die API gesendet wird) | ❌ | ✅ | ❌ |
| Daten mit mehreren Entitäten | ❌ | ❌ | ❌ | ✅ |
| Genaue Anzahl vor dem Versand | ❌ | ❌ | ❌ | ✅ |
| On-Demand-Segmentierung | ❌ | ❌ | ❌ | ✅ |
| Versandzeitoptimierung | ✅ | ❌ | ❌ | ❌ |
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

Aktionskampagnen sind in der Regel die einfachste (eine Nachricht an die Zielgruppe), gefolgt von API-ausgelösten Kampagnen, Journey (komplexer mit Mehrstufenlogik) und orchestrierten Kampagnen (am komplexesten aufgrund der Workflow-Funktionen der Arbeitsfläche und der Funktionen für mehrere Entitäten).

+++

+++ Welcher Ansatz ist besser für große Zielgruppen geeignet?

Alle vier können gut skalieren. Die richtige Wahl hängt von Ihrem Muster ab:

* **Audience-Journey lesen** und **Action-** sind für große Batch-Zielgruppen optimiert (eine Nachricht oder Fluss zu mehreren Profilen gleichzeitig).
* **Orchestrierte Kampagnen** zeichnen sich durch eine komplexe Segmentierung mit großen Datensätzen und Daten mit mehreren Entitäten aus.
* **Unitäre (ereignisbasierte) Journey** verarbeiten Profile einzeln, wenn Ereignisse auftreten. Die Skalierung hängt daher vom Ereignisvolumen und -durchsatz ab.

+++

+++ Kann ich dieselbe Zielgruppe für Journeys und Kampagnen verwenden?

Ja. In [!DNL Adobe Experience Platform] erstellte Audiences können in Journey-, Aktions- und orchestrierten Kampagnen verwendet werden (wobei die Audience-Logik auch auf der Arbeitsfläche nach Bedarf erstellt werden kann). API-ausgelöste Kampagnen sind Payload-gesteuert und verwenden vordefinierte Zielgruppen nicht auf die gleiche Weise.

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
>* [Häufig gestellte Fragen zu orchestrierten Kampagnen](../orchestrated/orchestrated-campaigns-faq.md)
