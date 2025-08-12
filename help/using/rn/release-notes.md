---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 4510cfde1579fbabe7deb1289f70f13ee21a3d4a
workflow-type: tm+mt
source-wordcount: '1460'
ht-degree: 96%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert. [!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.


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

<!--
## August '25 pre release notes {#25-7-rn}

**Pre release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: August 19, 2025


### New capabilities {#Aug-25-8-features}

New capabilities coming with this release are detailed below.

### Improvements {#Aug-25-8-improv}

Improvements coming with this release are listed below.
-->

## Updates vom 25. August {#25.8-rn}

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



## Versionshinweise Juli 2025 {#25-7-rn}

**Veröffentlichungsdatum**: 29. Juli 2025

### Neue Funktionen {#features-25-7}

Im Folgenden werden die neuen Funktionen dieser Version beschrieben.

#### Funktionen

<table>
<thead>
<tr>
<th><strong>Marken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Ihre eigenen Marken erstellen und anpassen, um Ihre visuelle und verbale Identität in der gesamten Kommunikation klar zu definieren. Der Markenausrichtungswert liefert Ihnen Echtzeit-Feedback dazu, wie gut Ihr Inhalt den Ton, den Stil und die Richtlinien Ihrer Marke widerspiegelt. So wird sichergestellt, dass alle von Ihnen versendeten Nachrichten markenkonform sind.</p>
<p>Diese Funktion wurde zuvor als Beta-Version veröffentlicht, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p><img src="assets/do-not-localize/brand-score.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../content-management/brands.md">ausführlichen Dokumentation</a>.</p>
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
<p>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.</p>
Weitere Informationen finden Sie in der <a href="../experience-decisioning/create-decision.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>LINE-Kanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer hat seine kanalübergreifenden Funktionen um die Unterstützung des LINE-Kanals erweitert. Diese Verbesserung ermöglicht es Ihnen, LINE-Erlebnisse zu erstellen, zu bearbeiten und in der Vorschau anzuzeigen, was eine stärker personalisierte und ansprechendere Interaktion ermöglicht. Mit LINE können Sie mit mehr Kundinnen und Kunden in Kontakt treten, relevante Inhalte versenden und Ihre Interaktion verbessern.</p>
<p>Der LINE-Kanal war zuvor nur auf Anfrage verfügbar, steht aber nun allen Benutzenden zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../line/get-started-line.md">ausführlichen Dokumentation</a>.</p></td>
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
<p>Der Journey-Probelauf ist ein spezieller Journey-Veröffentlichungsmodus in Adobe Journey Optimizer, der es Journey-Anwendenden ermöglicht, eine Journey mit echten Produktionsdaten zu testen, ohne echte Kundinnen und Kunden zu kontaktieren oder Profilinformationen zu aktualisieren. Mit dieser Funktion können Journey-Anwendende Vertrauen in ihr Journey-Design und die Zielgruppenbestimmung gewinnen, bevor sie die Journey live veröffentlichen.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Diese Funktion war zuvor nur eingeschränkt verfügbar, steht aber nun für alle Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/journey-dry-run.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Zusätzliche ID für Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können nun Journeys auslösen, indem Sie eine Profilkennung zusammen mit einer anderen Kennung wie einer Bestell-, Abonnement- oder Rezept-ID verwenden, sodass dasselbe Profil mehrmals in derselben Journey vorhanden sein kann. Dies ermöglicht Szenarien wie die parallele Verwaltung mehrerer Bestellungen oder Abonnements, wobei jede Instanz ihrem eigenen Pfad durch die Journey folgt.</p>
<p>Die Verwendung zusätzlicher IDs in Journeys war zuvor nur eingeschränkt verfügbar, steht nun aber für alle Umgebungen zur Verfügung. Im Rahmen dieser allgemein verfügbaren Version bietet diese Funktion nun Unterstützung für Journeys des Typs „Zielgruppe lesen“.</p>
<p><img src="assets/do-not-localize/gif-supplemental.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/supplemental-identifier.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Warnhinweise im Produkt

Sie können nun **E-Mail- und Warnhinweise im Produkt** für Journey Optimizer-Produktversionen abonnieren.

So abonnieren Sie sie:

* Navigieren Sie zu den **Voreinstellungen für Adobe Experience Cloud**.
* Suchen Sie unter **Benachrichtigungen** nach **neuen Versionen von Journey Optimizer**
* Aktivieren von In-App- und E-Mail-Benachrichtigungen

![](assets/do-not-localize/pulse-notif.png){width="70%" align="left"}


### Änderung bei den Journey-Bedingungen {#ee-change@}

Seit dem 8. Juli wird das Erstellen von Ausdrücken mit Erlebnisereignissen in neuen Kundenorganisationen in dem in Journey-Bedingungen verwendeten Ausdruckseditor nicht mehr unterstützt. Daher können Erlebnisereignisse in der [Experience Platform-Datenquelle](../datasource/adobe-experience-platform-data-source.md) nicht zum Erstellen von Ausdrücken verwendet werden. Alternative Ansätze und Best Practices zum Erstellen von Ausdrücken/Logik mit Erlebnisereignissen sind [hier](../building-journeys/exp-event-lookup.md) zu finden.

Der Zugriff auf Journey-Kontextereignisdaten in unitären Journeys wird nicht geändert. In den Ausdrucks- und Personalisierungseditoren können Benutzende weiterhin auf Daten zugreifen, die mit dem ersten Journey-Ereignis übergeben wurden.

Weitere Informationen finden Sie [in diesen FAQ](../building-journeys/exp-event-lookup.md#faq-ee).

### Verbesserungen {#25-7-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.

* **Kampagnen**

   * **Mehrere eingehende Aktionen in Kampagnen**: Um die Kampagnenorchestrierung zu vereinfachen, können Sie jetzt mehrere eingehende Aktionen in einer einzigen Kampagne definieren. Mit dieser Funktion können Sie mehrere Code-basierte Erlebnisse, In-App-Nachrichten, Inhaltskarten oder Web-Aktionen gleichzeitig an verschiedenen Orten bereitstellen, wobei jede Aktion einen bestimmten Inhalt enthält.
     [Weitere Informationen](../campaigns/campaign-action.md#multi-action)

   * **Neuorganisation des Kampagneninventars**: Geplante und API-ausgelöste Kampagnen sind jetzt im Kampagneninventar zur leichteren Navigation und Verwaltung in separate Registerkarten unterteilt.

[Mehr dazu](../campaigns/modify-stop-campaign.md)

* **Daten-Management**
   * **Aktualisierung der Systemdatensätze des Entscheidungs-Managements**: Die gelöschten personalisierten Angebote und Fallback-Angebote werden jetzt in den Datensätzen „decision_object_repository_personalized_offers“ und „decision_object_repository_fallback_offers“ als archiviert gekennzeichnet. Die vorhandenen Einträge im Datensatz werden nicht geändert.

[Mehr dazu](../offers/export-catalog/access-dataset.md)

* **Journeys**
   * **Verbesserungen an den Sandbox-Tools von Journeys**: Beim Kopieren von Journeys über mehrere Sandboxes hinweg mithilfe der Paketexport- und -importfunktionen sind jetzt auch die folgenden Funktionen verfügbar:
      * Auswählen eines vorhandenen Ereignisses am Ziel
      * Kopieren eines Ereignisses unabhängig von einer Journey
      * Erkennen von Feldergruppen-/Datenquellenbeziehungen und Verknüpfen dieser am Ziel, wenn sie vorhanden sind bzw. Erstellen dieser, wenn sie nicht vorhanden sind

[Mehr dazu](../configuration/copy-objects-to-sandbox.md)

* **Kanal: In-App**
   * **In-App-Schlüssel-Wert-Paare**: Bei In-App-Nachrichten können Sie Schlüssel-Wert-Paare definieren, um benutzerdefinierte Variablen in die Nachrichten-Payload einzuschließen. Diese Schlüssel-Wert-Paare ermöglichen es Ihnen, zusätzliche Daten basierend auf Ihrer spezifischen Konfiguration und Ihrem Anwendungsfall zu übergeben. [Weitere Informationen](../in-app/design-in-app.md)

* **Kanal: Inhaltskarte**

   * **Regelbasierte Kampagnendisqualifizierung**: Für die Bearbeitung zusätzlicher Versandregeln wurde die frühere Versandregeloption durch drei verschiedene Regeltypen ersetzt, um den Zeitpunkt und die Sichtbarkeit von Nachrichten besser zu steuern:
      * „Meldung anzeigen, wenn“: Bedingungen, die bestimmen, wann die Inhaltskarte angezeigt wird.
      * „Meldung verwerfen, wenn“: Bedingungen, die die Inhaltskarte vorübergehend ausblenden. Sie kann erneut angezeigt werden, wenn die Anzeigebedingungen wieder erfüllt sind.
      * „Meldung disqualifizieren, wenn“: Bedingungen, die dauerhaft verhindern, dass die Inhaltskarte erneut angezeigt wird.

[Mehr dazu](../content-card/design-content-card.md)

* **Entscheidungsfindung**
   * **Migration-Tooling-APIs**: Das Journey Optimizer-Team arbeitet derzeit an Migration-Tooling-APIs, um Entitäten für das Entscheidungs-Management in die Entscheidungsfindung zu migrieren. Diese Tools ermöglichen eine nahtlose Migration zwischen Sandboxes mit Funktionen zur Abhängigkeitsauflösung und zum Rollback. Wenden Sie sich bei Interesse an den Adobe-Support.

* **Personalisierung**
   * Im Personalisierungseditor wurde die neue Hilfsfunktion „SHA256“ hinzugefügt. Diese Funktion wird verwendet, um den SHA256-Hash einer Zeichenfolge zu berechnen und zurückzugeben.

[Mehr dazu](../personalization/functions/string.md#sha256)
