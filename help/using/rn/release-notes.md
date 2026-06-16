---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 02ce60020012083981c5599789b9e86804190627
workflow-type: tm+mt
source-wordcount: 3006
ht-degree: 86%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** stellt regelmäßig neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen zur Verfügung. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] verwendet ein kontinuierliches Bereitstellungsmodell, das es Adobe ermöglicht, laufend neue Funktionen, Verbesserungen und Fehlerbehebungen bereitzustellen. Dieser Ansatz ermöglicht ein skalierbares Rollout von Funktionen in Phasen, um die Leistung und Stabilität aller Umgebungen sicherzustellen. Aufgrund dieses Modells werden die Versionshinweise zwischen den monatlichen Versionen aktualisiert. Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

>[!NOTE]
>
>Die in diesen Versionshinweisen aufgeführten Funktionen umfassen ein **Verfügbarkeitsdatum**, das angibt, wann jede Änderung in Ihrer Umgebung verfügbar wird. Einträge in den Akkordeons **Demnächst verfügbar** werden in den kommenden Tagen oder Wochen erwartet. Informationen in diesen Abschnitten können Änderungen unterliegen.


## Updates vom 26. Juni {#june-26-updates}

<table>
<thead>
<tr>
<th><strong>Journey-Simulation (allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Jetzt können Sie Ihren Journey auf Simulation einstellen. In diesem Modus können Sie Ihre Logik mithilfe simulierter Benutzer überprüfen. Dies sind temporäre, speziell für die Simulation erstellte Profile, mit denen Sie frei testen können. So müssen Sie keine dauerhaften Testprofile in Adobe Experience Platform verwalten. </p>
<p>Journey-Simulation wurde zuvor mit eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung. Mit dieser allgemeinen Verfügbarkeit können Sie jetzt Journey Agent verwenden, um simulierte Benutzende und Ereignisse direkt im Simulationsmenü zu generieren.</p>
<p><img src="assets/do-not-localize/journey-simulation.gif"></p>
<p>Weitere Informationen finden Sie im <a href="../building-journeys/simulate-journey-gs.md">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 9. Juni 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Pfadoptimierung - Targeting (allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die <strong>Optimierungsaktivität</strong> unterstützt jetzt <strong>Targeting-Regeln</strong> mit denen Sie spezifische Kriterien definieren können, die Kundinnen und Kunden erfüllen müssen, um sich basierend auf Zielgruppensegmenten oder Profilattributen für einen bestimmten Journey-Pfad zu qualifizieren.</p>
<p>Im Gegensatz zu Experimenten, bei denen Kundinnen und Kunden nach dem Zufallsprinzip Pfaden zugewiesen werden, verwendet das Targeting deterministische Logik, um sicherzustellen, dass die entsprechende Zielgruppe oder das entsprechende Kundenprofil zum gewünschten Pfad weitergeleitet wird.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><img src="assets/do-not-localize/optimize.gif"></p>
<p>Weitere Informationen finden Sie im <a href="../building-journeys/path-targeting.md">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 8. Juni 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Fragments (allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt <strong>Journey-Fragmente</strong> in Adobe Journey Optimizer erstellen. Journey-Fragmente sind wiederverwendbare Sätze von Journey-Knoten, die Sie einmal erstellen und in einer beliebigen Journey in Ihrer Sandbox ablegen können. Unabhängig davon, ob es sich um eine Eignungsprüfung, eine bevorzugte Kanal-Routing-Logik oder eine Begrüßungssequenz handelt, helfen Fragmente Teams dabei, schneller und konsistent zu arbeiten, ohne dieselbe Logik jedes Mal von Grund auf neu zu erstellen.</p>
<p>Nach der Erstellung werden Fragmente in einem dedizierten <strong>Fragmentinventar</strong> gespeichert und können mithilfe der Aktivität <strong>Journey-Fragmente</strong> in Journeys eingefügt werden.</p>
<p>Diese Funktion war bisher nur in begrenzter Verfügbarkeit verfügbar und steht nun allgemein allen Kunden zur Verfügung. Journey-Fragmente unterstützen auch <strong>Sandbox-Tools</strong> mit denen Sie Fragmente über Sandboxes hinweg verpacken und exportieren können.</p>
<p>Weitere Informationen finden Sie im <a href="../building-journeys/journey-fragments.md">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 9. Juni 2026</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Simulieren von Inhaltsvarianten - Generieren aktualisierter Erlebnisse und KI-Varianten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Für den Workflow <strong>Inhalt simulieren“ sind jetzt zwei </strong> verfügbar:</p>
<ul>
<li><strong>Neuer Standardpfad</strong> - Wenn Sie auf <strong>Inhalt simulieren</strong> klicken, wird jetzt <strong> Erlebnis „Inhaltsvarianten simulieren</strong> geöffnet. Sie können auf einem einzigen Bildschirm Beispieleingaben manuell oder aus einer CSV-/JSON-Datei hinzufügen, simulierte Benutzer wiederverwenden, das Rendering in der Vorschau anzeigen und Testsendungen durchführen. Um eine Vorschau mit Adobe Experience Platform-Testprofilen anzuzeigen, Testsendungen mit Testprofildaten durchzuführen oder E-Mail-Posteingang - Rendering und Spam-Berichte zu überprüfen, klicken Sie auf <strong>Inhalt simulieren</strong> und wählen Sie dann <strong>Inhalt simulieren (AEP-Profile)</strong> aus der Dropdown-Liste aus.</li>
<li><strong>KI-generierte Inhaltsvarianten</strong> - Klicken Sie im Erlebnis <strong>Inhaltsvarianten simulieren</strong> auf <strong>Generieren</strong>, um KI zum automatischen Erstellen von Inhaltsvarianten zu verwenden. Das System analysiert Ihre Nachricht, erkennt Personalisierungsfelder und bedingte Verzweigungen und füllt realistische Werte aus, sodass Sie das Rendering überprüfen können, ohne jede Variante von Hand erstellen zu müssen.</li>
</ul>
<p>Weitere Informationen finden Sie im <a href="../test-approve/simulate-sample-input.md">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 9. Juni 2026</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Unterstützung von Entscheidungen im Direkt-Mail-Kanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Entscheidungsrichtlinien zu Direkt-Mail-Journeys und -Kampagnen hinzufügen. Entscheidungsrichtlinien sind Container für Angebote, die die Entscheidungs-Engine nutzen, um für jedes Zielgruppenmitglied die besten Inhalte bereitzustellen. Die Direkt-Mail-Entscheidungsfindung unterstützt auch Anwendungsfälle für Batch-Entscheidungen, mit denen Sie die entsprechenden Angebotselemente für jedes Profil in einer bestimmten Adobe Experience Platform-Zielgruppe exportieren können. </p>
<p><img src="assets/do-not-localize/exd-dm.gif"></p>
<p>Weitere Informationen finden Sie im <a href="../experience-decisioning/use-decision-policy.md">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 3. Juni 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>KI-Assistent für Journey-Ausdrücke (öffentliche Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der KI-Assistent arbeitet jetzt im erweiterten Ausdruckseditor von Journeys, um Prompts in natürlicher Sprache in gültige Ausdrücke und Bedingungslogik zu konvertieren. Beschreiben Sie die gewünschte Personalisierung und die KI generiert einsatzbereiten Code, den Sie sofort anwenden oder durch Folge-Prompts verfeinern können.</p>
<p>Diese Funktion steht allen Kundinnen und Kunden als öffentliche Beta-Version zur Verfügung.</p>
<p><img src="assets/do-not-localize/expression-assistant.gif"></p>
<p>Weitere Informationen finden Sie im <a href="../building-journeys/expression/expression-agent.md">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 3. Juni 2026</p> 
</td>
</tr>
</tbody>
</table>

* [!BADGE Wichtig]{type=Informative} **AJO-Nachrichten-Feedback-Ereignisdatensatz, der zur Batch-Aufnahme** wird - Der **AJO-Nachrichten-Feedback-** Ereignisdatensatz) wechselt von der Streaming-Aufnahme zur Batch-Aufnahme. Erwarten Sie daher für diesen Datensatz eine Datenlatenz von bis zu 2 Stunden. Wenn Sie Berichte in Customer Journey Analytics erstellt haben oder Abfragen mithilfe dieses Datensatzes ausführen, berücksichtigen Sie in Zukunft diese erhöhte Latenz. [Weitere Informationen](../data/datasets-query-examples.md#message-feedback-event-dataset)

  Verfügbarkeitsdatum: 10. Juni 2026

* **Automatischer Stopp für nicht wiederkehrende Journey des Typs „Zielgruppe lesen** - Nicht wiederkehrende **Zielgruppe lesen** Journey wechseln jetzt automatisch in den Status **Angehalten**, sobald das letzte aktive Profil beendet wurde. Zuvor blieben diese Journeys bis zum Ablauf der 91-tägigen globalen maximalen Wartezeit **live**, selbst wenn sie nicht mehr von Profilen durchlaufen wurden. Mit dieser Verbesserung spiegelt der Journey-Status den tatsächlichen Ausführungsstatus nach Abschluss wider, sodass der Journey-Bestand ohne manuelles Eingreifen stets korrekt ist.

  Beachten Sie, dass dieses Verhalten nicht für Journeys mit Knoten gilt, die Wartezeiten verursachen, z. B. Warteknoten, Reaktionsknoten oder durch Ereignisse ausgelöste Transitionen. Diese Journeys unterliegen weiterhin dem standardmäßigen globalen Timeout von 91 Tagen. [Weitere Informationen](../building-journeys/end-journey.md#auto-stop-non-recurring)

  Verfügbarkeitsdatum: 9. Juni 2026

* **Zertifikatbasierte benutzerdefinierte Authentifizierung in benutzerdefinierten Aktionen** – Benutzerdefinierte Aktionen unterstützen jetzt die zertifikatbasierte benutzerdefinierte Authentifizierung. Durch das Hinzufügen von `subType: "certificateCredential"` zu einer benutzerdefinierten Autorisierungskonfiguration verwendet Journey Optimizer das verwaltete Zertifikat von Adobe, um eine JWT-Client-Bestätigung zu signieren und sie gegen ein Zugriffstoken einzutauschen – kein Client-Geheimnis erforderlich. Entwickelt für Unternehmens-APIs, die eine zertifikatbasierte Identitätsüberprüfung erzwingen, z. B. die Microsoft Entra ID. [Weitere Informationen](../datasource/external-data-sources.md#certificate-credential)

  Verfügbarkeitsdatum: 4. Juni 2026


* **Kundenwarnungen für Kampagnen-Lebenszyklus-Ereignisse** – Neue Systemwarnungen benachrichtigen Sie jetzt über wichtige Lebenszyklus-Ereignisse für Aktionen und durch API ausgelöste Kampagnen. Abonnieren Sie auf Sandbox-Ebene. [Weitere Informationen](../reports/alerts.md)

  Verfügbarkeitsdatum: 1. Juni 2026

* **URL-Parameterverschlüsselung** – Sie können jetzt URL-Parameter in Tracking- und Landingpage-Links verschlüsseln, die Ihren E-Mail-Nachrichten hinzugefügt werden. Dies bietet eine zusätzliche Sicherheitsebene für vertrauliche Parameterdaten. Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit). [Weitere Informationen](../personalization/url-parameter-encryption.md)

  Verfügbarkeitsdatum: 1. Juni 2026

* **Neue Berechtigungen für die Schlüsselregistrierung** – Für den Zugriff auf und die Verwaltung der für die URL-Parameterverschlüsselung erforderlichen Schlüssel sind jetzt zwei neue Berechtigungen erforderlich: **Schlüsselregistrierung verwalten** und **Schlüsselregistrierung anzeigen**. [Weitere Informationen](../administration/high-low-permissions.md#administration-permissions)

  Verfügbarkeitsdatum: 1. Juni 2026

* **Zusätzliche Kennungsunterstützung für externe Zielgruppen** – Zusätzliche Kennungen in Journeys werden jetzt für externe Zielgruppen unterstützt, einschließlich Zielgruppen, die aus einer CSV-Datei importiert wurden, und Zielgruppen, die mit der Komposition föderierter Zielgruppen erstellt wurden. Sie können ein beliebiges Nicht-Identitätsattribut oder ein beliebiges Identitätsattribut aus der Zielgruppe als zusätzliche ID festlegen. Eine Schemakennzeichnung ist nicht erforderlich. [Weitere Informationen](../building-journeys/supplemental-identifier.md)

  Verfügbarkeitsdatum: 11. Juni 2026

<!--
+++ Coming soon — **Information below is subject to change.**

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default execution field set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.

  Availability date: Early June, 2026

+++
-->

## Versionshinweise für Mai ’26 {#may-26-rn}

### Journeys {#may-26-journeys}

Die folgenden Funktionen und Verbesserungen wurden in dieser Version zu Journeys hinzugefügt. Weitere Änderungen werden auch in den kommenden Tagen oder Wochen erwartet.

<table>
<thead>
<tr>
<th><strong>Journey-Fragmente (eingeschränkte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt <strong>Journey-Fragmente</strong> in Adobe Journey Optimizer erstellen. Journey-Fragmente sind wiederverwendbare Sätze von Journey-Knoten, die Sie einmal erstellen und in einer beliebigen Journey in Ihrer Sandbox ablegen können. Unabhängig davon, ob es sich um eine Eignungsprüfung, eine bevorzugte Kanal-Routing-Logik oder eine Begrüßungssequenz handelt, helfen Fragmente Teams dabei, schneller und konsistent zu arbeiten, ohne dieselbe Logik jedes Mal von Grund auf neu zu erstellen.</p>
<p>Nach der Erstellung werden Fragmente in einem dedizierten <strong>Fragmentinventar</strong> gespeichert und können mithilfe der Aktivität <strong>Journey-Fragmente</strong> in Journeys eingefügt werden.</p>
<!--<p><img src="assets/do-not-localize/journey-fragments.gif"></p>-->
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/journey-fragments.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 13. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Simulation (begrenzte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können Ihre Journey jetzt auf <strong>Simulation</strong> setzen. In diesem Modus können Sie Ihre Logik mithilfe von <strong>simulierten Benutzenden</strong> überprüfen. Dies sind temporäre, speziell für die Simulation erstellte Profile, mit denen Sie frei testen können. So müssen Sie keine dauerhaften Testprofile in Adobe Experience Platform verwalten.</p>
<p>Die Hauptfunktionen dieser Funktion sind derzeit eingeschränkt für alle Benutzenden verfügbar.</p>
<p><img src="assets/do-not-localize/simulate-user.gif"></p>
<p>Weitere Informationen finden Sie im <a href="../building-journeys/simulate-journey.md">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 5. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Journey path optimization – Targeting (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use the new <strong>Optimize</strong> node to target specific audiences to determine the best path to meet your business-centric KPIs.</p>
<p>This tool allows you to develop more effective marketing campaigns that are more likely to resonate at the 1:1 level, improve marketing personalization efforts for customers and enhance critical customer engagement KPIs, such as conversions and revenue.</p>
<p>Previously available in Limited Availability, this capability is now available to all environments.</p>
<p>Availability date: June 1, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Arbitration – ranking formulas (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use formulas to automatically boost journey priority scores based on customer profile attributes and contextual factors, ensuring customers enter the most relevant journeys.</p>
<p>Previously available in Limited Availability, this capability is now available to all environments.</p>
<p>Availability date: June 1, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

### Orchestrierte Kampagnen {#may-26-oc}

Die folgenden Funktionen und Verbesserungen wurden in dieser Version zu orchestrierten Kampagnen hinzugefügt. Weitere Änderungen werden auch in den kommenden Tagen oder Wochen erwartet.

<table>
<thead>
<tr>
<th><strong>Verkettete orchestrierte Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Orchestrierte Kampagnen können jetzt miteinander verknüpft werden, indem eine orchestrierte Kampagne direkt über die <strong>Endaktivität</strong> einer anderen orchestrierten Kampagne ausgelöst wird.</p>
<p>Dies ermöglicht es, komplexe Orchestrierungslogik in kleinere, wiederverwendbare Flüsse zu unterteilen, die von mehreren übergeordneten Kampagnen aufgerufen werden können, anstatt jedes Mal neu erstellt werden zu müssen. Die zur Laufzeit übergebene Payload ist für die Segmentierung und Personalisierung in der nachgelagerten Kampagne verfügbar, sodass jede verknüpfte Kampagne sich basierend auf dem empfangenen Kontext verhalten kann.</p>
<p><img src="assets/do-not-localize/oc-trigger.gif"></p>
<p>Weitere Informationen finden Sie im <a href="../orchestrated/trigger-orchestrated-campaign.md#signal-end">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 20. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

* **Links in Anreicherungsaktivität hinzufügen** – Die Funktion „Link hinzufügen“ ist jetzt in der Anreicherungsaktivität für orchestrierte Kampagnen verfügbar. Auf diese Weise können Sie eine direkte Beziehung zwischen Ihren Arbeitstabellendaten und Ihren vorhandenen Datenbanktabellen erstellen.

  Verfügbarkeitsdatum: 20. Mai 2026

<!--
+++ Coming soon — **Information below is subject to change.**

The following orchestrated campaign capability is expected in the upcoming days or weeks.

<table>
<thead>
<tr>
<th><strong>File-based targeting for orchestrated campaigns (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Orchestrated campaigns now support loading a CSV or TXT file directly into the campaign canvas as the targeting audience, without first ingesting the file into Adobe Experience Platform. The file data is consumed at execution time and is not persisted as an Adobe Experience Platform dataset. During file setup, you can define column mappings, data types, NULL handling, and per-column error policies. This supports ad-hoc sends or partner list campaigns where building a full ingestion pipeline is not practical.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>Availability date: June 1, 2026</p>
</td>
</tr>
</tbody>
</table>

* **Loop-based personalization for relational data** - The personalization editor now supports a Loop block that iterates over relational collections, such as orders, accounts, or bookings, and renders one content block per record inside a single email or SMS. Collections are configured through the data picker using personalization tokens, with no expression writing required.

  Availability date: Early June, 2026

* **Personalize email sender details per recipient and campaign** - Orchestrated campaigns now support personalization of email header fields, including From name, From address, and Reply-To, using profile attributes or relational data. This allows sender details to reflect the relevant advisor, location, or branch for each recipient, rather than routing all sends through a single corporate address.

  Header values can be set at the channel level and overridden per campaign using contextual data for more precise control.

  Availability date: Early June, 2026

+++
-->

### Entscheidungsfindung {#may-26-decisioning}

In dieser Version wurden die folgenden Funktionen und Verbesserungen zur Entscheidungsfindung hinzugefügt. Weitere Änderungen werden auch in den kommenden Tagen oder Wochen erwartet.

<table>
<thead>
<tr>
<th><strong>Entscheidungsregeln und KI-Optimierung der Ranking-Formel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] verwendet jetzt KI, um Entscheidungsregeln und Rangfolgeformeln zu erkennen, die vereinfacht werden können. Im Bestand wird für jede Regel, für die die KI eine Optimierungsmöglichkeit identifiziert hat, ein roter Indikator angezeigt. Wenn Sie auf den Indikator klicken, wird der ursprüngliche Ausdruck zusammen mit der von der KI vorgeschlagenen Version angezeigt. Dort können Sie eine Datei herunterladen, um zu überprüfen, wie simulierte Profile von jeder Version ausgewertet werden, und um zu prüfen, ob sie sich identisch verhalten, und dann den Ausdruck durch den optimierten Ausdruck ersetzen.</p>
<p><img src="assets/do-not-localize/rule-ai.gif"></p>
<p>Weitere Informationen finden Sie in der <a href="../start/ai-features.md#decisioning-optimization">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 5. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

* **Adobe Experience Manager-Inhaltsfragmente in der Entscheidungsfindung** – Sie können jetzt Adobe Experience Manager-Inhaltsfragmente Entscheidungselementen bei der Entscheidungsfindung zuordnen und sie innerhalb von Entscheidungsrichtlinien nutzen, um das richtige Fragment zum richtigen Zeitpunkt den richtigen Kundinnen und Kunden bereitzustellen. [Weitere Informationen](../integrations/aem-fragments.md#aem-decisioning)

  Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.

  Verfügbarkeitsdatum: 20. Mai 2026

* **Details zur Entscheidungsrichtlinie in der Kampagnenübersicht** – Auf der Seite mit der Kampagnenübersicht können Sie jetzt die vollständige Struktur jeder Entscheidungsrichtlinie überprüfen, einschließlich Auswahlstrategien, Entscheidungselementen und Fallback-Angeboten, ohne die Kampagne zu duplizieren oder zu bearbeiten. Sie können auch eine JSON-Zusammenfassung in die Zwischenablage kopieren, um die Fehlerbehebung beim Adobe-Support oder Ihrem Engineering-Team durchzuführen. [Weitere Informationen](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

  Verfügbarkeitsdatum: 20. Mai 2026

* **APIs für den Migrations-Workflow zur Entscheidungsfindung** – Der API-Vertrag zum Erstellen von Abhängigkeitsanalysen und Migrations-Workflows wurde aktualisiert: Übergeben Sie **`request-level`** als **Abfrageparameter** an die Anfrage-URL (`sandbox`, `offer` oder `decision`). Die Anfrageebene darf nicht mehr im JSON-Text gesendet werden. [Weitere Informationen](../experience-decisioning/decisioning-migration-api.md)

  Verfügbarkeitsdatum: 6. Mai 2026

### E-Mail-Kanal {#may-26-email}

In dieser Version wurden die folgenden Funktionen und Verbesserungen zum E-Mail-Kanal hinzugefügt. Weitere Änderungen werden auch in den kommenden Tagen oder Wochen erwartet.

<table>
<thead>
<tr>
<th><strong>Deeplinks im E-Mail-Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Über eine dedizierte Option im E-Mail-Designer ist es jetzt möglich, Deeplinks zu Ihren E-Mail-Inhalten hinzuzufügen. Dadurch wird sichergestellt, dass Benutzende direkt zu den richtigen In-App-Inhalten weitergeleitet werden, anstatt zu Browsern oder App-Stores, wodurch der Kontext und die Interaktion erhalten bleiben.</p>
<p>Beachten Sie, dass die Deeplink-Option zwar für alle Kundinnen und Kunden verfügbar ist, Deeplinks jedoch nur funktionieren, wenn Sie die erforderlichen Konfigurations- und Implementierungsschritte für Apps abgeschlossen haben.</p>
<p><img src="assets/do-not-localize/deeplinks.gif"></p>
<p>Weitere Informationen finden Sie im <a href="../email/deeplinks.md">entsprechenden Handbuch</a>.</p>
<p>Verfügbarkeitsdatum: 12. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

* **Einschränkung der Vererbungsunterbrechung bei Fragmenten** – Beim Erstellen oder Bearbeiten eines Fragments können Sie jetzt wählen, ob es bei der Verwendung in E-Mails geändert werden kann. Durch das Sperren eines Fragments wird sichergestellt, dass es überall synchronisiert bleibt, wo es angezeigt wird. Dadurch werden lokale Bearbeitungen verhindert, die gegen Markenstandards oder Compliance-Anforderungen verstoßen könnten. Diese Einstellung kann später aktualisiert werden und auf zukünftige Verwendungen angewendet werden. [Weitere Informationen](../content-management/create-fragments.md#lock-visual-fragment)

  Verfügbarkeitsdatum: 21. Mai 2026

### Mobile Messaging (SMS, MMS und RCS) {#may-26-mobile}

In dieser Version wurden die folgenden Funktionen und Verbesserungen zu Mobile Messaging hinzugefügt.

<table>
<thead>
<tr>
<th><strong>Neuer Mobile-Nachrichtenkanal und verbessertes RCS-Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>SMS, MMS und RCS sind jetzt in Adobe Journey Optimizer in einer einzigen <strong>Mobile Message</strong>-Aktion zusammengefasst, wodurch die Verwaltung aller Nachrichtentypen auf Mobilgeräten an einem Ort erleichtert wird. Im Rahmen dieses Updates können Sie jetzt Rich-Media-RCS-Nachrichten, einschließlich Bildern, Karussells und empfohlenen Aktionen, über ein neues natives Authoring-Erlebnis direkt in Journey Optimizer erstellen.</p>
<p>Weitere Informationen finden Sie in der <a href="../mobile/get-started-mobile.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 20. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

* **Zeichenanzahl**: In Adobe Journey Optimizer können Sie jetzt die Zeichenanzahl verwenden, um die Länge Ihrer SMS-Nachrichten in Echtzeit zu überwachen. Auf diese Weise lässt sich erkennen, wann eine Nachricht in mehrere Segmente aufgeteilt wird. So kann die Formatierung besser verwaltet und ein unerwartetes Ansteigen der Versandkosten vermieden werden. [Weitere Informationen](../mobile/create-mobile-message.md)

* **SMS-Eingänge in einen benutzerdefinierten Datensatz**: Leiten Sie in **SMS-API-Anmeldedaten** **eingehende SMS** an einen ausgewählten **benutzerdefinierten, profilaktivierten Erlebnisereignisdatensatz** weiter, anstatt nur an den Standard-Tracking-Datensatz. [Weitere Informationen](../mobile/mobile-webhook.md)

* **Verbesserung der Webhook-Oberfläche**: Die Benutzeroberfläche zur Konfiguration von SMS-Webhooks enthält jetzt ein integriertes Einrichtungshandbuch mit praktischen Beispielen, das die Abstimmung von Anbieter-Payloads und die Fehlerbehebung erleichtert, da der Konfigurationsfluss nicht verlassen werden muss. [Weitere Informationen](../mobile/mobile-webhook.md)

* **Deeplinks in SMS-Inhalten** – Mit der URL-Hilfsfunktion können Sie Ihren SMS-Inhalten jetzt Deeplinks hinzufügen. Dadurch wird sichergestellt, dass die Empfangenden direkt zu den gewünschten In-App-Inhalten geleitet werden, ohne sie über einen Webbrowser oder einen App Store weiterzuleiten – vorausgesetzt, Sie haben die erforderlichen Konfigurations- und Implementierungsschritte für Apps abgeschlossen. [Weitere Informationen](../email/deeplinks.md)

### WhatsApp-Kanal {#may-26-whatsapp}

Die folgenden Verbesserungen wurden in dieser Version zum WhatsApp-Kanal hinzugefügt.

* **Unterstützung für WhatsApp-Schaltflächen und Tracking** – WhatsApp-Vorlagen unterstützen jetzt **Schnelle Antworten**, **Aktionsaufruf – URL** und **Aktionsaufruf – Telefon**. **Code kopieren** wird nicht unterstützt. Journey Optimizer sendet unterstützte Schaltflächen und verfolgt Interaktionen zusammen mit Ihren anderen Kanalberichten.

* **WhatsApp-Kanal-Kontextdaten** – Journey Optimizer erfasst jetzt zusätzliche Interaktionsdaten, die vom WhatsApp-Kanal zurückgegeben werden, und speichert sie im **AJO EmailTrackingExperienceEvent-Datensatz** unter der Feldergruppe `whatsAppChannelContext`. [Weitere Informationen](../whatsapp/send-whatsapp.md#whatsapp-channel-context)

  +++ Die folgenden Felder werden erfasst und können verwendet werden, um Zielgruppen zu erstellen und die WhatsApp-Interaktion zu analysieren

   * **`messageType`** – WhatsApp-Nachrichtentyp (z. B. `templateBased`, `response`)
   * **`inboundMessage`** – Inhalt eingehender Antworten (z. B. `stop`, `start`, `subscribe`)
   * **`inboundNumber`** – Absender-ID, bei der die eingehende Nachricht empfangen wurde
   * **`channelType`** – Kanalkategorie (`Utility`, `Marketing` oder `Promotional`)
   * **`profileNumber`** – Telefonnummer, von der die eingehende Nachricht empfangen wurde
   * **`origTimestamp`** – Original-Zeitstempel von Meta/WhatsApp
   * **`status`** – Versandstatus einschließlich standardisiertem Provider-Feedback (`sent`, `delivered`, `bounce`, `error`, `delay`, `duplicate`, `denylist`, `exclude` oder `unknown`) und der rohen Provider-Statusmeldung
   * **`reactionEvent`** – Inhalt der Benutzerantwort: Emoji für Reaktionen oder Nachrichtentext für Antworten auf eine bestimmte Nachricht
   * **`reactionMessageID`** – ID der ursprünglichen Nachricht, auf die geantwortet wird
   * **`reactionActionName`** – Typ der Antwortaktion (`react`, `unreact` oder `reply`)
   * **`interactiveSelectedTitle`** – Von der oder dem Benutzenden ausgewählter Titel aus einer interaktiven WhatsApp-Nachricht
   * **`interactiveType`** – Interaktiver Nachrichtentyp (`list reply`, `button reply` oder `button`)
   * **`interactiveSelectedDescription`** – Beschreibung der ausgewählten interaktiven WhatsApp-Option
   * **`interactiveSelectedID`** – ID der aus WhatsApp ausgewählten Option

  +++

### Inhalte und Integrationen {#may-26-content}

In dieser Version wurden die folgenden Funktionen und Verbesserungen zum Content-Management und zu Integrationen hinzugefügt.

<table>
<thead>
<tr>
<th><strong>Content-Beratungs-Selektor</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer verwendet jetzt den <strong>Content-Beratungs-Selektor</strong>, ein einheitliches Modal zur Auswahl von Experience Manager-Assets und -Inhaltsfragmenten. Der neue Selektor umfasst:</p>
<ul>
<li><strong>Durchsuchen, Suchen und Filtern </strong>aller Assets und Fragmente.</li>
<li><strong>Semantische KI-Suche</strong>: Beschreiben Sie im Klartext, was Sie benötigen, z. B. „Kaffee in den Bergen“, um kontextuell relevante Assets basierend auf Bedeutung und Inhalt zu präsentieren, nicht nur Textübereinstimmungen. Mehrsprachige Abfragen werden ebenfalls unterstützt.</li>
<li><strong>Kurzer Upload</strong>: Laden Sie eine Marketing-Zusammenfassung hoch, um automatisch Assets zu präsentieren, die basierend auf ihrem Inhalt und ihren Anforderungen an Ihren Kampagnenkontext angepasst sind.</li>
<li><strong>Dynamic Media-Ausgabedarstellungen</strong>: Wählen Sie Bildausgabedarstellungen für dynamische Assets aus und wenden Sie sie an, ohne den Selektor verlassen zu müssen.</li>
</ul>
<p>Weitere Informationen finden Sie in der <a href="../integrations/aem-content-advisor.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 19. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integrationen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit der Funktion <b>Integrationen</b> können Sie Datenquellen von Drittanbietern direkt mit Adobe Journey Optimizer verbinden. Diese Funktion vereinfacht das Einbinden externer Daten und <b>zusammenstellbarer Inhalte</b> und erleichtert so die Bereitstellung personalisierter, dynamischer Nachrichten auf allen Kanälen.</p>
<p>Diese Funktion wurde zuvor als Beta-Version veröffentlicht, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../integrations/integrations.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 4. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

* **Organisationsübergreifender Repository-Zugriff im Assets-Selektor** – Sie können jetzt Assets aus Repositorys über mehrere Organisationen hinweg direkt im Asset-Selektor von Adobe Experience Manager auswählen.

<!--
+++ Coming soon — **Information below is subject to change.**

* **Message Feedback Event Dataset moving to batch ingestion** - The `AJO Message Feedback Event Dataset` is transitioning from streaming to batch ingestion mode. This change ensures that data ingestion does not exceed streaming ingestion limits. If you use this dataset in Customer Journey Analytics reports or run queries against it, expect an increase in data latency of up to 2 hours going forward.

  Availability date: June 1, 2026

+++
-->

### Verbesserungen der Benutzerfreundlichkeit {#may-26-usability}

Die folgenden Verbesserungen der Benutzerfreundlichkeit wurden ebenfalls im Mai 2026 veröffentlicht.

#### Listen

* **Massenaktionen** – Sie können jetzt mehrere Elemente gleichzeitig in den Listen **Kampagnen**, **Fragmente** und **Vorlagen** auswählen und Massenvorgänge über eine einzelne Aktionsleiste durchführen, einschließlich Elemente zu einem Paket hinzufügen, in einen Ordner verschieben, Tags bearbeiten, den Zugriff verwalten und archivieren oder löschen. [Weitere Informationen](../start/search-filter-categorize.md#bulk-actions)

  ![](../start/assets/bulk-actions-campaigns.png)

* **Sortieren und Ändern der Spaltengröße** – Die Listen **Kampagnen**, **Fragmente** und **Vorlagen** unterstützen jetzt die Sortierung durch Klicken auf eine beliebige Spaltenüberschrift. In der Ordneransicht von Kampagnen können Sie auch nach **[!UICONTROL Priorität]** und **[!UICONTROL Kanalkonfiguration]** sortieren und filtern. Die Spaltenbreiten in den Listen **Fragmente** und **Vorlagen** können auch in der Größe angepasst werden. Ziehen Sie den Spaltenrand, um ihn an die Daten anzupassen, die Ihnen am wichtigsten sind. [Weitere Informationen](../start/search-filter-categorize.md#filter-lists)

#### Inhaltserstellung

* **Inline-Bearbeitung von Profilattributen** – Die Inline-Bearbeitung von Profilattributen im E-Mail-Designer wurde ursprünglich im April veröffentlicht. Im Rahmen der Mai-Version wurde diese Funktion vom KI-Assistenten entkoppelt und auf den Push-Kanal-Editor erweitert. [Weitere Informationen](../personalization/personalize.md#inline-personalization)

  ![](../personalization/assets/inline-profile-attributes.png)

* **Link-URL-QuickInfo im Push-Kanal-Editor** – Wenn eine URL in einem Link- oder Medienfeld zu lang ist, um vollständig angezeigt zu werden, ist immer ein QuickInfo-Symbol neben dem Feld sichtbar. Bewegen Sie den Mauszeiger darüber, um die vollständige URL anzuzeigen. [Weitere Informationen](../push/design-push.md#on-click-behavior)

  ![](../rn/assets/do-not-localize/push-link-tooltip.png)

<!--
#### Simulation & Preview

* **Redesigned preview experience** - The content preview screen has been redesigned with a side-by-side layout that lets you compare how your content renders across multiple profiles at a glance, enabling quicker and more confident reviews before sending. [Learn more](../test-approve/simulate-sample-input.md#preview)

  ![](../test-approve/assets/simulation-preview-redesign.png)
-->

<!--
+++ Coming soon — **Information below is subject to change.**

* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders to improve navigation and management in the interface.

  Availability date: Early June, 2026

+++
-->

