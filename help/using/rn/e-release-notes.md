---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Frühzeitige Versionshinweise zu Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1cbc5512fe23db22eca4fe1a2cb512a154b01844
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 32%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

**Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise Juli 2024 {#e-2024}

**Veröffentlichungsdatum**: 30.-31. Juli 2024

### Neue Funktionen {#e-features}

Mit dieser Version werden die unten aufgeführten neue Funktionen eingeführt.

<table>
<thead>
<tr>
<th><strong>IP-Warmup-Workflow (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Beim Versenden von E-Mails an eine brandneue IP-Adresse können Sie nun einfach IP-Aufwärm-Workflows direkt über die Benutzeroberfläche ausführen. Adobe Journey Optimizer bietet eine standardisierte und effiziente Methode zum Aufwärmen von IP-Adressen, die den Best Practices für optimale Zustellbarkeit entspricht.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>SMS-Kanal mit beliebigem Provider (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Zusätzlich zu den Standardanbietern Sinch, Infobip und Twilio können Sie jetzt weitere SMS-Anbieter in Journey Optimizer konfigurieren.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Benutzerdefinierte Aktion Marketo Engage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Adobe Journey Optimizer in Adobe Marketo Engage integrieren, um Ihre B2B-Anwendungsfälle zu erstellen. Eine neue benutzerdefinierte Aktion ermöglicht es Ihnen, von einer Journey aus Daten in Marketo aufzunehmen.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Verbesserte Kanalkonfigurationen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die aktuellen Kanaloberflächenfunktionen wurden für einen konsistenten Ansatz über alle Kanäle hinweg verbessert. Sie können diese Konfigurationen jetzt für jeden Ihrer Kanäle definieren, verwalten und wiederverwenden.</p>
<p><ul>
<li>Kanaloberflächen werden jetzt in <strong>Kanalkonfigurationen</strong> umbenannt.</li>
<li>Aus dem Inventar der Kanalkonfigurationen können Sie jetzt wiederverwendbare Kanalkonfigurationen für alle Kanäle erstellen, einschließlich jetzt Web-, In-App-Messaging- oder Code-basiertem Erlebnis</li>
<li>Die Zugriffskontrolle auf Objektebene (OLAC) ist jetzt für jede Kanalkonfiguration verfügbar, sodass Sie entscheiden können, welche Ihrer Benutzer bestimmte Konfigurationen erstellen oder verwenden darf</li>
<li>Für einige Kanäle können Sie Kanalkonfigurationen erstellen, die auf mehrere Plattformen ausgerichtet sind. Ein Beispiel hierfür wäre eine In-App-Messaging-Kanalkonfiguration, die auf eine Webseite, eine iOS-App und eine Android-App ausgerichtet sein kann.</li>
</ul></p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Verbesserungen {#e-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Journeys**

* (Verfügbarkeit: 8. Juli) Sie können jetzt den erweiterten Ausdruckseditor beim Konfigurieren eines Ereignisses nutzen, um komplexere Ausdrücke zu definieren oder Funktionen in der Ereignis-ID-Bedingung zu verwenden. [Weitere Informationen](../event/about-creating.md#adv-exp-editor)

<!--* The `event-id` condition is now automatically filled during test mode. -->

**SMS-Kanal**

* Sie können jetzt bestehende SMS-Konfigurationen ändern.

**In-App-Kanal**

* Ausdrucksfragmente sind jetzt für den In-App-Kanal verfügbar.

**Push-Kanal**

* Sie können jetzt Ihre Push-Anmeldedaten für Mobile Apps in den Adobe Journey Optimizer-Kanalkonfigurationseinstellungen hinzufügen. Das Erstellen einer App-Oberfläche in der Adobe Experience Platform-Datenerfassung ist nicht mehr erforderlich.

**Zielgruppen**

* Die Verwendung von Zielgruppen und Attributen aus der Zielgruppenzusammensetzung und dem benutzerdefinierten Upload (CSV-Datei) ist jetzt für die Verwendung mit dem Gesundheitsschild oder dem Datenschutz- und Sicherheitsschild verfügbar.