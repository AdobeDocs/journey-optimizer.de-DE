---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 100%

---

# Versionshinweise {#release-notes}

Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für [!DNL Journey Optimizer] aufgelistet. Auf der Seite [Letzte Dokumentations-Updates](documentation-updates.md) finden Sie weitere Änderungsmöglichkeiten.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.


## Version Oktober 2022 {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### Verbesserungen {#oct-2022-improvements}

**Journeys**

* Die Option **Erneuten Eintritt bei Wiederholung erzwingen** wurde zu den Planparametern für wiederkehrende Lesesegmente hinzugefügt. Mit dieser Option können Sie alle noch in der Journey vorhandenen Profile bei der nächsten Ausführung automatisch entfernen. Wenn die Option deaktiviert ist, müssen Profile die Journey abschließen, bevor sie in einem anderen Vorkommen erneut eintreten können. [Weitere Informationen](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Administration**

* Es wurde eine Nachricht zur Benutzeroberfläche hinzugefügt, die darauf hinweist, dass die Konfigurationen von Subdomain, Landingpage-Subdomain, PTR-Eintrag und IP-Pool für alle Sandboxes gelten. Daher wirkt sich jede Änderung an einer dieser Konfigurationen auch auf die Produktions-Sandboxes aus.
* Die Schritte zum Hochladen der Unterdrückungsliste als CSV-Datei über die Benutzeroberfläche wurden geändert. [Weitere Informationen](../configuration/manage-suppression-list.md#download-suppression-list)

**Kampagnen**

* Sie können jetzt abgeschlossene und gestoppte Kampagnen archivieren. [Weitere Informationen](../campaigns/modify-stop-campaign.md#archive)
