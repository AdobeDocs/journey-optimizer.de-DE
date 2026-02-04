---
solution: Journey Optimizer
product: journey optimizer
title: Herausforderungen im Zusammenhang mit Treue aufrufen und verwalten
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer auf Herausforderungen und Aufgaben im Zusammenhang mit Treueprogrammen zugreifen, diese verwalten und organisieren können.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 3%

---


# Herausforderungen im Zusammenhang mit Treue aufrufen und verwalten {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md) - Übersicht, Workflow, Voraussetzungen
* **Zugriff auf Herausforderungen der Treue** ◀︎ **Sie sind hier** - Inventar-, Herausforderungen- und Aufgabenverwaltung
* [Herausforderungen erstellen](create-challenges.md) - Herausforderungen aufbauen und konfigurieren
* [Aufgaben erstellen](create-tasks.md) - Herausforderungen definieren

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

## Zugang zu loyalen Herausforderungen

Um auf die Herausforderungen im Zusammenhang mit dem Treueprogramm zuzugreifen, navigieren Sie zu Journey Optimizer und wählen **[!UICONTROL Treueprogramm (Beta)]** im Abschnitt **[!UICONTROL Journey-]** aus.

Die Benutzeroberfläche für Herausforderungen im Zusammenhang mit dem Treueprogramm bietet einen zentralen Ort zum Anzeigen, Verwalten und Organisieren aller Herausforderungen und Aufgaben. Sie können auf zwei Hauptinventare zugreifen:

* **Herausforderungen-Inventar**: Alle Herausforderungen im Zusammenhang mit der Treue anzeigen und verwalten, ihren Status überwachen und schnelle Aktionen durchführen
* **Aufgabeninventar**: Durchsuchen wiederverwendbarer Aufgaben, die für mehrere Herausforderungen verwendet werden können

## Herausforderungen-Inventar {#challenges-tab}

Auf **[!UICONTROL Registerkarte]** Herausforderungen“ werden alle Herausforderungen nach dem Datum der letzten Änderung sortiert angezeigt, wobei die zuletzt geänderten Herausforderungen zuerst angezeigt werden.

![](assets/challenges-inventory.png)

Wichtige angezeigte Informationen:

* **[!UICONTROL Challenge]**: Challenge-Name
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

  Wenn Sie eine veröffentlichte Herausforderung zur Bearbeitung öffnen, müssen Sie sie zunächst auf den Status Entwurf zurücksetzen:

   * Alle Anpassungen, die direkt an der automatisch generierten Journey vorgenommen werden, gehen verloren
   * Die Herausforderung kehrt zum Status Entwurf zurück
   * Nachdem Sie Ihre Änderungen vorgenommen haben, müssen Sie die Herausforderung speichern und erneut veröffentlichen
   * Sie müssen die zugehörige Journey erneut veröffentlichen, um die aktualisierte Challenge für Kunden verfügbar zu machen

  >[!IMPORTANT]
  >
  >Eine veröffentlichte Herausforderung kann nicht rückgängig gemacht werden. Berücksichtigen Sie die Auswirkungen auf Ihre aktive Journey, bevor Sie fortfahren.

## Aufgaben-Inventar {#tasks-tab}

Auf der Registerkarte **[!UICONTROL Aufgaben]** werden alle wiederverwendbaren Aufgaben angezeigt, die für mehrere Herausforderungen verwendet werden können. Hier erstellte Aufgaben stehen beim Erstellen oder Bearbeiten einer Herausforderung zur Auswahl.

![](assets/tasks-inventory.png)

Wichtige angezeigte Informationen:

* **[!UICONTROL Aufgabenname]**: Der Name, den Sie der Aufgabe zugewiesen haben
* **[!UICONTROL Beschreibung]**: Kurze Beschreibung dessen, was die Aufgabe erfordert
* **[!UICONTROL Aufgabenaktivität]**: Art der Aktivität (Kauf, Ausgaben)
* **[!UICONTROL SKU]**: Mögliche und/oder ausgeschlossene Elemente
* **[!UICONTROL In Herausforderungen verwendet]**: Anzahl der Herausforderungen, die derzeit diese Aufgabe verwenden

Auf der Registerkarte Aufgaben können Sie Aktionen für Aufgaben durchführen:

* **Aufgabe anzeigen/bearbeiten**: Aufgabennamen auswählen, um die vollständige Konfiguration anzuzeigen und die Aufgabe zu bearbeiten
* **Aufgabe duplizieren**: Wählen Sie das ![](assets/do-not-localize/Smock_More_18_N.svg) und dann **[!UICONTROL Duplizieren]**
* **Aufgabe löschen**: Wählen Sie das ![](assets/do-not-localize/Smock_More_18_N.svg) und klicken Sie auf **[!UICONTROL Löschen]**
