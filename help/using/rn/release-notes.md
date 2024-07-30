---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b2459757d1f1964c7d0b59de814bed29b0a394bb
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 91%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.

## Versionshinweise vom Juli 2024 {#27-4-2024}

**Veröffentlichungsdatum**: 30.–31. Juli 2024

### Neue Funktionen {#27-4-features}

Mit dieser Version werden die unten aufgeführten neue Funktionen eingeführt.

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>SMS-Kanal mit beliebigem Anbieter (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Zusätzlich zu den Standardanbietern Sinch, Infobip und Twilio können Sie jetzt weitere SMS-Anbieter in Journey Optimizer konfigurieren.</p>
<img src="assets/do-not-localize/byo_sms.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../sms/sms-configuration-custom.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Zusammengestellte Zielgruppenkomposition (begrenzte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Zusammengestellte Zielgruppenkomposition ist jetzt in Adobe Journey Optimizer verfügbar. Sie ermöglicht es Unternehmen, Daten zusammenzustellen, um sie in verschiedenen Anwendungsfällen besser zu nutzen. Mit diesem neuen Ansatz können Sie als Adobe Real-time Customer Data Platform- und/oder Adobe Journey Optimizer-Benutzer Datensätze direkt aus Ihrem vorhandenen Data Warehouse verbinden, um Adobe Experience Platform-Zielgruppen und -Attribute in einem System zu erstellen und anzureichern.</p>
<p>Weitere Informationen finden Sie in der <a href="https://experienceleague.adobe.com/en/docs/federated-audience-composition/using/home"  target="_blank">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#27-4-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Journeys**

* (Verfügbarkeitsdatum: 8. Juli) **Erweiterter Ausdruckseditor in der Journey-Ereigniskonfiguration** - Sie können jetzt den erweiterten Ausdruckseditor beim Konfigurieren eines-Ereignisses nutzen, um komplexere Ausdrücke zu definieren oder Funktionen in der Ereignis-ID-Bedingung zu verwenden. [Weitere Informationen](../event/about-creating.md#adv-exp-editor)

<!--**Audiences**

* The use of audiences from custom upload (CSV file) is now available for use with Privacy and Security Shield.-->

## Versionshinweise für Juni 2024 {#24-6-2024}

**Veröffentlichungsdatum**: 18.–19. Juni 2024

### Neue Funktionen {#june-24-features}

Mit dieser Version werden die unten aufgeführten neue Funktionen eingeführt.

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Anpassen von Inhaltsfragmenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Es ist nun möglich, bestimmte Felder in einem Fragment zu definieren. Diese Felder können bearbeitet werden, wenn das Fragment zu einer Kampagne oder Journey hinzugefügt wird. Dies ermöglicht die Anpassung von Inhaltsabschnitten zum Zeitpunkt ihrer Verwendung und bietet die Flexibilität zum Überschreiben von Standardwerten mit kontextspezifischen Details.</p>
<img src="../content-management/assets/do-not-localize/gif-fragments.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../content-management/customizable-fragments.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Reporting mit Customer Journey Analytics (begrenzte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Reporting verfügt über eine verbesserte Kompatibilität mit Customer Journey Analytics-Funktionen, wodurch die Berichterstellung plattformübergreifend standardisiert und die Datenkonsistenz und -zuverlässigkeit verbessert wird. Diese nahtlose Integration zwischen Journey Optimizer und Customer Journey Analytics bietet einen besseren Überblick über Leistungsmetriken und ermöglicht es Benutzenden, fundiertere Entscheidungen zu treffen.</p>
<img src="assets/do-not-localize/ajo-cja.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../reports/report-gs-cja.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>KI-Assistent in Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der KI-Assistent ist eine Funktion der Benutzeroberfläche, mit der Sie durch Adobe-Konzepte navigieren und diese verstehen und operative Erkenntnisse zu Ihrer spezifischen Umgebung erhalten können. Er ist in verschiedenen Produkten in Adobe Experience Cloud verfügbar, einschließlich Adobe Journey Optimizer.</p>
<p>Weitere Informationen finden Sie in der <a href="../start/ai-assistant.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Mehrsprachige Nachrichten in Journeys und Kampagnen (begrenzte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt im Rahmen einer Kampagne oder Journey mühelos Inhalte in mehreren Sprachen erstellen.  Mit dieser Funktion können Sie bei der Bearbeitung Ihrer Kampagne oder Journey zwischen Sprachen wechseln, den gesamten Bearbeitungsvorgang optimieren und Ihre mehrsprachigen Inhalte effizienter verwalten.</p>
<p>Mehrsprachige Inhalte sind derzeit nur für eine Gruppe von ausgewählten Organisationen verfügbar (begrenzte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an den Adobe-Support.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Experimentieren in Journeys (begrenzte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ist bereits in Kampagnen verfügbar und unterstützt jetzt Experimente in Journeys. Bei Experimenten handelt es sich um randomisierte Test, was im Rahmen von Online-Tests bedeutet, dass Sie einigen zufällig ausgewählten Benutzenden eine bestimmte Variante einer Nachricht anbieten und einer anderen zufällig ausgewählten Gruppe von Benutzenden eine andere Variante oder Abwandlung anbieten. Nach dem Angebot können Sie die Ihre gewünschten Ergebnismetriken messen, z. B. Öffnung von E-Mails, Abonnements oder Käufe.</p>
<p>Das Experimentieren in Journeys ist derzeit nur für eine Gruppe von ausgewählten Organisationen verfügbar (begrenzte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an den Adobe-Support.</p>
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

### Verbesserungen {#june24-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

#### Entscheidungs-Management

* **Unterstützung mehrerer Regeln im Entscheidungs-Management**: Sie können jetzt bis zu 10 Begrenzungsregeln für ein bestimmtes Angebot im Entscheidungs-Management hinzufügen. Dadurch wird eine bessere Kontrolle über die Art und Weise ermöglicht, wie die Angebote gesendet werden. [Weitere Informationen](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

#### Inhaltsfragmente

>[!AVAILABILITY]
>
>Bitte beachten Sie, dass diese Verbesserungen im Laufe der auf die erste Veröffentlichung folgenden Tage schrittweise eingeführt werden. Während einige Benutzende sofortigen Zugriff haben, kann es bei anderen einige Zeit dauern, bis die Verbesserungen in ihrer Umgebung verfügbar sind.

* Fragmente können nun bearbeitet werden und Änderungen können in allen Live-Journeys und Kampagnen, in denen sie verwendet werden, übernommen werden.
* Es wurden neue Status für Inhaltsfragmente eingeführt: **Entwurf**, **Live**, **Wird veröffentlicht** und **Archiviert**.
* Damit ein Fragment in einer Journey oder Kampagne verwendet werden kann, muss es sich jetzt im Status **Live** befinden. Der Prozess der Fragmenterstellung wurde um einen neuen Schritt erweitert, der es ermöglicht, das Fragment zu veröffentlichen und für die Verwendung in Journeys und Kampagnen verfügbar zu machen. Beachten Sie, dass die Veröffentlichung von Fragmenten eine neue Berechtigung erfordert.

  **ACHTUNG:** Da die Status **Entwurf** und **Live** mit der Version Juni von Journey Optimizer eingeführt wurden, haben alle Fragmente, die vor dieser Version erstellt wurden, den Status **Entwurf**, auch wenn sie in einer Journey oder Kampagne verwendet werden. Wenn Sie Änderungen an diesen Fragmenten vornehmen, müssen Sie sie [veröffentlichen](../content-management/create-fragments.md#publish), um sie „live“ zu schalten und die Änderungen an die zugehörigen Kampagnen und Journeys weiterzugeben. Außerdem müssen Sie eine neue Journey-/Kampagnenversion erstellen und veröffentlichen.

Weitere Informationen finden Sie in der Dokumentation zu [Inhaltsfragmenten](../content-management/fragments.md).

#### Journeys

* Die globale maximale Wartezeit für Journeys wurde auf 91 Tage verlängert. [Weitere Informationen](../building-journeys/journey-properties.md#global_timeout)

  Bei allen neu erstellten Journeys wird diese neue maximale Wartezeit angezeigt. Weitere Informationen finden Sie in diesem [FAQ-Abschnitt](../building-journeys/journey-properties.md#timeout-faq). Bitte beachten Sie, dass diese Änderungen im Laufe des Monats Juni schrittweise eingeführt werden. 


* Adobe Journey Optimizer unterstützt jetzt Datenschutzanfragen zum Löschen von bzw. für den Zugriff auf Daten sowie Anfragen zur Verwaltung des Datenlebenszyklus. [Weitere Informationen](../privacy/requests.md)
* Sie können nun die Spaltenbreite im Journey-Inventar ändern.
  <!--* **Advanced expression editor in Event configuration** is now GA - You can now leverage the advanced expression editor while configuring an event, allowing you to define more complex expressions or use functions in the event id condition. This capability is released in Limited Availability for selected customers. [Read more](../event/about-creating.md)-->
* **Zusammenführungsrichtlinien** sind nun allgemein verfügbar: Die von einer Journey verwendeten Zusammenführungsrichtlinien sind jetzt im gesamten Verlauf der Journey sichtbar und konsistent. [Weitere Informationen](../building-journeys/journey-properties.md#merge-policies)



#### Kampagnen

* Beim Erstellen einer Kampagne in Adobe Journey Optimizer können Sie nun in einem neuen Modal den Kampagnentyp (geplant oder ausgelöst) auswählen. [Weitere Informationen](../campaigns/create-campaign.md)

#### E-Mail-Kanal

* **Abmelde-Link:** Nach den jüngsten Ankündigungen von Gmail und Yahoo für Massenversender unterstützt Journey Optimizer die Option „Post/1-Klick“ für Abmelde-Links. Sehen Sie sich die folgenden Seiten an: [Opt-out-Verwaltung für E-Mails](../email/email-opt-out.md#unsubscribe-header) und [Konfigurieren von E-Mail-Einstellungen](../email/email-settings.md#list-unsubscribe).

  **HINWEIS** – Bei jeder neuen Kanaloberfläche ist standardmäßig die Option „Abmelde-Link in Kopfzeile“ aktiviert. Bei vorhandenen Oberflächen ist die Option „URL zum Abmelden mit einem Klick“ in den Einstellungen für die Kanaloberfläche standardmäßig deaktiviert. Wenn Sie zuvor eine URL zum Abmelden mit einem Klick im Text der E-Mail verwendet haben, ist diese Einstellung weiterhin gültig. Wenn in den Einstellungen der Kanaloberfläche die URL zum Abmelden mit einem Klick aktiviert ist, verwendet Adobe Journey Optimizer stattdessen die standardmäßig generierte URL zum Abmelden mit einem Klick in den Einstellungen der Kanaloberfläche.

#### SMS-Kanal

* Sie können jetzt mit einer einzigen API-Konfiguration eindeutige Kurzwahlnummern für jede Sandbox hinzufügen, was den Prozess effizienter und einfacher macht. [Weitere Informationen](../sms/sms-configuration.md)

* Nach der Erstellung wird das Feld **API-Token** auf der Seite **Details zu API-Anmeldedaten** jetzt maskiert.

<!--* You can now modify existing SMS configurations.-->

#### In-App-Kanal

<!--* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

* Sie können jetzt das Edge Delivery-Plug-in verwenden, um Informationen abzurufen, die Sie zum Verständnis Ihrer eingehenden Implementierungen und zur Fehlerbehebung bei diesen benötigen. [Weitere Informationen zur Ansicht „Edge Delivery“](https://experienceleague.adobe.com/de/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.


#### Direkt-Mail-Kanal

* Der Direkt-Mail-Kanal ist jetzt für alle Kundinnen und Kunden verfügbar.  [Weitere Informationen](../direct-mail/get-started-direct-mail.md)

