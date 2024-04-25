---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Frühzeitige Versionshinweise zu Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: be758a577dbff2ae400d0642f9e898b423353f90
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 44%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise April 2024 {#e-2024}

**Veröffentlichungsdatum**: Mittwoch, 30. April 2024

### Neue Funktion {#e-features}

Mit dieser Version werden die neuen Funktionen eingeführt, die nachfolgend beschrieben werden.

<!--table>
<thead>
<tr>
<th><strong>Business rules - Private Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>It is now possible to create and apply rule sets to your marketing communications.  </p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Experience Decisioning - begrenzte Verfügbarkeit</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experience Decisioning vereinfacht die Personalisierung, indem es einen zentralisierten Katalog von Marketing-Angeboten, die als „Entscheidungselemente“ bezeichnet werden und eine ausgereifte Entscheidungs-Engine anbietet. Diese Engine nutzt Regeln und Ranking-Kriterien, um die relevantesten Entscheidungselemente für jeden Kontakt auszuwählen und darzustellen.</p>
<p>Diese Entscheidungselemente sind über den neuen code-basierten Erlebniskanal, der jetzt in Journey Optimizer-Kampagnen verfügbar ist, nahtlos in eine breite Palette eingehender Oberflächen integriert. Entscheidungsrichtlinien für Erlebnisentscheidungen stehen nur in code-basierten Erlebniskampagnen zur Verfügung.</p>
<p>Experience Decisioning ist derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff zu erhalten.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Personalization - Local Lookups - Multi-Entity Support - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>TBD</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Multimedia Message Service (MMS) - alle Anbieter</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dem SMS-Kanal können Sie Ihre Kommunikation jetzt verbessern, indem Sie MMS-Nachrichten (Multimedia Message Service) senden, sodass Sie Bilder, GIFs oder Videos mit Ihren Kundinnen und Kunden teilen können. Anfangs nur mit Sinch verfügbar, MMS ist jetzt auch mit Infobip und Twilio verfügbar.</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the AI assistant. You can now use the AI assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow - LA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now easily perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel surfaces, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### Verbesserungen {#e-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

<!--
* **Experience Decisioning + Code-based experiences (LA)**: You can now leverage the Experience decisioning feature to use decision items in your code-based campaigns. Note: The Code-based experience channel and Experience decisioning are not available for organizations that have purchased the Adobe Healthcare Shield and Privacy and Security Shield add-on offerings.
-->
<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**Entscheidungs-Management**

* Die **Änderungsprotokoll** -Tab, in dem alle Änderungen angezeigt werden, die an einem Angebot oder einer entfernten Entscheidung vorgenommen wurden. Änderungen im Zusammenhang mit Angeboten und Entscheidungen sind jetzt im Abschnitt **Prüfungen** Menü.

**Erlebnisentscheidung**

Von Beta bis LA wurden die folgenden Verbesserungen hinzugefügt:

* Sie können jetzt Kontextdaten aus Adobe Experience Platform in Ihren Entscheidungsregeln mit der **Kontextdaten** Registerkarte.
* Für die Ressource &quot;Entscheidungsverwaltung&quot;ist jetzt die neue Berechtigung &quot;Erlebnisentscheidungen verwalten&quot;verfügbar. Sie können damit Berechtigungen im Zusammenhang mit Experience Decisioning verwalten.
* Sie können jetzt mehrere Begrenzungsregeln für ein Angebot hinzufügen. Auf diese Weise können Sie die Kontrolle über die Art und Weise, wie Angebote gesendet werden, erhöhen.
* Sie können jetzt mehrere Begrenzungsregeln für ein bestimmtes Entscheidungselement in Experience Decisioning hinzufügen. Auf diese Weise können Sie die Kontrolle über die Art und Weise, wie Angebote gesendet werden, erhöhen.
* Sie können jetzt benutzerdefinierte Berichterstellungs-Dashboards von Experience Decisioning-Kampagnen erstellen, indem Sie [!DNL Customer Journey Analytics].

**Journeys**

* **Verbesserter Journey Designer**

   * Die verbesserte Arbeitsfläche bietet ein intuitiveres und effizienteres Benutzererlebnis.
   * Aktivitäten sind klarer und enthalten mehr Informationen auf der Journey-Arbeitsfläche mit weniger Klicks.

* **Neue Live-Berichterstellung**: Die letzten 24 Stunden Journey-Berichte sind jetzt direkt auf der Journey-Arbeitsfläche verfügbar.

**Konfiguration**

* Jetzt können Sie eine Marketing-Aktion auf der Ebene der Kanaloberfläche auswählen. Bei Verwendung in einer Oberfläche werden alle mit dieser Marketing-Aktion verknüpften Zustimmungsrichtlinien genutzt, um die Voreinstellungen Ihrer Kundinnen und Kunden zu respektieren.
* Die Verwendung der Zugriffssteuerung auf Objektebene ist jetzt für Kanaloberflächen verfügbar.

