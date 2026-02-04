---
solution: Journey Optimizer
product: journey optimizer
title: Herausforderungen im Zusammenhang mit Treueprogrammen bewältigen
description: Erfahren Sie, wie Sie die Herausforderungen im Zusammenhang mit Treueprogrammen in Adobe Journey Optimizer verwalten, überwachen und optimieren können.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 2%

---


# Herausforderungen bewältigen {#manage-challenges}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md) - Übersicht, Workflow, Voraussetzungen
* [Herausforderungen im Zusammenhang mit Treueprogrammen](access-loyalty-challenges.md) - Inventar und Filterung
* [Herausforderungen erstellen](create-challenges.md) - Herausforderungen aufbauen und konfigurieren
* [Aufgaben erstellen](create-tasks.md) - Herausforderungen definieren
* **Herausforderungen verwalten** ◀︎ **Sie sind hier** - Bearbeiten, Überwachen, Optimieren

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

## Herausforderungen bewältigen {#manage-challenges-section}

### Challenge-Lebenszyklus {#challenge-lifecycle}

<!-- VISUAL: Flowchart diagram showing challenge lifecycle with status transitions: Draft → Scheduled → Live → Completed/Stopped/Archived -->

Challenges durchlaufen verschiedene Status während ihres Lebenszyklus:

* **Entwurf**: Herausforderung wird erstellt oder bearbeitet und steht Kunden noch nicht zur Verfügung
* **Geplant**: Die Herausforderung wurde veröffentlicht und wird am angegebenen Startdatum automatisch aktiviert
* **Live**: Die Challenge ist derzeit aktiv und Kunden können teilnehmen
* **Abgeschlossen**: Herausforderung ist abgelaufen - entweder ist das Enddatum abgelaufen oder alle Ziele wurden erreicht
* **Angehalten**: Die Herausforderung wurde manuell angehalten, bevor der natürliche Abschluss erreicht wurde
* **Archiviert**: Die Herausforderung wurde zu Organisationszwecken archiviert und ist nicht mehr im Hauptbestand sichtbar

### Herausforderungen bearbeiten {#edit-challenges}

Herausforderungen können je nach ihrem aktuellen Status bearbeitet werden:

* **Entwurfsherausforderungen**: Vollständige Bearbeitungsfunktion - alle Eigenschaften können geändert werden
* **Geplante/Live-Herausforderungen**: Eingeschränkte Bearbeitung - Sie können Inhalte, Nachrichten aktualisieren und Datumsangaben verlängern, aber nicht die grundlegende Challenge-Struktur (Typ, Zielgruppe oder Aufgabendefinitionen) ändern

So bearbeiten Sie eine Challenge:

1. Navigieren Sie zur **[!UICONTROL Herausforderungen]** im Inventar „Herausforderungen im Treueprogramm“.

1. Suchen Sie die Herausforderung, die Sie bearbeiten möchten.

1. Wählen Sie den Namen der Herausforderung aus, um sie im Bearbeitungsmodus zu öffnen.

1. Nehmen Sie Ihre Änderungen basierend auf dem Challenge-Status vor:
   * **Entwurfsherausforderungen**: Ändern von Eigenschaften, Aufgaben, Inhalten oder Nachrichten
   * **Geplante/Live-Herausforderungen**: Aktualisieren von Inhaltskarten, Nachrichten oder Verlängern der Enddaten nach Bedarf

1. Speichern Sie Ihre Änderungen. Für geplante oder Live-Herausforderungen werden Änderungen sofort oder gemäß Ihrem Aktualisierungszeitplan wirksam.

>[!NOTE]
>
>Für Änderungen, die größere Änderungen erfordern (z. B. Änderung des Challenge-Typs, der Audience oder der Aufgabenstruktur), duplizieren Sie die Challenge und erstellen Sie eine neue Version, anstatt die vorhandene zu bearbeiten.

### Herausforderungen duplizieren {#duplicate-challenges}

Herausforderungen duplizieren an:

* Wiederholen erfolgreicher Challenges für neue Zeiträume
* Varianten für verschiedene Audiences erstellen
* Aufgabenanforderungen oder Belohnungen aktualisieren
* Reaktivieren gestoppter oder abgeschlossener Herausforderungen

Durch das Duplizieren einer Challenge wird eine exakte Kopie mit allen Aufgaben, Inhalten und Nachrichten erstellt, sodass Sie schnell neue Versionen erstellen können, ohne von Grund auf neu zu beginnen.

So duplizieren Sie eine Herausforderung:

1. Navigieren Sie zur **[!UICONTROL Herausforderungen]** im Inventar „Herausforderungen im Treueprogramm“.

1. Suchen Sie die Herausforderung, die Sie duplizieren möchten.

1. Wählen Sie das Menü Mehr Aktionen (drei Punkte) neben dieser Challenge.

1. Wählen Sie **[!UICONTROL Duplizieren]**.

1. Eine Kopie der Challenge wird erstellt, wobei &quot;[Copy] an den Namen angehängt wird.

1. Öffnen Sie die duplizierte Herausforderung und ändern Sie die erforderlichen Eigenschaften:
   * Challenge-Namen aktualisieren
   * Start- und Enddatum anpassen
   * Ändern der Zielgruppe bei Bedarf
   * Aufgaben, Belohnungen, Inhalte oder Nachrichten nach Bedarf ändern

1. Überprüfen und veröffentlichen Sie die duplizierte Herausforderung.

### Überwachen der Leistung {#monitor-performance}

<!-- SCREENSHOT: Challenge Performance tab showing key metrics dashboard with participation, completion, reward, and engagement metrics -->

Nachverfolgen der Challenge-Performance anhand von Schlüsselmetriken:

* **Teilnahmemetriken**:
   * Registrierung: Anzahl der Kunden, die an der Challenge teilgenommen haben
   * Aktive Teilnehmer: Kunden, die sich derzeit mit der Challenge beschäftigen
* **Abschlussmetriken**:
   * Abschlussraten: Prozentsatz der registrierten Kunden, die die Herausforderung abgeschlossen haben
   * Durchschnittliche Abschlusszeit: Durchschnittliche Dauer bis zum Abschluss aller Aufgaben
* **Belohnungsmetriken**:
   * Insgesamt verteilte Belohnungen: Gesamtwert aller gewährten Belohnungen
   * Belohnungen nach Art: Aufschlüsselung der Belohnungen nach Belohnungskategorie
* **Interaktionsmetriken**:
   * Impressionen von Inhaltskarten: Gibt an, wie oft die Karte mit den Herausforderungen angezeigt wurde
   * Nachrichtenversand: Anzahl der erfolgreich über alle Kanäle gesendeten Nachrichten

So greifen Sie auf Leistungsdaten zu:

1. Navigieren Sie zur **[!UICONTROL Herausforderungen]** im Inventar „Herausforderungen im Treueprogramm“.

1. Wählen Sie die Herausforderung aus, die Sie überwachen möchten.

1. Öffnen Sie die **[!UICONTROL Performance]**, um Echtzeit-Metriken und -Analysen anzuzeigen.

<!-- SCREENSHOT: Journey report showing challenge performance data with graphs and tables -->

Sie können auch in den [automatisch generierten Journey-Berichten](../reports/journey-global-report-cja.md) auf detaillierte Leistungsdaten zugreifen, die zusätzliche Einblicke und historische Trends bieten.

## Aufgaben verwalten {#manage-tasks}

Aufgaben sind wiederverwendbare Komponenten, die über mehrere Herausforderungen hinweg verwendet werden können. Die effektive Verwaltung von Aufgaben stellt die Konsistenz Ihres gesamten Treueprogramms sicher und erleichtert die zentrale Aktualisierung von Aufgabendefinitionen. Aufgaben, die in einer Challenge erstellt wurden, können in anderen Challenges wiederverwendet werden, wodurch Duplizierungen reduziert und die Standardisierung aufrechterhalten werden.

### Aufgaben bearbeiten {#edit-tasks}

Sie können vorhandene Aufgaben im Aufgabeninventar bearbeiten. Beachten Sie Folgendes:

* **Aufgaben werden nicht in aktiven Herausforderungen verwendet**: Können frei bearbeitet werden - alle Eigenschaften können ohne Auswirkungen geändert werden
* **Aufgaben, die in Live-Herausforderungen verwendet werden**: Seien Sie vorsichtig, da Änderungen sich auf alle Herausforderungen auswirken, die die Aufgabe verwenden. Änderungen gelten sofort für alle referenzierenden Herausforderungen

Aufgabe bearbeiten:

1. Navigieren Sie zur **[!UICONTROL Aufgaben]** im Inventar „Herausforderungen im Treueprogramm“.

1. Suchen Sie die Aufgabe, die Sie bearbeiten möchten.

1. Wählen Sie den Aufgabennamen aus, um ihn im Bearbeitungsmodus zu öffnen.

1. Ändern Sie die Aufgabeneigenschaften nach Bedarf:
   * Aufgabennamen oder -beschreibung aktualisieren
   * Aktivitätstyp oder Attribute ändern
   * Zulässige Elemente und Ausschlüsse anpassen
   * Menge oder Menge ändern Anforderungen

1. Speichern Sie Ihre Änderungen.

>[!WARNING]
>
>Beim Bearbeiten einer Aufgabe, die aktiv in Live-Challenges verwendet wird, sollten Sie ein Duplikat mit einer neuen Version erstellen, anstatt das Original zu ändern. Dadurch werden unbeabsichtigte Änderungen an aktiven Herausforderungen verhindert und Sie können Änderungen testen, bevor Sie sie anwenden.

### Aufgaben löschen {#delete-tasks}

Aufgaben können nur gelöscht werden, wenn sie derzeit in keiner Herausforderung verwendet werden. Vor dem Löschen einer Aufgabe:

* Überprüfen Sie die Anzahl **[!UICONTROL Verwendet in Herausforderungen]** im Aufgabeninventar
* Stellen Sie sicher, dass kein Entwurf, keine geplanten oder Live-Herausforderungen auf die Aufgabe verweisen

So löschen Sie eine Aufgabe

1. Navigieren Sie zur **[!UICONTROL Aufgaben]** im Inventar „Herausforderungen im Treueprogramm“.

1. Suchen Sie die Aufgabe, die Sie löschen möchten.

1. Überprüfen Sie, **[!UICONTROL die]** „Wird in Herausforderungen verwendet“ 0 anzeigt. Wenn die Anzahl größer als 0 ist, müssen Sie die Aufgabe zunächst aus allen Herausforderungen entfernen, bevor Sie sie löschen.

1. Wählen Sie das Menü Mehr Aktionen (drei Punkte) neben der Aufgabe.

1. Wählen Sie **[!UICONTROL Löschen]**.

1. Bestätigen Sie den Löschvorgang im Dialogfeld.

>[!NOTE]
>
>Wenn eine Aufgabe in einer Herausforderung verwendet wird (Entwurf, geplant oder live), muss sie zunächst aus allen Herausforderungen entfernt werden, bevor sie gelöscht werden kann. Wenn Sie Aufgaben in Zukunft benötigen, sollten Sie sie archivieren oder duplizieren, anstatt sie zu löschen.
