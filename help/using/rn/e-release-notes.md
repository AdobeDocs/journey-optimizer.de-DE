---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Frühzeitige Versionshinweise zu Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 949d1e021cf46aebf7bf564797d717205e4cf4b8
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 25%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

**Frühe Versionshinweise unten können ohne vorherige Ankündigung bis zum Verfügbarkeitsdatum der Version geändert werden**. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

## Frühzeitige Versionshinweise Mai 2024 {#e-2024}

**Veröffentlichungsdatum**: 21.-22. Mai 2024

### Neue Funktionen {#e-features}

Mit dieser Version werden die unten aufgeführten neue Funktionen eingeführt.


<table>
<thead>
<tr>
<th><strong>Erlebnis-Entscheidung – begrenzte Verfügbarkeit</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experience Decisioning vereinfacht die Personalisierung, indem es einen zentralisierten Katalog von Marketing-Angeboten, die als „Entscheidungselemente“ bezeichnet werden und eine ausgereifte Entscheidungs-Engine anbietet. Diese Engine nutzt Regeln und Ranking-Kriterien, um die relevantesten Entscheidungselemente für jeden Kontakt auszuwählen und darzustellen.</p>
<p>Diese Entscheidungselemente sind über den neuen code-basierten Erlebniskanal, der jetzt in Journey Optimizer-Kampagnen verfügbar ist, nahtlos in eine breite Palette eingehender Oberflächen integriert. Entscheidungsrichtlinien für Erlebnisentscheidungen stehen nur in code-basierten Erlebniskampagnen zur Verfügung.</p>
<p>Erlebnis-Entscheidung ist derzeit nur für eine Gruppe von Organisationen verfügbar (begrenzte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an Ihren Adobe-Support.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../experience-decisioning/gs-experience-decisioning.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


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
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
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

**Erlebnisentscheidungen** (Eingeschränkte Verfügbarkeit)

Von der Beta-Version zu dieser Version wurden die folgenden Verbesserungen hinzugefügt:

* **Erlebnisentscheidungen + code-basierte Erlebnisse** - Sie können jetzt die Experience Decisioning-Funktion nutzen, um Entscheidungselemente in Ihren code-basierten Kampagnen zu verwenden. Hinweis: Der code-basierte Erlebniskanal und die Erlebnisentscheidung stehen nicht für Organisationen zur Verfügung, die das Adobe Healthcare Shield und das Datenschutz- und Sicherheitsschild-Add-On-Angebot erworben haben. [Weitere Informationen](../code-based/get-started-code-based.md)
* **Kontextdaten** - Sie können jetzt Kontextdaten aus Adobe Experience Platform in Ihren Entscheidungsregeln und Ranglisten-Formeln nutzen. [Weitere Informationen](../experience-decisioning/context-data.md)
* **Neue Berechtigung** - Für die Ressource &quot;Entscheidungsverwaltung&quot;ist jetzt die neue Berechtigung &quot;Erlebnisentscheidungen verwalten&quot;verfügbar. Sie können damit Berechtigungen im Zusammenhang mit Experience Decisioning verwalten. [Weitere Informationen](../experience-decisioning/gs-experience-decisioning.md)
* **Begrenzungsregeln** - Sie können jetzt mehrere Begrenzungsregeln für ein bestimmtes Entscheidungselement in Experience Decisioning hinzufügen. Auf diese Weise können Sie die Kontrolle über die Art und Weise, wie Angebote gesendet werden, erhöhen. [Weitere Informationen](../experience-decisioning/items.md#capping)
* **Berichterstellung** - Sie können jetzt benutzerdefinierte Reporting-Dashboards von Experience Decisioning-Kampagnen erstellen, indem Sie [!DNL Customer Journey Analytics]. [Weitere Informationen](../experience-decisioning/cja-reporting.md)


**Entscheidungs-Management**

* **Unterstützung mehrerer Regeln** - Sie können jetzt bis zu 10 Begrenzungsregeln für ein bestimmtes Angebot in der Entscheidungsverwaltung hinzufügen. Auf diese Weise können Sie die Kontrolle über die Art und Weise, wie Angebote gesendet werden, erhöhen.
* **Prüfungen** - die **Änderungsprotokoll** -Tab, in dem alle Änderungen angezeigt werden, die an einem Angebot oder einer entfernten Entscheidung vorgenommen wurden. Änderungen in Bezug auf Angebote und Entscheidungen können jetzt im Menü **Audits** eingesehen werden.


**E-Mail-Kanal**

* **List-unsubscribe** - Nach den jüngsten Ankündigungen von Gmail und Yahoo für Massen-Absender unterstützt Journey Optimizer die Option &quot;Post/1-Click&quot; List-Unsubscribe .
* **Spam-Bewertung** (Beta) - Sie können jetzt Ihre Spam-Bewertung von Inhalten in einem speziellen Spam-Bericht überprüfen. Mithilfe von SpamAssassin kann Adobe Journey Optimizer jetzt Ihren E-Mail-Inhalt testen und eine Punktzahl angeben, um anzugeben, ob ISP-Anbieter ihn als Spam betrachten oder nicht.
  <!--[Read more](../content-management/spam-report.md)-->

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

**Personalisierung**

* **Ausdrucksfragment** - Ausdrucksfragmente sind jetzt für die **In-App-Kanal**.
  <!--[Read more](../personalization/use-expression-fragments.md)-->

**Journeys**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **Unterstützung von mTLS** - Die mTLS-Authentifizierung wird jetzt in benutzerdefinierten Aktionen unterstützt. Für die benutzerdefinierte Aktion oder das Journey ist keine zusätzliche Konfiguration erforderlich, um mTLS zu aktivieren. Sie erfolgt automatisch, wenn ein mTLS-fähiger Endpunkt erkannt wird.
* **Suchtabellen in Ereignissen** - Sie können jetzt Daten aus einem Lookup-Datensatz nutzen, wenn eine Beziehung mithilfe eines Attributs innerhalb eines Arrays von Objekten definiert wurde. Die Suchwerte stehen in Journey zur Verfügung (Bedingungen, benutzerdefinierte Aktionen usw.) und der Nachrichtenpersonalisierung nicht verfügbar.
* **Erweiterter Ausdruckseditor in der Ereigniskonfiguration** - Sie können jetzt den erweiterten Ausdruckseditor beim Konfigurieren eines Ereignisses nutzen, um komplexere Ausdrücke zu definieren oder Funktionen in der Ereignis-ID-Bedingung zu verwenden.

**Globalisierung**

In unseren laufenden Bemühungen um ein einheitliches Benutzererlebnis harmonisieren wir die in den Adobe Experience Cloud-Produkten und -Apps verwendete Terminologie. Dies wirkt sich auf den deutschen Begriff &quot;Titel&quot; aus, der in &quot;Titel&quot; geändert wird, wenn er sich auf den Namen eines Objekts bezieht. Die Änderungen werden schrittweise in der Benutzeroberfläche und Dokumentation bereitgestellt.
