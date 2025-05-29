---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 951056d22975a34af50faa450859d635b542f90f
workflow-type: tm+mt
source-wordcount: '1235'
ht-degree: 35%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert. [!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Mai &#39;25 - Versionshinweise {#25-5-rn}

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
<p>Eine Kalenderansicht ist jetzt in den Journey- und Kampagnenlisten verfügbar. Damit können Sie alle Journey- und Kampagnenaktivierungen in den jeweiligen Listen visuell darstellen.</p>
<p>Diese Änderung ist derzeit nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um den Zugriff anzufordern, verwenden Sie <a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">dieses Formular</a>.</p>
<img src="assets/do-not-localize/calendar.gif">
<p>Weitere Informationen finden Sie in den folgenden Abschnitten: <a href="../building-journeys/journey-ui.md">Durchsuchen und Filtern Ihrer Journey</a>, <a href="../campaigns/modify-stop-campaign.md">Zugreifen auf Kampagnen</a>.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 28. Mai 2025</p>
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
<p>Durch die Integration von Adobe Experience Manager und Adobe Journey Optimizer können Sie jetzt mühelos Adobe Experience Manager-Inhaltsfragmente in Ihren Journey Optimizer-Inhalten verwenden. Diese nahtlose Verbindung erleichtert den direkten Zugriff auf und die Verwendung Ihrer AEM-Inhalte in Journey Optimizer.</p>
<p>Zuvor für eine begrenzte Anzahl von Organisationen (LA) verfügbar, ist diese Funktion jetzt allgemein verfügbar mit der folgenden Verbesserung:</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li-->
<li>Definieren Sie Platzhalter und Zuordnen von Personalisierungswerten in der Fragmentsignatur mithilfe des Editor-Modus.</li>
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>Weitere Informationen finden Sie in der <a href="../integrations/aem-fragments.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Samstag, 23. Mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager Dynamic Media-Integration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dynamic Media-Assets sind jetzt direkt in Journey Optimizer verfügbar und zugänglich. Die Integration bietet folgende Möglichkeiten:</p>
<ul>
<li>Verwalten Sie Assets zentral mit Echtzeit-Updates.</li>
<li>Ändern Sie die Einstellungen der Assets wie Breite und Höhe sofort.</li>
<li>Passen Sie Dynamic Media-Vorlagen an, indem Sie Ihre Inhalte aktualisieren und Personalisierungsfelder hinzufügen.</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>Diese Funktion wurde bereits in eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../integrations/aem-dynamic.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Samstag, 23. Mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Zusätzliche ID für ereignisausgelöste Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Journey-Trigger verwenden, indem Sie eine Profilkennung zusammen mit einer anderen Kennung wie einer Bestell-ID, einer Abonnement-ID oder einer verschreibungspflichtigen ID verwenden, sodass sich dasselbe Profil mehrmals gleichzeitig auf derselben Journey befindet. Dies ermöglicht Szenarien wie die parallele Verwaltung mehrerer Bestellungen oder Abonnements, wobei jede Instanz ihrem eigenen Pfad durch die Journey folgt.</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/supplemental-identifier.md">ausführlichen Dokumentation</a>.</p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p>Verfügbarkeitsdatum: Samstag, 23. Mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Inhaltsvarianten simulieren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die zuvor in der Beta-Version verfügbare Simulation von Inhaltsvarianten ist jetzt allgemein verfügbar (GA). Damit können Sie verschiedene Varianten Ihrer Inhalte in der Vorschau sehen, mithilfe von Beispieleingabedaten, die aus einer CSV- oder JSON-Datei hochgeladen oder manuell hinzugefügt wurden. Alle Attribute, die in Ihrem Inhalt für die Personalisierung verwendet werden, werden automatisch vom System erkannt und können für Ihre Tests zur Erstellung mehrerer Varianten verwendet werden.</p>
<p>Diese Funktion wurde bereits in eingeschränkter Verfügbarkeit veröffentlicht und ist jetzt für alle Umgebungen verfügbar. Mit dieser allgemeinen Verfügbarkeit bietet die Funktion jetzt Unterstützung für mehrsprachige Inhalte und Inhaltsexperimente, sodass Sie Varianten über verschiedene Sprachen und Varianten hinweg testen können. Darüber hinaus unterstützt sie jetzt kontextuelle Attribute (zusätzlich zu Profilattributen), was noch dynamischere und situationsbezogener Inhaltstests ermöglicht.</p>
<img src="assets/do-not-localize/variants.gif">
<p>Weitere Informationen finden Sie in der <a href="../test-approve/simulate-sample-input.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Samstag, 23. Mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Synchronisieren des Lesens des Zielgruppen-Zeitplans mit dem Batch-Segmentierungsauftrag</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt nach Abschluss der Batch-Segmentierung tägliche Journey-Ausführungen als Trigger ausführen. Diese Option ist jetzt in täglich geplanten Journey für alle Kunden verfügbar. Damit können Sie für ein Zeitfenster von bis zu 6 Stunden definieren, um auf Zielgruppendaten aus Batch-Segmentierungsvorgängen zu warten. So wird sichergestellt, dass Journey mit den aktuellsten Daten ausgeführt werden oder übersprungen werden, falls sie noch nicht bereit sind.</p>
<p>Diese Funktion wurde bereits in eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/read-audience.md#schedule">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Mittwoch, 20. Mai 2025</p>
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
<p>Mit Journey Optimizer können Sie jetzt über die Standardoptionen hinaus zusätzliche SMS-Anbieter konfigurieren: Sinch, Infobip und Twilio. Mit der Konfiguration benutzerdefinierter SMS-Anbieter können Sie Drittanbieter direkt integrieren, die erweiterte Payload-Anpassung für dynamisches Messaging nutzen und Einverständnisvoreinstellungen (Opt-in/Opt-out) verwalten, um die Einhaltung der Vorgaben sicherzustellen.</p>
<p>Weitere Informationen finden Sie in der <a href="../sms/sms-configuration-custom.md">ausführlichen Dokumentation</a>.</p>
<p>Diese Funktion wurde bereits in eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Verfügbarkeitsdatum: Mittwoch, 20. Mai 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Designs in E-Mail Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt schnell vorab genehmigte Designs anwenden, um die Markenkonsistenz über alle E-Mails hinweg sicherzustellen, den Prozess der Kampagnenerstellung zu beschleunigen und unabhängig hochwertige E-Mails zu erstellen, während Sie gleichzeitig die Abhängigkeit von Design-Teams reduzieren.</p>
<p>Diese Funktion befindet sich derzeit in der Beta-Version und steht nur der Beta-Kundschaft zur Verfügung. Wenden Sie sich an den Adobe-Support, um am Beta-Programm teilzunehmen.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Weitere Informationen finden Sie in der <a href="../email/apply-email-themes.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 14. Mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning - Neuer KI-Formelgenerator</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt spezifische Ranking-Folgen für die Entscheidungsfindung erstellen, indem Sie Kriterien in einer neuen, verbesserten Oberfläche definieren und kombinieren. Anstatt sich nur auf eine statische Angebotspriorität zu verlassen, können Sie benutzerdefinierte Rangfolgeformeln definieren, die KI-Modellbewertungen, Angebotsprioritäten, Profilattribute, Angebotsattribute und kontextuelle Signale über eine geführte Oberfläche kombinieren.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/exd-ranking-formulas.md">ausführlichen Dokumentation</a>.</p>
<p>Verfügbarkeitsdatum: Donnerstag, 14. Mai 2025</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Conflict & prioritization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer, managing the volume and timing of campaigns and journeys is essential to avoid overwhelming customers with too many interactions. Journey Optimizer now offers several tools for conflict management and prioritization - previously available only to limited-access (LA) organizations - that are now generally available (GA).</p>
<p>Previously released in Limited Availability, this capability is now available to all environments. With this General Availability release, the following enhancements have been introduced:</p>
<ul>
<li>Expanded Support: Conflict management tools now support both Unitary Journeys and Audience Qualification Journeys, in addition to Read audience journeys.</li>
<li>Improved Troubleshooting: Two new step event fields are now available in the Query Service, enabling you to analyze why a profile was rejected from a journey or campaign.</li>
<li>Enhanced Reporting: Reports now indicate which specific rule excluded a profile from a journey or campaign, providing greater transparency and actionable insights.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>For more information, refer to the <a href="../conflict-prioritization/gs-conflict-prioritization.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->


<!--table>
<thead>
<tr>
<th><strong>Scale your Experimentation winner</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Scale the Winner enables you to automatically or manually roll out the winning variation of an experiment to your full audience. This feature ensures that, once a top performer is identified, you can maximize its reach and effectiveness without constant manual oversight.</p>
</td>
</tr>
</tbody>
</table-->


### Verbesserungen {#25-05-improv}

Im Folgenden finden Sie die Verbesserungen dieser Version.


* **Neue Unterstützung von Kampagnenobjekten für Sandbox-Kopie** - Verfügbarkeitsdatum: 15. Mai 2025

  Beim Kopieren von Kampagnen über mehrere Sandboxes hinweg mithilfe der Package-Export- und -Importfunktionen werden jetzt auch die folgenden Abhängigkeiten kopiert: Kanalkonfigurationen, Experimentvarianten und -einstellungen, Entscheidungsrichtlinien und Elemente. [Weitere Informationen](../configuration/copy-objects-to-sandbox.md)

  <!--* **Decisioning** - Availability date: May 16, 2025

    Decisioning objects can now be copied between sandboxes, streamlining testing and deployment workflows. [Read more](../configuration/copy-objects-to-sandbox.md#decisioning)-->

* **Ordner für Landingpages** - Verfügbarkeitsdatum: 9. Mai 2025

  Um die Verwaltung Ihrer Landingpages zu vereinfachen, können Sie jetzt Ordner verwenden, um diese effektiver in einer strukturierten Hierarchie zu organisieren. [Weitere Informationen](../landing-pages/manage-lp.md)

* **Briefpost: SSH Key Support for SFTP Connections** - Verfügbarkeitsdatum: 5. Mai 2025

  In der Briefpost-Datei-Routing-Konfiguration können Sie jetzt zusätzlich zum vorhandenen SFTP mit dem Authentifizierungstyp „Passwort“ Ihre Briefpostdatei an einen SFTP-Server mit SSH-Schlüsselauthentifizierung exportieren. [Weitere Informationen](../direct-mail/direct-mail-configuration.md)

* **Pillenaktivierung zur Personalisierung** - Verfügbarkeitsdatum: 5. Mai 2025

  Im Personalisierungseditor wurde die neue Schaltfläche „Pillen“ hinzugefügt. Wenn diese Option aktiviert ist, werden Profil- und kontextuell Attribute als Pillen angezeigt, was die Lesbarkeit Ihres Codes verbessert. [Weitere Informationen](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >Diese Funktion wird in den nächsten 30 Tagen schrittweise in allen Umgebungen eingeführt.

* **Umleitung zur URL-Unterstützung im Web-Kanal** - Verfügbarkeitsdatum: 20. Mai 2025

  Mit dem Journey Optimizer-Webkanal können Sie Besuchende jetzt zu einer anderen bestehenden URL umleiten, anstatt im Visual Editor eine neue Variante zu erstellen. Mit dieser Funktion können Experimente durchgeführt werden, bei denen zwei völlig verschiedene Seiten verglichen werden, anstatt nur einige Elemente innerhalb einer Seite zu ändern. [Weitere Informationen](../web/create-web.md#web-redirect-to-url)

* **Ordner für Vorlagen und Fragmente** - Verfügbarkeitsdatum: 20. Mai 2025

  Mit Ordnern können Sie Ihre Objekte einfacher und effektiver in einer strukturierten Hierarchie organisieren. Ordner, die zuvor für eine Reihe von Organisationen (LA) verfügbar waren, stehen nun allen Benutzenden (GA) zur Verwaltung ihrer Inhaltsvorlagen und Fragmente zur Verfügung. Weitere Informationen finden Sie in den [Inhaltsvorlagen](../content-management/access-content-templates.md#folders) und [Fragmente](../content-management/manage-fragments.md#folders) Abschnitten.

* **Klick-Tracking in E-**-Vorlagen - Verfügbarkeitsdatum: 20. Mai 2025

  Das Klick-Tracking für `<area>` Elemente in Imagemaps im E-Mail-Inhalt wird jetzt nativ in [!DNL Journey Optimizer] unterstützt. Dadurch soll sichergestellt werden, dass Imagemap-Bereiche denselben Tracking-Umbruch, Tracking-Daten und angehängte Parameter wie Standard-Hyperlinks erhalten. [Weitere Informationen zum Nachrichten-Tracking](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **Rechte Leiste in der Kampagnenliste** - Verfügbarkeitsdatum: 20. Mai 2025

  Wenn Sie in der Kampagnenliste eine Kampagne auswählen, wird jetzt ein Bereich mit den zugehörigen Details geöffnet.

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.

* **Decision item attribute support for decisioning rules**
  
  You can now leverage decision item attributes to create decisioning rules.

* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->

