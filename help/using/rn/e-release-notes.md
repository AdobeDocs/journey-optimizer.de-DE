---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Frühzeitige Versionshinweise zu Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 61447b6400b65e29a9187790e74be47b09764c4a
workflow-type: tm+mt
source-wordcount: '1967'
ht-degree: 100%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

**Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise Oktober 2024 {#e-2024}

**Veröffentlichungsdatum**: 29.–30. Oktober 2024

### Neue Funktionen {#e-features}

Mit dieser Version werden die unten aufgeführten neue Funktionen eingeführt.

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
<!--p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/-->
</td>
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
<p>Genehmigungsrichtlinien, die zuvor nur für eine Reihe von Organisationen verfügbar gewesen sind (LA), stehen jetzt allen Benutzenden zur Verfügung (GA).</p>
<p>Weitere Informationen finden Sie in der <a href="../test-approve/gs-approval.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Personalisierung der E-Mail-Konfiguration (allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt beim Erstellen von E-Mail-Kanal-Konfigurationen dynamische Subdomains und personalisierte Kopfzeilenparameter definieren, um mehr Flexibilität und Kontrolle über Ihre E-Mail-Einstellungen zu erhalten.</p><p>Durch eine personalisierte Konfiguration in einer Kampagne oder Journey können Sie eine Vorschau Ihrer E-Mail-Inhalte anzeigen, um nach potenziellen Fehlern mit den von Ihnen definierten dynamischen Einstellungen zu suchen.</p>
<p>Die Personalisierung der E-Mail-Konfiguration, die zuvor nur für eine Reihe von Organisationen verfügbar gewesen ist (LA), steht jetzt allen Benutzenden zur Verfügung (GA).</p>
<p>Weitere Informationen finden Sie in der <a href="../email/surface-personalization.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Testen von Inhalten mit Beispieleingabedaten (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Journey Optimizer können Sie nun verschiedene Varianten Ihrer E-Mail-Inhalte testen, indem Sie in einer Vorschau anzeigen und Testsendungen mit Beispieleingabedaten senden, die aus einer CSV-Datei hochgeladen oder manuell hinzugefügt wurden. Alle Profilattribute, die in Ihren Inhalten für die Personalisierung verwendet werden, werden automatisch vom System erkannt und können für Ihre Tests zur Erstellung mehrerer Varianten verwendet werden.</p>
<p>Diese Funktion ist aktuell als Betaversion verfügbar.</p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
</td>
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
<p>In Journey Optimizer ist es wichtig, das Volumen und den Zeitpunkt von Kampagnen und Journeys zu steuern, um zu vermeiden, dass Kundinnen und Kunden mit zu vielen Interaktionen überfordert werden. Journey Optimizer bietet nun mehrere Tools zum Konflikt-Management und zur Priorisierung.</p><p><ul><li><b>Journey-Frequenzbegrenzung</b>: Sie können nun Regelsätze erstellen, die auf Ihre Journey angewendet werden, sodass Sie die Anzahl der Journeys für ein Profil pro Tag, Woche oder Monat begrenzen und die Anzahl gleichzeitig ausgeführter Journeys kontrollieren können.</li>
<li><b>Prioritätswert</b>: Sie können einer Kampagne oder Journey nun einen Prioritätswert zwischen 0 und 100 zuweisen. Eine höhere Zahl bedeutet eine höhere Priorität. Wenn zwei Kampagnen oder Journeys dieselbe Kanalkonfiguration verwenden, wählt Journey Optimizer die Kampagne oder Journey mit dem höchsten Prioritätswert aus. Wenn die Kampagnen den gleichen Wert aufweisen, wird die Kampagne ausgewählt, die zuletzt geändert wurde.</li>
<li><b>Potenzielle Konflikte anzeigen</b>: Mit der neuen Schaltfläche „Potenzielle Konflikte anzeigen“ in Journeys und Kampagnen können Sie nun Überschneidungen mit anderen Journeys oder Kampagnen identifizieren, z. B. beim Startdatum, bei der Zielgruppe oder bei der ausgewählten Kanalkonfiguration.</li>
<li><b>Journey Arbitration</b>: Mit dieser neuen Funktion können Sie die wichtigsten Journeys für Ihre Kundschaft priorisieren. Sie können eine Regel erstellen, um den Eintritt in eine Journey mit niedrigerer Priorität zu unterdrücken, wenn eine Kundin oder ein Kunde für eine bevorstehende Journey mit höherer Priorität qualifiziert ist.</li></ul></p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
<p>Die Funktionen zum Konflikt- und Prioritäten-Management sind für eine ausgewählte Gruppe von Kundinnen und Kunden verfügbar (eingeschränkte Verfügbarkeit). Sie werden in Zukunft schrittweise für weitere Benutzende eingeführt. Wenden Sie sich an Ihr Accountteam, wenn Sie auf die Warteliste für diese Funktionen gesetzt werden möchten.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Nicht visueller Bearbeitungsmodus für den Web-Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Als Alternative zum Web-Designer von Journey Optimizer können Sie nun Änderungen an Ihrer Website mit einem nicht visuellen Editor hinzufügen. Sie können Ihre Änderungen manuell eingeben, ohne die Seiten im visuellen Editor zu öffnen.
Dieser nicht visuelle Bearbeitungsmodus ist nützlich, wenn Sie keine Browser-Erweiterungen wie Adobe Experience Cloud Visual Helper installieren können, die zum Laden Ihrer Seiten in den Web-Designer erforderlich sind.</p>
<!--p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p-->
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
<p>Experimente in Journeys, die zuvor nur für eine Reihe von Organisationen verfügbar gewesen sind (LA), stehen jetzt allen Benutzenden zur Verfügung (GA).</p>
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
<p>Die Entscheidungsfindung, die zuvor nur für eine Reihe von Organisationen verfügbar gewesen ist (LA) und als Erlebnis-Entscheidung bezeichnet wurde, steht jetzt allen Benutzenden zur Verfügung (GA). Sie vereinfacht die Personalisierung, indem sie einen zentralen Katalog von Marketing-Angeboten, die als „Entscheidungselemente“ bezeichnet werden, und eine ausgereifte Entscheidungs-Engine anbietet. Diese Engine nutzt Regeln und Rangfolgekriterien, um die relevantesten Entscheidungselemente für jeden Kontakt auszuwählen und darzustellen. Diese Entscheidungselemente sind über den Code-basierten Erlebniskanal nahtlos in eine breite Palette eingehender Oberflächen integriert. </p>

<p>Für Kundinnen und Kunden, die die Zusatzangebote Adobe Healthcare Shield und Privacy and Security Shield erworben haben, ist die Entscheidungsfindung derzeit nicht verfügbar.</p>

<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Regelsätze (eingeschränkte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Regeln für eine genauere Frequenzbegrenzung erstellen und diese über Regelsätze auf Ihre Nachrichten oder Journeys anwenden. Diese neue Funktion ermöglicht es Ihnen, zu kontrollieren, wie oft Ihre Zielgruppen eine Nachricht erhalten, indem Sie kanalübergreifende Regeln festlegen, um zu oft angesprochene Profile automatisch aus Nachrichten und Aktionen auszuschließen.</p><p>Außerdem können Sie die Anzahl der Journeys pro Tag, Woche oder Monat begrenzen und die Anzahl gleichzeitig ausgeführter Journeys kontrollieren.</p>
<p>Regelsätze sind für eine ausgewählte Gruppe von Kundinnen und Kunden verfügbar (eingeschränkte Verfügbarkeit). Sie werden in Zukunft schrittweise für weitere Benutzende eingeführt. Wenden Sie sich an Ihr Accountteam, wenn Sie auf die Warteliste für diese Funktion gesetzt werden möchten.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
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
<p>Mit der allgemeinen Verfügbarkeit sind jetzt mehrsprachige Inhalte über alle Kanäle hinweg verfügbar. </p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
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
<li>Beschleunigen praktischer Workflows für Journey Optimizer-Kundschaft, die Da Vinci zum Authoring und AJO zur Optimierung und Versand verwendet</li>
<li>Optimieren von Da Vinci-Modellen mit Adobe-Daten</li></ul></p>
<!--p>For more information, refer to the <a href="../code-based/get-started-code-based.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aktualisiertes Reporting-Erlebnis (allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verfügbar seit dem 16. Oktober 2024</p>
<p>Das Journey Optimizer-Reporting ist nun allgemein verfügbar und bietet eine verbesserte Kompatibilität mit Customer Journey Analytics-Funktionen, wodurch die Berichterstellung plattformübergreifend standardisiert und die Datenkonsistenz und -zuverlässigkeit optimiert wird. Diese nahtlose Integration zwischen Journey Optimizer und Customer Journey Analytics bietet einen klareren Überblick über Leistungsmetriken und ermöglicht es Benutzenden, fundiertere Entscheidungen zu treffen.</p>
<p>Mit der allgemeinen Verfügbarkeit werden vier neue Funktionen eingeführt, die es ermöglichen, einfache Metriken zu erstellen, Zielgruppen zu erstellen und zu veröffentlichen, Ad-hoc-Fragen mit Insight Builder zu stellen und Berichte so zu planen, dass sie automatisch per E-Mail an wichtige Empfängerinnen und Empfänger gesendet werden.</p>
<p>Weitere Informationen finden Sie in der <a href="../reports/report-cja-manage.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Wichtig: Das aktuelle Reporting-Erlebnis wird im Januar 2025 eingestellt. Nach diesem Datum wird das neue Reporting-Erlebnis zum Standard. Wir empfehlen, sich mit den neuen Funktionen und Funktionalitäten vertraut zu machen, um einen reibungslosen Übergang zu gewährleisten. <a href="../reports/report-gs-cja.md">Informationen zu den ersten Schritten mit der neuen Reporting-Oberfläche von Journey Optimizer</a></p>
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
<p>Verfügbar seit dem 1. Oktober 2024</p>
<p>Mit dem Code-basierten Erlebniskanal ermöglicht Ihnen Adobe Journey Optimizer eine erweiterte Personalisierung und Tests für jede Ihrer eingehenden Eigenschaften durchzuführen. Dies ermöglicht den nahtlosen Versand von maßgeschneiderten Erlebnissen über verschiedene Touchpoints wie Web-Apps, Mobile-Apps, Desktop-Apps, Videokonsolen, mit dem Fernseher verbundene Geräte, Smart-TVs, Kioske, Geldautomaten, IoT-Geräte und mehr. Der Code-basierte Erlebniskanal ist jetzt auf der Journey-Arbeitsfläche verfügbar.</p>
<p>Weitere Informationen finden Sie in der <a href="../code-based/create-code-based.md">ausführlichen Dokumentation</a>.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
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
<p>Verfügbar seit dem 1. Oktober 2024</p>
<p>Mit dem Webkanal ermöglicht Ihnen Adobe Journey Optimizer das Web-Erlebnis zu personalisieren, das Sie Ihren Kundinnen und Kunden über eingehende Web-Journeys bereitstellen. Der Web-Kanal ist jetzt auf der Journey-Arbeitsfläche verfügbar.</p>
<p>Weitere Informationen finden Sie in der <a href="../web/create-web.md">ausführlichen Dokumentation</a>.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
</tr>
</tbody>
</table>

### Verbesserungen {#e-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**SMS-Kanal**

>[!AVAILABILITY]
>
>Folgende Verbesserungen sind nur bei Sinch- und Infobip-Anbietern verfügbar.

SMS-Verbesserungen wurden eingeführt, um Ihre Messaging-Funktionen zu verbessern:

* Sie können eindeutige Keywords für Ihre SMS-Kampagnen und Journeys definieren und verwalten, um eine personalisiertere und effizientere Kommunikation zu ermöglichen.

* Sie können eine standardmäßige SMS-Nachricht erstellen und senden, wenn ein Keyword nicht erkannt wird.

* Sie können nun eine SMS-API-Kanalkonfiguration bearbeiten oder löschen.

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

<!--* **Max number of Live journeys** - Journey Optimizer now has a guardrail of 500 live journeys on production sandboxes, instead of 100. The number of live journeys is visible in the journey canvas. (DOCAC-10977) -->

**Datensätze**

* **Time-to-Live-Limit**: Ab 1. November 2024 wird in neuen Sandboxes und neuen Organisationen für systemgenerierte Journey Optimizer-Datensätze das folgende Time-to-Live(TTL)-Limit eingeführt:

   * 90 Tage für Daten im Profilspeicher
   * 13 Monate für Daten im Data Lake

  Diese Änderung wird anschließend in einer zweiten Phase in bestehende Kunden-Sandboxes integriert.

  Außerdem unterstützt die Streaming-Segmentierung ab dem 1. November die Verwendung von Sende- und Öffnungsereignissen aus Tracking- und Feedback-Datensätzen nicht mehr. Diese Änderung gilt zu diesem Zeitpunkt für alle Kunden-Sandboxes und Organisationen. [Weitere Informationen](../data/datasets-ttl.md)

* **Parameter in benutzerdefinierten Aktionen** (Verfügbarkeitsdatum: 3. Oktober 2024): NULL und optionale Parameter werden nun in benutzerdefinierten Aktionen unterstützt. [Weitere Informationen](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Reporting**

* **Reporting für die Entscheidungsfindung** ist nun verfügbar und bietet wichtige Erkenntnisse zur Besucherinteraktion mit Ihren Erlebnissen.

**Richtlinien für Data Governance und Einverständnis** – Verfügbarkeitsdatum: 7. Oktober 2024

* Die Durchsetzung der **Data Governance-Richtlinien** erfolgt jetzt über alle Kanäle in Journey Optimizer. Für Kundinnen und Kunden, die Richtlinien in Adobe Experience Platform erstellt haben, werden diese im Rahmen der Einrichtung der Kanalkonfigurationen auf Marketing-Aktionen angewendet. Wenn Sie Inhalte mithilfe einer Konfiguration erstellen, prüft das System alle Personalisierungsfelder auf Verstöße gegen die Data Governance. Wenn ein Verstoß festgestellt wird, ist die Veröffentlichung einer Journey oder Kampagne nicht möglich. [Weitere Informationen](../action/action-privacy.md)

* **Benutzerdefinierte Einverständnisrichtlinien** gelten jetzt für alle Journey Optimizer-Kanäle. Bei der Durchsetzung vor dem Versand einer Nachricht oder der Zustellung eines eingehenden Erlebnisses prüft das System, ob die Benutzerin oder der Benutzer die Zustimmung zur Verwendung von Personalisierungsfeldern in den Inhalten erteilt hat, die erhalten werden. Wenn kein Einverständnis erteilt wird, wird das Erlebnis nicht angezeigt. [Weitere Informationen](../action/consent.md)

  >[!NOTE]
  >
  >Einverständnisrichtlinien sind derzeit nur für Organisationen verfügbar, die die Zusatzangebote Adobe **Healthcare Shield** und **Privacy and Security Shield** erworben haben.

**Zielgruppen** – Verfügbarkeitsdatum: 8. Oktober 2024

* Beim Targeting einer CSV-Datei-Zielgruppe können Sie jetzt Attribute aus der Datei im Personalisierungseditor und im Regel-Builder für Journeys und Kampagnen verwenden. [Weitere Informationen](../audience/about-audiences.md)

* Zielgruppen und Attribute aus benutzerdefinierten Uploads (CSV-Dateien) stehen jetzt zur Verwendung mit Healthcare Shield oder Privacy and Security Shield zur Verfügung.

**Code-basierter Kanal**

* Inhaltsvorlagen sind nun verfügbar. Sie können das Authoring Ihrer Code-basierten Erlebnisse beschleunigen, ausgehend von einer Inhaltsvorlage, die von Ihren Entwickelnden erstellt wurde. Durch Verwendung einer Inhaltsvorlage können Marketing-Fachleute nur einige Werte oder Felder ändern, anstatt die gesamte HTML- oder JSON-Inhalts-Payload zusammenzustellen.

**Entscheidungsfindung**

Benutzende von [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=de) können nun bei der Einrichtung eines KI-Modells in der Entscheidungsfindung (zuvor Erlebnis-Entscheidung) benutzerdefinierte Modelle für die Optimierung auswählen. So können Sie z. B. anhand einer benutzerdefinierten „Einkaufstabelle“ und nicht auf Grundlage definierter Einschränkungen wie der Clickthrough-Rate optimieren.
