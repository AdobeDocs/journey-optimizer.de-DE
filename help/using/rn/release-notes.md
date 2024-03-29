---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '1392'
ht-degree: 99%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.

## März 2024 – Versionshinweise {#mar-2024}

**Veröffentlichungsdatum**: 19.–20. März 2024

### Neue Funktion {#mar-features}

Mit dieser Version wird die unten aufgeführte neue Funktion eingeführt.

<table>
<thead>
<tr>
<th><strong>Code-basierte Erlebnisse</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dem neuen Code-basierten Erlebniskanal ermöglicht Ihnen Adobe Journey Optimizer, eine erweiterte Personalisierung und Tests für Inbound-Eigenschaften durchzuführen. Auf diese Weise können Sie maßgeschneiderte Erlebnisse für verschiedene Touchpoints wie Web-Apps, Mobile Apps, Desktop-Apps, Videokonsolen, TV-verbundene Geräte, Smart-TVs, Kioske, Geldautomaten, IoT-Geräte usw. nahtlos bereitstellen.</p>
<P>Die wichtigsten Funktionen ermöglichen Folgendes:</p>
<ul><li> Universelle Personalisierung: Erweiterung personalisierter Erlebnisse über alle Touchpoints hinweg, sodass eine kohärente und maßgeschneiderte Benutzer-Journey sichergestellt ist</li>
<li>Präzise Bearbeitungsgenauigkeit: Bearbeitung bestimmter Inhalte an einzelnen Stellen in Apps oder auf Web-Seiten</li>
<li>Vielseitige Implementierung: Unterstützung für Server-seitige, API-basierte oder SDK-basierte Implementierungsmethoden zur nahtlosen Integration in Ihre Entwicklungsumgebung</li></ul></p>
<p>Weitere Informationen finden Sie in der <a href="../code-based/get-started-code-based.md">ausführlichen Dokumentation</a>.</p>
<img src="assets/do-not-localize/code-based.gif">
</tr>
</tbody>
</table>

### Verbesserungen {#mar-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Inhaltsvorlagen**

* **Miniaturansicht**: Für Inhaltsvorlagen ist jetzt der Modus **Rasteransicht** verfügbar, um den visuellen Zugriff durch die Anzeige von Miniaturansichten zu verbessern. Derzeit werden nur HTML-Vorlagen für E-Mails unterstützt. [Weitere Informationen](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >Diese Funktion wird mit begrenzter Verfügbarkeit (Limited Availability, LA) für eine kleine Gruppe von Kundinnen und Kunden veröffentlicht.

**Journeys**

Dem Journey-Authoring-Lebenszyklus wurden neue Zwischenstatus hinzugefügt:

* der Status **Wird veröffentlicht** zwischen dem Status **Entwurf** und dem Status **Live**
* der Status **Wird gestoppt** zwischen dem Status **Live** und dem Status **Gestoppt**
* der Status **Testmodus wird aktiviert** oder **Testmodus wird deaktiviert** zwischen dem Status **Entwurf** und dem Status **Entwurf (Test)**

Wenn eine Journey in einem Zwischenzustand ist, ist sie schreibgeschützt. [Weitere Informationen](../building-journeys/journey-gs.md#filter)

## Februar 2024 – Versionshinweise {#feb-2024}

**Veröffentlichungsdatum**: 21.–22. Feb. 2024

### Neue Funktionen{#feb-features}

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
<p>Weitere Informationen finden Sie in der <a href="../in-app/create-in-app-web.md">ausführlichen Dokumentation</a>.<br></br></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Multi-Channel-Inhaltsvorlagen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Neben „E-Mail“ stehen nun auch Inhaltsvorlagen für die folgenden Kanäle zur Verfügung: „Push“, „In-App“, „SMS“ und „Briefpost“. Dabei verfügt jeder Kanal über dedizierte Vorlagentypen. Für „E-Mail“ können Sie nun den Inhaltstyp auswählen, mit dem Sie den Betreff als Teil Ihrer E-Mail-Vorlage speichern können. <br/><br/></p>
<p>Weitere Informationen finden Sie in der <a href="../content-management/content-templates.md">ausführlichen Dokumentation</a>.<br></br></p>
<img src="assets/do-not-localize/multi-chan-templates.gif">
</tr>
</tbody>
</table>


### Verbesserungen {#feb-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Zielgruppen**

* **Testadressenlisten**: bei der Verwendung von **Testadressenlisten** werden jetzt Varianten unterstützt. Die Testadressen erhalten eine Kopie aller Varianten derselben Nachricht (z. B. die verschiedenen Behandlungen eines Inhaltsexperiments). [Weitere Informationen](../configuration/seed-lists.md)

Die folgenden Verbesserungen, die bisher als Beta-Version verfügbar waren, stehen jetzt allen Benutzenden zur Verfügung:

* Sie können jetzt **Zielgruppen auswählen, die durch die Zielgruppenkomposition erstellt wurden**, und Anreicherungsattribute in Journeys nutzen. [Weitere Informationen](../building-journeys/read-audience.md)

* Sie können jetzt **Zielgruppen auswählen, die aus einer CSV-Datei** in Journeys und Kampagnen hochgeladen wurden. [Weitere Informationen](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* Die Verwendung von Zielgruppen und Attributen aus der Zielgruppenkomposition und dem benutzerdefinierten Upload (CSV-Datei) ist derzeit nicht für die Verwendung mit dem Health Care Shield oder dem Privacy and Security Shield verfügbar.
  >* Der **Zielgruppen-Upload aus einer CSV-Dateiverbesserung** wird im Laufe von mehreren Tagen nach der ersten Veröffentlichung schrittweise durchgeführt. Einige Benutzerinnen und Benutzer haben zwar sofort Zugriff, bei anderen kann es jedoch zu einer Verzögerung kommen, bevor dies in ihrer Umgebung verfügbar wird.

**Journeys**

* **Filtern von Journeys**: Sie können jetzt zusätzlich zu den vorhandenen vordefinierten Datumsfiltern **eigene Daten zum Filtern des Inventars von Journeys** verwenden. Sie können die Liste verfeinern, indem Sie sich Journeys anzeigen lassen, die an einem bestimmten Datum, in einem bestimmten Monat, in einem ganzen Jahr oder in bestimmten Zeiträumen erstellt oder veröffentlicht wurden. [Weitere Informationen](../building-journeys/journey-gs.md#filter)
* **Benutzerdefinierte Aktionen**: Sie können jetzt den **Content-Typ**-Header aktualisieren. Dieser neue **Content-Typ** sollte auf JSON-Inhalte verweisen. [Weitere Informationen](../action/about-custom-action-configuration.md#url-configuration)
* **Konfiguration**: Das Attribut „identityMap“ in „stepEvents“ ist jetzt vorausgefüllt. Die primäre Identität wird als „primary = true“ definiert. [Weitere Informationen](../reports/sharing-field-list.md)
* **Benutzeroberfläche**: Die obere Leiste in den Journey-Bildschirmen wurde für ein besseres Erlebnis umgestaltet. Unter den verschiedenen Updates sehen Sie, dass das Stiftsymbol, das Ihnen den Zugriff auf die Journey-Eigenschaften ermöglicht, nun links in der oberen Leiste neben dem Journey-Namen angezeigt wird. [Weitere Informationen](../building-journeys/journey-gs.md#change-properties)

**SMS-Kanal**

* **Opt-in/Opt-out-Keywords**: Bei der Konfiguration Ihres SMS-Kanals können Sie jetzt die **Opt-in- und Opt-out-Keywords** nach Ihren Wünschen anpassen. Journey Optimizer löst die Antwort anhand dieser angegebenen Keywords aus. [Weitere Informationen](../sms/sms-configuration.md#create-api)

**Kampagnen**

* **API-ausgelöste Kampagnen**: Der cURL-Code, der nach der Aktivierung einer API-ausgelösten Kampagne generiert wurde, wurde verbessert. Er enthält jetzt alle Personalisierungsvariablen (Profil und Kontext), die in der Nachricht verwendet werden. [Weitere Informationen](../campaigns/api-triggered-campaigns.md#execute)

**Häufigkeitsregeln**

* Zusätzlich zu „E-Mail“ und „Push“ können Sie nun Häufigkeitsregeln für SMS- und Briefpost-Kanäle erstellen. Häufigkeitsregeln schließen automatisch die zu oft angeforderten Profile aus Nachrichten und Aktionen aus, wenn die Frequenzbegrenzung erreicht wird. [Weitere Informationen](../configuration/frequency-rules.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->


## Januar 2024 – Versionshinweise {#jan-2024}

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
<p>Ab dem 1. Februar 2024 verlangen Google und Yahoo!, dass Sie einen DMARC-Eintrag für jede Domain haben, über die Sie E-Mails an sie senden. Stellen Sie sicher, dass Sie den DMARC-Eintrag für alle Subdomains eingerichtet haben, die Sie in Journey Optimizer an Adobe delegiert haben oder an Adobe delegieren.</p>
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

* **Wöchentliche Frequenzbegrenzung** – Sie können jetzt neben der monatlichen Anzahl auch die maximale Anzahl an Nachrichten festlegen, die pro Woche an ein Kundenprofil gesendet werden. Die Frequenzbegrenzung basiert auf dem ausgewählten Kalenderzeitraum und wird am Anfang des entsprechenden Zeitraums zurückgesetzt. [Weitere Informationen](../configuration/frequency-rules.md#create-new-rule)

  >[!NOTE]
  >
  >Auf Anfrage ist auch eine tägliche Frequenzbegrenzung möglich. Wenden Sie sich an den Adobe-Support.

**Entscheidungs-Management**

* **Frequenzbegrenzung für Edge** – Der Frequenzbegrenzungszähler wird jetzt in weniger als 3 Sekunden aktualisiert und in einer Entscheidung der Edge Decisioning-API zur Verfügung gestellt. [Weitere Informationen](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
