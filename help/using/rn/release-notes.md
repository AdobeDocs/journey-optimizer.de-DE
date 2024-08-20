---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d971d857a480868f5ef502f3a3f2c209afc93cca
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 70%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.

## Frühzeitige Versionshinweise August 2024 {#e-2024}

**Veröffentlichungsdatum**: 20.–21. August 2024

>[!CAUTION]
>
>**Frühe Versionshinweise unten können ohne vorherige Ankündigung bis zum Veröffentlichungsdatum geändert werden**. Links, Bildschirme und aktualisierte Dokumentation werden am Veröffentlichungsdatum veröffentlicht.
>

### Neue Funktionen {#e-features}

Mit dieser Version werden die unten aufgeführten neue Funktionen eingeführt.

<!--table>
<thead>
<tr>
<th><strong>Guided Channel Setup</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Guided Channel Setup enables you to automate and validate channel setup in a unified experience, speeding up the process of getting started with Journey Optimizer. This new guided setup streamlines rapid channel configuration, ensuring all necessary resources are readily installed and working within Experience Platform, Journey Optimizer, and Data Collection. This enables marketing, product and data engineering teams to quickly begin with campaign and journey creation.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Content Cards</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content card is a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Improved Channel Configurations</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The current channel surface capabilities have been enhanced for a consistent approach across all channels. You can now define, manage, and reuse these configurations for any of your channels, including Web, In-app messaging, or Code-based experience.</p>
<p><ul>
<li>Channel surfaces are now renamed to <strong>Channel configurations</strong></li>
<li>You can attach one or multiple marketing actions to enforce consent and data governance policies</li>
<li>Object level access control (OLAC) is now available for each channel configuration, allowing you to decide which of your users are allowed to create or use specific configurations</li>
<li>For some channels, you can create channel configurations that target multiple platforms. An example here would be an In-app messaging channel configuration that can target a web page, an iOS app and an Android app.</li>
</ul></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Marketo Engage-Benutzerdefinierte Aktion</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können Adobe Journey Optimizer jetzt in Adobe Marketo Engage integrieren, um Ihre B2B-Anwendungsfälle zu erstellen. Eine neue benutzerdefinierte Aktion ermöglicht es Ihnen, von einer Journey aus Daten in Marketo aufzunehmen.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Variablen in Inhaltsfragmenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Fragmente können jetzt Eingabevariablen verwenden, sowohl in <a href="../personalization/use-expression-fragments.md">Ausdrucksfragmenten</a> als auch in <a href="../email/use-visual-fragments.md">visuellen Fragmenten</a>. Sie können diese Variablen verwenden, um Ihren Nachrichteninhalt und Ihre Nachrichtenparameter in Ihren Kampagnen und Journey zu personalisieren.</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>IP-Aufwärm-Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verfügbarkeitsdatum: 13. August</p>
<p>Beim Versenden von E-Mails an eine brandneue IP-Adresse können Sie nun einfach IP-Aufwärm-Workflows direkt über die Benutzeroberfläche ausführen. Adobe Journey Optimizer bietet eine standardisierte und effiziente Methode zum Aufwärmen von IP-Adressen, die den Best Practices für optimale Zustellbarkeit entspricht.</p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/ip-warmup-gs.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


### Verbesserungen {#e-improvements}

Diese Version bringt die unten aufgeführten Verbesserungen.

**Journeys**

<!--* In the **Condition** activity, by default, the Time condition is now set by hour, from 00:00 to 12:00. [Read more](../building-journeys/condition-activity.md#time_condition)-->
* Beim Erstellen Ihrer Journey werden Warnhinweise jetzt in einer Dropdown-Liste angezeigt, um sie mit Kampagnenwarnungen abzustimmen und ein einheitliches Benutzererlebnis zu gewährleisten. [Weitere Informationen](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* Die Zoom-Optionen in der Journey-Symbolleiste wurden verbessert: Der Zoom-Prozentsatz ist jetzt sichtbar und Sie können den Zoomwert jetzt einfach auf 100 % zurücksetzen.

**Zielgruppen**

* Die Verwendung von Zielgruppen aus benutzerdefiniertem Upload (CSV-Datei) ist jetzt für die Verwendung mit dem Datenschutz- und Sicherheitsschild-Add-on verfügbar.
* Beim Targeting einer benutzerdefinierten Upload-Zielgruppe (CSV-Datei) können Sie jetzt Attribute aus der Datei in Ihren Kampagnen und Journey verwenden. Diese Attribute sind im Personalisierungseditor verfügbar, um Ihre Nachrichten zu personalisieren, sowie im erweiterten Ausdruckseditor von Journey.

## Versionshinweise Juli 2024 {#24-7-2024}

**Veröffentlichungsdatum**: 30.–31. Juli 2024

### Neue Funktionen {#27-4-features}

Mit dieser Version werden die unten aufgeführten neuen Funktionen eingeführt.

<table>
<thead>
<tr>
<th><strong>SMS-Kanal mit beliebigem Anbieter (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Zusätzlich zu den Standardanbietern Sinch, Infobip und Twilio können Sie jetzt weitere SMS-Anbieter in Journey Optimizer konfigurieren.</p>
<img src="assets/do-not-localize/byo_sms.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../sms/sms-configuration-custom.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Komposition föderierter Zielgruppen (begrenzte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Komposition föderierter Zielgruppen ist jetzt in Adobe Journey Optimizer verfügbar. Sie ermöglicht es Unternehmen, Daten für eine bessere Nutzung in verschiedenen Anwendungsfällen zusammenzustellen. Mit diesem neuen Ansatz können Benutzende von Adobe Real-Time Customer Data Platform bzw. Adobe Journey Optimizer Datensätze direkt aus ihrem vorhandenen Data Warehouse zusammenführen, um Zielgruppen und Attribute von Adobe Experience Platform in einem einzigen System anzureichern.</p>
<p>Weitere Informationen finden Sie in der <a href="https://experienceleague.adobe.com/de/docs/federated-audience-composition/using/home"  target="_blank">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#27-4-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Journeys**

* (Verfügbarkeitsdatum: 8. Juli) **Erweiterter Ausdruckseditor bei der Konfiguration von Journey-Ereignissen**: Sie können jetzt bei der Konfiguration eines Ereignisses den erweiterten Ausdruckseditor nutzen und komplexere Ausdrücke definieren oder Funktionen in der Bedingung der Ereignis-ID verwenden. [Weitere Informationen](../event/about-creating.md#adv-exp-editor)

