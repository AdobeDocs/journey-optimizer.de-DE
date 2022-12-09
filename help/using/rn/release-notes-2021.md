---
solution: Journey Optimizer
product: journey optimizer
title: Frühere Versionshinweise (2021)
description: Versionshinweise zu Journey Optimizer 2021
exl-id: 0e43be98-f471-4860-be84-8f99ab93e983
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '2077'
ht-degree: 0%

---

# Versionshinweise 2021 {#release-notes-2021}

Auf dieser Seite werden alle Funktionen und Verbesserungen für [!DNL Journey Optimizer] veröffentlicht im Jahr 2021.


## Version November 2021 {#november-2021-release}

<table>
<thead>
<tr>
<th><strong>CNAME-Subdomain-Zuweisung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer unterstützt jetzt CNAMEs. Ein CNAME oder Canonical Name-Datensatz ist ein Datensatz, der auf eine andere Domain-Adresse und nicht auf eine IP-Adresse verweist. Mit der Subdomain-Zuweisung von CNAME können Sie eine Subdomain erstellen und CNAMEs verwenden, um auf Adobe-spezifische Datensätze zu verweisen. Mit dieser Konfiguration sind Sie und Adobe gemeinsam für die Pflege des DNS verantwortlich, um eine Umgebung zum Senden, Rendern und Tracking von E-Mails einzurichten.</p>
<p>Diese Methode wird empfohlen, wenn die Richtlinien Ihres Unternehmens die Methode der vollständigen Subdomain-Zuweisung einschränken.</p>
<p>Erfahren Sie mehr über die Zuweisung von CNAME-Subdomains im <a href="../configuration/delegate-subdomain.md#cname-subdomain-delegation">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


## Version Oktober 2021 {#oct-2021-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Entscheidungsmanagement - Angebotssimulation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt simulieren, welche Angebote an ein Testprofil für eine bestimmte Platzierung in der Benutzeroberfläche von Journey Optimizer gesendet werden. Auf diese Weise können Sie Ihre Entscheidungslogik einschließlich Eignungsbegrenzungen und Rangalgorithmen einfach validieren, bevor Sie sie in die Produktion übernehmen. Diese Funktion ermöglicht es nichttechnischen und technischen Benutzern, die Entscheidungsverwaltung schnell zu testen und potenzielle Probleme zu beheben.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../offers/offer-activities/simulation.md">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Entscheidungsverwaltung - Personalisieren von Angeboten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt den Inhalt Ihrer Angebote mit Adobe Experience Platform-Profilattributen und -segmenten personalisieren, indem Sie dieselbe Ausdruckseditor-Komponente verwenden, die Sie in der Benutzeroberfläche von Journey Optimizer finden. </p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../offers/offer-library/creating-personalized-offers.md#custom-text">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


Siehe auch [Adobe Experience Platform - Versionshinweise Oktober](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html){target=&quot;_blank&quot;} für weitere Änderungen.

### Verbesserungen

**Journeys**

* **Ausdruckseditor** - Als Power User können Sie jetzt Funktionen verwenden, um mit Karten zu arbeiten. Diese Funktion kann mit den Abonnementlisten genutzt werden. Beispielsweise können Sie aus einem Segment jetzt eine E-Mail-Adresse aus einer Abonnementliste abrufen. [Weitere Informationen finden Sie in diesem Beispiel](../building-journeys/message-to-subscribers-uc.md)

* **Überwachung** - Schrittereignisse für Live-Journeys und Testmodus wurden verbessert. [Neue Felder](../reports/sharing-field-list.md#serviceevents) wurden im Zusammenhang mit Profilexportaufträgen hinzugefügt. Für ein besseres Benutzererlebnis sind die Felder für Schrittereignisse jetzt in verschiedenen Kategorien organisiert. Alle Felder für vorhergehende Schrittereignisse sind weiterhin im [stepEvents](../reports/sharing-legacy-fields.md) Kategorie.
* **Zugänglichkeit** - In Journeys wurden Verbesserungen an der Barrierefreiheit implementiert.
* **Sammlungen** - Arrays von Objekten, die Unterobjekte enthalten, werden jetzt unterstützt. [Mehr dazu](../building-journeys/collections.md)
* **Listen** - Die Bildschirme &quot;Listen&quot;wurden für Journeys, Ereignisse, Aktionen und Datenquellen verbessert.

**Berichterstellung**

* **Datenformat in der globalen Ansicht** - Sie können jetzt zwischen Zahlen und Prozentsätzen im **Globale Ansicht** des **Ausführung** Registerkarte.


**Administration**

* **Bearbeiten von Nachrichtenvorgaben** - Sie können jetzt Nachrichtenvorgaben bearbeiten und ihren Aktualisierungsstatus überwachen. [Weitere Infos](../configuration/channel-surfaces.md#edit-channel-surface)
* **PTR-Datensätze bearbeiten** - Sie können jetzt PTR-Einträge bearbeiten und ihren Aktualisierungsstatus überwachen. [Weitere Infos](../configuration/ptr-records.md#edit-ptr-record)

**Personalisierung**

* **Neue Hilfsfunktion für die Datumsformatierung** - Sie können jetzt angeben, wie eine Datums-Zeichenfolge dargestellt werden soll. [Weitere Infos](../personalization/functions/dates.md#format-date)


**Entscheidungsverwaltung**

* **Auswertungssequenzierung** - Mit dem neuen und verbesserten Entscheidungsfluss können Sie nicht nur nahtloser zwischen Entscheidungsobjekten navigieren, sondern auch vollständig steuern, wie Angebotskollektionen von der Entscheidungs-Engine bewertet werden. Dazu gehört, welche Sammlungen gemeinsam oder getrennt bewertet werden und in welcher Reihenfolge die Sammlungen bewertet werden sollen. [Weitere Infos](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### Fehlerbehebungen

* Fehlerkorrektur - Liste der Journeys, Nachrichtenliste und E-Mail-Designer werden jetzt angezeigt, wenn die Browsersprache nicht Englisch ist.
* Fehlerkorrektur - Beim Hinzufügen einer Personalisierung mithilfe eines Ausdrucks im E-Mail-Designer tritt kein Syntaxfehler mehr auf: Zeichen fehlerhaft maskiert wurden.
* Fehlerkorrektur - Beim Navigieren im **Administration** Menü.
* Es wurde ein Problem behoben, das andere Live-Journeys beim Testen einer Journey mit einem Geschäftsereignis ausgelöst hat.


## Version September 2021 {#september-2021-release}

### Neue Funktionen

<table>
<thead>
<tr>

<th><strong>Reporting - Bessere Einblicke in die Zielgruppe</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Neue Metriken sind in Berichten verfügbar: Targeting und Ausgeschlossen für E-Mail- und Push-Nachrichten sind sowohl in Live- als auch in globalen Berichten sichtbar. </br> Um Zugriff auf die neuesten Metriken zu erhalten, müssen Sie die verschiedenen Berichts-Dashboards für jeden Kanal und Berichtstyp zurücksetzen. Weiterführende Informationen zur Dashboard-Anpassung finden Sie im Abschnitt <a href="../reports/live-report.md">ausführliche Dokumentation.</a></p>
<p>Eine neue Spalte in der Ausführungsliste der Nachricht zeigt die Anzahl der Zielgruppenprofile für jede Nachrichtenausführung an. </p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../reports/global-report.md">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Dynamisches Übergeben von Datenlisten mithilfe benutzerdefinierter Aktionen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Sammlungen oder eine Liste von Daten in Ihren benutzerdefinierten Aktionsparametern übergeben, die zur Laufzeit dynamisch gefüllt werden. Es werden zwei Arten von Sammlungen unterstützt: einfache Sammlungen und Objektsammlungen. Zuvor erstellte benutzerdefinierte Aktionen funktionieren weiterhin. </p>
<p>Weiterführende Informationen zu Kollektionen finden Sie im Abschnitt <a href="../building-journeys/collections.md">Detaillierte Dokumentation</a>. </p>
<p>Die Filter- und Schnittfunktionen wurden der Liste der im erweiterten Ausdruckseditor verfügbaren Funktionen hinzugefügt. Dies bietet mehr Möglichkeiten zum Filtern und Vergleichen von Kollektionen.</p>
<p>Lesen Sie die Dokumentation im Abschnitt <a href="../building-journeys/functions/functionfilter.md">filter</a> und <a href="../building-journeys/functions/functionintersect.md">Schnittmenge</a> Funktionen.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journeys**

* Systemgenerierte Schemata und Datensätze, die während der Bereitstellung von Schrittereignissen erstellt wurden, befinden sich jetzt im schreibgeschützten Modus, um unbeabsichtigte Änderungen an kritischen Schemas zu vermeiden. [Weitere Infos](../reports/sharing-overview.md)
* Klare Beschriftung **Warten** -Aktivität mit einem Titel, der auf der Arbeitsfläche angezeigt wird. Die Bezeichnung wird auch in Berichts- und Testmodusprotokollen verwendet, um eindeutig zu identifizieren, was Sie tun. [Weitere Infos](../building-journeys/about-journey-activities.md#best-practices)
* Schnellere Suche nach Ereignissen und Aktionen durch Filtern von Elementen in **Veranstaltungen** und **Aktion** Kategorien mithilfe der Suche. Orchestrierungsaktivitäten werden nicht mehr gefiltert. [Weitere Infos](../building-journeys/using-the-journey-designer.md)
* Beim Definieren einer Ereignis-ID-Bedingung in einem regelbasierten oder geschäftlichen Ereignis ist jetzt der Operator &quot;enthält&quot;für Feldzeichenfolgen-Typen verfügbar. [Weitere Infos](../event/about-creating.md)

**E-Mail-Konfiguration**

* Wenn ein IP-Pool mit einer Nachrichtenvorgabe verknüpft wurde, können Sie sie jetzt bearbeiten, wobei die Aktualisierung asynchron erfolgt. Sie können auch den Status jedes IP-Pool-Updates überprüfen. [Weitere Infos](../configuration/ip-pools.md#edit-ip-pool)


## Version August 2021 {#august-2021-release}

### Neue Funktionen

<table>
<thead>
<tr>

<th><strong>Senden von Nachrichten zur besten Zeit - Sendezeitoptimierung</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Senden Sie Ihre Push- oder E-Mail-Benachrichtigung automatisch zum besten Zeitpunkt für jeden Kunden, den Sie mit Adobe Journey Optimizer verbinden. Die Sendezeitoptimierung basiert auf den KI-Diensten von Adobe und sagt die beste Zeit für den Versand einer E-Mail- oder Push-Nachricht voraus, um die Interaktion basierend auf historischen Öffnungs- und Klickraten nativ zu maximieren.</p>
<p>Diese Funktion befindet sich derzeit in der Betaversion und steht nur Beta-Kunden zur Verfügung. Wenden Sie sich an die Adobe-Kundenunterstützung, um am Betaprogramm teilzunehmen.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../building-journeys/journeys-message.md#send-time-optimization">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Nutzen von Schemabeziehungen in Geschäftsereignissen - Verwaltung von Suchtabellen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt beim Konfigurieren von Geschäftsereignissen Beziehungen zwischen Schemas nutzen. Dies bietet zusätzlich die Möglichkeit, Felder aus verknüpften Tabellen beim Konfigurieren eines einheitlichen Ereignisses, bei der Verwendung von Bedingungen in einer Journey, bei der Nachrichtenpersonalisierung und bei der Personalisierung benutzerdefinierter Aktionen zu nutzen.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../event/experience-event-schema.md#leverage_schema_relationships">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Personalisierte URLs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Personalisierte URLs führen Empfänger je nach Profilattributen zu bestimmten Seiten einer Website oder zu einer personalisierten Microsite. In Adobe Journey Optimizer können Sie URLs in Ihrem Nachrichteninhalt jetzt Personalisierung hinzufügen. Die URL-Personalisierung kann auf Text und Bilder angewendet werden und Profildaten oder Kontextdaten verwenden.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../personalization/personalization-syntax.md#perso-urls">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Stellen Sie sicher, dass Ihre E-Mails an Ihre Benutzer gesendet werden - E-Mail erneut versenden</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt den Wiederholungszeitraum pro Voreinstellung definieren, um sicherzustellen, dass Wiederholungsversuche nicht mehr ausgeführt werden, wenn sie nicht mehr benötigt werden. Beispielsweise können Sie die Wiederholungsdauer für eine Transaktionsnachricht zum Zurücksetzen des Kennworts, die einen nur für einen Tag gültigen Link enthält, auf 24 Stunden festlegen. Beachten Sie, dass Wiederholungseinstellungen nur für den E-Mail-Kanal gelten.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../configuration/retries.md#retry-duration">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Definieren der vom Versand auszuschließenden Adressen - Unterdrückungsliste</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Das Hinzufügen von E-Mail-Adressen und Domänen zur Unterdrückungsliste ist jetzt in der Benutzeroberfläche entweder einzeln im Bulk-Modus durch einen CSV-Datei-Upload verfügbar.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


### Verbesserungen

**Journeys**

* **Dynamische Header** - Sie können jetzt dynamische Daten in HTTP-Header-Parametern übergeben. Diese Parameter können von den Integrationssystemen verwendet werden, die die HTTP-Aufrufe der Journey-Aktion empfangen, z. B. Zeitstempel oder Tracking-ID. [Weitere Infos](../action/about-custom-action-configuration.md#url-configuration)
* **Dynamische URL-Pfade** - Sie können jetzt dynamische URL-Pfade für benutzerdefinierte Aktionen einrichten. [Weitere Infos](../action/about-custom-action-configuration.md#url-configuration)
* Die Gesamtdrosselungsrate für Lesesegmente wurde von 17.000 auf 20.000 Nachrichten pro Sekunde geändert. [Weitere Infos](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Benutzeroberfläche**

* **Suche** - Auf jeder Seite können Sie jetzt Geschäftsobjekte und Hilferessourcen direkt aus dem einheitlichen Experience Cloud-Suchfeld durchsuchen. [Weitere Infos](../start/user-interface.md#unified-search)
* **Letzte** - Die Anzeige der neuesten Elemente von der Startseite von Adobe Journey Optimizer wurde jetzt auf zusätzliche Geschäftsobjekte erweitert. Mit diesem Update umfassen die kürzlich aufgerufenen Verknüpfungen Nachrichten, Journeys, Segmente, Schemas, Datensätze, Datenquellen, Ereignisse, Aktionen, Quellen und Ziele. [Weitere Infos](../action/about-custom-action-configuration.md#passing-collection)

**Inhaltserstellung**

* **Hintergrund** - Hintergrundbilder werden jetzt in der Live-Vorschau unterstützt. [Weitere Infos](../email/preview.md)
* **Ausschluss-Link mit einem Klick** - Sie können einen neuen Link-Typ in Ihren E-Mail-Inhalt einfügen: die **Opt-out** -Link ermöglicht es Benutzern, sich von der Abmeldung in nur einem Klick abzumelden, ohne zu einer Landingpage weitergeleitet zu werden, um die Abmeldung zu bestätigen. [Weitere Infos](../privacy/opt-out.md#one-click-opt-out-link)

**Personalisierung**

* **Ausdruckseditor** - Sie können jetzt beim Definieren der Personalisierung einfach einen Fallback-Wert hinzufügen: Wenn das Personalisierungsfeld für ein Profil leer ist, wird der Fallback-Wert angezeigt. [Weitere Infos](../personalization/functions/helpers.md)

**E-Mail-Konfiguration**

* **Zulässige Liste** - Die Zulassungsliste kann jetzt über einen API-Aufruf in einer Nicht-Produktions-Sandbox aktiviert und deaktiviert werden. [Weitere Infos](../configuration/allow-list.md#enable-allow-list)
* **Navigation** - die Unterdrückungsliste, auf die unter der **Administration > Kanäle > E-Mail-Konfiguration > Allgemein** wurde in das neue **Unterdrückungsliste** -Untermenü, das alle zugehörigen Funktionen für einen leichteren Zugriff erfasst. [Weitere Infos](../configuration/manage-suppression-list.md#access-suppression-list)

**Entscheidungsmanagement**

* Die Art und Weise, wie Sie beim Erstellen eines Angebots Darstellungen hinzufügen und konfigurieren, wurde aktualisiert, um das Benutzererlebnis zu verbessern. Insbesondere wird die Asset-Bibliothek jetzt nur angezeigt, wenn Sie Bildinhalte für eine Darstellung definieren. [Weitere Infos](../offers/offer-library/creating-personalized-offers.md#representations)

### Fehlerbehebungen

* Es wurde ein Problem mit der Barrierefreiheit in der Navigation auf der Meldungsregisterkarte behoben.
* Es wurde ein Lokalisierungsproblem in den E-Mail-Designer-Bezeichnungen behoben.
* Es wurde ein Problem behoben, das beim Auswählen von mehr als einem Knoten in einer Journey und Klicken auf &quot;Löschen&quot;im Eigenschaftenbereich auftrat.
* Es wurde ein Problem behoben, das das Hinzufügen einer neuen Kopfzeile zu einer in einer Journey verwendeten Aktion verhinderte.
* Sie können jetzt durch eine präzisere Warnung in der Benutzeroberfläche feststellen, warum die Erstellung einer Nachrichtenvorgabe fehlgeschlagen ist.


## Version Juli 2021 {#july-2021-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Verwenden von Metadaten in Ihren Nachrichten - Verwaltung von Suchtabellen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Reichern Sie Ihre Erlebnisse mit Referenzdaten an, die Sie in Journey Optimizer geladen haben. Beispiele sind das Suchen von Metadaten für eine Reservierungs-ID in einem Erlebnisereignis oder das Suchen von Produktinformationen aus einer SKU in einem Erlebnisereignis zur Verwendung auf der Arbeitsfläche. </p>
<p>Sie können jetzt Beziehungen zwischen Schemas nutzen, um einen Datensatz als Lookup-Tabelle für einen anderen zu verwenden. Sie können dann alle Felder aus den verknüpften Tabellen bei der Konfiguration eines einheitlichen Ereignisses, bei der Verwendung von Bedingungen in einer Journey, bei der Nachrichtenpersonalisierung und bei der Personalisierung benutzerdefinierter Aktionen nutzen.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../event/experience-event-schema.md#leverage_schema_relationships">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Zulässige Liste</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt eine spezifische Liste für den Versand auf Sandbox-Ebene definieren, um eine sichere Umgebung für Testzwecke zu erhalten. Auf einer Nicht-Produktionsinstanz, bei der Fehler auftreten können, stellt die Zulassungsliste sicher, dass Sie kein Risiko haben, unerwünschte Nachrichten an Ihre Kunden zu senden. Diese Funktion wird durch die Verwendung von Unterdrückungs-APIs aktiviert.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../configuration/allow-list.md">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journeys**

* Die Gesamtdrosselungsrate aller Lesesegmente, die gleichzeitig in derselben Sandbox ausgeführt werden, ist auf 17.000 Nachrichten pro Sekunde beschränkt. [Mehr dazu](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Die **Aufbewahrungsfrist im Cache** -Feld wurde aus dem Konfigurationsbereich der Datenquelle entfernt. [Mehr dazu](../datasource/about-data-sources.md)
* Für externe Datenquellen wird jetzt automatisch eine Begrenzungsregel von 15 Aufrufen pro Sekunde definiert. [Mehr dazu](../configuration/external-systems.md#capping)
* Für Live-Journeys zeigt der Bildschirm &quot;Journey-Eigenschaften&quot;jetzt das Veröffentlichungsdatum und den Namen des Benutzers an, der die Journey veröffentlicht hat. [Mehr dazu](../building-journeys/journey-gs.md#change-properties)
* Im Bildschirm der Journey-Liste wurde der Filter für den Journey-Typ hinzugefügt. [Mehr dazu](../start/user-interface.md#filter-lists)
* Die **[!UICONTROL Throttling rate]** wurde in der Aktivität Segment lesen hinzugefügt. [Mehr dazu](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Vorschau und Test**

* Identität und Namespace sind jetzt im **[!UICONTROL Preview]** angezeigt. [Mehr dazu](../email/preview.md#preview-your-messages)
* Die Anzahl der Test-E-Mails für Testsendungen ist jetzt auf 10 beschränkt.
* Für die Variable **Betreffpräfix** in Testsendungen sind nun begrenzt. [Mehr dazu](../email/preview.md#send-proofs)

**Ausdruckseditor für Personalisierung**

* Die Dropdownliste &quot;Helper&quot;wurde umbenannt und neu angeordnet.

### Fehlerbehebungen

* Fehlerkorrektur - Jetzt werden keine doppelten Nachrichten mehr für den Batch-E-Mail-Versand gesendet.
* Ereignisse werden jetzt entsprechend generiert, wenn nach Ablauf des Wiederholungszeitraums kein E-Mail-Versand mehr durchgeführt wird.
* Es wurde ein Problem behoben, bei dem IP-Informationen im Bildschirm &quot;PTR-Datensätze&quot;fehlten.
* Die Lokalisierung in der Angebotsleiste im Ausdruckseditor ist jetzt implementiert.
* Es wurde ein falscher Abstand in Informations-Popups korrigiert.
* Fehlerkorrektur - Beim Hochladen einer HTML-Datei tritt in E-Mail-Designer kein Problem mehr auf, bei dem das interne Stylesheet mit `background-image` -Eigenschaft nicht unterstützt.
