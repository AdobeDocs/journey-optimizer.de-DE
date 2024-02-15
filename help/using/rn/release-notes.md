---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 13ee474819aa0b63561946d94111cd76f3d5689d
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 95%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.

## Frühzeitige Versionshinweise Januar 2024 {#jan-2024}

**Veröffentlichungsdatum**: 30.–31. Jan. 2024

### Neue Funktionen{#jan24-features}

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
<p>Ab dem 1. Februar 2024, Google und Yahoo! Sie benötigen einen DMARC-Datensatz für jede Domäne, mit der Sie E-Mails an sie senden. Stellen Sie sicher, dass Sie den DMARC-Eintrag für alle Subdomains eingerichtet haben, die Sie in Journey Optimizer an Adobe delegiert haben oder an Adobe delegieren.</p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/dmarc-record-update.md">ausführlichen Dokumentation</a>.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Anwendungsfall-Playbooks</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nutzen Sie einen Katalog mit branchenspezifischen Anwendungsfall-Playbooks in Real-Time CDP und Journey Optimizer für gängige Anwendungsfälle, die Sie mit Adobe Experience Platform und Adobe Journey Optimizer durchführen können.</p><p>Nachdem Sie das Playbook ausgewählt haben, das Ihren Anforderungen am besten entspricht, können Sie es aktivieren, um die Assets zu generieren, die zur Unterstützung Ihres Anwendungsfalls benötigt werden, wie z. B. Journeys, Nachrichten, Schemata oder Segmente, und diese für eine schnellere Amortisierungszeit an Ihr Schema anpassen.</p>
<p>Weitere Informationen finden Sie in der <a href="../start/playbooks.md">ausführlichen Dokumentation</a>.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### Verbesserungen {#jan24-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Reporting**

* **Neue Domain-basierte Widgets zur Aufschlüsselung** – Es wurden neue Widgets hinzugefügt, mit denen Sie Ihre Campaign- und Journey-Berichte optimieren können. Die Widgets **Bounce-Gründe nach Domain**, **Gesendet und zugestellt nach Domains**, **Öffnungen und Klicks nach Domains** und **Bounces und Fehler nach Domains** bieten eine detaillierte Aufschlüsselung für wichtige E-Mail-Versand- und Tracking-Metriken auf Domain-Ebene. [Weitere Informationen](../reports/channel-report.md)

**SMS-Kanal**

* **Double-Opt-in** – Der Workflow „Double-Opt-in“ für SMS garantiert, dass Benutzende sich explizit für den Empfang von Nachrichten anmelden, wenn die Anfrage von ihrem Gerät aus initiiert wird. Benutzende starten den Einverständnisprozess durch Senden einer eingehenden SMS. Nach der Bestätigung des Einverständnisses wird eine Folgenachricht gesendet, in der eine letzte Überprüfung angefordert wird. Wenn kein Benutzerprofil vorhanden ist, wird es nach erfolgreicher Bestätigung erstellt. [Weitere Informationen](../sms/sms-configuration.md#create-api)

  Hinweis: Diese Funktion ist bei Sinch- und Infobip-SMS-Anbietern verfügbar.

**Journeys**

* **Dauer von Reaktionsereignissen** – Die maximale Dauer, die Sie in den **Reaktionsereignissen** definieren können, beträgt jetzt 29 Tage statt 30 Tage. [Weitere Informationen](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Zielgruppe lesen** – Die Aktivität **Zielgruppe lesen** basiert jetzt auf dem Profil-Schnappschuss-Datensatz für Batch-Segmente, der nur einmal täglich nach der Ausführung des geplanten täglichen Batch-Vorgangs generiert wird. Die Daten sind also bis zum letzten täglichen Batch-Vorgang aktuell. [Weitere Informationen](../building-journeys/read-audience.md)

* **Feldergruppen** – Mit dieser Version wird ein Problem behoben, das die Speicherung von Feldergruppen in bestimmten Fällen verhinderte.

* Die Unterstützung für `<listObject>` wurde in mehreren Funktionen geändert.

**Häufigkeitsregeln**

* **Wöchentliche und tägliche Frequenzbegrenzung** – Sie können jetzt neben der monatlichen Anzahl auch die maximale Anzahl an Nachrichten festlegen, die in einer Woche oder an einem Tag an ein Kundenprofil gesendet werden. Die Frequenzbegrenzung basiert auf dem ausgewählten Kalenderzeitraum und wird am Anfang des entsprechenden Zeitraums zurückgesetzt. [Weitere Informationen](../configuration/frequency-rules.md#create-new-rule)

**Entscheidungs-Management**

* **Frequenzbegrenzung für Edge** – Der Frequenzbegrenzungszähler wird jetzt in weniger als 3 Sekunden aktualisiert und in einer Entscheidung der Edge Decisioning-API zur Verfügung gestellt. [Weitere Informationen](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)