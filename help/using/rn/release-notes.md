---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 9281adb50d13142ccf323ff5edb3f480b801d986
workflow-type: tm+mt
source-wordcount: '1806'
ht-degree: 87%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] verwendet ein kontinuierliches Bereitstellungsmodell, das es Adobe ermöglicht, laufend neue Funktionen, Verbesserungen und Fehlerbehebungen bereitzustellen. Dieser Ansatz ermöglicht ein skalierbares Rollout von Funktionen in Phasen, um die Leistung und Stabilität aller Umgebungen sicherzustellen.

Aufgrund dieses Modells werden die Versionshinweise zwischen den monatlichen Versionen aktualisiert.  Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Updates Februar &#39;26 {#feb-26-updates}

### Neue Funktionen {#feb-26-01-updates-features}

<table>
<thead>
<tr>
<th><strong>Aktivität „Inhaltsentscheidung“ </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine neue <strong>Aktivität „Inhaltsentscheidung“</strong> ist jetzt in der Journey-Arbeitsfläche verfügbar, mit der Sie <strong>personalisierte Angebote</strong> direkt in Ihre Customer Journeys integrieren können. Mit dieser Aktivität können Sie entscheidungsbasierte Inhalte bereitstellen und diese Angebote in Ihrer gesamten Journey referenzieren, zum Beispiel in Bedingungen für die Erstellung von Verzweigungen je nach Eignung, in benutzerdefinierten Aktionen für die Weitergabe von Angebotsdaten an externe Systeme und in anderen Aktivitäten für die Erstellung vollständig personalisierter Kundenerlebnisse.</p>
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
<p><strong>Migrations-Tool</strong>-APIs sind jetzt verfügbar, um Entitäten aus dem Entscheidungs-Management programmgesteuert in die Entscheidungsfindung zu migrieren. Sie bieten folgende Funktionen:</p>
<ul>
<li>Flexible Migrationsbereiche (Sandbox-, Angebots- oder Entscheidungsebene)</li>
<li>Automatische Analyse und Validierung von Abhängigkeiten</li>
<li>Rollback-Unterstützung für abgeschlossene Migrationen</li>
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
<p>Gewinnen Sie detailliertere Erkenntnisse zum Status und zur Leistung Ihrer <strong>benutzerdefinierten Aktionsendpunkte</strong> mit einem neuen Monitoring-Dashboard und angereicherten Ereignisdaten zu Journey-Schritten. Verfolgen Sie erfolgreiche Aufrufe, Fehler, Durchsatz, Antwortzeiten und Warteschlangenwartezeiten nach, um schnell zu erkennen, wann, wo und warum Anomalien auftreten.</p>
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
<p>Sie können jetzt den Inhalt Ihrer (SMS<strong>Nachrichten) mit </strong>Decisioning<strong> personalisieren und </strong>. Verwenden Sie Prioritätswerte, Formeln oder KI-Modelle, um Ihren Kundinnen und Kunden den besten Inhalt anzuzeigen.</p>
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/create-decision.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 2. Februar 2026</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#feb-26-01-updates-improv}

<!--
* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach <strong>fragments</strong> to <strong>decision items</strong> which can be leveraged in code-based experience campaigns through decision policies.

  Availability date: February 11, 2026.-->

* **SMS-Webhooks** - Webhooks werden jetzt von allen SMS-Anbietern unterstützt. Sie können jeden Webhook für einen bestimmten Zweck, eingehende Webhooks zum Erfassen eingehender Nachrichten und Feedback-Webhooks konfigurieren, um Versandbestätigungen, Statusaktualisierungen und andere nachrichtenbezogene Ereignisse zu erhalten. [Weitere Informationen](../sms/sms-webhook.md)

  Verfügbarkeit: 2. Februar 2026.

## Januar 2026 – Versionshinweise {#latest-rn}

<!--**Release date**: January 27-28, 2026-->

Die Abschnitte [Funktionen](#jan-26-01-features) und [Verbesserungen](#jan-26-01-improv) decken bereits verfügbare Funktionen ab, während [Demnächst verfügbar](#jan-26-01-coming-soon) Elemente auflistet, die für ein späteres Verfügbarkeitsdatum geplant sind.

<!-- **The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date. 

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### Neue Funktionen {#jan-26-01-features}


<table>
<thead>
<tr>
<th><strong>Unterstützung von Entscheidungen im Push-Kanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt den Inhalt Ihrer <strong>Push-Benachrichtigungen“ mit </strong>Decisioning<strong> personalisieren und </strong>. Verwenden Sie Prioritätswerte, Formeln oder KI-Modelle, um Ihren Kundinnen und Kunden den besten Inhalt anzuzeigen.</p>
<p>Für Experience Decisioning mit Push-Benachrichtigungen ist eine bestimmte Version der Mobile SDK erforderlich. Bevor Sie diese Funktion implementieren, überprüfen Sie die <a href="https://developer.adobe.com/client-sdks/home/release-notes/" target="_blank">Versionshinweise</a>, um die erforderliche Version zu identifizieren und sicherzustellen, dass Sie das Upgrade entsprechend durchgeführt haben. Sie können auch alle verfügbaren SDK-Versionen für Ihre Plattform in <a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions/" target="_blank">diesem Abschnitt</a> anzeigen.</p>
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/create-decision.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 30. Januar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direkt-Mail-Kanal in Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der Kanal <strong>Direkt-Mail</strong> war bisher auf Kampagnen beschränkt und ist jetzt auf der Journey-Arbeitsfläche verfügbar, sodass Sie Direkt-Mail in Ihre Journeys integrieren können. Direkt-Mail kann jetzt sowohl in <strong>Batch- als auch in 1:1-Journey-Szenarien verwendet werden</strong>, mit Unterstützung für die Dateiextraktionskonfiguration und zeitbasierte Häufigkeitseinstellungen.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><img src="assets/do-not-localize/dm-journey.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../direct-mail/get-started-direct-mail.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Freitag, 29. Januar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ruhezeiten (zeitbasierte Ausschlüsse)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mithilfe von <strong>Ruhezeiten</strong> können Sie zeitbasierte Ausschlüsse für den E-Mail-, SMS-, Push- und WhatsApp-Kanal definieren. Sie stellen sicher, dass während bestimmter Zeiträume keine Nachrichten gesendet werden, und helfen Ihnen so, Kundenpräferenzen und Compliance-Anforderungen zu erfüllen. Ruhezeiten können über <strong>Regelsätze</strong> angewendet werden, die zur präzisen Steuerung Einzelaktionen in Kampagnen oder Journeys zugewiesen werden können.</p>
<p>Diese Funktion wurde zuvor mit eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung. Mit dieser allgemeinen Verfügbarkeit bietet die Funktion jetzt die Möglichkeit, dass Kundinnen und Kunden eine Kampagnenaktion bis zum Abschluss der Ruhezeiten in die Warteschlange stellen und die aktivierte Regel für Ruhezeiten in der Vorschau anzeigen können.</p>
<p><img src="assets/do-not-localize/quiet-hour-ga.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../conflict-prioritization/quiet-hours.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Freitag, 29. Januar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nachrichtenexport</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine neue Funktion zum <strong>Nachrichtenexport</strong> ist jetzt für den E-Mail- und SMS-Kanal verfügbar. Mit dieser Funktion können Sie Inhalte gesendeter Nachrichten automatisch in einen dedizierten Experience Platform-Datensatz exportieren, um Folgendes zu ermöglichen:</p>
<ul>
<li>Einhaltung behördlicher Auflagen (z. B. HIPAA)</li>
<li>Archivieren von Nachrichten für Rechtsansprüche und Anfragen an die Kundenunterstützung</li>
<li>Aufbewahren von Kopien der an Kontakte gesendeten personalisierten Inhalte</li>
</ul>
<p>Einträge werden nach der Aufnahme 7 Kalendertage lang im AJO-Nachrichtenexport-Datensatz aufbewahrt. Während dieses Aufbewahrungszeitraums können Sie sie über Experience Platform-Ziele in Ihren eigenen Speicher exportieren. Die Funktion wird auf der Ebene der Kanalkonfiguration aktiviert, sodass Sie <strong>granulare Kontrolle</strong> über die exportierten Nachrichten erhalten.</p>
<p>Diese Funktion ist nur für den E-Mail- und SMS-Kanal verfügbar und steht Unternehmen zur Verfügung, die das Add-on für den Nachrichtenexport erworben haben. Weitere Informationen erhalten Sie beim Adobe-Support.</p>
<p><img src="assets/do-not-localize/message-export.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/message-export.md#message-export">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 28. Januar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direkt-Mail-Kanal in orchestrierten Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der Direkt-Mail-Kanal ist jetzt in orchestrierten Kampagnen verfügbar.  Die <strong>Direkt-Mail-Aktivität</strong> erleichtert den Direkt-Mail-Versand innerhalb der orchestrierten Kampagne und ermöglicht sowohl einmalige als auch wiederkehrende Nachrichten. Sie dient dazu, das Generieren der von Direkt-Mail-Dienstleistern benötigten <strong>Extraktionsdatei</strong> zu automatisieren. Kanalaktivitäten können in der Arbeitsfläche für orchestrierte Kampagnen kombiniert werden, um kanalübergreifende Kampagnen zu erstellen, mit denen basierend auf Kundenverhalten und Daten Aktionen ausgelöst werden können.</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../orchestrated/activities/channels.md#channel">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 28. Januar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent – Erstellen einer Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent bietet jetzt Funktionen zur Inhaltserstellung, mit denen Benutzende von Journey Optimizer über eine <strong>Schnittstelle für natürliche Sprache</strong> Marketing-Journeys erstellen und konfigurieren können. Mit diesen neuen Fähigkeiten können Fachleute schnell Journeys erstellen, indem sie ihre Anforderungen einfach in <strong>Dialog-Prompts</strong> beschreiben. Diese Neuerung optimiert den Prozess der Journey-Erstellung und ermöglicht es Marketing-Fachleuten, sich auf die Strategie statt auf die technische Konfiguration zu konzentrieren.</p>
<p>Weitere Informationen finden Sie in der <a href="../start/ai-features.md#journey-agent">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 12. Januar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API zum Abrufen von Aktionskampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine neue Journey Optimizer-API ist jetzt verfügbar, mit der Sie <strong>kampagnenbezogene Daten</strong> wie Details, Versionen und Konfigurationen programmgesteuert abrufen und überprüfen können.</p>
<p>Weitere Informationen finden Sie in der <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 24. November 2025</p>
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
<p>Sie können jetzt schnell <strong>vorab genehmigte Designs</strong> anwenden, um <strong>Markenkonsistenz</strong> über alle E-Mails hinweg sicherzustellen, den Prozess der Kampagnenerstellung zu beschleunigen und eigenständig hochwertige E-Mails zu erstellen, während Sie die Abhängigkeit von Designteams reduzieren.</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>Diese Funktion wurde bereits in der Beta-Version veröffentlicht und ist jetzt für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p>Weitere Informationen finden Sie in der <a href="../email/apply-email-themes.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 5. November 2025</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#jan-26-01-improv}

#### KI

* **Inhaltsqualitätsprüfungen mit dem KI-Assistenten** – Zusätzlich zur Markenausrichtung können Sie jetzt die gesamte <strong>Inhaltsqualität</strong> bewerten, um potenzielle Probleme mit <strong>Lesbarkeit</strong>, Kohärenz und Effektivität unabhängig von Ihren Markenrichtlinien aufzudecken. Diese automatisierten Prüfungen helfen bei der Erkennung von unklaren Botschaften, inkonsistentem Ton oder strukturellen Lücken. [Weitere Informationen](../content-management/brands-score.md#validate-quality).

   [Funktion im Video kennenlernen](https://video.tv.adobe.com/v/3470555/?captions=ger&learn=on).

#### Journeys

* **Kombinieren von Aktionen für native und Adobe Campaign-Nachrichten** – Mit Journey Optimizer können Sie jetzt Aktionen von <strong>Adobe Campaign v7/v8</strong>-Nachrichten mit <strong>nativen Kanalaktionen</strong> in derselben Journey kombinieren. [Weitere Informationen](../building-journeys/using-adobe-campaign-v7-v8.md)

  Verfügbarkeitsdatum: Mittwoch, 27. Januar 2026

* **Fehlerantwort-Payload für benutzerdefinierte Aktionen** – Sie können jetzt eine optionale <strong>Fehlerantwort-Payload</strong> für benutzerdefinierte Aktionen definieren. Wenn ein Aufruf fehlschlägt, wird die Fehler-Payload im Journey-Kontext (unter dem errorResponse-Knoten der Aktion) verfügbar gemacht und ist in der Verzweigung <strong>Timeout/Fehler</strong> verfügbar, um eine umfassendere Fallback-Logik und `jo_status_code` Debugging zu unterstützen. [Weitere Informationen](../action/about-custom-action-configuration.md#define-the-message-parameters)

  Verfügbarkeitsdatum: Mittwoch, 27. Januar 2026

* **Validierung der Journey-Payload-Größe in Journeys** – Journey Optimizer validiert jetzt <strong>Payload-Größen</strong>, um eine optimale Leistung und Systemstabilität sicherzustellen. Beim Erstellen oder Veröffentlichen von Journeys erhalten Sie deutliche <strong>Warnungen und Fehler</strong>, wenn die Payload-Größe die empfohlenen Grenzwerte erreicht oder überschreitet, sowie praktische Anleitungen zur Optimierung Ihrer Journey-Konfiguration. Diese proaktive Validierung hilft Ihnen, potenzielle Probleme frühzeitig zu erkennen und die Journey-Leistung aufrechtzuerhalten. [Weitere Informationen](../start/guardrails.md#journey-payload-size)

  Verfügbarkeitsdatum: Mittwoch, 27. Januar 2026


* **Journey-Warnhinweise** – Neue <strong>vorkonfigurierte Warnhinweise</strong> sind für Journeys verfügbar.
   * <strong>Verwerfungsrate für Profile überschritten</strong> – Das Verhältnis von verworfenen Profilen zu eingetretenen Profilen in den letzten 5 Minuten hat den Schwellenwert überschritten
   * <strong>Fehlerrate bei benutzerdefinierter Aktion überschritten</strong> – Das Verhältnis von Fehlern bei benutzerdefinierten Aktionen zu erfolgreichen HTTP-Aufrufen in den letzten 5 Minuten hat den Schwellenwert überschritten
   * <strong>Fehlerrate für Profile überschritten</strong> – Das Verhältnis von fehlerhaften Profilen zu eingetretenen Profilen in den letzten 5 Minuten hat den Schwellenwert überschritten

  Weitere Informationen finden Sie in der [ausführlichen Dokumentation](../reports/alerts.md).

  Verfügbarkeitsdatum: 14. Oktober 2025

#### Orchestrierte Kampagnen

* **Vererbung von Datennutzungs-Labels für Zielgruppen** – Labels, die in Adobe Experience Platform angewendet werden, werden jetzt beim Speichern von <strong>Zielgruppen</strong> in orchestrierten Kampagnen automatisch übernommen, wodurch das manuelle <strong>DULE-Tagging</strong> reduziert wird. [Weitere Informationen](../orchestrated/activities/save-audience.md)

* **Vordefinierte Filter mit Parametern** – Sie können jetzt <strong>vordefinierte Filter</strong> mit <strong>Parametern</strong> in orchestrierten Kampagnen erstellen, um wiederverwendbare, bearbeitbare Regeln zu erhalten. [Weitere Informationen](../orchestrated/predefined-filters.md)

* **Auswählen von Attributen und Kopieren von Verteilungswerten** – Sie können jetzt direkt in der Ansicht <strong>Werteverteilung</strong> in orchestrierten Kampagnen <strong>Werte auswählen oder kopieren</strong>. [Weitere Informationen](../orchestrated/build-query.md)

* **Nachrichtenbestätigung vor dem Versand** – Ein <strong>Bestätigungsschritt</strong> ist jetzt standardmäßig aktiviert, bevor orchestrierte Kampagnen gesendet werden, um versehentliche Sendungen zu reduzieren. [Weitere Informationen](../orchestrated/activities/channels.md#confirm-message-sending)

* **Vordefinierte Retargeting-Filter** – Um das Retargeting für Anwendungsfälle mit orchestrierten Kampagnen zu erleichtern, werden in dieser Version neue <strong>Kampagnen-Feedback-Filter</strong> eingeführt. Mit diesen Filtern können Sie Zielgruppen direkt ansprechen, die auf <strong>Interaktionen mit Nachrichten</strong> basieren, z. B. gesendet, nur geöffnet, geöffnet oder geklickt oder geöffnet und geklickt, und die spezifische Kampagne oder Kampagne in der Transitionsphase auswählen, die Sie erneut ansprechen möchten. [Weitere Informationen](../orchestrated/retarget.md)

* **Unterstützung der Ratensteuerung** – Orchestrierte Kampagnen unterstützen jetzt <strong>Ratensteuerung</strong>, um Sendungen zu beschleunigen und <strong>Volumenbeschränkungen</strong> einzuhalten. [Weitere Informationen](../orchestrated/activities/channels.md#rate-control)

* **Schaltfläche „Neu starten“** – Orchestrierte Kampagnen enthalten jetzt eine <strong>Schaltfläche „Neu starten“</strong>, damit Sie bei Bedarf schnell <strong>Ausführungen neu starten</strong> können, bevor Sie die Kampagne veröffentlichen. [Weitere Informationen](../orchestrated/start-monitor-campaigns.md)

* **Unterstützung benutzergenerierter Metadaten** – Die Helper-Funktion <strong>executionMetadata</strong> ist jetzt für orchestrierte Kampagnen im Personalisierungseditor verfügbar, damit Sie jeder nativen Aktion Kontextinformationen anhängen und sie in einem Datensatz speichern können, um sie in externe Systeme zu exportieren. [Weitere Informationen](../personalization/functions/helpers.md#execution-metadata)

  Verfügbarkeitsdatum: Mittwoch, 27. Januar 2026

* **Live-Kampagnen auf Entwurfsstatus zurücksetzen** - Sie können jetzt orchestrierte Live-Kampagnen auf den Entwurfsstatus zurücksetzen, wenn Ausführungsfehler auftreten oder Sie geplante Kampagnen ändern müssen, bevor sie ausgeführt werden können. Diese Option ist verfügbar, bis die erste Nachricht gesendet wird. [Weitere Informationen](../orchestrated/start-monitor-campaigns.md#back-to-draft)

#### Kampagnen

* **Kampagne mithilfe der Zeitzone des Profils planen** - Die Kampagnenplanung kann jetzt die <strong>Zeitzone“ jedes Profils verwenden, </strong> Nachrichten zur gewünschten lokalen Zeit zu versenden. [Weitere Informationen](../campaigns/campaign-schedule.md)

  **Hinweis**: Diese Verbesserung steht nur einer Reihe von Organisationen zur Verfügung (eingeschränkte Verfügbarkeit).

  Verfügbarkeitsdatum: Mittwoch, 27. Januar 2026

#### Berechtigungen

* **Verhindern von Selbstvalidierung für Journeys und Kampagnen** – Beim Erstellen oder Festlegen einer <strong>Validierungsrichtlinie</strong> wurde eine Option hinzugefügt, um Erstellende von Journeys oder Kampagnen daran zu hindern, <strong>ihre eigenen Objekte zu genehmigen</strong>. [Weitere Informationen](../test-approve/approval-policies.md)

  Verfügbarkeitsdatum: Mittwoch, 27. Januar 2026

<!--
## Coming soon {#jan-26-01-coming-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

### Features


<table>
<thead>
<tr>
<th><strong>Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports <strong>Web Push notifications</strong>, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both <strong>mobile and desktop browsers</strong>, enabling you to reach customers directly on their devices without requiring an app. This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>Previously released in Beta, this capability will be available to all environments (General Availability).</p>
<p>Availability date: February 11, 2026</p>
</td>
</tr>
</tbody>
</table>

### Improvements


-->