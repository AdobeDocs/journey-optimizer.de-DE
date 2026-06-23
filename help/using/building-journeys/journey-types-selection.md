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
hide: true
exl-id: 0c894dc1-76b6-4b33-baf8-eaf6686f7d38
TQID: https://experienceleague.adobe.com/rEANha6Lppyd5vog-0kZ3aL9VvZHc9kziW-d-jiWqeA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: cce82f05-fc3c-4af7-85ff-8bba603861a7id: cfba2953-2ce9-4b00-a00c-71cd338ae63fid: ebd64fe4-362a-4a1c-9476-b2573ed12a95id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 151b396b7945535cb4219f782dfb6a79e44463d4
workflow-type: tm+mt
source-wordcount: 2080
ht-degree: 23%

---

# Journey-Typen: Wählen Sie den richtigen aus {#journey-types-selection}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie die vier Journey-Typen - Unitäres Ereignis, Lesen von Zielgruppen, Zielgruppen-Qualifizierung und Geschäftsereignis - vergleichen und das Entscheidungshandbuch und die Funktionskompatibilitätsmatrix verwenden können, um den richtigen für Ihren Anwendungsfall auszuwählen.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] unterstützt vier Journey-Typen, die jeweils für unterschiedliche Einstiegsmechanismen und Geschäftsszenarien entwickelt wurden. Dieser Leitfaden hilft Ihnen, die Unterschiede zu verstehen und den richtigen Typ für Ihren Anwendungsfall auszuwählen.

>[!NOTE]
>
>Sie wissen nicht genau, welchen Typ sie wählen sollen? Beginnen Sie mit **Unitären Ereignis-Journey** für ereignisbasierte Erlebnisse oder **Audience-Journey lesen** für geplante Kampagnen. Diese decken die häufigsten Anwendungsfälle ab.

## Journey-Typen – Überblick {#journey-types}

>[!BEGINTABS]

>[!TAB Journey für unitäre Ereignisse]

**Verwendung:** In Echtzeit durch Ereignisse ausgelöste Erlebnisse

**Unitäre Ereignis-Journey** werden einzeln ausgelöst, wenn eine bestimmte Aktion auftritt (Kauf, App-Anmeldung, Formularübermittlung). Die Profile treten jeweils in Echtzeit einzeln ein, was dies ideal für sofortige, verhaltensgesteuerte Antworten macht.

**Perfekt für:** Bestellbestätigungen nach dem Kauf, Willkommens-E-Mails, wenn sich jemand anmeldet, Benachrichtigungen zum Zurücksetzen des Kennworts und Personalisierung nach der Anmeldung.

➡️ [Informationen zu Ereignissen](../event/about-events.md) | [Anwendungsfall „Nachricht an Abonnenten“](message-to-subscribers-uc.md) | [Erstellen einer unitären Ereignis-Journey](#build-unitary-event)

>[!TAB Journeys des Typs „Zielgruppe lesen“]

**Verwendung:** Geplante Kampagnen für Zielgruppensegmente

**Audience-Journey lesen** Beginnen Sie mit einer [!DNL Adobe Experience Platform] Audience und senden Sie Nachrichten im Batch an alle Profile gleichzeitig. Dieser Journey-Typ eignet sich ideal für geplante Kommunikation in großem Umfang. Verwenden Sie die Option **Inkrementelles Lesen** für wiederkehrende Journeys, um nur die Profile zu verarbeiten, die seit der letzten Ausführung der Zielgruppe beigetreten sind, anstatt jedes Mal die gesamte Zielgruppe erneut zu verarbeiten.

**Perfekt für:** monatliche Newsletter, Werbekampagnen für bestimmte Segmente, Produktankündigungen, wiederkehrende Interaktionsreihen und saisonale Marketing-Kampagnen.

➡️ [Erfahren Sie mehr über „Zielgruppe lesen](read-audience.md) | [Erste Schritte mit Zielgruppen](../audience/about-audiences.md) | [Erstellen einer „Zielgruppe lesen“Journey](#build-read-audience)

>[!TAB Journeys des Typs „Zielgruppenqualifizierung“]

**Verwendung:** Echtzeit-Reaktionen auf Änderungen der Zielgruppenzugehörigkeit

**Journeys des Typs „Zielgruppenqualifizierung“** werden ausgelöst, wenn Profile sich für ein bestimmtes Zielgruppensegment qualifizieren (oder daraus aussteigen). Profile treten einzeln ein, wenn sie die Kriterien erfüllen, was eine sofortige Interaktion ermöglicht, wenn sich das Kundenverhalten ändert. Für das Echtzeit-Einstiegsverhalten muss die Zielgruppe nur im nächsten Auswertungsfenster **Streaming-ausgewertet**; Trigger-Eintrag für Batch-ausgewertete Zielgruppen (bis zu 24 Stunden) erfolgen.

**Perfekt für:** Benachrichtigungen zu Upgrades der VIP-Stufe, Meldungen zu ersten Kauffeiern, Warnhinweise zu Abwanderungsrisiken und Übergänge in der Treueprogramm-Phase.

➡️ [Erfahren Sie mehr über Zielgruppen](audience-qualification-events.md) | [Erstellen von Zielgruppen](../audience/creating-a-segment-definition.md) | [Erstellen einer Journey zur Zielgruppen-Qualifizierung](#build-audience-qualification)

>[!TAB Journeys des Typs „Geschäftsereignis“]

**Verwendung:** Geschäftsbedingungen, die mehrere Kundinnen und Kunden betreffen

**Geschäftsereignis-Journey** werden durch ein Geschäftsereignis (Stock-Updates, Preisänderungen) ausgelöst, das mehrere Profile gleichzeitig betrifft. Intern folgt auf den Geschäftsereignis-Trigger immer der Schritt „Zielgruppe lesen“, der die relevanten Profile aufnimmt. Daher folgt der Profileintrag den Regeln des Zielgruppen-Durchsatzes lesen und nicht dem Durchsatz von unitären Ereignissen.

**Perfekt für:** Warnungen bei geringem Bestand an interessierte Kunden, Flash-Verkaufsankündigungen, Benachrichtigungen bei Preisrückgängen und Warnhinweise für das Produkt-Back-in-Stock.

➡️ [Erfahren Sie mehr über Geschäftsereignisse](../event/about-creating-business.md) | [Einstiegsverwaltung](entry-management.md) | [Erstellen einer Geschäftsereignis-Journey](#build-business-event)

>[!ENDTABS]

## Entscheidungshandbuch: Auswahl des Journey-Typs {#decision-guide}

Verwenden Sie die nachstehende Tabelle, um Ihr Ziel dem richtigen Journey-Typ zuzuordnen. Für die meisten neuen Benutzerinnen und **decken** Unitäres Ereignis“ oder **Zielgruppe lesen**-Journey die meisten Anwendungsfälle ab.

| Ihr Ziel | Empfohlener Journey-Typ | Warum |
|-----------|--------------------------|-----|
| Senden einer Bestellbestätigung nach Kauf | Unitäres Ereignis | Sofortige Reaktion auf einzelne Aktionen |
| Senden eines monatlichen Newsletters an Abonnentinnen und Abonnenten | Zielgruppe lesen | Geplante Batch-Kommunikation |
| Benachrichtigen von Kundinnen und Kunden, wenn sie VIP-Status erreichen | Zielgruppenqualifizierung | Echtzeit-Antwort auf den Eintrag in die Streaming-Zielgruppe |
| Benachrichtigen von Kundinnen und Kunden über niedrige Lagerbestände beobachteter Artikel | Geschäftsereignis | Geschäftsbedingung wirkt sich auf mehrere Kundinnen und Kunden aus |
| Begrüßen neuer Benutzender der App | Unitäres Ereignis | Durch Anmeldungsereignis ausgelöst |
| Erneute Interaktion mit inaktiven Kunden (wiederkehrend, geplant) | Zielgruppe lesen | Wiederkehrende Batch-Ausführung für Inaktivitätszielgruppe |
| Saisonale Promotion für Zielsegment | Zielgruppe lesen | Geplante Kampagne für Zielgruppe |
| Ankündigung von Blitzverkauf | Geschäftsereignis | Geschäftsentscheidung wirkt sich auf mehrere Kundinnen und Kunden aus |
| Reagieren, sobald ein Kunde die Gold-Treuestufe erreicht | Zielgruppenqualifizierung | Streaming-Zielgruppe, individueller Echtzeit-Eintrag |

## Detailvergleich der Journey-Typen {#journey-types-comparison}

| Aspekt | Journey für unitäre Ereignisse | Journeys des Typs „Zielgruppe lesen“ | Journeys des Typs „Zielgruppenqualifizierung“ | Journeys des Typs „Geschäftsereignis“ |
|--------|------------------------|------------------------|--------------------------------|------------------------|
| **Eintrittsmechanismus** | Individuelles Ereignis als Trigger | Geplanter Batch | Änderung der Zielgruppenzugehörigkeit in Echtzeit | Ereignis auf Unternehmensebene + Schritt „Zielgruppe lesen“ |
| **Eintrittszeitpunkt** | Echtzeit, sobald Ereignisse eintreten | Geplant (einmalig oder wiederkehrend) | Echtzeit, sobald die Qualifizierung erfolgt (Streaming-Zielgruppen); bei Batch-bewerteten Zielgruppen verzögert | Echtzeit-Trigger; Profilaufnahme folgt dem Durchsatz „Zielgruppe lesen“ |
| **Profileintritt** | Eins nach dem anderen | Alle gleichzeitig (Batch) | Eins nach dem anderen | Mehrere Profile über den internen Schritt „Zielgruppe lesen“ |
| **Quelle des Triggers** | Kundenaktion (Kauf, Klick, Anmeldung) | Zeitbasierter Plan | Ein- oder Ausstieg aus der Zielgruppenmitgliedschaft | Geschäftsbedingung (Aktie, Preis) |
| **Geeignet für** | Transaktionsnachrichten, Verhaltensreaktionen | Marketing-Kampagnen, Newsletter, wiederkehrende Programme | Treueprogramme, Übergänge in Lebenszyklusphasen | Bestandsbenachrichtigungen, Promotions, Geschäftsbedingungen |
| **Verwendung** | Sofortige Reaktion auf einzelne Aktionen sind erforderlich | Große Zielgruppensegmente sollen planmäßig angesprochen werden | Auf Änderungen des Kundenstatus in Echtzeit reagieren | Geschäftsereignisse wirken sich auf mehrere Kunden gleichzeitig aus |
| **Beispiele** | Bestellbestätigung, Passwortzurücksetzung | Monatlicher Newsletter, saisonale Kampagne | VIP-Upgrade, Warnhinweis zum Abwanderungsrisiko | Geringer Lagerbestand, Blitzverkauf, Preissenkung |
| **Erneuter Eintritt** | Konfigurierbar | Einmal pro Ausführung | Pro Qualifizierungsereignis konfigurierbar; ein bereits auf der Journey befindliches Profil kann nicht erneut auf dieselbe Version zugreifen | Mehrere Profile können von demselben Ereignis betroffen sein |
| **Maximaler Durchsatz** | 5.000 TPS (auf Organisationsebene mit Zielgruppen-Qualifizierung geteilt) | 20.000 TPS pro Sandbox | 5.000 TPS (auf Ebene der freigegebenen Organisation mit unitärem Ereignis) | Geschäftsereignis: 5.000 TPS; Audience-Schritt lesen: 20.000 TPS |
| **Datenanforderungen** | Ereignisschema mit Trigger-Daten | Zielgruppe [!DNL Adobe Experience Platform] | Streaming-Zielgruppe (erforderlich für Echtzeit-Eingabe); Batch-Zielgruppe unterstützt, Eingabe jedoch verzögert | Geschäftsereignisschema |

## Funktionskompatibilität nach Journey-Typ {#feature-compatibility}

Nicht alle Funktionen sind für alle Journey-Typen verfügbar. Mithilfe dieser Matrix können Sie herausfinden, welche Funktionen mit welchen Journey-Typen funktionieren:

| Funktion | Unitäres Ereignis | Zielgruppe lesen | Zielgruppenqualifizierung | Geschäftsereignis |
|---------------------|:-------:|:-------------:|:----------------------:|:--------------:|
| **Eintrittsmechanismen** | | | | |
| Durch Ereignis ausgelöster Eintritt | ✅ | ❌ | ❌ | ✅ (Geschäftsereignis-Trigger auf der Journey; Profileingabe über einen internen Schritt „Zielgruppe lesen„) |
| Geplanter Eintritt | ❌ | ✅ | ❌ | ❌ |
| Zielgruppenbasierter Eintritt | ❌ | ✅ (Stapel) | ✅ (Streaming) | ❌ |
| **Orchestrierungsfunktionen** | | | | |
| Warteaktivitäten | ✅ | ✅ | ✅ | ✅ |
| Bedingungsaktivitäten | ✅ | ✅ | ✅ | ✅ |
| Benutzerdefinierte Aktionen | ✅ | ✅ | ✅ | ✅ |
| Aktivität „Zielgruppe lesen“ (innerhalb von Journey) | ✅ | ✅ | ✅ | ✅ |
| Aktivität zur Zielgruppen-Qualifizierung (innerhalb von Journey) | ✅ | ✅ | ✅ | ✅ |
| Aktivität „Springen“ | ✅ | ❌ | ❌ | ✅ |
| **Profil-Management** | | | | |
| Erneuter Profileintritt | ✅ Konfigurierbar | ❌ Einmal pro Ausführung | ✅ Konfigurierbar (Profil, das sich bereits auf Journey befindet, kann nicht erneut in dieselbe Version wechseln) | ✅ Pro Ereignis |
| Namespace-Konfiguration | ✅ Erforderlich | ✅ Optional | ✅ Erforderlich | ✅ Erforderlich |
| Profilbegrenzung | ✅ | ✅ | ✅ | ✅ |
| **Tests und Optimierung** | | | | |
| Testmodus | ✅ | ✅ | ✅ | ✅ |
| Probelauf | ✅ | ✅ | ✅ | ✅ |
| Pfadexperimente (A/B-Tests) | ✅ | ✅ | ✅ | ❌ |
| Versandzeitoptimierung | ✅ | ✅ | ✅ | ✅ |
| **Kanäle** | | | | |
| E-Mail | ✅ | ✅ | ✅ | ✅ |
| Push-Benachrichtigungen | ✅ | ✅ | ✅ | ✅ |
| SMS/MMS | ✅ | ✅ | ✅ | ✅ |
| In-App-Nachrichten | ✅ | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ✅ | ✅ |
| Inhaltskarten | ✅ | ✅ | ✅ | ✅ |
| **Erweiterte Funktionen** | | | | |
| Inkrementelles Lesen | ❌ | ✅ | ❌ | ❌ |
| Exportieren der Zielgruppe | ✅ | ✅ | ✅ | ✅ |
| Zeitzonen-Management | ✅ | ✅ | ✅ | ✅ |
| Reaktionsereignisse | ✅ | ✅ | ✅ | ✅ |
| Externe Datenquellen | ✅ | ✅ | ✅ | ✅ |
| Drosselung/Begrenzung | ✅ | ✅ | ✅ | ✅ |

**Legende:** ✅ = Unterstützt | ❌ = Nicht unterstützt

>[!NOTE]
>
>Einschränkungen bei Sprungaktivitäten: Eine Journey, die mit der Aktivität „Zielgruppe lesen“ oder „Zielgruppen-Qualifizierung“ beginnt, kann keine Sprungaktivität enthalten und auch nicht das Ziel einer Sprungaktivität von einer anderen Journey sein.

## Nächste Schritte {#next-steps}

In jeder Tabelle sind die Schritte „Konfigurieren-durch-Verwalten“ für diesen Journey-Typ aufgeführt.

### Journey für unitäre Ereignisse {#build-unitary-event}

* **[Erstellen Ihrer ersten Journey](journey-gs.md)**: Schrittweise Anleitung
* **[Weitere Informationen über den Journey-Designer](using-the-journey-designer.md)**: Entwerfen Ihrer Journey-Arbeitsfläche
* **[Erkunden der Journey-Funktionen](journey.md#capabilities)**: Entdecken der erweiterten Funktionen
* **[Anzeigen häufig gestellter Fragen zu Journeys](journey-faq.md)**: Antworten auf häufig gestellte Fragen

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
* Der erneute Profileintritt in den Journey der Aktivität „Zielgruppe lesen“ ist auf einmal pro Ausführung beschränkt
* Zielgruppen-Qualifizierungs- und Zielgruppen-Journey lesen können keine Sprungaktivität enthalten und auch nicht das Ziel einer Sprungaktivität von einer anderen Journey sein
* Journey zur Zielgruppenqualifizierung erfordern eine vom Streaming ausgewertete Zielgruppe für die Echtzeiteingabe; Batch-ausgewertete Zielgruppen verursachen Einstiegsverzögerungen von bis zu 24 Stunden
* Journey mit einer unitären Ereignis- und Zielgruppenqualifizierung verwenden auf Unternehmensebene ein Durchsatzlimit von 5.000 TPS. Unter Zielgruppen-Journey lesen werden bis zu 20.000 TPS pro Sandbox unterstützt
* Ein bereits auf einer Journey vorhandenes Profil kann nicht dieselbe Journey erneut aufrufen, unabhängig von der Konfiguration des erneuten Eintritts

**Terminologie:**

* Kanonischer Name: Unitäres Ereignis-Journey — Varianten: ereignisgesteuertes Journey, unitäres Journey
* Kanonischer Name: Zielgruppen-Journey lesen — Varianten: Batch-Journey, Segment-Trigger-Journey, Segment-Journey lesen
* Kanonischer Name: Audience Qualification Journey — Varianten: Audience Qualification Event Journey
* Kanonischer Name: Geschäftsereignis-Journey — Varianten: Geschäftsereignis-ausgelöstes Journey
* Verwechseln Sie nicht: „Zielgruppen-Journey lesen“ ≠ „Zielgruppen-Qualifizierungs-Journey&quot; — „Zielgruppe lesen“ verarbeitet alle Zielgruppenmitglieder im Batch planmäßig. Die Zielgruppen-Qualifizierung reagiert auf individuelle Mitgliedschaftsänderungen in Echtzeit (Streaming-Zielgruppen nur für sofortigen Eintritt)
* Verwechseln Sie nicht: „Unitäres Ereignis-Journey&quot; ≠ „Geschäftsereignis-Journey&quot; — Unitäres Ereignis wird durch eine Kundenaktion ausgelöst, die ein Profil betrifft. Geschäftsereignis wird durch eine Geschäftsbedingung ausgelöst und nimmt über einen internen Schritt „Zielgruppe lesen“ mehrere auf

**FAQ:**

* **F: Welchen Journey-Typ sollte ich für einen monatlichen Newsletter verwenden?** - Verwenden Sie eine Journey mit dem Titel „Zielgruppe lesen“. Sie ist für die geplante Batch-Kommunikation mit allen Profilen in einem Zielgruppensegment gleichzeitig konzipiert.
* **F: Welcher Journey-Typ verarbeitet eine Bestellbestätigung nach einem Kauf?** - Verwenden Sie eine unitäre Ereignis-Journey. Sie bietet eine sofortige Echtzeit-Antwort auf eine individuelle Kundenaktion.
* **F: Kann ich A/B-Pfadexperimente auf einer Geschäftsereignis-Journey durchführen?** — Nein. Pfadexperimente werden für Geschäftsereignis-Journey nicht unterstützt.
* **F: Was ist der Unterschied zwischen einer unitären Ereignis-Journey und einer Zielgruppen-Qualifizierungs-Journey?** — Ein unitäres Ereignis-Journey wird durch eine bestimmte Kundenaktion ausgelöst (z. B. Kauf). Eine Zielgruppen-Qualifizierungs-Journey wird Trigger, wenn ein Profil basierend auf der Bewertung von Streaming-Kriterien in ein Zielgruppensegment eintritt oder daraus austritt.
* **F: Welche Journey-Typen unterstützen inkrementelles Lesen?** — Nur „Zielgruppen-Journey lesen“ unterstützt inkrementelles Lesen. Die anderen drei Journey-Typen nicht.
* **F: Kann ich eine Sprungaktivität in einer „Zielgruppe lesen“-Journey verwenden?** — Nein. Journey, die mit der Aktivität „Zielgruppe lesen“ oder „Zielgruppen-Qualifizierung“ beginnen, können keine Sprungaktivität enthalten und nicht das Ziel eines Sprungs von einer anderen Journey sein.
* **F: Die Journey „My Audience Qualification“ wird nicht in Echtzeit ausgelöst. Warum?** — Zielgruppen-Qualifizierungs-Journey erfordern eine vom Streaming ausgewertete Zielgruppe. Bei einer Batch-Auswertung der Zielgruppe (z. B. einer täglichen Momentaufnahme) wird die Eingabe bis zum nächsten Auswertungsfenster verzögert, was bis zu 24 Stunden dauern kann.
* **F: Was ist der Durchsatzunterschied zwischen dem unitären Ereignis und den Journey-Werten unter „Zielgruppe lesen“?** — Journey von unitären Ereignissen haben auf Unternehmensebene ein TPS-Limit von 5.000 mit Journey für Zielgruppen-Qualifizierung gemeinsam. Journey von Zielgruppen unterstützen bis zu 20.000 TPS pro Sandbox, wodurch sie sich besser für groß angelegte Batch-Kampagnen eignen.

+++
