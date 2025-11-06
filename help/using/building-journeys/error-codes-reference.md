---
solution: Journey Optimizer
product: journey optimizer
title: Referenz für Fehler-Codes
description: Erfahren Sie mehr über häufige Fehler-Codes in Adobe Journey Optimizer und wie Sie sie beheben können
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: Fehler, Codes, Fehlerbehebung, Journey, Kampagne, Nachrichten
source-git-commit: 405c87f9ca138e4e92438704b5051ce89c73d726
workflow-type: tm+mt
source-wordcount: '2392'
ht-degree: 1%

---


# Referenz für Fehler-Codes {#error-codes}

Adobe Journey Optimizer verwendet standardisierte Fehler-Codes, mit denen Sie Probleme in Journey-, Kampagnen- und Nachrichtenkonfigurationen schnell identifizieren und beheben können. Wenn Sie diese Fehler-Codes verstehen, können Sie die Zeit für die Fehlerbehebung erheblich verkürzen und die optimale Kampagnenleistung aufrechterhalten.

## Grundlagen zur Struktur des Fehler-Codes {#error-code-structure}

Adobe Journey Optimizer-Fehler-Codes folgen einem konsistenten Benennungsmuster, das bei der Identifizierung der Komponente und des Problemtyps hilft:

* **Service-Präfix**: Gibt an, welcher Adobe Journey Optimizer-Service den Fehler generiert hat (z. B. CJMPTS für Push/Transport-Service, CJMRT für Journey-Laufzeit, CJMMAS für den Nachrichtenerstellungs-Service, CJMCMP für Campaign, CJMTL für Transportschicht, CJMRPS für Reporting/Provisioning Service)
* **Fehlernummer**: Eindeutige Kennung für die spezifische Fehlerbedingung
* **HTTP-Status**: Standard-HTTP-Status-Code (z. B. 400, 403, 422, 500)

Beispiel: `CJMRT-030012-422` zeigt einen Journey-Laufzeitfehler (CJMRT) mit Fehlernummer 030012 und HTTP-Status 422 (Unverarbeitbare Entität) an.

## Wo finden Sie Fehler-Codes? {#find-error-codes}

Fehlercodes werden an verschiedenen Stellen in Adobe Journey Optimizer angezeigt:

* Journey von Ausführungsberichten und Protokollen
* Kampagnenaktivierungsbildschirme
* Warnungen bei Nachrichtenvalidierung
* Systembenachrichtigungen und Warnhinweise
* API-Antworten (bei Verwendung von REST-APIs)

Wenn ein Fehler auftritt, notieren Sie sich den vollständigen Fehler-Code und alle zugehörigen Anfrage-IDs, da diese für die Fehlerbehebung und Support-Eskalation unerlässlich sind.

## Häufige Fehler-Codes nach Service {#error-codes-by-service}

### CJMPTS: Push- und Transport-Service-Fehler {#cjmpts-errors}

Diese Fehler treten beim Versand von Push-Benachrichtigungen und beim Nachrichtentransport auf.

| Fehler-Code | Beschreibung | Grundursache | Auflösung |
|------------|-------------|-----------|-----------|
| **CJMPTS-1410-500** | Interner Server-Fehler bei Push-/Kanal-Sendeaktion | Ausfall des Kanal-Backends, abgelaufene Anmeldedaten, fehlerhafte Konfiguration oder Provider-Fehler | &#x200B;1. Nach Verzögerung erneut versuchen<br/>2. Überprüfen Sie die Anbieterkonfigurationen und -kontingente<br/>3. Überprüfen Sie, ob die Push-Anmeldeinformationen gültig <br/>.4. Mit einem alternativen Kanal testen<br/>5. Wenn persistent, kontaktieren Sie den Adobe-Support mit <br/><br/>**Dokumentation**: [Push-Konfiguration](../push/push-configuration.md) |
| **CJMPTS-1006-404** | Push/SMS schlägt mit „Ressource nicht gefunden“ fehl | Der referenzierte Anbieter/Kanal existiert nicht, ist falsch geschrieben oder die Bereitstellung wurde aufgehoben | &#x200B;1. Überprüfen und korrigieren Sie Provider-/Channel-Referenzen und IDs<br/>2. Audit-Sandbox-/Organisationskonfiguration<br/>3. Überprüfen Sie, ob die Kanalkonfigurationen aktiv sind<br/>4. Erstellen Sie die Kanalkonfiguration bei Bedarf neu <br/><br/>**Verwandte Dokumentation**: [Kanaloberflächen](../configuration/channel-surfaces.md) |
| **CJMPTS-1510-500** | Interner Server-Fehler beim Push-Kanal-Versand | Backend-Push/Transport-Fehlfunktion; Provider- oder Infrastrukturfehler | &#x200B;1. Kanalbereitstellungseinstellungen überprüfen<br/>2. Überprüfen Sie, ob die Push-Anmeldeinformationen gültig <br/> 3 sind. Wiederholen Sie den Vorgang<br/>4. Wenn persistent, kontaktieren Sie den Adobe-Support mit <br/><br/>**Dokumentation**: [Push-Konfiguration](../push/push-configuration.md) |
| **CJMPTS-1023-500** | Interner Server-Fehler während des Push-Sendevorgangs (Drittanbieter-Gateways) | Temporäre Cloud-Störung oder unbekannter Service-Fehler | &#x200B;1. Überprüfen Sie die Provider-/Kanal-<br/>.2. Gateway-Status von Drittanbietern überprüfen<br/>3. Nach einigen Minuten erneut versuchen<br/>4. Überprüfen Sie die Protokolle für <br/><br/>**weitere kontextbezogene Dokumentation**: [Push-Benachrichtigungen](../push/create-push.md) |
| **CJMPTS-1310-500** | Interner Fehler vom Render-Dienst (Vorschau oder Live-Versand) | Der nachgelagerte Vorlagen-Renderer ist in der Regel aufgrund von JSON-/Vorlagensyntax-Problemen fehlgeschlagen | &#x200B;1. Validieren der Vorlagensyntax und -struktur<br/>2. Überprüfen Sie, ob alle Personalisierungsvariablen gültig sind<br/>3. Verwenden Sie eine Test-Payload, um das Problem zu identifizieren<br/>4. Vereinfachung der Vorlagenkomplexität bei Bedarf <br/><br/>**Verwandte Dokumentation**: [Nachrichtenvorlagen](../content-management/content-templates.md), [Personalization-Syntax](../personalization/personalization-syntax.md) |

### CJMRT: Journey-Laufzeit- und API-Fehler {#cjmrt-errors}

Diese Fehler treten bei der Journey-Ausführung, der Ereignisverarbeitung und bei API-Vorgängen auf.

| Fehler-Code | Beschreibung | Grundursache | Auflösung |
|------------|-------------|-----------|-----------|
| **CJMRT-110001-500** | Maximale Anzahl von Ausführungen für Workflow-Schritt überschritten (z. B. Zeitüberschreitung bei Bereitstellungsschritt der IP-Affinität) | Der Workflow-/Bereitstellungsauftrag wurde nicht innerhalb der zulässigen Zeiträume abgeschlossen, was häufig auf eine Infrastruktur-/Service-Verzögerung oder ein temporäres Backend-Problem zurückzuführen ist. | &#x200B;1. Versuchen Sie es später erneut<br/>2. [Adobe-Status](https://status.adobe.com/de/) auf Ausfälle <br/>. Eskalieren Sie an den Adobe-Support mit workflow/job/org details<br/>4. Angabe von Protokollen und Netzwerkaufnahmen, falls verfügbar <br/><br/>**Verwandte Dokumentation**: [Fehlerbehebung beim Journey](troubleshooting.md) |
| **CJMRT-000071-400** | Fehlerhafte Anfrage beim Journey-/Testereignis oder API-Aufruf | Payload/Parameter sind fehlerhaft oder fehlen; Eingabe verweist auf eine nicht vorhandene oder inaktive Ressource | &#x200B;1. Prüfen Sie den Anfragetext auf Fehlerdetails<br/>2. Korrekte Referenz/Parameter<br/>3. Entfernen Sie die erweiterte Konfiguration und versuchen Sie es <br/>. Fügen Sie Funktionen einzeln hinzu, um die <br/><br/>**Dokumentation zu identifizieren**: [Fehlerbehebung beim Journey](troubleshooting.md), [Ereigniskonfiguration](../event/about-events.md) |
| **CJMRT-000013-401** | Nicht autorisierter Fehler während des Nachrichtenlaufzeitvorgangs/API-Ereignisses | Authentifizierungsfehler: Token ist abgelaufen, Berechtigungen fehlen oder die Integration/der Benutzer hat den Zugriff auf die Umgebung verloren | &#x200B;1. Überprüfen Sie Berechtigungen und Rollen<br/>2. Authentifizierungstoken3 <br/>. Verwenden Sie ein bekanntermaßen gültiges Benutzer-/Dienstkonto<br/>4. Produktprofilzuweisungen lesen <br/><br/>**Verwandte Dokumentation**: [Berechtigungen](../administration/permissions.md) |
| **CJMRT-080605-400** | Fehlerhafte Anfrage von der Journey-Laufzeit (z. B. Knoten-Trigger, Aktion usw.) | Konfiguration verweist auf eine entfernte/umbenannte oder veraltete Funktion/Vorlage/einen veralteten Kanal | &#x200B;1. Validieren Sie alle Ressourcenverweise<br/>2. Audit der Journey-Konfiguration und Feature Flags<br/>3. Aktualisieren Sie fehlerhafte Verweise<br/>4. Aktuelle Systemaktualisierungen und Migrationen ansehen <br/><br/>**Verwandte Dokumentation**: [Erstellung von Journey](journey-gs.md) |
| **CJMRT-030012-422** | Nicht verarbeitbare Entität - fehlgeschlagene Aktion, ungültiges Ereignis oder ungültige Payload | Ungültige Eingabedaten (z. B. nicht vorhandene Zielgruppe, Ereignis oder Attribut) | &#x200B;1. Überprüfen Sie die Payload-Struktur der Eingabe/des Ereignisses<br/>2. Überprüfen, ob referenzierte Objekte (Zielgruppen, Datensätze) vorhanden und aktiv sind<br/>3. Überprüfen Sie, ob alle erforderlichen Felder vorhanden sind<br/>4. Testen Sie mit einer zweifelsfrei funktionierenden Payload-<br/><br/>**Dokumentation**: [Fehlerbehebung beim Journey](troubleshooting.md), [Ereigniskonfiguration](../event/about-events.md) |
| **CJMRT-130004-400** | Fehlerhafte Anfrage - fehlerhafte Eingabe in der Journey-Knoten- oder Kanalkonfiguration | Journey-Payload oder Konfigurationsverweise entfernt/ungültige Ressource | &#x200B;1. Überprüfen Sie die Journey-Knotenkonfiguration.<br/>. Überprüfen Sie, ob alle referenzierten Ressourcen (Nachrichten, Zielgruppen, Aktionen) vorhanden sind<br/>3. Fehlerhafte Verweise beheben oder aktualisieren<br/>4. Journey-Konfiguration bei Bedarf neu erstellen <br/><br/>**Verwandte Dokumentation**: [Journey-Erstellung](journey-gs.md), [Benutzerdefinierte Aktionen](../action/about-custom-action-configuration.md) |
| **CJMRT-000032-409** | Konflikt - Ressource existiert bereits | Versuch, eine Ressource mit doppelter ID oder doppeltem Namen zu erstellen | &#x200B;1. Verwenden Sie eindeutige IDs und Namen für alle Ressourcen<br/>2. Prüfen Sie, ob vorhandene Ressourcen mit derselben Kennung vorhanden sind<br/>3. Löschen oder Umbenennen widersprüchlicher Objekte.<br/>. Namenskonventionen lesen <br/><br/>**Verwandte Dokumentation**: [Journey Versionen](journey-gs.md#journey-versions) |
| **CJMRT-170016-400** | Fehlerhafte Anfrage beim Journey der Konfiguration/Vorschau | Fehlende erforderliche Abhängigkeit in der Payload oder fehlerhafter Vorlagenlink | &#x200B;1. Überprüfen Sie, ob alle erforderlichen Ressourcen aktiv sind<br/>2. Stellen Sie sicher, dass Vorlagen und Inhaltsbausteine veröffentlicht werden<br/>3. Überprüfen Sie, ob alle Abhängigkeiten ordnungsgemäß verknüpft sind<br/>4. Überprüfen Sie die Ergebnisse des Journey <br/><br/>**Testmodus.Verwandte**: [Testen von Journey](testing-the-journey.md), [Journey-Abhängigkeiten](journey-gs.md) |
| **CJMRT-080608-400** | Fehlerhafte Anfrage in Domain/Kanal/Delegierung | Erforderliche DNS-Einträge oder E-Mail-/SMS-Konfiguration fehlen | &#x200B;1. Vollständige DNS-Konfiguration für E-Mail-Domains<br/>2. Überprüfen Sie, ob die Subdomain-Delegierung abgeschlossen <br/>3. Führen Sie die Konfigurationsassistenten erneut aus<br/>4. Planen Sie Zeit für die DNS-Verbreitung ein (bis zu 72 Stunden)<br/><br/>**Verwandte Dokumentation**: [Kanaloberflächen](../configuration/channel-surfaces.md), [Subdomain-Delegierung](../configuration/delegate-subdomain.md) |
| **CJMRT-110100-500** | Interner Fehler bei Payload | Backend-Daten-/Konfigurationsfehler oder nicht unterstützte Konfiguration | &#x200B;1. Wiederholen Sie den Vorgang<br/>2. Vereinfachte Konfiguration bei Verwendung erweiterter Funktionen<br/>3. Eskalieren Sie an den Adobe-Support mit der Anfrage-ID und der exakten Payload<br/>4. Suchen Sie in den Versionshinweisen/<br/><br/>**Dokumentation nach bekannten**: [Fehlerbehebung beim Journey](troubleshooting.md) |

### CJMAS: Fehler beim Nachrichtenerstellungs-Service {#cjmmas-errors}

Diese Fehler treten beim Erstellen, Bearbeiten oder Veröffentlichen von Nachrichten, Vorgaben und Inhalten auf.

| Fehler-Code | Beschreibung | Grundursache | Auflösung |
|------------|-------------|-----------|-----------|
| **CJMMAS-1732-500** | Testversand ist fehlgeschlagen - Alle Assets werden nicht veröffentlicht, wenn ein Testversand mit einem AEM-Asset durchgeführt wird | Kürzlich veröffentlichte Assets befinden sich noch nicht in AJO. Asset-ID stimmt nicht überein. Repository-übergreifende Verwendung; AEM-Synchronisierungsverzögerung | &#x200B;1. Verwenden Sie nur veröffentlichte Asset-IDs aus dem richtigen Repository/der richtigen Umgebung<br/>2. Zeit für die Synchronisierung zwischen AEM und AJO<br/>3 zulassen. Versuchen Sie es erneut mit einem zweifelsfrei funktionierenden Asset<br/>4. Überprüfen des Asset-Veröffentlichungsstatus in der AEM <br/><br/>**bezogenen Dokumentation**: [Assets-Integration](../content-management/assets.md) |
| **CJMMAS-1069-500** | Interner Fehler beim Speichern oder Veröffentlichen der Nachrichtenvorlage | Backend-Ausnahme (Fehler in Infrastruktur/Service oder Content-Problem); nicht unterstütztes Markup/nicht unterstützte Funktion | &#x200B;1. Vereinfachung oder Verringerung der Vorlagenkomplexität<br/>2. Fügen Sie in inkrementellen Schritten erneut Inhalte hinzu, um das Problem zu identifizieren<br/>3. Überprüfen Sie die [Adobe-Statusseite](https://status.adobe.com/de/)<br/>4. Entfernen Sie nicht unterstützte Funktionen oder <br/><br/>**Dokumentation**: [Inhaltsvorlagen](../content-management/content-templates.md) |
| **CJMMAS-1149-400** | Fehlerhafte Anfrage beim Speichern von Nachricht, Voreinstellung oder Variante | Erforderliche Felder fehlen in der Nachricht oder fehlerhafte Konfiguration | &#x200B;1. Füllen Sie alle erforderlichen Felder (mit einem Sternchen gekennzeichnet)<br/>2 aus. Validieren der Nachrichten-/Voreinstellungskonfiguration <br/>3. Überprüfen Sie die Formate und Begrenzungen der Feldwerte<br/>4. Überprüfen Sie die Validierungsmeldungen in der <br/><br/>**-bezogenen Dokumentation**: [E-Mail-](../email/get-started-email.md), [Kanaloberflächen](../configuration/channel-surfaces.md) |
| **CJMMAS-2073-422** | Nicht verarbeitbare Entität bei der Bearbeitung der Nachrichtenvoreinstellung | Validierungsfehler, nicht unterstütztes Feld oder falsche Syntax | &#x200B;1. Korrigieren Sie Syntax-/Feldfehler wie angegeben<br/>2. Vergleich mit einer zweifelsfrei funktionierenden Konfiguration<br/>3. Validierung der Nachrichtenbenutzeroberfläche vor dem Speichern von <br/>4 verwenden. Lesen Sie die Feldanforderungen in der <br/><br/>**Dokumentation**: [Nachrichtenvoreinstellungen](../configuration/channel-surfaces.md), [E-Mail-Einstellungen](../email/email-settings.md) |
| **CJMMAS-1300-500** | Interner Fehler bei der Nachrichtenbearbeitung | Backend-Absturz aufgrund von Infrastrukturproblemen, großen Inhalten oder Service-Ausfallzeiten | &#x200B;1. Vereinfachen von Vorlage/Inhalt (Reduzierung von Größe/Komplexität)<br/>2. Wiederholen Sie den Vorgang<br/>3. Arbeit inkrementell speichern<br/>4. Eskalieren Sie bei Beständigkeit an die Adobe <br/><br/>**Support-bezogene Dokumentation**: [Inhaltsvorlagen](../content-management/content-templates.md) |
| **CJMMAS-2001-200** | Erfolgsstatus aber Fehlerbanner: Ausschluss-Link fehlt | Erforderlicher Abmelde-Link fehlt in E-Mail-Variante | &#x200B;1. Fügen Sie allen E-Mail-Varianten einen Ausschluss-/Abmelde-Link hinzu<br/>2. Stellen Sie sicher, dass der Link in jeder Sprachversion 3 <br/> ist. Verwenden Sie den Personalisierungs-Helper zum Einfügen des Opt-out-Links<br/>4. Testen Sie alle Varianten vor <br/><br/>**Veröffentlichung**: [Opt-out-Verwaltung](../privacy/opt-out.md), [E-Mail-Design](../email/content-from-scratch.md) |
| **CJMMAS-1603-403** | Beim Aktualisieren/Veröffentlichen der Vorlage oder Vorgabe nicht zulässig | Dem Benutzer fehlen die erforderlichen Berechtigungen/Rollen oder die im aktuellen Status nicht zulässige Aktion | &#x200B;1. Überprüfen, ob der Benutzer über die entsprechenden Berechtigungen verfügt (Nachrichten-Manager, Autor usw.)<br/>2. Überprüfen Sie den Vorgabenstatus bzw. den Vorlagenstatus (Entwurf, veröffentlicht, archiviert)<br/>3. Fordern Sie bei Bedarf Zugriff von Administrator an<br/>4. Produktprofilzuweisungen überprüfen <br/><br/>**Verwandte Dokumentation**: [Berechtigungen](../administration/permissions.md), [Zugriffssteuerung](../administration/permissions-overview.md) |

### CJMCMP: Kampagnenfehler {#cjmcmp-errors}

Diese Fehler treten bei der Erstellung, Konfiguration und Aktivierung einer Kampagne auf.

| Fehler-Code | Beschreibung | Grundursache | Auflösung |
|------------|-------------|-----------|-----------|
| **CJMCMP-6003-400** | „Es ist mindestens eine falsche Kampagne vorhanden“ bei der Veröffentlichung/im Testmodus Journey/Nachricht | Knoten referenziert eine fehlende, nicht veröffentlichte oder ungültige Kampagne. Alte oder geklonte Journey erstellen keine Inline-Kampagnen | &#x200B;1. Öffnen Sie jeden Nachrichtenknoten und überprüfen Sie die Konfiguration<br/>2. Nachrichtenknoten 3 erneut verknüpfen oder <br/> hinzufügen. Testmodus aktivieren, um die Erstellung von Inline-Kampagnen zu erzwingen<br/>4. Wechseln Sie zum Assistenten für neue Journey, wenn das Problem häufig auftritt <br/><br/>**Dokumentation**: [Journey-Erstellung](journey-gs.md), [Journey testen](testing-the-journey.md) |
| **CJMCMP-2003-400** | UI-Banner: „Das Experiment ist falsch“ in E-Mail-Designer | Veraltetes oder fehlendes Experiment/Datenanbieter; fehlgeschlagene Bereinigung des Experiments, Schemakonflikt oder Fehler bei der Benutzeroberflächenvalidierung | &#x200B;1. Entfernen Sie nicht verwendete Experimentfelder<br/>2. Validieren von Schema- und Datenanbieterverbindungen<br/>3. Laden Sie die Benutzeroberfläche neu und löschen Sie den Browser-Cache<br/>4. Knoten/E-Mail bei ungelöstem Problem neu erstellen <br/><br/>**Verwandte Dokumentation**: [Inhaltsexperimente](../content-management/content-experiment.md) |
| **CJMCMP-3001-400** | Simulation/Vorschau „Filter für falschen Oberflächentyp“ | Knoten, der mit einer alten Struktur erstellt wurde, sendet type=surfaceId, das Backend erwartet brandingPresetId | &#x200B;1. Löschen und erstellen Sie den betroffenen Knoten<br/>2. Verwenden Sie die neue Journey-Version/Vorlage<br/>3. Verwenden Sie den Testmodus, um die Konfiguration zu löschen<br/>4. Massenneu erstellen von Knoten, wenn das Problem weit verbreitet ist <br/><br/>**Verwandte Dokumentation**: [Kanaloberflächen](../configuration/channel-surfaces.md), [Nachrichtensimulation](../content-management/preview.md) |
| **CJMCMP-2050-400** | Fehlerhafte Anfrage bei Aktivierung oder Validierung einer Kampagne | Kampagnenverweise - ungültige/fehlende Richtlinie oder Segment | &#x200B;1. Überprüfen Sie alle Kampagnenknoten-Konfigurationen<br/>2. Überprüfen Sie, ob Richtlinien-/Segmentverknüpfungen aktuell und gültig sind <br/> 3. Mit korrekter Konfiguration aktualisieren<br/>4. Kampagne vor der Aktivierung erneut testen <br/><br/>**Sachbezogene Dokumentation**: [Kampagnenerstellung](../campaigns/create-campaign.md), [Kampagnengenehmigung](../test-approve/gs-approval.md) |

### CJMTL: Fehler bei der Transportschicht {#cjmtl-errors}

Diese Fehler treten beim Nachrichtenversand und bei Versandvorgängen auf.

| Fehler-Code | Beschreibung | Grundursache | Auflösung |
|------------|-------------|-----------|-----------|
| **CJMTL-010018-422** | &quot;Personalization im Domain-Namen nicht zulässig“ beim Speichern/Senden von Inhalten | Eine zu strenge Validierung hat die Personalisierung der dynamischen href-Domain vorübergehend unterbrochen | &#x200B;1. Verknüpfungen bei Verwendung von Domain-Variablen umgestalten<br/>2. Stellen Sie sicher, dass die neueste AJO-Version verwendet wird<br/>3. Wiederholen Sie den Vorgang<br/>4. Verwenden Sie statische Domains, wenn das Problem weiterhin besteht <br/><br/>**Verwandte Dokumentation**: [Personalization-Syntax](../personalization/personalization-syntax.md), [E-Mail-Design](../email/content-from-scratch.md) |
| **CJMTL-010011-422** | Nicht verarbeitbare Entität - Push-/SMS-/E-Mail-Versand schlägt fehl, sagt „Feld ungültig“ | Payload- oder Empfänger-/Kontaktdaten fehlen oder sind ungültig | &#x200B;1. Überprüfen Sie die Protokolle auf bestimmte Feldfehler<br/>2. Profil-/Kontaktinformationen korrigieren<br/>3. Validieren mit Testprofil <br/>. Payload-Format nach Bedarf refaktorieren <br/><br/>**Verwandte Dokumentation**: [Profil-Management](../audience/get-started-profiles.md), [Testprofile](../audience/creating-test-profiles.md) |

### CJMRPS: Reporting- und Bereitstellungs-Service-Fehler {#cjmrps-errors}

Diese Fehler treten bei der Berichtskonfiguration und bei der Datensatzbereitstellung auf.

| Fehler-Code | Beschreibung | Grundursache | Auflösung |
|------------|-------------|-----------|-----------|
| **CJMRPS-1047-409** | „Konflikt. Datensatz wurde beim Hinzufügen des Reporting-Datensatzes bereits hinzugefügt | Es wird versucht, einen bereits bereitgestellten Datensatz hinzuzufügen | &#x200B;1. Überprüfen Sie die Datensatzkonfiguration in den Reporting-Einstellungen<br/>2. Datensätze nicht erneut hinzufügen, die bereits vorhanden sind<br/>3. Verwenden Sie offizielle Migrations-Checklisten für das Reporting der Migration<br/>4. Doppelte Datensatzverweise entfernen <br/><br/>**Sachbezogene Dokumentation**: [Globale Berichte](../reports/global-report.md), [Live-Berichte](../reports/live-report.md) |

## Allgemeiner Ansatz zur Fehlerbehebung {#troubleshooting-approach}

Befolgen Sie bei Auftreten eines Fehler-Codes diesen systematischen Ansatz:

1. **Fehler identifizieren**: Notieren Sie den vollständigen Fehler-Code, den HTTP-Status und alle zugehörigen Nachrichten- oder Anfrage-IDs.

2. **Service suchen**: Verwenden Sie das Service-Präfix (CJMPTS, CJMRT, CJMMAS, CJMCMP, CJMTL, CJMRPS), um zu identifizieren, welche Komponente betroffen ist.

3. **Überprüfen Sie den Status-Code**:
   * **400 (Fehlerhafte Anfrage)**: Eingabedaten und -konfiguration überprüfen
   * **403 (Verboten)**: Überprüfen Sie Berechtigungen und Zugriffsrechte
   * **409 (Konflikt)**: Suchen Sie nach doppelten oder widersprüchlichen Ressourcen
   * **422 (Nicht verarbeitbare Entität)**: Validieren von Daten anhand von Schemaanforderungen
   * **500 (Interner Server-Fehler)**: Wiederholen Sie den Vorgang und eskalieren Sie möglicherweise an den Support

4. **Aktuelle Änderungen überprüfen** Überlegen Sie, was kürzlich geändert wurde (Journey-Updates, neue Kampagnen, Konfigurationsänderungen usw.).

5. **Dokumentation einsehen**: Verwenden Sie die in diesem Handbuch enthaltenen Links, um auf die detaillierte Dokumentation für die betroffene Funktion zuzugreifen.

6. **Wiederholen, falls zutreffend**: Bei Fehlern der Serie 500 werden vorübergehende Probleme häufig durch einen einfachen Wiederholungsversuch nach einigen Minuten behoben.

7. **Bei Bedarf weiterleiten**: Wenn der Fehler nach den folgenden Lösungsschritten weiterhin auftritt, wenden Sie sich an den Adobe-Support unter:
   * Vollständiger Fehlercode
   * Anfrage-ID (falls verfügbar)
   * Schritte zur Reproduktion
   * Relevante Konfigurationsdetails

## Best Practices zur Vermeidung häufiger Fehler {#best-practices}

### Vor der Journey-Aktivierung {#journey-best-practices}

* **Alle Ressourcen validieren**: Stellen Sie sicher, dass alle referenzierten Zielgruppen, Ereignisse, Datenquellen und benutzerdefinierten Aktionen ordnungsgemäß konfiguriert sind
* **Gründlich testen**: Verwenden Sie den Testmodus, um Probleme vor der Veröffentlichung zu identifizieren [Weitere Informationen](testing-the-journey.md))
* **Volumes validieren**: Verwenden Sie Probelauf, um die Reichweite der Zielgruppe und die Verzweigungslogik vor der Live-Schaltung zu überprüfen [Weitere Informationen](journey-dry-run.md))
* **Berechtigungen überprüfen**: Stellen Sie sicher, dass Sie über die erforderlichen Zugriffsrechte für alle Komponenten verfügen
* **Abhängigkeiten überprüfen**: Stellen Sie sicher, dass alle verknüpften Nachrichten und Inhalte veröffentlicht werden

### Beim Erstellen von Nachrichten {#message-best-practices}

* **Pflichtfelder ausfüllen**: Vor dem Speichern immer alle Pflichtfelder ausfüllen
* **Opt-out-Links einschließen**: Links zur Abmeldung zu allen E-Mail-Varianten hinzufügen [Weitere Informationen](../privacy/opt-out.md))
* **Personalisierung validieren**: Alle dynamischen Inhalte mit Beispielprofilen testen ([Weitere Informationen](../personalization/personalization-build-expressions.md))
* **Vorlagen verwalten**: Vermeiden Sie übermäßig komplexe Vorlagen, die Rendering-Probleme verursachen können

### Für die Kampagnenverwaltung {#campaign-best-practices}

* **Überprüfen von Zielgruppendaten**: Stellen Sie sicher, dass Zielgruppen ordnungsgemäß konfiguriert und ausgefüllt sind
* **Genehmigungsstatus überprüfen**: Machen Sie sich mit den Genehmigungsanforderungen vertraut, bevor Sie versuchen, sie zu aktivieren ([Weitere Informationen](../test-approve/gs-approval.md))
* **Monitorkonfigurationen**: Kanaloberflächen und Voreinstellungen werden regelmäßig auf ihre Gültigkeit überprüft
* **DNS-Änderungen planen**: Lassen Sie beim Aktualisieren von Domains ausreichend Zeit für die DNS-Verbreitung

## Weitere Ressourcen {#additional-resources}

* [Fehlerbehebung bei Journeys](troubleshooting.md)
* [Fehlerbehebung bei der Ausführung](troubleshooting-execution.md)
* [Fehlerbehebung bei eingehenden Aktivitäten](troubleshooting-inbound.md)
* [Fehlerbehebung bei benutzerdefinierten Aktionen](../action/troubleshoot-custom-action.md)
* [Häufig gestellte Fragen zum Journey](journey-faq.md)
* [Leitlinien und Einschränkungen](../start/guardrails.md)

## Support erhalten {#getting-support}

Wenn Sie auf dauerhafte Fehler stoßen, die mit diesem Handbuch nicht behoben werden können:

1. **Informationen sammeln**: Erfassen Sie den Fehler-Code, die Anfrage-ID, Zeitstempel und Schritte zur Reproduktion
2. **Systemstatus überprüfen**: Besuchen Sie [Adobe-Status](https://status.adobe.com/de){target="_blank"}, um bekannte Service-Probleme anzuzeigen
3. **Suchdokumentation**: Lesen Sie [Adobe Experience League](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=de){target="_blank"} für Lösungen
4. **Engage-Community**: Stellen Sie Fragen in der [Adobe Journey Optimizer-Community](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}
5. **Adobe-Support kontaktieren**: Senden Sie ein Support-Ticket mit allen relevanten Details

>[!NOTE]
>
>Diese Fehlercode-Referenz wird laufend aktualisiert, wenn neue Codes identifiziert und dokumentiert werden. Die neuesten Informationen finden Sie regelmäßig in den [Adobe Journey Optimizer Community-Blogs](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/bg-p/journey-optimizer-blogs){target="_blank"}.

**Verwandte Themen**

* [Entmystifizierung von Adobe Journey Optimizer-Fehlercodes: Teil 1](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884){target="_blank"}
* [Entmystifizierung von Adobe Journey Optimizer-Fehler-Codes: Teil 2](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/bc-p/782661){target="_blank"}

