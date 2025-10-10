---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 5a530a183c3eba87dcee59d42162fad9c0c32942
workflow-type: tm+mt
source-wordcount: '1628'
ht-degree: 81%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert. [!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Updates Oktober &#39;25 {#25-10-rn}

### Neue Funktionen {#25-10-features}

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
<p>Verfügbarkeitsdatum: 30. September 2025</p>
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
<p>Eine neue Journey Optimizer-API ist jetzt verfügbar, um Journey und ihre zugehörigen Objekte wie Kampagnen und Oberflächen abzurufen.</p>
<p>Weitere Informationen finden Sie in der <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 25. September 2025</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#25-10-improvements}

**Unterstützung benutzerdefinierter Attribute für Mailto-Adresse (abmelden)**

Wenn Sie mit Journey Optimizer das Einverständnis außerhalb von Adobe verwalten, können Sie externe benutzerdefinierte Endpunkte festlegen, indem Sie Ihren eigenen Ein-Klick-Abmelde-Link und eine benutzerdefinierte Abmelde-E-Mail-Adresse in der E-Mail-Konfiguration definieren. Wenn Ihre Empfängerinnen oder Empfänger auf den Link zum Abmelden klicken, fügt Journey Optimizer standardmäßige profilspezifische Parameter an das Einverständnisaktualisierungsereignis an.

Um Ihre benutzerdefinierten Endpunkte weiter zu personalisieren, können Sie jetzt benutzerdefinierte Attribute definieren, die auch an das Einverständnisereignis angehängt werden. [Weitere Informationen](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Diese Funktion ist bereits seit dem 25. August für die benutzerdefinierte URL **[!UICONTROL Ein-Klick-Abmelde]** verfügbar und jetzt für die Option **[!UICONTROL Mailto (unsubscribe)]** in begrenzter Verfügbarkeit veröffentlicht. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

Verfügbarkeitsdatum: 6. Oktober 2025

## Versionshinweise für September 2025 {#25-9-rn}

**Veröffentlichungsdatum**: 23.–24. September 2025

### Neue Funktionen {#sept-25-9-features}

<table>
<thead>
<tr>
<th><strong>Journey Optimizer Experimentation Accelerator</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Experimentation Accelerator ist ein KI-gestütztes Produkt, das darauf ausgelegt ist, Ihre Experimente auf ein neues Niveau zu heben. Konzipiert für Benutzende von Adobe Journey Optimizer und Adobe Target, vereinheitlicht es die Verwaltung von Experimenten, bietet KI-gestützte Erkenntnisse und Chancen und stellt einen neuen Agent für Experimente vor.</p>
<p>Folgendes erwartet Sie:</p>
<ul>
<li><strong>Einheitliches Experimentinventar:</strong> Alle Experimente aus Adobe Journey Optimizer und Adobe Target lassen sich in einem zentralen Arbeitsbereich schnell anzeigen, filtern und verwalten.</li>
<li><strong>KI-gestützte Erkenntnisse und Möglichkeiten für Experimente:</strong> Gehen Sie mit Erkenntnissen und Empfehlungen auf Basis generativer KI über statistische Auswertungen hinaus. Jedes Experiment zeigt jetzt verwertbare Chancen auf, einschließlich einer nachvollziehbaren Begründung, sodass Teams fundierter entscheiden können, was als Nächstes getestet werden sollte.</li>
<li><strong>Unterstützung für Multi-Armed Bandit (MAB, mehrarmiger Bandit) in Journey Optimizer:</strong> Maximieren Sie die Wirkung und reduzieren Sie unnötigen Traffic mit Multi-Armed-Bandit-Experimenten. Anstatt Zielgruppen gleichmäßig aufzuteilen, weist MAB in Echtzeit automatisch den leistungsstärksten Varianten mehr Besuchende zu. Auf diese Weise können Sie mehr Kundinnen und Kunden bessere Erlebnisse bieten und gleichzeitig Erkenntnisse darüber gewinnen, was funktioniert.</li></ul>
<p><img src="assets/do-not-localize/experimentation-accelerator.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../content-management/experiment-accelerator.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 3. Oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent ist jetzt verfügbar.</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent ist in Journey Optimizer verfügbar und wird von <a href="https://experienceleague.adobe.com/de/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator" target="_blank">Adobe Experience Platform Agent Orchestrator</a> unterstützt. Er ermöglicht die Analyse von Journeys über eine Schnittstelle für natürliche Sprache. Der Agent erkennt Zielgruppen- oder Zeitplankonflikte und Profilabbrüche in einer Journey und hilft Ihnen, Maßnahmen zur Behebung zu ergreifen. Demnächst können Sie Journeys mit Agent-basierter Unterstützung erstellen.</p>
<p>Weitere Informationen finden Sie in der <a href="https://experienceleague.adobe.com/de/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze" target="_blank">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 24. September 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Dunkler Modus im E-Mail-Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der E-Mail-Designer von Journey Optimizer bietet jetzt die Möglichkeit, in die Ansicht „Dunkler Modus“ zu wechseln, in der Sie zusätzlich bestimmte benutzerdefinierte Einstellungen definieren können, die nur Empfängerinnen und Empfängern angezeigt werden, die ihre E-Mails im dunklen Modus lesen.</p>
<p>Beachten Sie dabei Folgendes:</p>
<ul>
<li>Das endgültige Rendern des dunklen Modus weicht möglicherweise ab und hängt vom E-Mail-Client der Empfängerinnen und Empfänger ab.</li>
<li>Nicht alle E-Mail-Clients unterstützen einen benutzerdefinierten dunklen Modus. Darüber hinaus wenden einige E-Mail-Clients ausschließlich ihren eigenen standardmäßigen dunklen Modus auf alle empfangenen E-Mails an. In beiden Fällen können die im E-Mail-Designer definierten benutzerdefinierten Einstellungen nicht gerendert werden.</li>
</ul>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../email/dark-mode.md">ausführlichen Dokumentation</a>.</p>
 <p>Verfügbarkeitsdatum: 16. September 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Pfadoptimierung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verwenden Sie den neuen Optimierungsknoten, um bestimmte Zielgruppen anzusprechen, oder führen Sie A/B-Tests durch, um den besten Pfad zum Erreichen Ihrer geschäftsbezogenen KPIs zu ermitteln.</p>
<p>Mit diesem Tool können Sie Kommunikation, Sequenzierung und Timing testen und variieren sowie anpassen, um Ihre Kundschaft optimal zu erreichen.</p>
<p>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/optimize.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 4. September 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Benutzerdefinierte Methode zur Delegierung von Subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Neben der vollständigen Delegierung und CNAME-Methode ist nun eine neue Methode zur Subdomain-Konfiguration verfügbar: die benutzerdefinierte Delegierung, mit der Sie alle Aspekte von DNS, die für den Versand, das Rendern und das Tracking von Nachrichten erforderlich sind, vollständig kontrollieren und verwalten können.</p>
<p>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.</p>
<p><img src="assets/do-not-localize/custom-delegation.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/delegate-custom-subdomain.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 4. September 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verwenden von Adobe Experience Platform-Daten für Personalisierung und Entscheidungsfindung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Diese Funktion wurde zuvor als öffentliche Beta-Version veröffentlicht, steht aber nun für alle Umgebungen zur Verfügung. Mit dieser Version wurden die folgenden Verbesserungen eingeführt:</p>
<ul><li>Unterstützung für die Personalisierung bei der Datensatzsuche in eingehenden Kanälen.</li>
<li>Die Hilfsfunktion „datasetLookup“ kann jetzt in Ausdrucksfragmenten verwendet werden. Derzeit ist diese Funktion nur für eine begrenzte Anzahl von Kundinnen und Kunden verfügbar. Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</li>
<li>Mit einer Option in der Oberfläche für Datensatz-Management können Sie jetzt auf Einträgen basierende Datensätze für die Lookup-Personalisierung aktivieren, ohne dass ein API-Aufruf durchgeführt werden muss.</li>
<li>Verbesserte Überwachung, um den Datenaufnahmestatus zu verfolgen und zu verstehen, wann Datensätze für die Suche bereit sind.</li>
<li>Aktualisierte Nutzungsrichtlinien und Schutzmechanismen, um optimale Leistung und Zuverlässigkeit sicherzustellen.</li>
<li>Adobe Experience Platform-Datensätze können jetzt in Begrenzungsregeln für die Entscheidungsfindung genutzt werden.</li></ul></p>
<p>Weitere Informationen finden Sie in der <a href="../data/lookup-aep-data.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 1. September 2025</p>
</td>
</tr>
</tbody>
</table>


### Verbesserungen {#sept-25-9-improvements}

* **Webhook-Unterstützung für Kampagnen, die durch API ausgelöst werden**\
  Kampagnen, die durch API ausgelöst werden, unterstützen jetzt Webhooks. Konfigurieren Sie eine Webhook-URL, um Statusaktualisierungen für jede Nachricht in Echtzeit zu erhalten, was die Beobachtbarkeit verbessert und eine nahtlose Überwachung und Automatisierung ermöglicht. [Weitere Informationen](../configuration/feedback-webhooks.md)

  Verfügbarkeitsdatum: 29. September 2025

* **mTLS-Unterstützung für SMS-Kanal**
Beim Einrichten eines benutzerdefinierten SMS-Anbieters haben Sie jetzt die Möglichkeit, die gegenseitige TLS-Authentifizierung (mTLS) zu aktivieren. Dazu müssen sowohl der Client als auch der Server die Identität des jeweils anderen bestätigen, bevor eine sichere Verbindung hergestellt wird. [Mehr zum Thema](../sms/sms-configuration-custom.md) – Verfügbarkeitsdatum: 23. September 2025

* **Modellbasierte Schemata**\
  Modellbasierte Schemata können jetzt verwendet werden, um Ihre Anforderungen an relationale Modellierung in orchestrierten Kampagnen zu unterstützen. [Mehr zum Thema](../orchestrated/gs-schemas.md) – Verfügbarkeitsdatum: 23. September 2025

* **Unterstützung der Datensatzsuche in Journeys**\
  Eine neue Aktivität in Journeys, **Datensatzsuche**, ermöglicht das dynamische Abrufen von Daten aus Adobe Experience Platform-Eintragsdatensätzen während der Laufzeit. Mit dieser Funktion können Sie auf Daten zugreifen, die sich möglicherweise nicht in der Profil- oder Ereignis-Payload befinden. So können Sie sicherstellen, dass Ihre Kundeninteraktionen sowohl relevant als auch zeitlich passend sind. [Mehr zum Thema](../building-journeys/dataset-lookup.md) – Verfügbarkeitsdatum: 23. September 2025

  Diese Aktivität ist nur für eine ausgewählte Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.

* **Unterstützung von Umleitungen in benutzerdefinierten Journey-Aktionen**\
  Umleitungen (302) werden jetzt in benutzerdefinierten Journey-Aktionen unterstützt. – Verfügbarkeitsdatum: 23. September 2025

* **Warnhinweise zum Kanalkonfigurations-Monitoring**: Sie können nun Systemwarnhinweise abonnieren – entweder per E-Mail oder im Journey Optimizer-Benachrichtigungszentrum –, falls bei der E-Mail-Kanalkonfiguration mit dem benutzerdefinierten Subdomain-Delegierungstyp ein Fehler auftritt. [Mehr zum Thema](../reports/alerts.md#alert-channel-config-failure) – Verfügbarkeitsdatum: 23. September 2025

* **Anfragen zur Abmeldung mit einem Klick** – Wir haben Verbesserungen eingeführt, die die Handhabung von Anfragen zur Abmeldung mit einem Klick, die unter „Von Adobe verwaltet“ konfiguriert wurden, weiter optimieren und eine zuverlässige und konsistente Verarbeitung sicherstellen. – Verfügbarkeitsdatum: 23. September 2025

* **Verschachtelte JSON-Parameter im Nachrichtentext werden jetzt in der benutzerdefinierten Authentifizierung unterstützt**\
  Beachten Sie beim Konfigurieren der benutzerdefinierten Authentifizierung für eine benutzerdefinierte Aktion, dass verschachtelte JSON-Objekte (z. B. Unterobjekte innerhalb von `bodyParams`) jetzt unterstützt werden. [Mehr zum Thema](../datasource/external-data-sources.md#custom-authentication-mode) – Verfügbarkeitsdatum: 18. September 2025

* **Stündliches Zurücksetzen der Begrenzungsfrequenz** – Sie können jetzt eine Begrenzung auf stündlicher Basis für Kanalregelsätze anwenden. Diese Funktion, die zuvor mit eingeschränkter Verfügbarkeit angeboten wurde, steht jetzt für alle Umgebungen zur Verfügung und ermöglicht die Auswahl von 1 Stunde (zuvor 3 Stunden). [Mehr zum Thema](../conflict-prioritization/channel-capping.md) – Verfügbarkeitsdatum: 17. September 2025

* **Simulieren von Inhaltsvarianten für alle eingehenden Kanäle**\
  Die Simulation von Inhaltsvarianten, die zuvor nur für die Kanäle E-Mail, SMS und Push-Benachrichtigung verfügbar war, gilt jetzt auch für alle eingehenden Kanäle. [Mehr zum Thema](../test-approve/simulate-sample-input.md) – Verfügbarkeitsdatum: 17. September 2025

* **Ausdruck für Begrenzungsregeln bei der Entscheidungsfindung** – Sie können jetzt eigene Ausdrücke erstellen, um den Schwellenwert einer Begrenzungsregel für ein Entscheidungselement zu definieren. [Mehr zum Thema](../experience-decisioning/items.md#capping) – Verfügbarkeitsdatum: 16. September 2025

* **Unterstützung dynamischer Domains** – Journey Optimizer unterstützt jetzt die vollständige/Basis-URL-Personalisierung für vordefinierte Domains, die von Adobe akzeptiert werden. [Mehr zum Thema](../personalization/personalization-build-expressions.md#where) – Verfügbarkeitsdatum: 12. September 2025

  Diese Funktion ist für eine ausgewählte Kundengruppe eingeschränkt verfügbar.

* **Webhooks** - Diese Version führt die folgenden Verbesserungen für Webhooks beim Konfigurieren eines benutzerdefinierten SMS-Anbieters ein:

   * Sie können jetzt den Zweck Ihres Webhooks definieren, entweder Eingehend oder Feedback, je nach dem Typ der Daten, die Sie erfassen möchten. [Mehr zum Thema](../sms/sms-configuration-custom.md#webhook) – Verfügbarkeitsdatum: 23. September 2025

   * Die Benutzeroberfläche zur Konfiguration von Keywords wurde verbessert, um die Einrichtung zu vereinfachen. [Mehr zum Thema](../sms/sms-configuration-custom.md#webhook) – Verfügbarkeitsdatum: 23. September 2025

* **SMS**

   * Beim Einrichten eines benutzerdefinierten SMS-Anbieters können Sie jetzt ein **Standard**-Keyword definieren, das verwendet wird, wenn eine eingehende SMS ein nicht erkanntes Keyword enthält. Sie können auch **benutzerdefinierte** Schlüsselwörter für bestimmte Aktionen erstellen. [Mehr zum Thema](../sms/sms-configuration-custom.md) – Verfügbarkeitsdatum: 23. September 2025

   * Sie können jetzt auf undefinierte eingehende Keyword-Antworten zugreifen, die über eine SMS-Nachricht gesendet werden, einschließlich Tippfehler, Wörter oder Sätze, die in der Konfiguration nicht explizit definiert sind. Sie werden im Datensatz **AJO Email Tracking Experience Event** unter **InboundMessage** für 13 Monate gespeichert. Nur bei Sinch, Infobip und benutzerdefinierten SMS-Anbietern verfügbar. - Verfügbarkeitsdatum: 23. September 2025

<!--
* **Approval policy permissions**
  Added an option when creating or setting Approval Policy to prevent Journey/Campaign creators from approving their own objects. [Read more](../test-approve/approval-policies.md) - Availability date: Sept 23, 2025-->

<!--
### Coming soon {#sept-25-9-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

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


* **New Journey Alerts**  
  New pre-configured alerts are available for journeys:

  * Profile Discard Rate Exceeded: Ratio of profile discards to entered profiles over the last 5 mins exceeded threshold.  
  * Custom Action Error Rate Exceeded: Ratio of custom action errors to successful HTTP calls over the last 5 mins exceeded threshold.  
  * Profile Error Rate Exceeded: Ratio of profiles-in-error to entered profiles over the last 5 mins exceeded threshold.


  * [Profile Discard Rate Exceeded](../reports/alerts.md#profile-discard-rate-exceeded): Ratio of profile discards to entered profiles over the last 5 mins exceeded threshold.  
  * [Custom Action Error Rate Exceeded](../reports/alerts.md#custom-action-error-rate-exceeded): Ratio of custom action errors to successful HTTP calls over the last 5 mins exceeded threshold.  
  * [Profile Error Rate Exceeded](../reports/alerts.md#profile-error-rate-exceeded): Ratio of profiles-in-error to entered profiles over the last 5 mins exceeded threshold.

  You can modify threshold values and subscribe to individual journey-level alerts vs globally.

  Availability date: Sept XX, 2025

-->
