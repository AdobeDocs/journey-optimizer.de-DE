---
solution: Journey Optimizer
product: journey optimizer
title: Journeys oder Kampagnen – Auswählen des richtigen Ansatzes
description: Vergleichen Sie Journey, Aktionskampagnen und API-ausgelöste Kampagnen, um den richtigen Ansatz für Ihre Marketing-Anforderungen in Adobe Journey Optimizer zu wählen.
feature: Journeys, Campaigns, Get Started, Overview
topic: Content Management
role: User
level: Beginner
keywords: Journey, Kampagne, Vergleich, Auswählen, Entscheidung, Workflow, Echtzeit, Batch, Orchestrierung, mehrstufig, geplant, API-ausgelöst, ereignisgesteuert
hide: true
exl-id: 8b4d010e-4278-49fd-a7d3-dcc706829577
TQID: https://experienceleague.adobe.com/RWLVSULVO0idnCs5OVQR1yVvNv1G0JwP3y-3sNXQg50
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: addf009e-030a-4310-8534-776a3e62ed48id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 1660
ht-degree: 43%

---

# Journey vs. Kampagnen: Wählen Sie den richtigen Ansatz {#journeys-vs-campaigns}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Vergleichen Sie Journey mit Aktionen und API-ausgelösten Kampagnen, damit Sie für jeden Marketing-Anwendungsfall in Adobe Journey Optimizer den richtigen Ansatz wählen können. Informationen zu orchestrierten Kampagnen finden Sie [Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md).

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] bietet zwei Möglichkeiten, Ihre Kunden zu erreichen und zu kontaktieren: **Journey** und **Kampagnen**. Journey sind für eine mehrstufige Orchestrierung in Echtzeit konzipiert, die vom Kundenverhalten gesteuert wird, während Kampagnen sich besser für einmalige oder geplante Sendungen an eine definierte Zielgruppe eignen. Sobald Sie sich für eine Kampagne entschieden haben, können Sie den Kampagnentyp auswählen, der Ihrem Anwendungsfall am besten entspricht.

Dieses Handbuch hilft Ihnen bei der Auswahl zwischen Journey, Aktionskampagnen und API-ausgelösten Kampagnen basierend auf dem Ausführungsstil, den Datenanforderungen und dem Anwendungsfall - mit einem schnellen Vergleich, einem Entscheidungsbaum und konkreten Beispielen.

>[!NOTE]
>
>**Orchestrierte Kampagnen** weisen unterschiedliche architektonische Merkmale auf (Hub-seitige Batch-Ausführung, relationale Daten mit mehreren Entitäten), die eine dedizierte Anleitung erfordern. Sie sind nicht in den folgenden Vergleichstabellen enthalten, um eine übermäßige Vereinfachung zu vermeiden. [Erfahren Sie mehr über orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)

## Schnellvergleich – Überblick {#quick-overview}

| Ansatz | Geeignet für | Ausführungsstil |
|----------|----------|-----------------|
| **Journeys** | Mehrstufige Echtzeit-Kundenerlebnisse mit bedingter Logik | 1:1-Orchestrierung – jedes Profil im eigenen Tempo |
| **Aktionskampagnen** | Geplante oder wiederkehrende Sendungen an Zielgruppen | Batch-Ausführung - Zielgruppe zum Versandzeitpunkt gemeinsam verarbeitet |
| **API-ausgelöste Kampagnen** | Ereignisgesteuerte oder Transaktionsnachrichten von externen Systemen | Ausführung auf Anfrage - ausgelöst durch API-Aufruf mit Payload |

>[!TIP]
>
>**Schnelle Faustregel:** muss sich jeder Kunde in seinem eigenen Tempo mit Echtzeit-Logik bewegen? Verwenden Sie **Journey**. Eine Nachricht nach einem Zeitplan an eine Zielgruppe senden? Verwenden Sie **Aktionskampagnen**. Einzelne Nachricht von einem externen System über API auslösen? Verwenden Sie **API-ausgelöste Kampagnen** - oder eine **Unitäres Ereignis-Journey**, wenn Sie nach dem API-gesendeten Ereignis eine mehrstufige Orchestrierung benötigen.

## Detaillierter Vergleich {#detailed-comparison}

Verwenden Sie diese umfassende Tabelle, um die wichtigsten Unterschiede zu verstehen:

| Funktion | Journeys | Aktionskampagnen | Durch API ausgelöste Kampagnen |
|---------|----------|------------------|------------------------|
| **Primärer Zweck** | Mehrstufige 1:1-Orchestrierung mit Echtzeit-Kundenkontext | Einmaliger oder wiederkehrender Nachrichtenversand an Zielgruppen | Transaktions- oder ereignisgesteuerte Nachrichten, die von externen Systemen initiiert werden |
| **Typ der Arbeitsfläche** | 1:1-Arbeitsfläche – jedes Profil bewegt sich im eigenen Tempo | Keine Arbeitsfläche – Ausführung einer einzelnen Aktion | Keine Arbeitsfläche – Ausführung einer einzelnen Aktion |
| **Ausführungsfluss** | Sequenzielle Aktionen, Profilstatus wird während der Journey beibehalten | Simultane Ausführung für die gesamte Zielgruppe | Sofortige Ausführung pro API-Aufruf |
| **Eintrittsmechanismus** | Veranstaltungen, Zielgruppen, Qualifizierungen, Geschäftsereignisse | Manuelle Aktivierung und Planung | API-Aufruf aus externem System |
| **Datenmodell** | Echtzeitprofil und Ereignisdaten | Profildaten aus Experience Platform-Zielgruppen | API-Payload-Daten mit optionaler Profilsuche |
| **Segmentierung** | Vorkonfigurierte Zielgruppen und Echtzeitbedingungen | Vorkonfigurierte Zielgruppen aus Experience Platform | Payload-gesteuertes Targeting (keine geplante Zielgruppe) |
| **Profilverarbeitung** | Individuell, in Echtzeit (wenn Ereignisse auftreten) | Batch, alle auf einmal | Per API-Aufruf, Payload-gesteuert |
| **Personalisierung** | Echtzeit-Kontextdaten und Profilattribute | Profilattribute | Payload-Daten + optionale Profilattribute |
| **Komplexität** | Mehrstufig mit Verzweigung, Wartezeiten, Bedingungen | Einzelne Aktion oder einfacher Workflow | Einzelne Aktion mit Payload-Zuordnung |
| **Geeignet für** | Kundenzyklus-Journeys, Onboarding, Warenkorbabbruch | Werbekampagnen, Newsletter, Ankündigungen | Bestellbestätigungen, Versandwarnungen, Zurücksetzen des Kennworts |
| **Timing** | Fortlaufend, ab Veröffentlichung immer aktiv | Geplante Start-/Enddaten | On-Demand, ereignisgesteuert über API |
| **Status-Management** | Behält den Kundenstatus für Echtzeit-Aktionen bei | Statuslose Ausführung | Staatenlose Ausführung pro Aufruf |
| **Verwendung** | Mehrere Touchpoints mit Entscheidungslogik in Echtzeit erforderlich | Einfache Nachricht an eine Audience zu einem bestimmten Zeitpunkt | Das externe System muss sofort einen Trigger für eine Nachricht erstellen |
| **Individuelle Funktionen** | Echtzeit-Reaktionen, Warteaktivitäten, profilbasierte Geschwindigkeit | Planung, Zielgruppen-Targeting, Ratensteuerung | API-Payload-Zuordnung, System-zu-System-Triggerung |

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

**Komplexer Batch-Workflow mit erweiterter Segmentierung, Daten aus mehreren Entitäten oder exakten Zählungen vor dem Versand?**
→ **Verwenden orchestrierter Kampagnen** - siehe [Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md) für eine ausführliche Anleitung.

### Schritt 2: Prüfen Sie Ihre Auswahl

| Ihre Anforderungen | Empfohlener Ansatz | Warum |
|-----------|---------------------|-----|
| Neue Kundschaft mit mehrstufigem Onboarding begrüßen | Journeys | Eintritt in Echtzeit, mehrere Touchpoints, bedingte Pfade |
| Senden eines monatlichen Newsletters an Abonnentinnen und Abonnenten | Aktionskampagnen | Einfache geplante Nachricht an Zielgruppe |
| Warenkorbabbruch mit Erinnerungssequenz | Journeys | Echtzeit-Trigger, Wartezeiten, bedingte Nachverfolgung |
| Werbeankündigung an alle Kundinnen und Kunden | Aktionskampagnen | Einmalige Nachricht, sofortiger Versand |
| Erneutes Ansprechen inaktiver Benutzender auf Grundlage des Verhaltens | Journeys | Ausgelöst durch Zielgruppenqualifizierung, personalisierter Pfad |
| Blitzverkauf ausgelöst durch Geschäftsereignis | Journeys (Geschäftsereignis) | Echtzeit-Trigger mit Auswirkung auf mehrere Kundinnen und Kunden |
| API-ausgelöste Transaktionsnachricht (Einzelversand) | API-ausgelöste Kampagnen | Externer System-Trigger, sofortiger einmaliger Versand |
| API-ausgelöster mehrstufiger Fluss | Journey (Unitäres Ereignis) | Externes System sendet unitäres Ereignis über API; Journey koordiniert die Folgeschritte |
| Komplexer Batch-Workflow mit Daten aus mehreren Entitäten | Orchestrierte Kampagnen | Siehe [Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md) |

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

## Funktionsverfügbarkeit {#feature-availability}

### Kanäle

| Kanal | Journeys | Aktionskampagnen | Durch API ausgelöste Kampagnen |
|---------|:--------:|:----------------:|:-----------------------:|
| E-Mail | ✅ | ✅ | ✅ |
| Push-Benachrichtigung | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ |
| In-App | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ❌ |
| Code-basiert | ✅ | ✅ | ❌ |
| Inhaltskarten | ✅ | ✅ | ❌ |
| Direkt-Mail | ✅ | ✅ | ❌ |
| LINE | ✅ | ✅ | ✅ |
| WhatsApp | ✅ | ✅ | ✅ |

>[!NOTE]
>
>Informationen zur Verfügbarkeit von Kanälen für orchestrierte Kampagnen finden Sie [Orchestrierte Kampagnen - Unterstützte Kanäle](../orchestrated/gs-orchestrated-campaigns.md).

### Erweiterte Funktionen

| Funktion | Journeys | Aktionskampagnen | Durch API ausgelöste Kampagnen |
|-----------|:--------:|:----------------:|:-----------------------:|
| Mehrstufige Workflows | ✅ | ❌ | ❌ |
| Echtzeit-Trigger | ✅ | ❌ | ✅ |
| Warteaktivitäten | ✅ | ❌ | ❌ |
| Bedingte Verzweigung | ✅ | ❌ | ❌ |
| Geplante Ausführung | ✅ | ✅ | ✅ |
| API-Auslösung | ✅ (Nur unitäres Ereignis - Ereignis, das über die API gesendet wird) | ❌ | ✅ |
| Daten mit mehreren Entitäten | ❌ | ❌ | ❌ |
| Genaue Anzahl vor dem Versand | ❌ | ❌ | ❌ |
| On-Demand-Segmentierung | ❌ | ❌ | ❌ |
| Versandzeitoptimierung | ✅ | ❌ | ❌ |
| A/B-Tests | ✅ | ✅ | ❌ |
| Genehmigungs-Workflows | ✅ | ✅ | ✅ |

>[!NOTE]
>
>Details zu den Funktionen koordinierter Kampagnen - einschließlich Inhaltsexperimenten, Batch-API-Triggern und Segmentierung mehrerer Entitäten - finden Sie unter [Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md).

## Häufige Fragen {#common-questions}

+++ Kann ich Journeys und Kampagnen in meiner Marketing-Strategie kombinieren?

Ja. Viele Unternehmen verwenden alle Ansätze für verschiedene Szenarien:

* **Journey** für verhaltensbezogene Interaktion in Echtzeit
* **Aktionskampagnen** für geplante Broadcast-Nachrichten
* **API-ausgelöste**) für Transaktionsnachrichten
* **Orchestrierte Kampagnen** für komplexe, datenintensive Batch-Kampagnen - siehe [Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)

Verwenden Sie für jeden Anwendungsfall das richtige Tool, anstatt für alles einen Ansatz zu erzwingen.

+++

+++ Kann ich eine Kampagne in eine Journey konvertieren oder umgekehrt?

Nein, Sie müssen das Erlebnis im entsprechenden Format neu erstellen. Sie können jedoch Inhalte, Zielgruppen und Logikkonzepte wiederverwenden.

+++

+++ Welcher Ansatz ist einfacher zu erstellen?

Aktionskampagnen sind in der Regel die einfachste (eine Nachricht an die Zielgruppe), gefolgt von API-ausgelösten Kampagnen, dann Journey (komplexer mit Mehrstufenlogik).

+++

+++ Welcher Ansatz ist besser für große Zielgruppen geeignet?

Alle drei können gut skaliert werden. Die richtige Wahl hängt von Ihrem Muster ab:

* **Audience-Journey lesen** und **Action-** sind für große Batch-Zielgruppen optimiert (eine Nachricht oder Fluss zu mehreren Profilen gleichzeitig).
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
