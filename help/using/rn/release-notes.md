---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: f274d56a19ccc21b04452b2bca2b17e07159d819
workflow-type: tm+mt
source-wordcount: '2067'
ht-degree: 20%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** liefert kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] folgt einem kontinuierlichen Bereitstellungsmodell, sodass Adobe kontinuierlich neue Funktionen, Verbesserungen und Fehlerbehebungen bereitstellen kann. Dieser Ansatz ermöglicht ein skalierbares Rollout von Funktionen in Phasen, um die Leistung und Stabilität aller Umgebungen sicherzustellen.

Aufgrund dieses Modells werden die Versionshinweise zwischen den monatlichen Versionen aktualisiert. Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Versionshinweise April &#39;26 {#april-26-rn}

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

Neue Funktionen und Verbesserungen, die Anfang April veröffentlicht wurden, werden mit ihrem Verfügbarkeitsdatum angekündigt.

**Veröffentlichungsdatum**: 28. bis 29. April 2026

### Neue Funktionen {#april-26-features}

<table>
<thead>
<tr>
<th><strong>Integrationen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit <b> Funktion </b>Integrationen“ können Sie Datenquellen von Drittanbietern direkt mit Adobe Journey Optimizer verbinden. Diese Funktion vereinfacht das Einlesen externer Daten und <b>zusammenstellbarer Inhalte</b> und erleichtert so die Bereitstellung personalisierter, dynamischer Nachrichten auf allen Kanälen.</p>
<p>Diese Funktion wurde zuvor als Beta-Version veröffentlicht, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../integrations/integrations.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 4. Mai 2026</p>
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
<p><strong>Orchestrierte Kampagnen</strong> unterstützen jetzt eine Aktivität vom Typ <strong>Inkrementelle Abfrage</strong>, die nur auf Profile oder Ereignisse abzielt, die seit der letzten Ausführung neu qualifiziert wurden.

Dadurch bleiben wiederkehrende Kampagnen auf neue Zielgruppen ausgerichtet (neue Anmeldungen, neu qualifizierte Mitglieder des Treueprogramms und ähnliche Segmente), während die Abfrage-Workloads reduziert und redundante Sendungen im Laufe der Zeit vermieden werden.</p>
<p>Weitere Informationen finden Sie in der <a href="../orchestrated/activities/incremental-query.md#incremental-query-configuration">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Absenderparameter im E-Mail-Header</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Journey Optimizer können Sie jetzt E-Mails senden, bei denen sich die sendende Entität (Absender) von der Authoring-Entität (Von) unterscheidet. E-Mail-Clients, die dies unterstützen, rendern es normalerweise als „Absender im Namen von Von“ oder zeigen einen „Über“-Indikator an. Füllen Sie die optionalen Felder <strong>Absender-Kopfzeilen</strong> in den Einstellungen des E-Mail-Kanals aus, um diese Funktion zu konfigurieren.</p>
<p><img src="assets/do-not-localize/sender-headers.gif"></p>
<p>Weitere Informationen finden Sie in der <a href="../email/header-parameters.md#sender-header">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>CC-Feld in E-Mail-Kanaleinstellungen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Jetzt können Sie in Ihren E-Mail-Kanaleinstellungen ein optionales CC-Feld (Carbon Copy) konfigurieren. Im Gegensatz zu BCC sind CC-Empfänger für den primären Empfänger sichtbar, was eine transparente Kommunikation und eine klarere Eigentümerschaft ermöglicht.</p>
<p>Auf diese Weise können Sie automatisch den richtigen Stakeholder für jede Nachricht kopieren - z. B. einen Beziehungs-Manager oder einen Kontoinhaber - und gleichzeitig sicherstellen, dass der Kunde weiß, an wen er sich zwecks Folgenachricht wenden muss.</p>
<p>Das CC-Feld unterstützt Personalisierung, sodass eine einzelne Konfiguration Kopien basierend auf Profildaten dynamisch weiterleiten kann, sodass sie ohne zusätzliche Einrichtung für mehrere Anwendungsfälle skalierbar ist.</p>
<p><img src="../configuration/assets/email-config-cc.png"></p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/cc-email-field.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Kopieren orchestrierter Kampagnen in Sandboxes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Sandbox-Tools unterstützen jetzt das Verpacken und Kopieren orchestrierter Kampagnen von einer Sandbox in eine andere. Dadurch entfällt die Notwendigkeit, Kampagnen in jeder Umgebung manuell neu zu erstellen. Wenn eine Kampagne in einem Package zusammengefasst wird, werden ihre abhängigen Kernobjekte wie Zusammenführungsrichtlinien und Nachrichten automatisch einbezogen, sodass die importierte Kampagne bereit für die Konfiguration und Validierung ist. Zum Schutz der Produktionsumgebungen landen alle importierten Kampagnen im Entwurfsstatus in der Ziel-Sandbox, sodass Teams vor der Live-Schaltung einer Kampagne einen Prüfungs- und Genehmigungsschritt erhalten.</p>
<p><img src="assets/do-not-localize/oc-sandbox.gif"></p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/copy-objects-to-sandbox.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Optimizer AI Agent-Integration über MCP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer bietet jetzt einen <strong>MCP (Model Context Protocol)-Server</strong> der Kampagnen-, Kanalkonfigurations- und Sandbox-Vorgänge direkt in jeder MCP-kompatiblen Anwendung aufbereitet. Mit dieser Integration können verschiedene Personas um dieselben Orchestrierungsdaten herum zusammenarbeiten. Anstatt Abfragen für die Adobe Journey Optimizer-REST-API zu schreiben oder durch mehrere Bildschirme der Benutzeroberfläche zu navigieren, können Sie Ihre Absicht im Gespräch beschreiben und das LLM die entsprechenden MCP-Tools aufrufen lassen. Diese Funktion ist derzeit in Claude Web und Desktop verfügbar.</p>
<p>Diese Funktion steht allen Kunden in Public Beta zur Verfügung.</p>
<p>Weitere Informationen finden Sie in der <a href="../integrations/ajo-mcp.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Schlichtung - KI-Modelle</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt <strong>KI-Modelle</strong> in Ihren Rangfolgeformeln verwenden, um die Journey-Prioritätswerte basierend auf Kundenprofilattributen und Kontextfaktoren automatisch zu erhöhen, sodass Kundinnen und Kunden die relevantesten Journey eingeben.</p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p><img src="assets/do-not-localize/journey-arbitration-ai-models.gif"></p>
<p>Weitere Informationen finden Sie in der <a href="../conflict-prioritization/journey-ai-models.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Express-Integration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Durch die <b>Adobe Express-Integration</b> in Adobe Journey Optimizer können Sie die Bearbeitungs-Tools von Adobe Express direkt während der Inhaltserstellung verwenden, sodass Sie die Größe ändern, Hintergründe entfernen, Assets zuschneiden und in JPEG oder PNG konvertieren können.
</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><img src="assets/do-not-localize/express_resize.gif"></p>
<p>Weitere Informationen finden Sie in der <a href="../integrations/express.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 23. April 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>E-Mail für KI-Posteingänge optimieren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer bietet jetzt eine neue Funktion, mit der sichergestellt wird, dass Ihre E-Mails für KI-gestützte Posteingänge wie Apple Intelligence und Google Gemini in Gmail optimal strukturiert sind.</p>
<p>Da KI-Assistenten zunehmend steuern, wie Empfängerinnen und Empfänger E-Mails lesen und darauf reagieren, hilft Ihnen diese Funktion bei der Erstellung und Erstellung von Inhalten, die in nachgelagerten KI-Aufgaben, einschließlich Zusammenfassung, Klassifizierung, Priorisierung und Extraktion von Absichten, gut funktionieren.</p>
<p><img src="assets/do-not-localize/optimize-for-ai.gif"></p>
<p>Weitere Informationen finden Sie unter <a href="../email/llm-email-optimizer.md">E-Mail für KI-Posteingänge optimieren</a>.</p>
<p>Verfügbarkeitsdatum: 17. April 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>KI-Assistent für Personalization Expressions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] enthält jetzt <strong>KI-Assistent</strong> direkt im Personalisierungseditor und die E-Mail-Designer, die Eingabeaufforderungen in natürliche Sprachen in gültige Personalisierungsausdrücke und bedingte Logik umwandelt, sodass kein Syntaxwissen erforderlich ist. Beschreiben Sie die Personalisierung, die Sie erreichen möchten, und KI generiert einsatzbereiten Code, den Sie sofort anwenden oder durch Folgeaufforderungen verfeinern können.</p>
<p>Der Assistent arbeitet auch rückwärts. Wählen Sie einen vorhandenen Ausdruck aus und bitten Sie ihn, die Logik zu erklären, Probleme zu identifizieren oder Verbesserungen vorzuschlagen. Dies ist nicht nur für das Erstellen neuer Ausdrücke nützlich, sondern auch für die Überprüfung und das Debugging vorhandener Ausdrücke in Ihrem Team.</p>
<p><img src="assets/do-not-localize/assistant-perso.gif"></p>
<p>Weitere Informationen finden Sie unter <a href="../content-management/generative-personalization-expressions.md">KI-Assistent für Personalization-Ausdrücke</a>.</p>
<p>Verfügbarkeitsdatum: 13. April 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Pfadexperiment</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verwenden Sie den neuen <strong>Optimieren</strong>-Knoten, um A/B-Tests oder Multi-Armed-Bandit-Experimente durchzuführen, um den besten Pfad zur Erfüllung Ihrer geschäftsorientierten KPIs zu ermitteln. Mit diesem Tool können Sie Kommunikation, Sequenzierung und Timing testen und variieren sowie anpassen, um Ihre Kundschaft optimal zu erreichen.
</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Als Teil der allgemeinen Verfügbarkeit führt diese Version die Auswahl <strong>Experimenttyp</strong> (A/B oder mehrarmiger Bandit) und <strong>Gewinner skalieren</strong> für einheitliche Journey ein.</p>
<p><img src="assets/do-not-localize/optimize-experiment.gif"></p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/path-experimentation.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 7. April 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Posteingang</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Posteingang</strong> ist eine Funktion für Mobilgeräte, die mit Inhaltskarten verfügbar ist und es Kunden ermöglicht, einen zentralen Ort in ihrer App oder Website zu erstellen, um Nachrichten anzuzeigen, die an ihre Benutzer gesendet werden. Dies verlängert die Lebensdauer der Marketing-Kommunikation, indem sichergestellt wird, dass Nachrichten auch nach ihrer Beendigung zugänglich bleiben.</p>
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../inbox/inbox-gs.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 7. April 2026</p>
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
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit). Mit dieser Version zur allgemeinen Verfügbarkeit werden nun Mirrorseiten unterstützt.</p>
<p><img src="assets/do-not-localize/exd-email.gif"></p>
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/create-decision-policy.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 6. April 2026</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#april-26-improv}

#### KI

<!--
* **Brand alignment score in Campaign dashboard** - You can now assess your brand alignment score directly within your Campaign dashboard to ensure content stays on-brand. This allows you to verify guidelines at a glance without having to open the content designer.
-->

* **Verbesserung des Eingabeaufforderungsassistenten** - Der Eingabeaufforderungsassistent verbessert die KI-Inhaltserstellung, indem er Benutzeraufforderungen in Echtzeit analysiert und Lücken in Klarheit, Vollständigkeit und Kontext erkennt. Es schlägt verbesserte Neuschreibungen vor und bietet praktische Anleitungen, um Eingabeaufforderungen mit wichtigen Details wie Zielgruppe, Ton und Absicht anzureichern. Die Funktion stellt außerdem gezielte Fragen, um Benutzenden zu helfen, ihre Eingaben vor der Generierung zu verfeinern. Dies führt zu genaueren, hochwertigeren Ausgaben mit weniger Iterationen. [Weitere Informationen](../content-management/ai-assistant-prompting-guide.md#prompt-assistant)

  Verfügbarkeitsdatum: 5. Mai 2026

#### Push-Benachrichtigung

* **App-ID in Kanaleinstellungen personalisieren** - In den Konfigurationseinstellungen für den Push-Kanal können Sie jetzt das Feld **App-ID** personalisieren, damit jeder Empfänger anhand seiner Profilinformationen eine Push-Benachrichtigung von der entsprechenden Marke erhalten kann. [Weitere Informationen](../push/push-configuration.md#app-id-personalization)

#### Entscheidungsfindung

* **Fragmente an Entscheidungselemente anhängen** - Journey Optimizer bietet jetzt die Möglichkeit, Fragmente an Entscheidungselemente anzuhängen, die über Entscheidungsrichtlinien in Code-basierten Erlebnis- und E-Mail-Kampagnen genutzt werden können. [Weitere Informationen](../experience-decisioning/fragments-decision-policies.md)

  Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).

* **Vorübergehend nicht verfügbare Fragmente werden übersprungen** - Bei der Verwendung von Fragmenten in Entscheidungselementen wird ein Fragment übersprungen, wenn es vorübergehend in Edge nicht verfügbar ist, und die Journey oder Kampagne wird weiter gerendert, anstatt fehlzuschlagen. [Weitere Informationen](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  Verfügbarkeitsdatum: 14. April 2026

<!--
#### SMS

* **Character Count** - In Adobe Journey Optimizer, you can now use the Character Count to monitor the length of your SMS messages in real time. It helps you see when a message will be split into multiple segments to better manage formatting and avoid unexpected increases in sending costs. [Read more](../sms/create-sms.md)

* **Opt-out and consent at phone number and sender** - For SMS, Journey Optimizer now records marketing consent and opt-out at the level of both the profile's phone number and short code. 

  This capability is currently only available for Sinch SMS configurations. [Read more](../sms/sms-configuration-sinch.md)

* **SMS inbounds to a custom dataset** - In **SMS API credentials**, route **inbound SMS** to a **custom, profile-enabled Experience Event dataset** you select instead of only the default tracking dataset. [Read more](../sms/sms-webhook.md)

* **Webhook interface enhancement** - When configuring SMS webhooks, the user interface now includes a built-in setup guide with practical examples, making it easier to align provider payloads and troubleshoot issues without leaving the configuration flow. [Read more](../sms/sms-webhook.md)

#### WhatsApp

* **WhatsApp interactive buttons and tracking** - WhatsApp in Journey Optimizer now supports interactive buttons required by your templates and use cases, along with built-in interaction tracking so you can measure engagement and analyze performance alongside your other channel reporting.
-->

#### Adobe Experience Manager-Integrationen

* **Unterstützung von Adobe Experience Manager-Inhaltsfragmentvarianten** - Sie können beim Einfügen von Adobe Experience Manager **Inhaltsfragmenten „Inhaltsfragmentvarianten“** (z. B. Sprach- oder Kanalvarianten) auswählen, um die Handhabung für Gebietsschema- und mehrsprachige Szenarien zu verbessern. [Weitere Informationen](../integrations/aem-fragments.md#aem-variations)

  Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).

* **Adobe Experience Manager-Inhaltsfragmentkontext beim Authoring** - Ihre Inhaltsfragmentauswahl bleibt beim Wechseln zwischen Textfeldern und Inhaltsblöcken aktiv, sodass Sie weitere Fragmentfelder hinzufügen können, ohne **AEM Content Advisor** erneut zu öffnen. [Weitere Informationen](../integrations/aem-fragments.md)

  Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).

#### E-Mail-Design

* **Erweiterter HTML-Editor für E-Mail** - Im erweiterten HTML-Modus können Sie die HTML-Quelle Ihres Inhalts in der E-Mail-Designer bearbeiten, erweiterte Ausdrücke (wie Bedingungen) in der Quelle hinzufügen und zwischen HTML- und Desktop-Ansicht wechseln, ohne Ihre Änderungen zu verlieren.

  Diese Funktion war bisher nur für E-Mail-Inhaltsvorlagen verfügbar und wird jetzt zusätzlich zu E-Mail **Inhaltsvorlagen für E-Mail-**-Inhalte in der E-Mail-Designer bereitgestellt (z. B. E-Mails, die in Journey und Kampagnen verfasst wurden). Sie ist derzeit nur eingeschränkt verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugang zu erhalten. [Weitere Informationen](../email/email-expert-mode.md)

  Verfügbarkeitsdatum: 9. April 2026

#### Journey-Pfadoptimierung

* **Experimenttyp** - Bei der Konfiguration eines Pfadexperiments können Sie jetzt zwischen A/B-Experiment (feste Aufspaltung am Beginn) oder Mehrarmiger Bandit (automatische Aufspaltung mit wöchentlichen Aktualisierungen der Gewichtung) wählen. [Weitere Informationen](../building-journeys/path-experimentation.md)

  Verfügbarkeitsdatum: 7. April 2026

* **Pfadexperiment: Skalieren Sie den Gewinner** - Sie können jetzt automatisch oder manuell den Gewinnpfad eines Experiments für Ihre gesamte Zielgruppe einführen. Sobald ein Gewinner ermittelt wurde, können Sie seine Reichweite und Effektivität steigern, ohne das Experiment ständig zu überwachen. [Weitere Informationen](../building-journeys/path-experimentation.md#scale-winner)

  Diese Funktion ist nur in unitären Journey verfügbar (ereignisausgelöst und Zielgruppenqualifikationen). Sie ist nicht für Journey unter Zielgruppe lesen verfügbar.

  Verfügbarkeitsdatum: 7. April 2026

* **Bedingungen** - Die Aktivität [Optimieren](../building-journeys/optimize.md) ist das neue Vehikel zum Erstellen bedingter Pfade in Journey. Sie ersetzt die frühere Aktivität **Bedingung**, die aus der Benutzeroberfläche entfernt wurde. Die gesamte bedingte Logik wird beibehalten und jetzt über die Bedingungen **Aktivität** Optimieren) verarbeitet. [Weitere Informationen](../building-journeys/conditions.md)

  Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).

  Verfügbarkeitsdatum: 7. April 2026

#### Orchestrierte Kampagnen

* **Globale Variablen in orchestrierten Kampagnen** - Orchestrierte Kampagnen unterstützen jetzt globale Variablen, die einmal definiert und über alle Aktivitäten innerhalb eines Workflows hinweg wiederverwendet werden können, um die Konfiguration zu vereinfachen und die Konsistenz von dynamischen Werten, Ausdrücken und der Personalisierung von Inhalten sicherzustellen. [Weitere Informationen](../orchestrated/global-variables.md)
* **Verbesserungen bei Data Modeler** - Orchestrierte relationale Schemata unterstützen jetzt zusammengesetzte Schlüssel, die mehrere Felder umfassen. Das Laden eines Schemas aus einer DDL-Datei führt auch zu Auflistungen, und beim Laden aus einer DDL- oder Excel-Datei werden automatisch zusammengesetzte Beziehungen zwischen Tabellen erstellt. In der Ansicht der Entitätsbeziehung zeigen zusammengesetzte Links jetzt den vollständigen Satz von Feldpaaren zwischen Tabellen an, nachdem eine Datei hochgeladen wurde. [Weitere Informationen](../orchestrated/gs-schemas.md)

## Demnächst {#coming-soon}

Die Veröffentlichung der folgenden Funktionen und Verbesserungen ist für die nächsten Tage geplant. **Informationen können Änderungen unterliegen**. Aktualisierte Links, Bildschirme und Dokumentationen werden freigegeben, sobald diese Aktualisierungen live in der Produktion verfügbar sind.

### Neue Funktionen {#comming-soon-features}

<table>
<thead>
<tr>
<th><strong>Journey-Simulation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Jetzt können Sie Ihren Journey auf <strong>Simulation</strong> einstellen. In diesem Modus können Sie Ihre Logik mithilfe von <strong>simulierten Benutzern</strong> überprüfen. Hierbei handelt es sich um temporäre Profile, die speziell für die Simulation erstellt wurden. Sie können also frei testen, ohne persistente Testprofile in Adobe Experience Platform verwalten zu müssen.</p>
<p>Diese Funktion steht allen Kunden als eingeschränkte Verfügbarkeit mit wichtigen Funktionen zur Verfügung.</p>
<!--p><img src="assets/do-not-localize/simulate-user.gif"></p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Deeplinks in der E-Mail-Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Es ist jetzt möglich, über eine dedizierte Option in der E-Mail-Designer Deeplinks zu Ihren E-Mail-Inhalten hinzuzufügen.</p><p>Dadurch wird sichergestellt, dass Benutzende direkt zu den richtigen In-App-Inhalten geleitet werden, anstatt zu Browsern oder App-Stores weitergeleitet zu werden, wodurch der Kontext und die Interaktion erhalten bleiben.</p>
<!--<p><img src="assets/do-not-localize/forms.gif"></p>-->
<p>Weitere Informationen finden Sie in der <a href="../email/message-tracking.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 7. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

