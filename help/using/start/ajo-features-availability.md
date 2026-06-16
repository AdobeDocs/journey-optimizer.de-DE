---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer-Funktionsverfügbarkeit
description: Eine einzige, konsolidierte Referenz, um zu ermitteln, welche Adobe Journey Optimizer-Funktionen verfügbar sind, welchen Lebenszyklusstatus sie haben (allgemeine Verfügbarkeit, eingeschränkte Verfügbarkeit oder Beta), auf welches Basisangebot sie sich beziehen, und wann sie versendet wurden - ohne Querverweise auf Versionshinweise.
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner, Intermediate
keywords: Journey Optimizer, Funktionsverfügbarkeit, Verfügbare Funktionen, Allgemein, Eingeschränkte Verfügbarkeit, Beta, Lebenszyklus, Veröffentlichungsdatum, Berechtigung, Basisangebot, Kampagnen, Journey
hide: true
source-git-commit: c0bfb3ea92ea1375fa6bdd2bdffc836c0046db7a
workflow-type: tm+mt
source-wordcount: '1880'
ht-degree: 13%

---


# Journey Optimizer-Funktionsverfügbarkeit {#ajo-features-availability}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, welche [!DNL Adobe Journey Optimizer] Funktionen verfügbar sind, in welcher Lebenszyklusphase sich die einzelnen Funktionen befinden (allgemeine Verfügbarkeit, eingeschränkte Verfügbarkeit oder Beta), für welches Basisangebot sie gelten und wann sie versendet wurden - so können Sie *„Kann ich dies verwenden?“* ohne die Versionshinweise durchzugehen.

>[!ENDSHADEBOX]

Auf dieser Seite wird die Funktionsverfügbarkeit in allen [!DNL Adobe Journey Optimizer] zusammengefasst, sodass Sie bestätigen können, was Sie während der Umfangsberechnung vor der Implementierung verwenden können. Die Funktionen sind nach Funktionsbereich gruppiert. Innerhalb jedes Bereichs listet jede Funktion ihren aktuellen Lebenszyklusstatus, das Basisangebot, für das sie gilt, das Datum, an dem sie verfügbar wurde, und alle Hinweise zur Konfiguration oder zu regionalen Einschränkungen auf.

Zeilen **Kernfunktion** in der Spalte *Verfügbar seit* sind langjährige, grundlegende Funktionen, die seit vor 2026 allgemein verfügbar sind. Datumsangaben spiegeln Änderungen wider, die 2026 bereitgestellt wurden.

>[!IMPORTANT]
>
>**Warum kann ich eine Funktion in meiner Umgebung nicht sehen?** Funktionen in **Eingeschränkte Verfügbarkeit** oder **Beta** sind nicht für alle sichtbar - sie werden erst für eine eingeschränkte Gruppe von Organisationen eingeführt. Wenn eine Funktion, über die Sie lesen, nicht in Ihrer Umgebung angezeigt wird, überprüfen Sie ihren Status unten: Wenn es sich um **LA** oder **Beta** handelt, wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff zu erhalten. Eine Funktion, die hier aufgelistet ist, bedeutet nicht, dass sie in Ihrer Umgebung aktiviert ist.

>[!NOTE]
>
>**Verfügbarkeit vs. Berechtigung.** Auf dieser Seite werden *Funktionslebenszyklus und Verfügbarkeit* (ob eine Funktion bereitgestellt wurde und mit welcher Laufzeit) verfolgt. Ob eine Funktion in *Lizenz enthalten ist* hängt von Ihrem Basisangebot und Ihren Add-ons ab (siehe [Pakete und Funktionen](ajo-packages.md).

## Was die Lebenszyklusstatus bedeuten {#status-definitions}

| Status | Bedeutung |
|--------|--------------|
| **GA** — Allgemeine Verfügbarkeit | Für alle Umgebungen freigegeben. Verfügbar für alle Organisationen, deren Lizenz die Funktion umfasst. |
| **LA** — Eingeschränkte Verfügbarkeit | Für einen eingeschränkten Satz von Organisationen freigegeben. **Wenden Sie sich an Ihren Adobe-**, um Zugriff anzufordern. |
| **Beta** | Early-Access-Version zur Auswertung. Kann sich vor der allgemeinen Verfügbarkeit ändern. Erfordert möglicherweise eine Anmeldung. |

## „Gilt für“-Zuordnungen zu Basisangeboten {#applies-to}

Die **Gilt für** bezieht sich auf die drei [!DNL Adobe Journey Optimizer] Basisangebote:

- **Journey Optimizer - Kampagnen** - Batch, zielgruppenbasierte Orchestrierung
- **Journey Optimizer - Journey** — Echtzeit, ereignisgesteuerte Orchestrierung
- **Journey Optimizer - Kampagnen und Journey** — beide

Die mit „Alle Basisangebote **gekennzeichneten Kanal-, Inhalts- und Plattformfunktionen** unabhängig vom Basisangebot verfügbar, für die meisten Funktionen ist jedoch weiterhin das entsprechende Kanal- oder Add-on für erweiterte Funktionen erforderlich. Weitere Informationen [ Berechtigungen finden Sie unter ](ajo-packages.md)Pakete und Funktionen“.

## Funktionen nach Funktionsbereich {#features-by-area}

>[!BEGINTABS]

>[!TAB Kanäle]

| Funktion | Status | Gilt für | Verfügbar seit | Anmerkungen |
|---------|--------|-----------|-----------------|-------|
| Neuer Mobile-Nachrichtenkanal (SMS, MMS, RCS) | GA | Alle Basisangebote | &#x200B;20. Mai 2026 | Einheitliche SMS/MMS/RCS; natives RCS-Authoring (Bilder, Karussells) |
| Deeplinks im E-Mail-Designer | GA | Alle Basisangebote | &#x200B;12. Mai 2026 | Erfordert Mobile-App-Konfiguration |
| Optimieren von E-Mails für KI-Posteingänge | GA | Alle Basisangebote | &#x200B;17. April 2026 | Apple Intelligence, Gmail Gemini |
| Absenderparameter im E-Mail-Header | GA | Alle Basisangebote | April 2026 | „Absender im Auftrag von“ / „über“ |
| CC-Feld in E-Mail-Kanaleinstellungen | GA | Alle Basisangebote | April 2026 | Unterstützt Personalisierung |
| Posteingang | GA | Alle Basisangebote | &#x200B;7. April 2026 | – |
| Kanal für Web-Push-Benachrichtigungen | GA | Alle Basisangebote | &#x200B;13. Februar 2026 | Zuvor Beta |
| Live-Aktivität für iOS | GA | Alle Basisangebote | &#x200B;3. März 2026 | Sperrbildschirm / Dynamic Island; zuvor Beta |
| Direkt-Mail-Kanal in Journeys | GA | Journey; Kampagnen und Journey | &#x200B;29. Januar 2026 | Zuvor LA |
| Direkt-Mail-Kanal in orchestrierten Kampagnen | GA | Kampagnen; Kampagnen und Journey | &#x200B;28. Januar 2026 | – |
| LINE-Kanal | GA | Alle Basisangebote | 2025 | – |
| Unterstützung und Tracking von WhatsApp-Schaltflächen | GA | Alle Basisangebote | Mai 2026 | Schnelle Antwort, CTA URL/Telefon |
| E-Mail | GA | Alle Basisangebote | Kernfunktionen | Add-on „Ausgehender Versand“ erforderlich |
| Push-Benachrichtigungen | GA | Alle Basisangebote | Kernfunktionen | Ausgehender Versand oder Mobile-Add-on erforderlich |
| SMS/MMS | GA | Alle Basisangebote | Kernfunktionen | Basierend auf Ihrer lizenzierten Konfiguration |
| Briefpost | GA | Alle Basisangebote | Kernfunktionen | Add-on „Ausgehender Versand“ erforderlich |
| In-App-Messaging | GA | Alle Basisangebote | Kernfunktionen | Erfordert Mobile-Add-on |
| Inhaltskarten | GA | Alle Basisangebote | Kernfunktionen | Erfordert Mobile-Add-on |
| Web-Kanal | GA | Alle Basisangebote | Kernfunktionen | Erfordert Web-Add-on |
| Code-basierte Erlebnisse | GA | Alle Basisangebote | Kernfunktionen | Erfordert Mobile- oder Web-Add-on |
| Landingpages | GA | Alle Basisangebote | Kernfunktionen | — |
| WhatsApp | GA | Alle Basisangebote | Kernfunktionen | Erfordert WhatsApp-Add-on; basierend auf der lizenzierten Konfiguration |

>[!TAB Journeys]

| Funktion | Status | Gilt für | Verfügbar seit | Anmerkungen |
|---------|--------|-----------|-----------------|-------|
| Journey-Fragmente | GA | Journey; Kampagnen und Journey | &#x200B;9. Juni 2026 | Wiederverwendbare Journey-Knoten; Unterstützung von Sandbox-Tools |
| Journey-Simulation | GA | Journey; Kampagnen und Journey | &#x200B;9. Juni 2026 | Logik mit simulierten Benutzern validieren |
| Journey-Pfadoptimierung - Targeting | GA | Journey; Kampagnen und Journey | &#x200B;8. Juni 2026 | deterministisches Pfadtracking |
| Unterstützung zusätzlicher Identifikatoren für externe Zielgruppen | GA | Journey; Kampagnen und Journey | &#x200B;11. Juni 2026 | CSV und Federated Audience Composition |
| Journey-Pfadexperiment | GA | Journey; Kampagnen und Journey | &#x200B;7. April 2026 | A/B-Bandit und mehrarmiger Bandit; „Ersteige den Gewinner“ |
| Aktionsaktivität in Journeys | GA | Journey; Kampagnen und Journey | &#x200B;20. Februar 2026 | Ersetzt veraltete native Kanalaktivitäten |
| Aktivität „Inhaltsentscheidung“ | GA | Journey; Kampagnen und Journey | &#x200B;10. Februar 2026 | Zuvor LA |
| Ruhezeiten (zeitbasierte Ausschlüsse) | GA | Journey; Kampagnen und Journey | &#x200B;29. Januar 2026 | Zuvor LA |
| KI-Assistent für Journey-Ausdrücke | Beta | Journey; Kampagnen und Journey | &#x200B;3. Juni 2026 | Öffentliche Beta |
| Journey-Schlichtung | LA | Journey; Kampagnen und Journey | &#x200B;24. Februar 2026 | Adobe-Support kontaktieren |
| Journey-Schlichtung - KI-Modelle | LA | Journey; Kampagnen und Journey | April 2026 | Adobe-Support kontaktieren |
| Unterstützung der Datensatzsuche in Journeys | LA | Journey; Kampagnen und Journey | März 2026 | Für Kunden mit Berechtigung zur Datensatzsuche |
| Senden ausgehender Nachrichten in Schüben (Journey) | LA | Journey; Kampagnen und Journey | &#x200B;16. März 2026 | GA in Kampagnen; LA in Journey |
| Automatisierte (ereignisgesteuerte) Journey | GA | Journey; Kampagnen und Journey | Kernfunktionen | Echtzeit, 1:1 Orchestrierung |
| Echtzeit-Ereignis-Trigger | GA | Journey; Kampagnen und Journey | Kernfunktionen | – |
| Audience lesen (zielgruppenbasiert) - Journey | GA | Journey; Kampagnen und Journey | Kernfunktionen | – |
| Journey-Berichte | GA | Journey; Kampagnen und Journey | Kernfunktionen | – |

>[!TAB Kampagnen]

| Funktion | Status | Gilt für | Verfügbar seit | Anmerkungen |
|---------|--------|-----------|-----------------|-------|
| Verkettete orchestrierte Kampagnen | GA | Kampagnen; Kampagnen und Journey | &#x200B;20. Mai 2026 | Trigger einer Kampagne aus der Endaktivität einer anderen Kampagne |
| Inkrementelle Abfrageaktivität in koordinierten Kampagnen | GA | Kampagnen; Kampagnen und Journey | &#x200B;30. April 2026 | Targeting nur von neuen geeigneten Profilen/Ereignissen |
| Kopieren orchestrierter Kampagnen in Sandboxes | GA | Kampagnen; Kampagnen und Journey | April 2026 | Importierte Kampagnen landen im Entwurfsstatus |
| Testaktivität in koordinierten Kampagnen | GA | Kampagnen; Kampagnen und Journey | März 2026 | – |
| Vom Trigger mit einem Signal orchestrierte Kampagnen | GA | Kampagnen; Kampagnen und Journey | März 2026 | bleibt eine Batch-Kampagne |
| Transaktionskategorie in koordinierten Kampagnen | GA | Kampagnen; Kampagnen und Journey | März 2026 | Schrittweise eingeführt nach Region |
| Senden ausgehender Nachrichten (Kampagnen) schwenken | GA | Kampagnen; Kampagnen und Journey | &#x200B;19. Februar 2026 | LA in Journey |
| Batch-Kampagne | GA | Kampagnen; Kampagnen und Journey | Kernfunktionen | Geplante, zielgruppenbasierte Sendungen |
| Orchestrierte Kampagnen (mehrstufige Workflows) | GA | Kampagnen; Kampagnen und Journey | Kernfunktionen | E-Mail, SMS, Push, Briefpost |
| Transaktionsnachrichten | GA | Alle Basisangebote | Kernfunktionen | E-Mail, Push, SMS; in jedem Basisangebot enthalten |

>[!TAB Inhalt und KI]

| Funktion | Status | Gilt für | Verfügbar seit | Anmerkungen |
|---------|--------|-----------|-----------------|-------|
| Content-Beratungs-Selektor | GA | Alle Basisangebote | &#x200B;19. Mai 2026 | KI-semantische Suche nach Assets und Fragmenten |
| Integrationen (Datenquellen von Drittanbietern) | GA | Alle Basisangebote | &#x200B;4. Mai 2026 | Zuvor Beta |
| Eingeschränkte Vererbung beim Unterbrechen von Fragmenten | GA | Alle Basisangebote | &#x200B;21. Mai 2026 | Sperren von Fragmenten gegen lokale Bearbeitung |
| Adobe Express-Integration | GA | Alle Basisangebote | &#x200B;23. April 2026 | Zuvor LA |
| KI-Assistent für Personalisierungsausdrücke | GA | Alle Basisangebote | &#x200B;13. April 2026 | Im Personalisierungseditor und in E-Mail Designer |
| Konvertieren von Bildern in E-Mail-Inhaltsvorlagen | GA | Alle Basisangebote | &#x200B;31. März 2026 | Zuvor LA |
| Benutzerdefinierte Formulare für Landingpages | GA | Alle Basisangebote | &#x200B;26. März 2026 | Zuvor LA (USA und Australien) |
| Integration benutzerdefinierter Firefly- und Drittanbieter-Bildmodelle | GA | Alle Basisangebote | &#x200B;2. März 2026 | Adobe, Partner (Gemini) und benutzerdefinierte Modelle |
| Erweiterter HTML-Editor für E-Mail-Vorlagen | LA | Alle Basisangebote | &#x200B;10. März 2026 | Nur E-Mail-Inhaltsvorlagen; Kontakt zu Kundenbetreuer aufnehmen |
| E-Mail-Expertenmodus im E-Mail-Inhalt | LA | Alle Basisangebote | &#x200B;9. April 2026 | Adobe-Support kontaktieren |
| Designs im E-Mail-Designer | LA | Alle Basisangebote | &#x200B;5. November 2025 | Zuvor Beta; Kundenbetreuer kontaktieren |
| E-Mail-Designer (Drag-and-Drop) | GA | Alle Basisangebote | Kernfunktionen | Visual Authoring und HTML |
| Inhaltsfragmente | GA | Alle Basisangebote | Kernfunktionen | Wiederverwendbare Inhaltsbausteine |
| Inhaltsvorlagen | GA | Alle Basisangebote | Kernfunktionen | – |
| Personalization-Editor | GA | Alle Basisangebote | Kernfunktionen | Ausdrucksbasierte Personalisierung |
| KI-Assistent für die Inhaltsgenerierung | GA | Alle Basisangebote | Kernfunktionen | Erfordert KI-Lizenzbedingungen |

>[!TAB Entscheidungsfindung]

Für alle Entscheidungsfunktionen ist das Add-on **Decisioning** erforderlich. Siehe [Pakete und Funktionen](ajo-packages.md).

| Funktion | Status | Gilt für | Verfügbar seit | Anmerkungen |
|---------|--------|-----------|-----------------|-------|
| Unterstützung von Entscheidungen im Direkt-Mail-Kanal | GA | Alle Basisangebote | &#x200B;3. Juni 2026 | Unterstützt Batch-Entscheidungen |
| Entscheidungsregeln und KI-Optimierung der Ranking-Formel | GA | Alle Basisangebote | &#x200B;5. Mai 2026 | Von KI vorgeschlagene Vereinfachungen |
| Unterstützung der Entscheidungsfindung im E-Mail-Kanal | GA | Alle Basisangebote | &#x200B;6. April 2026 | Unterstützte Mirrorseiten |
| KI-Modell-Monitoring | GA | Alle Basisangebote | &#x200B;9. März 2026 | Nur Modelle zur personalisierten Optimierung |
| Unterstützung der Entscheidungsfindung im SMS-Kanal | GA | Alle Basisangebote | &#x200B;2. Februar 2026 | – |
| Unterstützung der Entscheidungsfindung im Push-Kanal | GA | Alle Basisangebote | &#x200B;30. Januar 2026 | – |
| Adobe Experience Manager-Inhaltsfragmente in Decisioning | LA | Alle Basisangebote | &#x200B;20. Mai 2026 | Adobe-Support kontaktieren |
| Offer Decisioning (Entscheidungsrichtlinien) | GA | Alle Basisangebote | Kernfunktionen | Auswahl der besten Angebote in Echtzeit |
| KI-gestützte Rangfolge | GA | Alle Basisangebote | Kernfunktionen | Angebotsoptimierung für maschinelles Lernen |

>[!TAB KI-Agenten]

| Funktion | Status | Gilt für | Verfügbar seit | Anmerkungen |
|---------|--------|-----------|-----------------|-------|
| Journey Agent: Journey erstellen | GA | Journey; Kampagnen und Journey | Dienstag, 12. Januar 2026 | Erstellung von Journey in natürlicher Sprache |
| Journey Optimizer AI Agent-Integration über MCP | Beta | Alle Basisangebote | April 2026 | Public Beta; Claude Web und Desktop |
| Journey Agent: Kanalinhalt erstellen | LA | Alle Basisangebote | &#x200B;4. März 2026 | Adobe-Support kontaktieren |

>[!TAB Administration und Daten]

| Funktion | Status | Gilt für | Verfügbar seit | Anmerkungen |
|---------|--------|-----------|-----------------|-------|
| Zertifikatbasierte benutzerdefinierte Authentifizierung in benutzerdefinierten Aktionen | GA | Alle Basisangebote | &#x200B;4. Juni 2026 | Für zertifikatbasierte Identitäten (z. B. Microsoft Entra ID) |
| Kunden-Warnhinweise für Kampagnen-Lebenszyklusereignisse | GA | Alle Basisangebote | &#x200B;1. Juni 2026 | Abonnieren auf Sandbox-Ebene |
| URL-Parameterverschlüsselung | GA | Alle Basisangebote | &#x200B;1. Juni 2026 | Zuvor benötigt LA Registrierungsberechtigungen für Schlüssel |
| APIs für Self-Service-Migrations-Tools | GA | Alle Basisangebote | &#x200B;3. Februar 2026 | – |
| Monitoring von benutzerdefinierten Aktionen | GA | Alle Basisangebote | &#x200B;3. Februar 2026 | Zuvor LA |
| Nachrichtenexport | GA | Alle Basisangebote | &#x200B;28. Januar 2026 | Verfügbar als Add-on |
| API zum Abrufen von Aktionskampagnen | GA | Alle Basisangebote | &#x200B;24. November 2025 | – |
| Migrieren von Subdomains zur benutzerdefinierten Delegierung | LA | Alle Basisangebote | &#x200B;19. Februar 2026 | Adobe-Support kontaktieren |
| Sandboxes | GA | Alle Basisangebote | Kernfunktionen | Bis zu 5 Sandboxes; weitere verfügbar |
| Einheitliche Profile und Audiences | GA | Alle Basisangebote | Kernfunktionen | Built on Adobe Experience Platform |
| Reporting und Live-Berichte | GA | Alle Basisangebote | Kernfunktionen | – |
| Berechtigungen und Zugriffssteuerung | GA | Alle Basisangebote | Kernfunktionen | Rollenbasierter Zugriff |
| REST-APIs | GA | Alle Basisangebote | Kernfunktionen | API-First-Framework |

>[!ENDTABS]

>[!NOTE]
>
>Diese Liste wird aus den [2026-](../rn/release-notes-2026.md) und den [aktuellen Versionshinweisen](../rn/release-notes.md) zusammengestellt und enthält den neuesten bekannten Status jeder Funktion. Er ist nicht vollständig. Den vollständigen Verlauf und die neuesten Ergänzungen finden Sie immer in den [Versionshinweisen](../rn/release-notes.md).

## Verwandte Ressourcen {#related}

- **Verstehen Sie, was in Ihrem Paket enthalten ist** — [Pakete und Funktionen](ajo-packages.md)
- **Alles anzeigen, was** wurde[ — Versionshinweise](../rn/release-notes.md) | [2026 Versionshinweise](../rn/release-notes-2026.md)
- **Erste Schritte** — [Erste Schritte mit Journey Optimizer](get-started.md)
