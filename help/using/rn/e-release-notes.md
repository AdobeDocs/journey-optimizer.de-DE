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
source-git-commit: 004eb41b084f32993ec437f589e4e3d2cf7500d3
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 100%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in den [Versionshinweisen](release-notes.md) konsolidiert.

Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise Oktober 2023 {#oct-rn-2023}

**Veröffentlichungsdatum**: 25.–26. Oktober 2023

### Neue Funktionen{#oct-2023-features}

Mit dieser Version werden die unten aufgeführten neuen Funktionen eingeführt.

<table>
<thead>
<tr>
<th><strong>Sandbox-Werkzeuge</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Sandbox-Werkzeugen können Sie Objekte über mehrere Sandboxes hinweg kopieren, indem Sie den Export und Import von Paketen nutzen. Ein Paket kann aus einem oder mehreren Objekten bestehen. Alle Objekte, die in einem Paket enthalten sind, müssen aus derselben Sandbox stammen.</p>
<!--img src="../data/assets/dataset-export-setup.png"-->
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Composed audiences in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use audiences created in composition workflows in your journeys to target customers. Once an audience composition is published, and the audience saved, use a Read Audience activity to select this new audience in your journey canvas.</p>
<img src="assets/channel-reports.png"/>
<p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table -->

<table>
<thead>
<tr>
<th><strong>Multimedia Message Service (MMS) in SMS (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dem SMS-Kanal können Sie Ihre Kommunikation jetzt verbessern, indem Sie MMS-Nachrichten (Multimedia Message Service) senden, sodass Sie Bilder, GIFs oder Videos mit Ihren Kundinnen und Kunden teilen können. Beachten Sie, dass diese Funktion derzeit nur für Beta und mit Sinch verfügbar ist.</p>
<!--img src="assets/channel-reports.png"/-->
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

### Verbesserungen {#oct-2023-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Zielgruppen**

* Sie können jetzt Zielgruppen auswählen, die aus einer CSV-Datei in Journeys und Kampagnen hochgeladen wurden.
* Sie können jetzt Zielgruppen auswählen, die durch die Zielgruppenkomposition erstellt wurden, und Anreicherungsattribute in Journeys nutzen.

>[!AVAILABILITY]
>
>Diese Funktionen sind als private Betaversion verfügbar.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**Kampagnen**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* Tritt in einer Ihrer Kampagnen ein Fehler auf, wird in der Kampagnenliste neben dem Status der Kampagne nun ein Warnsymbol angezeigt.

**Journeys**

* Die maximale Dauer, die Sie in einer beliebigen Wartezeit definieren können, beträgt jetzt 29 Tage anstelle von 30. Dies gilt für:

   * das Feld **Dauer** in der [Warteaktivität](../building-journeys/wait-activity.md)
   * die **Wartezeit beim erneuten Eintritt** in den [Journey-Eigenschaften](../building-journeys/journey-gs.md#entrance)
   * das Feld **Warten auf** in der Timeout-Definition von [allgemeinen](../building-journeys/general-events.md#events-specific-time) und [reaktiven](../building-journeys/reaction-events.md) Ereignissen.

**Einverständnis in der Kanalkonfiguration**

* Jetzt können Sie eine Marketing-Aktion auf der Ebene der Kanaloberfläche auswählen. Bei Verwendung in einer Oberfläche werden alle mit dieser Marketing-Aktion verknüpften Zustimmungsrichtlinien genutzt, um die Voreinstellungen Ihrer Kundinnen und Kunden zu respektieren.

**Entscheidungs-Management**

* Mehrere Bezeichnungen zur Angebotsbegrenzung in der Benutzeroberfläche für das Entscheidungs-Management wurden aktualisiert.
