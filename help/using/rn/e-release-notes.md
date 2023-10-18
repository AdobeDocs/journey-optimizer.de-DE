---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Frühzeitige Versionshinweise zu Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 28a4f04ebcda27213d3bac763fb9bea8ea4a0146
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 100%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in den [Versionshinweisen](release-notes.md) konsolidiert.

Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## September 2023 – frühzeitige Versionshinweise {#sept-rn-2023}

**Veröffentlichungsdatum**: 26.-27. September 2023

### Neue Funktionen{#sept-2023-features}

Mit dieser Version werden die unten aufgeführten neuen Funktionen eingeführt.


<table>
<thead>
<tr>
<th><strong>Konsolidierte Kanalberichte</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Funktion „Kanalbericht“ bietet Analyse- und Marketing-Fachleuten einen umfassenden Überblick über Traffic- und Interaktionsmetriken auf Kanalebene. Um auf das Menü „Bericht“ zugreifen zu können, müssen Sie über die Berechtigung „Kanalberichte anzeigen“ verfügen.</p>
<img src="assets/channel-reports.png"/>
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Datensatzexportziele (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der Export von Journey Optimizer-Datensätzen in Cloud-Speicherziele ist jetzt allgemein verfügbar. Diese Funktion ermöglicht es Ihnen, eine Live-Verbindung mit Zielen im Cloud-Speicher herzustellen, um den Inhalt Ihrer Datensätze zu exportieren.</p>
<img src="../data/assets/dataset-export-setup.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Speicherung von Mobile App-Anmeldeinformationen per Sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dieser neuen Funktion können Sie Push-Anmeldeinformationen einfach in App-Oberflächen verwalten und mit einer dedizierten Sandbox verknüpfen.</p>
<p>Weitere Informationen finden Sie in der <a href="../in-app/inapp-configuration.md">ausführlichen Dokumentation</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Berechnete Attribute</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Berechnete Attribute ermöglichen eine einfache Zusammenfassung von Ereignisdaten in Profilattributen über eine intuitive Benutzeroberfläche für eine verbesserte verhaltensbasierte Segmentierung, Personalisierung und Aktivierung. Mit dieser Funktion können Sie berechnete Attribute selbstständig erstellen, verwalten und in Segmentierung, Echtzeit-Kundenprofilzielen oder Journey Optimizer verwenden.<br/><br/>
Darüber hinaus werden durch berechnete Attribute die Segmentierung und Journey-Workflows vereinfacht, sodass Sie relevante Erlebnisse nahtlos bereitstellen können. Weitere Informationen finden Sie in der <a href="https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=de">detaillierten Dokumentation</a>.</p>
<img src="assets/do-not-localize/computed-attributes.gif">
</tr>
</tbody>
</table>


### Verbesserungen {#sept-2023-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

<!--**Audiences**

* You can now target audiences uploaded from a CSV file into journeys and campaigns.
* You can now target audiences resulting from composition workflows into journeys. -->

**Personalisierung**

* Neben visuellen Fragmenten können nun auch Ausdrucksfragmente aus der Journey Optimizer-Schnittstelle mithilfe des Ausdruckseditors erstellt, gespeichert und wiederverwendet werden. Ausdrucksfragmente ersetzen die zuvor gespeicherten Ausdrücke.

**Warnhinweise**

* Eine neue Art von Systemwarnung wurde eingeführt. Sie können sich jetzt benachrichtigen lassen, wenn die Aktion „Zielgruppe lesen“ fehlschlägt.

**Web-Kanal**

* Einzelseitenanwendungen (SPA) können jetzt im Visual Editor von Web-Designer erstellt werden. Dort können Sie auswählen, auf welche spezifischen Ansichten Sie Ihre Web-Seiten-Änderungen anwenden möchten. Eine Ansicht kann als ganze Seite oder als Gruppe visueller Elemente auf einer Seite definiert werden, z. B. als Startseite, als gesamte Produktseite oder als Rahmen für Versandvoreinstellungen auf allen Checkout-Seiten. Um Adobe Journey Optimizer-Web-Kampagnen auf SPAs zu erstellen und auszuführen, ist ein einmaliges Entwicklungs-Setup erforderlich, damit Sie die Ansichten in der Adobe Experience Platform Web SDK-Implementierung definieren können.

* Bei der Bearbeitung einer Seite mit dem Web-Designer können Sie jetzt neue Änderungen direkt aus dem Bereich **Änderungen** in Ihren Inhalt übernehmen, ohne dass eine Komponente ausgewählt und über die Designer-Oberfläche bearbeitet werden muss.
* Beim Einrichten von Web-Subdomains haben Sie jetzt die Möglichkeit, Ihre eigene Subdomain hinzuzufügen – zusätzlich zur Verwendung einer Subdomain, die bereits an Adobe delegiert wurde.

**Journeys**

* Benutzerdefinierte Aktionsantworten werden jetzt allgemein unterstützt. Sie können jetzt API-Aufrufantworten in benutzerdefinierten Aktionen nutzen und Ihre Journey auf Grundlage dieser Antworten koordinieren. Darüber hinaus wurde ein neuer Schutzmechanismus hinzugefügt, mit dem alle benutzerdefinierten Aktionen auf 5000 Aufrufe/s pro Endpunkt beschränkt werden können.
* Beim Duplizieren einer Journey können Sie jetzt den Namen der Journey-Kopie festlegen.

<!--
* The maximum duration that you can define in the Wait activity is now 29 days instead of 30.
-->

**E-Mail-Kanal**

Eine neue Option in der E-Mail-Oberflächenkonfiguration ermöglicht den Versand von Transaktionsnachrichten an Profile, selbst wenn deren E-Mail-Adressen auf der Adobe Journey Optimizer-Unterdrückungsliste stehen.

**SMS-Kanal**

Zwei neue Felder, **Opt-in-Nachricht** und **Hilfemeldung**, wurden zum API-Konfigurationsbildschirm hinzugefügt, sodass Benutzende die Antworten an eingehende Keywords anpassen können. Beachten Sie, dass dies nur für den SMS-Anbieter Sinch verfügbar ist.

**Reporting**

Sie können jetzt Journey Optimizer-Berichte als CSV-Datei exportieren. [Weitere Informationen](../reports/global-report.md#export-reports)

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->
