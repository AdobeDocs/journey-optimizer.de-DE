---
solution: Journey Optimizer
product: journey optimizer
title: Vorab veröffentlichte Versionshinweise zu Journey Optimizer
description: Vorab veröffentlichte Versionshinweise zu Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 7f9828c1781468155702d9f8fd475736a7656188
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 47%

---

# Vorab veröffentlichte Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.


## Hinweise zur Vorabversion vom 25. August {#25-8-rn}

**Die unten stehenden Hinweise zu Vorabversionen können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Abbildungen und aktualisierte Dokumentationen werden zum Veröffentlichungsdatum in den Versionshinweisen veröffentlicht.

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
<li>Entwurfsverbesserungen für die Navigation in Datumsangaben,</li>
<li>Die Möglichkeit, Kampagnenentwürfe anzuzeigen, wenn Sie ein Start- und Enddatum festgelegt haben.</li>
<li>Eine neue Einstellung zum Ausblenden und Anzeigen von Kalenderelementen, die über einen langen Zeitraum ausgeführt werden.</li>
</ul>
<p><!--img src="assets/do-not-localize/calendar.gif"/>--></p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-ui.md#journeys-calendar">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Dunkler Modus im E-Mail-Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der E-Mail-Designer von Journey Optimizer bietet jetzt die Möglichkeit, in die Ansicht „Dunkler Modus“ zu wechseln, in der Sie zusätzlich bestimmte benutzerdefinierte Einstellungen definieren können, die nur Empfängerinnen und Empfängern angezeigt werden, die ihre E-Mails im dunklen Modus lesen.</p>
<p>Beachten Sie dabei Folgendes:</p>
<ul>
<li>Das endgültige Rendern des dunklen Modus weicht möglicherweise ab und hängt vom E-Mail-Client der Empfängerinnen und Empfänger ab.</li>
<li>Nicht alle E-Mail-Clients unterstützen einen benutzerdefinierten dunklen Modus. Darüber hinaus wenden einige E-Mail-Clients ausschließlich ihren eigenen standardmäßigen dunklen Modus auf alle empfangenen E-Mails an. In beiden Fällen können die im E-Mail-Designer definierten benutzerdefinierten Einstellungen nicht gerendert werden.</li>
</ul>
<P>Diese Funktion befindet sich derzeit in der Beta-Version und steht nur der Beta-Kundschaft zur Verfügung. Wenden Sie sich an den Adobe-Support, um am Beta-Programm teilzunehmen.</p>
<p><!--img src="assets/do-not-localize/dark-mode.gif"/>--></p>
<p><!--For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

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
<li>Unterstützung eingehender Kanäle,</li>
<li>Die Hilfsfunktion „datasetLookup“ kann jetzt in Ausdrucken und visuellen Fragmenten verwendet werden, um Inhalte mithilfe von Daten aus Adobe Experience Platform-Datensätzen zu personalisieren.</li>
<li>Mit einer Option im Datensatz können Sie jetzt Datensätze für die Lookup-Personalisierung aktivieren, ohne einen API-Aufruf durchführen zu müssen.</li>
</ul>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verwenden der Entscheidungsfindung im E-Mail-Kanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Entscheidungsrichtlinien zu E-Mail-Journeys und -Kampagnen hinzufügen. Entscheidungsrichtlinien sind Container für Angebote, die die Entscheidungs-Engine nutzen, um für jedes Zielgruppenmitglied die besten Inhalte bereitzustellen.</p>
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
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
<p>Journey Optimizer bietet Ihnen jetzt die Tools zur Optimierung Ihrer Journey, indem Sie KI- und Experimentier-Frameworks nutzen und gleichzeitig eine nahtlose Benutzerfreundlichkeit und Unterscheidung zwischen Bedingungs- und Optimierungsfunktionen sicherstellen.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aktionsaktivität in Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer unterstützt eine neue allgemeine Aktionsaktivität, mit der Sie sowohl Einzelaktionen als auch ausgehende Mehrkanal-Aktionen konfigurieren können, was eine optimierte Aktionskonfiguration innerhalb der Journey-Arbeitsfläche ermöglicht. Mit dieser neuen Aktivität können Sie auch Zielgruppenoptimierung, Experimente und mehrsprachige Sprachvarianten zu jeder integrierten Kanalaktion hinzufügen.</p>
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
<p>Diese Funktion befindet sich derzeit in der Beta-Version und steht nur der Beta-Kundschaft zur Verfügung. Wenden Sie sich an den Adobe-Support, um am Beta-Programm teilzunehmen.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>


### Verbesserungen {#Aug-25-8-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.

- **Administration**
   - **Warnhinweise zur Kanalkonfigurationsüberwachung** - Sie können jetzt Systemwarnhinweise abonnieren, entweder per E-Mail oder im Journey Optimizer-Benachrichtigungszentrum, falls eine Kanalkonfiguration fehlschlägt oder ein DNS-Eintrag fehlt.

- **Kampagnen**
   - **Ratenkontrolle in ausgehenden Kampagnen** - Sie können jetzt die Drosselungsratenkontrolle für ausgehende Kampagnen (E-Mail, SMS, Push-Benachrichtigungen) aktivieren, um eine Überlastung nachgelagerter Systeme wie Landingpages oder Kundenunterstützungsplattformen zu verhindern.
   - **Kampagnenplanung für Aktionen** - Die täglichen, wöchentlichen und monatlichen Kampagnenplaner wurden aktualisiert, um die Granularität zu verbessern. Sie können jetzt beispielsweise die Anzahl der Wochen/Monate zwischen zwei Zeitplänen festlegen, den Tag der Ausführung definieren und entscheiden, nach einer bestimmten Anzahl von Vorfällen oder an einem bestimmten Datum zu stoppen.

- **Kanal - Push**
   - **Ablaufdatum der Push-Benachrichtigung** - Sie können jetzt für jede Push-Benachrichtigung ein Ablaufdatum angeben, wodurch verhindert wird, dass zeitkritische Nachrichten (z. B. Black Friday Sale) nach einem bestimmten Datum gesendet werden, um so die Bereitstellung schlechter Erlebnisse für Ihre Kunden zu vermeiden.

- **Kanal - E-Mail**
   - **PDF-Anhänge zu E-Mails** - Sie können jetzt statische PDF-Dateien an E-Mails anhängen, die mit Journey Optimizer gesendet werden.

- **Konfiguration**
   - **Unterstützung dynamischer Domains** - Journey Optimizer unterstützt jetzt die Personalisierung bei der Verfolgung von URLs für vordefinierte Domains, die auf der Kanalkonfigurationsebene aufgeführt sind.
   - **Unterstützung benutzerdefinierter Attribute mit einer Ein-Klick-Abmelde-URL** - Bei Journey Optimizer können Sie einen externen benutzerdefinierten Endpunkt festlegen, indem Sie Ihren eigenen Ein-Klick-Abmelde-Link in der E-Mail-Konfiguration definieren, wenn Sie das Einverständnis außerhalb von Adobe verwalten. Wenn Ihre Empfänger auf den Abmelde-Link klicken, fügt Journey Optimizer einige standardmäßige profilspezifische Parameter an das Einverständnisaktualisierungsereignis an.

     Um Ihren Ein-Klick-Abmelde-Link weiter zu personalisieren, können Sie jetzt benutzerdefinierte Attribute definieren, die an das Einverständnisereignis angehängt werden.

- **Journeys**
   - **Journey-Massenvorgänge** - Aus der Liste Ihrer Journeys können Sie jetzt mehrere Elemente auswählen. Nach der Auswahl können Sie bis zu 10 Journey gleichzeitig anhalten oder fortsetzen.

