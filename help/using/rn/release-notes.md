---
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 8766f64c4ea7985c6c9d6e4ba022ef6b1fc0dbed
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 86%

---

# Versionshinweise {#release-notes}

Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für [!DNL Journey Optimizer] aufgelistet. Auf der Seite [Letzte Dokumentations-Updates](documentation-updates.md) finden Sie weitere Änderungsmöglichkeiten.

[!DNL Adobe Journey Optimizer] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Registrieren Sie sich noch heute für den [vierteljährlichen Adobe Journey Optimizer-Newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}, um jedes Quartal die neuesten Produktaktualisierungen, spannende Geschichten, Anwendungsbeispiele, Tipps und vieles mehr direkt in Ihrem Posteingang zu erhalten.

## Version Juli 2022 {#july-2022-release}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Neuer Fluss für Inline-Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer bietet einen neuen Fluss für die Nachrichtenbearbeitung in Journeys. Das Inline-Messaging spart Benutzenden viel Zeit und optimiert den Workflow-Prozess zum Erstellen und Versand einer E-Mail, einer Push-Benachrichtigung oder einer SMS in Journey Optimizer. Wenn Sie Nachrichten als separaten Schritt entfernen und sie stattdessen im Rahmen einer Journey-Arbeitsfläche bearbeitbar machen möchten, müssen Benutzende auf weniger Schaltflächen klicken und durch weniger Bildschirme navigieren, um Inhalte zu entwerfen und zu bearbeiten.</p>
<img src="assets/do-not-localize/inline.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../messages/get-started-content.md">detaillierten Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Attributbasierte Zugriffssteuerung (begrenzte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Schemafelder mit Bezeichnungen identifizieren, die Organisations- oder Datennutzungsbereiche definieren. Admins können über die Benutzeroberfläche „Berechtigungen“ Zugriffsrichtlinien für XDM-Schemafelder definieren und den Zugriff für Benutzende oder Benutzergruppen (interne, externe oder Drittbenutzende) besser verwalten sowie den Zugriff auf bestimmte Datentypen (d. h. sensible personenbezogene Daten/SPD) verwalten.</p>
<p>Die Verwendung der attributbasierten Zugriffssteuerung ist derzeit auf ausgewählte Benutzende beschränkt und wird in einer zukünftigen Version für alle Umgebungen bereitgestellt.</p>
<p>Weitere Informationen finden Sie in der <a href="../administration/attribute-based-access.md">detaillierten Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Batch-Entscheidungsaufträge</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Batch-Entscheidungsaufträge über die Benutzeroberfläche ausführen, sodass niemand mit Entwicklungskenntnissen benötigt wird, um Batch-API-Aufträge auszuführen, und die für das Marketing benötigte Zeit verkürzt wird. Mit dieser neuen Benutzeroberfläche können Sie Aufträge erstellen und aktuelle/frühere Aufträge verwalten.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../offers/batch-delivery.md">detaillierten Dokumentation.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Automatisches Verwenden des Angebots mit der besten Leistung bei Ihren Entscheidungen (begrenzte Verfügbarkeit)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt personalisierte Optimierungsmodellsysteme im Entscheidungs-Management verwenden. Dieser neue Modelltyp ermöglicht die Optimierung und Personalisierung von Angeboten basierend auf Segmenten und der Angebotsleistung.</p>
<p>Die Verwendung personalisierter KI-Modelle zur Optimierung ist derzeit auf ausgewählte Benutzende beschränkt und wird in einer zukünftigen Version in allen Umgebungen bereitgestellt.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Weitere Informationen finden Sie in der <a href="../offers/ranking/personalized-optimization-model.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journeys**

* **Beenden einer Journey** - Auf der Journey-Arbeitsfläche **Ende** -Aktivität wurde aus der Palette entfernt. End-Tags werden jetzt standardmäßig am Ende jedes Pfades hinzugefügt und können nicht entfernt werden. Diese Verbesserung ermöglicht eine bessere Berichterstellung darüber, wo ein Kunde von der Journey ausgeschlossen wurde, ohne dass der Journey-Anwender Maßnahmen ergreifen muss. Siehe Abschnitt [Dokumentation](../building-journeys/journey-end.md) und [Feature Video](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}.

**Nachrichten**

* Nachrichtenvoreinstellungen sind jetzt **Kanaloberflächen**. [Weitere Informationen](../configuration/channel-surfaces.md)

**Administration**

* **Bearbeitung von PTR-Einträgen**: Beim Aktualisieren eines PTR-Eintrags dauert die Verarbeitungszeit nur bis zu 3 Stunden. [Weitere Informationen](../configuration/ptr-records.md#processing)

* **Zulassungsliste per Benutzeroberfläche**: Sie können jetzt die Journey Optimizer-Benutzeroberfläche verwenden, um neue E-Mail-Adressen oder Domains zur Zulassungsliste hinzuzufügen. [Weitere Informationen](../configuration/allow-list.md)

* **Aktualisierung der Zulassungslistenlogik**: Die Logik der Zulassungsliste gilt nun, sobald die Funktion aktiviert ist, selbst wenn die Liste leer ist. [Weitere Informationen](../configuration/allow-list.md#logic)

* **URL-Tracking-Parameter** - Sie können jetzt den Ausdruckseditor verwenden, um URL-Tracking-Parameter auf Ihren E-Mail-Oberflächen (d. h. Vorgaben) zu konfigurieren. [Weitere Informationen](../configuration/email-settings.md#url-tracking)

**Offer Decisioning**

* **Zielgruppengröße**: In der Benutzeroberfläche wird jetzt eine neue Schätzung der Zielgruppengröße angezeigt, wenn eine Entscheidungsregel erstellt wird, ein Segment oder eine Regel zum Festlegen einer Angebotseignung ausgewählt wird oder ein Segment oder eine Regel zu einem Entscheidungsbereich hinzugefügt wird.