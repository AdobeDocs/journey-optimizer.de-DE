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
source-git-commit: 2eb1ffff7101362b52ae91f1a7277188664b2954
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 31%

---

# Frühzeitige Versionshinweise {#e-release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden am Ende jedes Monats in den [Versionshinweisen](release-notes.md) zusammengefasst.

Die nachfolgenden frühzeitigen Versionshinweise können bis zum Verfügbarkeitsdatum der Version ohne vorherige Ankündigung geändert werden. Links, Bildschirme und aktualisierte Dokumentation werden in den [Versionshinweisen](release-notes.md) am Veröffentlichungsdatum veröffentlicht.

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
<p>Weitere Informationen finden Sie in der <a href="../configuration/ip-warmup-gs.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Geschäftsregeln - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Regeln für die detaillierte Frequenzlimitierung erstellen und diese über Regelsätze auf verschiedene Arten der Marketing-Kommunikation anwenden. </p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Erweiterte Personalisierungsdaten - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Datenwerte in Adobe Experience Platform-Datensätzen suchen und abrufen und diese Werte zum Erstellen von Bedingungen in Adobe Journey Optimizer verwenden. Sie können Daten aus einem Lookup-Datensatz nutzen, wenn eine Beziehung mithilfe eines Attributs innerhalb eines Arrays von Objekten definiert wurde. Sie können nicht profilaktivierte Datensätze für die Suche angeben. Nach der Aktivierung können Sie ein Profilattribut als Join-Schlüssel für den angegebenen Datensatz verwenden, um weitere Daten zur Personalisierung abzurufen.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#e-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

**Erlebnisentscheidungen**

Von Beta bis LA wurden die folgenden Verbesserungen hinzugefügt:

* **Erlebnisentscheidungen + Code-basierte Erlebnisse (LA)**: Sie können jetzt die Experience Decisioning-Funktion nutzen, um Entscheidungselemente in Ihren code-basierten Kampagnen zu verwenden. Hinweis: Der code-basierte Erlebniskanal und die Erlebnisentscheidung stehen nicht für Organisationen zur Verfügung, die das Adobe Healthcare Shield und das Datenschutz- und Sicherheitsschild-Add-On-Angebot erworben haben. [Weitere Informationen](../code-based/get-started-code-based.md)
* Sie können jetzt Kontextdaten aus Adobe Experience Platform in Ihren Entscheidungsregeln und Ranglisten-Formeln nutzen. [Weitere Informationen](../experience-decisioning/context-data.md)
* Für die Entscheidungs-Management-Ressource ist jetzt die neue Berechtigung „Erlebnis-Entscheidung verwalten“ verfügbar. Sie können damit Berechtigungen im Zusammenhang mit Experience Decisioning verwalten. [Weitere Informationen](../experience-decisioning/gs-experience-decisioning.md)
* Sie können jetzt mehrere Begrenzungsregeln für ein bestimmtes Entscheidungselement in Erlebnis-Entscheidung hinzufügen. Auf diese Weise können Sie die Kontrolle über die Art und Weise, wie Angebote gesendet werden, erhöhen. [Weitere Informationen](../experience-decisioning/items.md#capping)
* Sie können jetzt benutzerdefinierte Berichterstellungs-Dashboards von Experience Decisioning-Kampagnen erstellen, indem Sie [!DNL Customer Journey Analytics]. [Weitere Informationen](../experience-decisioning/cja-reporting.md)


**Offer Decisioning**

* **Unterstützung mehrerer Regeln** - Sie können jetzt bis zu 10 Begrenzungsregeln für ein bestimmtes Angebot in der Entscheidungsverwaltung hinzufügen. Auf diese Weise können Sie die Kontrolle über die Art und Weise, wie Angebote gesendet werden, erhöhen.
* **Prüfungen** - die **Änderungsprotokoll** -Tab, in dem alle Änderungen angezeigt werden, die an einem Angebot oder einer entfernten Entscheidung vorgenommen wurden. Änderungen in Bezug auf Angebote und Entscheidungen können jetzt im Menü **Audits** eingesehen werden.


**E-Mail-Kanal**

* **List-unsubscribe** - Nach den jüngsten Ankündigungen von Gmail und Yahoo für Massen-Absender unterstützt Journey Optimizer die Option &quot;Post/1-Click&quot; List-Unsubscribe .
* **Spam-Bewertung** (Beta) - Sie können jetzt Ihre Spam-Bewertung von Inhalten in einem speziellen Spam-Bericht überprüfen. Mithilfe von SpamAssassin kann Adobe Journey Optimizer jetzt Ihren E-Mail-Inhalt testen und eine Punktzahl angeben, um anzugeben, ob ISP-Anbieter ihn als Spam betrachten oder nicht. [Weitere Informationen](../content-management/spam-report.md)


**Zielgruppen**

* Die Verwendung von Zielgruppen und Attributen aus der Zielgruppenzusammensetzung und dem benutzerdefinierten Upload (CSV-Datei) ist jetzt für die Verwendung mit dem Gesundheitsschild oder dem Datenschutz- und Sicherheitsschild verfügbar.

**Personalisierung**

* **Ausdrucksfragment** - Ausdrucksfragmente sind jetzt für die **In-App-Kanal**. [Weitere Informationen](../personalization/use-expression-fragments.md)

**Journeys**

* **Zusammenführungsrichtlinien** - Zusammenführungsrichtlinien können jetzt in Ihren Journey konfiguriert und verwendet werden.
* **Unterstützung von mTLS** - Das mTLS-Protokoll wird jetzt in Journey Optimizer-APIs und benutzerdefinierten Aktionen unterstützt.
* **Suchtabellen in Ereignissen** - Sie können jetzt Daten aus einem Lookup-Datensatz nutzen, wenn eine Beziehung mithilfe eines Attributs innerhalb eines Arrays von Objekten definiert wurde. Die Suchwerte stehen in Journey zur Verfügung (Bedingungen, benutzerdefinierte Aktionen usw.) und der Nachrichtenpersonalisierung nicht verfügbar.
