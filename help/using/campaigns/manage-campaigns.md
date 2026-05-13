---
solution: Journey Optimizer
product: journey optimizer
title: Zugreifen auf und Verwalten von Kampagnen
description: Erfahren Sie, wie Sie in Journey Optimizer auf Ihre Kampagnen zugreifen und diese verwalten können.
feature: Campaigns
topic: Content Management
role: User
mini-toc-levels: 1
level: Beginner
keywords: Verwalten von Kampagnen, Status, Zeitplan, Zugriff, Optimizer
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
TQID: https://experienceleague.adobe.com/k-BZOO4BOzdW2TVlBrDx1CH-Wte7KEXffXqZYRvUI7w
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d556b755-390a-43f0-be32-a08cf6236126id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: d2e8a157-b3b0-4143-9ff3-809bf400be56id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 1692
ht-degree: 0%

---

# Zugreifen auf und Verwalten von Kampagnen {#manage-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Orchestrierte Inventarkampagnen"
>abstract="Auf diesem Bildschirm können Sie auf die vollständige Liste der orchestrierten Kampagnen zugreifen, ihren aktuellen Status und das letzte/nächste Ausführungsdatum überprüfen und eine neue orchestrierte Kampagne erstellen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="Aktion"
>abstract="In diesem Abschnitt werden alle in der orchestrierten Kampagne verwendeten Aktionen aufgelistet."

Erfahren Sie, wie Sie in Adobe Journey Optimizer auf Kampagnen zugreifen und diese organisieren und verwalten können. Dieses Handbuch behandelt alle Themen, von der Suche nach Kampagnen über das Verstehen von Status, die Durchführung allgemeiner Vorgänge bis hin zur Pflege des Kampagnenarbeitsbereichs.

>[!BEGINSHADEBOX]

**Springen Sie direkt zu dem, was Sie benötigen:**

* **Neue Kampagne erstellen** - [Kampagnentyp wählen](get-started-with-campaigns.md#campaign-types) | [Aktionskampagne erstellen](create-campaign.md) | [API-ausgelöste Kampagne erstellen](api-triggered-campaigns.md) | [Orchestrierte Kampagne erstellen](../orchestrated/gs-orchestrated-campaigns.md)
* **Vorhandene Kampagnen suchen** - [Suchen und Filtern](#access)
* **Anzeigen der Kampagnenleistung** - [Kampagnenberichte](../reports/campaign-global-report-cja.md)
* **Kampagnen planen** - [Kalender verwenden](#calendar)
* **Konflikte verwalten** - [Handbuch für das Konfliktmanagement](../conflict-prioritization/gs-conflict-prioritization.md)

>[!ENDSHADEBOX]

## Zugreifen auf und Durchsuchen von Kampagnen {#access}

Auf Kampagnen kann über das Menü **[!UICONTROL Kampagnen]** zugegriffen werden. Verwenden Sie die Registerkarten, um Kampagnen nach Typ zu durchsuchen: **Aktion** Kampagnen, **API-ausgelöst** Kampagnen und **orchestrierte** Kampagnen. Erfahren Sie mehr über [Kampagnentypen](get-started-with-campaigns.md#campaign-types). Die verfügbaren Typen hängen von Ihrer Lizenzvereinbarung und Ihren Berechtigungen ab.

>[!BEGINTABS]

>[!TAB Aktionskampagnen]

Wählen Sie die **[!UICONTROL Aktion]** aus, um auf die Liste der Aktionskampagnen zuzugreifen.

Standardmäßig werden in der Liste alle Kampagnen mit dem Status **[!UICONTROL Entwurf]**, **[!UICONTROL Geplant]** und **[!UICONTROL Live]** angezeigt. Um gestoppte, abgeschlossene und archivierte Kampagnen anzuzeigen, müssen Sie den Filter löschen.

![](assets/create-campaign-list.png)

>[!TAB API-ausgelöste Kampagnen]

Wählen Sie die Registerkarte **[!UICONTROL API-ausgelöst]**, um auf die Liste der von einer API ausgelösten Kampagnen zuzugreifen.

Standardmäßig werden in der Liste alle Kampagnen mit dem Status **[!UICONTROL Entwurf]**, **[!UICONTROL Geplant]** und **[!UICONTROL Live]** angezeigt. Um gestoppte, abgeschlossene und archivierte Kampagnen anzuzeigen, müssen Sie den Filter löschen.

![](assets/api-triggered-list.png)

>[!TAB Orchestrierte Kampagnen]

Wählen Sie die **[!UICONTROL Orchestrierung]**, um auf die Liste der orchestrierten Kampagnen zuzugreifen.

![Bild mit dem Inventar der orchestrierten Kampagnen](assets/inventory.png){zoomable="yes"}

Jede orchestrierte Kampagne in der Liste zeigt Informationen wie den aktuellen (Status[ der Kampagne, ](#statuses) zugehörigen Kanal und Tags oder das letzte Mal, wann sie geändert wurde, an. Sie können die angezeigten Spalten anpassen, indem Sie auf die Schaltfläche ![Layout konfigurieren](assets/do-not-localize/inventory-configure-layout.svg) klicken.

>[!ENDTABS]

### Kampagnen durchsuchen und filtern {#search-filter}

Darüber hinaus stehen eine Suchleiste und Filter zur Verfügung, um die Suche innerhalb der Liste zu erleichtern. Sie können beispielsweise Kampagnen so filtern, dass nur die mit einem bestimmten Kanal oder Tag verknüpften oder die in einem bestimmten Datumsbereich erstellten Kampagnen angezeigt werden.

## Vorgänge in Campaign {#operations}

Die ![Abbildung mit der Schaltfläche Mehr Aktionen](assets/do-not-localize/rule-builder-icon-more.svg) im Kampagneninventar ermöglicht die Durchführung verschiedener Vorgänge.

![Bild mit dem Kampagneninventar](assets/inventory-actions.png)

### Verfügbare Aktionen

**Für alle Kampagnentypen:**

* **[!UICONTROL Alle Zeitberichte anzeigen]**/**[!UICONTROL Bericht zu letzten 24 Stunden anzeigen]** - Greifen Sie auf Berichte zu, um die Wirkung und Leistung Ihrer Kampagnen zu messen und zu visualisieren. [Erfahren Sie mehr über Kampagnenberichte →](../reports/campaign-global-report-cja.md)
* **[!UICONTROL Tags bearbeiten]** - Bearbeiten Sie die mit der Kampagne verknüpften Tags. [Erfahren Sie, wie Sie Tags-→ verwenden](../start/search-filter-categorize.md#add-tags)
* **[!UICONTROL Duplizieren]** - Mit dieser Option können Sie eine Kampagne duplizieren, z. B. um eine gestoppte orchestrierte Kampagne auszuführen. [Weitere Informationen zum Duplizieren von →](#duplicate-a-campaign)
* **[!UICONTROL Löschen]** - Verwenden Sie diese Option, um eine Kampagne zu löschen. [Weitere Informationen zum Löschen von →](#delete-a-campaign)
* **[!UICONTROL Archivieren]** - Archivieren Sie die Kampagne. Alle archivierten Kampagnen werden rollierend 30 Tage nach dem Datum ihrer letzten Änderung gelöscht. Diese Aktion steht für alle Kampagnen mit Ausnahme von Kampagnen **[!UICONTROL Entwurf]** zur Verfügung. [Erfahren Sie mehr über → Archivierung](#archive-a-campaign)

**Nur für von Aktionen und API ausgelöste Kampagnen:**

* **[!UICONTROL Zu Paket hinzufügen]** - Fügen Sie die Kampagne zu einem Paket hinzu, um sie in eine andere Sandbox zu exportieren. [Erfahren Sie, wie Sie Objekte → exportieren](../configuration/copy-objects-to-sandbox.md)
* **[!UICONTROL Entwurfsversion öffnen]** - Wenn eine neue Version der Kampagne erstellt wurde und noch nicht aktiviert wurde, können Sie mit dieser Aktion auf ihre Entwurfsversion zugreifen.

**Nur für orchestrierte Kampagnen:**

* **[!UICONTROL Zurück zum Entwurf]** - Rückgängigmachen der Veröffentlichung und Zurücksetzen einer Kampagne in den Entwurfsstatus zur Fehlerbehebung. Diese Aktion ist verfügbar, wenn eine geplante Kampagne noch nicht gestartet wurde oder wenn bei einer Live-Kampagne ein Fehler auftritt, bevor irgendwelche Ausführungen abgeschlossen sind. [Erfahren Sie mehr über das Zurücksetzen von Kampagnen →](../orchestrated/start-monitor-campaigns.md#back-to-draft)

## Kampagnenstatus {#statuses}

Jede Kampagne durchläuft einen Lebenszyklus, der sich in ihrem Status in der Benutzeroberfläche widerspiegelt. Wenn Sie diese Status verstehen, können Sie feststellen, welche Aktionen verfügbar sind und was als Nächstes zu tun ist.

| Status | Aktionskampagnen | API-ausgelöste Kampagnen | Orchestrierte Kampagnen | Was es bedeutet | Nächste Aktionen |
|--------|:----------------:|:-----------------------:|:----------------------:|---------------|--------------|
| **[!UICONTROL Entwurf]** | ✅ | ✅ | ✅ | In Bearbeitung, nicht aktiviert | Bearbeitung fortsetzen oder [Kampagne aktivieren](review-activate-campaign.md) |
| **[!UICONTROL Geplant]** | ✅ | ✅ | ✅ | Für bestimmtes Startdatum konfiguriert | Auf Launch warten, [bei Bedarf ändern](#modify) oder [im Kalender anzeigen](#calendar) |
| **[!UICONTROL Live]** | ✅ | ✅ | ✅ | Aktiviert und ausgeführt | [Überwachen der Leistung](../reports/campaign-global-report-cja.md), [Erstellen einer neuen Version](#modify) falls erforderlich. Für orchestrierte Kampagnen: [Zurück zum Entwurf](../orchestrated/start-monitor-campaigns.md#back-to-draft) für geplante Kampagnen, die noch nicht gestartet wurden, oder für Kampagnen mit Ausführungsfehlern, bevor Nachrichten gesendet werden |
| **[!UICONTROL Wird geprüft]** | ✅ | ✅ | — | Zur Genehmigung eingereicht | Warten auf [Genehmigung](../test-approve/gs-approval.md) oder ändern |
| **[!UICONTROL Angehalten]** | ✅ | ✅ | ✅ | Manuell angehalten, kann nicht reaktiviert werden | [Duplizieren zur Wiederverwendung](#duplicate-a-campaign) |
| **[!UICONTROL Abgeschlossen]** | ✅ | ✅ | ✅ | Ausführung abgeschlossen (wird 3 Tage nach Aktivierung automatisch zugewiesen oder endet bei wiederkehrender Ausführung am Enddatum) | [Anzeigen von Berichten](../reports/campaign-global-report-cja.md), [Archivieren](#archive-a-campaign) oder [Duplizieren](#duplicate-a-campaign) |
| **[!UICONTROL fehlgeschlagen]** | ✅ | ✅ | — | Ausführung fehlgeschlagen | Überprüfen Sie Protokolle, beheben Sie Probleme [Duplizieren Sie es erneut](#duplicate-a-campaign) |
| **[!UICONTROL Archiviert]** | ✅ | ✅ | ✅ | Archiviert (nach 30 Tagen automatisch gelöscht) | [Bei ](#access) mit Filter abrufen |
| **[!UICONTROL Geschlossen]** | — | — | ✅ | Wiederkehrende Kampagne geschlossen, keine neuen Einträge zulässig (wird fortgesetzt, bis alle Aktivitäten abgeschlossen sind) | Auf Abschluss warten |
| **[!UICONTROL Veröffentlichen]** | — | — | ✅ | In Veröffentlichung | Warten, bis die Veröffentlichung abgeschlossen ist |

>[!NOTE]
>
>Bei durch eine Aktion oder API ausgelösten Kampagnen zeigt das Symbol „Entwurfsversion öffnen“ neben einem Status **[!UICONTROL Live]** oder **[!UICONTROL Geplant]** an, dass eine neue Version erstellt wurde und noch nicht aktiviert wurde.

### Fehlerindikatoren

Wenn in einer Ihrer Kampagnen ein Fehler auftritt, wird neben dem Kampagnenstatus ein Warnsymbol angezeigt. Klicken Sie darauf, um Informationen zum Warnhinweis anzuzeigen. Diese Warnhinweise können in verschiedenen Situationen auftreten, z. B. wenn die Kampagnennachricht nicht veröffentlicht wurde oder wenn die ausgewählte Konfiguration falsch ist.

![](assets/campaign-alerts.png)

>[!NOTE]
>
>Assets/Images sind in bereitgestellten Inhalten für bis zu 2 Jahre (730 Tage) seit ihrer ersten Veröffentlichung in einem Fragment/einer Inline-Nachricht verfügbar. Nach Ablauf dieses Zeitraums (jederzeit nach 730 Tagen) ist eine erneute Veröffentlichung erforderlich, um sie für weitere 2 Jahre verfügbar zu halten. Eine erneute Veröffentlichung innerhalb von 730 Tagen nach der ersten Veröffentlichung verlängert den Ablauf der Assets/Bilder nicht auf die nächsten 730 Tage.

## Kampagnenkalender {#calendar}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_view"
>title="Listen- und Kalenderansichten für Kampagnen"
>abstract="Zusätzlich zur Kampagnenliste bietet [!DNL Journey Optimizer] eine Kalenderansicht Ihrer Kampagnen, die eine klare visuelle Darstellung ihrer Zeitpläne bietet. Über diese Schaltflächen können Sie jederzeit zwischen der Listen- und Kalenderansicht wechseln."

Zusätzlich zur Kampagnenliste bietet [!DNL Journey Optimizer] eine Kalenderansicht Ihrer Kampagnen, die eine klare visuelle Darstellung ihrer Zeitpläne bietet.

### Funktionsweise des Kalenders

Darstellung der Kampagnen:

* Standardmäßig zeigt das Kalenderraster alle Live- und geplanten Kampagnen für die ausgewählte Woche an. Zusätzliche Filteroptionen können abgeschlossene, gestoppte und abgeschlossene Aktivierungen oder Aktivierungen eines bestimmten Typs oder Kanals anzeigen.
* Kampagnenentwürfe werden nicht angezeigt.
* Kampagnen, die sich über mehrere Tage erstrecken, werden oben im Kalenderraster angezeigt.
* Wenn keine Startzeit angegeben wird, wird die nächstgelegene manuelle Aktivierungszeit verwendet, um sie im Kalender zu positionieren.
* Kampagnen werden als Zeiträume von 1 Stunde angezeigt, dies spiegelt jedoch nicht die tatsächliche Versand- oder Abschlusszeit wider.

### Navigieren im Kalender

1. Klicken Sie auf ![Kalender](assets/do-not-localize/Smock_Calendar_18_N.svg), um auf Ihren Kampagnenkalender zuzugreifen.

1. Verwenden Sie die Pfeiltasten oder die Datumsauswahl über dem Kalender, um zwischen Wochen zu wechseln.

   Der Kalender zeigt alle für die aktuelle Woche geplanten Kampagnen an.

   ![Kalenderansicht mit Live-Kampagnen](assets/campaigns-timeline.png)

1. Klicken Sie auf ![Zahnradsymbol](assets/do-not-localize/Smock_Gears_18_N.png), um die Anzeige von Elementen umzuschalten, die sich über mehrere Tage oder Wochen erstrecken.

   ![Kalenderansicht mit Live-Kampagnen](assets/campaign-long-term.png)

1. Klicken Sie auf das ![Kalender hinzufügen](assets/do-not-localize/Smock_CalendarAdd_18_N.svg)-Symbol, um bis zu drei externe Kalender zu verwalten und hinzuzufügen.

   ![Kalenderansicht mit externen Kalendern](assets/campaign-external-calendar.png)

1. CSV-Dateien mit Ereignisnamen, Start- und Enddaten per Drag-and-Drop ablegen.

   Hochgeladene Ereignisse werden für alle Benutzenden in Ihrer Organisation angezeigt und sowohl im Journey- als auch im Kampagnenkalender angezeigt.

   +++Das CSV-Format sollte wie folgt lauten:

   | Spalte 1 | Spalte 2 | Spalte 3 |
   |-|-|-|
   | Ereignisname | Startdatum im Format MM/TT/JJ | Enddatum im Format MM/TT/JJ |

   +++

1. Bei Bedarf können Sie hinzugefügte externe Kalender ausblenden, einblenden oder entfernen.

   ![Kalenderansicht mit externen Kalendern](assets/campaign-manage-calendar.png)

1. Um weitere Informationen zu einer Kampagne zu erhalten, klicken Sie auf den entsprechenden visuellen Block, um die entsprechenden Details zu öffnen. Daraufhin wird ein Informationsfenster mit verschiedenen Informationen über die Kampagne geöffnet, z. B. über den Kampagnentyp, den Zugriff auf die Berichte oder die zugewiesenen Tags.

   ![Kampagnenliste mit geöffnetem Informationsbereich](assets/campaign-rail.png)

## Ändern und Beenden wiederkehrender Aktionskampagnen {#modify}

### Ändern einer Aktionskampagne {#modify-an-action-campaign}

Gehen Sie wie folgt vor, um eine wiederkehrende Aktionskampagne zu ändern und eine neue Version zu erstellen:

1. Öffnen Sie die Aktionskampagne und klicken Sie auf die Schaltfläche **[!UICONTROL Kampagne ändern]**.

1. Eine neue Version der Kampagne wird erstellt. Sie können die Live-Version überprüfen, indem Sie auf **[!UICONTROL Live-Version öffnen]** klicken.

   ![](assets/create-campaign-draft.png)

   In der Liste der Kampagnen werden aktivierte Kampagnen, für die eine Entwurfsversion in Bearbeitung ist, mit einem speziellen Symbol in der Spalte **[!UICONTROL Status]** angezeigt. Klicken Sie auf dieses Symbol, um die Entwurfsversion der Kampagne zu öffnen.

   ![](assets/create-campaign-edit-list.png)

1. Sobald Sie mit den Änderungen fertig sind, können Sie die neue Version der Kampagne aktivieren (siehe [Kampagne überprüfen und aktivieren](review-activate-campaign.md)).

   >[!IMPORTANT]
   >
   >Durch die Aktivierung des Entwurfs wird die Live-Version der Kampagne ersetzt.

**Verwandte Themen:**
* [Kampagneneigenschaften](campaign-properties.md)
* [Kampagnenaktionen](campaign-action.md)
* [Kampagneninhalt](campaign-content.md)
* [Campaign-Zielgruppe](campaign-audience.md)
* [Kampagnenzeitplan](campaign-schedule.md)

### Stoppen einer Aktionskampagne {#stop}

Um eine wiederkehrende Kampagne zu stoppen, öffnen Sie sie und klicken Sie auf die Schaltfläche **[!UICONTROL Kampagne stoppen]**.

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>Das Anhalten einer Kampagne stoppt keinen laufenden Versand, aber es stoppt einen geplanten Versand oder die nächsten Vorfälle, wenn der Versand bereits im Gange ist.

## Archivieren einer Kampagne {#archive-a-campaign}

Mit der Zeit wächst die Liste der Kampagnen und erschwert letztendlich das Durchsuchen abgeschlossener und gestoppter Kampagnen.

Um dies zu verhindern, können Sie abgeschlossene und gestoppte Kampagnen archivieren, die Sie nicht mehr benötigen. Klicken Sie dazu auf die Schaltfläche mit den Auslassungspunkten und wählen Sie **[!UICONTROL Archivieren]**.

![](assets/create-campaign-archive.png)

Archivierte Kampagnen können dann mithilfe des entsprechenden Filters in der Liste abgerufen werden.

## Löschen einer Kampagne {#delete-a-campaign}

Um eine Kampagne zu löschen, verwenden Sie die Schaltfläche mit ![ Auslassungspunkten (Bild mit der Schaltfläche Mehr Aktionen](assets/do-not-localize/rule-builder-icon-more.svg) und wählen Sie **[!UICONTROL Löschen]**.

![](assets/delete-a-campaign.png){width="70%" align="left"}

>[!IMPORTANT]
>
>Diese Option ist nur für Kampagnen **[!UICONTROL Entwurf]** verfügbar.

## Duplizieren einer Kampagne {#duplicate-a-campaign}

Um eine Kampagne zu duplizieren (beispielsweise wenn sie gestoppt wurde), verwenden Sie die Schaltfläche mit den ![ (Bild mit der Schaltfläche Mehr Aktionen](assets/do-not-localize/rule-builder-icon-more.svg) und wählen Sie **[!UICONTROL Duplizieren]**.

Geben Sie den Namen der Kampagne ein und bestätigen Sie.

Die Kampagne wird erstellt und der Kampagnenliste hinzugefügt.

## Zusätzliche Ressourcen

* **Erste Schritte** - [Erste Schritte mit Kampagnen](get-started-with-campaigns.md) | [Erstellen Ihrer ersten Aktionskampagne](create-campaign.md) | [Handbuch für API-ausgelöste Kampagnen](api-triggered-campaigns.md) | [Handbuch für orchestrierte Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)

* **Kampagnenkonfiguration** - [Kampagneneigenschaften](campaign-properties.md) | [Kampagnenaktionen und -kanäle](campaign-action.md) | [Kampagneninhaltsdesign](campaign-content.md) | [Kampagnenzielgruppenauswahl](campaign-audience.md) | [Kampagnenplanung](campaign-schedule.md)

* **Erweiterte Funktionen** - [Genehmigungs-Workflows](../test-approve/gs-approval.md) | [Konfliktmanagement und Priorisierung](../conflict-prioritization/gs-conflict-prioritization.md) | [Frequenzlimitierung nach Kanal](../conflict-prioritization/channel-capping.md) | [Prioritätswerte](../conflict-prioritization/priority-scores.md) | [Kampagnen in andere Sandboxes exportieren](../configuration/copy-objects-to-sandbox.md)

* **Überwachung und Optimierung** - [Kampagnenberichte (CJA)](../reports/campaign-global-report-cja.md) | [Warnhinweise einrichten](../reports/alerts.md)

* **Organisation** - [Arbeiten mit Tags](../start/search-filter-categorize.md) | [Berechtigungen verwalten](../administration/ootb-product-profiles.md)
