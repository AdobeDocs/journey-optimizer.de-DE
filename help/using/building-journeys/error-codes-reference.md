---
solution: Journey Optimizer
product: journey optimizer
title: Referenz für Fehler-Codes
description: Erfahren Sie mehr über häufige  [!DNL Adobe Journey Optimizer]  in und wie Sie sie beheben können
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: Fehler, Codes, Fehlerbehebung, Journey, Kampagne, Nachrichten
exl-id: 84924153-1bb5-465a-b91c-797628fc816c
feature_v2: []
subfeature_v2: []
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 2902
ht-degree: 68%

---

# Referenz für Fehler-Codes {#error-codes}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Adobe Journey Optimizer-Fehler-Codes strukturiert sind, wo Sie sie finden und wie Sie häufige Fehler in Journey-, Kampagnen- und Nachrichtenkonfigurationen beheben können.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] verwendet standardisierte Fehlercodes, um Probleme in Journey-, Kampagnen- und Nachrichtenkonfigurationen schnell zu identifizieren und zu beheben. Wenn Sie diese Fehler-Codes verstehen, können Sie die Zeit für die Fehlerbehebung erheblich verkürzen und die optimale Kampagnen-Leistung aufrechterhalten.

## Grundlagen zur Struktur von Fehler-Codes {#error-code-structure}

[!DNL Adobe Journey Optimizer] Fehler-Codes folgen einem konsistenten Benennungsmuster, das bei der Identifizierung der Komponente und des Problemtyps hilft:

* **Service-Präfix**: Gibt an, welcher [!DNL Adobe Journey Optimizer]-Service den Fehler erzeugt hat.
Beispiele: CJMPTS (Push/Transport-Service), CJMRT (Journey-Laufzeit), CJMMAS (Nachrichten-Authoring-Service), CJMCMP (Kampagne), CJMTL (Transportschicht), CJMRPS (Reporting/Provisioning-Service)
* **Fehlernummer**: Eindeutige Kennung für die konkrete Fehlerbedingung
* **HTTP-Status-Code**: Standard-HTTP-Status-Code (z. B. 400, 403, 422, 500)

Beispiel: `CJMRT-030012-422` zeigt einen Journey-Laufzeitfehler (CJMRT) mit Fehlernummer 030012 und HTTP-Status 422 (Unverarbeitbare Entität) an.

## So finden Sie Fehler-Codes {#find-error-codes}

Fehlercodes werden an verschiedenen Stellen in [!DNL Adobe Journey Optimizer] angezeigt:

* Berichte und Protokolle zur Journey-Ausführung
* Bildschirme für Kampagnenaktivierung
* Warnungen zur Nachrichtenvalidierung
* Systembenachrichtigungen und Warnhinweise
* API-Antworten (bei Verwendung von REST-APIs)

Notieren Sie sich bei Auftreten eines Fehlers den vollständigen Fehler-Code und alle zugehörigen Anfrage-IDs, da diese für die Fehlerbehebung und Support-Eskalation unerlässlich sind.

## Häufige Fehler-Codes nach Service {#error-codes-by-service}

Verwenden Sie diesen Abschnitt, um Fehler-Codes zu finden, die nach Service gruppiert sind.

### CJMPTS: Push- und Transport-Service-Fehler {#cjmpts-errors}

Diese Fehler treten beim Versand von Push-Benachrichtigungen und beim Nachrichtentransport auf.

| Fehler-Code | Beschreibung | Ursache | Lösung |
|------------|-------------|-----------|-----------|
| **CJMPTS-1410-500** | Interner Server-Fehler bei Push-/Kanal-Versandaktion | Ausfall des Kanal-Backends, abgelaufene Anmeldedaten, fehlerhafte Konfiguration oder Anbieterfehler | &#x200B;1. Nach Verzögerung erneut versuchen<br/>2. Anbieterkonfigurationen und -kontingente prüfen<br/>3. Gültigkeit der Push-Anmeldedaten prüfen<br/>4. Mit einem alternativen Kanal testen<br/>5. Wenn der Fehler weiterhin besteht, Adobe-Support mit Anfrage-ID kontaktieren <br/><br/>**Verwandte Dokumentation**: [Push-Konfiguration](../push/push-configuration.md) |
| **CJMPTS-1006-404** | Push/SMS schlägt mit „Ressource nicht gefunden“ fehl | Der referenzierte Anbieter/Kanal existiert nicht, ist falsch geschrieben oder die Bereitstellung wurde aufgehoben | &#x200B;1. Überprüfen und korrigieren Sie Provider-/Kanalverweise und IDs<br/>2. Sandbox-/Organisationskonfiguration prüfen<br/>3. Prüfen, ob die Kanalkonfigurationen aktiv sind<br/>4. Kanalkonfiguration bei Bedarf neu erstellen <br/><br/>**Verwandte Dokumentation**: [Kanaloberflächen](../configuration/channel-surfaces.md) |
| **CJMPTS-1510-500** | Interner Server-Fehler beim Push-Kanal-Versand | Backend-Push-/Transport-Fehlfunktion; Anbieter- oder Infrastrukturfehler | &#x200B;1. Kanalbereitstellungseinstellungen überprüfen<br/>2. Gültigkeit der Push-Anmeldedaten prüfen<br/>3. Vorgang erneut versuchen<br/>4. Wenn der Fehler weiterhin besteht, Adobe-Support mit Anfrage-ID kontaktieren <br/><br/>**Verwandte Dokumentation**: [Push-Konfiguration](../push/push-configuration.md) |
| **CJMPTS-1023-500** | Interner Server-Fehler während des Push-Versandvorgangs (Drittanbieter-Gateways) | Temporäre Cloud-Störung oder unbekannter Service-Fehler | &#x200B;1. Überprüfen Sie die Provider-/Kanal-<br/>.2. Drittanbieter-Gateway-Status prüfen<br/>3. Nach einiger Zeit erneut versuchen<br/>4. Protokolle auf weiteren Kontext prüfen <br/><br/>**Verwandte Dokumentation**: [Push-Benachrichtigungen](../push/create-push.md) |
| **CJMPTS-1310-500** | Interner Fehler des Render-Service (Vorschau oder Live-Versand) | Der nachgelagerte Vorlagen-Renderer ist fehlgeschlagen, in der Regel aufgrund von JSON-/Vorlagensyntax-Problemen | &#x200B;1. Validieren der Vorlagensyntax und -struktur<br/>2. Alle Personalisierungsvariablen auf Gültigkeit prüfen<br/>3. Test-Payload verwenden, um das Problem zu identifizieren<br/>4. Komplexität der Vorlage bei Bedarf reduzieren <br/><br/>**Verwandte Dokumentation**: [Nachrichtenvorlagen](../content-management/content-templates.md), [Personalisierungssyntax](../personalization/personalization-syntax.md) |

### CJMRT: Journey-Laufzeit- und API-Fehler {#cjmrt-errors}

Diese Fehler treten bei der Journey-Ausführung, der Ereignisverarbeitung und bei API-Vorgängen auf.

| Fehler-Code | Beschreibung | Ursache | Lösung |
|------------|-------------|-----------|-----------|
| **CJMRT-110001-500** | Maximale Anzahl von Ausführungen für Workflow-Schritt überschritten (z. B. Timeout bei Bereitstellung der IP-Affinität) | Der Workflow-/Bereitstellungsauftrag wurde nicht innerhalb der zulässigen Zeiträume/Neuversuche abgeschlossen, was häufig auf eine Infrastruktur-/Service-Verzögerung oder ein temporäres Backend-Problem zurückzuführen ist | &#x200B;1. Nach einiger Zeit erneut versuchen<br/>2. [Adobe-Status](https://status.adobe.com/de/) auf Ausfälle prüfen<br/>3. An den Adobe-Support mit Details zu Workflow/Auftrag/Organisation eskalieren<br/>4. Protokolle und Netzwerkerfassungen bereitstellen, falls verfügbar <br/><br/>**Verwandte Dokumentation**: [Journey-Fehlerbehebung](troubleshooting.md) |
| **CJMRT-000071-400** | Fehlerhafte Anfrage beim Journey-/Testereignis oder API-Aufruf | Payload/Parameter sind fehlerhaft oder fehlen; Eingabe verweist auf eine nicht vorhandene oder inaktive Ressource | &#x200B;1. Überprüfen Sie den Anfragetext auf Fehlerdetails<br/>2. Referenz/Parameter korrigieren<br/>3. Erweiterte Konfiguration entfernen und erneut versuchen<br/>4. Funktionen einzeln wieder hinzufügen, um das Problem zu identifizieren <br/><br/>**Verwandte Dokumentation**: [Journey-Fehlerbehebung](troubleshooting.md), [Ereigniskonfiguration](../event/about-events.md) |
| **CJMRT-000013-401** | Autorisierungsfehler während Nachrichtenlaufzeitvorgang/API-Ereignis | Authentifizierungsfehler: Token ist abgelaufen, Berechtigungen fehlen oder Integration/Person hat keinen Zugriff auf die Umgebung mehr | &#x200B;1. Überprüfen Sie Berechtigungen und Rollen<br/>2. Authentifizierungs-Token aktualisieren<br/>3. Nachweislich gültiges Benutzer-/Service-Konto verwenden<br/>4. Produktprofilzuweisungen prüfen <br/><br/>**Verwandte Dokumentation**: [Berechtigungen](../administration/permissions.md) |
| **CJMRT-080605-400** | Fehlerhafte Anfrage der Journey-Laufzeit (z. B. Knoten-Trigger, Aktion usw.) | Konfiguration verweist auf eine entfernte/umbenannte oder veraltete Funktion/Vorlage/einen veralteten Kanal | &#x200B;1. Validieren Sie alle Ressourcenverweise<br/>2. Journey-Konfiguration und Feature Flags prüfen<br/>3. Fehlerhafte Verweise aktualisieren<br/>4. Aktuelle Systemaktualisierungen und -migrationen überprüfen <br/><br/>**Verwandte Dokumentation**: [Journey-Erstellung](journey-gs.md) |
| **CJMRT-030012-422** | Nicht verarbeitbare Entität – fehlgeschlagene Aktion, ungültiges Ereignis oder ungültige Payload | Ungültige Eingabedaten (z. B. nicht vorhandene Zielgruppe oder nicht vorhandenes Ereignis oder Attribut) | &#x200B;1. Überprüfen Sie die Payload-Struktur der Eingabe/des Ereignisses<br/>2. Überprüfen, ob referenzierte Objekte (Zielgruppen, Datensätze) vorhanden und aktiv sind<br/>3. Überprüfen, ob alle Pflichtfelder vorhanden sind<br/>4. Mit nachweislich funktionierender Payload testen <br/><br/>**Verwandte Dokumentation**: [Journey-Fehlerbehebung](troubleshooting.md), [Ereigniskonfiguration](../event/about-events.md) |
| **CJMRT-130004-400** | Fehlerhafte Anfrage – fehlerhafte Eingabe in der Knoten- oder Kanalkonfiguration der Journey | Journey-Payload oder Konfigurationsverweise entfernt/ungültige Ressource | &#x200B;1. Überprüfen Sie die Journey-Knotenkonfiguration<br/>2. Verfizieren, dass alle referenzierten Ressourcen (Nachrichten, Zielgruppen, Aktionen) vorhanden sind<br/>3. Fehlerhafte Verweise beheben oder aktualisieren<br/>4. Journey-Konfiguration bei Bedarf neu erstellen <br/><br/>**Verwandte Dokumentation**: [Journey-Erstellung](journey-gs.md), [Benutzerdefinierte Aktionen](../action/about-custom-action-configuration.md) |
| **CJMRT-000032-409** | Konflikt – Ressource existiert bereits | Versuch, eine Ressource mit doppelter ID oder doppeltem Namen zu erstellen | &#x200B;1. Verwenden Sie eindeutige IDs und Namen für alle Ressourcen<br/>2. Prüfen, ob vorhandene Ressourcen mit derselben Kennung vorhanden sind<br/>3. Konfliktbehaftete Objekte löschen oder umbenennen<br/>. Namenskonventionen prüfen <br/><br/>**Verwandte Dokumentation**: [Journey-Erstellung](journey-gs.md) |
| **CJMRT-170016-400** | Fehlerhafte Anfrage während der Journey-Konfiguration/Vorschau | In der Payload fehlt eine notwendige Abhängigkeit oder der Vorlage-Link ist fehlerhaft | &#x200B;1. Überprüfen Sie, ob alle erforderlichen Ressourcen aktiv sind<br/>2. Sicherstellen, dass Vorlagen und Inhaltsbausteine veröffentlicht sind<br/>3. Überprüfen, ob alle Abhängigkeiten ordnungsgemäß verknüpft sind<br/>4. Ergebnisse des Journey-Testmodus überprüfen <br/><br/>**Verwandte Dokumentation**: [Testen von Journeys](testing-the-journey.md), [Journey-Abhängigkeiten](journey-gs.md) |
| **CJMRT-080608-400** | Fehlerhafte Anfrage in Domain/Kanal/Delegierung | Erforderliche DNS-Einträge oder E-Mail-/SMS-Konfiguration fehlen | &#x200B;1. Vollständige DNS-Konfiguration für E-Mail-Domains<br/>2. Verifizieren, ob die Subdomain-Delegierung abgeschlossen ist<br/>3. Konfigurationsassistenten erneut ausführen<br/>4. Zeit für DNS-Verbreitung einplanen (bis zu 72 Stunden)<br/><br/>**Verwandte Dokumentation**: [Kanaloberflächen](../configuration/channel-surfaces.md), [Subdomain-Delegierung](../configuration/delegate-subdomain.md) |
| **CJMRT-110100-500** | Interner Fehler in der Payload | Backend-Daten-/Konfigurationsfehler oder nicht unterstützte Konfiguration | &#x200B;1. Wiederholen Sie den Vorgang<br/>2. Konfiguration bei Verwendung erweiterter Funktionen vereinfachen<br/>3. An den Adobe-Support mit der Anfrage-ID und der exakten Payload eskalieren<br/>4. In den Versionshinweisen nach bekannten Fehlern suchen <br/><br/>**Verwandte Dokumentation**: [Journey-Fehlerbehebung](troubleshooting.md) |

### CJMAS: Fehler des Nachrichtenerstellungs-Services {#cjmmas-errors}

Diese Fehler treten beim Erstellen, Bearbeiten oder Veröffentlichen von Nachrichten, Voreinstellungen und Inhalten auf.

| Fehler-Code | Beschreibung | Ursache | Lösung |
|------------|-------------|-----------|-----------|
| **CJMMAS-1732-500** | Testversand ist fehlgeschlagen; alle Assets bleiben unveröffentlicht, wenn ein Testversand mit einem AEM-Asset durchgeführt wird | Kürzlich veröffentlichtes Asset ist noch nicht in AJO enthalten; Asset-ID stimmt nicht überein; Repository-übergreifende Verwendung; AEM-Synchronisierungsverzögerung | &#x200B;1. Verwenden Sie nur veröffentlichte Asset-IDs aus dem richtigen Repository/der richtigen Umgebung<br/>2. Auf Synchronisierung zwischen AEM und AJO warten<br/>3. Mit nachweislich funktionierendem Asset erneut versuchen<br/>4. Asset-Veröffentlichungsstatus in AEM prüfen <br/><br/>**Verwandte Dokumentation**: [Assets-Integration](../integrations/assets.md) |
| **CJMMAS-1069-500** | Interner Fehler beim Speichern oder Veröffentlichen der Nachrichtenvorlage | Backend-Ausnahme (Fehler in Infrastruktur/Service oder Inhaltsproblem); nicht unterstütztes Markup/nicht unterstützte Funktion | &#x200B;1. Vereinfachen oder reduzieren Sie die Vorlagenkomplexität<br/>2. Inhalte in inkrementellen Schritten erneut hinzufügen, um das Problem zu identifizieren<br/>3. [Adobe-Statusseite](https://status.adobe.com/de/) prüfen<br/>4. Nicht unterstützte Funktionen oder Markups entfernen <br/><br/>**Verwandte Dokumentation**: [Inhaltsvorlagen](../content-management/content-templates.md) |
| **CJMMAS-1149-400** | Fehlerhafte Anfrage beim Speichern von Nachricht, Voreinstellung oder Variante | Erforderliche Felder fehlen in der Nachricht oder Konfiguration ist fehlerhaft | &#x200B;1. Füllen Sie alle erforderlichen Felder (mit einem Sternchen gekennzeichnet)<br/>2 aus. Nachrichten-/Voreinstellungskonfiguration validieren<br/>3. Formate und Einschränkungen der Feldwerte prüfen<br/>4. Validierungsmeldungen auf Benutzeroberfläche prüfen <br/><br/>**Verwandte Dokumentation**: [E-Mail-Kanal](../email/get-started-email.md), [Kanaloberflächen](../configuration/channel-surfaces.md) |
| **CJMMAS-2073-422** | Nicht verarbeitbare Entität bei der Bearbeitung der Nachrichtenvoreinstellung | Validierungsfehler, nicht unterstütztes Feld oder falsche Syntax | &#x200B;1. Korrigieren Sie Syntax-/Feldfehler wie angegeben<br/>2. Mit nachweislich funktionierender Konfiguration vergleichen<br/>3. Vor dem Speichern Validierung der Nachrichtenbenutzeroberfläche verwenden<br/>4. Feldanforderungen in der Dokumentation nachlesen <br/><br/>**Verwandte Dokumentation**: [Nachrichtenvoreinstellungen](../configuration/channel-surfaces.md), [E-Mail-Einstellungen](../email/email-settings.md) |
| **CJMMAS-1300-500** | Interner Fehler bei der Nachrichtenerstellung | Backend-Absturz aufgrund von Infrastrukturproblemen, großen Inhalten oder Service-Ausfall | &#x200B;1. Vereinfachen von Vorlage/Inhalt (Reduzierung von Größe/Komplexität)<br/>2. Vorgang erneut versuchen<br/>3. Arbeit inkrementell speichern<br/>4. Wenn der Fehler weiterhin besteht, an Adobe Support eskalieren <br/><br/>**Verwandte Dokumentation**: [Inhaltsvorlagen](../content-management/content-templates.md) |
| **CJMMAS-2001-200** | Status „erfolgreich“, aber Fehler-Banner: Opt-out-Link fehlt | Erforderlicher Abmelde-Link fehlt in E-Mail-Variante | &#x200B;1. Fügt allen E-Mail-Varianten einen Ausschluss-/Abmelde-Link hinzu<br/>2. Sicherstellen, dass der Link in jeder Sprachversion vorhanden ist<br/>3. Personalisierungs-Helper zum Einfügen des Opt-out-Links verwenden<br/>4. Alle Varianten vor Veröffentlichung testen <br/><br/>**Verwandte Dokumentation**: [Opt-out-Verwaltung](../privacy/opt-out.md), [E-Mail-Design](../email/content-from-scratch.md) |
| **CJMMAS-1603-403** | Beim Aktualisieren/Veröffentlichen der Vorlage oder Voreinstellung nicht zulässig | Benutzerin bzw. Benutzer verfügt nicht über die erforderlichen Berechtigungen/Rollen oder Aktion ist im aktuellen Status nicht zulässig | &#x200B;1. Stellen Sie sicher, dass der Benutzer über die entsprechenden Berechtigungen verfügt (Nachrichten-Manager, Autor usw.)<br/>2. Status der Voreinstellung bzw. der Vorlage überprüfen (Entwurf, veröffentlicht, archiviert)<br/>3. Bei Bedarf Zugriff von Ihrer oder Ihrem Admin anfordern<br/>4. Produktprofilzuweisungen überprüfen <br/><br/>**Verwandte Dokumentation**: [Berechtigungen](../administration/permissions.md), [Zugriffssteuerung](../administration/permissions-overview.md) |

### CJMCMP: Kampagnenfehler {#cjmcmp-errors}

Diese Fehler treten bei der Erstellung, Konfiguration und Aktivierung einer Kampagne auf.

| Fehler-Code | Beschreibung | Ursache | Lösung |
|------------|-------------|-----------|-----------|
| **CJMCMP-6003-400** | „Mindestens eine Kampagne ist falsch“ bei der Veröffentlichung oder im Testmodus einer Journey bzw. Nachricht | Der Knoten verweist auf eine fehlende, nicht veröffentlichte oder ungültige Kampagne; alte oder geklonte Journeys erstellen keine Inlines | &#x200B;1. Öffnen Sie jeden Nachrichtenknoten und überprüfen Sie die Konfiguration<br/>2. Nachrichtenknoten neu verknüpfen oder erneut hinzufügen<br/>3. Testmodus aktivieren, um die Erstellung von Inline-Kampagnen zu erzwingen<br/>4. Zum Assistenten für neue Journeys wechseln, wenn das Problem häufig auftritt <br/><br/>**Verwandte Dokumentation**: [Erstellen von Journeys](journey-gs.md), [Testen von Journeys](testing-the-journey.md) |
| **CJMCMP-2003-400** | Benutzeroberflächen-Banner: „Das Experiment ist falsch“ in E-Mail-Designer | Veraltetes oder fehlendes Experiment bzw. veralteter oder fehlender Datenanbieter; fehlgeschlagene Bereinigung des Experiments, Schemakonflikt oder Fehler bei der Benutzeroberflächenvalidierung | &#x200B;1. Ungenutzte Experimentfelder entfernen<br/>2. Verbindungen für Schemata und Datenanbieter validieren<br/>3. Benutzeroberfläche neu laden und Browsercache löschen<br/>4. Knoten/E-Mail neu erstellen, falls das Problem nicht gelöst ist <br/><br/>**Verwandte Dokumentation**: [Inhaltsexperimente](../content-management/content-experiment.md) |
| **CJMCMP-3001-400** | Simulation/Vorschau „Falscher Filter für den Oberflächentyp“ | Ein Knoten, der mit einer alten Struktur erstellt wurde, sendet „type=surfaceId“, Backend erwartet „brandingPresetId“ | &#x200B;1. Löschen und erstellen Sie den betroffenen Knoten <br/>2 neu. Neue Journey-Version/-Vorlage verwenden<br/>3. Testmodus verwenden, um die Konfiguration zu löschen<br/>4. Knoten massenhaft neu erstellen, wenn das Problem weit verbreitet ist <br/><br/>**Verwandte Dokumentation**: [Kanaloberflächen](../configuration/channel-surfaces.md), [Nachrichtensimulation](../content-management/preview.md) |
| **CJMCMP-2050-400** | Fehlerhafte Anfrage bei Aktivierung oder Genehmigung einer Kampagne | Kampagnenverweise ungültig/fehlende Richtlinie oder fehlendes Segment | &#x200B;1. Alle Kampagnenknotenkonfigurationen prüfen<br/>2. Überprüfen, ob Richtlinien- bzw. Segmentverknüpfungen aktuell und gültig sind<br/>3. Mit der korrekten Konfiguration aktualisieren<br/>4. Kampagne vor der Aktivierung erneut testen <br/><br/>**Verwandte Dokumentation**: [Erstellen einer Kampagne](../campaigns/create-campaign.md), [Genehmigen einer Kampagne](../test-approve/gs-approval.md) |

### CJMTL: Fehler der Transportschicht {#cjmtl-errors}

Diese Fehler treten während des Nachrichtentransports und bei Versandvorgängen auf.

| Fehler-Code | Beschreibung | Ursache | Lösung |
|------------|-------------|-----------|-----------|
| **CJMTL-010018-422** | „Personalisierung im Domain-Namen nicht zulässig“ beim Speichern/Senden von Inhalten | Eine zu strenge Validierung hat die dynamische Personalisierung der href-Domain vorübergehend unterbrochen | &#x200B;1. Links bei Verwendung von Domain-Variablen umgestalten<br/>2. Verifizieren, dass die neueste AJO-Version verwendet wird<br/>3. Vorgang erneut versuchen<br/>4. Statische Domains verwenden, wenn das Problem weiterhin besteht <br/><br/>**Verwandte Dokumentation**: [Personalisierungssyntax](../personalization/personalization-syntax.md), [E-Mail-Design](../email/content-from-scratch.md) |
| **CJMTL-010011-422** | Nicht verarbeitbare Entität – Push-/SMS-/E-Mail-Versand schlägt fehl, Meldung „Feld ungültig“ | Payload- oder Empfänger-/Kontaktdaten fehlen oder sind ungültig | &#x200B;1. Überprüfen Sie die Protokolle auf bestimmte Feldfehler<br/>2. Profil-/Kontaktinformationen korrigieren<br/>3. Mit Testprofil validieren<br/>4. Payload-Format nach Bedarf refaktorieren <br/><br/>**Verwandte Dokumentation**: [Profil-Management](../audience/get-started-profiles.md), [Testprofile](../audience/creating-test-profiles.md) |

### CJMRPS: Reporting- und Provisioning-Service-Fehler {#cjmrps-errors}

Diese Fehler treten bei der Reporting-Konfiguration und bei der Datensatzbereitstellung auf.

| Fehler-Code | Beschreibung | Ursache | Lösung |
|------------|-------------|-----------|-----------|
| **CJMRPS-1047-409** | „Konflikt. Datensatz wurde bereits hinzugefügt“ wird beim Hinzufügen des Reporting-Datensatzes angezeigt | Es wird versucht, einen bereits bereitgestellten Datensatz hinzuzufügen | &#x200B;1. Überprüfen Sie die Datensatzkonfiguration in den Reporting-Einstellungen<br/>2. Keine bereits vorhandenen Datensätze erneut hinzufügen<br/>3. Offizielle Migrations-Checklisten für die Reporting-Migration verwenden<br/>4. Doppelte Datensatzverweise entfernen <br/><br/>**Verwandte Dokumentation**: [Reporting – Überblick](../reports/gs-reports.md), [Kampagnenberichte](../reports/campaign-global-report-cja.md), [Journey-Berichte](../reports/journey-global-report-cja.md) |

## Allgemeiner Fehlerbehebungsansatz {#troubleshooting-approach}

Gehen Sie bei Auftreten eines Fehler-Codes entsprechend dem folgenden systematischen Ansatz vor:

1. **Identifizieren Sie den Fehler**: Notieren Sie den vollständigen Fehler-Code, den HTTP-Status und alle zugehörigen Nachrichten- oder Anfrage-IDs.

2. **Suchen Sie den Service**: Identifizieren Sie die betroffene Komponente anhand des Service-Präfix (CJMPTS, CJMRT, CJMMAS, CJMCMP, CJMTL, CJMRPS).

3. **Prüfen Sie den Status-Code**:
   * **400 (Fehlerhafte Anfrage)**: Prüfen Sie Eingabedaten und -konfiguration.
   * **403 (Unzulässig)**: Prüfen Sie Berechtigungen und Zugriffsrechte.
   * **409 (Konflikt)**: Suchen Sie doppelte oder miteinander in Konflikt stehende Ressourcen.
   * **422 (Nicht verarbeitbare Entität)**: Prüfen Sie Daten anhand der Schemaanforderungen.
   * **500 (Interner Server-Fehler)**: Versuchen Sie den Vorgang erneut und eskalieren Sie ihn bei Bedarf an den Support.

4. **Prüfen Sie kürzlich vorgenommene Änderungen**: Berücksichtigen Sie, was kürzlich geändert wurde (Journey-Updates, neue Kampagnen, Konfigurationsänderungen usw.).

5. **Lesen Sie in der Dokumentation nach**: Verwenden Sie die in diesem Leitfaden enthaltenen Links, um auf die detaillierte Dokumentation für die betroffene Funktion zuzugreifen.

6. **Versuchen Sie es ggf. erneut**: Bei Fehlern der Serie 500 kann ein einfacher Neuversuch nach einigen Minuten vorübergehende Probleme beheben.

7. **Bei Bedarf eskalieren**: Wenn der Fehler nach den folgenden Behebungsschritten weiterhin besteht, [kontaktieren Sie den Adobe-Support](../start/user-interface.md#support-ticket-guidelines) mit dem vollständigen Fehler-Code, der Anfrage-ID (falls verfügbar), den Schritten zur Reproduktion und relevanten Konfigurationsdetails.

## Best Practices zur Vermeidung häufiger Fehler {#best-practices}

Verwenden Sie diese Verfahren, um vermeidbare Fehler zu reduzieren und die Zuverlässigkeit zu verbessern.

### Vor der Journey-Aktivierung {#journey-best-practices}

* **Validieren Sie alle Ressourcen**: Stellen Sie sicher, dass alle referenzierten Zielgruppen, Ereignisse, Datenquellen und benutzerdefinierten Aktionen ordnungsgemäß konfiguriert sind.
* **Testen Sie sorgfältig**: Verwenden Sie den Testmodus, um Probleme vor der Veröffentlichung zu identifizieren. ([Weitere Informationen](testing-the-journey.md))
* **Validieren Sie die Volumen**: Verwenden Sie einen Probelauf, um die Reichweite der Zielgruppe und die Verzweigungslogik vor der Live-Schaltung zu prüfen. ([Weitere Informationen](journey-dry-run.md))
* **Prüfen Sie Berechtigungen**: Stellen Sie sicher, dass Sie über die erforderlichen Zugriffsrechte für alle Komponenten verfügen.
* **Prüfen Sie Abhängigkeiten**: Stellen Sie sicher, dass alle verknüpften Nachrichten und Inhalte veröffentlicht werden.

### Beim Erstellen von Nachrichten {#message-best-practices}

* **Füllen Sie Pflichtfelder aus**: Füllen Sie vor dem Speichern immer alle Pflichtfelder aus.
* **Schließen Sie Opt-out-Links ein**: Fügen Sie allen E-Mail-Varianten Abmelde-Links hinzu. ([Weitere Informationen](../privacy/opt-out.md))
* **Validieren Sie die Personalisierung**: Testen Sie alle dynamischen Inhalte mit Beispielprofilen. ([Weitere Informationen](../personalization/personalization-build-expressions.md))
* **Halten Sie Vorlagen überschaubar**: Vermeiden Sie übermäßig komplexe Vorlagen, die Probleme beim Rendering verursachen können

### Für die Kampagnenverwaltung {#campaign-best-practices}

* **Überprüfen Sie Zielgruppendaten**: Stellen Sie sicher, dass Zielgruppen ordnungsgemäß konfiguriert und befüllt sind
* **Überprüfen Sie den Genehmigungsstatus**: Machen Sie sich mit den Genehmigungsanforderungen vertraut, bevor Sie eine Aktivierung versuchen ([Weitere Informationen](../test-approve/gs-approval.md))
* **Überwachen Sie Konfigurationen**: Überprüfen Sie Kanaloberflächen und Voreinstellungen regelmäßig auf ihre Gültigkeit
* **Planen Sie DNS-Änderungen**: Planen Sie bei der Aktualisierung von Domains ausreichend Zeit für die DNS-Verbreitung ein

## Zusätzliche Ressourcen {#additional-resources}

* [Fehlerbehebung in Journeys](troubleshooting.md)
* [Fehlerbehebung der Ausführung](troubleshooting-execution.md)
* [Fehlerbehebung bei eingehenden Aktivitäten](troubleshooting-inbound.md)
* [Fehlerbehebung bei benutzerdefinierten Aktionen](../action/troubleshoot-custom-action.md)
* [Häufig gestellte Fragen zu Journeys](journey-faq.md)
* [Leitlinien und Einschränkungen](../start/guardrails.md)

## Erhalten von Unterstützung {#getting-support}

Gehen Sie folgendermaßen vor, wenn Sie auf anhaltende Fehler stoßen, die mit diesem Handbuch nicht behoben werden können:

1. **Sammeln Sie Informationen**: Erfassen Sie den Fehler-Code, die Anfrage-ID, die Zeitstempel und die Schritte zum Nachstellen
2. **Überprüfen Sie den Systemstatus**: Besuchen Sie [Adobe-Status](https://status.adobe.com/de/){target="_blank"} für bekannte Service-Probleme
3. **Durchsuchen Sie die Dokumentation**: Suchen Sie in [Adobe Experience League](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=de){target="_blank"} nach Lösungen
4. **Engage-Community**: Stellen Sie Fragen in der [[!DNL Adobe Journey Optimizer] Community](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=de){target="_blank"}
5. **Adobe-Support kontaktieren**: [Senden eines Support-Tickets](../start/user-interface.md#support-ticket-guidelines) mit allen relevanten Details

>[!NOTE]
>
>Diese Fehler-Code-Referenz wird laufend aktualisiert, wenn neue Codes identifiziert und dokumentiert werden. Die aktuellsten Informationen finden Sie in den [[!DNL Adobe Journey Optimizer] Community-Blogs](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/bg-p/journey-optimizer-blogs?profile.language=de){target="_blank"}.

**Verwandte Themen**

* [Entmystifizierung [!DNL Adobe Journey Optimizer] Fehler-Codes: Teil 1](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884){target="_blank"}
* [Entmystifizierung [!DNL Adobe Journey Optimizer] Fehler-Codes: Teil 2](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/bc-p/782661?profile.language=de){target="_blank"}

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Diese Seite ist eine Referenzanleitung zu standardisierten Adobe Journey Optimizer-Fehlercodes, die nach Service-Präfix geordnet sind, die Ursache jedes Fehlers erklären und eine schrittweise Anleitung zur Behebung bieten.

**intents:**

* Ermitteln Sie mithilfe des Service-Präfixes im Fehlercode, welcher AJO-Service einen Fehler erzeugt hat.
* Diagnose und Behebung von Push-/Transportfehlern (CJMPTS), die den Nachrichtenversand beeinträchtigen
* Fehlerbehebung bei Journey-Laufzeitfehlern und API-Fehlern (CJMRT) während der Journey-Ausführung oder Ereignisverarbeitung
* Beheben von Fehlern beim Verfassen von Nachrichten (CJMAS) beim Erstellen, Speichern oder Veröffentlichen von Nachrichten
* Beheben von Kampagnenfehlern (CJMCMP) während der Aktivierung oder Genehmigung der Kampagne
* Eskalieren persistenter Fehler an den Adobe-Support mit den richtigen Informationen

**Glossar:**

* **Service-Präfix**: Der alphanumerische Code am Anfang eines AJO-Fehlercodes, der angibt, welcher Service den Fehler verursacht hat (z. B. CJMRT = Journey Runtime) *(produktspezifisch)*
* **HTTP-Status-Code**: Der Standardstatus-Code, der in einen AJO-Fehler-Code eingebettet ist (z. B. 400 = Ungültige Anfrage, 403 = Verboten, 422 = Nicht verarbeitbare Entität, 500 = Interner Server-Fehler)
* **Anfrage-ID**: Eine eindeutige Kennung, die zu einem Fehler hinzugefügt wird, der bei der Eskalation an den Adobe Support *(produktspezifisch) erforderlich ist*
* **CJMRT**: Journey-Laufzeitdienst-Präfix - Fehler bei der Journey-Ausführung und bei API-Vorgängen *(produktspezifisch)*
* **CJMMAS**: Präfix des Nachrichtenerstellungs-Service — Fehler bei der Erstellung und Veröffentlichung von Nachrichten *(produktspezifisch)*
* **CJMPTS**: Push-/Transport-Service-Präfix — Fehler bei Push-Benachrichtigung und Nachrichtentransport *(produktspezifisch)*

**Leitplanken:**

* E-Mail-Varianten müssen einen Ausschluss-/Abmelde-Link enthalten; er wird ausgelassen mit den Trigger CJMMAS-2001-200.
* Zum Anhalten eines Journey ist die Berechtigung Journey verwalten erforderlich (relevant für CJMRT-Fehler, die Berechtigungen beinhalten).
* Die DNS-Verbreitung für die Zuweisung von Subdomains kann bis zu 72 Stunden dauern (relevant für CJMRT-080608-400).
* Suchschlüssel für Datensatzsuchaktivitäten müssen im erweiterten Modus definiert werden, nicht im einfachen Modus.

**Terminologie:**

* Kanonischer Name: Fehlercode — Akronym: n/a — Varianten: Fehlermeldung, Fehlerkennung
* Synonyme: „service prefix“ = „error prefix“ = „Komponenten-ID“
* Verwechseln Sie nicht: „400 Bad Request“ ≠ „422 Unverarbeitbare Entität“ — 400 zeigt eine fehlerhafte Eingabe an; 422 zeigt ein gültiges Format, aber ungültige Inhalte gemäß Schemaregeln an

**FAQ:**

* **F: Woher weiß ich, welcher AJO-Service einen Fehler verursacht hat?** — Lesen Sie das Service-Präfix zu Beginn des Fehler-Codes: CJMPTS (Push/Transport), CJMRT (Journey-Laufzeit), CJMMAS (Nachrichtenbearbeitung), CJMCMP (Kampagne), CJMTL (Transportschicht), CJMRPS (Reporting/Bereitstellung).
* **F: Was sollte ich tun, wenn ich einen Fehler der 500-Serie erhalte?** — Wiederholen Sie den Vorgang nach einigen Minuten, überprüfen Sie Adobe Status auf Ausfälle und eskalieren Sie dann an Adobe-Support mit dem vollständigen Fehler-Code und der Anfrage-ID, wenn das Problem weiterhin besteht.
* **F: Warum zeigt CJMMAS-2001-200 ein Fehlerbanner an, obwohl der Status „Erfolg“ lautet?** — In einer E-Mail-Variante fehlt ein erforderlicher Ausschluss-/Abmelde-Link. Fügen Sie ihn allen Varianten und Sprachversionen hinzu.
* **F: Welche Informationen sollte ich sammeln, bevor ich mich an den Adobe-Support wende?** — Erfassen Sie den vollständigen Fehler-Code, die Anfrage-ID, Zeitstempel, Schritte zur Reproduktion und alle relevanten Konfigurationsdetails.
* **F: Was verursacht CJMRT-030012-422?** — Ungültige Eingabedaten, z. B. Verweis auf eine nicht vorhandene Zielgruppe, ein Ereignis oder ein Attribut; Überprüfen, ob alle referenzierten Objekte vorhanden und aktiv sind.

+++
