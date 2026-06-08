---
solution: Journey Optimizer
product: journey optimizer
title: Simulieren der Journey
description: Erfahren Sie, wie Sie Ihren Journey simulieren
feature: Journeys, Test Profiles
topic: Content Management
role: User
level: Intermediate
keywords: testen, Journey, prüfen, Fehler, Fehlerbehebung
version: Journey Orchestration
hide: true
feature_v2: []
subfeature_v2: []
source-git-commit: 951343a6695b12aa44ecfc5df3771da2b61b6471
workflow-type: tm+mt
source-wordcount: 1831
ht-degree: 1%

---

# Simulieren der Journey {#simulate-journey}

>[!IMPORTANT]
>
>Sie benötigen mindestens eine der folgenden Berechtigungen, um auf die Funktion **[!UICONTROL Simulation]** zuzugreifen: **Journey simulieren**, **Journey veröffentlichen** oder **Journey genehmigen und veröffentlichen**. [Weitere Informationen](../administration/permissions.md)

Verwenden Sie **[!UICONTROL Simulation]**, um Ihren Journey mit **simulierten Benutzern** vor der Veröffentlichung zu validieren. Diese Seite führt Sie durch **[!UICONTROL Schnellsimulation]** und **[!UICONTROL Manuelle Simulation]**, das Erstellen und Senden simulierter Benutzer, das Auslösen von Einzelereignissen, wenn Ihr Journey sie benötigt, und das **[!UICONTROL Ergebnisse]**-Protokoll.

Einen Überblick nach Journey-Typ finden Sie unter [Erste Schritte mit der Journey-Simulation](simulate-journey-gs.md).

## Simulationstypen {#simulation-types}

Nach der Aktivierung bieten Batch-Journey mit dem Eintrag Zielgruppe lesen zwei Möglichkeiten, eine Simulation auszuführen:

* **[!UICONTROL Schnellsimulation]** wird End-to-End mit generierten Benutzern, generierten Ereigniswerten und standardmäßigen Testeinstellungen ausgeführt, unterstützt durch die Journey Agent. Es ist eine schnelle Möglichkeit, ein Journey End-to-End mit minimalem Eingriff zu simulieren. Sobald Sie diese Option auswählen, startet die Schnellsimulation.

* **[!UICONTROL Manuelle Simulation]** ermöglicht die manuelle Ausführung einer Simulation Schritt für Schritt. Erstellen Sie simulierte Benutzende (manuell oder mit der Journey Agent), fügen Sie sie in die Journey ein, definieren Sie Ereignis-Payloads (manuell oder mit der Journey Agent) und überschreiben Sie Wartezeiten.

![Bedienfeld „Simulationseinstellungen“ mit den Optionen „Schnellsimulation“ und „Manuelle Simulation“ neben der Journey-Arbeitsfläche](assets/quick-simulation-1.png)

### Schnellsimulation {#quick-simulation}

Auf jedem Journey in **[!UICONTROL Simulation]**, **[!UICONTROL Schnellsimulation]** wird die Journey mit generierten Benutzerinnen und Benutzern, Ereigniswerten und vorausgefüllten Einstellungen ausgeführt.

1. Wählen Sie **[!UICONTROL Schnellsimulation]** aus.

1. Überprüfen Sie die Felder, die Adobe Journey Optimizer für den Durchlauf gesammelt hat. Klicken Sie **[!UICONTROL Werte aktualisieren]**, um Testeinstellungen und Ausführungsadressen zu ändern oder ohne Änderungen fortzufahren.

   Dieser Schritt wird nur angezeigt, wenn die Journey Waits oder Channels verwendet. Sie können alle Wartezeiten und Ausführungsadressen für simulierte Benutzer anpassen, z. B. indem Sie Ihre eigene E-Mail verwenden, damit Nachrichten aus der Ausführung in Ihren Posteingang gelangen.

   ![Dialogfeld „Schnellsimulation“ zum Schritt Sammeln von Informationen mit den Werten „Aktualisieren“ und zum nächsten Schritt](assets/quick-simulation-2.png)

1. Wenn Sie **[!UICONTROL Werte aktualisieren]** geöffnet haben, bearbeiten Sie die Einstellungen, z. B. die für Testsendungen verwendete Adresse, und bestätigen Sie dann, dass Sie die Simulation starten möchten.

   ![Schritt „Schnellsimulation - Werte aktualisieren“ mit den Feldern „Wartezeit überschreiben“ und „E-Mail-Adresse und Telefonnummer prüfen“](assets/quick-simulation-3.png)

1. Der Journey Agent generiert aus der Journey-Definition eine Reihe simulierter Benutzender.

   Bei Journey mit einem E-Mail-, SMS- oder Push-Knoten fordert Sie der Agent auf, die zu verwendende E-Mail-Adresse, Telefonnummer oder das Push-Token zu bestätigen. Simulierte Benutzer werden anhand dieser Werte generiert. Klicken Sie abschließend auf **[!UICONTROL Generieren]**.

1. Klicken Sie nach Abschluss des Durchgangs **[!UICONTROL Ergebnisse anzeigen]**, um Pfade, Fehler und aufgedeckte Verzweigungen zu überprüfen. Siehe [Ergebnisse anzeigen](#viewing-results).

   ![Schnellsimulation wurde mit allen erfolgreichen Schritten abgeschlossen und die Ergebnisse sind verfügbar](assets/quick-simulation-4.png)

Die Schnellsimulation unterstützt auch ereignisausgelöste Journey und Journey, die Ereignisaktivitäten enthalten. Ereigniswerte werden automatisch für jeden generierten simulierten Benutzer festgelegt und ausgelöst. Sobald ein Anwender die Journey betritt, wird jedes Ereignis ausgelöst, sobald er die entsprechende Wartezeit erreicht.

### Manuelle Simulation {#manual-simulation}

Wählen Sie **[!UICONTROL Manuelle Simulation]** aus, wenn Sie jeden simulierten Benutzer auswählen, die Versandreihenfolge steuern, Ereignis-Payloads konfigurieren und **[!UICONTROL Wartezeiten]** für die Ausführung überschreiben müssen.

Fahren Sie mit [Erstellen und Verwalten simulierter Benutzer](#test-users), [Trigger Ihrer Ereignisse](#firing-events) und [Ergebnisse anzeigen](#viewing-results) fort.

## Erstellen und Verwalten simulierter Benutzer {#test-users}

>[!IMPORTANT]
>
>Sie benötigen mindestens eine der folgenden Berechtigungen, um auf die Funktion **[!UICONTROL Simulation]** zuzugreifen: **Journey simulieren**, **Journey veröffentlichen** oder **Journey genehmigen und veröffentlichen**. [Weitere Informationen](../administration/permissions.md)

Simulierte Benutzer sind temporäre profilähnliche Entitäten, die Sie in &quot;**[!UICONTROL &quot;]**. In diesem Abschnitt wird beschrieben, wie Sie sie erstellen, zur Wiederverwendung speichern, anpassen oder aus der Liste entfernen und an die Journey senden.

1. Füllen Sie zunächst die Liste **[!UICONTROL Testbenutzer]** aus:

   +++ Benutzer mit KI generieren

   Adobe Journey Optimizer generiert aus der Journey-Definition eine Reihe simulierter Benutzender.

   Bei Journey mit einem E-Mail- oder SMS-Knoten fordert Sie die KI auf, die zu verwendende E-Mail-Adresse oder Telefonnummer zu bestätigen. Klicken Sie abschließend auf **[!UICONTROL Generieren]**.

   ![Dialogfeld „Simulierte Benutzer generieren“ mit den Feldern „Ausführungs-E-Mail“ und „Telefonnummer“ und „Generieren“](assets/simulate-generate.png)

   +++

   +++ Durchsuchen des Inventars

   Wählen Sie **[!UICONTROL Inventar durchsuchen]**, um bereits gespeicherte simulierte Benutzer hinzuzufügen, z. B. Benutzer, die Sie aus einem Formular oder JSON erstellt haben, oder Benutzer, die Sie nach einer Ausführung der KI-Generierung behalten haben.

   ![Dialogfeld „Simulierte Benutzerinventare“ mit der Schaltfläche „Suchen“, „Benutzertabelle“ und „Auswählen“](assets/simulate-inventory.png)

   +++

   +++ Aus Formular erstellen

   1. Geben Sie einen **[!UICONTROL Anzeigenamen]**, **[!UICONTROL Identity-Namespace]** und **[!UICONTROL Beschreibung]** ein, um diesen simulierten Benutzer zu identifizieren.

      ![Erstellen eines Formulars für simulierte Benutzer mit Anzeigenamen, Identity-Namespace, Beschreibung und Vereinigungsschemaattributen](assets/simulate-form.png)

   1. Wählen Sie dann die Attribute aus dem Vereinigungsschema aus, die Sie für diesen Benutzer ausfüllen möchten.

   1. Klicken Sie **[!UICONTROL Zielgruppenzugehörigkeit hinzufügen]** um Segmentzugehörigkeiten zu simulieren.

   1. Klicken Sie im Fenster **[!UICONTROL Simulierte Benutzer erstellen]** auf **[!UICONTROL Simulierten Benutzer hinzufügen]**, um mehrere simulierte Benutzer in einer Sitzung zu definieren.

      Sie können ändern, wie Benutzer in der Liste angezeigt werden, jede Karte in der gestapelten Ansicht ausblenden oder die Attributmetadaten eines Benutzers öffnen.

      ![Erstellen der Fußzeile für simulierte Benutzer mit den Steuerelementen „Simulierten Benutzer hinzufügen“, „Alle reduzieren“ und „Layout-Ansicht“](assets/simulate-form-3.png)

   1. Verwenden Sie im simulierten Benutzermenü **[!UICONTROL Duplizieren]** um einen Benutzer zu kopieren, **[!UICONTROL alle Attribute auf andere Benutzer anwenden]** um die Attribute eines Benutzers auf jeden anderen Benutzer in der Sitzung zu kopieren, oder **[!UICONTROL Löschen]** um einen Benutzer zu entfernen.

      ![Erstellen Sie simulierte Benutzerkarten mit Duplikaten, wenden Sie alle Attribute auf andere Benutzer an und löschen Sie sie bei jedem Benutzer](assets/simulate-form-2.png)

   1. Klicken Sie **[!UICONTROL Speichern]** wenn Sie die Konfiguration der Benutzer in dieser Sitzung abgeschlossen haben.

   +++

   +++ Aus JSON erstellen

   Definieren Sie neue simulierte Benutzer, indem Sie die entsprechenden Felder mit Ihren simulierten Benutzerdaten aktualisieren.

   ![Erstellen Sie den JSON-Editor für simulierte Benutzer mit der Benutzervorlage und dem JSON-Steuerelement „Format“](assets/simulate-json.png)

   +++

1. Die von Ihnen erstellten simulierten Benutzer werden in der Liste **[!UICONTROL Testbenutzer]** angezeigt. Wählen Sie für jeden Eintrag eine der folgenden Optionen aus:

   * ![Bearbeiten-Symbol](assets/do-not-localize/Smock_Edit_18_N.svg): Aktualisieren Sie die Details des simulierten Benutzers.
   * ![Senden-Symbol](assets/do-not-localize/Smock_Send_18_N.svg): Führen Sie die Simulation nur für diesen simulierten Benutzer aus.

     Diese Option ist nicht für Journey verfügbar, die mit einem Ereignis beginnen, da der simulierte Benutzereintritt durch das gesendete Ereignis ausgelöst wird. [Weitere Informationen](#firing-events)

   * ![Symbol entfernen](assets/do-not-localize/Smock_Close_18_N.svg): Entfernen Sie den Benutzer aus dieser Liste. Der simulierte Benutzer wird nicht gelöscht und bleibt in der Auswahl Simulierte Benutzer verfügbar.

   ![Benutzerliste mit auf der Arbeitsfläche hervorgehobenen Aktionen „Bearbeiten“, „Senden“ und „Entfernen“ sowie dem simulierten Pfad testen](assets/simulate-4-2.png)

1. Um die Liste nach Ihrer Auswahl zu ändern, klicken Sie auf **[!UICONTROL Benutzer verwalten]**, um weitere simulierte Benutzer aus dem Inventar oder durch Erstellen neuer hinzuzufügen. Um jeden Benutzer für diese Ausführung aus der Liste **[!UICONTROL Benutzer testen]** zu entfernen, wählen Sie **[!UICONTROL Alle Benutzer löschen]**.

   ![Menü „Benutzer verwalten“ mit Optionen für zusätzliche Benutzer öffnen und „Alle Benutzer löschen“](assets/simulate-manage.png)

1. Wenn Ihr Journey eine Aktivität **[!UICONTROL Warten]** enthält, öffnen Sie die Registerkarte **[!UICONTROL Testeinstellungen]**, um die Dauer dieser Wartezeit während der Simulation genau abzustimmen. Wenn die Live-Aktivität **[!UICONTROL Warten]** beispielsweise für mehrere Tage konfiguriert ist, können Sie sie auf 10 Sekunden überschreiben, sodass der simulierte Benutzer nur diese Zeit auf dem Knoten verbringt, bevor er zur nächsten Aktivität wechselt.

1. Klicken Sie auf **[!UICONTROL Alle senden]**, um jeden simulierten Benutzer in der Liste auf die Journey zu senden, oder klicken Sie ![Senden-Symbol](assets/do-not-localize/Smock_Send_18_N.svg) in einer Zeile, um nur diesen Benutzer zu senden. Wenn die simulierten Benutzenden die Journey erfolgreich betreten haben, wird eine `Simulated users have entered the journey successfully.`-Bestätigungsmeldung angezeigt.

   ![Registerkarte „Testen von Benutzern“, nachdem Benutzer die Journey mit Erfolgsmeldung und Pfad auf der Arbeitsfläche eingegeben haben](assets/simulate-5-2.png)

1. Wenn die Journey unitäre Ereignisse enthält, müssen Sie das Ereignis zum Trigger auswählen. Siehe [Trigger Ihrer Ereignisse](#firing-events).

1. Rufen Sie die **[!UICONTROL Ergebnisse]** auf, um das Ausführungsprotokoll zu öffnen und die Ausführung der einzelnen Schritte zu überprüfen. Weitere Informationen finden Sie unter [Ergebnisse anzeigen](#viewing-results).

1. Öffnen Sie nach Abschluss des Tests das Menü **[!UICONTROL Simulation verwalten]**:

   * **[!UICONTROL Simulation schließen]**, um die aktuelle Simulationssitzung zu beenden.
   * **[!UICONTROL Simulation zurücksetzen]** um alle Daten aus dem aktuellen Durchgang, ausgewählten simulierten Benutzern, definierten Ereigniswerten und anderen Testeinstellungen zu löschen, damit Sie eine neue Simulation von Grund auf neu starten können.

     ![Menü Simulation verwalten mit den Optionen Simulation zurücksetzen und Simulation schließen öffnen](assets/simulate-15.png)

Nachdem Sie die Journey in **[!UICONTROL Simulation]** validiert haben, überprüfen Sie das **[!UICONTROL Ergebnisse]**-Protokoll. Wenn Fehler auftreten, lassen Sie **[!UICONTROL Simulation]**, wenden Sie die erforderlichen Änderungen auf die Journey an und führen Sie **[!UICONTROL Simulation]** erneut aus, bis der Durchlauf korrekt aussieht. Sie können dann die Journey veröffentlichen. Siehe [Veröffentlichen des Journey](../building-journeys/publish-journey.md).

## Auslösen Ihrer Ereignisse {#firing-events}

Wenn Ihr Journey ein oder mehrere unitäre Ereignisse enthält, können Sie diese mit einem Trigger versehen, während die Simulation aktiv ist. Für Journey, die nicht mit einem Ereignis beginnen, aber eines beinhalten, wird dieser Abschnitt erst angezeigt, wenn ein simulierter Benutzer auf die Journey zugreift.

1. Wählen **[!UICONTROL unter „Ereignistyp]**&quot; das Ereignis aus, das für diese Simulation ausgelöst werden soll.

   ![Wählen Sie das Dropdown-Menü Ereignistyp aus, das im Abschnitt Testereignisse der Simulationseinstellungen geöffnet ist](assets/simulate-10-2.png)

1. Um dieselbe Änderung auf alle Benutzenden in der Liste anzuwenden, verwenden Sie die Option **[!UICONTROL Ereignisse verwalten]** für:

   * **[!UICONTROL Ereigniswerte generieren]** damit die Journey Agent alle Payloads mithilfe von KI generieren kann. Wenn Werte generiert werden, wird der Benutzer als **[!UICONTROL Bereit zum Senden]** markiert.
   * **[!UICONTROL Ereignisdaten bearbeiten]**, um die Payload für jeden simulierten Benutzer in der Liste zu ändern.

   ![Menü „Ereignisse verwalten“ in „Testereignisse mit den Optionen „Mit KI generieren“ und „Alle bearbeiten“](assets/simulate-9-2.png)

1. Konfigurieren Sie die Ereignis-Payload für jeden Benutzer, indem Sie auf das ![Ereignis bearbeiten](assets/do-not-localize/Smock_Edit_18_N.svg) neben einem Benutzer klicken, um:

   * **[!UICONTROL Ereigniswerte generieren]** damit die Journey Agent die Payload mithilfe von KI generieren kann. Wenn Werte generiert werden, wird der Benutzer als **[!UICONTROL Bereit zum Senden]** markiert.
   * **[!UICONTROL Ereignisdaten bearbeiten]**, um die Payload nur für diesen simulierten Benutzer zu ändern.

   ![Menü pro Benutzer in Testereignissen mit den Optionen Ereigniswerte generieren und Ereignisdaten bearbeiten](assets/simulate-8-2.png)

1. Wählen Sie **[!UICONTROL Testereignisse]** entweder die Option **[!UICONTROL Alle senden]**, um dieses Ereignis für alle simulierten Benutzer zu senden, die unter **[!UICONTROL Testbenutzer]** aufgeführt sind, oder wählen Sie ![Senden-Symbol](assets/do-not-localize/Smock_Send_18_N.svg), damit ein einzelnes Ereignis nur für diesen Benutzer ausgelöst wird.

   ![Testen von Ereignissen mit den Steuerelementen „Alle senden“ und „Pro Benutzer senden“ für als bereit markierte Benutzer](assets/simulate-11-2.png)

1. Nachdem Ereignisse ausgelöst wurden, wird die Arbeitsfläche aktualisiert, um den Fortschritt jedes Benutzers widerzuspiegeln.

1. Rufen Sie die **[!UICONTROL Ergebnisse]** auf, um das Ausführungsprotokoll zu öffnen und die Ausführung der einzelnen Schritte zu überprüfen. Weitere Informationen finden Sie unter [Ergebnisse anzeigen](#viewing-results).

1. Öffnen Sie nach Abschluss des Tests das Menü **[!UICONTROL Simulation verwalten]**:

   * **[!UICONTROL Simulation schließen]**, um die aktuelle Simulationssitzung zu beenden.
   * **[!UICONTROL Simulation zurücksetzen]** um alle Daten aus dem aktuellen Durchgang, ausgewählten simulierten Benutzern, definierten Ereigniswerten und anderen Testeinstellungen zu löschen, damit Sie eine neue Simulation von Grund auf neu starten können.

     ![Menü Simulation verwalten mit den Optionen Simulation zurücksetzen und Simulation schließen öffnen](assets/simulate-15.png)

## Anzeigen von Ergebnissen {#viewing-results}

Auf **[!UICONTROL Registerkarte]** Ergebnisse“ können Sie die Testergebnisse anzeigen. Wählen **[!UICONTROL in der Dropdown]** Liste Testbenutzer den simulierten Benutzer aus, dessen Ausführung Sie überprüfen möchten.

Wählen Sie **[!UICONTROL Alle]** aus, um die Ergebnisse für jeden simulierten Benutzer in der Ausführung aggregiert anzuzeigen. In dieser Ansicht können Sie die gesamte Simulation auf einen Blick scannen, einschließlich Aktivitäten, Ergebnisse und Fehler, ohne zuerst einen einzelnen simulierten Benutzer auszuwählen.

![Registerkarte „Ergebnisse“ mit Simulationszusammenfassung, Testbenutzerfilter und Pfadabdeckung auf der Journey-Arbeitsfläche](assets/simulate-6-2.png)

Für jede Aktivität kann das Protokoll anzeigen, ob der simulierte Benutzer in den Schritt eingetreten ist oder ihn verlassen hat, sowie auf Fehler, die während der Simulation aufgetreten sind.

Bei **Warten**-Aktivitäten enthält das Protokoll zwei durationsbezogene Werte:

* **Definierte Dauer**: Die Dauer, die auf der Aktivität **Warten** für die veröffentlichte Journey angegeben und angewendet wird, sobald die Journey live ist. Im Protokoll wird aufgezeichnet, ob Simulation eine Überschreibung aus den Testeinstellungen vornimmt (z. B. 10 Sekunden), anstatt sich ausschließlich auf den auf der Journey definierten Wert zu verlassen.
* **Tatsächliche Dauer**: Die verstrichene Zeit, die der simulierte Benutzer auf der **Warten**-Aktivität verblieb. Dieser Wert wird auf der Registerkarte **[!UICONTROL Testeinstellungen]** festgelegt.

Wenn Fehler im Protokoll angezeigt werden, verlassen Sie **Simulation**, wenden Sie die erforderlichen Änderungen an der Journey an und führen Sie **Simulation** erneut aus. Nach erfolgreicher Validierung veröffentlichen Sie die Journey. Siehe [Veröffentlichen des Journey](../building-journeys/publish-journey.md).
