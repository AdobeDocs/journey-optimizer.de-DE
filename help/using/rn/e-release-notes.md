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
source-git-commit: 9fdaff7a4364bb7ecfeec27446ed8f4b4ce34488
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 52%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

**Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise August 2024 {#e-2024}

**Veröffentlichungsdatum**: 20.-21. August 2024

### Neue Funktionen {#e-features}

Mit dieser Version werden die unten aufgeführten neue Funktionen eingeführt.

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

* In der Aktivität **Bedingung** ist die Bedingung &quot;Zeit&quot;standardmäßig nach Stunde (von 00:00 Uhr bis 12:00 Uhr) festgelegt. [Weitere Informationen](../building-journeys/condition-activity.md#time_condition)

**Zielgruppen**

* Zielgruppen aus benutzerdefinierten Uploads (CSV-Datei) stehen jetzt zur Verwendung mit Privacy und Security Shield zur Verfügung.

<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
