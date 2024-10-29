---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 2fb8113f4ae85b661a3ea967327e6a0b532fc48f
workflow-type: tm+mt
source-wordcount: '1428'
ht-degree: 48%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in diesen Versionshinweisen in der letzten Woche jedes Monats konsolidiert. [!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Version Oktober 24 {#24-10-rn}

**Veröffentlichungsdatum**: 29.-30. Oktober 2024

### Neue Funktionen {#24-10-features}

Mit dieser Version werden die folgenden neuen Funktionen eingeführt:

<table>
<thead>
<tr>
<th><strong>Sperren von E-Mail-Inhalten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ermöglicht es nun, Inhalte in E-Mail-Vorlagen zu sperren, entweder durch Sperren der gesamten Vorlage oder durch Sperren bestimmter Strukturen und Komponenten. Auf diese Weise können Sie unbeabsichtigte Bearbeitungen oder Löschungen verhindern, sodass Sie das Anpassen von Vorlagen besser steuern und die Effizienz sowie Zuverlässigkeit Ihrer E-Mail-Kampagnen optimieren können.</p>
<p>Weitere Informationen finden Sie in der <a href="../content-management/content-locking.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
<p>Verfügbar seit dem 24. Oktober 2024</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Code-basierte Erlebnisse in Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dem Code-basierten Erlebniskanal ermöglicht Ihnen Adobe Journey Optimizer eine erweiterte Personalisierung und Tests für jede Ihrer eingehenden Eigenschaften durchzuführen. Dies ermöglicht den nahtlosen Versand von maßgeschneiderten Erlebnissen über verschiedene Touchpoints wie Web-Apps, Mobile-Apps, Desktop-Apps, Videokonsolen, mit dem Fernseher verbundene Geräte, Smart-TVs, Kioske, Geldautomaten, IoT-Geräte und mehr. Der Code-basierte Erlebniskanal ist jetzt auf der Journey-Arbeitsfläche verfügbar.</p>
<p>Weitere Informationen finden Sie in der <a href="../code-based/create-code-based.md">ausführlichen Dokumentation</a>.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
<p>Verfügbar seit dem 1. Oktober 2024</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web-Erlebnisse in Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dem Webkanal ermöglicht Ihnen Adobe Journey Optimizer das Web-Erlebnis zu personalisieren, das Sie Ihren Kundinnen und Kunden über eingehende Web-Journeys bereitstellen. Der Web-Kanal ist jetzt auf der Journey-Arbeitsfläche verfügbar.</p>
<p>Weitere Informationen finden Sie in der <a href="../web/create-web.md">ausführlichen Dokumentation</a>.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
<p>Verfügbar seit dem 1. Oktober 2024</p>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Conflict and priority management (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer, managing the volume and timing of campaigns and journeys is essential to avoid overwhelming customers with too many interactions. Journey Optimizer now offers several tools for conflict management and prioritization.</p><p><ul><li><b>Journey frequency capping</b>: You can now create rule sets to apply to your journeys, allowing you to limit the number of journeys for a profile per day, week, or month, as well as control the number of concurrent journeys running simultaneously.</li>
<li><b>Priority score</b>: You can now assign a priority score to a campaign or a journey, ranging from 0 to 100. A higher number indicates a higher priority. When two campaigns or journey actions use the same channel configuration, Journey Optimizer will select the one with the highest priority score. If the campaigns have the same score, the campaign that was least recently modified will be chosen.</li>
<li><b>View potential conflicts</b>: A new "View potential conflicts" button in journeys and campaigns now allows you to identify overlap with other journeys or campaigns such as the start date, the targeted audience, or the selected channel configuration.</li>
<li><b>Journey Arbitration</b>: This new capability enables you to prioritize the most important journeys for your customers. You can create a rule to suppress entry into a lower priority journey when a customer qualifies for an upcoming journey of higher priority.</li>
<li><b>Frequency capping by communication type: </b>With rule sets, you can now set granular rules by communication type (e.g., Sales, Promotional) to prevent overloading customers with similar messages. You can control frequency across multiple channels, automatically excluding over-solicited profiles to ensure a better customer experience.</li></ul>
<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>
<p>Conflict and priority management capabilities are available in Limited Availability to a select group of customers. Please note that these features will be gradually rolled out to more users in the future. Reach out to your account team if interested in being added to the waitlist for these features.</p>
</td>
</tr>
</tbody>
</table>-->


<table>
<thead>
<tr>
<th><strong>Integration von Wechselfarben und Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Movable Ink Da Vinci und Adobe Journey Optimizer integrieren. Mit dieser neuen Integration können Sie: </p>
<p><ul><li>Nutzen Sie die leistungsstarken Funktionen von Movable Ink's Da Vinci, um E-Mail-Varianten für Batch-Kampagnen zusammenzustellen und zu personalisieren.</li>
<li>Beschleunigen Sie Workflows für Journey Optimizer-Kunden, die Da Vinci für die Bearbeitung und Adobe Journey Optimizer für die Optimierung und Bereitstellung verwenden.</li>
<li>Optimieren Sie Da Vinci-Modelle mit Adobe-Daten.</li></ul></p>
<p>Weiterführende Informationen finden Sie in der Dokumentation zu <a href="https://movableink.com/adobe-and-movable-ink">Movable Ink Da Vinci</a> .</p>
</tr>
</tbody>
</table>

Zuvor für eine Reihe von Organisationen (LA) verfügbar, sind jetzt die folgenden Funktionen für alle Benutzer verfügbar (GA):

<table>
<thead>
<tr>
<th><strong>Personalisierung der E-Mail-Konfiguration (Allgemeine Verfügbarkeit) </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Für mehr Flexibilität und Kontrolle über Ihre E-Mail-Einstellungen können Sie beim Erstellen von E-Mail-Kanalkonfigurationen dynamische Subdomains und personalisierte Header-Parameter definieren.
</p>
<p>Weitere Informationen finden Sie in der <a href="../email/surface-personalization.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/surface-perso.gif"/>
<p>Verfügbar seit dem 23. Oktober 2024</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Genehmigungen in Journey und Kampagnen (Allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Genehmigungsrichtlinien können Sie nun einen Genehmigungsprozess in Journey Optimizer einrichten, mit dem Marketing-Teams sicherstellen können, dass Kampagnen und Journeys vor ihrer Live-Schaltung von den jeweiligen Stakeholdern geprüft und abgezeichnet werden.</p>
<p>Weitere Informationen finden Sie in der <a href="../test-approve/gs-approval.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
<p>Verfügbar seit dem 22. Oktober 2024</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Inhaltsexperimentierung in Journey (Allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ist bereits in Kampagnen verfügbar und unterstützt jetzt Experimente in Journeys. Bei Experimenten handelt es sich um randomisierte Test, was im Rahmen von Online-Tests bedeutet, dass Sie einigen zufällig ausgewählten Benutzenden eine bestimmte Variante einer Nachricht anbieten und einer anderen zufällig ausgewählten Gruppe von Benutzenden eine andere Variante oder Abwandlung anbieten. Nach dem Angebot können Sie die Ihre gewünschten Ergebnismetriken messen, z. B. Öffnung von E-Mails, Abonnements oder Käufe.</p>
<p>Weitere Informationen finden Sie in der <a href="../content-management/content-experiment.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Decisioning (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning, previously available for a set of organizations (LA) and known as Experience Decisioning, is now available to all users (GA), including organizations that have purchased the Adobe Healthcare Shield or Privacy and Security Shield add-on offerings.</p><p>Decisioning simplifies personalization by offering a centralized catalog of marketing offers known as 'decision items' and a sophisticated decision engine. This engine leverages rules and ranking criteria to select and present the most relevant decision items to each individual. These decision items are seamlessly integrated into a wide range of inbound surfaces through the code-based experience channel.</p>
<p>For more information, refer to the <a href="../experience-decisioning/gs-experience-decisioning.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<!--table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns (General availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now effortlessly create content in multiple languages within a single campaign or journey. With this feature, you can switch between languages when editing your campaign or your journey, streamlining the entire editing process and improving your capability to efficiently manage multilingual content.</p>
<p>For more information, refer to the <a href="../content-management/multilingual-gs.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/multilingual.gif">
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Aktualisiertes Berichtserlebnis (Allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Reporting ist jetzt allgemein verfügbar (GA) und verfügt über eine verbesserte Interoperabilität mit Customer Journey Analytics-Funktionen, Standardisierung der Berichterstellung auf beiden Plattformen und Verbesserung der Datenkonsistenz und -zuverlässigkeit. Diese nahtlose Integration zwischen Journey Optimizer und Customer Journey Analytics bietet einen klareren Überblick über Leistungsmetriken und ermöglicht es Benutzenden, besser fundierte Entscheidungen zu treffen.</p>
<p>Mit der allgemeinen Verfügbarkeit werden vier neue Funktionen eingeführt: die Möglichkeit, einfache Metriken zu erstellen, Zielgruppen zu erstellen und zu veröffentlichen, Ad-hoc-Fragen mit Insight Builder zu stellen und Berichte so zu planen, dass sie automatisch per E-Mail an wichtige Empfänger gesendet werden.</p>
<p>Weitere Informationen finden Sie in der <a href="../reports/report-cja-manage.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Wichtig: Die aktuelle Berichtserfahrung wird ab Januar 2025 eingestellt. Nach diesem Datum wird das neue Reporting-Erlebnis zum Standard. Wir empfehlen, sich mit den neuen Funktionen und Funktionalitäten vertraut zu machen, um einen reibungslosen Übergang zu gewährleisten. <a href="../reports/report-gs-cja.md">Informationen zu den ersten Schritten mit der neuen Reporting-Oberfläche von Journey Optimizer</a></p>
<p>Verfügbar seit dem 16. Oktober 2024</p>
</tr>
</tbody>
</table>


<!--The following capabilities are available to all customers in public beta:

<table>
<thead>
<tr>
<th><strong>Test your content using sample input data (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey optimizer now allows you to test different variants of your email content by previewing it and sending proofs using sample input data uploaded from a file or added manually. All the profiles attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p>
<p>This capability is currently available to all customers as a public beta.</p>
<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<!--<table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from Adobe Experience Platform in the personalization editor to personalize your content. To do this, datasets needed for lookup personalization must first be enabled through an API call. Once done, you can use their data to personalize your content into [!DNL Journey Optimizer].</p>
<p>This capability is currently available to all customers as a public beta.</p>
<p>For more information, refer to the <a href="../personalization/lookup-aep-data.md"</a>.</p>
</td>
</tr>
</tbody>
</table>-->

### Verbesserungen {#24-10-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**SMS-Kanal**

SMS-Verbesserungen wurden eingeführt, um Ihre Nachrichtenfunktionen zu verbessern:

* Sie können eindeutige Suchbegriffe für Ihre SMS-Kampagnen und Journey definieren und verwalten, um eine personalisiertere und effizientere Kommunikation zu ermöglichen.

* Sie können eine Standard-SMS-Nachricht erstellen und versenden, wenn ein Schlüsselwort nicht erkannt wird.

* Jetzt können Sie eine SMS-API-Kanalkonfiguration bearbeiten oder löschen.

Weitere Informationen zu diesen Verbesserungen finden Sie in der Dokumentation zur SMS-Konfiguration für [Infobip](../sms/sms-configuration-infobip.md) und [Sinch](../sms/sms-configuration-sinch.md).

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

&lt;!—* **Maximale Anzahl Live-Journey** - Journey Optimizer verfügt jetzt über einen Schutzmechanismus von 500 Live-Journey auf Produktions-Sandboxes anstelle von 100. Die Anzahl der Live-Journey ist auf der Journey-Arbeitsfläche sichtbar. <!-- DOCAC-10977-->

**Web-Kanal**

* **Nicht visueller Bearbeitungsmodus für den Webdesigner** - Als Alternative zum Journey Optimizer-Webdesigner können Sie jetzt Änderungen an Ihrer Website mit einem nicht visuellen Editor hinzufügen. Sie können Ihre Änderungen manuell eingeben, ohne die Seiten im Visual Editor zu öffnen. Dieser nicht visuelle Bearbeitungsmodus ist nützlich, wenn Sie keine Browsererweiterungen wie Adobe Experience Cloud Visual Helper installieren können, die zum Laden Ihrer Seiten in den Webdesigner erforderlich sind. [Weitere Informationen](../web/web-non-visual-editor.md)


**Datensätze**

* **Ereignisse senden und öffnen** - Ab dem 1. November 2024 bietet Streaming-Segmentierung keine Unterstützung mehr für das Senden und Öffnen von Ereignissen aus Journey Optimizer-Tracking und Feedback-Datensätzen. Diese Änderung gilt für alle Kunden-Sandboxes und -Organisationen. [Weitere Informationen](../data/datasets-ttl.md#segmentation-update)

* **Datensatzzeit bis zur Live-Schaltung (TTL)** - Ab Februar 2025 wird ein TTL-Schutzmechanismus (Time-to-Live) in systemgenerierten Journey Optimizer-Datensätzen in neuen Sandboxes und neuen Organisationen wie folgt bereitgestellt:

   * 90 Tage für Daten im Profilspeicher
   * 13 Monate für Daten im Data Lake

  Diese Änderung wird in einer nachfolgenden Phase auf bestehende Kunden-Sandboxes übertragen. [Weitere Informationen](../data/datasets-ttl.md#ttl)

* **Parameter in benutzerdefinierten Aktionen** (Verfügbarkeitsdatum: 3. Oktober 2024) - NULL und optionale Parameter werden jetzt in benutzerdefinierten Aktionen unterstützt. [Weitere Informationen](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Reporting**

* **Berichte zu Erlebnisentscheidungen** ist jetzt verfügbar und bietet wichtige Einblicke in die Interaktion Ihrer Besucher mit Ihren Erlebnissen. [Weitere Informationen](../reports/campaign-global-report-cja-code.md##decisioning-kpis)

**Richtlinien für Data Governance und Einverständnis** – Verfügbarkeitsdatum: 7. Oktober 2024

* Die Durchsetzung der **Data Governance-Richtlinien** erfolgt jetzt über alle Kanäle in Journey Optimizer. Kunden, die Richtlinien in Adobe Experience Platform erstellt haben, werden diese im Rahmen der Einrichtung der Kanalkonfigurationen auf Marketing-Aktionen angewendet. Wenn Sie Inhalte mithilfe einer Konfiguration erstellen, prüft das System alle Personalisierungsfelder auf Verstöße gegen die Data Governance. Wenn ein Verstoß festgestellt wird, ist die Veröffentlichung einer Journey oder Kampagne nicht möglich. [Weitere Informationen](../action/action-privacy.md)

* **Benutzerdefinierte Einverständnisrichtlinien** gelten jetzt für alle Journey Optimizer-Kanäle. Bei der Durchsetzung vor dem Versand einer Nachricht oder der Zustellung eines eingehenden Erlebnisses prüft das System, ob die Benutzerin oder der Benutzer die Zustimmung zur Verwendung von Personalisierungsfeldern in den Inhalten erteilt hat, die erhalten werden. Wenn kein Einverständnis erteilt wird, wird das Erlebnis nicht angezeigt. [Weitere Informationen](../action/consent.md)

  >[!NOTE]
  >
  >Einverständnisrichtlinien sind derzeit nur für Organisationen verfügbar, die die Zusatzangebote Adobe **Healthcare Shield** und **Privacy and Security Shield** erworben haben.

**Zielgruppen** – Verfügbarkeitsdatum: 8. Oktober 2024

* Beim Targeting einer CSV-Datei-Zielgruppe können Sie jetzt Attribute aus der Datei im Personalisierungseditor und im Regel-Builder für Journeys und Kampagnen verwenden. [Weitere Informationen](../audience/about-audiences.md)

* Zielgruppen und Attribute aus benutzerdefinierten Uploads (CSV-Dateien) stehen jetzt zur Verwendung mit Healthcare Shield oder Privacy and Security Shield zur Verfügung.

**Konfiguration** - Verfügbarkeitsdatum: 23. Oktober 2024

* Bei Verwendung einer personalisierten Konfiguration in einer Kampagne oder einer Journey können Sie jetzt eine Vorschau Ihres E-Mail-Inhalts anzeigen, um nach potenziellen Fehlern mit den von Ihnen definierten dynamischen Einstellungen zu suchen. [Weitere Informationen](../email/surface-personalization.md#check-configuration)

**Codebasierter Kanal**

* Inhaltsvorlagen sind jetzt verfügbar. Sie können das Authoring Ihrer code-basierten Erlebnisse beschleunigen, ausgehend von einer Inhaltsvorlage, die von Ihren Entwicklern erstellt wurde. Durch Verwendung einer Inhaltsvorlage kann der Marketing-Experte nur einige Werte oder Felder ändern, anstatt die gesamte HTML- oder JSON-Inhalts-Payload zusammenzustellen. [Weitere Informationen](../content-management/content-templates.md)

**Entscheidungsfindung**

<!--* [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html) users can now choose custom models to optimize on when setting up an AI model in Decisioning (formerly known as Experience Decisioning). This allows you, for example, to optimize on a custom "purchases" table rather than defined constraints such as clickthrough rate."-->

* Beim Hinzufügen einer Entscheidungsrichtlinie zu einer code-basierten Kampagne mit Experience Decisioning können Sie jetzt zusätzlich zu den Auswahlstrategien manuell einzelne Entscheidungselemente auswählen. Darüber hinaus können Sie jetzt mehr als ein Fallback-Angebot auswählen. Dadurch wird sichergestellt, dass eine bestimmte Anzahl von zurückgegebenen Entscheidungselementen vorhanden ist. [Weitere Informationen](../experience-decisioning/create-decision.md)
