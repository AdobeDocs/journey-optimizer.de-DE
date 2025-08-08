---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 378ead41924496f52f22026b3f0e05a9c9c76f89
workflow-type: tm+mt
source-wordcount: '1428'
ht-degree: 33%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert. [!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.


## Kampagnenorchestrierung

**Verfügbarkeitsdatum**: 4. August 2025

Journey Optimizer enthält jetzt **Kampagnenorchestrierung**, eine neue Funktion, die speziell für markeninitiierte Batch-Kampagnen entwickelt wurde. Diese Version führt eine Arbeitsfläche für die Kampagnenorchestrierung und eine verbesserte Datenmodellierung ein, die es Marketing-Experten ermöglichen, personalisierte Cross-Channel-Kampagnen zu planen, anzusprechen und bereitzustellen.

![Kampagnenorchestrierung GIF](assets/do-not-localize/release.gif)

Sie enthält [Relationale Schemata und Datensätze](#oc-relational) und [Campaign-Arbeitsfläche](#oc-canvas). Gemeinsam setzen diese beiden Innovationen einen neuen Standard für die Orchestrierung von Batch-Kampagnen in Journey Optimizer. Die wichtigsten Funktionen sind unten aufgeführt.

### Wichtigste Funktionen {#oc-capabilities}

* **Mehrstufige Workflows**

  Fördern Sie anspruchsvolle Multi-Channel-Batch-Kampagnen mit der neuen, speziell entwickelten Arbeitsfläche für die Kampagnenorchestrierung.

* **On-Demand-Zielgruppen**

  Segmentieren Sie Zielgruppen nach Bedarf, um sie sofort zu aktivieren.

* **Segmentierung mehrerer Entitäten**

  Erstellen Sie Zielgruppen mithilfe von Geschäftskontexten (Nicht-Personen-Dimensionen) wie Produkten, Geschäften, Erneuerungen, Reservierungen und mehr.

* **Sichtbarkeit vor dem Senden**

  Audiences und Kampagnen vor und während der Ausführung von Kampagnen überprüfen, verfeinern und optimieren

### Kampagnen-Arbeitsfläche {#oc-canvas}

Eine brandneue visuelle Orchestrierungsschnittstelle, die speziell für Batch-Kampagnen entwickelt wurde. Diese Arbeitsfläche ermöglicht Folgendes:

* Visuelle Planung von mehrstufigen, kanalübergreifenden Kampagnenflüssen

* Unterstützung für On-Demand-Zielgruppen, die aus relationalen Abfragen erstellt wurden

* Erweiterte Zielgruppenteilung, Wartezeiten und bedingte Logik

* Präzise Anzahl der Vorabsendungen nach Anwendung von Geschäftsregeln und Filtern

### Relationale Schemata und Datensätze {#oc-relational}

Adobe Journey Optimizer unterstützt jetzt relationale Entitäten (z. B. Produkte, Geschäfte, Buchungen, Verträge), die mit personenbasierten Profilen verknüpft sind. Dies ermöglicht die Segmentierung und Personalisierung über mehrdimensionale Datenstrukturen hinweg und ermöglicht Anwendungsfälle wie:

* Eine Nachricht pro Buchung, Abonnement oder Vertrag

* Segmentierung basierend auf zugehörigen Entitätsattributen (z. B. Produktkategorie oder Store-Standort)

* Verbesserte Adressierbarkeit (z. B. Senden an alle bekannten Kontakte, die mit einer Entität verknüpft sind)

### Warum es wichtig ist

Diese Version gibt Marketing-Experten die volle Kontrolle über markeninitiiertes, zielgruppenbasiertes Batch-Marketing, indem sie flexible Datenmodellierung mit einem speziell entwickelten Orchestrierungserlebnis kombiniert. Er wurde speziell für die Batch-Kampagnenorchestrierung von Echtzeit-Journey-Kampagnen entwickelt und bietet gleichzeitig erweiterte Personalisierung und Skalierbarkeit.

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
<p>Mit Journey Optimizer können Sie jetzt personalisierte und optimierte Inhalte für die Zielgruppen Ihrer Kampagnen bereitstellen, indem Sie Inhaltsexperimente durchführen, regelbasiertes Targeting erstellen und erweiterte Kombinationen aus beiden verwenden können, um die Effektivität Ihrer Kampagnen zu maximieren.</p>
<p>Mit der Optimierung können Sie:</p>
<ul>
<li>Testen Sie mehrere Inhaltsvarianten, um die effektivste Botschaft zu identifizieren.</li>
<li>Stellen Sie personalisierte Inhalte auf der Basis von Benutzerattributen und kontextuellen Daten bereit.</li>
<li>Kombinieren Sie Targeting und Experimentieren für erweiterte Kampagnenstrategien.</li>
<li>Filtern Sie Benutzer heraus, die nicht den Variantenkriterien entsprechen.</li>
<li>Fallback-Mechanismen zur Aufrechterhaltung der Benutzerinteraktion sicherstellen.</li>
</ul>
<P>Sobald die Kampagne live ist, werden Profile anhand der definierten Kriterien bewertet und auf der Grundlage übereinstimmender Kriterien mit dem entsprechenden Erlebnis oder Inhalt aus der Kampagne bereitgestellt.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>Veröffentlichungsdatum: 8. August 2025</p>
<p>Weitere Informationen finden Sie in der <a href="../campaigns/campaigns-message-optimization.md">detaillierten Dokumentation</a></p>
</td>
</tr>
</tbody>
</table>



## Versionshinweise Juli &#39;25 {#25-7-rn}

**Veröffentlichungsdatum**: Mittwoch, 29. Juli 2025

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
<p>Sie können nun Ihre eigenen Marken erstellen und anpassen, um Ihre visuelle und verbale Identität in der gesamten Kommunikation klar zu definieren. Über den Markenausrichtungswert erhalten Sie Echtzeit-Feedback dazu, wie gut Ihr Inhalt den Ton, den Stil und die Richtlinien Ihrer Marke widerspiegelt. So können Sie sicherstellen, dass jede gesendete Nachricht markenkonform ist.</p>
<p>Diese Funktion wurde bereits in Beta veröffentlicht und ist jetzt für alle Umgebungen verfügbar (allgemeine Verfügbarkeit).</p>
<p><img src="assets/do-not-localize/brand-score.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../content-management/brands.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verwenden von Decisioning im E-Mail-Kanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Entscheidungsrichtlinien zu E-Mail-Journey und -Kampagnen hinzufügen. Entscheidungsrichtlinien sind Container für Ihre Angebote, die die Decisioning-Engine nutzen, um dynamisch die besten Inhalte zurückzugeben, die für jedes Mitglied der Zielgruppe bereitgestellt werden können.</p>
<p>Diese Funktion ist nur in begrenztem Umfang verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.</p>
Weitere Informationen finden Sie in der <a href="../experience-decisioning/create-decision.md">detaillierten Dokumentation</a></p>
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
<p>Zuvor nur auf Anfrage verfügbar, ist der LINE-Kanal jetzt für alle Benutzer verfügbar (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../line/get-started-line.md">ausführlichen Dokumentation</a>.</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Probelauf</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der Journey-Probelauf ist ein spezieller Journey-Veröffentlichungsmodus in Adobe Journey Optimizer, der es Journey-Anwendenden ermöglicht, eine Journey mit echten Produktionsdaten zu testen, ohne echte Kundinnen und Kunden zu kontaktieren oder Profilinformationen zu aktualisieren. Mit dieser Funktion können Journey-Anwendende Vertrauen in ihr Journey-Design und die Zielgruppenbestimmung gewinnen, bevor sie die Journey live veröffentlichen.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Diese Funktion wurde zuvor mit eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/journey-dry-run.md">detaillierten Dokumentation</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Zusätzliche ID für Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können nun Journeys auslösen, indem Sie eine Profilkennung zusammen mit einer anderen Kennung wie einer Bestell-, Abonnement- oder Rezept-ID verwenden, sodass dasselbe Profil mehrmals in derselben Journey vorhanden sein kann. Dies ermöglicht Szenarien wie die parallele Verwaltung mehrerer Bestellungen oder Abonnements, wobei jede Instanz ihrem eigenen Pfad durch die Journey folgt.</p>
<p>Die Verwendung zusätzlicher IDs in Journey wurde früher nur eingeschränkt verfügbar gemacht und ist jetzt für alle Umgebungen verfügbar. Mit dieser allgemeinen Verfügbarkeitsversion bietet die Funktion jetzt Unterstützung für Journey unter Zielgruppe lesen .</p>
<p><img src="assets/do-not-localize/gif-supplemental.gif"/></p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/supplemental-identifier.md">detaillierten Dokumentation</a></p>
</td>
</tr>
</tbody>
</table>

### Warnhinweise im Produkt

Sie können jetzt **E-Mail- und produktinterne Warnhinweise** für Journey Optimizer-Produktversionen abonnieren.

Abonnieren:

* Zu **Adobe Experience Cloud-Voreinstellungen navigieren**
* Suchen **unter &quot;**&quot; nach **Journey Optimizer-Neuversionen**
* Aktivieren von In-App- und E-Mail-Benachrichtigungen

![](assets/do-not-localize/pulse-notif.png){width="70%" align="left"}


### Änderung bei den Journey-Bedingungen {#ee-change@}

Seit dem 8. Juli wird das Erstellen von Ausdrücken mit Erlebnisereignissen in neuen Kundenorganisationen in dem in Journey-Bedingungen verwendeten Ausdruckseditor nicht mehr unterstützt. Daher können Erlebnisereignisse in der [Experience Platform-Datenquelle](../datasource/adobe-experience-platform-data-source.md) nicht zum Erstellen von Ausdrücken verwendet werden. Alternative Ansätze und Best Practices zum Erstellen von Ausdrücken/Logik mit Erlebnisereignissen sind [hier](../building-journeys/exp-event-lookup.md) zu finden.

Der Zugriff auf Journey-Kontextereignisdaten in unitären Journeys wird nicht geändert. In den Ausdrucks- und Personalisierungseditoren können Benutzende weiterhin auf Daten zugreifen, die mit dem ersten Journey-Ereignis übergeben wurden.

Weitere Informationen finden Sie [in diesen FAQ](../building-journeys/exp-event-lookup.md#faq-ee).

### Verbesserungen {#25-7-improv}

Im Folgenden sind die Verbesserungen dieser Version aufgeführt.

* **Kampagnen**

   * **Mehrere eingehende Aktionen in Kampagnen** - Um die Kampagnenorchestrierung zu vereinfachen, können jetzt mehrere eingehende Aktionen in einer einzelnen Kampagne definiert werden. Mit dieser Funktion können Sie mehrere Code-basierte Erlebnisse, In-App-Nachrichten, Inhaltskarten oder Web-Aktionen gleichzeitig an verschiedenen Orten bereitstellen, wobei jede Aktion einen bestimmten Inhalt enthält.
     [Weitere Informationen](../campaigns/campaign-action.md#multi-action)

   * **Neuorganisation des Kampagnenbestands** - Geplante und API-ausgelöste Kampagnen sind jetzt im Kampagneninventar in separate Registerkarten unterteilt, um die Navigation und Verwaltung zu erleichtern.

[Mehr dazu](../campaigns/modify-stop-campaign.md)

* **Daten-Management**
   * **Aktualisierung der Systemdatensätze des Entscheidungs-Managements** - Die gelöschten personalisierten Angebote und Fallback-Angebote sind jetzt in den Datensätzen „decision_object_repository_personalized_offers“ und „decision_object_repository_fallback_offers“ als archiviert gekennzeichnet. Die vorhandenen Datensätze im Datensatz werden nicht geändert.

[Mehr dazu](../offers/export-catalog/access-dataset.md)

* **Journeys**
   * **Verbesserungen beim Journey der Sandbox-Tools** - Beim Kopieren von Journeys über mehrere Sandboxes hinweg mithilfe der Paketexport- und -importfunktionen sind jetzt auch die folgenden Funktionen verfügbar:
      * Auswählen eines vorhandenen Ereignisses am Ziel
      * Kopieren eines Ereignisses unabhängig von einer Journey
      * Erkennen von Feldergruppen-/Datenquellenbeziehungen, Verknüpfen mit ihnen am Ziel, wenn sie vorhanden sind, Erstellen von ihnen, wenn sie nicht vorhanden sind.

[Mehr dazu](../configuration/copy-objects-to-sandbox.md)

* **Kanal - In-App**
   * **In-App-Schlüssel/Wert-Paare** - Bei In-App-Nachrichten können Sie Schlüssel- und Wert-Paare definieren, um benutzerdefinierte Variablen in die Nachrichten-Payload aufzunehmen. Diese Schlüssel-Wert-Paare ermöglichen es Ihnen, zusätzliche Daten basierend auf Ihrer spezifischen Konfiguration und Ihrem Anwendungsfall zu übergeben. [Weitere Informationen](../in-app/design-in-app.md)

* **Kanal - Inhaltskarte**

   * **Regelbasierte Kampagnendisqualifizierung** - Bei der Bearbeitung zusätzlicher Versandregeln wurde die Option Vorherige Versandregeln durch drei verschiedene Regeltypen ersetzt, um den Zeitpunkt und die Sichtbarkeit der Nachricht besser zu steuern:
      * Nachricht anzeigen, wenn: Bedingungen, die bestimmen, wann die Inhaltskarte angezeigt wird.
      * Nachricht schließen, wenn: Bedingungen, die die Inhaltskarte vorübergehend ausblenden. Sie kann erneut angezeigt werden, wenn die Anzeigebedingungen erneut erfüllt sind.
      * Nachricht disqualifizieren, wenn: Bedingungen, die dauerhaft verhindern, dass die Inhaltskarte erneut angezeigt wird.

[Mehr dazu](../content-card/design-content-card.md)

* **Entscheidungsfindung**
   * **Migrations-Tool-APIs** - Das Journey Optimizer-Team arbeitet derzeit an Migrations-Tool-APIs, um Entscheidungs-Management-Entitäten in das Decisioning zu migrieren. Diese Tools ermöglichen eine nahtlose Migration zwischen Sandboxes mit Funktionen zur Abhängigkeitsauflösung und zum Rollback. Wenden Sie sich bei Interesse an Ihren Adobe-Support-Mitarbeiter.

* **Personalisierung**
   * Eine neue Hilfsfunktion, „SHA256“, wurde zum Personalisierungseditor hinzugefügt. Diese Funktion wird verwendet, um den sha256-Hash einer Zeichenfolge zu berechnen und zurückzugeben.

[Mehr dazu](../personalization/functions/string.md#sha256)
