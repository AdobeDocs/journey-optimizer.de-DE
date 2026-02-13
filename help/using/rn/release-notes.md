---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 7263e5ace72823ce7a3a184d2842f9bba495c068
workflow-type: tm+mt
source-wordcount: '1537'
ht-degree: 31%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] verwendet ein kontinuierliches Bereitstellungsmodell, das es Adobe ermöglicht, laufend neue Funktionen, Verbesserungen und Fehlerbehebungen bereitzustellen. Dieser Ansatz ermöglicht ein skalierbares Rollout von Funktionen in Phasen, um die Leistung und Stabilität aller Umgebungen sicherzustellen.

Aufgrund dieses Modells werden die Versionshinweise zwischen den monatlichen Versionen aktualisiert.  Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Hinweise zur Vorabversion vom Februar 2026 {#feb-26-01-rn}

**Die nachfolgenden Vorab- Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentationen werden in den Versionshinweisen am Veröffentlichungsdatum veröffentlicht.

Siehe auch [Vorab veröffentlichte Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Veröffentlichungsdatum**: 17.-18. Februar 2026

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
<p>Sie können den Versand ausgehender Nachrichten von <strong>Kampagnen</strong> oder <strong>Journey</strong> in kontrollierten <strong>Batches) </strong>.</p>
<p>Der Wave-Versand bietet die folgenden Vorteile:</p>
<ul>
<li>Bessere <strong>Zustellbarkeit</strong> - Spread sendet im Laufe der Zeit, um einen guten Ruf <strong> Absenders </strong> wahren und das Risiko zu verringern, als Spam gekennzeichnet zu werden.</li>
<li><strong>Lastkontrolle</strong> - Vermeiden Sie die Überlastung nachgelagerter Systeme (z. B. Callcenter, Landingpages), indem Sie einschränken, wie viele Nachrichten gleichzeitig gesendet werden.</li>
<li>Anwendungsfälle mit hohem Volumen und zeitkritischer Relevanz - geeignet für große Zielgruppen oder zur Steuerung des Timings (z. B. Call-Center-Kapazität, Anlaufphase oder zeitlich begrenzte Angebote).</li>
</ul>
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
<p>Sie können jetzt <strong>Formeln</strong> und <strong>KI-Modelle</strong> verwenden, um die <strong>Journey-Prioritätswerte </strong> auf der Grundlage von Kundenprofilattributen und Kontextfaktoren automatisch zu steigern und so sicherzustellen, dass Kunden die relevantesten Journey eingeben.</p>
<p>Diese Funktion ist nur für ausgewählte Organisationen verfügbar (<strong>eingeschränkte Verfügbarkeit</strong>). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
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
<p>Mit <strong>Adobe Experience Platform Agent Orchestrator </strong> ist <strong>Journey Agent</strong> in Journey Optimizer verfügbar und ermöglicht die Analyse von Journey über eine <strong>Natural Language Interface</strong>. Sie können jetzt auch kanalspezifische Inhalte direkt in Journey Agent generieren und verwalten, Inhalte für Kanäle wie E-Mail und Push erstellen, Vorlagen anwenden und in der Vorschau anzeigen, Ton und Stil durch Eingabeaufforderungen verfeinern und Inhalte in <strong>Content Designer</strong> zur kontextbezogenen Bearbeitung öffnen.</p>
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
<p><strong>Live-Aktivitäten</strong> bieten <strong>Echtzeit-Updates</strong> und interaktive Erlebnisse in mobilen Apps, sodass Benutzer direkt auf dem Bildschirm ihres Geräts über laufende Ereignisse oder Aufgaben informiert bleiben. Diese Funktion verbessert die Interaktion, indem Live-Informationen wie Fortschritts-Tracking, Ereignisaktualisierungen oder interaktive Inhalte bereitgestellt werden, ohne dass Benutzende die App öffnen müssen.</p>
<p>Diese Funktion wurde bereits in der Beta-Version veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
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
<p>Journey Optimizer unterstützt eine neue generische <strong>Aktionsaktivität</strong> mit der Sie sowohl Einzelaktionen als auch <strong>Aktionsgruppen mit mehreren eingehenden Aktionen</strong> konfigurieren können, was eine optimierte Aktionskonfiguration innerhalb der <strong>Journey-Arbeitsfläche </strong>. Diese neue Funktion ermöglicht insbesondere Folgendes:</p>
<ul>
<li>Eine vereinfachte, native Aktionskonfiguration innerhalb der Journey-Arbeitsfläche</li>
<li>Die Möglichkeit, eingehende Aktionsgruppen mit mehreren Aktionen zu erstellen</li>
<li>Die Möglichkeit, <strong>Optimierung</strong> zu jeder integrierten Kanalaktion hinzuzufügen.</li>
<li>Die Möglichkeit, jeder Aktion sowohl <strong>Experiment</strong> als <strong>mehrsprachig</strong> Optionen hinzuzufügen.</li>
</ul>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
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
<p>Adobe Journey Optimizer unterstützt jetzt <strong>Web-Push-Benachrichtigungen</strong> und erweitert damit den Push-Kanal über den mobilen Gebrauch hinaus. Sie können Benachrichtigungen nahtlos an mobile und Desktop-Browser senden, sodass Ihre Kundinnen und Kunden direkt auf ihren Geräten erreicht werden, ohne dass eine App erforderlich ist. Diese Verbesserung ermöglicht es Ihnen, Benutzer mit zeitnahen, personalisierten Nachrichten in Echtzeit zu interagieren, wobei die gleichen <strong>Authoring-Workflows</strong> und <strong>Targeting-Funktionen</strong> genutzt werden, die bereits für mobile Push-Benachrichtigungen verfügbar sind.</p>
<p>Diese Funktion wurde bereits in der Beta-Version veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum: Samstag, 13. Februar 2026</p>
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
<p>Eine neue <strong>Inhaltsentscheidungsaktivität</strong> ist jetzt auf der <strong>Journey-Arbeitsfläche verfügbar</strong> um "<strong> Angebote“ </strong> Ihren Kunden-Journey zu integrieren. Mit dieser Aktivität können Sie entscheidungsbasierte Inhalte bereitstellen und diese Angebote auf Ihrem gesamten Journey referenzieren - unter Bedingungen für die Erstellung von Verzweigungen auf der Grundlage der Eignung, bei benutzerdefinierten Aktionen zur Weitergabe von Angebotsdaten an externe Systeme und bei anderen Aktivitäten zur Erstellung vollständig personalisierter Kundenerlebnisse.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/content-decision.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 11. Februar 2026</p>
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
<p><strong>Migrations-Tool</strong>APIs sind jetzt verfügbar, um <strong>Entscheidungs-Management</strong>-Entitäten programmgesteuert nach <strong>Decisioning</strong> zu migrieren.</p>
<ul>
<li>Flexible Migrationsumfänge (<strong>Sandbox</strong>, <strong>Angebot</strong> oder <strong>Entscheidungs</strong>Ebene)</li>
<li>Automatisierte <strong>Abhängigkeitsanalyse</strong> und -validierung</li>
<li><strong>Rollback-Unterstützung</strong> für abgeschlossene Migrationen</li>
<li>Detaillierte Migrationsberichte mit Objektzuordnungen</li>
</ul>
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/decisioning-migration-api.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 3. Februar 2026</p>
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
<p>Vertiefen Sie insight in den Zustand und die Leistung Ihrer <strong>benutzerdefinierten Aktionsendpunkte</strong> mit einem neuen <strong>Überwachungs-Dashboard</strong> und angereicherten <strong>Journey-Schritt-Ereignisdaten</strong>. Verfolgen Sie erfolgreiche Aufrufe, Fehler, Durchsatz, Antwortzeiten und Warteschlangenwartezeiten nach, um schnell zu erkennen, wann, wo und warum Anomalien auftreten.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../action/reporting.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 3. Februar 2026</p>
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
<p>Sie können jetzt den Inhalt Ihrer (SMS<strong>Nachrichten) mit </strong>Decisioning<strong> personalisieren und </strong>. Verwenden Sie <strong>Prioritätswerte</strong>, <strong>Formeln</strong> oder <strong>KI-Modelle</strong>, um Ihren Kundinnen und Kunden den besten Inhalt anzuzeigen.</p>
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/create-decision.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 2. Februar 2026</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#feb-26-01-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.

#### Konfiguration

* **Nutzung von Erlebnisereignissen in Journey-Ausdrücken** - Ab dem 1. April 2026 wird die Verwendung von Erlebnisereignisattributen in Journey-Ausdrücken für Organisationen, die diese Funktion in den letzten 90 Tagen nicht verwendet haben, nicht mehr unterstützt. Diese Funktion ist bereits seit dem 8. Juli 2025 für neue Kundenorganisationen nicht mehr verfügbar. Alternativen finden Sie unter [Suche nach Erlebnisereignissen in Journey](../building-journeys/exp-event-lookup.md).


* **Wechsel der Methode der Subdomain** - Sie können jetzt von einer Methode <strong>Subdomain-Zuweisung</strong> zu einer anderen wechseln. Auf diese Weise können Sie Domains mit dem Modus <strong>CNAME-Delegierung</strong> in die Methode <strong>benutzerdefinierte Delegierung</strong> migrieren, um die Sicherheitsrichtlinien Ihres Unternehmens einzuhalten.

  **Hinweis**: Diese Funktion ist nur für eine Reihe von Organisationen verfügbar (<strong>eingeschränkte Verfügbarkeit</strong>). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.


#### E-Mail-Designer

* **Verwenden eines Markendesigns zum Konvertieren eines Bildes in eine E-Mail-Vorlage** - Beim Konvertieren eines Bildes in eine E-Mail-Vorlage in Journey Optimizer können Sie jetzt ein <strong>Design</strong> als Eingabe verwenden, sodass das generierte HTML Ihren <strong>Markenparametern</strong> folgt. Stile wie Hintergrundfarbe, Schaltflächenfarbe, Schriftarten, Zeilenabstand, Ränder und Abstand werden automatisch angewendet, wodurch die manuelle Entwurfsarbeit reduziert wird und eine Vorlage bereitgestellt wird, die mit minimalen Bearbeitungen verwendet werden kann.


* **Aktualisieren von Marken mit neuer Farbregisterkarte** - <strong>Markenrichtlinien</strong> helfen sicherzustellen, dass Ihre Marke auf allen Touchpoints konsistent präsentiert wird. Der neue <strong>Abschnitt „Farben“</strong> definiert die Standards für das Farbsystem Ihrer Marke und beschreibt, wie Farben in Erlebnissen ausgewählt, organisiert und angewendet werden. Es sorgt für die konsistente Verwendung von primären, sekundären, Akzent- und neutralen Farben, um eine kohärente, barrierefreie und erkennbare Markenidentität zu unterstützen.


#### KI

* **Integration von benutzerdefinierten Firefly-Modellen und Drittanbieter-Image-Generierungsmodellen** - Ermöglicht die nahtlose Integration von standardmäßigen und benutzerdefinierten <strong>Firefly-Modellen</strong> zusammen mit genehmigten <strong>Drittanbieter-Image-Modellen</strong> (z. B. NanoBanana), um mehr Flexibilität, Kontrolle und Markenausrichtung beim Generieren von Images zu bieten. Auf diese Weise können Sie für jeden Anwendungsfall das beste Modell auswählen: standardmäßige Firefly für allgemeine Anforderungen, benutzerdefinierte Firefly für die Markengenerierung oder genehmigte Drittanbietermodelle für spezialisierte oder experimentelle Szenarien.


#### Erlebnis-Entscheidung

* **Eingehende Edge-Unterstützung für die Verwendung von Adobe Experience Platform-Daten in Decisioning** - Die Entscheidungsunterstützung für die <strong>Experience Platform</strong>Datensuche umfasst jetzt Anwendungsfälle <strong>eingehende Edge</strong>Kanäle. Die Funktion ist weiterhin nur eingeschränkt verfügbar. Die allgemeine Verfügbarkeit der zugrunde liegenden Datensuchfunktion wird noch nicht angekündigt (AEP/Produktabhängigkeit).

  **Hinweis**: Diese Funktion ist nur für eine Reihe von Organisationen verfügbar (<strong>eingeschränkte Verfügbarkeit</strong>). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.


* **Experience Decisioning-Vorschau im Code-basierten Experience**-Kanal<strong> Sie können jetzt eine Vorschau von Entscheidungselementen</strong> anzeigen, wenn Sie <strong>Experience Decisioning</strong> mit dem <strong>Code-basierten Experience</strong>-Kanal konfigurieren. Die Vorschau ist vor der Live-Schaltung direkt in der Authoring-Oberfläche verfügbar.


* **Offer Ranking-KI-Modellbeobachtbarkeit** - Mit Journey Optimizer können Sie jetzt den <strong>Zustand</strong>, <strong>Trainingsstatus</strong> und <strong>Performance</strong> Ihrer <strong>KI-Modelle</strong> in Decisioning überwachen, um den Trainingserfolg zu überprüfen, Fehler zu beheben und die Auswirkungen auf Ihre Ergebnisse zu verstehen. Diese Funktion ist nur für personalisierte Optimierungsmodelle verfügbar (nicht für die automatische Optimierung).


* **Fragmente an Entscheidungselemente anhängen** - Journey Optimizer bietet jetzt die Möglichkeit, <strong>Fragmente</strong> an <strong>Entscheidungselemente</strong> anzuhängen, die in code-basierten Erlebniskampagnen über <strong>Entscheidungsrichtlinien</strong> werden können.

  **Hinweis**: Diese Funktion war zuvor nur in begrenzter Verfügbarkeit verfügbar und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).

  Verfügbarkeit: 12. Februar 2026.


#### Journeys

* **Mehrere eingehende Aktionen in Journey** - Um Ihre Journey-Orchestrierung zu vereinfachen, können Sie jetzt mehrere <strong>eingehende Aktionen</strong> in einer einzigen Journey definieren. Diese Funktion war bisher in Kampagnen verfügbar und ermöglicht es Ihnen, mehrere <strong>Code-basierte Erlebnisse</strong>, <strong>In-App-</strong>, <strong>Inhaltskarten</strong> oder <strong>Web-Aktionen</strong> an verschiedenen Orten gleichzeitig bereitzustellen, wobei jede Aktion bestimmte Inhalte enthält.

  **Hinweis**: Diese Funktion war zuvor nur in begrenzter Verfügbarkeit verfügbar und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).


* **SMS-Webhooks** – <strong>Webhooks</strong> werden jetzt für alle SMS-Anbieter unterstützt. Sie können jeden Webhook entsprechend seinem Verwendungszweck konfigurieren: <strong>eingehende Webhooks</strong> um eingehende Nachrichten und <strong>Feedback-Webhooks</strong> zu erfassen, um Versandbestätigungen, Statusaktualisierungen und andere nachrichtenbezogene Ereignisse zu erhalten. [Weitere Informationen](../sms/sms-webhook.md)

  Verfügbarkeit: 2. Februar 2026.