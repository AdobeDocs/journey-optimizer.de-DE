---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren der Einstellungen für eine mehrstufige Kampagne
description: Erfahren Sie, wie Sie mehrstufige Kampagneneinstellungen mit Adobe Journey Optimizer konfigurieren
hide: true
hidefromtoc: true
exl-id: a9bb3782-a4d1-43fe-ae2a-aef3f17ba588
source-git-commit: 323472ef9d6203cbbadc44ceb17ddcc7f6207323
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 41%

---

# Konfigurieren der Einstellungen für eine mehrstufige Kampagne {#workflow-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_creation_properties"
>title="Eigenschaften mehrstufiger Kampagnen"
>abstract="Wählen Sie in diesem Bildschirm die Vorlage aus, die zum Erstellen der Komposition verwendet werden soll, und geben Sie einen Titel an. Erweitern Sie den Abschnitt **Zusätzliche Optionen**, um weitere Einstellungen wie den internen Namen der mehrstufigen Kampagne, ihre Ordner, die Zeitzone und die Gruppe der Verantwortlichen zu konfigurieren. Es wird dringend empfohlen, eine Gruppe von Verantwortlichen auszuwählen, damit Benutzerinnen und Benutzer benachrichtigt werden, wenn Fehler auftreten."

Bei der Erstellung einer mehrstufigen Kampagne oder der Orchestrierung mehrstufiger Kampagnenaktivitäten auf der Arbeitsfläche können Sie auf die erweiterten Einstellungen für die mehrstufige Kampagne zugreifen. Sie können beispielsweise eine bestimmte Zeitzone für die mehrstufige Kampagne festlegen, verwalten, wie sich die mehrstufige Kampagne im Fehlerfall verhält, oder die Verzögerung verwalten, nach der der mehrstufige Kampagnenverlauf bereinigt werden soll.

Diese Einstellungen sind in der bei der Erstellung der mehrstufigen Kampagne ausgewählten Vorlage vorkonfiguriert, können jedoch bei Bedarf für diese spezifische mehrstufige Kampagne bearbeitet werden.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

## Eigenschaften mehrstufiger Kampagnen {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="Eigenschaften mehrstufiger Kampagnen"
>abstract="Dieser Abschnitt enthält allgemeine Eigenschaften für mehrstufige Kampagnen, auf die auch beim Erstellen der mehrstufigen Kampagne zugegriffen werden kann. Sie können die Vorlage auswählen, die zum Erstellen der mehrstufigen Kampagne verwendet werden soll, und einen Titel angeben. Erweitern Sie den Abschnitt „zusätzliche Optionen“, um bestimmte Einstellungen zu konfigurieren, z. B. den Ordner, in dem die mehrstufige Kampagne gespeichert wird, oder die Zeitzone."

Der Abschnitt **[!UICONTROL Eigenschaften]** enthält allgemeine Einstellungen, die beim Erstellen einer mehrstufigen Kampagne konfiguriert werden können. Um auf die Eigenschaften einer bestehenden mehrstufigen Kampagne zuzugreifen, klicken Sie auf die Schaltfläche **[!UICONTROL Einstellungen]**, die in der Aktionsleiste über der mehrstufigen Kampagnen-Arbeitsfläche verfügbar ist.


![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}


Diese Eigenschaften sind:

* Der **[!UICONTROL Titel]** der mehrstufigen Kampagne, die in der Liste angezeigt wird.
* Der **[!UICONTROL Interne Name]** der mehrstufigen Kampagne.
* Der **[!UICONTROL Ordner]** in dem die mehrstufige Kampagne gespeichert werden soll.
* Die Standardeinstellung **[!UICONTROL Zeitzone]**, die bei allen Aktivitäten der mehrstufigen Kampagne verwendet werden soll. Standardmäßig ist die Zeitzone der mehrstufigen Kampagne die für den aktuellen Campaign-Benutzer definierte Zeitzone.
Mögliche Werte sind:
   * **Server-Zeitzone**, um die Zeitzone Ihres Adobe Experience Platform-Unternehmens zu verwenden
   * **Benutzer-Zeitzone** nutzt die Zeitzone des Benutzers, der die mehrstufige Kampagne ausführt
   * **Zeitzone der Datenbank**, um die Zeitzone des Datenbank-Servers zu verwenden.
   * Eine bestimmte Zeitzone
* Wenn eine mehrstufige Kampagne fehlschlägt, werden die Benutzer, die zur Benutzergruppe gehören, die im Feld **[!UICONTROL Verantwortliche(r)) ausgewählt]**, per E-Mail benachrichtigt.
* Sie können auch eine **[!UICONTROL Beschreibung]** Ihrer mehrstufigen Kampagne eingeben.

## Segmentierungseinstellungen  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Segmentierungseinstellungen"
>abstract="In diesem Bereich können Sie die Zielgruppendimension auswählen, um Profile in der mehrstufigen Kampagne auszuwählen, und entscheiden, ob die Workflow-Ergebnisse zwischen zwei Ausführungen beibehalten werden sollen. Diese Option sollte nur zu Testzwecken verwendet werden und darf nie in einer mehrstufigen Produktionskampagne aktiviert werden."

* **[!UICONTROL Zielgruppendimension]**: Wählen Sie die Zielgruppendimension aus, die für die Zielgruppenbestimmung von Profilen verwendet werden soll: Empfängerinnen und Empfänger, Vertragsbegünstigte, Benutzerinnen und Benutzer, Abonnentinnen und Abonnenten usw.

* **[!UICONTROL Zwischen zwei Ausführungen die ermittelte Population festhalten]**: Standardmäßig werden nur die Arbeitstabellen der letzten Ausführung der mehrstufigen Kampagne beibehalten. Arbeitstabellen früherer Ausführungen werden durch eine technische mehrstufige Kampagne bereinigt, die täglich ausgeführt wird.

  Wenn diese Option aktiviert ist, werden Arbeitstabellen auch nach Ausführung der mehrstufigen Kampagne beibehalten. Sie können sie zu Testzwecken verwenden. Daher farf sie **nur** in Entwicklungs- oder Staging-Umgebungen genutzt werden. Sie darf nie in einer mehrstufigen Produktionskampagne aktiviert werden.

## Ausführungseinstellungen  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="Ausführungseinstellungen"
>abstract="In diesem Abschnitt können Sie die Einstellungen für die Ausführung des Workflows konfigurieren, beispielsweise für wie viele Tage der Verlauf der mehrstufigen Kampagne gespeichert wird."

* **[!UICONTROL Verlauf in Tagen]**: Gibt die Anzahl der Tage an, nach denen der Verlauf bereinigt werden muss. Der Verlauf enthält Elemente im Zusammenhang mit der mehrstufigen Kampagne: Protokolle, Aufgaben, Ereignisse (technische Objekte, die mit dem mehrstufigen Kampagnenvorgang verknüpft sind). Der Standardwert bei nativen mehrstufigen Kampagnenvorlagen beträgt 30 Tage. Die Bereinigung des Verlaufs erfolgt durch die mehrstufige technische Kampagne für die Datenbankbereinigung, die standardmäßig täglich ausgeführt wird

  >[!IMPORTANT]
  >
  >Wenn das Feld **[!UICONTROL Verlauf in Tagen]** leer gelassen wird, wird sein Wert als „1“ betrachtet; der Verlauf wird also nach einem Tag bereinigt.

* **[!UICONTROL Standardaffinität]**: Wenn Ihre Installation mehrere mehrstufige Kampagnenserver umfasst, geben Sie in diesem Feld den Server an, auf dem die mehrstufige Kampagne ausgeführt wird. Dies erzwingt die Ausführung dieser mehrstufigen Kampagne auf einem bestimmten Server. Sie können einen beliebigen vorhandenen Affinitätsnamen auswählen. Stellen Sie jedoch sicher, dass Sie keine Leerzeichen oder Satzzeichen verwenden. Wenn Sie verschiedene Server verwenden, geben Sie unterschiedliche Namen an, getrennt durch Kommas.

  >[!IMPORTANT]
  >
  >Wenn der in diesem Feld definierte Wert auf keinem Server vorhanden ist, bleibt die mehrstufige Kampagne ausstehend.


* **[!UICONTROL SQL-Abfragen im Protokoll speichern]**: Aktivieren Sie diese Option, um die SQL-Abfragen aus der mehrstufigen Workflow-Kampagne jetzt in den Protokollen zu speichern. Diese Funktion ist erfahrenen Benutzerinnen und Benutzern vorbehalten. Sie gilt für mehrstufige Kampagnen, die Zielgruppenbestimmungsaktivitäten enthalten, wie **[!UICONTROL Zielgruppe aufbauen]**. Wenn diese Option aktiviert ist, werden die SQL-Abfragen, die während der mehrstufigen Kampagnenausführung an die Datenbank gesendet werden, in den Protokollen der mehrstufigen Kampagne angezeigt, sodass Sie sie analysieren können, um Abfragen zu optimieren oder Probleme zu diagnostizieren.

## Einstellungen für den Umgang mit Fehlern  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Einstellungen für den Umgang mit Fehlern"
>abstract="In diesem Abschnitt können Sie definieren, wie die mehrstufige Kampagne mit Fehlern während ihrer Ausführung umgehen soll. Sie können festlegen, dass der Prozess angehalten werden soll, dass eine bestimmte Anzahl von Fehlern ignoriert werden soll oder dass die Ausführung der mehrstufigen Kampagne gestoppt werden soll."

* **[!UICONTROL Umgang mit Fehlern]** In diesem Feld können Sie festlegen, welche Aktionen ausgeführt werden sollen, wenn eine mehrstufige Kampagnenaufgabe Fehler aufweist. Es gibt drei mögliche Optionen:

   * **[!UICONTROL Prozess aussetzen]**: Die mehrstufige Kampagne wird automatisch ausgesetzt und ihr Status ändert sich in **[!UICONTROL Fehlgeschlagen]**. Sobald das Problem behoben ist, setzen Sie die mehrstufige Kampagne mit der Schaltfläche **[!UICONTROL Fortsetzen]** fort.
   * **[!UICONTROL Ignorieren]**: Der Status der Aufgabe, die den Fehler ausgelöst hat, ändert sich in **[!UICONTROL Fehlgeschlagen]** aber die mehrstufige Kampagne behält den Status **[!UICONTROL Gestartet]**. <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Prozess abbrechen]**: Die mehrstufige Kampagne wird automatisch angehalten und ihr Status ändert sich in **[!UICONTROL Fehlgeschlagen]**. Sobald das Problem behoben ist, starten Sie die mehrstufige Kampagne mithilfe der Schaltflächen **[!UICONTROL Starten]** neu.

* **[!UICONTROL Aufeinanderfolgende Fehler]**: Dieses Feld wird verfügbar, wenn im Feld **[!UICONTROL Im Fehlerfall]** der Wert **[!UICONTROL Ignorieren]** ausgewählt wurde. Sie können die Anzahl der Fehler angeben, die ignoriert werden können, bevor der Prozess angehalten wird. Sobald diese Zahl erreicht ist, ändert sich der mehrstufige Kampagnenstatus in **[!UICONTROL Fehlgeschlagen]**. Wenn der Wert dieses Felds 0 ist, wird die mehrstufige Kampagne unabhängig von der Fehleranzahl nie angehalten.

## Initialisierungsskript {#initialization-script}

Mit dem **Initialisierungsskript** können Sie Variablen initialisieren oder Aktivitätseigenschaften ändern. Klicken Sie auf die Schaltfläche **Code bearbeiten** und geben Sie den auszuführenden Code-Ausschnitt ein. Das Skript wird aufgerufen, wenn die mehrstufige Kampagne ausgeführt wird. Weitere Informationen finden Sie im Abschnitt zu den [Ereignisvariablen](event-variables.md).
