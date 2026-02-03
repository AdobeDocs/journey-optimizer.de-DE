---
solution: Journey Optimizer
product: journey optimizer
title: Journey-Typen und Auswahlrichtlinien
description: Vergleichen Sie Journey-Typen und wählen Sie mithilfe von Entscheidungsanleitungen und einer Funktionskompatibilitätsmatrix den richtigen für Ihren Anwendungsfall aus
feature: Journeys, Get Started, Overview
role: User
level: Beginner
keywords: Journey-Typen, unitär, Zielgruppe lesen, Zielgruppenqualifizierung, Geschäftsereignis, Vergleich, Entscheidungsanleitungen, Auswahl, Auswahl, in Echtzeit, geplant, Batch, ereignisausgelöst
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: f749eae4e0a826428880e913219cf6f5a135b17c
workflow-type: ht
source-wordcount: '986'
ht-degree: 100%

---


# Journey-Typen und Auswahlrichtlinien {#journey-types-selection}

Adobe Journey Optimizer unterstützt vier Journey-Typen, die jeweils für unterschiedliche Eintrittsmechanismen und Geschäftsszenarien entwickelt wurden. Dieser Leitfaden hilft Ihnen, die Unterschiede zu verstehen und den richtigen Typ für Ihren Anwendungsfall auszuwählen.

## Journey-Typen – Überblick {#journey-types}

>[!BEGINTABS]

>[!TAB Unitäre Journeys]

**Verwendung:** In Echtzeit durch Ereignisse ausgelöste Erlebnisse

**Unitäre Journeys** werden individuell ausgelöst, wenn eine bestimmte Aktion stattfindet (Kauf, App-Anmeldung, Formularübermittlung). Profile treten jeweils in Echtzeit einzeln ein, wodurch dies ideal für unmittelbare, verhaltensgesteuerte Antworten ist.

**Perfekt für:** Bestellbestätigungen nach dem Kauf, Willkommens-E-Mails bei Anmeldungen, durch Browsen ausgelöste Warenkorbabbrüche und Benachrichtigungen zum Zurücksetzen des Passworts.

➡️ [Informationen zu Ereignissen](../event/about-events.md) | [Anwendungsfall „Nachricht an Abonnentinnen und Abonnenten“](message-to-subscribers-uc.md)

>[!TAB Journeys des Typs „Zielgruppe lesen“]

**Verwendung:** Geplante Kampagnen für Zielgruppensegmente

**Journeys des Typs „Zielgruppe lesen“** beginnen mit einer Adobe Experience Platform-Zielgruppe und senden Nachrichten in Batch-Vorgängen an alle Profile gleichzeitig. Dieser Journey-Typ eignet sich ideal für geplante Kommunikation in großem Umfang.

**Perfekt für:** Monatliche Newsletter, Werbekampagnen für bestimmte Segmente, Produktankündigungen und saisonale Marketing-Kampagnen.

➡️ [Informationen zu „Zielgruppe lesen“](read-audience.md) | [Erste Schritte mit Zielgruppen](../audience/about-audiences.md)

>[!TAB Journeys des Typs „Zielgruppenqualifizierung“]

**Verwendung:** Echtzeit-Reaktionen auf Änderungen der Zielgruppenzugehörigkeit

**Journeys des Typs „Zielgruppenqualifizierung“** werden ausgelöst, wenn Profile sich für ein bestimmtes Zielgruppensegment qualifizieren (oder daraus aussteigen). Profile treten einzeln ein, wenn sie die Kriterien in Echtzeit erfüllen, was eine sofortige Interaktion ermöglicht, wenn sich das Kundenverhalten ändert.

**Perfekt für:** Benachrichtigungen zu VIP-Stufen-Upgrades, Rückgewinnung von inaktiven Kundinnen und Kunden, Nachrichten aufgrund von Erstkäufen und geografisches Targeting, wenn Kundinnen und Kunden umziehen.

➡️ [Informationen zur Zielgruppenqualifizierung](audience-qualification-events.md) | [Erstellen von Zielgruppen](../audience/creating-a-segment-definition.md)

>[!TAB Journeys des Typs „Geschäftsereignis“]

**Verwendung:** Geschäftsbedingungen, die mehrere Kundinnen und Kunden betreffen

**Journeys des Typs „Geschäftsereignis“** werden durch Ereignisse auf Unternehmensebene ausgelöst (Updates zum Warenbestand, Wetterwarnungen, Preisänderungen), die mehrere Profile gleichzeitig betreffen. Sie sind nicht auf Einzelaktionen, sondern auf umfassendere Geschäftsbedingungen ausgerichtet.

**Perfekt für:** Warnungen an interessierte Kundinnen und Kunden bei geringem Bestand, Ankündigungen von Blitzverkäufen, wetterbasierte Promotionen, Benachrichtigungen zu Preissenkungen und Benachrichtigungen, wenn Produkte wieder auf Lager sind.

➡️ [Informationen zu Geschäftsereignissen](../event/about-creating-business.md) | [Eintrittsverwaltung](entry-management.md)

>[!ENDTABS]

## Entscheidungsanleitung: Auswahl des Journey-Typs {#decision-guide}

Folgen Sie diesem Entscheidungsbaum, um den richtigen Journey-Typ für Ihren Anwendungsfall auszuwählen:

### Schritt 1: Wodurch wird die Journey ausgelöst?

* **Kundin/Kunde führt bestimmte Aktion durch** (Kauf, Klick, Anmeldung) → Mit Schritt 2 fortfahren
* **Zeit/Zeitplan** (zu einem bestimmten Zeitpunkt oder wiederkehrend senden) → **Journey „Zielgruppe lesen“ verwenden**
* **Änderungen des Kundenstatus** (tritt in ein Segment ein bzw. verlässt es) → Mit Schritt 3 fortfahren
* **Geschäftsbedingung** (Lagerbestand, Preisänderung, Wetter) → **Journey „Geschäftsereignis“ verwenden**

### Schritt 2: Individuelle Kundenaktion wird ausgelöst

* **Ist eine sofortige Reaktion in Echtzeit erforderlich?**
   * Ja → **Unitäre Journey verwenden**
   * Nein → Journey „Zielgruppe lesen“ mit geplanter Ausführung erwägen

### Schritt 3: Kundenstatus ändert sich

* **Muss eine Reaktion erfolgen, wenn Kundinnen und Kunden in ein Segment eintreten ODER aus einem aussteigen?**
   * Ja → **Journey „Zielgruppenqualifizierung“ verwenden**
   * Nein, nur bei Eintritt → Unitäre Journey mit Ereignis oder „Zielgruppe lesen“ mit Zielgruppenfilter erwägen

### Schnellauswahl nach Anwendungsfall

| Ihr Ziel | Empfohlener Journey-Typ | Warum |
|-----------|------------------------|-----|
| Senden einer Bestellbestätigung nach Kauf | Unitär | Sofortige Reaktion auf einzelne Aktionen |
| Senden eines monatlichen Newsletters an Abonnentinnen und Abonnenten | Zielgruppe lesen | Geplante Batch-Kommunikation |
| Benachrichtigen von Kundinnen und Kunden, wenn sie VIP-Status erreichen | Zielgruppenqualifizierung | Echtzeit-Reaktion auf Statusänderung |
| Benachrichtigen von Kundinnen und Kunden über niedrige Lagerbestände beobachteter Artikel | Geschäftsereignis | Geschäftsbedingung wirkt sich auf mehrere Kundinnen und Kunden aus |
| Begrüßen neuer Benutzender der App | Unitär | Durch Anmeldungsereignis ausgelöst |
| Rückgewinnung inaktiver Kundinnen und Kunden | Zielgruppenqualifizierung | Reagiert auf Eintritt in Inaktivitätssegment |
| Saisonale Promotion für Zielsegment | Zielgruppe lesen | Geplante Kampagne für Zielgruppe |
| Ankündigung von Blitzverkauf | Geschäftsereignis | Geschäftsentscheidung wirkt sich auf mehrere Kundinnen und Kunden aus |

>[!NOTE]
>
>Sie sind nicht sicher, welchen Typ Sie auswählen sollen? Beginnen Sie mit **unitären Journeys** für ereignisbasierte Erlebnisse oder **Journeys des Typs „Zielgruppe lesen“** für geplante Kampagnen. Diese decken die häufigsten Anwendungsfälle ab.

## Detailvergleich der Journey-Typen {#journey-types-comparison}

Verwenden Sie diese Tabelle, um Journey-Typen schnell zu vergleichen und den richtigen für Ihren Anwendungsfall auszuwählen:

| Aspekt | Unitäre Journeys | Journeys des Typs „Zielgruppe lesen“ | Journeys des Typs „Zielgruppenqualifizierung“ | Journeys des Typs „Geschäftsereignis“ |
|--------|------------------|------------------------|--------------------------------|------------------------|
| **Eintrittsmechanismus** | Individuelles Ereignis als Trigger | Geplanter Batch | Änderung der Zielgruppenzugehörigkeit in Echtzeit | Ereignis auf Unternehmensebene |
| **Eintrittszeitpunkt** | Echtzeit, sobald Ereignisse eintreten | Geplant (einmalig oder wiederkehrend) | Echtzeit, sobald eine Qualifizierung stattfindet | Echtzeit, sobald ein Geschäftsereignis ausgelöst wird |
| **Profileintritt** | Eins nach dem anderen | Alle gleichzeitig (Batch) | Eins nach dem anderen | Mehrere Profile gleichzeitig |
| **Quelle des Triggers** | Kundenaktion (Kauf, Klick, Anmeldung) | Zeitbasierter Plan | Zielgruppenzugehörigkeit (Eintritt/Ausstieg) | Geschäftsbedingung (Bestand, Wetter, Preis) |
| **Geeignet für** | Transaktionsnachrichten, Verhaltensreaktionen | Marketing-Kampagnen, Newsletter | Treueprogramme, Lebenszyklusphasen | Bestandsbenachrichtigungen, Promotions, Geschäftsbedingungen |
| **Verwendung** | Sofortige Reaktion auf einzelne Aktionen sind erforderlich | Große Zielgruppensegmente sollen planmäßig angesprochen werden | Reaktionen auf Änderungen des Kundenstatus sollen erfolgen | Geschäftsereignisse wirken sich auf mehrere Kundinnen und Kunden aus |
| **Beispiele** | Bestellbestätigung, Passwortzurücksetzung | Monatlicher Newsletter, saisonale Kampagne | VIP-Upgrade, Inaktivitätswarnung | Geringer Lagerbestand, Blitzverkauf, Preissenkung |
| **Erneuter Eintritt** | Konfigurierbar (mehrere Eintritte pro Profil zulassen) | Jedes Profil tritt einmal pro Ausführung ein | Konfigurierbar pro Qualifizierungsereignis | Mehrere Profile können von demselben Ereignis betroffen sein |
| **Datenanforderungen** | Ereignisschema mit Trigger-Daten | Adobe Experience Platform-Zielgruppe | Streaming- oder Batch-Zielgruppe | Geschäftsereignisschema |

## Funktionskompatibilität nach Journey-Typ {#feature-compatibility}

Nicht alle Funktionen sind für alle Journey-Typen verfügbar. Mithilfe dieser Matrix können Sie herausfinden, welche Funktionen mit welchen Journey-Typen funktionieren:

| Funktion | Unitär | Zielgruppe lesen | Zielgruppenqualifizierung | Geschäftsereignis |
|---------------------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Eintrittsmechanismen** |
| Durch Ereignis ausgelöster Eintritt | ✅ | ❌ | ❌ | ✅ |
| Geplanter Eintritt | ❌ | ✅ | ❌ | ❌ |
| Zielgruppenbasierter Eintritt | ❌ | ✅ | ✅ | ❌ |
| **Orchestrierungsfunktionen** |
| Warteaktivitäten | ✅ | ✅ | ✅ | ✅ |
| Bedingungsaktivitäten | ✅ | ✅ | ✅ | ✅ |
| Benutzerdefinierte Aktionen | ✅ | ✅ | ✅ | ✅ |
| Aktivität „Zielgruppe lesen“ (innerhalb von Journey) | ✅ | ✅ | ✅ | ✅ |
| Aktivität des Typs „Zielgruppenqualifizierung“ | ✅ | ✅ | ✅ | ✅ |
| Aktivität „Springen“ | ✅ | ✅ | ✅ | ✅ |
| **Profil-Management** |
| Erneuter Profileintritt | ✅ Konfigurierbar | ❌ Einmal pro Ausführung | ✅ Konfigurierbar | ✅ Pro Ereignis |
| Namespace-Konfiguration | ✅ Erforderlich | ✅ Optional | ✅ Erforderlich | ✅ Erforderlich |
| Profilbegrenzung | ✅ | ✅ | ✅ | ✅ |
| **Tests und Optimierung** |
| Testmodus | ✅ | ✅ | ✅ | ✅ |
| Probelauf | ✅ | ✅ | ✅ | ✅ |
| Pfadexperimente (A/B-Tests) | ✅ | ✅ | ✅ | ❌ |
| Versandzeitoptimierung | ✅ | ✅ | ✅ | ✅ |
| **Kanäle** |
| E-Mail | ✅ | ✅ | ✅ | ✅ |
| Push-Benachrichtigungen  | ✅ | ✅ | ✅ | ✅ |
| SMS/MMS | ✅ | ✅ | ✅ | ✅ |
| In-App-Nachrichten | ✅ | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ✅ | ✅ |
| Inhaltskarten | ✅ | ✅ | ✅ | ✅ |
| **Erweiterte Funktionen** |
| Inkrementelles Lesen | ❌ | ✅ | ❌ | ❌ |
| Exportieren der Zielgruppe | ✅ | ✅ | ✅ | ✅ |
| Zeitzonen-Management | ✅ | ✅ | ✅ | ✅ |
| Reaktionsereignisse | ✅ | ✅ | ✅ | ✅ |
| Externe Datenquellen | ✅ | ✅ | ✅ | ✅ |
| Drosselung/Begrenzung | ✅ | ✅ | ✅ | ✅ |

**Legende:** ✅ = Unterstützt | ❌ = Nicht unterstützt

## Nächste Schritte {#next-steps}

Nachdem Sie nun die Journey-Typen verstehen, können Sie Folgendes tun:

* **[Erstellen Ihrer ersten Journey](journey-gs.md)**: Schrittweise Anleitung
* **[Weitere Informationen über den Journey-Designer](using-the-journey-designer.md)**: Entwerfen Ihrer Journey-Arbeitsfläche
* **[Erkunden der Journey-Funktionen](journey.md#capabilities)**: Entdecken der erweiterten Funktionen
* **[Anzeigen häufig gestellter Fragen zu Journeys](journey-faq.md)**: Antworten auf häufig gestellte Fragen

**Müssen Sie Journeys mit Kampagnen vergleichen?**

* [Anleitung zum Vergleich zwischen Journeys und Kampagnen](../start/journeys-vs-campaigns.md): Wählen zwischen Journey-, Aktions-/API-Kampagnen und orchestrierten Kampagnen

