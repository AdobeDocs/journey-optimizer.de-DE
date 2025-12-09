---
solution: Journey Optimizer
product: journey optimizer
title: Ein- und Ausstiegskriterien für Journey
description: Erfahren Sie anhand von realen Beispielen und Best Practices, wie Sie effektiv verwalten können, wann Profile in Journey eintreten und diese verlassen
feature: Journeys, Profiles
role: User
level: Intermediate
hide: true
hidefromtoc: true
keywords: Eintritt, Austritt, Kriterien, Journey, Profil, Wiedereintritt, Best Practices
version: Journey Orchestration
source-git-commit: 9e5b85dec8a58a4d008ab63337589352c0fa5ee6
workflow-type: tm+mt
source-wordcount: '1445'
ht-degree: 1%

---


# Arbeiten mit Einstiegs- und Ausstiegskriterien für Journey {#entry-exit-criteria-guide}

Um in Customer Experience Orchestration die richtige Botschaft zur richtigen Zeit bereitzustellen, müssen Sie genau steuern können, wann Kunden Ihre Journey betreten und verlassen. Das Verständnis und die richtige Konfiguration der Ein- und Ausstiegskriterien können den Unterschied zwischen einer erfolgreichen, ansprechenden Kampagne und verpassten Gelegenheiten oder der Nachrichtenermüdung ausmachen.

Dieses Handbuch enthält praktische Anleitungen, Beispiele aus der Praxis und Best Practices für die Verwaltung der Ein- und Ausstiegskriterien für Journey in Adobe Journey Optimizer.

## Was sind Ein- und Ausstiegskriterien? {#what-are-criteria}

**Einstiegskriterien** bestimmen die Bedingungen, unter denen ein [Kundenprofil](../audience/get-started-profiles.md) zum Einstieg in eine bestimmte Journey berechtigt ist. Profile können auf folgender Grundlage eintreten:

* **[Kundenverhalten](../event/about-events.md)** - Aktionen, die von Kunden in Echtzeit für den Trigger-Journey-Eintrag ausgeführt werden, z. B. einen Kauf tätigen, einen Warenkorb verlassen oder Ihre Mobile App öffnen.

* **[Profilattribute](../audience/get-started-profiles.md)** - Die Kundenmerkmale bestimmen die Eignung anhand der in ihrem Profil gespeicherten Daten, z. B. Treuestufe, Standort, Alter oder Kommunikationsvoreinstellungen.

* Trigger **[Externe Ereignisse](../event/about-creating-business.md)** - Geschäfts- oder Umweltereignisse, die mehrere Kunden gleichzeitig betreffen, z. B. Warnhinweise bei geringem Bestand, Wetterbedingungen oder Preisänderungen.

* **[Zielgruppenzugehörigkeit](../audience/about-audiences.md)** - Die Zugehörigkeit zu einem bestimmten Zielgruppensegment ermöglicht zielgerichteten Journey für Gruppen wie hochwertige Kunden, inaktive Benutzende oder neue Abonnenten.

**Ausstiegskriterien** definieren, wann und wie ein Profil eine Journey verlässt oder daraus entfernt wird:

* **Journey-Abschluss** - Profile werden automatisch beendet, wenn sie das [Ende aller Journey-Pfade“ erreichen](end-journey.md) wodurch das entworfene Erlebnis abgeschlossen ist.

* **Erfolgsmetrik-Leistung** - Profile enden, wenn sie das [Journey-Ziel erreicht haben](success-metrics.md) z. B. einen Kauf tätigen oder eine App herunterladen, wodurch unnötige Nachfolgekommunikation entfällt.

* **Bedingungsbasiert** - Profile beenden, wenn [bestimmte Bedingungen](condition-activity.md) erfüllt sind, z. B. Inaktivität über einen bestimmten Zeitraum oder Änderungen an Profilattributen.

* **Ereignisbasiert** - Profile werden beendet, wenn [bestimmte Ereignisse](../event/about-events.md) wie Abonnementkündigung oder Produktrückgabe, eintreten.

* **Zielgruppen-**: Profile treten aus, wenn sie die [Zielgruppenkriterien“ nicht mehr erfüllen, &#x200B;](../audience/about-audiences.md) sicherzustellen, dass Nachrichten relevant bleiben.

## Warum Einreise- und Ausreisekriterien wichtig sind {#why-they-matter}

Die korrekte Definition der Ein- und Ausstiegskriterien bietet einen erheblichen geschäftlichen Nutzen:

* **Relevanz**: Nur die richtigen Kundinnen und Kunden steigen in die Journey ein, was die Interaktions- und Konversionsraten steigert, indem die Zielgruppe zum optimalen Zeitpunkt angesprochen wird.

* **Effizienz**: Verhindert, dass Kunden in irrelevanten Journey bleiben, und reduziert unnötige Kommunikation, Betriebskosten und die Verärgerung der Kunden.

* **Personalization**: Ermöglicht die dynamische Anpassung von Erlebnissen auf der Grundlage von Echtzeitdaten und -verhalten, wodurch aussagekräftigere Kundeninteraktionen entstehen.

* **Compliance**: Hilft bei der Verwaltung der Frequenzlimitierung und der Vermeidung von Überkommunikation, wobei Kundenpräferenzen und gesetzliche Anforderungen eingehalten werden und der Ruf der Marke erhalten bleibt.

## Beispiele aus der Praxis für das Ein- und Aussteigen von Journey {#real-world-examples}

Im Folgenden finden Sie gängige Szenarien, die zeigen, wie die Ein- und Ausstiegskriterien in der Praxis funktionieren:

**Willkommenskampagne für neue Abonnenten**

* **Eintritt**: Profile geben die Journey ein, wenn sie einen Newsletter abonnieren
* **Beenden**: Profile beenden, nachdem sie eine Willkommensreihe von E-Mails abgeschlossen haben, oder nach einer bestimmten Zeit, wenn sie nicht interagieren
* **Vorteil**: Stellt sicher, dass neue Abonnent*innen rechtzeitig einsteigen und sich wiederholende Nachrichten vermeiden

**Abgebrochene Wiederherstellung des Warenkorbs**

* **Einstieg**: Kunden geben die Journey ein, wenn sie Artikel zum Warenkorb hinzufügen, aber den Checkout nicht innerhalb von 24 Stunden abschließen
* **Beenden**: Profile beenden den Kauf, wenn sie ihn abschließen, oder nach 7 Tagen, wenn kein Kauf getätigt wird
* **Vorteil**: Fördert Konversionen durch rechtzeitige Erinnerungen ohne Spam an uninteressierte Kunden

**Interaktion mit Treueprogrammen**

* **Einstieg**: Kunden treten der Journey bei, nachdem sie einen bestimmten Schwellenwert für Treuepunkte erreicht haben
* **Beenden**: Profile beenden nach der Einlösung von Belohnungen oder wenn sie 60 Tage lang inaktiv waren
* **Vorteil**: Hält hochwertige Kunden mit personalisierten Angeboten in Verbindung und vermeidet Kommunikationsmüdigkeit

**Produkt-Feedback-Sammlung**

* **Einstieg**: Kunden geben die Journey ein, nachdem sie ein Bestätigungsereignis für den Produktversand erhalten haben
* **Beenden**: Profile beenden, wenn Feedback gesendet wird, oder nach 10 Tagen, wenn keine Antwort erfolgt
* **Vorteil**: Erfasst wertvolles Feedback sofort, ohne Kunden mit persistenten Anfragen zu belästigen

## Konfigurieren der Journey-Einstiegskriterien {#configure-entry}

>[!BEGINSHADEBOX]

**Hier erfahren Sie alles, was Sie über Einreisekriterien wissen müssen:**

* **[Ereignisbasierte Trigger](../event/about-events.md)**: Verwenden Sie Ereignisse wie „Profilerstellung“, „Transaktion abgeschlossen“ oder benutzerdefinierte Ereignisse, um einen Journey zu starten. [Ereignisse konfigurieren](../event/about-creating.md) definieren Sie unter **[!UICONTROL Administration]** > **[!UICONTROL Ereignisse]** [Ereignisschema und -felder](../event/experience-event-schema.md) und fügen Sie dann das Ereignis aus der Palette **[!UICONTROL Ereignisse]** im [Journey-Designer &#x200B;](using-the-journey-designer.md).

* **[Zielgruppenbasierter Eintrag](read-audience.md)**: Targeting von Journey für Profile, die zu bestimmten Zielgruppen gehören, entweder als einmaliger Batch oder in einem wiederkehrenden Zeitplan. [Zielgruppen erstellen](../audience/creating-a-segment-definition.md) im Menü **[!UICONTROL Zielgruppen]** fügen Sie dann eine Aktivität **[!UICONTROL Zielgruppe lesen]** hinzu und [&#x200B; Sie den Zeitplan](journey-properties.md#schedule).

* **[Einstieg in Zielgruppenqualifizierung](audience-qualification-events.md)**: Trigger-Journey, wenn Profile sich in Echtzeit für bestimmte Zielgruppen qualifizieren oder aus ihnen austreten. Definieren Sie [Streaming](../audience/about-audiences.md)Zielgruppen), fügen Sie ein **[!UICONTROL Zielgruppen-Qualifizierungsereignis]** aus der **[!UICONTROL Ereignisse]**-Palette hinzu und wählen Sie den Trigger-Typ aus.

* **[Attributfilter](condition-activity.md)**: Verfeinern Sie Eingabekriterien, indem Sie Ereignisse oder Zielgruppen mit Profilattributen und Kontext mithilfe der AND/OR-Logik kombinieren. Verwenden Sie [Bedingungen](conditions.md), um auf [Profilattribute](../audience/get-started-profiles.md) Ereignisse oder [externe Daten](../datasource/about-data-sources.md) zu verweisen.

* **[Zeitfenster und Planung](journey-properties.md#schedule)**: Legen Sie Zeitbeschränkungen fest, um Journey rechtzeitig und relevant zu halten. Konfigurieren Sie [Zeitpläne für die Aktivitäten &#x200B;](read-audience.md) Zielgruppe lesen[&#x200B; verwenden Sie Warteaktivitäten](wait-activity.md) und fügen Sie [zeitbasierte Bedingungen](conditions.md) hinzu, um die Zeitplanung zu steuern.

>[!ENDSHADEBOX]

## Einrichten von Journey-Beendigungskriterien {#configure-exit}

>[!BEGINSHADEBOX]

**Hier erfahren Sie alles, was Sie über Ausstiegskriterien wissen müssen:**

* **[Journey-Abschluss](end-journey.md)**: Profile werden automatisch beendet, nachdem sie den letzten Journey-Schritt erreicht haben. Entwerfen Sie Journey-Pfade, die auf **[!UICONTROL End]**-Aktivitäten enden.

* **[Erfolgsmetrik-Leistung](journey-properties.md#exit-criteria)**: Definieren Sie Erfolgsmetriken (wie Kauf oder Abonnement) und beenden Sie Profile nach Abschluss. Trigger Klicken Sie **[!UICONTROL Symbol &quot;]** anzeigen“, wählen Sie **[!UICONTROL Exitkriterien hinzufügen]** und wählen Sie ein [Ereignis](../event/about-events.md) oder [Zielgruppe](../audience/about-audiences.md) als Exitkriterium aus.

* **[Zeitüberschreitungen bei Inaktivität](wait-activity.md)**: Profile beenden, wenn innerhalb eines bestimmten Zeitraums keine Interaktion auftritt. Verwenden Sie [Ausstiegskriterien](journey-properties.md#exit-criteria) mit Zielgruppen, die das Datum der letzten Interaktion überprüfen, [Warteaktivitäten](wait-activity.md) mit definierten Dauer festlegen und [Bedingungen](condition-activity.md) verwenden, um nach Aktivität zu suchen.

* **[Regeln für den erneuten Eintritt](entry-management.md)**: Entscheiden Sie, ob Profile je nach Kampagnenstrategie mehrmals oder nur einmal auf die Journey zugreifen können. Konfigurieren Sie **[!UICONTROL Wiedereintritt]**-Einstellungen in Journey **[!UICONTROL Eigenschaften]**, um Wartezeiten festzulegen, den erzwungenen Wiedereintritt zu aktivieren oder [zusätzliche Kennungen](supplemental-identifier.md) für den kontextspezifischen Wiedereintritt zu verwenden.

>[!ENDSHADEBOX]

## Detaillierte Journey-Beispiele {#journey-examples}

Eine schrittweise Implementierungsanleitung mit vollständigen technischen Details finden Sie in diesen dokumentierten Anwendungsfällen:

* **[Customer Onboarding Journey](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)** - Erstellen personalisierter Willkommenserlebnisse mit Zielgruppen-Qualifizierung, Ereignis-Timeout und zielbasierten Ausstiegen

* **[Abgebrochene Wiederherstellung des Warenkorbs](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)** - Wiederherstellen verlorener Umsätze mit ereignisgesteuerten Journeys, Playbooks und Channel-Routing

* **[Rückgewinnungskampagnen](https://experienceleague.adobe.com/de/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)** - Gewinnen Sie inaktive Kunden mit verhaltensbezogener Zielgruppenbestimmung und Paid-Media-Aktivierung zurück.

* **[Nachrichten an Abonnenten senden](message-to-subscribers-uc.md)** - Targeting von Abonnementlisten mit „Zielgruppe lesen“ und personalisierten Inhalten

* **[Senden von Multi-Channel-Nachrichten](journeys-uc.md)** - Kombinieren Sie E-Mail und Push mit Reaktionsereignissen und Multi-Path-Logik

* **[Senden von E-Mails nur an Wochentagen](weekday-email-uc.md)** - Planen Sie die Kommunikation mithilfe zeitbasierter Bedingungen und Warteformeln

>[!TIP]
>
>Durchsuchen Sie alle verfügbaren Anwendungsfälle in der [Journey-Anwendungsfallbibliothek](jo-use-cases.md) um weitere Muster und Implementierungen zu erhalten, einschließlich [Anlaufsendungen](ramp-up-deliveries-uc.md), [Erlebnisereignismuster](exp-event-lookup.md) und [Entfernen von Profilen aus Live-Journey](journey-pause.md#apply-an-exit-criteria-in-a-paused-journey).

## Best Practices für die Verwaltung von Ein- und Austritten {#best-practices}

**Definition löschen**

* Dokumentieren Sie Ihre Einstiegs- und Ausstiegslogik, bevor Sie Journey erstellen, um Marketing- und Analytics-Teams aufeinander abzustimmen
* Erstellen Sie Flussdiagramme mit Einstiegspunkten, Journey-Pfaden und Ausgangsbedingungen
* Geschäftsregeln klar definieren: „Profile verlassen, wenn X geschieht, ODER nach Y Tagen“
* Verwenden Sie beschreibende Beschriftungen: „Beenden - Kauf abgeschlossen“ nicht „Beenden 1“
* [Tag-Journey](../start/search-filter-categorize.md#tags) für das Reporting und die Filterung konsistent

**Überlappende Journey vermeiden**

* [Audit Active Journey](journey-ui.md) vor dem Start ähnlicher Tools zur Konfliktvermeidung
* Nutzen Sie [Konfliktmanagement](../conflict-prioritization/conflicts.md) und [Prioritätswerte](../conflict-prioritization/priority-scores.md) um Überschneidungen zu beheben und Journey zu priorisieren
* Entwerfen Sie Journey, die sich ergänzen, anstatt miteinander zu konkurrieren

>[!NOTE]
>
>Bei erweiterten Szenarien wie dem automatischen Entfernen von Profilen, wenn sie sich für Journey mit höherer Priorität qualifizieren, verwenden Sie [Journey-Begrenzung und Schlichtung](../conflict-prioritization/journey-capping.md) anstelle von Beendigungskriterien.

**Überwachen und Optimieren**

* Verfolgen Sie Einstiegs-, Ausstiegs- und Abschlussrate für jede Journey mithilfe von [Journey-Berichten](../reports/journey-global-report-cja.md)
* Überwachen [Erfolgsmetriken](success-metrics.md): Prozentsatz der Beendigungen über Abschluss der Erfolgsmetrik vs. Zeitüberschreitung
* [Einstiegs- und Ausstiegskriterien](testing-the-journey.md) vor dem Start mit verschiedenen Profilszenarien testen
* Basierend auf Daten anpassen: Bei hohen frühen Beenden die Relevanz der Einstiegskriterien überprüfen; bei Abschluss einer niedrigen Erfolgsmetrik Inhalt und Timing analysieren
* Alle aktiven Journey vierteljährlich überprüfen

**Berücksichtigt Frequenzlimitierungen**

* Legen Sie [&#x200B; entsprechenden Wartezeiten für den erneuten &#x200B;](entry-management.md) fest oder deaktivieren Sie den erneuten Eintritt für einmalige Journey
* Verwenden [Frequenzlimitierungsregeln](../conflict-prioritization/rule-sets.md) um Überkommunikation zu vermeiden
* Überwachen von Häufigkeitsmetriken in Berichten, um die Einhaltung sicherzustellen

>[!NOTE]
>
>Verwenden Sie [Journey-Begrenzung und Schlichtung und Frequenzlimitierung nach Kanal, um die Frequenzlimitierung und &#x200B;](../conflict-prioritization/journey-capping.md) für den [-Eintrag in mehreren Journey Journey &#x200B;](../conflict-prioritization/channel-capping.md) verwalten.

## Zusammenfassung {#conclusion}

Die Ein- und Ausstiegskriterien für Journey sind von grundlegender Bedeutung für die Bereitstellung personalisierter, zeitnaher und effektiver Kundenerlebnisse mit Adobe Journey Optimizer. Durch sorgfältige Gestaltung dieser Bedingungen können Marketing-Experten die Interaktion steigern, Spannungen reduzieren und stärkere Kundenbeziehungen aufbauen.

Beginnen Sie damit, Ihre Kunden-Trigger und Ausgangspunkte klar zuzuordnen, gründlich zu testen und die Ergebnisse zu überwachen, um Ihre Journey-Orchestrierung kontinuierlich zu verfeinern.

## Verwandte Ressourcen {#related-resources}

**Technische Dokumentation**

* [Verwaltung des Profileintritts](entry-management.md) - Detaillierte technische Anleitung für Eintrittskontrollen
* [Journey-Eigenschaften und Beendigungskriterien](journey-properties.md) - Vollständige Konfigurationsreferenz
* [Wie Journey enden](end-journey.md) - Journey Lifecycle Management
* [Zusätzliche Kennungen](supplemental-identifier.md) - Erweiterte Szenarien für den erneuten Eintritt
* [Journey-Designer](using-the-journey-designer.md) - Journey erstellen und entwerfen

**Tutorials und Beispiele**

* [Journey-Anwendungsfälle](jo-use-cases.md) - Vollständige Journey-Beispiele und -Muster
* [Onboarding-Video für Kunden](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* [Video zu Transaktionsabbruch](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* [Community-Blog: Ein- und Ausstiegskriterien](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/mastering-journey-entry-and-exit-criteria-in-adobe-journey/ba-p/760958?profile.language=de)

**Verwandte Funktionen**

* [Zielgruppen-Qualifizierungsereignisse](audience-qualification-events.md)
* [Erfolgsmetriken und Ziele](success-metrics.md)
* [Konflikt-Management](../conflict-prioritization/conflicts.md)
* [Frequenzbegrenzung](../conflict-prioritization/rule-sets.md)
* [Testen von Journey](testing-the-journey.md)
* [Aktivität des Typs „Bedingung“](condition-activity.md)
* [Reaktionsereignisse](reaction-events.md)
* [Aktivität „Warten“](wait-activity.md)
