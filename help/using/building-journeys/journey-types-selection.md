---
solution: Journey Optimizer
product: journey optimizer
title: Journey-Typen und Auswahlhilfe
description: Vergleichen Sie Journey-Typen und wählen Sie den richtigen für Ihren Anwendungsfall mit Entscheidungshandbüchern und einer Funktionskompatibilitätsmatrix aus
feature: Journeys, Get Started, Overview
role: User
level: Beginner
keywords: Journey-Typen, unitär, Zielgruppe lesen, Zielgruppen-Qualifizierung, Geschäftsereignis, Vergleich, Entscheidungshandbuch, Auswahl, Auswahl, in Echtzeit, geplant, Batch, ereignisausgelöst
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: f749eae4e0a826428880e913219cf6f5a135b17c
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 4%

---


# Journey-Typen und Auswahlhilfe {#journey-types-selection}

Adobe Journey Optimizer unterstützt vier Journey-Typen, die jeweils für unterschiedliche Einstiegsmechanismen und Geschäftsszenarien entwickelt wurden. Dieser Leitfaden hilft Ihnen, die Unterschiede zu verstehen und den richtigen Typ für Ihren Anwendungsfall auszuwählen.

## Übersicht über Journey-Typen {#journey-types}

>[!BEGINTABS]

>[!TAB Unitäre Journey]

**Verwendung:** Erlebnisse in Echtzeit, ausgelöst durch Ereignisse

**Unitäre Journey** werden einzeln ausgelöst, wenn eine bestimmte Aktion stattfindet (Kauf, App-Anmeldung, Formularübermittlung). Profile treten jeweils in Echtzeit einzeln ein, wodurch dies ideal für sofortige, verhaltensgesteuerte Antworten ist.

**Perfekt für:** Bestellbestätigungen nach dem Kauf, Willkommens-E-Mails, wenn sich jemand anmeldet, Warenkorbabbruch, der durch Browsen ausgelöst wird, und Benachrichtigungen zum Zurücksetzen des Kennworts.

➡️ [Informationen zu Ereignissen](../event/about-events.md) | [Anwendungsfall „Nachricht an Abonnenten“](message-to-subscribers-uc.md)

>[!TAB Audience-Journey lesen]

**Verwendung:** Geplante Kampagnen für Zielgruppensegmente

**Zielgruppen-Journey lesen** Beginnen Sie mit einer Adobe Experience Platform-Zielgruppe und senden Sie Nachrichten im Batch an alle Profile gleichzeitig. Dieser Journey-Typ eignet sich ideal für geplante Kommunikation in großem Maßstab.

**Perfekt für:** monatliche Newsletter, Werbekampagnen für bestimmte Segmente, Produktankündigungen und saisonale Marketing-Kampagnen.

➡️ [Erfahren Sie mehr über „Zielgruppe lesen“](read-audience.md) | [Erste Schritte mit Audiences](../audience/about-audiences.md)

>[!TAB Journey zur Zielgruppenqualifizierung]

**Verwendung:** Echtzeit-Reaktionen auf Änderungen der Zielgruppenzugehörigkeit

**Journey für die Zielgruppenqualifizierung** Trigger, wenn Profile für eine bestimmte Zielgruppe qualifiziert sind (oder diese verlassen haben). Profile treten einzeln ein, wenn sie die Kriterien in Echtzeit erfüllen, was eine sofortige Interaktion ermöglicht, wenn sich das Kundenverhalten ändert.

**Ideal für:** Benachrichtigungen zu VIP-Stufen-Upgrades, Rückgewinnung von Interaktionen, wenn Kunden inaktiv werden, Nachrichten zu ersten Kauffeiern und geografisches Targeting, wenn Kunden umziehen.

➡️ [Informationen zur Zielgruppen-Qualifizierung](audience-qualification-events.md) | [Erstellen von Zielgruppen](../audience/creating-a-segment-definition.md)

>[!TAB Journey für Geschäftsereignisse]

**Verwendung:** Geschäftsbedingungen, die mehrere Kunden betreffen

**Geschäftsereignis-Journey** werden durch Ereignisse auf Unternehmensebene ausgelöst (Stock-Updates, Wetterwarnungen, Preisänderungen), die mehrere Profile gleichzeitig betreffen. Sie sind nicht auf Einzelaktionen, sondern auf umfassendere Geschäftsbedingungen ausgerichtet.

**Perfekt für:** Warnungen bei geringem Bestand an interessierte Kunden, Flash-Verkaufsankündigungen, wetterbasierte Werbeaktionen, Benachrichtigungen zu Preisrückgängen und Warnhinweise für das Produkt-Back-in-Stock.

➡️ [Erfahren Sie mehr über Geschäftsereignisse](../event/about-creating-business.md) | [Zutrittsverwaltung](entry-management.md)

>[!ENDTABS]

## Entscheidungshandbuch: Auswahl des Journey-Typs {#decision-guide}

Folgen Sie diesem Entscheidungsbaum, um den richtigen Journey-Typ für Ihren Anwendungsfall auszuwählen:

### Schritt 1: Welche Trigger die Journey?

* **Kunde führt bestimmte Aktionen durch** (Kauf, Klick, Anmeldung) → Mit Schritt 2 fortfahren
* **Zeit/Zeitplan** (zu einem bestimmten Zeitpunkt oder wiederkehrend senden) → **Zielgruppen-Journey lesen**
* **Änderungen des Kundenstatus** (führt zu einem Segment bzw. verlässt es) → Mit Schritt 3 fortfahren
* **Geschäftsbedingung** (Lagerbestand, Preisänderung, Wetter) → **Geschäftsereignis-Journey verwenden**

### Schritt 2: Individuelle Customer Action-Trigger

* **Ist eine sofortige Reaktion in Echtzeit erforderlich?**
   * Ja → **Unitäres Journey verwenden**
   * Keine → Zielgruppen-Journey mit geplanter Ausführung lesen

### Schritt 3: Änderungen des Kundenstatus

* **Müssen Kunden beim Eintritt oder Austritt aus einem Segment reagieren?**
   * Ja → **Journey zur Zielgruppenqualifizierung verwenden**
   * Nein, nur bei der Eingabe → Einzelnes Journey mit Ereignis oder Zielgruppe lesen mit Zielgruppenfilter berücksichtigen

### Schnelle Auswahl nach Anwendungsfall

| Ihr Ziel | Empfohlener Journey-Typ | Warum |
|-----------|------------------------|-----|
| Bestellbestätigung nach Kauf senden | Unitär | Sofortige Reaktion auf einzelne Maßnahmen |
| Monatlichen Newsletter an Abonnenten senden | Zielgruppe lesen | Geplante Batch-Kommunikation |
| Kunden benachrichtigen, wenn sie den VIP-Status erreichen | Zielgruppen-Qualifizierung | Echtzeit-Reaktion auf Statusänderung |
| Kunden über niedrige Lagerbestände bei überwachten Elementen informieren | Geschäftsereignis | Geschäftsbedingung wirkt sich auf mehrere Kunden aus |
| Neue App-Benutzer begrüßen | Unitär | Ausgelöst durch Anmeldungsereignis |
| Erneute Interaktion mit inaktiven Kunden | Zielgruppen-Qualifizierung | Reagiert auf Inaktivitäts-Segmenteintrag |
| Saisonale Promotion zum Zielsegment | Zielgruppe lesen | Geplante Kampagne für Zielgruppe |
| Ankündigung von Blitzverkauf | Geschäftsereignis | Geschäftsentscheidungen wirken sich auf mehrere Kunden aus |

>[!NOTE]
>
>Nicht sicher, welcher Typ ausgewählt werden soll? Beginnen Sie mit **Unitäre Journey** für ereignisbasierte Erlebnisse oder **Audience-Journey lesen** für geplante Kampagnen. Diese decken die häufigsten Anwendungsfälle ab.

## Detailvergleich der Journey-Typen {#journey-types-comparison}

Verwenden Sie diese Tabelle, um Journey-Typen schnell zu vergleichen und den richtigen für Ihren Anwendungsfall auszuwählen:

| Aspekt | Einheitliche Journeys | Journey der Zielgruppe lesen | Journey zur Zielgruppenqualifizierung | Journey für Geschäftsereignisse |
|--------|------------------|------------------------|--------------------------------|------------------------|
| **Eingabemechanismus** | Trigger einzelner Ereignisse | Geplanter Batch | Änderung der Zielgruppenzugehörigkeit in Echtzeit | Ereignis auf Unternehmensebene |
| **Eintrittszeitpunkt** | Echtzeit, wenn Ereignisse eintreten | Geplant (einmalig oder wiederkehrend) | Echtzeit, sobald eine Qualifizierung stattfindet | Echtzeit, wenn ein Geschäftsereignis ausgelöst wird |
| **Profileintrag** | Eins nach dem anderen | Alle gleichzeitig (Batch) | Eins nach dem anderen | Mehrere Profile gleichzeitig |
| **Quelltext des Triggers** | Kundenaktion (Kauf, Klick, Anmeldung) | Zeitbasierter Zeitplan | Zielgruppenzugehörigkeit (Einstieg/Ausstieg) | Geschäftsbedingung (Lager, Wetter, Preis) |
| **Am besten geeignet für** | Transaktionsnachrichten, Verhaltensantworten | Marketing-Kampagnen, Newsletter | Treueprogramme, Lebenszyklusphasen | Inventar-Warnhinweise, Promotions, Geschäftsbedingungen |
| **Verwenden Sie wenn** | Sofortige Reaktion auf einzelne erforderliche Maßnahmen | Erreichen großer Zielgruppensegmente planmäßig | Auf Änderungen des Kundenstatus reagieren | Geschäftsereignisse wirken sich auf mehrere Kunden aus |
| **Beispiele** | Bestellbestätigung, Kennwortzurücksetzung | Monatlicher Newsletter, saisonale Kampagne | VIP-Upgrade, Inaktivitätswarnung | Geringer Lagervorrat, Flash-Verkauf, Preisverfall |
| **Erneuter Eintritt** | Konfigurierbar (mehrere Einträge pro Profil zulassen) | Jedes Profil tritt einmal pro Ausführung ein | Pro Qualifizierungsereignis konfigurierbar | Mehrere Profile können von demselben Ereignis betroffen sein |
| **Datenanforderungen** | Ereignisschema mit Trigger-Daten | Adobe Experience Platform-Zielgruppe | Streaming- oder Batch-Zielgruppe | Geschäftsereignis-Schema |

## Funktionskompatibilität nach Journey-Typ {#feature-compatibility}

Nicht alle Features sind für alle Journey-Typen verfügbar. Mithilfe dieser Matrix können Sie herausfinden, welche Funktionen mit welchen Journey-Typen funktionieren:

| Funktion | Unitär | Zielgruppe lesen | Zielgruppen-Qualifizierung | Geschäftsereignis |
|---------------------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Zugangsmechanismen** |
| Ereignisausgelöster Eintrag | ✅ | ❌ | ❌ | ✅ |
| Geplanter Eintrag | ❌ | ✅ | ❌ | ❌ |
| Zielgruppenbasierter Eintrag | ❌ | ✅ | ✅ | ❌ |
| **Orchestrierungsfunktionen** |
| Warteaktivitäten | ✅ | ✅ | ✅ | ✅ |
| Bedingungsaktivitäten | ✅ | ✅ | ✅ | ✅ |
| Benutzerdefinierte Aktionen | ✅ | ✅ | ✅ | ✅ |
| Aktivität „Zielgruppe lesen“ (innerhalb von Journey) | ✅ | ✅ | ✅ | ✅ |
| Aktivität zur Zielgruppenqualifizierung | ✅ | ✅ | ✅ | ✅ |
| Aktivität „Springen“ | ✅ | ✅ | ✅ | ✅ |
| **Profil-Management** |
| Erneuter Profileintritt | ✅ konfigurierbar | Einmal pro Ausführung ❌ | ✅ konfigurierbar | ✅ pro Ereignis |
| Namespace-Konfiguration | ✅ erforderlich | ✅ optional | ✅ erforderlich | ✅ erforderlich |
| Profilbegrenzung | ✅ | ✅ | ✅ | ✅ |
| **Tests und Optimierung** |
| Testmodus | ✅ | ✅ | ✅ | ✅ |
| Probelauf | ✅ | ✅ | ✅ | ✅ |
| Pfadexperimente (A/B-Tests) | ✅ | ✅ | ✅ | ❌ |
| Optimierung des Versandzeitpunkts | ✅ | ✅ | ✅ | ✅ |
| **Kanäle** |
| E-Mail | ✅ | ✅ | ✅ | ✅ |
| Push-Benachrichtigungen  | ✅ | ✅ | ✅ | ✅ |
| SMS/MMS | ✅ | ✅ | ✅ | ✅ |
| In-App-Nachrichten | ✅ | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ✅ | ✅ |
| Inhaltskarten | ✅ | ✅ | ✅ | ✅ |
| **Erweiterte Funktionen** |
| Inkrementelles Lesen | ❌ | ✅ | ❌ | ❌ |
| Zielgruppe exportieren | ✅ | ✅ | ✅ | ✅ |
| Zeitzonen-Management | ✅ | ✅ | ✅ | ✅ |
| Reaktionsereignisse | ✅ | ✅ | ✅ | ✅ |
| Externe Datenquellen | ✅ | ✅ | ✅ | ✅ |
| Drosselung/Begrenzung | ✅ | ✅ | ✅ | ✅ |

**Legende:** ✅ = Unterstützt | ❌ = Nicht unterstützt

## Nächste Schritte {#next-steps}

Nachdem Sie nun die Journey-Typen verstehen, können Sie:

* **[Erstellen der ersten Journey](journey-gs.md)** - Schrittweise Anleitung
* **[Erfahren Sie mehr über den Journey-Designer](using-the-journey-designer.md)** - Entwerfen Sie Ihre Journey-Arbeitsfläche
* **[Erkunden der Journey-Funktionen](journey.md#capabilities)** - Erfahren Sie mehr über erweiterte Funktionen
* **[Häufig gestellte Fragen zum Journey](journey-faq.md)** - Häufig gestellte Fragen beantwortet

**Müssen Sie mit Kampagnen vergleichen?**

* Vergleichshandbuch zu [Journey und Kampagnen](../start/journeys-vs-campaigns.md) - Wählen Sie zwischen Journey-, Aktions-/API-Kampagnen und orchestrierten Kampagnen

