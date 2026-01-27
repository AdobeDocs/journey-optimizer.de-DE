---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 33bb27ff4181e196d05f320c5b958628a6bd6bf6
workflow-type: tm+mt
source-wordcount: '1707'
ht-degree: 19%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] verwendet ein kontinuierliches Bereitstellungsmodell, das es Adobe ermöglicht, laufend neue Funktionen, Verbesserungen und Fehlerbehebungen bereitzustellen. Dieser Ansatz ermöglicht ein skalierbares Rollout von Funktionen in Phasen, um die Leistung und Stabilität aller Umgebungen sicherzustellen.

Aufgrund dieses Modells werden die Versionshinweise zwischen den monatlichen Versionen aktualisiert. Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Hinweise zur Vorabversion vom Januar 2026 {#latest-rn}

**Veröffentlichungsdatum**: Mittwoch, 27. Januar 2026

**Die nachfolgenden Vorab- Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentationen werden in den Versionshinweisen am Veröffentlichungsdatum veröffentlicht.

Siehe auch [Vorab veröffentlichte Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

### Neue Funktionen {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Ruhige Stunden (zeitbasierte Ausschlüsse)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Ruhestunden können Sie <strong>zeitbasierte Ausschlüsse</strong> für E-Mail-, SMS-, Push- und WhatsApp-Kanäle definieren. Sie stellen sicher, dass während bestimmter Zeiträume keine Nachrichten gesendet werden, und helfen Ihnen so, Kundenpräferenzen und Compliance-Anforderungen zu erfüllen. Ruhezeiten können über <strong>Regelsätze</strong> angewendet werden, die zur präzisen Steuerung Einzelaktionen in Kampagnen oder Journeys zugewiesen werden können.</p>
<p>Diese Funktion wurde zuvor in eingeschränkter Verfügbarkeit veröffentlicht und ist jetzt für alle Umgebungen verfügbar (allgemeine Verfügbarkeit). Mit dieser allgemeinen Verfügbarkeit bietet die Funktion jetzt die Möglichkeit für Kunden, eine Kampagnenaktion bis zum Abschluss der Ruhezeiten in die Warteschlange einzureihen und eine Vorschau der aktivierten Regel für Ruhezeiten anzuzeigen.</p>
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
<p>Adobe Journey Optimizer unterstützt jetzt <strong>Web-Push-Benachrichtigungen</strong> und erweitert den Push-Kanal über Mobile hinaus. Sie können Benachrichtigungen sowohl an mobile als auch an Desktop-Browser senden, sodass Sie Kunden direkt auf ihren Geräten erreichen können, ohne eine App zu benötigen. Diese Verbesserung hilft Ihnen, Benutzer mit zeitnahen, personalisierten Nachrichten in Echtzeit zu interagieren, indem dieselben Authoring-Workflows und Targeting-Funktionen genutzt werden, die bereits für mobile Push-Benachrichtigungen verfügbar sind.</p>
<p>Diese Funktion wurde zuvor als Beta-Version veröffentlicht, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
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
<p>Zuvor auf Kampagnen beschränkt, ist <strong>Briefpostkanal</strong> jetzt auf der Journey-Arbeitsfläche verfügbar, sodass Sie Briefpost in Ihre Journey integrieren können. Briefpost kann jetzt sowohl in Batch- als auch in 1:1-Journey-Szenarien verwendet werden, mit Unterstützung für die Dateiextraktionskonfiguration und zeitbasierte Häufigkeitseinstellungen.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
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
<p>Der Briefpost-Kanal ist jetzt in orchestrierten Kampagnen verfügbar. Die <strong>Aktivität Briefpost</strong> erleichtert den Briefpostversand innerhalb Ihrer orchestrierten Kampagne für einmalige und wiederkehrende Nachrichten. Es automatisiert die Generierung der <strong>Extraktionsdatei</strong> die von Briefpostanbietern benötigt wird. Sie können Kanalaktivitäten in der orchestrierten Kampagnen-Arbeitsfläche kombinieren, um kanalübergreifende Kampagnen zu erstellen, mit denen basierend auf dem Kundenverhalten und den Kundendaten Trigger erstellt werden.</p>
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
<p>Sie können jetzt <strong>Entscheidungsrichtlinien“ </strong> SMS-Journey und -Kampagnen hinzufügen. Entscheidungsrichtlinien sind Container für Angebote, die die Entscheidungs-Engine nutzen, um für jedes Zielgruppenmitglied die besten Inhalte bereitzustellen.</p>
<p>Diese Funktion ist für eine Reihe von Organisationen in begrenzter Verfügbarkeit verfügbar. Wenden Sie sich an den Adobe-Support.</p>
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
<p><strong>Migrations-Tool</strong>APIs sind jetzt verfügbar, um Entscheidungs-Management-Entitäten programmgesteuert in Decisioning zu migrieren, einschließlich:</p>
<ul>
<li>Flexible Migrationsbereiche (Sandbox-, Angebots- oder Entscheidungsebene)</li>
<li>Automatisierte Analyse und Validierung von Abhängigkeiten</li>
<li>Rollback-Unterstützung für abgeschlossene Migrationen</li>
<li>Detaillierte Migrationsberichte mit Objektzuordnungen</li>
</ul>
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
<p>Vertiefen Sie insight in den Zustand und die Leistung Ihrer benutzerdefinierten Aktionsendpunkte mit einem neuen <strong>Überwachungs-Dashboard</strong> und angereicherten Journey-Schritt-Ereignisdaten. Verfolgen Sie erfolgreiche Aufrufe, Fehler, Durchsatz, Antwortzeiten und Warteschlangenwartezeiten, um schnell zu verstehen, wann, wo und warum Anomalien auftreten.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
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
<p>Journey Agent bietet jetzt Funktionen zur Inhaltserstellung, mit denen Journey Optimizer-Anwender Marketing-Journey über eine <strong>Natural Language Interface) erstellen und </strong> können. Praktizierende können schnell Journey erstellen, indem sie ihre Anforderungen in Gesprächsaufforderungen beschreiben. Dadurch wird der Prozess der Journey-Erstellung optimiert, sodass sich Marketer auf die Strategie und nicht auf die technische Konfiguration konzentrieren können.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#jan-26-01-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.

#### AI

* **KI-Assistent für Inhaltsqualitätsprüfungen** - Zusätzlich zur Markenausrichtung können Sie jetzt die gesamte <strong>Inhaltsqualität</strong> bewerten, um unabhängig von Ihren Markenrichtlinien potenzielle Probleme mit Lesbarkeit, Kohärenz und Effektivität aufzudecken. Diese automatisierten Prüfungen helfen bei der Erkennung unklarer Botschaften, inkonsistenter Tonwerte oder struktureller Lücken.

* **Aktualisieren von Marken mit neuer Farbregisterkarte** - Markenrichtlinien helfen sicherzustellen, dass Ihre Marke auf allen Kontaktpunkten konsistent präsentiert wird. Der neue <strong>Abschnitt Farben</strong> definiert die Standards für das Farbsystem Ihrer Marke und beschreibt, wie Farben in Erlebnissen ausgewählt, organisiert und angewendet werden. Es sorgt für die konsistente Verwendung von primären, sekundären, Akzent- und neutralen Farben, um eine kohärente, barrierefreie und erkennbare Markenidentität zu unterstützen.

#### Kanäle

* **SMS-Webhooks** - <strong>Webhooks</strong> werden jetzt von allen SMS-Anbietern unterstützt. Sie können jeden Webhook entsprechend seinem Verwendungszweck konfigurieren: eingehende Webhooks zum Erfassen eingehender Nachrichten und Feedback-Webhooks zum Empfangen von Versandbestätigungen, Statusaktualisierungen und anderen nachrichtenbezogenen Ereignissen.

#### Kampagnen

* **Kampagne mithilfe der Zeitzone des Profils planen** - Die Kampagnenplanung kann jetzt die <strong>Zeitzone“ jedes Profils verwenden, </strong> Nachrichten zur gewünschten lokalen Zeit zu versenden.

  **Hinweis**: Diese Verbesserung steht nur einer Reihe von Organisationen zur Verfügung (eingeschränkte Verfügbarkeit).


#### Experience Decisioning

* **Fragmente an Entscheidungselemente anhängen** - Journey Optimizer bietet jetzt die Möglichkeit, <strong>Fragmente</strong> an Entscheidungselemente anzuhängen, die in Code-basierten Erlebniskampagnen über Entscheidungsrichtlinien genutzt werden können.

  **Hinweis**: Diese Verbesserung wurde zuvor nur in begrenzter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).

#### Journeys

* **Nutzen einer Fehlerreaktions-Payload beim Journey benutzerdefinierter Aktionen** - Sie können jetzt eine optionale <strong>Fehlerreaktions-Payload</strong> für benutzerdefinierte Aktionen definieren. Wenn ein Aufruf fehlschlägt, wird die Fehler-Payload im Journey-Kontext angezeigt und ist in der Zeitüberschreitungs-/Fehlerverzweigung neben `jo_status_code` verfügbar, um eine umfassendere Ausweichlogik und das Debugging zu unterstützen.

* **Kombinieren von nativen und Adobe Campaign-Nachrichtenaktionen** - Mit Journey Optimizer können Sie jetzt Adobe Campaign v7/v8-Nachrichtenaktionen mit nativen Kanalaktionen auf derselben Journey kombinieren.

* **Validierung der Journey-Payload-Größe in Journey** - Journey Optimizer validiert jetzt die Journey-Payload-Größen, um eine optimale Leistung und Systemstabilität zu gewährleisten. Beim Erstellen oder Veröffentlichen von Journey erhalten Sie deutliche Warnhinweise und Fehler, wenn die Payload-Größe die empfohlenen Grenzwerte erreicht oder überschreitet, sowie praktische Anleitungen zur Optimierung Ihrer Journey-Konfiguration. Diese proaktive Validierung hilft Ihnen, potenzielle Probleme frühzeitig zu erkennen und die Journey-Leistung aufrechtzuerhalten.

#### Orchestrierte Kampagnen

* **Attribute auswählen und Verteilungswerte kopieren** - Sie können jetzt Werte direkt in der Ansicht Werteverteilung in orchestrierten Kampagnen auswählen oder kopieren.

* **Vererbung von Datennutzungskennzeichnungen für Zielgruppen** - Kennzeichnungen, die in Adobe Experience Platform angewendet werden, werden jetzt beim Speichern von Zielgruppen in orchestrierten Kampagnen automatisch übernommen, was das manuelle DULE-Tagging reduziert.

* **Vordefinierte Retargeting-Filter** - Um das Retargeting für Anwendungsfälle mit orchestrierten Kampagnen zu erleichtern, werden in dieser Version neue <strong>Kampagnen-Feedback-Filter</strong> eingeführt. Mit diesen Filtern können Sie Zielgruppen direkt ansprechen, basierend auf der Interaktion mit Nachrichten, wie z. B. gesendet, nur geöffnet, geöffnet oder geklickt oder geöffnet und geklickt, und die spezifische Kampagne oder Kampagne in der Übergangsphase auswählen, die Sie erneut ansprechen möchten.

* **Vordefinierte Filter mit Parametern** - Sie können jetzt vordefinierte Filter mit <strong>Parametern</strong> in orchestrierten Kampagnen für wiederverwendbare, bearbeitbare Regeln erstellen.

* **Nachrichtenbestätigung vor dem Versand** - Ein <strong>Bestätigungsschritt</strong> ist jetzt standardmäßig aktiviert, bevor orchestrierte Kampagnen gesendet werden, um versehentliche Sendungen zu reduzieren.

* **Unterstützung benutzergenerierter Metadaten** - Die Hilfsfunktion <strong>executionMetadata</strong> ist jetzt für orchestrierte Kampagnen im Personalisierungseditor verfügbar, sodass Sie jeder nativen Aktion Kontextinformationen anhängen und sie in einem Datensatz speichern können, um sie in externe Systeme zu exportieren.

* **Schaltfläche „Neustart** - Orchestrierte Kampagnen enthalten jetzt eine <strong>Schaltfläche „Neustart</strong>, sodass Sie Ausführungen bei Bedarf schnell neu starten können, bevor Sie die Kampagne veröffentlichen.

* **Unterstützung der Ratenkontrolle** - Orchestrierte Kampagnen unterstützen jetzt die <strong>Ratenkontrolle</strong>, damit Sie Sendungen schneller durchführen und sich an Volumenbeschränkungen ausrichten können.

#### Berechtigungen

* **Selbstvalidierung für Journey und Kampagnen verhindern** - Beim Erstellen oder Festlegen der Validierungsrichtlinie wurde eine Option hinzugefügt, mit der Journey- oder Kampagnenerstellende daran gehindert werden können, ihre eigenen Objekte zu validieren.

## Demnächst {#jan-26-01-coming-soon}

In den nächsten Tagen sind die folgenden Funktionen und Verbesserungen zur Veröffentlichung vorgesehen. **Informationen können Änderungen unterliegen**. Aktualisierte Links, Bildschirme und Dokumentationen werden freigegeben, sobald diese Aktualisierungen live in der Produktion verfügbar sind.

<table>
<thead>
<tr>
<th><strong>Inhaltserstellung in Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Adobe Experience Platform Agent Orchestrator ist <strong>Journey Agent</strong> in Journey Optimizer verfügbar und ermöglicht die Analyse von Journey über eine natürliche Sprachschnittstelle. Sie können jetzt kanalspezifische Inhalte direkt in Journey Agent generieren und verwalten, Inhalte für Kanäle wie E-Mail und Push erstellen, Vorlagen anwenden und in der Vorschau anzeigen, den Ton und Stil durch Eingabeaufforderungen verfeinern und Inhalte in <strong>Content Designer</strong> zur kontextbezogenen Bearbeitung öffnen.</p>
<p>Verfügbarkeitsdatum: Dienstag, 2. Februar 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Unterstützung von Entscheidungen im Push-Kanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt den Inhalt Ihrer Push-Nachrichten mit "<strong>" personalisieren und </strong>. Verwenden Sie <strong>Prioritätswerte</strong> Formeln oder KI-Modelle, um Ihren Kunden die besten Inhalte anzuzeigen.</p>
<p>Verfügbarkeitsdatum: Mittwoch, 3. Februar 2026</p>
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
<th><strong>Aktivität „Inhaltsentscheidung“ </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine neue <strong>Aktivität Inhaltsentscheidung</strong> ist jetzt auf der Journey-Arbeitsfläche verfügbar, um personalisierte Angebote direkt in die Journey Ihrer Kunden zu integrieren. Mit dieser Aktivität können Sie entscheidungsbasierte Inhalte bereitstellen und diese Angebote auf Ihrem gesamten Journey referenzieren. Dies erfolgt unter Bedingungen für die Erstellung von Verzweigungen auf der Grundlage der Eignung, in benutzerdefinierten Aktionen für die Weitergabe von Angebotsdaten an externe Systeme und in anderen Aktivitäten für die Erstellung vollständig personalisierter Kundenerlebnisse.</p>
<p>Diese Funktion steht allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum: Mittwoch, 3. Februar 2026</p>
</td>
</tr>
</tbody>
</table>
