---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 645db980155993155a10d27f4ff59967b000442f
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 19%

---

# Versionshinweise {#release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in diesen Versionshinweisen in der letzten Woche jedes Monats konsolidiert.

Frühere Versionshinweise finden Sie unter [diese Seite](release-notes-2022.md). Auf der Seite [Letzte Dokumentations-Updates](documentation-updates.md) finden Sie weitere Änderungsmöglichkeiten.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich für die [Vierteljährlicher Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} und erhalten Sie vierteljährlich die neuesten Produktaktualisierungen, spannenden Meldungen, Anwendungsbeispiele, Tipps und mehr direkt in Ihren Posteingang.


## Version Januar 2023 {#jan-2023-release}

### Neue Funktionen{#jan-2023-features}


<table>
<thead>
<tr>
<th><strong>Datenhygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform bietet eine Reihe von Funktionen zur Datenhygiene, mit denen Sie Ihre gespeicherten Daten durch programmgesteuerte Löschung von Verbraucherdatensätzen und -datensätzen verwalten können. Diese Funktion ist jetzt für Adobe Journey Optimizer verfügbar. </p>
<p>Sie können Ihre Datenspeicher verwalten, um sicherzustellen, dass Informationen erwartungsgemäß verwendet, aktualisiert werden, wenn falsche Datenanforderungen behoben werden müssen, und gelöscht wird, wenn dies aufgrund von organisatorischen Richtlinien erforderlich ist.</p>
<p><strong>Vorsicht</strong> - Die Funktionen zur Datenhygiene stehen derzeit nur Organisationen zur Verfügung, die die <strong>Gesundheitsschild</strong> und <strong>Datenschutz und Sicherheitsschild</strong> Add-On-Angebote.</p><p>Weitere Informationen zu Datensätzen finden Sie in der <a href="../privacy/data-hygiene.md">ausführlichen Dokumentation</a>.

</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Email content templates</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create standalone content templates that can be leveraged across journeys and campaigns for quick reuse.</p> 
<p>For more information, refer to the <a href="../personalization/get-started-dynamic-content.md">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>
-->

### Verbesserungen {#jan-2023-improvements}

**Journeys**

<!--
* The **Re-entrance wait period** field has been added to the journey properties. This field allows you to define the time to wait before allowing a profile to enter the journey again in unitary journeys (starting with an event or a segment qualification). This prevents journeys from being erroneously triggered multiple times for the same event. By default the field is set to 5 minutes. [Learn more](../building-journeys/journey-gs.md#entrance)

* Improvements have been made for **journey start and end dates**. If you have not specified a start date, it is now automatically added at publication time. For **Read segment** journeys, you can now add an end date. This allows profiles to exit automatically when the date is reached. [Learn more](../building-journeys/journey-gs.md#dates)
-->

* Beim Hinzufügen von **Segmentqualifizierung** oder **Segment lesen** In einer Journey ist der Namespace jetzt standardmäßig mit dem zuletzt verwendeten Namespace vorausgefüllt. Siehe Abschnitt [Segmentqualifizierung](../building-journeys/segment-qualification-events.md#about-segment-qualification) und [Segment lesen](../building-journeys/read-segment.md#configuring-segment-trigger-activity) Abschnitte.

* Auf der Journey-Arbeitsfläche ist eine neue Schaltfläche in der Symbolleiste verfügbar, mit der Sie einen Screenshot Ihrer Journey herunterladen können.

**Email Designer**

* Sie können jetzt den E-Mail-Inhalt aus der **HTML exportieren** Menü. Exportierte Dateien sind in einer ZIP-Archivdatei verfügbar.

**Administration**

* Ein neuer Unterabschnitt enthält Empfehlungen zum Erstellen der **Antwort an (E-Mail)** Adresse und Gewährleistung einer ordnungsgemäßen Antwortverwaltung. [Weitere Informationen](../email/email-settings.md#reply-to-email)

* Beim Erstellen oder Bearbeiten **IP-Pools**, werden die zugehörigen PTR-Datensätze jetzt in der IP-Liste angezeigt und wenn Sie den Mauszeiger über die ausgewählten IP-Adressen bewegen. [Weitere Informationen](../configuration/ip-pools.md#create-ip-pool)

* Nachdem ein IP-Pool auf einer Kanaloberfläche ausgewählt wurde, sind jetzt PTR-Datensatzinformationen sichtbar, wenn Sie den Mauszeiger über die IP-Adressen bewegen. [Weitere Informationen](../email/email-settings.md#subdomains-and-ip-pools)

* Die Benutzeroberfläche zur Bearbeitung [PTR-Datensätze](../configuration/ptr-records.md#edit-ptr-record) und [Ausführungsfelder](../configuration/primary-email-addresses.md) wurde aktualisiert.

* Die Benutzeroberfläche zum Erstellen und Bearbeiten von Subdomains wurde verbessert. [Weitere Informationen](../configuration/delegate-subdomain.md)

* Die Unterdrückungsliste **Letzte Uploads** wurde aktualisiert. [Weitere Informationen](../configuration/manage-suppression-list.md#recent-uploads)

**Kampagnen**

* Eine Beispiel-cURL-Anfrage, die die Ausführung API-gesteuerter Kampagnen ermöglicht, wird jetzt automatisch generiert und im Kampagnenbildschirm bereitgestellt. [Weitere Informationen](../campaigns/api-triggered-campaigns.md)

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**Personalisierung**

* Neue Hilfsfunktionen sind verfügbar: formatCurrency, charCodeAt, stringToDate, toString, formatNumber und toHexString. Darüber hinaus akzeptiert die Funktion toDateTimeOnly jetzt die Feldtypen String, Datum, Long und int. [Weitere Informationen](../personalization/functions/functions.md)
