---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 99dfadf6ac370187fd54d87f660c36662dbcb8d3
workflow-type: tm+mt
source-wordcount: '1709'
ht-degree: 22%

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

<!--**Release date**: January 27-28, 2026-->

Die Abschnitte [Funktionen](#jan-26-01-features) und [Verbesserungen](#jan-26-01-improv) decken bereits verfügbare Funktionen ab, während [in Kürze verfügbar](#jan-26-01-coming-soon) Elemente auflistet, die für ein späteres Verfügbarkeitsdatum geplant sind.

<!-- **The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date. 

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### Neue Funktionen {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Briefpost-Kanal in Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der Kanal <strong>Briefpost</strong> war bisher auf Kampagnen beschränkt und ist jetzt auf der Journey-Arbeitsfläche verfügbar, sodass Sie Briefpost in Ihre Journey integrieren können. Briefpost kann jetzt sowohl in Batch<strong> als auch in 1:1-Journey-Szenarien verwendet werden</strong> mit Unterstützung für die Dateiextraktionskonfiguration und zeitbasierte Häufigkeitseinstellungen.</p>
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
<th><strong>Ruhige Stunden (zeitbasierte Ausschlüsse)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Ruhige Stunden</strong> ermöglichen es Ihnen, zeitbasierte Ausschlüsse für E-Mail-, SMS-, Push- und WhatsApp-Kanäle zu definieren. Sie stellen sicher, dass während bestimmter Zeiträume keine Nachrichten gesendet werden, und helfen Ihnen so, Kundenpräferenzen und Compliance-Anforderungen zu erfüllen. Ruhezeiten können über <strong>Regelsätze</strong> angewendet werden, die zur präzisen Steuerung Einzelaktionen in Kampagnen oder Journeys zugewiesen werden können.</p>
<p>Diese Funktion wurde zuvor in eingeschränkter Verfügbarkeit veröffentlicht und ist jetzt für alle Umgebungen verfügbar. Mit dieser allgemeinen Verfügbarkeit bietet die Funktion jetzt die Möglichkeit, dass Kundinnen und Kunden eine Kampagnenaktion bis zum Abschluss der Ruhezeiten in die Warteschlange stellen und die aktivierte Regel für Ruhezeiten in der Vorschau anzeigen können.</p>
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
<p>Eine neue Funktion <strong>Nachrichtenexport</strong> ist jetzt für E-Mail- und SMS-Kanäle verfügbar. Mit dieser Funktion können Sie gesendeten Nachrichteninhalt automatisch in einen dedizierten Experience Platform-Datensatz exportieren, sodass Sie:</p>
<ul>
<li>Einhaltung behördlicher Auflagen (z. B. HIPAA)</li>
<li>Archivieren von Nachrichten für Rechtsansprüche und Anfragen an die Kundenunterstützung</li>
<li>Kopien der an Einzelpersonen gesendeten personalisierten Inhalte aufbewahren</li>
</ul>
<p>Datensätze werden im AJO-Nachrichtenexport-Datensatz 7 Kalendertage nach der Aufnahme aufbewahrt. Während dieses Aufbewahrungszeitraums können Sie sie über Experience Platform-Ziele in Ihren eigenen Speicher exportieren. Die Funktion wird auf der Ebene der Kanalkonfiguration aktiviert, sodass Sie <strong>granulare Kontrolle</strong> über die exportierten Nachrichten erhalten.</p>
<p>Diese Funktion ist nur für den E-Mail- und SMS-Kanal für Organisationen verfügbar, die das Add-on „Nachrichtenexport“ erworben haben. Weitere Informationen erhalten Sie beim Adobe-Support.</p>
<p><img src="assets/do-not-localize/message-export.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/message-export.md#message-export">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 28. Januar 2026</p>
</td>
</tr>
</tbody>
</table>

<!--table>
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
<p>Previously released in Beta, this capability is now available to all environments (General Availability).</p>
<p>For more information, refer to the detailed documentation.</p>
<p>Availability date: January 28, 2026</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Briefpost-Kanal in orchestrierten Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der Briefpost-Kanal ist jetzt in orchestrierten Kampagnen verfügbar. Die <strong>Briefpost-Aktivität</strong> erleichtert den Briefpostversand innerhalb Ihrer orchestrierten Kampagne, sowohl für einmalige als auch für wiederkehrende Nachrichten. Dies dient zur Automatisierung des Prozesses der Generierung der <strong>Extraktionsdatei</strong> die von Briefpostanbietern benötigt wird. Kanalaktivitäten können in der Arbeitsoberfläche für orchestrierte Kampagnen kombiniert werden, um kanalübergreifende Kampagnen zu erstellen, mit denen basierend auf Kundenverhalten und Daten Aktionen ausgelöst werden können.</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../orchestrated/activities/channels.md#channel">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 28. Januar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent - Journey erstellen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent bietet jetzt Funktionen zur Inhaltserstellung, mit denen Journey Optimizer-Anwender Marketing-Journey über eine <strong>Natural Language Interface) erstellen und </strong> können. Mit diesen neuen Fähigkeiten können Praktiker schnell Journey erstellen, indem sie ihre Anforderungen einfach in <strong>Gesprächshinweisen“ </strong>. Diese Neuerung optimiert den Prozess der Journey-Erstellung und ermöglicht es Marketing-Experten, sich auf die Strategie statt auf die technische Konfiguration zu konzentrieren.</p>
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
<p>Eine neue Journey Optimizer-API ist jetzt verfügbar, mit der Sie <strong>kampagnenbezogene Daten“ wie Details</strong> Versionen und Konfigurationen programmgesteuert abrufen und untersuchen können.</p>
<p>Weitere Informationen finden Sie in der <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Dienstag, 24. November 2025</p>
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
<p>Sie können jetzt <strong>vorab genehmigte Designs</strong> anwenden, um die <strong>Markenkonsistenz</strong> auf alle E-Mails sicherzustellen, den Prozess der Kampagnenerstellung zu beschleunigen und unabhängig hochwertige E-Mails zu erstellen, während Sie gleichzeitig die Abhängigkeit von Design-Teams reduzieren.</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>Diese Funktion wurde bereits in der Beta-Version veröffentlicht und ist jetzt für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p>Weitere Informationen finden Sie in der <a href="../email/apply-email-themes.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 5. November 2025</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#jan-26-01-improv}

#### AI

* **KI-Assistent für Inhaltsqualitätsprüfungen** - Zusätzlich zur Markenausrichtung können Sie jetzt die gesamte <strong>Inhaltsqualität</strong> bewerten, um potenzielle Probleme mit <strong>Lesbarkeit</strong>, Kohärenz und Effektivität unabhängig von Ihren Markenrichtlinien aufzudecken. Diese automatisierten Prüfungen helfen bei der Erkennung unklarer Botschaften, inkonsistenter Tonwerte oder struktureller Lücken. [Weitere Informationen](../content-management/brands-score.md#validate-quality).

  [Entdecken Sie diese Funktion im Video](https://video.tv.adobe.com/v/3470544/?learn=on).

#### Experience Decisioning

#### Journeys

* **Kombinieren von nativen und Adobe Campaign-Nachrichtenaktionen** - Mit Journey Optimizer können Sie jetzt <strong>Adobe Campaign v7/v8</strong>-Nachrichtenaktionen mit <strong>nativen Kanalaktionen</strong> auf derselben Journey kombinieren. [Weitere Informationen](../building-journeys/using-adobe-campaign-v7-v8.md)

  Verfügbarkeit: 27. Januar 2026.

* **Fehlerantwort-Payload für benutzerdefinierte Aktionen** - Sie können jetzt eine optionale <strong>Fehlerantwort-Payload</strong> für benutzerdefinierte Aktionen definieren. Wenn ein Aufruf fehlschlägt, wird die Fehler-Payload im Journey-Kontext (unter dem errorResponse-Knoten der Aktion) verfügbar gemacht und ist in der Verzweigung <strong>timeout/error</strong> verfügbar, um eine umfassendere Ausweichlogik und `jo_status_code` Debugging zu unterstützen. [Weitere Informationen](../action/about-custom-action-configuration.md#define-the-message-parameters)

  Verfügbarkeit: 27. Januar 2026.

* **Validierung der Journey-Payload-Größe in Journey** - Journey Optimizer validiert jetzt <strong>Payload-Größen</strong> um eine optimale Leistung und Systemstabilität sicherzustellen. Beim Erstellen oder Veröffentlichen von Journey erhalten Sie deutliche <strong>Warnungen und Fehler</strong> wenn die Payload-Größe die empfohlenen Grenzwerte erreicht oder überschreitet, sowie praktische Anleitungen zur Optimierung Ihrer Journey-Konfiguration. Diese proaktive Validierung hilft Ihnen, potenzielle Probleme frühzeitig zu erkennen und die Journey-Leistung aufrechtzuerhalten. [Weitere Informationen](../start/guardrails.md#journey-payload-size)

  Verfügbarkeit: 27. Januar 2026.


* **Journey-Warnhinweise** - Neue <strong>vorkonfigurierte Warnhinweise</strong> sind für Journey verfügbar.
   * <strong>Profil-Verwerfungsrate überschritten</strong> - Verhältnis der Verwerfen-Aktionen von Profilen zu den eingegebenen Profilen in den letzten 5 Minuten überschreitet den Schwellenwert
   * <strong>Fehlerrate für benutzerdefinierte Aktion überschritten</strong> - Verhältnis der Fehler benutzerdefinierter Aktionen zu erfolgreichen HTTP-Aufrufen in den letzten 5 Minuten überschreitet den Schwellenwert
   * <strong>Profilfehlerrate überschritten</strong> - Verhältnis der fehlerhaften Profile zu den in den letzten 5 Minuten eingegebenen Profilen hat den Schwellenwert überschritten

  Weitere Informationen finden Sie in der [ausführlichen Dokumentation](../reports/alerts.md).

  Verfügbarkeitsdatum: 14. Oktober 2025

#### Orchestrierte Kampagnen

* **Vererbung von Datennutzungskennzeichnungen für Zielgruppen** - Kennzeichnungen, die in Adobe Experience Platform angewendet werden, werden jetzt beim Speichern von <strong>Zielgruppen</strong> in orchestrierten Kampagnen automatisch übernommen, wodurch das manuelle <strong>DULE-Tagging</strong> reduziert wird. [Weitere Informationen](../orchestrated/activities/save-audience.md)

* **Vordefinierte Filter mit Parametern** - Sie können jetzt <strong>vordefinierte Filter</strong> mit <strong>Parametern</strong> in orchestrierten Kampagnen für wiederverwendbare, bearbeitbare Regeln erstellen. [Weitere Informationen](../orchestrated/predefined-filters.md)

* **Attribute auswählen und Verteilungswerte kopieren** - Sie können jetzt <strong>Werte auswählen oder kopieren</strong> direkt in der <strong>Werteverteilung</strong> in orchestrierten Kampagnen anzeigen. [Weitere Informationen](../orchestrated/build-query.md)

* **Nachrichtenbestätigung vor dem Versand** - Ein <strong>Bestätigungsschritt</strong> ist jetzt standardmäßig aktiviert, bevor orchestrierte Kampagnen gesendet werden, um versehentliche Sendungen zu reduzieren. [Weitere Informationen](../orchestrated/activities/channels.md#confirm-message-sending)

* **Vordefinierte Retargeting-Filter** - Um das Retargeting für Anwendungsfälle mit orchestrierten Kampagnen zu erleichtern, werden in dieser Version neue <strong>Kampagnen-Feedback-Filter</strong> eingeführt. Mit diesen Filtern können Sie Zielgruppen direkt ansprechen, die auf <strong>Interaktion mit Nachrichten</strong> basieren, z. B. gesendet, nur geöffnet, geöffnet oder geklickt oder geöffnet und geklickt, und die spezifische Kampagne oder Kampagne in der Übergangsphase auswählen, die Sie erneut ansprechen möchten. [Weitere Informationen](../orchestrated/retarget.md)

* **Unterstützung der Ratenkontrolle** - Orchestrierte Kampagnen unterstützen jetzt <strong>Ratenkontrolle</strong>, um Sendungen zu beschleunigen und <strong>Volumenbeschränkungen</strong>. [Weitere Informationen](../orchestrated/activities/channels.md#rate-control)

* **Schaltfläche „Neustart** - Orchestrierte Kampagnen enthalten jetzt eine <strong>Schaltfläche „Neustart</strong>, sodass Sie bei Bedarf schnell <strong>Neustarts durchführen</strong> können, bevor Sie die Kampagne veröffentlichen. [Weitere Informationen](../orchestrated/start-monitor-campaigns.md)

* **Unterstützung benutzergenerierter Metadaten** - Die Hilfsfunktion <strong>executionMetadata</strong> ist jetzt für orchestrierte Kampagnen im Personalisierungseditor verfügbar, sodass Sie jeder nativen Aktion Kontextinformationen anhängen und sie in einem Datensatz speichern können, um sie in externe Systeme zu exportieren. [Weitere Informationen](../personalization/functions/helpers.md#execution-metadata)

  Verfügbarkeit: 27. Januar 2026.

* **Live-Kampagnen auf Entwurfsstatus zurücksetzen** - Sie können jetzt orchestrierte Live-Kampagnen auf den Entwurfsstatus zurücksetzen, wenn Ausführungsfehler auftreten oder Sie geplante Kampagnen ändern müssen, bevor sie ausgeführt werden können. Diese Option ist verfügbar, bis die erste Nachricht gesendet wird. [Weitere Informationen](../orchestrated/start-monitor-campaigns.md#back-to-draft)

#### Kampagnen

* **Kampagne mithilfe der Zeitzone des Profils planen** - Die Kampagnenplanung kann jetzt die <strong>Zeitzone“ jedes Profils verwenden, </strong> Nachrichten zur gewünschten lokalen Zeit zu versenden. [Weitere Informationen](../campaigns/campaign-schedule.md)

  **Hinweis**: Diese Verbesserung steht nur einer Reihe von Organisationen zur Verfügung (eingeschränkte Verfügbarkeit).

  Verfügbarkeit: 27. Januar 2026.

#### Berechtigungen

* **Selbstvalidierung für Journey und Kampagnen verhindern** - Beim Erstellen oder Festlegen von <strong>Validierungsrichtlinie) wurde eine Option hinzugefügt, </strong> Journey- oder Kampagnenerstellende daran zu hindern, <strong>eigene Objekte zu genehmigen</strong>. [Weitere Informationen](../test-approve/approval-policies.md)

  Verfügbarkeit: 27. Januar 2026.

## Demnächst {#jan-26-01-coming-soon}

In den nächsten Tagen sind die folgenden Funktionen und Verbesserungen zur Veröffentlichung vorgesehen. **Informationen können Änderungen unterliegen**. Aktualisierte Links, Bildschirme und Dokumentationen werden freigegeben, sobald diese Aktualisierungen live in der Produktion verfügbar sind.

### Funktionen

<table>
<thead>
<tr>
<th><strong>Self-Service-Migrations-Tools-APIs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Migrations-Tool</strong>APIs sind jetzt verfügbar, um Entscheidungs-Management-Entitäten programmgesteuert in Decisioning zu migrieren, einschließlich:</p>
<ul>
<li>Flexible Migrationsbereiche (Sandbox-, Angebots- oder Entscheidungsebene)</li>
<li>Automatisierte Analyse und Validierung von Abhängigkeiten</li>
<li>Rollback-Unterstützung für abgeschlossene Migrationen</li>
<li>Detaillierte Migrationsberichte mit Objektzuordnungen</li>
</ul>
<p>Verfügbarkeitsdatum: Samstag, 30. Januar 2026</p>
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
<p>Mit Adobe Experience Platform Agent Orchestrator ist <strong>Journey Agent</strong> in Journey Optimizer verfügbar und ermöglicht die Analyse von Journey über eine natürliche Sprachschnittstelle. Sie können jetzt auch <strong>Inhalte generieren und verwalten</strong> direkt in Journey Agent, Inhalte für Kanäle wie E-Mail und Push erstellen, Vorlagen anwenden und in der Vorschau anzeigen, den Ton und Stil durch Eingabeaufforderungen verfeinern und Inhalte in Content Designer zur kontextbezogenen Bearbeitung öffnen.</p>
<p>Verfügbarkeitsdatum: Dienstag, 9. Februar 2026</p>
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
<p>Sie können jetzt den Inhalt Ihrer <strong>Push- und SMS-Nachrichten) mit </strong>Decisioning<strong> personalisieren und </strong>. Verwenden Sie Prioritätswerte, Formeln oder KI-Modelle, um Ihren Kunden den besten Inhalt anzuzeigen.</p>
<p>Verfügbarkeitsdatum: Dienstag, 9. Februar 2026</p>
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
<p>Eine neue <strong>Aktivität Inhaltsentscheidung</strong> ist jetzt auf der Journey-Arbeitsfläche verfügbar, um (<strong>) </strong> direkt in die Journey Ihrer Kunden zu integrieren. Mit dieser Aktivität können Sie entscheidungsbasierte Inhalte bereitstellen und diese Angebote auf Ihrem gesamten Journey referenzieren - unter Bedingungen für die Erstellung von Verzweigungen auf der Grundlage der Eignung, in benutzerdefinierten Aktionen für die Weitergabe von Angebotsdaten an externe Systeme und in anderen Aktivitäten für die Erstellung vollständig personalisierter Kundenerlebnisse.</p>
<p>Diese Funktion steht allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum: Dienstag, 9. Februar 2026</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen


* **Fragmente an Entscheidungselemente anhängen** - Journey Optimizer bietet jetzt die Möglichkeit, <strong>Fragmente</strong> an <strong>Entscheidungselemente</strong> anzuhängen, die in code-basierten Erlebniskampagnen über Entscheidungsrichtlinien genutzt werden können.

  Verfügbarkeitsdatum: 9. Februar 2026
