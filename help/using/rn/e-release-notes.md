---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Frühzeitige Versionshinweise zu Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: a0a4d39519f7f02265c52934db401e036ea12df6
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 16%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in den [Versionshinweisen](release-notes.md) konsolidiert.

Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise für Februar 2024 {#e-2024}

**Veröffentlichungsdatum**: 21.-22. Februar 2024

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
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Frequenzregeln für SMS und Briefpost</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können nun Frequenzregeln für SMS- und Briefpost-Kanäle erstellen. Häufigkeitsregeln schließen automatisch zu oft angeforderte Profile aus Nachrichten und Aktionen aus, wenn die Frequenzlimitierung erreicht wird. <br/><br/></p>
<img src="assets/do-not-localize/sms-dm-rules.gif">
</tr>
</tbody>
</table>

### Verbesserungen {#e-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Zielgruppen**

* **Testadressen** - Bei Verwendung von **Testadressen**. Wie jedes Profil aus der Zielgruppe erhalten auch die Testadressen eine Kopie aller Varianten derselben Nachricht (z. B. der unterschiedlichen Behandlungen eines Inhaltserprobungs).

Zuvor als Beta-Version verfügbar, sind nun die folgenden Verbesserungen für alle Benutzer verfügbar:

* Sie können jetzt **Zielgruppen, die durch die Zielgruppenzusammensetzung erstellt wurden** und nutzen Anreicherungsattribute in Journey. [Weitere Informationen](../building-journeys/read-audience.md)

* Sie können jetzt **aus einer CSV-Datei hochgeladene Zielgruppen** in Journey und Kampagnen. [Weitere Informationen](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* Die Verwendung von Zielgruppen und Attributen aus der Zielgruppenzusammensetzung und dem benutzerdefinierten Upload (CSV-Datei) ist derzeit nicht für die Verwendung mit dem Health Care Shield oder dem Privacy and Security Shield verfügbar.
  >* Bitte beachten Sie, dass der Zielgruppen-Upload aus einer CSV-Dateiverbesserung im Laufe von mehreren Tagen nach der ersten Veröffentlichung schrittweise durchgeführt wird. Einige Benutzer haben zwar sofort Zugriff, bei anderen kann es jedoch zu einer Verzögerung kommen, bevor sie in ihren Konten verfügbar werden.

**Journeys**

* **Journey filtern** - Sie können jetzt **Benutzerdefinierte Datumswerte zum Filtern der Journey** Inventar, zusätzlich zu den vorhandenen vordefinierten Datumsfiltern. Auf diese Weise können Sie die Liste verfeinern, indem Sie Journey anzeigen, die an einem bestimmten Datum, innerhalb eines bestimmten Monats, über ein ganzes Jahr oder innerhalb eines bestimmten Zeitraums erstellt oder veröffentlicht wurden.
* **Benutzerdefinierte Aktionen** - Sie können jetzt die **content-type** -Kopfzeile. Diese neue **content-type** sollte auf JSON-Inhalte verweisen.
* **Konfiguration** - Das Attribut identityMap in stepEvents ist jetzt vorausgefüllt. Die primäre Identität wird als &quot;primary = true&quot;definiert.
* **Benutzeroberfläche** - Die obere Leiste in den Journey-Bildschirmen wurde für ein besseres Erlebnis umstrukturiert. Unter den verschiedenen Updates sehen Sie, dass das &quot;Stiftsymbol&quot;, das Ihnen den Zugriff auf die Journey-Eigenschaften ermöglicht, jetzt links in der oberen Leiste neben dem Journey-Namen angezeigt wird.

**SMS-Kanal**

* **Opt-in-/Opt-out-Keywords** - Bei der Konfiguration Ihres SMS-Kanals können Sie jetzt die **Opt-in- und Opt-out-Keywords** gemäß Ihren Voreinstellungen. Journey Optimizer Trigger die Antwort anhand dieser angegebenen Schlüsselwörter.

**Kampagnen**

* **API-gesteuerte Kampagnen** - Der cURL-Code, der nach der Aktivierung einer API-gesteuerten Kampagne generiert wurde, wurde verbessert. Es enthält jetzt alle Personalisierungsvariablen (Profil und Kontext), die in der Nachricht verwendet werden.

**Entscheidungs-Management**

* **Begrenzungsregeln** - Sie können jetzt **Mehrfachbegrenzungsregeln** für ein Angebot. Auf diese Weise können Sie die Kontrolle über die Art und Weise, wie Angebote gesendet werden, erhöhen.

**Inhaltsvorlagen**

* **Miniatur** - A **Miniaturansicht** ist jetzt für Inhaltsvorlagen und Fragmente verfügbar, um den visuellen Zugriff zu verbessern.

  >[!AVAILABILITY]
  >
  >Diese Funktion wurde unter &quot;Eingeschränkte Verfügbarkeit&quot;(LA) für eine kleine Gruppe von Kunden veröffentlicht.

* **Mehrkanalvorlagen** - Inhaltsvorlagen sind jetzt verfügbar für **alle Kanäle**, außer Web. Für E-Mail können Sie jetzt den Typ (HTML oder Inhalt) auswählen.
