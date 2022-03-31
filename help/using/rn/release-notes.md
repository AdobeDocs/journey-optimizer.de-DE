---
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '2824'
ht-degree: 96%

---

# Versionshinweise {#release-notes}

Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für [!DNL Journey Optimizer] aufgelistet. Auf der Seite [Letzte Dokumentations-Updates](documentation-updates.md) finden Sie weitere Änderungsmöglichkeiten.

## Version März 2022 {#march-2022-release}

### Verbesserungen

**Journeys**

* Um zu vermeiden, dass im einheitlichen Profilschema unnötige Felder vorhanden sind, ist das Journey Step Event-Schema nicht mehr standardmäßig für Profile aktiviert. Bei Bedarf können Sie sie aktivieren. [Weitere Informationen](../reports/sharing-overview.md)
* Neue Schrittereignisse im Zusammenhang mit Exportvorgängen werden jetzt von Journey Optimizer an Adobe Experience Platform gesendet. Beispiele für Abfragen wurden der Dokumentation hinzugefügt. [Weitere Informationen](../reports/query-examples.md)

**Entscheidungs-Management**

<!--* You can now specify if offer capping is applied across all users or to one specific profile, and to all placements or per placement. [Learn more](../offers/offer-library/creating-personalized-offers.md)-->
* Mit der Batch Decisioning-API können Unternehmen die offer decisioning-Funktionalität für alle Profile in einem bestimmten Segment in einem einzigen Aufruf verwenden. Der Angebotsinhalt für jedes Profil im Segment wird in einem AEP-Datensatz platziert, wo er für benutzerdefinierte Batch-Workflows verfügbar ist. [Weitere Informationen](../offers/api-reference/batch-api/deliver-offers-batch.md)

<!--**Administration**

* You can now enable/disable the unsubscribe link in/from the email header at the message preset level, and set a custom unsubscribe URL at the message level. [Learn more](../configuration/message-presets.md#list-unsubscribe)
* The allowed list will can now be enabled and disabled through the [!DNL Journey Optimizer] interface. [Learn more](../messages/allow-list.md#enable-allow-list)-->

**Personalisierung**

* Sie können jetzt mehr als 40 Personalisierungsausdrücke in der Bibliothek speichern. [Weitere Informationen](../personalization/personalization-library.md)

## Version Februar 2022 {#feb-2022-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Landingpages für Abonnements</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können in Journey Optimizer jetzt Landingpages erstellen und gestalten und Ihre Benutzer zu Online-Formularen weiterleiten, über die sie sich für den Erhalt Ihrer Nachrichten anmelden oder abmelden oder einen bestimmten Service wie einen Newsletter abonnieren können.</p>
<p>Weitere Informationen finden Sie in der <a href="../landing-pages/create-lp.md">entsprechenden Dokumentation</a> und in diesem <a href="../landing-pages/lp-use-cases.md">Anwendungsfall</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Neue Ausdrucksbibliothek für die Personalisierung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer bietet jetzt eine Bibliothek, in der Sie auf vordefinierte Personalisierungsausdrücke zugreifen können. Diese Ausdrücke werden von Admin-Benutzern konfiguriert.</p>
<p>Weitere Informationen finden Sie in der <a href="../personalization/personalization-library.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs’ feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Übergeben von Informationen zur Nachverfolgung Ihrer Nachrichten mit UTM-Tracking-Parametern</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Nachrichteninhalten von Journey Optimizer können Sie jetzt UTM-Parameter zu Ihren Links hinzufügen. Diese können zusätzliche Daten zu diesem Link liefern und Ihnen dabei helfen herauszufinden, wo und warum eine Person auf Ihren Link geklickt hat.</p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/message-presets.md#configure-email-settings">entsprechenden Dokumentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journey**

* Um die Leistung zu optimieren, wechseln alle Journeys im Testmodus, die seit einer Woche nicht ausgelöst wurden, jetzt wieder in den Entwurfsstatus zurück. [Weitere Informationen](../building-journeys/testing-the-journey.md#important_notes)
* Die Integration zwischen Journey Optimizer und Adobe Campaign Classic wurde optimiert, um die Leistung zu verbessern. Die Standardkonfiguration für Begrenzungen wurde auf 4.000 Aufrufe/5 Minuten geändert.	[Weitere Informationen](../action/acc-action.md#important-notes)

**Reporting**

* Sendungen können nun nach ihrem Status gefiltert werden:
   * In der Liste „Nachrichtenausführung“ können Sie jetzt Testsendungen aus der Versandliste ausschließen.
   * Bei Ihren Live-/Global-Berichten können Sie auswählen, ob Sie Testereignisse ausschließen möchten.

* Sie können jetzt auf Berichte zu Sendezeitoptimierungsdaten zugreifen: die Anzahl der Personen, die unmittelbar benachrichtigt wurden, und die Anzahl der Personen, die mit einer 1-Stunden-Optimierung, einer 2-Stunden-Optimierung usw. benachrichtigt wurden.

<!--* Offer Decisioning reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Entscheidungs-Management**

* Rangfolgen und KI-Rangfolgen werden jetzt in einer Registerkarte zusammengefasst.

## Version Januar 2022 {#january-2022-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Journeys – Optimales Aufwärmen Ihrer IP-Adressen mit Profilbegrenzungsbedingungen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Beim Konfigurieren einer <strong>Bedingungs</strong>-Aktivität in einer Journey können Sie jetzt eine Profilobergrenze festlegen. Dieser neue Bedingungstyp ermöglicht es Ihnen, eine Höchstzahl von Profilen für einen Journey-Pfad festzulegen. Wenn diese Grenze erreicht ist, folgen die eintretenden Profile einem alternativen Pfad. Auf diese Weise können Sie das Volumen Ihrer Sendungen erhöhen (IP-Ramp-up). Sie können beispielsweise Ihre Sendungen in einer Domain schrittweise ausführen, indem Sie die Ausführung aufteilen: Sie senden 1.000 Nachrichten am Tag 1, 2.000 am Tag 2 usw.</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/condition-activity.md#profile_cap">entsprechenden Dokumentation</a> und in diesem <a href="../building-journeys/ramp-up-deliveries-uc.md">Anwendungsfall</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journeys – Verbesserung beim Lesen von Segmenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Option <strong>Inkrementelles Lesen</strong> wurde zu den wiederkehrenden <strong>Segment lesen</strong>-Aktivitäten hinzugefügt. Mit dieser Option haben Sie die Möglichkeit, nur die Personen anzusprechen, die seit der letzten Ausführung der Journey in das Segment eingetreten sind. Bei der ersten Ausführung sind immer alle Segmentmitglieder ausgewählt.</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">entsprechenden Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journey**

* Step-Ereignisse von Journey Optimizer können jetzt mit anderen Datensätzen in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=de) verknüpft werden. Das Feld **profileID** im integrierten Step-Ereignisschema einer Journey ist jetzt als Identitätsfeld definiert. [Weitere Informationen](../reports/sharing-overview.md#integration-cja)

**Offer Decisioning**

* Wenn Sie ein Angebot, ein Fallback-Angebot, eine Angebotssammlung oder eine Angebotsentscheidung aktualisieren, auf die direkt oder indirekt in einer veröffentlichten Nachricht verwiesen wird, werden die Aktualisierungen automatisch in der entsprechenden Nachricht angezeigt, ohne dass sie erneut veröffentlicht werden müssen. [Weitere Informationen](../offers/offers-e2e.md#insert-decision-in-email)

* Bei der Simulation, welche Angebote für ein bestimmtes Testprofil bereitgestellt werden sollen, können Sie jetzt die Standardsimulationseinstellungen ändern und den Code anzeigen, der Ihren Simulationen entspricht. Dieser Code kann zur Fehlerbehebung verwendet werden. [Weitere Informationen](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administration**

* Administratoren können jetzt PTR-Einträge mit einer Subdomain bearbeiten, die mit CNAME eingerichtet ist. [Weitere Informationen](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalisierung**

* **Zu Favoriten hinzufügen** – Um das Arbeiten mit Personalisierungen einfacher zu gestalten, haben die Speicherung von Favoriten ermöglicht. Durch das Hinzufügen verschiedener Attribute zum Favoritenmenü erhalten Sie schnellen Zugriff auf die am häufigsten verwendeten Elemente. [Weitere Informationen](../personalization/personalize.md#fav)

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
<p>Adobe Journey Optimizer unterstützt jetzt CNAMEs. Ein CNAME-Datensatz bzw. Datensatz mit kanonischem Namen ist ein Datensatz, der auf eine andere Domain-Adresse und nicht auf eine IP-Adresse verweist. Mit der CNAME-Subdomain-Delegierung können Sie eine Subdomain erstellen und CNAMEs verwenden, um auf Adobe-spezifische Datensätze zu verweisen. Mit dieser Konfiguration sind Sie und Adobe gemeinsam für die Pflege des DNS verantwortlich, um eine Umgebung für das Senden, Rendern und Tracking von E-Mails einzurichten.</p>
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
<p>Sie können jetzt simulieren, welche Angebote an ein Testprofil für eine bestimmte Platzierung in der Journey Optimizer-Benutzeroberfläche gesendet werden. Auf diese Weise können Sie Ihre Entscheidungslogik einschließlich Eignungsbegrenzungen und Ranking-Algorithmen einfach validieren, bevor Sie sie in die Produktion übernehmen.
Mit dieser Funktion können technisch versierte ebenso wie technisch nicht versierte Benutzer Offer Decisioning schnell testen und potenzielle Probleme beheben.</p>
<p>Weitere Informationen finden Sie in der <a href="../offers/offer-activities/simulation.md">entsprechenden Dokumentation</a>.</p>
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
<p>Weitere Informationen finden Sie in der <a href="../offers/offer-library/creating-personalized-offers.md#custom-text">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


Siehe auch [Adobe Experience Platform – Versionshinweise Oktober](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html?lang=de){target=&quot;_blank&quot;} für weitere Änderungen.

### Verbesserungen

**Journey**

* **Ausdruckseditor** – Als Power User können Sie jetzt Funktionen verwenden, um mit Karten zu arbeiten. Diese Funktion kann mit den Abonnement-Listen genutzt werden. Beispielsweise können Sie jetzt in einem Segment eine E-Mail-Adresse aus einer Abonnement-Liste abrufen. [In diesem Beispiel erfahren Sie mehr](../building-journeys/message-to-subscribers-uc.md).

* **Monitoring** – Step-Ereignisse für Live-Journeys und den Testmodus wurden verbessert. Es wurden [neue Felder](../reports/sharing-field-list.md#serviceevents) im Zusammenhang mit Profilexportvorgängen hinzugefügt. Für ein besseres Benutzererlebnis sind die Felder für Step-Ereignisse jetzt in verschiedenen Kategorien organisiert. Alle Felder für vorhergehende Step-Ereignisse sind weiterhin in der Kategorie [stepEvents](../reports/sharing-legacy-fields.md) verfügbar.
* **Barrierefreiheit** – Es wurden Verbesserungen an der Barrierefreiheit von Journeys implementiert.
* **Kollektionen** – Arrays von Objekten, die Unterobjekte enthalten, werden nun unterstützt. [Weitere Informationen](../building-journeys/collections.md)
* **Listen** – Die Bildschirme „Listen“ für Journeys, Ereignisse, Aktionen und Datenquellen wurden verbessert.

**Berichterstellung**

* **Datenformat in der globalen Ansicht** – Sie können jetzt in der **globalen Ansicht** der Registerkarte **Ausführung** zwischen Zahlen und Prozentsätzen hin- und herschalten. [Weitere Informationen](../reports/message-monitoring.md)


**Administration**

* **Bearbeiten von Nachrichtenvoreinstellungen** – Sie können jetzt Nachrichtenvoreinstellungen bearbeiten und ihren Aktualisierungsstatus überwachen. [Weitere Informationen](../configuration/message-presets.md#edit-message-preset)
* **PTR-Datensätze bearbeiten** – Sie können jetzt PTR-Einträge bearbeiten und ihren Aktualisierungsstatus überwachen. [Weitere Informationen](../configuration/ptr-records.md#edit-ptr-record)

**Personalisierung**

* **Neue Hilfsfunktion für die Datumsformatierung** – Sie können jetzt angeben, wie eine Datums-Zeichenfolge dargestellt werden soll. [Weitere Informationen](../personalization/functions/dates.md#format-date)


**Entscheidungs-Management**

* **Auswertungssequenzierung** – Mit dem neuen und verbesserten Entscheidungsfluss können Sie nicht nur einfacher zwischen Entscheidungsobjekten navigieren, sondern auch steuern, wie Angebotskollektionen von der Entscheidungs-Engine bewertet werden. Hierzu zählt auch die Frage, welche Kollektionen gemeinsam oder getrennt bewertet werden und in welcher Reihenfolge die Kollektionen bewertet werden sollen. [Weitere Informationen](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

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
<p>Weitere Informationen finden Sie in der <a href="../reports/message-monitoring.md">entsprechenden Dokumentation</a>.</p>
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
<p>Sie können jetzt Kollektionen oder eine Liste von Daten in Ihren benutzerdefinierten Aktionsparametern übergeben, die zur Laufzeit dynamisch gefüllt werden. Es werden zwei Arten von Kollektionen unterstützt: einfache Kollektionen und Objektkollektionen. Zuvor erstellte benutzerdefinierte Aktionen funktionieren weiterhin. </p>
<p>Weitere Informationen zu Kollektionen finden Sie in der <a href="../building-journeys/collections.md">entsprechenden Dokumentation</a>. </p>
<p>Der Filter und die Überschneidungsfunktionen wurden der Liste der im erweiterten Ausdruckseditor verfügbaren Funktionen hinzugefügt. Dies bietet mehr Möglichkeiten zum Filtern und Vergleichen von Kollektionen.</p>
<p>Lesen Sie die Dokumentation zu den Funktionen <a href="../building-journeys/functions/functionfilter.md">Filtern</a> und <a href="../building-journeys/functions/functionintersect.md">Überschneidung</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journey**

* Systemgenerierte Schemas und Datensätze, die während der Bereitstellung von Schrittereignissen erstellt wurden, befinden sich jetzt im schreibgeschützten Modus, um unbeabsichtigte Änderungen an kritischen Schemas zu verhindern. [Weitere Informationen](../reports/sharing-overview.md)
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
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/journeys-message.md#send-time-optimization">entsprechenden Dokumentation</a>.</p>
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
<p>Sie können jetzt beim Konfigurieren von Geschäftsereignissen Beziehungen zwischen Schemas nutzen. Dies bietet zusätzlich die Möglichkeit, Felder aus verknüpften Tabellen beim Konfigurieren eines unitären Ereignisses, bei der Verwendung von Bedingungen in einer Journey sowie bei der Personalisierung von Nachrichten und benutzerdefinierten Aktionen zu nutzen.</p>
<p>Weitere Informationen finden Sie in der <a href="../event/experience-event-schema.md#leverage_schema_relationships">entsprechenden Dokumentation</a>.</p>
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
<p>Personalisierte URLs führen Empfänger abhängig von den Profilattributen zu bestimmten Seiten einer Website oder zu einer personalisierten Microsite. In Adobe Journey Optimizer können Sie jetzt URLs im Nachrichteninhalt eine Personalisierung hinzufügen. Die URL-Personalisierung kann auf Text und Bilder angewendet werden und sie kann Profildaten oder Kontextdaten verwenden.</p>
<p>Weitere Informationen finden Sie in der <a href="../personalization/personalization-syntax.md#perso-urls">entsprechenden Dokumentation</a>.</p>
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
<p>Weitere Informationen finden Sie in der <a href="../configuration/retries.md#retry-duration">entsprechenden Dokumentation</a>.</p>
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
<p>Weitere Informationen finden Sie in der <a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


### Verbesserungen

**Journey**

* **Dynamische Header** – Sie können jetzt dynamische Daten in HTTP-Header-Parametern übergeben. Diese Parameter können von den Integrationssystemen verwendet werden, die die HTTP-Aufrufe der Journey-Aktion empfangen, z. B. Zeitstempel oder Tracking-ID. [Weitere Informationen](../action/about-custom-action-configuration.md#url-configuration)
* **Dynamische URL-Pfade** – Sie können jetzt dynamische URL-Pfade für benutzerdefinierte Aktionen einrichten. [Weitere Informationen](../action/about-custom-action-configuration.md#url-configuration)
* Die Gesamtdrosselungsrate für den Schritt „Segment lesen“ wurde von 17.000 auf 20.000 Nachrichten pro Sekunde geändert. [Weitere Informationen](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Benutzeroberfläche**

* **Suche** – Auf jeder Seite können Sie jetzt Geschäftsobjekte und Hilfeartikel direkt über das Suchfeld „Einheitliches Experience Cloud“ durchsuchen. [Weitere Informationen](../start/user-interface.md#unified-search)
* **Zuletzt ausgewertet** – Die Anzeige von kürzlich aufgerufenen Elementen auf der Adobe Journey Optimizer-Startseite wird jetzt auf weitere Geschäftsobjekte erweitert. Mit diesem Update umfassen die kürzlich aufgerufenen Verknüpfungen Nachrichten, Journeys, Segmente, Schemas, Datensätze, Datenquellen, Ereignisse, Aktionen, Quellen und Ziele. [Weitere Informationen](../action/about-custom-action-configuration.md#passing-collection)

**Inhaltserstellung**

* **Hintergrund** – Hintergrundbilder werden jetzt in der Live-Vorschau unterstützt. [Weitere Informationen](../design/preview.md)
* **Ein-Klick-Opt-out-Link** – Sie können einen neuen Link-Typ in Ihren E-Mail-Inhalt einfügen: Mit dem **Opt-out**-Link können sich Benutzer vom Erhalt Ihrer Nachrichten mit nur einem Klick abmelden, ohne zu einer Landingpage weitergeleitet zu werden, um die Abmeldung zu bestätigen. [Weitere Informationen](../messages/consent.md#one-click-opt-out-link)

**Personalisierung**

* **Ausdruckseditor** – Bei der Definition der Personalisierung können Sie jetzt einfach einen Fallback-Wert hinzufügen: Wenn das Personalisierungsfeld für ein Profil leer ist, wird der Fallback-Wert angezeigt. [Weitere Informationen](../personalization/functions/helpers.md)

**E-Mail-Konfiguration**

* **Zulassungsliste** – Die Zulassungsliste kann jetzt in einer Nicht-Produktions-Sandbox über einen API-Aufruf aktiviert und deaktiviert werden. [Weitere Informationen](../reports/allow-list.md#enable-allow-list)
* **Navigation** – Die Unterdrückungsliste, auf die über das Menü **Administration > Kanäle > E-Mail-Konfiguration > Allgemein** zugegriffen werden kann, wurde in das neue Untermenü **Unterdrückungsliste** verschoben, in dem alle zugehörigen Funktionen für einen einfacheren Zugriff zusammengefasst sind. [Weitere Informationen](../configuration/manage-suppression-list.md#access-suppression-list)

**Entscheidungs-Management**

* Die Art und Weise, wie Sie beim Erstellen eines Angebots Darstellungen hinzufügen und konfigurieren, wurde aktualisiert, um das Anwendererlebnis zu verbessern. Insbesondere wird die Asset-Bibliothek jetzt nur angezeigt, wenn Sie für eine Darstellung Bildinhalte definieren. [Weitere Informationen](../offers/offer-library/creating-personalized-offers.md#representations)

### Fehlerbehebungen

* Fehlerkorrektur – Die Barrierefreiheit in der Navigation auf der Nachrichtenregisterkarte funktioniert jetzt fehlerfrei.
* Fehlerkorrektur – Die Lokalisierung in den Email Designer-Bezeichnungen funktioniert jetzt fehlerfrei.
* Fehlerkorrektur – Die Auswahl von mehr als einem Knoten in einer Journey und anschließendem Klicken auf „Löschen“ im Eigenschafts-Panel funktioniert jetzt fehlerfrei.
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
<p>Sie können jetzt Beziehungen zwischen Schemas nutzen, um einen Datensatz als Lookup-Tabelle für einen anderen zu verwenden. Sie können dann alle Felder der verknüpften Tabellen verwenden, wenn Sie ein unitäres Ereignis konfigurieren oder Bedingungen in einer Journey oder bei der Personalisierung von Nachrichten und benutzerdefinierten Aktionen nutzen.</p>
<p>Weitere Informationen finden Sie in der <a href="../event/experience-event-schema.md#leverage_schema_relationships">entsprechenden Dokumentation</a>.</p>
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
<p>Weitere Informationen finden Sie in der <a href="../reports/allow-list.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journey**

* Die Gesamteinschränkungsrate aller Segment-Lesen-Schritte, die gleichzeitig in derselben Sandbox ausgeführt werden, ist auf 17.000 Nachrichten pro Sekunde beschränkt. [Mehr dazu](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Das Feld **Aufbewahrungsfrist im Cache** wurde aus dem Konfigurationsbereich der Datenquelle entfernt. [Mehr dazu](../datasource/about-data-sources.md)
* Für externe Datenquellen ist jetzt automatisch eine Begrenzungsregel von 15 Aufrufen pro Sekunde definiert. [Mehr dazu](../configuration/external-systems.md#capping)
* Für Live-Journeys werden im Journey-Eigenschaftsfenster das Veröffentlichungsdatum und der Name des Benutzers angezeigt, der die Journey veröffentlicht hat. [Mehr dazu](../building-journeys/journey-gs.md#change-properties)
* Im Journey-Listenfenster wurde ein Filter für den Journey-Typ hinzugefügt. [Mehr dazu](../start/user-interface.md#filter-lists)
* Der Parameter **[!UICONTROL Einschränkungsrate]** wurde in der Aktivität „Segment lesen“ hinzugefügt. [Mehr dazu](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Nachrichtenvorschau und Testversand**

* Identität und Namespace sind nun im Bildschirm **[!UICONTROL Vorschau]** sichtbar. [Mehr dazu](../design/preview.md#preview-your-messages)
* Die Anzahl der Test-E-Mails für Testsendungen ist jetzt auf 10 beschränkt.
* Die Anzahl der für das **Präfix der Betreffzeile** in Testsendungen zulässigen Zeichen ist jetzt begrenzt. [Mehr dazu](../design/preview.md#send-proofs)

**Ausdruckseditor für Personalisierung**

* Die Dropdown-Liste „Helper“ wurde umbenannt und neu angeordnet.

### Fehlerbehebungen

* Fehlerkorrektur – Jetzt werden keine doppelten Nachrichten mehr während des Batch-E-Mail-Versands gesendet.
* Fehlerkorrektur – Ereignisse werden jetzt entsprechend generiert, wenn nach Ablauf des Wiederholungszeitraums kein E-Mail-Versand mehr durchgeführt wird.
* Fehlerkorrektur – Im Bildschirm „PTR-Datensätze“ fehlen jetzt keine IP-Informationen mehr.
* Fehlerkorrektur – Die Lokalisierung in der Angebotsleiste im Ausdruckseditor ist jetzt implementiert.
* Fehlerkorrektur – Der Abstand in Informations-Popups ist jetzt korrekt.
* Fehlerkorrektur – Beim Hochladen einer HTML-Datei in Email Designer wird jetzt das interne Stylesheet mit der Eigenschaft `background-image` unterstützt.
