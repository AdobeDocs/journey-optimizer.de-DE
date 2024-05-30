---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 40e4aaa93400daf52c96aa5ac2de17151cdbb07f
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 93%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.


## Versionshinweise Mai 2024 {#may-2024}

**Veröffentlichungsdatum**: 21.–22. Mai 2024

### Neue Funktionen {#e-features}

Mit dieser Version werden die unten aufgeführten neue Funktionen eingeführt.


<table>
<thead>
<tr>
<th><strong>Erlebnis-Entscheidung – begrenzte Verfügbarkeit</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Erlebnis-Entscheidung vereinfacht die Personalisierung, indem sie einen zentralisierten Katalog von Marketing-Angeboten, die als „Entscheidungselemente“ bezeichnet werden, und eine ausgereifte Entscheidungs-Engine anbietet. Diese Engine nutzt Regeln und Ranking-Kriterien, um die relevantesten Entscheidungselemente für jeden Kontakt auszuwählen und darzustellen.</p>
<p>Diese Entscheidungselemente sind über den neuen Code-basierten Erlebniskanal, der jetzt in Journey Optimizer-Kampagnen verfügbar ist, nahtlos in eine breite Palette eingehender Oberflächen integriert. Entscheidungsrichtlinien für die Erlebnis-Entscheidung sind nur zur Verwendung in Code-basierten Erlebniskampagnen verfügbar.</p>
<p>Erlebnis-Entscheidung ist derzeit nur für eine Gruppe von Organisationen verfügbar (begrenzte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an Ihren Adobe-Support.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/gs-experience-decisioning.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Personalisierung der E-Mail-Oberfläche - Eingeschränkte Verfügbarkeit</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt beim Erstellen von E-Mail-Kanal-Oberflächen dynamische Subdomains und personalisierte Header-Parameter definieren, um mehr Flexibilität und Kontrolle über Ihre E-Mail-Einstellungen zu erhalten.</p>
<p>Die Personalisierung der E-Mail-Oberfläche ist derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an Ihren Adobe-Support.</p>
<p>Weitere Informationen finden Sie in der <a href="../email/surface-personalization.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Verbesserungen {#e-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Erlebnis-Entscheidung** (begrenzte Verfügbarkeit)

Von der Beta-Version bis hin zu dieser Version wurden die folgenden Verbesserungen hinzugefügt:

* **Erlebnis-Entscheidung und Code-basierte Erlebnisse**: Sie können jetzt die Funktion „Erlebnis-Entscheidung“ nutzen, um Entscheidungselemente in Ihren Code-basierten Kampagnen zu verwenden. Hinweis: Der Code-basierte Erlebniskanal und die Erlebnis-Entscheidung sind nicht für Organisationen verfügbar, die die Zusatzangebote Adobe Healthcare Shield und Privacy and Security Shield erworben haben.  [Weitere Informationen](../code-based/get-started-code-based.md)
* **Kontextdaten**: Sie können jetzt die Kontextdaten von Adobe Experience Platform in Ihren Entscheidungsregeln und Rangfolgeformeln nutzen. [Weitere Informationen](../experience-decisioning/context-data.md)
* **Neue Berechtigung**: Für die Entscheidungs-Management-Ressource ist jetzt die neue Berechtigung „Erlebnis-Entscheidung verwalten“ verfügbar. Sie können damit Berechtigungen im Zusammenhang mit der Erlebnis-Entscheidung verwalten.  [Weitere Informationen](../experience-decisioning/gs-experience-decisioning.md)
* **Begrenzungsregeln**: Sie können jetzt mehrere Begrenzungsregeln für ein bestimmtes Entscheidungselement in der Erlebnis-Entscheidung hinzufügen. Auf diese Weise können Sie die Kontrolle über die Art und Weise, wie Angebote gesendet werden, erhöhen.  [Weitere Informationen](../experience-decisioning/items.md#capping)
* **Reporting**: Sie können jetzt benutzerdefinierte Berichts-Dashboards von Erlebnis-Entscheidungs-Kampagnen mit [!DNL Customer Journey Analytics] erstellen. [Weitere Informationen](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**E-Mail-Kanal**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **Spam-Bewertung** (Beta): Sie können jetzt Ihre Spam-Bewertung von Inhalten in einem speziellen Spam-Bericht überprüfen. Mithilfe von SpamAssassin kann Adobe Journey Optimizer jetzt Ihre E-Mail-Inhalte testen und mit einer Punktzahl versehen, die angibt, ob ISPs oder Mailbox-Anbieter sie als Spam betrachten oder nicht. [Weitere Informationen](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >Diese Funktion befindet sich derzeit in der Beta-Version und steht nur Beta-Kundschaft zur Verfügung. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um am Betaprogramm teilzunehmen.

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**Journeys**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **Unterstützung von mTLS**: Die mTLS-Authentifizierung wird jetzt in benutzerdefinierten Aktionen unterstützt. Es ist keine zusätzliche Konfiguration in der benutzerdefinierten Aktion oder Journey erforderlich, um mTLS zu aktivieren, sondern dies geschieht automatisch, wenn ein mTLS-fähiger Endpunkt erkannt wird. [Weitere Informationen](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **Suchtabellen in Ereignissen**: Sie können jetzt Daten aus einem Lookup-Datensatz nutzen, wenn eine Beziehung mithilfe eines Attributs innerhalb eines Arrays von Objekten definiert wurde. Die Suchwerte sind in Journeys (Bedingungen, benutzerdefinierte Aktionen usw.) und der Nachrichtenpersonalisierung verfügbar. [Weitere Informationen](../event/experience-event-schema.md#relationships_limitations)
* **Erweiterter Ausdruckseditor in der Ereigniskonfiguration** (LA): Sie können jetzt den erweiterten Ausdruckseditor beim Konfigurieren eines Ereignisses nutzen, um komplexere Ausdrücke zu definieren oder Funktionen in der Ereignis-ID-Bedingung zu verwenden. Diese Funktion wird mit begrenzter Verfügbarkeit (Limited Availability, LA) für eine ausgewählte Gruppe von Kundinnen und Kunden veröffentlicht. [Weitere Informationen](../event/about-creating.md)
* **Zusammenführungsrichtlinien** (LA): Zusammenführungsrichtlinien, die von einer Journey verwendet werden, sind jetzt auf der gesamten Journey sichtbar und konsistent. Diese Funktion wird mit begrenzter Verfügbarkeit (Limited Availability, LA) für eine ausgewählte Gruppe von Kundinnen und Kunden veröffentlicht. [Weitere Informationen](../building-journeys/journey-gs.md#merge-policies)

**Globalisierung**

Im Rahmen unserer laufenden Bemühungen um ein einheitliches Benutzererlebnis harmonisieren wir die Terminologie der Adobe Experience Cloud-Produkte und -Apps. Dies wirkt sich auf den deutschen Begriff „Titel“ aus, der in „Label“ geändert wird, wenn er sich auf den Namen eines Objekts bezieht. Die Änderungen werden schrittweise in der Benutzeroberfläche und Dokumentation angewendet.



