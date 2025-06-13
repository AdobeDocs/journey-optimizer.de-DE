---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: c00d5a97e7bedf6f1a22a59cc3bd7588eb9ad32e
workflow-type: tm+mt
source-wordcount: '2164'
ht-degree: 61%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert. [!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.


## Frühzeitige Versionshinweise Juni 2025 {#25-6-rn}


**Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Screenshots und die aktualisierte Dokumentation werden am Veröffentlichungsdatum veröffentlicht.

**Veröffentlichungsdatum**: 17.-18. Juni 2025

Siehe auch [Adobe Experience Platform-Versionshinweise](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

### Neue Funktionen {#25-06-features}

Im Folgenden werden die neuen Funktionen dieser Version beschrieben.


<table>
<thead>
<tr>
<th><strong>RCS Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Rich Communication Services (RCS)-Messaging wird jetzt in Journey Optimizer unterstützt und ermöglicht die folgenden erweiterten Messaging-Funktionen, die der Provider- und Provider-Unterstützung unterliegen:</p>
<ul>
<li>Unterstützung für gebrandete und verifizierte Absender: Senden Sie Nachrichten mithilfe verifizierter Geschäftsprofile mit Branding-Elementen (Logo, Absendername usw.).</li>
<li>Einblicke in den Nachrichtenversand: Sie erhalten detaillierte Versandberichte einschließlich Statusaktualisierungen der Nachricht (z. B. gesendet, zugestellt, gelesen).</li>
<li>Linktracking: Einbetten und Verfolgen von URLs in RCS-Nachrichten für die Interaktionsanalyse.</li>
<li>Fallback zu SMS: Automatischer Fallback zu SMS, wenn das Gerät des Profils RCS nicht unterstützt oder über RCS vorübergehend nicht erreichbar ist.</li>
<li>Grundlegende Nachrichtenkomposition: Senden Sie textbasierte RCS-Nachrichten mit optionalen Medien und Rich-Elementen, je nach Anbieter-Support.</li>
</ul>
<!--p>For more information, refer to the <a href="../sms/sms-configuration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Formularfelder in Code-basierten Erlebnisinhalten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt bestimmte bearbeitbare Felder in JSON- oder HTML-Inhaltsvorlagen definieren, die es technisch nicht versierten Benutzenden ermöglichen, Inhalte in einer Formularansicht innerhalb der codebasierten Erlebniskanalbearbeitung einfach zu bearbeiten, ohne Code bearbeiten zu müssen. Darüber hinaus können Sie bei der Definition der Code-basierten Erlebnis-Inhaltsvorlagen jetzt Entscheidungsrichtlinien in die Vorlage einfügen, was die Wiederverwendbarkeit und Benutzerfreundlichkeit erhöht.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Benutzerdefinierte Methode zur Zuweisung von Subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Zusätzlich zur vollständigen Delegierung und der CNAME-Methode ist jetzt eine neue Methode zur Subdomain-Konfiguration verfügbar: die Methode der benutzerdefinierten Delegierung , mit der Sie alle Aspekte des DNS, die für den Versand, das Rendern und das Tracking von Nachrichten erforderlich sind, vollständig steuern und verwalten können.</p>
<p>Diese Funktion wurde zuvor mit eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Aktivität „Inhaltsentscheidung“ in Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt personalisierte Angebote über eine dedizierte Aktivität zur Inhaltsentscheidung in Ihre Journey auf der Journey-Arbeitsfläche einbeziehen und sie in Journey-Aktivitäten, einschließlich Bedingungen und benutzerdefinierter Aktionen, verwenden.</p>
<p>Diese Funktion ist nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit) und wird in einer zukünftigen Version global eingeführt.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey-Probelauf</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Dry Run ist ein spezieller Journey-Veröffentlichungsmodus in Adobe Journey Optimizer, der es Journey-Anwendern ermöglicht, eine Journey mit echten Produktionsdaten zu testen, ohne echte Kunden zu kontaktieren oder Profilinformationen zu aktualisieren. Mit dieser Funktion können Journey-Anwender Vertrauen in ihr Journey-Design und die Zielgruppenbestimmung gewinnen, bevor sie es live veröffentlichen.</p>
<p>Diese Funktion ist nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit) und wird in einer zukünftigen Version global eingeführt.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey pausieren und fortsetzen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Jetzt können Sie anhalten und Ihre Journey fortsetzen. Diese Funktion bietet Anwendern von Journey mehr Kontrolle und Flexibilität, da Live-Journey vorübergehend ausgesetzt werden können, ohne das Kundenerlebnis zu beeinträchtigen. Wenn angehalten, werden keine Nachrichten gesendet und die Profile verbleiben in einem ausgesetzten Zustand, bis die Journey fortgesetzt wird.</p>
<p>Sie können nur eine Journey anhalten und fortsetzen oder Massenpausierungs- und Wiederaufnahmevorgänge für eine Gruppe von Journeys durchführen.</p>
<p>Darüber hinaus können Sie globale Filter auf pausierte Journey anwenden, um Profile auf der Grundlage ihrer Attribute auszuschließen.</p>
<p>Diese Funktion ist nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit) und wird in einer zukünftigen Version global eingeführt.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Skalieren der Gewinner von Experimenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dem Gewinner des Experiments skalieren können Sie die erfolgreichste Variante eines Experiments automatisch oder manuell für Ihre gesamte Audience einführen. Dadurch wird sichergestellt, dass Sie die Reichweite und Effektivität einmal identifizierter Top-Performer ohne ständige manuelle Überwachung maximieren können.</p>
<p>Weitere Informationen finden Sie in der <a href="../content-management/content-experiment.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 2. Juni 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Konflikte und Priorisierung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer ist es wichtig, das Volumen und den Zeitpunkt von Kampagnen und Journeys zu verwalten, um zu vermeiden, dass Kundinnen und Kunden mit zu vielen Interaktionen überfordert werden. Journey Optimizer bietet nun mehrere Tools für das Konflikt-Management und die Priorisierung, die bisher nur eingeschränkt für bestimmte Organisationen verfügbar waren (LA) und jetzt allgemein zur Verfügung stehen (GA).</p>
<p>Diese Funktion wurde zuvor mit eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung. Mit dieser allgemein verfügbaren Version werden die folgenden Verbesserungen eingeführt:</p>
<ul>
<li>Erweiterte Unterstützung: Konflikt-Management-Tools unterstützen nun neben Journeys vom Typ „Zielgruppen lesen“ auch unitäre Journeys und Journeys vom Typ „Zielgruppen-Qualifizierung“.</li>
<li>Verbesserte Fehlerbehebung: Im Abfrage-Service sind nun zwei neue Schrittereignisfelder verfügbar, mit denen Sie analysieren können, warum ein Profil von einer Journey oder Kampagne abgelehnt wurde.</li>
<li>Erweitertes Reporting: Berichte zeigen jetzt an, durch welche spezifische Regel ein Profil von einer Journey oder Kampagne ausgeschlossen wurde, was für mehr Transparenz und verwertbare Erkenntnisse sorgt.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Weitere Informationen finden Sie in der <a href="../conflict-prioritization/gs-conflict-prioritization.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: 3. Juni 2025</p>
</td>
</tr>
</tbody>
</table>


### Verbesserungen {#25-06-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.

* **Kanalregelsätze**

   * **Benutzerdefiniertes Zeitfenster** für die Begrenzung - Im Konfigurationsbildschirm für Kanalregelsätze ist jetzt ein neues Feld **Wiederholungsanzahl** verfügbar, mit dem Sie Frequenzbegrenzungsregeln je nach angegebener Dauer über mehrere Tage, Wochen oder Monate anwenden können.

   * **Stündliche Dauer** - Sie können jetzt für Kanalregelsätze eine Begrenzung auf stündlicher Basis anwenden.

* **Code-basierte Erlebnisse**

  Entscheidungsrichtlinien sind jetzt in Code-basierten Erlebnis-Inhaltsvorlagen und in der rechten Leiste des Code-Editors verfügbar.

* **E-Mail-Designer**

   * **Unterstützung von benutzerdefiniertem CSS** - Mit Journey Optimizer können Sie Ihrem E-Mail-Inhalt jetzt benutzerdefiniertes CSS direkt im E-Mail-Designer hinzufügen.
   * **Unterstützung des Dunkelmodus** - Der Journey Optimizer E-Mail-Designer bietet jetzt die Möglichkeit, in den Dunkelmodus zu wechseln, in dem Sie bestimmte Einstellungen definieren können.

* **Kampagnen** - Neue Registerkartennavigation für Aktionskampagnen. Dieses neue Navigationsmuster ermöglicht einen schnelleren Zugriff auf die Inhaltserstellung und unterstützt die weitere Erweiterung der Einstellungen in allen Kampagnen.

* **Decisioning** - Verfügbarkeitsdatum: 3. Juni 2025

  Entscheidungsobjekte können jetzt zwischen Sandboxes kopiert werden, wodurch Test- und Bereitstellungs-Workflows optimiert werden. [Weitere Informationen](../configuration/copy-objects-to-sandbox.md#decisioning)

* **Unterstützung von Entscheidungselementattributen für Entscheidungsregeln** - Verfügbarkeitsdatum: 4. Juni 2025

  Sie können jetzt Entscheidungselement-Attribute nutzen, um Entscheidungsregeln zu erstellen. [Weitere Informationen](../experience-decisioning/rules.md#create)

* **Aktualisierung der Interactive Message Execution API** - Verfügbarkeitsdatum: 6. Juni 2025

  Mit der Interactive Message Execution API können Sie jetzt den Zeitplan der bevorstehenden Kampagnenausführung löschen. [Weitere Informationen](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}

## Versionshinweise Mai 2025 {#25-5-rn}

<!--**Release date**: May 20-21, 2025-->

### Neue Funktionen {#25-05-features}

Im Folgenden werden die neuen Funktionen dieser Version beschrieben.

<table>
<thead>
<tr>
<th><strong>Kalenderansicht für Kampagnen- und Journey-Inventar</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine Kalenderansicht ist nun in den Journey- und Kampagnenlisten verfügbar. Damit können Sie alle Journey- und Kampagnenaktivierungen in den jeweiligen Listen visualisieren.</p>
<p>Diese Änderung ist derzeit nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um den Zugriff anzufordern, verwenden Sie <a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">dieses Formular</a>.</p>
<img src="assets/do-not-localize/calendar.gif">
<p>Weitere Informationen finden Sie in den folgenden Abschnitten: <a href="../building-journeys/journey-ui.md">Durchsuchen und Filtern Ihrer Journey</a>, <a href="../campaigns/modify-stop-campaign.md">Zugreifen auf Kampagnen</a>.</p>
<p>Verfügbarkeitsdatum:Donnerstag, 28. Mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integration von Adobe Experience Manager-Inhaltsfragmenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Durch die Integration von Adobe Experience Manager und Adobe Journey Optimizer können Sie nun Adobe Experience Manager-Inhaltsfragmente mühelos in Ihren Journey Optimizer-Inhalten verwenden. Diese nahtlose Verbindung erleichtert den direkten Zugriff auf und die Verwendung von AEM-Inhalten in Journey Optimizer.</p>
<p>Diese Funktion war bisher nur für eine begrenzte Anzahl von Organisationen verfügbar und bietet jetzt folgende Verbesserung: Sie können jetzt im Editor-Modus Platzhalter definieren und Personalisierungswerte in der Fragmentsignatur zuordnen.</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li>
<li>Define placeholders and map personalization values within the fragment signature using the Editor mode.</li-->
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>Weitere Informationen finden Sie in der <a href="../integrations/aem-fragments.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Samstag, 23. Mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integration von Adobe Experience Manager Dynamic Media</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dynamic Media-Assets sind jetzt direkt in Journey Optimizer verfügbar und zugänglich. Die Integration bietet folgende Möglichkeiten:</p>
<ul>
<li>Zentrales Verwalten von Assets mit Echtzeit-Updates</li>
<li>Sofortiges Ändern von Asset-Einstellungen wie Breite und Höhe</li>
<li>Anpassen von Dynamic Media-Vorlagen durch Aktualisieren von Inhalten und Hinzufügen von Personalisierungsfeldern</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>Diese Funktion wurde zuvor mit eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../integrations/aem-dynamic.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Samstag, 23. Mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Zusätzliche ID für von einem Ereignis ausgelöste Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können nun Journeys auslösen, indem Sie eine Profilkennung zusammen mit einer anderen Kennung wie einer Bestell-, Abonnement- oder Rezept-ID verwenden, sodass dasselbe Profil mehrmals in derselben Journey vorhanden sein kann. Dies ermöglicht Szenarien wie die parallele Verwaltung mehrerer Bestellungen oder Abonnements, wobei jede Instanz ihrem eigenen Pfad durch die Journey folgt.</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/supplemental-identifier.md">ausführlichen Dokumentation</a>.</p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p>Verfügbarkeitsdatum: Samstag, 23. Mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simulieren von Inhaltsvarianten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<!--p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p-->
<p>Diese Funktion wurde zuvor mit eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung. Im Rahmen dieser allgemeinen Verfügbarkeit bietet die Funktion jetzt Unterstützung für mehrsprachige Inhalte und Inhaltsexperimente, sodass Sie Varianten über verschiedene Sprachen und Abwandlungen hinweg testen können. Darüber hinaus unterstützt sie jetzt kontextuelle Attribute (zusätzlich zu Profilattributen), was noch dynamischere und situationsbezogener Inhaltstests ermöglicht.</p>
<img src="assets/do-not-localize/variants.gif">
<p>Weitere Informationen finden Sie in der <a href="../test-approve/simulate-sample-input.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Samstag, 23. Mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Synchronisieren des Zeitplans „Zielgruppe lesen” mit Batch-Segmentierungsauftrag</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können nun tägliche Journey-Ausführungen nach Abschluss der Batch-Segmentierung auslösen. Diese Option ist jetzt bei täglich geplanten Journeys für alle Kundinnen und Kunden verfügbar. Sie können damit ein Zeitfenster von bis zu 6 Stunden definieren, in dem auf Zielgruppendaten aus Batch-Segmentierungsaufträgen gewartet wird. So wird sichergestellt, dass Journeys mit den aktuellen Daten ausgeführt oder übersprungen werden, falls sie noch nicht bereit sind. </p>
<p>Diese Funktion wurde zuvor mit eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/read-audience.md#schedule">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum:Mittwoch, 20. Mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Benutzerdefinierter SMS-Anbieter</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Journey Optimizer können Sie nun zusätzliche SMS-Anbieter neben den Standardoptionen Sinch, Infobip und Twilio konfigurieren. Durch die Konfiguration benutzerdefinierter SMS-Anbieter können Sie Drittanbieter direkt integrieren, die erweiterte Payload-Anpassung für dynamisches Messaging nutzen und Einverständnisvoreinstellungen (Opt-in/Opt-out) verwalten, um Compliance sicherzustellen.</p>
<p>Weitere Informationen finden Sie in der <a href="../sms/sms-configuration-custom.md">ausführlichen Dokumentation</a>.</p>
<p>Diese Funktion wurde zuvor mit eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum:Mittwoch, 20. Mai 2025</p>
</td>
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
<p>Diese Funktion befindet sich derzeit in der Beta-Version und steht nur der Beta-Kundschaft zur Verfügung. Wenden Sie sich an den Adobe-Support, um am Beta-Programm teilzunehmen.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Weitere Informationen finden Sie in der <a href="../email/apply-email-themes.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum:14. Mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Entscheidungsfindung – neuer KI-Formel-Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt spezifische Rangfolgeformeln für die Entscheidungsfindung erstellen, indem Sie Kriterien in einer neuen, verbesserten Oberfläche definieren und kombinieren. Anstatt sich nur auf eine statische Angebotspriorität zu verlassen, können Sie benutzerdefinierte Rangfolgeformeln definieren, die KI-Modellbewertungen, Angebotsprioritäten, Profilattribute, Angebotsattribute und kontextuelle Signale über eine geführte Benutzeroberfläche kombinieren.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/exd-ranking-formulas.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum:14. Mai 2025</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#25-05-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.


* **Neue Unterstützung von Kampagnenobjekten für Sandbox-Kopie** - Verfügbarkeitsdatum: 15. Mai 2025

  Beim Kopieren von Kampagnen mithilfe der Paketexport- und Paketimportfunktionen über mehrere Sandboxes hinweg werden nun auch die folgenden Abhängigkeiten kopiert: Kanalkonfigurationen, Experimentvarianten und -einstellungen, Entscheidungsrichtlinien und -elemente. [Weitere Informationen](../configuration/copy-objects-to-sandbox.md)

* **Ordner für Landingpages** – Verfügbarkeitsdatum: 9. Mai 2025

  Für eine einfache Verwaltung Ihrer Landingpages können Sie nun Ordner verwenden, um sie effektiver in einer strukturierten Hierarchie zu organisieren. [Weitere Informationen](../landing-pages/manage-lp.md)

* **Direkt-Mail: SSH-Schlüsselunterstützung für SFTP-Verbindungen** – Verfügbarkeitsdatum: 5. Mai 2025

  Bei der Direkt-Mail-Datei-Routing-Konfiguration können Sie nun zusätzlich zum vorhandenen SFTP mit passwortbasierter Authentifizierung Ihre Direkt-Mail-Datei auf einen SFTP-Server mittels SSH-Schlüsselauthentifizierung exportieren. [Weitere Informationen](../direct-mail/direct-mail-configuration.md)

* **Pillenaktivierung zur Personalisierung** – Verfügbarkeitsdatum: 5. Mai 2025

  Im Personalisierungseditor wurde die neue Schaltfläche „Pillen“ hinzugefügt. Wenn diese Option aktiviert ist, werden Profil- und kontextuell Attribute als Pillen angezeigt, was die Lesbarkeit Ihres Codes verbessert. [Weitere Informationen](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >Diese Funktion wird in den nächsten 30 Tagen schrittweise in allen Umgebungen eingeführt.

* **Umleitung zur URL-Unterstützung im Web-Kanal** - Verfügbarkeitsdatum: 20. Mai 2025

  Mit dem Journey Optimizer-Web-Kanal können Sie nun Besuchende zu einer anderen bestehenden URL umleiten, anstatt im visuellen Editor eine neue Variante zu erstellen. Mit dieser Funktion können Experimente durchgeführt werden, bei denen zwei völlig verschiedene Seiten verglichen und nicht nur einige Elemente auf einer Seite geändert werden. [Weitere Informationen](../web/create-web.md#web-redirect-to-url)

* **Ordner für Vorlagen und Fragmente** - Verfügbarkeitsdatum: 20. Mai 2025

  Mit Ordnern können Sie Ihre Objekte einfacher und effektiver in einer strukturierten Hierarchie organisieren. Ordner, die zuvor nur für eine Reihe von Organisationen verfügbar waren (LA), stehen nun allen Benutzenden zur Verwaltung ihrer Inhaltsvorlagen und Fragmente zur Verfügung (GA). Weitere Informationen finden Sie in den Abschnitten zu [Inhaltsvorlagen](../content-management/access-content-templates.md#folders) und [Fragmenten](../content-management/manage-fragments.md#folders).

* **Klick-Tracking in E-**-Vorlagen - Verfügbarkeitsdatum: 20. Mai 2025

  Das Klick-Tracking für `<area>`-Elemente in Imagemaps im E-Mail-Inhalt wird jetzt nativ in [!DNL Journey Optimizer] unterstützt. Dadurch soll sichergestellt werden, dass Imagemap-Bereiche dasselbe Tracking-Wrapping sowie dieselben Tracking-Daten und angehängten Parameter wie Standard-Hyperlinks erhalten. [Weitere Informationen zum Tracking von Nachrichten](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **Rechte Leiste in der Kampagnenliste** - Verfügbarkeitsdatum: 20. Mai 2025

  Wenn Sie in der Kampagnenliste eine Kampagne auswählen, wird jetzt ein Bereich mit den zugehörigen Details geöffnet.

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.-->

<!--* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->

