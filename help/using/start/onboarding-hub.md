---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer Onboarding-Hub
description: Ein kuratierter Onboarding-Hub für Adobe Journey Optimizer, der Schritt-für-Schritt-Anweisungen, Anwendungsfälle aus der Praxis und Videoinhalte zusammenführt, damit neue Benutzende schnell anfangen und ihr erstes Kundenerlebnis bereitstellen können.
feature: Get Started
topic: Content Management
role: User
level: Beginner
hide: true
keywords: Journey Optimizer, Onboarding, Onboarding-Hub, Anwendungsfälle, Videos, Tutorials, Erste Schritte, Anlauf, erste Journey
source-git-commit: 7af5076bb9a394110de6400991285ab2be86962d
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 12%

---

# Journey Optimizer Onboarding-Hub {#onboarding-hub}


>[!BEGINSHADEBOX]

**Auf dieser Seite:** Ramp up on Adobe Journey Optimizer fast - Sehen Sie sich eine kurze Einführung an, folgen Sie den schrittweisen Anweisungen, um Ihr erstes Erlebnis zu versenden, durchsuchen Sie Anwendungsfälle in der realen Welt und gehen Sie in kuratierte Videoinhalte ein.

>[!ENDSHADEBOX]

<!-- 
rebuild
-->

Neu bei [!DNL Adobe Journey Optimizer]? In diesem Hub werden die Ressourcen zusammengestellt, die Ihnen dabei helfen, Ihr erstes Live-Kundenerlebnis zu schaffen - mit schrittweisen Anweisungen für gemeinsame Ziele, Anwendungsfällen aus der Praxis, die zeigen, was möglich ist, und kuratierten Videoinhalten (Tutorials, exemplarische Vorgehensweisen und praktische Übungen).

>[!TIP]
>
>Nicht sicher, welche Funktion zu Ihrem Ziel passt? Beginnen Sie mit dem [&#x200B; „Finden Sie die richtige Journey Optimizer-Funktion für Ihr &#x200B;](ajo-use-case-guide.md)&quot; und kehren Sie dann hierher zurück, um schrittweise Anleitungen zu erhalten.

## Hier beginnen: ansehen und lernen {#start-here}

Beginnen Sie mit diesem Einführungsvideo, wenn Sie zehn Minuten Zeit haben. Er führt Sie durch die Benutzeroberfläche und hebt die wichtigsten Funktionen nach Rolle hervor.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

Dann bauen Sie mit diesen Lernressourcen praktisches Vertrauen auf:

* [Journey Optimizer-Tutorials](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} - Schrittweise Videos und Anleitungen zu jeder Rolle.
* [Expert-kuratierte Video-Wiedergabeliste](https://experienceleague.adobe.com/de/playlists?solution=Journey+Optimizer){target="_blank"} - Ein sequenzierter Satz von kurzen Videos, die in der richtigen Reihenfolge angesehen werden.
* [Trainings-Sandbox](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/configure-a-training-sandbox/introduction-and-prerequisites){target="_blank"} - Eine sichere Umgebung mit Beispieldaten zum Üben.
* [Praktische Herausforderungen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/challenges/introduction-and-prerequisites){target="_blank"} - Wenden Sie Ihr Wissen mit geführten Übungen an.

## Erstellen Ihres ersten Erlebnisses {#build-first}

Jede der folgenden Schritten ist kurz und ergebnisorientiert: Was Sie aufbauen werden, für wen es gedacht ist und wie Sie es erreichen. Wählen Sie das Ziel aus, das Ihrem ersten Projekt entspricht, und folgen Sie den Links zur detaillierten Dokumentation.

### Neue Kunden begrüßen {#build-welcome}

**Sie werden Folgendes erstellen:** Eine automatisierte Begrüßungsreihe, die alle neuen Abonnenten begrüßt und inaktive abstößt.
**Am besten geeignet für:** Marketingexperten ・ **Funktion:** Ereignisausgelöster Journey

1. Bestätigen Sie[&#x200B; dass Ihre einheitlichen Profile und &#x200B;](../audience/get-started-profiles.md) das Registrierungsereignis erhalten.
2. [Erstellen Sie Ihre erste &#x200B;](../building-journeys/journey-gs.md) und verwenden Sie das Registrierungsereignis als Eintrag.
3. Fügen Sie eine Begrüßungs[E-Mail](../email/get-started-email.md), dann einen Warteschritt und eine Folgenachricht [Push-Benachrichtigung](../push/get-started-push.md) für Profile hinzu, die nicht interagiert haben.
4. [Personalisieren des Inhalts](../personalization/personalize.md) mit Profilattributen wie Vorname und angegebenen Interessen.

➡️ [Beginnen Sie mit Journey](../building-journeys/journey-gs.md)

### Wiederherstellen von Transaktionsabbrüchen {#build-cart}

**Sie erstellen Folgendes:** Ein Echtzeit-Wiederherstellungsfluss, der Kunden an zurückgelassene Elemente erinnert.
**Am besten geeignet für:** Marketingexperten ・ **Funktion:** Ereignisausgelöster Journey

1. Stellen Sie sicher, dass das Warenkorbabbruchs-Ereignis Journey Optimizer erreicht (wenden Sie sich bei Bedarf an Ihr [Daten-](../data/gs-data.md)).
2. [Erstellen einer Journey](../building-journeys/journey-gs.md) ausgelöst durch das Abbruchereignis.
3. Senden Sie eine personalisierte Erinnerungs-E-Mail. Wenn innerhalb von 24 Stunden kein Klick erfolgt, verzweigen Sie zu einem [Push](../push/get-started-push.md)-Follow-up.
4. [Personalisieren](../personalization/personalize.md) mit den abgebrochenen Elementen und dem Treuestatus.

➡️ [Beginnen Sie mit Journey](../building-journeys/journey-gs.md)

### Senden von Transaktionsnachrichten {#build-transactional}

**Sie erstellen:** On-Demand-Bestellungen, Versandbestätigungen oder Terminbestätigungen, die von einem externen System ausgelöst werden.
**Am besten geeignet für:** Marketing-Experten und Entwickler ・ **Funktion:** API-ausgelöste Kampagne

1. Überprüfen Sie[&#x200B; wie API-ausgelöste Kampagnen &#x200B;](../campaigns/api-triggered-campaigns.md) und welche Payload sie erwarten.
2. Gestalten Sie die Nachrichtenvorlage und [&#x200B; Sie &#x200B;](../personalization/personalize.md) mit den Transaktionsdetails.
3. Bitten Sie Ihren Entwickler, den Campaign-Endpunkt aus Ihrem Auftrags- oder Erfüllungssystem aufzurufen.

➡️ [Arbeiten mit API-ausgelösten Kampagnen](../campaigns/api-triggered-campaigns.md)

### Starten einer Kampagne mit A/B-Tests {#build-campaign}

**Sie erstellen:** Eine geplante Promotion, die automatisch die Inhalte mit der besten Leistung auswählt.
**Am besten geeignet für:** Marketingexperten ・ **Funktion:** Geplante Kampagne + Inhaltsexperiment

1. [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md) und Definieren Ihrer Audience.
2. Verwenden Sie [KI-Inhaltserstellung](../content-management/gs-generative.md) um Betreffzeilen- und Kopiervarianten zu entwerfen.
3. Richten Sie ein [Inhaltsexperiment](../content-management/experiment-accelerator-gs.md) ein, um Varianten eines Beispiels zu testen, und senden Sie dann den Gewinner an den Rest.

➡️ [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md)

### Angebote pro Kunde personalisieren {#build-offers}

**Sie erstellen:** Eine Entscheidung, die jedem Kunden das beste Einzelangebot zeigt.
**Am besten geeignet für:** Marketing-Experten ・ **Funktion:** Decisioning

1. [Erste Schritte mit Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) und erstellen Sie Ihre Angebote und Eignungsregeln.
2. Fügen Sie die Entscheidung einer [Journey](../building-journeys/journey-gs.md) oder Kampagnennachricht hinzu.
3. Ebenen in [KI-Funktionen](ai-features.md) um Angebote automatisch zu ordnen und zu optimieren.

➡️ [Erste Schritte mit Offer Decisioning](../offers/get-started/starting-offer-decisioning.md)

## Anwendungsfälle nach Ziel {#use-cases}

Die obigen Beispiele decken die häufigsten Ausgangspunkte ab, aber Journey Optimizer unterstützt viele weitere Szenarien - von proaktiven Ausfallbenachrichtigungen und der Rückgewinnung von Kunden bis hin zu standortbezogenem Messaging in Echtzeit. Jedes Szenario kombiniert eine oder mehrere Funktionen, die zusammenarbeiten.

Um die genaue Funktion für Ihr *zu finden* verwenden Sie den vollständigen, zielgeordneten Index in [Finden der richtigen Journey Optimizer-Funktion für Ihr Ziel](ajo-use-case-guide.md). Durchgängige, funktionierende Beispiele finden Sie in der [Journey-Anwendungsfallbibliothek](../building-journeys/jo-use-cases.md).

## Videobibliothek {#videos}

Durchsuchen kuratierter Videoinhalte nach Thema. Jede Registerkarte ist mit den entsprechenden Tutorials und Wiedergabelisten auf Experience League verknüpft.

>[!BEGINTABS]

>[!TAB Erste Schritte]

* [Einführung in Journey Optimizer](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"} - Grundlegende Konzepte und eine Produkttour.
* [Übersicht über Journey Optimizer-Tutorials](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} - Der vollständige Katalog mit geführten Videos.

>[!TAB Journey und Kampagnen]

* [Einführung in das Erstellen einer Journey](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} - Erstellen Sie Ihre erste ereignisgesteuerte Journey.
* [Mit Journey Agent Journey erstellen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} - Erstellen Sie Journey anhand einer Aufforderung in natürlicher Sprache.

>[!TAB Personalization und KI]

* [KI-Assistent für die Inhaltserstellung](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} - Generieren von Kopien, Bildern und Varianten.
* [Verwenden von Decisioning zur Personalisierung von Web](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"}Angeboten - Angebote nach Kunde anpassen.

>[!TAB Reporting und Optimierung]

* [Überwachen und Analysieren Ihres Journey mit Live-Berichten](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} - Verfolgen Sie die Performance in Echtzeit.
* [Erstellen von Inhaltsexperimenten für E-Mail](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"}-Kampagnen - Testen und Optimieren von Inhalten.

>[!ENDTABS]

## Onboarding-Checkliste nach Rolle {#checklist}

Das Onboarding umfasst mehrere Rollen. Wählen Sie Ihre Rolle aus, um einen fokussierten Startpfad anzuzeigen:

* **Administrator** - Einrichten von Sandboxes, Berechtigungen und Kanälen. [Erste Schritte als Administrator](path/administrator.md)
* **Dateningenieur** - Modellieren von Schemata und Aufnehmen von Daten. [Erste Schritte als Datentechniker](path/data-engineer.md)
* **Entwickler** - Integrieren von SDKs und Trigger-Ereignissen. [Erste Schritte als Entwickler](path/developer.md)
* **Marketer** - Erstellen Sie Journey, Inhalte und Zielgruppen. [Erste Schritte als Marketing-Experte](path/marketer.md)

Einen vollständigen Überblick über die Zusammenarbeit dieser Rollen finden Sie unter [Rollen und Zuständigkeiten](quick-start.md).

## Verwandte Ressourcen {#related-resources}

* [Finden Sie die richtige Journey Optimizer-Funktion für Ihr Ziel](ajo-use-case-guide.md) - Ziel-zuerst-Entscheidungsleitfaden für jede Funktion.
* [Journey-Anwendungsfallbibliothek](../building-journeys/jo-use-cases.md) - Praxisbeispiele und Implementierungsmuster.
* [Schlüsselbegriffe](terminology.md) - Klärung der Konzepte hinter den einzelnen Funktionen.
* [KI und intelligente Funktionen](ai-features.md) — Erkunden Sie den KI-Assistenten, die Sendezeitoptimierung und die Inhaltserstellung.
* [Erste Schritte mit dem Daten-Management](../data/gs-data.md) - So werden Daten aufgenommen, vereinheitlicht und aktiviert.
