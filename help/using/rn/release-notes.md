---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 97b6041d4b8523b11b13dd78cd8b241a6410f1bc
workflow-type: tm+mt
source-wordcount: '2103'
ht-degree: 78%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert. [!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Version Oktober 2024 {#24-10-rn}

**Veröffentlichungsdatum**: 29.–30. Oktober 2024

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


<table>
<thead>
<tr>
<th><strong>Konflikt- und Prioritäten-Management (eingeschränkte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer ist es wichtig, das Volumen und den Zeitpunkt von Kampagnen und Journeys zu steuern, um zu vermeiden, dass Kundinnen und Kunden mit zu vielen Interaktionen überfordert werden. Journey Optimizer bietet nun mehrere Tools zum Konflikt-Management und zur Priorisierung. <p>Weitere Informationen finden Sie in der <a href="../conflict-prioritization/gs-conflict-prioritization.md">ausführlichen Dokumentation</a>.</p></p><p><ul><li><b>Journey-Frequenzbegrenzung</b>: Sie können nun Regelsätze erstellen, die auf Ihre Journey angewendet werden, sodass Sie die Anzahl der Journeys für ein Profil pro Tag, Woche oder Monat begrenzen und die Anzahl gleichzeitig ausgeführter Journeys kontrollieren können.</li>
<li><b>Prioritätswert</b>: Sie können einer Kampagne oder Journey nun einen Prioritätswert zwischen 0 und 100 zuweisen. Eine höhere Zahl bedeutet eine höhere Priorität. Wenn zwei Kampagnen oder Journeys dieselbe Kanalkonfiguration verwenden, wählt Journey Optimizer die Kampagne oder Journey mit dem höchsten Prioritätswert aus. Wenn die Kampagnen den gleichen Wert aufweisen, wird die Kampagne ausgewählt, die zuletzt geändert wurde.</li>
<li><b>Potenzielle Konflikte anzeigen</b>: Mit der neuen Schaltfläche „Potenzielle Konflikte anzeigen“ in Journeys und Kampagnen können Sie nun Überschneidungen mit anderen Journeys oder Kampagnen identifizieren, z. B. beim Startdatum, bei der Zielgruppe oder bei der ausgewählten Kanalkonfiguration.</li>
<li><b>Journey Arbitration</b>: Mit dieser neuen Funktion können Sie die wichtigsten Journeys für Ihre Kundschaft priorisieren. Sie können eine Regel erstellen, um den Eintritt in eine Journey mit niedrigerer Priorität zu unterdrücken, wenn eine Kundin oder ein Kunde für eine bevorstehende Journey mit höherer Priorität qualifiziert ist.</li>
<li><b>Frequenzbegrenzung nach Kommunikationstyp: </b>Mit Regelsätzen können Sie nun granulare Regeln nach Kommunikationstyp festlegen (z. B. Vertrieb, Verkaufsförderung), um zu verhindern, dass Kundinnen und Kunden mit ähnlichen Nachrichten überhäuft werden. Sie können die Frequenz über mehrere Kanäle hinweg steuern und automatisch Profile ausschließen, die zu oft angesprochen wurden, um ein besseres Kundenerlebnis sicherzustellen.</li></ul>

<img src="assets/do-not-localize/gif-conflict.gif">

<p>Die Funktionen zum Konflikt- und Prioritäten-Management sind für eine ausgewählte Gruppe von Kundinnen und Kunden verfügbar (eingeschränkte Verfügbarkeit). Sie werden in Zukunft schrittweise für weitere Benutzende eingeführt. Wenden Sie sich an Ihr Accountteam, wenn Sie auf die Warteliste für diese Funktionen gesetzt werden möchten.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Integration von Movable Ink und Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können nun Movable Ink Da Vinci und Adobe Journey Optimizer integrieren. Diese neue Integration ermöglicht Ihnen Folgendes: </p>
<p><ul><li>Nutzen der leistungsstarken Funktionen von Movable Ink Da Vinci, um E-Mail-Varianten für Batch-Kampagnen zusammenzustellen und zu personalisieren</li>
<li>Beschleunigen Sie Workflows für Journey Optimizer-Kunden, die Da Vinci für die Bearbeitung und Adobe Journey Optimizer für die Optimierung und Bereitstellung verwenden.</li>
<li>Optimieren von Vinci-Modelle mit Adobe-Daten</li></ul></p>
<p>Weiterführende Informationen finden Sie in der Dokumentation zu <a href="https://movableink.com/adobe-and-movable-ink">Movable Ink Da Vinci</a> .</p>
</tr>
</tbody>
</table>

Zuvor für eine Reihe von Organisationen (LA) verfügbar, sind jetzt die folgenden Funktionen für alle Benutzer verfügbar (GA):

<table>
<thead>
<tr>
<th><strong>Personalisierung der E-Mail-Konfiguration (allgemeine Verfügbarkeit) </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt beim Erstellen von E-Mail-Kanal-Konfigurationen dynamische Subdomains und personalisierte Kopfzeilenparameter definieren, um mehr Flexibilität und Kontrolle über Ihre E-Mail-Einstellungen zu erhalten.
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
<th><strong>Genehmigungen in Journeys und Kampagnen (allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Genehmigungsrichtlinien können Sie nun einen Genehmigungsprozess in Journey Optimizer einrichten, mit dem Marketing-Teams sicherstellen können, dass Kampagnen und Journeys vor ihrer Live-Schaltung von den jeweiligen Stakeholderinnen und Stakeholdern geprüft und abgezeichnet werden.</p>
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
<th><strong>Inhaltsexperimente in Journeys (allgemeine Verfügbarkeit)</strong><br/></th>
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


<table>
<thead>
<tr>
<th><strong>Entscheidungsfindung (allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Entscheidungsfindung, die zuvor nur für eine Reihe von Organisationen verfügbar gewesen ist (LA) und „Erlebnis-Entscheidung“  genannt wurde, steht jetzt allen Benutzenden zur Verfügung (GA). Dazu gehören auch Organisationen, die die Zusatzangebote Adobe Healthcare Shield und Privacy and Security Shield erworben haben.</p><p>Die Entscheidungsfindung vereinfacht die Personalisierung, indem sie einen zentralisierten Katalog von Marketing-Angeboten, die als „Entscheidungselemente“ bezeichnet werden, und eine ausgereifte Entscheidungs-Engine anbietet. Diese Engine nutzt Regeln und Rangfolgekriterien, um die relevantesten Entscheidungselemente für jeden Kontakt auszuwählen und darzustellen. Diese Entscheidungselemente sind über den Code-basierten Erlebniskanal nahtlos in eine breite Palette eingehender Oberflächen integriert. </p>
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/gs-experience-decisioning.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mehrsprachige Nachrichten in Journeys und Kampagnen (allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt im Rahmen einer Kampagne oder Journey mühelos Inhalte in mehreren Sprachen erstellen.  Mit dieser Funktion können Sie bei der Bearbeitung Ihrer Kampagne oder Journey zwischen Sprachen wechseln, den gesamten Bearbeitungsvorgang optimieren und Ihre mehrsprachigen Inhalte effizienter verwalten.</p>
<p>Weitere Informationen finden Sie in der <a href="../content-management/multilingual-gs.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/multilingual.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Neues Reporting-Erlebnis (allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Das Journey Optimizer-Reporting ist nun allgemein verfügbar und bietet eine verbesserte Kompatibilität mit Customer Journey Analytics-Funktionen, wodurch die Berichterstellung plattformübergreifend standardisiert und die Datenkonsistenz und -zuverlässigkeit optimiert wird. Diese nahtlose Integration zwischen Journey Optimizer und Customer Journey Analytics bietet einen klareren Überblick über Leistungsmetriken und ermöglicht es Benutzenden, fundiertere Entscheidungen zu treffen.</p>
<p>Mit der allgemeinen Verfügbarkeit werden vier neue Funktionen eingeführt: die Möglichkeit, einfache Metriken zu erstellen, Zielgruppen zu erstellen und zu veröffentlichen, Ad-hoc-Fragen mit Insight Builder zu stellen und Berichte so zu planen, dass sie automatisch per E-Mail an wichtige Empfänger gesendet werden.</p>
<p>Weitere Informationen finden Sie in der <a href="../reports/report-cja-manage.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Wichtig: Die aktuelle Berichtserfahrung wird ab Januar 2025 eingestellt. Nach diesem Datum wird das neue Reporting-Erlebnis zum Standard. Wir empfehlen, sich mit den neuen Funktionen und Funktionalitäten vertraut zu machen, um einen reibungslosen Übergang zu gewährleisten. <a href="../reports/report-gs-cja.md">Informationen zu den ersten Schritten mit der neuen Reporting-Oberfläche von Journey Optimizer</a></p>
<p>Verfügbar seit dem 16. Oktober 2024</p>
</tr>
</tbody>
</table>

<!--The following capabilities are available to all customers in public beta:-->

<table>
<thead>
<tr>
<th><strong>Testen von Inhalten mit Beispieleingabedaten (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Journey Optimizer können Sie jetzt verschiedene Varianten Ihres Inhalts testen, indem Sie eine Vorschau davon anzeigen und E-Mail-Testsendungen mit Beispieleingabedaten durchführen, die aus einer Datei hochgeladen oder manuell hinzugefügt wurden. Alle Profilattribute, die in Ihren Inhalten für die Personalisierung verwendet werden, werden automatisch vom System erkannt und können für Ihre Tests zur Erstellung mehrerer Varianten verwendet werden.</p>
<p>Diese Funktion steht derzeit allen Kunden als öffentliche Beta-Version für die Benachrichtigungskanäle E-Mail, SMS und Push-Benachrichtigung zur Verfügung.</p>
<p>Weitere Informationen finden Sie in der <a href="../test-approve/simulate-sample-input.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/gif-simulate.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Adobe Experience Platform-Daten für die Personalisierung verwenden (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nutzen Sie Daten aus Adobe Experience Platform im Personalisierungs-Editor, um Ihre Inhalte zu personalisieren. Dazu müssen Datensätze, die für die Lookup-Personalisierung erforderlich sind, zunächst über einen API-Aufruf aktiviert werden. Danach können Sie ihre Daten verwenden, um Ihren Inhalt in [!DNL Journey Optimizer] zu personalisieren.</p>
<p>Diese Funktion steht derzeit allen Kundinnen und Kunden als öffentliche Betaversion zur Verfügung.</p>
<p>Weitere Informationen finden Sie in der <a href="../personalization/lookup-aep-data.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#24-10-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**SMS-Kanal**

* Jetzt können Sie eine SMS-API-Kanalkonfiguration bearbeiten oder löschen. [Weitere Informationen](../sms/sms-configuration.md)

* Die folgenden Verbesserungen wurden eingeführt, um Ihre SMS-Nachrichtenfunktionen mit Infobip und Sinch zu verbessern:

   * Sie können eindeutige Keywords für Ihre SMS-Kampagnen und Journeys definieren und verwalten, um eine personalisiertere und effizientere Kommunikation zu ermöglichen.

   * Sie können eine standardmäßige SMS-Nachricht erstellen und senden, wenn ein Keyword nicht erkannt wird.

  Weitere Informationen zu diesen Verbesserungen finden Sie in der Dokumentation zur SMS-Konfiguration für [Infobip](../sms/sms-configuration-infobip.md) und [Sinch](../sms/sms-configuration-sinch.md).


<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

<!--* **Max number of Live journeys** - Journey Optimizer now has a guardrail of 500 live journeys on production sandboxes, instead of 100. The number of live journeys is visible in the journey canvas. (DOCAC-10977) -->

**Web-Kanal**

* **Nicht visueller Bearbeitungsmodus für den Webdesigner** - Als Alternative zum Journey Optimizer-Webdesigner können Sie jetzt Änderungen an Ihrer Website mit einem nicht visuellen Editor hinzufügen. Sie können Ihre Änderungen manuell eingeben, ohne die Seiten im Visual Editor zu öffnen. Dieser nicht visuelle Bearbeitungsmodus ist nützlich, wenn Sie keine Browsererweiterungen wie Adobe Experience Cloud Visual Helper installieren können, die zum Laden Ihrer Seiten in den Webdesigner erforderlich sind. [Weitere Informationen](../web/web-non-visual-editor.md)


**Datensätze**

* **Sende- und Öffnungsereignisse**: Ab dem 1. November 2024 unterstützt die Streaming-Segmentierung die Verwendung von Sende- und Öffnungsereignissen aus Tracking- und Feedback-Datensätzen von Journey Optimizer nicht mehr. Diese Änderung gilt für alle Kunden-Sandboxes und Organisationen. [Weitere Informationen](../data/datasets-ttl.md#segmentation-update)

* **Time-to-Live (TTL) für Datensätze**: Ab Februar 2025 wird in neuen Sandboxes und neuen Organisationen für systemgenerierte Journey Optimizer-Datensätze das folgende Time-to-Live(TTL)-Limit eingeführt:

   * 90 Tage für Daten im Profilspeicher
   * 13 Monate für Daten im Data Lake

  Diese Änderung wird in einer nachfolgenden Phase in bestehende Kunden-Sandboxes integriert. [Weitere Informationen](../data/datasets-ttl.md#ttl)

* **Parameter in benutzerdefinierten Aktionen** - Verfügbarkeitsdatum: 3. Oktober 2024 - NULL und optionale Parameter werden jetzt in benutzerdefinierten Aktionen unterstützt. [Weitere Informationen](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Reporting**

* **Entscheidungsberichte** sind jetzt verfügbar und bieten wichtige Einblicke in die Interaktion Ihrer Besucher mit Ihren Erlebnissen. [Weitere Informationen](../reports/campaign-global-report-cja-code.md#decisioning-kpis)

**Richtlinien für Data Governance und Einverständnis** – Verfügbarkeitsdatum: 7. Oktober 2024

* Die Durchsetzung der **Data Governance-Richtlinien** erfolgt jetzt über alle Kanäle in Journey Optimizer. Kunden, die Richtlinien in Adobe Experience Platform erstellt haben, werden diese im Rahmen der Einrichtung der Kanalkonfigurationen auf Marketing-Aktionen angewendet. Wenn Sie Inhalte mithilfe einer Konfiguration erstellen, prüft das System alle Personalisierungsfelder auf Verstöße gegen die Data Governance. Wenn ein Verstoß festgestellt wird, ist die Veröffentlichung einer Journey oder Kampagne nicht möglich. [Weitere Informationen](../action/action-privacy.md)

* **Benutzerdefinierte Einverständnisrichtlinien** gelten jetzt für alle Journey Optimizer-Kanäle. Bei der Durchsetzung vor dem Versand einer Nachricht oder der Zustellung eines eingehenden Erlebnisses prüft das System, ob die Benutzerin oder der Benutzer die Zustimmung zur Verwendung von Personalisierungsfeldern in den Inhalten erteilt hat, die erhalten werden. Wenn kein Einverständnis erteilt wird, wird das Erlebnis nicht angezeigt. [Weitere Informationen](../action/consent.md)

  >[!NOTE]
  >
  >Einverständnisrichtlinien sind derzeit nur für Organisationen verfügbar, die die Zusatzangebote Adobe **Healthcare Shield** und **Privacy and Security Shield** erworben haben.

**Zielgruppen** – Verfügbarkeitsdatum: 8. Oktober 2024

* Beim Targeting einer CSV-Datei-Zielgruppe können Sie jetzt Attribute aus der Datei im Personalisierungseditor und im Regel-Builder für Journeys und Kampagnen verwenden. [Weitere Informationen](../audience/about-audiences.md)

* Zielgruppen und Attribute aus benutzerdefinierten Uploads (CSV-Dateien) stehen jetzt zur Verwendung mit Healthcare Shield oder Privacy and Security Shield zur Verfügung.

**Konfiguration** – Verfügbarkeitsdatum: 23. Oktober 2024

* Durch eine personalisierte Konfiguration in einer Kampagne oder Journey können Sie eine Vorschau Ihrer E-Mail-Inhalte anzeigen, um nach potenziellen Fehlern mit den von Ihnen definierten dynamischen Einstellungen zu suchen. [Weitere Informationen](../email/surface-personalization.md#check-configuration)

**Code-basierter Kanal**

* Inhaltsvorlagen sind nun verfügbar. Sie können das Authoring Ihrer Code-basierten Erlebnisse beschleunigen, ausgehend von einer Inhaltsvorlage, die von Ihren Entwickelnden erstellt wurde. Durch Verwendung einer Inhaltsvorlage kann der Marketing-Experte nur einige Werte oder Felder ändern, anstatt die gesamte HTML- oder JSON-Inhalts-Payload zusammenzustellen. [Weitere Informationen](../content-management/content-templates.md)

**Entscheidungsfindung**

* Benutzende von [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=de) können nun bei der Einrichtung eines KI-Modells in der Entscheidungsfindung (zuvor Erlebnis-Entscheidung) benutzerdefinierte Modelle für die Optimierung auswählen. So können Sie beispielsweise eine benutzerdefinierte &quot;Einkaufstabelle&quot;optimieren, anstatt definierte Begrenzungen wie die Clickthrough-Rate festzulegen. [Weitere Informationen](../experience-decisioning/ranking.md)

* Beim Hinzufügen einer Entscheidungsrichtlinie zu einer code-basierten Kampagne mit Entscheidungsfindung können Sie jetzt zusätzlich zu den Auswahlstrategien manuell einzelne Entscheidungselemente auswählen. Darüber hinaus können Sie jetzt mehr als ein Fallback-Angebot auswählen. Dadurch wird sichergestellt, dass eine bestimmte Anzahl von Entscheidungselementen zurückgegeben wird. [Weitere Informationen](../experience-decisioning/create-decision.md)
