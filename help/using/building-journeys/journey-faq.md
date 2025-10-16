---
solution: Journey Optimizer
product: journey optimizer
title: Häufig gestellte Fragen zu Journey
description: Häufig gestellte Fragen zu Journey Optimizer Journey
feature: Journeys, Get Started
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: Journey, Fragen, Antworten, Fehlerbehebung, Hilfe, Anleitung
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: a7da542320a38dbc739ec42ee4926fce1dea1df0
workflow-type: tm+mt
source-wordcount: '2363'
ht-degree: 2%

---


# Häufig gestellte Fragen {#faq-journeys}

Im Folgenden finden Sie häufig gestellte Fragen zu Adobe Journey Optimizer Journey.

Sie würden gerne mehr erfahren? Verwenden Sie die Feedback-Optionen unten auf dieser Seite, um Ihre Frage zu stellen, oder vernetzen Sie sich mit der [Adobe Journey Optimizer-Community](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}.

## Allgemeine Konzepte

+++ Was ist eine Journey in Adobe Journey Optimizer?

Eine Journey ist eine mehrstufige Orchestrierung, mit der Sie Echtzeit-Kundenerlebnisse kanalübergreifend entwerfen und ausführen können. Journey kombinieren Ereignisse, Orchestrierungsaktivitäten, Aktionen und Nachrichten, um basierend auf Kundenverhalten und Geschäftsereignissen personalisierte, kontextuelle Erlebnisse zu schaffen.

Weitere Informationen zu [Journey](journey.md).

+++

+++ Was sind die verschiedenen Arten von Journey?

Adobe Journey Optimizer unterstützt drei Typen von Journey:

* **Unitäre Journey**: Wird einzeln durch ein Ereignis ausgelöst (z. B. Kauf, App-Anmeldung). Die Profile wechseln jeweils zu einem Zeitpunkt zum Journey, wenn das Ereignis eintritt.
* **Audience-Journey lesen**: Beginnen Sie mit einer Audience aus Adobe Experience Platform und senden Sie Nachrichten im Batch an alle Profile in dieser Audience.
* **Geschäftsereignis-Journey**: Ausgelöst durch Geschäftsereignisse (z. B. Stock-Updates, Wetterwarnungen), die mehrere Profile gleichzeitig betreffen.

Weitere Informationen zu [Journey-Typen](entry-management.md#types-of-journeys).

+++

+++ Was ist der Unterschied zwischen einer Journey und einer Kampagne?

**Journey** sind mehrstufige Orchestrierungen, die auf Ereignisse oder Zielgruppen reagieren und über den gesamten Kundenlebenszyklus hinweg eine komplexe Logik, Bedingungen, Wartezeiten und mehrere Berührungspunkte ermöglichen.

**Kampagnen** sind einmalige oder wiederkehrende Nachrichten, die an eine bestimmte Zielgruppe gesendet werden und sich ideal für eigenständige Nachrichten wie Werbeanzeigen oder Newsletter eignen.

**Best Practice**: Verwenden Sie Journey für fortlaufende, mehrstufige Interaktionen und Kampagnen für zielgerichtete, eigenständige Kommunikation.

+++

+++ Was sind die Hauptkomponenten einer Journey?

Eine Journey besteht aus:

* **Events**: Einstiegspunkte, an denen die Journey Trigger wird (z. B. Profilqualifizierung, Geschäftsereignisse)
* **Orchestrierungsaktivitäten**: Logikkomponenten wie Bedingungen, Warten, Zielgruppe lesen und Beenden
* **Aktionen**: Aktivitäten, die Aufgaben ausführen, z. B. Nachrichten senden, Profile aktualisieren oder externe APIs aufrufen
* **Integrierte Kanalaktionen**: Native Messaging-Funktionen für E-Mail, SMS, Push und andere Kanäle
* **Benutzerdefinierte Aktionen**: Integration mit Drittanbietersystemen

Weitere Informationen zu [Journey-Aktivitäten](about-journey-activities.md).

+++

## Erstellen von Journey

+++ Wie baue ich meine erste Journey?

Führen Sie die folgenden wichtigen Schritte aus:

1. **Voraussetzungen einrichten**: Konfigurieren Sie Ereignisse, Datenquellen und Aktionen nach Bedarf
2. **Journey erstellen**: Navigieren Sie zum Menü Journey und klicken Sie auf &quot;Journey erstellen“
3. **Journey-Eigenschaften definieren**: Legen Sie den Journey-Namen, die Beschreibung, den Namespace und andere Einstellungen fest
4. **Journey entwerfen**: Ziehen Sie Aktivitäten per Drag-and-Drop aus der Palette in die Arbeitsfläche
5. **Journey testen**: Testmodus zur Validierung der Journey-Logik verwenden
6. **Journey veröffentlichen**: Aktivieren der Journey, um sie live zu schalten

Befolgen Sie [Schritt-für-Schritt-Anleitung](journey-gs.md).

+++

+++ Welche Voraussetzungen müssen erfüllt sein, damit eine Journey erstellt werden kann?

Die Voraussetzungen hängen von Ihrem Journey-Typ ab:

* **Ereignisausgelöste Journey**: Konfigurieren Sie Ereignisse, um zu definieren, wann Profile in die Journey eintreten sollen
* **Zielgruppenbasierte Journey**: Erstellen von Zielgruppen in Adobe Experience Platform
* **Datenanreicherung**: Einrichten von Datenquellen, um zusätzliche Informationen abzurufen
* **Integrationen von Drittanbietern**: Konfigurieren von benutzerdefinierten Aktionen bei Verwendung externer Systeme

Weitere Informationen zur Konfiguration von [Journey](../configuration/about-data-sources-events-actions.md).

+++

+++ Kann ich auf meinem Journey Daten von externen Systemen verwenden?

Ja. Sie können **externe Datenquellen** so konfigurieren, dass Informationen von API-Services von Drittanbietern abgerufen und in Ihren Journey-Bedingungen, bei der Personalisierung oder bei Aktionen verwendet werden. Auf diese Weise können Sie das Kundenerlebnis mit Echtzeitdaten aus Ihrem CRM, Ihren Treuesystemen, Wetter-Services oder anderen externen Plattformen anreichern.

Weitere Informationen zu [externen Datenquellen](../datasource/external-data-sources.md).

+++

+++ Wie füge ich Bedingungen zu meinem Journey hinzu?

Sie können Bedingungen mithilfe der Aktivität **Bedingung** aus der Orchestrierungspalette hinzufügen. Bedingungen ermöglichen Folgendes:

* Erstellen einfacher oder erweiterter Bedingungen mithilfe des Ausdruckseditors
* Aufspaltung der Journey in mehrere Pfade basierend auf Profilattributen, Zielgruppenzugehörigkeit, Ereignissen oder kontextuellen Daten
* Zeitüberschreitungspfade für Profile definieren, die die Bedingung nicht innerhalb einer bestimmten Zeit erfüllen

Weitere Informationen zu [Bedingungen](condition-activity.md).

+++

+++ Kann ich Nachrichten auf einer Journey an Profile senden?

Ja. Journey Optimizer umfasst **integrierte Kanalaktionen** mit denen Sie Nachrichten per E-Mail, Push-Benachrichtigungen, SMS/MMS/RCS, In-App-Nachrichten, Web-Erlebnisse, Code-basierte Erlebnisse, Briefpost, Inhaltskarten, WhatsApp und LINE senden können. Sie können Nachrichteninhalte direkt in Journey Optimizer entwerfen und als Aktionsaktivitäten in Ihrem Journey hinzufügen.

Weitere Informationen zu [Nachrichten in Journey](journeys-message.md).

+++

+++ Wie warte ich auf eine bestimmte Zeit oder ein bestimmtes Ereignis auf einer Journey?

Verwenden Sie die **Warteaktivität**, um die Journey für eine bestimmte Dauer oder bis zu einem bestimmten Datum/zu einer bestimmten Uhrzeit anzuhalten. Warteaktivitäten sind nützlich für:

* Versand von Folgenachrichten nach einer Verzögerung (z. B. 3 Tage nach dem Kauf)
* Warten auf Geschäftszeiten, bevor Sie Maßnahmen ergreifen
* Erstellen von Drip-Kampagnen mit Zeitintervallen
* Kombination mit Bedingungen zum Erstellen von Zeitüberschreitungsszenarien

Weitere Informationen zu [Warteaktivitäten](wait-activity.md).

+++

+++ Kann ich Profilinformationen auf einer Journey aktualisieren?

Ja. Verwenden Sie die Aktivität **Profil aktualisieren**, um Profilattribute in Adobe Experience Platform auf der Grundlage von Journey-Ereignissen oder -Bedingungen zu ändern. Dies ist nützlich für die Aktualisierung von Treuepunkten, die Aufzeichnung von Journey-Meilensteinen, die Änderung der Präferenzeinstellungen oder die Verfolgung der Kundeninteraktionswerte.

Weitere Informationen zu [Profilaktualisierungen](update-profiles.md).

+++

## Testen und Veröffentlichen

+++ Wie kann ich meinen Journey vor der Veröffentlichung testen?

Journey Optimizer bietet zwei Testansätze:

* **Testmodus**: Simulieren Sie die einzelnen Profile, die sich Schritt für Schritt durch den Journey bewegen, sodass Sie Logik, Bedingungen und Aktionen überprüfen können, bevor Sie live gehen.
* **Probelauf-Modus**: Führen Sie Ihren Journey mit echten Produktionsdaten aus, ohne sich an tatsächliche Kunden zu wenden oder Profilinformationen zu aktualisieren. Dies gibt Ihnen Vertrauen in Zielgruppen-Targeting und Journey-Design.

**Best Practice**: Testen Sie Journey immer vor der Veröffentlichung, um sicherzustellen, dass sie wie erwartet funktionieren, und um Probleme frühzeitig zu identifizieren.

Weitere Informationen über [Testmodus](testing-the-journey.md) und [Probelauf](journey-dry-run.md).

+++

+++ Was passiert, wenn ich eine Journey veröffentliche?

Beim Veröffentlichen einer Journey:

* Die Journey wird **aktiv** und kann neue Profile akzeptieren
* Profile können basierend auf den Einstiegskriterien (Ereignis oder Zielgruppe) eintreten
* Nachrichten und Aktionen werden für Profile ausgeführt, die sich durch den Journey bewegen
* Eine veröffentlichte Journey kann nicht direkt bearbeitet werden (eine neue Version muss erstellt werden)

Weitere Informationen über [Veröffentlichen von Journey](publishing-the-journey.md).

+++

+++ Kann ich eine bereits veröffentlichte Journey modifizieren?

Live-Journey können nicht direkt bearbeitet werden. Änderungen vornehmen:

1. **Neue Version erstellen**: Duplizieren Sie die veröffentlichte Journey, um eine Entwurfsversion zu erstellen
2. **Änderungen vornehmen**: Bearbeiten Sie die Entwurfsversion nach Bedarf
3. **Neue Version testen**: Verwenden Sie den Testmodus, um Änderungen zu validieren
4. **Neue Version veröffentlichen**: Dadurch wird die vorherige Version automatisch geschlossen und die neue aktiviert

Profile, die sich bereits auf der Journey befinden, vervollständigen die Originalversion, während neue Profile in die neue Version eintreten.

Weitere Informationen zu [Journey-Versionen](journey-ui.md#journey-versions).

+++

+++ Wie stoppe ich eine Journey?

Sie können die Journey-Ausführung auf verschiedene Weise verwalten:

* **Für neue Eintritte schließen**: Stoppen Sie den Eintritt neuer Profile, während Sie vorhandenen Profilen erlauben, ihren Journey abzuschließen
* **Sofort anhalten**: Beenden Sie den Journey und beenden Sie alle aktuell darin enthaltenen Profile.
* **Pause**: Journey vorübergehend anhalten und später fortsetzen (für bestimmte Journey-Typen verfügbar)

Weitere Informationen zum [ von Journey](end-journey.md).

+++

## Ausführung und Überwachung von Journey

+++ Wie kann ich den Profilfortschritt auf einer Journey verfolgen?

Sie können die Journey-Ausführung überwachen mit:

* **Journey-Live-**: Echtzeitmetriken und KPIs für Ihren Journey anzeigen
* **Journey-All-Time-Bericht**: Analysieren der Journey-Leistung mit Customer Journey Analytics
* **Journey-Schrittereignisse**: Zugriff auf detaillierte Ausführungsdaten für benutzerdefinierte Berichte
* **Dashboard für Probelauf-Journey**: Überprüfen Sie die Ergebnisse der Testausführung, bevor Sie live gehen

Weitere Informationen zum [Journey-Reporting](report-journey.md).

+++

+++ Warum hat kein Profil meinen Journey eingegeben?

Häufige Gründe, warum Profile möglicherweise keine Journey eingeben:

* **Ereignis nicht empfangen**: Das auslösende Ereignis wurde nicht gesendet oder ordnungsgemäß konfiguriert
* **Zielgruppenkriterien nicht erfüllt**: Das Profil ist nicht für die Einstiegszielgruppe qualifiziert
* **Regeln für den erneuten Eintritt**: Das Profil hat kürzlich die Journey abgeschlossen und der erneute Eintritt ist blockiert
* **Journey nicht veröffentlicht**: Die Journey befindet sich im Entwurfsstatus
* **Ungültiger Namespace**: Der Journey-Namespace entspricht nicht der Profilidentität
* **Journey geschlossen**: Die Journey akzeptiert keine neuen Eintritte mehr

Weitere Informationen über [Einstiegsverwaltung](entry-management.md).

+++

+++ Was sind Journey-Schrittereignisse und wie kann ich sie verwenden?

Journey-Schrittereignisse sind automatisch generierte Datensätze, die detaillierte Informationen über jeden Schritt erfassen, den ein Profil auf einem Journey unternimmt. Dazu gehören Eintritts- und Ausstiegsereignisse, Aktionsausführung (gesendete Nachrichten, benutzerdefinierte Aktionen, die aufgerufen werden), Journey-Übergänge (Wechseln zwischen Aktivitäten) sowie Fehler und Zeitüberschreitungen.

**Anwendungsfälle**:

* Erstellen benutzerdefinierter Berichte in Customer Journey Analytics- oder BI-Tools
* Debuggen von Journey-Ausführungsproblemen
* Nachverfolgen des detaillierten Profilverhaltens
* Erstellen erweiterter Analyse- und Attributionsmodelle

Weitere Informationen zu [Journey-Schrittereignissen](../reports/sharing-overview.md).

+++

+++ Wie kann ich eine Fehlerbehebung bei einem Journey durchführen, der nicht erwartungsgemäß funktioniert?

Journey Optimizer bietet mehrere Ressourcen zur Fehlerbehebung:

* **Fehlerindikatoren**: Visuelle Warnhinweise auf der Journey-Arbeitsfläche zeigen Konfigurationsprobleme an
* **Testmodus**: Durchlaufen Sie die Journey, um Probleme zu identifizieren.
* **Journey-Berichte**: Überprüfen Sie die Ausführungsmetriken, um Engpässe oder Fehler zu finden
* **Journey-Schrittereignisse**: Analysieren Sie detaillierte Ausführungsdaten, um das Profilverhalten zu verstehen

**Häufige Probleme**:

* Falsch konfigurierte Ereignisse oder Zielgruppen
* Fehlende Datenquellenverbindungen
* Ungültige Ausdrücke in Bedingungen oder Personalisierung
* Zu kurze Zeitüberschreitungseinstellungen

Weitere Informationen zu [Fehlerbehebung bei Journey](troubleshooting.md).

+++

+++ Was passiert, wenn eine Aktion auf einer Journey fehlschlägt?

Wenn eine Aktion fehlschlägt (z. B. API-Aufruf-Timeout, Nachrichtenversand-Fehler), wird die Journey standardmäßig fortgesetzt, sofern nicht anders konfiguriert. Sie können Bedingungsaktivitäten definieren, um Fehlerszenarien zu handhaben. Fehler werden in Journey-Berichten und Schrittereignissen zur Überwachung protokolliert.

**Best Practice**: Legen Sie geeignete Zeitüberschreitungswerte für externe Aktionen fest und definieren Sie alternative Pfade für kritische Fehlerszenarien.

Weitere Informationen zu [Aktionsantworten](../action/action-response.md).

+++

## Erweiterte Konzepte

+++ Was ist ein Journey-Namespace und warum ist er wichtig?

Ein **Namespace** ist ein Identitätstyp (z. B. E-Mail, ECID, Telefonnummer), der bestimmt, wie Profile in der Journey identifiziert werden. Der Namespace definiert, welche Kennung zum Abgleichen von Profilen verwendet wird, muss ereignisübergreifend konsistent sein und sich auf das Verhalten beim Eintritt und erneuten Eintritt von Journey auswirken.

**Best Practice**: Wählen Sie einen Namespace aus, mit dem Ihre Kundinnen und Kunden über alle Berührungspunkte hinweg zuverlässig identifiziert werden.

Weitere Informationen zu [Identity-Namespaces](../audience/get-started-identity.md).

+++

+++ Können Profile mehrmals auf denselben Journey zugreifen?

Ja, abhängig von den **Einstellungen für den erneuten Eintritt**:

* **Erneuten Eintritt erlauben**: Profile können die Journey mehrmals nach Abschluss aufrufen
* **Wartezeit bis zum erneuten Eintritt**: Legen Sie eine Mindestzeit zwischen den Journey-Einträgen (z. B. 7 Tage) fest.
* **Erneuten Eintritt bei Ereignis erzwingen**: Trigger einer neuen Journey-Instanz, auch wenn sich das Profil bereits auf der Journey befindet

**Best Practice**: Verwenden Sie Regeln für den erneuten Eintritt, um das Ermüden von Nachrichten zu verhindern und eine angemessene Geschwindigkeit sicherzustellen.

Weitere Informationen über [Einstiegsverwaltung](entry-management.md).

+++

+++ Was ist die Optimierung des Versandzeitpunkts?

**Sendezeitoptimierung (STO)** KI, um die beste Sendezeit für jedes einzelne Profil vorherzusagen und so Öffnungsraten und Interaktion zu maximieren. STO analysiert historische Interaktionsmuster, um zu bestimmen, wann jeder Empfänger mit der größten Wahrscheinlichkeit mit Ihrer Nachricht interagiert.

**Vorteile**:

* Verbesserte Öffnungs- und Klickraten
* Besseres Kundenerlebnis durch zeitlich optimal abgestimmte Nachrichten
* Reduzierte Abmelderaten

Weitere Informationen über [Sendezeitoptimierung](send-time-optimization.md).

+++

+++ Was sind Journey-Begrenzungsregeln?

**Journey-Begrenzung** Ermöglicht es Ihnen, die Anzahl der Eintritte eines Profils in Journey innerhalb eines bestimmten Zeitraums zu begrenzen, wodurch die Nachrichtenermüdung verhindert und ein optimales Kundenerlebnis sichergestellt wird. Sie können die Höchstanzahl von Einträgen pro Profil für Journey oder bestimmte Journeys festlegen, Zeitfenster (täglich, wöchentlich, monatlich) definieren und Journeys priorisieren, wenn mehrere Journeys um dasselbe Profil konkurrieren.

Weitere Informationen zur [Journey-Begrenzung](../conflict-prioritization/journey-capping.md).

+++

+++ Kann ich meinen Journey mit externen Systemen integrieren?

Ja. Verwenden Sie **benutzerspezifische Aktionen** um APIs von Drittanbietern (CRM, Marketing-Automatisierung, Treueprogramm-Systeme) aufzurufen, Daten an externe Systeme zu senden, Echtzeit-Informationen für Entscheidungen abzurufen und Trigger-Workflows in externen Plattformen zu erstellen.

Benutzerdefinierte Aktionen unterstützen die Authentifizierung (API-Schlüssel, OAuth 2.0), die Anpassung der Anfrage-/Antwort-Payload, die Fehlerbehandlung und Zeitüberschreitungen sowie dynamische Parameter aus dem Journey-Kontext.

Weitere Informationen über [benutzerdefinierte Aktionen](using-custom-actions.md).

+++

+++ Wie kann ich Adobe Campaign mit Journey verwenden?

Journey Optimizer lässt sich nativ mit Adobe Campaign integrieren, um seine erweiterten Funktionen zu nutzen:

* **Adobe Campaign Standard**: Verwenden Sie Campaign Standard-Aktionen, um Transaktionsnachrichten zu senden
* **Adobe Campaign v7/v8**: Trigger-Campaign-Workflows und Verwendung der Versandinfrastruktur von Campaign

**Best Practice**: Verwenden Sie diese Integration, wenn Sie bereits über Campaign-Vorlagen und -Datenmodelle verfügen oder Campaign-spezifische Funktionen benötigen.

Weitere Informationen zur [Campaign-Integration](ajo-ac.md).

+++

+++ Was ist die Sprungaktivität?

Die **Sprungaktivität** ermöglicht den Übergang von Profilen von einer Journey auf eine andere und ermöglicht wiederverwendbare Journey-Muster, die Journey-Orchestrierung über mehrere Journey hinweg, eine vereinfachte Journey-Wartung und progressive Interaktionsstrategien.

Wenn ein Profil eine Sprungaktivität erreicht, verlässt es die aktuelle Journey und gelangt an ihrem Startpunkt auf die Ziel-Journey.

Weitere Informationen über [Sprungaktivität](jump.md).

+++

## Best Practices und Einschränkungen

+++ Was sind die wichtigsten Einschränkungen, die ich beachten sollte?

Zu den wichtigen Leitplanken gehören:

* **Journey-Komplexität**: Maximale Aktivitäten, Pfade und Verschachtelungsebenen
* **Durchsatz**: Nachrichtenübertragungsraten und API-Aufrufbeschränkungen
* **Time-to-Live**: Maximale Journey-Dauer (z. B. 91 Tage für unitäre Journey)
* **Zielgruppengröße**: Beschränkungen für die Größe von gelesenen Zielgruppen-Batches
* **Ausdruckskomplexität**: Zeichenbeschränkungen in Bedingungen und Personalisierung

Vollständige Ansicht [Leitplanken und ](../start/guardrails.md))

+++

+++ Was sind die Best Practices für das Journey-Design?

**Struktur und**:

* Konzentrieren der Journey auf bestimmte Anwendungsfälle
* Beschreibende Benennung für Aktivitäten verwenden
* Hinzufügen von Anmerkungen und Beschriftungen für komplexe Logik
* Gruppieren verwandter Journey mit Tags

**Performance**:

* Optimieren Sie Wartezeiten, um Interaktion und Volumen auszugleichen
* Beschränken von externen API-Aufrufen auf wichtige Anwendungsfälle
* Verwenden von Begrenzungsregeln, um das Ermüden von Nachrichten zu verhindern
* Journey-Metriken regelmäßig überwachen

**Testen**:

* Journey vor der Veröffentlichung immer testen
* Alle bedingten Pfade und Szenarien testen
* Verwenden realistischer Testprofile
* Validieren von Personalisierung und dynamischen Inhalten

**Wartung**:

* Regelmäßige Überprüfung der Journey-Performance
* Archivieren oder schließen Sie nicht verwendete Journey
* Journey-Logik und Geschäftsregeln dokumentieren
* Planen der Journey-Versionierung

Erfahren Sie mehr über die Best Practices für das [Journey-Design](using-the-journey-designer.md).

+++

+++ Wie viele Aktivitäten kann ich einer Journey hinzufügen?

Es gibt zwar keine strikte Begrenzung für die Anzahl der Aktivitäten, aber sehr komplexe Journey (über 50 Aktivitäten) können schwierig zu warten und zu beheben sein. Große Journey mit vielen Verzweigungen und Bedingungen können die Verarbeitungszeit und Lesbarkeit beeinträchtigen.

**Best Practice**: Wenn Ihr Journey zu komplex wird, sollten Sie ihn mithilfe der Sprungaktivität in mehrere Journey unterteilen, wiederverwendbare Unter-Journey erstellen oder die Logik mit effizienteren Bedingungen vereinfachen.

Weitere Informationen zum [Journey-Design](using-the-journey-designer.md).

+++

+++ Wie stelle ich sicher, dass mein Journey im großen Maßstab eine gute Leistung erzielt?

**Überlegungen zum Design**:

* Zielgruppenbasierte Einträge für Batch-Nachrichten anstelle einzelner Ereignisse verwenden
* Angemessene Wartezeiten implementieren, um das Nachrichtenvolumen zu verteilen
* Nutzen von Begrenzungsregeln, um Systemüberlastungen zu vermeiden
* Optimieren der Bedingungslogik zur Reduzierung der Verarbeitungskomplexität

**Überwachung**:

* Journey-Metriken regelmäßig verfolgen
* Überwachen der API-Leistung für benutzerdefinierte Aktionen
* Überprüfen der Fehlerquoten und Zeitüberschreitungsereignisse
* Einrichten von Warnhinweisen für kritische Journey-Fehler

**Optimierung**:

* Testmodus und Probelauf verwenden, um die Leistung vor der Veröffentlichung zu validieren
* Beschränken von Aufrufen externer Datenquellen auf wichtige Szenarien
* Häufig verwendete Daten zwischenspeichern, wenn möglich
* Überprüfen und Optimieren der Leistung des Nachrichtenversands

Weitere Informationen zur [Journey-Optimierung](../start/guardrails.md).

+++

## Weitere Ressourcen

Detailliertere Informationen und Updates finden Sie in den folgenden Ressourcen:

* [Erste Schritte mit Journeys](journey.md)
* [Erstellen Ihrer ersten Journey](journey-gs.md)
* [Handbücher zur Fehlerbehebung](troubleshooting.md)
* [Journey-Anwendungsfälle](jo-use-cases.md)
* [Produktbeschreibung zu Journey Optimizer](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
