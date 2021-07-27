---
title: Versionshinweise
description: Versionshinweise zu Journey Optimizer
source-git-commit: 0fb6d8f611a849696d83e0f129e6462431e5fe83
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 43%

---


# Versionshinweise {#release-notes}

Auf dieser Seite werden alle neuen Funktionen und Verbesserungen bei Journey Optimizer aufgelistet.
Sie können auch die neusten [Aktualisierungen der Dokumentation](documentation-updates.md) einsehen.

## Version Juli 2021 {#july-2021-release}

<table>
<thead>
<tr>
<th><strong>Nutzen von Schemabeziehungen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit Adobe Experience Platform können Sie Beziehungen zwischen Schemas definieren, um einen Datensatz als Lookup-Tabelle für einen anderen zu verwenden. Journey Optimizer kann jetzt Daten aus einem verknüpften Schema nutzen.</p>
<p>Diese Felder sind in der Konfiguration von Einzelereignissen, Journey-Bedingungen, der Nachrichtenpersonalisierung und der Personalisierung benutzerdefinierter Aktionen verfügbar.
<p>Weitere Informationen finden Sie in der <a href="event/experience-event-schema.md#leverage_schema_relationships">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

* Die Gesamtdrosselungsrate aller Lesesegmente, die gleichzeitig in derselben Sandbox ausgeführt werden, ist auf 17.000 Nachrichten pro Sekunde beschränkt. [Mehr dazu](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Das Feld **Cache-Dauer** wurde aus dem Konfigurationsbereich der Datenquelle entfernt. [Mehr dazu](datasource/about-data-sources.md)
* Für externe Datenquellen wird jetzt automatisch eine Begrenzungsregel von 15 Aufrufen pro Sekunde festgelegt. [Mehr dazu](configuration/external-systems.md#capping)
* Bei Live-Journeys zeigt der Journey-Eigenschaftenbildschirm jetzt das Veröffentlichungsdatum und den Namen des Benutzers an, der die Journey veröffentlicht hat. [Mehr dazu](building-journeys/journey-gs.md#change-properties)
* Auf dem Bildschirm mit der Journey-Liste wurde der Filter vom Typ Journey hinzugefügt. [Mehr dazu](user-interface.md#section_lgm_hpz_pgb)
* Der Parameter [!UICONTROL Einschränkungsrate] wurde in der Aktivität Segment lesen hinzugefügt. [Mehr dazu](building-journeys/read-segment.md#configuring-segment-trigger-activity)
