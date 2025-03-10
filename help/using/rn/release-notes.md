---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
feature: Release Notes
topic: Content Management
description: Versionshinweise zu Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 78c1464ccddec75e4827cbb1877d8fab5ac08b90
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 87%

---

# Versionshinweise {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Neue Funktionen"
>abstract="**Adobe Journey Optimizer** bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert."

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert. [!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Updates vom 25. März {#25-03-rn}

**Verbesserungen am Personalization-Editor**

Der Journey Optimizer-Personalisierungseditor wurde um neue Funktionen erweitert:
* **Aktualisiertes Design für den Code-Editor** - Eine sauberere, moderne Benutzeroberfläche für verbesserte Benutzerfreundlichkeit und Fokus.
* **Suchen und Ersetzen** - Es wurde eine Funktion hinzugefügt, mit der Inhalte im Editor schnell gesucht und ersetzt werden können.
* **Unterstützung zum Rückgängigmachen und Wiederholen** - Ermöglicht das einfache Zurücksetzen oder erneute Anwenden von Änderungen.
* **Anpassbare Schriftgröße** - Ermöglicht die Anpassung der Schriftgröße des Editors, um die Lesbarkeit zu verbessern.
* **Inline-JSON** Validierung - Client-seitige Validierung von JSON-Inhalten in Echtzeit, um die Fehlererkennung zu beschleunigen.
* **Automatische Vervollständigung für Profil- und**) - Bietet intelligente Vorschläge zur Optimierung der Inhaltserstellung.
* **Verbesserte Syntaxhervorhebung** - Verbessert die Lesbarkeit, indem die Code-Struktur visuell besser unterschieden wird.

Weitere Informationen finden Sie in der [ausführlichen Dokumentation](../personalization/personalization-build-expressions.md).

## Februar 2025 – Versionshinweise {#25-02-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**Veröffentlichungsdatum**: 18.–19. Februar 2025


### Neue Funktionen {#25-02-features}

Im Folgenden werden die neuen Funktionen dieser Version beschrieben.

<table>
<thead>
<tr>
<th><strong>Erstellen und Verwalten von Geschäftsregeln</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Geschäftsregeln mithilfe von Regelsätzen erstellen. Regelsätze sind Gruppen von Regeln, mit denen innerhalb von Kampagnen gesendete Nachrichten und kanalübergreifende Journey-Aktionen eingeschränkt sowie Profileintritte in Journeys gesteuert werden können.<p>
<p><ul><li>Erstellen Sie Kanalregelsätze, um die Anzahl der Nachrichten zu beschränken, die über einen oder mehrere Kanäle gesendet werden. Wenden Sie sie auf Kampagnen- oder Journey-Aktionen an, um die im Regelsatz definierten Regeln durchzusetzen. Mit einem Kanalregelsatz können Sie Begrenzungsregeln basierend auf Kommunikationstypen anwenden. Legen Sie beispielsweise einen Regelsatz fest, um sich auf „Werbenachrichten“ zu begrenzen, und einen weiteren für „Newsletter“. Wenden Sie den entsprechenden Regelsatz in Ihrer Kampagnen- oder Journey-Aktion an, je nach dem Kommunikationstyp, den Sie verwenden.</li>
<li> Erstellen Sie Journey-Regelsätze, um Profileintritte in Journeys zu steuern. Schränken Sie etwa ein, wie oft ein Profil innerhalb eines bestimmten Zeitraums auf eine Journey zugreifen kann oder für wie viele Journeys ein Profil gleichzeitig registriert sein kann. Wenden Sie diese Regeln auf der Journey-Ebene an, um eine ordnungsgemäße Eintrittsverwaltung sicherzustellen.</li></p>
<p>Geschäftsregeln, die zuvor nur für eine Reihe von Organisationen verfügbar waren (LA), stehen jetzt allen Benutzenden zur Verfügung (GA).</p>
<p>Weitere Informationen finden Sie in der <a href="../configuration/rule-sets.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Generieren von Landingpages mit dem KI-Assistenten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mithilfe des KI-Assistenten können Sie jetzt überzeugende Inhalte für Ihre Landingpages erstellen, einschließlich ganzseitiger Designs, personalisiertem Text und personalisierter Visualisierungen.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>Weitere Informationen finden Sie in der <a href="../content-management/generative-lp.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Marken mit dem KI-Assistenten (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Ihre eigenen Marken festlegen, um die visuelle und sprachliche Identität Ihrer Marke zu definieren. </p>
<p>Diese Funktion wird als Private Beta für eine begrenzte Anzahl von Kundinnen und Kunden veröffentlicht. Sie wird in zukünftigen Versionen schrittweise allen Kundinnen und Kunden zur Verfügung stehen.</p>
<p>Weitere Informationen finden Sie in der <a href="../content-management/brands.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Fehlerbehebung bei benutzerdefinierten Aktionen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt eine benutzerdefinierte Aktionskonfiguration validieren, indem Sie echte API-Aufrufe direkt aus Adobe Journey Optimizer durchführen. </p>
<p>Weitere Informationen finden Sie in der <a href="../action/troubleshoot-custom-action.md">ausführlichen Dokumentation</a>.</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Flexible Zielgruppenauswertung (eingeschränkte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit der flexiblen Zielgruppenauswertung können Sie nach Bedarf einen Segmentierungsauftrag für ausgewählte Zielgruppen ausführen, um sicherzustellen, dass Sie immer über die neuesten Zielgruppendaten verfügen, bevor Sie sie in Journey Optimizer-Journeys und -Kampagnen aufnehmen.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Weitere Informationen finden Sie in der <a href="../audience/creating-a-segment-definition.md#flexible">ausführlichen Dokumentation</a>.</p>
<p>Diese Funktion ist nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an den Adobe-Support.</p>
<p>Verfügbarkeitsdatum: 28. Januar 2025</p>
</tr>
</tbody>
</table>
</table>


### Verbesserungen {#25-02-improvements}

Die folgenden Verbesserungen werden mit dem Februar-Update vorgenommen.

* **Journeys**: Sie können jetzt Ihre benutzerdefinierten Aktionen testen, indem Sie API-Aufrufe vom Abschnitt „Administration“ aus senden. Mit dieser neuen Funktion können Sie Fehler bei benutzerdefinierten Aktionen beheben, bevor oder nachdem diese in einer Journey verwendet werden. [Weitere Informationen](../action/troubleshoot-custom-action.md)

* **Time-to-Live (TTL) für Datensätze**: Ab diesem Monat werden in neuen Sandboxes und neuen Organisationen für systemgenerierte Journey Optimizer-Datensätze als Schutzmechanismen die folgenden Limits für die Time-to-Live (TTL) eingeführt:

   * 90 Tage für Daten im Profilspeicher
   * 13 Monate für Daten im Data Lake

  Diese Änderung wird in einer nachfolgenden Phase in bestehende Kunden-Sandboxes integriert.

  Weitere Informationen zu diesem Update finden Sie in [den häufig gestellten Fragen zu diesem Thema](../data/datasets-ttl.md#frequently-asked-questions).

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **Briefpost**: Ein neuer Server-Typ, Data Landing Zone, wird jetzt für das Datei-Routing in der Konfiguration des Direkt-Mail-Kanals unterstützt. [Weitere Informationen](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **SMS**: Sie können jetzt den SMS-Nachrichtenversand über multiregionale Endpunkte verwalten, indem Sie Versand-, Feedback- und Callback-URLs sowie URLs eingehender Nachrichten überschreiben. Um dies zu unterstützen, wurde zur Konfiguration der API-Anmeldedaten das neue Feld „Überschreibungs-URL“ hinzugefügt. Diese Änderung ist nur beim Anbieter Sinch verfügbar. [Weitere Informationen](../sms/sms-configuration-sinch.md)

* **Personalisierung** (Verfügbarkeitsdatum: 29. Januar 2025): Es stehen neue Hilfsfunktionen für Datum/Uhrzeit zur Verwendung im Personalisierungseditor zur Verfügung. [Weitere Informationen](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **E-Mail-Konfiguration**: Im Falle einer Einverständnisverwaltung außerhalb von Adobe können Sie nun eine benutzerdefinierte Abmelde-E-Mail-Adresse und eine benutzerdefinierte URL zum Abmelden mit einem Klick im Rahmen Ihrer Konfigurationseinstellungen für den E-Mail-Kanal festlegen. [Weitere Informationen](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **Entscheidungsfindung** (Verfügbarkeitsdatum: 28. Januar 2025): Bei der Entscheidungsfindung werden nun Objektdatentypen beim Bearbeiten des Schemas des Elementkatalogs unterstützt. [Weitere Informationen](../experience-decisioning/catalogs.md)

