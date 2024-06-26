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
source-git-commit: 6c4e0418776622467e7f5b7bb3d9332d965becf1
workflow-type: ht
source-wordcount: '434'
ht-degree: 100%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

**Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden**. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise Juli 2024 {#e-2024}

**Veröffentlichungsdatum**: 18.–19. Juni 2024

### Neue Funktionen {#e-features}

Mit dieser Version werden die unten aufgeführten neue Funktionen eingeführt.

<table>
<thead>
<tr>
<th><strong>IP-Aufwärm-Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Beim Versenden von E-Mails an eine brandneue IP-Adresse können Sie nun einfach IP-Aufwärm-Workflows direkt über die Benutzeroberfläche ausführen. Adobe Journey Optimizer bietet eine standardisierte und effiziente Methode zum Aufwärmen von IP-Adressen, die den Best Practices für optimale Zustellbarkeit entspricht.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Content Fragments customization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define specific fields in a fragment that can be edited when the fragment is added to a campaign or journey. This allows for the adjustment of content portions at the time of use, providing flexibility to override default values with context-specific details.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->


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

* **Unterstützung mehrerer Regeln im Entscheidungs-Management**: Sie können jetzt bis zu 10 Begrenzungsregeln für ein bestimmtes Angebot im Entscheidungs-Management hinzufügen. Dadurch wird eine bessere Kontrolle über die Art und Weise ermöglicht, wie die Angebote gesendet werden. [Weitere Informationen](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

<!--**Content fragments**

* Fragments can now be edited, and changes can be propagated across all live journeys and campaigns where they are used.
* New statuses for content fragments have been introduced: **Draft**, **Live**, **Publishing**, and **Archived**. 
* To use a fragment in a journey or campaign, it must now be in the **Live** status. A new step has been added to the fragment creation process, allowing the fragment to be published and made available for use in journeys and campaigns. Note that fragment publishing requires a new permission.
   
   **CAUTION** - Since **Draft** and **Live** statuses have been introduced with Journey Optimizer June release, all fragments created before this release have the **Draft** status, even if they are used in a journey or campaign. Learn how to update your existing fragments in this section.-->

**Journeys**

* Der globale Timout für Journeys wurde von 30 auf 91 Tage erhöht.
* Adobe Journey Optimizer unterstützt jetzt Datenschutzanfragen zum Löschen/Zugriff auf Daten sowie Anfragen zur Verwaltung des Datenlebenszyklus.
* Sie können nun die Spaltenbreite im Journey-Inventar ändern.
* **Erweiterter Ausdruckseditor in der Ereigniskonfiguration** ist nun allgemein verfügbar: Sie können jetzt den erweiterten Ausdruckseditor beim Konfigurieren eines Ereignisses nutzen, um komplexere Ausdrücke zu definieren oder Funktionen in der Ereignis-ID-Bedingung zu verwenden. Diese Funktion wird mit begrenzter Verfügbarkeit (Limited Availability, LA) für eine ausgewählte Gruppe von Kundinnen und Kunden veröffentlicht. <!--[Read more](../event/about-creating.md)-->
* **Zusammenführungsrichtlinien** sind nun allgemein verfügbar: Die von einer Journey verwendeten Zusammenführungsrichtlinien sind jetzt im gesamten Verlauf der Journey sichtbar und konsistent. Diese Funktion wird mit begrenzter Verfügbarkeit (Limited Availability, LA) für eine ausgewählte Gruppe von Kundinnen und Kunden veröffentlicht. <!--[Read more](../building-journeys/journey-gs.md#merge-policies)-->



**Kampagnen**

* Beim Erstellen einer Kampagne in Adobe Journey Optimizer können Sie nun in einem neuen Modal den Kampagnentyp (geplant oder ausgelöst) auswählen.

<!--**Email channel**

* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**SMS-Kanal**

* Sie können jetzt mit einer einzigen API-Konfiguration eindeutige Kurzwahlnummern für jede Sandbox hinzufügen, was den Prozess effizienter und schlanker macht.
  <!--* You can now modify existing SMS configurations.-->

**In-App-Kanal**

* **Ausdrucksfragment** – Ausdrucksfragmente sind jetzt für den **In-App-Kanal** verfügbar. <!--[Read more](../personalization/use-expression-fragments.md)--> 


* Sie können jetzt das Edge Delivery-Plug-in verwenden, um Informationen abzurufen, die Sie zum Verständnis Ihrer eingehenden Implementierungen und zur Fehlerbehebung bei diesen benötigen. 
