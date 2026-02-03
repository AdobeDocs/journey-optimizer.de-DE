---
solution: Journey Optimizer
product: journey optimizer
title: Aufrufen und Verwalten von Kampagnen
description: Informationen zum Zugreifen auf und Verwalten von Kampagnen in Journey Optimizer.
feature: Campaigns
topic: Content Management
role: User
mini-toc-levels: 1
level: Beginner
keywords: Verwalten von Kampagnen, Status, Zeitplan, Zugriff, Optimizer
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 478bd6df8a82c9e37ec9319dedb27d99c021ee99
workflow-type: tm+mt
source-wordcount: '1682'
ht-degree: 95%

---

# Aufrufen und Verwalten von Kampagnen {#manage-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Inventar der orchestrierten Kampagnen"
>abstract="Auf diesem Bildschirm können Sie auf die vollständige Liste der orchestrierten Kampagnen zugreifen, ihren aktuellen Status sowie das Datum der letzten/nächsten Ausführung überprüfen und eine neue orchestrierte Kampagne erstellen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="Aktion"
>abstract="In diesem Abschnitt werden alle in der orchestrierten Kampagne verwendeten Aktionen aufgelistet."

Weitere Informationen zum Aufrufen, Organisieren und Verwalten von Kampagnen in Adobe Journey Optimizer. Dieser Leitfaden behandelt viele Themen, von der Suche nach Kampagnen über das Verstehen von Status, die Durchführung allgemeiner Vorgänge bis hin zur Pflege des Kampagnenarbeitsbereichs.

>[!BEGINSHADEBOX]

**Rufen Sie direkt das gewünschte Thema auf:**

* **Erstellen einer neuen Kampagne** – [Auswählen des Kampagnentyps](get-started-with-campaigns.md#campaign-types) | [Erstellen einer Aktionskampagne](create-campaign.md) | [Erstellen einer API-ausgelösten Kampagne](api-triggered-campaigns.md) | [Erstellen einer orchestrierten Kampagne](../orchestrated/gs-orchestrated-campaigns.md)
* **Suchen vorhandener Kampagnen** – [Suchen und Filtern](#access)
* **Anzeigen der Kampagnenleistung** – [Kampagnenberichte](../reports/campaign-global-report-cja.md)
* **Planen von Kampagnen** – [Verwenden des Kalenders](#calendar)
* **Verwalten von Konflikten** – [Leitfaden für das Konflikt-Management](../conflict-prioritization/gs-conflict-prioritization.md)

>[!ENDSHADEBOX]

## Aufrufen und Durchsuchen von Kampagnen {#access}

Auf Kampagnen kann über das Menü **[!UICONTROL Kampagnen]** zugegriffen werden. Verwenden Sie die Registerkarten, um Kampagnen nach Typ zu durchsuchen: **Aktionskampagnen**, **durch API ausgelöste Kampagnen** und **orchestrierte Kampagnen**. Erfahren Sie mehr über die [Kampagnentypen](get-started-with-campaigns.md#campaign-types). Die verfügbaren Typen hängen von Ihrer Lizenzvereinbarung und Ihren Berechtigungen ab.

>[!BEGINTABS]

>[!TAB Aktionskampagnen]

Wählen Sie die Registerkarte **[!UICONTROL Aktion]** aus, um auf die Liste aller Aktionskampagnen zuzugreifen.

Standardmäßig werden in der Liste alle Kampagnen mit dem Status **[!UICONTROL Entwurf]**, **[!UICONTROL Geplant]** oder **[!UICONTROL Live]** angezeigt. Um gestoppte, abgeschlossene und archivierte Kampagnen anzuzeigen, müssen Sie den Filter löschen.

![](assets/create-campaign-list.png)

>[!TAB Durch API ausgelöste Kampagnen]

Wählen Sie die Registerkarte **[!UICONTROL Durch API ausgelöst]** aus, um auf die Liste der Kampagnen zuzugreifen, die durch API ausgelöst werden.

Standardmäßig werden in der Liste alle Kampagnen mit dem Status **[!UICONTROL Entwurf]**, **[!UICONTROL Geplant]** oder **[!UICONTROL Live]** angezeigt. Um gestoppte, abgeschlossene und archivierte Kampagnen anzuzeigen, müssen Sie den Filter löschen.

![](assets/api-triggered-list.png)

>[!TAB Orchestrierte Kampagnen]

Wählen Sie die Registerkarte **[!UICONTROL Orchestrierung]** aus, um auf die Liste der orchestrierten Kampagnen zuzugreifen.

![Bild, das das Inventar der orchestrierten Kampagnen zeigt](assets/inventory.png){zoomable="yes"}

Zu jeder orchestrierten Kampagne in der Liste werden Informationen angezeigt, beispielsweise der aktuelle [Status](#statuses) der Kampagne, der zugehörige Kanal und zugehörige Tags oder der Zeitpunkt der letzten Änderung. Sie können die angezeigten Spalten anpassen, indem Sie auf die Schaltfläche ![Layout konfigurieren](assets/do-not-localize/inventory-configure-layout.svg) klicken.

>[!ENDTABS]

### Suchen und Filtern von Kampagnen {#search-filter}

Darüber hinaus stehen eine Suchleiste und Filter zur Verfügung, um die Suche innerhalb der Liste zu erleichtern. Sie können die Kampagnen beispielsweise so filtern, dass nur die einem bestimmten Kanal oder Tag angehörenden oder nur die während eines bestimmten Datumsbereichs erstellten Kampagnen angezeigt werden.

## Kampagnenvorgänge {#operations}

Die Schaltfläche ![Bild mit der Schaltfläche „Mehr Aktionen“](assets/do-not-localize/rule-builder-icon-more.svg) im Kampagneninventar ermöglicht die Durchführung unterschiedlicher Vorgänge.

![Bild mit Kampagneninventar](assets/inventory-actions.png)

### Verfügbare Aktionen

**Für alle Kampagnentypen:**

* **[!UICONTROL Bericht für gesamte Zeit anzeigen]** / **[!UICONTROL Bericht für letzte 24 Stunden anzeigen]**: Greifen Sie auf Berichte zu, um die Wirkung und Leistung Ihrer orchestrierten Kampagnen zu messen und zu visualisieren. [Weitere Informationen zu Kampagnenberichten →](../reports/campaign-global-report-cja.md)
* **[!UICONTROL Tags bearbeiten]**: Bearbeiten Sie die mit der Kampagne verknüpften Tags. [Weitere Informationen zum Verwenden von Tags →](../start/search-filter-categorize.md#add-tags)
* **[!UICONTROL Duplizieren]**: Verwenden Sie diese Option, um eine Kampagne zu duplizieren, z. B. um eine orchestrierte Kampagne auszuführen, die gestoppt wurde. [Weitere Informationen zum Duplizieren →](#duplicate-a-campaign)
* **[!UICONTROL Löschen]**: Verwenden Sie diese Option, um eine Kampagne zu löschen. [Weitere Informationen zum Löschen →](#delete-a-campaign)
* **[!UICONTROL Archivieren]**: Archiviert die Kampagne. Alle archivierten Kampagnen werden rollierend 30 Tage nach dem Datum ihrer letzten Änderung gelöscht. Diese Aktion ist für alle Kampagnen mit Ausnahme von Kampagnen im Status **[!UICONTROL Entwurf]** verfügbar. [Weitere Informationen zum Archivieren →](#archive-a-campaign)

**Nur für von Aktionen und API ausgelöste Kampagnen:**

* **[!UICONTROL Zu Paket hinzufügen]**: Fügt die Kampagne zu einem Paket hinzu, um sie in eine andere Sandbox zu exportieren. [Weitere Informationen zum Exportieren von Objekten →](../configuration/copy-objects-to-sandbox.md)
* **[!UICONTROL Entwurfsversion öffnen]**: Wenn eine neue Version der Kampagne erstellt und noch nicht aktiviert wurde, können Sie mit dieser Aktion auf ihre Entwurfsversion zugreifen.

**Nur für orchestrierte Kampagnen:**

* **[!UICONTROL Zurück zum Entwurf]** - Rückgängigmachen der Veröffentlichung und Zurücksetzen einer Kampagne in den Entwurfsstatus zur Fehlerbehebung. Diese Aktion ist verfügbar, wenn eine geplante Kampagne noch nicht gestartet wurde oder wenn bei einer Live-Kampagne ein Fehler auftritt, bevor irgendwelche Ausführungen abgeschlossen sind. [Erfahren Sie mehr über das Zurücksetzen von Kampagnen →](../orchestrated/start-monitor-campaigns.md#back-to-draft)

## Grundlegendes zum Kampagnenstatus {#statuses}

Jede Kampagne durchläuft einen Lebenszyklus, der sich in ihrem Status in der Benutzeroberfläche widerspiegelt. Wenn Sie diese Status verstehen, können Sie feststellen, welche Aktionen verfügbar sind und was als Nächstes zu tun ist.

| Status | Aktionskampagnen | Durch API ausgelöste Kampagnen | Orchestrierte Kampagnen | Bedeutung | Nächste Aktionen |
|--------|:----------------:|:-----------------------:|:----------------------:|---------------|--------------|
| **[!UICONTROL Entwurf]** | ✅ | ✅ | ✅ | In Bearbeitung, nicht aktiviert | Bearbeitung fortsetzen oder [Kampagne aktivieren](review-activate-campaign.md) |
| **[!UICONTROL Geplant]** | ✅ | ✅ | ✅ | Für bestimmtes Startdatum konfiguriert | Auf Launch warten, [bei Bedarf ändern](#modify) oder [im Kalender anzeigen](#calendar) |
| **[!UICONTROL Live]** | ✅ | ✅ | ✅ | Aktiviert und in Ausführung | [Überwachen der Leistung](../reports/campaign-global-report-cja.md), [Erstellen einer neuen Version](#modify) falls erforderlich. Für orchestrierte Kampagnen: [Zurück zum Entwurf](../orchestrated/start-monitor-campaigns.md#back-to-draft) für geplante Kampagnen, die noch nicht gestartet wurden, oder für Kampagnen mit Ausführungsfehlern, bevor Nachrichten gesendet werden |
| **[!UICONTROL Wird überprüft]** | ✅ | ✅ | – | Zur Genehmigung eingereicht | Auf [Genehmigung](../test-approve/gs-approval.md) warten oder ändern |
| **[!UICONTROL Gestoppt]** | ✅ | ✅ | ✅ | Manuell gestoppt, kann nicht wieder aktiviert werden | [Zur Wiederverwendung duplizieren](#duplicate-a-campaign) |
| **[!UICONTROL Abgeschlossen]** | ✅ | ✅ | ✅ | Ausführung abgeschlossen (wird 3 Tage nach Aktivierung automatisch zugewiesen oder bei wiederkehrender Ausführung am Enddatum) | [Berichte anzeigen](../reports/campaign-global-report-cja.md), [archivieren](#archive-a-campaign) oder [duplizieren](#duplicate-a-campaign) |
| **[!UICONTROL Fehlgeschlagen]** | ✅ | ✅ | – | Ausführung fehlgeschlagen | Protokolle prüfen, Probleme beheben, [duplizieren und erneut versuchen](#duplicate-a-campaign) |
| **[!UICONTROL Archiviert]** | ✅ | ✅ | ✅ | Archiviert (nach 30 Tagen automatisch gelöscht) | Bei Bedarf [mit Filter abrufen](#access) |
| **[!UICONTROL Geschlossen]** | – | – | ✅ | Wiederkehrende Kampagne geschlossen, keine neuen Eintritte zulässig (wird fortgesetzt, bis alle Aktivitäten abgeschlossen sind) | Auf Abschluss warten |
| **[!UICONTROL Wird veröffentlicht]** | – | – | ✅ | In Veröffentlichung | Auf Abschluss der Veröffentlichung warten |

>[!NOTE]
>
>Bei durch Aktionen oder API ausgelösten Kampagnen zeigt das Symbol „Entwurfsversion öffnen“ neben einem Status **[!UICONTROL Live]** oder **[!UICONTROL Geplant]** an, dass eine neue Version erstellt und noch nicht aktiviert wurde.

### Fehlerindikatoren

Tritt in einer Ihrer Kampagnen ein Fehler auf, wird neben dem Status der Kampagne ein Warnsymbol angezeigt. Klicken Sie darauf, um Informationen zum Warnhinweis anzuzeigen. Diese Warnhinweise können in verschiedenen Situationen auftreten, z. B. wenn die Kampagnennachricht nicht veröffentlicht wurde oder die gewählte Konfiguration falsch ist.

![](assets/campaign-alerts.png)

>[!NOTE]
>
>Assets/Bilder sind in bereitgestellten Inhalten für bis zu 2 Jahre (730 Tage) ab ihrer ersten Veröffentlichung in einem Fragment/einer Inline-Nachricht verfügbar. Nach Ablauf dieses Zeitraums (nach 730 Tagen) ist eine erneute Veröffentlichung erforderlich, um sie für weitere 2 Jahre verfügbar zu machen. Eine erneute Veröffentlichung innerhalb von 730 Tagen nach der ersten Veröffentlichung verlängert den Ablauf der Assets/Bilder nicht um weitere 730 Tage.

## Kampagnenkalender {#calendar}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_view"
>title="Listen- und Kalenderansicht für Kampagnen"
>abstract="Zusätzlich zur Kampagnenliste bietet [!DNL Journey Optimizer] eine Kalenderansicht Ihrer Kampagnen mit einer übersichtlichen Darstellung ihrer Zeitpläne. Über diese Schaltflächen können Sie jederzeit zwischen der Listen- und Kalenderansicht wechseln."

Zusätzlich zur Kampagnenliste bietet [!DNL Journey Optimizer] eine Kalenderansicht der Kampagnen mit einer übersichtlichen Darstellung der Zeitpläne. 

### Funktionsweise des Kalenders

Darstellung der Kampagnen:

* Standardmäßig zeigt das Kalenderraster alle Live- und geplanten Kampagnen für die ausgewählte Woche an. Zusätzliche Filteroptionen können abgeschlossene, gestoppte und beendete Aktivierungen oder Aktivierungen eines bestimmten Typs oder Kanals anzeigen.
* Kampagnenentwürfe werden nicht angezeigt.
* Kampagnen, die sich über mehrere Tage erstrecken, werden oben im Kalenderraster angezeigt.
* Wenn keine Startzeit angegeben ist, wird die nächste manuelle Aktivierungszeit zur Positionierung im Kalender verwendet.
* Kampagnen werden als Zeitspannen von 1 Stunde angezeigt, dies spiegelt jedoch nicht die tatsächliche Versand- oder Abschlusszeit wider.

### Navigieren im Kalender

1. Klicken Sie auf das Symbol ![Kalender](assets/do-not-localize/Smock_Calendar_18_N.svg), um auf Ihren Kampagnenkalender zuzugreifen.

1. Verwenden Sie die Pfeiltasten oder die Datumsauswahl über dem Kalender, um zwischen Wochen zu wechseln.

   Der Kalender zeigt alle für die aktuelle Woche geplanten Kampagnen an.

   ![Kalenderansicht mit Live-Kampagnen](assets/campaigns-timeline.png)

1. Klicken Sie auf das Symbol ![Zahnrad](assets/do-not-localize/Smock_Gears_18_N.png), um die Anzeige von Elementen umzuschalten, die sich über mehrere Tage oder Wochen erstrecken.

   ![Kalenderansicht mit Live-Kampagnen](assets/campaign-long-term.png)

1. Klicken Sie auf das Symbol ![Kalender hinzufügen](assets/do-not-localize/Smock_CalendarAdd_18_N.svg), um bis zu drei externe Kalender zu verwalten und hinzuzufügen.

   ![Kalenderansicht mit externen Kalendern](assets/campaign-external-calendar.png)

1. Verschieben Sie Ihre CSV-Dateien mit den Namen der Veranstaltungen sowie Start- und Enddaten per Drag-and-Drop.

   Hochgeladene Ereignisse werden für alle Benutzenden in Ihrer Organisation angezeigt und erscheinen sowohl im Journey- als auch im Kampagnenkalender.

   +++Das CSV-Format sollte wie folgt aussehen:

   | Spalte1 | Spalte2 | Spalte3 |
   |-|-|-|
   | Ereignisname | Startdatum im Format TT/MM/JJ | Enddatum im Format TT/MM/JJ |

   +++

1. Bei Bedarf können Sie hinzugefügte externe Kalender ausblenden, einblenden oder entfernen.

   ![Kalenderansicht mit externen Kalendern](assets/campaign-manage-calendar.png)

1. Durch Klicken auf den visuellen Block einer Kampagne werden weitere Details geöffnet. Dies öffnet einen Informationsbereich mit unterschiedlichen Informationen über die Kampagne, z. B. den Kampagnentyp, Zugriff auf die Berichte oder die zugewiesenen Tags.

   ![Kampagnenliste mit geöffnetem Informationsbereich](assets/campaign-rail.png)

## Ändern und Stoppen wiederkehrender Aktionskampagnen {#modify}

### Ändern einer Aktionskampagne {#modify-an-action-campaign}

Gehen Sie wie folgt vor, um eine neue Version einer wiederkehrenden Aktionskampagne zu ändern und zu erstellen:

1. Öffnen Sie die Aktionskampagne und klicken Sie dann auf die Schaltfläche **[!UICONTROL Kampagne ändern]**.

1. Eine neue Version der Kampagne wird erstellt. Sie können die Live-Version überprüfen, indem Sie auf **[!UICONTROL Live-Version öffnen]** klicken.

   ![](assets/create-campaign-draft.png)

   In der Liste der Kampagnen werden aktivierte Kampagnen, für die eine Entwurfsversion in Bearbeitung ist, mit einem speziellen Symbol in der Spalte **[!UICONTROL Status]** angezeigt. Klicken Sie auf dieses Symbol, um die Entwurfsversion der Kampagne zu öffnen.

   ![](assets/create-campaign-edit-list.png)

1. Sobald Sie mit den Änderungen fertig sind, können Sie die neue Version der Kampagne aktivieren (siehe [Überprüfung und Aktivierung einer Kampagne](review-activate-campaign.md)).

   >[!IMPORTANT]
   >
   >Durch die Aktivierung des Entwurfs wird die Live-Version der Kampagne ersetzt.

**Verwandte Themen:**
* [Eigenschaften der Kampagne](campaign-properties.md)
* [Kampagnenaktionen](campaign-action.md)
* [Kampagneninhalt](campaign-content.md)
* [Kampagnenzielgruppe](campaign-audience.md)
* [Kampagnenzeitplan](campaign-schedule.md)

### Stoppen einer Aktionskampagne {#stop}

Zum Stoppen einer wiederkehrenden Kampagne öffnen Sie diese und klicken Sie auf die Schaltfläche **[!UICONTROL Kampagne stoppen]**.

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>Das Stoppen einer Kampagne stoppt keinen laufenden Versand, aber es stoppt einen geplanten Versand oder die nächsten Vorgänge, wenn der Versand bereits läuft.

## Archivieren einer Kampagne {#archive-a-campaign}

Mit der Zeit wächst die Liste der Kampagnen, wodurch es zunehmend schwieriger wird, abgeschlossene und gestoppte Kampagnen zu durchsuchen.

Um dies zu verhindern, können Sie abgeschlossene und gestoppte Kampagnen archivieren, die Sie nicht mehr benötigen. Klicken Sie dazu auf die Schaltfläche mit den Auslassungspunkten und wählen Sie **[!UICONTROL Archivieren]**.

![](assets/create-campaign-archive.png)

Archivierte Kampagnen können dann mithilfe des entsprechenden Filters in der Liste abgerufen werden.

## Löschen einer Kampagne {#delete-a-campaign}

Um eine Kampagne zu löschen, verwenden Sie die Schaltfläche mit den Auslassungspunkten ![Bild mit der Schaltfläche „Weitere Aktionen“](assets/do-not-localize/rule-builder-icon-more.svg) und wählen Sie **[!UICONTROL Löschen]** aus.

![](assets/delete-a-campaign.png){width="70%" align="left"}

>[!IMPORTANT]
>
>Diese Aktion ist nur für Kampagnen im Status **[!UICONTROL Entwurf]** verfügbar.

## Duplizieren einer Kampagne {#duplicate-a-campaign}

Um eine Kampagne zu duplizieren (beispielsweise wenn sie gestoppt wurde), verwenden Sie die Schaltfläche mit den Auslassungspunkten ![Bild mit der Schaltfläche „Weitere Aktionen“](assets/do-not-localize/rule-builder-icon-more.svg) und wählen Sie **[!UICONTROL Duplizieren]** aus.

Geben Sie den Namen der Kampagne ein und speichern Sie ihn. 

Die Kampagne wurde erstellt und ist nun in der Kampagnenliste sichtbar.

## Weitere Ressourcen

* **Erste Schritte** – [Erste Schritte mit Kampagnen](get-started-with-campaigns.md) | [Erstellen der ersten Aktionskampagne](create-campaign.md) | [Leitfaden zu durch API ausgelösten Kampagnen](api-triggered-campaigns.md) | [Leitfaden zu orchestrierten Kampagnen](../orchestrated/gs-orchestrated-campaigns.md)

* **Kampagnenkonfiguration** – [Kampagneneigenschaften](campaign-properties.md) | [Kampagnenaktionen und -kanäle](campaign-action.md) | [Design des Kampagneninhalts](campaign-content.md) | [Auswählen der Kampagnenzielgruppe](campaign-audience.md) | [Kampagnenplanung](campaign-schedule.md)

* **Erweiterte Funktionen** – [Genehmigungs-Workflows](../test-approve/gs-approval.md) | [Konflikt-Management und Priorisierung](../conflict-prioritization/gs-conflict-prioritization.md) | [Frequenzbegrenzung nach Kanal](../conflict-prioritization/channel-capping.md) | [Prioritätswerte](../conflict-prioritization/priority-scores.md) | [Exportieren von Kampagnen in andere Sandboxes](../configuration/copy-objects-to-sandbox.md)

* **Überwachung und Optimierung** – [Kampagnenberichte (CJA)](../reports/campaign-global-report-cja.md) | [Einrichten von Warnhinweisen](../reports/alerts.md)

* **Organisation** – [Arbeiten mit Tags](../start/search-filter-categorize.md) | [Verwalten von Berechtigungen](../administration/ootb-product-profiles.md)
