---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: c54ad4cddeb7115f9a069102c67c41f0850a11ed
workflow-type: tm+mt
source-wordcount: '1601'
ht-degree: 89%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in diesen Versionshinweisen in der letzten Woche jedes Monats konsolidiert. [!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Aktualisierungen im Oktober 2024 {#24-10-rn}

Bevorstehende **Veröffentlichungsdatum**: 28.-30. Oktober 2024

Die unten aufgeführten [Funktionen](#24-10-features) und [Verbesserungen](#24-10-improvements) wurden diesen Monat veröffentlicht.

### Neue Funktionen {#24-10-features}

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
<p>Verfügbarkeitsdatum: 16. Oktober 2024</p>
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
<p>Verfügbarkeitsdatum: 1. Oktober 2024</p>
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
<p>Verfügbarkeitsdatum: 1. Oktober 2024</p>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>Die aktuelle Berichtserfahrung wird ab Januar 2025 eingestellt. Nach diesem Datum wird das neue Reporting-Erlebnis zum Standard. Wir empfehlen, sich mit den neuen Funktionen und Funktionalitäten vertraut zu machen, um einen reibungslosen Übergang zu gewährleisten.
>
> [Informationen zu den ersten Schritten mit der neuen Reporting-Oberfläche von Journey Optimizer](../reports/report-gs-cja.md)

### Verbesserungen {#24-10-improvements}

**Journeys** – Verfügbarkeitsdatum: 3. Oktober 2024

* **Parameter in benutzerdefinierten Aktionen**: NULL und optionale Parameter werden nun in benutzerdefinierten Aktionen unterstützt. [Weitere Informationen](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Richtlinien für Data Governance und Einverständnis** – Verfügbarkeitsdatum: 7. Oktober 2024

* Die Durchsetzung der **Data Governance-Richtlinien** erfolgt jetzt über alle Kanäle in Journey Optimizer. Für Kundinnen und Kunden, die Richtlinien in Adobe Experience Platform erstellt haben, werden diese im Rahmen der Einrichtung der Kanalkonfigurationen auf Marketing-Aktionen angewendet. Wenn Sie Inhalte mithilfe einer Konfiguration erstellen, prüft das System alle Personalisierungsfelder auf Verstöße gegen die Data Governance. Wenn ein Verstoß festgestellt wird, ist die Veröffentlichung einer Journey oder Kampagne nicht möglich. [Weitere Informationen](../action/action-privacy.md)

* **Benutzerdefinierte Einverständnisrichtlinien** gelten jetzt für alle Journey Optimizer-Kanäle. Bei der Durchsetzung vor dem Versand einer Nachricht oder der Zustellung eines eingehenden Erlebnisses prüft das System, ob die Benutzerin oder der Benutzer die Zustimmung zur Verwendung von Personalisierungsfeldern in den Inhalten erteilt hat, die erhalten werden. Wenn kein Einverständnis erteilt wird, wird das Erlebnis nicht angezeigt. [Weitere Informationen](../action/consent.md)

  >[!NOTE]
  >
  >Einverständnisrichtlinien sind derzeit nur für Organisationen verfügbar, die die Zusatzangebote Adobe **Healthcare Shield** und **Privacy and Security Shield** erworben haben.

**Zielgruppen** – Verfügbarkeitsdatum: 8. Oktober 2024

* Beim Targeting einer CSV-Datei-Zielgruppe können Sie jetzt Attribute aus der Datei im Personalisierungseditor und im Regel-Builder für Journeys und Kampagnen verwenden. [Weitere Informationen](../audience/about-audiences.md)

* Zielgruppen und Attribute aus benutzerdefinierten Uploads (CSV-Dateien) stehen jetzt zur Verwendung mit Healthcare Shield oder Privacy and Security Shield zur Verfügung.

## Version September 2024 {#24-9-rn}

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

**Veröffentlichungsdatum**: 24.–26. September 2024

### Neue Funktionen {#24-9-features}

Mit dieser Version werden die unten aufgeführten neue Funktionen eingeführt.

<table>
<thead>
<tr>
<th><strong>Inhaltskarten für mobile Apps und Websites</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Inhaltskarten sind eine neue Funktion für digitale Nachrichten in Adobe Journey Optimizer, die personalisierte und ansprechende Inhalte direkt in mobilen Apps und Websites bereitstellt. Im Gegensatz zu herkömmlichen Push-Benachrichtigungen integrieren sich Inhaltskarten nahtlos in die Benutzeroberfläche und bieten dauerhafte, nicht störende Aktualisierungen, die die Benutzerinteraktion und das Benutzererlebnis verbessern.</p>
<p>Diese Funktion ermöglicht es Marketing-Fachleuten, Benutzenden relevante Rich-Media-Inhalte präsentieren zu können, wodurch die Interaktion gesteigert und wichtige Nachrichten ohne Unterbrechung der Benutzer-Journey angezeigt werden.</p>
<p>Weitere Informationen finden Sie in der <a href="../content-card/get-started-content-card.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/content-card.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Genehmigungen in Journeys und Kampagnen (LA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Genehmigungsrichtlinien können Sie nun einen Genehmigungsprozess in Journey Optimizer einrichten, mit dem Marketing-Teams sicherstellen können, dass Kampagnen und Journeys vor ihrer Live-Schaltung von den jeweiligen Stakeholdern geprüft und abgezeichnet werden.</p>
<p>Genehmigungsrichtlinien sind derzeit nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p>Weitere Informationen finden Sie in der <a href="../test-approve/gs-approval.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Email Content Locking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer now allows you to lock content in email templates, either by locking the entire template or specific structures and component. This allows you to prevent unintentional edits or deletions, giving you greater control over template customization, and improving the efficiency and reliability of your email campaigns.</p>
<p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Globale Ausstiegskriterien in Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Es ist nun möglich, Ausstiegskriterien auf Journey-Ebene zu definieren. Durch Hinzufügen von Ausstiegskriterien sorgen Sie dafür, dass Profile die Journey verlassen, sobald ein Ereignis eintritt (z. B. ein Kauf) oder sie sich für eine Zielgruppe qualifizieren. Dadurch wird verhindert, dass Benutzende weitere Nachrichten von der Journey erhalten.</p>
<p>Weitere Informationen finden Sie in der <a href="../building-journeys/journey-properties.md#exit-criteria">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>KI-Assistent – Content Accelerator </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nachdem Sie Ihre Nachricht erstellt und personalisiert haben, stellen Sie mit dem AI Assistant Content Accelerator in Journey Optimizer Ihren Inhalt auf die nächste Stufe. Sie können jetzt den KI-Assistenten verwenden, um die Wirkung Ihrer Nachricht zu optimieren, indem Sie mit verschiedenen Haupttiteln und Bildern experimentieren. Jede Variante wird als eindeutige Abwandlung verwaltet, um zu messen und zu vergleichen, welcher Titel effektiv mehr Klicks generiert.</p>
<p>Machen Sie sich mit <a href="https://experienceleague.adobe.com/de/apps/journey-optimizer/ai-assistant-content-accelerator">unserer Live-Funktionsvorschau</a> auf praktische Weise vertraut, die Ihnen die Möglichkeit gibt, die Funktionen selbst zu entdecken und die entsprechenden Fähigkeiten vollständig zu verstehen.</a></p>
<p>Weitere Informationen finden Sie in der <a href="../content-management/gs-generative.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/>
<p>Verfügbarkeitsdatum: 12. September 2024</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Anleitung zur Kanaleinrichtung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit der Anleitung zur Kanaleinrichtung können Sie die Kanaleinrichtung in einem einheitlichen Erlebnis automatisieren und validieren und so schneller mit Journey Optimizer beginnen. Diese Anleitung zur Kanaleinrichtung optimiert die schnelle Kanalkonfiguration und stellt sicher, dass alle erforderlichen Ressourcen in Experience Platform, Journey Optimizer und Datenerfassung sofort installiert und verwendet werden. Dadurch können Marketing-, Produkt- und Datenentwicklungsteams schnell mit der Erstellung von Kampagnen und Journeys beginnen.</p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/set-mobile-config.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/guided-setup.gif"/>
<p>Verfügbarkeitsdatum: 3. September 2024</p>
</br>
</td>
</tr>
</tbody>
</table>


### Verbesserungen {#24-9-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Zielgruppen** – Verfügbarkeitsdatum: 17. September 2024

**Lizenznutzung**: Im Dashboard zur Lizenznutzung werden nun ansprechbare Profile anstelle von ansprechbaren Zielgruppen angezeigt. [Weitere Informationen](../audience/license-usage.md)

**Content-Management**

Sie können jetzt Inhaltsvorlagen und Fragmente zwischen Sandboxes exportieren. [Weitere Informationen](../configuration/copy-objects-to-sandbox.md)

**Journeys**

* **Verbesserungen beim Live-Reporting**: Das Live-Reporting liefert Erkenntnisse zur Performance Ihrer Journeys in den letzten 24 Stunden. Es wurde durch neue Metriken (eingetretene, ausgestiegene, verworfene und fehlerhafte Profile) erweitert, die Ihnen ein tieferes Verständnis für das Verhalten von Benutzerinnen und Benutzern sowie die Performance direkt über die Journey-Arbeitsfläche ermöglichen. [Weitere Informationen](../building-journeys/report-journey.md)


* (Verfügbarkeitsdatum: 10. September) **Automatische Wiederholung bei „Zielgruppe lesen“**: Beim Abrufen des Exportauftrags werden nun standardmäßig weitere Versuche bei zielgruppenseitig ausgelösten Journeys durchgeführt (beginnend mit der Aktivität **Zielgruppe lesen** oder einem **Geschäftsereignis**). Tritt bei der Erstellung des Exportauftrags ein Fehler auf, werden alle 10 Minuten, aber höchstens eine Stunde lang, weitere Versuche unternommen. Danach wird von einem Fehler ausgegangen. Diese Journey-Typen können daher bis zu einer Stunde nach der geplanten Zeit ausgeführt werden. [Weitere Informationen](../building-journeys/read-audience.md#retries)

**E-Mail-Kanal**

* **Nachrichtenkopfzeile in gesendeter E-Mail und Blindkopie (BCC)**: Allen E-Mail-Nachrichten wurde eine neue Kopfzeile hinzugefügt. Der Wert dieser Kopfzeile ist für jede gesendete E-Mail und die zugehörige BCC-E-Mail-Kopie eindeutig. Diese Kopfzeile wird auch in den Nachrichten- und BCC-Feedback-Datensätzen gespeichert, was eine Abstimmung zwischen der Blindkopie und den entsprechenden gesendeten E-Mail-Informationen ermöglicht. [Mehr dazu](../configuration/archiving-support.md#bcc-header)

* **Spam-Bewertung** (GA): Sie können jetzt Ihre Spam-Bewertung von Inhalten in einem speziellen **Spam-Bericht** überprüfen. Mithilfe von SpamAssassin kann Adobe Journey Optimizer jetzt Ihre E-Mail-Inhalte testen und mit einer Punktzahl versehen, die angibt, ob ISPs oder Mailbox-Anbieter sie als Spam betrachten oder nicht. [Weitere Informationen](../content-management/spam-report.md)

**SMS-Kanal**

* **Bearbeiten von API-Anmeldeinformationen**: Sie können nun Einstellungen in SMS-API-Anmeldeinformationen bearbeiten, einschließlich Aktualisierungen von Opt-in-/Opt-out-Keywords und Antworten.

**APIs**

* **Campaign Simulation-API**: Verwenden Sie diese API, um einen Testversand für eine Kampagne auszulösen. Das Senden eines Kampagnen-Testversands ist ein asynchroner Prozess. Die API gibt eine proofJobId zurück, mit der der Status des Testversands überprüft werden kann. [Weitere Informationen](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}

* (Verfügbarkeitsdatum: 10. September) Die [Adobe Journey Optimizer-API-Dokumentation](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} ist jetzt interaktiv. Sie können die API-Endpunkte direkt auf den Dokumentationsseiten sondieren, um sofort Feedback zu erhalten und die technische Implementierung zu beschleunigen.


  Alle API-Referenzseiten verfügen jetzt über eine Funktion zum **Ausprobieren**, mit der Sie API-Aufrufe direkt auf der Dokumentationsseite der Website testen können. [Beschaffen Sie sich die erforderlichen Authentifizierungsberechtigungen](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} und nutzen Sie die Funktion, um die API-Endpunkte zu sondieren.

  Untersuchen Sie mithilfe dieser neuen Funktion die Anfragen an und Antworten von API-Endpunkten, um sofort Feedback zu erhalten und die technische Implementierung zu beschleunigen.

  >[!CAUTION]
  >
  >Beachten Sie, dass Sie durch die Verwendung der interaktiven API-Funktionen auf den Dokumentationsseiten echte API-Aufrufe an die Endpunkte tätigen. Denken Sie daran, wenn Sie mit Produktions-Sandboxes experimentieren.

**Konfiguration**

* **IP-Aufwärmpläne**: Diese Funktion steht nun allen Kundinnen und Kunden zur Verfügung, einschließlich Organisationen, die die Adobe-Zusatzangebote **Helathcare Shield** oder **Privacy and Security Shield** erworben haben. [Weitere Informationen](../configuration/ip-warmup-gs.md)


![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.