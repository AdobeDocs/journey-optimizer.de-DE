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
source-git-commit: fae367cbbacffbbecde4cdbf7b39b1baeec452d1
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 20%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in den [Versionshinweisen](release-notes.md) konsolidiert.

Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise für Januar 2024 {#oct-jan-2024}

**Veröffentlichungsdatum**: 30.-31. Januar 2024

### Neue Funktionen{#jan-2024-features}

Mit dieser Version werden die unten aufgeführten neuen Funktionen eingeführt.


<table>
<thead>
<tr>
<th><strong>Zustellbarkeits-Updates</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer unterstützt jetzt die DMARC-Authentifizierungstechnologie.</p>
<p>Ab dem 1. Februar 2024, Google und Yahoo! erfordert, dass Sie über einen DMARC-Datensatz für jede Domäne verfügen, mit der Sie E-Mails an sie senden. Stellen Sie sicher, dass Sie DMARC-Datensatz für alle Subdomains eingerichtet haben, die Sie in Journey Optimizer an Adobe delegiert haben oder delegieren.</p>
<!--img src="assets/channel-reports.png"/-->
<p>Weitere Informationen finden Sie in der <a href="../configuration/dmarc-record-update.md">ausführlichen Dokumentation</a>.</p>
</tr>
</tbody>
</table>



### Verbesserungen {#jan-2024-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Reporting**

* **Kanalberichte nach Domain** - Es wurden neue Widgets hinzugefügt, um Ihre Kampagnen- und Journey-Berichte zu verbessern. Die **Bounce-Gründe nach Domain**, **Gesendet und von Domänen bereitgestellt**, **Öffnungen und Klicks nach Domain** und **Bounce und Fehler nach Domain** -Widgets bieten eine detaillierte Aufschlüsselung auf Domänenebene für wichtige E-Mail-Versand- und Tracking-Metriken.

**SMS-Kanal**

* **Double Opt-in** - Der Workflow für die Anmeldung mit zweifacher Bestätigung für SMS garantiert, dass Benutzer sich explizit für den Empfang von Nachrichten anmelden, wenn die Anfrage von ihrem Gerät aus initiiert wird. Benutzer starten den Genehmigungsprozess durch Senden einer eingehenden SMS. Nach Bestätigung der Zustimmung wird eine Folgenachricht gesendet, in der eine endgültige Überprüfung angefordert wird. Wenn kein Benutzerprofil vorhanden ist, wird es nach erfolgreicher Bestätigung erstellt.

  Beachten Sie, dass dies nur für die SMS-Anbieter Sinch und Infobip gilt.

**Journeys**

* **Dauer der Reaktionsereignisse** - Die maximale Dauer, die Sie im **Reaktionsereignisse** ist jetzt 29 Tage anstelle von 30.

* **Datumsfilter** - Sie können jetzt benutzerdefinierte Datumswerte verwenden, um das Journey-Inventar zusätzlich zu den bereits vordefinierten Datumsfiltern zu filtern. Auf diese Weise können Sie die Liste verfeinern, indem Sie Journey anzeigen, die an einem bestimmten Datum, innerhalb eines bestimmten Monats, über ein ganzes Jahr oder innerhalb eines bestimmten Zeitraums veröffentlicht wurden.

* **Audience lesen**  - Die Aktivität Audience lesen basiert jetzt auf dem Profil-Snapshot-Datensatz für Batch-Segmente, der nur einmal täglich nach Ausführung des geplanten täglichen Batch-Auftrags generiert wird.

**Häufigkeitsregeln**

* **Häufigkeitsgrenze pro Woche und Tag** - Sie können jetzt zusätzlich zum Monat die maximale Anzahl an Nachrichten festlegen, die an ein Kundenprofil in einer Woche oder an einem Tag gesendet werden. Die Frequenzlimitierung basiert auf dem ausgewählten Kalenderzeitraum und wird am Anfang des entsprechenden Zeitrahmens zurückgesetzt.


**Entscheidungs-Management**

* **Frequenzlimitierung an Edge** - Der Frequenzlimitierungszähler wird jetzt aktualisiert und ist in weniger als 3 Sekunden in einer Entscheidung der Edge Decisioning API verfügbar.