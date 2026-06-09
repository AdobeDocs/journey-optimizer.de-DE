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
source-git-commit: 00a8edd899673e2c2cf738df8a28dd53e085b680
workflow-type: tm+mt
source-wordcount: 2274
ht-degree: 6%

---


# Vorab veröffentlichte Versionshinweise {#e-release-notes}

Adobe Journey Optimizer bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

## Hinweise zur Vorabversion vom 26. Juni {#june-26-rn}

**Die nachfolgenden Vorab- Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentationen werden veröffentlicht, sobald Änderungen in der Produktion live sind. Die meisten Änderungen werden am Veröffentlichungsdatum bereitgestellt, einige werden jedoch möglicherweise später eingeführt. Weitere Informationen finden Sie unter Verfügbarkeitsdatum für jeden Eintrag.

Siehe auch [Vorab veröffentlichte Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Veröffentlichungsdatum**: 16.-17. Juni 2026

### Treue {#june-26-loyalty}

Die folgende Funktion wird in dieser Version auf „Treue“ angewendet.

<table>
<thead>
<tr>
<th><strong>Herausforderungen bezüglich der Treue</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Herausforderungen im Zusammenhang mit der Treue machen aus Treueinitiativen ansprechende, Gamified-Erlebnisse, die Kunden zu wertvollen Aktionen motivieren, z. B. Käufe tätigen, Bewertungen schreiben, in sozialen Medien interagieren oder Freunde verweisen.</p>
<p>Administratoren können das Menü „Treueprogramm-Admin“ verwenden, um Journey Optimizer mit Ihrem Treueprogramm-Ökosystem zu verbinden, einschließlich APIs für die Belohnungserfüllung, Ereignisdefinitionen, Produktinventar, Ausschlüsse und Identitätseinstellungen. Marketer können dann standardmäßige, Streak- oder sequenzielle Herausforderungen entwerfen, Aufgaben und Belohnungen definieren, eigene Inhaltskarten und Nachrichten bereitstellen und die Leistung mit integrierten Reporting-Dashboards überwachen. Journey Optimizer generiert die Journey, die jede Challenge im Hintergrund koordinieren, sodass sich die Teams auf das Kundenerlebnis und die Geschäftsziele konzentrieren können.</p>
<p>Diese Funktion ist jetzt für alle Umgebungen verfügbar (allgemeine Verfügbarkeit).</p>
</td>
</tr>
</tbody>
</table>

### Journeys {#june-26-journeys}

In dieser Version wurden die folgenden Funktionen und Verbesserungen für Journey implementiert.

<table>
<thead>
<tr>
<th><strong>Journey-Pfadoptimierung - Targeting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verwenden Sie den neuen Knoten Optimieren , um bestimmte Zielgruppen anzusprechen und den besten Pfad zur Erfüllung Ihrer geschäftsorientierten KPIs zu bestimmen.</p>
<p>Mit diesem Tool können Sie effektivere Marketing-Kampagnen entwickeln, die mit größerer Wahrscheinlichkeit auf 1:1-Ebene Resonanz finden, die Marketing-Personalisierungsbemühungen für Kunden verbessern und wichtige KPIs für die Kundeninteraktion wie Konversionen und Umsatz verbessern.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Schlichtung - Formeln</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Formeln verwenden, um anhand von Kundenprofilattributen und Kontextfaktoren automatisch die Journey-Prioritätswerte zu erhöhen und so sicherzustellen, dass Kunden in die relevantesten Journey eintreten.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
</td>
</tr>
</tbody>
</table>

* **Erhöhte Live-Journey-Beschränkung und neue**: Sie können jetzt bis zu 200 aktive Journey haben, die gegenüber der vorherigen Beschränkung von 100 erhöht wurden.

* **Start- und Enddatum im Journey-Header** - Wenn Start- und/oder Enddatum auf einer Live-Journey konfiguriert sind, werden sie jetzt in der Journey-Kopfzeile neben dem Live-Status-Badge angezeigt. Die angezeigte Beschriftung passt sich an, je nachdem, ob jedes Datum bevorsteht oder bereits vergangen ist.

* **Angehalten oder Anhaltende Journey direkt schließen** - Sie können jetzt eine Journey anhalten oder sie für neue Eintritte direkt aus dem angehaltenen Zustand schließen. Zuvor musste eine angehaltene Journey wieder live geschaltet werden, bevor sie angehalten oder geschlossen werden konnte.

* **Zusätzliche ID-Unterstützung in Journey für externe Zielgruppen** - Zusätzliche IDs in Journey werden jetzt für externe Zielgruppen unterstützt, einschließlich Zielgruppen, die aus einer CSV-Datei importiert wurden, und Zielgruppen, die mit Federated Audience Composition erstellt wurden. Sie können ein beliebiges Nicht-Identitätsattribut oder ein beliebiges Identitätsattribut aus der Zielgruppe als zusätzliche ID festlegen. Es ist keine Schemakennzeichnung erforderlich.

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
<p>Orchestrierte Kampagnen unterstützen jetzt das direkte Laden einer CSV- oder TXT-Datei in die Kampagnen-Arbeitsfläche als Zielgruppe, ohne die Datei zuerst in Adobe Experience Platform aufnehmen zu müssen. Die Dateidaten werden zur Ausführungszeit genutzt und nicht als Adobe Experience Platform-Datensatz beibehalten. Während der Dateieinrichtung können Sie Spaltenzuordnungen, Datentypen, die NULL-Verarbeitung und Fehlerrichtlinien pro Spalte definieren. Dies unterstützt Ad-hoc-Sendungen oder Partnerlisten-Kampagnen, bei denen der Aufbau einer vollständigen Aufnahme-Pipeline nicht praktisch ist.</p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Unterstützung der ruhigen Stunden für koordinierte Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt ruhige Stunden auf orchestrierte Kampagnen anwenden. Mit der Funktion „Ruhige Stunden“ können Sie zeitbasierte Ausschlüsse definieren, um zu verhindern, dass Nachrichten zu bestimmten Zeiten gesendet werden. So können Sie Kundenpräferenzen und Compliance-Anforderungen in allen Anwendungsfällen für die Kampagnenorchestrierung erfüllen.</p>
</td>
</tr>
</tbody>
</table>

* **Schleifenbasierte Personalisierung für relationale Daten in orchestrierten Kampagnen** - Der Personalisierungseditor unterstützt jetzt einen Schleifenblock, der relationale Sammlungen wie Bestellungen, Konten oder Buchungen durchläuft und einen Inhaltsblock pro Datensatz in einer einzelnen E-Mail oder SMS rendert. Sammlungen werden über die Datenauswahl mithilfe von Personalisierungs-Token konfiguriert, ohne dass ein Ausdruck geschrieben werden muss.

* **E-Mail-Absenderdetails nach Empfänger und Kampagne personalisieren** - Orchestrierte Kampagnen unterstützen jetzt die Personalisierung von E-Mail-Header-Feldern, einschließlich Absendername, Absenderadresse und Antwortadresse, mithilfe von Profilattributen oder relationalen Daten. Auf diese Weise können Absenderdetails den relevanten Berater, Standort oder die Zweigstelle für jeden Empfänger widerspiegeln, anstatt alle Sendungen über eine einzelne Unternehmensadresse weiterzuleiten. Header-Werte können auf Kanalebene festgelegt und pro Kampagne überschrieben werden, indem kontextuelle Daten verwendet werden, um die Kontrolle zu verbessern.

* **Vereinfachung der Zielgruppendimension in orchestrierten Kampagnen** - Die aktive Zielgruppendimension wird jetzt auf der Workflow-Arbeitsfläche angezeigt, sodass Sie sehen können, welche Dimension von einer Kanalaktivität verwendet wird. Der Segmentierungsfluss für mehrere Entitäten ist einfacher, da Sie keine separate Aktivität vom Typ „Dimensionsänderung“ mehr benötigen. Darüber hinaus können Sie jetzt explizit auswählen, ob Nachrichten auf Profilebene oder auf sekundärer Dimensionsebene gesendet werden sollen.

* **Standard-Ausführungsfeld in Kampagnen überschreiben** - Zuvor auf Journey-Ebene verfügbar, können Sie jetzt das Standard-Ausführungsfeld überschreiben, das in den Kampagnenparametern global für Ihre E-Mail-, SMS- und WhatsApp-Sendungen festgelegt ist.

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
<p>Sie können jetzt Adobe Experience Manager-Inhaltsfragmente Entscheidungselementen in Decisioning zuordnen und sie in Entscheidungsrichtlinien nutzen, um das richtige Fragment zum richtigen Zeitpunkt für den richtigen Kunden bereitzustellen.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
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
<p>Die E-Mail-Designer enthält jetzt eine Bibliothek mit einsatzbereiten Layout-Komponenten - wie Kopf- und Produktkarten (1, 2 oder 3 Spalten), Informationsblöcke und Fußzeilen -, die Sie direkt in die E-Mail-Arbeitsfläche ziehen und dort ablegen können. Jede Komponente verfügt über vorkonfigurierte bearbeitbare Eigenschaften (Bild, Titel, Text, Schaltfläche, Links) und kann über die WYSIWYG-Benutzeroberfläche vollständig angepasst werden, wodurch die E-Mail-Erstellung beschleunigt wird, ohne dass Sie Strukturen von Grund auf neu erstellen müssen.</p>
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
<p>Mit Journey Optimizer können Benutzer jetzt ihre E-Mail-Inhaltsqualität - einschließlich Lesbarkeit, Effektivität und Inhaltskohärenz - direkt über die Benutzeroberfläche von E-Mail-Designer überprüfen.</p>
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
<p>Mit dieser neuen Option können Sie die Größe der HTML in einer E-Mail reduzieren, indem Sie unnötige Leerzeichen, Kommentare und redundanten Code entfernen, ohne das Aussehen der E-Mail zu ändern. Dies verbessert die Zustellbarkeit (einige E-Mail-Anbieter lehnen übergroße E-Mails ab oder kennzeichnen sie) und kann die Ladezeit für Empfänger verkürzen.</p>
<p>Verfügbarkeitsdatum: 10. Juni 2026</p>
</td>
</tr>
</tbody>
</table>

* **Unterstützung des Textmodus in Fragmenten** - Um textbasierte E-Mail-Workflows zu unterstützen, können Sie jetzt Textversionen Ihrer visuellen Fragmente erstellen und verwalten, um sie optimal in der Nur-Text-Version von E-Mails zu verwenden, die dieses Fragment enthalten. Bei Verwendung eines Fragments, das vor der aktuellen Version erstellt wurde, kann die Textversion des Fragments falsch gerendert werden - sowohl in der E-Mail-Designer als auch in der endgültigen E-Mail, die an Ihre Empfängerinnen und Empfänger gesendet wird. Um optimale Ergebnisse mit älteren Fragmenten zu erzielen, bearbeiten, speichern und veröffentlichen Sie jedes Fragment erneut.

* **Aktualisierte Benchmarks für den Batch-Versanddurchsatz mit kundenorientierten Szenarien** - Die Benchmarks für den Batch-Versanddurchsatz von Adobe Journey Optimizer wurden aktualisiert, um die Leistung in Produktionsqualität für mehrere Personalisierungsszenarien widerzuspiegeln - von einfachen Sendungen bis hin zu komplexen dynamischen Inhalten mit bedingter Logik. Die aktualisierten Metriken sind jetzt in der Produktdokumentation verfügbar, damit Kunden ihre Messaging-Volumes genau planen können.

* **Feedback Loop OTP-Prozess für benutzerdefinierte Subdomains** - Der Konfigurationsprozess für benutzerdefinierte Subdomains (FBL) wurde verbessert, indem der Yahoo Sender Hub One-Time Password (OTP) direkt in der Produktoberfläche eingeblendet wurde. Benutzer können jetzt automatisch das OTP abrufen und anzeigen, das während der Verifizierung der Eigentümerschaft der Yahoo Sender Hub-Domain generiert wurde.

* **Bot-Klicks für E-Mail- und SMS-Reporting ausschließen** - Um eine genauere Übersicht über die tatsächliche Kundeninteraktion zu erhalten, sind jetzt neue Schätzmetriken für die Journey-, Kampagnen- und Kanalberichte verfügbar. Diese Metriken helfen beim Filtern nicht menschlicher Interaktionen (NHI) und Bot-Klicks aus Berichtsdaten: Geschätzte Klicks (Gesamtzahl der Klicks, die nach dem Entfernen des identifizierten Bot- und nicht menschlichen Traffics gezählt wurden), geschätzte CTR (geschätzte Klicks im Verhältnis zur Gesamtzahl der Sendungen) und Geschätzte CTR nur für E-Mails (geschätzte Klicks im Verhältnis zur geschätzten Öffnung).

### Mobile Messaging (SMS, MMS, RCS und LINE) {#june-26-mobile}

In dieser Version wurden folgende Verbesserungen für Mobile Messaging vorgenommen.

* **Eindeutige Klicks für SMS-Berichte** - Für SMS-Berichte wurde das neue Modul Eindeutige Klicks eingeführt, wodurch die Leistung von SMS genau so präzise verfolgt wird wie derzeit für E-Mail-Berichte.

* **LINE-Kanal - Authoring-**: Die Benutzeroberfläche des LINE-Kanals wurde um erweiterte Funktionen zur Nachrichtenerstellung erweitert. Diese Version bietet Unterstützung für mehrere Nachrichtenformate, einschließlich Text, Bild, Imagemap, Karussell und Flex (JSON-Editor), sowie für Gerätevorschauen in Echtzeit. Benutzer können jetzt gruppierte Nachrichten mit bis zu fünf sortierten Nachrichten verwalten (mit den Steuerelementen Hinzufügen, Entfernen und Neu anordnen) und den integrierten Personalisierungseditor für validierte, dynamische Nachrichten nutzen.

* **Journey Optimizer Resell - Nutzungsmetriken anzeigen** - Für Kunden, die SMS direkt über Adobe Journey Optimizer erwerben, wurde ein neues SMS-Nutzungs-Dashboard eingeführt. Sie können jetzt Ihre letzten 90 Tage der Nachrichten-Versandmetriken anzeigen und verfolgen, die nach von Mobilgeräten stammenden (MO) und von Mobilgeräten beendeten (MT) Nachrichten kategorisiert sind. Diese Daten können auch über CSV heruntergeladen werden, was eine bessere Sichtbarkeit und Kontrolle über Ihre SMS-Ausgaben ermöglicht.

### Inhalte und Integrationen {#june-26-content}

In dieser Version werden die folgenden Funktionen und Verbesserungen bei Content-Management und Integrationen eingeführt.

<table>
<thead>
<tr>
<th><strong>Inhaltsfragmente mit Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Diese Version bietet mehrere Verbesserungen, um Adobe Experience Manager-Inhaltsfragmente innerhalb von Journey Optimizer-Authoring-Workflows benutzerfreundlicher, kontrollierbarer und produktionsbereiter zu machen:</p>
<ul>
<li>Journey Optimizer unterstützt jetzt das Abrufen von Inhaltsfragmenten aus mehreren Adobe Experience Manager-Konfigurationen, einschließlich der Autoren-, Veröffentlichungs- und authentifizierten Veröffentlichungsebenen.</li>
<li>Sobald ein Fragment ausgewählt wurde, wird sein Kontext in der gesamten Nachricht beibehalten, sodass Autoren Fragmentfelder über Inhaltsblöcke hinweg wiederverwenden können, ohne die Auswahl erneut durchzuführen.</li>
<li>In Journey Optimizer wurde eine neue spezielle Seite zur Auflistung von Inhaltsfragmenten eingeführt, um die Lebenszyklusverwaltung zu verbessern. Benutzende können nicht synchronisierte Fragmente und manuelle Synchronisierungen von Triggern identifizieren, um auf dem neuesten Stand zu bleiben.</li>
<li>Die Unterstützung von Gebietsschemata und Varianten ermöglicht es Marketing-Experten jetzt, gezielter mit alternativen Versionen desselben Inhaltsfragments zu arbeiten.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager-Repository-Konfiguration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt flexibel darauf zugreifen, wie Adobe Journey Optimizer auf Ihre Adobe Experience Manager-Inhalte zugreift. Diese Version bietet die Möglichkeit, das Quell-Repository für Inhaltsfragmente zu wechseln, die in Ihren Journey und Kampagnen verwendet werden.</p>
</td>
</tr>
</tbody>
</table>

* **Integration nativer AEM-Inhaltsfragmente (Managed Services) in AJO** - Jetzt, kompatibel mit Managed Services, können Sie Adobe Experience Manager-Inhaltsfragmente direkt in Journey Optimizer anzeigen, darauf zugreifen und sie zur Personalisierung verwenden. Fügen Sie einfach Ihre Adobe Experience Manager Managed Services-Repository-URL in den Konfigurationseinstellungen als einmaliges Setup hinzu.

* **Emagica-Integration mit AEM Asset Essentials** - Der KI-Assistent ruft jetzt automatisch markengenehmigte Bilder direkt aus Ihrem Adobe Experience Manager Assets ab, wenn E-Mails, Web-Seiten und Push-Benachrichtigungen generiert werden. Dadurch entfällt die Notwendigkeit, die Assets manuell zu durchsuchen oder sich auf generische KI-Fallbacks zu verlassen, um sicherzustellen, dass jedes Bild perfekt präzise und markenkonform ist.

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
<p>Journey Optimizer führt jetzt benutzerdefinierte Kanäle ein, eine neue Funktion, mit der Administratoren jeden ausgehenden HTTP-basierten Nachrichtenkanal - wie WeChat, Kakao Talk, Messenger oder einen proprietären Anbieter - über einen Kanal-Builder ohne Code direkt in AJO importieren können. Nach der Konfiguration sind benutzerdefinierte Kanäle in allen Kampagnen, Journey und orchestrierten Kampagnen verfügbar und haben die gleichen umfassenden Funktionen wie native Kanäle: Personalisierung mit dem Ausdruckseditor, Inhaltsexperimentierung, Vorschau und Testversand, vorkonfiguriertes Reporting sowie die Durchsetzung von Einverständnis und Governance. Dadurch wird die Lücke gefüllt, die zuvor durch benutzerdefinierte Aktionen geschlossen wurde, die auf Journey beschränkt waren und denen es an dedizierter Inhaltserstellung fehlte.</p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
</td>
</tr>
</tbody>
</table>

### Konfiguration {#june-26-configuration}

In dieser Version werden die folgenden Verbesserungen bei der Konfiguration und Administration vorgenommen.

* **Whitelisting von Web Application Firewall (WAF) für Landingpages von AJO** - Adobe Journey Optimizer unterstützt jetzt die Whitelisting von Web Application Firewall (WAF) für Landingpages, sodass Unternehmen durchsetzen können, dass alle eingehenden Anfragen ausschließlich über ihre konfigurierte WAF-Infrastruktur weitergeleitet werden. Mit dieser Verbesserung können Kundinnen und Kunden AJO so konfigurieren, dass direkte Anfragen, die die WAF-Ebene umgehen, abgelehnt werden. So wird sichergestellt, dass in Tools wie Imperva definierte Sicherheitsrichtlinien konsistent angewendet werden. Diese Funktion verbessert die Sicherheitslage für Unternehmen mit strengen Anforderungen an den Netzwerkzugriff und gibt ihnen die volle Kontrolle über den Traffic-Fluss zu ihren von AJO gehosteten Landingpages.

* **Datensatz wechselt vom Streaming- in den Batch** Modus - Der AJO-Nachrichten-Feedback-Ereignisdatensatz wechselt vom Streaming- in den Batch-Erfassungsmodus. Durch diese Änderung wird sichergestellt, dass die Datenaufnahme die Streaming-Aufnahmebeschränkungen nicht überschreitet. Wenn Sie diesen Datensatz in Customer Journey Analytics-Berichten verwenden oder Abfragen dafür ausführen, erwarten Sie in Zukunft eine Zunahme der Datenlatenz von bis zu 2 Stunden.

### Verbesserungen der Benutzerfreundlichkeit {#june-26-usability}

In dieser Version wird die folgende Verbesserung der Benutzerfreundlichkeit eingeführt.

* **Ordner für Journey und Kampagnen** - Sie können Ihre Journey und Kampagnen jetzt in Ordnern organisieren, um die Navigation und Verwaltung in der Benutzeroberfläche zu verbessern.

