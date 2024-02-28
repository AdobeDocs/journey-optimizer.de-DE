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
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 90%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in den [Versionshinweisen](release-notes.md) konsolidiert.

Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise Februar 2024 {#e-2024}

**Veröffentlichungsdatum**: 21.–22. Feb. 2024

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
<p>Sie können jetzt die neue Web-In-App-Nachrichten-Funktion verwenden, um personalisierte Inhalte direkt auf Websites über modale Überlagerungsnachrichten anzuzeigen. Diese Funktion ermöglicht es Ihnen, effektiv mit Besucherinnen und Besuchern im Web zu interagieren und die Benutzerinteraktion, -bindung und Konversionsraten zu verbessern.<br/><br/></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Häufigkeitsregeln für SMS und Briefpost</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können nun Häufigkeitsregeln für SMS- und Briefpost-Kanäle erstellen. Häufigkeitsregeln schließen automatisch die zu oft angeforderten Profile aus Nachrichten und Aktionen aus, wenn die Frequenzbegrenzung erreicht wird. <br/><br/></p>
<img src="assets/do-not-localize/sms-dm-rules.gif">
</tr>
</tbody>
</table>

### Verbesserungen {#e-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Zielgruppen**

* **Testadressenlisten**: bei der Verwendung von **Testadressenlisten** werden jetzt Varianten unterstützt. Wie jedes Profil der Zielgruppe erhalten auch die Testadressenlisten eine Kopie aller Varianten derselben Nachricht (z. B. die verschiedenen Behandlungen eines Inhaltsexperiments).

Die folgenden Verbesserungen, die bisher als Beta-Version verfügbar waren, stehen jetzt allen Benutzenden zur Verfügung:

* Sie können jetzt **Zielgruppen auswählen, die durch die Zielgruppenkomposition erstellt wurden**, und Anreicherungsattribute in Journeys nutzen. [Weitere Informationen](../building-journeys/read-audience.md)

* Sie können jetzt **Zielgruppen auswählen, die aus einer CSV-Datei** in Journeys und Kampagnen hochgeladen wurden. [Weitere Informationen](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* Die Verwendung von Zielgruppen und Attributen aus der Zielgruppenkomposition und dem benutzerdefinierten Upload (CSV-Datei) ist derzeit nicht für die Verwendung mit dem Health Care Shield oder dem Privacy and Security Shield verfügbar.
  >* Bitte beachten Sie, dass der Zielgruppen-Upload aus einer CSV-Dateiverbesserung im Laufe von mehreren Tagen nach der ersten Veröffentlichung schrittweise durchgeführt wird. Einige Benutzende haben zwar sofort Zugriff, bei anderen kann es jedoch zu einer Verzögerung kommen, bevor dies in ihren Konten verfügbar wird.

**Journeys**

* **Filtern von Journeys**: Sie können jetzt zusätzlich zu den vorhandenen vordefinierten Datumsfiltern **eigene Daten zum Filtern des Inventars von Journeys** verwenden. Auf diese Weise können Sie die Liste verfeinern, indem Sie Journey anzeigen, die an einem bestimmten Datum, innerhalb eines bestimmten Monats, über ein ganzes Jahr oder innerhalb eines bestimmten Zeitraums erstellt oder veröffentlicht wurden.
* **Benutzerdefinierte Aktionen** - Sie können jetzt die **content-type** -Kopfzeile. Diese neue **content-type** sollte auf JSON-Inhalte verweisen.
* **Konfiguration**: Das Attribut identityMap in stepEvents ist jetzt vorausgefüllt. Die primäre Identität wird als „primary = true“ definiert.
* **Benutzeroberfläche**: Die obere Leiste in den Journey-Bildschirmen wurde für ein besseres Erlebnis umstrukturiert. Unter den verschiedenen Updates sehen Sie, dass das Stiftsymbol, das Ihnen den Zugriff auf die Journey-Eigenschaften ermöglicht, jetzt links in der oberen Leiste neben dem Journey-Namen angezeigt wird.

**SMS-Kanal**

* **Opt-in/Opt-out-Keywords**: Bei der Konfiguration Ihres SMS-Kanals können Sie jetzt die **Opt-in- und Opt-out-Keywords** nach Ihren Wünschen anpassen. Journey Optimizer triggert die Antwort anhand dieser angegebenen Keywords.

**Kampagnen**

* **API-ausgelöste Kampagnen**: Der cURL-Code, der nach der Aktivierung einer API-ausgelösten Kampagne generiert wurde, wurde verbessert. Es enthält jetzt alle Personalisierungsvariablen (Profil und Kontext), die in der Nachricht verwendet werden.

**Entscheidungs-Management**

* **Begrenzungsregeln**: Sie können jetzt **mehrere Begrenzungsregeln** für ein Angebot hinzufügen. Auf diese Weise können Sie die Kontrolle über die Art und Weise, wie Angebote gesendet werden, erhöhen.

**Inhaltsvorlagen**

* **Miniaturansicht**: Eine **Miniaturansicht** ist jetzt für Inhaltsvorlagen und Fragmente verfügbar, um den visuellen Zugriff zu verbessern.

  >[!AVAILABILITY]
  >
  >Diese Funktion wurde unter &quot;Eingeschränkte Verfügbarkeit&quot;(LA) für eine kleine Gruppe von Kunden veröffentlicht.

* **Multi-Channel-Vorlagen**: Inhaltsvorlagen sind jetzt für **alle Kanäle**, außer dem Web, verfügbar. Für E-Mail können Sie jetzt den Typ (HTML oder Inhalt) auswählen.
