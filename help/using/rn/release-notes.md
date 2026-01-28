---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3f363a006ed25c07f3ea5b516f5fc306b230d029
workflow-type: tm+mt
source-wordcount: '1799'
ht-degree: 15%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] verwendet ein kontinuierliches Bereitstellungsmodell, das es Adobe ermöglicht, laufend neue Funktionen, Verbesserungen und Fehlerbehebungen bereitzustellen. Dieser Ansatz ermöglicht ein skalierbares Rollout von Funktionen in Phasen, um die Leistung und Stabilität aller Umgebungen sicherzustellen.

Aufgrund dieses Modells werden die Versionshinweise zwischen den monatlichen Versionen aktualisiert. Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Versionshinweise Januar &#39;26 {#latest-rn}

**Veröffentlichungsdatum**: 27.-28. Januar 2026

Die Abschnitte [Funktionen](#jan-26-01-features) und [Verbesserungen](#jan-26-01-improv) decken bereits verfügbare Funktionen ab, während [in Kürze verfügbar](#jan-26-01-coming-soon) Elemente auflistet, die für ein späteres Verfügbarkeitsdatum geplant sind.

<!-- **The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date. 

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### Neue Funktionen {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Journey Agent - Journey erstellen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent bietet jetzt Funktionen zur Inhaltserstellung, mit denen Journey Optimizer-Anwender Marketing-Journey über eine <strong>Natural Language Interface) erstellen und </strong> können. Praktizierende können schnell Journey erstellen, indem sie ihre Anforderungen in Gesprächsaufforderungen beschreiben. Dadurch wird der Prozess der Journey-Erstellung optimiert, sodass sich Marketer auf die Strategie und nicht auf die technische Konfiguration konzentrieren können.</p>
<p>Weitere Informationen finden Sie in der <a href="../start/ai-features.md#journey-agent">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Dienstag, 12. Januar 2026</p>
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
<p>Mit einer neuen API können Sie Aktionskampagnen abrufen und nach Schlüsselattributen filtern, um Automatisierungs- und Reporting-Workflows zu unterstützen.</p>
<p>Weitere Informationen finden Sie in der <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Dienstag, 24. November 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Warnhinweise</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Neue Journey-Warnhinweise helfen Ihnen bei der Überwachung wichtiger Journey-Zustandssignale. Diese Version führt Warnhinweistypen für die Verwerfungsrate von Profilen, die Fehlerrate benutzerdefinierter Aktionen und die Profilfehlerrate sowie konfigurierbare Schwellenwerte und Warnhinweisabonnements auf Journey-Ebene aus dem Journey-Inventar ein.</p>
<p>Die Schwellenwerte gelten für alle Journey.</p>
<p>Weitere Informationen finden Sie in der <a href="../reports/alerts.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Mittwoch, 14. Oktober 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Designer-Designs per E-Mail versenden</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Wenden Sie beim Erstellen von E-Mail-Inhalten konsistente Stile in der E-Mail-Designer mit wiederverwendbaren Designs an.</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../email/apply-email-themes.md">ausführlichen Dokumentation</a>.</p>
<p>Diese Funktion ist für eine Reihe von Organisationen in begrenzter Verfügbarkeit verfügbar. Wenden Sie sich an den Adobe-Support.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 5. November 2025</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#jan-26-01-improv}

#### Experience Decisioning

* **Fragmente an Entscheidungselemente anhängen** - Journey Optimizer bietet jetzt die Möglichkeit, <strong>Fragmente</strong> an Entscheidungselemente anzuhängen, die in Code-basierten Erlebniskampagnen über Entscheidungsrichtlinien genutzt werden können. [Weitere Informationen](../experience-decisioning/items.md)

  **Hinweis**: Diese Verbesserung wurde zuvor nur in begrenzter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).

#### Journeys

* **Nutzen einer Fehlerreaktions-Payload beim Journey benutzerdefinierter Aktionen** - Sie können jetzt eine optionale <strong>Fehlerreaktions-Payload</strong> für benutzerdefinierte Aktionen definieren. Wenn ein Aufruf fehlschlägt, wird die Fehler-Payload im Journey-Kontext angezeigt und ist in der Zeitüberschreitungs-/Fehlerverzweigung neben `jo_status_code` verfügbar, um eine umfassendere Ausweichlogik und das Debugging zu unterstützen. [Weitere Informationen](../action/action-response.md)

* **Kombinieren von nativen und Adobe Campaign-Nachrichtenaktionen** - Mit Journey Optimizer können Sie jetzt Adobe Campaign v7/v8-Nachrichtenaktionen mit nativen Kanalaktionen auf derselben Journey kombinieren. [Weitere Informationen](../building-journeys/using-adobe-campaign-v7-v8.md)

* **Validierung der Journey-Payload-Größe in Journey** - Journey Optimizer validiert jetzt die Journey-Payload-Größen, um eine optimale Leistung und Systemstabilität zu gewährleisten. Beim Erstellen oder Veröffentlichen von Journey erhalten Sie deutliche Warnhinweise und Fehler, wenn die Payload-Größe die empfohlenen Grenzwerte erreicht oder überschreitet, sowie praktische Anleitungen zur Optimierung Ihrer Journey-Konfiguration. Diese proaktive Validierung hilft Ihnen, potenzielle Probleme frühzeitig zu erkennen und die Journey-Leistung aufrechtzuerhalten. [Weitere Informationen](../start/guardrails.md#message-content-size)

#### Orchestrierte Kampagnen

* **Attribute auswählen und Verteilungswerte kopieren** - Sie können jetzt Werte direkt in der Ansicht Werteverteilung in orchestrierten Kampagnen auswählen oder kopieren. [Weitere Informationen](../orchestrated/build-query.md)

* **Vererbung von Datennutzungskennzeichnungen für Zielgruppen** - Kennzeichnungen, die in Adobe Experience Platform angewendet werden, werden jetzt beim Speichern von Zielgruppen in orchestrierten Kampagnen automatisch übernommen, was das manuelle DULE-Tagging reduziert. [Weitere Informationen](../orchestrated/activities/save-audience.md)

* **Vordefinierte Retargeting-Filter** - Um das Retargeting für Anwendungsfälle mit orchestrierten Kampagnen zu erleichtern, werden in dieser Version neue <strong>Kampagnen-Feedback-Filter</strong> eingeführt. Mit diesen Filtern können Sie Zielgruppen direkt ansprechen, basierend auf der Interaktion mit Nachrichten, wie z. B. gesendet, nur geöffnet, geöffnet oder geklickt oder geöffnet und geklickt, und die spezifische Kampagne oder Kampagne in der Übergangsphase auswählen, die Sie erneut ansprechen möchten. [Weitere Informationen](../orchestrated/retarget.md)

* **Vordefinierte Filter mit Parametern** - Sie können jetzt vordefinierte Filter mit <strong>Parametern</strong> in orchestrierten Kampagnen für wiederverwendbare, bearbeitbare Regeln erstellen. [Weitere Informationen](../orchestrated/predefined-filters.md)

* **Nachrichtenbestätigung vor dem Versand** - Ein <strong>Bestätigungsschritt</strong> ist jetzt standardmäßig aktiviert, bevor orchestrierte Kampagnen gesendet werden, um versehentliche Sendungen zu reduzieren. [Weitere Informationen](../orchestrated/activities/channels.md#confirm-message-sending)

* **Unterstützung benutzergenerierter Metadaten** - Die Hilfsfunktion <strong>executionMetadata</strong> ist jetzt für orchestrierte Kampagnen im Personalisierungseditor verfügbar, sodass Sie jeder nativen Aktion Kontextinformationen anhängen und sie in einem Datensatz speichern können, um sie in externe Systeme zu exportieren. [Weitere Informationen](../personalization/functions/helpers.md#execution-metadata)

* **Schaltfläche „Neustart** - Orchestrierte Kampagnen enthalten jetzt eine <strong>Schaltfläche „Neustart</strong>, sodass Sie Ausführungen bei Bedarf schnell neu starten können, bevor Sie die Kampagne veröffentlichen. [Weitere Informationen](../orchestrated/start-monitor-campaigns.md)

* **Unterstützung der Ratenkontrolle** - Orchestrierte Kampagnen unterstützen jetzt die <strong>Ratenkontrolle</strong>, damit Sie Sendungen schneller durchführen und sich an Volumenbeschränkungen ausrichten können. [Weitere Informationen](../orchestrated/activities/channels.md#rate-control)

#### Berechtigungen

* **Selbstvalidierung für Journey und Kampagnen verhindern** - Beim Erstellen oder Festlegen der Validierungsrichtlinie wurde eine Option hinzugefügt, mit der Journey- oder Kampagnenerstellende daran gehindert werden können, ihre eigenen Objekte zu validieren. [Weitere Informationen](../test-approve/approval-policies.md)

#### KI-Assistent

* **KI-Assistent für Inhaltsqualitätsprüfungen** - Zusätzlich zur Markenausrichtung können Sie die gesamte <strong>Inhaltsqualität</strong> bewerten, um unabhängig von Ihren Markenrichtlinien potenzielle Probleme mit Lesbarkeit, Kohärenz und Effektivität aufzudecken. Diese automatisierten Prüfungen werden dabei helfen, unklare Botschaften, inkonsistente Tonwerte oder strukturelle Lücken zu erkennen. Verfügbarkeit: 28. Januar 2026.

## Demnächst {#jan-26-01-coming-soon}

In den nächsten Tagen sind die folgenden Funktionen und Verbesserungen zur Veröffentlichung vorgesehen. **Informationen können Änderungen unterliegen**. Aktualisierte Links, Bildschirme und Dokumentationen werden freigegeben, sobald diese Aktualisierungen live in der Produktion verfügbar sind.

### Funktionen

<table>
<thead>
<tr>
<th><strong>Nachrichtenexport</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine neue Funktion <strong>Nachrichtenexport</strong> ist für E-Mail- und SMS-Kanäle verfügbar. Mit dieser Funktion können Sie gesendeten Nachrichteninhalt automatisch in einen dedizierten Experience Platform-Datensatz exportieren, sodass Sie:</p>
<ul>
<li>Einhaltung behördlicher Auflagen (z. B. HIPAA)</li>
<li>Archivieren von Nachrichten für Rechtsansprüche und Anfragen an die Kundenunterstützung</li>
<li>Kopien der an Einzelpersonen gesendeten personalisierten Inhalte aufbewahren</li>
</ul>
<p>Datensätze werden im AJO-Nachrichtenexport-Datensatz 7 Kalendertage nach der Aufnahme aufbewahrt. Während dieser Aufbewahrungsfrist können Sie die Daten über Experience Platform-Ziele in Ihren eigenen Speicher exportieren. Die Funktion wird auf der Ebene der Kanalkonfiguration aktiviert, sodass Sie granulare Kontrolle darüber erhalten, welche Nachrichten exportiert werden.</p>
<p>Diese Funktion ist nur für den E-Mail- und SMS-Kanal für Organisationen verfügbar, die das Add-on „Nachrichtenexport“ erworben haben. Weitere Informationen erhalten Sie beim Adobe-Support.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 28. Januar 2026</p>
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
<p>Adobe Journey Optimizer unterstützt <strong>Web-Push-Benachrichtigungen</strong> und erweitert den Push-Kanal über Mobile hinaus. Sie können Benachrichtigungen sowohl an mobile als auch an Desktop-Browser senden, sodass Sie Kunden direkt auf ihren Geräten erreichen können, ohne eine App zu benötigen. Diese Verbesserung hilft Ihnen, Benutzer mit zeitnahen, personalisierten Nachrichten in Echtzeit zu interagieren, indem dieselben Authoring-Workflows und Targeting-Funktionen genutzt werden, die bereits für mobile Push-Benachrichtigungen verfügbar sind.</p>
<p>Diese Funktion wurde bereits in Beta veröffentlicht und steht allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum: Donnerstag, 28. Januar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Self-Service-Migrations-Tools-APIs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Migrations-Tool</strong>APIs stehen zur programmgesteuerten Migration von Entscheidungs-Management-Entitäten zu Decisioning zur Verfügung, einschließlich:</p>
<ul>
<li>Flexible Migrationsbereiche (Sandbox-, Angebots- oder Entscheidungsebene)</li>
<li>Automatisierte Analyse und Validierung von Abhängigkeiten</li>
<li>Rollback-Unterstützung für abgeschlossene Migrationen</li>
<li>Detaillierte Migrationsberichte mit Objektzuordnungen</li>
</ul>
<p>Verfügbarkeitsdatum: Donnerstag, 28. Januar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ruhige Stunden (zeitbasierte Ausschlüsse)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Ruhestunden können Sie <strong>zeitbasierte Ausschlüsse</strong> für E-Mail-, SMS-, Push- und WhatsApp-Kanäle definieren. Sie stellen sicher, dass während bestimmter Zeiträume keine Nachrichten gesendet werden, und helfen Ihnen so, Kundenpräferenzen und Compliance-Anforderungen zu erfüllen. Ruhestunden können über <strong>Regelsätze“ angewendet werden, </strong> zur präzisen Steuerung einzelnen Aktionen in Kampagnen oder Journey zugewiesen werden können.</p>
<p>Diese Funktion wurde bereits in eingeschränkter Verfügbarkeit veröffentlicht und steht allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit). In dieser Version für allgemeine Verfügbarkeit bietet die Funktion außerdem die Möglichkeit, eine Kampagnenaktion bis zum Abschluss der Ruhezeiten in die Warteschlange einzureihen und eine Vorschau der aktivierten Regel für ruhige Stunden anzuzeigen.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 28. Januar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Briefpost-Kanal in Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Zuvor war der Kanal <strong>Briefpost</strong> auf der Journey-Arbeitsfläche nur für Kampagnen verfügbar, sodass Sie Briefpost in Ihre Journey integrieren können. Briefpost wird sowohl in Batch- als auch in 1:1-Journey-Szenarien unterstützt, mit Dateiextraktionskonfiguration und zeitbasierten Häufigkeitseinstellungen.</p>
<p>Diese Funktion wurde bereits in eingeschränkter Verfügbarkeit veröffentlicht und steht allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum: Donnerstag, 28. Januar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Briefpost-Kanal in orchestrierten Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der Briefpost-Kanal ist in orchestrierten Kampagnen verfügbar. Die <strong>Aktivität Briefpost</strong> erleichtert den Briefpostversand innerhalb Ihrer orchestrierten Kampagne sowohl für einmalige als auch für wiederkehrende Nachrichten. Es automatisiert die Generierung der <strong>Extraktionsdatei</strong> die von Briefpostanbietern benötigt wird. Sie können Kanalaktivitäten in der orchestrierten Kampagnen-Arbeitsfläche kombinieren, um kanalübergreifende Kampagnen zu erstellen, mit denen basierend auf dem Kundenverhalten und den Kundendaten Trigger erstellt werden.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 28. Januar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Überwachung benutzerdefinierter Aktionen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dem neuen Überwachungs-Dashboard und den angereicherten Journey-Schritt<strong>Ereignisdaten können Sie die Konsistenz und Leistung Ihrer benutzerdefinierten Aktionsendpunkte </strong> insight vertiefen. Verfolgen Sie erfolgreiche Aufrufe, Fehler, Durchsatz, Antwortzeiten und Warteschlangenwartezeiten, um schnell zu verstehen, wann, wo und warum Anomalien auftreten.</p>
<p>Diese Funktion wurde bereits in eingeschränkter Verfügbarkeit veröffentlicht und steht allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum: Donnerstag, 28. Januar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Inhaltserstellung in Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Adobe Experience Platform Agent Orchestrator wird <strong>Journey Agent</strong> in Journey Optimizer verfügbar sein und Ihnen ermöglichen, Journey über eine natürliche Sprachschnittstelle zu analysieren. Sie können kanalspezifische Inhalte direkt in Journey Agent generieren und verwalten, Inhalte für Kanäle wie E-Mail und Push erstellen, Vorlagen anwenden und in der Vorschau anzeigen, Ton und Stil durch Eingabeaufforderungen verfeinern und Inhalte in <strong>Content Designer</strong> zur kontextbezogenen Bearbeitung öffnen.</p>
<p>Verfügbarkeitsdatum: Dienstag, 2. Februar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Unterstützung von Entscheidungen in Push- und SMS-Kanälen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können den Inhalt Ihrer Push- und SMS-Nachrichten mit "<strong>" personalisieren und </strong>. Verwenden Sie Entscheidungsrichtlinien, <strong>Prioritätswerte</strong> Formeln oder KI-Modelle, um Ihren Kundinnen und Kunden die besten Inhalte anzuzeigen.</p>
<p>Verfügbarkeitsdatum: Mittwoch, 3. Februar 2026</p>
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
<p>Eine neue <strong>Aktivität Inhaltsentscheidung</strong> steht auf der Journey-Arbeitsfläche zur Verfügung, um personalisierte Angebote direkt in die Journey Ihrer Kunden zu integrieren. Mit dieser Aktivität können Sie entscheidungsbasierte Inhalte bereitstellen und diese Angebote auf Ihrem gesamten Journey referenzieren. Dies erfolgt unter Bedingungen für die Erstellung von Verzweigungen auf der Grundlage der Eignung, in benutzerdefinierten Aktionen für die Weitergabe von Angebotsdaten an externe Systeme und in anderen Aktivitäten für die Erstellung vollständig personalisierter Kundenerlebnisse.</p>
<p>Diese Funktion steht allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum: Mittwoch, 3. Februar 2026</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

* **SMS-Webhooks** - <strong>Webhooks</strong> werden von allen SMS-Anbietern unterstützt. Sie können jeden Webhook für den jeweiligen Verwendungszweck konfigurieren: eingehende Webhooks zur Erfassung eingehender Nachrichten und Feedback-Webhooks für den Empfang von Empfangsbestätigungen, Statusaktualisierungen und anderen nachrichtenbezogenen Ereignissen. Verfügbarkeit: 28. Januar 2026.

* **Kampagne mithilfe der Zeitzone des Profils planen** - Die Kampagnenzeitplanung kann die <strong>Zeitzone“ jedes Profils verwenden, </strong> Nachrichten zur vorgesehenen lokalen Zeit zu versenden. **Hinweis**: Diese Verbesserung steht nur einer Reihe von Organisationen zur Verfügung (eingeschränkte Verfügbarkeit). Verfügbarkeit: 28. Januar 2026.
