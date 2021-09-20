---
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 5a21ac0c199bf237972122ac46e58bf9f8d0f8ab
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 86%

---

# Versionshinweise {#release-notes}

Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für [!DNL Journey Optimizer] aufgelistet. Sie können auch die neusten [Aktualisierungen der Dokumentation](documentation-updates.md) einsehen.


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
<p>Weitere Informationen finden Sie in der <a href="building-journeys/journeys-message.md#send-time-optimization">entsprechenden Dokumentation</a>.</p>
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
<p>Weitere Informationen finden Sie in der <a href="event/experience-event-schema.md#leverage_schema_relationships">entsprechenden Dokumentation</a>.</p>
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
<p>Personalisierte URLs führen Empfänger zu bestimmten Seiten einer Website oder zu einer personalisierten Microsite, je nach Profilattributen. In Adobe Journey Optimizer können Sie jetzt URLs im Nachrichteninhalt Personalisierung hinzufügen. Die URL-Personalisierung kann auf Text und Bilder angewendet werden und Profildaten oder Kontextdaten verwenden.</p>
<p>Weitere Informationen finden Sie in der <a href="personalization/personalization-syntax.md#perso-urls">entsprechenden Dokumentation</a>.</p>
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
<p>Weitere Informationen finden Sie in der <a href="configuration/retries.md#retry-duration">entsprechenden Dokumentation</a>.</p>
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
<p>Das Hinzufügen von E-Mail-Adressen und Domains zur Unterdrückungsliste ist jetzt in der Benutzeroberfläche entweder einzeln oder im Bulk-Modus durch einen CSV-Datei-Upload möglich.</p>
<p>Weitere Informationen finden Sie in der <a href="configuration/manage-suppression-list.md#add-addresses-and-domains">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Customer Alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now subscribe to event-based alerts regarding Adobe Journey Optimizer activities. The user interface allows you to view a history of received alerts based on metrics revealed by Adobe Experience Platform Observability Insights. The UI also allows you to view, enable, and disable available alert rules.</p>
<p>This feature is currently in beta version and only available to beta customers. To join the beta program, contact Adobe Customer Care.
</p>
<p>For more information, refer to the <a href="https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html">Adobe Experience Platform documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

### Verbesserungen

**Journeys**

* **Dynamische Header** – Sie können jetzt dynamische Daten in HTTP-Header-Parametern übergeben. Diese Parameter können von den Integrationssystemen verwendet werden, die die HTTP-Aufrufe der Journey-Aktion empfangen, z. B. Zeitstempel oder Tracking-ID. [Weitere Informationen](action/about-custom-action-configuration.md#url-configuration)
* **Dynamische URL-Pfade** – Sie können jetzt dynamische URL-Pfade für benutzerdefinierte Aktionen einrichten. [Weitere Informationen](action/about-custom-action-configuration.md#url-configuration)
* Die Gesamtdrosselungsrate für den Schritt „Segment lesen“ wurde von 17.000 auf 20.000 Nachrichten pro Sekunde geändert. [Weitere Informationen](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Benutzeroberfläche**

* **Suche** – Auf jeder Seite können Sie jetzt Geschäftsobjekte und Hilfeartikel direkt über das Suchfeld „Einheitliches Experience Cloud“ durchsuchen. [Weitere Informationen](user-interface.md#unified-search)
* **Zuletzt ausgewertet** – Die Anzeige von kürzlich aufgerufenen Elementen auf der Adobe Journey Optimizer-Startseite wird jetzt auf weitere Geschäftsobjekte erweitert. Mit diesem Update umfassen die kürzlich aufgerufenen Verknüpfungen Nachrichten, Journeys, Segmente, Schemas, Datensätze, Datenquellen, Ereignisse, Aktionen, Quellen und Ziele. [Weitere Informationen](action/about-custom-action-configuration.md#passing-collection)

**Inhaltserstellung**

* **Hintergrund** – Hintergrundbilder werden jetzt in der Live-Vorschau unterstützt. [Weitere Informationen](preview.md)
* **Ein-Klick-Opt-out-Link** – Sie können einen neuen Link-Typ in Ihren E-Mail-Inhalt einfügen: Mit dem **Opt-out**-Link können sich Benutzer vom Erhalt Ihrer Nachrichten mit nur einem Klick abmelden, ohne zu einer Landingpage weitergeleitet zu werden, um die Abmeldung zu bestätigen. [Weitere Informationen](message-tracking.md#one-click-opt-out-link)

**Personalisierung**

* **Ausdruckseditor**  - Bei der Definition der Personalisierung können Sie jetzt einfach einen Fallback-Wert hinzufügen: Wenn das Personalisierungsfeld für ein Profil leer ist, wird der Fallback-Wert angezeigt. [Weitere Informationen](personalization/functions/helpers.md)

**E-Mail-Konfiguration**

* **Zulassungsliste** – Die Zulassungsliste kann jetzt in einer Nicht-Produktions-Sandbox über einen API-Aufruf aktiviert und deaktiviert werden. [Weitere Informationen](allow-list.md#enable-allow-list)
* **Navigation**  - Die Unterdrückungsliste, auf die über das Menü  **Administration > Kanäle > E-Mail-Konfiguration >** Allgemein zugegriffen werden kann, wurde in das neue Untermenü  **Unterdrückung** verschoben, in dem alle zugehörigen Funktionen für einen einfacheren Zugriff zusammengefasst sind. [Weitere Informationen](configuration/manage-suppression-list.md#access-suppression-list)

**Entscheidungs-Management**

* Die Art und Weise, wie Sie beim Erstellen eines Angebots Darstellungen hinzufügen und konfigurieren, wurde aktualisiert, um das Benutzererlebnis zu verbessern. Insbesondere wird die Asset-Bibliothek jetzt nur angezeigt, wenn Sie Bildinhalte für eine Darstellung definieren. [Weitere Informationen](offers/offer-library/creating-personalized-offers.md#representations)

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
<p>Weitere Informationen finden Sie in der <a href="event/experience-event-schema.md#leverage_schema_relationships">entsprechenden Dokumentation</a>.</p>
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
<p>Weitere Informationen finden Sie in der <a href="allow-list.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journey**

* Die Gesamteinschränkungsrate aller Segment-Lesen-Schritte, die gleichzeitig in derselben Sandbox ausgeführt werden, ist auf 17.000 Nachrichten pro Sekunde beschränkt. [Mehr dazu](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Das Feld **Aufbewahrungsfrist im Cache** wurde aus dem Konfigurationsbereich der Datenquelle entfernt. [Mehr dazu](datasource/about-data-sources.md)
* Für externe Datenquellen ist jetzt automatisch eine Begrenzungsregel von 15 Aufrufen pro Sekunde definiert. [Mehr dazu](configuration/external-systems.md#capping)
* Für Live-Journeys werden im Journey-Eigenschaftsfenster das Veröffentlichungsdatum und der Name des Benutzers angezeigt, der die Journey veröffentlicht hat. [Mehr dazu](building-journeys/journey-gs.md#change-properties)
* Im Journey-Listenfenster wurde ein Filter für den Journey-Typ hinzugefügt. [Mehr dazu](user-interface.md#section_lgm_hpz_pgb)
* Der Parameter **[!UICONTROL Einschränkungsrate]** wurde in der Aktivität „Segment lesen“ hinzugefügt. [Mehr dazu](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Nachrichtenvorschau und Testversand**

* Identität und Namespace sind nun im Bildschirm **[!UICONTROL Vorschau]** sichtbar. [Mehr dazu](preview.md#preview-your-messages)
* Die Anzahl der Test-E-Mails für Testsendungen ist jetzt auf 10 beschränkt.
* Die Anzahl der für das **Präfix der Betreffzeile** in Testsendungen zulässigen Zeichen ist jetzt begrenzt. [Mehr dazu](preview.md#send-proofs)

**Ausdruckseditor für Personalisierung**

* Die Dropdown-Liste „Helper“ wurde umbenannt und neu angeordnet.

### Fehlerbehebungen

* Fehlerkorrektur – Jetzt werden keine doppelten Nachrichten mehr während des Batch-E-Mail-Versands gesendet.
* Fehlerkorrektur – Ereignisse werden jetzt entsprechend generiert, wenn nach Ablauf des Wiederholungszeitraums kein E-Mail-Versand mehr durchgeführt wird.
* Fehlerkorrektur – Im Bildschirm „PTR-Datensätze“ fehlen jetzt keine IP-Informationen mehr.
* Fehlerkorrektur – Die Lokalisierung in der Angebotsleiste im Ausdruckseditor ist jetzt implementiert.
* Fehlerkorrektur – Der Abstand in Informations-Popups ist jetzt korrekt.
* Fehlerkorrektur – Beim Hochladen einer HTML-Datei in Email Designer wird jetzt das interne Stylesheet mit der Eigenschaft `background-image` unterstützt.
