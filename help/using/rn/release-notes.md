---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 0433e312db84ee16a076c183a82345de372c6ae7
workflow-type: tm+mt
source-wordcount: '1112'
ht-degree: 94%

---

# Versionshinweise {#release-notes}

Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für [!DNL Journey Optimizer] aufgelistet. Auf der Seite [Letzte Dokumentations-Updates](documentation-updates.md) finden Sie weitere Änderungsmöglichkeiten.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.


## Oktober 2022 {#oct-2022-release}

### Verbesserungen{#oct-2022-improvements}

**Journeys**

* Die **Wiedereintritt erzwingen bei Wiederholung** wurde unter Planparametern für wiederkehrende Lesesegmente hinzugefügt. Mit dieser Option können Sie alle noch in der Journey vorhandenen Profile bei der nächsten Ausführung automatisch beenden. Wenn die Option deaktiviert ist, müssen Profile die Journey abschließen, bevor sie in einem anderen Vorkommen erneut eintreten können. [Weitere Informationen](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Kampagnen**

* Sie können jetzt abgeschlossene und gestoppte Kampagnen archivieren. [Weitere Informationen](../campaigns/modify-stop-campaign.md#archive)

## Version September 2022{#sept-2022-release}

### Neue Funktionen{#sept-2022-features}

<table>
<thead>
<tr>
<th><strong>Dynamischer Inhalt und neuer Builder für bedingte Regeln</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt dynamische Inhalte erstellen, um den Inhalt Ihrer Nachrichten basierend auf bedingten Regeln anzupassen.</p> 
<p>Bedingte Regeln werden mit einem visuellen Regel-Builder im Ausdruckseditor erstellt, in dem Sie sie zur weiteren Wiederverwendung in Ihren Journeys und Kampagnen speichern können.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../personalization/get-started-dynamic-content.md">detaillierten Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API-ausgelöste Kampagnen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Zusätzlich zu bereits geplanten Kampagnen können Sie jetzt API-ausgelöste Kampagnen in Journey Optimizer erstellen und diese über APIs von einem externen System aus aufrufen.</p>
<p>Auf diese Weise können Sie Nutzungsszenarien mit verschiedenen operativen und Transaktionsnachrichten abdecken, wie z. B. das Zurücksetzen von Kennwörtern, OTP-Token usw.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../campaigns/api-triggered-campaigns.md">detaillierten Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Datenzugriffssteuerung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Durch die attributbasierte Zugriffssteuerung können Admins den Zugriff auf bestimmte Objekte auf der Grundlage bestimmter Attribute steuern. Bei diesen Attributen kann es sich um Metadaten handeln, die einem Objekt hinzugefügt werden, wie z. B. Beschriftungen. Ab dieser Version können Admins auch Benutzerrollen definieren, die nur Zugriff auf bestimmte Felder und/oder Objekte haben, sowie auf Daten, die diesen Feldern und/oder Objekten entsprechen.</p>
<p> Die Verwendung der attributbasierten Zugriffssteuerung ist derzeit auf ausgewählte Kundinnen und Kunden beschränkt und wird in einer zukünftigen Version für alle Umgebungen bereitgestellt.</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../administration/object-based-access.md">detaillierten Dokumentation</a>.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Data Governance und Datenschutz</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dem Governance-Framework Data Usage Labeling and Enforcement (DULE) kann Journey Optimizer jetzt Governance-Richtlinien von Adobe Experience Platform nutzen, um zu verhindern, dass sensible Felder durch benutzerdefinierte Aktionen in Drittanbieter-Systeme exportiert werden. Wenn das System in den benutzerdefinierten Aktionsparametern ein eingeschränktes Feld identifiziert, wird ein Fehler angezeigt, der die Veröffentlichung der Journey verhindert.</p>
<p>Die Verwendung von Data Usage Labeling and Enforcement (DULE) ist derzeit auf ausgewählte Kundinnen und Kunden beschränkt und wird in einer zukünftigen Version für alle Umgebungen bereitgestellt.</p>
<p>Weitere Informationen finden Sie in der <a href="../action/action-privacy.md">detaillierten Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Automatisierte Durchsetzung von Einverständniserklärungen (Einverständnisrichtlinien)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Adobe Experience Platform können Sie einfach Marketing-Richtlinien übernehmen und durchsetzen, um die Einverständnispräferenzen Ihrer Kunden zu respektieren. Einverständniserklärungen werden in Adobe Experience Platform definiert. In Journey Optimizer können Sie diese Einverständniserklärungen auf Ihre benutzerdefinierten Aktionen anwenden. Beispielsweise können Sie Einverständniserklärungen definieren, um Kundinnen und Kunden auszuschließen, die dem Empfang von E-Mail-, Push- oder SMS-Nachrichten nicht zugestimmt haben.
<p>Die automatisierte Durchsetzung von Einverständniserklärungen ist derzeit nur für Organisationen verfügbar, die das Add-on Healthcare Shield erworben haben.</p>
<p>Weitere Informationen finden Sie in der <a href="../action/consent.md">detaillierten Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Berechtigungsverwaltung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer unterstützt das Definieren von Benutzerrollen und Zugriffsrichtlinien zum Verwalten von Berechtigungen für Funktionen und Objekte. Über <strong>Adobe Experience Cloud-Berechtigungen</strong> können Sie Rollen erstellen und verwalten sowie die gewünschten Ressourcenberechtigungen für diese Rollen zuweisen. Mit Berechtigungen können Sie auch die Bezeichnungen, Sandboxes und Benutzende verwalten, die einer bestimmten Rolle zugeordnet sind.</p>
<p> Die Verwendung von Berechtigungen ist derzeit auf ausgewählte Kundinnen und Kunden beschränkt und wird in einer zukünftigen Version für alle Umgebungen bereitgestellt.</p>
<p>Weitere Informationen finden Sie in der <a href="../administration/attribute-based-access.md">detaillierten Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alarmierung und Überwachung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Als Journey Optimizer-Benutzende können Sie jetzt über die Benutzeroberfläche auf Systemwarnungen zugreifen, um Benachrichtigungen zu erhalten, wenn Journeys nicht wie erwartet funktionieren. Sie können die verfügbaren Warnhinweise einsehen und abonnieren. Der erste Warnhinweis, der mit dieser Version verfügbar ist, warnt Sie, wenn eine Aktivität vom Typ „Segment lesen“ innerhalb des festgelegten Zeitraums kein Profil verarbeitet hat. Weitere werden folgen, sobald dieser Workflow freigeschaltet ist.</p>
<p>Weitere Informationen finden Sie in der <a href="../reports/alerts.md">detaillierten Dokumentation</a>.
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Data Hygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform provides a suite of data hygiene capabilities that allow you manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. </p>
<p>You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.</p>
<p><strong>Caution</strong> - Data Hygiene capabilities are currently only available for organizations that have purchased the Healthcare Shield add-on offering.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### Verbesserungen{#sept-2022-improvements}

**Journey**

* Der **Entitätsdatensatz** ist jetzt als vordefinierter Datensatz in Adobe Journey Optimizer verfügbar. Dieser Lookup-Datensatz enthält Metadaten, um die Informationen der Tracking- und Feedback-Datensätze zu erweitern. Auf diese Weise können Sie Ihre Berichte und Abfragen mit leichter verständlichen Daten verbessern. [Weitere Informationen](../start/datasets-query-examples.md#entity-dataset)
* Eine neue Sicherheitseinrichtung wurde zu unitären Journeys hinzugefügt (beginnend mit einem Ereignis oder einer Segmentqualifikation), um zu verhindern, dass Journeys fälschlicherweise mehrfach für dasselbe Ereignis ausgelöst werden. Der erneute Profileintritt wird jetzt standardmäßig fünf Minuten lang vorübergehend blockiert. [Weitere Informationen](../start/guardrails.md#events-g)

**Administration**

* Beim Aktivieren oder Deaktivieren der Zulassungsliste wird nun eine neue Warnung mit Details zu den Auswirkungen jeder Aktion angezeigt. [Weitere Informationen](../configuration/allow-list.md#enable-allow-list)
* Die Benutzeroberfläche zum Erstellen von Kanaloberflächen, zum Erstellen von IP-Pools, zum Verwalten der Unterdrückungsliste und der Zulassungsliste sowie zum Konfigurieren des SMS-Kanals wurde aktualisiert.
* Beim Erstellen der ersten Kanaloberfläche für eine bestimmte Subdomain beträgt die Verarbeitungszeit 10 Minuten bis 10 Tage und bei nachfolgenden Oberflächen, die diese Subdomain verwenden, nur noch bis zu 3 Stunden. [Weitere Informationen](../configuration/channel-surfaces.md#create-channel-surface)

<!--* Now when downloading the suppression list as a CSV file, you can choose the file that was previously generated, or generate a new file.-->
* Die Benutzeroberfläche zum Erstellen von Landingpage-Voreinstellungen und Landingpage-Subdomains wurde aktualisiert. [Weitere Informationen](../configuration/lp-subdomains.md)

**Audit-Kontrollen**

* Mit Journey Optimizer können Sie die von den Nutzenden im System durchgeführten Aktionen für verschiedene Services und Funktionen wie Kampagnen, Journeys, Nachrichten, Landingpages usw. ermitteln. Audit-Protokoll-Ressourcen enthalten jetzt Änderungen an verschiedenen anderen Aktionen und werden automatisch aufgezeichnet, wenn die Aktivität stattfindet. Weiterführende Informationen finden Sie auf [dieser Seite](../privacy/audit-logs.md).

**Archivierungsunterstützung**

* Der neue **Entitätsdatensatz** enthält ein Vorlagenfeld, mit dem Sie das Format und die Struktur der gesendeten Nachrichten zu Archivierungszwecken in alle Kanäle exportieren können. [Weitere Informationen](../configuration/archiving-support.md)

**Landingpages**

* Sie können jetzt kontextbezogene Daten verwenden, die von einer anderen Seite innerhalb derselben Landingpage stammen. Wenn Sie beispielsweise ein Kontrollkästchen mit einer Abonnementliste auf der primären Landingpage verknüpfen, können Sie diese Abonnementliste auf der Unterseite „Vielen Dank“ verwenden. [Weitere Informationen](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Weitere Änderungen{#sept-2022-other}

* Der Journey-Burst-Modus wurde durch den Kampagnen-Schnellversand-Modus ersetzt. [Weitere Informationen](../campaigns/create-campaign.md#rapid-delivery)
* Um die Leistung zu verbessern, können Feldergruppen für Erlebnisereignisse nicht mehr in Journeys verwendet werden, die mit einem Lesesegment, einer Segmentqualifikation oder einer Geschäftsereignisaktivität beginnen. Diese Änderung gilt nur für neue Journeys. Bestehende Journeys behalten das aktuelle Verhalten bei. [Weitere Informationen](../start/guardrails.md#expression-editor)
* Die 1-Stunden-Beschränkung für geplante Segment-Lese-Journeys wurde entfernt. Diese Journeys können jetzt ohne Verzögerung ausgeführt werden.

