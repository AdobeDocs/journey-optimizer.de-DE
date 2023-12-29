---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 299b34dec2e864fff5eb874b3fd491da80bc0c16
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 100%

---

# Versionshinweise {#release-notes}


>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert.

Frühere Versionshinweise finden Sie auf [dieser Seite](release-notes-2023.md). Auf der Seite [Letzte Dokumentations-Updates](documentation-updates.md) finden Sie weitere Änderungsmöglichkeiten.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.

## Versionshinweise für Oktober 2023 {#oct-rn-2023}

### Neue Funktionen{#oct-2023-features}

Mit dieser Version werden die unten aufgeführten neuen Funktionen eingeführt.

<table>
<thead>
<tr>
<th><strong>Sandbox-Werkzeuge</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Sandbox-Werkzeugen können Sie Objekte über mehrere Sandboxes hinweg kopieren, indem Sie den Export und Import von Paketen nutzen. Ein Paket kann aus einem oder mehreren Objekten bestehen. Alle Objekte, die in einem Paket enthalten sind, müssen aus derselben Sandbox stammen.</p>
<!--img src="../data/assets/dataset-export-setup.png"-->
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/copy-to-sandbox.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Composed audiences in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use audiences created in composition workflows in your journeys to target customers. Once an audience composition is published, and the audience saved, use a Read Audience activity to select this new audience in your journey canvas.</p>
<img src="assets/channel-reports.png"/>
<p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table -->

<table>
<thead>
<tr>
<th><strong>Multimedia Message Service (MMS) in SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dem SMS-Kanal können Sie Ihre Kommunikation jetzt verbessern, indem Sie MMS-Nachrichten (Multimedia Message Service) senden, sodass Sie Bilder, GIFs oder Videos mit Ihren Kundinnen und Kunden teilen können. Beachten Sie, dass diese Funktion derzeit nur mit Sinch verfügbar ist.</p>
<img src="assets/do-not-localize/mms.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../sms/create-sms.md#mms-content">ausführlichen Dokumentation</a>.</p>
</tr>
</tbody>
</table>

### Verbesserungen {#oct-2023-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Zielgruppen**

* Sie können jetzt Zielgruppen auswählen, die aus einer CSV-Datei in Journeys und Kampagnen hochgeladen wurden. [Weitere Informationen](../audience/about-audiences.md#segments-in-journey-optimizer)
* Sie können jetzt Zielgruppen auswählen, die durch die Zielgruppenkomposition erstellt wurden, und Anreicherungsattribute in Journeys nutzen. [Weitere Informationen](../building-journeys/read-audience.md)

>[!AVAILABILITY]
>
>Diese Funktionen sind als private Betaversion verfügbar.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**Kampagnen**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* Tritt in einer Ihrer Kampagnen ein Fehler auf, wird in der Kampagnenliste neben dem Status der Kampagne nun ein Warnsymbol angezeigt. [Weitere Informationen](../campaigns/modify-stop-campaign.md#statuses)

**Journeys**

* Die maximale Dauer, die Sie in einer beliebigen Wartezeit definieren können, beträgt jetzt 29 Tage anstelle von 30. Diese Verbesserung wurde eingeführt, um zu verhindern, dass Wartezeiten die Journey-Lebensdauer von 30 Tagen überschreiten. Dies gilt für:

   * das Feld **Dauer** in der [Warteaktivität](../building-journeys/wait-activity.md)
   * das Feld **Wartezeit bis zum erneuten Eintritt** in den [Journey-Eigenschaften](../building-journeys/journey-gs.md#entrance)
   * das Feld **Warten auf** in der Definition der maximalen Wartezeit von [Ereignisaktivitäten](../building-journeys/general-events.md#events-specific-time).

<!--
**Consent in channel configuration**

* You can now select a marketing action at the channel surface level. When used in a surface, all consent policies associated with that marketing action are leveraged in order to respect the preferences of your customers.-->

**Entscheidungs-Management**

* Mehrere Bezeichnungen zur Angebotsbegrenzung in der Benutzeroberfläche für das Entscheidungs-Management wurden aktualisiert. [Weitere Informationen](../offers/offer-library/add-constraints.md#capping)

