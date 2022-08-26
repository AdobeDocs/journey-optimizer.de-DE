---
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: bc036fc52424adaf129ab379872dedfc5994c3bb
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 50%

---

# Versionshinweise {#release-notes}

Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für [!DNL Journey Optimizer] aufgelistet. Auf der Seite [Letzte Dokumentations-Updates](documentation-updates.md) finden Sie weitere Änderungsmöglichkeiten.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.

## Version August 2022 {#aug-2022-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Erstellen und Verwalten von Kampagnen in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verwenden Sie Journey Optimizer-Kampagnen, um mithilfe verschiedener Kanäle einmalige Inhalte für ein bestimmtes Segment bereitzustellen. Bei Verwendung von Journey sind Aktionen so konzipiert, dass sie nacheinander ausgeführt werden. Bei Kampagnen werden Aktionen gleichzeitig, entweder sofort oder basierend auf einem festgelegten Zeitplan ausgeführt. </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>Erfahren Sie, wie Sie eine Kampagne im <a href="../campaigns/get-started-with-campaigns.md">Detaillierte Dokumentation</a> und <a href="https://video.tv.adobe.com/v/345376">Feature Video</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>SMS an Ihre Benutzer senden (allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt SMS in Journey Optimizer erstellen, personalisieren und senden, indem Sie eine Integration mit <b>Sinch</b> oder <b>Twilio</b> vornehmen.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>In dieser <a href="../messages/create-sms.md">detaillierten Dokumentation</a> erfahren Sie, wie Sie eine SMS erstellen und senden.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->



### Verbesserungen

**Reporting**

* Die Tabelle mit den Einwilligungsrichtlinien und das Diagramm sind jetzt in Journey-globalen Berichten verfügbar. Mit diesen Widgets können Sie die ausgeschlossenen Profile aus den Richtlinien in Ihren benutzerdefinierten Aktionen verfolgen. [Weitere Informationen](../reports/journey-global-report.md#journey-global)

   Um Zugriff auf die neuesten Widgets zu erhalten, müssen Sie die verschiedenen Berichts-Dashboards zurücksetzen. Weiterführende Informationen zur Dashboard-Anpassung finden Sie im Abschnitt [die ausführliche Dokumentation](../reports/global-report.md).

**Administration**

* Jetzt ist es möglich, die für den SMS-Kanal zu verwendende primäre Telefonnummer zu aktualisieren. [Weitere Informationen](../configuration/primary-email-addresses.md)