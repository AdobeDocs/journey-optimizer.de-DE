---
solution: Journey Optimizer
product: journey optimizer
title: Frühere Versionshinweise( 2021)
description: Versionshinweise zu Journey Optimizer 2021
exl-id: 0e43be98-f471-4860-be84-8f99ab93e983
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: ht
source-wordcount: '2068'
ht-degree: 100%

---

# Versionshinweise 2021 {#release-notes-2021}

Auf dieser Seite sind alle Funktionen und Verbesserungen für [!DNL Journey Optimizer] aufgeführt, die im Jahr 2021 veröffentlicht wurden.


## Version vom November 2021 {#november-2021-release}

<table>
<thead>
<tr>
<th><strong>CNAME-Subdomain-Delegierung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer unterstützt jetzt CNAMEs. Ein CNAME-Eintrag bzw. Eintrag mit kanonischem Namen ist ein Eintrag, der auf eine andere Domain-Adresse und nicht auf eine IP-Adresse verweist. Mit der CNAME-Subdomain-Delegierung können Sie eine Subdomain erstellen und CNAMEs verwenden, um auf Adobe-spezifische Einträge zu verweisen. Mit dieser Konfiguration sind Sie und Adobe gemeinsam für die Pflege des DNS verantwortlich, um eine Umgebung für das Senden, Rendern und Tracking von E-Mails einzurichten.</p>
<p>Diese Methode wird empfohlen, wenn Ihre Unternehmensrichtlinien die vollständige Subdomain-Delegierung nicht erlauben.</p>
<p>Weitere Informationen zur Delegierung von CNAME-Subdomains erhalten Sie in der <a href="../configuration/delegate-subdomain.md#cname-subdomain-delegation">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


## Version Oktober 2021 {#oct-2021-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Entscheidungs-Management – Angebotssimulation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt simulieren, welche Angebote an ein Testprofil für eine bestimmte Platzierung in der Journey Optimizer-Benutzeroberfläche gesendet werden. Auf diese Weise können Sie Ihre Entscheidungslogik einschließlich Eignungsbegrenzungen und Ranking-Algorithmen einfach validieren, bevor Sie sie in die Produktion übernehmen. Mit dieser Funktion können technisch versierte ebenso wie technisch nicht versierte Benutzende das Entscheidungs-Management schnell testen und potenzielle Probleme beheben.</p>
<p>Weitere Informationen finden Sie in der <a href="../offers/offer-activities/simulation.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Entscheidungs-Management – Personalisieren von Angeboten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt den Inhalt Ihrer Angebote mit Profilattributen und Segmenten von Adobe Experience Platform personalisieren, indem Sie die Ausdruckseditor-Komponente in der Journey Optimizer-Benutzeroberfläche verwenden. </p>
<p>Weitere Informationen finden Sie in der <a href="../offers/offer-library/creating-personalized-offers.md#custom-text">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


Siehe auch [Adobe Experience Platform – Versionshinweise Oktober](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html?lang=de){target="_blank"} für weitere Änderungen.

### Verbesserungen

**Journeys**

* **Ausdruckseditor** – Als Power User können Sie jetzt Funktionen verwenden, um mit Karten zu arbeiten. Diese Funktion kann mit den Abonnement-Listen genutzt werden. Beispielsweise können Sie jetzt in einem Segment eine E-Mail-Adresse aus einer Abonnement-Liste abrufen. [In diesem Beispiel erfahren Sie mehr](../building-journeys/message-to-subscribers-uc.md).

* **Monitoring** – Step-Ereignisse für Live-Journeys und den Testmodus wurden verbessert. Es wurden [neue Felder](../reports/sharing-field-list.md#serviceevents) im Zusammenhang mit Profilexportvorgängen hinzugefügt. Für ein besseres Benutzererlebnis sind die Felder für Step-Ereignisse jetzt in verschiedenen Kategorien organisiert. Alle Felder für vorhergehende Step-Ereignisse sind weiterhin in der Kategorie [stepEvents](../reports/sharing-legacy-fields.md) verfügbar.
* **Barrierefreiheit** – Es wurden Verbesserungen an der Barrierefreiheit von Journeys implementiert.
* **Sammlungen** – Arrays von Objekten, die Unterobjekte enthalten, werden nun unterstützt. [Weitere Informationen](../building-journeys/collections.md)
* **Listen** – Die Bildschirme „Listen“ für Journeys, Ereignisse, Aktionen und Datenquellen wurden verbessert.

**Reporting**

* **Datenformat in der globalen Ansicht**: Sie können jetzt in der **globalen Ansicht** der Registerkarte **Ausführung** zwischen Zahlen und Prozentsätzen hin- und herschalten.


**Administration**

* **Bearbeiten von Nachrichtenvoreinstellungen** – Sie können jetzt Nachrichtenvoreinstellungen bearbeiten und ihren Aktualisierungsstatus überwachen. [Weitere Informationen](../configuration/channel-surfaces.md#edit-channel-surface)
* **PTR-Datensätze bearbeiten** – Sie können jetzt PTR-Einträge bearbeiten und ihren Aktualisierungsstatus überwachen. [Weitere Informationen](../configuration/ptr-records.md#edit-ptr-record)

**Personalisierung**

* **Neue Hilfsfunktion für die Datumsformatierung** – Sie können jetzt angeben, wie eine Datums-Zeichenfolge dargestellt werden soll. [Weitere Informationen](../personalization/functions/dates.md#format-date)


**Entscheidungs-Management**

* **Auswertungssequenzierung** – Mit dem neuen und verbesserten Entscheidungsfluss können Sie nicht nur einfacher zwischen Entscheidungsobjekten navigieren, sondern auch steuern, wie Angebotssammlungen von der Entscheidungs-Engine bewertet werden. Hierzu zählt auch die Frage, welche Sammlungen gemeinsam oder getrennt bewertet werden und in welcher Reihenfolge die Sammlungen bewertet werden sollen. [Weitere Informationen](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### Fehlerbehebungen

* Es wurde ein Problem behoben, durch das die Journey-Liste, die Nachrichtenliste und E-Mail-Designer nicht angezeigt werden konnten, wenn die Browser-Sprache nicht Englisch war.
* Es wurde ein Syntaxfehler behoben, der beim Hinzufügen einer Personalisierung mit Hilfe eines Ausdrucks in E-Mail-Designer auftrat, wodurch Zeichen fälschlicherweise maskiert wurden.
* Es wurde ein Problem behoben, das zu einem 404-Fehler bei der Navigation im Menü **Administration** führte.
* Es wurde ein Problem behoben, das beim Testen einer Journey mithilfe eines Geschäftsereignisses weitere Live-Journeys auslöste.


## Version September 2021 {#september-2021-release}

### Neue Funktionen

<table>
<thead>
<tr>

<th><strong>Reporting – Bessere Einblicke in die Audience</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>In Berichten sind neue Metriken verfügbar: „Zielgruppe“ und „Ausgeschlossen“ für E-Mail- und Push-Nachrichten sind sowohl in Live- als auch in globalen Berichten sichtbar. </br> Um Zugriff auf die neuesten Metriken zu erhalten, müssen Sie die unterschiedlichen Reporting-Dashboards für jeden Kanal und Berichtstyp zurücksetzen. Weitere Informationen zur Anpassung von Dashboards finden Sie in der <a href="../reports/live-report.md">entsprechenden Dokumentation</a>.</p>
<p>Eine neue Spalte in der Liste der Nachrichtenausführungen zeigt die Anzahl der Zielprofile für jede Nachrichtenausführung an. </p>
<p>Weitere Informationen finden Sie in der <a href="../reports/global-report.md">ausführlichen Dokumentation</a>.</p>
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
<p>Weitere Informationen zu Sammlungen finden Sie in der <a href="../building-journeys/collections.md">entsprechenden Dokumentation</a>. </p>
<p>Der Filter und die Überschneidungsfunktionen wurden der Liste der im erweiterten Ausdruckseditor verfügbaren Funktionen hinzugefügt. Dies bietet mehr Möglichkeiten zum Filtern und Vergleichen von Sammlungen.</p>
<p>Lesen Sie die Dokumentation zu den Funktionen <a href="../building-journeys/functions/functionfilter.md">Filtern</a> und <a href="../building-journeys/functions/functionintersect.md">Überschneidung</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journeys**

* Systemgenerierte Schemata und Datensätze, die während der Bereitstellung von Schrittereignissen erstellt wurden, befinden sich jetzt im schreibgeschützten Modus, um versehentliche Änderungen an kritischen Schemata zu verhindern. [Weitere Informationen](../reports/sharing-overview.md)
* Sie können die Aktivität **Warten** eindeutig mit einer Bezeichnung benennen, die auf der Arbeitsfläche angezeigt wird. Die Bezeichnung wird auch in Reporting- und Testmodusprotokollen verwendet, um eindeutig zu identifizieren, was Sie tun. [Weitere Informationen](../building-journeys/about-journey-activities.md#best-practices)
* Ihre Ereignisse und Aktionen sind jetzt schneller auffindbar, indem Sie Elemente in den Kategorien **Ereignisse** und **Aktion** mithilfe der Suche filtern. Orchestrierungsaktivitäten werden nicht mehr gefiltert. [Weitere Informationen](../building-journeys/using-the-journey-designer.md)
* Beim Definieren einer Ereignis-ID-Bedingung in einem regelbasierten oder Geschäftsereignis ist jetzt der Operator „enthält“ für Felder vom Typ Zeichenfolge verfügbar. [Weitere Informationen](../event/about-creating.md)

**E-Mail-Konfiguration**

* Wenn ein IP-Pool mit einer Nachrichtenvoreinstellung verknüpft wurde, können Sie ihn jetzt bearbeiten, wobei die Aktualisierung asynchron erfolgt. Sie können auch den Status jedes IP-Pool-Updates überprüfen. [Weitere Informationen](../configuration/ip-pools.md#edit-ip-pool)


## Version August 2021 {#august-2021-release}

### Neue Funktionen

<table>
<thead>
<tr>

<th><strong>Senden von Nachrichten zur besten Zeit – Optimierung des Versandzeitpunktes</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Senden Sie mit Adobe Journey Optimizer Ihre Push-Benachrichtigung oder E-Mail automatisch zum besten Zeitpunkt für jeden Kunden. Die Optimierung des Versandzeitpunktes basiert auf den KI-Services von Adobe und sagt den besten Versandzeitpunkt für E-Mails oder Push-Benachrichtigungen voraus. Dadurch werden die Interaktionen auf der Grundlage historischer Öffnungs- und Klickraten automatisch maximiert.</p>
<p>Diese Funktion befindet sich derzeit in der Beta-Version und steht nur Beta-Kunden zur Verfügung. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/journeys-message.md#send-time-optimization">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Nutzen von Schemabeziehungen in Geschäftsereignissen – Verwalten von Lookup-Tabellen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt bei der Konfiguration von Geschäftsereignissen Beziehungen zwischen Schemata nutzen. Dies bietet zusätzlich die Möglichkeit, Felder aus verknüpften Tabellen beim Konfigurieren eines unitären Ereignisses, bei der Verwendung von Bedingungen in einer Journey sowie bei der Personalisierung von Nachrichten und benutzerdefinierten Aktionen zu nutzen.</p>
<p>Weitere Informationen finden Sie in der <a href="../event/experience-event-schema.md#leverage_schema_relationships">ausführlichen Dokumentation</a>.</p>
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
<p>Personalisierte URLs führen Empfänger abhängig von den Profilattributen zu bestimmten Seiten einer Website oder zu einer personalisierten Microsite. In Adobe Journey Optimizer können Sie jetzt URLs im Nachrichteninhalt eine Personalisierung hinzufügen. Die URL-Personalisierung kann auf Text und Bilder angewendet werden und Profil- oder kontextuelle Daten verwenden.</p>
<p>Weitere Informationen finden Sie in der <a href="../personalization/personalization-syntax.md#perso-urls">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Stellen Sie sicher, dass Ihre E-Mails Ihre Benutzer erreichen – Weitere Zustellversuche bei E-Mails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt den Zeitraum für weitere Zustellversuche pro Voreinstellung definieren, um sicherzustellen, dass keine weiteren Zustellversuche ausgeführt werden, wenn sie nicht mehr benötigt werden. Beispielsweise können Sie den Zeitraum für weitere Zustellversuche für eine Transaktionsnachricht zum Zurücksetzen des Passworts, die einen nur für einen Tag gültigen Link enthält, auf 24 Stunden begrenzen. Beachten Sie, dass Einstellungen für weitere Zustellversuche nur für den E-Mail-Kanal gelten.</p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/retries.md#retry-duration">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Definieren der vom Versand auszuschließenden Adressen – Unterdrückungsliste</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Das Hinzufügen von E-Mail-Adressen und Domains zur Unterdrückungsliste ist jetzt in der Benutzeroberfläche entweder einzeln oder im Bulk-Modus durch einen CSV-Datei-Upload möglich.</p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


### Verbesserungen

**Journeys**

* **Dynamische Header** – Sie können jetzt dynamische Daten in HTTP-Header-Parametern übergeben. Diese Parameter können von den Integrationssystemen verwendet werden, die die HTTP-Aufrufe der Journey-Aktion empfangen, z. B. Zeitstempel oder Tracking-ID. [Weitere Informationen](../action/about-custom-action-configuration.md#url-configuration)
* **Dynamische URL-Pfade** – Sie können jetzt dynamische URL-Pfade für benutzerdefinierte Aktionen einrichten. [Weitere Informationen](../action/about-custom-action-configuration.md#url-configuration)
* Die Gesamtdrosselungsrate für den Schritt „Segment lesen“ wurde von 17.000 auf 20.000 Nachrichten pro Sekunde geändert. [Weitere Informationen](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Benutzeroberfläche**

* **Suche** – Auf jeder Seite können Sie jetzt Geschäftsobjekte und Hilfeartikel direkt über das Suchfeld „Einheitliches Experience Cloud“ durchsuchen. [Weitere Informationen](../start/user-interface.md#unified-search)
* **Zuletzt ausgewertet** – Die Anzeige von kürzlich aufgerufenen Elementen auf der Adobe Journey Optimizer-Startseite wird jetzt auf weitere Geschäftsobjekte erweitert. Mit diesem Update können Sie über die kürzlich aufgerufenen Verknüpfungen auf Nachrichten, Journeys, Segmente, Schemata, Datensätze, Datenquellen, Ereignisse, Aktionen, Quellen und Ziele zugreifen. [Weitere Informationen](../action/about-custom-action-configuration.md#passing-collection)

**Inhaltserstellung**

* **Hintergrund** – Hintergrundbilder werden jetzt in der Live-Vorschau unterstützt. [Weitere Informationen](../email/preview.md)
* **Ein-Klick-Opt-out-Link** – Sie können einen neuen Link-Typ in Ihren E-Mail-Inhalt einfügen: Mit dem **Opt-out**-Link können sich Benutzer vom Erhalt Ihrer Nachrichten mit nur einem Klick abmelden, ohne zu einer Landingpage weitergeleitet zu werden, um die Abmeldung zu bestätigen. [Weitere Informationen](../privacy/opt-out.md#one-click-opt-out-link)

**Personalisierung**

* **Ausdruckseditor**: Bei der Definition der Personalisierung können Sie jetzt ganz einfach einen Fallback-Wert hinzufügen: Wenn das Personalisierungsfeld für ein Profil leer ist, wird der Fallback-Wert angezeigt. [Weitere Informationen](../personalization/functions/helpers.md)

**E-Mail-Konfiguration**

* **Zulassungsliste** – Die Zulassungsliste kann jetzt in einer Nicht-Produktions-Sandbox über einen API-Aufruf aktiviert und deaktiviert werden. [Weitere Informationen](../configuration/allow-list.md#enable-allow-list)
* **Navigation** – Die Unterdrückungsliste, auf die über das Menü **Administration > Kanäle > E-Mail-Konfiguration > Allgemein** zugegriffen werden kann, wurde in das neue Untermenü **Unterdrückungsliste** verschoben, in dem alle zugehörigen Funktionen für einen einfacheren Zugriff zusammengefasst sind. [Weitere Informationen](../configuration/manage-suppression-list.md#access-suppression-list)

**Entscheidungs-Management**

* Die Art und Weise, wie Sie beim Erstellen eines Angebots Darstellungen hinzufügen und konfigurieren, wurde aktualisiert, um das Anwendererlebnis zu verbessern. Insbesondere wird die Asset-Bibliothek jetzt nur angezeigt, wenn Sie für eine Darstellung Bildinhalte definieren. [Weitere Informationen](../offers/offer-library/creating-personalized-offers.md#representations)

### Fehlerbehebungen

* Fehlerkorrektur – Die Barrierefreiheit in der Navigation auf der Nachrichtenregisterkarte funktioniert jetzt fehlerfrei.
* Fehlerkorrektur – Die Lokalisierung in den E-Mail-Designer-Bezeichnungen funktioniert jetzt fehlerfrei.
* Fehlerkorrektur – Die Auswahl von mehr als einem Knoten in einer Journey und anschließendem Klicken auf „Löschen“ im Eigenschaftsfenster funktioniert jetzt fehlerfrei.
* Fehlerkorrektur – Ein neuer Header kann jetzt zu einer in einer Journey verwendeten Aktion hinzugefügt werden.
* Sie können jetzt durch eine präzisere Warnung in der Benutzeroberfläche feststellen, warum die Erstellung einer Nachrichtenvoreinstellung fehlgeschlagen ist.


## Version Juli 2021 {#july-2021-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Verwenden von Metadaten in Ihren Nachrichten – Verwalten von Lookup-Tabellen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Ihre Erlebnisse mit Referenzdaten anreichern, die Sie in Journey Optimizer geladen haben. Beispiele sind das Suchen von Metadaten für eine Reservierungs-ID in einem Erlebnisereignis oder das Suchen von Produktinformationen über eine Artikelnummer in einem Erlebnisereignis zur Verwendung auf der Arbeitsfläche. </p>
<p>Sie können jetzt Beziehungen zwischen Schemata nutzen, um einen Datensatz als Lookup-Tabelle für einen anderen zu verwenden. Sie können dann alle Felder der verknüpften Tabellen verwenden, wenn Sie ein unitäres Ereignis konfigurieren oder Bedingungen in einer Journey oder bei der Personalisierung von Nachrichten und benutzerdefinierten Aktionen nutzen.</p>
<p>Weitere Informationen finden Sie in der <a href="../event/experience-event-schema.md#leverage_schema_relationships">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Zulassungsliste</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt eine spezifische Sicherheitsliste für den Versand auf Sandbox-Ebene definieren, um eine sichere Umgebung für Testzwecke zu erhalten. Auf einer Nicht-Produktionsinstanz, bei der Fehler auftreten können, stellt die Zulassungsliste sicher, dass Sie kein Risiko haben, unerwünschte Nachrichten an Ihre Kunden zu senden. Diese Funktion wird durch die Verwendung von Unterdrückungs-APIs ermöglicht.</p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/allow-list.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journeys**

* Die Gesamteinschränkungsrate aller Segment-Lesen-Schritte, die gleichzeitig in derselben Sandbox ausgeführt werden, ist auf 17.000 Nachrichten pro Sekunde beschränkt. [Mehr dazu](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Das Feld **Aufbewahrungsfrist im Cache** wurde aus dem Konfigurationsbereich der Datenquelle entfernt. [Mehr dazu](../datasource/about-data-sources.md)
* Für externe Datenquellen ist jetzt automatisch eine Begrenzungsregel von 15 Aufrufen pro Sekunde definiert. [Mehr dazu](../configuration/external-systems.md#capping)
* Für Live-Journeys werden im Journey-Eigenschaftsfenster das Veröffentlichungsdatum und der Name des Benutzers angezeigt, der die Journey veröffentlicht hat. [Mehr dazu](../building-journeys/journey-gs.md#change-properties)
* Im Journey-Listenfenster wurde ein Filter für den Journey-Typ hinzugefügt. [Mehr dazu](../start/user-interface.md#filter-lists)
* Der Parameter **[!UICONTROL Einschränkungsrate]** wurde in der Aktivität „Segment lesen“ hinzugefügt. [Mehr dazu](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Vorschau und Test**

* Identität und Namespace sind nun im Bildschirm **[!UICONTROL Vorschau]** sichtbar. [Mehr dazu](../email/preview.md#preview-your-messages)
* Die Anzahl der Test-E-Mails für Testsendungen ist jetzt auf 10 beschränkt.
* Die Anzahl der für das **Präfix der Betreffzeile** in Testsendungen zulässigen Zeichen ist jetzt begrenzt. [Mehr dazu](../email/preview.md#send-proofs)

**Ausdruckseditor für Personalisierung**

* Die Dropdown-Liste „Helper“ wurde umbenannt und neu angeordnet.

### Fehlerbehebungen

* Fehlerkorrektur – Jetzt werden keine doppelten Nachrichten mehr während des Batch-E-Mail-Versands gesendet.
* Fehlerkorrektur – Ereignisse werden jetzt entsprechend generiert, wenn nach Ablauf des Wiederholungszeitraums kein E-Mail-Versand mehr durchgeführt wird.
* Fehlerkorrektur – Im Bildschirm „PTR-Einträge“ fehlen jetzt keine IP-Informationen mehr.
* Fehlerkorrektur – Die Lokalisierung in der Angebotsleiste im Ausdruckseditor ist jetzt implementiert.
* Fehlerkorrektur – Der Abstand in Informations-Popups ist jetzt korrekt.
* Fehlerkorrektur – Beim Hochladen einer HTML-Datei in E-Mail-Designer wird jetzt das interne Stylesheet mit der Eigenschaft `background-image` unterstützt.
