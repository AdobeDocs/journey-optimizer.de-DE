---
title: Senden von E-Mail-Testsendungen
description: Erfahren Sie, wie Sie E-Mail-Testsendungen versenden.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
feature_v2: []
subfeature_v2:
  - id: a5683ded-e5d5-4ec6-b9fd-e1b56a94ab96
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 464
ht-degree: 98%

---

# Durchführen von Testsendungen mit Testprofildaten {#send-proofs}

Ein Testversand dient der Validierung einer Nachricht, bevor sie an die wichtigste Zielgruppe gesendet wird. Die Empfänger des Testversands sind für die Überprüfung der Nachricht verantwortlich: Darstellung, Inhalt, Personalisierungseinstellungen, Konfiguration.

>[!NOTE]
>
>Mit [!DNL Journey Optimizer] können Sie verschiedene Varianten Ihrer Inhalte testen, indem Sie sie in der Vorschau anzeigen und einen Testversand mit Beispieleingabedaten durchführen, die aus einer CSV- oder JSON-Datei hochgeladen oder manuell hinzugefügt wurden. [Informationen zum Simulieren von Inhaltsvarianten](../test-approve/simulate-sample-input.md)

## Wichtige Informationen {#must-read}

**Regeln zur Frequenzbegrenzung** – Alle vorhandenen Regeln zur Frequenzbegrenzung gelten für Testsendungen. Wenn Sie [Regeln zur Frequenzbegrenzung](../conflict-prioritization/channel-capping.md) festgelegt haben (z. B. maximale Sendungen pro Profil), gelten diese Einschränkungen auch für den Versand von Testsendungen. Wenn ein Testprofil bereits das Limit der Frequenzbegrenzung erreicht hat, werden die Testsendungen als abgeschlossen angezeigt, es wird jedoch keine E-Mail gesendet. Für wiederholte Tests sollten Sie bei Bedarf eindeutige Testprofile verwenden oder Frequenzbegrenzungen für Testversandszenarien anpassen.

**Mirror-Seite** – Bei Testsendungen ist der Link zur Mirror-Seite nicht aktiv. Er wird erst in den endgültigen Nachrichten aktiviert.

**Assets** – Für Assets und Bilder gelten bestimmte Barrierefreiheitsregeln:

* Assets/Bilder sind in bereitgestellten Inhalten oder Testversandinhalten für bis zu 2 Jahre (730 Tage) ab ihrer ersten Veröffentlichung in einem Fragment/einer Inline-Nachricht verfügbar.
* Nach Ablauf dieses Zeitraums (nach 730 Tagen) ist eine erneute Veröffentlichung erforderlich, um sie für weitere 2 Jahre verfügbar zu machen.
* Eine erneute Veröffentlichung innerhalb von 730 Tagen nach der ersten Veröffentlichung verlängert den Ablauf der Assets/Bilder nicht um weitere 730 Tage.

## Durchführen von Testsendungen {#send-proofs-steps}

Um E-Mail-Testsendungen mithilfe von Testprofildaten durchzuführen, müssen Sie zunächst [Testprofile](test-profiles.md) auswählen. Gehen Sie dann wie folgt vor:

1. Klicken Sie im Bildschirm **[!UICONTROL Simulieren]** auf die Schaltfläche **[!UICONTROL Testversand senden]**.

   ![Schaltfläche „Testversand senden“ im Bildschirm „Simulieren“](../email/assets/send-proof-button.png)

1. Geben Sie im Fenster **[!UICONTROL Testversand senden]** die Empfänger-E-Mail-Adresse ein und klicken Sie auf **[!UICONTROL Hinzufügen]**, um den Testversand an sich selbst oder Mitglieder Ihrer Organisation zu senden.

   Beachten Sie, dass Sie bis zu zehn Empfangende für Ihren Testversand hinzufügen können.

   ![Hinzufügen von Empfangenden zum Testversand](../email/assets/send-proof-add.png)

1. Wählen Sie die **Testprofile** aus, die zur Personalisierung des Nachrichteninhalts verwendet werden.

   Die Anzahl der Testversandnachrichten, die jede Person erhält, entspricht der Anzahl der ausgewählten Testprofile. Wenn Sie beispielsweise fünf Empfänger-E-Mails hinzugefügt und zehn Testprofile ausgewählt haben, senden Sie fünfzig Testversandnachrichten. Jede Empfängerin bzw. jeder Empfänger erhält zehn davon.

1. Bei Bedarf können Sie der Betreffzeile des Testversands ein Präfix hinzufügen. Nur alphanumerische Zeichen und Sonderzeichen, wie z. B. . - _ ( ) [ ], sind als Präfix für die Betreffzeile zulässig.

1. Klicken Sie auf **[!UICONTROL Testversand durchführen]**.

   ![Auswählen von Testprofilen und Durchführen des Testversands](../email/assets/send-proof-select.png)

1. Um den Status zu prüfen, klicken Sie im Bildschirm **[!UICONTROL Simulieren]** auf die Schaltfläche **[!UICONTROL Testsendungen anzeigen]**.

   ![Schaltfläche „Testsendungen anzeigen“ zur Überprüfung des Versandstatus](../email/assets/send-proof-view.png)

Es wird empfohlen, nach jeder Änderung am Nachrichteninhalt Testsendungen durchzuführen.
