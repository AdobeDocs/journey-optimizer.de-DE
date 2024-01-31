---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 146a142afeb47debac0d56963e48225a85b0f2c4
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 28%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.

## Frühzeitige Versionshinweise für Januar 2024 {#jan-2024}

**Veröffentlichungsdatum**: 30.-31. Januar 2024

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
<p>Ab dem 1. Februar 2024, Google und Yahoo! erfordert, dass Sie über einen DMARC-Datensatz für jede Domäne verfügen, mit der Sie E-Mails an sie senden. Stellen Sie sicher, dass Sie DMARC-Datensatz für alle Subdomains eingerichtet haben, die Sie in Journey Optimizer an Adobe delegiert haben oder delegieren.</p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/dmarc-record-update.md">ausführlichen Dokumentation</a>.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Anwendungsbeispiele für Playbooks</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nutzen Sie einen Katalog branchenspezifischer Anwendungsfallbücher in Real-Time CDP und Journey Optimizer, um gängige Anwendungsfälle zu behandeln, die Sie mit Adobe Experience Platform und Adobe Journey Optimiser durchführen können.</p><p>Nachdem Sie das Playbook ausgewählt haben, das Ihren Anforderungen am besten entspricht, können Sie es aktivieren, um die Assets zu generieren, die zur Unterstützung Ihres Anwendungsfalls benötigt werden, wie z. B. Journey, Nachrichten, Schemas oder Segmente, und diese für eine schnellere Wertschöpfungszeit an Ihr Schema anpassen.</p>
<p>Weitere Informationen finden Sie in der <a href="../start/playbooks.md">ausführlichen Dokumentation</a>.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### Verbesserungen {#jan24-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Reporting**

* **Neue domänenbasierte Aufschlüsselungs-Widgets** - Es wurden neue Widgets hinzugefügt, um Ihre Kampagnen- und Journey-Berichte zu verbessern. Die **Bounce-Gründe nach Domain**, **Gesendet und von Domänen bereitgestellt**, **Öffnungen und Klicks nach Domain** und **Bounce und Fehler nach Domain** -Widgets bieten eine detaillierte Aufschlüsselung auf Domänenebene für wichtige E-Mail-Versand- und Tracking-Metriken. [Weitere Informationen](../reports/channel-report.md)

**SMS-Kanal**

* **Double Opt-in** - Der Workflow für die Anmeldung mit zweifacher Bestätigung für SMS garantiert, dass Benutzer sich explizit für den Empfang von Nachrichten anmelden, wenn die Anfrage von ihrem Gerät aus initiiert wird. Benutzer starten den Genehmigungsprozess durch Senden einer eingehenden SMS. Nach Bestätigung der Zustimmung wird eine Folgenachricht gesendet, in der eine endgültige Überprüfung angefordert wird. Wenn kein Benutzerprofil vorhanden ist, wird es nach erfolgreicher Bestätigung erstellt. [Weitere Informationen](../sms/sms-configuration.md#create-api)

  Beachten Sie, dass diese Funktion bei Sinch- und Infobip-SMS-Anbietern verfügbar ist.

**Journeys**

* **Dauer der Reaktionsereignisse** - Die maximale Dauer, die Sie im **Reaktionsereignisse** ist jetzt 29 Tage anstelle von 30. [Weitere Informationen](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Audience lesen**  - die **Audience lesen** -Aktivität basiert nun auf dem Profil-Snapshot-Datensatz für Batch-Segmente, der nur einmal täglich nach der Ausführung des geplanten täglichen Batch-Auftrags generiert wird. Daher werden die Daten bis zum letzten täglichen Batch-Auftrag aktualisiert. [Weitere Informationen](../building-journeys/read-audience.md)

* **Feldergruppen** - Diese Version behebt ein Problem, das die Speicherung von Feldergruppen in bestimmten Fällen verhinderte.

**Häufigkeitsregeln**

* **Häufigkeitsgrenze pro Woche und Tag** - Sie können jetzt zusätzlich zum Monat die maximale Anzahl an Nachrichten festlegen, die an ein Kundenprofil in einer Woche oder an einem Tag gesendet werden. Die Frequenzlimitierung basiert auf dem ausgewählten Kalenderzeitraum und wird am Anfang des entsprechenden Zeitrahmens zurückgesetzt. [Weitere Informationen](../configuration/frequency-rules.md#create-new-rule)

**Entscheidungs-Management**

* **Frequenzlimitierung an Edge** - Der Frequenzlimitierungszähler wird jetzt aktualisiert und ist in weniger als 3 Sekunden in einer Entscheidung der Edge Decisioning API verfügbar. [Weitere Informationen](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)