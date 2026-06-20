---
solution: Journey Optimizer
product: journey optimizer
title: Starten Sie von Ihrem Ziel | Adobe Journey Optimizer
description: Lernen Sie die wichtigsten Anwendungsfälle kennen, für die Adobe Journey Optimizer entwickelt wurde, und erfahren Sie, welche AJO-Funktionen am besten zu den einzelnen Szenarien passen.
feature: Get Started
topic: Content Management
role: User
level: Beginner
keywords: Journey-Optimizer, Anwendungsfall, Entscheidungshandbuch, welche Funktion, Erste Schritte, Anwenderziele, Tutorials
source-git-commit: 49146a29a474a240ca1fdb10b2a6ef175f44f595
workflow-type: tm+mt
source-wordcount: '3141'
ht-degree: 31%

---

# Von Ihrem Ziel starten {#ajo-use-case-guide}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Beginnen Sie mit dem, was Sie erreichen möchten, und springen Sie dann zu der Adobe Journey Optimizer-Funktion, die sie löst - ohne den Funktionsnamen zuerst kennen zu müssen.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] bietet viele Möglichkeiten. Die richtige hängt davon ab, was Sie erreichen möchten. Dieses Handbuch ist auf Geschäftsziele und nicht auf Produktfunktionen ausgerichtet: Suchen Sie das Ziel, das Ihren Anforderungen entspricht, und folgen Sie dann dem Link, um mit der empfohlenen Funktion zu beginnen.

Verwenden Sie diese Seite als schnellen Router - scannen Sie nach Ihrem Ziel und springen Sie direkt zur richtigen Funktion. Wenn Sie gerade erst anfangen, beginnen Sie mit [Erste Schritte mit Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md) um den richtigen Einstiegspunkt für Ihre Rolle zu finden.

>[!NOTE]
>
>Schrittweise Implementierungsbeispiele finden Sie in der [Journey-Anwendungsfallbibliothek](../building-journeys/jo-use-cases.md).

Wenn für ein bestimmtes Szenario kein durchgängiges Tutorial verfügbar ist, führt Sie der Link zum besten aktuellen Ausgangspunkt, um die Funktionen zu erlernen und zu beginnen.

KI ist in viele dieser Funktionen integriert - suchen Sie in den Tabellen unten nach dem Tag **(AI**. Der Conversational [AI Assistant](ai-features.md#ai-assistant) kann auch jederzeit Produktfragen beantworten und operative Erkenntnisse über Ihre Journey aufzeigen. Die vollständige Liste der intelligenten Funktionen finden Sie unter [KI- und intelligente Funktionen](ai-features.md).

>[!TIP]
>
>Neu bei Journey Optimizer? Beginnen Sie mit [Erste Schritte mit Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md) um den richtigen Pfad für Ihre Rolle auszuwählen, und lesen Sie dann [Was ist Journey Optimizer](get-started.md) für die Grundlagen. Um praktisches Vertrauen aufzubauen, durchsuchen Sie die [Journey Optimizer-Tutorials](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} folgen Sie einer von Experten kuratierten [Video-](https://experienceleague.adobe.com/en/playlists?solution=Journey+Optimizer){target="_blank"}) und üben Sie in einer [Trainings-](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/configure-a-training-sandbox/introduction-and-prerequisites){target="_blank"} oder mit den [praktischen Herausforderungen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/challenges/introduction-and-prerequisites){target="_blank"}.

## Einrichten von Journey Optimizer für Ihr Team {#setup-admin}

Für Administratoren und technische Benutzende, die die Umgebung konfigurieren müssen, bevor sie Journey oder Kampagnen erstellen.

| Ich möchte… | Empfohlene Funktion | Hier beginnen |
| --- | --- | --- |
| Konfigurieren von E-Mail-, SMS- oder Push-Kanälen vor dem Senden | Kanalkonfiguration | [Erste Schritte mit der Kanalkonfiguration](../configuration/get-started-configuration.md) |
| Neue IP-Adresse für den E-Mail-Versand einrichten | IP-Aufwärmplan | [Erste Schritte mit IP-Aufwärmung](../configuration/ip-warmup-gs.md) |
| Einrichten von Rollen, Berechtigungen und Zugriffssteuerung | Zugriffssteuerung | [Erste Schritte mit der Zugriffskontrolle](../administration/permissions-overview.md) |
| Arbeiten über mehrere Umgebungen oder Regionen hinweg | Sandboxes | [Arbeiten mit Sandboxes](../administration/sandboxes.md) |

## Kundeninteraktion bei Ereignissen {#engage-real-time}

Für Szenarien, in denen Sie direkt auf eine Kundenaktion oder ein Kundenereignis reagieren.

| Ich möchte… | Empfohlene Funktion | Hier beginnen |
| --- | --- | --- |
| Neuen Kunden oder Abonnenten automatisch willkommen heißen | Durch Ereignis ausgelöste Journey | [Erste Schritte mit Journey](../building-journeys/journey-gs.md) ・ [Einführung in das Erstellen einer Journey](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} |

>[!BEGINSHADEBOX]

**Vor dem Build:** Stellen Sie sicher, dass Sie (1) ein [Journey-Eintrittsereignis konfiguriert haben](../event/about-events.md) um den Anmelde-Trigger zu erfassen, (2) eine [E-Mail- oder Push-](../configuration/channel-surfaces.md)-Kanaloberfläche für Ihre Sandbox eingerichtet haben und (3) mindestens ein [Testprofil](../audience/creating-test-profiles.md) verfügbar sind, um die Journey vor der Veröffentlichung zu validieren.

>[!ENDSHADEBOX]

| Ich möchte… | Empfohlene Funktion | Hier beginnen |
| --- | --- | --- |
| Wiederherstellen einer abgebrochenen Warenkorb- oder Durchsuchen-Sitzung | Durch Ereignis ausgelöste Journey | [Erste Schritte mit Journey](../building-journeys/journey-gs.md) ・ [Tutorial zum Durchsuchen von Abbrüchen](https://experienceleague.adobe.com/de/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma){target="_blank"} |

>[!BEGINSHADEBOX]

**Vor dem Build:** benötigen Sie (1) ein [Verhaltensereignis](../event/about-events.md) das die Warenkorb- oder Durchsuchen-Aktion von Ihrem Web- oder mobilen SDK erfasst, (2) eine [Warteaktivität](../building-journeys/wait-activity.md) beschlossene Strategie (in der Regel 1-4 Stunden vor dem ersten Nugge) und (3) eine Kanaloberfläche, die für die Folgenachricht bereit ist. Hinweis: Der Journey muss eine Bedingung enthalten, damit Profile, die den Kauf abschließen, vor Ablauf der Wartezeit beendet werden können.

>[!ENDSHADEBOX]

| Ich möchte… | Empfohlene Funktion | Hier beginnen |
| --- | --- | --- |
| Trigger einer Journey aus einer Website-Formularübermittlung | Durch Ereignis ausgelöste Journey | [Erste Schritte mit Journey](../building-journeys/journey-gs.md) ・ [Tutorial](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/trigger-journey-on-form-submission/introduction){target="_blank"} |
| Reagieren auf das In-App-Verhalten (Öffnen der App, Bildschirmansicht) | Journey + In-App | [Erste Schritte mit In-App](../in-app/get-started-in-app.md) |
| Bestell-, Versand- oder Terminbestätigungen senden | API-ausgelöste Kampagne | [Arbeiten mit API-ausgelösten Kampagnen](../campaigns/api-triggered-campaigns.md) |
| Erneute Interaktion mit inaktiven oder abgelaufenen Kunden | Journey + Zielgruppen | [Erste Schritte mit Profilen und Audiences](../audience/get-started-profiles.md) ・ [Erstellen von Audiences mit dem Regel-Builder](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/profiles-audiences-subscriptions/create-audiences-using-the-rule-builder){target="_blank"} |

>[!BEGINSHADEBOX]

**Vor der Erstellung:** Sie benötigen (1) eine [Zielgruppe, die in Adobe Experience Platform definiert ist](../audience/about-audiences.md), die inaktive Profile identifiziert (z. B. kein Kauf oder keine Anmeldung in 60 Tagen), (2) eine Entscheidung über den Rückgewinnungskanal (E-Mail, Push oder SMS) und (3) eine Unterdrückungsregel oder [Häufigkeitsbegrenzung](../conflict-prioritization/channel-capping.md), um die Kontaktaufnahme mit kürzlich gesendeten Profilen zu vermeiden. Verwenden Sie für **Szenario einen**-Eintrag (Zielgruppe lesen), kein Ereignis.

>[!ENDSHADEBOX]

| Ich möchte… | Empfohlene Funktion | Hier beginnen |
| --- | --- | --- |
| Testen einer Journey mit echten Daten, bevor sie aktiviert wird | Journey Probelauf | [Testen Sie Ihren Journey mit Probelauf](../building-journeys/journey-dry-run.md) |
| Live-Journey anhalten, um Änderungen vorzunehmen, ohne die Bearbeitung von In-Flight-Profilen zu stoppen | Journey pausieren und fortsetzen | [Journey anhalten und fortsetzen](../building-journeys/journey-pause.md) |
| Erstellen oder optimieren Sie eine Journey über eine Aufforderung in natürlicher Sprache | Journey Agent **(AI)** | [KI-Agenten](ai-features.md#ai-agents) ・ [Journey Agent-Tutorial](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} |

## Zielgruppen im benötigten Umfang erreichen {#reach-at-scale}

Für geplante Eins-zu-Viele-Kontakte zu einer definierten Zielgruppe.

| Ich möchte… | Empfohlene Funktion | Hier beginnen |
| --- | --- | --- |
| Senden eines Newsletters oder einer Promotion an ein Segment | Geplante Kampagne | [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md) |

>[!BEGINSHADEBOX]

**Vor dem Erstellen:** benötigen Sie (1) ein [veröffentlichtes Zielgruppensegment](../audience/about-audiences.md) in Adobe Experience Platform, (2) eine [E-Mail-Kanaloberfläche](../configuration/channel-surfaces.md) mit einer verifizierten Versand-Domain und (3) alle [Inhaltsfragmente oder Vorlagen](../content-management/fragments.md) bereits veröffentlichte Inhalte wiederzuverwenden. Geplante Kampagnen sind hier die richtige Wahl - nicht Journey - wenn es sich um einen einmaligen oder wiederkehrenden Versand ohne Verzweigungslogik handelt.

>[!ENDSHADEBOX]

| Ich möchte… | Empfohlene Funktion | Hier beginnen |
| --- | --- | --- |
| Produkt mit A/B-Test starten | Inhaltsexperiment-**(KI)** | [Erste Schritte mit Inhaltsexperimenten](../content-management/experiment-accelerator-gs.md) ・ [Erstellen von Inhaltsexperimenten für E-Mail-Kampagnen](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} |
| Kunden über einen Ausfall oder eine Service-Aktualisierung benachrichtigen | Geplante Kampagne + Audiences | [Info über Zielgruppen](../audience/about-audiences.md) |
| Entwerfen einer mehrstufigen Kampagne mit Verzweigungslogik | Orchestrierte Kampagnen | [Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md) |
| Nur Profile ansprechen, die sich seit der letzten Kampagnenausführung geändert haben | Orchestrierte Kampagnen - inkrementelle Abfrage | [Erstellen von Abfragen in orchestrierten Kampagnen](../orchestrated/build-query.md) <!-- TODO: verify target — no dedicated "incremental query" page found; build-query.md ("Build your first rule") is the closest existing page --> |
| Überprüfen Sie vor dem Start, wie viele Profile meiner Zielgruppe entsprechen. | Zielgruppenvorschau | [Über Zielgruppen](../audience/about-audiences.md) <!-- TODO: verify target — no "create-compositions.md#preview" page/anchor exists; about-audiences.md used as placeholder --> |
| Skalierte Koordination von Messaging über viele Kanäle | Orchestrierung | [Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md) ・ [Skalierung der Orchestrierung auf Omni-Channel-Interaktion](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/scaling-orchestration-to-omnichannel-engagement/introduction){target="_blank"} |
| Senden Sie für jede Kundin und jeden Kunden jede Nachricht zur besten Zeit | Sendezeit-**(KI)** | [Versandzeitoptimierung](../building-journeys/send-time-optimization.md) |

## Personalisieren, was jeder Kunde sieht {#personalize}

Für die individuelle Anpassung von Angeboten und Inhalten.

| Ich möchte… | Empfohlene Funktion | Hier beginnen |
| --- | --- | --- |
| Für jeden Kunden das beste Angebot anzeigen | Entscheidungsfindung | [Erste Schritte mit Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) ・ [Tutorial zu Web-Angeboten](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} |

>[!BEGINSHADEBOX]

**Vor dem Erstellen** Für die Entscheidungsfindung ist eine bestimmte Einrichtungssequenz erforderlich. Sie benötigen (1) [Entscheidungselemente (Angebote) ](../experience-decisioning/items.md) Eignungsregeln und -attributen, (2) eine [Auswahlstrategie](../experience-decisioning/selection-strategies.md) oder Rangfolgenformel konfiguriert und (3) eine [Entscheidungsrichtlinie](../experience-decisioning/create-decision.md), die an die Oberfläche angehängt wird, auf der Angebote angezeigt werden. Das Überspringen dieser Sequenz ist der häufigste Grund, warum Erstentscheidungs-Setups keine Ergebnisse zurückgeben.

>[!ENDSHADEBOX]

| Ich möchte… | Empfohlene Funktion | Hier beginnen |
| --- | --- | --- |
| Angebote nach einer Formel sortieren (Postleitzahl, Einkommen, Wetter) | Decisioning - Rangfolgenformel | [Rangfolgeformeln](../experience-decisioning/ranking/ranking-formulas.md) ・ [Tutorial zur Rangfolgeformel](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/personalizing-offers-with-ranking-formulas-based-on-user-zip-code-and-income/introduction){target="_blank"} ・ [Tutorial zu Wetterdaten](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction){target="_blank"} |
| Verwenden externer Produkt- oder CRM-Daten zur Personalisierung von Angeboten | Decisioning - AEP-Datensatzsuche | [Verwenden der Datensatzsuche in Decisioning](../experience-decisioning/context-data.md) |
| Nachrichteninhalt mit Profildaten anpassen | Personalisierung | [Personalisieren von Inhalten](../personalization/personalize.md) |
| Generieren von Kopien, Bildern und Nachrichtenvarianten | KI-Inhaltserstellung **(AI)** | [KI-Inhaltserstellung](../content-management/gs-generative.md) ・ [Tutorial](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} |
| Konvertieren eines Designbilds in eine bearbeitbare E-Mail-Vorlage | Bild-zu-HTML-Konvertierer **(AI)** | [Konvertieren eines Bildes in eine E-Mail-Vorlage](../content-management/image-to-html.md) |
| Angebote automatisch ordnen und personalisieren | KI-Rangfolgemodelle **(KI)** | [KI-Modelle für die Entscheidungsfindung](../experience-decisioning/ranking/ai-models.md) |
| Bereitstellung von immer verfügbaren kontextuellen Inhalten (keine Kampagne) | Inhaltskarten | [Erste Schritte mit Inhaltskarten](../content-card/get-started-content-card.md) ・ [Erstellen von Inhaltskarten](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/channels/content-cards/create-content-cards){target="_blank"} |
| Bereitstellen personalisierter Inhalte über die API für eine beliebige App oder Oberfläche | Code-basiertes Erlebnis | [Erste Schritte mit Code-basierten Erlebnissen](../code-based/get-started-code-based.md) |
| Festlegen, welche Teile einer E-Mail-Vorlage mein Team bearbeiten kann | Sperren von Inhalten | [Sperren von Inhalten in E-Mail-Vorlagen](../content-management/content-locking.md) |

## Koordinieren und Steuern des Versands {#coordinate-govern}

Zur Steuerung, wie, wann und wie oft Kunden kanalübergreifend kontaktiert werden.

| Ich möchte… | Empfohlene Funktion | Hier beginnen |
| --- | --- | --- |
| Vermeiden der Nachrichtenermüdung kanalübergreifend | Frequenzbegrenzung | [Frequenzlimitierung nach Kanal einstellen](../conflict-prioritization/channel-capping.md) |
| Konfliktende oder konkurrierende Nachrichten auflösen | Konflikt-Priorisierung | [Identifizieren potenzieller Konflikte](../conflict-prioritization/conflicts.md) ・ [Tutorial](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"} |
| Festlegen, welche Journey Vorrang hat | Journey-Schlichtung | [Formeln verwenden, um Journey zu ordnen](../conflict-prioritization/journey-ranking-formulas.md) |
| Einhalten von ruhigen Stunden und Einverständnis | Ruhige Stunden / Privatsphäre | [Einstellen ruhiger Stunden](../conflict-prioritization/quiet-hours.md) |
| Durchsetzen von Einverständnisrichtlinien und Datennutzungskennzeichnungen kanalübergreifend | Einverständnis und Data Governance | [Erste Schritte mit dem Datenschutz](../privacy/get-started-privacy.md) |
| Warnen, wenn eine Journey hohe Fehler- oder Verwerfungsraten aufweist | Journey-Warnhinweise | [Einrichten von Journey-Warnhinweisen](../reports/alerts.md) |

## Kanal auswählen, über den geliefert werden soll {#choose-channel}

| Ich möchte weiterleiten… | Kanal | Hier beginnen |
| --- | --- | --- |
| E-Mail-Newsletter, Promotions oder Transaktionsnachrichten | E-Mail | [Erste Schritte mit E-Mails](../email/get-started-email.md) |
| Mobile Push-Benachrichtigungen (iOS und Android) | Push-Benachrichtigung | [Erste Schritte mit Push-Benachrichtigungen](../push/get-started-push.md) |
| SMS, MMS oder RCS Textnachrichten | SMS/MMS/RCS | [Erste Schritte mit SMS/MMS/RCS](../mobile/get-started-mobile.md) ・ [Mobile Learning Hub](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/mobile-learning-hub/overview){target="_blank"} |
| WhatsApp-Nachrichten über die Meta Cloud-API | WhatsApp | [Erste Schritte mit WhatsApp](../whatsapp/get-started-whatsapp.md) |
| In-Browser- oder In-App-Überlagerungen und Banner | In-App | [Erste Schritte mit In-App](../in-app/get-started-in-app.md) |
| Personalisierte Inhalte von Web-Seiten | Web | [Erste Schritte mit dem Web-Kanal](../web/get-started-web.md) |
| Beliebige Oberfläche über API (Kiosk, angeschlossenes Gerät, Headless-App) | Code-basiertes Erlebnis | [Erste Schritte mit Code-basierten Erlebnissen](../code-based/get-started-code-based.md) |
| Von einer Journey ausgelöste physische Postsendungen | Briefpost | [Erste Schritte mit Briefpost](../direct-mail/get-started-direct-mail.md) |

## Messen und optimieren {#measure-optimize}

Für die Verfolgung der Leistung, die Diagnose von Problemen und die Verbesserung der Ergebnisse im Laufe der Zeit.

| Ich möchte… | Empfohlene Funktion | Hier beginnen |
| --- | --- | --- |
| Siehe Leistungsmetriken für eine Live-Journey oder -Kampagne | Live-Berichte | [Live-Berichte](../reports/live-report.md) ・ [Überwachen und Analysieren Ihres Journey mit Live-Berichten](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} |
| Bericht über die vollständige Kampagnen- oder Journey-Performance nach Beendigung | Allgemeine Berichte | [Erste Schritte mit Reporting](../reports/gs-reports.md) |
| Analysieren eines Experiments und Abrufen von Empfehlungen für den nächsten Schritt | Experimentation Agent **(AI)** | [Experimentation Agent](ai-features.md#experimentation-agent) ・ [Tutorial](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/experimentation/experimentation-agent-overview){target="_blank"} |
| Überwachen des Zustands und der Latenz benutzerdefinierter Aktionen in meinen Journeys | Monitoring von benutzerdefinierten Aktionen | [Verwenden benutzerdefinierter Aktionen](../building-journeys/using-custom-actions.md) <!-- TODO: verify target — no dedicated "custom-action-monitoring.md" page found; using-custom-actions.md is the closest existing page --> |
| Warnen, wenn Journey-Fehler- oder Verwerfungsraten die Schwellenwerte überschreiten | Journey-Warnhinweise | [Einrichten von Journey-Warnhinweisen](../reports/alerts.md) |

## Starter-Flüsse {#starter-flows}

Jeder Starterfluss im Folgenden ist ein kurzer, ergebnisorientierter Satz von Schritten: Was Sie aufbauen werden, für wen es gedacht ist und wie Sie dorthin gelangen. Wählen Sie das Ziel aus, das Ihrem ersten Projekt entspricht, und folgen Sie den Links zur detaillierten Dokumentation.

### Neue Kunden begrüßen {#flow-welcome}

**Sie werden Folgendes erstellen:** Eine automatisierte Begrüßungsreihe, die alle neuen Abonnenten begrüßt und inaktive abstößt.
**Am besten geeignet für:** Marketingexperten ・ **Funktion:** Ereignisausgelöster Journey

1. Bestätigen Sie[ dass Ihre einheitlichen Profile und ](../audience/get-started-profiles.md) das Registrierungsereignis erhalten.
1. [Erstellen Sie Ihre erste ](../building-journeys/journey-gs.md) und verwenden Sie das Registrierungsereignis als Eintrag.
1. Fügen Sie eine Begrüßungs[E-Mail](../email/get-started-email.md), dann einen Warteschritt und eine Folgenachricht [Push-Benachrichtigung](../push/get-started-push.md) für Profile hinzu, die nicht interagiert haben.
1. [Personalisieren des Inhalts](../personalization/personalize.md) mit Profilattributen wie Vorname und angegebenen Interessen.

➡️ [Beginnen Sie mit Journey](../building-journeys/journey-gs.md)

### Wiederherstellen von Transaktionsabbrüchen {#flow-cart}

**Sie erstellen Folgendes:** Ein automatisierter Wiederherstellungsfluss, der Kunden an zurückgelassene Elemente erinnert.
**Am besten geeignet für:** Marketingexperten ・ **Funktion:** Ereignisausgelöster Journey

1. Stellen Sie sicher, dass das Warenkorbabbruchs-Ereignis Journey Optimizer erreicht (wenden Sie sich bei Bedarf an Ihr [Daten-](../data/gs-data.md)).
1. [Erstellen einer Journey](../building-journeys/journey-gs.md) ausgelöst durch das Abbruchereignis.
1. Senden Sie eine personalisierte Erinnerungs-E-Mail. Wenn innerhalb von 24 Stunden kein Klick erfolgt, verzweigen Sie zu einem [Push](../push/get-started-push.md)-Follow-up.
1. [Personalisieren](../personalization/personalize.md) mit den abgebrochenen Elementen und dem Treuestatus.

➡️ [Beginnen Sie mit Journey](../building-journeys/journey-gs.md)

### Senden von Transaktionsnachrichten {#flow-transactional}

**Sie erstellen:** On-Demand-Bestellungen, Versandbestätigungen oder Terminbestätigungen, die von einem externen System ausgelöst werden.
**Am besten geeignet für:** Marketing-Experten und Entwickler ・ **Funktion:** Kampagne, die von einem externen System ausgelöst wird

1. Überprüfen Sie, [ Kampagnen, die von einem externen System ausgelöst ](../campaigns/api-triggered-campaigns.md), funktionieren und welche Payload sie erwarten.
1. Gestalten Sie die Nachrichtenvorlage und [ Sie ](../personalization/personalize.md) mit den Transaktionsdetails.
1. Bitten Sie Ihren Entwickler, den Campaign-Endpunkt aus Ihrem Auftrags- oder Erfüllungssystem aufzurufen.

➡️ [Arbeiten mit Kampagnen, die von einem externen System ausgelöst werden](../campaigns/api-triggered-campaigns.md)

### Starten einer Kampagne mit Inhaltstests {#flow-campaign}

**Sie erstellen:** Eine geplante Promotion, die automatisch die Inhalte mit der besten Leistung auswählt.
**Am besten geeignet für:** Marketingexperten ・ **Funktion:** Geplante Kampagne + Inhaltsexperiment

1. [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md) und Definieren Ihrer Audience.
1. Verwenden Sie [Inhaltserstellung](../content-management/gs-generative.md), um die Betreffzeile zu entwerfen und Varianten zu kopieren.
1. Richten Sie ein [Inhaltsexperiment](../content-management/experiment-accelerator-gs.md) ein, um Varianten eines Beispiels zu testen, und senden Sie dann den Gewinner an den Rest.

➡️ [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md)

### Angebote pro Kunde personalisieren {#flow-offers}

**Sie erstellen:** Eine Entscheidung, die jedem Kunden das beste Einzelangebot zeigt.
**Am besten geeignet für:** Marketing-Experten ・ **Funktion:** Decisioning

1. [Erste Schritte mit Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) und erstellen Sie Ihre Angebote und Eignungsregeln.
1. Fügen Sie die Entscheidung einer [Journey](../building-journeys/journey-gs.md) oder Kampagnennachricht hinzu.
1. Ebene in [intelligenten Funktionen](ai-features.md) um Angebote automatisch zu ordnen und zu optimieren.

➡️ [Erste Schritte mit Offer Decisioning](../offers/get-started/starting-offer-decisioning.md)

## Beispielszenarien {#example-scenarios}

Diese Beispiele veranschaulichen, wie die Funktionen von Journey Optimizer in verschiedenen Rollen, Branchen und Kanälen zusammenarbeiten.

### Rückerstattung für verzögerte Sendungen {#scenario-delayed-shipment}

**Rolle:** Marketing-Fachkraft | **Kernfunktion:** [Einheitliches Profil + Zielgruppenausschluss](../audience/get-started-profiles.md)

Ein Bekleidungsgeschäft versendet in der Regel nach dem Kauf eine Umfrage an alle Kundinnen und Kunden, die in der letzten Woche Produkte erworben haben. Aufgrund des schlechten Wetters kam es bei einigen Lieferungen zu Verspätungen. Da das Bekleidungsgeschäft weiß, welche Kundinnen und Kunden ihre Lieferungen nicht erhalten haben, kann es diese vom geplanten Versand der Zufriedenheitsumfrage ausschließen. Stattdessen kann es eine personalisierte E-Mail versenden, in der es sich für die Verzögerung entschuldigt, und einen Rabatt-Code mit Produktempfehlungen einfügen, die auf früheren Käufen der Kundin bzw. des Kunden basieren.

[Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md)

### Echtzeit-Interaktion in Geschäften {#scenario-instore}

**Rolle:** Marketing-Fachkraft | **Kernfunktion:** [Geofence-Auslösung + Push](../push/get-started-push.md)

Dieselbe retailer kann einen treuen Kunden ansprechen, der auf den Parkplatz eines Geschäfts einbiegt, indem er ihm eine Push-Benachrichtigung über einen Pullover sendet, der wieder in der Größe des Kunden vorrätig ist.

[Erste Schritte mit Push-Benachrichtigungen](../push/get-started-push.md)

### Wiederherstellung bei Warenkorbabbruch {#scenario-cart}

**Rolle:** Marketing-Fachkraft | **Kernfunktion:** [Durch Ereignis ausgelöste mehrstufige Journey](../building-journeys/journey-gs.md)

Wenn ein Kunde Artikel in einen Online-Warenkorb legt, den Kauf jedoch nicht abschließt, erkennt Journey Optimizer das Ereignis und startet automatisch eine Wiederherstellungs-Journey. Die Person erhält eine personalisierte E-Mail, in der sie an die zurückgelassenen Artikel erinnert wird. Wenn sich die Person nicht innerhalb von 24 Stunden durchklickt, wird eine Folge-Push-Benachrichtigung gesendet, die basierend auf dem Browser-Verlauf und Treuestatus personalisiert wird.

[Erstellen Ihrer ersten Journey](../building-journeys/journey-gs.md)

### Begrüßungsserie für den Streaming-Service {#scenario-welcome}

**Rolle:** Marketing-Fachkraft | **Kernfunktion:** [Durch Ereignis ausgelöste Begrüßungs-Journey](../building-journeys/journey-gs.md)

Wenn eine Person einen Streaming-Service abonniert, erkennt Journey Optimizer das Registrierungsereignis und startet sofort eine mehrstufige Begrüßungs-Journey. Die Person erhält eine Begrüßungs-E-Mail, in der sie aufgefordert wird, die App zum ersten Mal zu öffnen. Wenn innerhalb von 48 Stunden keine Anmeldeaktivität erkannt wird, wird eine Folge-Push-Benachrichtigung mit personalisierten Inhaltsempfehlungen gesendet, die auf den bei der Registrierung angegebenen Interessen basieren. So werden passive Abonnierende vom ersten Tag an zu aktiven, interaktiven Benutzenden.

[Erstellen Ihrer ersten Journey](../building-journeys/journey-gs.md)

### Reservierungserinnerung mit Wegbeschreibung {#scenario-reservation}

**Rolle:** Marketing-Fachkraft | **Kernfunktion:** [Geplantes + standortbezogenes Messaging](../campaigns/get-started-with-campaigns.md)

Eine Marke im Gastgewerbe sendet allen Gästen eine Stunde vor ihrer Reservierung eine rechtzeitige Erinnerung. Die Benachrichtigung enthält den Namen des Gastes, die Reservierungszeit und die standortbasierte Wegbeschreibung zum Ort. Dies wird automatisch aus den Daten im Kundenprofil und der Buchung zusammengestellt, ohne dass manueller Aufwand des Marketing-Teams notwendig ist.

[Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md)

### Proaktive Benachrichtigung zu Service-Ausfall {#scenario-outage}

**Rolle:** Operations | **Kernfunktion:** [Automatisierte Zielgruppenauswahl im benötigten Umfang](../audience/about-audiences.md)

Wenn eine Service-Unterbrechung auftritt, identifiziert Journey Optimizer die betroffenen Personen automatisch anhand ihrer Kontodaten und Nutzungsmuster. Diese Personen erhalten eine proaktive Benachrichtigung, in der das Problem geschildert und die nächsten Schritte erläutert werden. Dies wandelt ein potenziell negatives Erlebnis in einen transparenten Moment um, der Vertrauen schafft und im benötigten Umfang bereitgestellt wird.

[Erstellen Ihrer ersten Journey](../building-journeys/journey-gs.md)

### Intelligente Werbekampagne {#scenario-ai-campaign}

**Rolle:** Marketing-Experte | **Kernfunktion:** [Inhaltserstellung + Experimentieren](ai-features.md)

Eine Einzelhandelsmarke, die eine Produkteinführung plant, verwendet den KI-Assistenten von Journey Optimizer, um mehrere Betreffzeilen- und Textkörpervarianten innerhalb weniger Minuten zu generieren, und zwar basierend auf einem Prompt in natürlicher Sprache und den hochgeladenen Markenrichtlinien. Integrierte Inhaltsexperimente identifizieren automatisch die leistungsstärkste Variante in einer anfänglichen Auswahl an Zielgruppen. Die erfolgreichste Nachricht wird dann an die verbleibenden Empfangenden gesendet, wodurch die Interaktion ohne zusätzlichen Texterstellungsaufwand maximiert wird.

[Intelligente Funktionen entdecken](ai-features.md) | [Erfahren Sie mehr über Inhaltsexperimente](../content-management/experiment-accelerator-gs.md)

### Wartungswarnhinweise über App {#scenario-maintenance}

**Rolle:** Operations | **Kernfunktion:** [Nicht-Marketing-Journey-Orchestrierung](../building-journeys/journey-gs.md)

Nicht-Marketing-Fachleute wie Operations- und Support-Teams können [!DNL Adobe Journey Optimizer] verwenden, um betriebliche Benachrichtigungen zu verwalten oder Onboarding-Prozesse zu überwachen. Beispielsweise kann Wartungspersonal eines Vergnügungsparks, in dem Besuchende eine App als Teil ihres Erlebnisses herunterladen, Journey Optimizer verwenden, um Besuchende des Parks über Attraktionen zu informieren, die aufgrund von Wartungsarbeiten derzeit geschlossen sind.

[Erstellen Ihrer ersten Journey](../building-journeys/journey-gs.md)

## Videobibliothek {#videos}

Durchsuchen kuratierter Videoinhalte nach Thema. Jede Registerkarte ist mit den entsprechenden Tutorials und Wiedergabelisten auf Experience League verknüpft.

>[!BEGINTABS]

>[!TAB Erste Schritte]

* [Einführung in Journey Optimizer](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"} - Grundlegende Konzepte und eine Produkttour.
* [Übersicht über Journey Optimizer-Tutorials](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} - Der vollständige Katalog mit geführten Videos.

>[!TAB Journey und Kampagnen]

* [Einführung in das Erstellen einer Journey](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} - Erstellen Sie Ihre erste ereignisgesteuerte Journey.
* [Mit Journey Agent Journey erstellen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} - Erstellen Sie Journey anhand einer Aufforderung in natürlicher Sprache.

>[!TAB Personalization und Intelligence]

* [KI-Assistent für die Inhaltserstellung](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} - Generieren von Kopien, Bildern und Varianten.
* [Verwenden von Decisioning zur Personalisierung von Web](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"}Angeboten - Angebote nach Kunde anpassen.

>[!TAB Reporting und Optimierung]

* [Überwachen und Analysieren Ihres Journey mit Live-Berichten](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} - Verfolgen Sie die Performance während der Ausführung Ihrer Journey.
* [Erstellen von Inhaltsexperimenten für E-Mail](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"}-Kampagnen - Testen und Optimieren von Inhalten.

>[!ENDTABS]

## Auswahl zwischen Journey, Kampagnen und koordinierten Kampagnen {#choosing}

| Szenario | Verwenden von |
| -------- | --- |
| Verhaltensgesteuert und in mehreren Schritten: Jeder Kunde bewegt sich in seinem eigenen Tempo | Journey |
| Einfache geplante oder durch eine API ausgelöste Nachricht an eine Zielgruppe | Campaign |
| Komplexer Batch-Workflow mit Segmentierung mehrerer Entitäten | Orchestrierte Kampagne |

## Nicht sicher? {#not-sure}

Wenn Ihr Produktziel einem Begriff zugeordnet ist, mit dem Sie nicht vertraut sind, oder Sie sich nicht sicher sind, auf welche Funktion die Tabelle verweist, beginnen Sie mit der Seite [Journey Optimizer-Schlüsselterminologie](terminology.md), um die Konzepte hinter den einzelnen Funktionen zu verdeutlichen.

Mit den durchgängigen Übungen in den [Journey Optimizer-Tutorials} können Sie auch praktisches Vertrauen ](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}.
