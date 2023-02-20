---
solution: Journey Optimizer
product: journey optimizer
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: f07a46e6fc42afb80275557dfe8bd27f51e4fad9
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 59%

---

# Versionshinweise {#release-notes}

[!DNL Adobe Journey Optimizer] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in der letzten Woche jedes Monats in diesen Versionshinweisen konsolidiert.

Frühere Versionshinweise finden Sie auf [dieser Seite](release-notes-2022.md). Auf der Seite [Letzte Dokumentations-Updates](documentation-updates.md) finden Sie weitere Änderungsmöglichkeiten.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.


## Frühzeitige Versionshinweise im Februar 2023 {#feb-2023}

Dieser Abschnitt enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden. Detaillierte Dokumentationen finden Sie am Releasedatum.

Verfügbarkeit: **22. Februar 2023**

### Verbesserungen {#feb-2023-improvements}

**Journeys**

* Die **Wartezeit beim erneuten Eintritt** wurde zu den Journey-Eigenschaften hinzugefügt. In diesem Feld können Sie die Wartezeit definieren, bevor Sie einem Profil erlauben, die Journey erneut in einheitlichen Journey zu betreten (beginnend mit einer Ereignis- oder Segmentqualifikation). Dadurch wird verhindert, dass Journey fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Standardmäßig ist das Feld auf 5 Minuten eingestellt.

* Es wurden Verbesserungen für **Start- und Enddatum der Journey**. Wenn Sie kein Startdatum angegeben haben, wird es jetzt automatisch zum Veröffentlichungszeitpunkt hinzugefügt. Für **Segment lesen** Journey können Sie jetzt ein Enddatum hinzufügen. Dadurch können Profile beim Erreichen des Datums automatisch die Journey verlassen.

* Die Journey-Arbeitsfläche wurde verbessert, um das Benutzererlebnis zu vereinfachen und zu verbessern. Am Ende jedes Pfads auf der Arbeitsfläche wurden die leeren Platzhalter entfernt. Jetzt können Sie Ihre Aktivitäten einfach hinzufügen, indem Sie sie an eine beliebige Stelle zwischen Knoten ziehen.

* Die Verwaltung von Zeitüberschreitung und Fehlern wurde in Journey verbessert. Timeout- und Fehlerpfade werden jetzt immer auf der Arbeitsfläche hinzugefügt. Eine neue Symbolleistenschaltfläche ist verfügbar, um diese Pfade ein-/auszublenden.

* Eine neue Art von Systemwarnung wurde eingeführt. Sie können jetzt benachrichtigt werden, wenn eine benutzerdefinierte Aktion fehlschlägt.


**Administration**

* **Zulassungsliste** - Sie können die Zulassungsliste jetzt als CSV-Datei herunterladen.

* **E-Mail-Oberfläche** - Eine zusätzliche Prüfung wurde zu den E-Mail-Oberflächeneinstellungen hinzugefügt: , wenn der MX-Datensatz für die in der **Antwortadresse (E-Mail)** oder in **BCC-E-Mail-Adresse** nicht ordnungsgemäß konfiguriert ist, kann die E-Mail-Oberfläche nicht mehr erstellt werden. Sie müssen sie konfigurieren lassen oder eine andere verwenden.

* **E-Mail-Oberfläche** - Im Bereich URL-Tracking-Parameter der E-Mail-Oberflächeneinstellungen ist die Begrenzung für jede **Wert** -Feld wurde aus Gründen der Kompatibilität mit Adobe Analytics-Tracking von 255 Zeichen auf 5 KB aktualisiert.

**Entscheidungs-Management**

* **Praktika** - Im Bildschirm zur Erstellung von Platzierungen wurden zusätzliche Parameter hinzugefügt. Sie ermöglichen es Ihnen zu steuern, ob ein Angebot über mehrere Platzierungen hinweg dupliziert werden kann, und anzugeben, ob der Inhalt und die Metadaten des Angebots in die API-Antwort aufgenommen werden sollen.

* **URL-Personalisierung** - Beim Hinzufügen von URLs als Inhalt zu den Darstellungen Ihrer Angebote können Sie diese URLs jetzt mit dem Ausdruckseditor personalisieren.



## Version Januar 2023 {#jan-2023-release}

### Neue Funktionen{#jan-2023-features}


<table>
<thead>
<tr>
<th><strong>Datenhygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform bietet eine Reihe von Funktionen zur Datenhygiene, mit denen Sie Ihre gespeicherten Daten durch programmgesteuerte Löschungen der Aufzeichnungen und Datensätze von Kundinnen und Kunden verwalten können. Diese Funktion ist jetzt für Adobe Journey Optimizer verfügbar. </p>
<p>Sie können Ihre Datenspeicher verwalten, um sicherzustellen, dass Informationen erwartungsgemäß verwendet werden, dass sie aktualisiert werden, wenn falsche Daten korrigiert werden müssen, und dass sie gelöscht werden, wenn dies aufgrund von Richtlinien der Organisation erforderlich ist.</p>
<p><strong>Achtung</strong> – Die Funktionen zur Datenhygiene stehen derzeit nur Organisationen zur Verfügung, die die Zusatzangebote <strong>Healthcare Shield</strong> und <strong>Privacy and Security Shield</strong> erworben haben.</p><p>Weitere Informationen finden Sie in der <a href="../privacy/data-hygiene.md">ausführlichen Dokumentation</a>.

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>E-Mail-Inhaltsvorlagen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt eigenständige Inhaltsvorlagen erstellen, die schnell in Journeys und Kampagnen wiederverwendet werden können.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>Wie Sie Inhaltsvorlagen erstellen, bearbeiten und verwenden, erfahren Sie in <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html?lang=de">diesem Video</a>. Weitere Informationen finden Sie in der <a href="../email/content-templates.md">ausführlichen Dokumentation</a>.
</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#jan-2023-improvements}

**Journeys**

<!--
* The **Re-entrance wait period** field has been added to the journey properties. This field allows you to define the time to wait before allowing a profile to enter the journey again in unitary journeys (starting with an event or a segment qualification). This prevents journeys from being erroneously triggered multiple times for the same event. By default the field is set to 5 minutes. [Learn more](../building-journeys/journey-gs.md#entrance)

* Improvements have been made for **journey start and end dates**. If you have not specified a start date, it is now automatically added at publication time. For **Read segment** journeys, you can now add an end date. This allows profiles to exit automatically when the date is reached. [Learn more](../building-journeys/journey-gs.md#dates)
-->

* Beim Hinzufügen von **Segmentqualifizierung** oder **Segment lesen** in einer Journey ist der Namespace jetzt standardmäßig mit dem zuletzt verwendeten Namespace vorausgefüllt. Siehe dazu die Abschnitte [Segmentqualifizierung](../building-journeys/segment-qualification-events.md#about-segment-qualification) und [Segment lesen](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Auf der Journey-Arbeitsfläche ist eine neue Schaltfläche in der Symbolleiste verfügbar, mit der Sie einen Screenshot Ihrer Journey herunterladen können.

**E-Mail-Designer**

* Sie können jetzt über das Menü **HTML exportieren** den E-Mail-Inhalt exportieren. Exportierte Dateien sind in einer ZIP-Archivdatei verfügbar.

**Administration**

* Ein neuer Unterabschnitt enthält Empfehlungen zum Erstellen der Adresse für **Antwort an (E-Mail)** und gewährleistet eine ordnungsgemäße Antwortverwaltung. [Weitere Informationen](../email/email-settings.md#reply-to-email)

* Beim Erstellen oder Bearbeiten von **IP-Pools** werden die zugehörigen PTR-Einträge jetzt in der IP-Liste angezeigt, und ebenfalls, wenn Sie den Mauszeiger über die ausgewählten IP-Adressen bewegen. [Weitere Informationen](../configuration/ip-pools.md#create-ip-pool)

* Nachdem ein IP-Pool auf einer Kanaloberfläche ausgewählt wurde, sind jetzt Informationen zum PTR-Eintrag sichtbar, wenn Sie den Mauszeiger über die IP-Adressen bewegen. [Weitere Informationen](../email/email-settings.md#subdomains-and-ip-pools)

* Die Benutzeroberfläche zur Bearbeitung von [PTR-Einträgen](../configuration/ptr-records.md#edit-ptr-record) und [Ausführungsfeldern](../configuration/primary-email-addresses.md) wurde aktualisiert.

* Die Benutzeroberfläche zum Erstellen und Bearbeiten von Subdomains wurde verbessert. [Weitere Informationen](../configuration/delegate-subdomain.md)

* Der Bildschirm **Letzte Uploads** der Unterdrückungsliste wurde aktualisiert. [Weitere Informationen](../configuration/manage-suppression-list.md#recent-uploads)

**Kampagnen**

* Eine Beispiel-cURL-Anfrage, die die Ausführung API-ausgelöster Kampagnen ermöglicht, wird jetzt automatisch generiert und im Kampagnenbildschirm bereitgestellt. [Weitere Informationen](../campaigns/api-triggered-campaigns.md)

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**Personalisierung**

* Neue Hilfsfunktionen sind verfügbar: formatCurrency, charCodeAt, stringToDate, toString, formatNumber und toHexString. Darüber hinaus akzeptiert die Funktion toDateTimeOnly jetzt die Feldtypen string, date, long und int. [Weitere Informationen](../personalization/functions/functions.md)
