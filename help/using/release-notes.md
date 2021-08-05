---
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
source-git-commit: a1800c333bfbee178682d773c729aad7e23d86d0
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 37%

---


# Versionshinweise {#release-notes}

Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für [!DNL Journey Optimizer] aufgelistet. Sie können auch die neusten [Aktualisierungen der Dokumentation](documentation-updates.md) einsehen.

## Version Juli 2021 {#july-2021-release}

<table>
<thead>
<tr>
<th><strong>Verwenden von Schemabeziehungen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Adobe Experience Platform können Sie Beziehungen zwischen Schemas definieren, um einen Datensatz als Lookup-Tabelle für einen anderen zu verwenden. [!DNL Journey Optimizer] kann jetzt Daten aus einem verknüpften Schema nutzen.</p>
<p>Diese Felder sind in der Konfiguration von Einzelereignissen, Journey-Bedingungen, der Nachrichtenpersonalisierung und der Personalisierung benutzerdefinierter Aktionen verfügbar.</p>
<p>Weitere Informationen finden Sie in der <a href="event/experience-event-schema.md#leverage_schema_relationships">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Zulassungsliste</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt eine spezifische Liste für den Versand auf Sandbox-Ebene definieren, um eine sichere Umgebung für Testzwecke zu erhalten. Auf einer Nicht-Produktionsinstanz, bei der Fehler auftreten können, stellt die Zulassungsliste sicher, dass Sie kein Risiko haben, unerwünschte Nachrichten an Ihre Kunden zu senden. Diese Funktion wird durch die Verwendung von Unterdrückungs-APIs aktiviert.</p>
<p>Weitere Informationen finden Sie in der <a href="allow-list.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Journeys**

* Die Gesamtdrosselungsrate aller Lesesegmente, die gleichzeitig in derselben Sandbox ausgeführt werden, ist auf 17.000 Nachrichten pro Sekunde beschränkt. [Mehr dazu](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Das Feld **Aufbewahrungsfrist im Cache** wurde aus dem Konfigurationsbereich der Datenquelle entfernt. [Mehr dazu](datasource/about-data-sources.md)
* Für externe Datenquellen ist jetzt automatisch eine Begrenzungsregel von 15 Aufrufen pro Sekunde definiert. [Mehr dazu](configuration/external-systems.md#capping)
* Für Live-Journeys werden im Journey-Eigenschaftsfenster das Veröffentlichungsdatum und der Name des Benutzers angezeigt, der die Journey veröffentlicht hat. [Mehr dazu](building-journeys/journey-gs.md#change-properties)
* Im Journey-Listenfenster wurde ein Filter für den Journey-Typ hinzugefügt. [Mehr dazu](user-interface.md#section_lgm_hpz_pgb)
* Der Parameter **[!UICONTROL Einschränkungsrate]** wurde in der Aktivität Segment lesen hinzugefügt. [Mehr dazu](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Vorschau erstellen und Nachrichten testen**

* Identität und Namespace sind nun im Bildschirm **[!UICONTROL Vorschau]** sichtbar. [Mehr dazu](preview.md#preview-your-messages)
* Die Anzahl der Test-E-Mails für Testsendungen ist jetzt auf 10 beschränkt.
* Die für das Betreffpräfix **Betreff** in Testsendungen zulässigen Zeichen sind jetzt begrenzt. [Mehr dazu](preview.md#send-proofs)

**Ausdruckseditor für Personalisierung**

* Die Dropdownliste &quot;Helper&quot;wurde umbenannt und neu angeordnet.

### Fehlerbehebungen

* Fehlerkorrektur - Jetzt werden keine doppelten Nachrichten mehr für den Batch-E-Mail-Versand gesendet.
* Ereignisse werden jetzt entsprechend generiert, wenn nach Ablauf des Wiederholungszeitraums kein E-Mail-Versand mehr durchgeführt wird.
* Es wurde ein Problem behoben, bei dem IP-Informationen im Bildschirm &quot;PTR-Datensätze&quot;fehlten.
* Die Lokalisierung in der Angebotsleiste im Ausdruckseditor ist jetzt implementiert.
* Es wurde ein falscher Abstand in Informations-Popups korrigiert.
* Fehlerkorrektur - Beim Hochladen einer HTML-Datei in Email Designer wird jetzt das interne Stylesheet mit der Eigenschaft `background-image` unterstützt.

