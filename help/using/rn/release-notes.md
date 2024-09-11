---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 633d2f423301680a7aff83b748a08a6f1a1bbf16
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 83%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.

## Aktualisierungen für September {#9-2024}

<table>
<thead>
<tr>
<th><strong>AI Assistant in Journey Optimizer - Content Accelerator </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nachdem Sie Ihre Nachricht erstellt und personalisiert haben, stellen Sie mit dem AI-Assistenten in Journey Optimizer for Content Acceleration den Inhalt auf die nächste Stufe. Sie können jetzt den KI-Assistenten verwenden, um die Wirkung Ihrer Nachricht zu optimieren, indem Sie mit verschiedenen Haupttiteln und Bildern experimentieren. Jede Variante wird als eindeutige Abwandlung verwaltet, um zu messen und zu vergleichen, welcher Titel effektiv mehr Klicks generiert.</p>
<p>Machen Sie sich mit <a href="https://experienceleague.adobe.com/en/apps/journey-optimizer/ai-assistant-content-accelerator">unserer Live-Funktionsvorschau</a> vertraut, die Ihnen ermöglicht, die Funktionen selbst zu entdecken und die Funktionen vollständig zu verstehen.</a></p>
<p>Weitere Informationen finden Sie in der <a href="../content-management/gs-generative.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/>
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
<p>Verfügbarkeitsdatum: 3. September</p>
</br>
</td>
</tr>
</tbody>
</table>

**Journeys**

(Verfügbarkeitsdatum: 10. September) **Wiederholungsfunktion** - Beim Abrufen des Exportauftrags werden nun standardmäßig Wiederholungen auf durch die Zielgruppe ausgelöste Journey angewendet (beginnend mit einer **Leserichtung** oder einem **Geschäftsereignis**). Tritt bei der Erstellung des Exportauftrags ein Fehler auf, werden alle 10 Minuten erneute Versuche unternommen, höchstens jedoch für eine Stunde. Danach werden wir es als Fehler betrachten. Diese Journey können daher bis zu 1 Stunde nach der geplanten Zeit ausgeführt werden. [Weitere Informationen](../building-journeys/read-audience.md#retries)

## Versionshinweise für August 2024 {#8-2024}

**Veröffentlichungsdatum**: 20.–21. August 2024

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

### Neue Funktionen {#8-features}

Mit dieser Version werden die unten aufgeführten neue Funktionen eingeführt.

<!--
<table>
<thead>
<tr>
<th><strong>Content Cards (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content cards are a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</br>
<p>Content card are currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Verbesserte Kanalkonfigurationen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die aktuellen Kanaloberflächenfunktionen wurden verbessert, um einen einheitlichen Ansatz für alle Kanäle zu gewährleisten. Sie können diese Konfigurationen jetzt für jeden Ihrer Kanäle definieren, verwalten und wiederverwenden, einschließlich Web, In-App-Nachrichten oder Code-basierter Erlebnisse.</p>
<p><ul>
<li>Kanaloberflächen sind jetzt in <strong>Kanalkonfigurationen</strong> umbenannt.</li>
<li>Sie können eine oder mehrere Marketing-Aktionen anhängen, um Einverständnis- und Data Governance-Richtlinien durchzusetzen.</li>
<li>Die Zugriffskontrolle auf Objektebene (OLAC) ist jetzt für jede Kanalkonfiguration verfügbar, sodass Sie entscheiden können, welche Ihrer Benutzenden bestimmte Konfigurationen erstellen oder verwenden dürfen.</li>
<li>Für einige Kanäle können Sie Kanalkonfigurationen erstellen, die auf mehrere Plattformen abzielt. Ein Beispiel hierfür wäre eine In-App-Messaging-Kanalkonfiguration, die auf eine Webseite, eine iOS-App und eine Android-App abzielt.</li>
</ul></p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/channel-surfaces.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Benutzerdefinierte Marketo Engage-Aktion</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können Adobe Journey Optimizer jetzt in Adobe Marketo Engage integrieren, um Ihre B2B-Anwendungsfälle zu erstellen. Eine neue benutzerdefinierte Aktion ermöglicht es Ihnen, von einer Journey aus Daten in Marketo aufzunehmen.</p>
<p>Weitere Informationen finden Sie in der <a href="../action/marketo-engage.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Variablen in Inhaltsfragmenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Globale Fragmentvariablen verbessern die vorhandene Fragmentfunktion, um die Effizienz der Wiederverwendbarkeit und Skripterstellung von Inhalten zu verbessern. Fragmente können jetzt Eingabevariablen verwenden und Ausgabevariablen erstellen, die in Kampagnen- und Journey-Inhalten verwendet werden können. In Fragmenten können Eingabevariablen verwendet werden, sowohl in <a href="../personalization/use-expression-fragments.md">Ausdrucksfragmenten</a> als auch in <a href="../email/use-visual-fragments.md">visuellen Fragmenten</a>. Sie können diese Variablen verwenden, um die Inhalte und Parameter der Nachrichten in Ihren Kampagnen und Journeys zu personalisieren.</p>
<p>Weitere Informationen finden Sie in der <a href="../personalization/use-expression-fragments.md">ausführlichen Dokumentation</a>.</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>IP-Aufwärm-Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Verfügbarkeitsdatum: 13. August</p>
<p>Beim Versenden von E-Mails an eine brandneue IP-Adresse können Sie nun einfach IP-Aufwärm-Workflows direkt über die Benutzeroberfläche ausführen. Adobe Journey Optimizer bietet eine standardisierte und effiziente Methode zum Aufwärmen von IP-Adressen, die den Best Practices für optimale Zustellbarkeit entspricht.</p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/ip-warmup-gs.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#8-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Journeys**

* In der Aktivität **Bedingung** ist die **[!UICONTROL Zeit-Bedingung]** jetzt standardmäßig stundenweise festgelegt, von 00:00 bis 12:00 Uhr. [Mehr dazu](../building-journeys/condition-activity.md#time_condition)
* Beim Erstellen Ihrer Journeys werden Warnhinweise jetzt über die Schaltfläche **Warnungen** angezeigt, um sie mit anderen Warnungen abzugleichen und ein einheitliches Anwendererlebnis zu gewährleisten. [Mehr dazu](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* Die Zoom-Optionen in der Journey-Symbolleiste wurden verbessert: Der Zoom-Prozentsatz ist jetzt sichtbar, und der Zoom-Wert kann leichter zurückgesetzt werden.

<!--**Audiences and Profiles**-->

<!--* The use of audiences from custom upload (CSV file) is now available for use with Privacy and Security Shield add-on.-->
<!--* When targeting a custom upload (CSV file) audience, you can now use attributes from the file in your campaigns and journeys. These attributes are available in the personalization editor, to personalize your messages, and the journey advanced expression editor.-->
<!--* The License usage dashboard now shows the count of Engageable Profiles. [Read more](../audience/license-usage.md)-->

**Push-Kanal**

* Sie können die Push-Anmeldedaten Ihrer App jetzt in den Konfigurationseinstellungen des Adobe Journey Optimizer-Kanals hinzufügen. Das Erstellen einer App-Oberfläche in der Adobe Experience Platform-Datenerfassung ist nicht mehr erforderlich.

### Weitere Änderungen {#changes}

**Reporting**

* Das aktuelle Reporting wird mit der Oktober-Version eingestellt. Nach diesem Datum wird das neue Reporting-Erlebnis zum Standard. Wir empfehlen, sich mit den neuen Funktionen und Funktionalitäten vertraut zu machen, um einen reibungslosen Übergang zu gewährleisten.

[Erste Schritte mit der neuen Reporting-Oberfläche von Journey Optimizer](../reports/report-gs-cja.md)

* Es wurden neue Anwendungsfälle zum neuen Berichtserlebnis hinzugefügt:

   * Erstellen Sie benutzerdefinierte berechnete Metriken direkt in Ihren Berichten.
   * Erstellen Sie eine Zielgruppe aus Berichtsdaten.
   * Verwenden Sie das Tool für die Sondierungsanalyse, um mühelos Tabellen und Visualisierungen aus Ihren ausgewählten **[!UICONTROL Dimensionen]** und **[!UICONTROL Metriken]** zu erstellen.

  Weitere Informationen finden Sie in der [ausführlichen Dokumentation](../reports/report-cja-manage.md).
