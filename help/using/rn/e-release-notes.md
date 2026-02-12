---
solution: Journey Optimizer
product: journey optimizer
title: Vorab veröffentlichte Versionshinweise zu Journey Optimizer
description: Vorab veröffentlichte Versionshinweise zu Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 4b6e988d79c48d0c5417c9e7f43a8da85a7fbe28
workflow-type: tm+mt
source-wordcount: '1553'
ht-degree: 42%

---

# Vorab veröffentlichte Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

## Hinweise zur Vorabversion vom Februar 2026 {#feb-26-01-rn}

**Die nachfolgenden Vorab- Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentationen werden in den Versionshinweisen am Veröffentlichungsdatum veröffentlicht.

Siehe auch [Vorab veröffentlichte Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Veröffentlichungsdatum**: Mittwoch, 17. Februar 2026

### Neue Funktionen {#feb-26-01-features}

<table>
<thead>
<tr>
<th><strong>Senden ausgehender Nachrichten schwenken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können den Versand ausgehender Nachrichten von Kampagnen oder Journey planen, die im Laufe der Zeit in kontrollierten Batches zugestellt werden sollen.</p>
<p>Der Wave-Versand bietet die folgenden Vorteile:</p>
<ul>
<li>Bessere Zustellbarkeit: Spread sendet im Laufe der Zeit, um einen guten Ruf als Absender zu wahren und das Risiko zu reduzieren, als Spam gekennzeichnet zu werden.</li>
<li>Laststeuerung - Vermeiden Sie die Überlastung nachgelagerter Systeme (z. B. Callcenter, Landingpages), indem Sie einschränken, wie viele Nachrichten gleichzeitig gesendet werden.</li>
<li>Anwendungsfälle mit hohem Volumen und zeitkritischer Relevanz - geeignet für große Zielgruppen oder zur Steuerung des Timings (z. B. Call-Center-Kapazität, Anlaufphase oder zeitlich begrenzte Angebote).</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11533">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Schlichtung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Formeln und KI-Modelle verwenden, um anhand von Kundenprofilattributen und Kontextfaktoren automatisch die Journey-Prioritätswerte zu erhöhen und so sicherzustellen, dass Kunden in die relevantesten Journey eintreten.</p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13976">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: Kanalinhalt erstellen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Adobe Experience Platform Agent Orchestrator ist Journey Agent in Journey Optimizer verfügbar und ermöglicht die Analyse von Journey über eine natürliche Sprachschnittstelle. Sie können jetzt auch direkt in Journey Agent Inhalte generieren und verwalten, Inhalte für Kanäle wie E-Mail und Push erstellen, Vorlagen anwenden und in der Vorschau anzeigen, den Ton und Stil mit Prompts verfeinern und Inhalte im Content-Designer zur kontextbezogenen Bearbeitung öffnen.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13980">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mobile Live-Aktivitäten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Live-Aktivitäten bieten Echtzeit-Updates und interaktive Erlebnisse in mobilen Apps, sodass Benutzer direkt auf dem Bildschirm ihres Geräts über laufende Ereignisse oder Aufgaben auf dem Laufenden bleiben können. Diese Funktion verbessert die Interaktion, indem Live-Informationen wie Fortschritts-Tracking, Ereignisaktualisierungen oder interaktive Inhalte bereitgestellt werden, ohne dass Benutzende die App öffnen müssen.</p>
<p>Diese Funktion wurde bereits in der Beta-Version veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13588">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aktionsaktivität in Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer unterstützt eine neue generische Aktionsaktivität, mit der Sie sowohl einzelne als auch eingehende Aktionsgruppen mit mehreren Aktionen konfigurieren können, was eine optimierte Aktionskonfiguration innerhalb der Journey-Arbeitsfläche ermöglicht. Diese neue Funktion ermöglicht insbesondere Folgendes:</p>
<ul>
<li>Eine vereinfachte, native Aktionskonfiguration innerhalb der Journey-Arbeitsfläche</li>
<li>Die Möglichkeit, eingehende Aktionsgruppen mit mehreren Aktionen zu erstellen</li>
<li>Die Möglichkeit, jeder integrierten Kanalaktion eine Optimierung hinzuzufügen</li>
<li>Die Möglichkeit, jeder Aktion sowohl experimentelle als auch mehrsprachige Optionen hinzuzufügen.</li>
</ul>
<p>Diese Funktion ist jetzt für alle Umgebungen verfügbar (allgemeine Verfügbarkeit).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13290">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Kanal für Web-Push-Benachrichtigungen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer unterstützt jetzt Web-Push-Benachrichtigungen und erweitert damit den Push-Kanal über den mobilen Gebrauch hinaus. Sie können Benachrichtigungen nahtlos an mobile und Desktop-Browser senden, sodass Ihre Kundinnen und Kunden direkt auf ihren Geräten erreicht werden, ohne dass eine App erforderlich ist. Diese Verbesserung ermöglicht es Ihnen, Benutzende in Echtzeit mit zeitnahen, personalisierten Nachrichten anzusprechen, unter Nutzung derselben Authoring-Workflows und Targeting-Funktionen, die bereits für mobile Push-Benachrichtigungen verfügbar sind.</p>
<p>Diese Funktion wurde bereits in der Beta-Version veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum: Freitag, 12. Februar 2026</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13581">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aktivität „Inhaltsentscheidung“ </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Auf der Journey-Arbeitsfläche ist jetzt eine neue Aktivität zur Inhaltsentscheidung verfügbar, mit der Sie personalisierte Angebote direkt in die Journey Ihrer Kunden integrieren können. Mit dieser Aktivität können Sie entscheidungsbasierte Inhalte bereitstellen und diese Angebote auf Ihrem gesamten Journey referenzieren - unter Bedingungen für die Erstellung von Verzweigungen auf der Grundlage der Eignung, bei benutzerdefinierten Aktionen zur Weitergabe von Angebotsdaten an externe Systeme und bei anderen Aktivitäten zur Erstellung vollständig personalisierter Kundenerlebnisse.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/content-decision.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 11. Februar 2026</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12902">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>APIs für Self-Service-Migrations-Tools</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Migrations-Tool</strong>-APIs sind jetzt verfügbar, um Entitäten aus dem Entscheidungs-Management programmgesteuert in die Entscheidungsfindung zu migrieren. Sie bieten folgende Funktionen:</p>
<ul>
<li>Flexible Migrationsbereiche (Sandbox-, Angebots- oder Entscheidungsebene)</li>
<li>Automatische Analyse und Validierung von Abhängigkeiten</li>
<li>Rollback-Unterstützung für abgeschlossene Migrationen</li>
<li>Detaillierte Migrationsberichte mit Objektzuordnungen</li>
</ul>
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/decisioning-migration-api.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 3. Februar 2026</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13837">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoring von benutzerdefinierten Aktionen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gewinnen Sie detailliertere Erkenntnisse zum Status und zur Leistung Ihrer <strong>benutzerdefinierten Aktionsendpunkte</strong> mit einem neuen Monitoring-Dashboard und angereicherten Ereignisdaten zu Journey-Schritten. Verfolgen Sie erfolgreiche Aufrufe, Fehler, Durchsatz, Antwortzeiten und Warteschlangenwartezeiten nach, um schnell zu erkennen, wann, wo und warum Anomalien auftreten.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../action/reporting.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 3. Februar 2026</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13981">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Entscheidungsunterstützung im SMS-Kanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt den Inhalt Ihrer (SMS<strong>Nachrichten) mit </strong>Decisioning<strong> personalisieren und </strong>. Verwenden Sie Prioritätswerte, Formeln oder KI-Modelle, um Ihren Kundinnen und Kunden den besten Inhalt anzuzeigen.</p>
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/create-decision.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 2. Februar 2026</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13426">Link zur JIRA-Aufgabe DOCAC</a></p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#feb-26-01-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.

#### Konfiguration

* **Einstellung der Suche nach Erlebnisereignissen** - Ab dem 1. April 2026 wird die Suche nach Erlebnisereignissen im Ausdruckseditor für Journey-Bedingungen für Organisationen eingestellt, die in den letzten 90 Tagen keine Suche nach Erlebnisereignissen verwendet haben. Diese Funktion ist bereits seit dem 8. Juli 2025 für neue Kundenorganisationen nicht mehr verfügbar. Alternativen finden Sie unter [Suche nach Erlebnisereignissen in Journey](../building-journeys/exp-event-lookup.md).

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14136">Link zur DOCAC JIRA-Aufgabe</a>

* **Wechsel der Methode der Subdomain** - Sie können jetzt von einer Methode der Subdomain-Zuweisung zur anderen wechseln. Auf diese Weise können Sie Domains mithilfe des CNAME-Delegierungsmodus zu der benutzerdefinierten Delegierungsmethode migrieren, um die Sicherheitsrichtlinien Ihres Unternehmens einzuhalten.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13610">Link zur DOCAC JIRA-Aufgabe</a>

#### E-Mail-Designer

* **Verwenden eines Markendesigns zum Konvertieren eines Bildes in eine E-Mail-Vorlage** - Beim Konvertieren eines Bildes in eine E-Mail-Vorlage in Journey Optimizer können Sie jetzt ein Design als Eingabe verwenden, sodass die generierte HTML Ihren Markenparametern entspricht. Stile wie Hintergrundfarbe, Schaltflächenfarbe, Schriftarten, Zeilenabstand, Ränder und Abstand werden automatisch angewendet, wodurch die manuelle Entwurfsarbeit reduziert wird und eine Vorlage bereitgestellt wird, die mit minimalen Bearbeitungen verwendet werden kann.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14105">Link zur DOCAC JIRA-Aufgabe</a>

* **Aktualisieren von Marken mit neuer Farbregisterkarte** – Markenrichtlinien helfen sicherzustellen, dass Ihre Marke an allen Touchpoints konsistent präsentiert wird. Im neuen Abschnitt Farben werden die Standards für das Farbsystem Ihrer Marke definiert und beschrieben, wie Farben in Erlebnissen ausgewählt, organisiert und angewendet werden. Es sorgt für die konsistente Verwendung von primären, sekundären, Akzent- und neutralen Farben, um eine kohärente, barrierefreie und erkennbare Markenidentität zu unterstützen.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13811">Link zur DOCAC JIRA-Aufgabe</a>

#### KI

* **Integration von benutzerdefinierten Firefly-Modellen und Drittanbieter-Image-Generierungsmodellen** - Ermöglichen Sie die nahtlose Integration von standardmäßigen und benutzerdefinierten Firefly-Modellen zusammen mit genehmigten Drittanbieter-Image-Modellen (z. B. NanoBanana), um mehr Flexibilität, Kontrolle und Markenausrichtung bei der Bilderstellung zu bieten. Auf diese Weise können Sie für jeden Anwendungsfall das beste Modell auswählen: standardmäßige Firefly für allgemeine Anforderungen, benutzerdefinierte Firefly für die Markengenerierung oder genehmigte Drittanbietermodelle für spezialisierte oder experimentelle Szenarien.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13918">Link zur DOCAC JIRA-Aufgabe</a>

* **Firefly-3P-Modellunterstützung für die Bildgenerierung von Drittanbietern** - Sie können jetzt Bildgenerierungsmodelle von Drittanbietern (wie OpenAI und Gemini) zusammen mit Firefly verwenden, um Bilder in Journey Optimizer zu erstellen. Dies bietet Ihnen mehr Flexibilität bei der Auswahl des richtigen Modells für jeden Anwendungsfall und bei der Integration genehmigter externer Anbieter über das Firefly 3P-Gateway.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14145">Link zur DOCAC JIRA-Aufgabe</a>

#### Kampagnen

* **Ordner für Journey und Kampagnen** - Sie können Ihre Journey und Kampagnen jetzt in Ordnern organisieren, um die Navigation und Verwaltung in der Benutzeroberfläche zu verbessern.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14038">Link zur DOCAC JIRA-Aufgabe</a>

#### Erlebnis-Entscheidung

* **Experience Decisioning-Vorschau im Code-basierten Erlebniskanal** - Sie können jetzt beim Konfigurieren von Experience Decisioning mit dem Code-basierten Erlebniskanal Entscheidungselemente in der Vorschau anzeigen. Die Vorschau ist vor der Live-Schaltung direkt in der Authoring-Oberfläche verfügbar.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14082">Link zur DOCAC JIRA-Aufgabe</a>

* **Offer Ranking-KI-Modell-Beobachtbarkeit** - Mit Journey Optimizer können Sie jetzt den Zustand, den Trainingsstatus und die Leistung Ihrer KI-Modelle in Decisioning überwachen, um den Trainingserfolg zu überprüfen, Fehler zu beheben und die Auswirkungen auf Ihre Ergebnisse zu verstehen. Diese Funktion ist nur für personalisierte Optimierungsmodelle verfügbar (nicht für die automatische Optimierung).

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14040">Link zur DOCAC JIRA-Aufgabe</a>

* **Anhängen von Fragmenten an Entscheidungselemente**: Journey Optimizer bietet jetzt die Möglichkeit, Fragmente an Entscheidungselemente anzuhängen, die in Code-basierten Erlebniskampagnen über Entscheidungsrichtlinien genutzt werden können.

  **Hinweis**: Diese Verbesserung steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).

  Verfügbarkeit: 12. Februar 2026.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13418">Link zur DOCAC JIRA-Aufgabe</a>

#### Journeys

* **Mehrere eingehende Aktionen in Journeys** – Um die Orchestrierung Ihrer Journeys zu vereinfachen, können Sie jetzt mehrere eingehende Aktionen in einer einzigen Journey definieren. Diese Funktion war bisher in -Kampagnen verfügbar und ermöglicht es Ihnen, mehrere Code-basierte Erlebnisse, In-App-Nachrichten, Inhaltskarten oder Web-Aktionen an verschiedene Orte gleichzeitig zu senden, wobei jede Aktion bestimmte Inhalte enthält.

  **Hinweis**: Diese Verbesserung steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13453">Link zur DOCAC JIRA-Aufgabe</a>

* **SMS-Webhooks** - Webhooks werden jetzt von allen SMS-Anbietern unterstützt. Sie können jeden Webhook für einen bestimmten Zweck, eingehende Webhooks zum Erfassen eingehender Nachrichten und Feedback-Webhooks konfigurieren, um Versandbestätigungen, Statusaktualisierungen und andere nachrichtenbezogene Ereignisse zu erhalten. [Weitere Informationen](../sms/sms-webhook.md)

  Verfügbarkeit: 2. Februar 2026.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13978">Link zur DOCAC JIRA-Aufgabe</a>

<!--
## January '26 pre-release notes {#jan-26-01-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: January 27, 2026

### New capabilities {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Action activity in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supports a new generic <strong>Action activity</strong> that enables you to configure both single actions and <strong>multi-action inbound action groups</strong>, allowing for streamlined action configuration within the journey canvas. In particular, this new feature allows for:</p>
<ul>
<li>A simplified native action configuration within the journey canvas.</li>
<li>The capacity to create multi-action inbound action groups.</li>
<li>The ability to add optimization to any built-in channel action.</li>
<li>The ability to add both experimentation and multi-lingual options to any action.</li>
</ul>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13290">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gain deeper insight into the health and performance of your custom action endpoints with a new <strong>monitoring dashboard</strong> and enriched journey step event data. Track successful calls, errors, throughput, response times, and queue wait times to quickly understand when, where, and why anomalies occur.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13981">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-126869">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Quiet Hours / Time Based Exclusions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Quiet hours let you define <strong>time-based exclusions</strong> for Email, SMS, Push, and WhatsApp channels. They ensure that no messages are sent during specific periods of time, helping you respect customer preferences and compliance requirements. You can apply quiet hours through <strong>rule sets</strong>, which can be assigned to individual actions in campaigns or journeys for precise control.</p>
<p>Previously released in Limited Availability, this feature is now available to all environments. With this General Availability release, the feature now includes the ability for customer to queue a campaign action until the completion of Quiet Hours, and the ability to preview the activated Quiet Hours rule.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13986">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-63912">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, the <strong>Direct Mail channel</strong> is now available on the <strong>journey canvas</strong>, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13543">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-38399">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports <strong>Web Push notifications</strong>, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app. This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13581">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-37866">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning support in Push and SMS channels</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add <strong>Decision policies</strong> into push and SMS journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13426">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/DOCAC-13425">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55817">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55818">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The <strong>Direct mail activity</strong> facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the <strong>extraction file</strong> required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13379">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-82584">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New <strong>source connectors</strong> are now available in Adobe Experience Platform for the Talon.One, Capillary and Kobie loyalty Apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13372">Link to DOCAC JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Message Export</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Message Export</strong> capability is now available for email and SMS channels. This feature allows you to automatically export sent message content to a dedicated Experience Platform dataset, enabling you to:</p>
<ul>
<li>Meet regulatory compliance requirements (such as HIPAA)</li>
<li>Archive messages for legal claims and customer care inquiries</li>
<li>Retain copies of personalized content sent to individuals</li>
</ul>
<p>Records are retained in the AJO Message Export Dataset for <strong>7 calendar days from ingestion</strong>. During this retention period, you can export the data to your own storage via Experience Platform destinations. The feature is enabled at the channel configuration level, giving you granular control over which messages are exported.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12915">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105313">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent - Create a Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Create Agent enables Journey Optimizer users to build and configure marketing journeys using a natural language interface. With Journey Create Agent, practitioners can quickly create journeys by describing their requirements in conversational prompts. The agent streamlines journey creation, allowing marketers to focus on strategy rather than technical configuration.</p>
<p><a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide" target="_blank">Learn more</a></p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13747">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95142">Link to PRODUCT JIRA task</a></p>
<p>Availability date: January 12, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New API to retrieve Action Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Journey Optimizer API</strong> is now available, enabling you to programmatically retrieve and inspect campaign-related data such as details, versions, and configurations.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13506">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-96195">Link to PRODUCT JIRA task</a></p>
<p>Availability date: November 24, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New journey alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Three new <strong>journey alerts</strong> are now available to help you monitor and track journey lifecycle events and custom action performance:</p>
<ul>
<li><strong>Journey Published</strong>: Receive notifications when a journey is published by a practitioner in the journey canvas.</li>
<li><strong>Journey Finished</strong>: Get alerts when a journey has finished, with specific definitions based on journey type (Read Audience or Event-triggered).</li>
<li><strong>Custom Action Capping Triggered</strong>: Be notified when capping is activated on a custom action endpoint.</li>
</ul>
<p>These alerts can be subscribed to at the organization level or for specific journeys.</p>
<p>For more information, refer to the <a href="../reports/alerts.md#journey-alerts">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13465">Link to DOCAC JIRA task</a></p>
<p>Availability date: November 5, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Themes in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply <strong>pre-approved themes</strong> to ensure brand consistency across all emails, speed up your campaign creation process, and independently produce high-quality emails while reducing dependency on design teams.</p>
<p>Previously released in beta version, this capability is now available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<img src="assets/do-not-localize/themes.gif">
<p>For more information, refer to the <a href="../email/apply-email-themes.md">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12941">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/NEO-88838">Link to PRODUCT JIRA task</a></p>
<p>Availability date: November 5, 2025</p>
</td>
</tr>
</tbody>
</table>

### Improvements {#jan-26-01-improv}

Improvements coming with this release are listed below.

#### AI

* **AI Assistant Content Quality Checks** - In addition to brand alignment, you can now evaluate overall <strong>content quality</strong> to uncover potential issues with readability, cohesiveness, and effectiveness, independent of your brand guidelines. These automated checks help identify unclear messaging, inconsistent tone, or structural gaps.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13917">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-103238">Link to PRODUCT JIRA task</a>
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors section</strong> defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13811">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-121183">Link to PRODUCT JIRA task</a>

#### Campaigns

* **Schedule Campaign using Profile Time Zone** - Campaign scheduling can now use each profile's <strong>time zone</strong> to deliver messages at the intended local time.

  **Note**: This improvement is only available for a set of organizations (Limited Availability).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-11534">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-43782">Link to PRODUCT JIRA task</a>

#### Channels

* **SMS Webhooks: Phase II** - Description to be provided.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13978">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-93914">Link to PRODUCT JIRA task</a>

#### Email Designer

* **In-place corrections in the Email designer** - <strong>AI-powered automatic content suggestions</strong> are now available in the Email Designer when violations are detected during content validation. If content is flagged as misaligned with brand guidelines or fails quality criteria, the system proactively generates corrected alternatives that can be reviewed and applied inline, improving compliance and accelerating production.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13979">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95365">Link to PRODUCT JIRA task</a>

#### Experience Decisioning

* **Self-service migration tooling APIs** - A new set of <strong>migration tooling APIs</strong> is available to migrate Offer management entities to Experience Decisioning. The tooling enables seamless migration between sandboxes with dependency resolution and rollback capabilities.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13837">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-109695">Link to PRODUCT JIRA task</a>

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach <strong>fragments</strong> to decision items which can be leveraged in code-based experience campaigns through decision policies.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13418">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-110282">Link to PRODUCT JIRA task</a>

#### Journeys

* **Leverage a failure response payload in journey Custom Actions** - You can now define an optional <strong>error response payload</strong> for custom actions. When a call fails, the error payload is exposed in the journey context and is available in the timeout/error branch to support richer fallback logic and debugging.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13977">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113125">Link to PRODUCT JIRA task</a>

* **Combine native and Adobe Campaign message actions** - Journey Optimizer now lets you combine Adobe Campaign v7/v8 message actions with native channel actions in the same journey.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13974">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113103">Link to PRODUCT JIRA task</a>

* **Journey payload size validation in journeys** - Journey Optimizer now provides <strong>payload size validation</strong> to help ensure optimal performance and system stability. When building or publishing journeys, you receive clear warnings and errors if payload sizes approach or exceed recommended limits, along with actionable guidance to optimize your journey configuration. This proactive validation helps you identify potential issues early and maintain journey performance.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13840">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-122236">Link to PRODUCT JIRA task</a>

* **Multiple inbound actions in journeys** - To simplify your journey orchestration, you can now define <strong>multiple inbound actions</strong> in a single journey. Previously available in campaigns, this capability enables you to deliver multiple code-based experiences, In-app messages, Content Cards or web actions to different locations at the same time, each action containing a specific content.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13453">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a>

#### Orchestrated campaigns

* **Select attributes and copy distribution values** - You can now select or copy values directly from the distribution of values view in orchestrated campaigns.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13973">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105244">Link to PRODUCT JIRA task</a>

* **Data usage label inheritance for audiences** - <strong>Data usage labels</strong> applied in Adobe Experience Platform now automatically carry over when saving audiences in orchestrated campaigns, reducing manual DULE tagging.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13972">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-120769">Link to PRODUCT JIRA task</a>

* **Predefined retargeting filters** - To support easier retargeting for orchestrated campaign use cases, this release introduces new <strong>retargeting filters</strong>. These filters let you directly target audiences based on message engagement, such as sent, opened only, opened or clicked, or opened and clicked, and select the specific campaign or in-transition campaign you want to retarget.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13971">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-116701">Link to PRODUCT JIRA task</a>

* **Predefined filters with parameters** - You can now create <strong>filters with parameters</strong> in orchestrated campaigns for reusable, editable rules.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13970">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-115431">Link to PRODUCT JIRA task</a>

* **Message confirmation before send** - A <strong>confirmation step</strong> is now enabled by default before sending orchestrated campaigns to reduce accidental sends.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13927">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-87219">Link to PRODUCT JIRA task</a>

* **User-generated metadata support** - The <strong>executionMetadata helper function</strong> is now available in the personalization editor for Orchestrated Campaigns, enabling you to attach contextual information to any native action and store it in a dataset for export to external systems.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13923">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-112697">Link to PRODUCT JIRA task</a>

* **Restart button** - Orchestrated campaigns now include a <strong>restart button</strong> so you can quickly re-launch runs when needed before publishing the campaign.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13920">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-106020">Link to PRODUCT JIRA task</a>

* **Rate control support** - Orchestrated campaigns now support <strong>rate control</strong> to help you pace deliveries and align with volume constraints.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13764">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113254">Link to PRODUCT JIRA task</a>

#### Permissions

* **Prevent self-approval for journeys and campaigns** - You can now require that creators cannot approve their own journeys or campaigns, improving <strong>separation of duties</strong> in approval workflows.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13472">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99957">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95676">Link to PRODUCT JIRA task</a>

## Coming soon {#jan-26-01-coming-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

<table>
<thead>
<tr>
<th><strong>Content generation within Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Powered by Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> is available in Journey Optimizer and enables you to analyze journeys through a natural language interface. You can now also generate and manage channel-specific content directly in Journey Agent, creating content for channels such as email and push, applying and previewing templates, refining tone and style through prompts, and opening content in Content Designer for in-context editing.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13980">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111882">Link to PRODUCT JIRA task</a></p>
<p>Availability date: February 2, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Content decision activity</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now include <strong>personalized offers</strong> in your journeys through a dedicated Content decision activity in the journey canvas, and use them in journey activities, including conditions and custom actions.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12902">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99223">Link to PRODUCT JIRA task</a></p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>
-->
