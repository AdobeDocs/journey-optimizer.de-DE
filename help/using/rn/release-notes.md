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
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: df64005d-8f9a-422e-ba4d-c6f6dc3454b4id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: cfba2953-2ce9-4b00-a00c-71cd338ae63fid: ee5bb250-0884-4d71-86eb-d8489e8bcadd
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 46e1b1fa15586254383c41dc76a5c67a1b1373fa
workflow-type: tm+mt
source-wordcount: 2771
ht-degree: 23%

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
>Die in diesen Versionshinweisen aufgeführten Funktionen umfassen ein **Verfügbarkeitsdatum** das angibt, wann jede Änderung in Ihrer Umgebung verfügbar wird. Im **Bald verfügbar** unten auf dieser Seite werden Funktionen und Verbesserungen aufgelistet, die in den nächsten Tagen veröffentlicht werden sollen. Informationen können sich ändern.

## Mai &#39;26 - Versionshinweise {#may-26-rn}

### Neue Funktionen {#may-26-features}

Die folgenden Funktionen wurden im Mai 2026 veröffentlicht.

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

<table>
<thead>
<tr>
<th><strong>Verkettete orchestrierte Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Orchestrierte Kampagnen können jetzt miteinander verknüpft werden, indem eine orchestrierte Kampagne direkt über die „Endaktivität“ einer anderen orchestrierten <strong> ausgelöst </strong>.</p>
<p>Dies ermöglicht es, komplexe Orchestrierungslogik in kleinere, wiederverwendbare Flüsse zu unterteilen, die von mehreren übergeordneten Kampagnen aufgerufen werden können, anstatt jedes Mal neu aufgebaut zu werden. Die zur Laufzeit übergebene Payload ist für die Segmentierung und Personalisierung in der nachgelagerten Kampagne verfügbar, sodass jede verknüpfte Kampagne sich basierend auf dem empfangenen Kontext verhalten kann.</p>
<p><img src="assets/do-not-localize/oc-trigger.gif"></p>
<p>Weitere Informationen finden Sie in der <a href="../orchestrated/trigger-orchestrated-campaign.md#signal-end">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 20. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Content Advisor-Auswahl</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer verwendet jetzt den <strong>Content Advisor-Selektor</strong>, ein einheitliches Modal zur Auswahl von Experience Manager Assets und Inhaltsfragmenten. Der neue Selektor umfasst:</p>
<ul>
<li><strong>Durchsuchen, Suchen und Filtern</strong> aller Assets und Fragmente.</li>
<li><strong>KI-Semantische Suche</strong> Beschreiben Sie, was Sie im Klartext benötigen, z. B. „Kaffee in den Bergen“, um kontextuell relevante Assets basierend auf Bedeutung und Inhalt zu präsentieren, nicht nur Textübereinstimmungen. Mehrsprachige Abfragen werden ebenfalls unterstützt.</li>
<li><strong>Kurzer Upload</strong>: Laden Sie eine Marketing-Zusammenfassung hoch, um automatisch Assets zu präsentieren, die basierend auf ihrem Inhalt und ihren Anforderungen an Ihren Kampagnenkontext angepasst sind.</li>
<li><strong>Dynamic Media-Ausgabedarstellungen</strong>: Wählen Sie Bildausgabeformate für dynamische Assets aus und wenden Sie sie an, ohne die Auswahl verlassen zu müssen.</li>
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
<th><strong>Journey Fragments</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt <strong>Journey-Fragmente</strong> in Adobe Journey Optimizer erstellen. Journey-Fragmente sind wiederverwendbare Sets von Journey-Knoten, die Sie einmal erstellen und in einer beliebigen Journey in Ihrer Sandbox ablegen können. Unabhängig davon, ob es sich um eine Eignungsprüfung, eine bevorzugte Kanal-Routing-Logik oder eine Begrüßungssequenz handelt, helfen Fragmente Teams dabei, schneller und konsistent zu arbeiten - ohne jedes Mal dieselbe Logik von Grund auf neu zu erstellen.</p>
<p>Nach der Erstellung werden Fragmente in einem dedizierten <strong>Fragmentinventar) </strong> können mithilfe der Aktivität <strong>Journey-Fragmente} in </strong> Journey eingefügt werden.</p>
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
<th><strong>Deeplinks im E-Mail-Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Es ist jetzt möglich, über eine dedizierte Option im E-Mail-Designer Deeplinks zu Ihren E-Mail-Inhalten hinzuzufügen.</p><p>Dadurch wird sichergestellt, dass Benutzende direkt zu den richtigen In-App-Inhalten weitergeleitet werden, anstatt zu Browsern oder App-Stores, wodurch der Kontext und die Interaktion erhalten bleiben.</p>
<p><img src="assets/do-not-localize/deeplinks.gif"></p>
<p>Weitere Informationen finden Sie in der <a href="../email/deeplinks.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 12. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Simulation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können Ihre Journey jetzt auf <strong>Simulation</strong> setzen. In diesem Modus können Sie Ihre Logik mithilfe von <strong>simulierten Benutzenden</strong> überprüfen. Dies sind temporäre, speziell für die Simulation erstellte Profile, mit denen Sie frei testen können. So müssen Sie keine dauerhaften Testprofile in Adobe Experience Platform verwalten.</p>
<p>Die Hauptfunktionen dieser Funktion sind derzeit eingeschränkt für alle Benutzenden verfügbar.</p>
<p><img src="assets/do-not-localize/simulate-user.gif"></p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/simulate-journey.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 5. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Entscheidungsregeln und KI-Optimierung der Rangfolgenformel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] verwendet jetzt KI, um Entscheidungsregeln und Rangfolgenformeln zu erkennen, die vereinfacht werden können. Im Bestand wird für jede Regel, für die die KI eine Optimierungsmöglichkeit identifiziert hat, ein roter Indikator angezeigt. Wenn Sie auf den Indikator klicken, wird der ursprüngliche Ausdruck zusammen mit der von KI vorgeschlagenen Version angezeigt. Dort können Sie eine Datei herunterladen, um zu überprüfen, wie simulierte Profile von jeder Version ausgewertet werden, und zu bestätigen, dass sie sich identisch verhalten, und dann den Ausdruck durch den optimierten Ausdruck ersetzen.</p>
<p><img src="assets/do-not-localize/rule-ai.gif"></p>
<p>Weitere Informationen finden Sie in der <a href="../start/ai-features.md#decisioning-optimization">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 5. Mai 2026</p>
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

### Verbesserungen {#may-26-improv}

Im Mai 2026 wurden auch die folgenden Verbesserungen veröffentlicht.

#### E-Mail-Designer

* **Einschränkung der Vererbung bei Fragmenten** - Beim Erstellen oder Bearbeiten eines Fragments können Sie jetzt auswählen, ob es bei der Verwendung in E-Mails geändert werden kann. Durch das Sperren eines Fragments wird sichergestellt, dass es überall synchronisiert bleibt, wo es angezeigt wird. Dadurch werden lokale Bearbeitungen verhindert, die Markenstandards oder Compliance-Anforderungen beschädigen könnten. Diese Einstellung kann später aktualisiert werden und auf zukünftige Verwendungen angewendet werden. [Weitere Informationen](../content-management/create-fragments.md#lock-visual-fragment)

  Verfügbarkeitsdatum: 21. Mai 2026

#### Orchestrierte Kampagnen

* **Links in Anreicherungsaktivität hinzufügen** - Die Funktion Link hinzufügen ist jetzt in der Anreicherungsaktivität für orchestrierte Kampagnen verfügbar. Auf diese Weise können Sie eine direkte Beziehung zwischen Ihren Arbeitstabellendaten und Ihren vorhandenen Datenbanktabellen erstellen.


  Verfügbarkeitsdatum: 20. Mai 2026

#### Entscheidungsfindung

* **Decisioning-Migrations-Workflow**-APIs - Der API-Vertrag zum Erstellen von Abhängigkeitsanalysen und Migrations-Workflows wurde aktualisiert: Übergeben Sie **`request-level`** als **Abfrageparameter** an die Anfrage-URL (`sandbox`, `offer` oder `decision`). Anfrageebene darf nicht mehr im JSON-Text gesendet werden. [Weitere Informationen](../experience-decisioning/decisioning-migration-api.md)

  Verfügbarkeitsdatum: 6. Mai 2026

* **Adobe Experience Manager-Inhaltsfragmente in Decisioning** - Sie können jetzt Adobe Experience Manager-Inhaltsfragmente Entscheidungselementen in Decisioning zuordnen und sie innerhalb von Entscheidungsrichtlinien nutzen, um das richtige Fragment zum richtigen Zeitpunkt für den richtigen Kunden bereitzustellen. [Weitere Informationen](../integrations/aem-fragments.md#aem-decisioning)

  Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.

  Verfügbarkeitsdatum: 20. Mai 2026

#### Integrationen

* **Organisationsübergreifender Repository-Zugriff im Assets-Selektor** - Sie können jetzt Assets aus Repositorys über mehrere Organisationen hinweg direkt im Adobe Experience Manager-Asset-Selektor auswählen.

#### SMS

<!--
* **Opt-out and consent at phone number and sender** - For SMS, Journey Optimizer now records marketing consent and opt-out at the level of both the profile's phone number and short code. 

  This capability is currently only available for Sinch SMS configurations. [Read more](../mobile/mobile-configuration-sinch.md)
-->

* **Zeichenanzahl**: In Adobe Journey Optimizer können Sie jetzt die Zeichenanzahl verwenden, um die Länge Ihrer SMS-Nachrichten in Echtzeit zu überwachen. Auf diese Weise lässt sich erkennen, wann eine Nachricht in mehrere Segmente aufgeteilt wird. So kann die Formatierung besser verwaltet und ein unerwartetes Ansteigen der Versandkosten vermieden werden. [Weitere Informationen](../mobile/create-mobile-message.md)

* **SMS-Eingänge in einen benutzerdefinierten Datensatz**: Leiten Sie in **SMS-API-Anmeldedaten** **eingehende SMS** an einen ausgewählten **benutzerdefinierten, profilaktivierten Erlebnisereignisdatensatz** weiter, anstatt nur an den Standard-Tracking-Datensatz. [Weitere Informationen](../mobile/mobile-webhook.md)

* **Verbesserung der Webhook-Oberfläche**: Die Benutzeroberfläche zur Konfiguration von SMS-Webhooks enthält jetzt ein integriertes Einrichtungshandbuch mit praktischen Beispielen, das die Abstimmung von Anbieter-Payloads und die Fehlerbehebung erleichtert, da der Konfigurationsfluss nicht verlassen werden muss. [Weitere Informationen](../mobile/mobile-webhook.md)

#### WhatsApp

* **Unterstützung und Tracking von WhatsApp-Schaltflächen** - WhatsApp-Vorlagen unterstützen jetzt **Schnellantwort**, **Call to action - URL** und **Call to action - Telefon**, **Code kopieren** wird nicht unterstützt. Journey Optimizer sendet unterstützte Schaltflächen und verfolgt Interaktionen zusammen mit Ihren anderen Kanalberichten.

* **WhatsApp-Kanal-Kontextdaten** - Journey Optimizer erfasst jetzt zusätzliche Interaktionsdaten, die vom WhatsApp-Kanal zurückgegeben werden, und speichert sie im **AJO EmailTrackingExperienceEvent-** unter der `whatsAppChannelContext`.

  +++ Die folgenden Felder werden erfasst und können verwendet werden, um Zielgruppen zu erstellen und die WhatsApp-Interaktion zu analysieren

   * **`messageType`** - WhatsApp-Nachrichtentyp (z. B. `templateBased`, `response`)
   * **`inboundMessage`** - Inhalt eingehender Antworten (z. B. `stop`, `start`, `subscribe`)
   * **`inboundNumber`** - Absender-ID, bei der die eingehende Nachricht empfangen wurde
   * **`channelType`** - Kanalkategorie (`Utility`, `Marketing` oder `Promotional`)
   * **`profileNumber`** - Telefonnummer, von der die eingehende Nachricht empfangen wurde
   * **`origTimestamp`** - Original-Zeitstempel von Meta / WhatsApp
   * **`status`** - Versandstatus einschließlich standardisiertem Provider-Feedback (`sent`, `delivered`, `bounce`, `error`, `delay`, `duplicate`, `denylist`, `exclude` oder `unknown`) und der rohen Provider-Statusmeldung
   * **`reactionEvent`** - Inhalt der Benutzerantwort: Emoji für Reaktionen oder Nachrichtentext für Antworten auf eine bestimmte Nachricht
   * **`reactionMessageID`** - ID der ursprünglichen Nachricht, auf die geantwortet wird
   * **`reactionActionName`** - Typ der Antwortaktion (`react`, `unreact` oder `reply`)
   * **`interactiveSelectedTitle`** - Vom Benutzer ausgewählter Titel aus einer interaktiven WhatsApp-Nachricht
   * **`interactiveType`** - Interaktiver Nachrichtentyp (`list reply`, `button reply` oder `button`)
   * **`interactiveSelectedDescription`** - Beschreibung der ausgewählten interaktiven WhatsApp-Option
   * **`interactiveSelectedID`** - ID der aus WhatsApp ausgewählten Option

  +++


## Demnächst {#coming-soon}

Die folgenden Funktionen und Verbesserungen sind für Ende Mai geplant. **Informationen können Änderungen unterliegen**. Aktualisierte Links, Bildschirme und Dokumentationen werden freigegeben, sobald diese Aktualisierungen live in der Produktion verfügbar sind.

### Neue Funktionen {#coming-soon-features}

<table>
<thead>
<tr>
<th><strong>KI-Assistent für Journey-Ausdrücke</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der KI-Assistent arbeitet jetzt im erweiterten Ausdruckseditor von Journey, um Eingabeaufforderungen in natürliche Sprachen in gültige Ausdrücke und Bedingungslogik zu konvertieren. Beschreiben Sie den Ausdruck, den Sie erstellen möchten, und der KI-Assistent generiert einsatzbereiten Code, den Sie sofort anwenden oder durch Folgeaufforderungen verfeinern können.</p>
<p>Diese Funktion steht allen Kunden von as a Public Beta zur Verfügung.</p>
<!--<p><img src="assets/do-not-localize/expression-assistant.gif"></p>-->
<p>Verfügbarkeitsdatum: 22. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Automatischer Abschluss für nicht wiederkehrende Journey beim Lesen von Zielgruppen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey, die nicht wiederkehrend <strong>Zielgruppe lesen</strong> sind, wechseln jetzt automatisch in den <strong>Stopped</strong>-Status, sobald das letzte aktive Profil beendet wurde. Zuvor blieben diese Journey-<strong> bis zum Ablauf der 91-tägigen globalen maximalen Wartezeit </strong>Live), selbst wenn keine Profile mehr durch sie hindurch strömten. Mit dieser Verbesserung spiegelt der Journey-Status den tatsächlichen Ausführungsstatus nach Abschluss wider, sodass der Journey-Bestand ohne manuelles Eingreifen stets korrekt ist.</p>
<p>Beachten Sie, dass dieses Verhalten nicht für Journey gilt, die Knoten enthalten, die Wartezeiten verursachen, z. B. Warteknoten, Reaktionsknoten oder ereignisausgelöste Transitionen. Diese Journey unterliegen weiterhin der standardmäßigen globalen 91-Tage-Zeitüberschreitung.</p>
<p>Verfügbarkeitsdatum: 21. Mai 2026</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Unterstützung von Entscheidungen im Briefpost-Kanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Entscheidungsrichtlinien zu Briefpost-Journey und -Kampagnen hinzufügen. Entscheidungsrichtlinien sind Container für Ihre Angebote, die die Decisioning-Engine nutzen, um dynamisch den besten Inhalt für jedes Zielgruppenmitglied zurückzugeben. Die Briefpost-Entscheidungsfindung unterstützt auch Anwendungsfälle für Batch-Entscheidungen, mit denen Sie die entsprechenden Angebotselemente für jedes Profil in einer bestimmten Adobe Experience Platform-Zielgruppe exportieren können.</p>
<!--<p><img src="assets/do-not-localize/exd-dm.gif"></p>-->
<p>Verfügbarkeitsdatum: 1. Juni 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Pfadoptimierung - Targeting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verwenden Sie den neuen <strong>Optimieren</strong>-Knoten, um bestimmte Zielgruppen anzusprechen und den besten Pfad zur Erfüllung Ihrer geschäftsorientierten KPIs zu ermitteln.</p>
<p>Mit diesem Tool können Sie effektivere Marketing-Kampagnen entwickeln, die mit größerer Wahrscheinlichkeit auf 1:1-Ebene Resonanz finden, die Marketing-Personalisierungsbemühungen für Kunden verbessern und wichtige KPIs für die Kundeninteraktion wie Konversionen und Umsatz verbessern.</p>
<p>Diese Funktion war zuvor nur in begrenzter Verfügbarkeit verfügbar und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum: 21. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Schlichtung - Rangfolgeformeln</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Formeln verwenden, um anhand von Kundenprofilattributen und Kontextfaktoren automatisch die Journey-Prioritätswerte zu erhöhen und so sicherzustellen, dass Kunden in die relevantesten Journey eintreten.</p>
<p>Diese Funktion war zuvor nur in begrenzter Verfügbarkeit verfügbar und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum: 21. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Simulation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können Ihre Journey jetzt auf <strong>Simulation</strong> setzen. In diesem Modus können Sie Ihre Logik mithilfe von <strong>simulierten Benutzenden</strong> überprüfen. Dies sind temporäre, speziell für die Simulation erstellte Profile, mit denen Sie frei testen können. So müssen Sie keine dauerhaften Testprofile in Adobe Experience Platform verwalten.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit). Mit der Version „Allgemeine Verfügbarkeit“ können Sie jetzt Journey Agent verwenden, um simulierte Benutzende und Ereignisse direkt im Simulationsmenü zu generieren.</p>
<p>Verfügbarkeitsdatum: Anfang Juni 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Dateibasiertes Targeting für koordinierte Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Orchestrierte Kampagnen unterstützen jetzt das direkte Laden einer CSV- oder TXT-Datei in die Kampagnen-Arbeitsfläche als Zielgruppe, ohne die Datei zuerst in Adobe Experience Platform aufnehmen zu müssen. Die Dateidaten werden zur Ausführungszeit genutzt und nicht als Adobe Experience Platform-Datensatz beibehalten. Während der Dateieinrichtung können Sie Spaltenzuordnungen, Datentypen, die NULL-Verarbeitung und Fehlerrichtlinien pro Spalte definieren. Dies unterstützt Ad-hoc-Sendungen oder Partnerlisten-Kampagnen, bei denen der Aufbau einer vollständigen Aufnahme-Pipeline nicht praktisch ist. </p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p>Verfügbarkeitsdatum: 1. Juni 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Pfadoptimierung - Targeting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verwenden Sie den neuen <strong>Optimieren</strong>-Knoten, um bestimmte Zielgruppen anzusprechen und den besten Pfad zur Erfüllung Ihrer geschäftsorientierten KPIs zu ermitteln.</p>
<p>Mit diesem Tool können Sie effektivere Marketing-Kampagnen entwickeln, die mit größerer Wahrscheinlichkeit auf 1:1-Ebene Resonanz finden, die Marketing-Personalisierungsbemühungen für Kunden verbessern und wichtige KPIs für die Kundeninteraktion wie Konversionen und Umsatz verbessern.</p>
<p>Diese Funktion war zuvor nur in begrenzter Verfügbarkeit verfügbar und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum: 21. Mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Schlichtung - Rangfolgeformeln</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Formeln verwenden, um anhand von Kundenprofilattributen und Kontextfaktoren automatisch die Journey-Prioritätswerte zu erhöhen und so sicherzustellen, dass Kunden in die relevantesten Journey eintreten.</p>
<p>Diese Funktion war zuvor nur in begrenzter Verfügbarkeit verfügbar und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum: 21. Mai 2026</p>
</td>
</tr>
</tbody>
</table>


### Verbesserungen {#coming-soon-improvements}

#### Navigation

* **Ordner für Journey und Kampagnen** - Sie können Ihre Journey und Kampagnen jetzt in Ordnern organisieren, um die Navigation und Verwaltung in der Benutzeroberfläche zu verbessern.

  Verfügbarkeitsdatum: 2. Juni 2026

#### Journeys

* **Zertifikatbasierte benutzerdefinierte Authentifizierung in benutzerdefinierten Aktionen** - Benutzerdefinierte Aktionen unterstützen jetzt die zertifikatbasierte benutzerdefinierte Authentifizierung. Durch Hinzufügen des Untertyps „certificateCredential“ zu einer benutzerdefinierten Autorisierungskonfiguration verwendet Journey Optimizer das verwaltete Zertifikat von Adobe, um eine JWT-Client-Bestätigung zu signieren und gegen ein Zugriffstoken einzutauschen - kein Client-Geheimnis erforderlich. Entwickelt für Unternehmens-APIs, die eine zertifikatbasierte Identitätsüberprüfung erzwingen, z. B. die Azure Entra ID.

  Verfügbarkeitsdatum: 21. Mai 2026

* **Zusätzliche Kennungsunterstützung für externe Zielgruppen** - Zusätzliche Kennungen in Journey werden jetzt für externe Zielgruppen unterstützt, einschließlich Zielgruppen, die aus einer CSV-Datei importiert wurden, und Zielgruppen, die mit Federated Audience Composition erstellt wurden. Sie können ein beliebiges Nicht-Identitätsattribut oder ein beliebiges Identitätsattribut aus der Zielgruppe als zusätzliche ID festlegen. Es ist keine Schemakennzeichnung erforderlich.

  Verfügbarkeitsdatum: 1. Juni 2026

#### Orchestrierte Kampagnen

* **Schleifenbasierte Personalisierung für relationale Daten** - Der Personalisierungseditor unterstützt jetzt einen Schleifenblock, der relationale Sammlungen wie Bestellungen, Konten oder Buchungen durchläuft und einen Inhaltsblock pro Datensatz in einer einzelnen E-Mail oder SMS rendert. Sammlungen werden über die Datenauswahl mithilfe von Personalisierungs-Token konfiguriert, ohne dass ein Ausdruck geschrieben werden muss.

  Verfügbarkeitsdatum: 1. Juni 2026

#### E-Mail-Designer

* **Rich-Text in bearbeitbaren Fragmentfeldern** - Sie können jetzt anpassbaren Fragmenten, die in Ihrem E-Mail-Inhalt verwendet werden, Rich-Text hinzufügen. Wenn Sie beispielsweise die Textkomponente als bearbeitbares Feld in der E-Mail-Designer verwenden, können Sie den Inhalt direkt formatieren (z. B. fett und kursiv) und Hyperlinks einfügen.

  Verfügbarkeitsdatum: 1. Juni 2026

#### Kampagnen

* **Kundenwarnungen für Kampagnen-Lebenszyklus-Ereignisse** - Neue Systemwarnungen benachrichtigen Sie jetzt über wichtige Lebenszyklus-Ereignisse für Aktionen und API-ausgelöste Kampagnen. Abonnieren Sie auf Sandbox-Ebene.

  Verfügbarkeitsdatum: 1. Juni 2026

* **Standard-Ausführungsfeld in Kampagnen überschreiben** - Zuvor auf Journey-Ebene verfügbar, können Sie jetzt das Standard-Ausführungsfeld überschreiben, das in den Kampagnenparametern global für Ihre E-Mail-, SMS- und WhatsApp-Sendungen festgelegt ist.

  Verfügbarkeitsdatum: 1. Juni 2026

#### E-Mail

* **E-Mail-Absenderdetails nach Empfänger und Kampagne personalisieren** - Orchestrierte Kampagnen unterstützen jetzt die Personalisierung von E-Mail-Header-Feldern, einschließlich Absendername, Absenderadresse und Antwortadresse, mithilfe von Profilattributen oder relationalen Daten. Auf diese Weise können Absenderdetails den relevanten Berater, Standort oder die Zweigstelle für jeden Empfänger widerspiegeln, anstatt alle Sendungen über eine einzelne Unternehmensadresse weiterzuleiten.

  Header-Werte können auf Kanalebene festgelegt und pro Kampagne überschrieben werden, indem kontextuelle Daten verwendet werden, um die Kontrolle zu verbessern.

  Verfügbarkeitsdatum: 1. Juni 2026

#### Konfiguration

* **Datensatz mit Nachrichten-Feedback-Ereignissen, der zur Batch-Aufnahme** wird`AJO Message Feedback Event Dataset` Der wechselt vom Streaming- in den Batch-Aufnahme-Modus. Durch diese Änderung wird sichergestellt, dass die Datenaufnahme die Streaming-Aufnahmebeschränkungen nicht überschreitet. Wenn Sie diesen Datensatz in Customer Journey Analytics-Berichten verwenden oder Abfragen dafür ausführen, erwarten Sie in Zukunft eine Zunahme der Datenlatenz von bis zu 2 Stunden.

  Verfügbarkeitsdatum: 1. Juni 2026

#### Reporting

* **Bot-Klicks für E-Mail- und SMS-Reporting ausschließen** - Neue geschätzte Metriken sind jetzt verfügbar, mit denen Sie nicht menschliche (Bot-)Interaktionen aus E-Mail- und SMS-Berichten herausfiltern können. Dazu gehören geschätzte Klicks, Clickthrough-Raten (CTR) und Clickto-Open-Raten (CTOR), die eine genauere Darstellung der echten Kundeninteraktion bieten. Vorhandene Metriken bleiben unverändert, und diese neuen Metriken können zusammen mit dem aktuellen Reporting für eine verbesserte Analyse verwendet werden.

  Verfügbarkeitsdatum: 1. Juni 2026
