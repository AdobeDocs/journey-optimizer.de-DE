---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Frühzeitige Versionshinweise zu Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 3d166f79d9f6334c6f873ba3eecd264a60b8f4ba
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 43%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in den [Versionshinweisen](release-notes.md) konsolidiert.

Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise für August 2023 {#aug-rn-2023}

**Veröffentlichungsdatum**: 23.-24. August 2023

### Neue Funktionen{#aug-2023-features}

Mit dieser Version werden die unten aufgeführten neuen Funktionen eingeführt.

<table>
<thead>
<tr>
<th><strong>In-App-Nachrichten in Ihren Journey senden</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können Ihren App-Benutzern jetzt innerhalb einer Journey personalisierte In-App-Nachrichten senden. Mit Journey Optimizer können Benachrichtigungen entworfen und das Nachrichten-Layout, die Anzeige, der Text und die Schaltflächen angepasst werden, um ein nahtloses Erlebnis zu schaffen.</p>
<img src="assets/in_app_journey_1.png"/>
<p>Weitere Informationen finden Sie in der <a href="../in-app/get-started-in-app.md">ausführlichen Dokumentation</a>.</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>E-Mails mit Seed-Listen validieren</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt in Journey Optimizer Testlisten erstellen und verwalten. Eine Testliste besteht aus Test-E-Mail-Adressen, an die Sie eine E-Mail senden, bevor sie an Ihre eigentliche Audience gesendet werden. Mit dieser Funktion können Sie die gesendeten E-Mail-Kopien überwachen und sicherstellen, dass alle Anzeigeformate, URLs, Bilder und Links korrekt sind.</p>
<img src="../configuration/assets/seed-list-details.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Generieren von Text und Bildern mit dem Inhaltsassistenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nachdem Sie Ihre Nachricht erstellt und personalisiert haben, stellen Sie mit dem Inhaltsassistenten die nächste Stufe Ihres Inhalts dar. Sie können jetzt den Inhaltsassistenten verwenden, um die Wirkung Ihrer Nachricht zu optimieren, indem Sie mit verschiedenen Haupttiteln und Bildern experimentieren. Jede Variante wird als individuelle Behandlung verwaltet, um zu messen und zu vergleichen, welcher Titel effektiv mehr Klicks generiert.</p>
<p>Diese Funktion ist als private Betaversion verfügbar.</p>
<img src="assets/gen-ai-image-2.png"/>
<!--p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>



### Verbesserungen {#aug-2023-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**APIs**

Eine neue API zum Erstellen und Verwalten von Inhaltsfragmenten ist jetzt verfügbar. [Weitere Informationen](https://developer.adobe.com/journey-optimizer-apis/references/content-templates/#tag/Content-fragment-API){target="_blank"}.

**E-Mail-Kanal**

* In den E-Mail-Oberflächeneinstellungen ist eine neue Option verfügbar, mit der E-Mail-Adressen eingeschlossen werden, die aufgrund von Spam-Beschwerden in Zielgruppen mit Transaktionsnachrichten unterdrückt wurden. Selbst wenn Marketing-Nachrichten als Spam gekennzeichnet wurden, können diese Profile Transaktionsnachrichten wie Kennwortzurücksetzung oder Kontoauszüge erhalten. Standardmäßig ist diese Option deaktiviert.

**Journeys**

* Sie können jetzt API-Aufrufantworten in benutzerdefinierten Aktionen nutzen und Ihre Journey basierend auf diesen Antworten koordinieren.
* Eine neue Art von Systemwarnung wurde eingeführt. Sie können sich jetzt benachrichtigen lassen, wenn eine benutzerdefinierte Aktion fehlschlägt.


**Briefpost**

* Unterstützung von Azure Blob als Routing-Ziel.
* Unterstützung von &quot;&amp;&quot;als benutzerdefiniertes Trennzeichen.