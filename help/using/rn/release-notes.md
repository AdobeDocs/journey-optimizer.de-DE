---
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ac3c49c16a2496b3d5bc9b803589644b69c6565c
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 78%

---

# Versionshinweise {#release-notes}

Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für [!DNL Journey Optimizer] aufgelistet. Auf der Seite [Letzte Dokumentations-Updates](documentation-updates.md) finden Sie weitere Änderungsmöglichkeiten.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.

## Version Juni 2022 {#june-2022-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>SMS an Ihre Benutzer senden (begrenzte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt SMS in Journey Optimizer erstellen, personalisieren und senden, indem Sie eine Integration mit <b>Sinch</b> oder <b>Twilio</b> vornehmen.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Der SMS-Kanal ist derzeit nur für eine Reihe von ausgewählten Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie bei Ihrem Adobe-Support-Mitarbeiter.</p>
<p>In dieser <a href="../messages/create-sms.md">detaillierten Dokumentation</a> erfahren Sie, wie Sie eine SMS erstellen und senden.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Schnellere Suche nach effektiveren Bildern mit Adobe Stock-Integration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Das Plug-in für die Integration von Email Designer mit Adobe Stock und Adobe Journey Optimizer bietet Kunden eine einfache Möglichkeit, zur Verwendung bei der Nachrichtenbearbeitung durch Bilder zu navigieren, sie zu lizenzieren und sie zu speichern. </br> Die neue Option <b>Ähnliche Stock-Fotos suchen</b> ermöglicht es Ihnen auch, Stock-Fotos zu finden, die mit Inhalt, Farbe und Komposition Ihrer Bilder übereinstimmen. </p>
<img src="assets/do-not-localize/stock-rn.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../design/stock.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verwenden von E-Mail-BCC für alle Ihre E-Mails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt die Funktion „E-Mail-BCC“ (Blind Carbon Copy) verwenden, um von Adobe Journey Optimizer gesendete E-Mails zu speichern. Aktivieren Sie diese Option in Ihren E-Mail-Voreinstellungen, damit jede gesendete E-Mail in Blindkopie an Ihre BCC-Adresse gesendet wird.</p>
<img src="assets/do-not-localize/bcc-rn.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../configuration/bcc-email.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Objekte zwischen Sandboxes kopieren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt die Erlebnisse von einer Journey Optimizer-Sandbox in eine andere neu erstellen, z. B. von einer Nicht-Produktions-Sandbox zu einer Produktions-Sandbox. Diese neue Funktion kopiert eine ganze Journey, einschließlich aller Objekte, von denen die Journey abhängig ist, um korrekt ausgeführt zu werden, von einer Umgebung in eine andere. Zusätzlich zu Journey können Sie auch andere Komponenten kopieren, z. B. Angebote, Nachrichten, Schemas, Datensätze, Datenquellen, Ereignisse und Aktionen.</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/copy-to-sandbox.md">entsprechenden Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content. In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Verbesserungen

**Entscheidungs-Management**

* **Unterstützung von HTML- und JSON-Dateien**: Sie können jetzt per Drag-and-Drop externe HTML- und JSON-Dateien aus der Asset-Bibliothek von Adobe Experience Cloud in den Inhalt der Angebotsdarstellung ziehen. [Weitere Informationen](../offers/offer-library/add-representations.md#html-json)


**E-Mail**

* **Als Vorlage speichern**: Sie können jetzt E-Mail-Inhalte als Vorlage speichern und sie bei der Erstellung anderer Nachrichten wiederverwenden. [Weitere Informationen](../design/email-templates.md)

<!--
**Journeys**

* **Ending a journey** - In the journey canvas, the **End** activity has been removed from the palette. End tags are now added by default at the end of each path and cannot be removed. This improvement allows better reporting of where a customer dropped out of the journey, without any action from the user.

-->

**Administration**

<!--* **Allowed list in the UI** - You can now use the Journey Optimizer user interface to add new email addresses or domains to the allowed list.-->

* **Vorschau von Tracking-URL-Parametern**: Wenn Sie bei der Konfiguration einer Nachrichtenvoreinstellung URL-Tracking-Parameter definieren, wird jetzt eine dynamische Vorschau der resultierenden Tracking-URL angezeigt. [Weitere Informationen](../configuration/email-settings.md#url-tracking)

* **Nachrichtenvorgabenbearbeitung** - Beim Aktualisieren einer Nachrichtenvorgabe kann die Verarbeitungszeit jetzt nur noch 3 Stunden dauern. [Weitere Informationen](../configuration/message-presets.md#edit-message-preset)

* **IP-Poolbearbeitung** - Beim Aktualisieren eines IP-Pools kann die Verarbeitungszeit jetzt nur noch bis zu 3 Stunden dauern. [Weitere Informationen](../configuration/ip-pools.md#edit-ip-pool)

<!--* **Personalize tracking URL parameters** - You can now use the Expression Editor to configure URL tracking parameters in your message presets. [Learn more](../configuration/email-settings.md#url-tracking)-->

<!--
**Reporting**

* **Performance measurement** - A new **Reporting** tab is now available in the Administration > Configurations menu to set up reporting data sources.
-->
