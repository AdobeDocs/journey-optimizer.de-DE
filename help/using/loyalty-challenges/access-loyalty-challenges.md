---
solution: Journey Optimizer
product: journey optimizer
title: Herausforderungen beim Treueprogramm
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer auf Herausforderungen im Zusammenhang mit der Treue zugreifen, diese durchsuchen und filtern können.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 2%

---


# Herausforderungen beim Treueprogramm {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md) - Übersicht, Workflow, Voraussetzungen
* **Herausforderungen im Zusammenhang mit Treueprogrammen** ◀︎ **Sie sind hier** - Inventar und Filterung
* [Herausforderungen erstellen](create-challenges.md) - Herausforderungen aufbauen und konfigurieren
* [Aufgaben erstellen](create-tasks.md) - Herausforderungen definieren
* [Herausforderungen verwalten](manage-challenges.md) - Bearbeiten, Überwachen, Optimieren

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

## Zugriff auf das Inventar der Herausforderungen im Treueprogramm {#access-inventory}

<!-- SCREENSHOT: Journey Optimizer main menu showing "Loyalty challenges" under "Customer journeys" section -->

Um auf die Herausforderungen im Zusammenhang mit dem Treueprogramm zuzugreifen, gehen Sie zu Journey Optimizer und wählen **[!UICONTROL Herausforderungen im Zusammenhang mit dem Treueprogramm]** im Abschnitt **[!UICONTROL Journey]** aus.

<!-- SCREENSHOT: Loyalty Challenges landing page showing the two tabs: Challenges and Tasks -->

Die Seite Herausforderungen im Zusammenhang mit dem Treueprogramm wird mit zwei Registerkarten angezeigt:

* **[!UICONTROL Challenges]**: Alle Herausforderungen im Zusammenhang mit der Treue anzeigen und verwalten

* **[!UICONTROL Aufgaben]**: Alle Aufgaben, die über Herausforderungen hinweg wiederverwendet werden können, anzeigen und verwalten

## Herausforderungen-Inventar {#challenges-tab}

<!-- SCREENSHOT: Challenges tab showing the inventory table with columns: Challenge name, Status, Type, Start date, End date, Created by, Last modified, Tags -->

Auf der Registerkarte Challenges werden alle Challenges sortiert nach dem Datum der letzten Änderung angezeigt, wobei die zuletzt geänderten Challenges zuerst erscheinen. Daraufhin werden die folgenden Informationen angezeigt:

* **[!UICONTROL Challenge name]**: Der Name, den Sie der Challenge zugewiesen haben
* **[!UICONTROL Status]**: Aktueller Status der Herausforderung (siehe Statusbeschreibungen unten)
* **[!UICONTROL type]**: Challenge-Typ (Standard, Streak oder sequenziell)
* **[!UICONTROL Startdatum]**: Wenn die Challenge aktiv wird
* **[!UICONTROL Enddatum]**: Wenn die Challenge abläuft
* **[!UICONTROL Erstellt von]**: Benutzer, der die Herausforderung erstellt hat
* **[!UICONTROL Zuletzt geändert]**: Datum und Uhrzeit der letzten Änderung
* **[!UICONTROL Tags]**: Alle Tags, die auf die Herausforderung für die Organisation angewendet werden

### Status der Herausforderung {#challenge-statuses}

<!-- VISUAL: Status badges showing different challenge statuses with color coding: Draft (gray), Scheduled (blue), Live (green), Completed (gray), Stopped (red), Archived (gray) -->

Herausforderungen werden mit verschiedenen Status angezeigt, die ihren aktuellen Status im Lebenszyklus angeben:

* **Entwurf**: Herausforderung wird erstellt oder bearbeitet
* **Geplant**: Die Herausforderung wird veröffentlicht und am Startdatum aktiv.
* **Live**: Challenge ist aktiv und Kunden können teilnehmen
* **Abgeschlossen**: Enddatum der Herausforderung wurde überschritten oder die Ziele wurden erreicht
* **Angehalten**: Die Herausforderung wurde vor dem Abschluss manuell angehalten
* **Archiviert**: Die Herausforderung wurde zu Organisationszwecken archiviert

Detaillierte Informationen zu Statusübergängen und dem Challenge-Lebenszyklus finden Sie unter [Challenge-Lebenszyklus](manage-challenges.md#challenge-lifecycle).

### Herausforderungen beim Suchen und Filtern {#search-challenges}

<!-- SCREENSHOT: Search bar and filter panel showing available filters (status, type, dates, tags) with an example of active filters applied -->

Mithilfe von Suche und Filtern können Sie Herausforderungen schnell finden:

**Suche:**

* Verwenden Sie die Suchleiste, um Herausforderungen zu finden, indem Sie Schlüsselwörter aus dem Namen oder der Beschreibung der Herausforderung eingeben. Die Suche aktualisiert die Ergebnisse während der Eingabe in Echtzeit.

**Filter:**

* Einen oder mehrere Filter anwenden, um die Ergebnisse einzugrenzen:
   * **Status**: Filtern nach Challenge-Status (Entwurf, Geplant, Live, Abgeschlossen, Gestoppt, Archiviert)
   * **Type**: Filtern nach Challenge-Typ (Standard, Streak, Sequential)
   * **Datumsangaben**: Filtern nach Startdatum oder Enddatumsbereichen
   * **Tags**: Filtern nach Tags, die auf Herausforderungen angewendet werden

Sie können mehrere Filter gleichzeitig kombinieren. Filtern Sie beispielsweise nach Live-Standard-Herausforderungen mit dem Tag „Sommer 2024“, um aktive saisonale Kampagnen schnell zu finden.

Um Filter zu löschen, wählen Sie **[!UICONTROL Alle löschen]** oder entfernen Sie einzelne Filter.

### Ergreifung von Maßnahmen zur Bewältigung von Herausforderungen {#inventory-actions}

<!-- SCREENSHOT: More actions menu (three dots) expanded showing options: Edit, Duplicate, Stop, Archive, Delete -->

Auf der Registerkarte Herausforderungen können Sie schnelle Aktionen für Herausforderungen durchführen:

* **Challenge-Details anzeigen**: Wählen Sie den Challenge-Namen aus, um die Detailseite zu öffnen
* **Herausforderung bearbeiten**: Wählen Sie das Menü **[!UICONTROL Mehr Aktionen]** (drei Punkte) und wählen Sie **[!UICONTROL Bearbeiten]**
* **Herausforderung duplizieren**: Wählen Sie das Menü **[!UICONTROL Mehr Aktionen]** und wählen Sie **[!UICONTROL Duplizieren]**
* **Live-Herausforderung anhalten**: Wählen Sie das Menü **[!UICONTROL Mehr Aktionen]** und wählen Sie **[!UICONTROL Anhalten]**
* **Herausforderung archivieren**: Wählen Sie das Menü **[!UICONTROL Mehr Aktionen]** und wählen Sie **[!UICONTROL Archivieren]**
* **Herausforderung „Entwurf löschen**: Wählen Sie das Menü **[!UICONTROL Mehr Aktionen]** und wählen Sie **[!UICONTROL Löschen]** (nur für Entwürfe verfügbar)

Detaillierte Informationen zum Verwalten von Herausforderungen nach der Erstellung, einschließlich Bearbeitungsbeschränkungen, Duplizierungsstrategien, Leistungsüberwachung und Fehlerbehebung, finden Sie unter [Verwalten von Herausforderungen](manage-challenges.md).

## Aufgaben-Inventar {#tasks-tab}

<!-- SCREENSHOT: Tasks tab showing the inventory table with columns: Task name, Task type, Description, Created by, Last modified, Used in challenges -->

Auf der Registerkarte Aufgaben werden alle wiederverwendbaren Aufgaben angezeigt, die über mehrere Herausforderungen hinweg verwendet werden können. Hier erstellte Aufgaben stehen beim Erstellen oder Bearbeiten einer Herausforderung zur Auswahl.

Das Aufgabeninventar zeigt die folgenden Informationen an:

* **[!UICONTROL Aufgabenname]**: Der Name, den Sie der Aufgabe zugewiesen haben
* **[!UICONTROL Aufgabentyp]**: Aktionstyp (Kauf, Ausgabenbetrag, Besuch, Interaktion, benutzerspezifisches Ereignis)
* **[!UICONTROL Beschreibung]**: Kurze Beschreibung dessen, was die Aufgabe erfordert
* **[!UICONTROL Erstellt von]**: Benutzer, der die Aufgabe erstellt hat
* **[!UICONTROL Zuletzt geändert]**: Datum und Uhrzeit der letzten Änderung
* **[!UICONTROL In Herausforderungen verwendet]**: Anzahl der Herausforderungen, die derzeit diese Aufgabe verwenden

### Ausführen von Aktionen für Aufgaben {#tasks-actions}

Auf der Registerkarte Aufgaben können Sie Aktionen für Aufgaben durchführen:

* **Aufgabendetails anzeigen**: Aufgabennamen auswählen, um die vollständige Konfiguration anzuzeigen
* **Aufgabe bearbeiten**: Wählen Sie das Menü **[!UICONTROL Mehr Aktionen]** (drei Punkte) und wählen Sie **[!UICONTROL Bearbeiten]**
* **Aufgabe duplizieren**: Wählen Sie das Menü **[!UICONTROL Mehr Aktionen]** und klicken Sie auf **[!UICONTROL Duplizieren]**
* **Aufgabe löschen**: Wählen Sie das Menü **[!UICONTROL Mehr Aktionen]** und wählen Sie **[!UICONTROL Löschen]** (nur, wenn es nicht in einer aktiven Herausforderung verwendet wird)
* **Nutzung anzeigen**: Ermitteln Sie, welche Herausforderungen derzeit die Aufgabe verwenden

## Nächste Schritte {#next-steps}

Jetzt, da Sie wissen, wie Sie auf das Inventar der Herausforderungen im Treueprogramm zugreifen und darin navigieren können:

* [Herausforderungen erstellen](create-challenges.md) - Erfahren Sie, wie Sie Ihre erste Herausforderung erstellen und Aufgaben konfigurieren
* [Aufgaben erstellen](create-tasks.md) - Erfahren Sie, wie Sie wiederverwendbare Aufgaben für Herausforderungen definieren.
* [Herausforderungen verwalten](manage-challenges.md) - Erfahren Sie, wie Sie Herausforderungen bearbeiten, überwachen und optimieren können.
