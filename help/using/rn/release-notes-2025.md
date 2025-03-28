---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise 2025
description: Versionshinweise zu Journey Optimizer 2025
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: e80554570d62d1ddb52516366be55711387c5d19
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 89%

---

# Versionshinweise 2025 {#release-notes-2025}

Auf dieser Seite sind alle Funktionen und Verbesserungen für [!DNL Journey Optimizer] aufgeführt, die im Jahr 2025 veröffentlicht wurden.

## Februar 2025 – Versionshinweise {#25-02-rn}

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
<li> Erstellen Sie Journey-Regelsätze, um Profileintritte in Journeys zu steuern. Schränken Sie etwa ein, wie oft ein Profil innerhalb eines bestimmten Zeitraums auf eine Journey zugreifen kann oder für wie viele Journeys ein Profil gleichzeitig registriert sein kann. Wenden Sie diese Regeln auf der Journey-Ebene an, um eine ordnungsgemäße Eintrittsverwaltung sicherzustellen.</li></ul></p>
<p>Bislang für eine Reihe von Organisationen (LA) verfügbar, stehen Geschäftsregeln jetzt für alle Benutzer (GA) zur Verfügung. Geschäftsregeln für Journey-Domains sind weiterhin nur für eine begrenzte Anzahl von Organisationen verfügbar.</p>
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
<p>Sie können jetzt eine benutzerdefinierte Aktionskonfiguration überprüfen, indem Sie echte API-Aufrufe direkt aus Adobe Journey Optimizer durchführen. Diese neue Funktion hilft Ihnen bei der Fehlerbehebung bei benutzerdefinierten Aktionen, bevor oder nachdem diese auf einer Journey verwendet werden. </p>
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

