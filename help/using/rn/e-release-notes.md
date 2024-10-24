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
source-git-commit: f715fb9135c446d569a4384ce73e9e92c72cb9ff
workflow-type: tm+mt
source-wordcount: '1897'
ht-degree: 42%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

**Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise Oktober 2024 {#e-2024}

**Veröffentlichungsdatum**: 29.-30. Oktober 2024

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
<th><strong>Genehmigungen in Journey und Kampagnen (Allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Genehmigungsrichtlinien können Sie nun einen Genehmigungsprozess in Journey Optimizer einrichten, mit dem Marketing-Teams sicherstellen können, dass Kampagnen und Journeys vor ihrer Live-Schaltung von den jeweiligen Stakeholdern geprüft und abgezeichnet werden.</p>
<p>Bisher für eine Reihe von Organisationen (LA) verfügbar, sind nun Genehmigungsrichtlinien für alle Benutzer verfügbar (GA).</p>
<p>Weitere Informationen finden Sie in der <a href="../test-approve/gs-approval.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Personalisierung der E-Mail-Konfiguration (Allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt beim Erstellen von E-Mail-Kanal-Konfigurationen dynamische Subdomains und personalisierte Kopfzeilenparameter definieren, um mehr Flexibilität und Kontrolle über Ihre E-Mail-Einstellungen zu erhalten.</p><p>Durch die Verwendung einer personalisierten Konfiguration in einer Kampagne oder einer Journey können Sie eine Vorschau Ihres E-Mail-Inhalts anzeigen, um nach potenziellen Fehlern mit den von Ihnen definierten dynamischen Einstellungen zu suchen.</p>
<p>Zuvor für eine Reihe von Organisationen (LA) verfügbar, ist jetzt die Personalisierung der E-Mail-Konfiguration für alle Benutzer verfügbar (GA).</p>
<p>Weitere Informationen finden Sie in der <a href="../email/surface-personalization.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Konfliktmanagement und Prioritätensetzung (begrenzte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer ist es wichtig, das Volumen und den Zeitpunkt von Kampagnen und Journeys zu verwalten, um zu vermeiden, dass Kunden mit zu vielen Interaktionen überfordert werden. Journey Optimizer bietet jetzt mehrere Instrumente für Konfliktbewältigung und Priorisierung.</p><p><ul><li><b>Journey-Frequenzlimitierung</b>: Sie können jetzt Regelsätze erstellen, die auf Ihre Journey angewendet werden, sodass Sie die Anzahl der Journey pro Tag, Woche oder Monat begrenzen und die Anzahl der gleichzeitig ausgeführten Journey steuern können.</li>
<li><b>Prioritätsbewertung</b>: Sie können einer Kampagne oder einer Journey jetzt eine Prioritätsbewertung im Bereich von 0 bis 100 zuweisen. Eine höhere Zahl bedeutet eine höhere Priorität. Wenn zwei Kampagnen oder Journey-Aktionen dieselbe Kanalkonfiguration verwenden, wählt Journey Optimizer die Kampagne mit der höchsten Prioritätsbewertung aus. Wenn die Kampagnen dasselbe Ergebnis aufweisen, wird die Kampagne ausgewählt, die zuletzt geändert wurde.</li>
<li><b>Potenzielle Konflikte anzeigen</b>: Mit der neuen Schaltfläche "Potenzielle Konflikte anzeigen"in Journey und Kampagnen können Sie jetzt Überschneidungen mit anderen Journey oder Kampagnen identifizieren, z. B. mit dem Startdatum, der Zielgruppe oder der ausgewählten Kanalkonfiguration.</li>
<li><b>Journey Arbitration</b>: Mit dieser neuen Funktion können Sie die wichtigsten Journey für Ihre Kunden priorisieren. Sie können eine Regel erstellen, um die Einsendung in eine Journey mit niedrigerer Priorität zu unterdrücken, wenn ein Kunde für eine bevorstehende Journey mit höherer Priorität qualifiziert ist.</li></ul></p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
<p>Funktionen zur Verwaltung von Konflikten und Prioritäten sind in der eingeschränkten Verfügbarkeit für eine ausgewählte Gruppe von Kunden verfügbar. Bitte beachten Sie, dass diese Funktionen künftig schrittweise für weitere Benutzer eingeführt werden. Wenden Sie sich an Ihr Account-Team, wenn Sie Interesse haben, auf diese Funktionen gesetzt zu werden.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Nicht visueller Bearbeitungsmodus für den Webdesigner</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Als Alternative zum Journey Optimizer-Webdesigner können Sie jetzt Änderungen an Ihrer Website mit einem nicht visuellen Editor hinzufügen. Sie können Ihre Änderungen manuell eingeben, ohne die Seiten im Visual Editor zu öffnen.
Dieser nicht visuelle Bearbeitungsmodus ist nützlich, wenn Sie keine Browsererweiterungen wie Adobe Experience Cloud Visual Helper installieren können, die zum Laden Ihrer Seiten in den Webdesigner erforderlich sind.</p>
<!--p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentieren in Journey (Allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ist bereits in Kampagnen verfügbar und unterstützt jetzt Experimente in Journeys. Bei Experimenten handelt es sich um randomisierte Test, was im Rahmen von Online-Tests bedeutet, dass Sie einigen zufällig ausgewählten Benutzenden eine bestimmte Variante einer Nachricht anbieten und einer anderen zufällig ausgewählten Gruppe von Benutzenden eine andere Variante oder Abwandlung anbieten. Nach dem Angebot können Sie die Ihre gewünschten Ergebnismetriken messen, z. B. Öffnung von E-Mails, Abonnements oder Käufe.</p>
<p>Bisher für eine Reihe von Organisationen (LA) verfügbar, sind nun Experimente in Journey verfügbar (GA).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Entscheidungsfindung (Allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Entscheidungsfindung, die zuvor für eine Reihe von Organisationen (LA) verfügbar war und als Experience Decisioning bezeichnet wurde, steht nun allen Benutzern zur Verfügung (GA). Sie vereinfacht die Personalisierung, indem sie einen zentralisierten Katalog von Marketing-Angeboten anbietet, der als "Entscheidungselemente"bezeichnet wird, und eine ausgereifte Entscheidungs-Engine. Diese Engine nutzt Regeln und Ranking-Kriterien, um die relevantesten Entscheidungselemente für jede Person auszuwählen und darzustellen. Diese Entscheidungselemente sind über den code-basierten Erlebniskanal nahtlos in eine breite Palette von eingehenden Oberflächen integriert.</p>

<p>Vorerst ist Decisioning nicht für Kunden verfügbar, die das Zusatzangebot Adobe Healthcare Shield und Privacy and Security Shield erworben haben.</p>

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
<p>Sie können jetzt Regeln für eine detaillierte Frequenzbegrenzung erstellen und diese über Regelsätze auf Ihre Nachrichten oder Journey anwenden. Mit dieser neuen Funktion können Sie steuern, wie oft Ihre Zielgruppen eine Nachricht erhalten, indem Sie kanalübergreifende Regeln festlegen, mit denen Profile, die zu oft angesprochen wurden, automatisch aus Nachrichten und Aktionen ausgeschlossen werden.</p><p>Außerdem können Sie die Anzahl der Journey pro Tag, Woche oder Monat begrenzen sowie die Anzahl der gleichzeitig ausgeführten Journey steuern.</p>
<p>Regelsätze sind in eingeschränkter Verfügbarkeit für eine ausgewählte Gruppe von Kunden verfügbar. Bitte beachten Sie, dass diese Funktionen künftig schrittweise für weitere Benutzer eingeführt werden. Wenden Sie sich an Ihr Account-Team, wenn Sie Interesse haben, auf die Warteliste für diese Funktion gesetzt zu werden.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Mehrsprachige Nachrichten in Journey und Kampagnen (Allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt im Rahmen einer Kampagne oder Journey mühelos Inhalte in mehreren Sprachen erstellen.  Mit dieser Funktion können Sie bei der Bearbeitung Ihrer Kampagne oder Journey zwischen Sprachen wechseln, den gesamten Bearbeitungsvorgang optimieren und Ihre mehrsprachigen Inhalte effizienter verwalten.</p>
<p>Bisher für eine Reihe von Organisationen verfügbar (LA), sind jetzt mehrsprachige Nachrichten für alle Benutzer verfügbar (GA).</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

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
<li>Beschleunigen Sie Workflows für Journey Optimizer-Kunden, die Da Vinci für die Bearbeitung und AJO für die Optimierung und Bereitstellung verwenden.</li>
<li>Optimieren Sie Da Vinci-Modelle mit Adobe-Daten.</li></ul></p>
<!--p>For more information, refer to the <a href="../code-based/get-started-code-based.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aktualisiertes Berichtserlebnis (Allgemeine Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verfügbar seit dem 16. Oktober 2024</p>
<p>Journey Optimizer Reporting ist jetzt allgemein verfügbar (GA) und verfügt über eine verbesserte Interoperabilität mit Customer Journey Analytics-Funktionen, Standardisierung der Berichterstellung auf beiden Plattformen und Verbesserung der Datenkonsistenz und -zuverlässigkeit. Diese nahtlose Integration zwischen Journey Optimizer und Customer Journey Analytics bietet einen klareren Überblick über Leistungsmetriken und ermöglicht es Benutzenden, besser fundierte Entscheidungen zu treffen.</p>
<p>Mit der allgemeinen Verfügbarkeit werden vier neue Funktionen eingeführt: die Möglichkeit, einfache Metriken zu erstellen, Zielgruppen zu erstellen und zu veröffentlichen, Ad-hoc-Fragen mit Insight Builder zu stellen und Berichte so zu planen, dass sie automatisch per E-Mail an wichtige Empfänger gesendet werden.</p>
<p>Weitere Informationen finden Sie in der <a href="../reports/report-cja-manage.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Wichtig: Die aktuelle Berichtserfahrung wird ab Januar 2025 eingestellt. Nach diesem Datum wird das neue Reporting-Erlebnis zum Standard. Wir empfehlen, sich mit den neuen Funktionen und Funktionalitäten vertraut zu machen, um einen reibungslosen Übergang zu gewährleisten. <a href="../reports/report-gs-cja.md">Informationen zu den ersten Schritten mit der neuen Reporting-Oberfläche von Journey Optimizer</a></p>
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

SMS-Verbesserungen wurden eingeführt, um Ihre Nachrichtenfunktionen zu verbessern:

* Sie können eindeutige Suchbegriffe für Ihre SMS-Kampagnen und Journey definieren und verwalten, um eine personalisiertere und effizientere Kommunikation zu ermöglichen.
* Sie können eine Standard-SMS-Nachricht erstellen und versenden, wenn ein Schlüsselwort nicht erkannt wird.

**Journeys**

* **Pfadexperiment in Journey** - Mit dem Journey-Pfadexperiment können Sie jetzt Schlüsselmetriken für Ihre Journey-Pfade definieren und verfolgen, sodass Sie die Wirkung Ihrer Aktivitäten messen und genauere Einblicke in Ihre Leistung erhalten.

* **Maximale Anzahl von Live-Journeys**: In Journey Optimizer gibt es nun ein Limit von 500 Live-Journeys bei Produktions-Sandboxes. Zuvor waren es 100. Die Anzahl der Live-Journey ist auf der Journey-Arbeitsfläche sichtbar. <!-- DOCAC-10977-->

* **Schutzdauer für die Live-Schaltung** - Ab dem 1. November 2024 wird in Journey Optimizer-systemgenerierten Datensätzen in neuen Sandboxes und neuen Organisationen ein TTL-Schutzschild (Time-to-Live) bereitgestellt:

   * 90 Tage für Daten im Profilspeicher
   * 13 Monate für Daten im Data Lake

  Diese Änderung wird in einer zweiten Phase in bestehenden Kunden-Sandboxes eingeführt.

  Außerdem unterstützt Streaming-Segmentierung ab dem 1. November die Verwendung von Sende- und Öffnungs-Ereignissen aus Tracking- und Feedback-Datensätzen nicht mehr. Diese Änderung gilt für alle Kunden-Sandboxes und -Organisationen zu diesem Zeitpunkt. [Weitere Informationen](../data/datasets-ttl.md)

* **Parameter in benutzerdefinierten Aktionen** (Verfügbarkeitsdatum: 3. Oktober 2024) - NULL und optionale Parameter werden jetzt in benutzerdefinierten Aktionen unterstützt. [Weitere Informationen](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Reporting**

* **Berichte zu Erlebnisentscheidungen** ist jetzt verfügbar und bietet wichtige Einblicke in die Interaktion Ihrer Besucher mit Ihren Erlebnissen.

**Richtlinien für Data Governance und Einverständnis** – Verfügbarkeitsdatum: 7. Oktober 2024

* Die Durchsetzung der **Data Governance-Richtlinien** erfolgt jetzt über alle Kanäle in Journey Optimizer. Für Kundinnen und Kunden, die Richtlinien in Adobe Experience Platform erstellt haben, werden diese im Rahmen der Einrichtung der Kanalkonfigurationen auf Marketing-Aktionen angewendet. Wenn Sie Inhalte mithilfe einer Konfiguration erstellen, prüft das System alle Personalisierungsfelder auf Verstöße gegen die Data Governance. Wenn ein Verstoß festgestellt wird, ist die Veröffentlichung einer Journey oder Kampagne nicht möglich. [Weitere Informationen](../action/action-privacy.md)

* **Benutzerdefinierte Einverständnisrichtlinien** gelten jetzt für alle Journey Optimizer-Kanäle. Bei der Durchsetzung vor dem Versand einer Nachricht oder der Zustellung eines eingehenden Erlebnisses prüft das System, ob die Benutzerin oder der Benutzer die Zustimmung zur Verwendung von Personalisierungsfeldern in den Inhalten erteilt hat, die erhalten werden. Wenn kein Einverständnis erteilt wird, wird das Erlebnis nicht angezeigt. [Weitere Informationen](../action/consent.md)

  >[!NOTE]
  >
  >Einverständnisrichtlinien sind derzeit nur für Organisationen verfügbar, die die Zusatzangebote Adobe **Healthcare Shield** und **Privacy and Security Shield** erworben haben.

**Zielgruppen** – Verfügbarkeitsdatum: 8. Oktober 2024

* Beim Targeting einer CSV-Datei-Zielgruppe können Sie jetzt Attribute aus der Datei im Personalisierungseditor und im Regel-Builder für Journeys und Kampagnen verwenden. [Weitere Informationen](../audience/about-audiences.md)

* Zielgruppen und Attribute aus benutzerdefinierten Uploads (CSV-Dateien) stehen jetzt zur Verwendung mit Healthcare Shield oder Privacy and Security Shield zur Verfügung.

**Codebasierter Kanal**

* Inhaltsvorlagen sind jetzt verfügbar. Sie können das Authoring Ihrer code-basierten Erlebnisse beschleunigen, ausgehend von einer Inhaltsvorlage, die von Ihren Entwicklern erstellt wurde. Durch Verwendung einer Inhaltsvorlage kann der Marketing-Experte nur einige Werte oder Felder ändern, anstatt die gesamte HTML- oder JSON-Inhalts-Payload zusammenzustellen.



