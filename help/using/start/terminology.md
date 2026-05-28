---
solution: Journey Optimizer
product: journey optimizer
title: Wichtige Terminologie
description: Grundlegende Begriffe und Konzepte in Adobe Journey Optimizer
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 14e72376-87ad-4fae-bf8c-f347109d7903
TQID: https://experienceleague.adobe.com/-aDvt4RUXyf0EnPfFTJkG1CvWgte-1Fr6YaWvgcNNu4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 0047bf4386b33c99fded37750e24ed9fbf4188f6
workflow-type: tm+mt
source-wordcount: 1569
ht-degree: 33%

---

# Wichtige Terminologie {#key-terminology}

In diesem Referenzhandbuch werden die wichtigsten Begriffe definiert, die bei der Verwendung von Adobe Journey Optimizer vorkommen. Wenn Sie diese Konzepte verstehen, können Sie sicher auf der Plattform navigieren und effektiv mit Ihrem Team zusammenarbeiten.

Für Paare ähnlich klingender Begriffe, die häufig verwechselt werden - z. B. **Entscheidungs- vs. Entscheidungs** Management oder **Inhaltskarten vs. In-App-Nachrichten** -, lesen Sie [Wenn Begriffe ähnlich &#x200B;](#disambiguation) unten auf dieser Seite.

>[!NOTE]
>
>Adobe Journey Optimizer basiert auf **Adobe Experience Platform**. Viele grundlegende Konzepte, auf die Sie stoßen werden - wie Echtzeit-Kundenprofile, Sandboxes, Schemata und Datensätze - sind Adobe Experience Platform-Konzepte, nicht Journey Optimizer-spezifische. Definitionen dieser Begriffe finden Sie im [Adobe Experience Platform-Glossar](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html?lang=de){target="_blank"}.

## Journey- und Kampagnenbedingungen {#journey-campaign-terms}

| Begriff | Definition |
|------|------------|
| **Journey** | Eine Reihe miteinander verbundener Schritte, um Kundinnen und Kunden im Zeitverlauf durch Erlebnisse mit Ihrer Marke zu führen. Jeder Schritt basiert auf Kundenaktionen oder zeitbasierten Triggern und ermöglicht sequenzielle, personalisierte Interaktionen. [Weitere Informationen](../building-journeys/journey.md) |
| **Kampagne** | Eine koordinierte Marketing-Aktion, die Inhalte für eine bestimmte Zielgruppe über einen oder mehrere Kanäle bereitstellt. Im Gegensatz zu Journey führen Kampagnen Aktionen gleichzeitig aus. Journey Optimizer unterstützt drei Kampagnentypen: **Aktionskampagnen** (geplante Batch-Sendungen), **API-ausgelöste Kampagnen** (Echtzeit, ereignisgesteuertes Messaging über die API) und **Orchestrierte Kampagnen** (komplexe, mehrstufige Workflows mit einer visuellen Arbeitsfläche). [Weitere Informationen](../campaigns/get-started-with-campaigns.md) |
| **Ereignis** | Eine Aktion oder ein Auftreten, durch die bzw. das eine Journey ausgelöst oder fortgesetzt wird. Bei Ereignissen kann es sich um Kundenaktionen (einen Kauf tätigen, einen Warenkorb verlassen) oder Systemereignisse (Datum/Uhrzeit, Datenänderung) handeln. [Weitere Informationen](../event/about-events.md) |
| **Kanal** | Die Methode, die zur Kommunikation mit Kundinnen und Kunden verwendet wird: E-Mail, SMS, Push-Benachrichtigungen, In-App-Nachrichten, Web oder Direkt-Mail. Jeder Kanal erfordert eine bestimmte Konfiguration. [Weitere Informationen](../configuration/get-started-configuration.md) |

## Begriffe für Kunden und Zielgruppen {#customer-audience-terms}

| Begriff | Definition |
|------|------------|
| **Zielgruppe** | Eine Gruppe von Kundinnen und Kunden, die gemeinsame Merkmale oder Verhaltensweisen aufweisen, z. B. „Personen, die in den letzten 30 Tagen etwas gekauft haben“ oder „Mitglieder des Treueprogramms“. Zielgruppen werden verwendet, um bestimmte Kundensegmente anzusprechen. [Weitere Informationen](../audience/about-audiences.md) |
| **Zielgruppenqualifizierung** | Der Prozess, der abläuft, wenn eine Kundin bzw. ein Kunde in eine Zielgruppe eintritt oder sie verlässt. Journey Optimizer kann Aktionen auslösen, wenn eine Person in eine Zielgruppe eintritt oder sie verlässt, um eine zeitnahe und relevante Kommunikation sicherzustellen. [Weitere Informationen](../building-journeys/audience-qualification-events.md) |
| **Kontaktierbare Zielgruppe** | Die Anzahl der Kundenprofile, mit denen Sie sich basierend auf Ihrer Lizenzvereinbarung aktiv über Adobe Journey Optimizer in Verbindung setzen können. Dies bezieht sich in der Regel auf Profile, mit denen Sie innerhalb der letzten 12 Monate interagiert haben. |
| **Testprofil** | Fiktive Profile, die zum Testen und zur Vorschau von Nachrichten verwendet werden, bevor sie an echte Kundschaft gesendet werden. Mit Testprofilen können Sie Personalisierung, Inhalte und Journey-Logik prüfen. [Weitere Informationen](../audience/creating-test-profiles.md) |

## Begriffe für Inhalt und Personalisierung {#content-terms}

| Begriff | Definition |
|------|------------|
| **Personalisierung** | Der Prozess der Anpassung von Inhalten an einzelne Kundinnen und Kunden anhand ihrer Profildaten, Präferenzen und Verhaltensweisen. Beispielsweise das Einfügen eines Kundennamens oder das Anzeigen von Produktempfehlungen basierend auf dem Navigationsverlauf. [Weitere Informationen](../personalization/personalize.md) |
| **Inhaltsvorlage** | Ein wiederverwendbares Nachrichten-Design, das in mehreren Kampagnen und Journeys verwendet werden kann, um die Markenkonsistenz zu wahren und die Inhaltserstellung zu beschleunigen. [Weitere Informationen](../content-management/content-templates.md) |
| **Fragment** | Ein wiederverwendbarer Inhaltsbaustein (z. B. Kopfzeile, Fußzeile oder Werbe-Banner), der für mehrere Nachrichten verwendet werden kann, um Konsistenz zu gewährleisten und zentralisierte Aktualisierungen zu ermöglichen. [Weitere Informationen](../content-management/fragments.md) |
| **Landingpage** | Eine eigenständige Web-Seite, auf der Kundinnen und Kunden sich für die Kommunikation anmelden oder abmelden, Services abonnieren oder Informationen über Online-Formulare bereitstellen können. [Weitere Informationen](../landing-pages/get-started-lp.md) |
| **Inhaltsexperiment** | Ein Framework für A/B-Tests, das eine Zielgruppe in zufällige Gruppen aufteilt und für jede Gruppe verschiedene Nachrichtenvarianten (Inhalt, Betreffzeile oder Angebot) bereitstellt und dann anhand einer definierten Erfolgsmetrik die Variante mit der besten Performance identifiziert. [Weitere Informationen](../content-management/get-started-experiment.md) |
| **Experimentieren** | Die umfassendere Funktion in Journey Optimizer zum Testen und Optimieren von Entscheidungen: Inhaltsexperimente testen Nachrichtenvarianten in Kampagnen und Journey, während Entscheidungsexperimenttests Auswahlstrategien bieten. Beide nutzen statistische Analysen, um erfolgreiche Ansätze zu ermitteln. [Weitere Informationen](../content-management/get-started-experiment.md) |

## Entscheidungs- und Angebotsbedingungen {#decision-terms}

| Begriff | Definition |
|------|------------|
| **Entscheidungsfindung** | Das Entscheidungsframework der aktuellen Generation in Journey Optimizer, das für neue Implementierungen empfohlen wird. Bietet eine schemabasierte Elementkatalogverwaltung, flexible Sammlungsregeln, wiederverwendbare Entscheidungskomponenten und Experimentierfunktionen. Verfügbar für Code-basiertes Erlebnis, Push, SMS und E-Mail. [Weitere Informationen](../experience-decisioning/gs-experience-decisioning.md) |
| **Entscheidungs-Management** | Die alte Offer Decisioning-Funktion in Journey Optimizer. Verwendet eine zentrale Bibliothek mit Marketing-Angeboten und eine regelbasierte Entscheidungs-Engine, die Einschränkungen auf Echtzeit-Kundenprofile anwendet. Wird weiterhin für bestehende Implementierungen unterstützt, aber neue Implementierungen sollten stattdessen Decisioning verwenden. Unterstützt E-Mail, In-App, Push, SMS und Briefpost. [Weitere Informationen](../offers/get-started/starting-offer-decisioning.md) |
| **Angebot** | Eine Marketing-Nachricht, ein Rabatt oder eine Promotion, die bzw. der Kundinnen und Kunden präsentiert werden kann. Angebote beinhalten Eignungsregeln, die bestimmen, welche Personen sie erhalten können. [Weitere Informationen](../offers/offer-library/creating-personalized-offers.md) |
| **Entscheidungsrichtlinie** | Eine Reihe von Regeln und Strategien, die basierend auf Einschränkungen wie Berechtigung, Priorität und Begrenzungsregeln bestimmen, welches Angebot welcher Person zu welchem Zeitpunkt angezeigt werden soll. [Weitere Informationen](../experience-decisioning/create-decision.md) |

## Daten- und Konfigurationsbedingungen {#data-config-terms}

| Begriff | Definition |
|------|------------|
| **Kanalkonfiguration** | Die Einstellungen, die definieren, wie Nachrichten für einen bestimmten Kanal bereitgestellt werden - einschließlich Absenderdetails, Subdomain, IP-Pool und Nachrichtentyp (Marketing oder Transaktion). Zuvor in der älteren Dokumentation als „Oberfläche“ oder „Voreinstellung“ bezeichnet. [Weitere Informationen](../configuration/channel-surfaces.md) |
| **Unterdrückungsliste** | Eine Liste der E-Mail-Adressen und Domains, die aufgrund von Hardbounces, Spam-Beschwerden oder manuellen Ergänzungen automatisch vom Nachrichtenversand ausgeschlossen werden. Das Senden an unterdrückte Adressen wird blockiert, um die Zustellbarkeit und die Reputation des Absenders zu schützen. [Weitere Informationen](../reports/suppression-list.md) |

## Konflikt- und Prioritätsbegriffe {#conflict-terms}

| Begriff | Definition |
|------|------------|
| **Regelsatz** | Eine benannte Gruppe von Geschäftsregeln, die auf Journey und Kampagnen angewendet werden und das Verhalten von Nachrichten steuern. Ein Regelsatz kann Frequenzlimitierung, Journey-Eingabebeschränkungen und Ruhezeiten in einer einzigen wiederverwendbaren Richtlinie kombinieren. [Weitere Informationen](../conflict-prioritization/rule-sets.md) |
| **Frequenzlimitierung** | Eine Regel innerhalb eines Regelsatzes, die begrenzt, wie viele Nachrichten ein Profil innerhalb eines bestimmten Zeitraums pro Kanal oder Kommunikationstyp (Verkauf, Werbung usw.) empfangen kann. Profile, die die Obergrenze überschreiten, werden automatisch vom Versand ausgeschlossen. [Weitere Informationen](../conflict-prioritization/channel-capping.md) |

## Wenn Begriffe ähnlich aussehen: Leitfaden für die Begriffsklärung {#disambiguation}

Adobe Journey Optimizer ist über mehrere Jahre gewachsen, was bedeutet, dass einige Funktionsbereiche ähnliche Namen haben. Verwenden Sie die folgenden Tabellen, um schnell zu ermitteln, welche Funktion Ihren Anforderungen entspricht.

### Entscheidungs- vs. Entscheidungs-Management {#decisioning-vs-dm}

Beide Funktionen wählen Angebote aus und stellen sie bereit, sie dienen jedoch verschiedenen Phasen des Produktlebenszyklus.

| | Entscheidungsfindung | Entscheidungs-Management |
|---|---|---|
| **Status** | Aktuell — Wird für alle neuen Implementierungen empfohlen | **Legacy** - wird weiterhin unterstützt, wird aber für neue Implementierungen nicht mehr empfohlen |
| **Artikelkatalog** | Schemabasierte, flexible Metadaten | Zentralisierte Angebotsbibliothek |
| **Unterstützte Kanäle** | Code-basiertes Erlebnis, Push, SMS, E-Mail | E-Mail, In-App, Push, SMS, Briefpost |
| **Wichtigstes Unterscheidungsmerkmal** | Wiederverwendbare Entscheidungskomponenten, Experimentieren, umfassendere Kanal-Roadmap | Bewährte Einschränkungs-Engine; Migration zu Decisioning für neue Projekte |
| **Erste Schritte** | [Entscheidungsfindung](../experience-decisioning/gs-experience-decisioning.md) | [Entscheidungs-Management](../offers/get-started/starting-offer-decisioning.md) |

Wenn Sie derzeit Entscheidungs-Management verwenden und wechseln möchten, lesen Sie den [Migrationshandbuch](../experience-decisioning/migrate-to-decisioning.md).

### Kampagnentypen {#campaign-types-disambiguation}

Journey Optimizer bietet drei Kampagnentypen, die unterschiedlich aktiviert werden und unterschiedliche Anwendungsfälle unterstützen.

| | Aktionskampagnen (geplante Kampagnen) | Durch API ausgelöste Kampagnen | Orchestrierte Kampagnen |
|---|---|---|---|
| **Aktivierung** | Manuell oder geplant | Externer API-Aufruf | Visuelle Workflow-Arbeitsfläche |
| **Geeignet für** | Einmalige oder wiederkehrende Batch-Sendungen (Newsletter, Werbeaktionen) | Ereignisgesteuertes Messaging in Echtzeit (Bestellbestätigungen, Zurücksetzen des Kennworts) | Komplexe, mehrstufige kanalübergreifende Programme |
| **Personalization-Quelle** | Profilattribute | Profilattribute + API-Payload-Kontext | Profilattribute + relationale Daten |
| **Erste Schritte** | [Aktionskampagnen](../campaigns/create-campaign.md) | [API-ausgelöste Kampagnen](../campaigns/api-triggered-campaigns.md) | [Orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md) |

Eine vollständige Übersicht über alle Kampagnentypen und deren Verwendung finden Sie unter [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md).

### Frequenzlimitierung vs. Journey-Schlichtung {#capping-vs-arbitration}

Bei beiden handelt es sich um regelbasierte Mechanismen im Rahmen des Toolsets für Konflikte und Priorisierung , die jedoch unterschiedliche Probleme angehen.

| | Frequenzbegrenzung | Journey-Schlichtung |
|---|---|---|
| **Problem, das dadurch gelöst wird** | Ein Profil erhält im Laufe der Zeit zu viele Nachrichten | Ein Profil ist für mehrere Journey gleichzeitig qualifiziert |
| **Perimeter** | Pro Kanal und Kommunikationstyp (Verkauf, Werbung usw.) | Journey-Registrierung — Anzahl der gleichzeitigen Journey oder welche Journey gewinnt |
| **Mechanismus** | Begrenzt die Anzahl der Nachrichten pro Zeitraum und schließt zu viele Profile automatisch aus | Verwendet Prioritätswerte und Begrenzungsregeln, um zu entscheiden, auf welche Journey ein Profil zugreift |
| **Konfiguriert in** | Regelsätze → Frequenzlimitierung | Regelsätze → Journey-Begrenzung und Schlichtung |
| **Weitere Informationen** | [Frequenzlimitierung nach Kanal einstellen](../conflict-prioritization/channel-capping.md) | [Verwalten von Journey-Begrenzung und Schlichtung](../conflict-prioritization/journey-capping.md) |

### Inhaltskarten im Vergleich zu In-App-Nachrichten {#content-cards-vs-in-app}

Beide Kanäle liefern Nachrichten innerhalb einer Mobile App oder Web-Anwendung, haben jedoch unterschiedliche Rendering-Modelle und Persistenzverhalten.

| | Inhaltskarten | In-App-Nachrichten |
|---|---|---|
| **Anzeigemodell** | Beständige Karten, die in die App-Benutzeroberfläche eingebettet sind (Feed, Posteingang oder benutzerdefinierte Oberfläche) | Überlagerte Überlagerungen, Banner oder Modale, die über der App angezeigt werden |
| **Persistenz** | Sichtbar, bis explizit abgelehnt oder abgelaufen | Verschwindet, nachdem der Benutzer interagiert oder es geschlossen hat |
| **Trigger** | SDK wird beim Laden gerendert. Regeln steuern die Anzeige und die Beendigung | Ein Echtzeit-Ereignis im Versand von Journey- oder Campaign-Triggern |
| **Geeignet für** | Laufende Promotions, Treuestatus, persistente Warnhinweise | Onboarding-Tipps, zeitlich begrenzte Angebote, vorübergehende Benachrichtigungen |
| **Erste Schritte** | [Inhaltskarten](../content-card/create-content-card.md) | [In-App-Nachrichten](../in-app/get-started-in-app.md) |

>[!NOTE]
>
>**Adobe Journey Optimizer vs. Journey Optimizer B2B edition:** Hierbei handelt es sich um zwei separate Produkte innerhalb derselben Markenfamilie. Adobe Journey Optimizer (diese Dokumentation) richtet sich an B2C-Kunden-Journey. Journey Optimizer B2B edition wurde speziell für Account-basiertes Marketing entwickelt und arbeitet mit Einkaufsgruppen und Account-Zielgruppen. Wenn Sie nach B2B edition-Dokumentation suchen, besuchen Sie das [Handbuch zu Journey Optimizer B2B edition](https://experienceleague.adobe.com/de/docs/journey-optimizer-b2b/user/guide-overview){target="_blank"}.

## Verwandte Themen {#related-topics}

* [Funktionsweise von Journey Optimizer](understanding-ajo.md) - Erfahren Sie, wie Journey, Kampagnen, Profile und Kanäle in der Produktarchitektur zusammenpassen.
* [Erste Schritte mit Entscheidungsfunktionen](../experience-decisioning/gs-decision.md) - Vergleichen Sie Entscheidungsfindung und Entscheidungs-Management nebeneinander und wählen Sie den richtigen Ansatz für Ihre Implementierung aus.
* [Erste Schritte mit Journey](../building-journeys/journey.md) - Erfahren Sie, wie Sie ereignisgesteuerte, sequenzielle Kundenerlebnisse Schritt für Schritt erstellen.
* [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md) - Verstehen Sie die drei Kampagnentypen (Aktion, API-ausgelöst, orchestriert) und wann jede verwendet werden sollte.
* [Konfliktmanagement und &#x200B;](../conflict-prioritization/gs-conflict-prioritization.md) - Erfahren Sie, wie Sie Regelsätze, Frequenzlimitierungen, Prioritätswerte und ruhige Stunden verwenden können, um Übernachrichten zu vermeiden.
* [Erste Schritte mit Kommunikationskanälen](../channels/gs-channels.md) - Durchsuchen Sie alle verfügbaren Kanäle und sehen Sie sich deren Voraussetzungen und deren Konfiguration an.
