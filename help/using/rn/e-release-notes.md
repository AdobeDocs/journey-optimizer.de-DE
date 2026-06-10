---
solution: Journey Optimizer
product: journey optimizer
title: Vorab veröffentlichte Versionshinweise zu Journey Optimizer
description: Vorab veröffentlichte Versionshinweise zu Adobe Journey Optimizer
feature: Release Notes
hide: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 51d356bfab2f989422d43c5e6582901519f5ebf1
workflow-type: tm+mt
source-wordcount: 1851
ht-degree: 10%

---


# Vorab veröffentlichte Versionshinweise {#e-release-notes}

Adobe Journey Optimizer bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

## Hinweise zur Vorabversion vom 26. Juni {#june-26-rn}

**Die nachfolgenden Vorab- Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentationen werden veröffentlicht, sobald Änderungen in der Produktion live sind. Die meisten Änderungen werden am Veröffentlichungsdatum bereitgestellt, einige werden jedoch möglicherweise später eingeführt. Weitere Informationen finden Sie unter Verfügbarkeitsdatum für jeden Eintrag.

Siehe auch [Vorab veröffentlichte Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Veröffentlichungsdatum**: 16.-17. Juni 2026


### Journeys {#june-26-journeys}

In dieser Version wurden die folgenden Funktionen und Verbesserungen für Journey implementiert.

<table>
<thead>
<tr>
<th><strong>Journey-Schlichtung - Formeln</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt <strong>Formeln</strong> verwenden, um Journey basierend </strong> Kundenprofilattributen und Kontextfaktoren automatisch <strong>zu priorisieren und zu schlichten), um sicherzustellen, dass Kunden die relevantesten Journey eingeben.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14719">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

* **Erhöhte Live-Journey-Grenze und neue**: Sie können jetzt bis zu **200 aktive Journey-** haben, die gegenüber der vorherigen Grenze von 100 erhöht wurden.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14826">Link zur DOCAC JIRA-Aufgabe</a>

* **Start- und Enddatum im Journey-Header** - Wenn Start- und/oder Enddatum auf einer Live-Journey konfiguriert sind, werden sie jetzt in der Kopfzeile **Journey** neben dem Live-Status-Badge angezeigt. Die angezeigte Beschriftung passt sich an, je nachdem, ob jedes Datum bevorsteht oder bereits vergangen ist.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14702">Link zur DOCAC JIRA-Aufgabe</a>

* **Angehalten oder Anhaltende Journey direkt schließen** - Sie können jetzt **eine Journey anhalten oder bei neuen Eintritten schließen** direkt aus dem Status **Angehalten**. Zuvor musste eine angehaltene Journey wieder live geschaltet werden, bevor sie angehalten oder geschlossen werden konnte.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14229">Link zur DOCAC JIRA-Aufgabe</a>

* **Zusätzliche Kennungsunterstützung für externe Zielgruppen** - Zusätzliche Kennungen in Journey werden jetzt für externe Zielgruppen unterstützt, einschließlich Zielgruppen, die aus einer CSV-Datei importiert wurden, und Zielgruppen, die mit Federated Audience Composition erstellt wurden. Sie können ein beliebiges Nicht-Identitätsattribut oder ein beliebiges Identitätsattribut aus der Zielgruppe als zusätzliche ID festlegen. Es ist keine Schemakennzeichnung erforderlich.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14541">Link zur DOCAC JIRA-Aufgabe</a>

### Orchestrierte Kampagnen {#june-26-oc}

Orchestrierte Kampagnen in dieser Version weisen die folgenden Funktionen und Verbesserungen auf.

<table>
<thead>
<tr>
<th><strong>Laden der Dateiaktivität in orchestrierten Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Orchestrierte Kampagnen unterstützen jetzt das Laden einer <strong>CSV- oder TXT-Datei</strong> direkt in die Kampagnen-Arbeitsfläche als Zielgruppe, ohne die Datei zuerst in Adobe Experience Platform aufzunehmen. Die Dateidaten werden zur Ausführungszeit genutzt und nicht als Adobe Experience Platform-Datensatz beibehalten. Während der Dateieinrichtung können Sie Spaltenzuordnungen, Datentypen, die NULL-Verarbeitung und Fehlerrichtlinien pro Spalte definieren. Dies unterstützt Ad-hoc-Sendungen oder Partnerlisten-Kampagnen, bei denen der Aufbau einer vollständigen Aufnahme-Pipeline nicht praktisch ist.</p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14704">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

* **Schleifenbasierte Personalisierung für relationale Daten in orchestrierten Kampagnen** - Der Personalisierungseditor unterstützt jetzt einen **Schleifenblock**, der relationale Sammlungen wie Bestellungen, Konten oder Buchungen durchläuft und einen Inhaltsblock pro Datensatz in einer einzelnen E-Mail oder SMS rendert. Sammlungen werden über die Datenauswahl mithilfe von Personalisierungs-Token konfiguriert, ohne dass ein Ausdruck geschrieben werden muss.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14703">Link zur DOCAC JIRA-Aufgabe</a>

* **Personalisieren von E-Mail-Absenderdetails pro Empfänger und Kampagne** - Orchestrierte Kampagnen unterstützen jetzt die Personalisierung von **E-Mail-Header-Feldern**, einschließlich Absendername, Absenderadresse und Antwortadresse, mithilfe von Profilattributen oder relationalen Daten. Auf diese Weise können Absenderdetails den relevanten Berater, Standort oder die Zweigstelle für jeden Empfänger widerspiegeln, anstatt alle Sendungen über eine einzelne Unternehmensadresse weiterzuleiten. Header-Werte können auf Kanalebene festgelegt und pro Kampagne überschrieben werden, indem kontextuelle Daten verwendet werden, um die Kontrolle zu verbessern.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13761">Link zur DOCAC JIRA-Aufgabe</a>

* **Überschreiben des Standard-Ausführungsfelds in Kampagnen** - Zuvor auf Journey-Ebene verfügbar, können Sie jetzt das Standard-**Ausführungsfeld** überschreiben, das in den Kampagnenparametern global für Ihre E-Mail-, SMS- und WhatsApp-Sendungen festgelegt ist.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14718">Link zur DOCAC JIRA-Aufgabe</a>

### Entscheidungsfindung {#june-26-decisioning}

In dieser Version wird die folgende Funktion zur Entscheidungsfindung verwendet.

<table>
<thead>
<tr>
<th><strong>Verwenden von Adobe Experience Manager-Inhaltsfragmenten in Decisioning</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt <strong>Adobe Experience Manager-Inhaltsfragmente</strong> in Decisioning <strong>Entscheidungselementen</strong> zuordnen und diese in Entscheidungsrichtlinien nutzen, um das richtige Fragment zum richtigen Zeitpunkt für den richtigen Kunden bereitzustellen.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14885">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

### E-Mail-Kanal {#june-26-email}

In dieser Version werden die folgenden Funktionen und Verbesserungen für den E-Mail-Kanal bereitgestellt.

<table>
<thead>
<tr>
<th><strong>Erweiterte Komponenten - Layouts (Super-Komponenten)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die E-Mail-Designer enthält jetzt eine <strong>Bibliothek mit einsatzbereiten Layout-Komponenten</strong> wie Kopf- und Produktkarten (1, 2 oder 3 Spalten), Informationsblöcke und Fußzeilen, die Sie per Drag-and-Drop direkt auf die E-Mail-Arbeitsfläche ziehen können. Jede Komponente verfügt über vorkonfigurierte bearbeitbare Eigenschaften (Bild, Titel, Text, Schaltfläche, Links) und kann über die WYSIWYG-Benutzeroberfläche vollständig angepasst werden, wodurch die E-Mail-Erstellung beschleunigt wird, ohne dass Sie Strukturen von Grund auf neu erstellen müssen.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14877">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Inhaltsprüfung in E-Mail Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Journey Optimizer können Benutzer jetzt ihre <strong>E-Mail-Inhaltsqualität</strong> einschließlich Lesbarkeit, Effektivität und Inhaltskohärenz direkt in der Benutzeroberfläche von E-Mail-Designer überprüfen.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14870">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Reduzierung der E-Mail-Größe aktivieren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dieser neuen Option können Sie <strong>Größe der HTML reduzieren</strong> in einer E-Mail, indem Sie unnötige Leerzeichen, Kommentare und redundanten Code entfernen - ohne das Aussehen der E-Mail zu ändern. Dies verbessert die Zustellbarkeit (einige E-Mail-Anbieter lehnen übergroße E-Mails ab oder kennzeichnen sie) und kann die Ladezeit für Empfänger verkürzen.</p>
<p>Verfügbarkeitsdatum: 10. Juni 2026</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14777">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

* **Unterstützung des Textmodus in Fragmenten** - Um textbasierte E-Mail-Workflows zu unterstützen, können Sie jetzt **Textversionen** Ihrer visuellen Fragmente erstellen und verwalten, um sie in der Nur-Text-Version von E-Mails zu verwenden, die dieses Fragment enthalten. Bei Verwendung eines Fragments, das vor der aktuellen Version erstellt wurde, kann die Textversion des Fragments falsch gerendert werden - sowohl in der E-Mail-Designer als auch in der endgültigen E-Mail, die an Ihre Empfängerinnen und Empfänger gesendet wird. Um optimale Ergebnisse mit älteren Fragmenten zu erzielen, bearbeiten, speichern und veröffentlichen Sie jedes Fragment erneut.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14204">Link zur DOCAC JIRA-Aufgabe</a>

* **Aktualisierte Benchmarks für den Batch-Versanddurchsatz mit kundenorientierten Szenarien** - Die **Benchmarks für den Batch-Versanddurchsatz** von Adobe Journey Optimizer wurden aktualisiert, um die Leistung in Produktionsqualität für mehrere Personalisierungsszenarien widerzuspiegeln - von einfachen Sendungen bis hin zu komplexen dynamischen Inhalten mit bedingter Logik. Die aktualisierten Metriken sind jetzt in der Produktdokumentation verfügbar, damit Kunden ihre Messaging-Volumes genau planen können.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14816">Link zur DOCAC JIRA-Aufgabe</a>

* **Feedback Loop OTP-Prozess für benutzerdefinierte Subdomains** - Der Konfigurationsprozess für benutzerdefinierte Subdomains (FBL) wurde verbessert, indem der Yahoo Sender Hub **One-Time Password (OTP)** direkt in der Produktoberfläche angezeigt wird. Benutzer können jetzt automatisch das OTP abrufen und anzeigen, das während der Verifizierung der Eigentümerschaft der Yahoo Sender Hub-Domain generiert wurde.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14815">Link zur DOCAC JIRA-Aufgabe</a>

### Mobile Messaging (SMS, MMS, RCS und LINE) {#june-26-mobile}

In dieser Version wurden folgende Verbesserungen für Mobile Messaging vorgenommen.

* **Eindeutige Klicks für SMS-Berichte** - Für SMS-Berichte wurde das neue Modul **Eindeutige Klicks** eingeführt, wodurch die Leistung von SMS nun genauso präzise verfolgt wird wie bei E-Mail-Berichten.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14895">Link zur DOCAC JIRA-Aufgabe</a>

* **LINE-Kanal - Authoring-**: Die Benutzeroberfläche des LINE-Kanals wurde um erweiterte Funktionen zur Nachrichtenerstellung erweitert. Diese Version bietet Unterstützung für **mehrere Nachrichtenformate** einschließlich Text, Bild, Imagemap, Karussell und Flex (JSON-Editor) sowie Gerätevorschauen in Echtzeit. Benutzer können jetzt gruppierte Nachrichten mit bis zu fünf sortierten Nachrichten verwalten (mit den Steuerelementen Hinzufügen, Entfernen und Neu anordnen) und den integrierten Personalisierungseditor für validierte, dynamische Nachrichten nutzen.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14869">Link zur DOCAC JIRA-Aufgabe</a>

* **SMS - Nutzungsmetriken anzeigen** - Für Kundinnen und Kunden, die SMS direkt über Adobe Journey Optimizer erwerben, **ein neues**SMS-Nutzungs-Dashboard) eingeführt. Sie können jetzt Ihre letzten 90 Tage der Nachrichten-Versandmetriken anzeigen und verfolgen, die nach von Mobilgeräten stammenden (MO) und von Mobilgeräten beendeten (MT) Nachrichten kategorisiert sind. Diese Daten können auch über CSV heruntergeladen werden, was eine bessere Sichtbarkeit und Kontrolle über Ihre SMS-Ausgaben ermöglicht.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14345">Link zur DOCAC JIRA-Aufgabe</a>

### Inhalte und Integrationen {#june-26-content}

In dieser Version werden die folgenden Funktionen und Verbesserungen bei Content-Management und Integrationen eingeführt.

<table>
<thead>
<tr>
<th><strong>Verbesserungen an Adobe Experience Manager-Inhaltsfragmenten in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Diese Version bietet mehrere Verbesserungen, um <strong>Adobe Experience Manager</strong>Inhaltsfragmente innerhalb von Journey Optimizer-Authoring-Workflows nutzbarer, besser kontrollierbar und produktionsbereiter zu machen:</p>
<ul>
<li>Journey Optimizer unterstützt jetzt das Abrufen von Inhaltsfragmenten aus mehreren Adobe Experience Manager-Konfigurationen, einschließlich der Autoren-, Veröffentlichungs- und authentifizierten Veröffentlichungsebenen.</li>
<li>Sobald ein Fragment ausgewählt wurde, wird sein Kontext in der gesamten Nachricht beibehalten, sodass Autoren Fragmentfelder über Inhaltsblöcke hinweg wiederverwenden können, ohne die Auswahl erneut durchzuführen.</li>
<li>In Journey Optimizer wurde eine neue spezielle Seite zur Auflistung von Inhaltsfragmenten eingeführt, um die Lebenszyklusverwaltung zu verbessern. Benutzende können nicht synchronisierte Fragmente und manuelle Synchronisierungen von Triggern identifizieren, um auf dem neuesten Stand zu bleiben.</li>
<li>Die Unterstützung von Gebietsschemata und Varianten ermöglicht es Marketing-Experten jetzt, gezielter mit alternativen Versionen desselben Inhaltsfragments zu arbeiten.</li>
<li>Sie können jetzt flexibel darauf zugreifen, wie Adobe Journey Optimizer auf Ihre Adobe Experience Manager-Inhalte zugreift. Diese Version bietet die Möglichkeit, <strong> Quell-Repository für Inhaltsfragmente </strong> wechseln, die in Ihren Journey und Kampagnen verwendet werden.</li>
<li>Jetzt, mit <b>Managed Services</b> kompatibel, können Sie Adobe Experience Manager-Inhaltsfragmente direkt in Journey Optimizer anzeigen, darauf zugreifen und sie zur Personalisierung verwenden. Fügen Sie einfach Ihre Adobe Experience Manager Managed Services-Repository-URL in den Konfigurationseinstellungen als einmaliges Setup hinzu.</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14686">Link zur JIRA-Aufgabe DOCAC</a></p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14821">Link zur JIRA-Aufgabe DOCAC</a></p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14684">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integration des KI-Assistenten mit Adobe Experience Manager Asset Essentials</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der KI-Assistent ruft jetzt automatisch <b>markenbestätigte Bilder</b> direkt aus Ihrer Adobe Experience Manager Assets ab, wenn E-Mails, Web-Seiten und Push-Benachrichtigungen generiert werden. Dadurch entfällt die Notwendigkeit, die Assets manuell zu durchsuchen oder sich auf generische KI-Fallbacks zu verlassen, um sicherzustellen, dass jedes Bild perfekt präzise und markenkonform ist.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14761">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

### Benutzerdefinierte Kanäle {#june-26-channels}

In dieser Version stehen den Kanälen die folgenden Funktionen zur Verfügung.

<table>
<thead>
<tr>
<th><strong>Benutzerdefinierter ausgehender Kanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer führt jetzt <strong>Benutzerdefinierte Kanäle</strong> ein, eine neue Funktion, mit der Administratoren ausgehende HTTP-basierte Nachrichtenkanäle - wie WeChat, Kakao Talk, Messenger oder ein proprietärer Anbieter - über einen <strong>Code-Kanal-Builder</strong> direkt in AJO einbringen können. Nach der Konfiguration sind benutzerdefinierte Kanäle in allen Kampagnen, Journey und orchestrierten Kampagnen verfügbar und haben die gleichen umfassenden Funktionen wie native Kanäle: Personalisierung mit dem Ausdruckseditor, Inhaltsexperimentierung, Vorschau und Testversand, vorkonfiguriertes Reporting sowie die Durchsetzung von Einverständnis und Governance. Dadurch wird die Lücke gefüllt, die zuvor durch benutzerdefinierte Aktionen geschlossen wurde, die auf Journey beschränkt waren und denen es an dedizierter Inhaltserstellung fehlte.</p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11381">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

### Berichterstellung {#june-26-reporting}

In dieser Version werden die folgenden Verbesserungen beim Reporting vorgenommen.

* **Neue geschätzte Klickmetriken für E-Mail- und SMS-Reporting** - Um eine genauere Übersicht über die tatsächliche Kundeninteraktion zu erhalten, sind jetzt neue geschätzte Metriken in Journey-, Kampagnen- und Kanalberichten verfügbar. Diese Metriken helfen beim Filtern nicht-menschlicher Interaktionen (NHI) und Bot-Klicks aus Berichtsdaten:
   * Geschätzte Klicks: Gesamtzahl der gezählten Klicks nach der Entfernung von identifiziertem Traffic, der nicht von Personen oder Bots stammt.
   * Geschätzte CTR: Geschätzte Klicks im Verhältnis zu den gesamten Sendungen.
   * Geschätzter CTOR nur für E-Mail: Geschätzte Klicks im Verhältnis zu den geschätzten Öffnungen.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14354">Link zur DOCAC JIRA-Aufgabe</a>

### Konfiguration {#june-26-configuration}

In dieser Version werden die folgenden Verbesserungen bei der Konfiguration und Administration vorgenommen.

* **Web Application Firewall (WAF) IP Whitelisting für AJO-Landingpages** - Adobe Journey Optimizer unterstützt jetzt **Web Application Firewall (WAF) IP Whitelisting** für Landingpages, sodass Unternehmen durchsetzen können, dass alle eingehenden Anfragen ausschließlich über ihre konfigurierte WAF-Infrastruktur weitergeleitet werden. Mit dieser Verbesserung können Kundinnen und Kunden AJO so konfigurieren, dass direkte Anfragen, die die WAF-Ebene umgehen, abgelehnt werden. So wird sichergestellt, dass in Tools wie Imperva definierte Sicherheitsrichtlinien konsistent angewendet werden. Diese Funktion verbessert die Sicherheitslage für Unternehmen mit strengen Anforderungen an den Netzwerkzugriff und gibt ihnen die volle Kontrolle über den Traffic-Fluss zu ihren von AJO gehosteten Landingpages.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14814">Link zur DOCAC JIRA-Aufgabe</a>

* **Datensatz wechselt vom Streaming- in den Batch** Modus - Der AJO-Nachrichten-Feedback-Ereignisdatensatz wechselt vom Streaming- in **Batch-Erfassungsmodus**. Durch diese Änderung wird sichergestellt, dass die Datenaufnahme die Streaming-Aufnahmebeschränkungen nicht überschreitet. Wenn Sie diesen Datensatz in Customer Journey Analytics-Berichten verwenden oder Abfragen dafür ausführen, erwarten Sie in Zukunft eine Zunahme der Datenlatenz von bis zu 2 Stunden.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14771">Link zur DOCAC JIRA-Aufgabe</a>

### Verbesserungen der Benutzerfreundlichkeit {#june-26-usability}

In dieser Version wird die folgende Verbesserung der Benutzerfreundlichkeit eingeführt.

* **Ordner für Journey und Kampagnen** - Sie können Ihre Journey und Kampagnen jetzt in **Ordner** organisieren, um die Navigation und Verwaltung in der Benutzeroberfläche zu verbessern.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14038">Link zur DOCAC JIRA-Aufgabe</a>

