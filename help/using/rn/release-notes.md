---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ec2cccb651360ec796610781affcedca96d66af4
workflow-type: ht
source-wordcount: '1278'
ht-degree: 100%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert. [!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.


## Neueste Aktualisierungen {#latest-updates}

### Änderung bei den Journey-Bedingungen {#ee-change@}

Ab dem 8. Juli wird das Erstellen von Ausdrücken mit Erlebnisereignissen in neuen Kundenorganisationen in dem in Journey-Bedingungen verwendeten Ausdruckseditor nicht mehr unterstützt. Daher können Erlebnisereignisse in der [Experience Platform-Datenquelle](../datasource/adobe-experience-platform-data-source.md) nicht zum Erstellen von Ausdrücken verwendet werden. Alternative Ansätze und Best Practices zum Erstellen von Ausdrücken/Logik mit Erlebnisereignissen sind [hier](../building-journeys/exp-event-lookup.md) zu finden.

Der Zugriff auf Journey-Kontextereignisdaten in unitären Journeys wird nicht geändert. In den Ausdrucks- und Personalisierungseditoren können Benutzende weiterhin auf Daten zugreifen, die mit dem ersten Journey-Ereignis übergeben wurden.

Weitere Informationen finden Sie [in diesen FAQ](../building-journeys/exp-event-lookup.md#faq-ee).


## Versionshinweise für Juni 2025 {#25-6-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**Veröffentlichungsdatum**: 18. Juni 2025

<!--See also [Adobe Experience Platform Pre Release Notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### Neue Funktionen {#25-06-features}

Im Folgenden werden die neuen Funktionen dieser Version beschrieben.

<table>
<thead>
<tr>
<th><strong>Adobe Experience Platform-Datensätze in der Entscheidungsfindung (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform-Datensätze, die zuvor bereits für die Personalisierung verfügbar waren, können jetzt auch für die Entscheidungsfindung genutzt werden. So können Sie die Definition Ihrer Entscheidungsattribute auf zusätzliche Daten in Datensätzen erweitern, um sie bei sich regelmäßig ändernden Massen-Updates zu nutzen, ohne dass Sie die Attribute einzeln manuell aktualisieren müssen. Beispielsweise Verfügbarkeit, Wartezeiten usw.</p>
<p>Diese Funktion steht derzeit allen Kundinnen und Kunden als öffentliche Beta-Version zur Verfügung. Wenden Sie sich an Ihren Kontakt in der Kundenbetreuung, wenn Sie Zugriff wünschen.</p>
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/aep-data-exd.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 20. Juni 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>RCS-Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Das Messaging über Rich Communication Services (RCS) wird jetzt in Journey Optimizer unterstützt und ermöglicht die folgenden erweiterten Messaging-Funktionen, die der Anbieter- und Betreiberunterstützung unterliegen:</p>
<ul>
<li>Unterstützung für Nachrichten mit Markenelementen von verifizierten Absendenden: Senden Sie Nachrichten mithilfe verifizierter Geschäftsprofile mit Markenelementen (Logo, Absendername usw.).</li>
<li>Erkenntnisse bezüglich des Nachrichtenversands: Erhalten Sie detaillierte Versandberichte einschließlich Statusaktualisierungen der Nachricht (z. B. gesendet, zugestellt, gelesen).</li>
<li>Linktracking: Betten Sie URLs ein und verfolgen Sie diese in RCS-Nachrichten für die Interaktionsanalyse.</li>
<li>Fallback zu SMS: Automatischer Fallback zu SMS, wenn das Gerät des Profils RCS nicht unterstützt oder über RCS vorübergehend unerreichbar ist.</li>
<li>Grundlegende Nachrichtenkomposition: Senden Sie textbasierte RCS-Nachrichten mit optionalen Medien und umfangreichen Elementen, je nach Anbieter-Support.</li>
</ul>
<p>Weitere Informationen finden Sie in der <a href="../sms/sms-configuration.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Formularfelder in Code-basierten Erlebnisinhalten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt bestimmte bearbeitbare Felder in JSON- oder HTML-Inhaltsvorlagen definieren, die es technisch nicht versierten Benutzenden ermöglichen, Inhalte in einer Formularansicht innerhalb der Code-basierten Erlebniskanalerstellung einfach und ohne Code-Änderungen zu bearbeiten.<br />Darüber hinaus können Sie bei der Definition der Inhaltsvorlagen für Code-basierte Erlebnisse jetzt Entscheidungsrichtlinien in die Vorlage einfügen, was die Wiederverwendbarkeit und Benutzerfreundlichkeit erhöht.</p>
<img src="assets/do-not-localize/form-fields.gif">
<p>Weitere Informationen finden Sie in der <a href="../code-based/code-based-form-fields.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Custom delegation method for subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering and tracking messages.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Aktivität „Inhaltsentscheidung“ in Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt personalisierte Angebote über eine dedizierte Aktivität „Inhaltsentscheidung“ in Ihre Journeys auf der Journey-Arbeitsfläche einbeziehen und sie in Journey-Aktivitäten verwenden, einschließlich Bedingungen und benutzerdefinierten Aktionen.</p>
<img src="assets/do-not-localize/content-decision.gif">
<p>Diese Funktion ist nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit) und wird in einer zukünftigen Version global eingeführt.</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/content-decision.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Probelauf</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der Journey-Probelauf ist ein spezieller Journey-Veröffentlichungsmodus in Adobe Journey Optimizer, der es Journey-Anwendenden ermöglicht, eine Journey mit echten Produktionsdaten zu testen, ohne echte Kundinnen und Kunden zu kontaktieren oder Profilinformationen zu aktualisieren. Mit dieser Funktion können Journey-Anwendende Vertrauen in ihr Journey-Design und die Zielgruppenbestimmung gewinnen, bevor sie die Journey live veröffentlichen.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Diese Funktion ist nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit) und wird in einer zukünftigen Version global eingeführt.</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/journey-dry-run.md">ausführlichen Dokumentation</a>.</p>

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Pausieren und Fortsetzen von Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können Ihre Journeys jetzt pausieren und fortsetzen. Diese Funktion gibt Journey-Anwendenden mehr Kontrolle und Flexibilität, da Live-Journeys vorübergehend ausgesetzt werden können, ohne das Kundenerlebnis zu stören. Während der Pause werden keine Nachrichten gesendet und die Profile verbleiben in einem ausgesetzten Zustand, bis die Journey fortgesetzt wird.</p>
<p>Sie können nur eine Journey pausieren und fortsetzen oder Vorgänge zur Massenpause und -fortsetzung von einer Gruppe von Journeys durchführen.</p>
<p>Darüber hinaus können Sie globale Filter auf pausierte Journeys anwenden, um Profile auf der Grundlage ihrer Attribute auszuschließen.</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>Diese Funktion ist nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit) und wird in einer zukünftigen Version global eingeführt.</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/journey-pause.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Skalieren der Gewinner von Experimenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit der Funktion zum Skalieren des Gewinners von Experimenten können Sie die erfolgreichste Variante eines Experiments automatisch oder manuell für Ihre gesamte Zielgruppe einführen. Dadurch wird sichergestellt, dass Sie die Reichweite und Effektivität einmal identifizierter Top-Performer ohne ständige manuelle Überwachung maximieren können.</p>
<p>Weitere Informationen finden Sie in der <a href="../content-management/content-experiment.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 2. Juni 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Konflikte und Priorisierung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer ist es wichtig, das Volumen und den Zeitpunkt von Kampagnen und Journeys zu verwalten, um zu vermeiden, dass Kundinnen und Kunden mit zu vielen Interaktionen überfordert werden. Journey Optimizer bietet nun mehrere Tools für das Konflikt-Management und die Priorisierung, die bisher nur eingeschränkt für bestimmte Organisationen verfügbar waren (LA) und jetzt allgemein zur Verfügung stehen (GA).</p>
<p>Diese Funktion wurde zuvor mit eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung. Mit dieser allgemein verfügbaren Version werden die folgenden Verbesserungen eingeführt:</p>
<ul>
<li>Erweiterte Unterstützung: Konflikt-Management-Tools unterstützen nun neben Journeys vom Typ „Zielgruppen lesen“ auch unitäre Journeys und Journeys vom Typ „Zielgruppen-Qualifizierung“.</li>
<li>Verbesserte Fehlerbehebung: Im Abfrage-Service sind nun zwei neue Schrittereignisfelder verfügbar, mit denen Sie analysieren können, warum ein Profil von einer Journey oder Kampagne abgelehnt wurde.</li>
<li>Erweitertes Reporting: Berichte zeigen jetzt an, durch welche spezifische Regel ein Profil von einer Journey oder Kampagne ausgeschlossen wurde, was für mehr Transparenz und verwertbare Erkenntnisse sorgt.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Weitere Informationen finden Sie in der <a href="../conflict-prioritization/gs-conflict-prioritization.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 3. Juni 2025</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#25-06-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.

* **Kanalregelsätze**

   * **Benutzerdefiniertes Zeitfenster** für die Begrenzung – Im Konfigurationsbildschirm für Kanalregelsätze ist jetzt ein neues Feld **Alle** verfügbar, mit dem Sie Frequenzbegrenzungsregeln je nach angegebener Dauer für mehrere Tage, Wochen oder Monate anwenden können.

   * **Stündliches Zurücksetzen der Begrenzungsfrequenz** – Sie können jetzt eine Begrenzung auf stündlicher Basis für Kanalregelsätze anwenden. Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Wenden Sie sich an die Kundenunterstützung, um die Funktion aktivieren zu lassen.

   * **Tägliche Dauer** – Die zuvor nur eingeschränkt verfügbare Frequenzbegrenzung „Täglich“ ist in Kanalregelsätzen jetzt für alle Kundinnen und Kunden verfügbar.

  Weitere Informationen finden Sie in der [ausführlichen Dokumentation](../conflict-prioritization/channel-capping.md).

* **Code-basierte Erlebnisse**

   * Das Hinzufügen einer Entscheidungsrichtlinie ist jetzt in Code-basierten Erlebnis-Inhaltsvorlagen verfügbar. Dort kann sie zur Nutzung von Angeboten in bearbeitbaren Formularfeldern verwendet werden. [Weitere Informationen](../code-based/code-based-form-fields.md)

   * Auf dem Bearbeitungsbildschirm der Code-basierten Erlebnis-Journey oder -Kampagne können Sie jetzt direkt eine Entscheidungsrichtlinie hinzufügen, ohne den Personalisierungseditor zu öffnen. [Weitere Informationen](../code-based/create-code-based.md#edit-code)

* **Unterstützung für benutzerdefiniertes CSS im E-Mail-Designer**

  Mit Journey Optimizer können Sie Ihrem E-Mail-Inhalt jetzt benutzerdefiniertes CSS direkt im E-Mail-Designer hinzufügen. [Weitere Informationen](../email/custom-css.md)

* **Neue Registerkartennavigation für Kampagnen**

  Ein neues Navigationsmuster ermöglicht einen schnelleren Zugriff auf das Content-Authoring und unterstützt die weitere Erweiterung der Einstellungen in allen Kampagnen. [Weitere Informationen](../campaigns/create-campaign.md)

* **Entscheidungsfindung**

   * **Sandbox – Kopien und Entscheidungsfindung** (Verfügbarkeitsdatum: 3. Juni 2025) – Entscheidungsobjekte können jetzt zwischen Sandboxes kopiert werden, um Test- und Bereitstellungs-Workflows zu optimieren. [Weitere Informationen](../configuration/copy-objects-to-sandbox.md#decisioning)

   * **Unterstützung von Entscheidungselementattributen für Entscheidungsregeln** (Verfügbarkeitsdatum: 4. Juni 2025) – Sie können jetzt Entscheidungselementattribute für die Erstellung von Entscheidungsregeln verwenden. [Weitere Informationen](../experience-decisioning/rules.md#create)

* **Aktualisierung des API für die Ausführung interaktiver Nachrichten** – Verfügbarkeitsdatum: 6. Juni 2025

  Mit dem API für die Ausführung interaktiver Nachrichten können Sie jetzt den Zeitplan der bevorstehenden Kampagnenausführung löschen. [Weitere Informationen](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}
