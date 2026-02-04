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
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 3%

---


# Herausforderungen und Aufgaben verwalten {#manage-challenges}

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

### Status herausfordern {#challenge-lifecycle}

Challenges durchlaufen verschiedene Status während ihres Lebenszyklus:

* **Entwurf**: Herausforderung wird erstellt oder bearbeitet und steht Kunden noch nicht zur Verfügung.
* **Veröffentlicht**: Herausforderung ist aktiv und die zugehörige Journey wurde erstellt.

### Herausforderungen bearbeiten {#edit-challenges}

Sie können Challenges bearbeiten, indem Sie sie im Challenges-Inventar öffnen. Das Bearbeitungsverhalten variiert je nach Challenge-Status:

**Entwurfsherausforderungen**: Sie haben vollständige Bearbeitungsfunktion. Alle Eigenschaften, Aufgaben, Inhalte und Nachrichten können ohne Einschränkungen geändert werden.

**Veröffentlichte Herausforderungen**: Wenn Sie eine veröffentlichte Herausforderung zur Bearbeitung öffnen, müssen Sie sie zunächst in den Entwurfsstatus zurücksetzen.

* Alle Anpassungen, die direkt an der automatisch generierten Journey vorgenommen werden, gehen verloren.
* Die Herausforderung kehrt zum Status Entwurf zurück.
* Nachdem Sie Ihre Änderungen vorgenommen haben, müssen Sie die Herausforderung speichern und erneut veröffentlichen.
* Sie müssen die zugehörige Journey erneut veröffentlichen, um die aktualisierte Challenge für Kunden verfügbar zu machen.

>[!IMPORTANT]
>
>Eine veröffentlichte Herausforderung kann nicht rückgängig gemacht werden. Berücksichtigen Sie die Auswirkungen auf Ihre aktive Journey, bevor Sie fortfahren.

### Herausforderungen duplizieren {#duplicate-challenges}

Durch das Duplizieren einer Challenge wird eine exakte Kopie mit allen Aufgaben, Inhalten und Nachrichten erstellt, sodass Sie schnell neue Versionen erstellen können, ohne von Grund auf neu zu beginnen.

So duplizieren Sie eine Herausforderung:

1. Navigieren Sie zur Registerkarte **[!UICONTROL Herausforderungen]** und suchen Sie die Herausforderung, die Sie duplizieren möchten.

1. Klicken Sie auf das ![](assets/do-not-localize/Smock_More_18_N.svg) neben dieser Herausforderung und wählen Sie **[!UICONTROL Duplizieren]**.

1. Eine Kopie der Challenge wird erstellt. Öffnen Sie die duplizierte Herausforderung und ändern Sie die erforderlichen Eigenschaften.

1. Speichern Sie die duplizierte Challenge und generieren Sie die zugehörige Journey.

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

Aufgaben sind wiederverwendbare Komponenten, die über mehrere Herausforderungen hinweg verwendet werden können. Die effektive Verwaltung von Aufgaben stellt die Konsistenz Ihres gesamten Treueprogramms sicher und erleichtert die zentrale Aktualisierung von Aufgabendefinitionen. Aufgaben, die in einer Challenge erstellt wurden, können in anderen Challenges wiederverwendet werden, wodurch Duplikate reduziert und die Standardisierung beibehalten wird.

### Aufgaben bearbeiten {#edit-tasks}

Sie können vorhandene Aufgaben im Aufgabeninventar bearbeiten. Beachten Sie Folgendes:

* **Aufgaben werden nicht in aktiven Herausforderungen verwendet**: Können frei bearbeitet werden. Alle Eigenschaften können ohne Auswirkungen geändert werden.
* **Aufgaben in Live-Herausforderungen**: Seien Sie vorsichtig, da sich Änderungen auf alle Herausforderungen auswirken, die die Aufgabe verwenden. Änderungen werden sofort auf alle referenzierenden Herausforderungen angewendet.

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

* Überprüfen Sie die Anzahl **[!UICONTROL Verwendet in Herausforderungen]** im Aufgabeninventar.
* Stellen Sie sicher, dass keine Entwurfs-, geplanten oder Live-Herausforderungen auf die Aufgabe verweisen.

So löschen Sie eine Aufgabe

1. Navigieren Sie zur **[!UICONTROL Aufgaben]** im Inventar „Herausforderungen im Treueprogramm“.

1. Suchen Sie die Aufgabe, die Sie löschen möchten.

1. Überprüfen Sie, **[!UICONTROL die]** „Wird in Herausforderungen verwendet“ 0 anzeigt. Wenn die Anzahl größer als 0 ist, müssen Sie die Aufgabe zunächst aus allen Herausforderungen entfernen, bevor Sie sie löschen.

1. Wählen Sie das ![](assets/do-not-localize/Smock_More_18_N.svg) neben der Aufgabe aus.

1. Wählen Sie **[!UICONTROL Löschen]**.

1. Bestätigen Sie den Löschvorgang im Dialogfeld.

>[!NOTE]
>
>Wenn eine Aufgabe in einer Herausforderung verwendet wird (Entwurf, geplant oder live), muss sie zunächst aus allen Herausforderungen entfernt werden, bevor sie gelöscht werden kann. Wenn Sie Aufgaben in Zukunft benötigen, sollten Sie sie archivieren oder duplizieren, anstatt sie zu löschen.
