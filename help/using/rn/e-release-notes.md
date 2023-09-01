---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Frühzeitige Versionshinweise zu Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 0ed72b947c176b54220b5e00cdae6ccf91aac9a8
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 100%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in den [Versionshinweisen](release-notes.md) konsolidiert.

Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise August 2023 {#aug-rn-2023}

**Veröffentlichungsdatum**: 23.-24. August 2023

### Neue Funktionen{#aug-2023-features}

Mit dieser Version werden die unten aufgeführten neuen Funktionen eingeführt.

<table>
<thead>
<tr>
<th><strong>Senden von In-App-Nachrichten in Ihren Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Es können nun innerhalb einer Journey personalisierte In-App-Nachrichten an Benutzende Ihrer App gesendet werden. Mit Journey Optimizer können Benachrichtigungen entworfen und das Nachrichten-Layout, die Anzeige, der Text und die Schaltflächen angepasst werden, um ein nahtloses Erlebnis zu schaffen.</p>
<img src="assets/in_app_journey_1.png"/>
<p>Weitere Informationen finden Sie in der <a href="../in-app/get-started-in-app.md">ausführlichen Dokumentation</a>.</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Validieren von E-Mails mit Testadressenlisten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können in Journey Optimizer jetzt Testadressenlisten erstellen und verwalten. Eine Testadressenliste besteht aus internen Adressen, die zu Ihrer eigentlichen Zielgruppe hinzugefügt werden können und zum Zeitpunkt der Versandausführung genau die gleiche Nachricht wie die angesprochenen Profile erhalten. Mit dieser Funktion können Sie die gesendeten Kommunikationen überwachen und sicherstellen, dass alle Anzeigeformate, URLs, Bilder und Links korrekt sind.</p>
<img src="../configuration/assets/seed-list-details.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Generate text and images with the Content assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the Content assistant. You can now use the Content assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
<p>This capability is currently available as a private beta.</p>
<img src="assets/gen-ai-image-2.png"/>
<p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->



### Verbesserungen {#aug-2023-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**APIs**

Eine neue API zum Erstellen und Verwalten von Inhaltsfragmenten ist jetzt verfügbar. [Weitere Informationen](https://developer.adobe.com/journey-optimizer-apis/references/content-templates/#tag/Content-fragment-API){target="_blank"}.

**E-Mail-Kanal**

In den Einstellungen für die E-Mail-Oberfläche ist eine neue Option verfügbar, mit der E-Mail-Adressen eingeschlossen werden, die aufgrund von Spam-Beschwerden in Zielgruppen mit Transaktionsnachrichten unterdrückt wurden. Selbst wenn Marketing-Nachrichten als Spam gekennzeichnet wurden, können diese Profile Transaktionsnachrichten wie Passwortzurücksetzung oder Kontoauszüge erhalten. Standardmäßig ist diese Option deaktiviert.

**Journeys**

* Sie können jetzt API-Aufrufantworten in benutzerdefinierten Aktionen nutzen und Ihre Journey basierend auf diesen Antworten koordinieren. Diese Funktion ist als private Betaversion verfügbar.
<!--* A new type of system alert has been introduced. You can now get notified when a custom action fails.
* When duplicating a journey, you can now define the name of the journey copy.-->


**Briefpost**

* Azure kann jetzt in der Konfiguration des Datei-Routings als Server-Typ ausgewählt werden.
* In den Einstellungen für die Briefpost-Oberfläche ist jetzt das kaufmännische Und-Zeichen als Spaltentrennfeld verfügbar.