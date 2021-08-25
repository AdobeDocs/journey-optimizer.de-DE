---
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
source-git-commit: ff48c78cfa5c48f32073e9df1f126504e291ab5a
workflow-type: tm+mt
source-wordcount: '995'
ht-degree: 38%

---


# Versionshinweise {#release-notes}

Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für [!DNL Journey Optimizer] aufgelistet. Sie können auch die neusten [Aktualisierungen der Dokumentation](documentation-updates.md) einsehen.


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
<p>Senden Sie Ihre Push- oder E-Mail-Benachrichtigung automatisch zum besten Zeitpunkt für jeden Kunden, den Sie mit Adobe Journey Optimizer verbinden. Die Sendezeitoptimierung basiert auf den KI-Diensten von Adobe und sagt die beste Sendezeit für E-Mails oder Push-Nachrichten voraus, um die Interaktion basierend auf historischen Öffnungs- und Klickraten vorkonfiguriert zu maximieren.</p>
<p>Diese Funktion befindet sich derzeit in der Betaversion und steht nur Beta-Kunden zur Verfügung. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Betaprogramm teilzunehmen.</p>
<p>Weitere Informationen finden Sie in der <a href="building-journeys/journeys-message.md#send-time-optimization">entsprechenden Dokumentation</a>.</p>
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
<p>Sie können jetzt beim Konfigurieren von Geschäftsereignissen Beziehungen zwischen Schemas nutzen. Dies bietet zusätzlich die Möglichkeit, Felder aus verknüpften Tabellen beim Konfigurieren eines Einzelereignisses, bei der Verwendung von Bedingungen in einer Journey, bei der Nachrichtenpersonalisierung und bei der Personalisierung benutzerdefinierter Aktionen zu nutzen.</p>
<p>Weitere Informationen finden Sie in der <a href="event/experience-event-schema.md#leverage_schema_relationships">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>
<!--
<table>
<thead>
<tr>
<th><strong>Personalized URLs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Personalized URLs take recipients to specific pages of a website, or to a personalized microsite, depending on the profile attributes. In Adobe Journey Optimizer, you can now add personalization to URLs in your message content. URL personalization can be applied to text and images, and use profile data or contextual data.</p>
<p>For more information, refer to the <a href="documentation-updates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

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
<p>Weitere Informationen finden Sie in der <a href="configuration/retries.md">entsprechenden Dokumentation</a>.</p>
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

* **Dynamische Header**  - Sie können jetzt dynamische Daten in HTTP-Header-Parametern übergeben. Diese Parameter können von den Integrationssystemen verwendet werden, die die HTTP-Aufrufe der Journey-Aktion empfangen, z. B. Zeitstempel oder Tracking-ID. [Weitere Informationen](action/about-custom-action-configuration.md#url-configuration)
* **Dynamische URL-Pfade**  - Sie können jetzt dynamische URL-Pfade für benutzerdefinierte Aktionen einrichten. [Weitere Informationen](action/about-custom-action-configuration.md#url-configuration)
* Die Gesamtdrosselungsrate für Lesesegmente wurde von 17.000 auf 20.000 Nachrichten pro Sekunde geändert. [Mehr dazu](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Benutzeroberfläche**

* **Suche**  - Auf jeder Seite können Sie jetzt Geschäftsobjekte und Hilfeartikel direkt über das Suchfeld &quot;Einheitliches Experience Cloud&quot;durchsuchen. [Weitere Informationen](user-interface.md#unified-search)
* **Neuigkeiten**  - Die Anzeige von Elementen der neuesten Version von der Adobe Journey Optimizer-Startseite wird jetzt auf weitere Geschäftsobjekte erweitert. Mit diesem Update umfassen die kürzlich aufgerufenen Verknüpfungen Nachrichten, Journey, Segmente, Schemas, Datensätze, Datenquellen, Ereignisse, Aktionen, Quellen und Ziele. [Weitere Informationen](action/about-custom-action-configuration.md#passing-collection)

**Inhaltserstellung**

* **Hintergrund**  - Hintergrundbilder werden jetzt in der Live-Vorschau unterstützt. [Weitere Informationen](preview.md)
* **Ein-Klick-Ausschluss-Link**  - Sie können einen neuen Link-Typ in Ihren E-Mail-Inhalt einfügen: Mit dem  **Opt-** out-Link können sich Benutzer von der Anmeldung für Ihre Nachrichten mit nur einem Klick abmelden, ohne zu einer Landingpage weitergeleitet zu werden, um die Abmeldung zu bestätigen. [Weitere Informationen](message-tracking.md#one-click-opt-out-link)

**Personalisierung**

* **Ausdruckseditor**  - Bei der Definition der Personalisierung können Sie jetzt einfach einen Fallback-Wert hinzufügen: Wenn das Personalisierungsfeld für ein Profil leer ist, wird der Fallback-Wert angezeigt. [Weitere Informationen](documentation-updates.md)

**E-Mail-Konfiguration**

* **Zulassungsliste**  - Die Zulassungsliste kann jetzt in einer Nicht-Produktions-Sandbox über einen API-Aufruf aktiviert und deaktiviert werden. [Weitere Informationen](allow-list.md#enable-allow-list)

<!--* **Suppression list** - Adding email addresses and domains into the suppression list is now available from the user interface, either one by one, either in bulk mode through a CSV file upload. [Learn more](configuration/manage-suppression-list.md#add-addresses-and-domains)-->
<!--* **Navigation** - The suppression list, which was accessible under the **Channels > Email configuration > General** menu, has been moved to the **Channels > Email configuration > Suppression list** menu for easier access. [Learn more](configuration/manage-suppression-list.md#access-suppression-list)-->


### Fehlerbehebungen

* Es wurde ein Problem mit der Barrierefreiheit in der Navigation auf der Meldungsregisterkarte behoben.
* Es wurde ein Lokalisierungsproblem in den E-Mail-Designer-Bezeichnungen behoben.
* Fehlerkorrektur - Es wurde ein Problem behoben, das bei der Auswahl von mehr als einem Knoten in einer Journey und beim Klicken auf &quot;Löschen&quot;im Eigenschaftsbereich auftrat.
* Fehlerkorrektur - Eine neue Kopfzeile kann jetzt zu einer in einer Journey verwendeten Aktion hinzugefügt werden.
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
<p>Sie können jetzt Beziehungen zwischen Schemas nutzen, um einen Datensatz als Lookup-Tabelle für einen anderen zu verwenden. Sie können dann alle Felder der verknüpften Tabellen bei der Konfiguration eines Einzelereignisses, bei der Verwendung von Bedingungen in einer Journey, bei der Nachrichtenpersonalisierung und bei der Personalisierung benutzerdefinierter Aktionen nutzen.</p>
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
* Fehlerkorrektur - Beim Hochladen einer HTML-Datei in Email Designer wird jetzt das interne Stylesheet mit der Eigenschaft `background-image` unterstützt.

