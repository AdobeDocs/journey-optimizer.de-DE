---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 0c6b92d11b60e28c7dc918f7c4d7d7ced07a2ab5
workflow-type: tm+mt
source-wordcount: '1260'
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

## Versionshinweise Februar 2026 {#feb-26-01-rn}

Die Abschnitte [Neue Funktionen](#feb-26-01-features) und [Verbesserungen](#feb-26-01-improv) decken bereits verfügbare Funktionen ab. Der [Demnächst](#coming-soon) Abschnitt enthält Funktionen und Verbesserungen, die im Februar veröffentlicht werden sollen.

<!--**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

<!--**Release date**: February 17-18, 2026-->

### Neue Funktionen {#feb-26-01-features}


<!--
<table>
<thead>
<tr>
<th><strong>Mobile Live Activities</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Live Activities</strong> provide real-time updates and interactive experiences within mobile apps, allowing users to stay informed about ongoing events or tasks directly on their device's screen. This feature enhances engagement by delivering live information, such as progress tracking, event updates, or interactive content, without requiring users to open the app.</p>
<p>Previously released in beta, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Migrieren von Subdomains zur benutzerdefinierten Delegierung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Subdomains mit dem CNAME-Delegierungsmodus direkt über die Benutzeroberfläche in die benutzerdefinierte Delegierung migrieren, damit Sie strengere Sicherheitsrichtlinien gemäß den Richtlinien Ihres Unternehmens einhalten können, ohne die Kanalkonfigurationen neu erstellen zu müssen.</p>
<p><img src="assets/do-not-localize/subdomain-migration.gif"/></p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/custom-subdomain-migration.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Freitag, 19. Februar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web-Push-Benachrichtigungskanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer unterstützt jetzt <strong>Web-Push-Benachrichtigungen</strong> und erweitert den Push-Kanal über Mobile hinaus. Sie können Benachrichtigungen nahtlos an <strong>mobile und Desktop-Browser</strong> senden, sodass Ihre Kundinnen und Kunden direkt auf ihren Geräten erreicht werden, ohne dass eine App erforderlich ist. Diese Verbesserung ermöglicht es Ihnen, Benutzende in Echtzeit mit zeitnahen, personalisierten Nachrichten anzusprechen, unter Nutzung derselben Authoring-Workflows und Targeting-Funktionen, die bereits für mobile Push-Benachrichtigungen verfügbar sind.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>Diese Funktion wurde bereits in Beta veröffentlicht und steht allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../push/push-configuration-web.md">ausführlichen Dokumentation</a>.</p>
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
<p>Eine neue <strong>Aktivität Inhaltsentscheidung</strong> ist jetzt auf der Journey-Arbeitsfläche verfügbar, um personalisierte Angebote direkt in die Journey Ihrer Kunden zu integrieren. Mit dieser Aktivität können Sie entscheidungsbasierte Inhalte bereitstellen und diese Angebote auf Ihrem gesamten Journey referenzieren - unter Bedingungen für die Erstellung von Verzweigungen auf der Grundlage der Eignung, bei benutzerdefinierten Aktionen zur Weitergabe von Angebotsdaten an externe Systeme und bei anderen Aktivitäten zur Erstellung vollständig personalisierter Kundenerlebnisse.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/content-decision.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Mittwoch, 10. Februar 2026</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#feb-26-01-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.

#### Konfiguration

* **Nutzung von Erlebnisereignissen in Journey-Ausdrücken** - Ab dem 1. April 2026 wird die Verwendung von Erlebnisereignisattributen in Journey-Ausdrücken für Organisationen, die diese Funktion in den letzten 90 Tagen nicht verwendet haben, nicht mehr unterstützt. Diese Funktion ist bereits seit dem 8. Juli 2025 für neue Kundenorganisationen nicht mehr verfügbar. Alternativen finden Sie unter [Suche nach Erlebnisereignissen in Journey](../building-journeys/exp-event-lookup.md).

#### E-Mail-Designer

* **Texteinzug** - Sie können jetzt eine anpassbare linke Einrückung auf die erste Zeile von Absätzen in Textkomponenten direkt über das Eigenschaftenbedienfeld anwenden. <!--The new **Indentation** control lets you define indentation in pixels or percentage via a numeric input or slider, with live preview on the canvas. -->Dies verbessert die Lesbarkeit von Langforminhalten wie Leitartikeln und Artikeln.

  Verfügbarkeit: 18. Februar 2026.

#### Inhaltsvorlagen

* **Verwenden von Designs zum Konvertieren von Bildern in E-Mail-Vorlagen** - Beim Konvertieren eines Bildes in eine E-Mail-Vorlage in Journey Optimizer können Sie jetzt ein Design als Eingabe verwenden, sodass die generierte HTML Ihren Markenparametern entspricht. Stile wie Hintergrundfarbe, Schaltflächenfarbe, Schriftarten, Zeilenabstand, Ränder und Abstand werden automatisch angewendet, wodurch die manuelle Entwurfsarbeit reduziert wird und eine Vorlage bereitgestellt wird, die mit minimalen Bearbeitungen verwendet werden kann. [Weitere Informationen](../content-management/image-to-html.md)

  Verfügbarkeit: 17. Februar 2026.


#### Erlebnis-Entscheidung

* **Eingehende Edge-Unterstützung für die Verwendung von Adobe Experience Platform-Daten in Decisioning** - Die Verwendung von Adobe Experience Platform-Daten in Decisioning unterstützt jetzt eingehende Edge-Anwendungsfälle zusätzlich zu E-Mail und benutzerdefinierten Aktionen in Journey. [Weitere Informationen](../experience-decisioning/aep-data-exd.md)

  **Hinweis**: Diese Funktion ist nur für eine Reihe von Organisationen verfügbar (<strong>eingeschränkte Verfügbarkeit</strong>). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.


* **Anhängen von Fragmenten an Entscheidungselemente** – Journey Optimizer bietet jetzt die Möglichkeit, Fragmente an Entscheidungselemente anzuhängen, die in Code-basierten Erlebniskampagnen über Entscheidungsrichtlinien genutzt werden können. [Weitere Informationen](../experience-decisioning/fragments-decision-policies.md)

  **Hinweis**: Diese Funktion war zuvor nur in begrenzter Verfügbarkeit verfügbar und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).

  Verfügbarkeit: 12. Februar 2026.

## Demnächst {#coming-soon}

Die folgenden Funktionen und Verbesserungen sind für Ende Februar geplant. Veröffentlichungstermine und Umfang können sich ohne vorherige Ankündigung ändern.

<table>
<thead>
<tr>
<th><strong>Journey Agent: Erstellung von Kanalinhalten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit <strong>Adobe Experience Platform Agent Orchestrator </strong> ist <strong>Journey Agent</strong> in Journey Optimizer verfügbar und ermöglicht es Ihnen, Journey über eine natürliche Sprachschnittstelle zu analysieren. Sie können jetzt auch kanalspezifische Inhalte direkt in Journey Agent generieren und verwalten, Inhalte für Kanäle wie E-Mail und Push erstellen, Vorlagen anwenden und in der Vorschau anzeigen, Ton und Stil durch Eingabeaufforderungen verfeinern und Inhalte in <strong>Content Designer</strong> zur kontextbezogenen Bearbeitung öffnen.</p>
<p>Verfügbarkeitsdatum: Samstag, 20. Februar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Senden ausgehender Nachrichten schwenken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt den Versand von ausgehenden Nachrichten aus Journey Optimizer-Kampagnen oder Journey-Sendungen in kontrollierten Batches über einen bestimmten Zeitraum planen.</p>
<p>Der Wave-Versand bietet die folgenden Vorteile:</p>
<ul>
<li>Bessere Zustellbarkeit: Spread sendet im Laufe der Zeit, um einen guten Ruf als Absender zu wahren und das Risiko zu reduzieren, als Spam gekennzeichnet zu werden.</li>
<li>Laststeuerung - Vermeiden Sie die Überlastung nachgelagerter Systeme (z. B. Callcenter, Landingpages), indem Sie einschränken, wie viele Nachrichten gleichzeitig gesendet werden.</li>
<li>Anwendungsfälle mit hohem Volumen und zeitkritischer Relevanz - geeignet für große Zielgruppen oder zur Steuerung des Timings (z. B. Call-Center-Kapazität, Anlaufphase oder zeitlich begrenzte Angebote).</li>
</ul>
<p>In -Kampagnen ist diese Funktion für alle Umgebungen verfügbar (allgemeine Verfügbarkeit).</p>
<p>In Journey ist diese Funktion nur für bestimmte Unternehmen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p>Verfügbarkeitsdatum: Samstag, 20. Februar 2026</p>
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
<p>Sie können jetzt <strong>Rangfolgeformeln</strong> und <strong>KI-Modelle</strong> verwenden, um die Journey-Prioritätswerte basierend auf Kundenprofilattributen und Kontextfaktoren automatisch zu erhöhen und so sicherzustellen, dass Kunden in die relevantesten Journey eintreten.</p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p>Verfügbarkeitsdatum: Mittwoch, 24. Februar 2026</p>
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
<p>Journey Optimizer unterstützt eine neue generische <strong>Aktionsaktivität</strong> mit der Sie sowohl Einzelaktionen als auch eingehende Aktionsgruppen mit mehreren Aktionen konfigurieren können, was eine optimierte Aktionskonfiguration innerhalb der Journey-Arbeitsfläche ermöglicht. Diese neue Funktion ermöglicht insbesondere Folgendes:</p>
<ul>
<li>Eine vereinfachte, native Aktionskonfiguration innerhalb der Journey-Arbeitsfläche</li>
<li>Die Möglichkeit, eingehende Aktionsgruppen mit mehreren Aktionen zu erstellen</li>
<li>Die Möglichkeit, jeder integrierten Kanalaktion eine Optimierung hinzuzufügen</li>
<li>Die Möglichkeit, jeder Aktion sowohl experimentelle als auch mehrsprachige Optionen hinzuzufügen.</li>
</ul>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum: Samstag, 20. Februar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>KI-Modellüberwachung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Journey Optimizer können Sie jetzt den Zustand, den Trainingsstatus und die Leistung Ihrer KI-Modelle für die Entscheidungsfindung überwachen. Auf diese Weise können Sie den Schulungserfolg überprüfen, Fehler beheben und die Auswirkungen auf Ihre Ergebnisse verstehen, um mithilfe von KI die besten Angebote für jeden Kunden auszuwählen. Beachten Sie, dass diese Funktion nur für <strong>Decisioning</strong> verfügbar ist (nicht für ältere Entscheidungs-Management-Modelle).</p>
<p>Diese Funktion ist derzeit nur für Modelle <strong>personalisierte Optimierung</strong> verfügbar (nicht für die automatische Optimierung).</p>
<p>Verfügbarkeitsdatum: Samstag, 20. Februar 2026</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#coming-soon-improv}

* **Experience Decisioning-Vorschau im Code-basierten Erlebniskanal** - Sie können jetzt beim Konfigurieren von Experience Decisioning mit dem Code-basierten Erlebniskanal Entscheidungselemente in der Vorschau anzeigen. Die Vorschau ist vor der Live-Schaltung direkt in der Authoring-Oberfläche verfügbar.

  Verfügbarkeit: 20. Februar 2026.

* **Integration von benutzerdefinierten Firefly-Modellen und Drittanbieter-Image-Generierungsmodellen** - Ermöglichen Sie die nahtlose Integration von standardmäßigen und benutzerdefinierten Firefly-Modellen zusammen mit genehmigten Drittanbieter-Image-Modellen (z. B. NanoBanana), um mehr Flexibilität, Kontrolle und Markenausrichtung bei der Bilderstellung zu bieten. Auf diese Weise können Sie für jeden Anwendungsfall das beste Modell auswählen: standardmäßige Firefly für allgemeine Anforderungen, benutzerdefinierte Firefly für die Markengenerierung oder genehmigte Drittanbietermodelle für spezialisierte oder experimentelle Szenarien.

  Verfügbarkeit: 20. Februar 2026.

