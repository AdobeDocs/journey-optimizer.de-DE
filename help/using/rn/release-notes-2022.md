---
title: Versionshinweise 2022
description: Versionshinweise zu Journey Optimizer 2022
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: f5e3b7cee816be420a09abd8aa9404faaccfec87
workflow-type: ht
source-wordcount: '1069'
ht-degree: 100%

---

# Versionshinweise 2022 {#release-notes-2022}

Auf dieser Seite sind alle Funktionen und Verbesserungen für [!DNL Journey Optimizer] aufgeführt, die im Jahr 2022 veröffentlicht wurden.

Die neuesten Versionshinweise sind [auf dieser Seite](release-notes.md) verfügbar.

## Version April 2022 {#april-2022-release}

### Verbesserungen

**Landingpages**

* **Neue Option für Opt-in-/Opt-out-Kontrollkästchen** - Sie können jetzt ein einziges Kontrollkästchen für das Opt-in/Opt-out in Abonnement-Landingpages einfügen. Benutzer müssen das Kontrollkästchen aktivieren, um ihr Einverständnis zu erteilen (Opt-in), und es deaktivieren, um ihr Einverständnis zurückzuziehen (Opt-out). [Weitere Informationen](../landing-pages/design-lp.md#define-lp-specific-content)

* **Vorausfüllen von Feldern auf Landingpages** - Benutzer können jetzt die Felder auf der Landingpage mit Profilinformationen befüllen. [Weitere Informationen](../landing-pages/create-lp.md#configure-primary-page)

**Entscheidungs-Management**

* **Decisioning-API in Edge** - Die Decisioning-API in Edge kann personalisierte Angebote bereitstellen und rendern, die in Offer Decisioning verwaltet werden. Sie können Ihre Angebote und andere verwandte Objekte über APIs oder die Benutzeroberfläche (UI) von Offer Decisioning erstellen. [Weitere Informationen](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Administration**

* **PTR-Sendedauer** - PTR-Bearbeitungen werden nun nach ein paar Stunden wirksam. [Weitere Informationen](../configuration/ptr-records.md#processing)

**E-Mail-Design**

* **20 neue E-Mail-Vorlagen** sind jetzt verfügbar, um E-Mail-Inhalte in Journey Optimizer zu erstellen.

**Benutzeroberfläche**

* **Kontexthilfe in der Benutzeroberfläche von Journey Optimizer** - Auf mehreren Seiten in Journey Optimizer wurden Links zur Kontexthilfe hinzugefügt. Wenn verfügbar, klicken Sie auf das Symbol „i“, um eine kurze Beschreibung der aktuellen Funktion anzuzeigen und auf zugehörige Artikel zuzugreifen.

**Integration mit Adobe Campaign Standard**

Als Adobe Campaign Standard-Kunde können Sie jetzt mit Journey Optimizer E-Mails, Push-Benachrichtigungen und SMS versenden. Verwenden Sie die neuen integrierten Aktionen, um die Funktionen für den Transaktionsnachrichtenversand von Campaign Standard in Journey Optimizer zu nutzen.  [Weitere Informationen](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## Version März 2022 {#march-2022-release}

### Verbesserungen

**Journeys**

* Um im einheitlichen Profilschema unnötige Felder zu vermeiden, ist das Schema „Journey-Schrittereignisse“ nicht mehr standardmäßig für Profile aktiviert. Bei Bedarf können Sie es aktivieren. [Weitere Informationen](../reports/sharing-overview.md)
* Neue Schrittereignisse im Zusammenhang mit Exportvorgängen werden jetzt von Journey Optimizer an Adobe Experience Platform gesendet. Beispiele für Abfragen wurden der Dokumentation hinzugefügt. [Weitere Informationen](../reports/query-examples.md)

**Entscheidungs-Management**

* Sie können jetzt definieren, ob die Angebotsbegrenzung für alle Benutzer oder für ein bestimmtes Profil bzw. für alle Platzierungen oder nur für eine einzeln Platzierung gelten soll. [Weitere Informationen](../offers/offer-library/add-constraints.md#capping)
* Mit der Batch Decisioning-API können Unternehmen die Offer-Decisioning-Funktionalität für alle Profile in einem bestimmten Segment in einem einzigen Aufruf verwenden. Der Angebotsinhalt für jedes Profil im Segment wird in einem AEP-Datensatz platziert, wo er für benutzerdefinierte Batch-Workflows zur Verfügung steht. [Weitere Informationen](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Administration**

* Sie können jetzt den Abmelde-Link im E-Mail-Header auf der Voreinstellungsebene der Nachricht aktivieren/deaktivieren und eine benutzerdefinierte Abmelde-URL auf Nachrichtenebene festlegen. [Weitere Informationen](../configuration/message-presets.md#list-unsubscribe)
* Die Zulassungsliste kann jetzt über die [!DNL Journey Optimizer]-Benutzeroberfläche für Produktions- und Nicht-Produktions-Sandboxes aktiviert und deaktiviert werden. [Weitere Informationen](../reports/allow-list.md#enable-allow-list)

**Personalisierung**

* Sie können jetzt mehr als 40 Personalisierungsausdrücke in der Bibliothek speichern. [Weitere Informationen](../personalization/personalization-library.md)

## Version Februar 2022 {#feb-2022-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Landingpages für Abonnements</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können in Journey Optimizer jetzt Landingpages erstellen und gestalten und Ihre Benutzer zu Online-Formularen weiterleiten, über die sie sich für den Erhalt Ihrer Nachrichten anmelden oder abmelden oder einen bestimmten Service wie einen Newsletter abonnieren können.</p>
<p>Weitere Informationen finden Sie in der <a href="../landing-pages/create-lp.md">entsprechenden Dokumentation</a> und in diesem <a href="../landing-pages/lp-use-cases.md">Anwendungsfall</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Neue Ausdrucksbibliothek für die Personalisierung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer bietet jetzt eine Bibliothek, in der Sie auf vordefinierte Personalisierungsausdrücke zugreifen können. Diese Ausdrücke werden von Admin-Benutzern konfiguriert.</p>
<p>Weitere Informationen finden Sie in der <a href="../personalization/personalization-library.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs’ feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Übergeben von Informationen zur Nachverfolgung Ihrer Nachrichten mit UTM-Tracking-Parametern</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Nachrichteninhalten von Journey Optimizer können Sie jetzt UTM-Parameter zu Ihren Links hinzufügen. Diese können zusätzliche Daten zu diesem Link liefern und Ihnen dabei helfen herauszufinden, wo und warum eine Person auf Ihren Link geklickt hat.</p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/message-presets.md#configure-email-settings">entsprechenden Dokumentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journeys**

* Um die Leistung zu optimieren, wechseln alle Journeys im Testmodus, die seit einer Woche nicht ausgelöst wurden, jetzt wieder in den Entwurfsstatus zurück. [Weitere Informationen](../building-journeys/testing-the-journey.md#important_notes)
* Die Integration zwischen Journey Optimizer und Adobe Campaign Classic wurde optimiert, um die Leistung zu verbessern. Die Standardkonfiguration für Begrenzungen wurde auf 4.000 Aufrufe/5 Minuten geändert.	[Weitere Informationen](../action/acc-action.md#important-notes)

**Reporting**

* Sendungen können nun nach ihrem Status gefiltert werden:
   * In der Liste „Nachrichtenausführung“ können Sie jetzt Testsendungen aus der Versandliste ausschließen.
   * Bei Ihren Live-/Global-Berichten können Sie auswählen, ob Sie Testereignisse ausschließen möchten.

* Sie können jetzt auf Berichte zu Sendezeitoptimierungsdaten zugreifen: die Anzahl der Personen, die unmittelbar benachrichtigt wurden, und die Anzahl der Personen, die mit einer 1-Stunden-Optimierung, einer 2-Stunden-Optimierung usw. benachrichtigt wurden.

<!--* Offer Decisioning reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Entscheidungs-Management**

* Rangfolgen und KI-Rangfolgen werden jetzt in einer Registerkarte zusammengefasst.

## Version Januar 2022 {#january-2022-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Journeys – Optimales Aufwärmen Ihrer IP-Adressen mit Profilbegrenzungsbedingungen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Beim Konfigurieren einer <strong>Bedingungs</strong>-Aktivität in einer Journey können Sie jetzt eine Profilobergrenze festlegen. Dieser neue Bedingungstyp ermöglicht es Ihnen, eine Höchstzahl von Profilen für einen Journey-Pfad festzulegen. Wenn diese Grenze erreicht ist, folgen die eintretenden Profile einem alternativen Pfad. Auf diese Weise können Sie das Volumen Ihrer Sendungen erhöhen (IP-Ramp-up). Sie können beispielsweise Ihre Sendungen in einer Domain schrittweise ausführen, indem Sie die Ausführung aufteilen: Sie senden 1.000 Nachrichten am Tag 1, 2.000 am Tag 2 usw.</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/condition-activity.md#profile_cap">entsprechenden Dokumentation</a> und in diesem <a href="../building-journeys/ramp-up-deliveries-uc.md">Anwendungsfall</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journeys – Verbesserung beim Lesen von Segmenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Option <strong>Inkrementelles Lesen</strong> wurde zu den wiederkehrenden <strong>Segment lesen</strong>-Aktivitäten hinzugefügt. Mit dieser Option haben Sie die Möglichkeit, nur die Personen anzusprechen, die seit der letzten Ausführung der Journey in das Segment eingetreten sind. Bei der ersten Ausführung sind immer alle Segmentmitglieder ausgewählt.</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">entsprechenden Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journeys**

* Step-Ereignisse von Journey Optimizer können jetzt mit anderen Datensätzen in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=de) verknüpft werden. Das Feld **profileID** im integrierten Step-Ereignisschema einer Journey ist jetzt als Identitätsfeld definiert. [Weitere Informationen](../reports/sharing-overview.md#integration-cja)

**Offer Decisioning**

* Wenn Sie ein Angebot, ein Fallback-Angebot, eine Angebotssammlung oder eine Angebotsentscheidung aktualisieren, auf die direkt oder indirekt in einer veröffentlichten Nachricht verwiesen wird, werden die Aktualisierungen automatisch in der entsprechenden Nachricht angezeigt, ohne dass sie erneut veröffentlicht werden müssen. [Weitere Informationen](../offers/offers-e2e.md#insert-decision-in-email)

* Bei der Simulation, welche Angebote für ein bestimmtes Testprofil bereitgestellt werden sollen, können Sie jetzt die Standardsimulationseinstellungen ändern und den Code anzeigen, der Ihren Simulationen entspricht. Dieser Code kann zur Fehlerbehebung verwendet werden. [Weitere Informationen](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administration**

* Administratoren können jetzt PTR-Einträge mit einer Subdomain bearbeiten, die mit CNAME eingerichtet ist. [Weitere Informationen](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalisierung**

* **Zu Favoriten hinzufügen** – Um das Arbeiten mit Personalisierungen einfacher zu gestalten, haben die Speicherung von Favoriten ermöglicht. Durch das Hinzufügen verschiedener Attribute zum Favoritenmenü erhalten Sie schnellen Zugriff auf die am häufigsten verwendeten Elemente. [Weitere Informationen](../personalization/personalize.md#fav)
