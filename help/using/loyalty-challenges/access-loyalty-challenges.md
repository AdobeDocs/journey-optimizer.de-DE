---
solution: Journey Optimizer
product: journey optimizer
title: Zugriff und Verwaltung von Herausforderungen und Aufgaben
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer auf Herausforderungen und Aufgaben im Zusammenhang mit Treueprogrammen zugreifen, diese verwalten und organisieren können.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
source-git-commit: 94b553b19dbb0ba3020979fa710c2c35af237816
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 3%

---


# Zugriff und Verwaltung von Herausforderungen und Aufgaben {#access-loyalty-challenges}

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md) - Übersicht, Workflow, Voraussetzungen
* **Zugriff und Verwaltung von Herausforderungen und Aufgaben** ◀︎ **Sie sind hier** - Inventar-, Challenge- und Aufgabenverwaltung
* [Herausforderungen erstellen](create-challenges.md) - Herausforderungen aufbauen und konfigurieren
* [Aufgaben erstellen](create-tasks.md) - Herausforderungen definieren

>[!ENDSHADEBOX]

## Zugriff und Verwaltung von Herausforderungen und Aufgaben

Um auf die Herausforderungen im Zusammenhang mit dem Treueprogramm zuzugreifen, navigieren Sie zu Journey Optimizer und wählen **[!UICONTROL Treueprogramm (Beta)]** im Abschnitt **[!UICONTROL Journey-]** aus. Die Benutzeroberfläche für Herausforderungen im Zusammenhang mit dem Treueprogramm bietet einen zentralen Ort zum Anzeigen, Verwalten und Organisieren aller Herausforderungen und Aufgaben.

Die Benutzeroberfläche bietet Zugriff auf zwei Hauptinventare:

* **Herausforderungen**: Anzeigen und Verwalten aller Herausforderungen im Zusammenhang mit dem Treueprogramm, Überwachen des Status und Ausführen schneller Aktionen wie das Anzeigen, Bearbeiten, Duplizieren oder Löschen von Herausforderungen
* **Aufgaben**: Durchsuchen Sie wiederverwendbare Aufgaben, die für mehrere Herausforderungen verwendet werden können, und verwalten Sie Aufgabendefinitionen unabhängig voneinander


## Herausforderungen-Inventar {#challenges-tab}

Auf **[!UICONTROL Registerkarte]** Herausforderungen“ werden alle Herausforderungen nach dem Datum der letzten Änderung sortiert angezeigt, wobei die zuletzt geänderten Herausforderungen zuerst angezeigt werden.

![](assets/challenges-inventory.png)

Wichtige angezeigte Informationen:

* **[!UICONTROL State]**: Aktueller Status der Herausforderung (Entwurf oder veröffentlicht)
* **[!UICONTROL Aufgaben]**: Anzahl der in der Herausforderung konfigurierten Aufgaben
* **[!UICONTROL Journey]**: Link zur automatisch generierten Journey, die mit der Challenge verknüpft ist
* **[!UICONTROL Status]**: Aktueller Status der zugehörigen Journey (Entwurf, Live, Angehalten usw.)
* **[!UICONTROL Start-/Enddatum (UTC)]**: Wenn die Challenge aktiv wird und abläuft

Auf der Registerkarte Herausforderungen können Sie Aktionen für Herausforderungen durchführen:

* **Herausforderung anzeigen**: Wählen Sie den Namen der Herausforderung aus, um ihre Detailseite zu öffnen
* **Herausforderung duplizieren**: Wählen Sie das ![](assets/do-not-localize/Smock_More_18_N.svg) und dann **[!UICONTROL Duplizieren]**. Es wird eine Kopie erstellt, in der alle Aufgaben, Inhalte und Nachrichten intakt sind.
* **Herausforderung löschen**: Wählen Sie das ![](assets/do-not-localize/Smock_More_18_N.svg) und wählen Sie **[!UICONTROL Löschen]**
* **Herausforderung bearbeiten**: Wählen Sie den Namen der Herausforderung aus, um die zugehörige Detailseite zu öffnen und zu bearbeiten.

  Wenn Sie eine veröffentlichte Herausforderung zur Bearbeitung öffnen, müssen Sie sie zunächst in den Status „Entwurf“ zurücksetzen. Alle Anpassungen, die direkt an der automatisch generierten Journey vorgenommen werden, gehen verloren. Nachdem Sie Ihre Änderungen vorgenommen haben, speichern und veröffentlichen Sie die Challenge erneut und veröffentlichen Sie die zugehörige Journey erneut.

  >[!IMPORTANT]
  >
  >Eine veröffentlichte Herausforderung kann nicht rückgängig gemacht werden. Berücksichtigen Sie die Auswirkungen auf Ihre aktive Journey, bevor Sie fortfahren.

## Aufgaben-Inventar {#tasks-tab}

Auf der Registerkarte **[!UICONTROL Aufgaben]** werden alle wiederverwendbaren Aufgaben angezeigt, die für mehrere Herausforderungen verwendet werden können. Hier erstellte Aufgaben stehen beim Erstellen oder Bearbeiten einer Herausforderung zur Auswahl.

![](assets/tasks-inventory.png)

Wichtige angezeigte Informationen:

* **[!UICONTROL Beschreibung]**: Kurze Beschreibung dessen, was die Aufgabe erfordert
* **[!UICONTROL Aufgabenaktivität]**: Art der Aktivität (Kauf, Ausgaben)
* **[!UICONTROL SKU]**: Mögliche und/oder ausgeschlossene Elemente
* **[!UICONTROL In Herausforderungen verwendet]**: Anzahl der Herausforderungen, die derzeit diese Aufgabe verwenden

Auf der Registerkarte Aufgaben können Sie Aktionen für Aufgaben durchführen:

* **Aufgabe anzeigen/bearbeiten**: Wählen Sie den Aufgabennamen aus, um die vollständige Konfiguration anzuzeigen und die Aufgabe zu bearbeiten
* **Aufgabe duplizieren**: Wählen Sie das ![](assets/do-not-localize/Smock_More_18_N.svg) und dann **[!UICONTROL Duplizieren]**
* **Aufgabe löschen**: Wählen Sie das ![](assets/do-not-localize/Smock_More_18_N.svg) und klicken Sie auf **[!UICONTROL Löschen]**
