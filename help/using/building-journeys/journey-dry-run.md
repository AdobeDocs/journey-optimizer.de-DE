---
solution: Journey Optimizer
product: journey optimizer
title: Journey-Probelauf
description: Erfahren Sie, wie Sie eine Journey im Probelauf-Modus veröffentlichen
feature: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
keywords: veröffentlichen, Journey, live, Gültigkeit, prüfen
exl-id: 58bcc8b8-5828-4ceb-9d34-8add9802b19d
source-git-commit: f308668ba1b7b20f6144e9200328e54986f66103
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 11%

---

# Journey-Probelauf {#journey-dry-run}

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="Probelauf-Modus"
>abstract="Diese Journey befindet sich im Probelauf. Journey Dry Run ist ein spezieller Journey-Veröffentlichungsmodus in Adobe Journey Optimizer, der es Journey-Anwendern ermöglicht, eine Journey mit echten Produktionsdaten zu testen, ohne echte Kunden zu kontaktieren oder Profilinformationen zu aktualisieren.  Mit dieser Funktion können Journey-Anwender Vertrauen in ihr Journey-Design und die Zielgruppenbestimmung gewinnen, bevor sie es live veröffentlichen."


>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run_start"
>title="Veröffentlichen einer Journey im Probelauf-Modus"
>abstract="Journey Dry Run ist ein spezieller Journey-Veröffentlichungsmodus in Adobe Journey Optimizer, der es Journey-Anwendern ermöglicht, eine Journey mit echten Produktionsdaten zu testen. Nachdem Sie Ihre Journey entworfen haben, führen Sie einen Probelauf aus, um deren Funktionalität zu bestätigen und sicherzustellen, dass die Schritte korrekt sind. In diesem Veröffentlichungsmodus können Sie eine Journey testen, ohne Mitteilungen an ein Profil zu senden."

Journey Dry Run ist ein spezieller Journey-Veröffentlichungsmodus in Adobe Journey Optimizer, der es Journey-Anwendern ermöglicht, eine Journey mit echten Produktionsdaten zu testen, ohne echte Kunden zu kontaktieren oder Profilinformationen zu aktualisieren.  Mit dieser Funktion können Journey-Anwender Vertrauen in ihr Journey-Design und die Zielgruppenbestimmung gewinnen, bevor sie es live veröffentlichen.


>[!AVAILABILITY]
>
>Diese Funktion ist nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit) und wird in einer zukünftigen Version global eingeführt.


## Wichtigste Vorteile {#journey-dry-run-benefits}

Journey Dry Run steigert das Vertrauen der Anwender und den Journey-Erfolg, indem es sicheres, datengesteuertes Testen von Journey-Kunden ermöglicht, die echte Produktionsdaten verwenden - ohne das Risiko, Kunden zu kontaktieren oder Profilinformationen zu ändern. Mit dieser Funktion können Journey-Anwender die Reichweite ihrer Zielgruppe und die Verzweigungslogik vor der Live-Schaltung überprüfen und so sicherstellen, dass die Journey ihren beabsichtigten Geschäftszielen entsprechen.

Mit Journey Dry Run können Sie Probleme frühzeitig identifizieren, Zielgruppenbestimmungsstrategien optimieren und das Journey-Design basierend auf tatsächlichen Daten - und nicht auf Annahmen - verbessern. Dry Run ist direkt in die Journey-Arbeitsfläche integriert und bietet intuitive Berichte und Einblicke in wichtige Leistungsindikatoren, sodass Teams sicher iterieren und Genehmigungs-Workflows optimieren können. Dies erhöht die betriebliche Effizienz, verringert das Launch-Risiko und steigert die Kundeninteraktion.

Diese Funktion verbessert letztendlich die Time-to-Value und reduziert Journey-Fehler.

Journey Dry Run bringt:

1. **Sichere Testumgebung**: Profile im Probelauf-Modus werden nicht kontaktiert, sodass kein Risiko besteht, dass Nachrichten gesendet werden oder Live-Daten beeinträchtigt werden.
1. **Zielgruppeneinblicke**: Journey-Anwender können die Erreichbarkeit der Zielgruppe auf verschiedenen Journey-Knoten vorhersagen, einschließlich Opt-outs, Ausschlüssen und anderer Bedingungen.
1. **Echtzeit-Feedback**: Metriken werden direkt auf der Journey-Arbeitsfläche angezeigt, ähnlich wie bei Live-Berichten, sodass Journey-Anwendende ihr Journey-Design verfeinern können.


>[!CAUTION]
>
>* Die Berechtigungen zum Starten des Probelaufs sind auf Benutzer mit der Berechtigung **[!DNL Publish journeys]** hoher Ebene beschränkt. Die Berechtigungen zum Stoppen des Probelaufs sind auf Benutzer mit der Berechtigung **[!DNL Manage journeys]** hoher Ebene beschränkt. Weitere Informationen zur Verwaltung der Zugriffsrechte für [!DNL Journey Optimizer]-Benutzende finden Sie in [diesem Abschnitt](../administration/permissions-overview.md).
>
>* Bevor Sie mit der Verwendung der Dry-Run-Funktion beginnen[ lesen Sie die Leitplanken und Einschränkungen ](#journey-dry-run-limitations).


## Probelauf starten {#journey-dry-run-start}

Sie können die Probelauf-Funktion in jeder Entwurfs-Journey fehlerfrei verwenden.

Gehen Sie wie folgt vor, um Probelauf zu aktivieren:

1. Öffnen Sie die Journey, die Sie testen möchten.
1. Klicken Sie auf die Schaltfläche **Probelauf**.

   ![Starten Sie den Journey-Probelauf](assets/dry-run-button.png)

1. Bestätigen Sie die Veröffentlichung.

   Während der Transition wird die Statusmeldung **Probelauf aktivieren** angezeigt.

1. Nach der Aktivierung wechselt die Journey in den **Dry Run**-Modus.

## Überwachen eines Probelaufs {#journey-dry-monitor}

Sobald die Veröffentlichung im Trockenmodus gestartet wurde, können Sie die Journey-Ausführung und den Fortschritt der Profile in den Journey-Verzweigungen und -Knoten visualisieren.

Metriken werden direkt auf der Journey-Arbeitsfläche angezeigt.

![Überwachen der Journey-Probelauf-Ausführung](assets/dry-run-metrics.png)

Für jede Aktivität können Sie Folgendes überprüfen:

* **[!UICONTROL Eingetreten]**: Gesamtzahl der Kontakte, die in diese Aktivität eingetreten sind.
* **[!UICONTROL Ausgestiegen (erfüllte die Ausstiegskriterien)]**: Gesamtzahl der Kontakte, die aufgrund eines Ausstiegskriteriums die Journey aus dieser Aktivität verlassen haben.
* **[!UICONTROL Exited (Forced Exit)]**: Gesamtzahl der Personen, die die Journey verlassen haben, während sie aufgrund einer Journey-Practitioner-Konfiguration angehalten wurde. Diese Metrik ist für Journey im Probelauf-Modus immer gleich null.
* **[!UICONTROL Fehler]**: Gesamtzahl der Kontakte, bei denen während dieser Aktivität ein Fehler aufgetreten ist.


Auf Journey-Ebene können Sie Folgendes überprüfen:

* Die Gesamtzahl der **Eingetretenen Profile**
* Die Gesamtzahl der **Ausgestiegenen Profile**
* Die Gesamtzahl der **fehlerhaften Profile**
* Die Gesamtzahl der **verworfenen Profile** im Journey

Sie können auch auf die Berichte **Letzte 24-Stunden** und **Alle-Zeit** für den Probelauf zugreifen. Um auf diese Berichte zuzugreifen, klicken **auf die Schaltfläche** Bericht anzeigen“ oben rechts auf der Journey-Arbeitsfläche.

![Auf die Berichte für die Journey-Probelauf-Ausführung zugreifen](assets/dry-run-report.png)

>[!CAUTION]
>
> Berichtsdaten sind nur verfügbar, wenn der Probelauf **aktiv** ist.  Nach dem Stoppen sind die Berichtsdaten nicht mehr zugänglich. Verwenden Sie die Schaltfläche **Exportieren** oberhalb der Berichte, um sie bei Bedarf herunterzuladen.


## Probelauf stoppen {#journey-dry-run-stop}

Dry Run Journey **muss** manuell angehalten werden.

Klicken Sie auf **Schließen**, um den Test zu beenden, und klicken Sie zur Bestätigung **Zurück** Entwurf.

<!-- After 14 days, Dry run journeys automatically transition to the **Draft** status.-->

## Schutzmechanismen und Einschränkungen {#journey-dry-run-limitations}

* Der Dry Run-Modus ist nicht für Journey verfügbar, die Reaktionsereignisse enthalten.
* Profile im Dry-Run-Modus werden als ansprechbare Profile gezählt.
* Dry Run-Journey wirken sich nicht auf Geschäftsregeln aus.
* Wenn beim Erstellen einer neuen Journey-Version eine vorherige Journey-Version **Live** ist, ist die Probelauf-Aktivierung in der neuen Version nicht zulässig.
* Journey Dry Run generiert stepEvents. Diese stepEvents haben ein bestimmtes Flag und eine Probelauf-ID:
   * `_experience.journeyOrchestration.stepEvents.inDryRun` gibt `true` zurück, wenn der Probelauf aktiviert ist, `false` andernfalls
   * `_experience.journeyOrchestration.stepEvents.dryRunID` gibt die ID einer Probelauf-Instanz zurück
* Während des Probelaufs wird die Journey mit den folgenden Besonderheiten ausgeführt:

   * **Kanalaktion** Knoten wie E-Mail, SMS oder Push-Benachrichtigungen werden nicht ausgeführt.
   * **Benutzerdefinierte Aktionen** werden während des Probelaufs deaktiviert und ihre Antworten sind auf null festgelegt.
   * **Warteknoten** werden während des Probelaufs umgangen.
     <!--You can override the wait block timeouts, then if you have wait blocks duration longer than allowed dry run journey duration, then that branch will not execute completely.-->
   * **Datenquellen** einschließlich externer Datenquellen, werden standardmäßig ausgeführt.