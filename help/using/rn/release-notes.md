---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: c50553f5a591ae1f462f8162313999424bec533c
workflow-type: tm+mt
source-wordcount: '1715'
ht-degree: 46%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert. [!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.


## Vorab veröffentlichte Versionshinweise August 2025 {#25-8-rn}

**Die nachfolgenden vorab veröffentlichten Versionshinweise können sich bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung ändern**. Links, Screenshots und die aktualisierte Dokumentation werden am Veröffentlichungsdatum veröffentlicht.

Siehe auch [Vorab veröffentlichte Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Veröffentlichungsdatum**: 19. August 2025


### Neue Funktionen {#Aug-25-8-features}

Im Folgenden werden die neuen Funktionen dieser Version beschrieben.

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
<p>Nutzen Sie Daten aus [!DNL Adobe Experience Platform] im Personalisierungseditor, um Ihre Inhalte und Entscheidungsattribute zu personalisieren. Auf diese Weise können Sie insbesondere die Definition Ihrer Attribute auf zusätzliche Daten in Datensätzen erweitern, um Massenaktualisierungen zu ermöglichen, die sich regelmäßig ändern, ohne die Attribute einzeln manuell aktualisieren zu müssen.</p>
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
<p>Journey Optimizer bietet Ihnen jetzt die Tools zur Optimierung Ihrer Journey, indem Sie KI- und Experimentier-Frameworks nutzen und gleichzeitig eine nahtlose Benutzerfreundlichkeit und Unterscheidung zwischen Bedingungs- und Optimierungsfunktionen sicherstellen.</p>
<p>Verwenden Sie die Pfadoptimierung zum Targeting, Experimentieren oder Verwenden von KI, um die Sequenzierung von Kommunikationen, die Zeit zwischen ihnen, Kanalkombinationen und alles, von dem Sie auf der Journey-Arbeitsfläche träumen können, zu bestimmen.</p>
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
<th><strong>Aktionsaktivität in Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer unterstützt eine neue generische Aktionsaktivität, mit der Sie sowohl einzelne als auch eingehende Aktionsgruppen mit mehreren Aktionen konfigurieren können, was eine optimierte Aktionskonfiguration innerhalb der Journey-Arbeitsfläche ermöglicht. Diese neue Funktion ermöglicht insbesondere Folgendes:</p>
<ul>
<li>Eine vereinfachte native Aktionskonfiguration auf der Journey-Arbeitsfläche.</li>
<li>Die Möglichkeit, eingehende Knoten mit mehreren Aktionen zu erstellen.</li>
<li>Die Möglichkeit, jeder integrierten Kanalaktion eine Optimierung hinzuzufügen.</li>
<li>Die Möglichkeit, jeder Aktion sowohl experimentelle als auch mehrsprachige Optionen hinzuzufügen.</li>
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

<table>
<thead>
<tr>
<th><strong>Optimierung in Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ermöglicht Ihnen jetzt das Bereitstellen personalisierter und optimierter Inhalte für die Zielgruppen Ihrer Kampagnen. Sie können Inhaltsexperimente durchführen, regelbasiertes Targeting erstellen und erweiterte Kombinationen aus beiden verwenden, um die Effektivität Ihrer Kampagnen zu maximieren.</p>
<p>Mit der Optimierung können Sie:</p>
<ul>
<li>Mehrere Inhaltsvarianten testen, um das effektivste Messaging zu identifizieren.</li>
<li>Personalisierte Inhalte auf Basis von Benutzerattributen und kontextuellen Daten bereitstellen.</li>
<li>Targeting und Experimente für erweiterte Kampagnenstrategien kombinieren.</li>
<li>Benutzende herausfiltern, die nicht den Variantenkriterien entsprechen.</li>
<li>Fallback-Mechanismen zur Aufrechterhaltung der Benutzerinteraktion sicherstellen.</li>
</ul>
<P>Sobald die Kampagne live ist, werden die Profile anhand der definierten Kriterien bewertet, und basierend auf den passenden Kriterien wird ihnen das entsprechende Erlebnis oder der entsprechende Inhalt aus der Kampagne bereitgestellt.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>Veröffentlichungsdatum: 8. August 2025</p>
<p>Weitere Informationen finden Sie in der <a href="../campaigns/campaigns-message-optimization.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#Aug-25-8-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.

* **Administration**

   * **Warnhinweise zur Kanalkonfigurationsüberwachung** - Sie können jetzt Systemwarnhinweise abonnieren, entweder per E-Mail oder im Journey Optimizer-Benachrichtigungszentrum, falls eine Kanalkonfiguration fehlschlägt oder ein DNS-Eintrag fehlt.

* **Kampagnen**

   * **Ratenkontrolle in ausgehenden Kampagnen** - Sie können jetzt die Drosselungsratenkontrolle für ausgehende Kampagnen (E-Mail, SMS, Push-Benachrichtigungen) aktivieren, um eine Überlastung nachgelagerter Systeme wie Landingpages oder Kundenunterstützungsplattformen zu verhindern.

   * **Kampagnenplanung für Aktionen** - Die täglichen, wöchentlichen und monatlichen Kampagnenplaner wurden aktualisiert, um eine detailliertere Kontrolle über wiederkehrende Zeitpläne zu ermöglichen:

      * **Wöchentliches Intervall**: Sie können die Kampagne jetzt wöchentlich oder alle zwei Wochen wiederholen und die Wochentage auswählen, an denen sie ausgeführt werden soll.

      * **Monatliches Intervall**: Sie können die Kampagne jetzt jeden Monat oder jeden zweiten Monat wiederholen und den Tag des Monats auswählen, an dem sie ausgeführt werden soll.

      * **Tägliche, wöchentliche oder monatliche Zeitpläne** Sie können angeben, ob der wiederkehrende Zeitplan an einem bestimmten Datum oder nach einer bestimmten Anzahl von Vorfällen beendet werden soll.

   * **Geplante Transaktionsaktionskampagnen** - Geplante Transaktionsaktionskampagnen sind jetzt zum Senden von Batch-, zielgruppenbasierten Transaktionsnachrichten über E-Mail-, SMS- und Push-Kanäle verfügbar.

* **Kanal - Push**

   * **Ablaufdatum der Push-Benachrichtigung** - Sie können jetzt für jede Push-Benachrichtigung ein Ablaufdatum angeben, wodurch verhindert wird, dass zeitkritische Nachrichten (z. B. Black Friday Sale) nach einem bestimmten Datum gesendet werden, um so die Bereitstellung schlechter Erlebnisse für Ihre Kunden zu vermeiden.

* **Kanal - E-Mail**

   * **PDF-Anhänge zu E-Mails** - Sie können jetzt statische PDF-Dateien an E-Mails anhängen, die mit Journey Optimizer gesendet werden. Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.

* **Kanal - SMS**

   * **Ungefähres Opt-out** - Wenn diese Option aktiviert ist, erkennt **unscharfe Opt-out** eingehende Nachrichten, die definierten Opt-out-Schlüsselwörtern ähneln (z. B. „CANCIL„), und sendet automatisch eine Bestätigungsantwort, um die Abmeldeabsicht des Benutzers zu überprüfen. Wenn der/die Benutzende die Anmeldung über die definierte Eingabeaufforderung bestätigt, wird das Abonnement gekündigt.

     Beachten Sie, dass **Fuzzy-Opt-out** nur mit Sinch und Infobip verfügbar ist.

   * **SMS-Verbindung überprüfen** - Sie können jetzt Ihre SMS-API-Anmeldeinformationen in Adobe Journey Optimizer einfach testen und überprüfen, indem Sie eine Beispielnachricht an ein bestimmtes Gerät senden.

* **Konfiguration**

   * **Unterstützung dynamischer Domains** - Journey Optimizer unterstützt jetzt die Personalisierung bei der Verfolgung von URLs für vordefinierte Domains, die auf der Kanalkonfigurationsebene aufgeführt sind.

   * **Unterstützung benutzerdefinierter Attribute mit einer Ein-Klick-Abmelde-URL** - Bei Journey Optimizer können Sie einen externen benutzerdefinierten Endpunkt festlegen, indem Sie Ihren eigenen Ein-Klick-Abmelde-Link in der E-Mail-Konfiguration definieren, wenn Sie das Einverständnis außerhalb von Adobe verwalten. Wenn Ihre Empfänger auf den Abmelde-Link klicken, fügt Journey Optimizer einige standardmäßige profilspezifische Parameter an das Einverständnisaktualisierungsereignis an.

     Um Ihren Ein-Klick-Abmelde-Link weiter zu personalisieren, können Sie jetzt benutzerdefinierte Attribute definieren, die an das Einverständnisereignis angehängt werden.

* **Entscheidungsfindung**

   * **Anhängen von Fragmenten an Entscheidungselemente** - Journey Optimizer bietet jetzt die Möglichkeit, Fragmente an Entscheidungselemente anzuhängen, die in Code-basierten Erlebniskampagnen über Entscheidungsrichtlinien genutzt werden können.

* **Journeys**

   * **Journey-Massenvorgänge** - Aus der Liste Ihrer Journeys können Sie jetzt mehrere Elemente auswählen. Nach der Auswahl können Sie bis zu 10 Journey gleichzeitig anhalten oder fortsetzen.

   * **Unterstützung von Umleitungen (302) in benutzerdefinierten Aktionen** - Benutzerdefinierte Aktionen können jetzt HTTP-302-Umleitungen pro Anfrage verarbeiten. Dadurch können Journey-Benutzerinnen und -Benutzer eine Integration mit APIs vornehmen, die Anfragen an lokalisierte oder regionsspezifische URLs umleiten. Weiterleitungen werden automatisch gefolgt, um sicherzustellen, dass der richtige Inhalt ohne zusätzliche Konfiguration bereitgestellt wird.

* **Datensätze**

   * **Experience Decisioning-Objekt-Repository - Personalisierte**: Der integrierte Exportdatensatz erfasst jetzt alle Angebotsattribute und den Lebenszyklusstatus und ermöglicht so eine vollständige Personalisierung und Berichterstellung.

## Kampagnenorchestrierung

**Verfügbarkeitsdatum**: 4. August 2025

Journey Optimizer enthält jetzt die neue Funktion **Kampagnenorchestrierung**, die speziell für markeninitiierte Batch-Kampagnen entwickelt wurde. Diese Version führt eine Arbeitsfläche für die Kampagnenorchestrierung und eine verbesserte Datenmodellierung ein, was es Marketing-Fachleuten ermöglicht, personalisierte Cross-Channel-Kampagnen zu planen, auf eine Zielgruppe anzupassen und bereitzustellen.

>[!IMPORTANT]
>
>Um auf die Kampagnenorchestrierung zugreifen zu können, muss die Lizenz entweder das Paket **Journey Optimizer - Kampagnen und Journey** oder das Paket **Journey Optimizer - Kampagnen** enthalten. Wenden Sie sich an den Adobe-Support, um Ihre Lizenz zu bestätigen und bei Bedarf zu aktualisieren.

![GIF zur Kampagnenorchestrierung](assets/do-not-localize/release.gif)

Dazu gehören [relationale Schemata und Datensätze](#oc-relational) und eine [Kampagnenarbeitsfläche](#oc-canvas). Gemeinsam ermöglichen diese beiden Innovationen einen neuen Standard für die Orchestrierung von Batch-Kampagnen in Journey Optimizer. Die wichtigsten Funktionen sind unten aufgeführt.

### Wichtige Funktionen {#oc-capabilities}

* **Mehrstufige Workflows**

  Fördern Sie anspruchsvolle Multi-Channel-Batch-Kampagnen mit der neuen, speziell entwickelten Arbeitsfläche für die Kampagnenorchestrierung.

* **On-Demand-Zielgruppen**

  Segmentieren Sie Zielgruppen nach Bedarf, um sie sofort zu aktivieren.

* **Segmentierung mehrerer Entitäten**

  Erstellen Sie Zielgruppen auf Grundlage von Geschäftskontexten (Nicht-Personen-Dimensionen) wie Produkten, Ladengeschäften, Erneuerungen, Reservierungen und mehr.

* **Sichtbarkeit vor dem Senden**

  Überprüfen, verfeinern und optimieren Sie Zielgruppen und Kampagnen vor dem Start sowie während er Ausführung von Kampagnen.

### Kampagnenarbeitsfläche {#oc-canvas}

Eine brandneue visuelle Orchestrierungsoberfläche, die speziell für Batch-Kampagnen entwickelt wurde. Diese Arbeitsfläche ermöglicht Folgendes:

* Visuelle Planung von mehrstufigen Multi-Channel-Kampagnenflüssen

* Unterstützung für aus relationalen Abfragen erstellte On-Demand-Zielgruppen

* Erweiterte Zielgruppenaufspaltung, Wartezeiten und bedingte Logik

* Präzise Zählung vor dem Senden nach Anwendung von Geschäftsregeln und Filtern

### Relationale Schemata und Datensätze {#oc-relational}

Adobe Journey Optimizer unterstützt jetzt relationale Entitäten (z. B. Produkte, Geschäfte, Buchungen, Verträge), die mit personenbasierten Profilen verknüpft sind. Dies ermöglicht die Segmentierung und Personalisierung über mehrdimensionale Datenstrukturen hinweg und ermöglicht Anwendungsfälle wie:

* Eine Nachricht pro Buchung, Abonnement oder Vertrag

* Segmentierung basierend auf zugehörigen Entitätsattributen (z. B. Produktkategorie oder Geschäftsstandort)

* Verbesserte Adressierbarkeit (z. B. Senden an alle bekannten, mit einer Entität verknüpften Kontakte)

### Warum dies wichtig ist

Diese Version gibt Marketing-Fachleuten die volle Kontrolle über markeninitiiertes, zielgruppenbasiertes Batch-Marketing, indem sie flexible Datenmodellierung mit einem speziell entwickelten Orchestrierungserlebnis kombiniert. Sie wurde speziell für die Batch-Kampagnenorchestrierung von Echtzeit-Journeys entwickelt und bietet gleichzeitig erweiterte Personalisierung und Skalierbarkeit.

### Weitere Informationen

Weitere Informationen finden Sie in der [Dokumentation zur Kampagnenorchestrierung](../orchestrated/gs-orchestrated-campaigns.md).


