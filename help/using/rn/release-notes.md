---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: dcb2be7fef47e0d62fdd5a423799823ba4ef586c
workflow-type: tm+mt
source-wordcount: '2053'
ht-degree: 71%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert. [!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.


## Versionshinweise Juli &#39;25 {#25-7-rn}

<!--
**Pre release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

**Veröffentlichungsdatum**: Mittwoch, 29. Juli 2025

### Neue Funktionen {#features-25-7}

Im Folgenden werden die neuen Funktionen dieser Version beschrieben.

#### Funktionen

<table>
<thead>
<tr>
<th><strong>WhatsApp-Kanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer unterstützt jetzt WhatsApp-Direktnachrichten und ermöglicht so eine reibungslose Integration in Ihre Journey und Kampagnen zur Verbesserung der Empfängerkommunikation und -interaktion. Dieser native Kanal bietet vorkonfigurierte Integration von WhatsApp-Vorlagen, Nachrichtenvorschau, Personalisierung, Versandberichte, Webhooks, Opt-in- und Opt-out-Einverständnisverwaltung und mehr.</p>
<p>Diese Funktion wurde bereits in Beta veröffentlicht und ist jetzt für alle Umgebungen verfügbar (allgemeine Verfügbarkeit).</p>
<p><img src="../whatsapp/assets/do-not-localize/WA-Animation.gif"/><p>
<p>Weitere Informationen finden Sie in der <a href="../whatsapp/get-started-whatsapp.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Marken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Ihre eigenen Marken erstellen und anpassen, um Ihre visuelle und verbale Identität in der gesamten Kommunikation klar zu definieren. Mit der Bewertung zur Markenausrichtung erhalten Sie Echtzeit-Feedback dazu, wie gut Ihr Inhalt den Ton, den Stil und die Richtlinien Ihrer Marke widerspiegelt. So bleiben Sie mit jeder gesendeten Nachricht konsequent auf dem Laufenden.</p>
<p>Diese Funktion wurde bereits in Beta veröffentlicht und ist jetzt für alle Umgebungen verfügbar (allgemeine Verfügbarkeit).</p>
<p><img src="assets/do-not-localize/brand-score.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../content-management/brands.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verwenden von Experience Decisioning im E-Mail-Kanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Entscheidungsrichtlinien zu E-Mail-Journey und -Kampagnen hinzufügen. Entscheidungsrichtlinien sind Container für Ihre Angebote, die die Decisioning-Engine nutzen, um dynamisch die besten Inhalte zurückzugeben, die für jedes Mitglied der Zielgruppe bereitgestellt werden können.</p>
<p>Diese Funktion ist nur in begrenztem Umfang verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.</p>
Weitere Informationen finden Sie in der <a href="../experience-decisioning/create-decision.md">detaillierten Dokumentation</a></p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Optimization in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer now empowers you with the tools to deliver personalized and optimized content to your campaigns' audience, allowing you to run content experiments, create rule-based targeting, and use advanced combinations of both, to maximize the effectiveness of your campaigns.</p>
<p>With Optimization, you can:</p>
<ul>
<li>Test multiple content variations to identify the most effective messaging.</li>
<li>Deliver personalized content based on user attributes and contextual data.</li>
<li>Combine targeting and experimentation for advanced campaign strategies.</li>
<li>Filter out users that do not match variant criteria.</li>
<li>Ensure fallback mechanisms to maintain user engagement.</li>
</ul>
<P>Once the campaign is live, profiles are evaluated against the defined criteria, and based on matching criteria, they are delivered with the appropriate experience or content from the campaign.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>
-->

<!--table>
<thead>
<tr>
<th><strong>Dark mode in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Journey Optimizer Email Designer now offers the ability to switch to dark mode view, where you can additionally define specific custom settings that will display only for recipients reading their emails in dark mode.</p>
<p>Note the following:</p>
<ul>
<li>The dark mode final rendering may vary and depends on the recipient's email client.</li>
<li>Not all email clients support custom dark mode. Moreover, some email clients only apply their own default dark mode for all emails that are received. In both cases, the custom settings that you defined in the Email Designer cannot be rendered.</li>
</ul>
<P>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a>. </p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey Probelauf</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der Journey-Probelauf ist ein spezieller Journey-Veröffentlichungsmodus in Adobe Journey Optimizer, der es Journey-Anwendenden ermöglicht, eine Journey mit echten Produktionsdaten zu testen, ohne echte Kundinnen und Kunden zu kontaktieren oder Profilinformationen zu aktualisieren. Mit dieser Funktion können Journey-Anwendende Vertrauen in ihr Journey-Design und die Zielgruppenbestimmung gewinnen, bevor sie die Journey live veröffentlichen.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Diese Funktion wurde zuvor mit eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/journey-dry-run.md">detaillierten Dokumentation</a></p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Calendar view</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A calendar view is now available in the journeys and campaigns lists. It allows you to visualize all journeys and campaigns activations in the respective lists.</p>
<p>Previously available in Limited Availability, this feature is now available to all environments. With this General Availability release, the feature includes:</p>
<ul>
<li>Design improvements for the navigation in dates</li>
<li>The ability to see draft campaigns if you have set a start and end date</li>
<li>A new setting to hide and show calendar items running for a long time</li>
</ul>
<img src="assets/do-not-localize/calendar.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Zusätzliche ID für Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können nun Journeys auslösen, indem Sie eine Profilkennung zusammen mit einer anderen Kennung wie einer Bestell-, Abonnement- oder Rezept-ID verwenden, sodass dasselbe Profil mehrmals in derselben Journey vorhanden sein kann. Dies ermöglicht Szenarien wie die parallele Verwaltung mehrerer Bestellungen oder Abonnements, wobei jede Instanz ihrem eigenen Pfad durch die Journey folgt.</p>
<p>Die Verwendung zusätzlicher IDs in Journey wurde früher nur eingeschränkt verfügbar gemacht und ist jetzt für alle Umgebungen verfügbar. Mit dieser allgemeinen Verfügbarkeitsversion bietet die Funktion jetzt Unterstützung für Journey unter Zielgruppe lesen .</p>
<p><img src="assets/do-not-localize/gif-supplemental.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/supplemental-identifier.md">detaillierten Dokumentation</a></p>
</td>
</tr>
</tbody>
</table>

### Änderung bei den Journey-Bedingungen {#ee-change@}

Seit dem 8. Juli wird das Erstellen von Ausdrücken mit Erlebnisereignissen in neuen Kundenorganisationen in dem in Journey-Bedingungen verwendeten Ausdruckseditor nicht mehr unterstützt. Daher können Erlebnisereignisse in der [Experience Platform-Datenquelle](../datasource/adobe-experience-platform-data-source.md) nicht zum Erstellen von Ausdrücken verwendet werden. Alternative Ansätze und Best Practices zum Erstellen von Ausdrücken/Logik mit Erlebnisereignissen sind [hier](../building-journeys/exp-event-lookup.md) zu finden.

Der Zugriff auf Journey-Kontextereignisdaten in unitären Journeys wird nicht geändert. In den Ausdrucks- und Personalisierungseditoren können Benutzende weiterhin auf Daten zugreifen, die mit dem ersten Journey-Ereignis übergeben wurden.

Weitere Informationen finden Sie [in diesen FAQ](../building-journeys/exp-event-lookup.md#faq-ee).

### Verbesserungen {#25-7-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.

- **Kampagnen**

   - **Mehrere eingehende Aktionen in Kampagnen** - Um die Kampagnenorchestrierung zu vereinfachen, können jetzt mehrere eingehende Aktionen in einer einzelnen Kampagne definiert werden. Mit dieser Funktion können Sie mehrere Code-basierte Erlebnisse, In-App-Nachrichten, Inhaltskarten oder Web-Aktionen gleichzeitig an verschiedenen Orten bereitstellen, wobei jede Aktion einen bestimmten Inhalt enthält.
  <!-- [Read more](../FILE.md) -->

   - **Neuorganisation des Kampagnenbestands** - Geplante und API-ausgelöste Kampagnen sind jetzt im Kampagneninventar in separate Registerkarten unterteilt, um die Navigation und Verwaltung zu erleichtern.

[Mehr dazu](../campaigns/modify-stop-campaign.md)

- **Daten-Management**
   - **Aktualisierung der Systemdatensätze des Entscheidungs-Managements** - Die gelöschten personalisierten Angebote und Fallback-Angebote sind jetzt in den Datensätzen „decision_object_repository_personalized_offers“ und „decision_object_repository_fallback_offers“ als archiviert gekennzeichnet. Die vorhandenen Datensätze im Datensatz werden nicht geändert.

[Mehr dazu](../offers/export-catalog/access-dataset.md)

- **Journeys**
   - **Verbesserungen beim Journey der Sandbox-Tools** - Beim Kopieren von Journeys über mehrere Sandboxes hinweg mithilfe der Paketexport- und -importfunktionen sind jetzt auch die folgenden Funktionen verfügbar:
      - Auswählen eines vorhandenen Ereignisses am Ziel
      - Kopieren eines Ereignisses unabhängig von einer Journey
      - Erkennen von Feldergruppen-/Datenquellenbeziehungen, Verknüpfen mit ihnen am Ziel, wenn sie vorhanden sind, Erstellen von ihnen, wenn sie nicht vorhanden sind.

[Mehr dazu](../configuration/copy-objects-to-sandbox.md)

- **Kanal - In-App**
   - **In-App-Schlüssel/Wert-Paare** - Bei In-App-Nachrichten können Sie Schlüssel- und Wert-Paare definieren, um benutzerdefinierte Variablen in die Nachrichten-Payload aufzunehmen. Diese Schlüssel-Wert-Paare ermöglichen es Ihnen, zusätzliche Daten basierend auf Ihrer spezifischen Konfiguration und Ihrem Anwendungsfall zu übergeben. [Weitere Informationen](../in-app/design-in-app.md)

- **Kanal - Inhaltskarte**

   - **Regelbasierte Kampagnendisqualifizierung** - Bei der Bearbeitung zusätzlicher Versandregeln wurde die Option Vorherige Versandregeln durch drei verschiedene Regeltypen ersetzt, um den Zeitpunkt und die Sichtbarkeit der Nachricht besser zu steuern:
      - Nachricht anzeigen, wenn: Bedingungen, die bestimmen, wann die Inhaltskarte angezeigt wird.
      - Nachricht schließen, wenn: Bedingungen, die die Inhaltskarte vorübergehend ausblenden. Sie kann erneut angezeigt werden, wenn die Anzeigebedingungen erneut erfüllt sind.
      - Nachricht disqualifizieren, wenn: Bedingungen, die dauerhaft verhindern, dass die Inhaltskarte erneut angezeigt wird.

[Mehr dazu](../content-card/design-content-card.md)

- **Entscheidungsfindung**
   - **Migrations-Tool-APIs** - Das Journey Optimizer-Team arbeitet derzeit an Migrations-Tool-APIs, um Entscheidungs-Management-Entitäten in das Decisioning zu migrieren. Diese Tools ermöglichen eine nahtlose Migration zwischen Sandboxes mit Funktionen zur Abhängigkeitsauflösung und zum Rollback. Wenden Sie sich bei Interesse an Ihren Adobe-Support-Mitarbeiter.

- **Personalisierung**
   - Eine neue Hilfsfunktion, „SHA256“, wurde zum Personalisierungseditor hinzugefügt. Diese Funktion wird verwendet, um den sha256-Hash einer Zeichenfolge zu berechnen und zurückzugeben.

[Mehr dazu](../personalization/functions/string.md#sha256)

## Versionshinweise für Juni 2025 {#25-6-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**Veröffentlichungsdatum**: 18. Juni 2025

<!--See also [Adobe Experience Platform Pre Release Notes](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

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

- **Kanalregelsätze**

   - **Benutzerdefiniertes Zeitfenster** für die Begrenzung – Im Konfigurationsbildschirm für Kanalregelsätze ist jetzt ein neues Feld **Alle** verfügbar, mit dem Sie Frequenzbegrenzungsregeln je nach angegebener Dauer für mehrere Tage, Wochen oder Monate anwenden können.

   - **Stündliches Zurücksetzen der Begrenzungsfrequenz** – Sie können jetzt eine Begrenzung auf stündlicher Basis für Kanalregelsätze anwenden. Diese Funktion ist nur für eine ausgewählte Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Wenden Sie sich an die Kundenunterstützung, um die Funktion aktivieren zu lassen.

   - **Tägliche Dauer** – Die zuvor nur eingeschränkt verfügbare Frequenzbegrenzung „Täglich“ ist in Kanalregelsätzen jetzt für alle Kundinnen und Kunden verfügbar.

  Weitere Informationen finden Sie in der [ausführlichen Dokumentation](../conflict-prioritization/channel-capping.md).

- **Code-basierte Erlebnisse**

   - Das Hinzufügen einer Entscheidungsrichtlinie ist jetzt in Code-basierten Erlebnis-Inhaltsvorlagen verfügbar. Dort kann sie zur Nutzung von Angeboten in bearbeitbaren Formularfeldern verwendet werden. [Weitere Informationen](../code-based/code-based-form-fields.md)

   - Auf dem Bearbeitungsbildschirm der Code-basierten Erlebnis-Journey oder -Kampagne können Sie jetzt direkt eine Entscheidungsrichtlinie hinzufügen, ohne den Personalisierungseditor zu öffnen. [Weitere Informationen](../code-based/create-code-based.md#edit-code)

- **Unterstützung für benutzerdefiniertes CSS im E-Mail-Designer**

  Mit Journey Optimizer können Sie Ihrem E-Mail-Inhalt jetzt benutzerdefiniertes CSS direkt im E-Mail-Designer hinzufügen. [Weitere Informationen](../email/custom-css.md)

- **Neue Registerkartennavigation für Kampagnen**

  Ein neues Navigationsmuster ermöglicht einen schnelleren Zugriff auf das Content-Authoring und unterstützt die weitere Erweiterung der Einstellungen in allen Kampagnen. [Weitere Informationen](../campaigns/create-campaign.md)

- **Entscheidungsfindung**

   - **Sandbox – Kopien und Entscheidungsfindung** (Verfügbarkeitsdatum: 3. Juni 2025) – Entscheidungsobjekte können jetzt zwischen Sandboxes kopiert werden, um Test- und Bereitstellungs-Workflows zu optimieren. [Weitere Informationen](../configuration/copy-objects-to-sandbox.md#decisioning)

   - **Unterstützung von Entscheidungselementattributen für Entscheidungsregeln** (Verfügbarkeitsdatum: 4. Juni 2025) – Sie können jetzt Entscheidungselementattribute für die Erstellung von Entscheidungsregeln verwenden. [Weitere Informationen](../experience-decisioning/rules.md#create)

- **Aktualisierung des API für die Ausführung interaktiver Nachrichten** – Verfügbarkeitsdatum: 6. Juni 2025

  Mit dem API für die Ausführung interaktiver Nachrichten können Sie jetzt den Zeitplan der bevorstehenden Kampagnenausführung löschen. [Weitere Informationen](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}
