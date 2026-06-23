---
solution: Journey Optimizer
product: journey optimizer
title: Journey-Eintritts- und -Ausstiegskriterien
description: Erfahren Sie anhand von praktischen Beispielen und Best Practices, wie Sie effektiv verwalten können, wann Profile in Journeys eintreten und diese verlassen
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: Eintritt, Ausstieg, Kriterien, Journey, Profil, Wiedereintritt, Best Practices
version: Journey Orchestration
exl-id: e879a0f6-b969-4de0-a733-f2880d58d59b
TQID: https://experienceleague.adobe.com/6OJQsorJ9p7gtO1ep-rIss60J2TmKzqiNS3Btfhh8Gs
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c3f67a94-f1ff-4f5e-bf6f-bc22405930a3id: ebd64fe4-362a-4a1c-9476-b2573ed12a95id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e0eb8757-182f-49f3-94a4-1587d16f5094id: e1e0219c-f879-479f-8427-888ed2a6e9c2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 2251
ht-degree: 68%

---

# Arbeiten mit Journey-Eintritts- und -Ausstiegskriterien {#entry-exit-criteria-guide}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie anhand von realen Beispielen und Best Practices, wie Sie steuern können, wann Journey-Eintritts- und -Austrittskriterien in Ihre Journey eintreten und wann sie verlassen werden, und wie Sie diese konfigurieren.

>[!ENDSHADEBOX]

Damit Sie bei der Orchestrierung von Kundenerlebnissen die richtige Botschaft zur richtigen Zeit bereitstellen können, müssen Sie genau steuern können, wann Kundinnen und Kunden in Ihre Journey eintreten und aus dieser aussteigen. Das Verständnis und die richtige Konfiguration der Eintritts- und Ausstiegskriterien können den Unterschied zwischen einer erfolgreichen, ansprechenden Kampagne und verpassten Gelegenheiten oder der Nachrichtenermüdung ausmachen.

Dieses Handbuch enthält praktische Anleitungen, Beispiele aus der Praxis und Best Practices für die Verwaltung der Ein- und Ausstiegskriterien für Journey in [!DNL Adobe Journey Optimizer].

## Was sind Eintritts- und Ausstiegskriterien? {#what-are-criteria}

**Eintrittskriterien** bestimmen die Bedingungen, unter denen ein [Kundenprofil](../audience/get-started-profiles.md) zum Eintritt in eine bestimmte Journey berechtigt ist. Profile können auf folgender Grundlage eintreten:

* **[Kundenverhalten](../event/about-events.md)** – Von Kundinnen und Kunden ausgeführte Aktionen lösen in Echtzeit den Journey-Eintritt aus, z. B. das Tätigen eines Kaufs, ein Abbruch des Warenkorbs oder das Öffnen Ihrer Mobile App.

* **[Profilattribute](../audience/get-started-profiles.md)** – Die Kundenmerkmale bestimmen die Eignung anhand der in ihrem Profil gespeicherten Daten, z. B. Treuestufe, Standort, Alter oder Kommunikationsvoreinstellungen.

* **[Externe Ereignisse](../event/about-creating-business.md)** – Geschäfts- oder Umweltereignis-Trigger, die mehrere Kundinnen und Kunden gleichzeitig betreffen, z. B. Warnhinweise bei geringem Bestand, Wetterbedingungen oder Preisänderungen.

* **[Zielgruppenzugehörigkeit](../audience/about-audiences.md)** – Die Zugehörigkeit zu einem bestimmten Zielgruppensegment ermöglicht zielgerichtete Journeys für Gruppen wie hochwertige Kundschaft, inaktive Benutzende oder neue Abonnentinnen und Abonnenten.

**Ausstiegskriterien** definieren, wann und wie ein Profil eine Journey verlässt oder daraus entfernt wird:

* **Journey-Abschluss** – Profile steigen automatisch aus, wenn sie das [Ende aller Journey-Pfade](end-journey.md) erreichen, wodurch das erstellte Erlebnis abgeschlossen ist.

* **Erreichen der Erfolgsmetrik** – Profile steigen aus, wenn sie das [Journey-Ziel](success-metrics.md) erreicht haben, z. B. einen Kauf getätigt oder eine App heruntergeladen haben, wodurch unnötige Nachfolgekommunikation entfällt.

* **Bedingungsbasiert** – Profile steigen aus, wenn [bestimmte Bedingungen](conditions.md) erfüllt sind, z. B. Inaktivität über einen bestimmten Zeitraum oder Änderungen an Profilattributen.

* **Ereignisbasiert** – Profile steigen aus, wenn [bestimmte Ereignisse](../event/about-events.md) wie Abonnementkündigung oder Produktrückgabe eintreten.

* **Zielgruppendisqualifzierung** – Profile steigen aus, wenn sie die [Zielgruppenkriterien](../audience/about-audiences.md) nicht mehr erfüllen, wodurch sichergestellt ist, dass Nachrichten relevant bleiben.

## Bedeutung von Eintritts- und Ausstiegskriterien {#why-they-matter}

Die korrekte Definition der Eintritts- und Ausstiegskriterien bietet einen erheblichen geschäftlichen Nutzen:

* **Relevanz:** Nur die richtigen Kundinnen und Kunden treten in die Journey ein, was die Interaktions- und Konversionsraten steigert, indem die Zielgruppe zum optimalen Zeitpunkt angesprochen wird.

* **Effizienz:** Verhindert, dass Kundinnen und Kunden in irrelevanten Journeys bleiben, und reduziert unnötige Kommunikation, Betriebskosten und die Verärgerung der Kundschaft.

* **Personalisierung:** Ermöglicht die dynamische Anpassung von Erlebnissen auf der Grundlage von Echtzeitdaten und -verhalten, wodurch relevante Kundeninteraktionen entstehen.

* **Compliance:** Hilft bei der Verwaltung der Frequenzbegrenzung und der Vermeidung von Überkommunikation, wobei Kundenvoreinstellungen und gesetzliche Anforderungen eingehalten werden und die Markenreputation gewahrt bleibt.

## Beispiele aus der Praxis für Journey-Eintritte und -Ausstiege {#real-world-examples}

In den folgenden gängigen Szenarien wird demonstriert, wie die Eintritts- und Ausstiegskriterien in der Praxis funktionieren:

**Begrüßungskampagne für neue Abonnentinnen und Abonnenten**

Erstellen Sie einen personalisierten ersten Eindruck, indem Sie neue Abonnentinnen und Abonnenten automatisch durch eine Einführung in Ihre Marke, Ihre Produkte und Ihre Services leiten.

* **Eintritt:** Profile treten in die Journey ein, wenn sie einen Newsletter abonnieren
* **Ausstieg:** Profile steigen aus, nachdem sie eine Reihe von Begrüßungs-E-Mails abgeschlossen haben, oder nach einer bestimmten Zeit, wenn sie nicht interagieren
* **Vorteil:** Stellt sicher, dass das Onboarding von neuen Abonnentinnen und Abonnenten rechtzeitig geschieht, und vermeidet repetitive Nachrichten

**Wiederherstellen abgebrochener Warenkörbe**

Gewinnen Sie verlorene Einnahmen zurück, indem Sie Kundinnen und Kunden an zurückgelassene Artikel erinnern und Anreize für den Abschluss ihres Kaufs bieten.

* **Eintritt:** Kundinnen und Kunden treten in die Journey ein, wenn sie Artikel zum Warenkorb hinzufügen, aber den Checkout nicht innerhalb von 24 Stunden abschließen
* **Ausstieg:** Profile steigen aus, wenn sie den Kauf abschließen, oder nach 7 Tagen, wenn kein Kauf getätigt wird
* **Vorteil:** Fördert Konversionen durch rechtzeitige Erinnerungen ohne Spam an uninteressierte Kundinnen und Kunden

**Interaktionen im Rahmen des Treueprogramms**

Belohnen Sie Ihre wertvollsten Kundinnen und Kunden mit exklusiven Vorteilen und personalisierter Kommunikation, die die Markentreue stärken und den Lebenszeitwert steigern.

* **Eintritt:** Kundinnen und Kunden treten in die Journey ein, nachdem sie einen bestimmten Schwellenwert für Treuepunkte erreicht haben
* **Ausstieg:** Profile steigen aus, wenn sie Belohnungen einlösen oder 60 Tage lang inaktiv waren
* **Vorteil:** Sorgt bei hochwertiger Kundschaft für Interaktionen mit personalisierten Angeboten und vermeidet Kommunikationsermüdung

**Erfassung von Produkt-Feedback**

Sammeln Sie Erkenntnisse über Kundenzufriedenheit und Produktleistung, indem Sie zum optimalen Zeitpunkt nach dem Versand Feedback anfordern.

* **Eintritt:** Kundinnen und Kunden treten in die Journey ein, nachdem sie ein Bestätigungsereignis für den Produktversand erhalten haben
* **Ausstieg:** Profile steigen aus, wenn Feedback gesendet wird, oder nach 10 Tagen, wenn keine Antwort erfolgt
* **Vorteil:** Erfasst wertvolles Feedback sofort, ohne Kundschaft mit fortdauernden Anfragen zu belästigen

## So konfigurieren Sie Journey-Eintrittskriterien {#configure-entry}

>[!BEGINSHADEBOX]

**Hier erfahren Sie alles, was Sie über Eintrittskriterien wissen müssen:**

* **[Ereignisbasierte Trigger:](../event/about-events.md)** Verwenden Sie Ereignisse wie „Profilerstellung“, „Transaktion abgeschlossen“ oder benutzerdefinierte Ereignisse, um eine Journey zu starten. [Konfigurieren Sie Ereignisse](../event/about-creating.md) unter **[!UICONTROL Administration]** > **[!UICONTROL Ereignisse]** und definieren Sie [Ereignisschema und -felder](../event/experience-event-schema.md). Fügen Sie dann das Ereignis aus der **[!UICONTROL Ereignisse]**-Palette im [Journey-Designer hinzu](using-the-journey-designer.md).

* **[Zielgruppenbasierter Eintritt:](read-audience.md)** Richten Sie Journeys an Profile, die zu bestimmten Zielgruppen gehören, entweder als einmaligen Batch oder gemäß einem wiederkehrenden Zeitplan. [Erstellen Sie Zielgruppen](../audience/creating-a-segment-definition.md) im Menü **[!UICONTROL Zielgruppen]**, fügen Sie dann eine Aktivität des Typs **[!UICONTROL Zielgruppe lesen]** hinzu und [konfigurieren Sie den Zeitplan](journey-properties.md#schedule). Verwenden Sie nach der Eingabe Bedingungen [Segmentieren, Ausschließen oder Zusammenführen von Verzweigungen](read-audience.md#audience-targeting-in-journeys).

* **[Eintritt nach Zielgruppenqualifizierung:](audience-qualification-events.md)** Lösen Sie Journeys in Echtzeit aus, wenn Profile sich für bestimmte Zielgruppen qualifizieren oder aus ihnen aussteigen. Definieren Sie [Streaming-Zielgruppen](../audience/about-audiences.md), fügen Sie ein Ereignis des Typs **[!UICONTROL Zielgruppenqualifizierung]** aus der Palette **[!UICONTROL Ereignisse]** hinzu und wählen Sie den Trigger-Typ aus.

* **[Attributfilter:](conditions.md)** Verfeinern Sie Eintrittskriterien, indem Sie Ereignisse oder Zielgruppen mit Profilattributen und Kontext mithilfe der UND/ODER-Logik kombinieren. Verwenden Sie [Bedingungen](conditions.md), um auf [Profilattribute](../audience/get-started-profiles.md), Ereignisse oder [externe Daten](../datasource/about-data-sources.md) zu verweisen.

* **[Zeitfenster und Planung:](journey-properties.md#schedule)** Legen Sie Zeitbeschränkungen fest, damit Journeys zeitgerecht und relevant bleiben. Konfigurieren Sie [Zeitpläne für Aktivitäten des Typs „Zielgruppe lesen“](read-audience.md), verwenden Sie [Warteaktivitäten](wait-activity.md) und fügen Sie [zeitbasierte Bedingungen](conditions.md) hinzu, um das Timing zu steuern.

>[!ENDSHADEBOX]

## So richten Sie Journey-Ausstiegskriterien ein {#configure-exit}

>[!BEGINSHADEBOX]

**Hier erfahren Sie alles, was Sie über Ausstiegskriterien wissen müssen:**

* **[Journey-Abschluss:](end-journey.md)** Profile steigen automatisch aus, nachdem sie den letzten Journey-Schritt erreicht haben. Entwerfen Sie Journey-Pfade, die bei Aktivitäten des Typs **[!UICONTROL Ende]** enden.

* **[Erreichen einer Erfolgsmetrik:](journey-properties.md#exit-criteria)** Definieren Sie Erfolgsmetriken (wie Kauf oder Abonnement) und lassen Sie Profile nach Abschluss aussteigen. Klicken Sie auf das Symbol **[!UICONTROL Ausstiegskriterien anzeigen]**, wählen Sie **[!UICONTROL Ausstiegskriterien hinzufügen]** und wählen Sie ein [Ereignis](../event/about-events.md) oder eine [Zielgruppe](../audience/about-audiences.md) als Trigger aus.

* **[Timeouts bei Inaktivität](wait-activity.md)**: Profile sollen aussteigen, wenn innerhalb eines bestimmten Zeitraums keine Interaktion auftritt. Verwenden Sie [Ausstiegskriterien](journey-properties.md#exit-criteria) mit Zielgruppen, die das Datum der letzten Interaktion prüfen, legen Sie [Warteaktivitäten](wait-activity.md) mit definierten Dauer fest und verwenden Sie [Bedingungen](conditions.md), um auf Aktivität zu prüfen.

* **[Regeln für den erneuten Eintritt:](entry-management.md)** Entscheiden Sie, ob Profile je nach Kampagnenstrategie mehrmals oder nur einmal in die Journey eintreten können. Konfigurieren Sie die Einstellungen für den **[!UICONTROL Wiedereintritt]** in den **[!UICONTROL Eigenschaften]** der Journey, um Wartezeiten festzulegen, den erzwungenen Wiedereintritt zu aktivieren oder [zusätzliche Kennungen](supplemental-identifier.md) für den kontextspezifischen Wiedereintritt zu verwenden.

>[!ENDSHADEBOX]

## Detaillierte Journey-Beispiele {#journey-examples}

Eine schrittweise Implementierungsanleitung mit vollständigen technischen Details finden Sie in diesen dokumentierten Anwendungsfällen:

* **[Kunden-Onboarding-Journey](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)** – Erstellen Sie personalisierte Begrüßungserlebnisse mit Zielgruppenqualifizierung, Ereignis-Timeout und zielbasierten Ausstiegen

* **[Wiederherstellung abgebrochener Warenkörbe](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)** – Gewinnen Sie verlorene Umsätze mit ereignisgesteuerten Journeys, Playbooks und Kanal-Routing zurück

* **[Rückgewinnungskampagnen](https://experienceleague.adobe.com/de/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)** – Gewinnen Sie inaktive Kundschaft mit verhaltensbezogener Zielgruppenbestimmung und Paid-Media-Aktivierung zurück

* **[Senden von Nachrichten an Abonnentinnen und Abonnenten](message-to-subscribers-uc.md)** – Sprechen Sie Abonnement-Listen mit „Zielgruppe lesen“ und  personalisierten Inhalten an

* **[Senden von Multi-Channel-Nachrichten](journeys-uc.md)** – Kombinieren Sie E-Mail und Push mit Reaktionsereignissen und Mehrpfad-Logik

* **[Senden von E-Mails nur an Wochentagen](weekday-email-uc.md)** – Planen Sie die Kommunikation mithilfe zeitbasierter Bedingungen und Warteformeln

>[!TIP]
>
>Durchsuchen Sie alle verfügbaren Anwendungsfälle in der [Journey-Anwendungsfallbibliothek, ](jo-use-cases.md) Sie nach weiteren Mustern und Implementierungen. Beispiele sind [Steigern von ](ramp-up-deliveries-uc.md), [Erlebnisereignismuster](exp-event-lookup.md) und [Entfernen von Profilen aus Live-Journey](journey-pause.md#apply-an-exit-criteria-in-a-paused-journey).

## Best Practices für die Verwaltung von Eintritten und Ausstiegen {#best-practices}

**Klare Definition**

Erstellen Sie klare Dokumentations- und Namenskonventionen, um sicherzustellen, dass Ihr Team versteht, wie sich Profile durch Ihre Journeys bewegen:

* Dokumentieren Sie Ihre Eintritts- und Ausstiegslogik, bevor Sie Journeys erstellen, um Marketing- und Analytics-Teams aufeinander abzustimmen
* Erstellen Sie Flussdiagramme mit Eintrittspunkten, Journey-Pfaden und Ausstiegsbedingungen
* Definieren Sie klare Geschäftsregeln: „Profile treten aus, wenn X geschieht, ODER nach Y Tagen“
* Verwenden Sie beschreibende Labels: „Ausstieg – Kauf abgeschlossen“, nicht „Ausstieg 1“
* [Versehen Sie Journeys konsistent mit Tags](../start/search-filter-categorize.md#tags) für Reporting und Filterung

**Vermeiden überlappender Journeys**

Vermeiden Sie Kundenverwirrung und Nachrichtenkonflikte, indem Sie Ihre Journey-Strategie kampagnenübergreifend koordinieren:

* [Führen Sie ein Audit der aktiven Journeys](journey-ui.md) vor dem Start ähnlicher Journeys durch, um Konflikte zu vermeiden
* Nutzen Sie [Konfliktmanagement](../conflict-prioritization/conflicts.md) und [Prioritätswerte](../conflict-prioritization/priority-scores.md), um Überschneidungen aufzulösen und Journeys zu priorisieren
* Erstellen Sie Journeys, die einander ergänzen, statt miteinander zu konkurrieren

>[!NOTE]
>
>Verwenden Sie bei erweiterten Szenarien wie dem automatischen Entfernen von Profilen bei Qualifizierung für Journeys mit höherer Priorität [Journey-Begrenzung und Schlichtung](../conflict-prioritization/journey-capping.md) anstelle von Ausstiegskriterien.

**Überwachen und Optimieren**

Bewerten Sie kontinuierlich die Journey-Leistung und verfeinern Sie Ihre Eintritts- und Ausstiegskriterien basierend auf dem tatsächlichen Kundenverhalten:

* Verfolgen Sie Eintrittsrate, Ausstiegsrate und Abschlussrate für jede Journey mithilfe von [Journey-Berichten](../reports/journey-global-report-cja.md)
* Überwachen Sie [Erfolgsmetriken](success-metrics.md): Prozentsatz der Ausstiege über Erfolgsmetrik „Abschluss“ vs. Timeout
* [Testen Sie Eintritts- und Ausstiegskriterien](testing-the-journey.md) vor dem Start mit verschiedenen Profilszenarien
* Nehmen Sie basierend auf Daten Anpassungen vor: Prüfen Sie bei vielen frühen Ausstiegen die Relevanz der Eintrittskriterien; analysieren Sie bei niedriger Erfüllung der Erfolgsmetrik den Inhalt und das Timing
* Prüfen Sie alle aktiven Journeys vierteljährlich

**Beachten von Frequenzbegrenzungen**

Wahren Sie das Vertrauen und die Interaktionen Ihrer Kundschaft, indem Sie die Häufigkeit der Nachrichten in Ihrer gesamten Journey-Kommunikation steuern:

* Legen Sie angemessene [Wartezeiten für den erneuten Eintritt](entry-management.md) fest oder deaktivieren Sie den erneuten Eintritt für einmalige Journeys
* Verwenden Sie [Frequenzbegrenzungsregeln](../conflict-prioritization/rule-sets.md), um Überkommunikation zu vermeiden
* Überwachen Sie Frequenzmetriken in Berichten, um deren Einhaltung sicherzustellen

>[!NOTE]
>
>Verwenden Sie [Journey-Begrenzung und Schlichtung](../conflict-prioritization/journey-capping.md) und [Frequenzbegrenzung nach Kanal](../conflict-prioritization/channel-capping.md), um die Begrenzungen für Frequenz und Journey-Eintritte zu verwalten.

## Zusammenfassung {#conclusion}

Die Ein- und Ausstiegskriterien für Journey sind grundlegend für die Bereitstellung personalisierter, zeitnaher und effektiver Kundenerlebnisse mit [!DNL Adobe Journey Optimizer]. Durch sorgfältige Gestaltung dieser Bedingungen können Marketing-Fachleute die Interaktion steigern, Spannungen reduzieren und stärkere Kundenbeziehungen aufbauen.

Beginnen Sie damit, Ihre Kunden-Trigger und Ausstiegspunkte klar zuzuordnen, gründlich zu testen und die Ergebnisse zu überwachen, um Ihre Journey-Orchestrierung kontinuierlich zu verfeinern.

## Verwandte Ressourcen {#related-resources}

**Technische Dokumentation**

[Profileintrittsverwaltung](entry-management.md) | [Journey-Eigenschaften und -Ausstiegskriterien](journey-properties.md) | [So enden Journeys](end-journey.md) | [Zusätzliche Kennungen](supplemental-identifier.md) | [Journey-Designer](using-the-journey-designer.md)

**Tutorials und Beispiele**

[Journey-Anwendungsfälle](jo-use-cases.md) | [Video zum Kunden-Onboarding](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding) | [Video zu Warenkorbabbrüchen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart) | [Community-Blog: Eintritts- und Ausstiegskriterien](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/mastering-journey-entry-and-exit-criteria-in-adobe-journey/ba-p/760958)

**Verwandte Funktionen**

[Zielgruppen-Qualifizierungsereignisse](audience-qualification-events.md) | [Erfolgsmetriken und -ziele](success-metrics.md) | [Konfliktmanagement](../conflict-prioritization/conflicts.md) | [Frequenzlimitierung](../conflict-prioritization/rule-sets.md) | [Journey testen](testing-the-journey.md) | [Aktivität optimieren](optimize.md) | [Reaktionsereignisse](reaction-events.md) | [Warteaktivität](wait-activity.md)

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** In diesem Handbuch wird erläutert, wie Sie in Adobe Journey Optimizer Einstiegs- und Ausstiegskriterien für Journey definieren, konfigurieren und optimieren können. Es enthält Beispiele aus der Praxis und Best Practices, um sicherzustellen, dass die richtigen Profile zum richtigen Zeitpunkt erreicht werden.

**intents:**

* Konfigurieren von ereignis-, zielgruppen- oder attributbasierten Einstiegskriterien für eine Journey
* Richten Sie Ausstiegskriterien basierend auf dem Journey-Abschluss, Erfolgsmetriken, Timeouts für Inaktivität oder der Audience-Disqualifizierung ein.
* Wenden Sie Regeln für den erneuten Eintritt an, um zu steuern, ob Profile mehrmals auf einen Journey zugreifen können
* Vermeiden Sie überlappende Journey mit Konfliktmanagement und Prioritätswerten
* Überwachung und Optimierung der Ein- und Ausstiegsraten mithilfe von Journey-Berichten

**Glossar:**

* **Einstiegskriterien**: Die Bedingungen, die bestimmen, wann ein Kundenprofil für die Eingabe eines Journey-*qualifiziert ist (produktspezifisch)*
* **Ausstiegskriterien**: Bedingungen, die definieren, wann und wie ein Profil einen Journey verlässt oder von einem Profil entfernt wird *produktspezifisch)*
* **Zielgruppenqualifizierung**: Ein Journey-Eingabemechanismus, der Trigger auslöst, wenn ein Profil in Echtzeit in eine Streaming-Zielgruppe eintritt oder aus ihr austritt *(produktspezifisch)*
* **Erneuter Eintritt**: Profile können mehrmals auf dieselbe Journey zugreifen. Dies kann mit einer Wartezeit konfiguriert werden *(produktspezifisch)*
* **Frequenzlimitierung**: Eine Regel, die begrenzt, wie viele Nachrichten ein Profil innerhalb eines bestimmten Zeitfensters empfangen kann *(produktspezifisch)*

**Leitplanken:**

* Ein Profil kann nicht mehrmals zur gleichen Zeit auf derselben Journey vorhanden sein.
* Der erneute Eintritt muss explizit aktiviert werden; die standardmäßige Wartezeit bis zum erneuten Eintritt beträgt 5 Minuten mit einem Maximum von 91 Tagen.
* Verwenden Sie für das erweiterte Multi-Journey-Frequenzmanagement eine Journey-Begrenzung und Schlichtung anstelle individueller Ausstiegskriterien.
* Journey-Überschneidungen müssen proaktiv gemanagt werden. Verwenden Sie das Konflikt-Management und Prioritätswerte, um konkurrierende Journey aufzulösen.

**Terminologie:**

* Kanonische Bezeichnung: Einreisekriterien — Akronym: n/a — Varianten: Einreisebedingungen, Journey-Trigger
* Kanonische Bezeichnung: Ausstiegskriterien — Akronym: n/a — Varianten: Ausstiegsbedingungen, Regeln zum Entfernen von Profilen
* Synonyme: „Zielgruppen-Disqualifizierung“ = „Zielgruppen-Austritt“ als Exit-Trigger
* Verwechseln Sie nicht: „Für neue Eintritte schließen“ ≠ „Ausstiegskriterien“ — erstere blockieren neue Eintritte; Ausstiegskriterien entfernen laufende Profile.

**FAQ:**

* **F: Kann sich ein Profil zweimal gleichzeitig auf derselben Journey befinden?** — Nein, ein Profil kann nicht gleichzeitig auf derselben Journey vorhanden sein. Die Profilidentität wird als Schlüssel zur Durchsetzung dieser Bestimmung verwendet.
* **F: Wie kann ich verhindern, dass ein Profil erneut auf eine Journey gelangt?** — Deaktivieren Sie den erneuten Eintritt im Bedienfeld Journey-Eigenschaften oder fügen Sie eine Bedingung hinzu, um zu überprüfen, ob das Profil bereits eingegeben wurde.
* **F: Was ist der Unterschied zwischen Ausstiegskriterien und dem Schließen einer Journey?** — Beendigungskriterien entfernen Einzelprofile von einer Live-Journey basierend auf Bedingungen; durch Schließen einer Journey werden alle neuen Eintritte gestoppt, während die aktuellen Profile beendet werden.
* **F: Wie kann ich die übermäßige Kommunikation mit Kunden in mehreren Journey unterbinden?** — Verwenden Sie Regeln zur Frequenzlimitierung und Journey-Limitierung und Schlichtung, um Cross-Journey-Nachrichtenbeschränkungen durchzusetzen.
* **F: Was ist eine Zielgruppen-Disqualifizierung als Exit-Trigger?** — Wenn ein Profil die Segmentkriterien der Zielgruppe nicht mehr erfüllt, wird es automatisch von der Journey entfernt, um die Kommunikation relevant zu halten.

+++
