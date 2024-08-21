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
source-git-commit: 428e08ca712724cb0b3453681bee1c7e86ce49dc
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 61%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

**Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise August 2024 {#e-2024}

**Veröffentlichungsdatum**: 20.–21. August 2024

### Neue Funktionen {#e-features}

Mit dieser Version werden die unten aufgeführten neue Funktionen eingeführt.

<table>
<thead>
<tr>
<th><strong>Variablen in Inhaltsfragmenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Fragmente können jetzt Eingabevariablen verwenden, sowohl in <a href="../personalization/use-expression-fragments.md">Ausdrucksfragmenten</a> als auch in <a href="../email/use-visual-fragments.md">visuellen Fragmenten</a>. Sie können diese Variablen verwenden, um Ihren Nachrichteninhalt und Ihre Nachrichtenparameter in Ihren Kampagnen und Journey zu personalisieren.</p>
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

* In der Aktivität **Bedingung** ist die Bedingung „Zeit“ jetzt standardmäßig stundenweise festgelegt, von 00:00 bis 12:00 Uhr. [Weitere Informationen](../building-journeys/condition-activity.md#time_condition)
* Beim Erstellen Ihrer Journey werden Warnhinweise jetzt in einer Dropdown-Liste angezeigt, um sie mit Kampagnenwarnungen abzustimmen und ein einheitliches Benutzererlebnis zu gewährleisten. [Weitere Informationen](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* Die Zoom-Optionen in der Journey-Symbolleiste wurden verbessert: Der Zoom-Prozentsatz ist jetzt sichtbar und Sie können den Zoomwert jetzt einfach auf 100 % zurücksetzen.

**Zielgruppen**

* Zielgruppen aus benutzerdefinierten Uploads (CSV-Datei) stehen jetzt zur Verwendung mit Privacy und Security Shield zur Verfügung.
* Beim Targeting einer benutzerdefinierten Upload-Zielgruppe (CSV-Datei) können Sie jetzt Attribute aus der Datei in Ihren Kampagnen und Journey verwenden. Diese Attribute sind im Personalisierungseditor verfügbar, um Ihre Nachrichten zu personalisieren, sowie im erweiterten Ausdruckseditor von Journey.


<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
