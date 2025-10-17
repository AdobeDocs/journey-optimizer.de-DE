---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3eb73751fdb746dd2659e31c1b776fe2d767809f
workflow-type: tm+mt
source-wordcount: '2478'
ht-degree: 64%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] verwendet ein kontinuierliches Bereitstellungsmodell, das es Adobe ermöglicht, laufend neue Funktionen, Verbesserungen und Fehlerbehebungen bereitzustellen. Dieser Ansatz ermöglicht einen skalierbaren, schrittweisen Rollout von Funktionen, um die Leistung und Stabilität aller Umgebungen sicherzustellen.

Aufgrund dieses Modells werden die Versionshinweise zwischen den monatlichen Versionen aktualisiert.  In einem speziellen Abschnitt [Neueste Aktualisierungen](#updates-rn) werden neue Funktionen und Verbesserungen bei der Bereitstellung in der Produktion hervorgehoben, sodass Sie immer in Echtzeit über alle Änderungen informiert sind. <!--For full details about the release cycle and availability phases, see [Journey Optimizer release cycle](#releases.md).-->

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Hinweise zur Vorabversion vom Oktober 2025 {#oct-25-10-rn}

**Die unten stehenden Hinweise zu Vorabversionen können bis zum Veröffentlichungsdatum ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentationen werden in den Versionshinweisen am Veröffentlichungsdatum veröffentlicht.

Siehe auch [Vorab veröffentlichte Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

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
<p>Ruhestunden können über Regelsätze angewendet werden, die zur präzisen Steuerung Einzelaktionen in Kampagnen oder Journey zugewiesen werden können. Durch die Optimierung dieser Prozesse.</p>
<p>Diese Funktion ist nur für eine ausgewählte Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Überwachung und Reporting für benutzerdefinierte Aktionen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Diese Funktion bietet eine verbesserte Sichtbarkeit hinsichtlich des Zustands und der Ausführung von Journeys, einschließlich Lebenszyklusstatus- und Leistungswarnungen. Sie können jetzt schnell nachvollziehen, wann, wo und warum eine ungewöhnliche Situation in einer benutzerdefinierten Aktion auftritt.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

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

<table>
<thead>
<tr>
<th><strong>Neue API zum Abrufen von Aktionskampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine neue Journey Optimizer-API ist jetzt verfügbar, mit der Sie kampagnenbezogene Daten wie Details, Versionen und Konfigurationen programmgesteuert abrufen und überprüfen können.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Neue Quell-Connectoren für Treue-Apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Adobe Experience Platform sind jetzt neue Quell-Connectoren für die Treueprogramme von Talon.One, Capillary und Kobie verfügbar. Mit diesen Connectoren können Sie Treueprogramm-Daten nahtlos in Adobe Experience Platform streamen und diese Daten in Journey Optimizer nutzen.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Unterstützung von Entscheidungen im E-Mail-Kanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Entscheidungsrichtlinien zu E-Mail-Journeys und -Kampagnen hinzufügen. Entscheidungsrichtlinien sind Container für Angebote, die die Entscheidungs-Engine nutzen, um für jedes Zielgruppenmitglied die besten Inhalte bereitzustellen.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Hoher Durchsatzmodus für API-ausgelöste E-Mail-Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Für Kampagnen, die durch API ausgelöst werden, ist jetzt ein neuer Modus mit hohem Durchsatz verfügbar. Dieser Modus ist für groß angelegtes Echtzeit-Messaging konzipiert (bis zu 5.000 Transaktionen pro Sekunde) und bietet eine höhere Verfügbarkeit bei geringerer Latenz.</p>
<p>Diese Funktion ist nur für den E-Mail-Kanal verfügbar und steht Unternehmen zur Verfügung, die das Adobe Add-on für Transaktionsnachrichten mit hohem Durchsatz erworben haben. Weitere Informationen erhalten Sie beim Adobe-Support.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
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
<p>Mit Journey Optimizer können Sie jetzt Regeln über ein dediziertes Benutzeroberflächenmenü erstellen und beim Erstellen von Targeting nutzen, entweder im Rahmen der Inhaltsoptimierung in einer Kampagne oder auf einer Journey, entweder in der Aktivität Journey optimieren .</p>
<p>Zielgruppenbestimmungsregeln sind derzeit für Organisationen verfügbar, die das Add-on Decisioning erworben haben, und sie sind für andere Organisationen nach Bedarf verfügbar (eingeschränkte Verfügbarkeit).</p>
<p>Diese Funktion wird nach und nach für alle Kunden eingeführt. Wenden Sie sich in der Zwischenzeit an Ihren Adobe-Support-Mitarbeiter, um Zugang zu erhalten.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

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
<p>Diese Funktion wurde bereits in der Beta-Version veröffentlicht und ist jetzt für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Weitere Informationen finden Sie in der <a href="../email/apply-email-themes.md">ausführlichen Dokumentation</a>.</p>
<!--p>Availability date: October 22, 2025</p-->
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
<p>Verfügbarkeitsdatum: 14. Oktober 2025</p>
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
<p>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.</p>
<p>Weitere Informationen finden Sie in der <a href="../personalization/functions/helpers.md#execution-metadata">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 13. Oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentieragent ist hier!</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit <a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator.html" target="_blank">Adobe Experience Platform Agent Orchestrator </a> ist der Experimentationsagent in Journey Optimizer verfügbar. </p>
<p>Der Experimentierungs-Agent ist ein KI-gestütztes Tool, das die Ausführung und Verwaltung digitaler Experimente auf Websites, E-Mails, Push-Nachrichten und Anwendungen modernisiert. Sie hilft Ihnen, Experimente effizienter durchzuführen, Geschäftsziele zu organisieren und umsetzbare Einblicke zu generieren, indem sie hervorhebt, was funktioniert hat, was nicht und wo Sie als Nächstes experimentieren können.</p>
<p>Weitere Informationen finden Sie in der <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html?lang=de" target="_blank">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 10. Oktober 2025</p>
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




<!--
## Latest updates {#updates-rn}

New capabilities and improvements released in the past weeks are listed below, with their availability date. They will be grouped with the next release notes content at the end of the month. See also the latest [release notes below](#latest-rn).
-->

### Verbesserungen {#updates-improvements}

**Ausführungsfeld für WhatsApp-Kanal**

Zusätzlich zu E-Mail und SMS können Sie das Standardausführungsfeld für Ihre WhatsApp-Sendungen auf Sandbox-Ebene aktualisieren. Es ist auch möglich, das global eingestellte Ausführungsfeld zu überschreiben, indem es in den erweiterten Parametern der WhatsApp-Journey-Aktivität oder in der WhatsApp-Kanalkonfiguration geändert wird. <!-- [Read more](../FILE.md) -->

**Unterstützung benutzerdefinierter Attribute für Mailto-Adresse (abmelden)**

Wenn Sie mit Journey Optimizer das Einverständnis außerhalb von Adobe verwalten, können Sie externe benutzerdefinierte Endpunkte festlegen, indem Sie Ihren eigenen Ein-Klick-Abmelde-Link und eine benutzerdefinierte Abmelde-E-Mail-Adresse in der E-Mail-Konfiguration definieren. Wenn Ihre Empfängerinnen oder Empfänger auf den Link zum Abmelden klicken, fügt Journey Optimizer standardmäßige profilspezifische Parameter an das Einverständnisaktualisierungsereignis an.

Um Ihre benutzerdefinierten Endpunkte weiter zu personalisieren, können Sie jetzt benutzerdefinierte Attribute definieren, die auch an das Einverständnisereignis angehängt werden. [Weitere Informationen](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Diese Funktion ist bereits seit dem 25. August für die benutzerdefinierte URL **[!UICONTROL Ein-Klick-Abmelde]** verfügbar und jetzt für die Option **[!UICONTROL Mailto (unsubscribe)]** in begrenzter Verfügbarkeit veröffentlicht. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

Verfügbarkeitsdatum: 6. Oktober 2025

## Versionshinweise für September 2025 {#latest-rn}

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
-->
