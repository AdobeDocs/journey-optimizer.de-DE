---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Frühzeitige Versionshinweise zu Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 553743d6d041cd719eb3c8bf7f02288595d8c2a5
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 30%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

**Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise für Juni 2024 {#e-2024}

**Veröffentlichungsdatum**: 18.-19. Juni 2024

### Neue Funktionen {#e-features}

Mit dieser Version werden die unten aufgeführten neue Funktionen eingeführt.

<table>
<thead>
<tr>
<th><strong>IP-Warmup-Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Wenn Sie E-Mails an eine brandneue IP-Adresse senden, können Sie jetzt einfach IP-Warmup-Workflows direkt über die Benutzeroberfläche durchführen. Adobe Journey Optimizer bietet eine standardisierte und effiziente Möglichkeit, Ihre IP-Adressen aufzuwärmen, die den Best Practices für eine optimale Zustellbarkeit entsprechen.</p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/ip-warmup-gs.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Anpassung von Inhaltsfragmenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt bestimmte Felder in einem Fragment definieren, die bearbeitet werden können, wenn das Fragment einer Kampagne oder Journey hinzugefügt wird. Dies ermöglicht die Anpassung der Inhaltsabschnitte zum Zeitpunkt der Verwendung und bietet Flexibilität, Standardwerte mit kontextspezifischen Details zu überschreiben.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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


<!--table>
<thead>
<tr>
<th><strong>Reporting with Customer Journey Analytics (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer reporting is now fully integrated with Customer Journey Analytics capabilities, standardizing reporting across both platforms and improving data consistency and reliability. This seamless integration between Journey Optimizer and Customer Journey Analytics provides a clearer view of performance metrics, enabling users to make more informed decisions.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns  (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now effortlessly create content in multiple languages within a single campaign or journey. With this feature, you can switch between languages when editing your campaign or your journey, streamlining the entire editing process and improving your capability to efficiently manage multilingual content.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Experimentation in journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Already available in campaigns, Adobe Journey Optimizer now supports experiments in journeys. Experiments are randomized trials, which in the context of online testing, means that you expose some randomly selected users to a given variation of a message, and another randomly selected set of users to some other variation or treatment. After exposure, you can then measure the outcome metrics you are interested in, such as opens of emails, subscriptions, or purchases.</p>
</td>
</tr>
</tbody>
</table-->



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


**Entscheidungs-Management**

* **Unterstützung mehrerer Regeln in der Entscheidungsverwaltung** - Sie können jetzt bis zu 10 Begrenzungsregeln für ein bestimmtes Angebot in der Entscheidungsverwaltung hinzufügen. Auf diese Weise können Sie die Kontrolle über die Art und Weise, wie Angebote gesendet werden, erhöhen.  [Weitere Informationen](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

**Inhaltsfragmente**

* Fragmente können jetzt bearbeitet werden und Änderungen können über alle Live-Journey und Kampagnen hinweg übernommen werden, in denen sie verwendet werden.
* Es wurden neue Status für Inhaltsfragmente eingeführt: **Entwurf**, **Live**, **Publishing**, und **Archiviert**.
* Um ein Fragment in einer Journey oder Kampagne zu verwenden, muss es sich jetzt in der **Live** -Status. Dem Fragmenterstellungsprozess wurde ein neuer Schritt hinzugefügt, mit dem das Fragment veröffentlicht und für die Verwendung in Journey und Kampagnen verfügbar gemacht werden kann - Beachten Sie, dass für die Fragmentveröffentlichung eine neue Berechtigung erforderlich ist.

  **VORSICHT** - seit **Entwurf** und **Live** -Status mit der Journey Optimizer-Version vom Juni eingeführt wurden, haben alle vor dieser Version erstellten Fragmente die **Entwurf** Status, auch wenn sie in einer Journey oder Kampagne verwendet werden. In diesem Abschnitt erfahren Sie, wie Sie Ihre vorhandenen Fragmente aktualisieren.

**Journeys**

* Die globale Zeitüberschreitung bei der Journey wurde von 30 auf 91 Tage erhöht.
* Adobe Journey Optimizer unterstützt jetzt Datenschutz-Löschungs-/Zugriffsanfragen.
* Sie können nun die Spaltengröße im Journey-Inventar ändern.
* **Erweiterter Ausdruckseditor in der Ereigniskonfiguration** ist jetzt allgemein verfügbar - Sie können jetzt den erweiterten Ausdruckseditor beim Konfigurieren eines Ereignisses nutzen, um komplexere Ausdrücke zu definieren oder Funktionen in der Ereignis-ID-Bedingung zu verwenden. Diese Funktion wird mit begrenzter Verfügbarkeit (Limited Availability, LA) für eine ausgewählte Gruppe von Kundinnen und Kunden veröffentlicht. [Weitere Informationen](../event/about-creating.md)
* **Zusammenführungsrichtlinien** sind jetzt allgemein verfügbar - Zusammenführungsrichtlinien, die von einem Journey verwendet werden, sind jetzt auf dem gesamten Journey sichtbar und konsistent. Diese Funktion wird mit begrenzter Verfügbarkeit (Limited Availability, LA) für eine ausgewählte Gruppe von Kundinnen und Kunden veröffentlicht. [Weitere Informationen](../building-journeys/journey-gs.md#merge-policies)



**Kampagnen**

* Beim Erstellen einer Kampagne in Adobe Journey Optimizer können Sie jetzt den Kampagnentyp (geplant oder ausgelöst) in einem neuen Modal auswählen.

**E-Mail-Kanal**

* **List-unsubscribe** - Nach den jüngsten Ankündigungen von Gmail und Yahoo für Massen-Absender unterstützt Journey Optimizer die Option &quot;Post/1-Click&quot; List-Unsubscribe . <!--Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**SMS-Kanal**

* Sie können jetzt eindeutige Kurzwahlnummern für jede Sandbox mit einer einzelnen API-Konfiguration hinzufügen, wodurch der Prozess effizienter und rationeller wird.
  <!--* You can now modify existing SMS configurations.-->

**In-App-Kanal**

* **Ausdrucksfragment** - Ausdrucksfragmente sind jetzt für die **In-App-Kanal**. [Weitere Informationen](../personalization/use-expression-fragments.md)


* Sie können jetzt das Edge-Bereitstellungs-Plug-in verwenden, um Informationen zu erhalten, die zum Verständnis und zur Fehlerbehebung bei Ihren eingehenden Implementierungen erforderlich sind.


