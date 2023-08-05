---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Frühzeitige Versionshinweise zu Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 100%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in den [Versionshinweisen](release-notes.md) konsolidiert.

Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise Juli 2023 {#july-rn-2023}

**Veröffentlichtungsdatum**: 26.-27. Juli

### Neue Funktionen{#july-2023-features}

Mit dieser Version werden die unten aufgeführten neuen Funktionen eingeführt.

<table>
<thead>
<tr>
<th><strong>Zielgruppenkomposition</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können nun einen Kompositions-Workflow erstellen, um vorhandene Adobe Experience Platform-Zielgruppen in einer visuellen Arbeitsfläche zu kombinieren und verschiedene Aktivitäten (Aufteilung, Anreicherung …) zum Erstellen neuer Zielgruppen zu nutzen. Neu erstellte Zielgruppen werden zusammen mit vorhandenen Zielgruppen wieder in Adobe Experience Platform gespeichert und können in Journey Optimizer-Kampagnen zur Kundenansprache verwendet werden.</p>
<p>Weitere Informationen finden Sie in der <a href="../audience/get-started-audience-orchestration.md">ausführlichen Dokumentation</a>.</p>
<p>Die Zielgruppenkomposition ist vollständig in das neue Adobe Experience Platform-Menü „Zielgruppen“ integriert, das als zentralisiertes Portal für Zielgruppen dient. Sie können jetzt eine Seite zum Durchsuchen verwenden, die ein neues Dashboard mit Segmenttrends und Überschneidungen enthält, um neue Einblicke zu erhalten und Organisations-Tools für die Ordner- und Tagging-Verwaltung zu erkunden. Eingebettet in dieses Erlebnis sind Governance-Steuerelemente für standardisierte Zielgruppenbeschriftungen sowie Funktionen für das Management des Zielgruppen-Lebenszyklus, um Aktivierungs-Workflows zu verwalten. Mit diesem neuen Management-Erlebnis können Sie Zielgruppen jetzt einfach und sicher von einem Ort aus verwalten. Weitere Informationen sind in der <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=de" target="_blank">Dokumentation zu Adobe Experience Platform</a> verfügbar.</p></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
<img src="assets/do-not-localize/gif-dm.gif"/>
<p>For more information, refer to the <a href="../direct-mail/create-direct-mail.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Konvertieren von HTML-Inhalten für den E-Mail-Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt alle HTML-Inhalte in den E-Mail-Editor von Journey Optimizer importieren und dort konvertieren. Inhaltsbausteine werden automatisch identifiziert und stehen im E-Mail-Designer zur Verfügung: Nutzen Sie seine leistungsstarken Design-Funktionen, um sie zu aktualisieren und zu personalisieren!</p>
<img src="../email/assets/html-imported_2.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Verwenden von Tags in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Zusätzlich zu Kampagnen und Journeys können Sie Ihren Landingpages, Inhaltsvorlagen, Fragmenten und Abonnementlisten jetzt einheitliche Tags von Adobe Experience Platform zuweisen. Auf diese Weise können Sie sie einfach klassifizieren und die Suche und Navigation in allen Listen verbessern. </p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../start/search-filter-categorize.md#tags">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>APIs für Inhaltsvorlagen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Adobe Journey Optimizer-Inhaltsvorlagen mithilfe von dedizierten APIs erstellen und verwalten, um eine nahtlose Integration in Ihr vorhandenes Inhaltssystem zu ermöglichen.</p>
<!--<p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p>-->
</td>
</tr>
</tbody>
</table>


### Verbesserungen {#july-2023-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

<!--
**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.-->
* Eine neue Art von Systemwarnung wurde eingeführt. Sie können sich jetzt benachrichtigen lassen, wenn eine benutzerdefinierte Aktion fehlschlägt.
-->

**Kampagnen**

* Kontextbezogene Ereignisse im Zusammenhang mit Kampagnen sind jetzt im Menü „Kontextuelle Attribute“ des Personalisierungseditors verfügbar.


**Zielgruppen**

Die Zielgruppenauswahl in Journeys oder Kampagnen wurde verbessert, indem neue Spalten hinzugefügt werden, die die Herkunft und Aktualisierungshäufigkeit von Zielgruppen anzeigen.

Mit der Veröffentlichung des Portals „Zielgruppenkomposition“ haben Adobe Experience Platform und Adobe Journey Optimizer die Verwendung der Begriffe „Zielgruppen“ und „Segment“ im System und in der Dokumentation aktualisiert.

* Zielgruppe: eine Gruppe von Personen, Konten, Haushalten oder anderen Entitäten, die gemeinsame Merkmale und Verhaltensweisen aufweisen.
* Segmentdefinition: In Adobe Experience Platform sind dies die Regeln zur Beschreibung der Hauptmerkmale oder des Verhaltens einer Zielgruppe. Dieser Begriff war früher einfach als „Segment“ bekannt.

Daher wird in Adobe Journey Optimizer und auf der Benutzeroberfläche von Adobe Experience Platform „Segmente“ durch „Zielgruppen“ ersetzt, um diesen neuen Pfad der Zielgruppenerstellung und -verwaltung widerzuspiegeln.

**APIs**

Authentifizierung der Adobe Journey Optimizer-APIs – Die JWT-Methode zum Generieren von Zugriffstoken wird nicht mehr unterstützt. Alle neuen Integrationen müssen mit der Authentifizierungsmethode OAuth-Server-zu-Server erstellt werden. Adobe empfiehlt auch, Ihre vorhandenen Integrationen zur OAuth-Methode zu migrieren. [Weitere Informationen](https://developer.adobe.com/journey-optimizer-apis/references/authentication/)


**Weitere Änderungen**

Der Export von Journey Optimizer-Datensätzen in Cloud-Speicher-Ziele ist jetzt für alle Kundinnen und Kunden als öffentliche Beta verfügbar. Diese Funktion ermöglicht es Ihnen, eine Live-Verbindung mit Zielen im Cloud-Speicher herzustellen, um den Inhalt Ihrer Datensätze zu exportieren. [Weitere Informationen](../data/export-datasets.md)




