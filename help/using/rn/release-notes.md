---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d93b7ce225294257f49caee6ac08cfb575611a93
workflow-type: tm+mt
source-wordcount: '1122'
ht-degree: 45%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] verwendet ein kontinuierliches Bereitstellungsmodell, das es Adobe ermöglicht, laufend neue Funktionen, Verbesserungen und Fehlerbehebungen bereitzustellen. Dieser Ansatz ermöglicht einen skalierbaren, schrittweisen Rollout von Funktionen, um die Leistung und Stabilität aller Umgebungen sicherzustellen.

Aufgrund dieses Modells werden die Versionshinweise zwischen den monatlichen Versionen aktualisiert.  In einem speziellen Abschnitt [Neueste Aktualisierungen](#updates-rn) werden neue Funktionen und Verbesserungen bei der Bereitstellung in der Produktion hervorgehoben, sodass Sie immer in Echtzeit über alle Änderungen informiert sind. <!--For full details about the release cycle and availability phases, see [Journey Optimizer release cycle](#releases.md).-->

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Versionshinweise Oktober &#39;25 {#oct-25-10-rn}

**Veröffentlichungsdatum**: Donnerstag, 22. Oktober 2025

### Neue Funktionen {#oct-25-10-features}

<table>
<thead>
<tr>
<th><strong>Ruhige Stunden/zeitbasierte Ausschlüsse</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit der Einstellung „Ruhige Stunden“ können Sie zeitbasierte Ausschlüsse für E-Mail-, SMS-, Push- und WhatsApp-Kanäle definieren. Sie stellen sicher, dass während bestimmter Zeiträume keine Nachrichten gesendet werden, und helfen Ihnen so, Kundenpräferenzen und Compliance-Anforderungen zu erfüllen.</p>
<p>Ruhestunden können über Regelsätze angewendet werden, die zur präzisen Steuerung Einzelaktionen in Kampagnen oder Journey zugewiesen werden können.</p>
<p>Regeln für ruhige Stunden sind derzeit nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um auf die Warteliste gesetzt zu werden, bitte den Adobe-Support kontaktieren.</p>
<img src="assets/do-not-localize/quiet-hour.gif">
<p>Weitere Informationen finden Sie in der <a href="../conflict-prioritization/quiet-hours.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 22. Oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With the new RCS Basic add-on offering, you can now deliver basic Rich Communication Services (RCS) messaging in Journey Optimizer, enabling the following enhanced messaging capabilities subject to provider and geographical support:</p>
<ul>
<li><strong>Branded and verified sender support:</strong> Send messages using verified business profiles with branding elements (logo, sender name, etc.).</li>
<li><strong>Message delivery insights:</strong> Receive detailed delivery reports including message status updates (e.g., sent, delivered, read).</li>
<li><strong>Link tracking:</strong> Embed and track URLs within RCS messages for engagement analytics.</li>
<li><strong>Fallback to SMS:</strong> Automatic fallback to SMS when the recipient's device does not support RCS or is temporarily unreachable via RCS.</li>
<li><strong>Basic message composition:</strong> Send basic text-based RCS messages.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The Direct mail activity facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the extraction file required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, Direct Mail channel is now available on the journey canvas, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p> Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>New API to retrieve Action Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new Journey Optimizer API is now available, enabling you to programmatically retrieve and inspect campaign-related data such as details, versions, and configurations.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary and Kobie loyalty Apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
<p>For more information, refer to the <a href="../start/get-started-sources.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table>-->

<!--table>
<thead>
<tr>
<th><strong>Decisioning support in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Nachrichten mit hohem Durchsatz für API-ausgelöste E-Mail-Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In API-ausgelösten Kampagnen ist ein neuer Transaktionsnachrichtenmodus mit hohem Durchsatz verfügbar. Dieser Modus wurde für umfangreiches Echtzeit-Transaktionsnachrichten entwickelt und unterstützt bis zu 5.000 Transaktionen pro Sekunde bei höherer Verfügbarkeit. Dieser Modus unterstützt auch Transaktionsnachrichten ohne Verweis auf oder Erstellung von Kundenprofilen, wie z. B. Gast-Checkout, Bestellbestätigung, Zurücksetzen des Kennworts, Sicherheitsbenachrichtigungen und andere Service-/Betriebsbenachrichtigungen.</p>
<p>Diese Funktion ist nur für den E-Mail-Kanal für Organisationen verfügbar, die das Add-on Adobe Transaktionsnachrichten mit hohem Durchsatz erworben haben. Weitere Informationen erhalten Sie beim Adobe-Support.</p>
<p>Weitere Informationen finden Sie in der <a href="../campaigns/api-triggered-high-throughput.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 22. Oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Wiederverwendbare Zielgruppenbestimmungsregeln</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Um Zeit und Aufwand zu sparen, können Sie mit Journey Optimizer jetzt wiederverwendbare Regeln über ein dediziertes Benutzeroberflächenmenü erstellen und beim Erstellen von Targeting nutzen, entweder im Rahmen der Inhaltsoptimierung in einer Kampagne oder einer Journey, entweder in der Aktivität Journey optimieren .</p>
<p>Zielgruppenbestimmungsregeln sind derzeit nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten. Beachten Sie, dass diese Funktion nur für Organisationen verfügbar ist, die das Add-on Decisioning erworben haben. Er wird nach und nach für alle Kunden eingeführt.</p>
<img src="assets/do-not-localize/targeting-rules.gif">
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/rules.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 22. Oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Neue Journey-Warnhinweise</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Für die Überwachung der Journey-Ausführung stehen neue vorkonfigurierte Warnhinweise zur Verfügung:</p>
<ul><li><a href="../reports/alerts.md#alert-discard-rate">Profilverwerfungsrate überschritten</a>: Verhältnis der Profilverwerfen zu den in den letzten 5 Minuten eingetretenen Profilen hat den Schwellenwert überschritten</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate">Fehlerrate für benutzerdefinierte Aktion überschritten</a>: Verhältnis der Fehler benutzerdefinierter Aktionen zu erfolgreichen HTTP-Aufrufen in den letzten 5 Minuten hat den Schwellenwert überschritten</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate">Profilfehlerrate überschritten</a>: Verhältnis der fehlerhaften Profile zu den eingegebenen Profilen in den letzten 5 Minuten hat den Schwellenwert überschritten.</li></ul> <p>Sie können Schwellenwerte anpassen und Warnhinweise entweder auf Journey-Ebene oder global abonnieren.</p>
<p>Weitere Informationen finden Sie in der <a href="../reports/alerts.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Mittwoch, 14. Oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Metadaten-Assistent für die Ausführung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine neue Hilfsfunktion „executionMetadata“ ist im Personalisierungseditor verfügbar. Damit können Sie kontextuelle Informationen an jede native Aktion anhängen und sie in einem Datensatz erfassen, um sie in externe Systeme zu exportieren.</p>
<p>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.</p>
<img src="assets/do-not-localize/execution-metadata.gif">
<p>Weitere Informationen finden Sie in der <a href="../personalization/functions/helpers.md#execution-metadata">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Dienstag, 13. Oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentation Accelerator mit Experimentieragenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Experimentation Accelerator enthält jetzt den Experimentationsagenten, ein KI-gestütztes, dialogorientiertes Tool, mit dem Sie mit Ihren Experimenten, Erkenntnissen und Chancen interagieren können. Dies verbessert das Journey Optimizer Experimentation Accelerator-Erlebnis, sodass Sie Experimente effizienter durchführen, herausfinden können, was funktioniert, und herausfinden können, wo als Nächstes optimiert werden kann.</p>
<p>Weitere Informationen finden Sie in der <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html?lang=de" target="_blank">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Samstag, 10. Oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>PDF-Anhänge an E-Mails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt eine statische PDF-Datei an eine mit Journey Optimizer gesendete E-Mail anhängen.</p>
<ul>
<li>Pro Profil können pro Jahr bis zu 6 Nachrichten mit einem PDF-Anhang gesendet werden.</li>
<li>Die maximale Dateigröße pro Anhang beträgt 5 MB.</li>
<li>Für zusätzliche Größen oder Volumen können Sie das Add-on für PDF-Anhänge erwerben. Weitere Informationen erhalten Sie beim Adobe-Support.</li>
</ul>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../email/pdf-attachments.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 30. September 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Öffentliche API zum Abrufen von Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine neue Journey Optimizer-API ist jetzt verfügbar, um Journeys und ihre zugehörigen Objekte wie Kampagnen und Oberflächen abzurufen.</p>
<p>Weitere Informationen finden Sie in der <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 25. September 2025</p>
</td>
</tr>
</tbody>
</table>

<!--
## Latest updates {#updates-rn}

New capabilities and improvements released in the past weeks are listed below, with their availability date. They will be grouped with the next release notes content at the end of the month. See also the latest [release notes below](#latest-rn).
-->

### Verbesserungen {#updates-improvements}

<!--Availability date: October 22, 2025-->

**Ausführungsfeld für WhatsApp-Kanal**

Zusätzlich zu E-Mail und SMS können Sie das Standardausführungsfeld für Ihre WhatsApp-Sendungen auf Sandbox-Ebene aktualisieren. Es ist auch möglich, das global eingestellte Ausführungsfeld zu überschreiben, indem es in den erweiterten Parametern der WhatsApp-Journey-Aktivität oder in der WhatsApp-Kanalkonfiguration geändert wird. [Weitere Informationen](../configuration/primary-email-addresses.md)

Verfügbarkeitsdatum: Donnerstag, 22. Oktober 2025

**Unterstützung benutzerdefinierter Attribute für Adresse für „E-Mail an (abmelden)“**

Wenn das Einverständnis außerhalb von Adobe verwaltet wird, können Sie in Journey Optimizer externe, benutzerdefinierte Endpunkte festlegen, indem Sie einen individuellen Link zum Abmelden mit einem Klick und eine benutzerdefinierte Abmelde-E-Mail-Adresse in der E-Mail-Konfiguration definieren. Wenn Ihre Empfängerinnen oder Empfänger auf den Link zum Abmelden klicken, fügt Journey Optimizer standardmäßige profilspezifische Parameter an das Einverständnisaktualisierungsereignis an.

Um Ihre benutzerdefinierten Endpunkte weiter zu personalisieren, können Sie jetzt benutzerdefinierte Attribute definieren, die an das Einverständnisereignis angehängt werden. [Weitere Informationen](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Diese Funktion ist bereits seit August 2025 für die benutzerdefinierte **[!UICONTROL URL zum Abmelden mit einem Klick]** verfügbar und wird jetzt für die Option **[!UICONTROL E-Mail an (abmelden)]** in eingeschränkter Verfügbarkeit veröffentlicht. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

Verfügbarkeitsdatum: 6. Oktober 2025

### Demnächst {#oct-25-10-soon}

In den nächsten Tagen sind die folgenden Funktionen und Verbesserungen zur Veröffentlichung vorgesehen. **Informationen können Änderungen unterliegen**. Aktualisierte Links, Bildschirme und Dokumentationen werden freigegeben, sobald diese Aktualisierungen live in der Produktion verfügbar sind.

#### Neue Funktionen {#oct-25-10-soon-features}

<table>
<thead>
<tr>
<th><strong>Designs im E-Mail-Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt schnell vorab genehmigte Designs anwenden, um Markenkonsistenz über alle E-Mails hinweg sicherzustellen, den Prozess der Kampagnenerstellung zu beschleunigen und eigenständig hochwertige E-Mails zu erstellen, während Sie die Abhängigkeit von Designteams reduzieren.</p>
<p>Diese Funktion wurde bereits in der Beta-Version veröffentlicht und ist jetzt für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<!--img src="assets/do-not-localize/themes.gif">
<p>For more information, refer to the <a href="../email/apply-email-themes.md">detailed documentation</a>.</p>
<p>Availability date: November 4, 2025</p-->
</td>
</tr>
</tbody>
</table>

#### Verbesserungen {#oct-25-10-soon-improvements}

**Entscheidungen in E-Mails über KI-Modelle**

Sie können jetzt KI-Modelle verwenden, um den besten Inhalt in Ihrer E-Mail durch die Verwendung von Decisioning zu optimieren. Beispielsweise können Sie mit dieser Funktion die besten Inhalte basierend auf benutzerdefinierten Ereignissen wie Käufen, Schaltflächen-Klicks, Hinzufügen zum Warenkorb usw. anbieten.

<!--
<table>
<thead>
<tr>
<th><strong>New Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports Web Push notifications, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app.</p>
<p>This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Custom action monitoring and reporting is now available. This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
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
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary, and Kobie loyalty apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Landing page custom forms</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With [!DNL Journey Optimizer], you can now capture profile attributes though your landing pages.</p>
<p>Create, design and manage custom forms tailored to your needs based on a specific dataset. You can then leverage these forms in landing pages to add the profile attributes of your choice into the dataset defined for each form.</p>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../landing-pages/lp-forms.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>
-->
