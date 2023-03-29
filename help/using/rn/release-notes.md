---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '1320'
ht-degree: 81%

---

# Versionshinweise {#release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert.

Frühere Versionshinweise finden Sie auf [dieser Seite](release-notes-2022.md). Auf der Seite [Letzte Dokumentations-Updates](documentation-updates.md) finden Sie weitere Änderungsmöglichkeiten.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.


## März 2023 - Versionshinweise {#mar-2023}

Die nachfolgenden Informationen können bis zum Verfügbarkeitsdatum der Veröffentlichung ohne vorherige Ankündigung geändert werden. Die aktualisierte Dokumentation wird am Veröffentlichungsdatum veröffentlicht und auf dieser Seite werden direkte Links hinzugefügt.

**Verfügbarkeitsdatum**: 29. März 2023

### Neue Funktionen{#mar-2023-features}

<!--
<table>
<thead>
<tr>
<th><strong>In-app channel (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now send personalized In-app messages to your app users within a campaign. Use Journey Optimizer to design notifications and customize the message layout, display, text, and buttons to create a seamless experience.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>SMS-Klick-Tracking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dem Klick-Tracking für SMS können Sie die Leistung Ihrer gekürzten URLs überwachen, ermitteln, wer auf sie geklickt hat, und diese Daten verwenden, um Kunden mit nachfolgenden Kampagnen erneut anzusprechen.</p>
<img src="assets/do-not-localize/sms-tracking.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../sms/create-sms.md#sms-content">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Verwenden von Tags in Ihren Journey (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Als Anwenderin bzw. Anwender von Journey Optimizer können Sie Ihre Geschäftsobjekte jetzt mithilfe von Tags organisieren. Tags sind eine schnelle und einfache Möglichkeit, Objekte zu klassifizieren, um die Suche zu verbessern. Diese Funktion befindet sich derzeit in der Beta-Phase und steht nur für Journeys zur Verfügung.</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/tags.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


### Verbesserungen {#mar-2023-improvements}

**Journeys**

* Die neue **Einschränkungs-API** ermöglicht es Ihnen, die Anzahl der pro Sekunde gesendeten Ereignisse zu begrenzen, wodurch überwältigende Traffic-Spitzen auf Ihren externen Systemen oder in Ihrer API verhindert werden. Wenn das festgelegte Limit erreicht ist, werden alle nachfolgenden API-Aufrufe in der Reihenfolge, in der sie empfangen wurden, in die Warteschlange gestellt und so bald wie möglich verarbeitet. Beachten Sie, dass diese Funktion nur eine Einschränkungskonfiguration für alle Sandboxes unterstützt. [Weitere Informationen](../configuration/external-systems.md)
* Die Journey-Arbeitsfläche wurde verbessert, um das Benutzererlebnis zu vereinfachen und zu verbessern. Am Ende jedes Pfads auf der Arbeitsfläche wurden die leeren Platzhalter entfernt. Jetzt können Sie Ihre Aktivitäten einfach hinzufügen, indem Sie sie an das Ende eines Pfads ziehen.
* Auf der Journey-Arbeitsfläche ist der Titel der **Ende** -Tag nicht mehr automatisch mit dem Namen der vorherigen Aktivität festgelegt wird. Benutzer können bei Bedarf manuell eine benutzerdefinierte Bezeichnung hinzufügen.
* Die standardmäßige Timeout- und Fehlerdauer in den Journey-Eigenschaften wurde von 5 auf 30 Sekunden geändert. [Weitere Informationen](../configuration/external-systems.md#timeout)
* Die standardmäßige Drosselungsrate in Aktivitäten mit Lesesegmenten wurde von 20.000 auf 5.000 Nachrichten pro Sekunde geändert. [Weitere Informationen](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

<!-- 
* When adding an Email, SMS or Push action in a journey, the surface is now pre-filled, by default, with the last used surface for that channel.
* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)
* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)
* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->

**Entscheidungs-Management**

* Um eine mögliche Verwechslung mit der kürzlich veröffentlichten Tags-Funktion in Adobe Experience Platform zu vermeiden, wurden Entscheidungs-Management-Tags in „Sammlungsqualifizierer“ umbenannt.

   Beachten Sie, dass der Begriff „Tag“ zwar nicht mehr in der Benutzeroberfläche des Entscheidungs-Managements verwendet wird, aber weiterhin in Backend-Diensten wie APIs und Datensätzen zu finden ist.

* Sie können den Angebotsbegrenzungszähler auf täglicher, wöchentlicher oder monatlicher Basis zurücksetzen. [Weitere Informationen](../offers/offer-library/add-constraints.md#capping)

* Sie können auch festlegen, welches Adobe Experience Platform-Ereignis nach einer Entscheidungs-Management-Begrenzung geprüft werden soll. [Weitere Informationen](../offers/offer-library/add-constraints.md#capping)

<!--* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--**Personalization**

* You can now include default fallback text for string-based profile attributes in the Expression Editor. These values will display if the selected attributes return no result. [Learn more](../personalization/personalization-build-expressions.md#add)-->

<!--
**Reporting**

* The reporting widget functionality has been improved with the ability to customize how users view their data. With this improvement, users can now choose between multiple visualization options, including graph, table, and donut charts.

    To have access to the latest widgets, please note that you will have to reset the different reporting dashboards. For more information on dashboard customization, refer to the [detailed documentation](../reports/global-report.md#modify-dashboard).
-->

## Versionshinweise Februar 2023 {#feb-2023}

### Neue Funktionen{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>In-App-Kanal (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Es können nun innerhalb einer Kampagne personalisierte In-App-Nachrichten an Benutzende Ihrer App gesendet werden. Mit Journey Optimizer können Benachrichtigungen entworfen und das Nachrichten-Layout, die Anzeige, der Text und die Schaltflächen angepasst werden, um ein nahtloses Erlebnis zu schaffen.</p>
<p><strong>Vorsicht</strong> – Diese Funktion befindet sich derzeit in der Beta-Version und steht nur der Beta-Kundschaft zur Verfügung. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../in-app/get-started-in-app.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Exportieren von Journey Optimizer-Datensätzen in Cloud-Speicher-Ziele (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Es kann jetzt eine Live-Verbindung mit Cloud-Speicherorten hergestellt werden, um den Inhalt der Datensätze zu exportieren. Verfügbare Ziele sind: Amazon S3-Cloud-Speicherziele, Azure Blob, Azure Data Lake Gen 2, Data Landing Zone, Google Cloud Storage, SFTP.</p>
<p><strong>Vorsicht</strong> – Diese Funktion befindet sich derzeit in der Beta-Phase und steht allen Adobe Journey Optimizer-Benutzenden zur Verfügung. Bitte wenden Sie sich an den Adobe-Support, um Zugang zu Zielen zu erhalten, falls Sie noch keinen Zugang haben.</p>
<img src="assets/do-not-localize/gif-destinations.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../data/export-datasets.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--

<table>
<thead>
<tr>
<th><strong>Performance Measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the <strong>Objective</strong> tab of your campaign reports. </p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

+++ Learn more about Performance Measurement

The **[!UICONTROL Objective]** tab of your Campaign report allows you to better fine-tune your deliveries' reports by targeting one specific metric. With this feature, you can effectively track and analyze your campaign's performance and make informed decisions to improve your results.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of pre-configured **[!UICONTROL Objectives]** is available, but you can also customize your report by adding new **[!UICONTROL Datasets]** and defining your own objectives. 

By selecting the desired Objectives, the **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets provide a comprehensive and insightful summary of your delivery performance, allowing you to closely monitor and evaluate the success of your campaign.

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your primary objective against another performance metric.

Note that each widget can be resized and deleted as needed.
+++




<table>
<thead>
<tr>
<th><strong>Use Tags in your Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer practitioner, you can now organize your business objects using tags. Tags are a quick and easy way of classifying objects to improve search. Tags are currently only available for Journeys.</p>
</td>
</tr>
</tbody>
</table>

-->

### Verbesserungen {#feb-2023-improvements}

**Journeys**

* Das Feld **Wartezeit bis zum erneuten Eintritt** wurde zu den Journey-Eigenschaften hinzugefügt. In diesem Feld kann die Wartezeit definiert werden, bevor es einem Profil erlaubt wird, in unitären Journeys erneut in die Journey einzutreten (beginnend mit einem Ereignis oder einer Segmentqualifikation). Dadurch wird verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Standardmäßig ist das Feld auf 5 Minuten eingestellt. [Weitere Informationen](../building-journeys/journey-gs.md#entrance)

* Es wurden Verbesserungen in Bezug auf die **Start- und Enddaten einer Journey** vorgenommen. Wenn kein Startdatum angegeben wurde, wird es jetzt automatisch zum Veröffentlichungszeitpunkt hinzugefügt. Für **Segment-lesen**-Journeys kann jetzt ein Enddatum hinzugefügt werden. Dadurch können Profile beim Erreichen des Datums automatisch die Journey verlassen. [Weitere Informationen](../building-journeys/journey-gs.md#dates)

<!--

* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty placeholders have been removed. You can now simply add your activities by dragging them anywhere between nodes. [Learn more](../building-journeys/using-the-journey-designer.md)

* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->


**Administration**

* **Zulassungsliste** – Die Zulassungsliste kann jetzt als CSV-Datei heruntergeladen werden. [Weitere Informationen](../configuration/allow-list.md#download-allowed-list)

* **E-Mail-Oberfläche** – Eine zusätzliche Prüfung wurde zu den E-Mail-Oberflächeneinstellungen hinzugefügt: Wenn der MX-Eintrag für die in der **Antwortadresse (E-Mail)** oder der **BCC-E-Mail-Adresse** verwendete Subdomain nicht ordnungsgemäß konfiguriert ist, kann die E-Mail-Oberfläche nicht mehr erstellt werden. Sie müssen ihn konfigurieren oder einen anderen verwenden. [Weitere Informationen](../email/email-settings.md#reply-to-email)

* **E-Mail-Oberfläche** – Im Bereich **URL-Tracking-Parameter** in den E-Mail-Oberflächeneinstellungen wurde die Begrenzung für jedes **Wert**-Feld aus Gründen der Kompatibilität mit Adobe Analytics-Tracking von 255 Zeichen auf 5 KB aktualisiert. [Weitere Informationen](../email/email-settings.md#url-tracking)

**Entscheidungs-Management**

<!--
* **Placements** - Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)
-->

* **URL-Personalisierung** – Beim Hinzufügen von URLs als Inhalt zu den Darstellungen von Angeboten können diese URLs jetzt mit dem Ausdruckseditor personalisiert werden. [Weitere Informationen](../offers/offer-library/add-representations.md)

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
<p>Adobe Experience Platform bietet eine Reihe von Funktionen zur Datenhygiene, mit denen Sie Ihre gespeicherten Daten durch programmgesteuerte Löschungen der Aufzeichnungen und Datensätze von Kundinnen und Kunden verwalten können. Diese Funktion ist jetzt für Adobe Journey Optimizer verfügbar. </p>
<p>Sie können Ihre Datenspeicher verwalten, um sicherzustellen, dass Informationen erwartungsgemäß verwendet werden, dass sie aktualisiert werden, wenn falsche Daten korrigiert werden müssen, und dass sie gelöscht werden, wenn dies aufgrund von Richtlinien der Organisation erforderlich ist.</p>
<p><strong>Achtung</strong> – Die Funktionen zur Datenhygiene stehen derzeit nur Organisationen zur Verfügung, die die Zusatzangebote <strong>Healthcare Shield</strong> und <strong>Privacy and Security Shield</strong> erworben haben.</p><p>Weitere Informationen finden Sie in der <a href="../privacy/data-hygiene.md">ausführlichen Dokumentation</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>E-Mail-Inhaltsvorlagen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt eigenständige Inhaltsvorlagen erstellen, die schnell in Journeys und Kampagnen wiederverwendet werden können.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>Wie Sie Inhaltsvorlagen erstellen, bearbeiten und verwenden, erfahren Sie in <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html?lang=de">diesem Video</a>. Weitere Informationen finden Sie in der <a href="../email/content-templates.md">ausführlichen Dokumentation</a>.
</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#jan-2023-improvements}

**Journeys**

* Beim Hinzufügen von **Segmentqualifizierung** oder **Segment lesen** in einer Journey ist der Namespace jetzt standardmäßig mit dem zuletzt verwendeten Namespace vorausgefüllt. Siehe dazu die Abschnitte [Segmentqualifizierung](../building-journeys/segment-qualification-events.md#about-segment-qualification) und [Segment lesen](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Auf der Journey-Arbeitsfläche ist eine neue Schaltfläche in der Symbolleiste verfügbar, mit der Sie einen Screenshot Ihrer Journey herunterladen können.

**E-Mail-Designer**

* Sie können jetzt über das Menü **HTML exportieren** den E-Mail-Inhalt exportieren. Exportierte Dateien sind in einer ZIP-Archivdatei verfügbar.

**Administration**

* Ein neuer Unterabschnitt enthält Empfehlungen zum Erstellen der Adresse für **Antwort an (E-Mail)** und gewährleistet eine ordnungsgemäße Antwortverwaltung. [Weitere Informationen](../email/email-settings.md#reply-to-email)

* Beim Erstellen oder Bearbeiten von **IP-Pools** werden die zugehörigen PTR-Einträge jetzt in der IP-Liste angezeigt, und ebenfalls, wenn Sie den Mauszeiger über die ausgewählten IP-Adressen bewegen. [Weitere Informationen](../configuration/ip-pools.md#create-ip-pool)

* Nachdem ein IP-Pool auf einer Kanaloberfläche ausgewählt wurde, sind jetzt Informationen zum PTR-Eintrag sichtbar, wenn Sie den Mauszeiger über die IP-Adressen bewegen. [Weitere Informationen](../email/email-settings.md#subdomains-and-ip-pools)

* Die Benutzeroberfläche zur Bearbeitung von [PTR-Einträgen](../configuration/ptr-records.md#edit-ptr-record) und [Ausführungsfeldern](../configuration/primary-email-addresses.md) wurde aktualisiert.

* Die Benutzeroberfläche zum Erstellen und Bearbeiten von Subdomains wurde verbessert. [Weitere Informationen](../configuration/delegate-subdomain.md)

* Der Bildschirm **Letzte Uploads** der Unterdrückungsliste wurde aktualisiert. [Weitere Informationen](../configuration/manage-suppression-list.md#recent-uploads)

**Kampagnen**

* Eine Beispiel-cURL-Anfrage, die die Ausführung API-ausgelöster Kampagnen ermöglicht, wird jetzt automatisch generiert und im Kampagnenbildschirm bereitgestellt. [Weitere Informationen](../campaigns/api-triggered-campaigns.md)


**Personalisierung**

* Neue Hilfsfunktionen sind verfügbar: formatCurrency, charCodeAt, stringToDate, toString, formatNumber und toHexString. Darüber hinaus akzeptiert die Funktion toDateTimeOnly jetzt die Feldtypen string, date, long und int. [Weitere Informationen](../personalization/functions/functions.md)
