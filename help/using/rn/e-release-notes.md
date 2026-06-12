---
solution: Journey Optimizer
product: journey optimizer
title: Vorab veröffentlichte Versionshinweise zu Journey Optimizer
description: Vorab veröffentlichte Versionshinweise zu Adobe Journey Optimizer
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: a2257f19ea46aaf4bcf45580a0e6cf0d207be355
workflow-type: tm+mt
source-wordcount: 1876
ht-degree: 5%

---


# Vorab veröffentlichte Versionshinweise {#e-release-notes}

Adobe Journey Optimizer bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

## Hinweise zur Vorabversion vom 26. Juni {#june-26-rn}

**Die nachfolgenden Vorab- Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentationen werden veröffentlicht, sobald Änderungen in der Produktion live sind. Die meisten Änderungen werden am Veröffentlichungsdatum bereitgestellt, einige werden jedoch möglicherweise später eingeführt. Weitere Informationen finden Sie unter Verfügbarkeitsdatum für jeden Eintrag.

Siehe auch [Vorab veröffentlichte Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Veröffentlichungsdatum**: 16.-17. Juni 2026

### Journeys {#june-26-journeys}

In dieser Version wurden die folgenden Funktionen und Verbesserungen für Journey implementiert.

* **Erhöhte Live-Journey-Grenze und neue**: Sie können jetzt bis zu **200 aktive Journey-** haben, die gegenüber der vorherigen Grenze von 100 erhöht wurden.

* **Start- und Enddatum im Journey-Header** - Wenn Start- und/oder Enddatum auf einer Live-Journey konfiguriert sind, werden sie jetzt in der Kopfzeile **Journey** neben dem Live-Status-Badge angezeigt. Die angezeigte Beschriftung passt sich an, je nachdem, ob jedes Datum bevorsteht oder bereits vergangen ist.

* **Angehalten oder Anhaltende Journey direkt schließen** - Sie können jetzt **eine Journey anhalten oder bei neuen Eintritten schließen** direkt aus dem Status **Angehalten**. Zuvor musste eine angehaltene Journey wieder live geschaltet werden, bevor sie angehalten oder geschlossen werden konnte.

### Orchestrierte Kampagnen {#june-26-oc}

Orchestrierte Kampagnen in dieser Version weisen die folgenden Funktionen und Verbesserungen auf.

<table>
<thead>
<tr>
<th><strong>Dateibasiertes Targeting in koordinierten Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Orchestrierte Kampagnen unterstützen jetzt das Laden einer <strong>CSV- oder TXT-Datei</strong> direkt in die Kampagnen-Arbeitsfläche als Zielgruppe, ohne die Datei zuerst in Adobe Experience Platform aufzunehmen. Die Dateidaten werden zur Ausführungszeit genutzt und nicht als Adobe Experience Platform-Datensatz beibehalten. Während der Dateieinrichtung können Sie Spaltenzuordnungen, Datentypen, die NULL-Verarbeitung und Fehlerrichtlinien pro Spalte definieren. Zeilen, die bei der Validierung fehlschlagen, werden abgelehnt und protokolliert, bevor die Kampagne ausgeführt wird. Dadurch wird die Zielgruppe ohne manuelle Vorverarbeitung sauber gehalten. Dies eignet sich besonders für Ad-hoc-Sendungen oder Partnerlisten-Kampagnen, bei denen der Aufbau einer vollständigen Aufnahme-Pipeline nicht praktisch ist.</p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
</td>
</tr>
</tbody>
</table>

* **Schleifenbasierte Personalisierung für relationale Daten in orchestrierten Kampagnen** - Der Personalisierungseditor unterstützt jetzt einen **Schleifenblock**, der relationale Sammlungen wie Bestellungen, Konten oder Buchungen durchläuft und einen Inhaltsblock pro Datensatz in einer einzelnen E-Mail oder SMS rendert. Sammlungen werden über die Datenauswahl mithilfe von Personalisierungs-Token konfiguriert, ohne dass ein Ausdruck geschrieben werden muss. Sie können eine Vorschau davon anzeigen, wie Schleifenblöcke mit Beispieldaten gerendert werden, bevor die Kampagne live geschaltet wird, einschließlich der Verarbeitung leerer Sammlungen.

* **Personalisieren von E-Mail-Absenderdetails pro Empfänger und Kampagne** - Orchestrierte Kampagnen unterstützen jetzt die Personalisierung von **E-Mail-Header-Feldern**, einschließlich Absendername, Absenderadresse und Antwortadresse, mithilfe von Profilattributen oder relationalen Daten. Auf diese Weise können Absenderdetails den relevanten Berater, Standort oder die Zweigstelle für jeden Empfänger widerspiegeln, anstatt alle Sendungen über eine einzelne Unternehmensadresse weiterzuleiten. Header-Werte können auf Kanalebene festgelegt und pro Kampagne überschrieben werden, indem kontextuelle Daten verwendet werden, um die Kontrolle zu verbessern.

<!--
* **Target dimension simplification in Orchestrated campaigns** - The active **targeting dimension** is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->

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
</td>
</tr>
</tbody>
</table>

* **Dynamische Angebotsattribute** - Angebotsattribute in Decisioning können jetzt zur Versandzeit mithilfe von Profil-, Kontext- und Zielgruppendaten personalisiert werden. Dadurch entfällt die Notwendigkeit, doppelte Angebote für kleinere Inhaltsvarianten zu verwalten, sodass Marketer weniger, flexiblere Entscheidungselemente verwalten können.

* **Frequenzlimitierung auf Platzierungsebene in Decisioning** - Frequenzlimitierungsregeln in Decisioning können jetzt auf einzelne Platzierungen angewendet werden, sodass Sie besser steuern können, wie oft ein Angebot auf einer bestimmten Oberfläche angezeigt wird. Zwei Modi sind verfügbar:

   * Platzierungsspezifische Begrenzung: Definieren Sie eine Begrenzung, die nur gilt, wenn das Angebot an einer ausgewählten Platzierung angezeigt wird.
   * Begrenzung pro Platzierung: Wenden Sie eine Begrenzung unabhängig auf jede Platzierung an, an der das Angebot angezeigt wird, sodass jede Platzierung ihren eigenen Begrenzungszähler beibehält.

### E-Mail {#june-26-email}

In dieser Version werden die folgenden Funktionen und Verbesserungen für den E-Mail-Kanal bereitgestellt.

<table>
<thead>
<tr>
<th><strong>Qualitätsprüfungen von Inhalten in der E-Mail-Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer bietet jetzt eine direkte Bewertung der Inhaltsqualität in Email Designer, das Ihre E-Mail vor dem Launch dreidimensional analysiert: Rechtschreibung, Grammatik und Zeichensetzung, Lesbarkeit und Ton, einschließlich Kennzeichnungen für lange Sätze, Passivstimme und Jargon sowie Betreffzeile und CTA-Effektivität, bewertet aus Gründen der Klarheit, Dringlichkeit und Struktur. Bei jeder Prüfung werden umsetzbare Vorschläge angezeigt, sodass Teams Probleme erkennen und lösen können, ohne die Authoring-Oberfläche verlassen zu müssen.</p>
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
<p>Journey Optimizer bietet jetzt eine Option, die HTML Ihrer E-Mail zu verkleinern, indem unnötige Leerzeichen, Kommentare und redundanter Code entfernt werden - ohne die Darstellung der E-Mail zu beeinflussen. Dies kann die Zustellbarkeit verbessern, indem Größenschwellen vermieden werden, die einige E-Mail-Anbieter zum Kennzeichnen oder Ablehnen von Nachrichten verwenden, und kann die Ladezeit für Empfänger verkürzen.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Rich-Text in bearbeitbaren Feldern für Fragmente</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Rich-Text zu anpassbaren Fragmenten hinzufügen, die in Ihren E-Mail-Inhalten verwendet werden. Wenn Sie beispielsweise die Textkomponente als bearbeitbares Feld in der E-Mail-Designer verwenden, können Sie den Inhalt direkt formatieren (z. B. fett und kursiv) und Hyperlinks einfügen.</p>
</td>
</tr>
</tbody>
</table>

* **Erweiterter Konverter von Bildern zu HTML** - Eine neue Version der Funktion „Konverter von Bildern zu HTML&quot; ist jetzt verfügbar und bietet eine höhere Genauigkeit bei der HTML-Erstellung. Diese Aktualisierung nutzt höherstufige LLM-Modelle, um eine präzisere und zuverlässigere HTML-Ausgabe aus Bildeingaben zu ermöglichen.

+++ Demnächst verfügbar **Informationen unten können sich ändern**

<table>
<thead>
<tr>
<th><strong>Module in der E-Mail-Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>E-Mail-Designer enthält jetzt eine Bibliothek einsatzbereiter Layout-Module - wie Kopf- und Produktkarten, Informationsblöcke und Fußzeilen -, die Sie per Drag-and-Drop direkt in Ihre E-Mail-Arbeitsfläche ziehen können.</p>
<p>Jedes Modul ist mit bearbeitbaren Eigenschaften (Bild, Titel, Text, Schaltfläche, Links) vorkonfiguriert und kann über die WYSIWYG-Benutzeroberfläche vollständig angepasst werden, wodurch die E-Mail-Erstellung beschleunigt wird, ohne dass Sie Strukturen von Grund auf neu erstellen müssen.</p>
<p>Verfügbarkeitsdatum: 22. Juni 2026</p>
</td>
</tr>
</tbody>
</table>

+++

### Mobile Messaging (SMS, MMS, RCS und LINE) {#june-26-mobile}

In dieser Version wurden folgende Verbesserungen für Mobile Messaging vorgenommen.

* **Eindeutige Klicks für SMS-Berichte** - Für SMS-Berichte wurde das neue Modul **Eindeutige Klicks** eingeführt, wodurch die Leistung von SMS nun genauso präzise verfolgt wird wie bei E-Mail-Berichten.

* **LINE-Kanal - Authoring-**: Die Benutzeroberfläche des LINE-Kanals wurde um erweiterte Funktionen zur Nachrichtenerstellung erweitert. Diese Version bietet Unterstützung für **mehrere Nachrichtenformate** einschließlich Text, Bild, Imagemap, Karussell und Flex (JSON-Editor) sowie Gerätevorschauen in Echtzeit. Benutzer können jetzt gruppierte Nachrichten mit bis zu fünf sortierten Nachrichten verwalten (mit den Steuerelementen Hinzufügen, Entfernen und Neu anordnen) und den integrierten Personalisierungseditor für validierte, dynamische Nachrichten nutzen.

* **SMS - Nutzungsmetriken anzeigen** - Für Kundinnen und Kunden, die SMS direkt über Adobe Journey Optimizer erwerben, **ein neues** SMS-Nutzungs-Dashboard) eingeführt. Sie können jetzt Ihre letzten 90 Tage der Nachrichten-Versandmetriken anzeigen und verfolgen, die nach von Mobilgeräten stammenden (MO) und von Mobilgeräten beendeten (MT) Nachrichten kategorisiert sind. Diese Daten können auch über CSV heruntergeladen werden, was eine bessere Sichtbarkeit und Kontrolle über Ihre SMS-Ausgaben ermöglicht.

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
</td>
</tr>
</tbody>
</table>

<!--
### Campaigns {#june-26-campaigns}

The following improvement is coming to campaigns in this release.

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default **execution field** set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.
-->

### Berichterstellung {#june-26-reporting}

In dieser Version werden die folgenden Verbesserungen beim Reporting vorgenommen.

* **Geschätzte Klicks für E-Mail- und SMS-Berichte** - Eine neue **Geschätzte Klicks**-Metrik ist jetzt in Journey-, Kampagnen- und Kanalberichten für E-Mail und SMS verfügbar. Diese Metrik schließt identifizierten Traffic von sowohl als auch Nicht-Human Interaction (NHI) aus, um einen klareren Überblick über die echte Kundeninteraktion zu erhalten. Die Metrik Bestehende Klicks bleibt verfügbar und zeigt weiterhin die Gesamtklicks an.

+++ Demnächst verfügbar **Informationen unten können sich ändern**

* **Neue geschätzte Klickmetriken für E-Mail- und SMS-Reporting** - Um eine genauere Übersicht über die tatsächliche Kundeninteraktion zu erhalten, sind jetzt neue geschätzte Metriken in Journey-, Kampagnen- und Kanalberichten verfügbar. Diese Metriken helfen beim Filtern nicht-menschlicher Interaktionen (NHI) und Bot-Klicks aus Berichtsdaten:

   * Geschätzte CTR: Geschätzte Klicks im Verhältnis zu den gesamten Sendungen.
   * Geschätzter CTOR nur für E-Mail: Geschätzte Klicks im Verhältnis zu den geschätzten Öffnungen.

  Verfügbarkeitsdatum: Ende Juni 2026

+++

### Konfiguration {#june-26-configuration}

In dieser Version werden die folgenden Verbesserungen bei der Konfiguration und Administration vorgenommen.

* **Datensatz wechselt vom Streaming- in den Batch** Modus - Der AJO-Nachrichten-Feedback-Ereignisdatensatz wechselt vom Streaming- in **Batch-Erfassungsmodus**. Durch diese Änderung wird sichergestellt, dass die Datenaufnahme die Streaming-Aufnahmebeschränkungen nicht überschreitet. Wenn Sie diesen Datensatz in Customer Journey Analytics-Berichten verwenden oder Abfragen dafür ausführen, erwarten Sie in Zukunft eine Zunahme der Datenlatenz von bis zu 2 Stunden.

+++ Demnächst verfügbar **Informationen unten können sich ändern**

* **Web Application Firewall (WAF) IP Whitelisting** - Adobe Journey Optimizer unterstützt jetzt die IP-Whitelisting von Web Application Firewall (WAF) für Landingpages, sodass Unternehmen durchsetzen können, dass alle eingehenden Anfragen ausschließlich über ihre konfigurierte WAF-Infrastruktur weitergeleitet werden. Mit dieser Verbesserung können Kundinnen und Kunden Journey Optimizer so konfigurieren, dass direkte Anfragen, die die WAF-Ebene umgehen, abgelehnt werden. So wird sichergestellt, dass in Tools wie Imperva definierte Sicherheitsrichtlinien konsistent angewendet werden. Diese Funktion verbessert die Sicherheitslage für Unternehmen mit strengen Anforderungen an den Netzwerkzugriff und gibt ihnen die volle Kontrolle über den Traffic-Fluss zu ihren von AJO gehosteten Landingpages.

  Verfügbarkeitsdatum: Ende Juni 2026

+++

### Verbesserungen der Benutzerfreundlichkeit {#june-26-usability}

In dieser Version wird die folgende Verbesserung der Benutzerfreundlichkeit eingeführt.

* **Ordner für Journey und Kampagnen** - Sie können Ihre Journey und Kampagnen jetzt in **Ordner** organisieren, um die Navigation und Verwaltung in der Benutzeroberfläche zu verbessern.
