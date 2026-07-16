---
title: Testen des benutzerdefinierten Kanals
description: Erfahren Sie, wie Sie vor der Aktivierung die Verbindung testen, Inhalte simulieren und Ihre benutzerdefinierten Kanalnachrichten in Adobe Journey Optimizer testen können.
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 2%

---


# Testen des benutzerdefinierten Kanals {#test-custom-channel}

Überprüfen Sie vor der Aktivierung einer Journey oder Kampagne, die einen benutzerdefinierten Kanal verwendet, ob Ihr Endpunkt erreichbar ist, die Authentifizierung funktioniert und ob Personalisierungs-Token für Ihre Zielprofile korrekt aufgelöst werden.

## Testen der Verbindung mit dem Channel Builder {#test-connection}

Wenn sich ein benutzerdefinierter Kanal im Status **[!UICONTROL Entwurf]** befindet, verwenden Sie die Schaltfläche **[!UICONTROL Test]** im Kanal Builder, um eine Testanfrage an Ihren Endpunkt zu senden und die End-to-End-Verbindung vor der Aktivierung zu validieren. [Weitere Informationen](create-custom-channel.md#test-connection)

Dieser Test bestätigt:

* Dass der Endpunkt von den ausgehenden IPs von [!DNL Journey Optimizer] erreichbar ist.
* Überprüfen Sie, ob die konfigurierten Authentifizierungsberechtigungen gültig sind.
* Dass der Endpunkt eine HTTP-2xx-Antwort zurückgibt.

Überprüfen Sie die Protokolle Ihres externen Systems, um sicherzustellen, dass die Testanfrage mit den erwarteten Kopfzeilen und der Payload-Struktur empfangen wurde.

## Simulieren von Inhalten mit Testprofilen {#simulate-content}

Die Funktion **[!UICONTROL Inhalt simulieren]** löst Personalisierungsausdrücke in Testprofilen auf, sodass Sie die genaue Payload überprüfen können, die gesendet werden würde, bevor eine echte Nachricht zugestellt wird.

1. Klicken Sie auf dem Bildschirm Journey-Aktion oder Kampagnenbearbeitung auf **[!UICONTROL Inhalt simulieren]**.

1. Klicken Sie **[!UICONTROL Testprofil hinzufügen]** und wählen Sie ein oder mehrere Profile aus. [Informationen zum Erstellen von Testprofilen](../audience/creating-test-profiles.md)

1. Überprüfen Sie die aufgelöste Payload im Bedienfeld „Vorschau“. Überprüfen Sie für jedes Testprofil Folgendes:

   * Alle Personalisierungs-Token (z. B. `{{profile.person.name.firstName}}`) wurden durch die erwarteten Werte aus dem Profil ersetzt.
   * Es verbleiben keine ungelösten Token (angezeigt als leere Zeichenfolgen oder literale `{{...}}`).
   * Erforderliche Payload-Felder werden ausgefüllt.
   * Helper-Funktionen erzeugen die erwartete formatierte Ausgabe.

>[!TIP]
>
>Testen Sie mit mehreren Profilen, die verschiedene Zielgruppensegmente darstellen, um Randfälle zu erfassen, z. B. Profile mit fehlenden optionalen Attributen, nicht lateinischen Zeichensätzen oder Nullwerten in personalisierten Feldern.

## Durchführen eines Testversands {#send-proof}

Um den End-to-End-Versand vor der Aktivierung zu validieren, senden Sie einen Testversand an eine Gruppe von Testempfängerinnen und Testempfängern:

1. Wechseln Sie im Bedienfeld **[!UICONTROL Inhalt simulieren]** zur Registerkarte **[!UICONTROL Testversand]**).

1. Fügen Sie die Profile hinzu, die Sie verwenden möchten. Sie können eine CSV-Datei mit Profilen hochladen, die nicht als Testprofile in [!DNL Journey Optimizer] definiert sind.

1. Klicken Sie auf **[!UICONTROL Testversand durchführen]**. [!DNL Journey Optimizer] ruft für jedes ausgewählte Profil Ihren externen Endpunkt mit der personalisierten Payload auf.

1. Überprüfen Sie Ihr externes System, um zu bestätigen, dass die Payloads für den Testversand empfangen wurden. Überprüfen Sie bei Messaging-Kanälen (z. B. WeChat oder Kakao Talk), ob die Nachricht auf dem Zielgerät oder in der Messaging-App angezeigt wird.

Das Ergebnis des Korrekturabzugs wird mit denselben Validierungsmustern wie das E-Mail-Proofing angezeigt: Pflichtfelder, nicht übereinstimmende Typen und Fehler bei der Schemavalidierung werden angezeigt, bevor der Korrekturabzug gesendet wird.

Erfahren Sie mehr über den Versand von Testsendungen [Kampagnen](../campaigns/create-campaign.md#send-proof) und [Journey](../building-journeys/testing-the-journey.md).

## Testen im Journey-Testmodus {#test-journey}

Für eine End-to-End-Journey-Validierung aktivieren Sie die Journey im **[!UICONTROL Testmodus]**:

1. Klicken Sie auf der Journey-Arbeitsfläche **[!UICONTROL Test]** im oberen rechten Bereich.

1. Konfigurieren Sie das Trigger-Ereignis oder wählen Sie ein Testprofil für eine zielgruppengesteuerte Journey aus.

1. Klicken Sie auf **[!UICONTROL Trigger eines Ereignisses]** oder lassen Sie das Profil über eine Aktivität vom Typ **[!UICONTROL Zielgruppe lesen]** eintreten.

1. Beobachten Sie den Fluss auf der Arbeitsfläche. Wenn ein Profil den benutzerdefinierten Kanalaktionsknoten erreicht, ruft [!DNL Journey Optimizer] Ihren externen Endpunkt mit der personalisierten Payload auf.

1. Überprüfen Sie die Protokolle Ihres externen Systems, um zu bestätigen, dass die Anfrage korrekt empfangen wurde.

1. Klicken Sie **[!UICONTROL Test anhalten]** wenn Sie fertig sind.

Erfahren Sie mehr über das Testen von Journey [Testmodus](../building-journeys/testing-the-journey.md).

## Journey simulieren {#simulate-journey}

Im **Simulationsmodus** von [!DNL Journey Optimizer] können Sie Ihr Journey End-to-End mit simulierten Benutzern validieren - temporäre profilähnliche Entitäten, die nicht in Adobe Experience Platform bestehen bleiben -, ohne dass vorab erstellte Testprofile erforderlich sind.

Bei benutzerdefinierten Kanälen löst die Simulation Personalisierungsausdrücke auf und rendert die Payload-Vorschau für jeden simulierten Benutzer, sodass Sie überprüfen können, ob der richtige Inhalt bereitgestellt wird, bevor Sie live gehen.

So simulieren Sie eine Journey mithilfe eines benutzerdefinierten Kanals:

1. Klicken Sie auf der Journey-Arbeitsfläche **[!UICONTROL Simulieren]** im oberen rechten Bereich.

1. Fügen Sie simulierte Benutzer manuell hinzu oder generieren Sie sie mithilfe der Option KI-**[!UICONTROL Schnellsimulation]** .

1. Konfigurieren Sie alle erforderlichen Eintrittsereignisse und erstellen Sie dann über die Journey einen Trigger für die simulierten Benutzenden.

1. Wenn ein simulierter Benutzer den benutzerdefinierten Kanalaktionsknoten erreicht, überprüfen Sie die aufgelöste Payload im Vorschaubereich, um sicherzustellen, dass Personalisierungs-Token und die Payload-Struktur korrekt sind.

>[!NOTE]
>
>Die Simulation ist sowohl für Entwurfs- als auch für Live-Journey verfügbar und verwendet temporäre simulierte Benutzende, die nicht auf Profilkontingente oder echte Endpunktaufrufe angerechnet werden.

[Weitere Informationen zur Journey-Simulation](../building-journeys/simulate-journey-gs.md)

## Checkliste für die Voraktivierung {#checklist}

Bevor Sie Ihren Journey oder Ihre Kampagne aktivieren, bestätigen Sie Folgendes:

* Der Verbindungstest aus dem Channel Builder war erfolgreich (Endpunkt erreichbar, Authentifizierung gültig).
* Simulierte Payloads zeigen erwartete Werte für alle Testprofile an.
* Es verbleiben keine ungelösten Personalisierungs-Token in der Payload.
* Alle erforderlichen Payload-Felder werden ausgefüllt.
* Ein Testversand wurde korrekt von Ihrem externen System gesendet und empfangen.
* Fehlerpfade in der Aktionsaktivität Journey (falls konfiguriert) verarbeiten Fehlerszenarien erwartungsgemäß.

Fahren Sie nach Abschluss des Tests mit der Aktivierung fort. [Weitere Informationen](create-custom-experience.md#activate)
