---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen von orchestrierten Kampagnen mit Journey Optimizer
description: Erfahren Sie, wie Sie mit Adobe Journey Optimizer eine koordinierte Kampagne erstellen
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 935ab0399da88c792104b7dc14793b69713951fc
workflow-type: tm+mt
source-wordcount: '1734'
ht-degree: 32%

---


# Erstellen einer orchestrierten Kampagne {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Liste der orchestrierten Kampagnen"
>abstract="Unter der Registerkarte **Mehrstufig** werden alle mehrstufigen Kampagnen aufgelistet. Klicken Sie auf den Namen einer orchestrierten Kampagne, um sie zu bearbeiten. Über die Schaltfläche **Orchestrierte Kampagne erstellen** können Sie eine neue orchestrierte Kampagne hinzufügen."

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten der ersten orchestrierten Kampagne | Abfragen der Datenbank | Orchestrierte Kampagnenaktivitäten |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](configuration-steps.md)<br/><br/>[Zugreifen auf und Verwalten von orchestrierten Kampagnen](access-manage-orchestrated-campaigns.md) | [Wichtige Schritte für die orchestrierte Kampagnenerstellung](gs-campaign-creation.md)<br/><br/><b>[Erstellen und konfigurieren Sie die ](create-orchestrated-campaign.md)</b><br/><br/>[-Aktivitäten](orchestrate-activities.md)<br/><br/>[ Senden Sie Nachrichten mit orchestrierten Kampagnen](send-messages.md)<br/><br/>[Starten und überwachen Sie die Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen Sie Ihre ersten ](build-query.md)<br/><br/>[-Bearbeitungsausdrücke](edit-expressions.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimensionsänderung](activities/change-dimension.md) - [Kombinieren](activities/combine.md) - [Deduplizierung](activities/enrichment.md) - [Verzweigung](activities/fork.md) - [Abstimmung](activities/reconciliation.md) - [Aufspaltung](activities/split.md)[ ](activities/wait.md) Warten](activities/deduplication.md) [ |

{style="table-layout:fixed"}

+++

<br/>

## Erstellen der Kampagne {#create}

Gehen Sie wie folgt vor, um eine orchestrierte Kampagne zu erstellen:

1. Navigieren Sie zum Menü **Kampagnen** .

1. Klicken Sie auf **[!UICONTROL Orchestrierte Kampagne erstellen]** in der oberen rechten Ecke des Bildschirms.

1. Wählen Sie im Dialogfeld **Eigenschaften** die Vorlage aus, die zur Erstellung der orchestrierten Kampagne verwendet werden soll (Sie können auch die standardmäßige integrierte Vorlage verwenden). [Erfahren Sie mehr über orchestrierte Kampagnenvorlagen](#campaign-templates).

1. Geben Sie einen Titel für die orchestrierte Kampagne ein. Darüber hinaus empfehlen wir dringend, zu Ihrer orchestrierten Kampagne eine Beschreibung im entsprechenden Feld des Abschnitts „Zusätzliche **[!UICONTROL &quot;]** Bildschirms hinzuzufügen.

1. Erweitern Sie den Abschnitt **[!UICONTROL Zusätzliche Optionen]**, um weitere Einstellungen für die orchestrierte Kampagne zu konfigurieren.

1. Klicken Sie auf **[!UICONTROL Orchestrierte Kampagne erstellen]**, um die Erstellung Ihrer orchestrierten Kampagne zu bestätigen.

Ihre orchestrierte Kampagne wird jetzt erstellt und ist in der Liste der Workflows verfügbar. Sie können jetzt auf die visuelle Arbeitsfläche zugreifen und mit dem Hinzufügen, Konfigurieren und Orchestrieren der Aufgaben beginnen, die ausgeführt werden sollen. [Erfahren Sie, wie Sie orchestrierte Kampagnenaktivitäten ](orchestrate-activities.md).

## Kampagneneinstellungen konfigurieren {#settings}

<!--Overview of new admin settings> schemas, execution fields, merge policy. [Learn more](configuration-steps.md)-->

Bei der Erstellung einer orchestrierten Kampagne oder der Orchestrierung von Kampagnenaktivitäten auf der Arbeitsfläche können Sie auf erweiterte Einstellungen im Zusammenhang mit der orchestrierten Kampagne zugreifen. Sie können beispielsweise eine bestimmte Zeitzone für die orchestrierte Kampagne festlegen, verwalten, wie sich die orchestrierte Kampagne im Fehlerfall verhalten soll, oder die Verzögerung verwalten, nach der der orchestrierte Kampagnenverlauf bereinigt werden soll.

Diese Einstellungen sind in der bei der Erstellung der orchestrierten Kampagne ausgewählten Vorlage vorkonfiguriert, können jedoch bei Bedarf für diese spezifische orchestrierte Kampagne bearbeitet werden.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

### Eigenschaften orchestrierter Kampagnen {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="Eigenschaften orchestrierter Kampagnen"
>abstract="Dieser Abschnitt enthält allgemeine Eigenschaften für orchestrierte Kampagnen, auf die auch beim Erstellen der orchestrierten Kampagne zugegriffen werden kann. Sie können die Vorlage auswählen, die zum Erstellen der orchestrierten Kampagne verwendet werden soll, und ein Label angeben. Erweitern Sie den Abschnitt „Zusätzliche Optionen“, um bestimmte Einstellungen zu konfigurieren, z. B. den Ordner, in dem die orchestrierte Kampagne gespeichert wird, oder die Zeitzone."

Der Abschnitt **[!UICONTROL Eigenschaften]** enthält allgemeine Einstellungen, die beim Erstellen einer orchestrierten Kampagne konfiguriert werden können. Um auf die Eigenschaften einer bestehenden orchestrierten Kampagne zuzugreifen, klicken Sie auf die Schaltfläche **[!UICONTROL Einstellungen]**, die in der Aktionsleiste über der orchestrierten Kampagnen-Arbeitsfläche verfügbar ist.

![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}

Diese Eigenschaften sind:

* Der **[!UICONTROL Titel]** der orchestrierten Kampagne, der in der Liste angezeigt wird.
* Der **[!UICONTROL Interne Name]** der orchestrierten Kampagne.
* Der **[!UICONTROL Ordner]** in dem die orchestrierte Kampagne gespeichert werden soll.
* Die **[!UICONTROL Zeitzone]**, die bei allen Aktivitäten der orchestrierten Kampagne verwendet wird. Standardmäßig ist die Zeitzone der orchestrierten Kampagne die für den aktuellen Campaign-Benutzer definierte Zeitzone.
Mögliche Werte sind:
   * **Server-Zeitzone**, um die Zeitzone Ihres Adobe Experience Platform-Unternehmens zu verwenden
   * **Zeitzone des Benutzers** nutzt die Zeitzone des Benutzers, der die orchestrierte Kampagne ausführt
   * **Zeitzone der Datenbank**, um die Zeitzone des Datenbank-Servers zu verwenden.
   * Eine bestimmte Zeitzone
* Wenn eine orchestrierte Kampagne fehlschlägt, werden die Benutzer, die zur Benutzergruppe gehören, die im Feld **[!UICONTROL Verantwortliche(r)) ausgewählt]**, per E-Mail benachrichtigt.
* Sie können auch eine **[!UICONTROL Beschreibung]** Ihrer orchestrierten Kampagne eingeben.

### Segmentierungseinstellungen  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Segmentierungseinstellungen"
>abstract="In diesem Abschnitt können Sie die Zielgruppendimension auswählen, um Profile in der orchestrierten Kampagne auszuwählen, und entscheiden, ob die Workflow-Ergebnisse zwischen zwei Ausführungen beibehalten werden sollen. Diese Option sollte nur zu Testzwecken verwendet werden und darf nie in einer orchestrierten Produktionskampagne aktiviert werden."

* **[!UICONTROL Zielgruppendimension]**: Wählen Sie die Zielgruppendimension aus, die für die Zielgruppenbestimmung von Profilen verwendet werden soll: Empfängerinnen und Empfänger, Vertragsbegünstigte, Benutzerinnen und Benutzer, Abonnentinnen und Abonnenten usw.

* **[!UICONTROL Zwischen zwei Ausführungen die ermittelte Population festhalten]**: Standardmäßig werden nur die Arbeitstabellen der letzten Ausführung der orchestrierten Kampagne beibehalten. Arbeitstabellen früherer Ausführungen werden durch eine technisch orchestrierte Kampagne bereinigt, die täglich ausgeführt wird.

  Wenn diese Option aktiviert ist, werden Arbeitstabellen auch nach Ausführung der orchestrierten Kampagne beibehalten. Sie können sie zu Testzwecken verwenden. Daher farf sie **nur** in Entwicklungs- oder Staging-Umgebungen genutzt werden. Sie darf nie in einer produktionsorientierten Kampagne aktiviert werden.

### Ausführungseinstellungen  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="Ausführungseinstellungen"
>abstract="In diesem Abschnitt können Sie die Einstellungen für die Ausführung des Workflows konfigurieren, beispielsweise für wie viele Tage der Verlauf der orchestrierten Kampagne gespeichert wird."

* **[!UICONTROL Verlauf in Tagen]**: Gibt die Anzahl der Tage an, nach denen der Verlauf bereinigt werden muss. Der Verlauf enthält Elemente, die mit der orchestrierten Kampagne in Verbindung stehen: Protokolle, Aufgaben, Ereignisse (technische Objekte, die mit dem orchestrierten Kampagnenvorgang verknüpft sind). Der Standardwert bei vorkonfigurierten orchestrierten Kampagnenvorlagen beträgt 30 Tage. Die Bereinigung des Verlaufs erfolgt durch die technisch orchestrierte Kampagne für die Datenbankbereinigung, die standardmäßig täglich ausgeführt wird

  >[!IMPORTANT]
  >
  >Wenn das Feld **[!UICONTROL Verlauf in Tagen]** leer gelassen wird, wird sein Wert als „1“ betrachtet; der Verlauf wird also nach einem Tag bereinigt.

* **[!UICONTROL Standardaffinität]**: Wenn Ihre Installation mehrere Server für orchestrierte Kampagnen umfasst, geben Sie in diesem Feld den Server an, auf dem die orchestrierte Kampagne ausgeführt werden soll. Dies erzwingt die Ausführung dieser orchestrierten Kampagne auf einem bestimmten Server. Sie können einen beliebigen vorhandenen Affinitätsnamen auswählen. Stellen Sie jedoch sicher, dass Sie keine Leerzeichen oder Satzzeichen verwenden. Wenn Sie verschiedene Server verwenden, geben Sie unterschiedliche Namen an, getrennt durch Kommas.

  >[!IMPORTANT]
  >
  >Wenn der in diesem Feld definierte Wert auf keinem Server vorhanden ist, bleibt die orchestrierte Kampagne ausstehend.


* **[!UICONTROL SQL-Abfragen im Protokoll speichern]**: Aktivieren Sie diese Option, um die SQL-Abfragen aus der mehrstufigen Workflow-Kampagne jetzt in den Protokollen zu speichern. Diese Funktion ist erfahrenen Benutzerinnen und Benutzern vorbehalten. Dies gilt für orchestrierte Kampagnen, die Zielgruppenbestimmungsaktivitäten enthalten, wie **[!UICONTROL Zielgruppe aufbauen]**. Wenn diese Option aktiviert ist, werden die SQL-Abfragen, die während der Ausführung der orchestrierten Kampagne an die Datenbank gesendet werden, in den Protokollen der orchestrierten Kampagne angezeigt, sodass Sie sie analysieren können, um Abfragen zu optimieren oder Probleme zu diagnostizieren.

### Einstellungen für den Umgang mit Fehlern  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Einstellungen für den Umgang mit Fehlern"
>abstract="In diesem Abschnitt können Sie definieren, wie die orchestrierte Kampagne mit Fehlern während ihrer Ausführung umgehen soll. Sie können festlegen, dass der Prozess angehalten, eine bestimmte Anzahl von Fehlern ignoriert oder die Ausführung der orchestrierten Kampagne gestoppt werden soll."

* **[!UICONTROL Umgang mit Fehlern]** In diesem Feld können Sie festlegen, welche Aktionen ausgeführt werden sollen, wenn eine orchestrierte Kampagnenaufgabe Fehler aufweist. Es gibt drei mögliche Optionen:

   * **[!UICONTROL Prozess aussetzen]**: Die orchestrierte Kampagne wird automatisch ausgesetzt und der Status ändert sich in **[!UICONTROL Fehlgeschlagen]**. Sobald das Problem behoben ist, setzen Sie die orchestrierte Kampagne mit der Schaltfläche **[!UICONTROL Fortsetzen]** fort.
   * **[!UICONTROL Ignorieren]**: Der Status der Aufgabe, die den Fehler ausgelöst hat, ändert sich in **[!UICONTROL Fehlgeschlagen]** aber die orchestrierte Kampagne behält den **[!UICONTROL Gestartet]** Status. <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Vorgang abbrechen]**: Die orchestrierte Kampagne wird automatisch angehalten und der Status ändert sich in **[!UICONTROL Fehlgeschlagen]**. Sobald das Problem behoben ist, starten Sie die orchestrierte Kampagne mithilfe der Schaltflächen **[!UICONTROL Starten]** neu.

* **[!UICONTROL Aufeinanderfolgende Fehler]**: Dieses Feld wird verfügbar, wenn im Feld **[!UICONTROL Im Fehlerfall]** der Wert **[!UICONTROL Ignorieren]** ausgewählt wurde. Sie können die Anzahl der Fehler angeben, die ignoriert werden können, bevor der Prozess angehalten wird. Sobald diese Zahl erreicht ist, ändert sich der Status der orchestrierten Kampagne in **[!UICONTROL Fehlgeschlagen]**. Wenn der Wert dieses Felds 0 ist, wird die orchestrierte Kampagne unabhängig von der Fehleranzahl nie angehalten.

## Arbeiten mit Vorlagen für orchestrierte Kampagnen {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Vorlagen für orchestrierte Kampagnen"
>abstract="Vorlagen für orchestrierte Kampagnen enthalten vorkonfigurierte Einstellungen und Aktivitäten, die zur Erstellung neuer orchestrierter Kampagnen wiederverwendet werden können."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Eigenschaften orchestrierter Kampagnen"
>abstract="Vorlagen für orchestrierte Kampagnen enthalten vorkonfigurierte Einstellungen und Aktivitäten, die zur Erstellung neuer orchestrierter Kampagnen wiederverwendet werden können. Geben Sie in diesem Bildschirm das Label der Vorlage für orchestrierte Kampagnen ein und konfigurieren Sie die zugehörigen Einstellungen wie den internen Namen, den Ordner und die Ausführungsordner, die Zeitzone und die Gruppe der Verantwortlichen."

Vorlagen für orchestrierte Kampagnen enthalten vorkonfigurierte Einstellungen und Aktivitäten, die zur Erstellung neuer orchestrierter Kampagnen wiederverwendet werden können. Sie können bei der Erstellung einer orchestrierten Kampagne die Vorlage der orchestrierten Kampagne in den Eigenschaften der orchestrierten Kampagne auswählen. Standardmäßig wird eine leere Vorlage bereitgestellt.

Sie können eine Vorlage aus einer vorhandenen orchestrierten Kampagne erstellen oder eine neue Vorlage von Grund auf neu erstellen. Beide Methoden werden nachfolgend beschrieben.

>[!BEGINTABS]

>[!TAB Erstellen Sie eine Vorlage aus einer vorhandenen orchestrierten Kampagne]

Gehen Sie wie folgt vor, um eine orchestrierte Kampagnenvorlage aus einer vorhandenen orchestrierten Kampagne zu erstellen:

1. Öffnen Sie das Menü **Kampagne** und navigieren Sie zur orchestrierten Kampagne, um sie als Vorlage zu speichern.
1. Klicken Sie auf die drei Punkte rechts neben dem Namen der orchestrierten Kampagne und wählen Sie **Als Vorlage kopieren**.
1. Bestätigen Sie im Popup-Fenster die Vorlagenerstellung.
1. Markieren, fügen Sie die Aktivitäten auf der Arbeitsfläche der orchestrierten Kampagnenvorlage nach Bedarf hinzu und konfigurieren Sie sie.
1. Navigieren Sie über die Schaltfläche **Einstellungen** zum Namen der orchestrierten Kampagnenvorlage und geben Sie eine Beschreibung ein.
1. Wählen Sie den **Ordner** und den **Ausführungsordner** der Vorlage aus. Der Ordner ist der Speicherort, an dem die orchestrierte Kampagnenvorlage gespeichert wird. Der Ausführungsordner ist der Ordner, in dem die auf dieser Vorlage basierenden orchestrierten Kampagnen gespeichert werden.
1. Speichern Sie Ihre Änderungen.

Die orchestrierte Kampagnenvorlage ist jetzt in der Vorlagenliste verfügbar. Sie können eine auf dieser Vorlage basierende orchestrierte Kampagne erstellen. Diese orchestrierte Kampagne wird mit den in der Vorlage definierten Einstellungen und Aktivitäten vorkonfiguriert.


>[!TAB Erstellen einer Vorlage von Grund auf]


Gehen Sie wie folgt vor, um eine neue orchestrierte Kampagnenvorlage zu erstellen:

1. Öffnen Sie das Menü **Kampagne** und navigieren Sie zur Registerkarte **Vorlagen**. Eine Liste der verfügbaren orchestrierten Kampagnenvorlagen wird angezeigt.
1. Klicken Sie auf **[!UICONTROL Vorlage erstellen]** in der rechten oberen Ecke des Bildschirms.
1. Geben Sie den Titel ein und öffnen Sie die zusätzlichen Optionen, um eine Beschreibung Ihrer orchestrierten Kampagnenvorlage einzugeben.
1. Wählen Sie den Ordner und den Ausführungsordner der Vorlage aus. Der Ordner ist der Speicherort, an dem die orchestrierte Kampagnenvorlage gespeichert wird. Der Ausführungsordner ist der Ordner, in dem die auf dieser Vorlage basierenden orchestrierten Kampagnen gespeichert werden.
1. Klicken Sie anschließend auf die Schaltfläche **Erstellen**, um Ihre Einstellungen zu bestätigen.
1. Fügen Sie auf der Arbeitsfläche für orchestrierte Kampagnenvorlagen die Aktivitäten nach Bedarf hinzu und konfigurieren Sie sie.

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. Speichern Sie Ihre Änderungen.

Die orchestrierte Kampagnenvorlage ist jetzt in der Vorlagenliste verfügbar. Sie können eine auf dieser Vorlage basierende orchestrierte Kampagne erstellen. Diese orchestrierte Kampagne wird mit den in der Vorlage definierten Einstellungen und Aktivitäten vorkonfiguriert.

>[!ENDTABS]
