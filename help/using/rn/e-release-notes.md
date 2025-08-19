---
solution: Journey Optimizer
product: journey optimizer
title: Vorab veröffentlichte Versionshinweise zu Journey Optimizer
description: Vorab veröffentlichte Versionshinweise zu Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 75c3db704853b8d2d8920ddd0086681d1fb02a93
workflow-type: ht
source-wordcount: '1033'
ht-degree: 100%

---

# Vorab veröffentlichte Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.


## Vorab-Versionshinweise für August 2025 {#25-8-rn}

**Die nachfolgenden Vorab- Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentationen werden in den Versionshinweisen am Veröffentlichungsdatum veröffentlicht.

Siehe auch [Vorab veröffentlichte Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Veröffentlichungsdatum**: 19. August 2025


### Neue Funktionen {#Aug-25-8-features}

<table>
<thead>
<tr>
<th><strong>Pausieren und Fortsetzen von Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können Ihre Journeys jetzt pausieren und fortsetzen. Diese Funktion gibt Journey-Anwendenden mehr Kontrolle und Flexibilität, da Live-Journeys vorübergehend ausgesetzt werden können, ohne das Kundenerlebnis zu stören. Während der Pause werden keine Nachrichten gesendet und die Profile verbleiben in einem ausgesetzten Zustand, bis die Journey fortgesetzt wird.</p>
<p>Sie können nur eine Journey pausieren und fortsetzen oder Vorgänge zur Massenpause und -fortsetzung von einer Gruppe von Journeys durchführen.</p>
<p>Darüber hinaus können Sie globale Filter auf pausierte Journeys anwenden, um Profile auf der Grundlage ihrer Attribute auszuschließen.</p>
<p><!--img src="assets/do-not-localize/PauseResume.gif"/>--></p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-pause.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Kalenderansicht</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Eine Kalenderansicht ist nun in den Journey- und Kampagnenlisten verfügbar. Damit können Sie alle Journey- und Kampagnenaktivierungen in den jeweiligen Listen visualisieren.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht nun aber für alle Umgebungen zur Verfügung. Im Rahmen dieser allgemein verfügbaren Version bietet die Funktion:</p>
<ul>
<li>Design-Verbesserungen für die Datumsnavigation</li>
<li>Die Möglichkeit, Kampagnenentwürfe anzuzeigen, wenn ein Start- und Enddatum festgelegt wurde</li>
<li>Eine neue Einstellung zum Aus-/Einblenden von Kalenderelementen, die über einen langen Zeitraum ausgeführt werden</li>
</ul>
<p><!--img src="assets/do-not-localize/calendar.gif"/>--></p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-ui.md#journeys-calendar">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dark mode in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Journey Optimizer Email Designer now offers the ability to switch to dark mode view, where you can additionally define specific custom settings that will display only for recipients reading their emails in dark mode.</p>
<p>Note the following:</p>
<ul>
<li>The dark mode final rendering may vary and depends on the recipient's email client.</li>
<li>Not all email clients support custom dark mode. Moreover, some email clients only apply their own default dark mode for all emails that are received. In both cases, the custom settings that you defined in the Email Designer cannot be rendered.</li>
</ul>
<P>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Verwenden von Adobe Experience Platform-Daten für die Personalisierung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verwenden Sie Daten aus Adobe Experience Platform im Personalisierungseditor, um Ihre Inhalte zu personalisieren.  Hierzu müssen Datensätze, die für die Personalisierung der Suche erforderlich sind, zunächst über einen API-Aufruf aktiviert werden. Anschließend können Sie die Daten verwenden, um Ihre Inhalte in [!DNL Journey Optimizer] zu personalisieren.</p>
<p>Diese Funktion wurde zuvor mit eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung. Mit dieser allgemein verfügbaren Version werden die folgenden Verbesserungen eingeführt:</p>
<ul>
<li>Unterstützung eingehender Kanäle</li>
<li>Die Hilfsfunktion „datasetLookup“ kann jetzt in Ausdrücken und visuellen Fragmenten verwendet werden, um Inhalte mithilfe von Daten aus Adobe Experience Platform-Datensätzen zu personalisieren.</li>
<li>Mit einer Option im Datensatz können Sie jetzt Datensätze für die Lookup-Personalisierung aktivieren, ohne dass ein API-Aufruf durchgeführt werden muss.</li>
</ul>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Use Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><img src="assets/do-not-localize/FILE.gif"/></p>
<p><For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey-Pfadoptimierung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer bietet Ihnen jetzt die Tools zur Optimierung Ihrer Journeys, indem Sie KI und Experimentier-Frameworks nutzen und gleichzeitig eine nahtlose Benutzerfreundlichkeit und Unterscheidung zwischen Bedingungs- und Optimierungsfunktionen sicherstellen.</p>
<p>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
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
<p>Journey Optimizer unterstützt eine neue generische Aktionsaktivität, mit der Sie sowohl einzelne als auch eingehende Aktionsgruppen mit mehreren Aktionen konfigurieren können, was eine optimierte Aktionskonfiguration innerhalb der Journey-Arbeitsfläche ermöglicht. Diese neue Funktion ermöglicht insbesondere Folgendes:</p>
<ul>
<li>Eine vereinfachte, native Aktionskonfiguration auf der Journey-Arbeitsfläche</li>
<li>Die Möglichkeit, eingehende Knoten mit mehreren Aktionen zu erstellen</li>
<li>Die Möglichkeit, jeder integrierten Kanalaktion eine Optimierung hinzuzufügen</li>
<li>Die Möglichkeit, jeder Aktion sowohl experimentelle als auch mehrsprachige Optionen hinzuzufügen</li>
</ul>
<p>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Benutzerdefinierte Formulare für Landingpages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Journey Optimizer können Sie jetzt benutzerdefinierte Formulare erstellen und in Landingpages nutzen, um Profilattribute in dem für jedes Formular definierten Datensatz zu erfassen.</p>
<p>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.</p>
<p><!--This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.--></p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>


### Verbesserungen {#Aug-25-8-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.

* **Administration**

   * **Warnhinweise zur Kanalkonfigurationsüberwachung**: Sie können nun Systemwarnhinweise abonnieren – entweder per E-Mail oder im Journey Optimizer-Benachrichtigungszentrum –, falls eine Kanalkonfiguration fehlschlägt oder ein DNS-Eintrag fehlt.

* **Kampagnen**

   * **Ratenkontrolle in ausgehenden Kampagnen**: Sie können nun die Drosselungsratenkontrolle für ausgehende Kampagnen (E-Mail, SMS, Push-Benachrichtigungen) aktivieren, um eine Überlastung nachgelagerter Systeme wie Landingpages oder Kundenunterstützungsplattformen zu verhindern.

   * **Kampagnenplanung für Aktionen**: Die täglichen, wöchentlichen und monatlichen Kampagnenplaner wurden zur Verbesserung der Granularität aktualisiert. Sie können nun beispielsweise die Anzahl der Wochen/Monate zwischen Zeitplänen festlegen, den Tag der Ausführung definieren oder entscheiden, dass eine Kampagne nach einer bestimmten Anzahl von Vorkommen oder an einem bestimmten Datum gestoppt werden soll.

   * **Geplante Transaktionsaktionskampagnen**: Geplante Transaktionsaktionskampagnen sind jetzt zum Senden von zielgruppenbasierten Batch-Transaktionsnachrichten über E-Mail-, SMS- und Push-Kanäle verfügbar.

* **Kanal – Push**

   * **Ablaufdatum für Push-Benachrichtigungen**: Sie können nun für jede Push-Benachrichtigung ein Ablaufdatum angeben, wodurch verhindert wird, dass zeitkritische Nachrichten (z. B. zum Black Friday Sale) nach einem bestimmten Datum gesendet werden, und somit eine schlechte Kundenerfahrung vermieden wird.

* **Kanal – E-Mail**

   * **PDF-Anhänge an E-Mails**: Sie können jetzt statische PDF-Dateien an E-Mails anhängen, die mit Journey Optimizer gesendet werden.

* **Kanal – SMS**

   * **Unpräzises Opt-out**: Wenn diese Option aktiviert ist, erkennt das **unpräzise Opt-out** eingehende Nachrichten, die definierten Opt-out-Schlüsselwörtern sehr ähnlich sind (z. B. „CANCIL“), und sendet automatisch eine Bestätigungsantwort, um die Abmeldeabsicht der Benutzenden zu überprüfen. Wenn Benutzende die Anmeldung über den definierten Prompt bestätigen, wird das Abonnement gekündigt.

     Beachten Sie, dass **Unpräzises Opt-out** nur mit Sinch und Infobip verfügbar ist.

   * **SMS-Verbindung überprüfen**: Sie können nun SMS-API-Anmeldeinformationen in Adobe Journey Optimizer ganz einfach testen und überprüfen, indem eine Beispielnachricht an ein bestimmtes Gerät gesendet wird.

* **Konfiguration**

   * **Unterstützung dynamischer Domains**: Journey Optimizer unterstützt jetzt die Personalisierung bei der Verfolgung von URLs für vordefinierte Domains, die auf der Kanalkonfigurationsebene aufgeführt sind.

   * **Unterstützung benutzerdefinierter Attribute mit einer URL zum Abmelden mit einem Klick**: Bei Journey Optimizer können Sie einen externen, benutzerdefinierten Endpunkt festlegen, indem Sie einen individuellen Link zum Abmelden mit einem Klick in der E-Mail-Konfiguration definieren, wenn das Einverständnis außerhalb von Adobe verwaltet wird. Wenn Ihre Empfängerinnen oder Empfänger auf den Link zum Abmelden klicken, fügt Journey Optimizer standardmäßige profilspezifische Parameter an das Einverständnisaktualisierungsereignis an.

     Um einen Link zum Abmelden mit einem Klick weiter zu personalisieren, können Sie jetzt benutzerdefinierte Attribute definieren, die an das Einverständnisereignis angehängt werden.

* **Entscheidungsfindung**

   * **Anhängen von Fragmenten an Entscheidungselemente**: Journey Optimizer bietet jetzt die Möglichkeit, Fragmente an Entscheidungselemente anzuhängen, die in Code-basierten Erlebniskampagnen über Entscheidungsrichtlinien genutzt werden können.

* **Journeys**

   * **Journey-Massenvorgänge**: Sie können nun mehrere Elemente aus der Liste Ihrer Journeys auswählen. Nach der Auswahl können Sie bis zu 10 Journeys gleichzeitig anhalten oder fortsetzen.
