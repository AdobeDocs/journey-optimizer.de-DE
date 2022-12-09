---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise 2022
description: Versionshinweise zu Journey Optimizer 2022
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '3479'
ht-degree: 0%

---

# Versionshinweise 2022 {#release-notes-2022}

Auf dieser Seite werden alle Funktionen und Verbesserungen für [!DNL Journey Optimizer] veröffentlicht im Jahr 2022.


## Version September 2022{#sept-2022-release}

### Neue Funktionen{#sept-2022-features}

<table>
<thead>
<tr>
<th><strong>Dynamischer Inhalt und neuer bedingter Regel-Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt dynamischen Inhalt erstellen, um den Inhalt Ihrer Nachrichten basierend auf bedingten Regeln anzupassen.</p> 
<p>Bedingte Regeln werden mit einem visuellen Regel-Builder im Ausdruckseditor erstellt, in dem Sie sie zur weiteren Wiederverwendung in Ihren Journeys und Kampagnen speichern können.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../personalization/get-started-dynamic-content.md">Detaillierte Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API-gesteuerte Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Zusätzlich zu bereits geplanten Kampagnen können Sie jetzt API-gesteuerte Kampagnen in Journey Optimizer erstellen und diese über APIs von einem externen System aus aufrufen.</p>
<p>Auf diese Weise können Sie verschiedene betriebliche und Transaktionsnachrichten abdecken, wie z. B. Kennwortrücksätze, OTP-Token usw.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../campaigns/api-triggered-campaigns.md">Detaillierte Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Data Access Control</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mithilfe der attributbasierten Zugriffskontrolle können Administratoren den Zugriff auf bestimmte Objekte anhand bestimmter Attribute steuern. Diese Attribute können Metadaten sein, die einem Objekt hinzugefügt werden, z. B. Beschriftungen. Ab dieser Version können Administratoren auch Benutzerrollen definieren, die nur Zugriff auf bestimmte Felder und/oder Objekte haben, sowie Daten, die diesen Feldern und/oder Objekten entsprechen.</p>
<p> Die Verwendung der attributbasierten Zugriffskontrolle ist derzeit auf ausgewählte Kunden beschränkt und wird in einer zukünftigen Version für alle Umgebungen bereitgestellt.</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../administration/object-based-access.md">Detaillierte Dokumentation</a>.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Data Governance und Datenschutz</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dem Data Usage Labeling and Enforcement (DULE)-Governance-Framework kann Journey Optimizer jetzt Governance-Richtlinien von Adobe Experience Platform nutzen, um zu verhindern, dass sensible Felder durch benutzerdefinierte Aktionen in Drittanbietersysteme exportiert werden. Wenn das System in den benutzerdefinierten Aktionsparametern ein eingeschränktes Feld identifiziert, wird ein Fehler angezeigt, der die Veröffentlichung der Journey verhindert.</p>
<p>Die Verwendung von DULE (Data Usage Labeling and Enforcement) ist derzeit auf ausgewählte Kunden beschränkt und wird in einer zukünftigen Version in allen Umgebungen bereitgestellt.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../action/action-privacy.md">Detaillierte Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Automatisierte Durchsetzung von Einverständniserklärungen (Einverständnisrichtlinien)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Adobe Experience Platform können Sie einfach Marketing-Richtlinien übernehmen und durchsetzen, um die Zustimmungsvoreinstellungen Ihrer Kunden zu respektieren. Einverständnisrichtlinien werden in Adobe Experience Platform definiert. In Journey Optimizer können Sie diese Zustimmungsrichtlinien auf Ihre benutzerdefinierten Aktionen anwenden. Beispielsweise können Sie Einwilligungsrichtlinien definieren, um Kunden auszuschließen, die dem Empfang von E-Mail-, Push- oder SMS-Nachrichten nicht zugestimmt haben.
<p>Die automatisierte Einverständnisvollstreckung ist derzeit nur für Organisationen verfügbar, die das Zusatzangebot zum Gesundheitsschild erworben haben.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../action/consent.md">Detaillierte Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Berechtigungsverwaltung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer unterstützt das Definieren von Benutzerrollen und Zugriffsrichtlinien zum Verwalten von Berechtigungen für Funktionen und Objekte. bis <strong>Adobe Experience Cloud-Berechtigungen</strong>können Sie Rollen erstellen und verwalten sowie die gewünschten Ressourcenberechtigungen für diese Rollen zuweisen. Mit Berechtigungen können Sie auch die Bezeichnungen, Sandboxes und Benutzer verwalten, die einer bestimmten Rolle zugeordnet sind.</p>
<p> Die Verwendung von Berechtigungen ist derzeit auf ausgewählte Kunden beschränkt und wird in einer zukünftigen Version in allen Umgebungen bereitgestellt.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../administration/attribute-based-access.md">Detaillierte Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Benachrichtigung und Überwachung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Als Benutzer von Journey Optimizer können Sie jetzt über die Benutzeroberfläche auf Systemwarnungen zugreifen, um Benachrichtigungen zu erhalten, wenn Journeys nicht wie erwartet funktionieren. Sie können die verfügbaren Warnungen anzeigen und abonnieren. Der erste Warnhinweis, der mit dieser Version verfügbar ist, warnt Sie, wenn eine Aktivität vom Typ Segment lesen im festgelegten Zeitraum kein Profil verarbeitet hat. Nach dem Entsperren dieses Workflows werden weitere Änderungen folgen.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../reports/alerts.md">Detaillierte Dokumentation</a>.
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Data Hygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform provides a suite of data hygiene capabilities that allow you manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. </p>
<p>You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.</p>
<p><strong>Caution</strong> - Data Hygiene capabilities are currently only available for organizations that have purchased the Healthcare Shield add-on offering.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### Verbesserungen{#sept-2022-improvements}

**Journeys**

* Die **Entitätsdatensatz** ist jetzt als vordefinierter Datensatz in Adobe Journey Optimizer verfügbar. Dieser Lookup-Datensatz enthält Metadaten zur Anreicherung der Tracking- und Feedback-Datensatzinformationen. Auf diese Weise können Sie Ihre Berichte und Abfragen mit leichter verständlichen Daten verbessern. [Weitere Infos](../data/datasets-query-examples.md#entity-dataset)
* Eine neue Limits wurde zu einheitlichen Journeys hinzugefügt (angefangen bei einem Ereignis oder einer Segmentqualifikation), um zu verhindern, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Eintritt von Profilen wird jetzt standardmäßig fünf Minuten lang vorübergehend blockiert. [Weitere Infos](../start/guardrails.md#events-g)

**Administration**

* Beim Aktivieren oder Deaktivieren der Zulassungsliste wird nun eine neue Warnung mit Details zu den Auswirkungen jeder Aktion angezeigt. [Weitere Infos](../configuration/allow-list.md#enable-allow-list)
* Die Benutzeroberfläche zum Erstellen von Kanaloberflächen, Erstellen von IP-Pools, Verwalten der Unterdrückungsliste und der Zulassungsliste sowie Konfigurieren des SMS-Kanals wurde aktualisiert.
* Beim Erstellen der ersten Kanaloberfläche für eine bestimmte Subdomain dauert die Verarbeitungszeit 10 Minuten bis 10 Tage und bei nachfolgenden Oberflächen, die diese Subdomain verwenden, bis zu 3 Stunden. [Weitere Infos](../configuration/channel-surfaces.md#create-channel-surface)
* Die Benutzeroberfläche zum Erstellen von Landingpage-Vorgaben und Landingpage-Subdomains wurde aktualisiert - [Weitere Infos](../landing-pages/lp-subdomains.md)

**Auditkontrollen**

* Mit Journey Optimizer können Sie Aktionen identifizieren, die von Benutzern im System für verschiedene Dienste und Funktionen wie Kampagnen, Journeys, Nachrichten, Landingpages usw. ausgeführt werden. Auditprotokollressourcen enthalten jetzt Änderungen an verschiedenen anderen Aktionen und werden automatisch aufgezeichnet, wenn die Aktivität stattfindet. Weitere Infos [auf dieser Seite](../privacy/audit-logs.md).

**Archivierungsunterstützung**

* Die neue **Entitätsdatensatz** enthält ein Feld Vorlage , mit dem Sie das Format und die Struktur der gesendeten Nachrichten zu Archivierungszwecken in alle Kanäle exportieren können. [Weitere Infos](../configuration/archiving-support.md)

**Landingpages**

* Sie können jetzt Kontextdaten verwenden, die von einer anderen Seite innerhalb derselben Landingpage stammen. Wenn Sie beispielsweise ein Kontrollkästchen mit einer Abonnementliste auf der primären Landingpage verknüpfen, können Sie diese Abonnementliste auf der Unterseite &quot;Vielen Dank!&quot;verwenden. [Weitere Infos](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Sonstige Änderungen{#sept-2022-other}

* Der Journey Burst-Modus wurde durch den Campaign-Modus für den schnellen Versand ersetzt. [Weitere Infos](../campaigns/create-campaign.md#rapid-delivery)
* Um die Leistung zu verbessern, können Feldergruppen für Erlebnisereignisse nicht mehr in Journeys verwendet werden, die mit einem Segment lesen, einer Segmentqualifikation oder einer Business-Event-Aktivität beginnen. Diese Änderung gilt nur für neue Journeys. Vorhandene Verhaltensweisen behalten das aktuelle Verhalten bei. [Weitere Infos](../start/guardrails.md#expression-editor)
* Die Beschränkung von 1 Stunde für geplante Journeys von Lesesegmenten wurde entfernt. Diese Journeys können jetzt ohne Verzögerung ausgeführt werden.




## Version August 2022 {#aug-2022-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Erstellen und Verwalten von Kampagnen in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verwenden Sie Journey Optimizer-Kampagnen, um einmalige Inhalte mithilfe verschiedener Kanäle für ein bestimmtes Segment bereitzustellen. Bei der Verwendung von Journeys sind Aktionen so konzipiert, dass sie nacheinander ausgeführt werden. Bei Kampagnen werden Aktionen gleichzeitig, entweder sofort oder basierend auf einem festgelegten Zeitplan ausgeführt. </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>Erfahren Sie, wie Sie eine Kampagne im <a href="../campaigns/get-started-with-campaigns.md">Detaillierte Dokumentation</a> und <a href="https://video.tv.adobe.com/v/346680">Feature Video</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>SMS an Ihre Benutzer senden (allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt SMS in Journey Optimizer erstellen, personalisieren und senden, indem Sie eine Integration mit <b>Sinch</b> oder <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Hier erfahren Sie, wie Sie eine SMS erstellen und senden. <a href="../sms/create-sms.md">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Verbesserungen

**Berichterstellung**

* Die Tabelle mit den Einwilligungsrichtlinien und das Diagramm sind jetzt in den globalen Journey-Berichten verfügbar. Mit diesen Widgets können Sie die ausgeschlossenen Profile aus den Richtlinien in Ihren benutzerdefinierten Aktionen verfolgen. [Weitere Infos](../reports/journey-global-report.md#journey-global)

   Um Zugriff auf die neuesten Widgets zu erhalten, müssen Sie die verschiedenen Berichts-Dashboards zurücksetzen. Weiterführende Informationen zur Dashboard-Anpassung finden Sie im Abschnitt [die ausführliche Dokumentation](../reports/global-report.md).

**Administration**

* Jetzt ist es möglich, die für den SMS-Kanal zu verwendende primäre Telefonnummer zu aktualisieren. [Weitere Infos](../configuration/primary-email-addresses.md)


## Version Juli 2022 {#july-2022-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Neuer Inline-Messaging-Fluss</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer bietet einen neuen Fluss für die Nachrichtenbearbeitung in Journeys. Durch die Inline-Benachrichtigung sparen Benutzer erheblich Zeit und optimieren den Workflow-Prozess zum Erstellen und Versand einer E-Mail, einer Push-Benachrichtigung oder einer SMS in Journey Optimizer. Wenn Sie Nachrichten als separaten Schritt entfernen und sie stattdessen im Rahmen einer Aktion auf der Journey-Arbeitsfläche bearbeitbar machen, müssen Benutzer auf weniger Schaltflächen klicken und weniger Bildschirme navigieren, um ihren Inhalt zu entwerfen und zu bearbeiten.</p>
<img src="assets/do-not-localize/inline.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Attributbasierte Zugriffssteuerung (begrenzte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Jetzt können Sie Schemafelder mit Bezeichnungen identifizieren, die Organisations- oder Datennutzungsbereiche definieren. Administratoren können über die Benutzeroberfläche "Berechtigungen"Zugriffsrichtlinien für XDM-Schemafelder definieren und den Zugriff für Benutzer oder Benutzergruppen (interne, externe oder externe Benutzer) besser verwalten sowie den Zugriff auf bestimmte Datentypen (d. h. sensible personenbezogene Daten/EPD) verwalten.</p>
<p>Die Verwendung der attributbasierten Zugriffssteuerung ist derzeit auf ausgewählte Benutzer beschränkt und wird in einer zukünftigen Version für alle Umgebungen bereitgestellt.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../administration/attribute-based-access.md">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Batch-Entscheidungsaufträge</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Batch-Entscheidungsaufträge über die Benutzeroberfläche ausführen, sodass ich keinen Entwickler benötige, um Batch-API-Aufträge auszuführen, und ich kann die für das Marketing benötigte Zeit verkürzen. Mit dieser neuen Benutzeroberfläche können Sie Aufträge erstellen und aktuelle/frühere Aufträge verwalten.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../offers/batch-delivery.md">ausführliche Dokumentation.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Automatisches Verwenden des Angebots mit der besten Leistung bei Ihren Entscheidungen (begrenzte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt personalisierte Optimierungsmodellsysteme im Entscheidungs-Management verwenden. Dieser neue Modelltyp ermöglicht die Optimierung und Personalisierung von Angeboten basierend auf Segmenten und der Angebotsleistung.</p>
<p>Die Verwendung personalisierter KI-Modelle zur Optimierung ist derzeit auf ausgewählte Benutzer beschränkt und wird in einer zukünftigen Version in allen Umgebungen bereitgestellt.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../offers/ranking/personalized-optimization-model.md">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journeys**

* **Beenden einer Journey** - Auf der Arbeitsfläche der Journey muss die **Ende** -Aktivität wurde aus der Palette entfernt. End-Tags werden jetzt standardmäßig am Ende jedes Pfades hinzugefügt und können nicht entfernt werden. Diese Verbesserung ermöglicht eine bessere Berichterstellung darüber, wo ein Kunde die Journey abgebrochen hat, ohne dass vom Journey-Experten Maßnahmen erforderlich sind. Siehe Abschnitt [Dokumentation](../building-journeys/end-journey.md) und [Feature Video](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}.


* Die **Zeitzone des Profils** in den Journey-Eigenschaften jetzt standardmäßig deaktiviert. [Weitere Infos](../building-journeys/timezone-management.md#timezone-from-profiles)

**Nachrichten**

* Nachrichtenvorgaben sind jetzt **Kanaloberflächen**. [Weitere Infos](../configuration/channel-surfaces.md)

**Administration**

* **PTR-Record-Bearbeitung** - Beim Aktualisieren eines PTR-Datensatzes dauert die Verarbeitungszeit nur bis zu 3 Stunden. [Weitere Infos](../configuration/ptr-records.md#processing)

* **Benutzeroberfläche für zulässige Listen** - Sie können jetzt die Benutzeroberfläche von Journey Optimizer verwenden, um der Zulassungsliste neue E-Mail-Adressen oder Domänen hinzuzufügen. [Weitere Infos](../configuration/allow-list.md)

* **Aktualisierung der zulässigen Listenlogik** - Die Logik der zulässigen Liste gilt nun, sobald die Funktion aktiviert ist, auch wenn die Liste leer ist. [Weitere Infos](../configuration/allow-list.md#logic)

* **URL-Tracking-Parameter** - Sie können jetzt den Ausdruckseditor verwenden, um URL-Tracking-Parameter auf Ihren E-Mail-Oberflächen (d. h. Vorgaben) zu konfigurieren. [Weitere Infos](../email/email-settings.md#url-tracking)

**Entscheidungsmanagement**

* **Zielgruppengröße** - Eine neue Schätzung der Zielgruppengröße wird jetzt in der Benutzeroberfläche angezeigt, wenn eine Entscheidungsregel erstellt wird, wenn ein Segment oder eine Regel zum Festlegen einer Angebotseignung ausgewählt oder ein Segment oder eine Regel zu einem Entscheidungsbereich hinzugefügt wird.


## Version Juni 2022 {#june-2022-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>SMS an Ihre Benutzer senden (begrenzte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt SMS in Journey Optimizer erstellen, personalisieren und senden, indem Sie eine Integration mit <b>Sinch</b> oder <b>Twilio</b>.</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>Der SMS-Kanal ist derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie von Ihrem Adobe-Support-Mitarbeiter.</p>
<p>Hier erfahren Sie, wie Sie eine SMS erstellen und senden. <a href="../sms/create-sms.md">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Schnellere Suche nach effektiveren Bildern mit der Adobe Stock-Integration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Das Integrations-Plug-in Adobe Stock und Adobe Journey Optimizer Email Designer bietet Kunden eine einfache Möglichkeit, Bilder zur Verwendung bei der Nachrichtenbearbeitung zu navigieren, zu lizenzieren und zu speichern. </br> Die neue <b>Ähnliche Stock-Fotos suchen</b> ermöglicht Ihnen auch, Stock-Fotos zu finden, die mit Inhalt, Farbe und Komposition Ihrer Bilder übereinstimmen. </p>
<!--img src="assets/do-not-localize/stock-rn.gif"/-->
<p>Weitere Informationen finden Sie im Abschnitt <a href="../email/stock.md">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>E-Mail-BCC für alle E-Mails verwenden</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt die Funktion E-Mail-BCC (Blind Carbon Copy) verwenden, um von Adobe Journey Optimizer gesendete E-Mails zu speichern. Aktivieren Sie diese Option in Ihren E-Mail-Vorgaben, damit jede gesendete E-Mail blind in Ihre BCC-Adresse kopiert wird.</p>
<!--img src="assets/do-not-localize/bcc-rn.gif"/-->
<p>Weitere Informationen finden Sie im Abschnitt <a href="../configuration/archiving-support.md#bcc-email">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Objekte zwischen Sandboxes kopieren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können nun die Erlebnisse von einer Journey Optimizer-Sandbox in eine andere neu erstellen, z. B. von einer Nicht-Produktions-Sandbox zu einer Produktions-Sandbox. Mit dieser neuen Funktion wird eine gesamte Journey kopiert, einschließlich aller Objekte, von denen die Journey für die korrekte Ausführung abhängig ist, von einer Umgebung in eine andere. Zusätzlich zu Journeys können Sie auch andere Komponenten kopieren, z. B. Angebote, Nachrichten, Schemata, Datensätze, Datenquellen, Ereignisse und Aktionen.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../building-journeys/copy-to-sandbox.md">Detaillierte Dokumentation</a>.
</td>
</tr>
</tbody>
</table>




### Verbesserungen

**Entscheidungsmanagement**

* **Unterstützung von HTML- und JSON-Dateien** - Sie können jetzt externe HTML- und JSON-Dateien aus der Adobe Experience Cloud Asset-Bibliothek in den Inhalt der Angebotsdarstellung ziehen. [Weitere Infos](../offers/offer-library/add-representations.md#html-json)


**Email**

* **Als Vorlage speichern** - Jetzt können Sie E-Mail-Inhalte als Vorlage speichern und sie bei der Erstellung anderer Nachrichten wiederverwenden. [Weitere Infos](../email/email-templates.md)


**Administration**

* **Vorschau von Tracking-URL-Parametern** - Wenn Sie bei der Konfiguration einer Nachrichtenvorgabe URL-Tracking-Parameter definieren, wird jetzt eine dynamische Vorschau der resultierenden Tracking-URL angezeigt. [Weitere Infos](../email/email-settings.md#url-tracking)

* **Nachrichtenvorgabenbearbeitung** - Beim Aktualisieren einer Nachrichtenvorgabe kann die Verarbeitungszeit jetzt nur noch 3 Stunden dauern. [Weitere Infos](../configuration/channel-surfaces.md#edit-channel-surface)

* **IP-Poolbearbeitung** - Beim Aktualisieren eines IP-Pools kann die Verarbeitungszeit jetzt nur noch bis zu 3 Stunden dauern. [Weitere Infos](../configuration/ip-pools.md#edit-ip-pool)




## Version Mai 2022 {#may-2022-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Regeln zur Nachrichtenhäufigkeit</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt kanalübergreifende Geschäftsregeln festlegen, mit denen Profile, die zu oft angesprochen wurden, automatisch aus Nachrichten und Aktionen ausgeschlossen werden.</p>
<!--img src="assets/do-not-localize/frequency-rn.gif"/-->
<p>Weitere Informationen finden Sie im Abschnitt <a href="../configuration/frequency-rules.md">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Entscheidungsverwaltung - Automatisch optimiertes AI-Ranking-Modell</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt trainierte Modellsysteme im Entscheidungsmanagement verwenden. Mit dieser neuen Funktion werden Angebote nach Rang geordnet, die für ein bestimmtes Profil angezeigt werden.</p>
<!--img src="assets/do-not-localize/optimization.gif"/-->
<p>Weitere Informationen finden Sie im Abschnitt <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Auditprotokolle von Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Aktionen überwachen, die von Benutzern auf Adobe Journey Optimizer-Ressourcen ausgeführt werden.</p>
<!--img src="assets/do-not-localize/audit-rn.gif"/-->
<p>Weitere Informationen finden Sie im Abschnitt <a href="../privacy/audit-logs.md">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Personalisierung**

* **Neue Hilfsfunktion für ausgeblendete Zeichen** - die `mask` Mit der Hilfsfunktion können Sie einen Teil einer Zeichenfolge durch &quot;X&quot;-Zeichen ersetzen. [Weitere Infos](../personalization/functions/string.md#mask)

**Landingpages**

* **Landingpages ohne Formular** - Sie können jetzt eine Landingpage erstellen und veröffentlichen, die kein Formular enthält und keine Aktion von Besuchern erfordert.
* **Landingpage-Vorlagen** - Jetzt können Sie eine Landingpage als Vorlage speichern und sie bei der Erstellung anderer Landingpages wiederverwenden. [Weitere Infos](../landing-pages/lp-templates.md)
* **Zurück zur primären Seite** - Sie können nun von einer beliebigen Unterseite innerhalb derselben Landingpage aus einen Link zur primären Seite hinzufügen.
* **Benutzerdefinierte JavaScript-Unterstützung** - Sie können jetzt benutzerdefinierten JavaScript-Code zu Ihren Landingpage-Inhalten hinzufügen, um erweiterte Formatierungen durchzuführen oder Ihren Landingpages benutzerspezifische Verhaltensweisen hinzuzufügen.    [Weitere Infos](../landing-pages/lp-custom-js.md)

**Journeys**

* **Segment lesen** - Einmalige Lesen von Segment-Journeys wechseln 30 Tage nach der Ausführung der Journey in den Status Abgeschlossen . Bei geplanten Read-Segmenten ist es 30 Tage nach der Ausführung des letzten Vorkommens. [Weitere Infos](../building-journeys/read-segment.md)
* **Ausdruckseditor** - die [limit](../building-journeys/functions/functionlimit.md) wurde hinzugefügt, damit Sie die Anzahl der Elemente einer Liste begrenzen können. Die [sort](../building-journeys/functions/functionsort.md) -Funktion können Sie nun ein Listenobjekt sortieren. Die Unterstützung von listObject wurde auch der [distinct](../building-journeys/functions/functiondistinct.md) und [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) Funktionen.

**Administration**

* **Aktualisierung des Lizenzverwendungs-Dashboards** - Das Dashboard zur Lizenzverwendung im [!DNL Adobe Journey Optimizer] Die Benutzeroberfläche spiegelt jetzt den genauen Wert für die **Lizenziert** Durchschnittliche Reichweite des Profils. In dieser Metrikdarstellung wird ein Rückgang angezeigt, was bedeutet, dass die Lizenzbeschränkung jetzt korrekt gemeldet wird. [Weitere Infos](../segment/license-usage.md)


## Version April 2022 {#april-2022-release}

### Verbesserungen

**Landingpages**

* **Neue Option für Opt-in-/Opt-out-Checkboxes** - Sie können jetzt eine einzige Checkbox für das Opt-in/Opt-out in Abonnement-Landingpages einfügen. Benutzer müssen das Kontrollkästchen aktivieren, um zuzustimmen (Opt-in), und es deaktivieren, um ihre Zustimmung zu entfernen (Opt-out). [Weitere Infos](../landing-pages/design-lp.md#define-lp-specific-content)

* **Felder für Landingpages vorbefüllen** - Benutzer können jetzt die Landingpage-Felder mit Profilinformationen vorab ausfüllen. [Weitere Infos](../landing-pages/create-lp.md#configure-primary-page)

**Entscheidungsmanagement**

* **Decisioning-API in Edge** - Die Edge Decisioning-API kann personalisierte Angebote bereitstellen und rendern, die im Entscheidungsmanagement verwaltet werden. Sie können Ihre Angebote und andere verwandte Objekte mithilfe der Entscheidungs-Management-Benutzeroberfläche (UI) oder APIs erstellen. [Weitere Infos](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Administration**

* **PTR-Sendedauer** - Die Dauer der PTR-Bearbeitung ist jetzt ein paar Stunden. [Weitere Infos](../configuration/ptr-records.md#processing)

**Email Design**

* **20 neue E-Mail-Vorlagen** sind jetzt verfügbar, um Ihren E-Mail-Inhalt in Journey Optimizer zu erstellen.

**Benutzeroberfläche**

* **Kontexthilfe in der Benutzeroberfläche von Journey Optimizer** - Auf mehreren Seiten in Journey Optimizer wurden Links zur kontextuellen Hilfe hinzugefügt. Wenn verfügbar, klicken Sie auf das Symbol &quot;i&quot;, um eine kurze Beschreibung der aktuellen Funktion anzuzeigen und auf zugehörige Artikel zuzugreifen.

**Integration mit Adobe Campaign Standard**

Als Adobe Campaign Standard-Kunde können Sie jetzt mit Journey Optimizer E-Mails, Push-Benachrichtigungen und SMS versenden. Verwenden Sie die neuen integrierten Aktionen, um die Transaktionsnachrichten-Funktionen von Campaign Standard in Journey Optimizer zu nutzen.  [Weitere Infos](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## Version März 2022 {#march-2022-release}

### Verbesserungen

**Journeys**

* Um zu vermeiden, dass im einheitlichen Profilschema unnötige Felder vorhanden sind, ist das Journey Step Event-Schema nicht mehr standardmäßig für Profile aktiviert. Bei Bedarf können Sie sie aktivieren. [Weitere Infos](../reports/sharing-overview.md)
* Neue Schrittereignisse im Zusammenhang mit Exportvorgängen werden jetzt von Journey Optimizer an Adobe Experience Platform gesendet. Beispiele für Abfragen wurden der Dokumentation hinzugefügt. [Weitere Infos](../reports/query-examples.md)

**Entscheidungsmanagement**

* Sie können jetzt festlegen, ob die Angebotsbegrenzung für alle Benutzer oder für ein bestimmtes Profil sowie für alle Platzierungen oder pro Platzierung gilt. [Weitere Infos](../offers/offer-library/add-constraints.md#capping)
* Mit der Batch Decisioning-API können Unternehmen Entscheidungsverwaltungsfunktionen für alle Profile in einem bestimmten Segment in einem Aufruf verwenden. Der Angebotsinhalt für jedes Profil im Segment wird in einem AEP-Datensatz platziert, wo er für benutzerdefinierte Batch-Workflows verfügbar ist. [Weitere Infos](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Administration**

* Sie können jetzt den Abmelde-Link im/vom E-Mail-Header auf der Vorgabenebene der Nachricht aktivieren/deaktivieren und eine benutzerdefinierte Abmelde-URL auf Meldungsebene festlegen. [Weitere Infos](../configuration/channel-surfaces.md#list-unsubscribe)
* Die Zulassungsliste kann jetzt über die [!DNL Journey Optimizer] -Schnittstelle für Produktions- und Nicht-Produktions-Sandboxes. [Weitere Infos](../configuration/allow-list.md#enable-allow-list)

**Personalisierung**

* Sie können jetzt mehr als 40 Personalisierungsausdrücke in der Bibliothek speichern. [Weitere Infos](../personalization/personalization-library.md)

## Version Februar 2022 {#feb-2022-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Abonnement-Landingpages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Landingpages in Journey Optimizer erstellen und entwerfen und Ihre Benutzer zu Online-Formularen weiterleiten, über die sie sich anmelden oder abmelden können, wenn sie Ihre Nachrichten erhalten oder einen bestimmten Dienst wie einen Newsletter abonnieren.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../landing-pages/create-lp.md">Detaillierte Dokumentation</a> und verwandte <a href="../landing-pages/lp-use-cases.md">Beispielanwendungsfall</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Neue Ausdrucksbibliothek für Personalisierung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer bietet jetzt eine Bibliothek, in der Sie auf vordefinierte Personalisierungsausdrücke zugreifen können. Diese Ausdrücke werden von Admin-Benutzern konfiguriert.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../personalization/personalization-library.md">Detaillierte Dokumentation</a>.</p>
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
The suppression list helps you with honoring the ISPs' feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
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
<p>In Journey Optimizer-Nachrichteninhalten können Sie Ihren Links jetzt UTM-Parameter hinzufügen: Sie können zusätzliche Daten zu diesem Link bereitstellen und Ihnen dabei helfen, herauszufinden, wo und warum eine Person auf Ihren Link geklickt hat.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../configuration/channel-surfaces.md#configure-email-settings">Detaillierte Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journeys**

* Um die Leistung zu optimieren, wechseln alle Journeys im Testmodus, die seit einer Woche nicht ausgelöst wurden, jetzt wieder in den Entwurfsstatus. [Mehr dazu](../building-journeys/testing-the-journey.md#important_notes)
* Die Integration zwischen Journey Optimizer und Adobe Campaign Classic wurde optimiert, um die Leistung zu verbessern. Die Standardkonfiguration für Begrenzungen wurde auf 4000 Aufrufe/5 Minuten geändert.    [Mehr dazu](../action/acc-action.md#important-notes)

**Berichterstellung**

* Sendungen können nun nach ihrem Status gefiltert werden:
   * In der Liste Nachrichtenausführung können Sie jetzt Testsendungen aus der Versandliste ausschließen.
   * Aus Ihren Live-/Global-Berichten können Sie auswählen, ob Sie Testereignisse ausschließen möchten.

* Sie können jetzt auf Berichte zu Sendezeitoptimierungsdaten zugreifen: die Anzahl der Personen, die unmittelbar Nachrichten waren, die Anzahl der Personen, die mit einer 1-Stunden-Optimierung, einer 2-Stunden-Optimierung usw. benachrichtigt wurden.

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Entscheidungsmanagement**

* Rankings und KI-Rankings werden jetzt in einem Tab zusammengefasst.

## Version Januar 2022 {#january-2022-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Journeys - Optimieren Sie Ihren IP-Ramp mit Profilbegrenzungsbedingungen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Beim Konfigurieren von <strong>Bedingung</strong> -Aktivität in einer Journey können Sie jetzt eine Profilbegrenzung definieren. Mit diesem neuen Bedingungstyp können Sie eine maximale Anzahl von Profilen für einen Journey-Pfad festlegen. Wenn diese Grenze erreicht ist, nehmen die Eingabeprofile einen alternativen Pfad an. Auf diese Weise können Sie das Volumen Ihrer Sendungen erhöhen (IP-Ramp-up). Sie können beispielsweise Ihre Sendungen in einer Domain zusammenfassen, indem Sie die Ausführung aufteilen: 1000 Nachrichten am Tag 1, 2000 usw. zu senden.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../building-journeys/condition-activity.md#profile_cap">Detaillierte Dokumentation</a> und verwandte <a href="../building-journeys/ramp-up-deliveries-uc.md">Beispielanwendungsfall</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journeys - Verbesserung von Segmenten lesen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die <strong>Inkrementelles Lesen</strong> wurde zur wiederkehrenden <strong>Segment lesen</strong> Aktivitäten. Mit dieser Option können Sie nur Kontakte ansprechen, die seit der letzten Ausführung der Journey in das Segment eingestiegen sind. Die erste Ausführung zielt immer auf alle Segmentmitglieder ab.</p>
<p>Weitere Informationen finden Sie im Abschnitt <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">Detaillierte Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journeys**

* Journey Optimizer-Schrittereignisse können jetzt mit anderen Datensätzen in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html). Die **profileID** -Feld im integrierten Journey Step Event-Schema jetzt als Identitätsfeld definiert. [Weitere Infos](../reports/sharing-overview.md#integration-cja)

**Entscheidungsmanagement**

* Wenn Sie ein Angebot, Fallback-Angebot, eine Angebotskollektion oder eine Angebotsentscheidung aktualisieren, auf die direkt oder indirekt in einer veröffentlichten Nachricht verwiesen wird, werden die Aktualisierungen automatisch in der entsprechenden Nachricht widergespiegelt, ohne dass sie erneut veröffentlicht werden müssen. [Weitere Infos](../offers/offers-e2e.md#insert-decision-in-email)

* Bei der Simulation, welche Angebote für ein bestimmtes Testprofil bereitgestellt werden sollen, können Sie jetzt die Standardsimulationseinstellungen ändern und den Code anzeigen, der Ihren Simulationen entspricht, die zur Fehlerbehebung verwendet werden können. [Weitere Infos](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administration**

* Administratoren können jetzt PTR-Einträge mit einer Subdomain bearbeiten, die mit CNAME eingerichtet ist. [Weitere Infos](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalisierung**

* **Zu Favoriten hinzufügen** - Um die Effizienz bei der Arbeit mit Personalisierungen zu verbessern, haben wir das Konzept der Speicherung von Favoriten eingeführt. Durch das Hinzufügen verschiedener Attribute zum Favoritenmenü erhalten Sie schnellen Zugriff auf die am häufigsten verwendeten Elemente. [Weitere Infos](../personalization/personalize.md#fav)
