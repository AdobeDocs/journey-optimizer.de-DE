---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Frühzeitige Versionshinweise zu Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: d5fa80ee2823131bb69bae0f366b92bf1fae3020
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 56%

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

<!--table>
<thead>
<tr>
<th><strong>Experience Decisioning - Limited Availability</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experience Decisioning simplifies personalization by offering a centralized catalog of marketing offers known as 'decision items' and a sophisticated decision engine. This engine leverages rules and ranking criteria to select and present the most relevant decision items to each individual.</p>
<p>These decision items are seamlessly integrated into a wide range of inbound surfaces through the new code-based experience channel, now accessible within Journey Optimizer campaigns. Experience Decisioning decision policies are available for use in code-based experience campaigns only.</p>
<p>Experience Decisioning is currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->

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

<table>
<thead>
<tr>
<th><strong>Verbesserte Journey Designer- und Live-Berichterstellung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Diese Version enthält eine verbesserte Arbeitsfläche für Journey und bietet ein intuitiveres und effizienteres Benutzererlebnis. Aktivitäten sind klarer und enthalten mehr Informationen auf der Journey-Arbeitsfläche mit weniger Klicks.</p>
<img src="assets/new-canvas3.gif"/>
<p>Neben dem verbesserten Journey-Canvas-Design bieten wir die Möglichkeit, die Berichtsmetriken der letzten 24 Stunden direkt auf der Journey-Arbeitsfläche zu sehen. </p>
<img src="assets/new-canvas6bis.png"/>
<p><br>Hinweis</br>:Diese Änderung wird schrittweise eingeführt. Möglicherweise werden die Änderungen nicht sofort in Ihrer Umgebung angezeigt.</p>
<p>Weitere Informationen finden Sie in der <a href="new-canvas.md">ausführlichen Dokumentation</a>.</p>
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

<!--
**Decision management** 

* The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu.

**Experience decisionning**

From beta to LA, the following improvements that have been added:

* You can now leverage context data from Adobe Experience Platform in your decision rules using the **Context data** tab.  
* A new "Manage Experience decisions" permission is now available for the Decision Management resource. It allows you to manage rights related to Experience Decisioning.   
* You can now add multiple capping rules for a given decision item in Experience Decisioning. This allows you to increase the level of control over the way offers are sent.
* You can now create custom reporting dashboards of Experience Decisioning campaigns using [!DNL Customer Journey Analytics].
-->



**Konfiguration**

* Jetzt können Sie eine Marketing-Aktion auf der Ebene der Kanaloberfläche auswählen. Bei Verwendung in einer Oberfläche werden alle mit dieser Marketing-Aktion verknüpften Zustimmungsrichtlinien genutzt, um die Voreinstellungen Ihrer Kundinnen und Kunden zu respektieren.
* Die Verwendung der Zugriffssteuerung auf Objektebene ist jetzt für Kanaloberflächen verfügbar.

