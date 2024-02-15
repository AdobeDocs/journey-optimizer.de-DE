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
source-git-commit: 9eb0e37b0547a3eb00802711825ecff63ab5f4a6
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 20%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in den [Versionshinweisen](release-notes.md) konsolidiert.

Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise für Februar 2024 {#e-2024}

**Veröffentlichungsdatum**: 20.-21. Februar 2024

### Neue Funktionen{#e-features}

Mit dieser Version werden die unten aufgeführten neuen Funktionen eingeführt.


<table>
<thead>
<tr>
<th><strong>Web-In-App-Nachrichten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt die neue Web-In-App-Messaging-Funktion verwenden, um personalisierte Inhalte direkt auf Websites über modale Überlagerungsnachrichten anzuzeigen. Diese Funktion ermöglicht es Ihnen, effektiv mit Webbesuchern zu interagieren und die Benutzerinteraktion, -bindung und Konversionsraten zu verbessern.<br/><br/></p>
<!--img src="assets/do-not-localize/computed-attributes.gif"-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Geschäftsregeln (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Regeln für die Frequenzlimitierung erstellen, die für SMS- und Briefpost-Kanäle gelten. Darüber hinaus können Sie Frequenzlimitierungsregeln nach Kommunikationstyp festlegen.<br/><br/></p>
<!--img src="assets/do-not-localize/computed-attributes.gif"-->
</tr>
</tbody>
</table>



### Verbesserungen {#e-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Zielgruppen**

* Bei Verwendung von **Testadressen**. Wie jedes Profil aus der Zielgruppe erhalten auch die Testadressen eine Kopie aller Varianten derselben Nachricht (z. B. der unterschiedlichen Behandlungen eines Inhaltserprobungs).

Zuvor als Beta-Version verfügbar, sind nun die folgenden Verbesserungen für alle Benutzer verfügbar:

* Sie können jetzt **aus einer CSV-Datei hochgeladene Zielgruppen** in Journey und Kampagnen. [Weitere Informationen](../audience/about-audiences.md#segments-in-journey-optimizer)
* Sie können jetzt **Zielgruppen, die durch die Zielgruppenzusammensetzung erstellt wurden** und nutzen Anreicherungsattribute in Journey. [Weitere Informationen](../building-journeys/read-audience.md)

**Journeys**

* Sie können jetzt **Benutzerdefinierte Datumswerte zum Filtern der Journey** Inventar, zusätzlich zu den vorhandenen vordefinierten Datumsfiltern. Auf diese Weise können Sie die Liste verfeinern, indem Sie Journey anzeigen, die an einem bestimmten Datum, innerhalb eines bestimmten Monats, über ein ganzes Jahr oder innerhalb eines bestimmten Zeitraums veröffentlicht wurden.
* Sie können jetzt die Kopfzeile &quot;content-type&quot;in **benutzerdefinierte Aktionen**.
* Das Attribut identityMap in stepEvents ist jetzt vorausgefüllt. Die primäre Identität wird als &quot;primary = true&quot;definiert.
* Die obere Leiste in den Journey-Bildschirmen wurde für ein besseres Erlebnis umstrukturiert. Unter den verschiedenen Updates sehen Sie, dass das &quot;Stiftsymbol&quot;, das Ihnen den Zugriff auf die Journey-Eigenschaften ermöglicht, jetzt links in der oberen Leiste neben dem Journey-Namen angezeigt wird.


**SMS-Kanal**

* Bei der Konfiguration Ihres SMS-Kanals können Sie jetzt die **Opt-in- und Opt-out-Keywords** gemäß Ihren Voreinstellungen. Journey Optimizer Trigger die Antwort anhand dieser angegebenen Schlüsselwörter.

**Kampagnen**

* Im Abschnitt &quot;cURL-Anfrage&quot;von **API-gesteuerte Kampagnen** die sich im Status &quot;Entwurf&quot;befinden, um anzugeben, dass die Beispiel-cURL-Anforderung erst sichtbar ist, nachdem die Kampagne veröffentlicht und ausgeführt wurde.

**Entscheidungs-Management**

* Sie können jetzt **Mehrfachbegrenzungsregeln** für ein Angebot. Auf diese Weise können Sie die Kontrolle über die Art und Weise, wie Angebote gesendet werden, erhöhen.

**Inhaltsvorlagen**

* A **Miniaturansicht** ist jetzt für Inhaltsvorlagen und Fragmente verfügbar, um den visuellen Zugriff zu verbessern.
* Inhaltsvorlagen sind jetzt verfügbar für **alle Kanäle**, außer Web.