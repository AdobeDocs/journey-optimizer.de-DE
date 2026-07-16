---
solution: Journey Optimizer
product: journey optimizer
title: Dokumentation – Aktualisierungen
description: Erfahren Sie mehr über die letzten Aktualisierungen der Dokumentation
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: eef9b6b37edd1722fb9894b18e1504496c70a142
workflow-type: tm+mt
source-wordcount: 9685
ht-degree: 87%

---

# Dokumentation – Aktualisierungen {#latest-updates}

Auf dieser Seite werden alle aktuellen Änderungen in der [!DNL Journey Optimizer] Dokumentation sowie die Aktualisierungen im Zusammenhang mit den Funktionen und Verbesserungen der monatlichen Versionen aufgeführt.

## Juli 2026 {#july-2026}

* Die Seite **Inhaltsprüfung** wurde mit einem neuen Abschnitt **Informationen zur HTML- und CSS-Größe** aktualisiert, in dem erläutert wird, was in der Schätzung zur Bearbeitungszeit enthalten ist (HTML-Struktur, Inline-CSS, Personalisierungs-Token, Fragmente, bedingte Blöcke und Bildreferenzen), warum sich die Schätzung von der bereitgestellten Größe unterscheidet und was die Größenwarnungen für Autorinnen und Autoren bedeuten. [Weitere Informationen](../email/content-check.md#size-estimation)

* Die Seite **Erstellen von IP-Aufwärmkampagnen** wurde aktualisiert, um klarzustellen, dass Zielgruppenbestimmungsregeln auf IP-Aufwärmkampagnen angewendet werden können, und um das Auswertungsverhalten zu dokumentieren: Die Zielgruppenzugehörigkeit wird bei der Ausführungsaktivierung (tägliche Batch-Segmentierung) festgelegt, während Profilattribute zur Ausführungszeit aus den zuletzt erfassten Batch-Daten gelesen werden. [Weitere Informationen](../configuration/ip-warmup-campaign.md)
* Die Seite **Beenden eines Journey** wurde aktualisiert, um den automatischen Stopp-Zeitpunkt für nicht wiederkehrende Journey von „Zielgruppe lesen“ zu verdeutlichen: ein Sicherheitspuffer von ca. **96 Stunden (~4 Tage)** nach der geplanten Ausführung, während der die Journey im **Live**-Status verbleiben kann, bevor sie beim nächsten Scannerdurchgang auf **Angehalten** wechselt. Auf der Seite wird nun auch klargestellt, dass Wavebasierte Journey , einschließlich Anwendungsfällen für die Sendezeitoptimierung, von diesem automatischen Stopp ausgeschlossen sind und stattdessen dem standardmäßigen 91-Tage-Journey-Timeout folgen. [Weitere Informationen](../building-journeys/end-journey.md#auto-stop-non-recurring)

* Die Seiten **Benutzerdefinierter Upload** und **Zielgruppe lesen** wurden korrigiert, um das inkrementelle Leseverhalten für externe/benutzerdefinierte Zielgruppen (einschließlich CSV-Upload und Federated Audience Composition) zu verdeutlichen: Inkrementelles Lesen wird für diese Zielgruppentypen heute nicht funktional unterstützt, und die vollständige Zielgruppe wird bei jeder Wiederholung verarbeitet, unabhängig von der Einstellung Inkrementelles Lesen . Die Anleitung verknüpft nun Wiederholungskontrollen, einschließlich **Erneuten Eintritt bei Wiederholung erzwingen**. [Weitere Informationen über benutzerdefiniertes Hochladen](../audience/custom-upload.md) und [Weitere Informationen zum Lesen von Zielgruppen-Zeitplänen](../building-journeys/read-audience.md#schedule)

* Auf der Seite **PTR-Einträge bearbeiten** wurde eine Warnung hinzugefügt, die Kunden darüber informiert, dass beim Hinzufügen eines neuen Forward-DNS-Eintrags zu ihrer Plattform der Forward-DNS-Eintrag für die alte Subdomain erst entfernt werden darf, wenn die Verschiebung abgeschlossen ist, da sonst die Bearbeitung fehlschlägt. [Weitere Informationen](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

* Die Seiten **Senden mithilfe von**) wurden aktualisiert, um das Verhalten bei der Neubewertung der Zielgruppe über mehrere Schübe hinweg zu verdeutlichen: Die Zielgruppenzugehörigkeit wird zum Zeitpunkt der Aktivierung (Momentaufnahme) festgelegt, aber Profilattribute und Einverständnis werden zum Zeitpunkt der Verarbeitung jeder Schübe ausgewertet. Das bedeutet, dass Ausstiegsoptionen zwischen mehreren Schüben respektiert werden. Weitere Informationen finden Sie in den häufig gestellten Fragen [&#128279;](../building-journeys/send-using-waves.md#faq) &lbrace;0[Journey](../campaigns/send-using-waves.md#faq) und Kampagnen.

* Die **Data Governance** wurde aktualisiert, um klarzustellen, dass die Durchsetzung der DULE-Richtlinie nur für (**) Profilattributfelder**. Ereignisbasierte Felder (Kontextattribute wie das Journey von Ereignisfeldern) werden nicht unterstützt: Beschriftungen, die auf diese Felder in der Benutzeroberfläche angewendet werden, schränken die Datennutzung nicht ein. [Weitere Informationen](../action/action-privacy.md)

* Die Dokumentation **Optimierung des Versandzeitpunkts** wurde aktualisiert und enthält jetzt das neue **[!UICONTROL Senden innerhalb]** nächsten von **2-100 Stunden** (zuvor 1-168) und unterstützte AEP Hub-Regionen für diese Funktion. [Weitere Informationen](../building-journeys/send-time-optimization.md#use-send-time-optimization)

* Die Seiten **Modell für personalisierte Optimierung** wurden aktualisiert, um die neuesten Modellverbesserungen widerzuspiegeln, einschließlich der Funktionsweise des Ensemble-Modells, der Datensatzanforderungen, Anwendungsfälle, wichtiger Annahmen und des Kaltstart-Verhaltens. Weitere Informationen finden Sie in den [Experience Decisioning](../experience-decisioning/ranking/personalized-optimization-model.md) und [Offer Decisioning](../offers/ranking/personalized-optimization-model.md) Abschnitten.

* Auf der Seite **Rangfolgeformeln für Journey-Schlichtungen** wurde ein Hinweis hinzugefügt, der angibt, dass Rangfolgeformeln nur für Organisationen verfügbar sind, die das Add-on-Angebot **Decisioning** erworben haben. [Weitere Informationen](../conflict-prioritization/journey-ranking-formulas.md)

* Eine neue Seite **Dynamische**&quot; ist jetzt verfügbar. Er dokumentiert, wie mithilfe der dynamischen Fragmentauflösung [!DNL Journey Optimizer] ausgewählt werden kann, welches veröffentlichte Fragment zur Laufzeit in eine Nachricht eingefügt wird. Dies erfolgt auf der Grundlage von Profilattributen, Datensatzsuchen oder Kontextdaten, die zum Sendezeitpunkt übergeben werden. [Weitere Informationen](../content-management/dynamic-fragments.md)

## Juni 2026 {#june-2026}

* Die Seite **Überprüfen und Senden einer Briefpostnachricht** wurde aktualisiert, um den Zeitpunkt des Briefpost-Exports und das Batch-Verhalten zu verdeutlichen, einschließlich des festen 4-Stunden-UTC-Exportplans, warum mehrere Dateien an einem Tag generiert werden können, wenn **[!UICONTROL Profil aktualisieren]** in Journey ausgeführt wird, und Empfehlungen für Einzeldateiszenarien pro Tag. [Weitere Informationen](../direct-mail/test-send-direct-mail.md#dm-export-timing)

* Neue **Journey-Typen: Wählen Sie die richtige aus** Die Seite ist jetzt verfügbar. Er vergleicht alle Journey-Einstiegspunkte - „Zielgruppe lesen“, „Zielgruppen-Qualifizierung“, „Unitäres Ereignis“ und „Geschäftsereignis“ - mit Entscheidungshandbüchern und einer Funktionskompatibilitätsmatrix, um Sie bei der Auswahl des richtigen Typs für Ihren Anwendungsfall zu unterstützen. [Weitere Informationen](../building-journeys/journey-types-selection.md)

* Eine neue Seite **Journey vs. Kampagnen** ist jetzt verfügbar. Er vergleicht Journey, Aktionskampagnen und API-ausgelöste Kampagnen im Ausführungsstil, Datenmodell und Anwendungsfall, einschließlich der Aktivierung eingehender Kanäle für Edge-Personalisierung mit niedriger Latenz, eingehenden Versand über mehrere Oberflächen und Anleitungen zur Verwendung orchestrierter Kampagnen (Ad-hoc-Zielgruppenkomposition, Federated Data). [Weitere Informationen](../start/journeys-vs-campaigns.md)

* Die Seite **Hochdurchsatzmodus** wurde aktualisiert, um die erweiterte regionale Verfügbarkeit widerzuspiegeln: Die Funktion ist jetzt in allen Regionen außer der Schweiz für Organisationen verfügbar, die mit dem Add-on „Hochdurchsatz-Transaktionsnachrichten“ lizenziert sind. [Weitere Informationen](../campaigns/api-triggered-high-throughput.md)

* Ein neuer Abschnitt **Interaktionsfähige Profile und Lizenznutzung** wurde zur Seite **Erste Schritte mit Profilen** als zentrale Datenquelle für dieses Konzept hinzugefügt, mit zielgerichteten Verweisen, die über die Abschnitte Audiences, Kampagnen und Entscheidungen hinweg hinzugefügt wurden. [Weitere Informationen](../audience/get-started-profiles.md#engageable-profiles)

* Die Dokumentation zur **Aufspaltung**-Aktivität wurde aktualisiert, um das Feld **[!UICONTROL Segment-Code]** zu dokumentieren, das in den Einstellungen für jede Teilmenge verfügbar ist. Dadurch können Sie jedem Zielgruppensegment zu Tracking- und Berichtszwecken eine eindeutige Kennung zuweisen. [Weitere Informationen](../orchestrated/activities/split.md)

* Die Seite **Zielgruppendimension konfigurieren** wurde aktualisiert, um die beiden Zielgruppendimensionstypen zu dokumentieren, die in orchestrierten Kampagnen verfügbar sind: die integrierte **Zielgruppendimension** (keine Konfiguration erforderlich) und **benutzerdefinierte Zielgruppendimensionen** basierend auf relationalen Schemata. [Weitere Informationen](../orchestrated/target-dimension.md)

* Die **Nutzen von Designs in einem Fragment** wurde präzisiert, um explizit das 5-Design-Kompatibilitätslimit zu dokumentieren (einschließlich der Adobe-Standard-Design-Einschränkung) und zu erklären, dass das Einfügen von Fragmenten blockiert wird, wenn das E-Mail-Design nicht zu den mit Fragmenten verknüpften Designs gehört. [Weitere Informationen](../email/apply-email-themes.md#leverage-themes-fragment)

* Die Seiten **Erste Schritte mit Datensätzen** und **Erste Schritte mit Schemata** wurden mit Anleitungen zur Aktivierung von Datensätzen und Schemata für das Echtzeit-Kundenprofil aktualisiert, einschließlich wichtiger Überlegungen, der Unterscheidung zwischen der Deaktivierung eines Datensatzes und seinem zugrunde liegenden Schema sowie Links zur Dokumentation zu Planung und Best Practices für Adobe Experience Platform. [Weitere Informationen zu Datensätzen](../data/get-started-datasets.md) und [Weitere Informationen zu Schemata](../data/get-started-schemas.md)

* Ein neuer Onboarding **Hub „Erste Schritte mit Adobe Journey Optimizer** ist jetzt verfügbar. Neue Benutzer können ihren Pfad nach Rolle auswählen, Grundlagen erkunden oder zu den täglichen Bereichen springen, wenn sie bereits integriert sind - ohne wissen zu müssen, wo sie zuerst suchen müssen. [Weitere Informationen](../../rp_landing_pages/get-started-landing-page.md)

* Mit einer neuen **Von Ihrem Ziel starten** können Sie von dem ausgehen, was Sie erreichen möchten, und nicht von einem Funktionsnamen. Er ordnet Geschäftsziele den empfohlenen Journey Optimizer-Funktionen für Einrichtung, Journey, Kampagnen, Personalisierung, Entscheidungsfindung und Reporting zu. [Weitere Informationen](../start/ajo-use-case-guide.md)

* Das **Erste Schritte für Entwickler** Rollenhandbuch wurde mit klareren Einführungen für jeden Abschnitt und verbesserten Registerkarten **Zusammenarbeit zwischen Rollen** aktualisiert, die auf Journey verweisen und Links zu wichtigen Implementierungsseiten enthalten. [Weitere Informationen](../start/path/developer.md)

* Ein neuer Unterabschnitt **Pfadzuweisung beim erneuten Eintritt von Journey** wurde zur Dokumentation **Pfadexperiment** hinzugefügt. Dadurch wird klargestellt, dass die Pfadzuweisung für ein Profil über mehrere Eintritte in dieselbe Journey-Version hinweg persistent ist, jedoch nur innerhalb dieser Journey-Version. Zuweisungen werden zurückgesetzt, wenn eine neue Journey-Version veröffentlicht wird und jede Pfadexperimentieraktivität in einer Journey eine unabhängige zufällige Zuweisung anwendet. [Weitere Informationen](../building-journeys/path-experimentation.md#path-assignment)
* Die Verweise auf **Adobe Experience Cloud** wurden in der [!DNL Journey Optimizer]-Dokumentation an die **[!DNL Adobe CX Enterprise]** Marke angepasst.

* Die Dokumentation zur **`nowWithDelta()`Datumsfunktion** aktualisiert, um das Monatsendverhalten zu verdeutlichen: Wenn der Zielmonat weniger Tage als der aktuelle Tag des Monats hat, wird das Ergebnis auf den letzten gültigen Tag dieses Monats normalisiert. [Weitere Informationen](../building-journeys/functions/date-functions.md#nowWithDelta)

* Die Seite **Erste Schritte mit der Zustellbarkeit** wurde mit dem neuen Unterabschnitt **Anbieter ohne FBL pro Empfänger bzw. Empfängerin** aktualisiert. Darin sind die wichtigsten Postfachanbieter aufgeführt, die keine Spam-Beschwerden pro Empfänger bzw. Empfängerin zurückgeben – Gmail/Google Workspace, Apple iCloud und Corporate Microsoft 365/Exchange Online –, und es wird erklärt, warum für Empfängerinnen und Empfänger, die diese Services verwenden, das Fehlen eines Eintrags in der Unterdrückungsliste erwartet wird. [Weitere Informationen](../reports/deliverability.md#providers-no-fbl)

* **Erlebnis-Entscheidung ist jetzt für den Direkt-Mail-Kanal verfügbar.** Auf der neuen Seite **Batch-Entscheidungsfindung in Direkt-Mail** wird beschrieben, wie Sie die Decisioning-Engine verwenden, um Direkt-Mail-Extraktionsdateien zu personalisieren oder Profile und ihre Entscheidungsfindungsergebnisse zur Verwendung in nachgelagerten Systemen zu exportieren. **Direkt-Mail** wurde als unterstützter Kanal zur gesamten Dokumentation zur Entscheidungsfindung hinzugefügt (Erste Schritte, Erstellen einer Entscheidungsrichtlinie, Verwenden von Entscheidungsrichtlinien in Nachrichten, Erste Schritte mit Entscheidungsrichtlinien), einschließlich der Möglichkeit, mehrere Entscheidungselemente pro Profil über das Feld **[!UICONTROL Anzahl der Elemente]** zurückzugeben. [Weitere Informationen](../experience-decisioning/batch-decisioning-direct-mail.md)

* Die Dokumentation zu **Journey-Fragmenten** ist nicht mehr als „Eingeschränkte Verfügbarkeit“ gekennzeichnet. Die Seite enthält jetzt einen Hinweis zum Unterscheiden von Journey-Fragmenten aus **[!UICONTROL Inhaltsfragmenten]** und **AEM-Inhaltsfragmenten** (von allen drei Seiten vernetzt) sowie Dokumente zur Unterstützung von **Sandbox-Tools**, **Auditprotokollen** und **Tagging**. Journey-Fragmente wurden auch zur Seite **Erste Schritte mit Journeys** hinzugefügt. [Weitere Informationen](../building-journeys/journey-fragments.md)

* Die Dokumentation zu **externen Datenquellen** und **benutzerdefinierten Aktionen** wurde im Hinblick auf die benutzerdefinierte Authentifizierung aktualisiert. Im Feld `tokenInResponse` können Sie jetzt angeben, ob das oder das `access_token`&#x200B;`id_token`als Anmeldeinformationen verwendet werden soll, wenn ein Endpunkt beide zurückgibt. Für die zertifikatsbasierte benutzerdefinierte Authentifizierung sind die Felder `subType` und `aud` jetzt obligatorisch, der Token-Endpunkt `method` muss `POST` sein und Verweise auf „Azure Entra ID“ wurden zu „Microsoft Entra ID“ korrigiert. [Weitere Informationen](../datasource/external-data-sources.md#certificate-credential)

* Die Seite **Erste Schritte mit der Entscheidungsfindung** wurde mit einem Prozessdiagramm aktualisiert, das den durchgängigen Entscheidungs-Workflow zusammenfasst, von der Verwaltung von Entscheidungselementen und der Konfiguration von Auswahlstrategien bis zur Einbettung von Entscheidungsrichtlinien in eine Journey oder Kampagne. [Weitere Informationen](../experience-decisioning/gs-experience-decisioning.md#process)

* In der Dokumentation zu **Absender-Headern** wird nun klargestellt, dass die Felder **[!UICONTROL Absendername]** und **[!UICONTROL Absender-E-Mail]** beide festgelegt oder beide leer gelassen werden müssen. Andernfalls können Journeys und Kampagnen nicht veröffentlicht werden. [Weitere Informationen](../email/header-parameters.md#sender-header)

## Mai 2026 {#may-2026}

* Die Einschränkungen und Best Practices bei der Verwendung dynamischer Inhalte in visuellen Fragmenten wurden zu einem einzigen Abschnitt **Verwalten bedingter Inhalte in Fragmenten** zusammengeführt, um die Lesbarkeit zu verbessern. [Weitere Informationen](../email/use-visual-fragments.md#fragment-dynamic-content)

* Zwei neue Berechtigungen auf hoher Ebene wurden hinzugefügt: **Verwalten der Schlüsselregistrierung**, mit der Benutzende Schlüssel in der Schlüsselregistrierung anzeigen, erstellen, drehen und widerrufen können, und **Anzeigen der Schlüsselregistrierung**, mit der Benutzende die Liste der Schlüsselregistrierung und Schlüsseldetails anzeigen können. [Weitere Informationen](../administration/high-low-permissions.md#administration-permissions)

* In der Dokumentation **Verwenden von Entscheidungsrichtlinien in Nachrichten** wird jetzt beschrieben, wie Sie die vollständige Struktur einer Entscheidungsrichtlinie in der Kampagnenübersicht anzeigen und eine technische JSON-Zusammenfassung zur Fehlerbehebung in die Zwischenablage kopieren können. [Weitere Informationen](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

* Die veraltete Seite **Entscheidungs-Management** – [Modelle für die automatische Optimierung](../offers/ranking/auto-optimization-model.md) wurde umgeschrieben, um sie an die aktualisierte Dokumentation zur Entscheidungsfindung anzupassen, einschließlich der Übersicht über vertiefendes Lernen, Anforderungen und Einschränkungen, Abwägung von Optimierung mit Lernen und Details zum Thompson-Stichprobenverfahren. [Weitere Informationen](../offers/ranking/auto-optimization-model.md)

* Die Seite **Versionshinweise** wurde mit einem themenbasierten Layout neu strukturiert. Änderungen werden jetzt nach Produktbereich anstatt nach Änderungstyp gruppiert. Ein neuer Abschnitt zu **Verbesserungen der Benutzerfreundlichkeit** wurde hinzugefügt. Demnächst verfügbare Einträge werden in jedem Thema als erweiterbare Akkordeons angezeigt. [Weitere Informationen](release-notes.md)

* Auf der Seite **Leitlinien und Einschränkungen für orchestrierte Kampagnen** wird nun das Limit für **Kanalaktivitäten** pro orchestrierter Kampagne dokumentiert. [Weitere Informationen](../orchestrated/guardrails.md#activities-limitations)

* Die Dokumentation **Kopieren von Journey Optimizer-Objekten zwischen Sandboxes** enthält jetzt einen wichtigen Hinweis für **orchestrierte Kampagnen**: Duplizieren Sie die Kampagne nach dem Import in der Ziel-Sandbox und verwenden Sie das Duplikat für die Ausführung, um sicherzustellen, dass das Reporting Feedback- und Tracking-Daten korrekt erfasst. [Weitere Informationen](../configuration/copy-objects-to-sandbox.md#copy-to-sandbox)

* Die Seite **Wichtige Terminologie** wurde überarbeitet: Sechs neue Begriffe wurden hinzugefügt, ein neuer Abschnitt **Konflikt- und Prioritätsbegriffe** wurde eingeführt und ein neuer Leitfaden **Wenn Begriffe ähnlich aussehen** für vier häufig verwechselte Begriffspaare wurde hinzugefügt. Adobe Experience Platform-spezifische Begriffe wurden entfernt und durch einen Hinweis ersetzt, der auf das Adobe Experience Platform-Glossar verweist. [Weitere Informationen](../start/terminology.md)

* Die **Deeplinks**-Dokumentation wurde um einen neuen Abschnitt **Erstellen von Deeplinks** erweitert, in dem die beiden für E-Mail verfügbaren Optionen (Benutzeroberfläche von E-Mail-Designer und Code im Personalisierungs-Editor) und die URL-Funktionssyntax für SMS beschrieben werden. Die Seite **SMS-Nachricht erstellen** enthält jetzt einen Deeplink-Schritt im Inhaltserstellungsfluss. [Weitere Informationen](../email/deeplinks.md)

* Die **URL**-Hilfereferenz wurde mit einem speziellen Abschnitt in der Personalisierungsdokumentation aktualisiert. [Weitere Informationen](../personalization/functions/helpers.md#url)

* Die Hilfedokumentation zu **Ausführungsmetadaten** wurde um eine Einschränkung erweitert: Die Funktion wird in eingehenden Kanälen (Web, Code-basiertes Erlebnis, In-App-Nachricht, Inhaltskarten) nicht unterstützt. [Weitere Informationen](../personalization/functions/helpers.md#execution-metadata)

* Eine neue Seite **Personalisierungsrezepte** wurde hinzugefügt, die einsatzbereite Personalisierungsmuster für die häufigsten Anwendungsfälle in Journey Optimizer bereitstellt. Sie behandelt Rezepte für Datum und Uhrzeit (Formatierung des aktuellen Datums, Countdown bis zum Ablauf, Berechnungen für Tage vor dem Ablauf, Anzeige nur für Zeit und Erkennung von Wochenenden vs. Wochentagen), Zeichenfolgenrezepte (Verwendung von `replaceAll` mit Variablenzuweisung) und bedingte Fallback-Rezepte (Fallbacks mit leeren Feldern unter Verwendung von `isEmpty`). [Weitere Informationen](../personalization/personalization-recipes.md)

* Die Dokumentation zur **Personalisierungssyntax** wurde mit einer erweiterten Einführung aktualisiert, die den Unterschied zwischen Handlebars- (`{{...}}`) und PQL-(`{%= ... %}`)-Syntax verdeutlicht, einschließlich einer Verwendungstabelle, einer Anleitung zum Maskieren von doppelten Anführungszeichen für literale Anführungszeichen sowie einem neuen Abschnitt mit **PQL-Syntaxregeln für spezielle Attributschlüssel**, der reservierte Schlüsselwörter, Schlüssel mit Trennzeichen und numerische Ereignis-IDs behandelt. Der Hinweis zum Maskieren von Backtick-Zeichen wurde ebenfalls korrigiert: Getrennte Feldnamen können direkt in `{{...}}`-Blöcken referenziert werden; nur die Backtick-Syntax schlägt dort fehl. [Weitere Informationen](../personalization/personalization-syntax.md)

* Die Dokumentation zu **Datums- und Zeitfunktionen** wurde um neue Beispiele aus der Praxis erweitert: ein Countdown-Muster für `dateDiff`, eine Wochenende-vs.-Wochentag-Bedingung für `dayOfWeek` (mit einem Hinweis zur Verwendung der Journey-Bedingungsaktivität für Routing-Anwendungsfälle) und ein Nur-Zeit-Anzeigemuster, bei dem `extractHours` und `extractMinutes` mit einem Schutzmechanismus mit führenden Nullen kombiniert werden. [Weitere Informationen](../personalization/functions/dates.md)

* Die Dokumentation zu **Zeichenfolgenfunktionen** wurde mit einem neuen Beispiel für `replaceAll` aktualisiert, in dem gezeigt wird, wie das Ergebnis einer `{% let %}`-Variablen zugewiesen werden kann, um es über mehrere Ausdrücke in derselben Vorlage hinweg wiederzuverwenden. [Weitere Informationen](../personalization/functions/string.md#replace-all)

* Die Dokumentation zu **Array-Funktionen** wurde mit einem neuen Abschnitt **Iterieren über ein Array** aktualisiert, in dem der Handlebars-Block-Helper `{{#each}}` dokumentiert wird. Außerdem wird darin klargestellt, dass `{{#each}}` nur im Personalisierungs-Editor unterstützt wird und nicht in Journey-Bedingungsaktivitäten verwendet werden kann. [Weitere Informationen](../personalization/functions/arrays-list.md#each-loop)

* Die Seite **Erste Schritte mit Datensätzen** wurde mit einem neuen Eintrag **Eingehend** im Abschnitt zu Systemdatensätzen aktualisiert, der den _Datensatz „Eingehendes AJO-Aktivitätsereignis“_ dokumentiert. Ein Hinweis wurde hinzugefügt, der klarstellt, dass bei einem Profil mindestens eine Nachricht von [!DNL Journey Optimizer] gesendet werden muss, bevor eingehende Nachrichten in diesem Datensatz erfasst werden. [Weitere Informationen](../data/get-started-datasets.md#system-datasets)

* Die Dokumentation zum **Exportieren von Nachrichteninhalten** wurde um **Häufig gestellte Fragen zum Nachrichtenexport** (personalisierte Inhalte, Bilder und Medien, getrackte Links, personenbezogene Daten, Kundenbindung, Anwendungsfälle usw.) und **Beispiele für exportiertes JSON** für SMS und E-Mail erweitert. [Weitere Informationen](../configuration/message-export.md)

* Eine neue Seite **AJO-Nachrichtenexport-Schema** dokumentiert jedes Feld im AJO-Nachrichtenexport-Datensatz mit Datentypen und einer Hierarchie für die exportierte E-Mail- und SMS-Payload. [Weitere Informationen](../configuration/message-export-schema.md)

* Eine neue Seite **Personalisieren von URLs in E-Mails** wurde hinzugefügt, die Anleitungen zur dynamischen URL-Personalisierung, zur vollständigen/einfachen URL-Personalisierung, zur Personalisierung von URL-Tracking-Parametern und zu wichtigen Leitlinien enthält. [Weitere Informationen](../email/url-personalization.md)

* Der neue Abschnitt **Geschäftsregelabfragen** wurde zur Seite mit den Abfragebeispielen hinzugefügt und bietet eine Data-Lake-Abfrage, um alle Profilverwerfungsaktionen aufgrund von Journey-Frequenzbegrenzungs-Ausschlüssen in einer bestimmten Journey nach einem bestimmten Datum zu überprüfen. Die Abfrage enthält das Feld `eventCodeReason`, um anzugeben, ob Profile aufgrund einer erreichten Begrenzung (`CAP_REACHED`) oder aufgrund einer niedrigeren Priorität (`LOWER_PRIORITY`) ausgeschlossen wurden. [Weitere Informationen](../reports/query-examples.md#business-rules-queries)

* Die Dokumentation zu **Journey-Eigenschaften** wurde aktualisiert, um den neuen Indikator **Aktuelle Größe der Journey-Payload** im Panel „Journey-Eigenschaften“ zu dokumentieren. Dieses schreibgeschützte Feld zeigt die aktuelle Größe der Journey-Payload im Vergleich zum konfigurierten Limit an (z. B. 1,5 MB von 2 MB), sodass Sie die Komplexität von Journeys vor der Veröffentlichung überwachen und größenbedingte Veröffentlichungsfehler vermeiden können. [Weitere Informationen](../building-journeys/journey-properties.md#journey-payload-size)

## April 2026 {#april-2026}

* Die Dokumentation zur Aktivität **Dimensionsänderung** wurde aktualisiert, um klarzustellen, dass Einträge ohne übereinstimmendes Profil in der neuen Targeting-Dimension zum Zeitpunkt des Nachrichtenversands im Hintergrund verworfen werden, auch wenn die Aktivität einen externen Join verwendet und alle Einträge im Dimensionsänderungsschritt speichert. [Weitere Informationen](../orchestrated/activities/change-dimension.md)

* Die Leitlinien in der Dokumentation **Hinzufügen eines CC-Felds zu E-Mails** wurden erweitert. Sie verdeutlichen jetzt, dass die CC-Adresse nicht mit dem Einverständnis oder der Unterdrückung abgeglichen wird und dass Öffnungen und Klicks aus E-Mails an die CC-Adresse in der Versandanalyse in der Gesamtzahl der Öffnungen und Klicks berücksichtigt werden. [Weitere Informationen](../configuration/cc-email-field.md)

* Die Dokumentation zu **Kanalaktivitäten** wurde mit einem neuen Abschnitt **Marketing- vs. Transaktionsnachrichten** aktualisiert, in dem die Verhaltensunterschiede zwischen den beiden Kanalkategorien erläutert werden: Opt-in-Anforderungen, Geschäftsregelanwendung, Kanalkonfigurationstyp und empfohlene Anwendungsfälle. [Weitere Informationen](../orchestrated/activities/channels.md#marketing-vs-transactional)

* Die Dokumentation zur Aktivität **Verzweigung** wurde um einen neuen Abschnitt **Beispiele** erweitert, in dem veranschaulicht wird, wie mit der Aktivität „Verzweigung“ eine Zielgruppe in einer einzigen Kampagnenausführung auf zwei parallele E-Mail-Verzweigungen aufgeteilt wird: eine Marketing- und eine Transaktionsverzweigung. [Weitere Informationen](../orchestrated/activities/fork.md#fork-examples)

* Die Dokumentation zur Aktivität **Zielgruppe erstellen** wurde um ein neues Beispiel erweitert, das zeigt, wie Profile mithilfe des Regel-Builders nach einem Abonnementplanattribut gefiltert werden können. [Weitere Informationen](../orchestrated/activities/build-audience.md#build-audience-examples)

* Die Seite **Erste Schritte mit orchestrierten Kampagnen** dokumentiert das Einstiegsmuster **Zielgruppe erstellen → Verzweigung → Kanal A + Kanal B** in **Was befindet sich in einer orchestrierten Kampagne?** mit Querverweisen auf die Seiten zur Aktivität „Verzweigung“ und zu den Unterschieden zwischen Marketing- und Transaktionsnachrichten. [Weitere Informationen](../orchestrated/gs-orchestrated-campaigns.md#gs-ms-campaign-inside)

* Die Seite **Bearbeiten von E-Mail-Inhalten mit dem erweiterten HTML-Editor** wurde aus dem Abschnitt „Content-Management“ in den Abschnitt **E-Mail** der Dokumentation verschoben. Auf der Seite wird nun dokumentiert, dass der erweiterte HTML-Editor im E-Mail-Designer für E-Mail-Nachrichten und für E-Mail-Inhaltsvorlagen verfügbar ist. [Weitere Informationen](../email/email-expert-mode.md)

* Die Dokumentation **Starten und Überwachen orchestrierter Kampagnen** wurde mit einem neuen Abschnitt aktualisiert, der die interne Ausführungssequenz zur Veröffentlichungszeit sowie eine Tabelle mit dem Kampagnenlebenszyklusstatus, eine Checkliste zur Vorbereitung der Veröffentlichung und den Versand einer Bestätigungswarnung für nicht wiederkehrende Kampagnen enthält. [Weitere Informationen](../orchestrated/start-monitor-campaigns.md#publication-sequence)

* Die Dokumentation zur Aktivität **Zielgruppe speichern** wurde mit einem Hinweis aktualisiert, der klarstellt, dass Aktivitäten des Typs „Zielgruppe speichern“ zum Zeitpunkt der Veröffentlichung immer vor Nachrichtenaktivitäten ausgeführt werden. [Weitere Informationen](../orchestrated/activities/save-audience.md)

* Den **Häufig gestellten Fragen zu orchestrierten Kampagnen** wurden drei neue Themen hinzugefügt: Was intern zur Veröffentlichungszeit passiert, eine 7-Punkte-Checkliste mit Gründen, warum Nachrichten nach der Veröffentlichung möglicherweise nicht gesendet werden, und wie sich die Suche nach Profil-Snapshots von der Echtzeit-Profilauflösung unterscheidet. [Weitere Informationen](../orchestrated/orchestrated-campaigns-faq.md)

* Ein neuer Abschnitt **[Aufgrund von blockierter Journey-Instanz verworfene Ereignisse](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached)** wurde der Dokumentation zur Fehlerbehebung bei Journeys hinzugefügt, in dem der `maxInstanceStackEventsReached`-Grund für das Verwerfen, der Zeitpunkt sowie die Maßnahmen zur Behebung des Problems erläutert werden. Die Seiten mit Leitlinien und Schrittereignisfeldlisten wurden ebenfalls entsprechend aktualisiert.

* Die Dokumentation **Nutzen von Fragmenten in Entscheidungsrichtlinien** enthält jetzt Leitlinien für den **E-Mail**-Kanal: **[!UICONTROL Inhalte simulieren]** zeigt keine Ausdrucksfragmente aus dem Entscheidungselement an, während **[!UICONTROL Testversand durchführen]** und aktivierte Kampagnen dies tun. Auf der Seite wird auch angegeben, dass **[!UICONTROL visuelle Fragmente]** keinem Entscheidungselement zugewiesen werden können. Nur **Ausdrucksfragmente** werden in diesem Kontext unterstützt. [Weitere Informationen](../experience-decisioning/fragments-decision-policies.md)

## März 2026 {#march-2026}

* Die Dokumentation **Vorschau von Code-basierten Erlebnissen mit Erlebnis-Entscheidung** stellt jetzt klar, dass es sich bei **[!UICONTROL Inhalte simulieren]** nur um eine Vorschau von Inhalten handelt. Kontextdaten aus Live-Edge-Anfragen werden in der Authoring-Vorschau nicht simuliert. [Weitere Informationen](../code-based/test-code-based.md#preview-code-based)

* Die Dokumentation **Verwenden von Adobe Experience Platform-Daten** wurde aktualisiert: Die Leitlinien geben nicht mehr an, dass Datensatzsuchen nicht verkettet werden können. Dies spiegelt das aktuelle Produktverhalten wider. [Weitere Informationen](../data/lookup-aep-data.md)

* Die Dokumentation zur Aktivität **Profil aktualisieren** wurde aktualisiert, um die Unterstützung für die Aktualisierung von bis zu fünf Profilattributen in einer einzigen Aktion zu dokumentieren. [Weitere Informationen](../building-journeys/update-profiles.md)

* Die Aktivität **Zielgruppe lesen** und die Dokumentation **Journey-Eigenschaften** wurden aktualisiert, um den 91-tägigen Journey-Lebenszyklus für immer aktive, wiederkehrende Journey zu genauer zu erklären. Der Zeitplanabschnitt bestätigt jetzt explizit, dass wiederkehrende Journeys ohne Enddatum länger als 91 Tagen aktiv bleiben. Die häufig gestellten Fragen zum globalen Timeout wurden erweitert, um die 91-tägige Profil-TTL vom 91-tägigen Reporting-Fenster zu unterscheiden. [Weitere Informationen](../building-journeys/read-audience.md#schedule)

* Die Dokumentation zur Aktivität **Datensatzsuche** wurde aktualisiert, um klarzustellen, dass der Lookup-Schlüssel im erweiterten Modus konfiguriert werden muss, damit die `@datasetLookup{}`-Syntax in nachgelagerten Bedingungsaktivitäten funktioniert. Es wurde ein Abschnitt zur Fehlerbehebung mit Anleitungen zur Behebung des Fehlers „Datensatzsuche nicht gefunden“ hinzugefügt. [Weitere Informationen](../building-journeys/dataset-lookup.md#troubleshooting)

* Die Dokumentation zu **Datums-/Uhrzeitfunktionen** wurde mit einem neuen Beispiel aktualisiert, das zeigt, wie ein Zeitstempel aus einem Kontextereignisattribut formatiert werden soll, einschließlich der `toDateTime()`-Anforderung, der Backtick-Syntax für numerische Ereignis-IDs und einem allgemeinen Fehlerhinweis für den PQL-Fehler „Nicht übereinstimmende Eingabe“. [Weitere Informationen](../personalization/functions/dates.md#format-date)

* Die Dokumentationen **Leitlinien und Einschränkungen für orchestrierte Kampagnen** und **Erste Schritte mit Quell-Connectoren** wurden aktualisiert, um klarzustellen, dass für die dateibasierte Änderungsdatenerfassung das Feld `_change_request_type` erforderlich ist und seine Werte `u` (upsert) oder `d` (delete) klein- und nicht großgeschrieben werden müssen. [Weitere Informationen](../orchestrated/guardrails.md)

* Die Dokumentation **Hinzufügen von Links und Verfolgen von Nachrichten** wurde mit Anleitungen aktualisiert, wie Tracking-Kennungen (urlID) generiert werden: Eine eindeutige urlID wird nur zugewiesen, wenn sowohl die URL als auch das Label eindeutig sind. Um dieselbe URL über mehrere E-Mails hinweg (oder mehrmals in einer E-Mail) zu verfolgen, müssen Benutzende für jede ähnliche URL ein eindeutiges Label verwenden. Andernfalls kann [!DNL Journey Optimizer] nicht ermitteln, auf welchen Link geklickt wurde. [Weitere Informationen](../email/message-tracking.md#track-across-multiple-emails)

* Die Dokumentation **Erstellen von Testprofilen** wurde mit einem wichtigen Hinweis zu den Identitätsdeskriptoranforderungen aktualisiert: wenn ein Datensatz gelöscht und neu erstellt wird, muss das Schema den richtigen Identitätsdeskriptor für das primäre Identitätsfeld beibehalten. Ohne ihn werden aufgenommene Profile nicht als `testProfile = true` gekennzeichnet, selbst wenn die Aufnahme erfolgreich abgeschlossen wurde. Eine Checkliste zur Fehlerbehebung wurde hinzugefügt. [Weitere Informationen](../audience/creating-test-profiles.md)

* Die Dokumentation zur Aktivität **Zielgruppe lesen** wurde aktualisiert, um klarzustellen, dass eine Aktivität des Typs **Geschäftsereignis** eine Ausnahme von der Regel darstellt, dass „Zielgruppe lesen“ die erste Aktivität einer Journey sein muss. Es wurde auch ein Hinweis zur Aktivität **Optimieren** als erweiterte Alternative zur Steuerung des Zielgruppen-Targetings hinzugefügt. [Weitere Informationen](../building-journeys/read-audience.md)

* **Senden in Schüben** in Journey ist jetzt allgemein verfügbar. Die Markierung „Eingeschränkte Verfügbarkeit“ wurde aus der Dokumentation entfernt. [Weitere Informationen](../building-journeys/send-using-waves.md)

* Die Dokumentation zur Aktivität **Sprung** wurde um einen neuen Abschnitt zur Entwurfsstrategie erweitert (**Kleinere Teil-Journeys**), in dem erläutert wird, wie komplexe End-to-End-Flüsse in kleinere, fokussierte Teil-Journeys unterteilt werden, die über die Aktivität „Sprung“ verbunden sind. [Weitere Informationen](../building-journeys/jump.md#jump-strategy)

* Die Dokumentation zu **Tags** wurde mit Anleitungen zur Verwendung von Tag-Kategorien als Alternative zu komplexen Namenskonventionen aktualisiert. In einem neuen Abschnitt wird erläutert, wie Tag-Kategorien für skalierbares Journey-Management eingerichtet werden. [Weitere Informationen](../building-journeys/tags.md)

* Die Dokumentation **Über Datenquellen** enthält jetzt einen neuen Abschnitt, der den Benutzenden bei der Auswahl zwischen drei Datenzugriffsstrategien hilft: Zugreifen auf externe Daten über benutzerdefinierte Aktionen, Verwenden eines Datensatzes, der nicht für Profile aktiviert ist, oder Verwenden eines profilaktivierten Datensatzes. Jede Option wird mit Kompromissen und empfohlenen Anwendungsfällen beschrieben. [Weitere Informationen](../datasource/about-data-sources.md#data-access-strategy)

* Die Dokumentation **Push-Benachrichtigungs-Design** wurde mit einem Hinweis aktualisiert, der das Verhalten universeller Links in iOS erläutert: wenn die Benachrichtigungs-URL als universeller Link registriert ist, wird die zugehörige App unabhängig von der ausgewählten Web-URL-Aktion geöffnet. Es wurden Anleitungen hinzugefügt, wie das Öffnen eines Browsers erzwungen werden kann. [Weitere Informationen](../push/design-push.md)

* Eine neue Seite **Überwachen Ihrer KI-Modelle** ist jetzt in der Dokumentation zur Entscheidungsfindung verfügbar. Es wird erläutert, wie Sie Gesamtstatus, Trainings-Status und Leistung personalisierter Optimierungsmodelle direkt in [!DNL Journey Optimizer] verfolgen können. [Weitere Informationen](../experience-decisioning/ranking/ai-model-observability.md)

* Der **erweiterte HTML-Editor** (Expertenmodus) für E-Mail-Vorlagen ist jetzt eingeschränkt verfügbar. Die Dokumentationsseite ist jetzt öffentlich zugänglich. Mit dieser Funktion können Sie die HTML-Rohquelle von E-Mail-Inhaltsvorlagen direkt über den E-Mail-Designer anzeigen und bearbeiten. [Weitere Informationen](../email/email-expert-mode.md)

* Die Dokumentationen zu **URL-Tracking** und **Journey-Fehlerbehebung** wurden aktualisiert, um das Verhalten von `context.system.source.actionId` in geschlossenen Journeys zu dokumentieren. Geschlossene oder nicht erneut veröffentlichte Journeys können leere `{}`-Platzhalter in Tracking-URLs erzeugen. Es wurden Anleitungen hinzugefügt, wie Sie das Problem beheben können, indem Sie die Journey erneut veröffentlichen oder den betroffenen Parameter entfernen. [Weitere Informationen](../email/url-tracking.md)

* Die Dokumentation **Adobe Experience Platform-Datenquelle** wurde mit dem Hinweis aktualisiert, dass in der Datenquellenkonfiguration nur Schemata des Typs „XDM-Profil für Einzelpersonen“ unterstützt werden. [Weitere Informationen](../datasource/adobe-experience-platform-data-source.md)

* Die Dokumentation **Leitlinien für die Time-to-Live (TTL) von Datensätzen** wurde um einen neuen Eintrag in den häufig gestellten Fragen erweitert, indem eindeutig erläutert wird, welche Datensätze der TTL unterliegen. TTL gilt ausschließlich für Zeitreihendatensätze. Datensätze des Typs „Eintrag“ wie Entitätsdatensätze, Klassifizierungsdatensätze und Entscheidungsobjekt-Repositorys unterliegen nicht der TTL und sind von dem Rollout der Leitlinien nicht betroffen. [Weitere Informationen](../data/datasets-ttl.md)

* Die Dokumentationen **Journey-Eigenschaften** und **Pausieren einer Journey** wurden aktualisiert, sodass sie die neuen Felder zum Pausieren und Wiederaufnehmen dokumentieren, die jetzt in den technischen Details zum Journey verfügbar sind. Die Schaltfläche **Technische Details kopieren** enthält jetzt zusätzlich zum vorhandenen `pausedJourneySettings`-Block `lastPausedAt`, `lastPausedBy`, `lastPausedById`, `lastResumedAt`, `lastResumedBy` und `lastResumedById`. Es wurde auch ein neuer Abschnitt zur Seite **Pausieren einer Journey** hinzugefügt, in dem erläutert wird, wie Zeitstempel für Pausen und Wiederaufnahmen direkt aus den Journey-Eigenschaften angezeigt werden können. [Weitere Informationen](../building-journeys/journey-properties.md)

## Februar 2026 {#february-2026}

* Eine neue Seite ist jetzt für das Entscheidungs-Management verfügbar. Es werden alle Operatoren, Helper und Funktionen aufgelistet, die bei der Personalisierung von Angebotsinhalten (Darstellungen) mit dem Personalisierungseditor unterstützt werden. Verwenden Sie diese Liste, um Laufzeitfehler zu vermeiden. Bei der Personalisierung von Inhalten in Offer Decisioning werden nur die dokumentierten Funktionen unterstützt. [Weitere Informationen](../offers/offer-library/personalization-editor-supported-functions.md)

* Die Dokumentationen **Erstellen von Entscheidungsrichtlinien** und **Verwenden von Entscheidungsrichtlinien in Nachrichten** wurden für E-Mails aktualisiert:in einem Hinweis wird jetzt erklärt, dass die Engine Angebote dedupliziert (jede Platzierung erhält ein anderes Angebot), wenn dasselbe Angebot von mehr als einer Entscheidungsrichtlinie im E-Mail-Textkörper ausgewählt werden kann. Um dasselbe Angebot in mehreren Platzierungen anzuzeigen (z. B. Kopf- und Fußzeile), verwenden Sie **Entscheidungsausgabe wiederverwenden**. [Weitere Informationen](../experience-decisioning/create-decision-policy.md)

* Die Seite „Entscheidungselemente“ wurde mit Informationen zum Push-Kanal und zur Begrenzung benutzerdefinierter Ereignisse aktualisiert. [Weitere Informationen](../experience-decisioning/items.md#capping)

* Die Dokumentation **Suche nach Erlebnisereignissen in Journeys** wurde mit der Einstellungszeitleiste aktualisiert: ab dem 1. April 2026 haben Organisationen, die in den letzten 90 Tagen keine Erlebnisereignisattribute in Journey-Ausdrücken verwendet haben, keinen Zugriff mehr auf diese Funktion. Die häufig gestellten Fragen konzentrieren sich jetzt auf die Einstellungs-Timeline und darauf, wer betroffen ist. Die Seite mit dem Erlebnisereignisschema wurde mit einem direkten Link zu alternativen Ansätzen abgestimmt. [Weitere Informationen](../building-journeys/exp-event-lookup.md)

* Die Dokumentation zur **Entscheidungsfindung** wurde für die **Datensatzsuche** mit Adobe Experience Platform-Daten aktualisiert: Die Leitlinie für unterstützte Kanäle gibt jetzt an, dass die Datensatzsuche für alle Kanäle funktioniert, für die die Entschiedungsfindung verfügbar ist (Code-basiertes Erlebnis, E-Mail, Push, SMS und die Aktivität „Inhaltsentscheidung“ in Journeys). Hinweise zur eingeschränkten Verfügbarkeit und öffentlichen Beta-Version wurden aus den Seiten mit Entscheidungsregeln, Rangfolgeformeln und Entscheidungselementen entfernt. [Weitere Informationen](../experience-decisioning/aep-data-exd.md)

* Die Seite zur Integration externer Systeme wurde mit Links zu benutzerdefinierten Datenquellen und benutzerdefinierten Aktionen aktualisiert und stellt klar, dass der Ausgangs-Proxy eine statische IP für ausgehende Aufrufe von **benutzerdefinierten Aktionen** an Ihre externen Systeme bereitstellt. [Weitere Informationen](../configuration/external-systems.md)

* Die Dokumentation zum Journey-Probelauf wurde erweitert: die Schrittereignisattribute `inDryRun` und `dryRunID` dokumentieren jetzt, dass sie die `true`-/Instanz-ID im Probelauf-Modus und `null` für Test- oder Live-Journeys zurückgeben. Die Anleitung zum Ausschluss von Probelaufschrittereignissen in Reporting-Abfragen wurde entsprechend aktualisiert. [Weitere Informationen](../building-journeys/journey-dry-run.md)

* **Web-Push** ist jetzt allgemein verfügbar. Die Dokumentation zu Push-Benachrichtigungen wurde entsprechend umstrukturiert und aktualisiert (Erste Schritte, Gestalten, Senden, Erstellen). [Weitere Informationen](../push/get-started-push.md)

* Die Seite zur Web-Push-Konfiguration ist jetzt in der Dokumentation verfügbar. [Weitere Informationen](../push/push-configuration-web.md)

* Die Dokumentation zur Verwendung von Fragmenten in der Entscheidungsfindung wurde aktualisiert: in den Abschnitten „Fragmente“ und „Entscheidungen“ wurden Notizen hinzugefügt und die Seite „Fragmente in Entscheidungsrichtlinien“ wurde aktualisiert. [Weitere Informationen](../experience-decisioning/fragments-decision-policies.md)

* Die SMS-Webhook-Dokumentation wurde aktualisiert: Twilio-Webhook-Inhalte wurden entfernt. [Weitere Informationen](../mobile/mobile-webhook.md)

* Die Dokumentation **Konvertieren von Bildern in Inhaltsvorlagen** wurde um umfassendere Leitlinien und Empfehlungen, gängige Anwendungsfälle und klarere Anleitungen zum Konvertieren von Bild-Designs in bearbeitbare HTML-Inhaltsvorlagen erweitert. Außerdem wird erwähnt, dass Sie jetzt ein Design als Eingabe für die Konvertierung verwenden können. [Weitere Informationen](../content-management/image-to-html.md)

* Die Dokumentation zur Entscheidungsfindungsmigrations-API wurde aktualisiert. [Weitere Informationen](../experience-decisioning/decisioning-migration-api.md)

* Die Aktivität **Inhaltsentscheidung** ist jetzt allgemein verfügbar. Die Seite zur Aktivität „Inhaltsentscheidung“ wurde mit einem Abschnitt zu Entscheidungsfindungsdaten aktualisiert, die in Schrittereignissen verfügbar sind. [Weitere Informationen](../building-journeys/content-decision.md)

* Links zur Dokumentation zur Treue-Challenge-API wurden zum Abschnitt „Treue-Challenges“ hinzugefügt (Erste Schritte, Erstellen von Challenges, Erstellen von Aufgaben, Zugreifen auf Treue-Challenges). [Weitere Informationen](../loyalty-challenges/get-started.md)

* Die Informationen zu den unterstützten Kanälen in der Dokumentation zum Assistenten zur Kampagnenerstellung wurden korrigiert. Die Seiten „Erste Schritte mit Kanälen“ und „Häufig gestellte Fragen zu orchestrierten Kampagnen“ wurden entsprechend aktualisiert. [Weitere Informationen](../campaigns/get-started-with-campaigns.md)

* Die Dokumentation zu Berechtigungen wurde in Bezug auf Berechtigungen vom Typ **Journey verwalten** und **Genehmigen** korrigiert. [Weitere Informationen](../administration/ootb-permissions.md)

* Die Dokumentation zu AEM-Integrationen (Adobe Experience Manager) wurde mit überarbeiteter Benennung aktualisiert (dynamische AEM-Inhalte und AEM-Fragmente). [Weitere Informationen](../integrations/aem-fragments.md)

* Der Ausschlussliste wurde ein neuer Ausschlussgrund hinzugefügt: **UnsubscribeLinkNotValid** (Fehler-Code 050081). Dieser Ausschluss wird generiert, wenn die Betrefflänge von „List-Unsubscribe mailTo“ das RFC-Limit von 998 Zeichen überschreitet. [Weitere Informationen](../reports/exclusion-list.md)

* Die Dokumentation zur Helper-Funktion formatDate wurde um den Hinweis erweitert, dass die Funktion einen Datums-/Uhrzeitfeldtyp (keine Zeichenfolge) erfordert, und es wurden mehrere Beispiele hinzugefügt: Formatieren eines Datums-/Uhrzeitfelds, Konvertieren einer Zeichenfolge zuerst in ein Datum, vollständiges Datum mit Name des Tages, dynamisches Datum aus Systemzeit und Wochentagsformat einschließlich Ausgabe in Kleinschreibung. [Weitere Informationen](../personalization/functions/dates.md#format-date)

* Die Dokumentation zur Textversion-E-Mail wurde um umfassende Anleitungen zu Anwendungsfällen erweitert, einschließlich Entscheidungskriterien für die Verwendung von benutzerdefiniertem Klartext im Vergleich zur automatischen Synchronisierung, praktische Beispiele mit realen Szenarien und einen Abschnitt mit häufig gestellten Fragen. [Weitere Informationen](../email/text-version-email.md#when-to-use)

* Die Dokumentation zu E-Mail-Designer-Designs wurde mit Informationen zu den Einschränkungen der Unterstützung von Web-Schriften und zur Bedeutung von Fallback-Schriften aktualisiert. [Weitere Informationen](../email/apply-email-themes.md#themes-guardrails)

* Es wurde eine Einschränkung zur Dokumentation zum Helper für Ausführungsmetadaten hinzugefügt, um klarzustellen, dass Metadaten nicht für Profile erfasst werden, die von der Aktion ausgeschlossen sind. [Weitere Informationen](../personalization/functions/helpers.md#execution-metadata)

* Die Dokumentation mit Beispielen für Code-basierte Implementierung wurde aktualisiert und enthält jetzt das Token-Feld in propositionAction, um ein genaues Tracking und die Attribution in der Entscheidungsfindung zu ermöglichen. [Weitere Informationen](../code-based/code-based-implementation-samples.md#client-side-how)

* Es wurde ein Hinweis zur Dokumentation zu URL-Tracking und Abmelde-Liste hinzugefügt, um klarzustellen, dass die Reihenfolge der an URLs angehängten URL-Tracking-Parameter zufällig ist und nicht gesteuert werden kann. [Weitere Informationen](../email/url-tracking.md)

## Januar 2026 {#january-2026}

* Die Dokumentation zum Lizenznutzungs-Dashboard wurde mit aktualisierten Anleitungen zu **kontaktierbaren Profilen** ergänzt, einschließlich Definitionsdetails und Anleitungen zur Fehlerbehebung. [Weitere Informationen](../audience/license-usage.md#what-is-engageable-profile)

* Es wurde ein Hinweis zur Dokumentation zu E-Mail-Designer-Designs hinzugefügt, um die Einschränkungen der Unterstützung von Web-Schriften näher zu erläutern. [Weitere Informationen](../email/apply-email-themes.md#themes-guardrails)

* Ein neuer Abschnitt mit Leitlinien wurde hinzugefügt, um die Validierung der Journey-Payload-Größe zu dokumentieren, einschließlich Warn- und Fehlerschwellen und Anleitungen zur Optimierung von Journeys. [Weitere Informationen](../start/guardrails.md#journey-payload-size)

* Die Dokumentation zu Leitlinien für die Entscheidungsfindung wurde aktualisiert und enthält jetzt Größenbeschränkungen für Entscheidungselemente (1 KB für Elemente, einschließlich Attributen, maximal 30 Attribute). [Weitere Informationen](../experience-decisioning/decisioning-guardrails.md)

* Der Dokumentation zur Erstellung von Entscheidungsrichtlinien wurde ein Hinweis hinzugefügt, um Benutzende darüber zu informieren, dass es nach der Erstellung einer Entscheidungsrichtlinie bis zu 15 Minuten dauern kann, bis die Änderungen in alle Datenregionen propagiert werden (bis zu 30 Minuten für Kanada). [Weitere Informationen](../experience-decisioning/create-decision-policy.md#review)

* Der Fragmentdokumentation wurde ein Hinweis hinzugefügt, der darüber informiert, dass der Tracking-Datensatz den URL-Wert anstelle des Label-Werts protokolliert, wenn sowohl das Schaltflächen-Label als auch die URL in einem Fragment bearbeitbar gemacht werden. [Weitere Informationen](../content-management/customizable-fragments.md#visual)

* Eine neue Seite ist verfügbar, die die Vorteile der Migration vom Entscheidungs-Management zur Entscheidungsfindung beschreibt, einschließlich Informationen über bevorstehende Migrations-Tool-APIs. [Weitere Informationen](../experience-decisioning/migrate-to-decisioning.md)

* Eine Leitlinie wurde hinzugefügt, die klarstellt, dass Lookup-Datensätze für die eingehende Edge-basierte Aktivierung nur in der Region verfügbar sind, in der sich die Sandbox des Datensatzes befindet. [Weitere Informationen](../data/lookup-aep-data.md#guidelines)

* Der Dokumentation zur Konfiguration des Kanals für orchestrierte Kampagnen wurde ein neuer Abschnitt hinzugefügt, in dem erläutert wird, wie kontextuelle Attribute (wie Kampagnen-ID, Name und Aktionsdetails) in URL-Tracking-Parametern für Analyse- und Berichtszwecke verwendet werden. [Weitere Informationen](../orchestrated/channel-config.md#url-tracking)

* Die Dokumentation zur Inhaltsoptimierung wurde für mehr Klarheit umstrukturiert. Die Hauptoptimierungsseite wurde in vier fokussierte Unterseiten unterteilt: eine Erste-Schritte-Seite, eine spezielle Seite für das Targeting, eine für Experimente und eine weitere für die Kombination beider Ansätze. [Weitere Informationen](../content-management/gs-message-optimization.md)

* Die Hinweise zur eingeschränkten Verfügbarkeit wurden aus drei Journey-Warnhinweisen entfernt („Journey veröffentlicht“, „Journey abgeschlossen“ und „Begrenzung für benutzerdefinierte Aktionen ausgelöst“), da diese Funktionen jetzt allgemein verfügbar sind. [Weitere Informationen](../reports/alerts.md)

* Die Landingpage zum Testen, Validieren und Genehmigen wurde um neue Abschnitte erweitert, die einen Überblick über Testfunktionen, häufig gestellte Fragen, einen Entscheidungsbaum mit Navigations-Links und verbesserte Terminologie mit Links zur Dokumentation enthalten. [Weitere Informationen](../../rp_landing_pages/test-landing-page.md)

* Der Dokumentation zur Personalisierungssyntax wurde ein neuer Abschnitt hinzugefügt, um zu verdeutlichen, wie reservierte Keywords in Personalisierungsausdrücken verwendet werden. Bestimmte PQL-Keywords wie `next`, `last` und `this` müssen durch Umschließen mit Backticks maskiert werden, sofern sie als Feldnamen in Ihrem XDM-Schema verwendet werden. [Weitere Informationen](../personalization/personalization-syntax.md#reserved-keywords)

* Die Seiten [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md) und [Verwalten von Kampagnen](../campaigns/manage-campaigns.md) wurden mit einer verbesserten Informationsarchitektur strukturell überarbeitet, einschließlich eines umfassenden Workflows mit typspezifischen Handbüchern, erweiterter Kampagnentypvergleiche und konsolidierter Statustabellen.

* Die Landingpage für Journeys wurde neu gestaltet, um das Onboarding durch einen neuen 6-Schritte-Workflow, verbesserte Vergleiche von Journey-Typen und verbesserte Navigation in der gesamten Dokumentation zu erleichtern. [Weitere Informationen](../building-journeys/journey.md)

* Es wurde ein detaillierter Abschnitt hinzugefügt, um Benutzenden bei der Generierung von Base64-codierten OpenSSH-Privatschlüsseln für die SFTP-Authentifizierung zu helfen, wenn sie das Datei-Routing für Direkt-Mail konfigurieren, um Verbindungsfehler zu vermeiden. [Weitere Informationen](../direct-mail/direct-mail-configuration.md#ssh-key-generation)

* Der Dokumentation zur Delegierung von Subdomains wurde ein Hinweis hinzugefügt, der Benutzende darüber informiert, dass eine DNS-Propagierung von 24 bis 48 Stunden eingeplant werden muss, bevor die Delegierung an Adobe erfolgt. [Weitere Informationen](../configuration/delegate-subdomain.md#set-up-subdomain)

## Dezember 2025 {#december-2025}

* Die Dokumentation zu benutzerdefinierten Upload-Zielgruppen für die Entscheidungsfindung wurde aktualisiert und enthält nun ein erforderliches API-Flag zum Abrufen von Anreicherungsdaten. Wenn Sie per CSV hochgeladene Zielgruppen in der Angebotsentscheidung verwenden, müssen Sie `"xdm:enrichedAudience": true` in Ihre API-Anfrage-Payload aufnehmen, um Anreicherungsattribute in der Antwort zur Angebotsentscheidung abzurufen. [Weitere Informationen](../offers/custom-upload-decisioning.md#must-read)

* Der Dokumentation zum Testversand wurde ein Hinweis hinzugefügt, um zu verdeutlichen, dass die Regeln zur Frequenzbegrenzung für Testsendungen gelten. Die Seite enthält jetzt einen Abschnitt „Wichtige Informationen“ mit wichtigen Überlegungen zum Verhalten der Frequenzbegrenzung, zu Einschränkungen bei Mirror-Seiten sowie zu Regeln für die Barrierefreiheit von Assets. [Weitere Informationen](../content-management/proofs.md)

* Die Seite „Erste Schritte mit Kanälen“ wurde um eine neue Tabelle zur Verfügbarkeit von Kommunikationskanälen ergänzt, die anzeigt, welche Kanäle in Journeys und Kampagnen unterstützt werden (Aktionskampagnen, durch API ausgelöste Kampagnen und orchestrierte Kampagnen). [Weitere Informationen](../channels/gs-channels.md#channels)

* Eine neue umfassende Tracking-Landingpage wurde erstellt, um Benutzenden zu helfen, alle in Journey Optimizer verfügbaren Tracking- und Monitoring-Funktionen zu entdecken und darauf zuzugreifen. [Weitere Informationen](../start/get-started-tracking.md)

* Die Seite zur Verwaltung des E-Mail-Opt-outs wurde um detaillierte Informationen zum Abmeldefluss erweitert, die die erwartete Reihenfolge der Ereignisse für das Landingpage-Opt-out erläutern. [Weitere Informationen](../email/email-opt-out.md#send-message-unsubscribe-link)

* Die Dokumentation zur Abonnement-Liste wurde aktualisiert und enthält jetzt Informationen zu den Eignungskriterien für Streaming-Segmente. [Weitere Informationen](../landing-pages/subscription-list.md#define-subscription-list)

* Ein neues Handbuch zur IP-Aufwärmzustellbarkeit ist verfügbar, das umfassende Anleitungen zu den Reputationsgrundlagen, zur Vorbereitung vor dem Einsatz, zu Monitoring-Metriken und zu Best Practices für den Übergang von keiner Reputation zu einer erfolgreichen Posteingangsplatzierung bietet. [Weitere Informationen](../configuration/ip-warmup-deliverability-guide.md)

* Den Abschnitten „Landingpage“ und „E-Mail-Opt-out“ wurde eine Warnung hinzugefügt, die klarstellt, dass durch Klicken auf einen Abmelde-Link nur die Landingpage geöffnet wird, Benutzende das Formular jedoch absenden müssen, um den Opt-out-Prozess abzuschließen. [Weitere Informationen](../landing-pages/lp-use-cases.md#configure-opt-out)

* Eine neue Bibliothek mit Journey-Anwendungsfällen ist jetzt verfügbar, die eine Sammlung praktischer Anwendungsfälle enthält, einschließlich taktischer Muster (Unterdrückungslogik, Personalisierungstechniken, Journey-Ausstiegsstrategien) und vollständiger End-to-End-Szenarien für Marketing-Workflows und technische Workflows. [Weitere Informationen](../building-journeys/jo-use-cases.md)

* Ein neues Anwendungsbeispiel ist jetzt verfügbar, das zeigt, wie eine Journey so konfiguriert werden kann, dass nur an Wochentagen (Montag bis Freitag) E-Mails gesendet werden. Dabei werden Eintritte am Wochenende automatisch in die Warteschlange gestellt, sodass am Montag zu einem bestimmten Zeitpunkt ein Versand erfolgt. [Weitere Informationen](../building-journeys/weekday-email-uc.md)

* Eine neue Seite ist jetzt verfügbar, auf der die Entscheidungsfunktionen von Journey Optimizer erläutert werden, einschließlich der Unterschiede zwischen dem Entscheidungsfindungs-Framework der nächsten Generation und der etablierten Entscheidungs-Management-Lösung sowie deren wichtigsten Vorteilen bei der kanalübergreifenden Bereitstellung personalisierter Angebote. [Weitere Informationen](../experience-decisioning/gs-decision.md)

* Es wurde ein neuer Abschnitt zur Dokumentation der Zielgruppenaktivierung hinzugefügt, in dem erläutert wird, wie nicht unterstützte Zielgruppentypen (wie Customer Journey Analytics-Zielgruppen) in [!DNL Journey Optimizer] aktiviert werden, indem sie in eine neue Segmentdefinition im Zielgruppenportal eingeschlossen werden. [Weitere Informationen](../audience/target-audiences.md#activation-non-supported)

* Es wurde ein neuer Abschnitt zur Dokumentation der Warteaktivität hinzugefügt, in dem erläutert wird, wie die Attribute von Profilen, die bei einer Warteaktivität in Journeys des Typs „Zielgruppe lesen“ geparkt sind, automatisch vom einheitlichen Profildienst (UPS) aktualisiert werden. Dadurch wird klargestellt, dass sich Profildaten während der Journey-Ausführung nach einem Warteknoten ändern können, was zu unerwarteten Ergebnissen führen kann, wenn konsistente Snapshot-Daten über die gesamten Journey hinweg erwartet werden. [Weitere Informationen](../building-journeys/wait-activity.md#profile-refresh)

* Dem Abschnitt „Pfadexperiment“ wurde ein Warnhinweis hinzugefügt, der Benutzende darauf hinweist, die Metadaten eines Pfadexperiments nach der Veröffentlichung nicht zu bearbeiten, da dies die Berechnung und das Reporting der Experimentergebnisse stört. [Weitere Informationen](../building-journeys/path-experimentation.md)

* Dem Abschnitt „Erstellen einer Formularvoreinstellung“ wurde ein Hinweis hinzugefügt, in dem die Anforderungen für Streaming-Verbindungen angegeben werden, die in der Auswahl-Dropdown-Liste angezeigt werden sollen. [Weitere Informationen](../landing-pages/lp-forms.md#create-form-preset)

* Eine neue Seite ist jetzt im Abschnitt „Entscheidungsfindung“ verfügbar, auf der beschrieben wird, wie die Datenerfassung für das Tracking von Impressions, Klicks und benutzerdefinierten Ereignissen konfiguriert wird. [Weitere Informationen](../experience-decisioning/data-collection/schema-requirement.md)

* Die Dokumentation zur Inhaltsgenerierung mit dem KI-Assistenten wurde neu strukturiert, um mehr Klarheit und Benutzerfreundlichkeit zu erzielen. Die vorherigen fünf kanalspezifischen Seiten (E-Mail, Push, SMS, Web und Landingpage) wurden in drei Seiten nach Generierungstyp zusammengefasst: [Generieren von vollständigem Inhalt](../content-management/generative-full-content.md), [Generieren von Text](../content-management/generative-text.md) und [Generieren von Bildern](../content-management/generative-image.md).

## November 2025 {#november-2025}

* Eine neue Seite mit häufig gestellten Fragen zur Entscheidungsfindung ist jetzt verfügbar, die Themen wie Begrenzungsregeln, KI-Modellkonfiguration, Traffic-Anforderungen und Angebotsoptimierungsstrategien behandelt. [Weitere Informationen](../experience-decisioning/decisioning-faq.md)

* Die Seite „Erste Schritte mit E-Mail-Design“ wurde aktualisiert, um zu erläutern, wie auf den E-Mail-Designer zugegriffen werden kann. [Weitere Informationen](../email/get-started-email-design.md)

* Der Seite „DMARC-Einträge“ wurde ein Abschnitt zur Fehlerbehebung der Latenz der DNS-Verbreitung hinzugefügt. [Weitere Informationen](../configuration/dmarc-record.md#troubleshooting)

* Die Seite „Arbeiten mit GenStudio for Performance Marketing“ wurde durch neue Abschnitte verbessert, die wichtige Funktionen, gängige Anwendungsfälle, Voraussetzungen und häufig gestellte Fragen enthalten. [Weitere Informationen](../integrations/genstudio.md)

* Der Seite „Leitlinien und Einschränkungen“ wurde eine Leitlinie zum Targeting pseudonymer Profile mit Inbound-Kanälen hinzugefügt: Wenn Sie nicht authentifizierte Besuchende ansprechen, erhöht sich die Gesamtzahl der ansprechbaren Profile. Daher empfiehlt Adobe das Festlegen einer Time-to-Live (TTL) für das automatische Löschen von Profilen, um die damit verbundenen Kosten zu verwalten. [Weitere Informationen](../start/guardrails.md#profile-management-inbound)

* Auf der Seite „Code-basierte Implementierungsmethoden“ finden Sie jetzt Verweise auf zwei Tutorials zum Konfigurieren des Web SDK für die Entscheidungsfindung und Code-basierte Erlebnisse. [Weitere Informationen](../code-based/code-based-decisioning-implementations.md#tutorials)

* Es wurde ein Hinweis hinzugefügt, dass Assets und Bilder bis zu 2 Jahre (730 Tage) ab der ersten Veröffentlichung verfügbar bleiben und nach Ablauf erneut veröffentlicht werden müssen. [Weitere Informationen](../content-management/proofs.md)

* Ein umfassendes Handbuch zur Erstellung von Inhalts-Prompts für den KI-Assistenten ist jetzt verfügbar. In diesem Handbuch erfahren Sie, wie Sie effektive Prompts formulieren, um hochkonvertierende, markenkonforme Marketing-Inhalte zu erstellen. Lernen Sie Best Practices für die Formulierung von Marketing-Zielen, die Verwendung von Marken-Assets und die Optimierung von Inhalten für verschiedene Kanäle kennen. [Weitere Informationen](../content-management/ai-assistant-prompting-guide.md)

* Der Dokumentation zum Definieren von Segmenten wurde ein Hinweis hinzugefügt, um klarzustellen, dass das Attribut `frequencyMap` bei der Verwendung in Segmentdefinitionen nicht unterstützt wird und nicht als Teil von Kriterien für die Zielgruppensegmentierung verwendet werden kann. Bei Targeting anhand von Häufigkeit sollten Sie den Einsatz von Frequenzbegrenzungsregeln unter Geschäftsregeln in Erwägung ziehen. [Weitere Informationen](../audience/creating-a-segment-definition.md)
* Ein neues Beispiel, das zeigt, wie benutzerdefinierte Aktionsantworten auf nativen Kanälen verwendet werden, wurde zur Dokumentation der API-Aufrufantworten hinzugefügt. Das Beispiel zeigt, wie mithilfe der Handlebars-Syntax in E-Mails, Push- und SMS-Nachrichten über verschachtelte Arrays aus benutzerdefinierten Aktionsantworten iteriert werden können. [Weitere Informationen](../action/action-response.md#response-in-channels)

* Ein neuer Abschnitt wurde der Dokumentation zur Integration von Campaign V7/V8 hinzugefügt, in dem beschrieben wird, wie vorhandene benutzerdefinierte Aktionen aktualisiert werden, wenn sich der Echtzeit-Endpunkt (RT) ändert. Der Abschnitt enthält schrittweise Anweisungen zum Aktualisieren der Endpunkt-URL, zum Testen der Verbindung und zum Überprüfen von Änderungen vor dem Speichern. [Weitere Informationen](../action/acc-action.md#update-action)

* Es wurden neue Abschnitte über Einschränkungen und Best Practices zur Dokumentation für visuelle Fragmente hinzugefügt, um Benutzende vor nicht unterstützter Verschachtelung von Fragmenten mit bedingtem Inhalt in anderen entsperrten Fragmenten mit bedingtem Inhalt zu warnen. Die Anleitung enthält Schritte zur Fehlerbehebung bei Problemen mit dem Kompatibilitätsmodus und Empfehlungen für die richtige Gestaltung der E-Mail-Struktur. [Weitere Informationen](../email/use-visual-fragments.md#fragment-dynamic-content)

* Ein Abschnitt zur Fehlerbehebung wurde der Journey-Dokumentation für Live-Reporting hinzugefügt, um Benutzende bei der Lösung von Problemen mit fehlenden Reporting-Daten zu unterstützen. Der Abschnitt behandelt die Synchronisierung von Journey-Namen mit Reporting-Datensätzen, den Zeitpunkt der Datenaktualisierung, die Überprüfung von Zugriffsberechtigungen und die Anforderungen an den Journey-Status. [Weitere Informationen](../building-journeys/report-journey.md#troubleshooting-missing-data)

* In der Dokumentation zu Assets wurden drei neue häufig gestellte Fragen hinzugefügt, die den Ablauf von Assets und die Lebenszyklusverwaltung beschreiben. Behandelte Themen umfassen die Time-To-Live-Richtlinie (TTL) für AEM-Assets (730 Tage), die Behebung defekter Bilder aufgrund abgelaufener Assets und Informationen zu bevorstehenden Verbesserungen der Logik für den Ablauf von Assets. [Weitere Informationen](../integrations/assets.md#faq-assets)

* Ein ausführlicher Abschnitt zur Fehlerbehebung wurde der Dokumentation zur Aktivität „Zielgruppe lesen“ hinzugefügt. Darin wird erläutert, wie Abweichungen bei der Zielgruppengröße zwischen der geschätzten und der tatsächlichen Anzahl von Profilen, die in Journeys eintreten, behoben werden können. Der Abschnitt behandelt Probleme bei der Zeitplanung und Datenübertragung, Techniken zur Datenvalidierung und -überwachung sowie Best Practices, einschließlich der Verwendung der Option „Nach Auswertung der Batch-Zielgruppe auslösen“. [Weitere Informationen](../building-journeys/read-audience.md#audience-count-mismatch)

* Ein Hinweis wurde der Dokumentation zu Ereignissen für Zielgruppenqualifizierung hinzugefügt. Darin wird die Latenz bei der Streaming-Segmentierung (bis zu 2 Stunden) erläutert und das Hinzufügen einer Warteaktivität oder eines Pufferzeitraums für zeitkritische Journeys empfohlen. [Weitere Informationen](../building-journeys/audience-qualification-events.md#streamed-speed-segment-qualification)

* Ein neuer Abschnitt wurde der Dokumentation für E-Mail-Leitlinien hinzugefügt, der die Größenbeschränkung von 2 MB für Nachrichteninhalte bei der Veröffentlichung von Journeys beschreibt und Best Practices enthält, um erstellte Inhalte unter 1 MB zu halten und so den Mehraufwand für die Backend-Verarbeitung zu berücksichtigen. [Weitere Informationen](../start/guardrails.md#message-content-size)

* Die Dokumentation für die Option „Inkrementelles Lesen“ in den Aktivitäten „Zielgruppe lesen“ wurde verbessert, um Abhängigkeiten beim Timing von Snapshots und die 24-stündige Lookback-Einschränkung zu erläutern, einschließlich Empfehlungen zur Vermeidung fehlender Profile. [Weitere Informationen](../building-journeys/read-audience.md)

* Es wurde ein Hinweis zu den Leitlinien für die Datensatzsuche hinzugefügt, der angibt, dass Suchen nicht miteinander verkettet werden können. [Weitere Informationen](../data/lookup-aep-data.md#guidelines)

* Die Kanäle WhatsApp und LINE sind jetzt für Aktionskampagnen verfügbar. [Weitere Informationen](../campaigns/campaign-content.md)

* Der Dokumentation zur Eintrittsverwaltung wurde ein neuer Abschnitt zur Journey-Verarbeitungsrate hinzugefügt, der Profileintrittsraten, Ereignisse und Zielgruppenqualifikationen innerhalb von Journeys, Auswirkungen auf Warteaktivitäten und Auswirkungen auf Aktionsaktivitäten behandelt. [Weitere Informationen](../building-journeys/entry-management.md#journey-processing-rate)

* Beim Entwerfen von E-Mail-Nachrichten prüft das System jetzt auf wichtige Einstellungen und zeigt Warnhinweise für Warnungen und Fehler an. Informationen zu E-Mail-Warnhinweisen und Validierungsanforderungen wurden zur Seite „Leitlinien“ hinzugefügt. [Weitere Informationen](../email/create-email.md#check-email-alerts)

* Der Warnhinweis, der besagt, dass die Frequenzbegrenzung für zuvor erstellte Angebote nicht aktiviert oder deaktiviert werden kann, wurde aus dem Abschnitt „Hinzufügen von Einschränkungen zu einer Angebotsseite“ entfernt. [Weitere Informationen](../offers/offer-library/add-constraints.md#capping)

* Die Dokumentation zum Arbeiten mit Journey-Schrittereignissen ist jetzt verfügbar. [Weitere Informationen](../reports/journey-step-events-overview.md)

* Ein neues, umfassendes Handbuch zu den Journey-Eintritts- und -Ausstiegskriterien ist jetzt verfügbar, das Best Practices, Beispiele aus der Praxis und praktische Anleitungen für die Verwaltung von Profilen beim Eintritt in und Ausstieg aus Journeys in Adobe Journey Optimizer enthält. [Weitere Informationen](../building-journeys/entry-exit-criteria-guide.md)

* Eine neue Seite ist jetzt verfügbar, auf der erläutert wird, wie über kontextuelle Daten in Nachrichten iteriert wird. In diesem Handbuch wird die Verwendung der Handlebars-Syntax beschrieben, um dynamische Listen aus Ereignissen, Antworten benutzerdefinierter Aktionen, Datensatzsuchen und anderen Kontextquellen in Ihrer Personalisierung anzuzeigen. [Weitere Informationen](../personalization/iterate-contextual-data.md)

* Die Abfrage zur Identifizierung verworfener Ereignisse in Journeys wurde korrigiert, sodass jetzt die richtigen Filter für Fehler beim Exportieren von Segmentaufträgen, Dispatcher-Verwerfungen und State-Machine-Verwerfungen enthalten sind. [Weitere Informationen](../reports/query-examples.md#common-queries)

* In der Dokumentation für Abfragebeispiele wurden einleitende Sätze zu allen 37 Abfragebeispielen hinzugefügt, um besseren Kontext zu bieten und zu erklären, was jede Abfrage tut, bevor der SQL-Code angezeigt wird. Dies verbessert das Verständnis der Benutzenden und bietet eine klarere Anleitung dazu, wann jede Abfrage verwendet werden soll [Weitere Informationen](../reports/query-examples.md)

## Oktober 2025 {#october-2025}

* Sie können jetzt Bilder mithilfe des Bild-zu-HTML-Converters in HTML-Vorlagen umwandeln. [Weitere Informationen](../content-management/image-to-html.md)

* Informationen zum Veröffentlichungszyklus von Adobe Journey Optimizer sind jetzt verfügbar. [Weitere Informationen](releases.md)

* Eine neue Seite mit häufig gestellten Fragen zu Journeys ist jetzt verfügbar. [Weitere Informationen](../building-journeys/journey-faq.md)

* Die Funktion zum Überwachen benutzerdefinierter Aktionen ist jetzt verfügbar. [Weitere Informationen](../action/reporting.md)

* Der Modus mit hohem Durchsatz für durch API ausgelöste Kampagnen ist jetzt verfügbar. [Weitere Informationen](../campaigns/api-triggered-high-throughput.md)

* Eine Referenz zu Fehler-Codes für Journeys ist jetzt verfügbar. [Weitere Informationen](../building-journeys/error-codes-reference.md)

* Die Dokumentation zu Journey Optimizer Experimentation Accelerator ist jetzt verfügbar. [Weitere Informationen](../content-management/experiment-accelerator-gs.md)

* Es wurde ein neuer Abschnitt zur Dokumentation der **formatDate**-Helferfunktion hinzugefügt. In diesem Abschnitt wird die Bedeutung von Schlüsselmustersymbolen wie y, Y, M, d und D erläutert. [Weitere Informationen](../personalization/functions/dates.md#pattern-characters)

* Ein PQL-Beispiel wurde zum Abschnitt „Entscheiden der Rangfolgenformel“ hinzugefügt, um zu zeigen, wie Sie Angebote basierend auf der Postleitzahl und dem Jahreseinkommen eines Profils optimieren können. [Weitere Informationen](../experience-decisioning/ranking/ranking-formulas.md#ranking-formula-examples)

* Im Abschnitt zum Journey-Testmodus wurde eine Einschränkung hinzugefügt, um darauf hinzuweisen, dass der Testmodus keine benutzerdefinierte Anreicherung von Zielgruppenattributen beim Hochladen unterstützt. [Weitere Informationen](../building-journeys/testing-the-journey.md#important_notes)

* Auf den Seiten [Leitlinien und Einschränkungen für das Entscheidungs-Management](../offers/decision-management-guardrails.md#configurations) und [Leitlinien und Einschränkungen für die Entscheidungsfindung](../experience-decisioning/decisioning-guardrails.md#configurations) wurde ein neuer Abschnitt hinzugefügt, um die maximale Anzahl unterstützter Konfigurationen (20.000) anzugeben, die der Gesamtzahl der in Ihrer Sandbox vorhandenen Begrenzungsregeln entspricht.

* Im Abschnitt „Bedingungsaktivität“ von Journeys wurde ein Hinweis hinzugefügt, dass die Bedingungsauswertung für Profile mit mehr als zwei geräteübergreifenden Identitäten fehlschlägt. [Weitere Informationen](../building-journeys/conditions.md)

* Eine neue Seite wurde hinzugefügt, auf der beschrieben wird, wie Einverständnisrichtlinien verwendet werden können, um die Voreinstellungen Ihrer Kundinnen und Kunden basierend auf ihrer Auswahl zu berücksichtigen und gleichzeitig ihr Einverständnis zu respektieren. [Weitere Informationen](../action/preference-center.md)

* Auf den Seiten zu den ersten Schritten mit Profilen und Leitlinien wurde ein Hinweis hinzugefügt, dass bei der Datenaufnahme bei E-Mails die Groß- und Kleinschreibung beachtet wird. Das bedeutet, dass doppelte Profile erstellt und beim Targeting der entsprechenden Empfängerin bzw. des entsprechenden Empfängers verwendet werden können. [Weitere Informationen](../audience/get-started-profiles.md)

* Im Personalisierungseditor wurde ein neues `render`-Attribut eingeführt. Legen Sie es auf `false` fest, wenn Sie den Inhalt eines Ausdrucksfragments ausblenden möchten. [Weitere Informationen](../personalization/use-expression-fragments.md#use-expression-fragment)

* Dem Abschnitt wurde eine Liste von Leitlinien hinzugefügt, die beschreiben, wie Fragmente genutzt werden können, die in Entscheidungsrichtlinien an Entscheidungselemente angehängt sind. [Weitere Informationen](../experience-decisioning/use-decision-policy.md#fragments)

* Es wurden Best Practices für die Datensatzsuche hinzugefügt: Aktivieren Sie die Optionen, um Indizierungsprobleme zu vermeiden, und machen Sie sich mit den Auswirkungen von Batch-Löschvorgängen auf die Datensuche vertraut. [Weitere Informationen](../data/lookup-aep-data.md#guidelines)

* Es wurde eine Einschränkung hinzugefügt, die darauf hinweist, dass bei der Verwendung von Journeys vom Typ „Zielgruppe lesen“ mit zusätzlichen Kennungen nur Zielgruppen des einheitlichen Profildienstes unterstützt werden. [Weitere Informationen](../building-journeys/supplemental-identifier.md#guardrails)

* Die Dokumentation für Experimentation Accelerator wurde in eine andere Sammlung verschoben. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/experimentation-accelerator/using/overview)

## September 2025 {#september-2025}

* Der Seite mit Leitlinien und Einschränkungen wurde ein neuer Abschnitt für Inbound-Kanäle hinzugefügt, um alle Einschränkungen zu erfassen, die für die Kanäle „Web“, „In-App“, „Code-basierte Erlebnisse“ und „Inhaltskarten“ gelten. Hier werden die Einschränkung auf 5.000 eingehende Anfragen pro Sekunde für alle eingehenden Anfragen sowie die maximale Anzahl von 500 aktiven eingehenden Aktionen erwähnt. [Weitere Informationen](../start/guardrails.md#inbound-guardrails)

* Für orchestrierte Kampagnen wurde eine Seite mit häufig gestellten Fragen veröffentlicht. [Weitere Informationen](../orchestrated/orchestrated-campaigns-faq.md)

* Der Dokumentation für Journey-Schrittereignisse wurde ein Abschnitt zur Fehlerbehebung hinzugefügt, der Definitionen, häufige Ursachen und Schritte zur Fehlerbehebung für die am häufigsten auftretenden Verwerfungstypen von Ereignissen enthält. [Weitere Informationen](../reports/sharing-field-list.md#discarded-events)

* Die Dokumentation zur Verwendung zusätzlicher Kennungen in Journeys enthält jetzt eine Tabelle, in der beschrieben wird, wie sich Profile verhalten, wenn Ausstiegskriterien in Journeys mit zusätzlicher Kennung angewendet werden. [Weitere Informationen](../building-journeys/supplemental-identifier.md#exit-criteria)

* Ein Abschnitt zur Fehlerbehebung wurde hinzugefügt, um Verwerfungen von Profilen in pausierten Journeys besser nachvollziehen zu können. [Weitere Informationen](../building-journeys/journey-pause.md#discards-troubleshoot)

* In der Dokumentation zum Schemaüberblick wurden Informationen hinzugefügt, um Standard- und relationale Schemata zu unterscheiden, die für orchestrierte Kampagnen verwendet werden. [Weitere Informationen](../data/gs-data.md)

* In der Dokumentation zu Entscheidungsfindung und Entscheidungs-Management wurden Informationen zu den Anforderungen für das erfolgreiche Trainieren der Modelle für [automatische Optimierung](../experience-decisioning/ranking/auto-optimization-model.md) und [personalisierte Optimierung](../experience-decisioning/ranking/personalized-optimization-model.md) hinzugefügt.

* Es wurde klargestellt, dass REST-API-Aufrufe zur interaktiven Nachrichtenausführung ein Timeout von 60 Sekunden aufweisen, wobei es interne Wiederholungsversuche gibt, um den Versand sicherzustellen. [Weitere Informationen](../campaigns/trigger-campaigns.md)

* Die Seite mit Entscheidungselementsammlungen wurde aktualisiert, um das Verhalten des Operators **CONTAINS** beim Definieren von Regeln zu verdeutlichen. [Weitere Informationen](../experience-decisioning/collections.md)

* Die Seite „Zuweisen von Prioritätswerten“ wurde mit den spezifischen Schritten aktualisiert, um einen Prioritätswert für eingehende Kanalaktionen innerhalb der Aktivität **Aktion** zu definieren. [Weitere Informationen](../conflict-prioritization/priority-scores.md#priority-action)

## August 2025 {#august-2025}

* Es wurde eine neue Seite mit den Best Practices für die Gestaltung barrierefreier E-Mail- und Landingpage-Inhalte mit [!DNL Journey Optimizer] hinzugefügt. [Weitere Informationen](../email/accessible-content.md)

* Die Dokumentation zu zusätzlichen Kennungen in Journeys wurde mit den folgenden Klarstellungen aktualisiert:

   * Nachdem Sie eine zusätzliche Kennung zu einem Schema hinzugefügt haben, muss ein neues Ereignis (für ereignisgesteuerte Journeys) oder eine neue Feldergruppe (für Journeys des Typs „Zielgruppen lesen“) erstellt werden. Bestehende Entitäten werden nicht automatisch aktualisiert und erkennen die neue Kennung nicht.

   * Zusätzliche Kennungen werden nicht anhand der DULE-Richtlinien (Data Usage Labeling &amp; Enforcement) validiert und bei Data-Governance-Prüfungen in Journeys nicht berücksichtigt.

     [Mehr dazu](../building-journeys/supplemental-identifier.md)

* Die Seite zur Optimierung in Kampagnen wurde aktualisiert, um der Tatsache Rechnung zu tragen, dass die Optimierung jetzt auch in Journeys verfügbar ist. [Weitere Informationen](../content-management/gs-message-optimization.md)

* Es wurde ein Link zum Tutorial-Video hinzugefügt, in dem beschrieben wird, wie die Nachrichtenoptimierung in einer Kampagne genutzt werden kann. [Weitere Informationen](../content-management/gs-message-optimization.md)

## Juli 2025 {#july-2025}

* Die Benutzeroberfläche für Kampagnen verfügt jetzt über zwei separate Registerkarten: **Aktion** und **Durch API ausgelöst**. Die Dokumentation wurde entsprechend aktualisiert, wobei die Informationen zu den einzelnen Kampagnentypen in eigenen Abschnitten organisiert wurden, um Klarheit und Benutzerfreundlichkeit zu verbessern. [Weitere Informationen](../campaigns/get-started-with-campaigns.md)

* Die Seiten [Erste Schritte mit der Delegierung von Subdomains](../configuration/about-subdomain-delegation.md) und [Delegieren einer Subdomain](../configuration/delegate-subdomain.md) wurden aktualisiert, um die verschiedenen Delegierungsmethoden und die Schritte bei ihrer Einrichtung besser darzustellen.

* Im Abschnitt „Fragmente” wurde ein Hinweis hinzugefügt, der besagt, dass bei aktivierter Nachverfolgung in einer Journey oder Kampagne Links in einem Fragment, das in einer Nachricht verwendet wird, ebenso wie alle anderen Links in der Nachricht nachverfolgt werden. [Weitere Informationen](../content-management/create-fragments.md#content)

* Die Leitlinien und Einschränkungen, die für die Delegierung einer Subdomain in Journey Optimizer gelten, wurden erweitert und in einem eigenen Abschnitt zusammengefasst. [Weitere Informationen](../configuration/delegate-subdomain.md#guardrails)

* Den Seiten „Erstellen von Fallback-Angeboten“ und „Erstellen von Entscheidungen“ wurde ein Hinweis hinzugefügt, in dem erwähnt wird, dass Fallback-Angebote alle in einer Entscheidung verwendeten Darstellungen enthalten sollten. [Weitere Informationen](../offers/offer-library/creating-fallback-offers.md)

* Die Leitlinien für Fragmente wurden erweitert. [Weitere Informationen](../start/guardrails.md#fragments-guardrails).

* Es wurde ein Hinweis hinzugefügt, dass Links in Nachrichten nach 25 Monaten und Links zu Mirror-Seiten nach 90 Tagen ablaufen. [Weitere Informationen](../email/message-tracking.md)

<!--* The possible email error types that could happen upon sending email deliveries with are now listed in a dedicated section. [Read more](../configuration/email-error-types.md)-->

## Juni 2025 {#june-2025}

* Es wurde ein neuer Abschnitt hinzugefügt, in dem beschrieben wird, wie Rich-Text (z. B. Zeilenumbrüche, fett, kursiv usw.) mithilfe von HTML-Komponenten zu anpassbaren Fragmenten hinzugefügt werden kann. [Weitere Informationen](../content-management/customizable-fragments.md#rich-text)

* Der Teil zur Entscheidungsfindung wurde mit einem speziellen Abschnitt zum Erstellen von KI-Modellen überarbeitet. [Weitere Informationen](../experience-decisioning/ranking/ai-models.md)

* Es wurde eine Empfehlung zur Verwendung des Feldes `actionExecutionTime` in der Aktion „journeyStep-Ereignisse“ hinzugefügt. [Weitere Informationen](../reports/sharing-execution-fields.md#actionexecutiontime-field)

* Es wurde ein Hinweis zur `messageID` hinzugefügt, die möglicherweise nicht bei jedem einzelnen Versand eindeutig ist. [Weitere Informationen](../data/datasets-query-examples.md)

* Es wurde eine Empfehlung zur Verwaltung historischer Ereignisse bei Datenhygienevorgängen hinzugefügt. [Weitere Informationen](../privacy/data-hygiene.md#data-hygiene-recommendations)

* Es wurde ein Schutzmechanismus hinzugefügt, der verhindert, dass Landingpages bei der Migration zwischen Sandboxes unterstützt werden. [Weitere Informationen](../configuration/copy-objects-to-sandbox.md#global)

* Es wurde ein Warnhinweis zu verschachtelten JSON-Objekten hinzugefügt, die bei der benutzerdefinierten Authentifizierung für benutzerdefinierte Aktionen nicht unterstützt werden. [Weitere Informationen](../datasource/external-data-sources.md)

* Es wurde ein Warnhinweis zur Namensgebung von bedingten Inhaltsvarianten im E-Mail-Designer hinzugefügt. [Weitere Informationen](../personalization/create-conditions.md)

* Der Abschnitt „Aufheben der Delegierung einer Landingpage-Subdomain“ wurde aktualisiert. [Weitere Informationen](../landing-pages/lp-subdomains.md#undelegate-subdomain)

* Klarstellung der Regeln für den erneuten Journey-Eintritt bei Verwendung zusätzlicher Kennungen. [Weitere Informationen](../building-journeys/supplemental-identifier.md#guardrails)

* Es wurde ein neuer Hinweis hinzugefügt, um klarzustellen, dass Sie den Ausdruckseditor im erweiterten Modus verwenden müssen, wenn Sie bei der Ereigniskonfiguration das zusätzliche Kennungsattribut auswählen. [Weitere Informationen](../building-journeys/supplemental-identifier.md#add)

* Es wurde eine Klarstellung hinzugefügt, wie der Journey-Wiedereintritt mit zusätzlichen Kennungen funktioniert. [Weitere Informationen](../building-journeys/supplemental-identifier.md#guardrails)

## Mai 2025 {#may-2025}

* Die in Journey Optimizer verfügbaren Adobe-Integrationen werden jetzt im Abschnitt „Verbinden von Systemen und Umgebungen“ aufgeführt. [Weitere Informationen](../integrations/ajo-integrations.md)

* Die Inhaltsintegrationen sind jetzt im Abschnitt „Content-Management“ gruppiert. [Weitere Informationen](../integrations/content-integrations.md)

* Architekturdiagramme für Adobe Experience Platform und Journey Optimizer wurden aktualisiert. [Weitere Informationen](../start/get-started.md#architecture)

* Es wurde ein Video über den Personalisierungseditor-Playground hinzugefügt, in dem Sie erfahren, wie Sie Personalisierungs-Code mithilfe von Beispieldaten schreiben und testen können. [Weitere Informationen](../personalization/personalize.md#video-perso)

* Die maximal zulässige Anzahl von Adressen in einer Testadressenliste wurde von 50 auf 300 erhöht. [Weitere Informationen](../configuration/seed-lists.md#create-seed-list)

* Ein neuer Schritt, der beschreibt, wie Code bei Verwendung von Entscheidungsrichtlinien im Editor für Code-basierte Erlebnisse eingeschlossen wird, wurde zur Seite „Erstellen von Entscheidungsrichtlinien“ hinzugefügt. [Weitere Informationen](../experience-decisioning/create-decision.md#create-decision)

* Es wurde ein Hinweis zur Dokumentation zu Code-basierten Erlebnissen hinzugefügt, in dem angegeben wird, dass bei der Ausführung mehrerer Code-basierter Erlebnisaktionen auf derselben Oberfläche der Kampagnen- oder Journey-Prioritätswert bestimmt, was an Endbenutzende gesendet wird, wenn sie für mehr als eine Aktion qualifiziert sind. [Weitere Informationen](../code-based/code-based-surface.md#surface-definition)

* Eine neue Seite zur Fehlerbehebung bei eingehenden Aktionen in Journeys enthält eine schrittweise Anleitung, um Probleme unabhängig zu identifizieren und zu beheben, bevor Sie sich an den Support wenden. [Weitere Informationen](../building-journeys/troubleshooting-inbound.md)

* Es wurde eine neue [Seite](../code-based/code-based-decisioning-implementations.md) hinzugefügt, auf der beschrieben wird, wie Sie Ihrer Client-Implementierung die folgenden Flags hinzufügen, wenn Sie Entscheidungsfindung in Code-basierten Erlebnissen verwenden:

   * Hinzufügen des Flags `dryRun` zum Testen der Entscheidungsfindung in Code-basierten Erlebnissen. [Weitere Informationen](../code-based/code-based-decisioning-implementations.md#code-based-test-decisions)

   * Wenden Sie die Deduplizierung auf Entscheidungsanfragen in Code-basierten Erlebnissen an. [Weitere Informationen](../code-based/code-based-decisioning-implementations.md#code-based-decisioning-deduplication)

## April 2025 {#apr-2025}

* Das Kapitel „Konfiguration“ ist jetzt in drei Kapitel unterteilt: [Kanalkonfiguration](../configuration/get-started-configuration.md), [Journey-Konfiguration](../configuration/about-data-sources-events-actions.md) und [Verbinden Ihrer Systeme](../configuration/ajo-apis.md).
* Es wurde ein Warnhinweis zur Verwendung von Erlebnisereignissen in Journey-Ausdrücken und -Bedingungen hinzugefügt. [Weitere Informationen](../building-journeys/expression/expressionadvanced.md#discovering-the-interface)
* Es wurde ein Hinweis zur Direkt-Mail-Konfigurationsseite zum temporären Speichern der Ausgabedatei hinzugefügt. [Weitere Informationen](../direct-mail/direct-mail-configuration.md)
* Im Abschnitt zum Editor für erweiterte Journey-Ausdrücke wurde ein Tipp zu den Richtlinien für Bedingungsformate hinzugefügt. [Weitere Informationen](../building-journeys/expression/expressionadvanced.md)
* Im Abschnitt zur `inAudience`-Funktion wurde ein Warnhinweis zu Auswirkungen und Best Practices beim Umbenennen einer Zielgruppe hinzugefügt. [Weitere Informationen](../building-journeys/functions/functioninaudience.md)
* Es wurde eine Empfehlung zur Verwendung nativer Keywords bei der Verwendung von bidirektionalen SMS hinzugefügt. [Weitere Informationen](../mobile/mobile-opt-out.md)
* Die Journey-Testseite wurde mit einem Hinweis auf die Notwendigkeit aktualisiert, einen Identity-Namespace in das verwendete Ereignis einzuschließen. [Weitere Informationen](../building-journeys/testing-the-journey.md)
* Die Delegierung von Subdomains kann derzeit nicht über die Benutzeroberfläche von [!UICONTROL Journey Optimizer] aufgehoben werden. Sie müssen sich hierzu an den Adobe-Support wenden. Die Schritte zum Aufheben der Delegierung einer Subdomain werden jetzt für [E-Mails](../configuration/delegate-subdomain.md#undelegate-subdomain), [SMS](../mobile/mobile-subdomains.md#undelegate-subdomain), [Web-Erlebnisse](../web/web-delegated-subdomains.md#undelegate-subdomain) und [Landingpages](../landing-pages/lp-subdomains.md#undelegate-subdomain) beschrieben.<!--[Read more](../configuration/delegate-subdomain.md#undelegate-subdomain)-->
* Es wurde eine Klarstellung zum optionalen `maxHttpConnections`-Parameter im Journey-Begrenzungs-API hinzugefügt, einschließlich Anleitungen zu dessen Verwendung zusammen mit Drosselungskonfigurationen für denselben Endpunkt. [Weitere Informationen](../configuration/throttling.md)
* Im Abschnitt „Entscheidungsfindung“ wurde ein Hinweis hinzugefügt, der erklärt, dass genehmigte Angebotselemente nicht gelöscht werden können, wenn sie in einer Sammlung oder Entscheidung verwendet werden. Es wurden Schritte zum Ändern ihres Status in „Entwurf“ mithilfe der Option **[!UICONTROL Genehmigung rückgängig machen]** eingeschlossen. [Weitere Informationen](../experience-decisioning/items.md#manage)
* Informationen zu Sandboxes wurden in einem neuen Abschnitt zur Sandbox-Verwaltung zusammengefasst. Dieser neue Abschnitt enthält Informationen zur Verwendung und Zuweisung von Sandboxes und zur Verwendung der Paketexport- und -importfunktionen zum Kopieren von Objekten wie Journeys, Inhaltsvorlagen oder Fragmenten über mehrere Sandboxes hinweg. [Weitere Informationen](../administration/sandboxes.md)

## März 2025 {#mar-2025}

* Die Seite über Zielgruppen-Qualifizierungsereignisse wurde mit neuen Empfehlungen aktualisiert. [Weitere Informationen](../building-journeys/audience-qualification-events.md)
* Die Fehlerbehebungsfunktion für benutzerdefinierte Aktionen ist jetzt für alle Kundinnen und Kunden verfügbar (GA). [Weitere Informationen](../action/troubleshoot-custom-action.md)
* „Datenhygiene“ wird in der Benutzeroberfläche des Produkts jetzt als „Datenlebenszyklus“ bezeichnet. Die Dokumentation wurde entsprechend dieser Änderung aktualisiert. [Weitere Informationen](../privacy/data-hygiene.md)
* Die fehlenden integrierten Berechtigungen für die Landingpage wurden der Dokumentation hinzugefügt. [Weitere Informationen](../administration/ootb-permissions.md)
* Es wurde ein Hinweis zur Planung wiederkehrender Kampagnen hinzugefügt. [Weitere Informationen](../campaigns/create-campaign.md)
* Der Abschnitt zum Einfügen von Links und Aktivieren des Trackings in einer E-Mail-Nachricht wurde aktualisiert und neu organisiert. [Weitere Informationen](../email/message-tracking.md)
* Der Abschnitt über Personalisierungsfunktionen in Adobe Journey Optimizer wurde neu organisiert und verbessert. [Weitere Informationen](../personalization/personalize.md)
* Die Entscheidungs-Management-API zur Auflistung personalisierter Angebote wurde um ein Beispiel für die Durchführung einer Paginierung ergänzt, falls mehrere personalisierte Angebote in der Antwort fehlen. [Weitere Informationen](../offers/api-reference/offers-api/personalized-offers/offers-list.md)
* Zur besseren Übersichtlichkeit wurde eine neue Seite erstellt, die alle Informationen zur Funktion „Abbestellung der Liste“ enthält. [Weitere Informationen](../email/list-unsubscribe.md)
* Der Abschnitt „Frequenzbegrenzung“ wurde aktualisiert und beschreibt nun, wie der Frequenzbegrenzungszähler für die Decisioning- und Batch Decisioning-APIs zusätzlich zum Edge Decisioning-API aktualisiert wird. [Weitere Informationen](../offers/offer-library/add-constraints.md#frequency-capping)

## Februar 2025 {#feb-2025}

* Die Leitlinien für die Aktivität „Zielgruppe lesen“ wurden aktualisiert. Sie geben jetzt vor, dass in einer Journey nur eine Aktivität verwendet werden und diese nur eine Zielgruppe ansprechen kann. [Weitere Informationen](../building-journeys/read-audience.md)
* Die Journey-Leitlinien bei der Verwendung von Adobe Campaign-Aktivitäten wurden aktualisiert. [Weitere Informationen](../start/guardrails.md#ac-g)
* Die Schritte zum Erstellen Ihrer ersten Journey wurden ausführlich beschrieben, und zum Dokumentationsabschnitt wurden Links hinzugefügt. [Weitere Informationen](../building-journeys/journey-gs.md)
* Es ist jetzt eine neue Seite verfügbar, auf der das Journey-Dashboard und die Benutzeroberfläche zum Filtern beschrieben werden. [Weitere Informationen](../building-journeys/journey-ui.md)
* Die Dokumentation zur **[!UICONTROL Optimierung des Versandzeitpunkts]** und die zugehörigen häufig gestellten Fragen wurden aktualisiert, verbessert und auf eine neue dedizierte Seite verschoben. [Weitere Informationen](../building-journeys/send-time-optimization.md)
* Es wurden neue Schutzmechanismen für Journey-Ereignisse hinzugefügt. [Weitere Informationen](../start/guardrails.md#events-g)
* Die Seite mit den integrierten Kanalaktionen wurde neu angeordnet. [Weitere Informationen](../building-journeys/journey-action.md)
* Den Abschnitten „Entscheidungsfindung“ und „Entscheidungs-Management“ wurden Leitlinien und Einschränkungen hinzugefügt.
   * [Leitlinien und Einschränkungen für die Entscheidungsfindung](../experience-decisioning/decisioning-guardrails.md)
   * [Schutzmechanismen und Einschränkungen für das Entscheidungs-Management](../offers/decision-management-guardrails.md)
* Der Dokumentation zum Entscheidungs-Management wurde ein neuer Abschnitt zu Kontextdaten hinzugefügt. Er enthält Informationen zur Nutzung von Kontextdaten in der Entscheidungs-Engine, beispielsweise zum Entwerfen einer Entscheidungsregel, die verlangt, dass das aktuelle Wetter zum Zeitpunkt der Entscheidungsanfrage wärmer als 25 °C sein muss. [Weitere Informationen](../offers/context-data.md)

## Januar 2025 {#jan-2025}

* In der E-Mail-Konfiguration wurde ein neuer Abschnitt zur Option **[!UICONTROL Ausführungsadresse]** hinzugefügt. Die primäre Adresse wird auf Sandbox-Ebene definiert, aber die Standardeinstellung kann für eine bestimmte E-Mail-Konfiguration überschrieben werden. [Weitere Informationen](../email/email-settings.md#execution-address)

* Die Seite **Erste Schritte mit der Zustellbarkeit** wurde aktualisiert und bietet nun die Möglichkeit, IP-Aufwärm-Workflows direkt über die Benutzeroberfläche zu erstellen. [Weitere Informationen](../reports/deliverability.md#reputation)

* Der Abschnitt **Header-Parameter** wurde aktualisiert und enthält jetzt die neuen Labels und Änderungen an der Benutzeroberfläche. [Weitere Informationen](../email/email-settings.md#email-header)

* Der Abschnitt **Weiterleiten von E-Mails** wurde aktualisiert und gibt nun an, dass alle an die Adresse unter **Von E-Mail** gesendeten E-Mails an die Weiterleitungs-E-Mail-Adresse weitergeleitet werden. Wenn keine Weiterleitungs-E-Mail-Adresse angegeben ist, werden diese E-Mails verworfen. [Weitere Informationen](../email/email-settings.md#email-settings)

* Die maximale Größe von kontextuellen Attributen, die an eine API-ausgelöste Kampagnenanfrage übergeben werden, wurde auf 200 KB aktualisiert. [Weitere Informationen](../campaigns/api-triggered-campaigns.md#contextual)

* Es wurde ein neuer Abschnitt zur Seite **Verwalten von Fragmenten** hinzugefügt, in dem beschrieben wird, wie einem Live-Fragment neue Attribute hinzugefügt werden. Außerdem wurde die gesamte Seite verbessert. [Weitere Informationen](../content-management/manage-fragments.md#adding-new-attributes)

* Der Abschnitt „Leitlinien und Einschränkungen“ wurde zur Dokumentation der Werkzeuge für Konflikt-Management und Priorisierung hinzugefügt. [Weitere Informationen](../conflict-prioritization/gs-conflict-prioritization.md)

* Es wurde ein neuer vollständiger Anwendungsfall hinzugefügt, der alle Schritte umfasst, die zur Verwendung der Entscheidungsfindung in Inhaltsexperimenten mit dem Code-basierten [!DNL Journey Optimizer]-Erlebniskanal erforderlich sind. [Weitere Informationen](../experience-decisioning/experience-decisioning-uc.md)

* Die Seite **Konfigurieren von E-Mail-Einstellungen** wurde zur besseren Lesbarkeit in mehrere Unterseiten unterteilt, einschließlich neuer eigenständiger Seiten für [Von der Liste abmelden](../email/list-unsubscribe.md), [Header-Parameter](../email/header-parameters.md) und [URL-Tracking](../email/url-tracking.md).

+++ 2024

## Dezember 2024 {#nov-2024}

* Es wurde eine Notiz hinzugefügt, die bei der Fehlerbehebung bezüglich einer potenziellen Fehlermeldung hilft, wenn ein API-Aufruf durchgeführt wird, um Datensätze für die Personalisierung mithilfe von Daten der Adobe Experience Platform zu aktivieren. [Weitere Informationen](../personalization/aep-data-perso.md)

## Oktober 2024 {#oct-2024}

* Alle neuen Funktionen und Verbesserungen von [!DNL Journey Optimizer] in der Version Oktober 2024 sind in der Dokumentation beschrieben. [Mehr dazu](release-notes.md)
* Alle in [!DNL Journey Optimizer] verfügbaren Kommunikationskanäle sind jetzt in einem speziellen Abschnitt der Dokumentation gruppiert. [Mehr dazu](../channels/gs-channels.md)
* Die Seite **Konfigurieren des Code-basierten Erlebnisses** wurde verbessert, um den Vorgang klarer zu beschreiben. Dazu gehört auch der Abschnitt, in dem erklärt wird, was ein Oberflächen-URI ist. [Mehr dazu](../code-based/code-based-configuration.md)
* Die Seite **Erstellen einer Web-Kanalkonfiguration** wurde aktualisiert, um die Schritte beim Erstellen einer Regel zum Seitenabgleich zu verdeutlichen, die auch für die Code-basierte Erlebniskonfiguration gelten. [Mehr dazu](../web/web-configuration.md#web-page-matching-rule)
* Es wurde ein Hinweis zum anstehenden Time-to-Live(TTL)-Limit für systemgenerierte Datensätze hinzugefügt. [Mehr dazu](../data/get-started-datasets.md)
* Es wurde ein neuer Abschnitt hinzugefügt, in dem beschrieben wird, wie Sie Ihre Code-basierten personalisierten Erlebnisse direkt in Ihrem Browser oder auf Ihren Mobilgeräten mithilfe der Option **Vorschau auf Gerät** anzeigen können, wenn Sie Inhalte in einer Journey oder Kampagne simulieren. [Mehr dazu](../code-based/test-code-based.md#preview-on-device)
* Es wurde eine neue Seite hinzugefügt, auf der erläutert wird, wie benutzerdefinierte Upload-Zielgruppen für die Entscheidungsfindung genutzt werden können. [Mehr dazu](../offers/custom-upload-decisioning.md)
* Eine neue Seite wurde hinzugefügt, auf der die in Journey Optimizer verfügbaren Entscheidungsfunktionen vorgestellt werden. [Weitere Informationen](../experience-decisioning/gs-decision.md)
* Der Dokumentation zur Entscheidungsfindung wurden Schutzmechanismen und Einschränkungen hinzugefügt. [Mehr dazu](../experience-decisioning/gs-experience-decisioning.md#guardrails)

## September 2024 {#sept-2024}

* Alle neuen Funktionen und Verbesserungen, die mit der Version September 2024 von [!DNL Journey Optimizer] eingeführt werden, sind in der Dokumentation ausführlich beschrieben. [Mehr dazu](release-notes.md)
* Ein Abschnitt über die Verwaltung von Wiederholungsversuchen in Journey wurde hinzugefügt. [Mehr dazu](../building-journeys/read-audience.md#read-audience-retry)
* Die häufig gestellten Fragen zur Begrenzungs-/Einschränkungsregel für benutzerdefinierte Aktionen wurden aktualisiert und erwähnen nun die standardmäßige Begrenzungsregel. [Mehr dazu](../configuration/external-systems.md#faq)
* Der Abschnitt über die Zugriffskontrolle wurde mit Berechtigungen im Zusammenhang mit dem Inhaltsgenerator des KI-Assistenten aktualisiert. [Weitere Informationen](../administration/high-low-permissions.md#ai-orchestrated-campaign)
* Es wurde ein Video über den Inhaltsgenerator des KI-Assistenten für die E-Mail-Erstellung hinzugefügt. [Weitere Informationen](../content-management/generative-full-content.md#video)

+++

<!--
## August 2024 {#aug-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] August '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Performance guardrails for Decision management have been updated to mention Decisioning APIs delivery throughputs with/without Edge Segmentation. [Read more](../start/guardrails.md#decision-management)
* Journey guardrails have been updated. [Read more](../start/guardrails.md#journeys-guardrails-journeys)


## July 2024 {#july-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] July '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A personalization use case has been added on how to personalize an email with information related health plans and prescriptions. [Read more](../personalization/perso-uc-plan-prescriptions.md)

## June 2024 {#june-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] June '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A note about the usage of merge policies in journeys has been added on [this page](../building-journeys/journey-properties.md#merge-policies).
* The page about how to configure a **Wait** activity in a journey has been reorganized and improved. [Read more](../building-journeys/wait-activity.md)
* A new page has been created to detail journey's properties. [Read more](../building-journeys/journey-properties.md)

## May 2024 {#may-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] May '24 release have been detailed in the documentation. [Read more](release-notes.md)
* The section on seed lists has been updated regarding recurring journeys. [Read more](../configuration/seed-lists.md#use-seed-list)
* The setion on external data sources has been updated. [Read more](../datasource/external-data-sources.md#custom-authentication-access-token)
* The global journey timeout of 30 days has been added to the Guardrail and limitation page. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* The section on the Adobe Campaign v7/v8 integration has been updated with information on provisionning. [Read more](../action/acc-action.md#access)
* The expression editor used to personalize content has been renamed in the documentation to "personalization editor" to clearly differenciate it from the [Journey expression editor](../building-journeys/expression/expressionadvanced.md). [Read more](../personalization/personalization-build-expressions.md)

## April 2024 {#april-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] April '24 release have been detailed in the documentation. [Read more](release-notes.md#apr-2024)
* Configuration steps for In-app messaging have been detailed. [Read more](../in-app/inapp-configuration.md)
* Documentation for [Offer decisioning APIs](../offers/api-reference/offer-delivery-api/decisioning-api.md) and [Batch decisioning APIs](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md) have been updated.
* Information has been added in the Decision management documentation regarding edge and hub regions management when using frequency capping with the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)
* Information has been added on identity creation with custom namespaces when working with API-triggered campaigns. [Read more](../campaigns/api-triggered-campaigns.md)
* Screeshots have been updated to reflect the improved Journey canvas.
* Naming constraints has been updated in the following page: [Configure a unitary event](../event/about-creating.md), [Configure a business event](../event/about-creating-business.md#gs-business-events), [Configure a custom action](../action/about-custom-action-configuration.md#configuration-steps), [External data sources](../datasource/external-data-sources.md)
* A note has been added on Send Time Optimization availability. [Read more](../building-journeys/send-time-optimization.md)
* A new technical use case has been added on how to create a custom action to send data to Experience Platform. [Read more](../building-journeys/custom-action-aep.md)

## March 2024 {#march-2024}
 
* A Frequently Asked Questions section has been added to address common questions regarding the use of audience composition and custom upload audiences in Journey Optimizer. [Read more](../audience/about-audiences.md#faq)
* All new features and improvements coming with [!DNL Journey Optimizer] March '24 release have been detailed in the documentation. [Read more](release-notes.md#mar-2024)
* The page on profile entrance management has been improved. [Read more](../building-journeys/entry-management.md)
* Troubleshooting information has been added to the Alerts page. [Read more](../reports/alerts.md#alert-profile-error-rate)
* Information on the Wait activity has been added to the page on journey reports. [Read more](../reports/sharing-overview.md)
* For Journeys in test mode, following shortcuts have been disabled:
    * T: Shortcut to toggle the test mode on or off.
    * E: Shortcut used to trigger an event in an event-based journey.
    * P: Shortcut to trigger an event in an audience-based journey for which the Single profile at a time option is turned on.
    * L: Shortcut designated to display the test logs.
* The Message frequency rules page has been updated with a new subsection on daily frequency cap, which is available on demand in addition to weekly or monthly capping.
* The Work with consent policies page has been improved and updated with useful links to the Experience Platform documentation. [Read more](../action/consent.md)
* A new section has been added to reflect the fact that you can display HTML email content templates as thumbnails with the Grid view mode (Limited Availability). [Read more](../content-management/content-templates.md#template-thumbnails)
* A new section has been added to the Deliverability page to explain what feedback loops are and how to leverage them. [Read more](../reports/deliverability.md#feedback-loops)
* A note has been added to the Create personalized offers section to specify that the size of an offer including all its representations cannot exceed 300KB. [Read more](../offers/offer-library/creating-personalized-offers.md#create-offer)

## February 2024 {#feb-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] February '24 release have been detailed in the documentation. [Read more](release-notes.md#feb-2024)
* The Journey Optimizer + Workfront integration has been added to the integrations page. [Read more](../integrations/ajo-integrations.md)
* Information has been added on how to personalize offers' representations based on context data. [Read more](../offers/offer-library/add-representations.md#context-data)
* The guardrails page has ben updated with a note on custom actions which support JSON format only when using request or response payloads. [Read more](../start/guardrails.md#custom-actions-g)
* Additional information has been added about the basic authentication type in external datasources. [Read more](../datasource/external-data-sources.md)
* A note has been added to clearly differenciate the [Journey expression editor](../building-journeys/expression/expressionadvanced.md) from the [personalization editor](../personalization/functions/functions.md).
* The list of functions available in the advanced expression editor has been updated. [Read more](../building-journeys/expression/functions.md)
* The page on the Split function has been updated. [Read more](../building-journeys/functions/functioninaudience.md)
* Information has been added regarding the impact of the opt-in or opt-out of push notifications on In-app messages. [Read more](../in-app/create-in-app.md)
* The Message frequency rules page has been updated to reflect the Duration options available in the user interface (weekly or monthly).
* The Edit a PTR record section has been updated to clarify the fact that PTR records cannot be created manually and that you need to edit PTR records to assign them new subdomains. [Read more](../configuration/ptr-records.md#edit-ptr-record)

## January 2024 {#jan-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] January '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A guardrail about the journey size has been added. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* Journey timeout management has been detailed [in the following section](../building-journeys/journey-properties.md#global_timeout).
* Journey Optimizer [documentation home](../../ajo-home.md) page has been redesigned.
* Recommendations about the Update Profiles activity have been added. [Read more](../building-journeys/update-profiles.md) 
* Information has been added regarding the behavior of timeouts on event activities in journeys. When no event is received during the specified timeout period, individuals will continue the journey if no timeout path is defined. [Read more](../building-journeys/general-events.md#events-specific-time)
* In-app channel configuration prerequisites have been updated with a note about the usage of a custom Dataset preference merge policy. [Read more](../in-app/inapp-configuration.md)
* More details have been added about how to manipulate collections in a custom action response. [Read more](../action/action-response.md#exp-syntax).
* A link to the [Schema Dictionary for Adobe Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=de) has been added to the home page.
* An outdated reference to the AJO Message resource has been removed from the list of resources available in the Audit Log. When an update is done on a message in a journey, a **Journey** log is created. [Read more](../privacy/audit-logs.md)
* Additional recommendations have been added about the usage of the **Read Audience** activity. [Read more](../building-journeys/read-audience.md#must-read)
* The Get started with Adobe Experience Platform audiences page has been improved with a list of audience generation methods. [Read more](../audience/about-audiences.md)
* Best practices have been added when choosing an endpoint to target using a custom action. [Read more](../action/about-custom-action-configuration.md)
* An note has been added to notify users that events cannot be fired from external systems using an API. [Read more](../building-journeys/testing-the-journey.md#important_notes)
* Information on the **currentActionField** function has been added to the list of [collection management functions](../building-journeys/expression/collection-management-functions.md). An expression sample leveraging the function has been added in the [Use API call reponses in custom actions](../action/action-response.md) page.
* Update custom authentication doc regarding cache duration. [Read more] (../datasource/external-data-sources.md)
* Support of `<listObject>` has been modified in multiple functions.
* Update the **duration** parameter in the `toString` function. [Read more](../building-journeys/functions/conversion-functions.md#toString)
* For some external data sources use-cases, usage of custom actions is recommended.
* Event field syntax has been updated. The following syntax is deprecated `@(my_event.myfield}` and replaced by `@event{my_event.myfield}`. [Read more](../building-journeys/expression/field-references.md)

+++ 2023

## November 2023 {#nov-2023}

* The guardrail that limits all custom actions has been changed from 150,000 calls over 30 seconds to 300,000 calls over one minute. In addition, the default capping no longer applies to each endpoint. It is now performed per host and per sandbox. For example, on a sandbox, if you have two endpoints with the same host (eg: `https://www.adobe.com/endpoint1` and `https://www.adobe.com/endpoint2`), the capping will apply for all endpoints under the adobe.com host. "endpoint1" and "endpoint2" will share the same capping configuration and having one endpoint reach the limit will have an impact on the other endpoint. [Read more](../action/about-custom-action-configuration.md)
* A new status for email campaigns has been added to the list of campaigns' statuses. [Read more](../campaigns/manage-campaigns.md#modify-an-action-campaign)
* The Get started with Adobe Experience Platform audiences section has been updated to reflect the audience evaluation methods available and how to select them. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* A new subsection has been added to specify which events should be avoided when building your audience if you are using the streaming segmentation evaluation method. [Read more](../audience/about-audiences.md#streaming-segmentation-events-guardrails)

## October 2023 {#oct-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] October '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added GIFs to illustrate some key capabilities, such as: [Content templates](../content-management/content-templates.md), [Fragments](../content-management/fragments.md), [Computed attributes](../audience/computed-attributes.md), [Direct mail](../direct-mail/get-started-direct-mail.md), [Tags](../start/search-filter-categorize.md#tags), [Decision management optimization models](../offers/ranking/personalized-optimization-model.md), [API-triggered campaigns](../campaigns/api-triggered-campaigns.md), and [Content experiment](../content-management/content-experiment.md).
* The Schema creation process has been updated to reflect latest updates in the user interface, coming with Adobe Experience Platform changes. [Read more](../audience/creating-test-profiles.md) 
* Decision management guardrails have been added to the Guardrails and limitations page. [Read more](../start/guardrails.md#decision-management)
* The Header parameters section has been updated to reflect how out-of-office notifications and challenge responses are handled (they are received on the **[!UICONTROL Error email]**). [Read more](../email/email-settings.md#email-header)
* A new section on how to preview and test your content has been created. [Read more](../content-management/preview-test.md)
* The Implement single-page applications page has been moved to the Adobe Experience Paltform Web SDK documentation. [Read more](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html?lang=de){target="_blank"}
* The Capping section has been updated to reflect the label changes relating to offer capping in the Decision management interface. [Read more](../offers/offer-library/add-constraints.md#capping)
* The Add dynamic content into emails has been updated with details on how to delete a variant. [Read more](../personalization/dynamic-content.md#emails)
* The example for capping & throttling configurations has been updated. [Read more](../configuration/external-systems.md)
* The limitation regarding scalar arrays has been removed from the external data source section. [Read more](../datasource/external-data-sources.md)
* The multi-channel journey use case has been updated. [Read more](../building-journeys/journeys-uc.md)
* The Journey Optimizer documentation set has been updated to reflect the new Experience Platform schema creation process. 

## September 2023 {#september-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] September '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added with scaling best practices and real-time stitching guidance. [Read more](../start/best-practices.md)
* A Frequently-Asked-Questions section has been added for Send-Time Optimization. [Read more](../building-journeys/send-time-optimization.md#faq-send-time)
* A note has been added for the audience qualification activity. It may take up to 10 minutes to be active and listen to profiles entering or exiting the audience. [Read more](../building-journeys/audience-qualification-events.md#batch-speed-segment-qualification)
* A list of limitations to be aware of when creating decision rules has been added to the Decision management documentation. [Read more](../offers/offer-library/creating-decision-rules.md)
* Links to access control documentation have been updated. [Read more](../administration/permissions.md)
* In-app channel prerequisites have been updated with Adobe Experience Platform Data Collection details. [Read more](../in-app/inapp-configuration.md)
* Some expressions presented in ranking formula examples have been updated to avoid validation errors. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* A warning has been added to the Define decision scopes section to specify that if AI model is used in an evaluation criteria group, all the evaluation criteria in that group must use the AI ranking method, with the same specific AI model. Moreover, only one evaluation criteria group can use AI model. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## August 2023 {#august-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] August '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The note about **authentication cache management** in journey has been updated to detail that the token is not shared between different journeys. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* The page about journey **entry management** has been updated to clarify behavior. [Read more](../building-journeys/entry-management.md)
* Offer decisioning **export datasets** are now enabled by default. The note about the previous behavior has been removed.  [Read more](../offers/export-catalog/get-started-export.md)
* Various **campaign report metrics** have been renamed, in both Live and Global reports. [Read more](../reports/campaign-live-report.md)
* A new section has been added on content experiment prerequisites for the web channel. [Read more](../web/web-prerequisites.md#experiment-prerequisites)
* A warning has been added on the **Work with content templates** page to indicate that currently tracking is not supported when testing email content templates. To test tracking, you must use the content template in an email and send a proof. [Read more](../content-management/content-templates.md#content-templates)
* Several warnings have been added in the **Create and publish landing pages** section to specify that you cannot access your landing page by simply copy-pasting into a web browser the URL defined when creating the page, even if published. Instead you can test it using the preview function. [Read more](../landing-pages/create-lp.md)
* A new section has been added on how to **manage consent** for the direct mail channel. [Read more](../direct-mail/test-send-direct-mail.md)

## July 2023 {#july-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] July '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The wait activity documentation page has been improved with additional information and best practices related to the global timeout and reentrance usage. [Read more](../building-journeys/wait-activity.md)
* The page on entry management has been improved. [Read more](../building-journeys/entry-management.md)
* Additional information has been added about the throttling rate in the Read audience activity documentation. [Read more](../building-journeys/read-audience.md)
* Additional information has been added about retries. [Read more](../start/guardrails.md#general-actions-g)
* The **Implement personalization consent** section has been updated to describe how to manually enforce personalization consent in campaigns: you can use the segment rule builder to create an audience containing opt-out profiles or add a split activity to a composition workflow. [Read more](../privacy/opt-out.md#opt-out-expression-editor)

## June 2023 {#june-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] June '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the discard rate ratio in the Journeys overview screen. [Read more](../building-journeys/journey-gs.md#journey-access)
* A note has been added with the steps to follow if you modify your schema with new enumeration values after creating an event [Read more](../event/about-creating.md)
* A recommendation has been added to use journeyVersionID instead of journeyVersionName when querying journeys. [Read more](../reports/sharing-common-fields.md#journeyversionid-field)
* Additional examples on the evaluation criteria order have been added to the **Create decisions** section to illustrate cases where multiple criteria and multiple decision scopes are used. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* Decision management documentation has been clarified with a note specifying that the use of Object Level Access Control is not available for dynamic collections. [Read more](../offers/offer-library/creating-collections.md)

## May 2023 {#may-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] May '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added to describe how to set up the subdomain that will be used to publish content coming from the Adobe Experience Manager Assets Essentials in your web experiences. [Read more](../web/web-delegated-subdomains.md)
* A new subsection has been added to explain how to add personalized tracking parameters to URLs in the Email Designer. [Read more](../email/message-tracking.md#url-tracking)
* A new section has been added to describe how to ensure that the choice of your customers who opt out from having their profile data used for personalization is honored. [Read more](../privacy/opt-out.md#opt-out-personalization)
* A note has been added about using special international characters in URLs included in email contents. [Read more](../email/message-tracking.md#insert-links)
* The permission needed to test and publish landing pages has been added. [Read more](../landing-pages/create-lp.md)
* A note has been added about the Adobe Experience Platform endpoints needed to have your custom events accounted for in Decision management frequency capping. [Read more](../offers/data-collection/schema-requirement.md#track-custom-events)

## April 2023 {#apr-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] April '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A note has been added to specify that built-in actions cannot be removed. [Read more](../start/guardrails.md#custom-actions-g)
* Information has been added on serviceEvents as well as a query example to check the details of a serviceEvent. [Read more](../reports/query-examples.md#common-queries) 
* A note has been added to specify that you cannot perform queries on time series. [Read more](../building-journeys/conditions.md)
* Adobe Experience Manager Assets Essentials and Adobe Stock have been added to the multi-solution integration page. [Read more](../integrations/ajo-integrations.md)
* The warning on multi-level email subdomains not being allowed has been removed as they are now supported. [Read more](../configuration/delegate-subdomain.md)
* A note has been added to specify that, if changes are made to an offer decision which is being used in a journey's message, you need to unpublish the journey and republish it. [Read more](../building-journeys/publish-journey.md)
* Explanation on how to make sure events are correctly accounted for in the capping counter has been clarified in the Decision management **Capping event** section. [Read more](../offers/offer-library/add-constraints.md#capping-event)
* A new section has been added to the **Change execution addresses** page. It specifies that it is possible to override the execution field set globally in the journey advanced parameters, but the email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. [Read more](../configuration/primary-email-addresses.md#override-execution-address-journey)
* The **URL tracking** section now provides the list and description of all contextual attributes that can be set for URL tracking in an email channel configuration. [Read more](../email/email-settings.md#url-tracking)

## March 2023 {#march-2023}

* The Journey Optimizer schema dictionary is now available. You will find the complete list of fields and attributes for each schema.  [Read more](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=de)
* All new features and improvements coming with [!DNL Journey Optimizer] March '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a step to enable Adobe Analytics events in your journeys. [Read more](../event/about-analytics.md)
* A new section has been created in the Decision management guide on how to collect offer decisioning feedback in Adobe Experience Platform, including which offers are displayed and how users interact with them. [Read more](../offers/data-collection/data-collection.md)
* A new subsection has been added to the **Create decision** section to explain the difference between evaluating criteria in a sequential order or at the same time. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* A guardrail has been added for read audience journeys with incremental read. You cannot create a new version, you need to duplicate the journey. [Read more](../start/guardrails.md#journey-versions-g)
* The use case on how to limit throughput put has been updated with information on throttling capabilities. [Read more](../building-journeys/limit-throughput.md)
* A note has been added to specify that scalar arrays are not supported in response payload definition. [Read more](../datasource/external-data-sources.md)
* The section on profile cap conditions has been updated. [Read more](../building-journeys/conditions.md#profile_cap)

## February 2023 {#feb-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the canvas toolbar. [Read more](../building-journeys/using-the-journey-designer.md#gs-journey-design)
* Information has been added to state that internal Adobe addresses are not allowed in URLs and APIs. [Read more](../start/guardrails.md)
* A note has been added in the API-triggered campaigns documentation to specify that contextual attributes passed into the request cannot exceed 50kb. [Read more](../campaigns/api-triggered-campaigns.md#contextual)
* Information was added on how opt-out information is stored in the **Consent Service Dataset** after recipients are unsubscribed through a landing page. [Read more](../landing-pages/lp-use-cases.md#configure-opt-out)

## January 2023 {#jan-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added on custom authentication endpoints in the capping documentation. [Read more](../configuration/external-systems.md)
* A new custom authentication example has been added in the external datasources section. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* A note has been added about Data Collection Core Service (DCCS) for event-triggered journeys. [Read more](../start/guardrails.md#events-g)
* A note on identity namespace retrieval has been added in the [Read audience](../building-journeys/read-audience.md), [Audience qualification](../building-journeys/audience-qualification-events.md) and [Event creation](../event/about-creating.md) sections.
* Accessibility features in [!DNL Journey Optimizer] are now grouped in a dedicated page. [Read more](../start/accessibility.md)
* The examples have been updated in the Operators section of the advanced expression editor documentation. [Read more](../building-journeys/expression/operators.md)
* A note has been added about the limitation on lookup with array of objects. [Read more](../event/experience-event-schema.md#relationships_limitations)
* Added a new page about data management in [!DNL Journey Optimizer]. [Read more](../data/gs-data.md)
* Added a table listing all codes that can be returned in the response when delivering offers using the Decisioning API. [Read more](../offers/api-reference/offer-delivery-api/decisioning-api.md)

+++

+++ 2022

## December 2022 {#december-2022}

* The Messages guide has been reorganized and split into dedicated guides for each channel:

    * [Email channel](../email/get-started-email.md)
    * [Push notification channel](../../rp_landing_pages/push-landing-page.md)
    * [SMS channel](../mobile/get-started-mobile.md)

* The Configuration guide has been reorganized for improved readability. [Read more](../configuration/get-started-configuration.md)

## November 2022 {#november-2022}

* Added a new page about Journey Optimizer integrations. [Read more](../integrations/ajo-integrations.md)
* Added a recommendation about the length of mirror pages URLs. [Read more](../email/message-tracking.md)
* A new subsection in the email settings configuration has been added on the reply to email address, including recommendations to ensure proper reply management. [Read more](../email/email-settings.md#send-to-suppressed-email-addresses)
* Added a section on how to modify the content of a message in a live journey. [Read more](../building-journeys/journey-action.md#update-live-content)

## October 2022 {#october-2022}

* Added a journey use case on how to limit throughput using External Data Sources and Custom Actions. [Read more](../building-journeys/limit-throughput.md)
* The journey use case section has been reorganized into two categories: [Business use cases](../building-journeys/journeys-uc.md) and [Technical use cases](../building-journeys/collections.md).
* The **Entity Dataset** section has been updated with more details. [Read more](../data/datasets-query-examples.md#entity-dataset)
* The opt-out management and consent policies sections have been reorganized. [Read more](../privacy/opt-out.md)
* The section on advanced parameters in journey messages has been clarified and now specifies that email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. 
* Added a note to the **Configure landing page subdomains** section to specify that capital letters are not allowed in landing page subdomains. [Read more](../landing-pages/lp-subdomains.md)

## September 2022 {#september-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] September '22 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a best practice related to the use of wait activities in recurring read audience journeys. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added new step event query examples as well as information on the difference between id, instanceid and profileid. [Read more](../reports/query-examples.md).
* Updated the pages related to the [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly) and [toString](../building-journeys/functions/conversion-functions.md#toString) functions.
* Added details on the time condition parameters. [Read more](../building-journeys/conditions.md#time_condition)
* Added information on built-in datasets. [Read more](../data/get-started-datasets.md#access-datasets)
* The Global report and Live report sections have been improved and reorganized. [Read more](../reports/report-gs-cja.md)
* A list of every reporting metric available in Adobe Journey Optimizer has been added.
[Read more](../reports/report-gs-cja.md#email-and-sms-metrics)
* The BCC email section has been moved to the new Support for archiving page. [Read more](../configuration/archiving-support.md)

## August 2022 {#august-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] August '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The Frequency rules section has been updated to reflect the new in-line messaging flow.
* A video showing how to configure subscriptions and create landing pages is now referenced in the Get started with landing pages section. [Read more](../landing-pages/get-started-lp.md#video)
* A limitation has been added for journeys using Read Audience activities. [Read more](../building-journeys/read-audience.md)
* The expression editor operators page has been improved. [Read more](../building-journeys/expression/operators.md)
* A section on how to schedule a campaign has been added. [Read more](../campaigns/create-campaign.md)
* General syntax rules section for expression editor has been updated to take into account the new rule regarding the backslash symbol escaping in literal functions. The existing published messages are not impacted by this change. Only the new or draft messages must be updated. [Read more](../personalization/personalization-syntax.md#general-rules)

## July 2022 {#july-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] July '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Set up channel configurations** section has been clarified and updated with links to the page describing how to configure the SMS channel. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* In the journey properties, the **Profile Time zone** option is now disabled by default. [Read more](../building-journeys/timezone-management.md#timezone-from-profiles)
* In the **Wait** activity, the **Fixed date** option is no longer available. [Read more](../building-journeys/wait-activity.md)
* Added more information on the **Incremental read** option in the **Read audience** activity. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added recommendations on the **Profile cap** condition type. [Read more](../building-journeys/conditions.md#profile_cap)
* Added a limitation on business events. [Read more](../start/guardrails.md#events-g)

## June 2022 {#june-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] June '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new section about Privacy requests has been added to the documentation. [Read more](../privacy/requests.md)
* A new section about Audit logs on resources has been added to the documentation. [Read more](../privacy/audit-logs.md)
* A new section about how to add HTML or JSON content coming from Adobe Experience Cloud Asset library to an offer representation has been added to the documentation. [Read more](../offers/offer-library/add-representations.md#html-json)
* Added a new page on journey lifecyle. [Read more](../building-journeys/journey.md)
* Updated the Wait activity page. [Read more](../building-journeys/wait-activity.md)
* Added the list of Adobe Journey Optimizer datasets with query examples. [Read more](../data/datasets-query-examples.md)
* The Allowed list page has been moved to the Configuration section. [Read more](../configuration/allow-list.md)
* The Suppression list page has been updated to clarify some information, including the fact that all ASCII characters comprised between 32 and 126 are allowed in the reason for suppression field. [Read more](../configuration/manage-suppression-list.md)
* The link to guardrails and static limits for Decision management has been added. [Read more](../start/guardrails.md)
* Send-Time Optimization is now available for all customers. The beta mention has been removed. [Read more](../building-journeys/send-time-optimization.md)
* The Batch Decisioning API has been added to the list of available APIs to delivery personalized offers. [Read more](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## May 2022 {#may-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] May '22 release have been detailed in the documentation. [Read more](release-notes.md)
* New query examples related to [audience qualification](../reports/query-examples.md#segment-qualification-queries) and [events](../reports/query-examples.md#event-based-queries) have been added.
* The email design section now mentions new built-in templates available to start content with. Related screenshots have been updated. [Read more](../email/get-started-email-design.md)
* Links to key resources have been updated in Journey Optimizer documentation home page.
* Screenshots for landing page and subscription reporting have been updated. [Read more](../reports/live-report.md)
* A note has been added stating that the Delete method is not supported in custom actions. [Read more](../action/about-custom-action-configuration.md)
* Links to how-to videos have been updated.
* The [Email configuration](../configuration/about-subdomain-delegation.md), [Message presets](../configuration/channel-surfaces.md) and [Configure landing pages](../landing-pages/lp-subdomains.md) sections have been reorganized for improved readability.
* The URL tracking section has been updated and improved with examples. [Read more](../email/email-settings.md#url-tracking)
* A new subsection on setting up a forward email address has been added. Note that you cannot do it through the user interface. [Read more](../email/email-settings.md#email-settings)

## April 2022 {#april-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] April '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **reactions** event documentation page has been updated. [Read more](../building-journeys/reaction-events.md)
* Videos for Decision management capabilities have been updated to reflect Journey Optimizer user interface. [Read more](../offers/get-started/starting-offer-decisioning.md)
* The **Get Started with Datasets** section has been improved to detail how to access and create datasets. [Read more](../data/get-started-datasets.md)
* Links to help guides and product release notes have been added to the **Adobe Journey Optimizer Documentation** home page. [Read more](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=de)
* The **Create message presets** section now specifies that you cannot proceed with preset creation while the selected IP pool is under edition (**[!UICONTROL Processing]** status) and has never been associated with the selected subdomain. [Read more](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* The message presets **URL tracking** section has been updated to reflect minor changes in the user interface. [Read more](../configuration/channel-surfaces.md#url-tracking)

## March 2022 {#march-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] March '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page on getting started with AI models has been added to the **Offer decisioning** section, including a thorough description of the [auto-optimization model](../offers/ranking/auto-optimization-model.md), the algorithm it uses and more technical details. [Read more](../offers/ranking/ai-models.md)
* The test profile creation page has been moved to the  **Audience, profiles and identity** section. [Read more](../audience/creating-test-profiles.md)
* Added an example on how to add an expression as a default value in the expression editor. [Read more](../building-journeys/expression/field-references.md#default-value)
* The **Create personalized offers** section has been reorganized for improved readability. [Read more](../offers/offer-library/creating-personalized-offers.md)
* A new section has been added to describe the impacts that changing an offer's start and/or end dates may have on this offer's frequency capping. [Read more](../offers/offer-library/add-constraints.md#capping-change-date)
* The **Change the primary email addresses** section has been updated to reflect the user interface changes. [Read more](../configuration/primary-email-addresses.md)

## February 2022 {#feb-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The [replace](../building-journeys/functions/string-functions.md#replace) and [replaceAll](../building-journeys/functions/string-functions.md#replaceAll) function documentation pages have been updated with additional information and examples regarding the target parameter.
* Best practices have been added to the [Operators](../building-journeys/expression/operators.md#important-notes) page.

## January 2022 {#january-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Offer decisioning AI rankings** section has been updated with a more detailed description of the auto-optimization model. [Read more](../offers/ranking/auto-optimization-model.md)
* A new section on the schema requirements needed to be able to send in event types when using an AI model has been added. [Read more](../offers/data-collection/schema-requirement.md)
* The section related to [!DNL Journey Optimizer] personalization capabilities has been reorganized for better readability. [Read more](../personalization/personalize.md)
* The **Create message presets** section has been divided into several sections for improved clarity. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* The **Opt-out management** section has been clarified and slightly reorganized. [Read more](../privacy/opt-out.md#opt-out-decision-management)
* The **Insert links** section has been updated to reflect the recent user interface changes. [Read more](../email/message-tracking.md#insert-links)

+++

+++ 2021

## November 2021 {#november-2021}

* A full description of the **advanced expression editor** used in journeys is now available. [Read more](../building-journeys/expression/expressionadvanced.md)
* A new section about **CNAME subdomain delegation method** has been added. [Read more](../configuration/delegate-subdomain.md#cname-subdomain-setup)

## October 2021 {#october-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] Oct '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added **Date time function** list. [Read more](../personalization/functions/dates.md)
* New **Get Started sections per user persona**. Take your own path to get to your goals faster! [Read more](../start/quick-start.md)
* New **Edit a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New **Edit a PTR record** section. [Read more](../configuration/ptr-records.md#edit-ptr-record)
* New **Deactivate a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New limitations added to the **Decision Management API developer guide** on offer constraints not supported with the mobile [!DNL Experience Edge] workflows. [Read more](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* New **Create simulations** section. [Read more](../offers/offer-activities/simulation.md)
* Updated **Add decision scopes** section. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Updated **Define content for your representations** section, including a new [subsection](../offers/offer-library/creating-personalized-offers.md#custom-text) on how to define and personalize custom text. [Read more](../offers/offer-library/creating-personalized-offers.md#content)

## September 2021 {#september-2021}

* The following function pages have been updated: [sethours](../building-journeys/functions/date-functions.md#setHours), [getListItem](../building-journeys/functions/list-functions.md#getListItem), [inSegment](../building-journeys/functions/functioninaudience.md)

* The following functions have been added: [filter](../building-journeys/functions/list-functions.md#filter), [intersect](../building-journeys/functions/list-functions.md#intersect), [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly)

* The dateOnly date type has been added in the expression editor documentation. [Read more](../building-journeys/expression/data-types.md)

* Added details on custom action cache duration. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)

* Added information on custom action default ports. [Read more](../action/about-custom-action-configuration.md#url-configuration)

* Added information on multiple business event use cases. [Read more](../event/about-creating-business.md#multiple-business-events)

* Added commonly used examples to query Journey Step Events in Data Lake. [Read more](../reports/query-examples.md)

* Added a new **Limitations** page. [Read more](../start/guardrails.md)

* Improved the **Quick start** page with steps for different personas. [Read more](../start/quick-start.md)

* Now all the Decision management features described in the dedicated section also apply to the Adobe Experience Platform users leveraging the Offer Decisioning application. [Read more](../offers/get-started/starting-offer-decisioning.md)

* Added a subsection to clarify the differences between using audiences versus decision rules when applying a constraint to restrict the selection of offers for a given placement. [Read more](../offers/offer-activities/create-offer-activities.md#decision-list)

* Added specific ranking formula examples to illustrate some real-life use cases. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Added a subsection on how to edit IP pools. [Read more](../configuration/ip-pools.md#edit-ip-pool)

## August 2021 {#august-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] August '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Updated Decision management permissions. [Read more](../administration/ootb-product-profiles.md)
* Updated Email Designer screenshots with latest UI.
* Updated the configuration procedure for custom actions with dynamic URL paths and dynamic headers. [Read more](../action/about-custom-action-configuration.md#url-configuration)
* Added a section about accessibility features and shortcuts. [Read more](../start/user-interface.md#accessibility)
* Added a section about audience evaluation methods. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* Added notes to the Suppression list, Allowed list and Email global/live report sections to specify that profiles with Suppressed and Not allowed statuses are excluded from the Email report Sent metrics. [Read more](../reports/report-gs-cja.md)
* Added a new section to describe how to retrieve email addresses or domains that were excluded from a sending because they were not on the allowed list. [Read more](../configuration/allow-list.md#reporting)
* Updated the Enable the allow list section. [Learn more](../configuration/allow-list.md#enable-allow-list)
* Updated the Monitor message presets section with the possible preset creation failure reasons and details on such errors. [Read more](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Updated and renamed the Retry time period section to reflect the fact that you can now adjust the email retry setting in the message presets. [Read more](../configuration/retries.md#retry-duration)
* Updated the Delegate a subdomain section with more detailed information on the validation process performed by Adobe. [Read more](../configuration/delegate-subdomain.md#subdomain-validation)
* Added a section to describe how to manually add email addresses and domains to the suppression list. [Read more](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Updated the [Access the suppression list](../configuration/manage-suppression-list.md#access-suppression-list) section and [Retries](../configuration/retries.md) sections to reflect the new user interface.
* The new flow to add and configure representations when creating an offer has been documented. [Read more](../offers/offer-library/creating-personalized-offers.md#representations)

## July 2021 {#july-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] July '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added direct links to Experience Platform services documentation in [!DNL Journey Optimizer] home page and table of contents
* New landing pages for Experience Platform services available in [!DNL Journey Optimizer] 
* Added links to [!DNL Journey Optimizer] product description in the home page
* Added tutorial videos in multiple pages
* Optimized home page imagery
* Moved, improved and renamed 'Message tracking' section to 'Add links and track messages'. [Read more](../email/message-tracking.md)
* Added a subsection on mirror pages. [Read more](../email/message-tracking.md#mirror-page)
* Renamed 'offer activities' as 'decisions' and 'decisions' as 'decision scopes' in documentation and screens. [Read more](../offers/get-started/starting-offer-decisioning.md)
* New use case: [personalize a message with helper functions](../personalization/personalization-use-case-helper-functions.md)
* Updated the Read audience documentation to reflect materialized segment impacts. [Read more](../building-journeys/read-audience.md)
* Updated the Journey limitations. [Read more](../start/guardrails.md)
* Updated the Configure offers selection in decisions section. [Read more](../offers/offer-activities/configure-offer-selection.md)
* Added a warning to mention that event-based offers are not currently supported. [Read more](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Documented the Decision management new **[!UICONTROL Overview]** tab. [Read more](../offers/get-started/user-interface.md#overview)
* Added new sections to describe the actions available from the offer and decision lists: [Offer list](../offers/offer-library/creating-personalized-offers.md#offer-list) and [Decision list](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
-->

