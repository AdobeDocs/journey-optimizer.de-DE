---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 48d1e15bab9bc01d31795358cc4f632fd2a5b7dc
workflow-type: tm+mt
source-wordcount: '3121'
ht-degree: 28%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] verwendet ein kontinuierliches Bereitstellungsmodell, das es Adobe ermöglicht, laufend neue Funktionen, Verbesserungen und Fehlerbehebungen bereitzustellen. Dieser Ansatz ermöglicht ein skalierbares Rollout von Funktionen in Phasen, um die Leistung und Stabilität aller Umgebungen sicherzustellen.

Aufgrund dieses Modells werden die Versionshinweise zwischen den monatlichen Versionen aktualisiert.  Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Hinweise zur Vorabversion vom 26. März {#march-26-rn}

**Die nachfolgenden Vorab- Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentationen werden in den Versionshinweisen am Veröffentlichungsdatum veröffentlicht.

Siehe auch [Vorab veröffentlichte Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Veröffentlichungsdatum**: 24.-25. März 2026

### Neue Funktionen {#march-26-features}

<!--
<table>
<thead>
<tr>
<th><strong>LLM email optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now optimize your email content for deliverability using large language model (LLM) technology. The LLM email optimizer analyzes your email content and provides actionable recommendations to improve sender reputation, avoid spam filters, and enhance overall deliverability performance.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Journey Agent: Anwendungsfall für orchestrierte Kampagnen erstellen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey Agent</strong>, unterstützt durch Adobe Experience Platform Agent Orchestrator, kann jetzt vollständige <strong>Orchestrierte Kampagne</strong>-Anwendungsfälle über eine natürliche Sprachschnittstelle erstellen. Beschreiben Sie Ihre Kampagnenziele und -anforderungen in verständlicher Sprache. Journey Agent konfiguriert die Kampagnenstruktur, die Aktivitäten und das Targeting für Sie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: Kanalinhalte erstellen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit <strong>Adobe Experience Platform Agent Orchestrator </strong> ist <strong>Journey Agent</strong> in Journey Optimizer verfügbar und ermöglicht es Ihnen, Journey über eine natürliche Sprachschnittstelle zu analysieren. Sie können jetzt auch kanalspezifische Inhalte direkt in Journey Agent generieren und verwalten, Inhalte für Kanäle wie E-Mail und Push erstellen, Vorlagen anwenden und in der Vorschau anzeigen, Ton und Stil durch Eingabeaufforderungen verfeinern und Inhalte in <strong>Content Designer</strong> zur kontextbezogenen Bearbeitung öffnen.</p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p>Weitere Informationen finden Sie in der <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 4. März 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Transaktionsnachrichten in koordinierten Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Orchestrierte Kampagnen unterstützen jetzt <strong>Transaktionsnachrichten</strong>, sodass Sie ereignisgesteuerte Nachrichten in Echtzeit wie Bestellbestätigungen, Buchungsbenachrichtigungen und Kontoaktualisierungen direkt in Ihrem Kampagnen-Workflow Trigger können.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vom Trigger orchestrierte Kampagnen mithilfe der API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt einen Trigger für eine orchestrierte Kampagne über die API durchführen. Konfigurieren Sie die Zielkampagne als „Ausgelöst durch ein Signal“ und veröffentlichen Sie sie. Verwenden Sie dann einen API-Aufruf, um die Kampagne auszulösen. Der API-Aufruf kann Parameter enthalten, die als Variablen in der ausgelösten Kampagne verfügbar sind.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Inkrementelle Abfrageaktivität in koordinierten Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine neue Aktivität <strong>Inkrementelle Abfrage</strong> ist jetzt in orchestrierten Kampagnen verfügbar. Diese Aktivität fragt nur neue oder aktualisierte Datensätze seit der letzten Ausführung des Workflows ab, wodurch die Verarbeitungszeit erheblich verkürzt und die Effizienz wiederkehrender Kampagnen, die auf große Datensätze abzielen, verbessert wird.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Testaktivität in koordinierten Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine neue <strong>Test</strong>-Aktivität ist jetzt in orchestrierten Kampagnen verfügbar. Diese Aktivität leitet die Workflow-Ausführung basierend auf definierten Bedingungen an verschiedene Verzweigungen weiter, sodass Sie Kampagnenlogik und -konfigurationen vor der Aktivierung von Live-Sendungen validieren können.</p>
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
<p><strong>Journey-Pfadoptimierung: </strong> KI, um die bisherige Journey-Leistung zu analysieren und automatisch den besten Pfad für jeden Kunden auszuwählen, um Konversions- und Interaktionsergebnisse zu maximieren.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Unterstützung der Datensatzsuche in Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine neue Aktivität in Journey namens Datensatzsuche ermöglicht während der Laufzeit das dynamische Abrufen von Daten aus Adobe Experience Platform-Datensatzdatensätzen. Mit dieser Funktion können Sie auf Daten zugreifen, die sich möglicherweise nicht in der Profil- oder Ereignis-Payload befinden. So können Sie sicherstellen, dass Ihre Kundeninteraktionen sowohl relevant als auch zeitlich passend sind. Diese Funktion wurde bereits in eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit). Weitere Informationen finden Sie in der <a href="../building-journeys/dataset-lookup.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Native Kanalaktionsaktivitäten werden nicht mehr unterstützt</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nach der allgemeinen Verfügbarkeit der <strong>Aktionsaktivität</strong> im Februar 2026 werden alte native Kanalaktionsaktivitäten (E-Mail, SMS, Push, In-App usw.) auf der Journey-Arbeitsfläche jetzt nicht mehr unterstützt. Vorhandene Journey, die ältere Kanalaktivitäten verwenden, funktionieren weiterhin, ohne dass Änderungen oder eine Migration erforderlich sind. Weitere Informationen finden Sie in der <a href="../building-journeys/journey-action.md">ausführlichen Dokumentation</a>.</p>
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
<p>Sie können jetzt <strong>Decisioning</strong> verwenden, um den Inhalt Ihrer E-Mail-Nachrichten zu personalisieren und zu optimieren. Nutzen Sie Prioritätswerte, Formeln oder KI-Modelle, um jedem Empfänger die relevantesten Angebote und Inhalte anzuzeigen.</p>
<p>Diese Funktion wurde bereits in eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit). Mit dieser Version zur allgemeinen Verfügbarkeit werden nun Mirrorseiten unterstützt.</p>
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/create-decision-policy.md">ausführlichen Dokumentation</a>.</p>
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
<p><img src="assets/do-not-localize/ai-model-observability.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/ranking/ai-model-observability.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Dienstag, 9. März 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Benutzerdefinierte Formulare in Landingpages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt <strong>benutzerdefinierte Formulare</strong> in Landingpages erstellen, um bestimmte Abonnentendaten über die standardmäßigen Opt-in-Felder hinaus zu erfassen. Definieren Sie Ihre eigenen Formularfelder, Validierungsregeln und Übermittlungsverhalten, um eine breitere Palette von Anwendungsfällen für Abonnements und Profilanreicherung zu unterstützen.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nachrichten-Posteingang</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer In <strong> ist jetzt ein neuer </strong>Nachrichten-Posteingang“ verfügbar, der eine zentralisierte Ansicht der empfangenen In-App-, Push- und SMS-Nachrichten bietet. Empfänger und Empfängerinnen können an einem Ort auf alle ihre Nachrichten zugreifen und mit ihnen interagieren, was eine umfassendere Interaktion und erneute Interaktion mit ihnen ermöglicht.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Konvertieren von Bildern in E-Mail-Inhaltsvorlagen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Bilder direkt in Journey Optimizer in E-Mail-Inhaltsvorlagen konvertieren. Verwenden Sie die KI-gestützte Analyse, um automatisch strukturierte HTML-Vorlagen aus visuellen Referenzen zu generieren, wodurch die E-Mail-Design-Zeit erheblich verkürzt wird.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Erweiterter HTML-Editor für E-Mail-Vorlagen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Im erweiterten HTML-Modus für E-Mail-Inhaltsvorlagen können Sie die HTML-Quelle Ihres Inhalts in der E-Mail-Designer bearbeiten, erweiterte Ausdrücke (z. B. Bedingungen) in der Quelle hinzufügen und zwischen der HTML-Ansicht und der Desktop-Ansicht wechseln, ohne Ihre Änderungen zu verlieren.</p>
<p>Diese Funktion ist nur für den E-Mail-Kanal in Inhaltsvorlagen verfügbar. Sie ist derzeit nur eingeschränkt verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugang zu erhalten.</p>
<p><img src="assets/do-not-localize/expert-mode.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../content-management/email-template-expert-mode.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Mittwoch, 10. März 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integration von benutzerdefinierten Firefly-Modellen und Drittanbieter-Image-Generierungsmodellen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ermöglichen Sie die nahtlose Integration von standardmäßigen und benutzerdefinierten Firefly-Modellen zusammen mit genehmigten Bildmodellen von Drittanbietern, um die Flexibilität, Kontrolle und Markenausrichtung beim Erzeugen von Bildern zu verbessern.</p>
<p>Wählen Sie das richtige Modell für Ihre Anforderungen:</p>
<ul><li> <strong>Adobe-Modell</strong> (unterstützt von Firefly Image Model 4) für die sofortige Bildgenerierung ohne zusätzliche Einrichtung</li><li> <strong>Partnermodell</strong> (unterstützt von Gemini 2.5 Flash) für spezielle Funktionen</li><li><strong>Benutzerdefinierte Modelle</strong> (markenspezifische Modelle, die auf Ihren eigenen Assets trainiert wurden) für die Generierung innerhalb der Marke, die genau auf Ihre Markenidentität, Ihren Stil und Ihre visuellen Richtlinien abgestimmt ist.</li></ul>
<p>Weitere Informationen finden Sie in der <a href="../content-management/generative-models.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Dienstag, 2. März 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Live-Aktivität für iOS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit iOS Live Activity in Adobe Journey Optimizer können Sie Echtzeit-Erlebnisse direkt in Lock Screens und Dynamic Island Ihrer Kunden integrieren. Live-Updates bereitstellen, von der Bestellverfolgung und dem Flugstatus bis hin zu Zählungen von Ereignissen, Live-Scores und Versandfortschritt, ohne dass Benutzer Ihre App öffnen müssen. Halten Sie Ihr Publikum zum richtigen Zeitpunkt und an der richtigen Stelle auf dem Laufenden und engagieren Sie sich aktiv.</p>
<p>Diese Funktion wurde bereits in der Beta-Version veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../mobile-live/get-started-mobile-live.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Mittwoch, 3. März 2026</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#march-26-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.

#### Journeys

* **Journey-Schlichtung - KI-Modelle** - Zusätzlich zu den Rangfolgeformeln können KI-Modelle jetzt mit der Journey-Schlichtung verwendet werden, um den Journey-Eintrag für Kunden automatisch zu ordnen und zu priorisieren. Dabei wird maschinelles Lernen verwendet, um die relevanteste Journey für jedes Profil auf der Grundlage von Verlaufsverhalten und Kontextsignalen zu ermitteln. Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.

* **Senden ausgehender Nachrichten in Journey** - Sie können jetzt den Versand von Nachrichten aus Journey Optimizer Journey in kontrollierten Batches über einen bestimmten Zeitraum planen. [Weitere Informationen](../building-journeys/send-using-waves.md)

  Diese Funktion wurde bereits in eingeschränkter Verfügbarkeit für den Einsatz in Journey veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).

  Verfügbarkeitsdatum: Dienstag, 16. März 2026

* **Pause- und Fortsetzungsdetails beim Journey technischer Details** - Die Journey **technischen Details** enthalten jetzt zusätzliche Informationen zu Pause und Wiederaufnahme: das Datum und die Uhrzeit der letzten Pause und Wiederaufnahme, den Anzeigenamen und die interne Kennung des Benutzers, der die jeweilige Aktion ausgeführt hat, sowie einen vollständigen Satz von Einstellungen für das pausierte Journey wie Pausenverhalten, die maximale Pausendauer und den Status der automatischen Wiederaufnahme. [Weitere Informationen](../building-journeys/journey-properties.md)

  Verfügbarkeitsdatum: Dienstag, 2. März 2026

#### Reporting

* **Bot-Klicks für E-Mail- und SMS-Reporting ausschließen** - Die E-Mail- und SMS-Berichterstellung filtert jetzt Bot-Klicks aus Klickmetriken automatisch heraus, bietet genauere Interaktionsdaten und verhindert, dass der automatisierte Traffic Ihre Leistungszahlen in die Höhe treibt.

* **Sendezeitoptimierung: Die Steuerelemente Speicherort der aktualisierten Steuerelemente und Neuer Aufstiegsbericht** - Sendezeitoptimierung (STO) wurden in das Menü Aktionskonfiguration verschoben. Darüber hinaus ist jetzt ein neuer Steigerungsbericht in den Journey-Berichten verfügbar, um die Auswirkungen von STOP auf Ihre Kampagnenleistungsmetriken zu messen.

#### E-Mail-Designer

* **Open-Time-Personalisierung mit Dynamic Media (Beta)** - Sie können jetzt E-Mail-Inhalte zur offenen Zeit mit Adobe Dynamic Media-Assets personalisieren, sodass empfängerspezifische Bilder und Visualisierungen in Echtzeit generiert werden, die dynamisch auf den Attributen der einzelnen Empfänger zum Zeitpunkt der E-Mail-Öffnung basieren. Diese Funktion befindet sich derzeit in Beta.

* **E-Mail-Designer in Unified Shell angezeigt** - Die E-Mail-Designer wird jetzt in Unified Shell angezeigt und bietet ein konsistentes Navigations- und Kopfzeilenerlebnis, das mit anderen Adobe-Programmen übereinstimmt.

* **Unterstützung des Textmodus in Fragmenten** - Fragmente unterstützen jetzt die Bearbeitung im Textmodus, sodass Sie Textversionen Ihrer Inhaltsfragmente zur Verwendung in textbasierten E-Mail-Workflows und Multi-Channel-Szenarien erstellen und verwalten können.

#### Entscheidungsfindung

* **Unterstützung des Ausdrucksfragmentverweis-Änderungs-Feeds in Edge Decisioning** - Diese Verbesserung ermöglicht es, Änderungen an Fragmentverweisen automatisch in allen Elementen widerzuspiegeln, die auf Fragmente verweisen, ohne etwas manuell aktualisieren zu müssen (erneute Veröffentlichung der Kampagne oder der Entscheidungsrichtlinie).

* **Optionale Fragmente in Entscheidungselementen** - Fragmente, die an Entscheidungselemente angehängt sind, können jetzt als optional konfiguriert werden, was eine größere Flexibilität bei der Inhaltskomposition bietet, wenn nicht alle Entscheidungselement-Renderings ein bestimmtes Fragment erfordern.

#### Konfiguration

* **URL-**: URL-Parameter in Tracking-Links und Landingpages können jetzt verschlüsselt werden, was eine zusätzliche Sicherheitsebene für vertrauliche Parameterdaten bietet. Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.

* **Ordner für Journey und Kampagnen** - Sie können Ihre Journey und Kampagnen jetzt in Ordnern organisieren, was eine strukturierte Navigation und eine einfachere Verwaltung für Teams ermöglicht, die mit großen Inhaltsmengen arbeiten. Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.

* **Änderung im Ereignisdatensatz für das Sekundäre Empfängerfeedback in AJO** - Der Ereignisdatensatz für das E-Mail-BCC-Feedback in AJO wird in den Ereignisdatensatz für das Sekundäre Empfängerfeedback in AJO umbenannt.
   * **Vorhandene Benutzer**: Nur der Anzeigename ändert sich. Der zugrunde liegende Tabellenname bleibt unverändert.
   * **Neue Benutzer und neue Sandboxes**: Sowohl der Anzeigename als auch der Tabellenname verwenden den neuen Namen.
   * **Vorhandene Benutzer/Organisationen mit neuen Sandboxes**: Sowohl der Anzeigename als auch der Tabellenname ändern sich in den neuen Namen.

  Verfügbarkeitsdatum: Dienstag, 2. März 2026

#### Orchestrierte Kampagnen

* **Globale Variablen in orchestrierten Kampagnen** - Orchestrierte Kampagnen unterstützen jetzt globale Variablen, die einmal definiert und über alle Aktivitäten innerhalb eines Workflows hinweg wiederverwendet werden können, um die Konfiguration zu vereinfachen und die Konsistenz von dynamischen Werten, Ausdrücken und der Personalisierung von Inhalten sicherzustellen.

* **Vereinfachung der Zielgruppendimension in orchestrierten Kampagnen** - Sie können jetzt die richtigen Zielgruppendimensionen und sekundären Dimensionen in orchestrierten Kampagnen einfach auswählen oder automatisch ableiten, um eine genaue, effiziente Zielgruppenaktivierung zu ermöglichen.

## Versionshinweise Februar 2026 {#feb-26-01-rn}

Die Abschnitte [Neue Funktionen](#feb-26-01-features) und [Verbesserungen](#feb-26-01-improv) decken bereits verfügbare Funktionen ab. Der [Demnächst](#coming-soon) Abschnitt enthält Funktionen und Verbesserungen, die im Februar veröffentlicht werden sollen.

<!--**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

<!--**Release date**: February 17-18, 2026-->

### Neue Funktionen {#feb-26-01-features}


<table>
<thead>
<tr>
<th><strong>Journey-Schlichtung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt <strong>Rangfolgeformeln</strong> verwenden, um die Journey-Prioritätswerte basierend auf Kundenprofilattributen und Kontextfaktoren automatisch zu erhöhen, sodass Kundinnen und Kunden in die relevantesten Journey gelangen.</p>
<p><img src="assets/do-not-localize/journey-arbitration-formulas.gif"/></p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p>Weitere Informationen finden Sie in der <a href="../conflict-prioritization/journey-ranking-formulas.md">ausführlichen Dokumentation</a>.</p>
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
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/journey-action.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Samstag, 20. Februar 2026</p>
<p><strong>Hinweis:</strong> Alle nativen Kanäle sind jetzt über die Aktion-Journey-Aktivität zugänglich. Ältere native Kanalaktivitäten werden mit der März-Version eingestellt. Vorhandene Journey mit Legacy-Aktionen funktionieren weiterhin wie bisher - es ist keine Migration erforderlich.</p>
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
<p>Sie können jetzt einen Zeitplan für Nachrichten aus Journey Optimizer-Kampagnen oder Journeys festlegen, die im Laufe der Zeit in kontrollierten Batches versendet werden.</p>
<p>Der Wave-Versand bietet die folgenden Vorteile:</p>
<ul>
<li>Bessere Zustellbarkeit: Spread sendet im Laufe der Zeit, um einen guten Ruf als Absender zu wahren und das Risiko zu reduzieren, als Spam gekennzeichnet zu werden.</li>
<li>Laststeuerung - Vermeiden Sie die Überlastung nachgelagerter Systeme (z. B. Callcenter, Landingpages), indem Sie einschränken, wie viele Nachrichten gleichzeitig gesendet werden.</li>
<li>Anwendungsfälle mit hohem Volumen und zeitkritischer Relevanz - geeignet für große Zielgruppen oder zur Steuerung des Timings (z. B. Call-Center-Kapazität, Anlaufphase oder zeitlich begrenzte Angebote).</li>
</ul>
<p><img src="assets/do-not-localize/waves.gif"/></p>
<p>In <strong>Kampagnen</strong> ist diese Funktion für alle Umgebungen verfügbar (allgemeine Verfügbarkeit). Weitere Informationen finden Sie in der <a href="../campaigns/send-using-waves.md">ausführlichen Dokumentation</a>.</p>

<p>In <strong>Journey</strong> ist diese Funktion nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff zu erhalten. Weitere Informationen finden Sie in der <a href="../building-journeys/send-using-waves.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Freitag, 19. Februar 2026</p>
</td>
</tr>
</tbody>
</table>

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

<table>
<thead>
<tr>
<th><strong>APIs für Self-Service-Migrations-Tools</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Migrations-Tool-APIs sind jetzt verfügbar, um <strong> (Entscheidungs-Management)-</strong> programmgesteuert nach <strong>Decisioning</strong> zu migrieren, mit:</p>
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
<p>Vertiefen Sie insight in den Zustand und die Leistung Ihrer benutzerdefinierten Aktionsendpunkte mit einem neuen Überwachungs-Dashboard und angereicherten Journey-Schritt-Ereignisdaten. Verfolgen Sie erfolgreiche Aufrufe, Fehler, Durchsatz, Antwortzeiten und Warteschlangenwartezeiten nach, um schnell zu erkennen, wann, wo und warum Anomalien auftreten.</p>
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
<p>Sie können jetzt den Inhalt Ihrer SMS-Nachrichten mit Decisioning personalisieren und optimieren. Verwenden Sie Prioritätswerte, Formeln oder KI-Modelle, um Ihren Kundinnen und Kunden den besten Inhalt anzuzeigen.</p>
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

#### Content-Management

<!--
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors</strong> section defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity. [Read more](../content-management/brands.md)
-->

* **Verwenden von Designs zum Konvertieren von Bildern in E-Mail-Vorlagen** - Beim Konvertieren eines Bildes in eine E-Mail-Vorlage in Journey Optimizer können Sie jetzt ein Design als Eingabe verwenden, sodass die generierte HTML Ihren Markenparametern entspricht. Stile wie Hintergrundfarbe, Schaltflächenfarbe, Schriftarten, Zeilenabstand, Ränder und Abstand werden automatisch angewendet, wodurch die manuelle Entwurfsarbeit reduziert wird und eine Vorlage bereitgestellt wird, die mit minimalen Bearbeitungen verwendet werden kann. [Weitere Informationen](../content-management/image-to-html.md)

  Verfügbarkeit: 17. Februar 2026.

<!--* **Text mode for fragments** - You can now create and manage text versions of your fragments, supporting workflows that rely on plain text content and providing the same flexibility as in email content. [Read more](../content-management/create-fragments.md)-->

#### E-Mail-Designer

* **Texteinzug** - Sie können jetzt eine anpassbare linke Einrückung auf die erste Zeile von Absätzen in Textkomponenten direkt über das Eigenschaftenbedienfeld anwenden. <!--The new **Indentation** control lets you define indentation in pixels or percentage via a numeric input or slider, with live preview on the canvas. -->Dies verbessert die Lesbarkeit von Langforminhalten wie Leitartikeln und Artikeln. [Weitere Informationen](../email/get-started-email-style.md)

  Verfügbarkeit: 18. Februar 2026.

#### Entscheidungsfindung

* **Eingehende Edge-Unterstützung für die Verwendung von Adobe Experience Platform-Daten in Decisioning** - Die Verwendung von Adobe Experience Platform-Daten in Decisioning unterstützt jetzt eingehende Edge-Anwendungsfälle zusätzlich zu E-Mail und benutzerdefinierten Aktionen in Journey. [Weitere Informationen](../experience-decisioning/aep-data-exd.md)

  Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.


* **Anhängen von Fragmenten an Entscheidungselemente** – Journey Optimizer bietet jetzt die Möglichkeit, Fragmente an Entscheidungselemente anzuhängen, die in Code-basierten Erlebniskampagnen über Entscheidungsrichtlinien genutzt werden können. [Weitere Informationen](../experience-decisioning/fragments-decision-policies.md)

  Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).

  Verfügbarkeit: 12. Februar 2026.

#### Personalisierung

* **Execution Metadata Helper** - Die Hilfsfunktion `executionMetadata` ist jetzt für alle Journey Optimizer-Kunden verfügbar. Verwenden Sie diese Option, um kontextuelle Informationen dynamisch an eine native Aktion anzuhängen und in einem Datensatz zu erfassen, damit sie in externe Systeme exportiert werden können. [Weitere Informationen](../personalization/functions/helpers.md#execution-metadata)

  Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).

  Verfügbarkeit: 20. Februar 2026.

#### SMS

* **SMS-Webhooks** - Webhooks werden jetzt von allen SMS-Anbietern unterstützt. Sie können jeden Webhook für einen bestimmten Zweck konfigurieren: eingehende Webhooks zur Erfassung eingehender Nachrichten und Feedback-Webhooks für den Empfang von Versandbestätigungen, Statusaktualisierungen und anderen nachrichtenbezogenen Ereignissen. [Weitere Informationen](../sms/sms-webhook.md)

  Verfügbarkeit: 2. Februar 2026.

<!--## Coming soon {#coming-soon}

The features and improvements below are planned for release later in February. Release dates and scope may change without prior notice.

### Improvements {#coming-soon-improv}

* **Decisioning preview in Code-based Experience channel** - You can now preview decision items when configuring Decisioning with the Code-based Experience channel. Preview is available directly in the authoring interface before going live.

  Availability date: February 18, 2026
-->

