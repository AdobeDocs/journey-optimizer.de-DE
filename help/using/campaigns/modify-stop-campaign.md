---
solution: Journey Optimizer
product: journey optimizer
title: Zugreifen auf und Verwalten von Kampagnen
description: Informationen zum Zugreifen auf und Verwalten von Kampagnen in Journey Optimizer.
feature: Campaigns
topic: Content Management
role: User
mini-toc-levels: 1
level: Beginner
keywords: Verwalten von Kampagnen, Status, Zeitplan, Zugriff, Optimizer
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 73%

---

# Zugreifen auf und Verwalten von Kampagnen {#modify-stop-campaign}

## Zugriff auf Kampagnen {#access}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_view"
>title="Listen- und Kalenderansicht für Kampagnen"
>abstract="Zusätzlich zur Kampagnenliste bietet [!DNL Journey Optimizer] eine Kalenderansicht Ihrer Kampagnen mit einer übersichtlichen Darstellung ihrer Zeitpläne. Über diese Schaltflächen können Sie jederzeit zwischen der Listen- und Kalenderansicht wechseln."

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Orchestrierte Inventarkampagnen"
>abstract="Auf diesem Bildschirm können Sie auf die vollständige Liste der orchestrierten Kampagnen zugreifen, ihren aktuellen Status sowie das Datum der letzten/nächsten Ausführung überprüfen und eine neue orchestrierte Kampagne erstellen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="Aktion"
>abstract="In diesem Abschnitt werden alle in der orchestrierten Kampagne verwendeten Aktionen aufgelistet."

Auf Kampagnen kann über das Menü **[!UICONTROL Kampagnen]** zugegriffen werden.

>[!BEGINTABS]

>[!TAB Aktionskampagnen]

Wählen Sie die **[!UICONTROL Aktion]** aus, um auf die Liste der Aktionskampagnen zuzugreifen.

Standardmäßig werden in der Liste alle Kampagnen mit dem Status **[!UICONTROL Entwurf]**, **[!UICONTROL Geplant]** oder **[!UICONTROL Live]** angezeigt. Um gestoppte, abgeschlossene und archivierte Kampagnen anzuzeigen, müssen Sie den Filter löschen.

![](assets/create-campaign-list.png)

>[!TAB Kampagnen, die durch API ausgelöst werden]

Wählen Sie die Registerkarte **[!UICONTROL Durch API ausgelöst]** aus, um auf die Liste der Kampagnen zuzugreifen, die durch API ausgelöst werden.

Standardmäßig werden in der Liste alle Kampagnen mit dem Status **[!UICONTROL Entwurf]**, **[!UICONTROL Geplant]** oder **[!UICONTROL Live]** angezeigt. Um gestoppte, abgeschlossene und archivierte Kampagnen anzuzeigen, müssen Sie den Filter löschen.

![](assets/api-triggered-list.png)

>[!TAB Orchestrierte Kampagnen]

Wählen Sie die **[!UICONTROL Orchestrierung]**, um auf die Liste der orchestrierten Kampagnen zuzugreifen.

![Bild mit dem Inventar der orchestrierten Kampagnen](assets/inventory.png){zoomable="yes"}{zoomable="yes"}

Jede orchestrierte Kampagne in der Liste zeigt Informationen wie den aktuellen (Status[ der Kampagne, ](#status) zugehörigen Kanal und Tags oder das letzte Mal, wann sie geändert wurde, an. Sie können die angezeigten Spalten anpassen, indem Sie auf die Schaltfläche ![Layout konfigurieren](assets/do-not-localize/inventory-configure-layout.svg) klicken.

>[!ENDTABS]

Darüber hinaus stehen eine Suchleiste und Filter zur Verfügung, um die Suche innerhalb der Liste zu erleichtern. Sie können beispielsweise Kampagnen so filtern, dass nur die mit einem bestimmten Kanal oder Tag verknüpften oder die in einem bestimmten Datumsbereich erstellten Kampagnen angezeigt werden.

Die Schaltfläche ![Bild mit der Schaltfläche „Mehr Aktionen“](assets/do-not-localize/rule-builder-icon-more.svg) im Kampagneninventar ermöglicht die Durchführung der folgenden Vorgänge.

![Bild mit dem Kampagneninventar](assets/inventory-actions.png)

* **[!UICONTROL Alle Zeitberichte anzeigen]**/**[!UICONTROL Bericht zu letzten 24 Stunden anzeigen]** - Greifen Sie auf Berichte zu, um die Wirkung und Leistung Ihrer Kampagnen zu messen und zu visualisieren.
* **[!UICONTROL Tags bearbeiten]**: Bearbeiten Sie die mit der Kampagne verknüpften Tags.
* **[!UICONTROL Duplizieren]** - In einigen Fällen müssen Sie möglicherweise eine Kampagne duplizieren, z. B. um eine orchestrierte Kampagne auszuführen, die gestoppt wurde.
* **[!UICONTROL Löschen]**: Löscht die Kampagne. Diese Aktion ist nur für Kampagnen **[!UICONTROL Entwurf]** verfügbar.
* **[!UICONTROL Archivieren]**: Archiviert die Kampagne. Alle archivierten Kampagnen werden rollierend 30 Tage nach dem Datum ihrer letzten Änderung gelöscht. Diese Aktion ist für alle Kampagnen mit Ausnahme von Kampagnen im Status **[!UICONTROL Entwurf]** verfügbar.

Für von einer Aktion und API ausgelöste Kampagnen sind die folgenden zusätzlichen Aktionen verfügbar:

* **[!UICONTROL Zu Paket hinzufügen]** - Fügen Sie die Kampagne zu einem Paket hinzu, um sie in eine andere Sandbox zu exportieren. [Objekte in eine andere Sandbox exportieren](../configuration/copy-objects-to-sandbox.md)
* **[!UICONTROL Entwurfsversion öffnen]** - Wenn eine neue Version der Kampagne erstellt wurde und noch nicht aktiviert wurde, können Sie mit dieser Aktion auf ihre Entwurfsversion zugreifen.

## Kampagnenstatus und Warnungen {#statuses}

Kampagnen können mehrere Status aufweisen:

>[!BEGINTABS]

>[!TAB Aktionskampagnen]

* **[!UICONTROL Entwurf]**: Die Kampagne wird noch bearbeitet, sie wurde nicht aktiviert.
* **[!UICONTROL Geplant]**: Die Kampagne wurde so konfiguriert, dass sie an einem bestimmten Startdatum aktiviert wird.
* **[!UICONTROL Live]**: Die Kampagne wurde aktiviert.
* **[!UICONTROL Wird überprüft]**: Die Kampagne wurde zur Genehmigung eingereicht, damit sie veröffentlicht werden kann. [Informationen zum Arbeiten mit Genehmigungen](../test-approve/gs-approval.md)
* **[!UICONTROL Gestoppt]**: Die Kampagne wurde manuell gestoppt. Sie können sie nicht mehr aktivieren oder wiederverwenden. [Informationen zum Stoppen einer Kampagne](modify-stop-campaign.md#stop)
* **[!UICONTROL Abgeschlossen]**: Die Kampagne ist abgeschlossen. Dieser Status wird automatisch 3 Tage nach der Aktivierung einer Kampagne zugewiesen oder am Enddatum der Kampagne, wenn sie eine wiederkehrende Ausführung aufweist.
* **[!UICONTROL Fehlgeschlagen]**: Die Ausführung der Kampagne ist fehlgeschlagen. Überprüfen Sie die Protokolle, um das Problem zu identifizieren.
* **[!UICONTROL Archiviert]**: Die Kampagne wurde archiviert. [Informationen zum Archivieren von Kampagnen](modify-stop-campaign.md#archive)

>[!NOTE]
>
>Das Symbol „Entwurfsversion öffnen“ neben einem Status **[!UICONTROL Live]** oder **[!UICONTROL Geplant]** zeigt an, dass eine neue Version einer von einer Aktion oder API ausgelösten Kampagne erstellt wurde und noch nicht aktiviert wurde.

>[!TAB Kampagnen, die durch API ausgelöst werden]

* **[!UICONTROL Entwurf]**: Die Kampagne wird noch bearbeitet, sie wurde nicht aktiviert.
* **[!UICONTROL Geplant]**: Die Kampagne wurde so konfiguriert, dass sie an einem bestimmten Startdatum aktiviert wird.
* **[!UICONTROL Live]**: Die Kampagne wurde aktiviert.
* **[!UICONTROL Wird überprüft]**: Die Kampagne wurde zur Genehmigung eingereicht, damit sie veröffentlicht werden kann. [Informationen zum Arbeiten mit Genehmigungen](../test-approve/gs-approval.md)
* **[!UICONTROL Gestoppt]**: Die Kampagne wurde manuell gestoppt. Sie können sie nicht mehr aktivieren oder wiederverwenden. [Informationen zum Stoppen einer Kampagne](modify-stop-campaign.md#stop)
* **[!UICONTROL Abgeschlossen]**: Die Kampagne ist abgeschlossen. Dieser Status wird automatisch 3 Tage nach der Aktivierung einer Kampagne zugewiesen oder am Enddatum der Kampagne, wenn sie eine wiederkehrende Ausführung aufweist.
* **[!UICONTROL Fehlgeschlagen]**: Die Ausführung der Kampagne ist fehlgeschlagen. Überprüfen Sie die Protokolle, um das Problem zu identifizieren.
* **[!UICONTROL Archiviert]**: Die Kampagne wurde archiviert. [Informationen zum Archivieren von Kampagnen](modify-stop-campaign.md#archive)

>[!NOTE]
>
>Das Symbol „Entwurfsversion öffnen“ neben einem Status **[!UICONTROL Live]** oder **[!UICONTROL Geplant]** zeigt an, dass eine neue Version einer von einer Aktion oder API ausgelösten Kampagne erstellt wurde und noch nicht aktiviert wurde.

>[!TAB Orchestrierte Kampagnen]

* **[!UICONTROL Entwurf]**: Die orchestrierte Kampagne wurde erstellt. Sie wurde noch nicht veröffentlicht.
* **[!UICONTROL Veröffentlichen]**: Die orchestrierte Kampagne wird veröffentlicht.
* **[!UICONTROL Live]**: Die orchestrierte Kampagne wurde veröffentlicht und wird ausgeführt.
* **[!UICONTROL Geplant]**: Die Ausführung der orchestrierten Kampagne wurde geplant.
* **[!UICONTROL Abgeschlossen]**: Die Ausführung der orchestrierten Kampagne ist abgeschlossen. Der Status „Abgeschlossen“ wird einer Kampagne automatisch bis zu 3 Tage nach dem fehlerfreien Versand von Nachrichten zugewiesen.
* **[!UICONTROL Geschlossen]**: Dieser Status wird angezeigt, wenn eine wiederkehrende Kampagne geschlossen wurde. Die Kampagne wird ausgeführt, bis alle Aktivitäten abgeschlossen sind, aber es können keine weiteren Profile in die Kampagne eintreten.
* **[!UICONTROL Archiviert]**: Die koordinierte Kampagne wurde archiviert. Alle archivierten Kampagnen werden rollierend 30 Tage nach dem Datum ihrer letzten Änderung gelöscht. Sie können eine archivierte Kampagne bei Bedarf duplizieren, um sie weiter zu bearbeiten.
* **[!UICONTROL Angehalten]**: Die Ausführung der orchestrierten Kampagne wurde angehalten. Um die Kampagne erneut zu starten, müssen Sie sie duplizieren.

>[!ENDTABS]

Tritt in einer Ihrer Kampagnen ein Fehler auf, wird neben dem Status der Kampagne ein Warnsymbol angezeigt. Klicken Sie darauf, um Informationen zum Warnhinweis anzuzeigen. Diese Warnhinweise können in verschiedenen Situationen auftreten, z. B. wenn die Kampagnennachricht nicht veröffentlicht wurde oder die gewählte Konfiguration falsch ist.

![](assets/campaign-alerts.png)

## Kampagnenkalender {#calendar}

Zusätzlich zur Kampagnenliste bietet [!DNL Journey Optimizer] eine Kalenderansicht der Kampagnen mit einer übersichtlichen Darstellung der Zeitpläne. 

>[!AVAILABILITY]
>
>Die Kalenderansicht ist derzeit nur für von Aktionen und API ausgelöste Kampagnen für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Verwenden Sie [dieses Formular](https://forms.cloud.microsoft/r/FC49afuJVi){target=”_blank”} zum Anfordern des Zugriffs.
>
>Diese Funktion befindet sich in der aktiven Entwicklung. Wir freuen uns über Ihre Rückmeldungen und Anfragen über die Schaltfläche **[!UICONTROL Beta-Feedback]** im oberen Menü.

Der Kalender zeigt alle für die aktuelle Woche geplanten Kampagnen an. Navigieren Sie mit den Pfeiltasten über dem Kalender zwischen Wochen.

![Kalenderansicht mit Live-Kampagnen](assets/campaigns-timeline.png)

Darstellung der Kampagnen:

* Standardmäßig zeigt das Kalenderraster alle Live- und geplanten Kampagnen für die ausgewählte Woche an. Zusätzliche Filteroptionen können abgeschlossene, gestoppte und beendete Aktivierungen oder Aktivierungen eines bestimmten Typs oder Kanals anzeigen.
* Kampagnenentwürfe werden nicht angezeigt.
* Kampagnen, die sich über mehrere Tage erstrecken, werden oben im Kalenderraster angezeigt.
* Wenn keine Startzeit angegeben ist, wird die nächste manuelle Aktivierungszeit zur Positionierung im Kalender verwendet.
* Kampagnen werden als Zeitspannen von 1 Stunde angezeigt, dies spiegelt jedoch nicht die tatsächliche Versand- oder Abschlusszeit wider.

Durch Klicken auf den visuellen Block einer Kampagne werden weitere Details geöffnet.

Wählen Sie eine Kampagne aus der Liste aus, um Details für diese spezifische Kampagne anzuzeigen. Dies öffnet einen Informationsbereich mit unterschiedlichen Informationen über die Kampagne, z. B. den Kampagnentyp, Zugriff auf die Berichte oder die zugewiesenen Tags.

![Kampagnenliste mit geöffnetem Informationsbereich](assets/campaign-rail.png)

## Ändern und Beenden wiederkehrender Aktionskampagnen {#modify}

### Ändern einer Aktionskampagne

Gehen Sie wie folgt vor, um eine wiederkehrende Aktionskampagne zu ändern und eine neue Version zu erstellen:

1. Öffnen Sie die Aktionskampagne und klicken Sie auf die Schaltfläche **[!UICONTROL Kampagne ändern]**.

1. Eine neue Version der Kampagne wird erstellt. Sie können die Live-Version überprüfen, indem Sie auf **[!UICONTROL Live-Version öffnen]** klicken.

   ![](assets/create-campaign-draft.png)

   In der Liste der Kampagnen werden aktivierte Kampagnen, für die eine Entwurfsversion in Bearbeitung ist, mit einem speziellen Symbol in der Spalte **[!UICONTROL Status]** angezeigt. Klicken Sie auf dieses Symbol, um die Entwurfsversion der Kampagne zu öffnen.

   ![](assets/create-campaign-edit-list.png)

1. Sobald Sie mit den Änderungen fertig sind, können Sie die neue Version der Kampagne aktivieren (siehe [Überprüfung und Aktivierung einer Kampagne](create-campaign.md#review-activate)).

   >[!IMPORTANT]
   >
   >Durch die Aktivierung des Entwurfs wird die Live-Version der Kampagne ersetzt.

### Stoppen einer Aktionskampagne {#stop}

Zum Stoppen einer wiederkehrenden Kampagne, öffnen Sie diese und klicken Sie auf die Schaltfläche **[!UICONTROL Kampagne stoppen]**.

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>Das Anhalten einer Kampagne stoppt keinen laufenden Versand, aber es stoppt einen geplanten Versand oder die nächsten Vorgänge, wenn der Versand bereits im Gange ist.

## Archivieren einer Kampagne {#archive}

Mit der Zeit wächst die Liste der Kampagnen, wodurch es zunehmend schwieriger wird, abgeschlossene und gestoppte Kampagnen zu durchsuchen.

Um dies zu verhindern, können Sie abgeschlossene und gestoppte Kampagnen archivieren, die Sie nicht mehr benötigen. Klicken Sie dazu auf die Schaltfläche mit den Auslassungspunkten und wählen Sie **[!UICONTROL Archivieren]**.

![](assets/create-campaign-archive.png)

Archivierte Kampagnen können dann mithilfe des entsprechenden Filters in der Liste abgerufen werden.
