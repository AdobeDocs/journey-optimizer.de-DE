---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: fec6b15db9f8e6b2a07b55bc9e8fc4d9cb0d73d7
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 60%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.


## Versionshinweise für Juni 2024 {#24-6-2024}

**Frühe Versionshinweise unten können ohne vorherige Ankündigung bis zum Verfügbarkeitsdatum der Version geändert werden**.

**Veröffentlichungsdatum**: 18.–19. Juni 2024

### Neue Funktionen {#june-24-features}

Mit dieser Version werden die unten aufgeführten neue Funktionen eingeführt.

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


<!--<table>
<thead>
<tr>
<th><strong>Content Fragments customization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define specific fields in a fragment that can be edited when the fragment is added to a campaign or journey. This allows for the adjustment of content portions at the time of use, providing flexibility to override default values with context-specific details.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->




<table>
<thead>
<tr>
<th><strong>Berichterstellung mit Customer Journey Analytics (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Journey Optimizer-Berichterstellung ist nun vollständig in Customer Journey Analytics-Funktionen integriert, wodurch die Berichterstellung plattformübergreifend standardisiert und die Datenkonsistenz und -zuverlässigkeit verbessert wird. Diese nahtlose Integration zwischen Journey Optimizer und Customer Journey Analytics bietet einen klareren Überblick über Leistungsmetriken und ermöglicht es Benutzern, fundiertere Entscheidungen zu treffen.</p>
<p>Weitere Informationen finden Sie in der <a href="../reports/report-gs-cja.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>KI-Assistent in Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der KI-Assistent ist eine Funktion der Benutzeroberfläche, mit der Sie durch Adobe-Konzepte navigieren und diese verstehen und operative Erkenntnisse zu Ihrer spezifischen Umgebung erhalten können. Er ist in verschiedenen Produkten in Adobe Experience Cloud verfügbar, einschließlich Adobe Journey Optimizer.</p>
<p>Weitere Informationen finden Sie in der <a href="../start/ai-assistant.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now effortlessly create content in multiple languages within a single campaign or journey. With this feature, you can switch between languages when editing your campaign or your journey, streamlining the entire editing process and improving your capability to efficiently manage multilingual content.</p>
<p>Multilingual content is currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Experimentation in journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Already available in campaigns, Adobe Journey Optimizer now supports experiments in journeys. Experiments are randomized trials, which in the context of online testing, means that you expose some randomly selected users to a given variation of a message, and another randomly selected set of users to some other variation or treatment. After exposure, you can then measure the outcome metrics you are interested in, such as opens of emails, subscriptions, or purchases.</p>
<p>Experimentation in journeys is currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
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

### Verbesserungen {#june24-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.


**Entscheidungs-Management**

* **Unterstützung mehrerer Regeln im Entscheidungs-Management**: Sie können jetzt bis zu 10 Begrenzungsregeln für ein bestimmtes Angebot im Entscheidungs-Management hinzufügen. Dadurch wird eine bessere Kontrolle über die Art und Weise ermöglicht, wie die Angebote gesendet werden. [Weitere Informationen](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

**Inhaltsfragmente**

>[!AVAILABILITY]
>
>Bitte beachten Sie, dass diese Verbesserungen im Laufe von mehreren Tagen nach der ersten Veröffentlichung schrittweise eingeführt werden. Einige Benutzer haben zwar sofort Zugriff, bei anderen kann es aber zu einer Verzögerung kommen, bevor sie in ihren Umgebungen verfügbar werden.

* Fragmente können nun bearbeitet werden und Änderungen können in allen Live-Journeys und Kampagnen, in denen sie verwendet werden, übernommen werden.
* Es wurden neue Status für Inhaltsfragmente eingeführt: **Entwurf**, **Live**, **Wird veröffentlicht** und **Archiviert**.
* Damit ein Fragment in einer Journey oder Kampagne verwendet werden kann, muss es sich jetzt im Status **Live** befinden. Der Prozess der Fragmenterstellung wurde um einen neuen Schritt erweitert, der es ermöglicht, das Fragment zu veröffentlichen und für die Verwendung in Journeys und Kampagnen verfügbar zu machen. Beachten Sie, dass die Veröffentlichung von Fragmenten eine neue Berechtigung erfordert.

  **ACHTUNG:** Da die Status **Entwurf** und **Live** mit der Version Juni von Journey Optimizer eingeführt wurden, haben alle Fragmente, die vor dieser Version erstellt wurden, den Status **Entwurf**, auch wenn sie in einer Journey oder Kampagne verwendet werden. In diesem Abschnitt erfahren Sie, wie Sie vorhandene Fragmente aktualisieren können.

Weitere Informationen finden Sie unter [Inhaltsfragment](../content-management/fragments.md) Dokumentation.

**Journeys**

* Die globale Zeitüberschreitung für Journey wurde auf 91 Tage verlängert. [Weitere Informationen](../building-journeys/journey-properties.md#global_timeout)

  Bei allen neuen Journey wird diese neue Zeitüberschreitung angezeigt. Bitte beachten Sie dies [FAQ-Abschnitt](../building-journeys/journey-properties.md#timeout-faq) , um mehr zu erfahren. Bitte beachten Sie, dass diese Änderungen im Laufe des Monats Juni schrittweise eingeführt werden.


* Adobe Journey Optimizer unterstützt jetzt Datenschutz-Lösch-/Zugriffsanfragen sowie Data Life Cycle Management-Anfragen. [Weitere Informationen](../privacy/requests.md)
* Sie können nun die Spaltengröße im Journey-Inventar ändern.
  <!--* **Advanced expression editor in Event configuration** is now GA - You can now leverage the advanced expression editor while configuring an event, allowing you to define more complex expressions or use functions in the event id condition. This capability is released in Limited Availability for selected customers. [Read more](../event/about-creating.md)-->
* **Zusammenführungsrichtlinien** sind nun allgemein verfügbar: Die von einer Journey verwendeten Zusammenführungsrichtlinien sind jetzt im gesamten Verlauf der Journey sichtbar und konsistent. [Weitere Informationen](../building-journeys/journey-properties.md#merge-policies)



**Kampagnen**

* Beim Erstellen einer Kampagne in Adobe Journey Optimizer können Sie jetzt den Kampagnentyp (geplant oder ausgelöst) in einem neuen Modal auswählen. [Weitere Informationen](../campaigns/create-campaign.md)

<!--**Email channel**

* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**SMS-Kanal**

* Sie können jetzt eindeutige Kurzwahlnummern für jede Sandbox mit einer einzelnen API-Konfiguration hinzufügen, wodurch der Prozess effizienter und rationeller wird. [Weitere Informationen](../sms/sms-configuration.md)

* Nach der Erstellung wird die **API-Token** im Feld **API-Anmeldedetails** -Seite wird nun maskiert.

<!--* You can now modify existing SMS configurations.-->

**In-App-Kanal**

<!--* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

* Sie können jetzt das Edge-Bereitstellungs-Plug-in verwenden, um Informationen zu erhalten, die zum Verständnis und zur Fehlerbehebung bei Ihren eingehenden Implementierungen erforderlich sind. [Weitere Informationen zur Ansicht &quot;Edge Delivery&quot;](https://experienceleague.adobe.com/de/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.


**Briefpost-Kanal**

* Der Briefpost-Kanal ist jetzt für Unternehmen verfügbar, die die Adobe erworben haben **Gesundheitsschild** und **Datenschutz und Sicherheitsschild** Add-On-Angebote.
