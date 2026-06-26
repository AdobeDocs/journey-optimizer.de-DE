---
solution: Journey Optimizer
product: journey optimizer
title: 'Journey-Typen: Wählen Sie den richtigen aus'
description: Vergleichen Sie Journey-Typen und wählen Sie mithilfe von Entscheidungsanleitungen und einer Funktionskompatibilitätsmatrix den richtigen für Ihren Anwendungsfall aus
feature: Journeys, Get Started, Overview
role: User
level: Beginner
keywords: Journey-Typen, unitär, Zielgruppe lesen, Zielgruppenqualifizierung, Geschäftsereignis, Vergleich, Entscheidungsanleitungen, Auswahl, Auswahl, in Echtzeit, geplant, Batch, ereignisausgelöst
version: Journey Orchestration
source-git-commit: d4ed86ea2833c1753d89186a460ba24ae57773fd
workflow-type: tm+mt
source-wordcount: '2109'
ht-degree: 10%

---


# Journey-Typen: Wählen Sie den richtigen aus {#journey-types-selection}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie mehr über die vier AJO-Journey-Typen - Unitäres Ereignis, Lesen von Zielgruppen, Zielgruppen-Qualifizierung und Geschäftsereignis - und finden Sie heraus, welcher für Ihren Anwendungsfall geeignet ist.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] unterstützt vier Journey-Typen, die jeweils für eine andere Art von Trigger- und Geschäftsszenario entwickelt wurden. Wenn Sie den Unterschied verstehen, können Sie von Anfang an das richtige Erlebnis schaffen.

## Die vier Journey-Typen {#journey-types}

>[!BEGINTABS]

>[!TAB Journey für unitäre Ereignisse]

**Verwendung:** In Echtzeit durch Ereignisse ausgelöste Erlebnisse

**Unitäre Ereignis-Journey** werden einzeln ausgelöst, wenn eine bestimmte Aktion auftritt (Kauf, App-Anmeldung, Formularübermittlung). Die Profile treten jeweils in Echtzeit einzeln ein, was dies ideal für sofortige, verhaltensgesteuerte Antworten macht.

**Perfekt für:** Wiederherstellung bei Warenkorbabbruch, Onboarding von neuen Mitgliedern, Willkommens-E-Mails, wenn sich jemand anmeldet, und Personalisierung nach der Anmeldung.

➡️ [Informationen zu Ereignissen](../event/about-events.md) | [Anwendungsfall „Nachricht an Abonnenten“](message-to-subscribers-uc.md) | [Erstellen Sie Ihre erste Journey](journey-gs.md)

>[!TAB Journeys des Typs „Zielgruppe lesen“]

**Verwendung:** Geplante Kampagnen für Zielgruppensegmente

**Audience-Journey lesen** Beginnen Sie mit einer [!DNL Adobe Experience Platform] Audience und senden Sie Nachrichten im Batch an alle Profile gleichzeitig. Dieser Journey-Typ eignet sich ideal für geplante Kommunikation in großem Umfang. Verwenden Sie die Option **Inkrementelles Lesen** für wiederkehrende Journeys, um nur die Profile zu verarbeiten, die seit der letzten Ausführung der Zielgruppe beigetreten sind, anstatt jedes Mal die gesamte Zielgruppe erneut zu verarbeiten.

**Perfekt für:** monatliche Newsletter, Werbekampagnen für bestimmte Segmente, Produktankündigungen, wiederkehrende Interaktionsreihen und saisonale Marketing-Kampagnen.

➡️ [Erfahren Sie mehr über „Zielgruppe lesen](read-audience.md) | [Erste Schritte mit Zielgruppen](../audience/about-audiences.md) | [Erstellen Sie Ihre erste Journey](journey-gs.md)

>[!TAB Journeys des Typs „Zielgruppenqualifizierung“]

**Verwendung:** Echtzeit-Reaktionen auf Änderungen der Zielgruppenzugehörigkeit

**Journeys des Typs „Zielgruppenqualifizierung“** werden ausgelöst, wenn Profile sich für ein bestimmtes Zielgruppensegment qualifizieren (oder daraus aussteigen). Profile treten einzeln ein, wenn sie die Kriterien erfüllen, was eine sofortige Interaktion ermöglicht, wenn sich das Kundenverhalten ändert. Verwenden Sie **Streaming-ausgewertete** Zielgruppen - dies sind die einzigen unterstützten Zielgruppentypen für diese Aktivität.

>[!CAUTION]
>
>Ab **. August** können Journey, die eine Batch-Zielgruppe in einem Zielgruppen-Qualifizierungsknoten verwenden, nicht mehr veröffentlicht werden. [Erfahren Sie, wie Sie Ihre Journey migrieren](aq-batch-audiences-migration.md)

**Perfekt für:** Benachrichtigungen zu Upgrades der VIP-Stufe, Meldungen zu ersten Kauffeiern, Warnhinweise zu Abwanderungsrisiken und Übergänge in der Treueprogramm-Phase.

➡️ [Erfahren Sie mehr über Zielgruppen-](audience-qualification-events.md) | [Erstellen von Zielgruppen](../audience/creating-a-segment-definition.md) | [Erstellen Sie Ihre erste Journey](journey-gs.md)

>[!TAB Journeys des Typs „Geschäftsereignis“]

**Verwendung:** Geschäftsbedingungen, die mehrere Kundinnen und Kunden betreffen

**Geschäftsereignis-Journey** werden durch ein Geschäftsereignis (Stock-Updates, Preisänderungen) ausgelöst, das mehrere Profile gleichzeitig betrifft. Intern folgt auf den Geschäftsereignis-Trigger immer der Schritt „Zielgruppe lesen“, der die relevanten Profile aufnimmt. Daher folgt der Profileintrag den Regeln des Zielgruppen-Durchsatzes lesen und nicht dem Durchsatz von unitären Ereignissen.

**Perfekt für:** Warnungen bei geringem Bestand an interessierte Kunden, Flash-Verkaufsankündigungen, Benachrichtigungen bei Preisrückgängen und Warnhinweise für das Produkt-Back-in-Stock.

➡️ [Erfahren Sie mehr über Geschäftsereignisse](../event/about-creating-business.md) | [Einstiegsverwaltung](entry-management.md) | [Erstellen Sie Ihre erste Journey](journey-gs.md)

>[!ENDTABS]

## Welchen Typ sollten Sie verwenden? {#decision-guide}

Die Antwort läuft gewöhnlich auf eine Frage hinaus: *Was startet die Journey?*

Wenn **Kunde etwas Bestimmtes tut** — den Warenkorb verlässt, sich anmeldet, einen Kauf tätigt — verwenden Sie eine **Unitäre Ereignis-Journey**. Er wird sofort ausgelöst, wenn die Aktion stattfindet, ein Profil nach dem anderen.

Wenn Sie **eine Zielgruppe nach einem Zeitplan erreichen möchten** - einen monatlichen Newsletter, eine saisonale Kampagne, eine wiederkehrende Rückgewinnungsserie -, verwenden Sie eine **Zielgruppen-Journey lesen**. Sie definieren die Zielgruppe und das Timing; AJO verarbeitet alle gleichzeitig.

Wenn Sie reagieren möchten **sobald ein Kunde einen Meilenstein erreicht** — indem Sie einer Treuestufe beitreten, einen Schwellenwert für das Abwanderungsrisiko erreichen, einen ersten Kauf abschließen —, verwenden Sie eine **Zielgruppen-Qualifizierungs-Journey**. Er Trigger, sobald sich die Zugehörigkeit zur Streaming-Zielgruppe ändert, nicht nach einem festen Zeitplan.

Wenn sich etwas **in Ihrem Unternehmen** das mehrere Kunden gleichzeitig betrifft - ein Lagerbestand fällt, ein Preis ändert, ein Verkauf beginnt - verwenden Sie eine **Geschäftsereignis-Journey**.

>[!TIP]
>
>**Sie sind sich nicht sicher, wo Sie anfangen sollen?** Die meisten Teams beginnen mit **Unitäres Ereignis** für verhaltensgesteuerte Erlebnisse und **Zielgruppe lesen** für Kampagnen. Diese beiden decken den Großteil der Anwendungsfälle ab.

| Ihr Ziel | Empfohlener Journey-Typ | Warum |
|-----------|--------------------------|-----|
| Wiederherstellen eines Transaktionsabbruchs | Unitäres Ereignis | Sofortige Reaktion auf individuelles Verhalten |
| Senden eines monatlichen Newsletters an Abonnentinnen und Abonnenten | Zielgruppe lesen | Geplante Batch-Kommunikation |
| Benachrichtigen von Kundinnen und Kunden, wenn sie VIP-Status erreichen | Zielgruppenqualifizierung | Echtzeit-Antwort auf den Eintrag in die Streaming-Zielgruppe |
| Benachrichtigen von Kundinnen und Kunden über niedrige Lagerbestände beobachteter Artikel | Geschäftsereignis | Geschäftsbedingung wirkt sich auf mehrere Kundinnen und Kunden aus |
| Begrüßen neuer Benutzender der App | Unitäres Ereignis oder Zielgruppen-Qualifizierung | Anmeldungsereignis (unitäres Ereignis) oder Eintritt in eine Streaming-Zielgruppe für neue Benutzer (Zielgruppen-Qualifizierung) |
| Erneute Interaktion mit inaktiven Kunden (wiederkehrend, geplant) | Zielgruppe lesen | Wiederkehrende Batch-Ausführung für Inaktivitätszielgruppe |
| Saisonale Promotion für Zielsegment | Zielgruppe lesen | Geplante Kampagne für Zielgruppe |
| Ankündigung von Blitzverkauf | Geschäftsereignis | Geschäftsentscheidung wirkt sich auf mehrere Kundinnen und Kunden aus |
| Reagieren, sobald ein Kunde die Gold-Treuestufe erreicht | Zielgruppenqualifizierung | Streaming-Zielgruppe, individueller Echtzeit-Eintrag |

## Referenz zur Funktionsverfügbarkeit {#feature-compatibility}

Alle Journey-Typen unterstützen den vollständigen AJO-Kanalsatz (E-Mail, Push, SMS, In-App, Web, Inhaltskarten), Kernorchestrierungsaktivitäten (Warten, Bedingung, benutzerdefinierte Aktionen), den Testmodus, den Probelauf und die Sendezeitoptimierung. Die nachstehende Tabelle zeigt nur die Funktionen, die sich je nach Typ unterscheiden.

>[!NOTE]
>
>Einschränkungen bei Sprungaktivitäten: Eine Journey, die mit der Aktivität „Zielgruppe lesen“ oder „Zielgruppen-Qualifizierung“ beginnt, kann keine Sprungaktivität enthalten und auch nicht das Ziel einer Sprungaktivität von einer anderen Journey sein.
>
>Die Aktivität „Zielgruppe lesen“ als Journey-Eintrag ist nur in den Journey **Zielgruppe lesen** und **Geschäftsereignis** verfügbar und kann nicht zu den Journey für Unitäres Ereignis oder Zielgruppen-Qualifizierungseintrag hinzugefügt werden.

| Funktion | Unitäres Ereignis | Zielgruppe lesen | Zielgruppenqualifizierung | Geschäftsereignis |
|-----------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Eintritt** | | | | |
| Durch Ereignis ausgelöster Eintritt | ✅ | ❌ | ❌ | ✅ (Geschäftsereignis-Trigger auf der Journey; Profileingabe über einen internen Schritt „Zielgruppe lesen„) |
| Geplanter Eintritt | ❌ | ✅ | ❌ | ❌ |
| Zielgruppenbasierter Eintritt | ❌ | ✅ (Stapel) | ✅ (nur Streaming) | ❌ |
| **Orchestrierung** | | | | |
| Aktivität „Zielgruppe lesen“ (Journey-Eintrag) | ❌ | ✅ | ❌ | ✅ (automatischer Schritt nach dem Geschäftsereignis) |
| Aktivität „Springen“ | ✅ | ❌ | ❌ | ✅ |
| **Profil-Management** | | | | |
| Erneuter Profileintritt | ✅ Konfigurierbar | Standardmäßig einmal pro Ausführung ❌ ([Erneuten Eintritt bei Wiederholung erzwingen](read-audience.md#schedule) verfügbar) | ✅ Konfigurierbar (Profil, das sich bereits auf Journey befindet, kann nicht erneut in dieselbe Version wechseln) | ✅ Pro Ereignis |
| **Optimierung** | | | | |
| Pfadexperimente (A/B-Tests) | ✅ | ✅ | ✅ | ❌ |
| **Erweitert** | | | | |
| Inkrementelles Lesen | ❌ | ✅ | ❌ | ❌ |
| Maximaler Durchsatz | 5.000 TPS (auf Organisationsebene mit Zielgruppen-Qualifizierung geteilt) | 20.000 TPS pro Sandbox | 5.000 TPS (auf Ebene der freigegebenen Organisation mit unitärem Ereignis) | Geschäftsereignis: 5.000 TPS; Audience-Schritt lesen: 20.000 TPS |

**Legende:** ✅ = Unterstützt | ❌ = Nicht unterstützt

## Nächste Schritte {#next-steps}

Nachdem Sie nun einen Journey-Typ ausgewählt haben:

* **[Erstellen Sie Ihre erste Journey](journey-gs.md)** — Schrittweise Anleitung von der Eingabe bis zur Veröffentlichung
* **[Erfahren Sie mehr über den Journey-Designer](using-the-journey-designer.md)** — Entwerfen Sie Ihre Journey-Arbeitsfläche
* **[Profileintritt in Journey](entry-management.md)** — Eintrittsregeln, Wiedereintritt und Durchsatz nach Typ
* **[Erste Schritte mit Journey](journey.md)** — Überblick über Grundlagen und Funktionen
* **[Häufig gestellte Fragen zu Journey Orchestration](journey-faq.md)** — Häufig gestellte Fragen beantwortet

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Diese Seite bietet einen umfassenden Vergleich der vier AJO-Journey-Typen - Unitäres Ereignis, Zielgruppe lesen, Zielgruppen-Qualifizierung und Geschäftsereignis - sowie ein Entscheidungshandbuch und eine Funktionskompatibilitätsmatrix, die Benutzern bei der Auswahl des richtigen Typs für ihren Anwendungsfall helfen.

**intents:**

* Wählen Sie mithilfe der Entscheidungstabelle den richtigen Journey-Typ für einen bestimmten geschäftlichen Anwendungsfall aus
* Vergleichen Sie Journey-Typen nebeneinander mithilfe der detaillierten Funktionskompatibilitätsmatrix
* Verstehen, wann Audience-Journey lesen für geplante Batch-Kommunikationen verwendet werden sollte
* Erfahren Sie, wann einheitliche Ereignis-Journey für ereignisgesteuerte Erlebnisse in Echtzeit verwendet werden sollten
* Erfahren Sie, wann Journey zur Zielgruppenqualifizierung für Echtzeit-Antworten auf Statusänderungen verwendet werden sollten
* Verstehen, wann Geschäftsereignis-Journey für geschäftsbedingungsgesteuerte Kommunikation verwendet werden sollten
* Verständnis der Durchsatzbeschränkungen pro Journey-Typ bei der Planung von Bereitstellungen mit hohem Volumen

**Glossar:**

* **Unitäres Ereignis-Journey**: Ein Journey, das durch eine bestimmte individuelle Kundenaktion ausgelöst wird (z. B. Kauf, Anmeldung), bei der Profile in Echtzeit jeweils einen Eintrag eingeben. *(produktspezifisch)*
* **Zielgruppen-Journey lesen**: Eine Journey, die mit einer Adobe Experience Platform-Zielgruppe beginnt und Nachrichten im Batch nach einem Zeitplan gleichzeitig an alle Profile sendet. *(produktspezifisch)*
* **Zielgruppen-Qualifizierungs-Journey**: Eine Journey, die Trigger erstellt, wenn sich Profile für ein bestimmtes Zielgruppensegment qualifizieren oder dieses verlassen. Erfordert eine vom Streaming bewertete Zielgruppe für das Echtzeit-Einstiegsverhalten. *(produktspezifisch)*
* **Geschäftsereignis-Journey**: Ein Journey, das durch ein Geschäftsereignis ausgelöst wird (z. B. Stock-Update, Preisänderung), das mehrere Profile gleichzeitig betrifft. Es ist immer mit einem internen Schritt „Zielgruppe lesen“ für die Profilaufnahme verknüpft. *(produktspezifisch)*
* **Inkrementelles Lesen**: Eine Funktion zum Lesen von Zielgruppen, die nur Profile verarbeitet, die seit der letzten Ausführung der Zielgruppe beigetreten sind, nicht jedes Mal die vollständige Zielgruppe. Nur für „Zielgruppen-Journey lesen“ verfügbar. *(produktspezifisch)*
* **Streaming-Zielgruppe**: Eine Adobe Experience Platform-Zielgruppe, die kontinuierlich in Echtzeit ausgewertet wird, im Gegensatz zu einer Batch-Zielgruppe, die anhand eines Zeitplans (z. B. täglich) ausgewertet wird. Erforderlich, damit Journey für die Zielgruppenqualifizierung das Echtzeit-Einstiegsverhalten erzielen. *(produktspezifisch)*

**Leitplanken:**

* Inkrementelles Lesen ist nur für die Journey-Gruppe „Zielgruppe lesen“ verfügbar, nicht für unitäre Journey, Zielgruppenqualifikationen oder Geschäftsereignisse
* Pfadexperimente (A/B-Tests) werden für Geschäftsereignis-Journey nicht unterstützt
* Der erneute Profileintritt in den Journey der Aktivität „Zielgruppe lesen“ ist standardmäßig auf einmal pro Ausführung beschränkt. Verwenden Sie bei wiederholten Ausführungen die Option „Erneuten Eintritt bei Wiederholung erzwingen“, damit Profile bei der nächsten Ausführung erneut eintreten können
* Die Aktivität „Zielgruppe lesen“ ist nur als Journey-Eintrag in den Journey-Einträgen „Zielgruppe lesen“ und „Geschäftsereignis“ verfügbar, nicht jedoch in den Journey-Einträgen „Unitäres Ereignis“ oder „Zielgruppen-Qualifizierung“
* Zielgruppen-Qualifizierungs- und Zielgruppen-Journey lesen können keine Sprungaktivität enthalten und auch nicht das Ziel einer Sprungaktivität von einer anderen Journey sein
* Zielgruppen-Qualifizierungs-Journey erfordern eine vom Streaming ausgewertete Zielgruppe. Ab August 2026 können Batch-ausgewertete Zielgruppen nicht mehr in einem Zielgruppen-Qualifizierungsknoten verwendet werden - siehe [Migrationshandbuch](aq-batch-audiences-migration.md)
* Journey mit einer unitären Ereignis- und Zielgruppenqualifizierung verwenden auf Unternehmensebene ein Durchsatzlimit von 5.000 TPS. Unter Zielgruppen-Journey lesen werden bis zu 20.000 TPS pro Sandbox unterstützt
* Ein bereits auf einer Journey vorhandenes Profil kann nicht dieselbe Journey erneut aufrufen, unabhängig von der Konfiguration des erneuten Eintritts

**Terminologie:**

* Kanonischer Name: Unitäres Ereignis-Journey — Varianten: ereignisgesteuertes Journey, unitäres Journey
* Kanonischer Name: Zielgruppen-Journey lesen — Varianten: Batch-Journey
* Kanonischer Name: Audience Qualification Journey — Varianten: Audience Qualification Event Journey
* Kanonischer Name: Geschäftsereignis-Journey — Varianten: Geschäftsereignis-ausgelöstes Journey
* Verwechseln Sie nicht: „Zielgruppen-Journey lesen“ ≠ „Zielgruppen-Qualifizierungs-Journey&quot; — „Zielgruppe lesen“ verarbeitet alle Zielgruppenmitglieder im Batch planmäßig. Die Zielgruppen-Qualifizierung reagiert auf individuelle Mitgliedschaftsänderungen in Echtzeit (Streaming-Zielgruppen nur für sofortigen Eintritt)
* Verwechseln Sie nicht: „Unitäres Ereignis-Journey&quot; ≠ „Geschäftsereignis-Journey&quot; — Unitäres Ereignis wird durch eine Kundenaktion ausgelöst, die ein Profil betrifft. Geschäftsereignis wird durch eine Geschäftsbedingung ausgelöst und nimmt über einen internen Schritt „Zielgruppe lesen“ mehrere auf

**FAQ:**

* **F: Welchen Journey-Typ sollte ich für einen monatlichen Newsletter verwenden?** - Verwenden Sie eine Journey mit dem Titel „Zielgruppe lesen“. Sie ist für die geplante Batch-Kommunikation mit allen Profilen in einem Zielgruppensegment gleichzeitig konzipiert.
* **F: Welchen Journey-Typ sollte ich verwenden, um einen Transaktionsabbruch wiederherzustellen?** — Verwenden Sie eine unitäre Ereignis-Journey. Sie wird sofort bei Eintreten des Abbruchsereignisses Trigger und reagiert in Echtzeit auf das Verhalten des Kontakts.
* **F: Kann ich A/B-Pfadexperimente auf einer Geschäftsereignis-Journey durchführen?** — Nein. Pfadexperimente werden für Geschäftsereignis-Journey nicht unterstützt.
* **F: Was ist der Unterschied zwischen einer unitären Ereignis-Journey und einer Zielgruppen-Qualifizierungs-Journey?** — Ein unitäres Ereignis-Journey wird durch eine bestimmte Kundenaktion ausgelöst (z. B. Kauf). Eine Zielgruppen-Qualifizierungs-Journey wird Trigger, wenn ein Profil basierend auf der Bewertung von Streaming-Kriterien in ein Zielgruppensegment eintritt oder daraus austritt.
* **F: Welche Journey-Typen unterstützen inkrementelles Lesen?** — Nur „Zielgruppen-Journey lesen“ unterstützt inkrementelles Lesen. Die anderen drei Journey-Typen nicht.
* **F: Kann ich die Aktivität „Zielgruppe lesen“ zu einer unitären Ereignis-Journey hinzufügen?** — Nein. Die Aktivität „Zielgruppe lesen“ ist nur als Journey-Eintrag in den Journey-Dateien „Zielgruppe lesen“ und „Geschäftsereignis“ verfügbar.
* **F: Kann ich eine Sprungaktivität in einer „Zielgruppe lesen“-Journey verwenden?** — Nein. Journey, die mit der Aktivität „Zielgruppe lesen“ oder „Zielgruppen-Qualifizierung“ beginnen, können keine Sprungaktivität enthalten und nicht das Ziel eines Sprungs von einer anderen Journey sein.
* **F: Kann ich neue App-Benutzer mit einer Zielgruppen-Qualifizierungs-Journey willkommen heißen?** — Ja, wenn der Eintrag von einer Streaming-Zielgruppe gesteuert wird (z. B. wenn ein Profil einem Neubenutzersegment beitritt). Ein unitäres Anmeldungsereignis-Journey ist ebenfalls ein gängiges Muster.
* **F: Die Journey „My Audience Qualification“ wird nicht in Echtzeit ausgelöst. Warum?** — Zielgruppen-Qualifizierungs-Journey erfordern eine vom Streaming ausgewertete Zielgruppe. Die Verwendung einer Batch-ausgewerteten Zielgruppe ist veraltet und wird ab August 2026 blockiert. [Siehe Migrationshandbuch](aq-batch-audiences-migration.md)
* **F: Was ist der Durchsatzunterschied zwischen dem unitären Ereignis und den Journey-Werten unter „Zielgruppe lesen“?** — Journey von unitären Ereignissen haben auf Unternehmensebene ein TPS-Limit von 5.000 mit Journey für Zielgruppen-Qualifizierung gemeinsam. Journey von Zielgruppen unterstützen bis zu 20.000 TPS pro Sandbox, wodurch sie sich besser für groß angelegte Batch-Kampagnen eignen.

+++
