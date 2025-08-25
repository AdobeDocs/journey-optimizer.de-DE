---
title: Senden von E-Mail-Testsendungen
description: Erfahren Sie, wie Sie E-Mail-Testsendungen versenden.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
source-git-commit: aa28d13b2ad874e4dc61510bfdc250415e8e8be1
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 100%

---

# Durchführen von Testsendungen mit Testprofildaten {#send-proofs}

Ein Testversand dient der Validierung einer Nachricht, bevor sie an die wichtigste Zielgruppe gesendet wird. Die Empfänger des Testversands sind für die Überprüfung der Nachricht verantwortlich: Darstellung, Inhalt, Personalisierungseinstellungen, Konfiguration.

>[!NOTE]
>
>Mit [!DNL Journey optimizer] können Sie verschiedene Varianten Ihrer Inhalte testen, indem Sie sie in der Vorschau anzeigen und einen Testversand mit Beispieleingabedaten durchführen, die aus einer CSV- oder JSON-Datei hochgeladen oder manuell hinzugefügt wurden. [Informationen zum Simulieren von Inhaltsvarianten](../test-approve/simulate-sample-input.md)

Um E-Mail-Testsendungen mithilfe von Testprofildaten durchzuführen, müssen Sie zunächst [Testprofile](test-profiles.md) auswählen. Gehen Sie dann wie folgt vor:

1. Klicken Sie im Bildschirm **[!UICONTROL Simulieren]** auf die Schaltfläche **[!UICONTROL Testversand durchführen]**.

   ![](../email/assets/send-proof-button.png)

1. Geben Sie im Fenster **[!UICONTROL Testversand starten]** die E-Mail-Adresse Ihres Empfängers ein und klicken Sie auf **[!UICONTROL Hinzufügen]**, um den Testversand an sich selbst oder Mitglieder Ihrer Organisation zu senden.

   Beachten Sie, dass Sie bis zu zehn Empfänger für Ihren Testversand hinzufügen können.

   ![](../email/assets/send-proof-add.png)

1. Wählen Sie die **Testprofile** aus, die zur Personalisierung des Nachrichteninhalts verwendet werden.

   Die Anzahl der Testversandnachrichten, die jede Person erhält, entspricht der Anzahl der ausgewählten Testprofile. Wenn Sie beispielsweise fünf Empfänger-E-Mails hinzugefügt und zehn Testprofile ausgewählt haben, senden Sie fünfzig Testversandnachrichten, von denen jeder Empfänger zehn erhält.

1. Bei Bedarf können Sie der Betreffzeile des Testversands ein Präfix hinzufügen. Nur alphanumerische Zeichen und Sonderzeichen, wie etwa . - _ ( ) [ ], sind als Präfix für die Betreffzeile zulässig.

1. Klicken Sie auf **[!UICONTROL Testversand durchführen]**.

   ![](../email/assets/send-proof-select.png)

1. Um den Status zu prüfen, klicken Sie im Bildschirm **[!UICONTROL Simulieren]** auf die Schaltfläche **[!UICONTROL Testsendungen anzeigen]**.

   ![](../email/assets/send-proof-view.png)

Es wird empfohlen, nach jeder Änderung am Nachrichteninhalt Testsendungen durchzuführen.

>[!NOTE]
>
>Bei Testsendungen ist der Link zur Mirrorseite nicht aktiv. Er wird erst in den endgültigen Nachrichten aktiviert.
